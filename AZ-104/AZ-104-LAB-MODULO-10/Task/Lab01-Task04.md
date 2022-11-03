# AZ-104-LAB-MOD-10

 <h2>Lab 10 - Azure Backup</h2> <br>

 ***Tarefa 4:***  
    *Execute a recuperação da VM.*

Dentro do portal, na home do Azure, digite no campo de pesquisa Virtual Machine: 

![image](https://user-images.githubusercontent.com/107069287/199803959-31d9d5b3-03f2-497a-a3dd-31af9ccffc34.png)

Clique na máquina virtual que criamos na atividade anterior: 

![image](https://user-images.githubusercontent.com/107069287/199804158-22d2328a-32c9-49df-94c4-fe2c39185f47.png)

Em seguida iremos acessa-la. Em Overview clique em connect e em seguida RDP: 

![image](https://user-images.githubusercontent.com/107069287/199804363-6d1f4d50-5c01-48d2-a9e8-177001a6685d.png)

Em seguida clique em Download RDP File: 

![image](https://user-images.githubusercontent.com/107069287/199804504-902c980b-486f-4626-9d93-3e63eac75963.png)

Em seguida execute o arquivo e conecte na máquina: 

![image](https://user-images.githubusercontent.com/107069287/199805614-3f4b02e5-7eb3-4725-b50f-a91e96d02cb6.png)

Digite o usuário e a senha da máquina que criamos no portal: 

![image](https://user-images.githubusercontent.com/107069287/199805895-702da9ed-2ab3-4c1e-a430-fbb641fcec79.png)

Clique em sim: 

![image](https://user-images.githubusercontent.com/107069287/199806024-2f6d0daa-06be-4183-827b-4b4f202d7685.png)

![image](https://user-images.githubusercontent.com/107069287/199811627-63dbbd3a-f35e-4a75-9336-a05c03e09e66.png)

Feito o acesso, vamos remover o arquivo hosts na máquina. Use o caminho abaixo: 

C:\Windows\System32\drivers\etc 

![image](https://user-images.githubusercontent.com/107069287/199817158-9f56ed97-765d-47e6-b2e2-b7cd0943525d.png)

Feito o delete do arquivo, minimize a máquina e volte ao portal do Azure. 

![image](https://user-images.githubusercontent.com/107069287/199817315-b450c234-ecdf-45d9-a0ef-5695dbe1b757.png)

Vá novamente ao Recovery Service Vault: 

![image](https://user-images.githubusercontent.com/107069287/199817555-369c834c-4148-4b53-b0c3-8362bc623286.png)

Clique no rsv-az104 que criamos: 

![image](https://user-images.githubusercontent.com/107069287/199817704-16300684-cef4-4f8b-9233-f874914cb812.png)

Em seguida clique em Backup itens: 

![image](https://user-images.githubusercontent.com/107069287/199818088-3d7158e6-c795-4bfa-a21a-c547eb1e71c1.png)

E em seguida Azure Virtual Machines: 

![image](https://user-images.githubusercontent.com/107069287/199818215-d939fe50-1d56-4d13-9284-38b16fdea8cc.png)

Em vm-bkp01, clique em View Details: 

![image](https://user-images.githubusercontent.com/107069287/199818795-39eb9e37-4a23-4847-ad39-16342969f025.png)



