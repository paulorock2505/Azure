# AZ-104-LAB-MOD-02
Repositório do Laboratório do módulo 01 para o exame de certificação AZ-104. (Credits by TFTEC)

Task 02 Forçar tagging via an Azure policy. 

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
 
 No portal do Azure, no campo de pesquisa procure pelo item policy: 

![image](https://user-images.githubusercontent.com/107069287/188447120-420934ae-1140-449b-8af3-0296b7950985.png)

Neste exemplo iremos criar uma policy que force a utilização da TAG, no entanto sem aplicar uma remediação. 

Dentro de policy clique em Definitions: 

![image](https://user-images.githubusercontent.com/107069287/188447475-04b94a1c-91e2-48f0-b841-15422029b684.png)

Ajuste o filtro do Definition Type para Policy: 

![image](https://user-images.githubusercontent.com/107069287/188448119-8878166d-a1f1-435c-9a78-286ff44d123e.png)

OBS: Neste exemplo só iremos utilizar policy e iremos excluir as Initiative Policy. 

Ajuste também o filtro Category. Desmarque a a opção Select ALL e deixe apenas marcado o campo da TAG: 

![image](https://user-images.githubusercontent.com/107069287/188448664-948e014f-2207-4940-beae-53b530d950e5.png)

Na opção Require a tag and its value on resources, no ícone ... clique em Assign: 

![image](https://user-images.githubusercontent.com/107069287/188449369-22c7e91c-6e73-4f2e-b29a-becdee8ef9dd.png)

No campo Scope, aplique a politica para o tenant root conforme mostrado na imagem: 

![image](https://user-images.githubusercontent.com/107069287/188450529-69c42e33-6258-42b4-b092-87bb661aa30a.png)

OBS: Podemos aplicar a política para todos os itens da assinatura, bem como atribuirmos de maneira granular, apenas no resource group ou assinaturas especificas que estejam na sua subscrição. 

No campo exclusão, não iremos atribuir nada, mas vale salientar que esse campo é muito importante pois define quais serão os grupos que não pertceram a essa política.

Ajuste o nome da TAG conforme a descrição da politica: 

![image](https://user-images.githubusercontent.com/107069287/188451467-9f605473-64eb-45c2-937c-11f30282a6e2.png)

Clique em Next. 

No campo Parameters, preencha o campo conforme a imagem abaixo: 

![image](https://user-images.githubusercontent.com/107069287/188451702-7680e037-bb22-463c-8a27-d0f8f4e30765.png)

Clique em Next. 

No campo remediation, não precisa preencher nada pois não iremos criar nenhuma politica de remediação para este exemplo. 

![image](https://user-images.githubusercontent.com/107069287/188451912-855a743b-a75c-4dde-bf6e-6ff5fdbea755.png)

Clique em Review + create e em seguida Create para criar a policy.

Na sequência crie um recusro dentro da RG que aplicamos a policy e valide a politica recém criada. 










 
