# AZ-104-LAB-MOD-05

 <h2>Lab 05b - Configuração de VPN</h2> <br>

 ***Tarefa 4:***  <br>
    *Deploy Local Network Gateway*

Pré-requisitos: 
- Conexão RDP com a máquina conforme a atividade anterior. 
- IP público configurado corretamente conforme a atividade anterior. 

No portal do Azure, no campo de pesquisa digite Local Network Gateway: 

![image](https://user-images.githubusercontent.com/107069287/192557085-2523e730-33ed-4dde-b248-f72cbfd321d2.png)

Em seguida clique em + Create: 

![image](https://user-images.githubusercontent.com/107069287/192557347-91f03323-ec55-45ac-844f-6e534d390602.png)

Abra uma nova guia e copie o IP publico da máquina destinada ao firewall. 

Digite no campo de pesquisa Virtual Machine: 

![image](https://user-images.githubusercontent.com/107069287/192558363-2338c8ca-35b3-4404-9ebd-a56c65cb6645.png)

Em seguida clique VM-FW-OnPremises: 

![image](https://user-images.githubusercontent.com/107069287/192558480-41055951-9879-4cb4-abd4-3631918dbab5.png)

Em Overview copie o endereço público da virtual machine: 

![image](https://user-images.githubusercontent.com/107069287/192558789-65fbd389-886a-4b5e-b075-77dc413436a0.png)

Volte para a aba anterior e agora iremos configurar conforme as configurações da imagem: <br> 
*OBS: No campo IP Address iremos copiar o ip público que coletamos da máquina virtual VM-FW-OnPremises*

 ![image](https://user-images.githubusercontent.com/107069287/192559775-f6a1c636-cb9c-45b3-8196-764020c102d8.png)

Clique em Next. 

Em Advanced, não iremos fazer nenhuma alteração, apenas clique em Next: 

![image](https://user-images.githubusercontent.com/107069287/192560068-1513ed3a-1aee-4aed-8414-a02b660860fc.png)

Depois clique em Review + Create e em seguida Create e aguarde o término do deploy. 

