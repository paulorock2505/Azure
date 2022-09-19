<h2>Lab 04 - Implement Virtual Networking</h2>
 
<h3>Task 6: Configurar o DNS do Azure para resolução de nomes externos</h3>

Validar o domínio: https://www.godaddy.com/domains/domain-name-search

<table border="1">    
  <tr>
    <th colspan="1">DNS Externo</th> 
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
    <th colspan="1">Registro VM0</th> 
</table>

<table border="1">    
  <tr>
    <th colspan="1">Setting</th>  	              
    <th colspan="2">Value</th>
  </tr>
<td>Name</td>
    <td>az104-04-vm0</td>
  </tr>
  <tr>
    <td>Type</td>
    <td>A</td>
  </tr>
   <tr>
    <td>TTL</td>
    <td>1</td>
  </tr>
   <tr>
    <td>TTL unit</td>
    <td>Hours</td>
  </tr>
   <tr>
    <td>Ip address</td>
    <td>the public IP address of az104-04-vm0</td>
  </tr>
  </table>

  <table border="1">    
  <tr>
    <th colspan="1">Registro VM1</th> 
</table>

<table border="1">    
  <tr>
    <th colspan="1">Setting</th>  	              
    <th colspan="2">Value</th>
  </tr>
<td>Name</td>
    <td>az104-04-vm1</td>
  </tr>
  <tr>
    <td>Type</td>
    <td>A</td>
  </tr>
   <tr>
    <td>TTL</td>
    <td>1</td>
  </tr>
   <tr>
    <td>TTL unit</td>
    <td>Hours</td>
  </tr>
   <tr>
    <td>Ip address</td>
    <td>the public IP address of az104-04-vm0</td>
  </tr>
  </table>

  No portal, pesquise por DNS Zone: 

  ![image](https://user-images.githubusercontent.com/107069287/191110424-2da3edd6-4ef3-445d-bf82-0626783a9476.png)

  Clique em + Create: 

  ![image](https://user-images.githubusercontent.com/107069287/191110542-35887928-78e1-4979-abf4-25677259b4bc.png)

  Configure o Resource Group e dominio (personalizado)

  ![image](https://user-images.githubusercontent.com/107069287/191110837-cef105a6-df11-4c49-8361-a03d72a77fac.png)

  Clique em Next. 

  Configure as TAGs como fizemos na atividade anterior: 

  ![image](https://user-images.githubusercontent.com/107069287/191110986-73d421b8-23af-4953-a57f-d6fd0617d9fe.png)

  Depois clique em Review + Create e em seguida Create. 

  Após o término clique em Go to Resource. 

  Abra uma nova guia, no portal, pesquise por Virtual Machine: 

  ![image](https://user-images.githubusercontent.com/107069287/191112129-e697591c-f56d-4479-9cc5-f12458303cb3.png)

  Anote o hostname e o IP público de cada máquina em um bloco de notas: 

  ![image](https://user-images.githubusercontent.com/107069287/191112335-f8ce83b9-626a-4495-ab57-420e8ef1a886.png)

  Caso não consiga visualizar, acesse cada uma delas e na tela Overview anote as informações: 

  ![image](https://user-images.githubusercontent.com/107069287/191112502-d37e2432-4374-4b21-97e8-3be8119f0bf6.png)

  Volte para aba anterior e com as informações em mãos vamos adicionar as máquinas no nosso registro. 

  Clique em + Record Set: 

  ![image](https://user-images.githubusercontent.com/107069287/191112937-d1596668-d4ba-4870-a2d9-ac4b2e0540c0.png)

  Adicione os registros conforme nossa tabela acima: 

  ![image](https://user-images.githubusercontent.com/107069287/191113104-459b4bd1-baf3-4613-8d5d-356d3ccc1de3.png)

 Em seguida clique em Ok. 

 Faça a mesma etapa para a segunda máquina: 

 ![image](https://user-images.githubusercontent.com/107069287/191113404-a204e529-4057-4756-aab5-5eae315e6445.png)

 Clique em ok. 

 *Como desafio final, acesse o Cloudshell e faça os testes abaixo:* <br>
 **Nota: Utilize os endereços apontados na opção Value no Overview**

```
nslookup az104-04-vm0.alpatec.com.br ns1-06.azure-dns.com
nslookup az104-04-vm1.alpatec.com.br ns1-06.azure-dns.com
```
*Caso no teste a resposta esteja apontado para o ip público de cada máquina a atividade foi concluida com sucesso.*

Ao término remova todos os recursos com o comando abaixo: 

```
Get-AzResourceGroup -Name 'RG-MOD04' | Remove-AzResourceGroup -Force -AsJob
```
