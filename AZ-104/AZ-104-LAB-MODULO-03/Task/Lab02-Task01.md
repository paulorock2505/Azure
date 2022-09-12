<h2>Lab 02 - Manage Azure resources with templates</h2> 

<h3>Lab Scenario</h3> 

Agora que você explorou os recursos básicos de administração do Azure associados ao provisionamento de recursos e à organização com base em grupos de recursos usando o portal do Azure, é necessário executar a tarefa equivalente usando os modelos do Azure Resource Manager. 

<h3>Objetivos:</h3>

<table border="1">    
  <tr>
    <th colspan="1">Tarefa 1:</th>  	              
    <th colspan="2">Implante um modelo ARM usando um deploy seu como base.</th>
  </tr>
<td>Tarefa 2:</td>
    <td>Implante recursos através de um ARM diretamente do GitHub.</td>
  </tr>
 </table>
 
 <table border="1">    
  <tr>
    <th colspan="1">Resource Group</th> 
</table>

<table border="1">    
  <tr>
    <th colspan="1">Setting</th>  	              
    <th colspan="2">Value</th>
  </tr>
<td>Resource Group</td>
    <td>RG-LAB-01</td>
  </tr>
  <tr>
    <td>Region </td>
    <td>East US 2</td>
  </tr>
  <td>Name</td>
    <td>VM-ARM-01</td>
  </tr>
  <tr>
    <td>Image</td>
    <td>Linux Ubuntu</td>
  </tr>
  <tr>
    <td>Size</td>
    <td>B2s</td>
  </tr>
 </table>
 <h6><i>OBS: Para este Laboratório, utilizaremos os mesmos Grupos de Recursos das tasks anteriores.</i></h6>

No portal do azure, no campo de pesquisa, digite Resource Groups:

