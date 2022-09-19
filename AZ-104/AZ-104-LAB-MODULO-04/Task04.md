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

Em Overview note que um ip público foi associado a placa de rede: 

![image](https://user-images.githubusercontent.com/107069287/191086453-b0a7f836-cbfc-48c7-a112-8d6352b61a5b.png)

Na sequência iremos repetir o processo para a próxima máquina. 

Vamos acessar novamente o resource Groups e em seguida, em Overview, vamos acessa a nossa segunda placa de rede: 

![image](https://user-images.githubusercontent.com/107069287/191086834-ea2b96c2-dfd8-4f17-be43-c03a44af1940.png)

![image](https://user-images.githubusercontent.com/107069287/191086898-89fd047c-8cba-4758-af52-cd597b19ada5.png)

Vá novamente até a opção IP configurations, na sessão Settings: 

![image](https://user-images.githubusercontent.com/107069287/191087277-62481bfd-547d-405f-bfeb-b9f9bdeda9bc.png)

Em seguida clique em ipconfig: 

![image](https://user-images.githubusercontent.com/107069287/191087569-e9633182-6d71-42c2-a20a-fb4493586107.png)

Vamos criar um ip público para essa máquina. 

Em public IP Address, clique em Associate e em seguida clique em Create New: 

![image](https://user-images.githubusercontent.com/107069287/191088466-d00844cf-c5ff-4181-8020-7bf33b5c9970.png)

Configuraremos conforme o exemplo anterior, alterando apenas as informações conforme a tabela acima: 

![image](https://user-images.githubusercontent.com/107069287/191088924-0e914ae1-9fa1-49ac-b595-023718ce4274.png)

Clique em Ok e em seguida Save. 

Vá até o portal, no campo de pesquisa busque por virtual machine:

![image](https://user-images.githubusercontent.com/107069287/191089979-8d1c1036-0e67-4027-82af-aa02476c7324.png)

Clique na VM az104-04-vm1 que criamos: 

![image](https://user-images.githubusercontent.com/107069287/191090135-9cc4aeb4-34a5-4717-a67b-e894095106ce.png)

Em Overview, note que a máquina já está associada a um IP Público: 

![image](https://user-images.githubusercontent.com/107069287/191090284-d6cd31bb-8895-4a4d-8e49-9ce8cbd2d64b.png)

```
Nota: Caso queira de maneira optativa tente fazer os acessos as duas máquinas por conexão RDP. Note que os acessos não estão liberados. Isso está ocorrendo pois não atribuímos nenhuma regra de acesso ao NSG.
```

Nesta etapa iremos criar uma regra para o NSG. 

Volte para a home do Azure e no campo de pesquisa digite Resource Group: 

![image](https://user-images.githubusercontent.com/107069287/191093707-1e0fc00d-4c1a-4e0f-936e-a15a7c033871.png)

Clique novamente em RG-MOD04:

![image](https://user-images.githubusercontent.com/107069287/191093863-a34963b6-940a-4e35-a9d3-3158f4745b82.png)

Em Overview, vamos clicar na NSG que criamos: 

![image](https://user-images.githubusercontent.com/107069287/191094030-f7b3804d-7589-474c-b3ab-0b6dac0ecc75.png)

Associe as subnets que criamos, clique em subnet e depois associate: 

![image](https://user-images.githubusercontent.com/107069287/191094944-600b87b3-f8ec-42db-a327-4d481478f0e0.png)

Associe as duas subnets que criamos a essa NSG. 

Em seguida, clique em inbound security rules no campo Settings: 

![image](https://user-images.githubusercontent.com/107069287/191094199-66f17c07-b33f-427a-804a-04d45fa39053.png)

Em seguida clique em + Add: 

![image](https://user-images.githubusercontent.com/107069287/191094314-eaaf01f8-3987-4c3f-bed6-ac32f5ed1df4.png)

Vamos criar a regra de liberação de acesso a porta 3389 conforme a imagem abaixo: <br>
*note que iremos restringir o acesso apenas para os ips das máquinas*

![image](https://user-images.githubusercontent.com/107069287/191096421-f576c608-5e7b-42e2-b38d-c899e41623f8.png)

Em seguida clique em Add. 

``
OBS: Sempre altere a prioridade da regra para um valor que deixe margem para adicionar outras regras no futuro. Note que os valores começam em 100, busque sempre valores com espaço para criar outras regras no futuro. Ex: 500. 
``

Teste o acesso RDP das máquinas utilizando o IP público de cada uma. 

*Nota: O usuário e senha para este laboratório das máquinas estão no arquivo parameters, deixo essa etapa como desafio para acostumarmos com a interpretação do arquivo .json* 

Feito essas etapas concluímos a atividade deste laboratório. 


