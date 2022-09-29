# AZ-104-LAB-MOD-05

 <h2>Lab 05a - Configuração de VPN</h2> <br>

 ***Tarefa 1:***  
    *Implementar Azure Load Balancer.*

<table border="1">    
  <tr>
    <th colspan="1">VNET</th> 
</table>

<table border="1">    
  <tr>
    <th colspan="1">Setting</th>  	              
    <th colspan="2">Value</th>
  </tr>
<td>Resource Group</td>
    <td>RG-AZ104</td>
  </tr>
  <tr>
    <td>Region </td>
    <td>East US</td>
  </tr>
  <td>Vnet</td>
    <td>VNET-AZ104 (10.10.0.0/22)</td>
  </tr>
  <tr>
    <td>Subnet</td>
    <td>SUB-01 (10.10.0.0/24)</td>
  </tr>
    <tr>
    <td>Subnet</td>
    <td>SUB-02 (10.10.1.0/24)</td>
  </tr>
    <tr>
    <td>NSG</td>
    <td>NSG-AZ104-06</td>
  </tr>
 </table> 

Acesse o portal do Azure, e no campo de pesquisa, digite Resource Groups: 

![image](https://user-images.githubusercontent.com/107069287/193047057-bd654cce-953d-43fd-8bd2-05a2f2b8ac85.png)

Em seguida clique em + Create: 

![image](https://user-images.githubusercontent.com/107069287/193047203-4beeea27-44a8-4ca2-ad5b-e10fd16771ea.png)

Em seguida vamos preencher as insformações conforme descriminado na tabela acima: 

![image](https://user-images.githubusercontent.com/107069287/193048276-c57acd1c-8e41-43ac-bd69-706c9f8930d4.png)

Clique em Next. 

Vamos preencher a TAG conforme a imagem abaixo: 

![image](https://user-images.githubusercontent.com/107069287/193048686-8766a076-6330-4889-a97c-3eed5be5bb7e.png)

Em seguida clique em Review + Create e depois em Create para criarmos o grupo de recursos. 

Na próxima etapa iremos criar a Virtual Network. 

Vá até a home do portal novamente, no campo de pesquisa digite Virtual Network: 

![image](https://user-images.githubusercontent.com/107069287/193049598-0d15f827-f2ba-4f78-99d6-4ec6e0eb8d2d.png)

Clique em + Create: 

![image](https://user-images.githubusercontent.com/107069287/193055765-1584835a-bc52-4516-b620-2dcd7cce8693.png)

Em basics, escolha o resource group que acabamos de criar e preencha o campo virtual name de acordo com o escopo da tabela acima: 

![image](https://user-images.githubusercontent.com/107069287/193056452-da049d2a-9951-4134-b716-f20ca781458b.png)

Clique em Next. 

Em security não iremos fazer nenhuma alteração, apenas clicar em Next: 

![image](https://user-images.githubusercontent.com/107069287/193056786-52aa75c0-2191-40c1-a977-4673cc8d5605.png)

Em IP Address, vamos deletar o range que está configurado por padrão. Clique em ... e em seguida Delete Address Space: 

![image](https://user-images.githubusercontent.com/107069287/193057115-88be7b8f-2119-4dfe-98ea-f096c711f971.png)

Em seguida clique em Add an IP Address Space: 

![image](https://user-images.githubusercontent.com/107069287/193057329-6312a826-122b-442e-8ed3-81b2776098d5.png)

Configure o endereço de IP e a máscara conforme a imagem abaixo: 

![image](https://user-images.githubusercontent.com/107069287/193057813-c61ab4ad-5898-447c-b54a-a1c0a89593a1.png)

Clique em Add. 

Em seguida clique em + Add a subnet para adicionarmos a subnet: 

![image](https://user-images.githubusercontent.com/107069287/193058230-bae91cde-368e-4965-94f4-6845fc138c6b.png)

Preencha conforme o padrão estabelecido na tabela acima: 

![image](https://user-images.githubusercontent.com/107069287/193058551-4ac2bbf3-0e7d-4239-88a9-c84b3424081c.png)

Clique em Add. 

Novamente clique em + Add a subnet para adicionarmos a segunda subnet: 

![image](https://user-images.githubusercontent.com/107069287/193059016-addc6306-8360-4387-82ac-8eb8b5d4867f.png)

Preencha conforme o padrão estabelecido na tabela acima:

![image](https://user-images.githubusercontent.com/107069287/193059426-3c7a6830-60b0-4c69-9465-ae4f7659be66.png)

Em seguida clique em Add. 

Em seguida clique em Next. 

Em TAG preencha conforme a imagem abaixo: 

![image](https://user-images.githubusercontent.com/107069287/193060024-8d39d74c-9132-4617-9812-91e91dded4d0.png)

Em seguida clique em Review + Create e depois create para criarmos a VNET para o nosso Laboratório. 





 
 