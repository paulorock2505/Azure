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
 

 
AdminPassword=ChangeYourAdminPassword1
- az network public-ip create --resource-group "RG-LAB-04" --name "VMCLIIPPUB"
- az network nsg create --resource-group "RG-LAB-04" --name "VM-CLI01-NSG"
- az network nic create --resource-group "RG-LAB-04" --name "VMCLIS01Nic" --vnet-name "VNET-04" --subnet "SUB-LAN" --network-security-group "VM-CLI01-NSG" --public-ip-- address "VMCLIIPPUB"
- az vm create --resource-group "RG-LAB-04" --name "VM-CLI01" --location eastus2 --nics "VMCLIS01Nic" --image win2019datacenter --admin-username admin.raphael --admin-password $AdminPassword
- az vm open-port --port 3389 --resource-group "RG-LAB-04" --name "VM-CLI01"
