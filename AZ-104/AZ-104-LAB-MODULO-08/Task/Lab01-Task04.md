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

Preencha os campos conforme a imagem abaixo: 

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







