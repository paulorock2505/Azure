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
 
 <h3>Task 2:	Criar um Resource Group, uma VNET e uma Subnet.</h3>
 
 <table border="1">    
  <tr>
    <th colspan="1">Resource Group</th> 
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
 </table>
 
 <table border="1">    
  <tr>
    <th colspan="1">Vnet</th> 
</table>
 
 <table border="1">    
  <tr>
    <th colspan="1">Setting</th>  	              
    <th colspan="2">Value</th>
  </tr>
<td>Vnet Name</td>
    <td>VNET-03</td>
  </tr>
  <tr>
    <td>Region </td>
    <td>East US 2</td>
  </tr>
  <tr>
    <td>Address</td>
    <td>10.3.0.0/16</td>
  </tr>
 </table>
 
 <table border="1">    
  <tr>
    <th colspan="1">Seubnet</th> 
</table>
 
 <table border="1">    
  <tr>
    <th colspan="1">Virtual Machine</th> 
</table>

<table border="1">    
  <tr>
    <th colspan="1">Setting</th>  	              
    <th colspan="2">Value</th>
  </tr>
<td>Subnet Name</td>
    <td>SUB-LAN</td>
  </tr>
  <tr>
    <td>Address</td>
    <td>10.3.0.0/24</td>
  </tr>
 </table>

Criar Resource Group:
- New-AzResourceGroup -Name "RG-LAB-03" -Location "eastus2" -Tag @{Modulo="MOD03"}

Criar uma VNET:
- $virtualNetwork = New-AzVirtualNetwork `
  -ResourceGroupName "RG-LAB-03" `
  -Location "eastus2" `
  -Name "VNET-03" `
  -AddressPrefix 10.3.0.0/16

Adicionar uma Subnet
- $subnetConfig = Add-AzVirtualNetworkSubnetConfig `
  -Name "SUB-LAN" `
  -AddressPrefix 10.3.0.0/24 `
  -VirtualNetwork $virtualNetwork
  
Setar a Subsnet criada na VNET existente
- $virtualNetwork | Set-AzVirtualNetwork
