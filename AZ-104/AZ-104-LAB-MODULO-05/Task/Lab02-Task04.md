# AZ-104-LAB-MOD-05

 <h2>Lab 05b - Configuração de VPN</h2> <br>

 ***Tarefa 4:***  <br>
    *Deploy Local Network Gateway*

Pré-requisitos: 
- Conexão RDP com a máquina conforme a atividade anterior. 
- IP público configurado corretamente conforme a atividade anterior. 

No portal do Azure, no campo de pesquisa digite Local Network Gateway: 

![image](https://user-images.githubusercontent.com/107069287/192557085-2523e730-33ed-4dde-b248-f72cbfd321d2.png)

Em seguida clique em + Create: 

![image](https://user-images.githubusercontent.com/107069287/192557347-91f03323-ec55-45ac-844f-6e534d390602.png)

Abra uma nova guia e copie o IP publico da máquina destinada ao firewall. 

Digite no campo de pesquisa Virtual Machine: 

![image](https://user-images.githubusercontent.com/107069287/192558363-2338c8ca-35b3-4404-9ebd-a56c65cb6645.png)

Em seguida clique VM-FW-OnPremises: 

![image](https://user-images.githubusercontent.com/107069287/192558480-41055951-9879-4cb4-abd4-3631918dbab5.png)

Em Overview copie o endereço público da virtual machine: 

![image](https://user-images.githubusercontent.com/107069287/192558789-65fbd389-886a-4b5e-b075-77dc413436a0.png)

Volte para a aba anterior e agora iremos configurar conforme as configurações da imagem: <br> 
*OBS: No campo IP Address iremos copiar o ip público que coletamos da máquina virtual VM-FW-OnPremises*

 ![image](https://user-images.githubusercontent.com/107069287/192559775-f6a1c636-cb9c-45b3-8196-764020c102d8.png)

Clique em Next. 

Em Advanced, não iremos fazer nenhuma alteração, apenas clique em Next: 

![image](https://user-images.githubusercontent.com/107069287/192560068-1513ed3a-1aee-4aed-8414-a02b660860fc.png)

Depois clique em Review + Create e em seguida Create e aguarde o término do deploy. 

Feito essa etapa, volte a home do portal e no campo de pesquisa digite Virtual Network Gateway: 

![image](https://user-images.githubusercontent.com/107069287/192561189-f9e0c9b6-187f-42b4-8123-ab18fed68ac0.png)

Acesse o Virtual Network Gateway qye criamos: 

![image](https://user-images.githubusercontent.com/107069287/192561358-0875f2cd-fc4c-49d6-8d8e-ecfd57a8d22a.png)

Em seguida acesse a opção Connections na área Settings: 

![image](https://user-images.githubusercontent.com/107069287/192561576-44f339cb-41eb-4a31-be83-8b6d037826ea.png)

Nessa etapa iremos adicionar uma nova conexão. 

Clique em + Add: 

![image](https://user-images.githubusercontent.com/107069287/192561865-29a61419-c6de-43bd-ad25-d62d2a202978.png)

Preencha as configurações conforme fizemos nas atividades anteriores: 

![image](https://user-images.githubusercontent.com/107069287/192562437-7df9a23b-fc8f-456b-84c2-5894314c0949.png)

Em seguida clique em Ok. 

Volte até a máquina VM-FW-OnPremies, vá até o server manager, clique em Tools e em seguida Routing and Remote Access: 

![image](https://user-images.githubusercontent.com/107069287/192563246-83596c2f-9495-442c-8b70-d93b491299ec.png)

Vá em Network Interfaces e em seguida clique com o botão direito em FW-Azure e vá em Properties: 

![image](https://user-images.githubusercontent.com/107069287/192563637-43386b9f-5068-48a3-9af4-8901fe09786e.png)

Vá até a aba Option e marque a opção Persistent Connection: 

![image](https://user-images.githubusercontent.com/107069287/192563986-00f0f154-6705-4f0f-8fe1-b3a9b5e240a6.png)

Em seguida clique em Ok. 

Clique novamente com o botão direito em FW-Azure e clique em Connect: 

![image](https://user-images.githubusercontent.com/107069287/192564396-d6a431e4-1221-49b6-9d1e-a13d5c552a0f.png)

Verifique o status e veja se foi estabelecido a conexão com o Azure: 

![image](https://user-images.githubusercontent.com/107069287/192564582-7f12a699-6ec6-4002-90d6-2f2c549ce2b0.png)

*Tarefa Opcional: Faça os testes de ping para as máquinas virtuais Linux e Windows. Note que o ping irá funcionar apenas para a máquina Linux, localizada em eastus. A VM Windows não pingará, pois até essa etapa não habilitamos a transitividade de gateway entre as VNETs.*

No portal, no campo de pesquisa, digitw Virtual Network: 

![image](https://user-images.githubusercontent.com/107069287/192567708-575a057a-a436-4a15-8c80-b14421ae0912.png)

Selecione a VNET-USA01: 

![image](https://user-images.githubusercontent.com/107069287/192585084-037aa025-9c2a-4a17-9494-a608f3e0cd80.png)

Em seguida, no campo Settings, clique em Peerings: 

![image](https://user-images.githubusercontent.com/107069287/192585415-9550b1fa-6ae9-462e-9eae-c153c5496257.png)

Acesse a opção VNET-USA01-to-VNET-BRA01: 

![image](https://user-images.githubusercontent.com/107069287/192585763-cffe4ae7-c642-4a9e-b449-7480e6f9e53a.png)

Em seguida selecione a opção Use this virtual network's gateway or Route Server: 

![image](https://user-images.githubusercontent.com/107069287/192585938-ac74078f-0951-4348-8ae5-103c31ff1012.png)

E em seguida clique em Save. 

Na sequência volte até a opção de Virtual Network e clique VNET-BRA01: 

![image](https://user-images.githubusercontent.com/107069287/192586354-8a4af138-0f17-4672-a9dc-018939dd9362.png)

Vá até a opção Settings e clique em Peerings: 

![image](https://user-images.githubusercontent.com/107069287/192586545-6fefcfe8-83f8-496c-b60d-ebba1dfe2a16.png)

Acesse a opção VNET-BRA01to-VNET-USA01: 

![image](https://user-images.githubusercontent.com/107069287/192587018-45d3da2c-fa8c-4613-9067-04dfd8072e6f.png)

E selecione a opção Use the remote virtual network's gateway or Route Server: 

![image](https://user-images.githubusercontent.com/107069287/192587175-3710edbb-6946-4e7a-8232-47232cd29f83.png)

Em seguida clique em Save. 

*Tarefa opcional: Faça os testes de ping e caso queira faça um acesso via remote desktop para validar a conexão. Note que após essa etapa todas as conexões irão estabelecer normalmente.*

Concluido esta etapa, a tarefa foi finalizada. 

