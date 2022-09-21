# AZ-104-LAB-MOD-05

 <h2>Lab 05 - Configuração de VPN</h2> <br>

 ***Tarefa 2:***  <br>
    *Criar configuração de peering entre VNETs.*

No portal, no campo de pesquisa, busque por Virtual Network: 

![image](https://user-images.githubusercontent.com/107069287/191541021-3adbdf96-9e0d-43ed-bdae-7f4676a66353.png)

Clique em VNET-USA01: 

![image](https://user-images.githubusercontent.com/107069287/191541196-7cb05771-b974-4e70-9a33-7458110a9362.png)

Em seguida, na área Settings, clique em Peerings: 

![image](https://user-images.githubusercontent.com/107069287/191541397-ccb2bec6-8758-42e7-bf79-e0b874f975ff.png)

Clique em + Add: 

![image](https://user-images.githubusercontent.com/107069287/191541610-67c5327c-9480-48f4-85ec-fa5656920db1.png)

Configure o pering conforme a imagem abaixo: <br>
*OBS: Na nomenclatura usamos o padrão Vnet de Origem para Vnet de Destino. Nesse caso utilizamos dessa forma para que fique fácil a identificação do pering em ambos os lados. É importante também selecionar a Vnet de Destino na área Remote virtual network.*

![image](https://user-images.githubusercontent.com/107069287/191542902-370e82da-ab9e-4f72-939a-ee406a6dd395.png)

![image](https://user-images.githubusercontent.com/107069287/191543036-5ec21f71-7a69-4348-98ab-6e312c671ec0.png)

![image](https://user-images.githubusercontent.com/107069287/191543099-0277a4ea-bc9b-45ef-b5cc-6e88cfc9af41.png)

Em seguida clique em Add. 

Novamente no campo pering, vamos criar nosso segundo pering. 

Clique em + Add: 

![image](https://user-images.githubusercontent.com/107069287/191544653-c8b8618f-1bed-4a59-ad14-abc2d6f6135c.png)

Agora vamos criar o pering para a Europa. Configure os parametros conforme a imagem abaixo: 

![image](https://user-images.githubusercontent.com/107069287/191544977-94f65d9f-e921-4a60-a78c-6845758a67ba.png)

![image](https://user-images.githubusercontent.com/107069287/191545188-50302811-ef56-4ae5-9839-a2eb539366f8.png)

![image](https://user-images.githubusercontent.com/107069287/191545314-7ceddac7-fe2e-4536-991d-c5bf7f43fceb.png)

Clique em Add. 

Após essa etapa a tarefa foi concluída. 




