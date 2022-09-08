# AZ-104-LAB-MOD-03
Repositório do Laboratório do módulo 01 para o exame de certificação AZ-104. (Credits by TFTEC)

<h2>Lab 01 - Manage Azure resources with the azure Portal</h2>

<h3>Task 1:	Criar resource groups e implantar recursos nestes resource groups</h3>

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
    <td>RG-LAB-01</td>
  </tr>
  <tr>
    <td>Region </td>
    <td>East US 2</td>
  </tr>
 </table>
 
 <table border="1">    
  <tr>
    <th colspan="1">Setting</th>  	              
    <th colspan="2">Value</th>
  </tr>
<td>Resource Group</td>
    <td>RG-LAB-02</td>
  </tr>
  <tr>
    <td>Region </td>
    <td>East US 2</td>
  </tr>
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
<td>Resource Group</td>
    <td>RG-LAB-01</td>
  </tr>
  <tr>
    <td>Region </td>
    <td>East US 2</td>
  </tr>
  <td>Name</td>
    <td>VM-01</td>
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
 
 Abra o portal do Azure e no campo de pesquisa busque por Resource Group: 

![image](https://user-images.githubusercontent.com/107069287/188698335-20367846-81f1-4af7-a9b2-60e6fb6f8666.png)

Em Resource Group clique em + Create: 

![image](https://user-images.githubusercontent.com/107069287/188700702-991f683b-fc2d-48aa-a643-9b0e774edbd4.png)

Em basics preencha o nome do recurso conforme a imagem: 

![image](https://user-images.githubusercontent.com/107069287/188700953-fb98fbec-c8a0-49e4-b516-1747eae2f16f.png)

Clique em Next. 

Para melhor prática, preencha as TAGs conforme a imagem: 

![image](https://user-images.githubusercontent.com/107069287/188702837-89d885b1-0c99-4071-a362-386ecbed3f99.png)

Clique em Next e na sequência Review + Create e em seguida Create para criarmos o grupo de recursos. 

Na sequência criaremos o segundo Resource Group. 

No portal do Azure, clique novamente em Resource Group: 

![image](https://user-images.githubusercontent.com/107069287/188703302-7ef8a01e-24c3-4614-a091-f789c12522bb.png)

Clique em + Create: 

![image](https://user-images.githubusercontent.com/107069287/188703364-254f497f-4ffb-4a06-adb4-7f54a57d8b56.png)

Em basics preencha o nome do recurso conforme a imagem: 

![image](https://user-images.githubusercontent.com/107069287/188703709-9e4a147c-4573-4358-a67f-30f20fec35c2.png)

Clique em Next. 

Para melhor prática, preencha as TAGs conforme a imagem: 

![image](https://user-images.githubusercontent.com/107069287/188703816-25b1b2ae-f029-4989-86d1-17fc63037b39.png)

Clique em Next e na sequência Review + Create e em seguida Create para criarmos o grupo de recursos. 

Após a criação do Recurso, no campo de notificações clique em Go to Resource: 

![image](https://user-images.githubusercontent.com/107069287/188704286-8f03de1d-c9a4-40a1-9282-ca5066ffd044.png)

Agora iremos criar uma virtual machine: 

No portal do Azure, no campo de pesquisa digite Virtual Machine: 

![image](https://user-images.githubusercontent.com/107069287/188704818-c0464a97-004e-4ba9-b667-ac3134184a30.png)

Na sequência clique em + Create e em seguida Azure Virtual Machine: 

![image](https://user-images.githubusercontent.com/107069287/188704989-11c4dcfe-0ef6-449b-b6be-6d3529f7d9d8.png)

Preencha os campos como mostrado na imagem e seguindo a nossa tabela no início do nosso tópico: 

![image](https://user-images.githubusercontent.com/107069287/188705340-cf66e761-9cb7-45e6-af87-698f8e82c132.png)

Em size, clique em See All Sizes e vamos escolher o tamanho proposto para esse laboratório, o B2s e em seguida clique em select: 

![image](https://user-images.githubusercontent.com/107069287/188707611-f1d60f24-c7b2-4845-bc86-dc3216499a83.png)
![image](https://user-images.githubusercontent.com/107069287/188707643-c5fbe111-7a30-48fb-9b8d-8caf6a3cbfbd.png)

Na sequência determine um usuário e senha para acesso a máquina: 

![image](https://user-images.githubusercontent.com/107069287/188707881-2cb646b6-106c-49ea-846f-e71fb6e4d527.png)

E em seguida clique em Next. 

Em disk, não vamos alterar nada, manteremos a opção padrão: 

![image](https://user-images.githubusercontent.com/107069287/188709233-1b5a64db-ced3-4298-8751-75187422167b.png)

Clique em Next. 

Em network manteremos também a opção padrão: 

![image](https://user-images.githubusercontent.com/107069287/188709569-f6cc6b5a-0eae-4630-ac92-3ae1330ebc15.png)

Em Management, no menu boot diagnostics, marcaremos a opção disable e desamrcaremos a opção Enable OS Diagnostics: 

![image](https://user-images.githubusercontent.com/107069287/188721528-2c38a883-97a3-46d2-a68a-9fb4cb43b205.png)

Clique em Next. 

Na opção Advanced não faremos nenhuma alteração: 

![image](https://user-images.githubusercontent.com/107069287/188710232-2917fcb3-3e69-4f98-8ade-eff2b432aa24.png)

Clique em Next. 

Na opção de TAGs, iremos colocar a TAG conforme colocamos nos recursos anteriores: 

![image](https://user-images.githubusercontent.com/107069287/188710442-892ec5aa-e601-438a-b67c-6eca617f8e5c.png)

Clique Review + Create e em seguida Create para criarmos o máquina virtual. 

Após a conclusão da criação da máquina virtual, va na opção Resources Group e valide a criação dos dois grupo de recursos. 

Após a validação, vá novamente ao portal e no campo de pesquisa procure por Virtual Machines: 

![image](https://user-images.githubusercontent.com/107069287/188722584-7ee2c156-83a0-45ea-98ee-c645afd7035b.png)

Clique na máquina virtual que acabamos de criar: 

![image](https://user-images.githubusercontent.com/107069287/188722777-3c7e7421-3653-4d0a-8d82-c17c1ce745de.png)

Em Overview iremos clicar em Connect, em seguida selecionaremos RDP: 

![image](https://user-images.githubusercontent.com/107069287/188722885-dc76fe7d-aa60-45d0-bf2c-d913379a9d32.png)

Clicaremos em Download RDP File: 

![image](https://user-images.githubusercontent.com/107069287/188722989-d4c08d10-0e46-4fbd-89bc-c6b57b2e8c62.png)

Após o download da aplicação RDP, iremos fazer a conexão na máquina que criamos: 

![image](https://user-images.githubusercontent.com/107069287/188723102-c580486b-19a7-4344-ac27-9d4e1f7808da.png)

Clicaremos em connect e em seguida utilizaremos as credencias que cconfiguramos (usuário e senha) nesse Laboratório: 

![image](https://user-images.githubusercontent.com/107069287/188723219-f9e74163-156e-4b41-a31f-a4ebdda5bbc1.png)

Clique em sim:

![image](https://user-images.githubusercontent.com/107069287/188723350-d73a9711-53bb-4dba-85f6-cde0f33d563c.png)

E estamos conectados na máquina recém criada: 

![image](https://user-images.githubusercontent.com/107069287/188723507-67449a1b-3831-427d-b2bf-334b4e1f5c9c.png)























