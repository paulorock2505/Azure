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

 <table border="1">    
  <tr>
    <th>Virtual Machine</th> 
</table>

<table border="1">    
  <tr>
    <th colspan="1">Setting</th>  	              
    <th colspan="2">Value</th>
  </tr>
<td>Resource Group</td>
    <td>RG-LAB-03</td>
  </tr>
  <tr>
    <td>Region </td>
    <td>East US 2</td>
  </tr>
   <tr>
    <td>Name</td>
    <td>VM-PS01</td>
  </tr>
   <tr>
    <td>Image</td>
    <td>Windows Server 2019</td>
  </tr>
   <tr>
    <td>Size</td>
    <td>B2s</td>
  </tr>
 </table>
 
Acesse o cloudshell dentro do portal do Azure: 

![image](https://user-images.githubusercontent.com/107069287/189972215-0bb5c950-5339-4c42-b390-a3ba95d60db4.png)
![image](https://user-images.githubusercontent.com/107069287/189973247-346f8e09-b89b-4f15-86b8-b672029d6055.png)

Digite os comandos descritos abaixo ou faça o upload do arquivo e utilize ./ para executar o script: 
- <i>OBS: Não precisa copiar os comentarios com #.</i>

Monte o script abaixo e salve o arquivo como .ps1: 

 <table border="1">    
  <tr>
    <td><b>#Variables for common values</b></td>   
  </tr>
  <tr>
    <td><i>$resourceGroup = "RG-LAB-03"</i></td>
  </tr>
  <tr>
    <td><i>$location = "eastus2"</i></td>
  </tr>
  <tr>
    <td><i>$vmName = "VM-PS01"</i></td>
  </tr>
  <tr>
    <td><i>$vnet = "VNET-03"</i></td>
  </tr>
  <tr>
    <td><i>$subnet = "SUB-LAN"</i></td>
  </tr>
     <tr>
       <td colspan="1"><b>#Create user object</b></td>   
  </tr>
  <tr>
    <td><i>$cred = Get-Credential -Message "Enter a username and password for the virtual machine."<i></td>
  </tr>
<tr>
  <td colspan="1"><b>#Create a public IP address and specify a DNS name</b></td>   
  </tr>
  <tr>
    <td><i>$pip = New-AzPublicIpAddress -ResourceGroupName $resourceGroup -Location $location</i></td>
  </tr>
  <tr>
    <td><i>-Name "VMPSIPPUB" -AllocationMethod Dynamic</i></td>
  </tr>  
<tr>
  <td colspan="1"><b>#Create an inbound network security group rule for port 3389</b></td>   
  </tr>
  <tr>
    <td><i>$nsgRuleRDP = New-AzNetworkSecurityRuleConfig -Name AllowRDP  -Protocol Tcp `</i></td>
  </tr>
  <tr>
    <td><i>-Direction Inbound -Priority 1000 -SourceAddressPrefix * -SourcePortRange * -DestinationAddressPrefix * `</i></td>
  </tr>
  <tr>
    <td><i>-DestinationPortRange 3389 -Access Allow</i></td>    
  </tr>
<tr>
  <td colspan="1"><b>#Create a network security group</b></td>   
  </tr>
  <tr>
    <td><i>$nsg = New-AzNetworkSecurityGroup -ResourceGroupName $resourceGroup -Location $location `</i></td>
  </tr>
  <tr>
    <td><i>-Name "VM-PS01-NSG" -SecurityRules $nsgRuleRDP</i></td> 
  </tr>
     <td colspan="1"><b>#Get the subnet details for the specified virtual network + subnet combination.</b></td>   
  </tr>
  <tr>
    <td><i>$azureVnetSubnet = (Get-AzVirtualNetwork -Name $vnet -ResourceGroupName $resourceGroup).Subnets | Where-Object {$_.Name -eq $subnet}</i></td> 
  </tr> 
       <td colspan="1"><b>#Create a virtual network card and associate with public IP address and NSG</b></td>   
  </tr>
  <tr>
    <td><i>$nic = New-AzNetworkInterface -Name "VMPS01Nic" -ResourceGroupName $resourceGroup -Location $location `</i></td> 
  <tr>
    <td><i>-SubnetId $azureVnetSubnet.Id -PublicIpAddressId $pip.Id -NetworkSecurityGroupId $nsg.Id</i></td>
  </tr>
       <td colspan="1"><b>#Create a virtual machine configuration</b></td>   
  </tr>
  <tr>
  <td><i>$vmConfig = New-AzVMConfig -VMName $vmName -VMSize Standard_B2S | `</i></td>
  </tr>
  <tr>
  <td><i>Set-AzVMOperatingSystem -Windows -ComputerName $vmName -Credential $cred | `</i></td>
  </tr>
  <tr>
    <td><i>Set-AzVMSourceImage -PublisherName MicrosoftWindowsServer -Offer WindowsServer -Skus 2019-Datacenter -Version latest | `</i></td>
  </tr>
  <tr>
  <td><i>Add-AzVMNetworkInterface -Id $nic.Id</i></td>
  </tr>
  <tr>
  <td colspan="1"><b>#Create a virtual machine</b></td>   
  </tr>
  <tr>
  <td><i>New-AzVM -ResourceGroupName $resourceGroup -Location $location -VM $vmConfig</i></td> 
  </tr>
</table>



[PowerShell_MOD3_LAB_CLOUD (1).zip](https://github.com/paulorock2505/Microsoft-Azure-Jobs/files/9560075/PowerShell_MOD3_LAB_CLOUD.1.zip)
