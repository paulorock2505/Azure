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








