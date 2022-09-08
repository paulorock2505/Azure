# AZ-104-LAB-MOD-02
Repositório do Laboratório do módulo 01 para o exame de certificação AZ-104. (Credits by TFTEC)

<h3>Lab 01 - Gerenciar identidades do Azure Active Directory</h3>

Task 03 - Associar RBAC Roles 

<table border="1">    
  <tr>
    <th colspan="1">Usuário 03</th> 
</table>

<table border="1">    
  <tr>
    <th colspan="1">Setting</th>  	              
    <th colspan="2">Value</th>
  </tr>
<td>User Name</td>
    <td>alpa03</td>
  </tr>
  <tr>
    <td>Name</td>
    <td>alpa03</td>
  </tr>
  <td>Let me create password</td>
    <td>enable</td>
  </tr>
  <tr>
    <td>Initial password</td>
    <td>123@Mudar</td>
  </tr>
  <td>Usage Location</td>
    <td>United States</td>
  </tr>
  </table>
  
  
Criação do usuário: 

No portal do Azure pesquise por Azure Active Directory: 

![image](https://user-images.githubusercontent.com/107069287/188213488-d8827fa3-8516-4909-a66b-faf2cd239e8f.png)

Clique em Users: 

![image](https://user-images.githubusercontent.com/107069287/188213600-8f5539fe-d264-4da1-beca-e77f06215d87.png)

E vamos clicar em + New User e em seguda Create a New User: 

![image](https://user-images.githubusercontent.com/107069287/188213745-975eb862-5f72-4c3e-b05f-7ecf30b2faac.png)

Criaremos o usuário conforme o parametro mencionado na tabela acima: 

![image](https://user-images.githubusercontent.com/107069287/188214405-2c23813c-2298-4e5e-a5a5-366af2680169.png)

![image](https://user-images.githubusercontent.com/107069287/188214453-f56fbf3f-b835-4ee6-aeca-9a17698ad103.png)

Após essa etapa, clique em create. 

![image](https://user-images.githubusercontent.com/107069287/188214550-8ac2636d-4a58-4d3a-aeed-c4733af5082f.png)

Na sequência iremos fazer um teste de autenticação para este usuário. 

Abra uma janela anônima do navegador e abra o portal do Azure: 

![image](https://user-images.githubusercontent.com/107069287/188214942-9f4a4a02-c24a-4c0f-941e-e3660d181d00.png)

Insira o nome completo do usuário que acabamos de criar: *OBS: Copie o User Principal por completo* 

Nesse exempo usamos o alpa03@paulocloud02092022outlookco.onmicrosoft.com

![image](https://user-images.githubusercontent.com/107069287/188215217-846d33d5-5488-4cd0-a347-0213f88d5115.png)

Insira a senha: 

![image](https://user-images.githubusercontent.com/107069287/188215266-0acc1b89-0e69-4b99-9d59-43f7602d1a1c.png)7

Redefina a senha por uma de sua confiança: 

![image](https://user-images.githubusercontent.com/107069287/188215361-dea78724-4b0d-40ec-ac70-f01c25630789.png)

E em seguida clique em entrar. 

Note que apenas criamos o usuário, este usário não tem nenhum tipo de permissão. 

Na sequência iremos associar esse usuário ao RBAC que acabamos de criar: 

No portal, vá até Management Group: 

![image](https://user-images.githubusercontent.com/107069287/188215937-8abc6ddb-7323-457a-a9fe-0521a0e0b50c.png)

Em Management Groups, clique no Managemente Group que criamos AZ104-mg1: 

Clique em Access Control (IAM): 

![image](https://user-images.githubusercontent.com/107069287/188216378-89748c35-3d4f-4b9c-a1d5-2f7042e7c25b.png)

Em Grant Access to this resource, vá até add role assigment: 

![image](https://user-images.githubusercontent.com/107069287/188216697-b2812b93-e6a6-443e-90a0-0c53e16e80d0.png)

Busque pela role que criamos: 

![image](https://user-images.githubusercontent.com/107069287/188216788-5b0a4214-0f77-4572-a6e0-bd0a9b45423c.png)

Clique em Next. 

Em members clique +select members e na sequência busque o usuário que crlamos alpa03: 

![image](https://user-images.githubusercontent.com/107069287/188217027-f2afcef9-fd6c-4f8e-9ecc-83cde8b0bd38.png)

Selecione ele e clique em select. 

Clique em Review + create. 

Verifique em Access Control (IAM) no AZ104-mg1 se a RBAC foi aplicada no campo Role Assignements. 

![image](https://user-images.githubusercontent.com/107069287/188217600-f3a77688-8bc0-40a9-8f32-c8ca001f2285.png)

Após essa etapa, verifique se o usuário já estou permissão: 

![image](https://user-images.githubusercontent.com/107069287/188217691-7fe3550d-8ab0-496c-80ac-7279e1117b0b.png)

Na conta criada, iremos abrir uma seção de suporte. 

Na guia anonima com a conta recém criada aberta, clique em ? na parte superior da janela: 

![image](https://user-images.githubusercontent.com/107069287/188218561-66f41b34-5274-477e-9e22-5cb8ccfc295f.png)

Na sequência clique em ajuda + suporte: 

![image](https://user-images.githubusercontent.com/107069287/188218655-ec004115-dfc7-4ba0-9082-f97d656eb4c8.png)

Clique em crie uma solicitação de suporte: 

![image](https://user-images.githubusercontent.com/107069287/188218767-77785848-70d1-4c95-82bc-11eb1815795d.png)

Para este exemplo iremos abrir uma solicitação pedindo aumento no limite de serviço e assinatura: 

![image](https://user-images.githubusercontent.com/107069287/188218886-2d1ffcf0-9e42-42e2-a0f7-7235af9ee324.png)

Clique na opção desejada, para esse exmplo marquei a opção outras solicitações: 

![image](https://user-images.githubusercontent.com/107069287/188219121-509fa5b5-0533-4e7a-8e66-bd99d2eb99ca.png)

Preencha os dados abaixo e escolha o tipo de suporte que você quer receber (telefone ou email). 

![image](https://user-images.githubusercontent.com/107069287/188219266-85988184-a700-4bd2-b912-679070ffd41b.png)

![image](https://user-images.githubusercontent.com/107069287/188219311-d340d622-c5f2-431c-b028-0151c188d851.png)

![image](https://user-images.githubusercontent.com/107069287/188219342-d0e058f1-ba28-457b-91bf-9402990ea2b4.png)











