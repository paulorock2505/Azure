# AZ-104-LAB-MOD-08

 <h2>Lab 08 - Manage Azure Storage</h2> <br>

 ***Tarefa 4:***  
    *Implante zone-resilient scale sets usando Azure portal.*

Diagrama: 

![image](https://user-images.githubusercontent.com/107069287/196254572-00d0e9a7-d0cf-4d7c-90f0-fc9d08bd2833.png)

No portal, digite no campo de pesquisa, scale set: 

![image](https://user-images.githubusercontent.com/107069287/196255429-120f0e3a-b32a-41e2-a933-c0a8609eaa39.png)

Clique em + Create para criarmos a estrutura: 

![image](https://user-images.githubusercontent.com/107069287/196452755-bc3638eb-5315-40ed-8fe3-4d9e18eb1198.png)

Preencha os campos confrme a imagem abaixo: 

![image](https://user-images.githubusercontent.com/107069287/196454037-fe701c29-fed1-42ac-8717-00272a22184e.png)

![image](https://user-images.githubusercontent.com/107069287/196454240-734b40c8-03df-4fec-b6b0-d32bee7064b0.png)

Em Size, altere o tamanho da máquina para a B2s: 

![image](https://user-images.githubusercontent.com/107069287/196454771-2ab460b1-3327-42e4-adc8-0a737682d792.png)

Clique em select e continue a configuração. Em seguida coloque um usuário e senha de sua preferência: 

![image](https://user-images.githubusercontent.com/107069287/196455021-01e7fe4b-6a6e-48dc-9045-96b25c7b6e2b.png)

Clique em Next. 

Em Disks, não iremos alterar os discos: 

![image](https://user-images.githubusercontent.com/107069287/196455599-e27b00db-18bf-49bd-a7e2-94725f155173.png)

Clique em Next. 

Em Networking, por padrão ele irá sugerir que criamos uma nova virtual network, nesse caso utilizaremos a Vnet que criamos na Task anterior: 

![image](https://user-images.githubusercontent.com/107069287/196456593-9139ee08-39d7-4d29-803e-9216b82708c0.png)

Marque também a opão Use Load Balancer: 

![image](https://user-images.githubusercontent.com/107069287/196456732-d6379879-c335-4b6e-ba0f-33d109032906.png)

Em seguida clique em Next. 

Configure o scalling conforme a imagem abaixo: 

![image](https://user-images.githubusercontent.com/107069287/196457600-2d9824dd-bc43-4533-8ec1-b8218a86dcc5.png)

![image](https://user-images.githubusercontent.com/107069287/196457879-19f46f4f-6a47-4507-b862-13fdf32c4d92.png)

Em seguida clique em Next. 

Em Management apenas altere o modo de upgrade para automático e desabilite o boot diagnostics: 

![image](https://user-images.githubusercontent.com/107069287/196458826-ceb4a510-c22a-41cc-89e8-5d6c633a9a30.png)

Clique em Next. 

Em Helth não vamos fazer nenhuma alteração: 

![image](https://user-images.githubusercontent.com/107069287/196459253-fb2be39b-5f76-45f7-90bf-2e6872f91a9a.png)

Clique em Next. 

Em Advanced também não iremos fazer nenhuma alteração: 

![image](https://user-images.githubusercontent.com/107069287/196459655-57469dec-6aa2-4f1d-bbe5-64cd4dc2b457.png)

Clique em Next. 

Em Tags preencha os campos conforme a imagem abaixo: 

![image](https://user-images.githubusercontent.com/107069287/196459817-773c6e58-764d-4a0d-afa3-6516218a0e84.png)

Em seguida clique em Review + Create e em seguida Create. 

Ao término do deploy clique em Go to Resource. 

Em Settings, clique em Extensions + Applications: 

![image](https://user-images.githubusercontent.com/107069287/196461720-29b03530-9d1a-4848-a843-2a3d670bd92c.png)

Em Extensions, clique em + Add: 

![image](https://user-images.githubusercontent.com/107069287/196461840-abf0e06c-ea05-4c69-a38c-0340612465fb.png)

No campo de pesquisa, digite Custom Script Extension: 

![image](https://user-images.githubusercontent.com/107069287/196462615-0c678322-d925-4326-8b7e-812ca22eb0dc.png)

Em seguida clique em Next. 

Na próxima tela, clique em Browser: 

![image](https://user-images.githubusercontent.com/107069287/196462914-6a1a1957-7a63-4989-83a7-9d5ede5ab6c0.png)

Selecione o Blob que criamos na task anterior: 

![image](https://user-images.githubusercontent.com/107069287/196463149-d18bd373-9dd7-4746-adda-83b81de3be90.png)

Em seguida clique em scriptaz104: 

![image](https://user-images.githubusercontent.com/107069287/196463420-960be511-3eae-4f05-9a20-0c509699f956.png)

Clique no script .ps1 que armazenamos e em seguida clique em select: 

![image](https://user-images.githubusercontent.com/107069287/196463724-7a403220-e4df-43df-bcd4-d24e6e1ff9e7.png)

Em seguida clique em Create: 

![image](https://user-images.githubusercontent.com/107069287/196463966-6fcb1dce-a08a-402c-967c-110d2381f8f8.png)

Aguarde até o processo finalizar. 

Feito isso, iremos criar uma regra para a liberação da porta 80 das máquinas. 

Vá até Networking: 

![image](https://user-images.githubusercontent.com/107069287/196487235-00f685b9-5d28-4d0b-99a2-490c5ba14cc9.png)

Clique em Add inbound port rule: 

![image](https://user-images.githubusercontent.com/107069287/196487385-b7e61965-25f5-4e0e-82b7-d0e803e2d779.png)

Preencha os campos conforme a imagem abaixo: 

![image](https://user-images.githubusercontent.com/107069287/196487633-01ff278e-8b36-4697-b06a-e440ef12ea40.png)

Clique em Add. 

Valide o acesso da máquina, utilizando o IP público mencionado no Overview. Copie o IP público e cole no navegador para checar a instalação do IIS. 

Feito essa etapa, iremos dar sequência agora no teste de estresse da máquina. Para isso, iremos utilizar a máquina virtual que criamos na task anterior. 

Vá a home, no campo de pesquisa digite Virtual Machine: 

![image](https://user-images.githubusercontent.com/107069287/196490039-11dbf7ce-99c5-4c40-9f12-77a451db022b.png)

Acessa a máquina VM01 que criamos anteriormente: 

![image](https://user-images.githubusercontent.com/107069287/196490102-1af1c465-9658-4839-8497-6da3d79f5bcb.png)

Em Overview, clique em connect e em seguida RDP: 

![image](https://user-images.githubusercontent.com/107069287/196490250-e6305441-3d1b-433d-8bf8-ce01aa0cfd54.png)

Faça o download do cliente RDP, execute e acesse a máquina com as credenciais que foram configuradas anteriormente: 

![image](https://user-images.githubusercontent.com/107069287/196490874-88c97041-082c-48e4-bf90-625eec6e487a.png)

![image](https://user-images.githubusercontent.com/107069287/196491087-0d5af035-8d72-4f37-ad1f-4d70c232a4c2.png)

Dentro da máquina, vá run e digite mstsc para acessarmos a máquina do pool via TS: 

![image](https://user-images.githubusercontent.com/107069287/196492304-3df7e953-1e28-45ed-91e9-569ad179203d.png)

Utilize as credencias que criamos: 

![image](https://user-images.githubusercontent.com/107069287/196492700-1d87a155-52af-4b59-8127-eaefb401e961.png)

![image](https://user-images.githubusercontent.com/107069287/196493251-1cbd8315-7b56-4777-913b-62705f92639d.png)

Faça o download do software heavy para fazermos o teste de estresse na máquina. Abaixo o link:

https://www.jam-software.com/heavyload?ca=1

OBS: O link pode variar conforme o tempo, você pode usar tanto a sugestão que estamos dando como qualquer outro software de teste que você preferir

Ao término da instalação iremos executar os testes e analisarmos a perfomance do scale set que criamos: 

![image](https://user-images.githubusercontent.com/107069287/196495539-4a00209b-c656-468f-92f7-d0494ee37f9a.png)

Marque a CPU usage e pode iniciar o teste: 

![image](https://user-images.githubusercontent.com/107069287/196496433-1bc6130b-066a-4cfd-9f0f-e50b09dbfb68.png)

Aguarde os 5 minutos que ajustamos no scale set e note o deploy de novas máquinas que vão sendo criados. Após parar o teste, note a destruição das máquinas dentro de nosso ambiente. 

Após aproximadamente 12 minutos de teste o cenário ficou assim: 

![image](https://user-images.githubusercontent.com/107069287/196499273-a87041ac-5070-439a-8e45-09baba9a924c.png)

Pare o teste e note o processo de destruição das instâncias até chegar novamente a uma instância: 

![image](https://user-images.githubusercontent.com/107069287/196500963-9cc04591-498e-4fe0-8441-b42307f5ef94.png)

Feito esse teste a atividade foi concluída. 