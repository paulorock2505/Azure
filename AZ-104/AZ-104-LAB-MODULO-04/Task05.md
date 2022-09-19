<h2>Lab 04 - Implement Virtual Networking</h2>
 
<h3>Task 5: Configurar o DNS do Azure para resolução interna do nome</h3>

<table border="1">    
  <tr>
    <th colspan="1">DNS Interno</th> 
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
    <td>Name</td>
    <td>alpatec.com.br</td>
  </tr>
  </table>
   
<table border="1">    
  <tr>
    <th colspan="1">Link DNS</th> 
</table>

<table border="1">    
  <tr>
    <th colspan="1">Setting</th>  	              
    <th colspan="2">Value</th>
  </tr>
<td>Link Name</td>
    <td>az104-04-vnet1-link</td>
  </tr>
  <tr>
    <td>Virtual Network</td>
    <td>az-104-04-vnet1</td>
  </tr>
   <tr>
    <td>Enable auto registration</td>
    <td>Enabled</td>
  </tr>
  </table>

  Na home do portal do azure, pesquise por Private DNS Zones: 

  ![image](https://user-images.githubusercontent.com/107069287/191101808-df3eba80-82a6-4221-a644-a675625a5537.png)

  Clique em + Create: 

  ![image](https://user-images.githubusercontent.com/107069287/191101920-7aa3073d-4fbe-41e0-8b9e-b9f518ae01ec.png)

  Preencha os campos abaixo conforme nossa tabela acima: 

  ![image](https://user-images.githubusercontent.com/107069287/191102371-5185a431-2eda-4d85-b053-1b1dbfcb09ed.png)

  Clique em Next. 

  Em Tags, preencha os campos como foi feito nas atividades anteriores: 

  ![image](https://user-images.githubusercontent.com/107069287/191102650-b67d464c-88d3-4829-bcb4-c90b138232fd.png)

  Em seguida clique em Review + Create e em seguida Create. 

  Após o processo vá em Go to Resource. 

  Note que criamos uma Zona onde temos os nossos registros. 

  ![image](https://user-images.githubusercontent.com/107069287/191103847-24cfa677-12b6-48a7-890c-4aba64fd693a.png)

  Em seguida iremos fazer o link de qual virtual network usará essa zona de DNS. 

  Vá até Virtual Network Links: 

  ![image](https://user-images.githubusercontent.com/107069287/191104416-b02d0b87-bd9c-48fc-9c2f-4d7d33d06da3.png)

  Em seguida clique em + Add: 

  ![image](https://user-images.githubusercontent.com/107069287/191104567-d1a6b5c7-88ab-4b20-bec7-ef0c3d869014.png)

  Utilize os parametros que definimos na tabela acima: 

  ![image](https://user-images.githubusercontent.com/107069287/191105112-b233228c-de17-480a-ac99-59e9a63c2e36.png)

  Em seguida clique em Ok. 

  Aguarde até que o link status apareça como Completed. Esse processo pode demorar alguns minutos. 

  ![image](https://user-images.githubusercontent.com/107069287/191105761-e3906db3-bbf5-492d-ae8a-b74ea925c420.png)

  Em Overview, note que as duas máquinas já se registraram: 

  ![image](https://user-images.githubusercontent.com/107069287/191106326-8c24e5ad-2578-41db-9a67-7c517446342d.png)

*Como desafio final, acesse remotamente uma das máquinas e dentro do PowerShell ou Prompt de comando faça testes de ping e o nslookup com os códigos abaixo:*

```
ping az104-04-vm0.alpatec.com.br 
nslookup az104-04-vm0.alpatec.com.br
nslookup az104-04-vm1.alpatec.com.br 
```
*Caso tenha resposta dos dois comandos a atividade foi concluida com êxito.*
