# AZ-104-LAB-MOD-03
Repositório do Laboratório do módulo 01 para o exame de certificação AZ-104. (Credits by TFTEC)

<h2>Lab 01 - Manage Azure resources with the azure Portal</h2>

Task 2:	Mover recursos entre os resource groups

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

No portal do Azure, no campo de pesquisa procure por Resource Groups: 

![image](https://user-images.githubusercontent.com/107069287/188728056-dd3f9700-b246-445b-b84d-2a472a1e1cc8.png)

Acesse o grupo de recursos RG-LAB-01: 

![image](https://user-images.githubusercontent.com/107069287/188728163-5243fa25-6925-4e4a-9da2-49cfd3d09c19.png)

Na sequência iremos movimentar todos os recursos que criamos para o outro grupo de recursos: 

Em Overview selecionaremos todos os recursos disponíveis exceto a vnet, conforme a imagem: 

![image](https://user-images.githubusercontent.com/107069287/188728702-c6f7d17a-83a7-4d4c-be44-ddc8d4017a92.png)
![image](https://user-images.githubusercontent.com/107069287/188728737-0e43ef20-8146-42c6-9d4f-49af517c5e2a.png)

Em seguida clicaremos em move e na sequência move to another resource group: 

![image](https://user-images.githubusercontent.com/107069287/188728868-96a41918-0a10-450f-90d4-158e71b81e41.png)

Na tela Source + target escolheremos o outro recurso que criamos RG-LAB-02: 

Clicaremos em seguida em next. 

Em Resources to move aguarde a validação: 

![image](https://user-images.githubusercontent.com/107069287/188729705-9e91a700-de3e-41a5-9403-2d0aaeda6615.png)

Feito a validação clique em Next. 

![image](https://user-images.githubusercontent.com/107069287/188729988-dfa8abb7-b5dd-42fe-a920-b96cec4159a0.png)

Marque a opção I understand that tools and scripts associated with moved resources will not work until update them to use new resource IDs e em seguida clique em move. 

![image](https://user-images.githubusercontent.com/107069287/188730348-08bee865-2b3e-41d8-9510-de2ef95ded05.png)

Aguarde até que todos os recursos sejam transferidos: 

![image](https://user-images.githubusercontent.com/107069287/188730439-f6ab5fe1-1aa8-4750-b795-da3f94d97d94.png)

Caso queira acompanhar o andamento do processo, podemos acompanhar todo o processo clicando no Activity Log: 

![image](https://user-images.githubusercontent.com/107069287/188730766-4839c34d-7cde-492e-b8e6-7396d75f4ee0.png)

Acesse o RG-LAB-02 e verifique os recursos que foram movidos. 










 
 
 
