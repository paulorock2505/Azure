# AZ-104-LAB-MOD-03
Repositório do Laboratório do módulo 01 para o exame de certificação AZ-104. (Credits by TFTEC)

<h2>Movendo uma VM de região com o Azure Resource Mover</h3>

<h3>Azure Resource Mover</h3>

Recursos que podem ser movidos: 

- Azure Vms e discos associados 
- NICs
- Availability Sets
- Azure Virtual networks 
- Public IP Address 
- Network Security Groups 
- Internal and public load balancers 
- Azure SQL databases and elastic pools

Etapas para movimentação de recursos entre regiões: 

![image](https://user-images.githubusercontent.com/107069287/189147459-9007a8f1-c108-4e57-a4bf-49062b4d1172.png)

Criação dos recursos: 

No portal do Azure criaremos o primeiro grupo de recursos. 

Acesse o portal e no campo de pesquisa digite Resource Group: 

![image](https://user-images.githubusercontent.com/107069287/189152794-100e6d05-97a3-46b3-9af7-dd8ebde2bd1b.png)

Clique em + Create: 

![image](https://user-images.githubusercontent.com/107069287/189152912-f014c0c9-8246-42a3-8249-3bd53e7dc8e5.png)

Criaremos o recurso com o nome RG-Origem na localização de East US: 

![image](https://user-images.githubusercontent.com/107069287/189153281-c6d22d8b-b773-4c69-9b22-310bb6efa92c.png)

No campo tag não preencheremos nada: 

![image](https://user-images.githubusercontent.com/107069287/189153375-d222a025-0b5e-4519-987b-390e9919d048.png)

Na sequência clique em Next, depois Review + Create e depois create. 

![image](https://user-images.githubusercontent.com/107069287/189153603-092594d1-7448-45e8-85a5-c50adb149af6.png)

Na sequência criaremos o resource group de Destino. 

Ainda dentro da aba Resource Manager, clique + Create: 

![image](https://user-images.githubusercontent.com/107069287/189154065-4aa548af-41aa-46d5-9cbe-e93b852a9903.png)

Crie um Resource Group com nome de RG-Destino e localizado no Brazil South: 

![image](https://user-images.githubusercontent.com/107069287/189154323-a8581132-0ff5-41af-9ecd-6fb7d38db2f2.png)

Clique e Review + Create e em seguida create: 

![image](https://user-images.githubusercontent.com/107069287/189154473-230a36c6-49e2-4456-b8fb-66de8a013b5e.png)

Na sequência criaremos os dois virtual networks. 

No portal do Azure, no campo de pesquisa, digite virtual network: 

![image](https://user-images.githubusercontent.com/107069287/189155030-d1d20481-f625-4ac0-83c3-eeba3462855a.png)

Clique em + Create para criarmos as virtual networks: 

![image](https://user-images.githubusercontent.com/107069287/189155331-1da12d8a-8d05-4bd3-9879-979b4f42295b.png)

Primeiro criaremos a Virtual Network (VNET) de origem. 

Na primeira tela em Basics preenchemos o campo Resource Groups com o recurso que criamos RG-Origem e colocaremos o nome de VNET-Origem:

![image](https://user-images.githubusercontent.com/107069287/189155956-97a07cf3-4414-490a-9178-93f53a89b954.png)

Em IP Address manteremos as configurações padrão, sugerida pela plataforma e clicaremos em next: 

![image](https://user-images.githubusercontent.com/107069287/189156168-2958b2ec-599d-4578-a276-0adaac4e71d6.png)

Mantenha as configurações default em security e clique a seguir em Review + Create: 

![image](https://user-images.githubusercontent.com/107069287/189156388-9b92116e-803f-4b57-8320-5436a50ef7f7.png)

A seguir clique em create para criar a VNET. 

Aguarde até a conclusão do processo de criação para não ter overlap de rede. 

Acessaremos novamente a aba de virtual network e criaremos a segunda vnet. 

Clique novamente em + Create: 

![image](https://user-images.githubusercontent.com/107069287/189157524-3c6bea42-356f-4c5a-999b-fc4af9595a11.png)

Na guia basic selecionaremos o Resource Group RG-Destino e nomearemos a Vnet de VNET-Destino: 

![image](https://user-images.githubusercontent.com/107069287/189157864-dba2d9f2-2411-4fba-ad03-05e6f406f506.png)

Clique em Next. 

Na aba IP Address note que o ip está diferente do que configuramos anteriormente. Novamente mantemos as configurações default e clicamos em next. 

![image](https://user-images.githubusercontent.com/107069287/189158423-8ebf84fb-d8d9-4691-9e38-71c6f8df971a.png)

Clique em Review + Create e em seguida create para criarmos a VNET. 

![image](https://user-images.githubusercontent.com/107069287/189158594-96915ca7-eb90-4fbd-beef-7fa941328616.png)

Na sequência criaremos as máquinas virtuais. 

Novamente na tela principal do portal, no campo pesquisa, digite Virtual Machines: 

Clique em + Create e em seguida Azure Virtual Machines: 

![image](https://user-images.githubusercontent.com/107069287/189159297-9dfc2d63-e4eb-49b0-90cc-6f4a7846ed7f.png)

Preencheremos os campos a seguir conforme a imagem abaixo: 
OBS: O grupo de recursos usado nessa etapa será o RG-Origem. 

![image](https://user-images.githubusercontent.com/107069287/189160209-e16d9672-8fe8-4369-b8d2-a04a79b03ee0.png)

Preencha o usuário e senha de sua preferência: 

![image](https://user-images.githubusercontent.com/107069287/189160374-aa0ff296-51e8-4337-9a50-d9eea1ab3df8.png)

Clique em Next. 

Em Disks iremos configurar com as opções sugeridas pela plataforma, podemos seguir clicando em Next: 

![image](https://user-images.githubusercontent.com/107069287/189160722-ff09330f-3c38-4362-a71f-6abfbdeca22c.png)

Valide apenas as configurações que foram associadas e clique em Next: 

![image](https://user-images.githubusercontent.com/107069287/189161090-3b8b353a-87a0-42aa-9962-c9b28f5e6f67.png)

Em management clique novamente em Next para manter as configurações default: 

![image](https://user-images.githubusercontent.com/107069287/189161234-a95d2f04-6a0c-45a7-b2bf-ddd1dc487ec4.png)

Em monitoring na opção Boot Diagnostics marque a opção disable: 

![image](https://user-images.githubusercontent.com/107069287/189161431-c873337d-b619-4706-9444-9c660e588176.png)

Pode clicar na sequência em Review + Create e em seguida create para criarmos a Virtual Machine (VM): 

![image](https://user-images.githubusercontent.com/107069287/189161695-655e05a1-8eaa-4212-a527-15853a554e31.png)

Assim que VM for criada clique em go to resource: 

![image](https://user-images.githubusercontent.com/107069287/189164007-a2df6e91-e596-4bb7-88a2-d107fec9440e.png)

Em seguida rodaremos o script abaixo: 

![image](https://user-images.githubusercontent.com/107069287/189364720-f676088b-5d9e-4a85-937c-c65a54b71843.png)

Na aba lateral, role a barra até Operations e vá em Run Command: 

![image](https://user-images.githubusercontent.com/107069287/189164392-0592dff0-19dc-4089-8ebf-cd848aa931eb.png)

Em seguida clique em RunPowerShellScript: 

![image](https://user-images.githubusercontent.com/107069287/189164538-2a8627d9-80a1-4ff2-bcde-c62e5f4f258f.png)

Em seguida cole o script na tela de Power Shell Script para instalarmos IIS e aguarde até a conclusão da execução do comando: 

![image](https://user-images.githubusercontent.com/107069287/189367846-25809fa0-3667-42b0-88b9-d69f2e43338f.png)

Na sequência iremos liberar o acesso a porta 80 na máquina para visualizarmos a página que criamos. 

No portal, na aba de pesquisa vá novamente em Virtual Machine: 

![image](https://user-images.githubusercontent.com/107069287/189165988-3559e9c5-fa56-4c07-ba02-2d1ce64f6194.png)

Clique em VM-Mover (Máquina que criamos logo acima):

![image](https://user-images.githubusercontent.com/107069287/189166290-849284b5-1e63-4c05-be51-301eef4c5505.png)

Na aba ao lado, no campo Settings, clique em Networking:

![image](https://user-images.githubusercontent.com/107069287/189166255-e4aeb8ca-3df2-4fb3-ab28-e14ec933c356.png)

Clique em Add inbound port:

![image](https://user-images.githubusercontent.com/107069287/189166447-cb78e8d2-a126-43d6-8135-ec7def0e7a92.png)

Criaremos a regra conforme a imagem para o ip de destino configurado na máquina: 

![image](https://user-images.githubusercontent.com/107069287/189166936-4e7fea26-4ae1-4c3e-aacc-1d0ba7015015.png)
![image](https://user-images.githubusercontent.com/107069287/189167115-aab7fec4-9660-4533-b471-1f3d83cfd83f.png)

Clique em add. 

Na sequência, no portal, pesquise por Azure Resourcer Mover: 

![image](https://user-images.githubusercontent.com/107069287/189372621-2f29758c-273e-459a-bbed-494a97a053fa.png)

Na tela principal, clique em Move Across Regions: 

![image](https://user-images.githubusercontent.com/107069287/189372960-a4d78995-5ec6-42bf-9e89-c8bbafc55236.png)

No primeiro campo preencha a sua região de origem e no segundo campo preencha a sua região de destino: 

![image](https://user-images.githubusercontent.com/107069287/189373479-0aebf5da-ccc8-44f7-aa22-f287fda0b3d0.png)

Clique em Next. 

Em seguida clique em Select Resource: 

![image](https://user-images.githubusercontent.com/107069287/189373757-7fcd0440-4acc-43ed-9455-61bf65123d74.png)

Note que aparecerá todos os recursos criados, nesse caso selecionaremos apenas o que precisamos movimentar: 

![image](https://user-images.githubusercontent.com/107069287/189374008-10b204e7-07df-43f7-8a4f-4efa58de65b0.png)

![image](https://user-images.githubusercontent.com/107069287/189374240-c957ac99-45d0-4d36-8dca-f9b830747a8a.png)

Clique em Done. 

Na próxima tela clique em Next: 

![image](https://user-images.githubusercontent.com/107069287/189374587-3a01288d-9d27-49c7-87c6-ba8155cd85e4.png)

Na próxima página marque a opção I understand that metadata information related to this move will be stored in Resource group - 'ResourceMoverRG-eastus-brazilsouth-brs' which will be created in the region - Brazil South. I am granting permissions to create a System Assigned Managed Identity on my behalf to access the resources in the subscription - Azure Pass – Sponsorship e na sequência clique em Proceed: 

![image](https://user-images.githubusercontent.com/107069287/189374896-48f7e071-3e2f-4721-b065-c3240c87e386.png)

OBS: Esse processo pode demorar um pouco mais que o norrmal, aguarde até a finalização desta etapa. 

Durante o processo clique em Added resource to move para acompanhar essa etapa: 

![image](https://user-images.githubusercontent.com/107069287/189375838-44e703f7-bdc8-4d5d-abc4-3191fb3420f6.png)

Primeira etapa, clique em validate dependences para validar as dependências: 

![image](https://user-images.githubusercontent.com/107069287/189376423-72046e36-e5e8-48f6-bcb3-5cd207087a77.png)

Após a validação, note que alguns itens estão ainda aguardando a validação das dependências: 

![image](https://user-images.githubusercontent.com/107069287/189377297-d5e70688-ff0e-4430-8be0-55a85f569d1a.png)

Analisando o erro, note que o erro está apontando para um erro relacionado a Virtuan Network: 

![image](https://user-images.githubusercontent.com/107069287/189377757-078cd058-8762-40fb-a647-845644c98282.png)

Clique em add dependencies: 

![image](https://user-images.githubusercontent.com/107069287/189377938-98d468d9-9070-4eb2-acc3-eca8ad633e33.png)

E em seguida inclua as duas dependecias listadas e depois clique em Add dependencies: 

![image](https://user-images.githubusercontent.com/107069287/189378079-cf5b79a8-8242-4b6a-88c1-2c90ee2771de.png)

Aguarde até o processo finalizar. 

Corrigido as dependecias, novamente será solicitado que valide novamente. Clique em Validate Dependencies novamente e aguarde até a conclusão: 

![image](https://user-images.githubusercontent.com/107069287/189378912-abeea699-fe2c-4d6a-b328-25cf0cec3168.png)

OBS: Cada item que for dando erro, precisa ser corrigido manualmente item a item. 

Note que novamente apresentamos outro erro, vamos analisa-lo:

![image](https://user-images.githubusercontent.com/107069287/189379341-bf50fe66-be63-4773-976b-47b5c3fc62dc.png)

Nesse caso o erro está indicando que precisamos fazer um commit em alguns resources groups. 

Vamos alterar agora o Resource Group: 

Clique no Resource group indicado na tela: 

![image](https://user-images.githubusercontent.com/107069287/189379894-379b186c-2c0b-4781-b3cc-a0612549f437.png)

Vamos alterar essa propriedade para o grupo de recursos que já criamos, RG-Destino: 

![image](https://user-images.githubusercontent.com/107069287/189380148-f25e68b8-69c3-4b70-ad6c-b6d309a48dff.png)

Clique em Save Changes e em seguida Save and Validate dependencies: 

![image](https://user-images.githubusercontent.com/107069287/189380322-82c4e09e-84df-41f5-ab51-e51d00159edf.png)

Aguarde novamente a validação. 

Após a validação volte na tela anterior e ajuste o parametro da VNET: 

![image](https://user-images.githubusercontent.com/107069287/189380840-94b8c23e-cc82-4bc0-83d3-0dca238d99bd.png)

Neste caso vamos alterar para a VNET-Destino: 

![image](https://user-images.githubusercontent.com/107069287/189380983-ad31523a-2e23-4657-996e-4d095a64fbff.png)

Clique novamente em Save Changes e em seguida Save and Validate Dependencies: 

![image](https://user-images.githubusercontent.com/107069287/189381119-4850009f-8134-40c8-8d79-d09f596da523.png)

Após a validação agora daremos o commit nos dois recursos pendentes: 

![image](https://user-images.githubusercontent.com/107069287/189381679-dde897cc-ebdf-44af-b9c3-2c23eff41df8.png)

Marcamos os recursos e clicamos em commit. 

Após essa etapa, concluiremos o processo dando o commit: 

![image](https://user-images.githubusercontent.com/107069287/189382120-08ed6cbd-eec2-4f3d-90a4-c7f0bdd59503.png)

Aguardamos novamente essa etapa concluir. 

Note que a mensagem de erro que estava aparecendo anteriormente sumiu: 

![image](https://user-images.githubusercontent.com/107069287/189382584-cef7a3ee-be0f-458c-935f-ded11a16cc49.png)

Agora iremos selecionar todos os recursos que estão como prepare pending e iremos acionar o Prepare: 

![image](https://user-images.githubusercontent.com/107069287/189383011-a516ffda-6e61-402f-8680-08869a0f4967.png)

Valide novamente a preparação e clique em Prepare: 

![image](https://user-images.githubusercontent.com/107069287/189383131-f2a95848-65e6-455d-9caa-49fbc278a7b7.png)

Essa etapa é a etapa mais demorada, aguarde até ao término do processo: 

![image](https://user-images.githubusercontent.com/107069287/189383318-837979d6-9aa0-4729-8700-fb8630807b7a.png)

Após o processo de prepare note que as máquinas estão com o initiate move pending, estando nesse estágio podemos dar sequência no processo de moving. 

Selecione novamente os recursos e clique em initiate move: 

![image](https://user-images.githubusercontent.com/107069287/189398106-b866243c-af89-44af-ac95-c88609ff27df.png)

Valide os recursos a serem movimentados e clique novamente em initiate move: 

![image](https://user-images.githubusercontent.com/107069287/189398293-c2422d75-4b27-4b97-8a9d-9553606108b3.png)

Aguarde novamente até a conclusão do processo. 

Durante o processo algumas alterações importantes a ser feita. 

Abra uma nova guia e no portal pesquise por Resource Group: 

![image](https://user-images.githubusercontent.com/107069287/189399930-5c34b48b-5e22-4568-aa31-da1009f32264.png)

Acesse o Resource Group RG-Destino: 

![image](https://user-images.githubusercontent.com/107069287/189400032-5688baac-c223-4b2c-946a-e05599660e71.png)

Em Overview acesse a máquina VM-Mover: 

![image](https://user-images.githubusercontent.com/107069287/189400161-7fc2af66-55f3-4f68-a93f-9801080ab481.png)

Vá ate a opção Networking: 

![image](https://user-images.githubusercontent.com/107069287/189400259-d53975c8-9343-46f8-9f15-9fa163758ab8.png)

Clique em Add inbound port rule e altere a regra criada para o novo ip privado: 

![image](https://user-images.githubusercontent.com/107069287/189401409-c5916703-8356-4d81-8045-7b995ff3acfa.png)

![image](https://user-images.githubusercontent.com/107069287/189401450-e1eed101-f79c-4006-b7af-306677907a7e.png)

Copie o no ip público e teste novamente o acesso e veja se abre o site do IIS: 

![image](https://user-images.githubusercontent.com/107069287/189401611-5a17ea64-2861-4e88-aa3d-0993c77c3142.png)

<h3>OBS: Até essa etapa, o processo pode ser reversível, ou seja, a máquina ainda está fazendo a replicação e mantendo a máquina em sua origem. A partir de agora todos os passos a seguir serão definitivos. </h3>

Após a conclusão, agora iremos fazer o commit nos recursos: 

Selecione novamente os recursos e clique em commit move: 

![image](https://user-images.githubusercontent.com/107069287/189402608-8b0770e9-dd9c-4122-9c95-852a2b608eae.png)

Clique novamente em commit: 

![image](https://user-images.githubusercontent.com/107069287/189402838-22a6278b-a755-412b-942c-1c9250f5bfb0.png)

Aguarde até a conclusão do processo. 

Duas condições: Caso você não queira deletar os recursos do Resource Group de Origem basta clicar na Opção Remove: 

![image](https://user-images.githubusercontent.com/107069287/189404941-6d2cb3f2-96a0-4e7f-8638-b7333bbbe508.png)

Agora caso queira deletar os recursos do RG-Origem utilize a opção Delete source: 

![image](https://user-images.githubusercontent.com/107069287/189405221-374a9680-9c35-4557-b135-dcbbecce9d33.png)

Nesse exemplo utilizaremos o Delete Reource, após acionar a opção digite yes para confirmar e clique em Delete source: 

![image](https://user-images.githubusercontent.com/107069287/189406136-b5979980-762a-46e0-b0f7-0e38f96dbee1.png)

Aguarde até a conclusão. 







































































