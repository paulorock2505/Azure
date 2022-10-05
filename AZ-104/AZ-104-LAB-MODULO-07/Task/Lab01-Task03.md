# AZ-104-LAB-MOD-07

 <h2>Lab 07 - Manage Azure Storage</h2> <br>

 ***Tarefa 3:***  
    *Gerenciar autenticação e autorização para Azure Storage*

Acesse o portal, no campo de pesquisa digite Storage Account: 

![image](https://user-images.githubusercontent.com/107069287/194133897-a2e5ac43-b2c3-43e2-93e6-ebe703aee1f4.png)

Em seguida clique no blob que acabamos de criar: 

![image](https://user-images.githubusercontent.com/107069287/194134001-7ce22241-692a-430c-93bf-7d745c75f4b2.png)

Vá até a opção Data Storage e acesse o blob que criamoz, blobaz: 

![image](https://user-images.githubusercontent.com/107069287/194134300-58aaa864-6507-4f97-a5a9-fa8ff7d86c6b.png)

Em Change Access Level, altere para o modo Private: 

![image](https://user-images.githubusercontent.com/107069287/194134514-3b8ad7f8-20fc-4165-b32a-4cc6ef922508.png)

Em seguida clique em Ok. 

Acesse a Overview do arquivo e copie novamente o endereço da URL. Note que ao acessar, teremos o erro novamente para acessar o arquivo: 

![image](https://user-images.githubusercontent.com/107069287/194134859-5b07d600-6b9a-42c0-ab91-1d4703e9cb52.png)

Volte ao portal, vá até a opção Shared Acess Token: 

![image](https://user-images.githubusercontent.com/107069287/194135497-bd6460b4-c393-48e5-990f-8115699def66.png)

Nessa etapa iremos gerar um Token SAS.<br>
***Importante: Para testarmos a revogação do token SAS, coloque um tempo para expiração de 5 minutos para testarmos:***

![image](https://user-images.githubusercontent.com/107069287/194136076-be9ddf7e-6606-4746-b3bc-cce0bb33ecbd.png)

Clique em Generate SAS token and URL: 

![image](https://user-images.githubusercontent.com/107069287/194136128-1ee48bc5-b860-42e9-8604-741f5d238db9.png)

Copie o Blob SAS URL e cole no navegador: 

![image](https://user-images.githubusercontent.com/107069287/194136305-49c28f1a-08e1-4f2b-9ccf-b33b78cbc834.png)

Note que mesmo assim o acesso ainda não está autorizado. Esse se deu porque as permissões que colocamos foi no blob como um todo. Dessa forma, a única maneira de acessarmos é através de um programa que gerencia os arquivos. No entanto, podemos mmontar a nossa URL conforme a maneira abaixo: 

![image](https://user-images.githubusercontent.com/107069287/194137614-5408ccaa-0cef-4e38-8436-51250a5c5352.png)

Feito dessa maneira que expomos, o resultado será o acesso a imagem que está no blob: 

![image](https://user-images.githubusercontent.com/107069287/194137767-9fd4ce5a-40f9-4080-9253-4d470037ed77.png)

Na sequência, iremos dar o permissionamento para o usuário gerenciar o blob através do Azure Active Directory. 

Dentro do blobaz, vá em Overview e clique em Switch to Azure Active Directory: 

 ![image](https://user-images.githubusercontent.com/107069287/194139427-2d7fe57e-44c5-4b69-9a7f-19880ee7662c.png)

Note que você não tem permissão para realizar essa função. 

Vá até Access Control IAM: 

![image](https://user-images.githubusercontent.com/107069287/194139598-25cb695e-cd50-4037-8341-a86fa2388d6f.png)

Em Grant Access to this resource clique Add role assignment: 

![image](https://user-images.githubusercontent.com/107069287/194139768-610c70ea-6c23-4dad-8504-775b82a5abab.png)

Escolha a rule Storage Blob Data Owner: 

![image](https://user-images.githubusercontent.com/107069287/194140182-b177bf68-e981-4e89-8491-cee81e4b29f7.png)

Clique em Next. 

Clique em + Select Member: 

![image](https://user-images.githubusercontent.com/107069287/194140302-c7f9d304-bcc0-428b-99bc-3366c5d881cf.png)

Escolha o usuário que você quer dar permissão, no meu caso escolhi o meu prório usuário: 

![image](https://user-images.githubusercontent.com/107069287/194140481-4c9586cf-25fa-47a9-8761-9a0332840671.png)

Clique em select. 

Em seguida clique em Next. 

Logo após clique em Review + Create e em seguida create. 

Terminado essa etapa, aguarde uns 5 minutos e teste novamente o acesso em Overview ao Switch to Azure Active Directory. 

Note que agora não apresentou nehnum tipo de erro. Essa função é interessante pois agora você poderá dar autorização ao blob tanto em nível de AD quanto através do token SAS. 

Finalizado esta etapa, a tarefa foi concluída com sucesso. 

