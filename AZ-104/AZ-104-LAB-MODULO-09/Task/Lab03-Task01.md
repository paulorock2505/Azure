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





