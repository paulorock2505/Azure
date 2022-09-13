 <h2>Lab04 - Manage Azure resources with the Azure CLI</h2>

<h3>Task 3: Iniciar uma sessão do Bash no Cloud Shell do Azure e criar uma VM</h3>


 <table border="1">    
  <tr>
    <th>Virtual Machine</th>
  </tr>
</table>

<table border="1">    
  <tr>
    <th colspan="1">Setting</th>  	              
    <th colspan="2">Value</th>
  </tr>
<tr>
<td>Resource Group</td>
    <td>RG-LAB-04</td>
  </tr>
<tr>
<td>Region</td>
    <td>East US 2</td>
  </tr>
<td>Name</td>
    <td>VM-CLI-01</td>
 </tr>
  <td>Image</td>
    <td>Windows Server 2019</td>
  </tr>
  <td>Size</td>
    <td>B2s</td>
  </tr>
 </table>
 
  <table border="1">    
  <tr>
    <th>VNET</th>
  </tr>
</table>
 
 #Criar Resource Group:
- az group create --location eastus2 --name "RG-LAB-04" --tags "Modulo=MOD03"

#Criar uma VNET e uma Subnet:
- az network vnet create --name "VNET-04" --resource-group “RG-LAB-04” --address-prefix 10.4.0.0/16 --subnet-name "SUB-LAN" --subnet-prefix 10.4.0.0/24
