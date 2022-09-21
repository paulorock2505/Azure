# AZ-104-LAB-MOD-01

<h2>Lab 01 - Gerenciar as identidades do Azure Active Directory - Task 02</h2> 

 

<table border="1">    
  <tr>
    <th colspan="1">Grupo 01</th>  	              
    <th colspan="2">Regra 01</th>
  </tr>    
<table border="1">    
   <tr>
    <td>Settings</td>
    <td>Value</td>
    <td>Settings</td>
    <td>Value</td>
  </tr>
  <tr>
    <td>Group type</td>
    <td>Security</td>
    <td>Property</td>
    <td>jobTitle</td>
  </tr>
 <tr>
    <td>Group Name</td>
    <td>IT Cloud Administrators</td>
    <td>Operator</td>
    <td>Equals</td>
  </tr>
 <tr>
    <td>Group description</td>
    <td>Contoso IT cloud administrators</td>
    <td>Value</td>
    <td>Cloud Administrator</td>
  </tr>
 <tr>
    <td>Membership type</td>
    <td>Dynamic User</td>
    <td>Value</td>
    <td>Cloud Administrator</td>
  </tr>
 <tr>
    <td>Membership type</td>
    <td>Dynamic User</td>
  </tr>
</table>
<table border="1">    
  <tr>
    <th colspan="1">Grupo 02</th>  	              
    <th colspan="2">Regra 02</th>
  </tr>    
<table border="1">    
   <tr>
    <td>Settings</td>
    <td>Value</td>
    <td>Settings</td>
    <td>Value</td>
  </tr>    
  <tr>
    <td>Group type</td>
    <td>Security</td>
    <td>Property</td>
    <td>jobTitle</td>
  </tr>
 <tr>
    <td>Group Name</td>
    <td>IT System Administrators</td>
    <td>Operator</td>
    <td>Equals</td>
  </tr>
 <tr>
    <td>Group description</td>
    <td>Contoso IT system administrators</td>
    <td>Value</td>
    <td>System Administrator</td>
  </tr>
 <tr>
    <td>Membership type</td>
    <td>Dynamic User</td>
    <td>Value</td>
    <td>System Administrator</td>
  </tr>
 <tr>
    <td>Membership type</td>
    <td>Dynamic User</td>
  </tr>
</table>    

 Acesse ao Azure Active Directory: 
 
