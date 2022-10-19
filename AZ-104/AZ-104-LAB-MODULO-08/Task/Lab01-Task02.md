# AZ-104-LAB-MOD-08

 <h2>Lab 08 - Manage Virtual Machines</h2> <br>

 ***Tarefa 2:***  
    *Configure as máquinas virtuais do Azure usando extensões de máquina virtual.*

Recursos:<br>
https://github.com/paulorock2505/Microsoft-Azure-Jobs/files/9803101/Instala_IIS.zip

No portal do Azure, no campo de pesquisa digite Virtual Machine: 

![image](https://user-images.githubusercontent.com/107069287/196232151-940a8f03-cf5b-447d-81d1-d2fbbe1fc3ad.png)

Clique em VM01: 

![image](https://user-images.githubusercontent.com/107069287/196232255-1e0be1ec-5f45-4204-aab0-03e8f4399fd9.png)

Em Settings, clique em Extensions + Applications: 

![image](https://user-images.githubusercontent.com/107069287/196232519-955b9840-2820-4786-a841-9e7050021050.png)

Em extensions, clique em + Add: 

![image](https://user-images.githubusercontent.com/107069287/196232619-4cd60c84-c509-4501-af7e-757cec59270a.png)

No campo de pesquisa, busque por Custom Script Extension: 

![image](https://user-images.githubusercontent.com/107069287/196234258-dc6f48d4-59c4-4936-b8d1-59212bdedca4.png)

Clique uma vez e em seguida clique em Next: 

![image](https://user-images.githubusercontent.com/107069287/196234417-682f367a-efd1-4287-9a40-8f44d6e4caa8.png)

Em seguida clique em Browse: 

![image](https://user-images.githubusercontent.com/107069287/196234944-ba01a8da-7ebb-4eb3-bb5e-0a89721f19f8.png)

Crie um novo storage account para armazenar os scripts. Clique em + Storage Account: 

![image](https://user-images.githubusercontent.com/107069287/196235181-e6629749-0f28-4c40-a25e-35da2c57dc39.png)

Preencha as informações como o modelo abaixo: 

![image](https://user-images.githubusercontent.com/107069287/196235400-c3c7b061-11e5-49ae-8688-4d1332609b31.png)

Em seguida clique em Ok. 

![image](https://user-images.githubusercontent.com/107069287/196235549-0d529385-4393-4c80-b456-412a6f0dc6fd.png)

Feito isso clique no storage account que acabamos de criar: 

![image](https://user-images.githubusercontent.com/107069287/196236006-fbd95e00-efc8-48e8-88a8-13916c1d7fcc.png)

Em seguida clique em + Container para criarmos um container para o nosso storage account: 

![image](https://user-images.githubusercontent.com/107069287/196236161-088d69f3-7ddb-4185-8c0f-813f3880bd02.png)

Preencha conforme a imagem abaixo: 

![image](https://user-images.githubusercontent.com/107069287/196236358-7d3cde33-a955-4cf8-a50d-c848c8fdeadd.png)

Clique em Create. 

Em seguida clique no container scriptaz104 e iremos fazer o upload do arquivo ps1. 

Clique em upload: 

![image](https://user-images.githubusercontent.com/107069287/196237062-fcbf8f28-ed05-42ed-a74e-396d1fece50e.png)

Descompacte o arquivo que fizemos o download nos recursos no início do laboratório, em seguida, em files, busque o arquivo .ps1: 

![image](https://user-images.githubusercontent.com/107069287/196237414-625a3adb-03e1-493b-97f4-4e7a21332413.png)

Em seguida clique em upload: 

![image](https://user-images.githubusercontent.com/107069287/196237494-ae049bc0-0664-4aa7-a50e-7f3e5826175a.png)

![image](https://user-images.githubusercontent.com/107069287/196237583-01a45d82-6cc3-4b2a-b1b3-2bc86a2ba0bf.png)

Em seguida selecione o script e clique em select: 

![image](https://user-images.githubusercontent.com/107069287/196237778-2cd742b2-b825-4cb2-a088-ae5dff4077a3.png)

Em seguida clique em Review + Create e em seguida Create. 

Feito essa etapa, em Overview copie o ip publico da máquina e teste o link. 

Note que o IIS foi instalado e e mensagem no browser é: 

Hello World from VM01 

Faça o mesmo processo para a VM02. 

Após essa etapa, crie uma regra para liberar a porta 80 para a VM01. 

Em VM02, vá até networking: 

![image](https://user-images.githubusercontent.com/107069287/196245243-403c2125-f42d-4f8c-bca4-3151221c411f.png)

Em seguida clique em Add inbound port rule: 

![image](https://user-images.githubusercontent.com/107069287/196245590-9fffa9e9-c0ca-4c09-9466-ea6ba80468ce.png)

Preencha os campos conforme a imagem abaixo e em seguida clique em Add: 

![image](https://user-images.githubusercontent.com/107069287/196246538-984426e6-5e4d-4046-a6f5-1a30d3998cf4.png)

Feito essa etapa a tarefa foi concluída. 







