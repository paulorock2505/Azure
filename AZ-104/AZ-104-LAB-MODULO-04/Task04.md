<h2>Lab 04 - Implement Virtual Networking</h2>
 
<h3>Task 4: Configurar endereços IP públicos e privados das VMs do Azure</h3>

<table border="1">    
  <tr>
    <th colspan="1">Public IP</th> 
</table>

<table border="1">    
  <tr>
    <th colspan="1">Setting</th>  	              
    <th colspan="2">Value</th>
  </tr>
<td>Name</td>
    <td>az104-04-pip</td>
  </tr>
  <tr>
    <td>SKU</td>
    <td>Standard</td>
  </tr>
  </table>
   
<table border="1">    
  <tr>
    <th colspan="1">Public IP</th> 
</table>

<table border="1">    
  <tr>
    <th colspan="1">Setting</th>  	              
    <th colspan="2">Value</th>
  </tr>
<td>Name</td>
    <td>az104-04-pip1</td>
  </tr>
  <tr>
    <td>SKU</td>
    <td>Standard</td>
  </tr>
  <tr>
  </table>


No portal do Azure, no campo de pesquisa, busque por resource groups: 

![image](https://user-images.githubusercontent.com/107069287/191070172-8d0c3dda-b833-4aac-bc15-227251ee7117.png)

Acesse o grupo de recursos que criamos, RG-MOD04:

![image](https://user-images.githubusercontent.com/107069287/191070572-37bd8860-5b02-496a-b64f-27d6dd9772cf.png)

Nessa etapa, iremos criar os IPs públicos das nossas máquinas. 
A maneira mais prática é utilizando as próprias interfaces de rede: 

Iremos começar essa configuração pela primeira nic, em Overview acesse a az104-04-nic0:

![image](https://user-images.githubusercontent.com/107069287/191071144-228e9b81-d5c5-42ae-85f4-01edb2e7edbe.png)

Vá até a opção IP configurations, na sessão Settings: 

![image](https://user-images.githubusercontent.com/107069287/191071985-1964ebdb-c56f-4ef4-9357-4cdad1b8c71a.png)

Em seguida clique em ipconfig: 

![image](https://user-images.githubusercontent.com/107069287/191072297-e81d9f54-13fc-466e-b73e-ba7b40d21366.png)

Nesta opção podemos associar ou criarmos um ip público para essa máquina. 
Neste exemplo iremos criar um novo IP público. 

Clique em Associate e em seguida Create New: 

![image](https://user-images.githubusercontent.com/107069287/191072680-c74dfb67-d38f-4f78-a804-01a3d1e6c31b.png)

Neste caso iremos configurar conforme as definições descritas em nossa tabela: 

![image](https://user-images.githubusercontent.com/107069287/191072915-6f7506cd-4584-4f2e-ab01-ab043301ff0f.png)

Clique em Ok e na sequência clique em Save. 

