 <h2>Lab04 - Manage Azure resources with the Azure CLI</h2>

<h3>Task 2: Criar um resource group, uma VNET e uma Subnet usando o Azure CLI</h3>


 
 <table border="1">    
  <tr>
    <th>Resource Group</th> 
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
 </table>
 
  <table border="1">    
  <tr>
    <th>VNET</th> 
</table>

<table border="1">    
  <tr>
    <th colspan="1">Setting</th>  	              
    <th colspan="2">Value</th>
  </tr>
<tr>
<td>Vnet Name</td>
    <td>VNET-04</td>
  </tr>
<tr>
<td>Region</td>
    <td>East US 2</td>
  </tr>
<tr>
<td>Address</td>
    <td>10.4.0.0/16</td>
  </tr>
 </table>

<table border="1">    
  <tr>
    <th>Subnet</th> 
</table>

<table border="1">    
  <tr>
    <th colspan="1">Setting</th>  	              
    <th colspan="2">Value</th>
  </tr>
<tr>
<td>Subnet Name</td>
    <td>SUB-LAN</td>
  </tr>
<tr>
<td>Address</td>
    <td>10.4.0.0/24</td>
  </tr>
 </table>
 
 #Criar Resource Group:
az group create --location eastus2 --name "RG-LAB-04" --tags "Modulo=MOD03"

#Criar uma VNET e uma Subnet:
az network vnet create --name "VNET-04" --resource-group “RG-LAB-04” --address-prefix 10.4.0.0/16 --subnet-name "SUB-LAN" --subnet-prefix 10.4.0.0/24
