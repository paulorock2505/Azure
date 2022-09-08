# AZ-104-LAB-MOD-01
Repositório do Laboratório do módulo 01 para o exame de certificação AZ-104. (Credits by TFTEC)

Lab-01: Gerenciar identidades do azure Activity Directory - Task 04

Adicionar uma conta convidada externa ao tenant e conceder permissão para criar recursos em toda a subscrição.

Dentro do Portal do Azure, vá em Azure Active Directory: 
![Task-04-photo-00](https://user-images.githubusercontent.com/107069287/187771054-f892144a-121e-48f0-b236-eae510c92819.png)

Vá até a aba Users: 
![Task-04-photo-01](https://user-images.githubusercontent.com/107069287/187771974-28e4e069-09bd-475d-b936-fcebb9db7ca3.png)

Em Users, clique em + New User e Depois Invite External Users: 
![Task-04-photo-02](https://user-images.githubusercontent.com/107069287/187772261-3a9090b2-1dad-4883-bc32-c5c863d4d314.png)

Nessa etapa, ao invés de criarmos diretamente uma conta, iremos convidar uma conta de email já existente: 

Preencha os campos com os dados do usuário a ser convidado: 
![Task-04-photo-03](https://user-images.githubusercontent.com/107069287/187773460-94da8eb3-e21e-4164-a0a9-f56f5c087fdb.png)

E na sequência clique em Invite: 
![Task-04-photo-04](https://user-images.githubusercontent.com/107069287/187773574-cc5326fe-ba72-40be-bd3d-df86ee9e0aef.png)

O usuário receberá o email de convite e precisará fazer o aceite, conforme a imagem: 
![Task-04-photo-05](https://user-images.githubusercontent.com/107069287/187774791-6a5eb86c-a2bd-43e2-84dd-4cadafe52bbb.png)
![image](https://user-images.githubusercontent.com/107069287/187774864-209522a3-12bb-4b0d-a22a-3a524937efbd.png)
![image](https://user-images.githubusercontent.com/107069287/187774987-565f2590-626a-45a2-81dc-947a7cac99e3.png)
![image](https://user-images.githubusercontent.com/107069287/187775084-218117ad-ef88-438f-be4b-1b9cc1654af0.png)
![image](https://user-images.githubusercontent.com/107069287/187775144-c3b4c394-11ce-4444-ace7-754f7181d17d.png)

Nessa etapa clique em aceitar conforme a instrução: 
![image](https://user-images.githubusercontent.com/107069287/187775222-091509f0-2a22-4725-8530-f5eaf84334de.png)

Pronto, você estará dentro da área de trabalho para convidados do tentant: 
![image](https://user-images.githubusercontent.com/107069287/187775382-798e62c2-6a10-44cb-ab79-4a748e967e7e.png)

Acesse o portal com a conta recém criada: 
OBS: Para acessar o portal o usuário precisará antes entrar pelo dominio da empresa para poder ter o acesso. 
![image](https://user-images.githubusercontent.com/107069287/187778041-f506d638-bdb6-4e7b-a590-f0199121366d.png)
![image](https://user-images.githubusercontent.com/107069287/187778094-f4dcc23b-db3e-4258-bbf6-da961bbdcdda.png)
![image](https://user-images.githubusercontent.com/107069287/187778160-9a71beb7-7aaf-432e-b100-a703423f104f.png)

Após essas etapas o acesso será liberado no portal Azure: 
![image](https://user-images.githubusercontent.com/107069287/187778784-dd9c5e7e-7526-48d3-a534-0c01b1f3732a.png)

Após essa etapa iremos dar a permissão pelo RBAC a subscription: 

Na conta princpal, vá em Subscription: 
![image](https://user-images.githubusercontent.com/107069287/187779332-99aeaafb-f1c5-484e-9c12-a65f239eb40b.png)

Clique na assinatura do Azure Vigente: 
![image](https://user-images.githubusercontent.com/107069287/187779402-e38893d2-2680-4568-986c-8880637fc8e3.png)

E vá Access Control (IAM): 
![image](https://user-images.githubusercontent.com/107069287/187779540-fa35b788-57a4-4d35-996f-a611160c622d.png)

Vá em Grant Access to this resource e clique em Add role Assignment: 
![image](https://user-images.githubusercontent.com/107069287/187780101-f3893ee9-5a21-4e1f-90dd-6d43ddc74f3b.png)

Nesse exemplo, criaremos uma Role que o usuário poderá criar, excluir e gerenciar recursos nessa assinatura. O grupo mais indicado nesse caso é o Contributor: 
![image](https://user-images.githubusercontent.com/107069287/187780307-528c519c-baad-4d1e-9b92-ad9f71b446b7.png)

Associaremos o usuário que convidamos: 

- Clique em + select members e na sequência associe ao usuário desejado: 
![image](https://user-images.githubusercontent.com/107069287/187780539-7f79f40d-75fc-4f6d-8e43-e1c0466ccf1d.png)
![image](https://user-images.githubusercontent.com/107069287/187780572-d81693b5-7b2c-4e8c-aa50-ff00b5775129.png)
![image](https://user-images.githubusercontent.com/107069287/187780611-00f12dd7-1d8d-425b-ac10-025985f3a2ef.png)

Após concluido essa etapa clique em next e após o processo revise as configurações e clique em Review + assign. 

Checaremos as permissões concedidas ao usuário. 

Crie um resource group e valide os testes finais. 











