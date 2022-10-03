# AZ-104-LAB-MOD-05

 <h2>Lab 06b - Configuração de VPN</h2> <br>

 ***Tarefa 2:***  
    *Implementar Azure Application Gateway.*

<table border="1">    
  <tr>
    <th colspan="1">Application Gateway Subnet</th> 
</table>

<table border="1">    
  <tr>
    <th colspan="1">Setting</th>  	              
    <th colspan="2">Value</th>
  </tr>
<td>Name</td>
    <td>SUB-APPGW</td>
  </tr>
  <tr>
    <td>Address Range (CIDR)</td>
    <td>10.10.2.0/27</td>
  </tr>
  <td>Vnet</td>
    <td>VNET-AZ104 (10.10.0.0/22)</td>
  </tr>
 </table>

 Nessa primeira etapa iremos adicionar a Subnet para o Application Gateway. 

 Vá até o portal e no campo de pesquisa digite Virtual Network: 

 ![image](https://user-images.githubusercontent.com/107069287/193648813-0ef24a40-5a8d-45a2-849f-1454e6ce4f30.png)

 Em seguida acesse a VNET-AZ104-06: 

 ![image](https://user-images.githubusercontent.com/107069287/193648984-977a909e-f9a1-4967-9638-1a5cbf32c220.png)

 Vá até a opções Settings e em seguiga clique em Subnets: 

 ![image](https://user-images.githubusercontent.com/107069287/193649107-69eead4a-58e2-4148-941f-741b6c8cd32c.png)

 Clique em + Subnet:

 ![image](https://user-images.githubusercontent.com/107069287/193649443-e9a5c540-38c1-453e-a098-b1666d03f736.png)

 Digite os parâmetros como conforme a imagem abaixo: 

 ![image](https://user-images.githubusercontent.com/107069287/193649595-da162285-c575-48fb-b06f-60baf5ae9331.png)

 Em seguida clique em Save. 

 Criado a Subnet, vá até a home novamente e no campo de pesquisa digite Application Gateway: 

 ![image](https://user-images.githubusercontent.com/107069287/193650063-9476a386-f553-450a-a3bf-ec3c2d061c76.png)

 Clique em + Create: 

 ![image](https://user-images.githubusercontent.com/107069287/193650182-1f614abd-dc2d-4bfd-a972-f592244b8993.png)

 Em Basics, configure os parâmetros conforme a imagem abaixo: 

 ![image](https://user-images.githubusercontent.com/107069287/193651000-01468508-3b0e-4bfb-adaf-bc226c09d696.png)

 ![image](https://user-images.githubusercontent.com/107069287/193651084-c10ed834-6df7-4b72-af12-67fb1561232c.png)

 *OBS: Caso a subnet não apareça automaticamente, selecione a subnet que criamos o SUB-APPGW.* 

 Em seguida clique em Next. 

 Em Frontends, em Public IP Address, clique em Add New: 

 ![image](https://user-images.githubusercontent.com/107069287/193651791-c5509aa9-fa15-47e9-a56b-4cdc74b384a5.png)

 Configure o IP Público conforme o parâmetro abaixo: 

 ![image](https://user-images.githubusercontent.com/107069287/193651938-bbec7f31-b949-428f-b666-a7ab4e9542e7.png)

 Em seguida clique em Ok. 

Clique em Next. 

Em Backends, iremos criar dois backends pool. Clique em Add a backend pool: 

![image](https://user-images.githubusercontent.com/107069287/193659114-7f87fcbd-5477-45db-ac65-cfd8c7194117.png)

Configure o  primeiro Pool conforme os parâmetros abaixo: 

![image](https://user-images.githubusercontent.com/107069287/193659747-a5b25f5e-35be-43a9-9eb5-44221995160a.png)

Clique em Add.

Em seguida configuraremos o próximo pool. Faça as configurações conforme a imagem: 

![image](https://user-images.githubusercontent.com/107069287/193660048-9ddd4ec6-c88e-4202-890d-eda1c827e71f.png)

Clique em Add. 

Clique em Next. 

Em seguida clique em + Add a Routing Rule: 

![image](https://user-images.githubusercontent.com/107069287/193661148-ed8cc493-848b-4566-a4da-9158126e29ea.png)

Configure o Listener e o Backend Target conforme as imagens abaixo: 

![image](https://user-images.githubusercontent.com/107069287/193661859-d809b379-c831-4700-97e0-afb3d7d62ea4.png)

![image](https://user-images.githubusercontent.com/107069287/193662211-75f2bea4-d236-49dd-a2b1-08e55a96c62d.png)

No entanto, ainda não temos o nosso HTTP Settings configurado, clique em Add new: 

![image](https://user-images.githubusercontent.com/107069287/193662343-9ea86521-a3d8-42d3-af1e-663957f86ddc.png)

Configure conforme a imagem abaixo: 

![image](https://user-images.githubusercontent.com/107069287/193663140-07e6d2c8-3aaa-4e4c-ab3f-b8d3b38ed82a.png)

Clique em Add. 

Novamente clique em Add: 

![image](https://user-images.githubusercontent.com/107069287/193663489-1f39ec23-1d6e-4127-9d0f-c3676297399a.png)

Agora iremos criar a regra para o segundo Pool. Clique novamente em + Add a routing rule: 

![image](https://user-images.githubusercontent.com/107069287/193663820-457e1090-24ee-4513-9565-d72426702503.png)

Configure o Listener e o Backend Target conforme as imagens abaixo: 

![image](https://user-images.githubusercontent.com/107069287/193664170-b6ee3227-a7f0-48ae-af7a-836a401811d1.png)

![image](https://user-images.githubusercontent.com/107069287/193664271-fbbba55b-4c55-4eca-bd1f-e2ed8f8673ed.png)

No entanto, ainda não temos o nosso HTTP Settings configurado, clique em Add new: 

![image](https://user-images.githubusercontent.com/107069287/193664384-1fba9491-cd4f-41cb-8b03-b6a3290a0947.png)

 ![image](https://user-images.githubusercontent.com/107069287/193664537-d05bc328-199a-4a55-a378-fdb1426526bf.png)

Clique em Add. 

Clique em Add novamente para adicionarmos a regra: 

![image](https://user-images.githubusercontent.com/107069287/193664651-f7b6712d-cfbb-4a2d-8086-fa3aa535e0c2.png)

Clique em Next. 

Na parte de TAGs, configure conforme o escopo abaixo: 

![image](https://user-images.githubusercontent.com/107069287/193664969-1a69e799-9e2d-4fb6-a1e6-b8b5393ed1ca.png)

Em seguida clique em Review + Create e depois Create. 

Enquanto o recurso está sendo criado, vá até a home, no campo de pesquisa digite Virtual Machine: 

![image](https://user-images.githubusercontent.com/107069287/193665967-f80eb699-74f7-447c-8464-10141437f0b3.png)

Em seguida clique em VM-01: 

![image](https://user-images.githubusercontent.com/107069287/193666067-35ecb772-001c-4d91-b3f5-e6df87136ef0.png)

Em Operations, clique em Run Command: 

![image](https://user-images.githubusercontent.com/107069287/193666182-e542d4d1-fade-410b-b3f7-360f1bf378bc.png)

Clique em RunPowerShellScript: 

![image](https://user-images.githubusercontent.com/107069287/193666281-dac92654-01af-4e87-b287-6c8fdf334cc5.png)

E aplique o código abaixo: 

![image](https://user-images.githubusercontent.com/107069287/193666420-af2ab1b7-2aba-4b36-b1b9-1cb897d8c355.png)

![image](https://user-images.githubusercontent.com/107069287/193667317-24146074-8988-4d81-9ff9-5c9d2f9decd5.png)

Clique em Run. 

Aguarde até o término do processamento do código. 

![image](https://user-images.githubusercontent.com/107069287/193667550-833a6823-7034-4bfa-8b14-f873b27ce16b.png)

Faça o mesmo procesdimento para a máquina VM-02, altere apenas o domínio no script para www.alpars.com.br: 

![image](https://user-images.githubusercontent.com/107069287/193668064-041c249f-1806-4f31-aaab-0976ff1ce99f.png)

Feito esta etapa, precisamos agora fazer a alteração na própria máquina que estamos utilizando para que os domínios simulados possa ser reconhecidos para concluirmos o laboratório. 

Vá até a home do Azure, digite no campo de pesquisa Application Gateway: 

![image](https://user-images.githubusercontent.com/107069287/193669156-1eb79872-a817-49e9-ad4e-357f1ff5447c.png)

Em seguida copie o endereço público que aparece na tela: 

![image](https://user-images.githubusercontent.com/107069287/193669275-550a2cad-f250-4a01-9a87-b2dedcd519d4.png)

Copie esse endereço em um bloco de notas para utilizarmos posteriormente. 

Em sua máquina naveggue até o diretório etc para alterarmos o arquivo hosts: 

C:\Windows\System32\drivers\etc

Configure o arquivo host conforme a imagem abaixo: 

![image](https://user-images.githubusercontent.com/107069287/193670871-1326adbe-d450-4338-a337-ad478571a1d7.png)

Salve o arquivo para darmos sequência nos testes. 

*OBS: Caso não consiga salvar, acesse o bloco de notas como administrador e abra o arquivo*

Feito esta etapa o Laboratório foi concluido com sucesso. 

***Tarefa opcional:***<br>
*- Abra o navegador e acesse os dois sites que acabamos de criar. (ambos os sites precisam responder e veja os resultados)*

Ao término deste laboratório pode remover todos os recursos que criamos. 

