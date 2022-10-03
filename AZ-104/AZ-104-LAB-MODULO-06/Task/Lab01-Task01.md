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

Após essa etapa, iremos criar uma NSG para a Virtual Network que acabamos de criar. 

Vá até a home do portal do Azure, no campo de pesquisa digite Network Security Group e acesse a área: 

![image](https://user-images.githubusercontent.com/107069287/193121205-afdb6899-d7ca-44e6-9c53-38b0f55a2139.png)

Em seguida clique em + Create: 

![image](https://user-images.githubusercontent.com/107069287/193121529-372d026d-3ce1-40a2-bba3-356f8e4cea71.png)

Na sequência iremos configurar conforme a nossa tabela acima: 

![image](https://user-images.githubusercontent.com/107069287/193121738-855ff439-843a-4486-ac29-b4a9a2b3c086.png)

Selecione o Resource Group que criamos e nomeie conforme a imagem. Após esta etapa clique em Next. 

Preencha as TAGs conforme o padrão que já estamos utilizando: 

![image](https://user-images.githubusercontent.com/107069287/193122047-9f8b7962-47fa-4788-9f18-0058ce8e4df2.png)

Clique em seguida em Review + Create e em seguida Create. 

Na sequência clique em Go to Resources: 

![image](https://user-images.githubusercontent.com/107069287/193122620-15799014-f2e4-49a9-87b9-395035e35bd6.png)

Vá até o campo settings e clique em subnets: 

![image](https://user-images.githubusercontent.com/107069287/193122767-3ce915c9-99ec-4e92-9da6-2819df3d049e.png)

Clique em + Associate e vamos associas as duas subnets que criamos: 

![image](https://user-images.githubusercontent.com/107069287/193122992-147349ed-f0fd-42f9-8089-bcecda20e081.png)

Clique em Ok para a primeira subnet associada e em seguida adicione a próxima: 

![image](https://user-images.githubusercontent.com/107069287/193123205-0a072cf9-0968-426b-a5d8-118ecc0c8f33.png)

Clique em Ok novamernte. 

Feito essa etapa, o próximo passo será criar as Virtual Machines. 

Vá a home do azure, no campo de pesquisa digite Virtual Machine: 

![image](https://user-images.githubusercontent.com/107069287/193123668-1cd06f25-072f-43f1-b603-5c93ee29e949.png)

Em seguida clique em + Create e em seguida Azure Virtual Machine: 

![image](https://user-images.githubusercontent.com/107069287/193123855-b7856bb8-9dcd-424c-badf-94ce0eb1a775.png)

No campo Basics, vamos criar as Virtual Machines seguido os parâmetros conforme a imagem abaixo: 

![image](https://user-images.githubusercontent.com/107069287/193580208-740c0ceb-6c1a-45f9-8c06-884aea4f2b59.png)

Adicione o usuário e senha de sua preferência: 

![image](https://user-images.githubusercontent.com/107069287/193580443-566cfbc7-5026-404c-a0e4-ffe8a1644cd0.png)

![image](https://user-images.githubusercontent.com/107069287/193580555-c740b3da-9ba6-4e8a-95fe-b3f5c59de8d4.png)

Em seguida clique em Next. 

Em Disks vamos manter o padrão sugerido pelo próprio Azure: 

![image](https://user-images.githubusercontent.com/107069287/193581091-7c4ccd22-e4bf-4151-987c-5f750dd0a11c.png)

Clique em Next. 

Em Network, para esse laboratório, não iremos configurar o ip público da máquina. Vamos configurar seguindo o modelo abaixo: 

![image](https://user-images.githubusercontent.com/107069287/193581677-4a36621e-a4b0-41cb-a1eb-05d07db8c88e.png)

Em seguida clique em Next. 

Em management, não iremos fazer nenhuma alteração: 

![image](https://user-images.githubusercontent.com/107069287/193581807-60a552bb-23d7-4384-94fa-7610bdcdf655.png)

Clique em Next. 

Em monitoring clique em Disable Boot Diagnostics: 

![image](https://user-images.githubusercontent.com/107069287/193582067-4a58188b-0a4a-440e-b7f1-68e610004d02.png)

Clique em Next. 

Am Advanced não iremos fazer nenhuma alteração: 

![image](https://user-images.githubusercontent.com/107069287/193582206-74376076-f8fd-40c2-9df9-3e0b2f04b904.png)

Clique em Next. 

Em TAGs, preencha conforme a imagem abaixo: 

![image](https://user-images.githubusercontent.com/107069287/193582423-d04955b4-2587-41d4-b627-3a28da4c9184.png)

Em seguida clique em Review + Create e em seguida Create. 

Após essa etapa, vamos criar a segunda máquina virtual para este laboratório. 

Volte ao home do Azure, no campo de pesquisa digite Virtual Machine: 

![image](https://user-images.githubusercontent.com/107069287/193583298-fe8be106-4629-4f0f-88c8-79f11d788add.png)

Clique em + Create e em seguida Azure Virtual Machines: 

![image](https://user-images.githubusercontent.com/107069287/193583529-6d46f061-3a6d-452b-9d21-d9cdc3ccbd02.png)

Em seguida vamos configurar a máquina seguindo os parâmetros indicado para este Laboratório. Em basics configure conforme os parâmetros mostrado abaixo: 

![image](https://user-images.githubusercontent.com/107069287/193584049-e0b573fb-1ea1-4d03-b73b-df8dcd6dc174.png)

Configure o usuário e senha de sua preferência: 

![image](https://user-images.githubusercontent.com/107069287/193584290-5c58533d-4e46-438a-86d1-e109e9636af9.png)

![image](https://user-images.githubusercontent.com/107069287/193584373-2738c30b-f035-4631-b3b3-460e5b018392.png)

Em seguida clique em Next. 

Em Disks, não vamos fazer nenhuma alteração, vamos manter o mesmo padrão sugerido pelo Azure: 

![image](https://user-images.githubusercontent.com/107069287/193584899-1e6aadaf-a957-40e1-b106-abae9fbefdac.png)

Clique em Next novamente. 

Em Networking iremos selecionar a subnet SUB02 e vamos seguir o padrão de configuração conforme a imagem abaixo: 

![image](https://user-images.githubusercontent.com/107069287/193585336-4106955b-9791-45bb-b795-4500f5e852ab.png)

Clique em Next. 

Em Management, não iremos fazer nenhuma alteração: 

![image](https://user-images.githubusercontent.com/107069287/193585544-fb5c4906-16ae-4068-b8d1-71605519386c.png)

Em seguida clique em Next. 

Em monitoring vamos desabilitar o boot diagnostics: 

![image](https://user-images.githubusercontent.com/107069287/193585960-885bcb5b-1d26-4bd0-ae70-3d570b879471.png)

Clique em Next. 

Em Advanced não iremos fazer nenhuma alteração: 

![image](https://user-images.githubusercontent.com/107069287/193586401-611c68cf-05f6-4b11-af19-adb55bb33ead.png)

Clique em Next novamente. 

Em TAGs, iremos preencher conforme a definição abaixo: 

![image](https://user-images.githubusercontent.com/107069287/193587417-6bd2464e-3d8a-4cf4-8751-636c4d469d0a.png)

Em seguida clique em Review + Create e em seguida Create para criarmos a segunda máquina virtual. 

Em seguida vá até a home do Azure, pesquise novamente por Virtual Machine: 

![image](https://user-images.githubusercontent.com/107069287/193588308-d001da23-1eb4-4cdc-a956-56ab6318a7fb.png)

Clique em VM-01: 

![image](https://user-images.githubusercontent.com/107069287/193588415-0b6dbbcd-b1b0-40ba-9955-2f8448ae0570.png)

Em seguida, no campo Operations, vá em Run Command: 

![image](https://user-images.githubusercontent.com/107069287/193589945-9a3e7f38-035c-497a-b21c-498adbdd3ae8.png)

Em seguida clique em RunPowerShellScript: 

![image](https://user-images.githubusercontent.com/107069287/193590175-3bbd1393-04b8-4b9d-be16-16f3e03ff9f4.png)

Execute o script abaixo: 

![image](https://user-images.githubusercontent.com/107069287/193590569-d05ff27c-c6a4-4012-9126-c912cbca9b11.png)

![image](https://user-images.githubusercontent.com/107069287/193590738-ae2b9b07-d8cc-48c1-ae8e-9888abbc5ca8.png)

Em seguida clique em Run. 

Aguarde até o término do processamento: 

![image](https://user-images.githubusercontent.com/107069287/193591182-348b6b40-7111-424d-8fbc-58bd241f350e.png)

Em seguida vamos fazer o mesmo processo na segunda máquina virtual que criamos. 

Vá novamente a home do Azure e pesquise por Virtual Machines: 

![image](https://user-images.githubusercontent.com/107069287/193591808-94c7be9b-3d78-49ab-be5f-c3016345e58e.png)

Em seguida clique em VM-02: 

![image](https://user-images.githubusercontent.com/107069287/193591923-9109f6ff-fc10-4197-b38a-de93371e9508.png)

Clique novamente em Operations e clique em Run Command: 

![image](https://user-images.githubusercontent.com/107069287/193592176-72144497-6844-4ba4-9add-7b30b057c155.png)

Clique novamente em RunPowerShellScript: 

![image](https://user-images.githubusercontent.com/107069287/193592485-03a02493-200f-4b83-8afb-2651e91f6e4e.png)

E execute o script abaixo: 

![image](https://user-images.githubusercontent.com/107069287/193592595-6f3a7502-3829-4fc6-8253-25f4febeaba7.png)

![image](https://user-images.githubusercontent.com/107069287/193592692-2208ae4a-9802-4048-8ad6-486484e19a6e.png)

Aguarde até o término do processamento. 

![image](https://user-images.githubusercontent.com/107069287/193593146-bd7e5da9-143c-47f5-83d9-96619b64fb35.png)

Terminado essa etapa, estamos com a estrutura pronta. Na sequência iremos agora de fato configurar o Load Balancer. 

Vá até a home do portal e no campo de pesquisa digite Load Balancers: 

![image](https://user-images.githubusercontent.com/107069287/193595578-9a3d8ded-1882-4097-9aba-1a45d5c31d6a.png)

Em seguida vamos em + Create: 

![image](https://user-images.githubusercontent.com/107069287/193599904-e582ab78-453d-45ce-8052-3c604599622f.png)

Em Basics, configure os parametros abaixo conforme a imagem abaixo: 

![image](https://user-images.githubusercontent.com/107069287/193601667-d4c7088d-210c-4308-b328-623d19b1eead.png)

Em seguida clique em next. 

Clique em + Add a frontend IP configuration: 

![image](https://user-images.githubusercontent.com/107069287/193601104-89c7a4bc-8fe2-44cd-a616-d49ad5c244e2.png)

Preencha conforme a imagem abaixo e em seguida em Public IP Address clique em Create New: 

![image](https://user-images.githubusercontent.com/107069287/193602251-e596ac53-ce05-404a-8aec-3679e1b65962.png)

Preencha os parametros conforme a imagem abaixo e clique em Ok. 

![image](https://user-images.githubusercontent.com/107069287/193602636-8faa5824-4d79-4ea5-9c4e-619a9b227b7c.png)

Em seguida clique em Add. 

Em seguida clique em Next. 

Em Backend Pools, clique em + Add a backend pool: 

![image](https://user-images.githubusercontent.com/107069287/193603524-f52a6d45-b6c9-4e8c-9c81-2fc6b52bcb5d.png)

Preencha o campo conforme a imagem e em seguida no campo IP Configuration clique em + Add: 

![image](https://user-images.githubusercontent.com/107069287/193604386-28d266db-5576-4d5d-8f8c-5af75f1c5d55.png)

Marque as 2 VMs que criamos e clique em Add: 

 ![image](https://user-images.githubusercontent.com/107069287/193604646-d8bc6112-c88f-4a31-94c2-b0b40a099db3.png)

Clique em Save: 

![image](https://user-images.githubusercontent.com/107069287/193604769-c8627239-c021-4c37-b88a-a987adb285e9.png)

Clique em Next. 

Em inbound rules clique em + Add a load balancing rule: 

![image](https://user-images.githubusercontent.com/107069287/193605399-7def5176-5e7a-4da3-8902-495ba8f0f4bb.png)

Configure a regra conforme a imagem e em seguida em Health probe, clique em Create New: 

![image](https://user-images.githubusercontent.com/107069287/193605877-f214d980-ce7f-4187-89e5-88c15b535deb.png)

Configure os parâmetros conforme a imagem e em seguida clique em Ok. 

![image](https://user-images.githubusercontent.com/107069287/193606822-0a5621d6-a557-41f6-943c-3ff6d18409da.png)

Em seguida, clique em Add. 

![image](https://user-images.githubusercontent.com/107069287/193607841-c21b3afe-c455-4312-bd9d-ca72ad40d522.png)

Em seguida clique em Next. 

Em Outbound Rules, não faremos nenhuma alteração: 

![image](https://user-images.githubusercontent.com/107069287/193609084-2e695447-57a1-428e-9f17-f930ef2592a1.png)

Clique em Next. 

Em TAGs, preencha conforme o nosso scopo do laboratório: 

 ![image](https://user-images.githubusercontent.com/107069287/193609327-e1d64eb4-2f05-404e-bee1-b2c8d616ad95.png)

Clique em Review + Create e em seguida Create. 

Configurado o Load Balancer, vamos seguir liberando a porta 80 no Network Security Group para que a aplicação esteja habilitada para acessarmos. 

Vá até o home novamente, no campo de pesquisa digite Network Security Group: 

![image](https://user-images.githubusercontent.com/107069287/193633015-3c4e862a-9f7c-4bad-aaf5-a116b67a0a03.png)

Em seguida, clique em NSG-AZ104-06: 

![image](https://user-images.githubusercontent.com/107069287/193633117-d2ba0901-cc1d-460d-b13f-17377286bbf1.png)

Antes, precisamos copiar os IPs privados de cada máquina Virtual que criamos. 

Abra uma nova guia e vá em Virtual Machines: 

![image](https://user-images.githubusercontent.com/107069287/193633567-ba14bf15-f9fe-43aa-8c87-7f7269b0eb19.png)

Acesse a VM-01: 

![image](https://user-images.githubusercontent.com/107069287/193633913-c1c5667e-e3b1-4a43-82d3-e6f19c80afc4.png)

E copie o endereço que está aparecendo em Private IP Address: 

![image](https://user-images.githubusercontent.com/107069287/193634075-f6d73786-41a7-431d-bd5a-c3c1f2e833b6.png)

Salve esse endereço em um bloco de notas e repita o mesmo processo para VM-02. 

Volte até a guia onde está aberto a área do NSG e agora vamos configurar as regras de acesso. 

Na página principal do Network Security Group, vá até o campo settings e clique em Inbound security rules: 

![image](https://user-images.githubusercontent.com/107069287/193634986-3e58c692-0fde-49a8-9a62-39cf3fdcd8d6.png)

Em seguida clique em + Add: 

![image](https://user-images.githubusercontent.com/107069287/193635090-4f029739-f3d6-47e6-a496-9da379c9979c.png)

Configure a regra conforme a imagem abaixo e clique em Add: 

![image](https://user-images.githubusercontent.com/107069287/193635880-bc7ed571-c916-41f3-bb14-8ed714809f8e.png)

Feito essas etapas todo o laboratório foi concluido com sucesso. 

*Tarefa Opcional:* <br>
*- Pegue o IP público das máquinas e abram ele em dois navegadores diferentes para testar o balanceador.* <br>
*- Desligue uma das máquinas e analise a resposta do load balancer.(note o tempo de resposta para enviar as requisições para a outra máquina)*










 
 