# AZ-104-LAB-MOD-03
Repositório do Laboratório do módulo 01 para o exame de certificação AZ-104. (Credits by TFTEC)

<h2>Lab 01 - Manage Azure resources with the azure Portal</h2>

Task 3:	Implementar e testar resource locks

<table border="1">    
  <tr>
    <th colspan="1">Resource Locks</th> 
</table>

<table border="1">    
  <tr>
    <th colspan="1">Setting</th>  	              
    <th colspan="2">Value</th>
  </tr>
<td>Resource Group</td>
    <td>RG-LAB3-01</td>
  </tr>
  <tr>
    <td>Locks</td>
    <td>Read Only</td>
  </tr>
 </table> 
 <table border="1">    
  <tr>
    <th colspan="1">Setting</th>  	              
    <th colspan="2">Value</th>
  </tr>
<td>Resource Group</td>
    <td>RG-LAB3-02</td>
  </tr>
  <tr>
    <td>Locks</td>
    <td>Delete</td>
  </tr>
 </table>
 
 No portal do Azure, vá até o campo de pesquisa e busque por Resource Group:

![image](https://user-images.githubusercontent.com/107069287/189655325-854c69b1-3809-4d91-9e11-0b892070908a.png)

Clique em RG-LAB-01:

![image](https://user-images.githubusercontent.com/107069287/189655669-7d7c0f19-1fe3-4f23-a00a-1ebc605284d1.png)

Em seguida vá até o campo Locks:

![image](https://user-images.githubusercontent.com/107069287/189655831-976a7d6f-5079-40ed-8c3e-5d7e0d0237d0.png)

Clique em + Add e preencher os campos conforme a imagem: 

![image](https://user-images.githubusercontent.com/107069287/189657129-c04d7233-dfd1-4324-896b-5e2549598a7b.png)

Em seguida clique em Ok. 

Após essa etapa iremos validar o bloqueio aplicado. 

Vá até o portal e tente criar uma máquina virtual. Clique no campo de pesquisa e digite virtual machine: 

![image](https://user-images.githubusercontent.com/107069287/189657694-0c070118-9b54-477c-a3ae-d11ac08ad784.png)

Em seguida clique em + Create e em seguida Azure Virtual Machine: 

![image](https://user-images.githubusercontent.com/107069287/189657842-b2d474c2-9292-4b95-8adf-09ac8af46792.png)

Selecione o RG-LAB-01 e note a mensagem de erro apresentada. Perceba que o lock aplicado é apenas de Read Only: 

![image](https://user-images.githubusercontent.com/107069287/189658073-8bab5264-d7d1-41dd-931f-105242bc1629.png)

Volte ao portal. 

Faremos um novo lock em RG-LAB-02. No portal, dentro do campo de pesquise digite Resource Group: 

![image](https://user-images.githubusercontent.com/107069287/189658471-098dac34-e26c-4acf-98e3-bbdc8ce641e0.png)

Em seguida clique em RG-LAB-02:

![image](https://user-images.githubusercontent.com/107069287/189658715-407b6b12-ac1d-4f8f-ad39-46d80bc9f039.png)

Vá até a opção Locks: 

![image](https://user-images.githubusercontent.com/107069287/189658793-7257015d-22f2-4e7b-9bbe-9ca50f577a6b.png)

E clique em + Add e preencha os campos conforme a imagem:

![image](https://user-images.githubusercontent.com/107069287/189659008-e8ba8fbe-dcf5-47a5-a6a3-da46f501cadd.png)

Em seguida clique em Ok. 

Após essa etapa iremos validar o bloqueio aplicado. 

Vá até o portal e tente criar um storage account. Clique no campo de pesquisa na página principal do Azure e digite storage accounts: 

![image](https://user-images.githubusercontent.com/107069287/189662910-563c0ab8-3f85-4a5e-8b3a-a736c5f29c0a.png)

Em seguida clique em + Create: 

![image](https://user-images.githubusercontent.com/107069287/189663032-37fcaad2-cc30-4dc3-900d-c534e2c83597.png)

Nessa etapa, criaremos um storage account com as opções default: 

Utilize as opções padrão e no campo Storage Account Name, crie um nome que não exista dentro da estrutura. Pode utilizar qualquer nome neste campo: 

![image](https://user-images.githubusercontent.com/107069287/189663692-133d2ff0-ad59-48ec-931d-da2c997f7048.png)

Clique em Review e em seguida create. 

Após a criação do recurso, vá em Go to Resource e vamos validar o bloqueio: 

![image](https://user-images.githubusercontent.com/107069287/189664587-b0aa9ced-b1bc-40a0-89fd-8cfe2c5fd7d2.png)

Em Overview, vamos clique em delete e aguarde o comportamento. 

Note que ao deletar o recurso nos deparamos com o erro abaixo:

![image](https://user-images.githubusercontent.com/107069287/189664863-0c35f5ef-e65a-4e4e-9e1a-9a120a2f66c1.png)

Ou seja, o usuário possui permissão para criar os recursos, mas não tem permissão para deletar o recurso conforme a política de bloqueio que aplicamos no Resource Group. 

Algumas observaçõs: 

- Os Locks só são removidos com o usuário que possui privilégio de administrador da subscription ou do RG. 
- Em storage account, caso o lock de read only estiver aplicado, o usuário não consegue visualizar as Access Key do storage. 























