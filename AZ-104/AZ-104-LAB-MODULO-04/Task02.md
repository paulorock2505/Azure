<h2>Lab 04 - Implement Virtual Networking</h2>
 
<h3>Task 2: Configurar grupos de segurança de rede (NSG)</h3>

<table border="1">    
  <tr>
    <th colspan="1">NSG</th> 
</table>

<table border="1">    
  <tr>
    <th colspan="1">Setting</th>  	              
    <th colspan="2">Value</th>
  </tr>
<td>NSG</td>
    <td>az104-04-nsg01</td>
  </tr>
  <tr>
    <td>Resource Group</td>
    <td>RG-MOD04</td>
  </tr>
  <tr>
    <td>Region</td>
    <td>East US 2</td>
  </tr>
  <tr>
    <td>Associate</td>
    <td>subnet0</td>
  </tr>
  <tr>
    <td>Associate</td>
    <td>subnet1</td>
  </tr>
 </table> 
 
 Acesse o portal do azure, no campo de pesquisa digite Network Security Group: 

![image](https://user-images.githubusercontent.com/107069287/190701577-3f4749d6-1ace-472f-8a5e-ccbdc4d4e104.png)

Clique em + Create: 

![image](https://user-images.githubusercontent.com/107069287/190701731-566a503c-c796-46d1-b429-d38556f08407.png)

Vamos criar o NSG de agordo com as instruções detalhadas na tabela acima: 

![image](https://user-images.githubusercontent.com/107069287/190701894-cfe18e38-b0e5-44ab-a056-655462fc04c3.png)

Clique em Next. 

No campo TAGs, vamos digitar as informações para mantermos os padrões dos demais Laboratórios: 

![image](https://user-images.githubusercontent.com/107069287/190702037-66b251c7-28e0-4317-842a-9840af1f7626.png)

Clique em Review + Create e em seguida Create para criarmos a NSG. 

Após a criação clique em Go to Resource: 

![image](https://user-images.githubusercontent.com/107069287/190702366-84323feb-e3f3-4c56-a94a-275a00cc86f4.png)

Após a conclusão desta etapa, iremos associar as nossas subnets a NSG que criamos. 

Vá até a opção settings e em seguida clique em subnet: 

![image](https://user-images.githubusercontent.com/107069287/190702733-b9deaf76-5779-487a-9076-d141220fa4ce.png)

Em seguida clique em + Associate: 

![image](https://user-images.githubusercontent.com/107069287/190702824-1f62a27f-8ce9-456d-ac20-6bd768fd7b31.png)

Clique em Virtual Network e escolha a virtual network que criamos: 

![image](https://user-images.githubusercontent.com/107069287/190702975-7be1809b-c837-4c4e-a7b5-8aacdd131ade.png)

Em seguida determine a subnet que iremos utilizar nesse laboratório: 

![image](https://user-images.githubusercontent.com/107069287/190703080-a805f1d9-2d3b-4437-901b-d11883f5808b.png)

Clique em Ok. 

Faça o processo novamente para a subnet1. 

![image](https://user-images.githubusercontent.com/107069287/190703275-227f6741-683a-44ed-8b69-24186c19fdde.png)

![image](https://user-images.githubusercontent.com/107069287/190703360-e1bcc285-86ed-4fea-91ea-dd88b1a44baa.png)

Após essas etapas, a configuração da NSG foi concluída. 












 
