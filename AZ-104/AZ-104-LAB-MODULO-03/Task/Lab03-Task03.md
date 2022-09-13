<h2>Lab 03 - Manage Azure Resources with PowerShell</h2> 

<h3>Lab scenario:</h3> 

Agora que você explorou os recursos básicos de administração do Azure associados ao provisionamento de recursos e organizou-os com base em grupos de recursos usando o portal do Azure e os modelos do Azure Resource Manager, deseja as tarefas equivalentes com o Azure Power Shell. Para evitar a instalação dos módulos do Azure PowerShell, você aproveitará o Azure Cloud Shell. 

<h3>Objetivos:</h3> 

<table border="1">    
  <tr>
    <th colspan="1">Tarefa 1:</th>  	              
    <th colspan="2">Instalar Azure PowerShell localmente e conectar na sua subscrição do Azure.</th>
  </tr>
<td>Tarefa 2:</td>
    <td>Criar um Resource Group, uma VNET e uma Subnet.</td>
  </tr>
  <tr>
    <td>Tarefa 3:</td>
    <td>Iniciar uma sessão do PowerShell no Cloud Shell do Azure e criar uma VM.</td>
  </tr>
 </table>
 
 <h3>Task 3:	Iniciar uma sessão do PowerShell no Cloud Shell do Azure e criar uma VM.</h3>



#Variables for common values
- $resourceGroup = "RG-LAB-03"
- $location = "eastus2"
- $vmName = "VM-PS01"
- $vnet = "VNET-03"
- $subnet = "SUB-LAN"

#Create user object
- $cred = Get-Credential -Message "Enter a username and password for the virtual machine."

#Create a public IP address and specify a DNS name
- $pip = New-AzPublicIpAddress -ResourceGroupName $resourceGroup -Location $location `
  -Name "VMPSIPPUB" -AllocationMethod Dynamic

#Create an inbound network security group rule for port 3389
- $nsgRuleRDP = New-AzNetworkSecurityRuleConfig -Name AllowRDP  -Protocol Tcp `
-   -Direction Inbound -Priority 1000 -SourceAddressPrefix * -SourcePortRange * -DestinationAddressPrefix * `
-   -DestinationPortRange 3389 -Access Allow

#Create a network security group
- $nsg = New-AzNetworkSecurityGroup -ResourceGroupName $resourceGroup -Location $location `
-   -Name "VM-PS01-NSG" -SecurityRules $nsgRuleRDP
  
#Get the subnet details for the specified virtual network + subnet combination.
- $azureVnetSubnet = (Get-AzVirtualNetwork -Name $vnet -ResourceGroupName $resourceGroup).Subnets | Where-Object {$_.Name -eq $subnet}  

#Create a virtual network card and associate with public IP address and NSG
- $nic = New-AzNetworkInterface -Name "VMPS01Nic" -ResourceGroupName $resourceGroup -Location $location `
-   -SubnetId $azureVnetSubnet.Id -PublicIpAddressId $pip.Id -NetworkSecurityGroupId $nsg.Id
  
#Create a virtual machine configuration
- $vmConfig = New-AzVMConfig -VMName $vmName -VMSize Standard_B2S | `
- Set-AzVMOperatingSystem -Windows -ComputerName $vmName -Credential $cred | `
- Set-AzVMSourceImage -PublisherName MicrosoftWindowsServer -Offer WindowsServer -Skus 2019-Datacenter -Version latest | `
- Add-AzVMNetworkInterface -Id $nic.Id

#Create a virtual machine
- New-AzVM -ResourceGroupName $resourceGroup -Location $location -VM $vmConfig
