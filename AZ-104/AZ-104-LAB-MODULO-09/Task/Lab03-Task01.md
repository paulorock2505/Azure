# AZ-104-LAB-MOD-09

 <h2>Lab 09c - Implement Azure Kubernets Service</h2> <br>

 ***Tarefa 1:***  
    *Implantar um cluster do Azure Kubernetes Service e realizar tarefas de gerenciamento.*

***Modo 01 - Configuração por interface gráfica***

No portal, no campo de pesquisa digite Kubernetes: 

![image](https://user-images.githubusercontent.com/107069287/198093194-ced0804f-94c3-407a-b8d9-96e9d1164e9f.png)

Em seguida, acessando a opção clique em + Create e em seguida clique em + Create a Kubernets Cluster: 

![image](https://user-images.githubusercontent.com/107069287/198093394-fa5c86e1-ed43-40e5-8479-8a3d8d6eb83e.png)

Configure o Kubernetes de acordo com a imagem abaixo: 

![image](https://user-images.githubusercontent.com/107069287/198096690-7c07c149-4430-416e-8bfc-91c9358ab3bb.png)

![image](https://user-images.githubusercontent.com/107069287/198096782-6f86566b-1b2b-4518-9834-a32af90be9cd.png)

![image](https://user-images.githubusercontent.com/107069287/198096858-d7809a57-3036-49c3-b421-057d7db75596.png)

Em seguida clique em Next. 

Em Node Pool mantenha as configurações abaixo: 

![image](https://user-images.githubusercontent.com/107069287/198097125-b4dadae4-fd64-43d2-9878-e578c2913348.png)

Clique em Next. 

Em Acess também vamos manter o padrão proposto pelo Azure conforme a imagem: 

![image](https://user-images.githubusercontent.com/107069287/198099319-4541f529-d6be-4cc4-987c-325cd0cd168c.png)

Clique em Next. 

Em Networking, altere o network configuration para o Azure CNI e as demais configurações mantenha o padrão: 

*OBS: Note que será criado uma subnet default para o Kubernetes, bem como serviço de endereço para o range, um serviço de DNS e um Docker Bridge Access.*

![image](https://user-images.githubusercontent.com/107069287/198100247-7f37f536-0c87-44cd-8adf-2b0572432335.png)

![image](https://user-images.githubusercontent.com/107069287/198100317-66ce1548-73b7-43aa-b8d2-8c784ac007d6.png)

![image](https://user-images.githubusercontent.com/107069287/198100354-0ad1a006-2585-437c-a383-855dc5d63db3.png)

Clique em Next. 

Em integrations mantenha o padrão abaixo: 

![image](https://user-images.githubusercontent.com/107069287/198100752-839cee92-5430-42e2-9780-b428f2704e2b.png)

Em seguida clique em next. 

Em TAGs configure conforme a imagem abaixo e como já usamos nas demais tarefas: 

![image](https://user-images.githubusercontent.com/107069287/198101056-26480829-6ce7-485e-9506-599e87bc4a1e.png)

Em seguida clique em Create e depois em Review + Create. 

*OBS: Essa é a etapa que utilizaríamos para criar o Kubernetes utilizando a interface gráfica. Em ambientes de produção raramente utilizamos esse processo, na maioria das vezes utilizamos sempre o azure CLI.*

***Modo 02 - Configuração por Azure CLI*** 

No portal, no canto superior a direita, abra o CloudShell: 

![image](https://user-images.githubusercontent.com/107069287/198101795-bef1bcd3-fd9a-4071-9267-041d67d488e3.png)

Ao abrir clique no quinto item da esquera para a direita para abrir o CloudShell em uma segunda aba: 

![image](https://user-images.githubusercontent.com/107069287/198102603-25510347-1508-4249-9ca0-179aa6a0dca6.png)

![image](https://user-images.githubusercontent.com/107069287/198103011-aaf17921-cb76-4631-b604-56682feb53b2.png)

Faça o download dos arquivos abaixo para usar como guia para a execução dos comando a seguir: 

[Yaml-AKS (1).txt](https://github.com/paulorock2505/Microsoft-Azure-Jobs/files/9872547/Yaml-AKS.1.txt)

[AKS (1).txt](https://github.com/paulorock2505/Microsoft-Azure-Jobs/files/9872558/AKS.1.txt)

Abra o arquivo e execute os dois primeiros comandos: 

az provider show -n Microsoft.OperationsManagement -o table <br>
az provider show -n Microsoft.OperationalInsights -o table <br>

![image](https://user-images.githubusercontent.com/107069287/198104150-90396768-f88c-485e-b718-142870719689.png)

![image](https://user-images.githubusercontent.com/107069287/198104219-6ca2ca65-7789-4023-ab1e-eac7b5fd1a4a.png)

Caso ele retorne o comando como mostrado na tela, NotRegistred, use o comando a seguir para registrar: 

az provider register --namespace Microsoft.OperationsManagement <br>
az provider register --namespace Microsoft.OperationalInsights <br> 

Note, que depois de executar, ao usar o az provider show -n (OperationsManagement e OperationalInsights)
o retorno será Registered: 

![image](https://user-images.githubusercontent.com/107069287/198105265-7e45fdb0-5f97-43c2-909f-2dc814006ce5.png)

Na segunda etapa iremos criar o Resource Group: 

az group create --name "RG-ALPALABS" --location eastus <br>

![image](https://user-images.githubusercontent.com/107069287/198105831-cf107d69-a0f0-4e1d-af18-d8df15552f71.png)

![image](https://user-images.githubusercontent.com/107069287/198105892-5dddf425-8b15-4af1-add3-0992d0b14899.png)

Na terceira etapa iremos fazer a configuração do Cluster: 

az aks create --resource-group "RG-ALPALABS" --name AKSALPA01 --node-count 1 --enable-addons monitoring --generate-ssh-keys <br>

![image](https://user-images.githubusercontent.com/107069287/198106204-c33e90fe-2327-4d0f-9fe6-76094aa9e14d.png)

Aguarde até o fim do deploy. 

Na sequência, baixe as credenciais de acesso: 

az aks get-credentials --resource-group "RG-ALPALABS" --name AKSALPA01

![image](https://user-images.githubusercontent.com/107069287/198110179-069da977-fe72-4a84-8a14-f98e32edbfe4.png)

Valide o deploy dos nodes: 

kubectl get nodes 

![image](https://user-images.githubusercontent.com/107069287/198110475-310cb2c5-1697-452d-97c1-d56f90c136f2.png)

![image](https://user-images.githubusercontent.com/107069287/198110535-5c1603b3-ed61-4674-bddb-7575618ba0f4.png)

Na sequência iremos criar um arquivo Yaml para testarmos a nossa aplicação. Acesse o visual code dentro do azure para criarmos a nossa estrutua: 

code azure-vote.yaml

![image](https://user-images.githubusercontent.com/107069287/198111824-585ed59e-c806-4482-9de9-ab6632253642.png)

Note que abrirá um arquivo vazio. Ainda não criamos o nosso código. 

![image](https://user-images.githubusercontent.com/107069287/198111952-1b83197b-3c6c-4452-aa21-77880e7a3456.png)

Abra o arquivo que foi disponibilizado no ínicio, YAML-AKS, abra em um bloco de notas, copie o código por completo e cole no visual code no portal: 

![image](https://user-images.githubusercontent.com/107069287/198112889-db73860f-8255-4c35-9cff-15d4c8e59431.png)

Em seguida clique com o botão direito do mouse e clique em Save e em seguida Quit. 

Agora iremos fazer o Deploy do arquivo Yaml: 

kubectl apply -f azure-vote.yaml

![image](https://user-images.githubusercontent.com/107069287/198114315-77d7e3e8-ac41-4502-8843-a68ddf27b570.png)

Na sequência verifique se o IP da aplicação. Utilize o comando abaixo: 

kubectl get service azure-vote-front --watch

![image](https://user-images.githubusercontent.com/107069287/198114706-a5cdd0b4-6836-4ded-bdc1-b838844f9acc.png)

*Note que o ip público está sendo fornekcido por um load balancer* 

Dê um Ctrl + C para parar a escuta da aplicação. 

Vamos validar os deployments com o comando abaixo: 

kubectl get deployments

![image](https://user-images.githubusercontent.com/107069287/198116005-6b813bbb-f840-4d53-bb0c-f4f1895d0169.png)

Note que agora possuímos duas aplicações: 

![image](https://user-images.githubusercontent.com/107069287/198116126-62dd1593-cca0-468d-b210-5dcf770fcebc.png)

Valide os pods que foram criados com o comando abaixo: 

kubectl get pods --show-labels

![image](https://user-images.githubusercontent.com/107069287/198116564-30b1dae0-5933-4f2c-94c5-b0eaffae93fa.png)

![image](https://user-images.githubusercontent.com/107069287/198116602-bb5920b0-e5bf-47b2-8dc6-7854931a7596.png)

Vamos escalar nossa aplicação adicionando mais um pod: 

kubectl scale --replicas=2 deployment/azure-vote-front 

Note que em 4 s ele cria uma nova instância: 

![image](https://user-images.githubusercontent.com/107069287/198117854-c0eac1c8-a200-4a3f-bd39-5a179a36b6f2.png)

Altere as replicas para 10 e veja o resultado: 

kubectl scale --replicas=10 deployment/azure-vote-front

Note a velocidade que é criado cada pod. 

![image](https://user-images.githubusercontent.com/107069287/198118525-dc88f1ac-4468-4cdb-b15a-47d6edb233ac.png)

Note que após a criação, ainda ficou um node com status de pending: 

![image](https://user-images.githubusercontent.com/107069287/198129069-73d85799-17e7-4d0b-bcec-3d5ba077de31.png)

Vamos instanciar novos pods com o comando abaixo: 

az aks scale --resource-group "RG-ALPALABS" --name AKSALPA01 --node-count 2

Após a criação do node o status de pending da máquina ficou no mesmo estado que as outras: 

![image](https://user-images.githubusercontent.com/107069287/198133546-5b616046-0a5c-471e-8d4e-5f443ab346e7.png)

Por fim valide em qual node estão os pods com o comando abaixo: 

kubectl get pod -o=custom-columns=NODE:.spec.nodeName,POD:.metadata.name

![image](https://user-images.githubusercontent.com/107069287/198133806-cd3fb0e4-4900-4cbd-bf93-1ea395b0f1d2.png)

Após essa etapa a atividade foi concluída com sucesso. 

Pode remover todos os recursos que criamos neste laboratório. 





