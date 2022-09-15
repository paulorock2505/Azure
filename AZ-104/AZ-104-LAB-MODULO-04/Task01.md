<h2>Lab 04 - Implement Virtual Networking</h2>

<p>Task 01: Crie um RG, uma VNET e duas Subnets.</p>

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
    <td>RG-MOD04</td>
  </tr>
  <tr>
    <td>Region </td>
    <td>East US 2</td>
  </tr>
 </table> 
 
 <table border="1">    
  <tr>
    <th colspan="1">VNET</th> 
</table>

<table border="1">    
  <tr>
    <th colspan="1">Setting</th>  	              
    <th colspan="2">Value</th>
  </tr>
<td>VNET Name</td>
    <td>az104-04-vnet1</td>
  </tr>
  <tr>
    <td>Region </td>
    <td>East US 2</td>
  </tr>
  <tr>
    <td>Address</td>
    <td>10.40.0.0/20</td>
  </tr>
 </table> 
 
 <table border="1">    
  <tr>
    <th colspan="1">Subnet0</th> 
</table>

<table border="1">    
  <tr>
    <th colspan="1">Setting</th>  	              
    <th colspan="2">Value</th>
  </tr>
<td>Subnet Name</td>
    <td>subnet0</td>
  </tr>
  <tr>
    <td>Address</td>
    <td>10.40.0.0/24</td>
  </tr>
 </table> 
 
 <table border="1">    
  <tr>
    <th colspan="1">Subnet1</th> 
</table>

<table border="1">    
  <tr>
    <th colspan="1">Setting</th>  	              
    <th colspan="2">Value</th>
  </tr>
<td>Subnet Name</td>
    <td>subnet1</td>
  </tr>
  <tr>
    <td>Address</td>
    <td>10.40.1.0/24</td>
  </tr>
 </table> 

Abra o portal do Azure e no campo de pesquisa busque por Resource Group: 

![image](https://user-images.githubusercontent.com/107069287/190425063-189df598-896c-492b-8a13-f7f7dcfa1534.png)

Clique em + Create: 

![image](https://user-images.githubusercontent.com/107069287/190425174-b6544753-1998-4693-851b-8f124d53d162.png)

Em Resource Group, vamos criar o recurso de acordo com a tabela acima: 

![image](https://user-images.githubusercontent.com/107069287/190425535-33ca6276-c852-41fc-b33a-57dfedd51e6e.png)

Clique em Next. 

Vamos criar uma TAG mantendo o padrão utilizado anteriormente, utilize as TAGs conforme a imagem abaixo: 

![image](https://user-images.githubusercontent.com/107069287/190426041-a327f853-3833-4715-ada6-fa968fc54829.png)

Clique em Review + Create e em seguida Create para criar o grupo de recursos. 

Em seguida clique em Go to Resource Group: 

![image](https://user-images.githubusercontent.com/107069287/190426578-bd43bb00-590f-4101-9350-579170e2f894.png)

Em Overview, clique em + Create: 

![image](https://user-images.githubusercontent.com/107069287/190427508-123c8611-a30f-4434-af4e-0fd0939506d5.png)

No Marketplace, no campo de pesquisa procure por Virtual Network:

![image](https://user-images.githubusercontent.com/107069287/190427692-8ceb94e3-aad5-4206-8e3c-9734022b09ad.png)

Clique em Create e em seguida Virtual Network:

![image](https://user-images.githubusercontent.com/107069287/190427847-5f1b9e4f-6b7d-4668-8f82-9e2b4cf73dc8.png)

Na sessão Basics, defina o Resource Groups que acabamos de criar e preencha os campos conforme definimos na tabela acima: 

![image](https://user-images.githubusercontent.com/107069287/190429678-f1ba3a53-bff4-44d5-a745-e1dba87ee10e.png)

Clique em Next. 

Em IPv4 Address Space vamos alterar para o padrão que definimos acima: 

![image](https://user-images.githubusercontent.com/107069287/190430105-7949859e-9781-4b9f-9f35-adb0afd0c795.png)

Clique em + Add subnet para adicionarmos uma subnet: 

![image](https://user-images.githubusercontent.com/107069287/190430751-a869c5e8-91ef-46b1-9b56-4fa044fcc20b.png)

Vamos definir os valores que definimos na tabela acima: 

![image](https://user-images.githubusercontent.com/107069287/190431036-a70e5687-a332-409f-afb7-ebdc4c368c53.png)

Em seguida clique Add. 

<i>OBS: Poderíamos criar a segunda subnet já nesta fase, mas para fins didáticos irei criar já dentro da VNET para desenvolvermos um outro método de criação.</i>

Clique em Next. 

Em Security vamos manter todas as opções desabilitadas e clicarmos em Next novamente: 

![image](https://user-images.githubusercontent.com/107069287/190432618-af35474c-b025-4a5f-aeb5-9914580de558.png)

Em Tags, vamos adicionar a TAG utilizada anteriormente: 

![image](https://user-images.githubusercontent.com/107069287/190432773-f0980e36-1ee8-49f5-9d4d-bd8ae6bf80e9.png)

Em seguida clique em Review + Create e na sequência Create. 

Clique em Go to resource: 

![image](https://user-images.githubusercontent.com/107069287/190433125-758990b5-6f64-4086-bd94-e1f41e081b6f.png)

Para criarmos a segunda subnet, iremos ao campo settings e em seguida clicaremos em subnet: 

![image](https://user-images.githubusercontent.com/107069287/190433369-8337d425-cd02-4221-a486-38fd213651d4.png)

Note que já temos a nossa primeira subnet configurada, agora criaremos a segunda clicando em + Subnet:

![image](https://user-images.githubusercontent.com/107069287/190433524-4df5984b-8c78-4db9-b56f-7f90b891fc75.png)

Preencha os campos conforme definimos na tabela acima novamente: 

![image](https://user-images.githubusercontent.com/107069287/190434808-e5112889-a796-44e1-87d3-1d783f4874ec.png)

Clique em Save. 

Note que as duas subnet foram criadas seguindo as denicões acima. 
