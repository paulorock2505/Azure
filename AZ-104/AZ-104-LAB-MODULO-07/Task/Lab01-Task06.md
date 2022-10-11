# AZ-104-LAB-MOD-07

 <h2>Lab 07 - Manage Azure Storage</h2> <br>

 ***Tarefa 6:***  
    *Gerenciar o acesso a rede para Azure Storage*

No portal, pesquise por storage accounts: 

![image](https://user-images.githubusercontent.com/107069287/195172740-dfbccd60-3386-4cec-b4cd-f0f641d9a8c3.png)

Em seguida clique no storage que criamos: 

![image](https://user-images.githubusercontent.com/107069287/195172822-95dbff7f-7518-4391-982b-c51a079784e7.png)

No campo Security + Networking, vá até Networking: 

![image](https://user-images.githubusercontent.com/107069287/195173273-7463cbbd-7357-4ada-90f4-9a33439e5c2f.png)

Antes, abra uma aba extra e mapeie a unidade do file share direto no servidor. Faça os passos a seguir. 

Clique em File Share: 

![image](https://user-images.githubusercontent.com/107069287/195173556-36a32592-88de-4cce-b000-cff94f10cf7b.png)

Em seguida clique no File Share que criamos: 

![image](https://user-images.githubusercontent.com/107069287/195173736-98c78a28-256f-499d-905b-63b7e75f0441.png)

Em Overview, clique connect: 

![image](https://user-images.githubusercontent.com/107069287/195173858-7a23544c-fc14-4f06-9624-b5bd58ad7720.png)

Altere a unidade compartilhade e clique em Show Script: 

![image](https://user-images.githubusercontent.com/107069287/195173993-093b1acb-9181-4ec8-9906-d51c88ca2994.png)

Copie o script e abra um Powershell no servidor e na máquina que você esteja utilizando. Em seguida cole o camndo para fazer o mapeamento. <br> 
*Dúvidas sobre o procedimento veja a tarefa anterior onde fizemos o passo a passo deste processo.*

![image](https://user-images.githubusercontent.com/107069287/195175462-fd579161-1586-46cf-af10-088c975bd536.png)

Volte ao portal do Azure, no campo Networking e na aba Firewall e Networking: 

![image](https://user-images.githubusercontent.com/107069287/195175928-808866b6-1a73-49c4-990f-4ded1589ed9c.png)

Marque a opção Enabled from selected virtual networks and IP addresses: 

![image](https://user-images.githubusercontent.com/107069287/195176128-6d61f09a-2987-4340-afa1-92baff3023a7.png)

Em seguida clique em + Add existing virtual network: 

![image](https://user-images.githubusercontent.com/107069287/195176279-fd590da6-d810-43e6-b4f9-fa2ba320a560.png)

Configure a Virtual Network conforme a imagem abaixo: 

![image](https://user-images.githubusercontent.com/107069287/195176683-8924a327-9ed9-4377-ab08-321f673d1a69.png)

Em seguida clique em enable, em seguida clique em Add e depois Save. 

Note que a conexão da pasta compartilhada na máquina foi fechada. No entanto na nossa máquina virtual o acesso continua funcionando. 

*Tarefa extra: Delete a configuração do IP do servidor e configure o IP publico de sua máquina e refaça os testes. Note que o acesso será perdido no servidor e sua máquina voltará a fazer o acesso ao File Share*

![image](https://user-images.githubusercontent.com/107069287/195178426-b8a33b84-c821-49ad-90e2-dd0df518d4f3.png)

Concluido essa etapa a tarefa foi concluída com êxito. 

Remoção dos recursos passo a passo: 
- Primeiro remova o storage sync. 

No portal pesquise por Storage Sync Server: 

![image](https://user-images.githubusercontent.com/107069287/195179451-18801a5d-c067-4565-8c6b-9f1101447720.png)

Clique no sto104sync: 

![image](https://user-images.githubusercontent.com/107069287/195179563-df005101-87e5-42f3-8bad-4cd011306b7a.png)

Acesse o Group-FS: 

![image](https://user-images.githubusercontent.com/107069287/195179668-dbd3adc9-c2cc-4dbd-8833-d3a2211f38ac.png)

Em FS-01 clique nos ... em seguida clique em Delete: 

![image](https://user-images.githubusercontent.com/107069287/195179805-23f257d6-3f35-4508-a0ff-ae50df25363c.png)

Em seguida, vá até as opções do sto104sync e clique Registered Servers: 

![image](https://user-images.githubusercontent.com/107069287/195180544-af477ce2-ef45-4472-8a9e-64c78412c96f.png)

Clique em ... e em seguida clique em Unregister server: 

![image](https://user-images.githubusercontent.com/107069287/195180722-5ab28aa0-1a45-423e-be7e-6cb1487ac3db.png)

Digite o nome do endpoint e em seguida clique em Unregister: 

![image](https://user-images.githubusercontent.com/107069287/195180870-8c90079c-e4f2-4b8d-a40d-3b9ed4568702.png)

Vá novamente em Sync Groups e em seguida clique em Group-FS: 

![image](https://user-images.githubusercontent.com/107069287/195181048-cc3799dc-7896-4207-b771-14bf4f91d2ef.png)

Clique no File Share que criamos em seguida clique nos ... em seguida clique em Delete: 

![image](https://user-images.githubusercontent.com/107069287/195181194-900d3d3b-9718-4466-a8e0-c799d3fedcad.png)

Remova o syncgroup que criamos sto104sync: 

![image](https://user-images.githubusercontent.com/107069287/195181861-668a6eb2-cf55-485b-b8c7-cc9e2dcbd62e.png)


Feito essa etapa pode deletar todos os Recursos que criamos durante essa atividade. 

