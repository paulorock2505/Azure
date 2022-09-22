# AZ-104-LAB-MOD-05

 <h2>Lab 05a - Configuração de VPN</h2> <br>

 ***Tarefa 3:***  <br>
    *Realizar deploy de uma VM na VNET East US e Brazil South.*

No portal do Azure, no campo de pesquisa, digite Virtual Machines:

![image](https://user-images.githubusercontent.com/107069287/191563113-c7b4c379-4653-47e6-bdbd-ec7eeb1e0bb4.png)

Clique em + Create e em seguida Azure Virtual Machine: 

![image](https://user-images.githubusercontent.com/107069287/191563288-e06cdc00-37be-4c5b-a89e-ba308023a140.png)

Configure a máquina conforme o padrão abaixo: 

![image](https://user-images.githubusercontent.com/107069287/191564256-d7efa8df-69d2-420c-8c0d-286184f162d8.png)

![image](https://user-images.githubusercontent.com/107069287/191564383-426d52eb-a945-49d6-9051-8a3db2048184.png)

*OBS: Caso não apareça o tamanho de máquina b2s como demonstrado, clique em see all sizes e na lista vigente irá aparecer ela: 

![image](https://user-images.githubusercontent.com/107069287/191564692-8da8202b-471e-4a1e-b352-c0fe9942208b.png)

Em authentication type, digite um usuário e senha de sua preferência: 

![image](https://user-images.githubusercontent.com/107069287/191565035-8aef9c05-0643-4c72-8f3d-6ff85c38bcf0.png)

Pode manter a porta ssh selecionado e clique em Next. 

Em discos, pode manter o disco premium mesmo como sugerido: 

![image](https://user-images.githubusercontent.com/107069287/191585614-22568b8e-a0ef-4973-ab80-4a3287a81900.png)

Clique em Next. 

Em Networking valide se as configurações foram determinadas como a imagem abaixo: 
*OBS: Note que a GatewaySubnet não está disponível para uso. Ela fica desta maneira pois a microsoft exige que não tenha nenhum dispositivo conectado a ela. É para o uso exclusivo do Gateway de Subnet.*

![image](https://user-images.githubusercontent.com/107069287/191586170-7992c06d-56ce-4c76-8437-371704313eb8.png)

Clique em Next. 

Em management, não altere nenhuma informação e em seguida clique em Next. 

![image](https://user-images.githubusercontent.com/107069287/191586697-790c94c9-fc1c-4476-922e-795072752803.png)

Em monitoring, desabilite o boot diagnostics: 

![image](https://user-images.githubusercontent.com/107069287/191586798-9fe5e828-ac89-4d08-a04a-f1d7b467be10.png)

Não altere nada em Advanced e clique em Next. 

![image](https://user-images.githubusercontent.com/107069287/191586923-f529e07a-ad9d-4ce7-96f0-b4da5450af23.png)

Em Tags, coloque para mantermos o hábito, coloque os valores conforme a imagem abaixo: 

![image](https://user-images.githubusercontent.com/107069287/191587149-a8109fa5-6d89-4cbd-b8e0-fe548a74d375.png)

Clique em Review + Create e em seguida Create. 

Após a conclusão desta etapa, vamos criar a segunda máquina. 

No portal do Azure, pesquise novamente por Virtual Machine: 

![image](https://user-images.githubusercontent.com/107069287/191588024-2c045ab0-25de-4819-bc4b-f1852b5ed8b3.png)

Em seguida clique em + Create e em seguida Azure Virtual Machine: 

![image](https://user-images.githubusercontent.com/107069287/191588160-62076dee-5541-4257-a7ab-09bebd175be3.png)

Nesta etapa iremos criar uma máquina Windows para seguirmos com os testes, iremos usar o mesmo Grupo de Recursos, só que em outra região. Utilize o padrão conforme a imagem abaixo: <br>
*Atenção: A região que iremos alocar a máquina é Brazil South* 

![image](https://user-images.githubusercontent.com/107069287/191588873-2fcbadea-e00d-4299-85f3-c9b41ac7c356.png)

Em usuário e senha utilize o padrão que preferir: 

![image](https://user-images.githubusercontent.com/107069287/191589055-7835e04a-8d29-4e1a-be77-afb744989438.png)

Pode manter a porta 3389 habilitada e em seguida clicar em Next: 

![image](https://user-images.githubusercontent.com/107069287/191589198-850a0c31-e907-4cd0-bc5f-4a1a29d44f67.png)

Em disks, mantemos o padrão sugerido: 

![image](https://user-images.githubusercontent.com/107069287/191589424-81a19d8b-1ccb-4d5e-ba46-654a4282473d.png)

Em seguida clicamos em Next. 

Na opção Networking, altere a subnet para SUB-Webservers: 

![image](https://user-images.githubusercontent.com/107069287/191589689-7d7c5786-f985-4d76-8234-89aca62d28fa.png)

Clique em Next. 

Em management, não fazemos nenhuma alteração: 

![image](https://user-images.githubusercontent.com/107069287/191589921-91640c62-1a1d-4483-bb1e-7c5b2bf5ea00.png)

Clique em Next. 

Em monitoring, desabilite o boot diagnostics: 

![image](https://user-images.githubusercontent.com/107069287/191590045-cc177bc3-2fa7-44cb-b071-26b0a4873a10.png)

Clique em Next. 

Em Advanced, não faremos nenhuma alteração: 

![image](https://user-images.githubusercontent.com/107069287/191590124-0119565c-6c0c-4cdc-a25b-f6d63664a6f4.png)

Clique em Next. 

Em TAGS, utilizaremos os valores conforme a imagem abaixo: 

![image](https://user-images.githubusercontent.com/107069287/191590338-f46ce0d4-32db-4f15-9506-17bcf961bab2.png)

Clique em Review + Create e em seguida Create. 

Aguarde até o término do processo de criação da VM. 

Ao término clique em go to Resource. 

Em Overview, clique em Connect e em seguida RDP para fazermos o acesso remoto a máquina: 

![image](https://user-images.githubusercontent.com/107069287/191591375-ab44e0ca-7b2e-4058-ba55-7fb2a73aec27.png)

Em seguida clique em Download RDP File e faça o download do client RDP. 

![image](https://user-images.githubusercontent.com/107069287/191591543-24b16d07-6918-4c4e-abe1-9e4463c46b38.png)

Conecte a máquina: 

![image](https://user-images.githubusercontent.com/107069287/191594187-582abe6f-0b7a-47e6-90cf-d58645cf1dba.png)

![image](https://user-images.githubusercontent.com/107069287/191594298-a31fc51f-bac7-44ce-bec8-799256d30bd1.png)

![image](https://user-images.githubusercontent.com/107069287/191594364-9ee5bc74-577e-4935-b43b-0661459722e9.png)

![image](https://user-images.githubusercontent.com/107069287/191594553-f7515e41-8b13-41bf-82d0-ced49eb355de.png)

Na sequência desabilite o firewall do Windows para realizarmos os seguintes testes: 
- Ping para o ip da VM Linux que criamos; 
- Acesso SSH através do PowerShell na Máquina Linux; 
- Ping da VM Linux para a VM Windows; 

Comando para ssh no power shell: 

```
ssh 'usuario'@ip_da_máquina 
```
Em seguida digite sua senha e se conecte a VM Linux. 

Feito os testes acima, o pering está estabelecido entre as rede, validado e funcionando conforme a atividade. 

*OBS: Lembre de dar um stop nas máquinas caso não faça os demais laboratórios na sequência.*
