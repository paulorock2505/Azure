# AZ-104-LAB-MOD-05

 <h2>Lab 05b - Configuração de VPN</h2> <br>

 ***Tarefa 2:***  <br>
    *Criar estrutura de rede para simular o ambiente On-Premises*

No portal do Azure, na barra de pesquisa, busque por Resource Group: 

![image](https://user-images.githubusercontent.com/107069287/191776472-0e770e3f-156e-4e95-9f32-36fd3be542cb.png)

Em seguida clique em + Create: 

![image](https://user-images.githubusercontent.com/107069287/191776647-91010b1b-1fd5-4975-a110-6b832013468c.png)

Vamos criar o recurso conforme a imagem abaixo: 

![image](https://user-images.githubusercontent.com/107069287/191777197-f0d31de3-6da3-4c82-914d-26c1a410e745.png)

Clique em Next. 

Em TAGs, para mantermos o hábito das marcações, iremos preencher conforme a imagem: 

![image](https://user-images.githubusercontent.com/107069287/191777959-e7fe48ed-8f52-4b43-bbd6-52b3adc49fa8.png)

Em seguida clique em Review + Create e em seguida Create. 

Na sequência iremos criar a Virtual Network para esse RG que acabamos de criar. 

Volte a Home do Azure, no campo de pesquisa, digite Virtual Network: 

![image](https://user-images.githubusercontent.com/107069287/191778805-162c54bf-24fc-444d-9f00-8b569ff99be3.png)

Clique em + Create: 

![image](https://user-images.githubusercontent.com/107069287/191778951-3601c88a-b51a-4a93-bb24-f69b4d0723cc.png)

Em Basics, preencha a descrição conforme a ilustração: <br>
*OBS: Ao selecionar o Grupo de Resource certifique-se de que a região está no local correto que foi configurado, caso não, altere a região para Westus 2.*

![image](https://user-images.githubusercontent.com/107069287/191779714-c4f30c65-f03e-4a7f-a248-6d891e2a031b.png)

Clique em Next. 

Em Security, não iremos fazer nenhuma alteração: 

![image](https://user-images.githubusercontent.com/107069287/191779877-5441222a-f63f-4d0d-84ed-58b2442303d8.png)

Clique em Next. 

Em IP Address, iremos excluir a configuração default para criarmos a estrutura nova. 
Clique em ... e em seguida Delete Address Space: 

![image](https://user-images.githubusercontent.com/107069287/191780241-d0874830-454a-411e-8d53-4ad8a3728f1b.png)

Em seguida clique em Add an IP adress space: 

![image](https://user-images.githubusercontent.com/107069287/191780468-d760be2f-aedf-4e7a-b437-a879420131b5.png)

Configure o endereço de IP com o scopo 192.168.0.0/16: 

![image](https://user-images.githubusercontent.com/107069287/191780838-617eddcc-6336-4168-b8f9-2b2863eb9e0b.png)

Clique em Add. 

Na sequência clique em + Subnet: 

![image](https://user-images.githubusercontent.com/107069287/191781010-f193acf5-866d-4727-a04d-d43fb847974c.png)

Vamos incluir uma Sub rede com a máscara /24. Configure a subnet conforme o escopo abaixo: 

![image](https://user-images.githubusercontent.com/107069287/191781435-2307bee0-f42e-44f7-929b-7536b3ba2c44.png)

Clique em Add.

Clique em Next. 

Em Tags vamos manter os valores que já utilizamos nas atividades anteriores: 

![image](https://user-images.githubusercontent.com/107069287/191781782-b18eb68f-87e8-4047-b45c-135b7825d8b6.png)

Em seguida clique em Review + Create e depois Create. 

Após a criação essa tarefa foi concluída com sucesso. 