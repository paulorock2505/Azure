# AZ-104-LAB-MOD-02
Repositório do Laboratório do módulo 01 para o exame de certificação AZ-104. (Credits by TFTEC)

Lab 01 - Gerenciar identidades do Azure Active Directory 

Task 02 - Criar custom RBAC Roles 

<table border="1">    
  <tr>
    <th colspan="1">RBAC</th> 
</table>

![image](https://user-images.githubusercontent.com/107069287/188203576-3b732bf2-5051-4607-997b-39f1707071bf.png)

Dentro do portal do Azure procure por Management Group no campo de pesquisa: 

![image](https://user-images.githubusercontent.com/107069287/188206817-110c40fa-176b-4caf-8e32-c963cd8079c1.png)

Em management Group, copie o nome que criamos: 

![image](https://user-images.githubusercontent.com/107069287/188206937-730709af-760d-4fba-bbae-6093d5f254bc.png)

E cole no campo selecionado conforme imagem: 

![image](https://user-images.githubusercontent.com/107069287/188207068-7d65d52e-a504-4527-aa5e-44ecadab34b2.png)

 Após essa etapa precisamos do subscription ID. 
 
 Na tela do Management Group, clique no Mangement Group que criamos e acesse a subscription: 

![image](https://user-images.githubusercontent.com/107069287/188208051-dd6642c4-6c76-4044-b2af-3aa8ce0d213b.png)

Dentro do campo subscription em Overview copie o subscription ID: 

![image](https://user-images.githubusercontent.com/107069287/188208155-8c8e0ae4-eb3b-4997-9f36-3d8c50b22193.png)

Cole a subscription ID no arquivo .json conforme a imagem: 

![image](https://user-images.githubusercontent.com/107069287/188208275-851a7498-33a5-4045-b57b-4f7b420088db.png)

Salve o arquivo editado customrbac.json 

Abra o cloud shell no campo superior do portal, é o primeiro item: 

![image](https://user-images.githubusercontent.com/107069287/188208780-f0599046-5428-4c9c-aa64-989d6a16b771.png)

Ao abrir será solicitado que você crie um storage: 

![image](https://user-images.githubusercontent.com/107069287/188209003-7b7e42c1-b71d-4a92-af81-497cd067bade.png)

Iremos escolher nesse caso o PowerShell:

![image](https://user-images.githubusercontent.com/107069287/188209151-4e18b801-617e-440e-87d5-aa487985c0a1.png)

Nesse exemplo iremos utilizar as opções avançadas do cloud shell e iremos definir alguns parâmetros manualmente: 

![image](https://user-images.githubusercontent.com/107069287/188209700-f14cb0f5-7f84-408a-898a-16d0989ba722.png)

Com o cloudshell aberto, ireos fazer o upload do arquivo clicando no botão de transferência ao lado da engrenagem: 

![image](https://user-images.githubusercontent.com/107069287/188210423-483eca07-c5c3-4cf5-8371-b5222d3e3cc3.png)

Clique em carregar: 

![image](https://user-images.githubusercontent.com/107069287/188210488-ab491d90-5308-4d5c-afb0-03197b7ab1a1.png)

Iremos selecionar o arquivo que acabamos de editar e clicamos em abrir: 

![image](https://user-images.githubusercontent.com/107069287/188210570-b75f8014-c8f0-4093-9d9f-65bbde691db2.png)

![image](https://user-images.githubusercontent.com/107069287/188210726-39ccd753-450d-4a4b-83cc-83ad16b7d62e.png)

Após o carregamento do arquivo rodaremos o comando abaixo no cloudshell: 

New-AzRoleDefinition -InputFile $HOME/customrbac.json

O resultado será esse: 

![image](https://user-images.githubusercontent.com/107069287/188211227-456d90d9-c531-450b-9843-6139c91ff6f3.png)

Confira a criação do RBAC: 

Vá em Resource Groups: 

![image](https://user-images.githubusercontent.com/107069287/188211759-a09c06d2-6745-4b38-8a3f-72c6faf8d1f9.png)

Clique no recurso que acabamos de criar RG-RBAC: 

![image](https://user-images.githubusercontent.com/107069287/188211871-64c6c192-859f-4ef4-b920-742044b6a1f7.png)

Em seguida vá até Access Control (IAM): 

![image](https://user-images.githubusercontent.com/107069287/188211983-3640596c-af35-4ae9-a253-3ccfdcd171f2.png)

Vá em Add Role Assigment: 

![image](https://user-images.githubusercontent.com/107069287/188212075-f3c9aec1-59bf-4ccb-af42-1a1d71d384ea.png)

E procure pela role que acabamos de criar "Support Reques Contributor (Custom)"

![image](https://user-images.githubusercontent.com/107069287/188212259-682a9fdd-19bb-4867-8ca7-7d350e1b1f83.png)












  
