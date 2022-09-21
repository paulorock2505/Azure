# AZ-104-LAB-MOD-05

 <h2>Lab 05 - Configuração de VPN</h2> <br>

 ***Tarefa 1:***  
    *Criar estrutura de rede usando 3 VNETs em regiões diferentes, com suas respectivas Subnets.*

Acesse o portal e em home pesquise por Resource Groups: 

![image](https://user-images.githubusercontent.com/107069287/191505212-f619a413-369b-4e01-ae65-ccd9248c0441.png)

Clique em + Create: 

![image](https://user-images.githubusercontent.com/107069287/191505345-8d1e103e-65ae-4d1f-bca6-b38c4b6bfa09.png)

Crie o Resource Group da maneira como quiser, neste exemplo estou seguindo o diagrama da tarefa: 

![image](https://user-images.githubusercontent.com/107069287/191505759-30f17aa7-56d4-4920-8244-7a597f320adf.png)

Clique em Next. 

Na aba TAGs para mantermos o hábito, iremos criar a TAG referenciando o nosso laboratório: 

![image](https://user-images.githubusercontent.com/107069287/191506136-8aeae22a-dd19-466e-a2e6-c777226aaff4.png)

Clique em Review + Create e em seguida create para criarmos o nosso Recurso. 

Na seuqência iremos criar as nossas Virtual Networks. 

Acesse o recurso que acabamos de criar: 

![image](https://user-images.githubusercontent.com/107069287/191506795-f4b655f1-2a83-4753-b30f-a1f65cfd7ea7.png)

Em Overview, clique em + Create: 

![image](https://user-images.githubusercontent.com/107069287/191506905-04c30f2f-ffc8-4339-aada-36bccfc1d3b8.png)

No campo de pesquisa, busque por Virtual Network: 

![image](https://user-images.githubusercontent.com/107069287/191507167-df8b83b9-a23c-4a17-af29-bdd29f966959.png)

Em virtual Network clique em Create e em seguida Virtual Network: 

![image](https://user-images.githubusercontent.com/107069287/191507379-78a9b537-c0bb-4241-a2b1-5668c12f0ade.png)

Na sequência criaremos todas as nossas VNETs, respeitando o diagrama. 
*OBS: Para configurar as VNETs, utilizem como guia o diagrama que está no README deste módulo.*

Neste momento iremos criar a primeira VNET, conforme a imagem abaixo: <br>
***Atenção: A microsoft fez uma alteração no ambiente gráfico do portal, irei aplicar as configurações baseado no novo modelo.***

![image](https://user-images.githubusercontent.com/107069287/191508943-6db814ec-dc5a-4ab3-a0a5-e1f91a7b166e.png)

Clique em Next. 

Em Security não iremos fazer nenhuma alteração. 

![image](https://user-images.githubusercontent.com/107069287/191509125-9f2c4a12-c953-4ea7-a90d-c6fe612c1839.png)

Clique em Next. 

Em IP Address note que já temos uma configuração aplicada por padrão, podemos aplicar nossas configurações de duas maneiras, utilizando o resize address space ou delete address space. Neste exemplo irei deletar. Clique em ... em seguida Delete Address Space: 

![image](https://user-images.githubusercontent.com/107069287/191510679-2d70ca95-6f9a-4a0b-a3ae-b103b16b72fb.png)

Agora iremos criar um novo Ip Address Space, Clique em Add an IP address space: 

![image](https://user-images.githubusercontent.com/107069287/191510949-ebb9919e-8e95-4c41-9a4f-78d7c116a554.png)

Coloque as configurações conforme nosso diagrama: 

![image](https://user-images.githubusercontent.com/107069287/191511100-2c0c3537-8938-47f3-9f49-5f7be4f91368.png)

Clique em Add. 

Em seguida clique em + Subnet: 

![image](https://user-images.githubusercontent.com/107069287/191511796-841c0f22-1ec1-43b5-8ccc-ddc28285b412.png)

Configure a Subnet como definimos no diagrama: 

![image](https://user-images.githubusercontent.com/107069287/191511697-c5ff55c7-9582-4310-a619-99ba80b2a0a7.png)

Clique em Add. 

Em seguida iremos criar a segunda subnet.

Clique em + Add Subnet: 

![image](https://user-images.githubusercontent.com/107069287/191512172-25bfcc9a-f6f2-446d-b818-10d3ef721ea5.png)

Configure a segunda Subnet: 

![image](https://user-images.githubusercontent.com/107069287/191512528-65dccbad-c2f4-4140-8530-3e2cd90c5140.png)

Clique em Add. 

Em seguida clique em Next. 

Em TAGs, adicione as mesmas TAGs que usamos no grupo de recursos: 

![image](https://user-images.githubusercontent.com/107069287/191513079-610e7917-9afb-4bb8-9113-8ef86f09adf7.png)

Em seguida clique em Review + Create e em seguida clique em Create. 

Ao finalizar a criação da VNET, acesse a home do portal e no campo de pesquisa digite Virtual Network para criarmos a nossa segunda VNET: 

![image](https://user-images.githubusercontent.com/107069287/191514882-14160b37-19e5-4d7e-b9ee-ff41e02f8299.png)

Clique em + Create: 

![image](https://user-images.githubusercontent.com/107069287/191515063-254715d0-fccf-4f33-906c-479b971e4f9f.png)

Criaremos a nossa segunda VNET que estará localizada na região da europa: 

![image](https://user-images.githubusercontent.com/107069287/191515523-5c587692-34b0-40bc-baeb-52d90148d8d6.png)

Clique em Next. 

Em Security não alteraremos nada: 

![image](https://user-images.githubusercontent.com/107069287/191515992-0bdc2965-c6a6-4b54-b972-4ee884344da8.png)

Clique em Add. 

Novamente clique em + Add a Subnet: 

![image](https://user-images.githubusercontent.com/107069287/191517900-afe1bebe-edd0-4bb8-ab24-db9139ebf10e.png)



Clique em Next. 

Em IP Address clique em ... em seguida Delete Address Space:

![image](https://user-images.githubusercontent.com/107069287/191517129-992180a2-6db8-4bb8-87c4-83e0f4e00ec8.png)

Clique em Add an IP Address space: 

![image](https://user-images.githubusercontent.com/107069287/191517372-2954bef4-dc13-4ec3-9d15-b063b4f8df2d.png)

Configure o IP novamente conforme o nosso escopo: 

![image](https://user-images.githubusercontent.com/107069287/191517693-22b1164f-1d7c-4295-8d2f-bbebb591046a.png)

Após essa etapa, vamos add nossa Subnet, clique em + Add a subnet: 

![image](https://user-images.githubusercontent.com/107069287/191521518-79d98fa4-a0e0-4e08-aceb-f7e2e9edf4ff.png)

Em seguida configure conforme o escopo do Laboratório: 

![image](https://user-images.githubusercontent.com/107069287/191522001-c7e41919-1892-4883-affd-6a731e7eda1a.png)

Clique em Add. 

Em seguida clique em Next. 

Preencha as TAGs para mantermos o hábito de utilizarmos: 

![image](https://user-images.githubusercontent.com/107069287/191522984-3c8c838c-3f3f-4869-80fe-20b39fb20f9b.png)

Em seguida clique em Review + Create e em seguida Create. 




