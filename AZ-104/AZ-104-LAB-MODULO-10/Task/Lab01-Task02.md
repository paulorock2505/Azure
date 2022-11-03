# AZ-104-LAB-MOD-10

 <h2>Lab 10 - Azure Backup</h2> <br>

 ***Tarefa 2:***  
    *Implementar backup em nível de máquina virtual do Azure.*

No portal, no campo de pesquisa digite Virtual Machine: 

![image](https://user-images.githubusercontent.com/107069287/199322009-08ce20a8-a1db-462b-8be9-68747beb6829.png)

Anote o nome da máquina virtual que criamos na tarefa anteior no bloco de notas. 

Em seguida, vá até a home novamente e clique em Recovery Service Vault: 

![image](https://user-images.githubusercontent.com/107069287/199322356-5d2b020b-6df1-49ca-a885-154c69869a8c.png)

Acesse o recovery service vault que criamos: 

![image](https://user-images.githubusercontent.com/107069287/199322463-a4600904-b7e1-4ca8-8035-9ec538247d41.png)

Vá até a opção Backup: 

![image](https://user-images.githubusercontent.com/107069287/199322573-60c7ca4b-bc16-45d8-b3f9-ca48730c179b.png)

Nesta etapa iremos criar a rotina de backup em uma máquina virtual que está no Azure. 

Faça a configuração conforme a imagem abaixo: 

![image](https://user-images.githubusercontent.com/107069287/199322928-2d19721e-e0aa-4a6d-aea5-891ca3c4913a.png)

Em seguida, em backup policy, clique em Create new: 

![image](https://user-images.githubusercontent.com/107069287/199324031-33523091-9f86-4dcf-b164-d182daa609c9.png)

Configure as politicas de backup conforme a imagem abaixo: 

![image](https://user-images.githubusercontent.com/107069287/199324207-ef882bf4-5ed5-4a63-82ba-75a9009f8230.png)

Clique em Ok. 

Em virtual machines clique em Add: 

![image](https://user-images.githubusercontent.com/107069287/199324506-2575fe24-661c-41be-8c49-d726883c33c4.png)

Selecione a virtual machine elegível para criarmos a rotina de backup: 

![image](https://user-images.githubusercontent.com/107069287/199728603-df983e3e-c637-4fc3-8bae-941e3db8d759.png)

Marque a máquina que temos disponível e clique em Ok. 

Em seguida clique em enable backup: 

![image](https://user-images.githubusercontent.com/107069287/199729248-800dccb4-3ca9-4ee0-90ee-6a584aa0bf43.png)

Clique em Go to Resource e valide a criação da política de backup em Backup itens. 

Feito essa etapa a atividade foi concluída. 
