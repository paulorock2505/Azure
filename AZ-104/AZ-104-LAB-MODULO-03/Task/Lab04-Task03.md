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
 
 Acesse o portal e abra o cloudshell do azure: 

![image](https://user-images.githubusercontent.com/107069287/189999697-281964fe-6273-48e8-bfc4-01788f8b7e88.png)

Ao abrir o cloudshell, selecione a opção Bash, como na imagem abaixo: 

![image](https://user-images.githubusercontent.com/107069287/189999828-6d74a9e4-665e-4a0d-8f80-39c6e554b347.png)

Em seguida pode copiar os comandos abaixo por completo que o bash executará todos eles em seguida: 
 
AdminPassword=ChangeYourAdminPassword1
- az network public-ip create --resource-group "RG-LAB-04" --name "VMCLIIPPUB"
- az network nsg create --resource-group "RG-LAB-04" --name "VM-CLI01-NSG"
- az network nic create --resource-group "RG-LAB-04" --name "VMCLIS01Nic" --vnet-name "VNET-04" --subnet "SUB-LAN" --network-security-group "VM-CLI01-NSG" --public-ip-- address "VMCLIIPPUB"
- az vm create --resource-group "RG-LAB-04" --name "VM-CLI01" --location eastus2 --nics "VMCLIS01Nic" --image win2019datacenter --admin-username admin.paulo --admin-password $AdminPassword
- az vm open-port --port 3389 --resource-group "RG-LAB-04" --name "VM-CLI01"
