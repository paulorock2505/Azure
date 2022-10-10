# AZ-104-LAB-MOD-07

 <h2>Lab 07 - Manage Azure Storage</h2> <br>

 ***Tarefa 4:***  
    *Crie e configure um Azure Files Shares*

No portal do Azure, no campo de pesquisa, digite Storage Accounts: 

![image](https://user-images.githubusercontent.com/107069287/194878604-39e9977f-c9a5-48fa-be1d-1629b9eccd3b.png)

Em storage Accounts, clique no storage que criamos conforme a atividade anterior: 

![image](https://user-images.githubusercontent.com/107069287/194878716-390c20b2-b198-4c4b-a7dd-dae5e1562b9d.png)

Em seguida no campo Data Storage, clique em File Shares: 

![image](https://user-images.githubusercontent.com/107069287/194880324-3c2f3609-e78d-40a5-842a-9c2566d27509.png)

Em seguida clique em + File Share: 

![image](https://user-images.githubusercontent.com/107069287/194880480-9ff9c2af-8458-435b-a416-fe75e78c6d07.png)

Crie o file share conforme a imagem abaixo: 

![image](https://user-images.githubusercontent.com/107069287/194882119-4bf9206d-ff0f-4f3c-af55-d5f12f5cc859.png)

Em seguida clique em Create. 

Na sequência acesse o File Share que acabamos de criar: 

![image](https://user-images.githubusercontent.com/107069287/194882456-d1cfae6a-277a-42e7-b6de-65c2c73a6b36.png)

Em Overview, clique em edit quota: 

![image](https://user-images.githubusercontent.com/107069287/194882570-483733df-1ad5-45ce-9533-7fd65cefe99f.png)

Em seguida altere para 1 GB: 

![image](https://user-images.githubusercontent.com/107069287/194882706-d0edfea3-93fe-412f-b3e1-52f66e420785.png)

Em seguida clique em Ok. 

Para esta atividade iremos criar uma estrutura de pastas para simularmos um ambiente convencional. 

Em Overview, clique em Upload: 

![image](https://user-images.githubusercontent.com/107069287/194887633-f4ebae29-1416-449d-b2e2-a205e75e36c2.png)

Em seguida, clique no ícone com uma pasta, no canto direito e em seguida faça um upload de um arquivo de imagem qualquer para o ambiente: 

![image](https://user-images.githubusercontent.com/107069287/194888117-e453eaac-5172-4422-8cd5-c78e4f1b9f2f.png)

Em seguida clique em upload. 

![image](https://user-images.githubusercontent.com/107069287/194888253-bc6415cb-5113-45cd-b69f-2b5e4d6eeab2.png)

Em seguida clique em + Add Directory e adicione um diretório chamado Dados TI: 

![image](https://user-images.githubusercontent.com/107069287/194888406-fd55705e-19fd-4279-aa76-95ac953de3e4.png)

![image](https://user-images.githubusercontent.com/107069287/194888460-be76c759-f721-471f-a365-723d69d7e5f0.png)

Em seguida clique em ok. 

Acesse a pasta Dados TI, e faça o upload de outro arquivo para esse diretório: 

![image](https://user-images.githubusercontent.com/107069287/194888648-e72860fc-449e-41dc-9ee4-ce9ed57733f9.png)

![image](https://user-images.githubusercontent.com/107069287/194888686-f3d6d895-2744-448e-a25a-eb81ade3383c.png)

![image](https://user-images.githubusercontent.com/107069287/194888787-da89e7e3-ce8f-40df-b68d-04c6746b4293.png)

Em seguida clique em Ok e na sequência Upload. 

Após essa etapa iremos simular a utilização do snapshot. 

Clique na opção Snapshot no campo Operation: 

![image](https://user-images.githubusercontent.com/107069287/194889065-4eeb0e4e-2d75-44ba-b35c-e9cae99e9bf4.png)

Clique em + Add Snapshot: 

![image](https://user-images.githubusercontent.com/107069287/194889162-7d856727-c8f4-4eb7-98a6-570bf8d26994.png)

Adicione um comentário, no meu exemplo utilizarei a data vigente: 

![image](https://user-images.githubusercontent.com/107069287/194889347-c6a50c38-64ab-4517-817b-0c39ac9f11d8.png)

Em seguida clique em ok. 

Acesse o snapshot e note que a estrutura de pasta que criamos se mantém ali, da mesma forma que criamos. 

![image](https://user-images.githubusercontent.com/107069287/194889615-d1ffa861-bde7-4391-9dba-dfa7ac916843.png)

Feito essa etapa, agora vamos mapear a unidade em nosso dispositivo. 

Acesse novamente o Overview de nosso File Share e clique em Connect: 

![image](https://user-images.githubusercontent.com/107069287/194891671-5eb2b115-16c9-42d8-8954-e4b4d4e02bad.png)

Defina o nome da unidade que lhe atender melhor: 

![image](https://user-images.githubusercontent.com/107069287/194891930-9e40ec51-c3e9-4196-87d3-e2af7ebee674.png)

Para este exemplo utilizei a unidade Z. 

Em seguida clique em Show Script: 
*Note que para cada sistema operacional existe um formato de script diferente.* 

![image](https://user-images.githubusercontent.com/107069287/194892225-da3f591a-6c6f-4402-993d-6d55ce2985f3.png)

Copie todo o script que foi gerado: 

![image](https://user-images.githubusercontent.com/107069287/194892369-d6ef1102-b609-4617-beb9-0e7881759323.png)

E em seguida abra um powershell no seu computador e cole o script que foi copiado: 

![image](https://user-images.githubusercontent.com/107069287/194892597-bede52a4-8e70-4fd1-b9aa-074b1fd0cf31.png)

![image](https://user-images.githubusercontent.com/107069287/194894493-11afe547-9461-4afb-907b-b95fc80c084a.png)

Na sequência, navegue pelo link abaixo e faça o Download do Storage Explorer: 

https://azure.microsoft.com/en-us/products/storage/storage-explorer/#features

Abra o storage Explorer e clique na opção entrar com o azure: 

![image](https://user-images.githubusercontent.com/107069287/194917054-45e96f51-a09f-449b-9588-afd2eb37cf48.png)

Em seguida marque a opção Azure e clique em Avançar: 

![image](https://user-images.githubusercontent.com/107069287/194917208-50fe147c-3fb0-4fd9-ad85-5e19152ac31b.png)

Logue com a sua conta do azure: 

![image](https://user-images.githubusercontent.com/107069287/194917400-acaba7e1-7777-497a-bb33-6550e231d87d.png)

E aguarde até o término do processo. Finalizando o software disparará uma mensagem informando que sua conta foi conectada. 

Note que a partir de então você pode visualizar os seus containers e blobs através do próprio storage explorer. 

![image](https://user-images.githubusercontent.com/107069287/194918440-0d90847c-222a-4fa0-8786-1a39255f439a.png)

Concluido esta etapa, a atividade foi concluida com êxito. 




