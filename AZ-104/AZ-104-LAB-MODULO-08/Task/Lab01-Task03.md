# AZ-104-LAB-MOD-08

 <h2>Lab 08 - Manage Azure Storage</h2> <br>

 ***Tarefa 3:***  
    *Dimensione o tamanho de máquina para Azure VM.*

No portal do azure, no campo de pesquisa digita Virtual Machine: 

![image](https://user-images.githubusercontent.com/107069287/196250773-1301b896-6278-40fd-be0e-1e6ffd604794.png)

Clique em VM02: 

![image](https://user-images.githubusercontent.com/107069287/196250835-72866c1e-c83a-4786-95bb-a70f23683219.png)

Navegue até o campo Settings e clique em Size: 

![image](https://user-images.githubusercontent.com/107069287/196250931-e97a2501-8a4e-4ef9-8394-0d080a842eb5.png)

Escolha o modelo D2s_v3 e em seguida clique em Resize: 

![image](https://user-images.githubusercontent.com/107069287/196251207-a48df183-cfbe-40da-a330-aedf8195cc08.png)

Aguarde até a conclusão do processo. 

*OBS: Esse processo causa indisponibilidade da VM por alguns instantes, caso utilize em ambiente de produção, programe um horário que não irá impactar na operação. O processo de resize não apaga configurações ou arquivos, ele apenas altera o tamanho da máquina.*

Feito essa etapa, pode deletar a VM02. 