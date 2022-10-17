# AZ-104-LAB-MOD-08

 <h2>Lab 08 - Manage Azure Storage</h2> <br>

 ***Tarefa 1:***  
    *Implante availability set virtual com 2 máquinas no portal do Azure.*

Vá até o portal e no campo de pesquisa, digite Resource Group: 

![image](https://user-images.githubusercontent.com/107069287/196176645-6c98a59a-6c34-4e93-b520-3bc67fe26589.png)

Em seguida clique em + Create: 

![image](https://user-images.githubusercontent.com/107069287/196176775-76288a0a-40e4-43b2-b825-d47a06448066.png)

Preencha os campos conforme a imagem abaixo: 

![image](https://user-images.githubusercontent.com/107069287/196176907-ca0c1355-1681-4939-a1f0-4f7aa8bc26fe.png)

Em seguida clique em Next. 

No campo TAG, vamos criar as TAGs conforme a imagem abaixo: 

![image](https://user-images.githubusercontent.com/107069287/196177310-32265daa-3bff-4118-b693-83f440ccac06.png)

Em seguida clique em Review + Create e em seguida Create para criarmos o grupo de recursos. 

Na sequência iremos criar uma estrutura de rede para darmos andamento em todo o nosso laboratório. 

Vá a home do Azure e no campo de pesquisa digite Virtual Network: 

![image](https://user-images.githubusercontent.com/107069287/196177720-f4813cef-7cc6-4413-b03d-ce6396a0b0ea.png)

Em seguida clique em + Create: 

![image](https://user-images.githubusercontent.com/107069287/196177900-dd2ad71e-a267-48b0-bf61-1f8088aab669.png)

Faça a configuração como mostrado abaixo: 

![image](https://user-images.githubusercontent.com/107069287/196181713-22bc290c-bd3a-4892-82b9-1db2bed21d62.png)

Em seguida clique em Next. 

Configure o ip com o range abaixo: 

![image](https://user-images.githubusercontent.com/107069287/196181960-2fc0a07e-62ef-469e-a88b-a3d39393690c.png)

Em seguida clique em + Add subnet e configure com o range abaixo: 

![image](https://user-images.githubusercontent.com/107069287/196182234-291a188b-c375-4589-acf0-26bbc8c2e92a.png)

Em seguida clique em Add e em seguida clique em Next. 

Em securrity mantenha o padrão abaixo e clique em Next: 

![image](https://user-images.githubusercontent.com/107069287/196182614-8ac57255-b582-47c4-9114-07545e8002ac.png)

Em TAGs, preencha os campos conforme a imagem abaixo: 

![image](https://user-images.githubusercontent.com/107069287/196182898-c2882291-f330-46ac-a9af-167fbd5131d4.png)

Em seguida clique em Review + Create e em seguida Create. 

Volte para o home do azure e no campo de pesquisa digite Virtual Machine: 

![image](https://user-images.githubusercontent.com/107069287/196185007-73ea80b9-e5c1-49b4-b335-412ee6ce1013.png)

Em seguida clique em + Create e depois Azure Virtual Machine: 

![image](https://user-images.githubusercontent.com/107069287/196185148-b1b1d02f-f2e3-4902-a2b5-8c980cf116c3.png)

Preencha o campo conforme abaixo: 

![image](https://user-images.githubusercontent.com/107069287/196186139-6bf30262-7a1c-4f9c-bdd1-bb9107efc822.png)

Em seguida, em Availability set, clique em Create New e configure o Update Domain e o Fault domain conforme a imagem abaixo: 

![image](https://user-images.githubusercontent.com/107069287/196186740-169f33e5-631d-4d8c-98f1-183b3f9dde36.png)

Clique em Ok. 

Altere o tipo de máquina virtual para B2s com 2 VCPus e 4 GB de ram (caso não encontre no menu clique em See All Sizes): 

![image](https://user-images.githubusercontent.com/107069287/196188219-d86470c9-4a1d-461c-b730-465c7cec06bb.png)

![image](https://user-images.githubusercontent.com/107069287/196188364-c1ee7bc0-18ff-4675-848d-78be5c56354f.png)

Em seguida clique em select. 

Novamente na tela de criação, crie um usuário administrador para a máquina virtual e uma senha de sua escolha:: 

![image](https://user-images.githubusercontent.com/107069287/196188752-a14e05c4-ad3d-42b4-ad78-1037e1d8c694.png)

Libere além da porta 3389 a porta 80 para darmos andamento no laboratório: 

![image](https://user-images.githubusercontent.com/107069287/196189240-ff7af389-ea29-48bc-8296-15726398605d.png)

Em seguida clique em Next. 

Em Disks, vamos manter as opções sugeridas pelo portal e vamos clicar novamente em Next: 

![image](https://user-images.githubusercontent.com/107069287/196191677-21002fcd-d5d9-49cc-a1c4-90a3bb606d8c.png)

Em Network, perceba que a máquina já atrelou a configuração do IP da VNET que criamos. Nesta fase vamos apenas liberar também a porta 80 para acesso http: 

![image](https://user-images.githubusercontent.com/107069287/196192439-fadf2c3f-fec2-4b73-8461-c64a7b67eac0.png)

Os demais itens vamos deixar no padrão do Azure. Em seguida clique novamente em Next. 

Em management, habilite a opção auto-shutdown e no campo email coloque um endereço de sua preferência: 

![image](https://user-images.githubusercontent.com/107069287/196194779-028a193d-e23f-47b7-9524-ed1626c706c2.png)

Em seguida clique em Next. 

Em boot Diagnostics, clique em Disable e novamente clique em Next: 

![image](https://user-images.githubusercontent.com/107069287/196195075-c8b54b68-542d-47c8-94d2-7a284c3cdc82.png)

Em Advanced, não vamos fazer nenhuma alteração, apenas clique em Next: 

![image](https://user-images.githubusercontent.com/107069287/196195320-98ba348d-99b5-4069-86cf-1c105c98b05d.png)

Em TAGs, novamente preencha conforme a imagem abaixo: 

![image](https://user-images.githubusercontent.com/107069287/196195933-f03823da-5eb1-472d-a21a-09d10dafe90c.png)

Em seguida clique em Review + Create e depois em Create. 

Ao término da criação, clique em Template e em seguida clique em Deploy: 

![image](https://user-images.githubusercontent.com/107069287/196197110-d9ac4502-900b-4b0e-b082-b5dc56ab476b.png)

Nessa etapa, apenas altere os itens que não podem se repetir e que são particularidades de cada VM, como nome da máquina, placa de rede, etc. Abaixo a imagem ilustrativa para orientação da configuração da segunda máquina: 

![image](https://user-images.githubusercontent.com/107069287/196197718-00fd88e7-8eb8-457b-8299-102aaf9d053b.png)

![image](https://user-images.githubusercontent.com/107069287/196197792-2d6825d1-a9c4-4a29-8f8d-a9c94142d493.png)

![image](https://user-images.githubusercontent.com/107069287/196198191-c6417b47-2674-4ae5-8789-0f4e9fe43528.png)

![image](https://user-images.githubusercontent.com/107069287/196198260-34dce179-3962-49a6-8fd0-4d6c32847e1f.png)

Feito as configurações clique em Review + Create e em seguida clique em Create. 