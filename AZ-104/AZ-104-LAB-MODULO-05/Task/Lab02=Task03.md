# AZ-104-LAB-MOD-05

 <h2>Lab 05b - Configuração de VPN</h2> <br>

 ***Tarefa 3:***  <br>
    *Deploy VM para simular firewall on-premises*

Vá até o portal do Azure, e no campo de pesquisa, digite Virtual Machine: 

![image](https://user-images.githubusercontent.com/107069287/191811626-55ddcd64-f4c6-418a-864a-6518634d55c2.png)

Clique em + Create e em seguida Azure Virtual Machine:

![image](https://user-images.githubusercontent.com/107069287/192291365-b978ae97-61d0-41dd-be00-f030d84a7687.png)

***Importante: Para esse Laboratório precisei fazer a movimentação dos recursos de East US 2 para Central US, pois as máquinas do tipo B não estavam disponíveis para a região esatus 2. Caso precisem fazer o mesmo processo, utilize a atividade sobre Resource Mover para concluir essa movimentação.***

Configure a Virtual Machine seguido os parametros abaixo: 

![image](https://user-images.githubusercontent.com/107069287/192367153-7c36c075-5583-44b8-95f8-1848c53c76da.png)

Utilize o tamanho da máquina B2s e configure o usuário administrador conforme a sua escolha: 

![image](https://user-images.githubusercontent.com/107069287/192367416-9ab7bd17-2e6b-42bd-9cdc-3c994faf1185.png)

![image](https://user-images.githubusercontent.com/107069287/192367495-9071741b-9ea1-4787-82b2-5abcd1aeb4e4.png)

Clique em Next. 

Em Disks, vamos utilizar o disco premium para ter um pouco mais de perfomance: 

![image](https://user-images.githubusercontent.com/107069287/192367720-b3641a0c-c9bb-4179-8a52-00f25376bb3d.png)

Clique em Next. 

Em Network vamos manter o nosso escopo de acordo com o cenário que configuramos: 

![image](https://user-images.githubusercontent.com/107069287/192368152-2c1a09f9-b0e9-46da-a128-3e7ddd79c4ac.png)

Clique em Next. 

Em Management, não iremos fazer nenhuma alteração: 

![image](https://user-images.githubusercontent.com/107069287/192368343-54c047c3-6cfc-4b54-bff3-ce439705f7b7.png)

Em monitoring, vamos desabilitar o boot diagnostics: 

![image](https://user-images.githubusercontent.com/107069287/192368508-b6f8416e-52d1-4aa8-94f3-5323f69fa320.png)

Clique em Next. 

Em Advanced, não vamos fazer nenhuma alteração: 

![image](https://user-images.githubusercontent.com/107069287/192368831-8c920c90-4ec7-429a-923f-eecca09d0107.png)

Clique em Next. 

Em Tags, vamos manter o escopo que utilizamos nos exercicíos anteriores: 

![image](https://user-images.githubusercontent.com/107069287/192368997-f15e46ec-646e-4c0a-b0dd-253a59d1fb42.png)

Por fim, clique em Review + Create e em seguida Create. 

Após finalizarmos o deploy de nossa VM, clique em Go to Resource: 

![image](https://user-images.githubusercontent.com/107069287/192370082-9bd25e4c-b0e5-49be-adab-7f12bf616242.png)

Em Overview, vamos nos conectar a nossa VM. Clique em Connect, em seguida RDP: 

![image](https://user-images.githubusercontent.com/107069287/192370283-b5025247-9db0-485e-bb88-e393b51e9341.png)

Clique em Download RDP File: 

![image](https://user-images.githubusercontent.com/107069287/192370427-b7c218d5-2ba9-4e1a-92bf-59756f9d9f2a.png)

Execute o arquivo que acabamos de fazer o download e clique em conectar: 

![image](https://user-images.githubusercontent.com/107069287/192370703-87f5b733-7f8e-4055-b5e6-a3776961a94b.png)

Digite o usuário e senha que configuramos no portal e clique em ok: 

![image](https://user-images.githubusercontent.com/107069287/192370915-b32287cb-3bca-42ac-94aa-1bce4a5e3d94.png)

![image](https://user-images.githubusercontent.com/107069287/192370965-f306cae2-bf0b-4242-b212-ffa2f8591e9f.png)

![image](https://user-images.githubusercontent.com/107069287/192371301-b7a909d0-c86d-4724-af36-d4136e0b1284.png)

Ao se concetar, acesse o server manager: 

![image](https://user-images.githubusercontent.com/107069287/192377035-664f0148-12bc-49f2-8903-1e8b598084ca.png)

Clique em Manager e em seguida Roles and Features: 

![image](https://user-images.githubusercontent.com/107069287/192377230-352907d4-763e-4228-be38-3a772b487146.png)

Clique em Next na primeira tela: 

![image](https://user-images.githubusercontent.com/107069287/192377536-b4e42cda-fa10-40fd-918b-2e2d03495c73.png)

Marque a opção Role-based or feature-based installation e em seguida clique em Next: 

![image](https://user-images.githubusercontent.com/107069287/192377796-839a32ec-c929-4ad3-8f77-f191ef9bc5b9.png)

A seguir clique em Next novamente: 

![image](https://user-images.githubusercontent.com/107069287/192378045-de281952-92c5-410f-a0a5-ee18944ac399.png)

Em seguida, clicaremos na opção Remote Access: 

![image](https://user-images.githubusercontent.com/107069287/192378361-f76b9bbc-8e16-4da4-acc6-044eed1c7cd1.png)

Clique em Next. 

A seguir entraremos na opção features, novamente avançamos: 

![image](https://user-images.githubusercontent.com/107069287/192378691-84d49a97-6e13-40db-a20d-c2cc061a3590.png)

Na opção Remote Access, avançamos novamente clicando em Next: 

![image](https://user-images.githubusercontent.com/107069287/192378964-af5118ef-e917-4d94-96a7-df9d2708d3c1.png)

Em Role Services, adicionaremos algumas features. Marque a opção DirectAccess and VPN: 

![image](https://user-images.githubusercontent.com/107069287/192379209-4ca816b5-7daa-4fda-9780-4cbac1f55f25.png)

Em seguida clique em Add Features: 

![image](https://user-images.githubusercontent.com/107069287/192379394-d739dd9e-e010-46f6-8dc6-80a49ff0f899.png)

Em seguida marque tabém a opção Routing: 

![image](https://user-images.githubusercontent.com/107069287/192379605-ad4b13d9-090d-4d40-b658-d3c20bf59736.png)

Após selecionarmos as duas opções clicamos em next para avançarmos: 

![image](https://user-images.githubusercontent.com/107069287/192380169-ae7d5792-bf17-4884-a5fd-310b05284ef9.png)

Em Web Server Roles, clicamos em next: 

![image](https://user-images.githubusercontent.com/107069287/192380340-94727d95-40bf-42cd-83ad-463054f2d351.png)

Em Role Services, clique em Next: 

![image](https://user-images.githubusercontent.com/107069287/192380484-150aac2c-a5d1-4cad-bebe-b30d1f304684.png)

E em seguida clicamos em install: 

![image](https://user-images.githubusercontent.com/107069287/192380599-3247e618-b5b7-4020-afca-2c3a65d7809c.png)

Aguarda até a conclusão da instalação: 

![image](https://user-images.githubusercontent.com/107069287/192380693-23a62be6-3bd2-4413-93df-cd93bdba9eb1.png)

Após a instalação clique em close e volte para o server manager: 

Clique nas notificações acima e em seguida clique em Open the Getting Started Wizard: 

![image](https://user-images.githubusercontent.com/107069287/192381349-a89b1403-e318-466a-b25e-9799078c9f15.png)

***OBS: Caso não abra a opção, faça os passos abaixo:***

*Vá em Tools e em seguida clique Remote Access Management:*

![image](https://user-images.githubusercontent.com/107069287/192382133-f03285b1-8c10-4199-9f42-afc11d779d60.png)

*Clique em DirectAccess and VPN e em seguida Run the Getting Started Wizard:* 

![image](https://user-images.githubusercontent.com/107069287/192382592-3940c068-6202-4ef2-bf93-94ec6b7af0fd.png)

Clique em Deploy VPN only: 

![image](https://user-images.githubusercontent.com/107069287/192382989-76814c5e-b2b2-4604-9a4a-26e1bf3e1251.png)

Clique com o botão direito no nome do servidor e em seguida clique Configure an Enabled Routing and Remote Access: 

![image](https://user-images.githubusercontent.com/107069287/192383336-751eda69-8292-4bb5-9c14-36cf9f9343cf.png)

Na primeira tela do Wizard de instalação vamos clicar em Next: 

![image](https://user-images.githubusercontent.com/107069287/192383605-37e23856-7368-485c-8470-2d429103934e.png)

Marque a opção Secure connection between two private networks e em seguida clique em Next: 

![image](https://user-images.githubusercontent.com/107069287/192384329-fdf2c635-0b71-41e2-9545-d14bcc97882f.png)

Em Demmand Dial Up Connections, vamos marcar a opção yes e em seguida clicar em next: 

![image](https://user-images.githubusercontent.com/107069287/192384619-c9ee52bf-1ea7-4b49-bf73-49d7e34a3528.png)

Em IP Address Assigment, mantenha a opção automatico e em seguida clique em Next: 

![image](https://user-images.githubusercontent.com/107069287/192385013-806fc63c-4675-48c3-a39c-f3e0ebe71023.png)

Complete a instalação clicando em finish: 

![image](https://user-images.githubusercontent.com/107069287/192385060-ce973d7f-135f-41d4-9336-d75934c80bc2.png)

Aguarde até a conclusão do processo. 

Em seguida vamos configurar a interface que irá se conectar diretamente com o ambiente do Azure. 

Nessa primeira tela clique em Next: 

![image](https://user-images.githubusercontent.com/107069287/192385371-7a7438a8-e7d3-465c-8375-8848804b4b94.png)

Em interface Name, renomeie para FW-Azure e clique em Next: 

![image](https://user-images.githubusercontent.com/107069287/192385645-21ac0cdf-f213-42a0-a92d-558bffdc2aa9.png)

Em connection type, deixe marcado a opção Connect using virtual private networking e clique em next: 

![image](https://user-images.githubusercontent.com/107069287/192385825-e8804c0d-a954-4ea8-9abc-86363287604d.png)

Em VPN type, vamos marcar a opção IKEv2 e clicar em next novamente: 

![image](https://user-images.githubusercontent.com/107069287/192386023-b9429b5a-57b6-4aee-a541-e38eb08fa83a.png)

Nessa etapa, iremos precisar do ip publico do Azure. 

Vá até o portal do azure: 

No campo de pesquisa, digite Virtual Network Gateway: 

![image](https://user-images.githubusercontent.com/107069287/192398226-0ed1b85c-f26d-4472-a39f-d6a59dc38015.png)

Em seguida clique no Virtual Network Gateway que criamos, nesse exemplo é o VNG-01: 

![image](https://user-images.githubusercontent.com/107069287/192398316-20d9cf06-3e99-4189-98e0-e7c2966bb91f.png)

Em Overview, copie o ip público que foi dado a nossa VNG-01: 

![image](https://user-images.githubusercontent.com/107069287/192398419-8d8930aa-42df-4715-aab5-64e7ab23c5c2.png)

Copie o endereço e cole ele no nosso servidor de firewall: 

![image](https://user-images.githubusercontent.com/107069287/192398491-414961c2-ce73-42eb-a4e0-a688624fa16a.png)

Tenha o cuidado para deixar apenas o endereço no campo de endereço: 

![image](https://user-images.githubusercontent.com/107069287/192398588-19f433f3-2f7e-4d4b-beb2-605222497410.png)

Em seguida clique em next. 

Em protocols and Security, mantenha a opção Route IP packets on this interface marcada e clique em next: 

![image](https://user-images.githubusercontent.com/107069287/192398762-41f45b9f-3950-4c1a-aa16-3759f4155d43.png)

Em static routes for remote network, clique add para adicionarmos todas as rotas do azure que precisamos que seja conectado: 

![image](https://user-images.githubusercontent.com/107069287/192398928-dcf6670b-96aa-420f-be2a-f1ebd7c98b91.png)

Cadastre todas as rotas do azure que determinamos: 

![image](https://user-images.githubusercontent.com/107069287/192399090-3eb04b56-69f3-4cbe-8080-256a306fdf46.png)

![image](https://user-images.githubusercontent.com/107069287/192399182-eedb45ba-665f-4839-9a86-aa319aeec611.png)

![image](https://user-images.githubusercontent.com/107069287/192399296-7dde1b1d-2231-49ce-81f0-3843a890d387.png)

![image](https://user-images.githubusercontent.com/107069287/192399374-9a31d114-3009-4fb6-9d19-aeeacba0d339.png)

Após essa etapa clique em next. 

Em Dial-Out Credentials, pode deixar em branco e clique em next: 

![image](https://user-images.githubusercontent.com/107069287/192399563-8ba52fdd-fbf0-4218-9ee4-0e7c53132ae9.png)

Complete a configuração clicando em finish: 

![image](https://user-images.githubusercontent.com/107069287/192399638-c93c72f9-364c-4333-834f-30184c97245a.png)

Depois dessa etapa, precisamos criar as rotas estáticas. 

Clique em IPv4, em seguida Static Routes e com o botão direito do mouse clique em New Static Routes: 

![image](https://user-images.githubusercontent.com/107069287/192399840-5b980916-a299-46f7-980b-f16ad8f6bd46.png)

Configure as rotas conforme as imagens abaixo: <br>
*altere de ethernet para FW-Azure a interface.*

![image](https://user-images.githubusercontent.com/107069287/192400045-db3fc897-8d1e-4777-b7d2-aeb30d14c77b.png)

![image](https://user-images.githubusercontent.com/107069287/192400141-04d67916-0768-4d2d-84a2-cfcd4043e4c6.png)

![image](https://user-images.githubusercontent.com/107069287/192400196-2f500a17-9d43-491d-ab40-84ad17840944.png)

![image](https://user-images.githubusercontent.com/107069287/192400282-dd038c27-a367-41bb-888f-30c9630825e9.png)

Terminado esta etapa, vamos alterar algumas propriedades para concluirmos nossa configuração. 

Clique em Network Interfaces e em seguida clique com o botão direito em FW-AZURE e selecione propriedades: 

![image](https://user-images.githubusercontent.com/107069287/192400669-f5a14902-995f-4f2e-8108-b5f9971b37a9.png)

Vá até a opção Security e altere a opção Use machine certificates para use preshared key for authentication e em seguida crie uma senha da sua escolha: 

![image](https://user-images.githubusercontent.com/107069287/192400902-6b856ddd-b35c-4ad2-8a1f-e9851fca9258.png)

Em seguida clique em ok. 

*Opcional: Caso queira para fazer os testes de ping desabilite o firewall da máquina* 

Por fim, no portal do azure, no campo de pesquisa, digite virtual macbine: 

![image](https://user-images.githubusercontent.com/107069287/192401426-b0be1b63-8b3e-43a1-9592-6fc1a289ef90.png)

Clique em VM-FW-OnPremises: 

![image](https://user-images.githubusercontent.com/107069287/192401589-0683f2a1-31a4-45e0-9775-bd44c72b23ea.png)

Em Settings, clique em Networking: 

![image](https://user-images.githubusercontent.com/107069287/192401659-87c30c83-8e0e-485b-ac07-3c2cbede3b47.png)

Clique na interface de rede que criamos: 

![image](https://user-images.githubusercontent.com/107069287/192401749-2b8711a4-57f7-4fe4-8b0e-7169ba8199f8.png)

Vá até IP Configurations: 

![image](https://user-images.githubusercontent.com/107069287/192401840-bf7405a2-f3a8-44d6-ab6a-b31bab39b990.png)

E habilite o IP Fowarding: 

![image](https://user-images.githubusercontent.com/107069287/192401888-9da55ebf-cdf5-4d47-9ba1-059f1b4cff6c.png)

Em seguida clique em Save. 

Após essa etapa concluímos nossa tarefa.