![image](https://user-images.githubusercontent.com/107069287/189681759-ed7d2108-5464-4dee-adb7-0e8985e488db.png)

Verifique os grupos de recursos criados: 

![image](https://user-images.githubusercontent.com/107069287/189683287-171e9d44-c1ac-41d5-a470-d26205a51479.png)

Na sequência iremos criar as máquinas virtuais que serão utilizadas nesse laboratório. 

Vá até a página inicial do Azure, no campo de pesquisa digite Virtual Machines: 

![image](https://user-images.githubusercontent.com/107069287/189683533-ed1bd2aa-d8f8-4074-aed8-9d19583487fd.png)

Em virtual Machine, clique em + Create e em seguida Azure Virtual Machine: 

![image](https://user-images.githubusercontent.com/107069287/189683823-7cb99cb3-2e34-4be3-9747-acdacfb9f58b.png)

Vamos alterar preencher os campos seguindo o modelo adotado: 
- Em Resource Group utilizaremos o RG-LAB-01; 
- Em Virtual Machine Name utilizaremos o nome VM-ARM01
- Image pesquisaremos em See All Images por Ubuntu 18.04 gen2; 
- Size utilizaremos o B2s 
- Utilizaremos em authentication type a opção password
- Por fim criaremos um usuário e senha para o administrador 

Veja imagem abaixo: 

![image](https://user-images.githubusercontent.com/107069287/189688910-d68da61b-62e1-4d0e-bcc1-f594a10329b3.png)
![image](https://user-images.githubusercontent.com/107069287/189685095-8a7d8519-f75b-4a05-a76e-acb7943583b2.png)
![image](https://user-images.githubusercontent.com/107069287/189685404-bde9c515-a6ca-40cc-9fac-bf9e3e8e35d0.png)

Clique em Next. 

Na opção de discos, não iremos fazer nenhuma alteração, manteremos as opções Default: 

![image](https://user-images.githubusercontent.com/107069287/189686147-d885a92e-8292-4a85-bebb-9946fd5098b4.png)

Clique em Next. 

Em Networking, novamente não iremos fazer nenhuma alteração e manteremos as opções Default:

![image](https://user-images.githubusercontent.com/107069287/189686516-3997961e-73e6-45d9-a242-ed444df9a3fe.png)

Clique em Next.

![image](https://user-images.githubusercontent.com/107069287/189687164-d79fd555-6228-4719-bdda-c0901c4be72b.png)

![image](https://user-images.githubusercontent.com/107069287/189686719-8198d8a5-9064-4b41-a6b1-64b1804f5fd2.png)

Clique em Next.

Na opção Monitoring, iremos desabilitar o boot diagnostics, clique em Disable: 

![image](https://user-images.githubusercontent.com/107069287/189687007-6a495303-94b1-4d0d-85f3-e8bfd50a92f0.png)

Clique em Next. 

Em Advanced, novamente não iremos fazer nenhuma alteração e manteremos as opções Default:

![image](https://user-images.githubusercontent.com/107069287/189687294-34a90894-d075-465d-b3f8-c2db2cc94e45.png)

Em Tags, colocaremos o padrão conforme a imagem: 
- Name Modulo 
- Value MOD03

![image](https://user-images.githubusercontent.com/107069287/189687551-18e0608b-3655-4334-b8f7-5cf41936dc9f.png)

Clique em Next Review + Create e em seguida Create para criarmos a máquina. 

Antes de irmos par o Recurso, na tela de criação do Recurso, iremos fazer o download do Template: 

![image](https://user-images.githubusercontent.com/107069287/189710631-a68352da-46d4-4e7b-82af-285f00aa816b.png)

Também adicionaremos o template em nossa biblioteca. Clique em Template: 

![image](https://user-images.githubusercontent.com/107069287/189715054-3d3af519-c447-4fae-976d-672b3d295206.png)

Clique em Add to library:

Preencha os campos name, Resource Group, neste exemplo coloquei com o RG-LAB-01 e version (v1, 1.0, etc): 

![image](https://user-images.githubusercontent.com/107069287/189715766-c219d72b-e487-4b68-b92c-bc83455930ca.png)
![image](https://user-images.githubusercontent.com/107069287/189715789-b3baf2a2-5c41-4390-8a5a-e81ba7ad3037.png)

Na tela inicial do portal, no campo de pesquisa, digite template: 

![image](https://user-images.githubusercontent.com/107069287/189713871-4bc574b4-9732-4eab-a4c9-39c87019f062.png)

Em seguida clique em create: 

![image](https://user-images.githubusercontent.com/107069287/189713953-ac1eae1a-e33a-41bc-b6b9-292ab5584350.png)

Clique em Next. 


Na próxima etapa, podemos customizar nosso template da forma que quisermos, nesse exemplo mantive o padrão do template: 

![image](https://user-images.githubusercontent.com/107069287/189715997-95c8e43c-0ee6-4ded-98a6-79369ea511bb.png)

Em tags mantemos os parâmetros abaixo: 

![image](https://user-images.githubusercontent.com/107069287/189716155-cae681a2-093e-48c1-bfad-1f02b3a701a3.png)

Clique em Review + Create e em seguida Create. 

Neste exemplo vamos salvar o template baseado nos arquivos que fizemos o download: 

No portal, no campo de pesquisa digite templates: 

![image](https://user-images.githubusercontent.com/107069287/189718847-247ba9ae-4c68-4512-888b-9d8bf5c8cd90.png)

Clique nos ... (3 pontos) na lateral do template que acabamos de criar e na sequência clique em edit:

![image](https://user-images.githubusercontent.com/107069287/189719141-43144998-e168-42ad-add5-8659ffd872ef.png)

Abra o template em um editor de texto da sua preferência (no exemplo utilizei o Visual Studio) copie o código todo: 

![image](https://user-images.githubusercontent.com/107069287/189719329-0ea96e1e-be95-4685-97dc-9c6ff3e0e65e.png)

No portal do Azure clique em Arm Template e em seguida cole o código e seguida clique em Save: 

![image](https://user-images.githubusercontent.com/107069287/189719496-ed1c51dc-b6d4-4ed0-ae55-4ee3267afaf6.png)



Finalizado esta etapa, iremos fazer o deploy da máquina a partir do template que geramos. 



















