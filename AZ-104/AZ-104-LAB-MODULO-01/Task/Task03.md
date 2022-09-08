# AZ-104-LAB-MOD-01
Repositório do Laboratório do módulo 01 para o exame de certificação AZ-104. (Credits by TFTEC)

<h3>Lab-01: Gerenciar identidades do azure Activity Directory - Task 03</h3>
<table border="1">    
   <tr>
    <td>Settings</td>
    <td>Value</td>
  </tr>
  <tr>
    <td>Directory Type</td>
    <td>Azure Active Directory</td>
  </tr>
 <tr>
    <td>Organization Name Name</td>
    <td>ALPA Lab</td>
  </tr>
 <tr>
    <td>Initial domain name</td>
    <td>alpalab01</td>
  </tr>
 <tr>
    <td>Country Region</td>
    <td>United States</td>
  </tr>
</table>

Primeiro passo para criar um novo tenant: 

Vá em Create Reource

![Task-03-photo-00](https://user-images.githubusercontent.com/107069287/187738335-a859e6d9-b326-4f7b-baaf-d1631c7df241.png)

Em seguida busque pelo recurso Azure Active Directory: 
![Task-03-photo-01](https://user-images.githubusercontent.com/107069287/187738822-fd1c63ba-b0f6-4513-b6ca-556a9e56c0ca.png)

Em seguida clicaremos em create: 
![Task-03-photo-02](https://user-images.githubusercontent.com/107069287/187738941-22d0a6da-668e-48f5-995f-851773ce44f3.png)

Ao clicarmos em create escolheremos a opção Azure Active Directory e clicaremos em Next: 
![Task-03-photo-03](https://user-images.githubusercontent.com/107069287/187739493-1090255e-ee58-4496-99c2-414afa4bc716.png)

Configuraremos o Display name e o Organization Name conforme a imgem abaixo e em seguinda clicamos em Next: 
![Task-03-photo-04](https://user-images.githubusercontent.com/107069287/187740220-c87f5879-490a-4a85-8ce6-22ed20e11023.png)


Revise os parâmetros configurados e clique em create: 
![Task-03-photo-05](https://user-images.githubusercontent.com/107069287/187740248-c863f210-be97-49d8-b45e-3ec9e4ccc62b.png)

Aguarde até que o processo seja finalizado. 

Após a criação do novo tenant, para fazer acesso a nova subsctiption recém criada, no menu suspenso, no segundo ícone a direita clique neste botão conforme a imagem: 
![Task-03-photo-06](https://user-images.githubusercontent.com/107069287/187741587-8c00ea3b-c5e2-4923-987a-699ec3205a12.png)

Faça um switch no tenant recém criado para fazer o acesso ao novo tenant: 
![Task-03-photo-07](https://user-images.githubusercontent.com/107069287/187742308-5a5c665f-d263-4e0a-8b7b-39e3618954fc.png)
![Task-03-photo-08](https://user-images.githubusercontent.com/107069287/187742310-7b149854-753e-4c39-960a-5227f90a9471.png)

Lembrando, quando criamos o tenant, não temos a portabilidade de usuários. Apenas o usuário que criou o tenant tem acesso e permissão para fazer criação de recursos ou acesso a infraestrutura. 

Caso eu queira migrar todos os recursos da subsctription principal: 

Faça novamente um switch para a conta principal: 
![Task-03-photo-09](https://user-images.githubusercontent.com/107069287/187743602-263c1f01-e6a9-4eb1-8501-ab5278ddcf6b.png)

Em seguida vá em subscription: 
![Task-03-photo-10](https://user-images.githubusercontent.com/107069287/187743784-4c6a217c-d5f0-4eec-9189-3509c79894bc.png)

Clique na sua subcription: 
![Task-03-photo-11](https://user-images.githubusercontent.com/107069287/187744118-6549a73b-36c7-4261-af49-dd59695cd4c6.png)

Clique na opção change directory: 
![Task-03-photo-12](https://user-images.githubusercontent.com/107069287/187744268-ec86e85d-9633-46e1-b23d-174f52a684e3.png)

E em seguida abrirá uma janela no lado esquerdo na qual ele mostrará para qual Subscription você gostaria de mover: 
![Task-03-photo-13](https://user-images.githubusercontent.com/107069287/187744575-7ffa3c4f-e344-4520-80f0-34ba7216f2f2.png)

Você escolherá qual a subscription irá mover, marcará a opção I understand that changing directory does not transfer some resources, for example, all Azure role-based access control assignments are deleted (See affected users) and system/user assigned managed identities are invalidated and not transferred to target directory. Learn more e em seguida clicará em Change. 

![Task-03-photo-14](https://user-images.githubusercontent.com/107069287/187744870-1138f194-61a4-4d9c-ae3d-d755a1160222.png)

Adicionando um domínio personalizado: 

Vá novamente até o Azure Active Directory: 
![Task-03-photo-15](https://user-images.githubusercontent.com/107069287/187765994-6e523d5b-978d-4e79-9d3c-9500f0caff16.png)

Selecione a opção custom domain: 
![Task-03-photo-16](https://user-images.githubusercontent.com/107069287/187766188-190c1ef7-f23f-4bc4-93e1-92e598cb756d.png)

Clique em Add Custom Domain: 
![Task-03-photo-17](https://user-images.githubusercontent.com/107069287/187766558-fc53168a-6a3b-4e5c-b20e-2260ad4e9745.png)

E adicione o seu domínio personalizado (Ex: www.meudominio.com.br): 
![image](https://user-images.githubusercontent.com/107069287/187766703-70a441e1-90be-434e-9430-2e743d012bf5.png)

Feito essa etapa, será necessário validar o domínio para a microsoft identificar que o domínio configurado pertence ao dono da subscription. Após essa etapa será importante você configurar os dados no seu provedor de hospedagem (Registro.br, locaweb, uol, godaddy, etc):
OBS: Para esse processo a microsoft só permite registros do tipo TXT ou MX: 
![Task-03-photo-18](https://user-images.githubusercontent.com/107069287/187767272-c7a870b9-a201-4a79-80c9-4ac7b6c7f41f.png)
![Task-03-photo-19](https://user-images.githubusercontent.com/107069287/187767383-73c2cc40-7af9-4b5f-9d35-43c7e6c72334.png)

Após essa etapa é só clicar em verify e aguardar a verificação da microsoft. 













