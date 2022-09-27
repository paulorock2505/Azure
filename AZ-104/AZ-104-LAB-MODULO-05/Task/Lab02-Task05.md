# AZ-104-LAB-MOD-05

 <h2>Lab 05b - Configuração de VPN</h2> <br>

 ***Tarefa 5:***  <br>
    *Deploy VPN Point to Site*

Configuração da VPN P2S:

Tenant:
https://login.microsoftonline.com/coloque seu Tenant ID aqui/

Audience:
41b23e61-6c1e-4545-b367-cd054e0ed4b4

Issuer:
https://sts.windows.net/coloque seu Tenant ID/

 

Link para permissão de uso do aplicativo de VPN no Tenant:

IMPORTANTE: Para liberar a permissão de uso, você deve usar um usuário Global Admin que seja nativo do seu tenant, ou seja, não pode ser usuários @outlook.com, @hotmail.com ...

https://login.microsoftonline.com/common/oauth2/authorize?client_id=41b23e61-6c1e-4545-b367-cd054e0ed4b4&response_type=code&redirect_uri=https://portal.azure.com&nonce=1234&prompt=admin_consent

Vá até o portal e pesquise por Virtual Network Gateway: 

![image](https://user-images.githubusercontent.com/107069287/192593803-243b0b10-33fb-4346-9150-41fbebd1b464.png)

Acesse o Virtual Gateway que criamos, nesse caso VNG-01: 

![image](https://user-images.githubusercontent.com/107069287/192593967-aa561812-e03c-4908-b38b-15afedb3b60a.png)

Clique em Point-to-site-configuration: 

![image](https://user-images.githubusercontent.com/107069287/192594225-f796ad17-4918-4ef6-aecb-ffbff346c00a.png)

Em seguida, clique em configure now: 

![image](https://user-images.githubusercontent.com/107069287/192594325-9495d8e4-e750-4942-9344-4e5e7d6d056d.png)

Nessa etapa, precisamos buscar o tenant id da conta para concluirmos a configuração. Acesse em outra aba a plataforma do Azure e no campo de pesquisa busque por Azure Active Directory: 

![image](https://user-images.githubusercontent.com/107069287/192595350-6158d3bb-e849-489f-91d4-6df106e36bd5.png)

Em Overview, copie o valor do tenant id que está exposto: 

![image](https://user-images.githubusercontent.com/107069287/192595556-c57f188d-6f0d-4d28-8670-8736b85e19d7.png)

Volte a tela e preencha os campos conforme colocamos no início da atividade: 

![image](https://user-images.githubusercontent.com/107069287/192596008-52a0f99b-38cf-4955-998d-0249f279c802.png)

![image](https://user-images.githubusercontent.com/107069287/192596241-e51db0a7-0acd-4bd0-ad1f-54926f32eb86.png)

Em seguida clique em Grant administrator consent for Azure VPN client application:

![image](https://user-images.githubusercontent.com/107069287/192596714-e1033585-9746-4b87-a88c-b9bbd5ae5d0b.png)

Clique em Aceitar: 

![image](https://user-images.githubusercontent.com/107069287/192596962-305bc976-a6ac-42e0-8c66-d4d2560813fc.png)

Aguarde o processamento e em seguida ele redirecionará novamente para o portal do Azure. 

Volte para as configurações e clique em Save: 

![image](https://user-images.githubusercontent.com/107069287/192597184-a41138a8-191a-4b7d-ab98-09c0c3b9a525.png)

Terminado essa etapa, iremos fazer o download do pacote de instalação client de VPN. Clique em Download VPN Client: 

![image](https://user-images.githubusercontent.com/107069287/192598611-7f3b7307-6f37-4395-84ff-44a6a0526591.png)

Após o download extraia o arquivo que contém em pasta de sua escolha. 

A seguir, navegue pelo microsoft store do seu notebook (clientes Windows) e busque por Azure VPN. Ao achar o aplicativo instale ele em seu dispositivo Windows. 

Na captura de tela apareceu abrir, pois já temos o aplicativo instalado na máquina: 

![image](https://user-images.githubusercontent.com/107069287/192625328-30feb98c-9a89-426c-aae0-1ecc8c43e5c6.png)

Após a instalação, clique no sinal de + no rodapé da janela: 

![image](https://user-images.githubusercontent.com/107069287/192625776-5822c0a7-848d-435d-9300-f00e08e8053e.png)

Em seguida clique em importar: 

![image](https://user-images.githubusercontent.com/107069287/192625969-719314c3-ef5d-41e1-a9c8-2cc02f30b110.png)

Aponte para o arquivo azurevpnconfig.xml (ou azurevpnconfig) dentro da pasta AzureVPN: 

![image](https://user-images.githubusercontent.com/107069287/192626450-3ee7fca4-7840-4d59-bbaa-8df6f6375bdb.png)

Em seguida clique em Salvar. 
*Obs: Caso queira mudar o nome da conexão para um nome que você achar melhor, pode alterar, esse nome é apenas o que ficará no display de sua máquina*

Feito essa etapa, salve e teste a conexão. 

*Tarefa Optativa: Teste o acesso nas máquinas que foram criadas neste laboratório e valide as conexões em cada uma delas. A máquina relacionado ao firewall não irá conectar de imediato pois precisará habilitar a transitividade de gateway entre as VNETs. Caso queira habilite conforme estudamos nesta tarefa.*

Após concluirmos essa etapa, todo o laboratório deste módulo foi realizado. 

Por fim, delete todos os recursos que criamos neste laboratório para que não aja cobrança adicional. 

