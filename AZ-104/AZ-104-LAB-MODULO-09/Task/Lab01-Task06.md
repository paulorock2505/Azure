# AZ-104-LAB-MOD-09

 <h2>Lab 09a - Manage Azure Storage</h2> <br>

 ***Tarefa 6:***  
    *Configure e teste o autoscaling do Azure web app.*

Acesse a home do portal do Azure e no campo de pesquisa digite App Service: 

![image](https://user-images.githubusercontent.com/107069287/196757570-97fbfd5f-274b-4d54-a208-277d2a0f691d.png)

Em seguida, acesse o app service que criamos na task anterior: 

![image](https://user-images.githubusercontent.com/107069287/196757744-79ba4d68-9b74-434d-a6a5-59e98e298b24.png)

Em seguida, abra uma nova guia para configurarmos o insights antes e no campo de pesquisa digite subscriptions: 

![image](https://user-images.githubusercontent.com/107069287/196777598-c3207829-d2f5-4566-9b52-ea4fc7fb544d.png)

Clique na sua assinatura: 

![image](https://user-images.githubusercontent.com/107069287/196777848-37ad22b0-9c6a-45f9-83fd-e8de18ef58e1.png)

Em Settings, clique em Resource Providers: 

![image](https://user-images.githubusercontent.com/107069287/196778035-1391a6f4-c074-44b8-bc5d-72c02758783b.png)

No campo de pesquisa digite microsoft.insights e veja se ele está registrado. Caso não esteja clique em register e registre o recurso: 

![image](https://user-images.githubusercontent.com/107069287/196778384-c79fcefc-fe80-4253-aa42-df8591f9f252.png)

Feito essa etpa, volte a tela anterior e em Settings, clique em Scale Out: 

![image](https://user-images.githubusercontent.com/107069287/196778665-4f125634-629c-41bf-b410-c50b813811d0.png)

Nessa etapa iremos criar um custom auto-scale para a nossa aplicação. Clique em Custom autoscale: 

![image](https://user-images.githubusercontent.com/107069287/196779724-3a6a9b34-8c76-48b0-add4-b513bb5bf307.png)

Em seguida altere o scale mode para Scale Based on a metric e aumente a Instance Limits para o máximo de duas: 

![image](https://user-images.githubusercontent.com/107069287/196780578-83d02577-e7a3-41b4-8a3a-a4808570763b.png)

Em seguida em Rules, clique em Add a rule: 

![image](https://user-images.githubusercontent.com/107069287/196780729-799ad9fe-b6c7-4c26-9da5-9295032a077f.png)

Preencha os campos conforme a imagem abaixo: 

![image](https://user-images.githubusercontent.com/107069287/196781567-cdc9f800-e7bb-414d-a90b-e3b9ae6d1547.png)

![image](https://user-images.githubusercontent.com/107069287/196781649-e2e371cb-3cd2-4281-9cba-8b0500d3b052.png)

Clique em Add. 

Feito essa etpa, volte a tela anterior e em Settings, clique em Scale Out e altere as regras que criamos (Average): 

![image](https://user-images.githubusercontent.com/107069287/196785827-7ecef743-0890-4dba-a9e5-d8890f26ed71.png)

Altere conforma a imagem abaixo e clique em Update: 

![image](https://user-images.githubusercontent.com/107069287/196785955-9a36dcdc-373c-4044-99b9-fa6bb4e74e7d.png)

Em seguida clique em + Add Rule: 

![image](https://user-images.githubusercontent.com/107069287/196788846-e6a81cd0-5f18-435b-8be4-56aaa874e689.png)

Configure os parametros conforme a imagem abaixo: 

![image](https://user-images.githubusercontent.com/107069287/196788916-dfa88276-bd4c-4acf-bc63-0b98eb614bcb.png)

![image](https://user-images.githubusercontent.com/107069287/196789028-5f06575d-d8c5-4c66-8ed2-73aa0d45f310.png)

Clique em Add. 

Configurado essa etapa clique em Save. 

Agora abra o cloudshell na opção Power Shell e execute o comando abaixo: 

$rgName = 'RG-MOD09'

![image](https://user-images.githubusercontent.com/107069287/196782545-2b1662a7-e6ea-4c08-9ab5-7f7bbdb27077.png)

$webapp = Get-AzWebApp -ResourceGroupName $rgName

![image](https://user-images.githubusercontent.com/107069287/196782656-66c56499-80e2-4106-981d-b05b0e8e7e0d.png)

while ($true) { Invoke-WebRequest -Uri $webapp.DefaultHostName }

![image](https://user-images.githubusercontent.com/107069287/196782835-38a4c8c6-da4d-4903-865e-d5f8e4fac7f3.png)

