# AZ-104-LAB-MOD-02
Repositório do Laboratório do módulo 01 para o exame de certificação AZ-104. (Credits by TFTEC)

<h3>Lab 02b - Manage Governance via Azure Policy</h3>

Task 01 Criar e associar tags via the Azure Portal. 

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

Abra o portal do Azure e procure por Resource Group: 

![image](https://user-images.githubusercontent.com/107069287/188443099-ea6a2152-21f3-41ee-a07a-cb469fe30aa2.png)

Acesse o Resource Group que criamos (Neste exemplo criamos um Resource Group apenas para armazenar a storage do cloudshell): 

![image](https://user-images.githubusercontent.com/107069287/188443844-87f53f2d-12e1-48dc-b0ca-d7871eaf5aaa.png)

Em Overview, no campo TAGs clique em Click here to add tags: 

![image](https://user-images.githubusercontent.com/107069287/188445368-3858fb3f-1d07-46d3-9cdb-37046251a1b2.png)


Preencha os campos conforme a imagem abaixo e clique em save: 

![image](https://user-images.githubusercontent.com/107069287/188445409-882f2744-d37d-4e2b-8061-b20eed25a1f3.png)

OBS: Quando criamos a TAG no Resource Group, conforme demonstrado neste exemplo, os objetos filhos não herdam as TAGs criadas anteriormente. Ou seja, qualquer outro recurso que for criado pode ser adicionado ou não uma TAG de qualquer valor. 








