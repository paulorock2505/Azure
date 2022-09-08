# AZ-104-LAB-MOD-02
Repositório do Laboratório do módulo 01 para o exame de certificação AZ-104. (Credits by TFTEC)

Task 03 Aplicar tagging via Azure Policy. 

<table border="1">    
  <tr>
    <th colspan="1">TAG</th> 
</table>

<table border="1">
  <tr>
    <th colspan="1">Name</th>  	              
    <th colspan="2">Value</th>
  </tr>
  <tr>
    <th colspan="1">Departamento</th>  	              
    <th colspan="2">TI</th>
  </tr>
 </table>
 
 No portal do Azure, vá em Policy: 

![image](https://user-images.githubusercontent.com/107069287/188467897-2b613362-b0f8-4a90-9a51-a6780fe3ea84.png)

Delete a policy criada anteriormente. 

![image](https://user-images.githubusercontent.com/107069287/188468031-be2419e4-72fd-4f63-9999-42729cd2ba5d.png)

Na sequência, vá na opção Definition: 

![image](https://user-images.githubusercontent.com/107069287/188468252-d1652ab5-18f8-408c-abf7-a1ef63512158.png)

Em Definition Type, marque a opção Policy e em seguida em categoria desmarque a opção Select all e marque apenas a TAG, conforme imagem abaixo: 

![image](https://user-images.githubusercontent.com/107069287/188468835-1ed1c09d-67db-4f5a-a3f0-8f3b591680c5.png)

Clique em Inherit a tag from the resource group if missing 

![image](https://user-images.githubusercontent.com/107069287/188469329-1d65dfb2-c192-4362-b106-1db3bddd7001.png)

Clique em Assign. 

![image](https://user-images.githubusercontent.com/107069287/188469550-6d16452e-ea05-442b-9c62-6c45735a6973.png)

Atribua a política a assinatura e ao Resource Group conforme a imagem: 

![image](https://user-images.githubusercontent.com/107069287/188469817-10dd8e94-9da9-42ee-a03a-1c937a7f9828.png)

Clique em Next. 

Em parameters iremos configurar a TAG de nossa política: 

![image](https://user-images.githubusercontent.com/107069287/188470069-c9cc150c-3fa4-45c0-be5f-5eddfb94f673.png)

Clique em Next. 

Em remediation marque a opção Create a remediation task e mantém os padrões conforme imagem abaixo: 

![image](https://user-images.githubusercontent.com/107069287/188470324-768240a4-e297-4a35-95ab-17c51d944fae.png)

Clique em Review + Create e depois em Create para criar a policy. 


Na sequência crie um recusro dentro da RG que aplicamos a policy e valide a politica recém criada.