![Task-02-photo-00](https://user-images.githubusercontent.com/107069287/187280345-3c8a6b73-dec6-4731-8d15-26545f8ac14d.png)
 ![Task-02-photo-01](https://user-images.githubusercontent.com/107069287/187280548-2fecb005-fff6-46f8-9496-a3946edfa95d.png)
 
 Vá até a aba Licenses: 

![Task-02-photo-02](https://user-images.githubusercontent.com/107069287/187280886-b4466f05-8433-49ab-8e09-c34cc56003ad.png)
![Task-02-photo-03](https://user-images.githubusercontent.com/107069287/187280891-5c2e9bac-40c1-4ce7-bac6-35f429c81d34.png)

Em seguida clique em All Products: 

![Task-02-photo-04](https://user-images.githubusercontent.com/107069287/187281172-444e5de0-d1c1-4bd9-9704-2b1da97c5ef8.png)
 
 Agora iremos ativar a licença P2. Clique em Try/Buy e na blade Azure AD Premium P2, clique em Free Trial e em seguida Activate: 

![Task-02-photo-05](https://user-images.githubusercontent.com/107069287/187281808-37572a37-dd75-4c66-b8e3-35f3870e3109.png)
![Task-02-photo-06](https://user-images.githubusercontent.com/107069287/187281812-1f22ae09-834a-4a38-a20b-f1166ca62e7b.png)
![Task-02-photo-07](https://user-images.githubusercontent.com/107069287/187281818-0e623dc2-f322-46cc-9f67-b692a4b03e50.png)
 ![Task-02-photo-08](https://user-images.githubusercontent.com/107069287/187282167-c0b8bd37-f6e9-4f7f-8f67-c493fe1bc06d.png)
 
 Agora vamos associar a licensa Premium aos usuários: 

Clique em cima Azure Active Directory Premium P2: 

![image](https://user-images.githubusercontent.com/107069287/187283579-97d5310c-609f-47ca-8dab-658d23217af4.png)
![Task-02-photo-10](https://user-images.githubusercontent.com/107069287/187283643-d1ffc0a5-8690-45ec-acc4-ccbb616425e8.png)
 
E depois clique em Assign: 

![Task-02-photo-11](https://user-images.githubusercontent.com/107069287/187283795-75c27c94-59d3-47d2-8b6c-e409df9948c3.png)
 
 Após clicar em Assign iremos associar a licença para os usuários que queremos que utilize. Nesse caso associaremos para os 3 usuários criados: 

![Task-02-photo-12](https://user-images.githubusercontent.com/107069287/187284213-007903ff-4bc5-4548-8242-6fa1c17a2315.png)
![Task-02-photo-13](https://user-images.githubusercontent.com/107069287/187284215-5b021ce2-a041-4e13-8075-d9ce1b27bc4a.png)
![Task-02-photo-14](https://user-images.githubusercontent.com/107069287/187284216-6dd9ad0b-53fe-453a-8165-bf4804a598ab.png)

 Após associado clicar em Review + Create para fazer a associação das licenças. 
 
 ![Task-02-photo-15](https://user-images.githubusercontent.com/107069287/187284560-cd4c9859-beff-4848-85c3-5dbbbe44d881.png)

 Após essa etpa volte para a aba Active Directory e vá até a aba grupos: 

![Task-02-photo-16](https://user-images.githubusercontent.com/107069287/187286048-42247860-2534-4353-84e7-8c7cb047e491.png)
![Task-02-photo-17](https://user-images.githubusercontent.com/107069287/187286051-ff257c0c-4281-4032-bcad-cd612b7883b4.png)
![Task-02-photo-18](https://user-images.githubusercontent.com/107069287/187286054-875e7875-bc36-4a73-a6f2-60f307925272.png)

 Dentro da opção Grupos iremos criar os nossos grupos: 

![Task-02-photo-19](https://user-images.githubusercontent.com/107069287/187286318-0a31a03c-67a0-4514-b3ae-622214bcfe99.png)
 
 Na sequência iremos preencher os camos conforme descrito na imagem: 
![Task-02-photo-20](https://user-images.githubusercontent.com/107069287/187286909-8de3da02-e6a8-4f02-aae9-ffd133c8aca2.png)
![Task-02-photo-21](https://user-images.githubusercontent.com/107069287/187286913-ccf84787-a606-4569-849f-21487c107cdd.png)
 
 Após a criação do grupo iremos adicionar como um membro de associação dinâmica: 

Iremos acessar o grupo criado: 

![Task-02-photo-22](https://user-images.githubusercontent.com/107069287/187288320-4b1f7ce6-6620-47ef-bae3-11d52a288a6f.png)
![Task-02-photo-23](https://user-images.githubusercontent.com/107069287/187288325-7ee82a5d-a65d-4935-b7ad-1f20fe659faa.png)
 
 E iremos adicionar ele como um membro de um grupo dinâmico: 

![Task-02-photo-24](https://user-images.githubusercontent.com/107069287/187288428-b32e9b4f-a032-4242-8613-b0e25d1a836b.png)

Antes de adiciona-lo ao grupo precisamos criar uma query para esse grupo: 

Clique em adddynamic query: 

![Task-02-photo-25](https://user-images.githubusercontent.com/107069287/187289028-2dd1ccdf-7269-40ac-8a18-52eb62816e69.png)
![Task-02-photo-26](https://user-images.githubusercontent.com/107069287/187289034-241d2d39-68f1-4332-9438-a2875ad9d0b6.png)
 
 Em seguida crie a query conforme a imagem abaixo: 
 
 ![Task-02-photo-27](https://user-images.githubusercontent.com/107069287/187289516-faf5623e-878b-4354-b7cb-c162fa91d467.png)
 
 Feito essa etapa clique em Save nas duas etapas seguintes. 
 
 Na sequência criaremos o segundo grupo. 
 
 Iremos novamente no Active Directory, acessaremos a aba groups e criaremos nosso segundo grupo: 

![Task-02-photo-28](https://user-images.githubusercontent.com/107069287/187290108-9e72082e-c753-4c93-bbf9-79ee92bcaaa6.png)
 
 Criaremos o grupo com os parametros descrito na imagem: 

![Task-02-photo-29](https://user-images.githubusercontent.com/107069287/187290539-4996ea15-bca9-4ded-98f4-a6b7650a5e5c.png)
 
Adicionaremos uma nova query: 

![Task-02-photo-30](https://user-images.githubusercontent.com/107069287/187290995-960d0f3c-4d35-49f5-8603-f52c55121da9.png)
 
 Em seguida daremos o create. 
 
 Após o processo aguardar entre 3 a 5 minutos para fazer as associações. 
 
 Revisar a associação dos usuários e seguir para a próxima Task. 








 





 
