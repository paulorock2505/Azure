# AZ-104-LAB-MOD-07

 <h2>Lab 07 - Manage Azure Storage</h2> <br>

 ***Tarefa 2:***  
    *Gerenciar blob storage.*

No portal do Azure, pesquise por Storage Accounts: 

![image](https://user-images.githubusercontent.com/107069287/194113156-fd751e32-15cd-4cb2-89ee-5bd79a139219.png)

Em seguida, clique no storage account que criamos na tarefa anterior: 

![image](https://user-images.githubusercontent.com/107069287/194113345-f965916b-7c09-46ed-a975-26235b80ff5a.png)

Na sessão Data Storage, clique em containers: 

![image](https://user-images.githubusercontent.com/107069287/194113468-67d8003e-2074-4d77-839e-f6fb45c1e714.png)

Em seguida clique em + Containers: 

![image](https://user-images.githubusercontent.com/107069287/194113579-0a4574b9-6c3f-40bd-9da6-e69176764ebe.png)

Criaremos inicialmente um blob com o nome blobaz e em modo privado: 

![image](https://user-images.githubusercontent.com/107069287/194114370-a53d5898-7c8b-475b-90be-c23cc42bf93c.png)

![image](https://user-images.githubusercontent.com/107069287/194114417-1bb81a0e-b0d1-4d35-9c37-d924c57bd88f.png)

Em seguida, acesse o blob que acabamos de criar: 

![image](https://user-images.githubusercontent.com/107069287/194115603-6ec9aafa-4304-4a73-929f-19bf4c142c9a.png)

Em Overview, carregue um arquivo de imagem qualquer de sua máquina. 

Clique em upload: 

![image](https://user-images.githubusercontent.com/107069287/194115759-3608688d-1cbb-418a-8c80-01ecbfdd5ae2.png)

Clique no símbolo de pasta conforme a imagem: 

![image](https://user-images.githubusercontent.com/107069287/194115845-f0d8e88a-db8b-4dc4-9f58-866b485b808a.png)

E faça o upload de um arquivo de sua máquina para o blob. 

![image](https://user-images.githubusercontent.com/107069287/194116113-4154d26f-f210-4ef5-aab4-d31de733b952.png)

Em seguida clique em upload. 

Acesse o arquivo que acabamos de enviar e em Overview, copie a URL do arquivo: 

![image](https://user-images.githubusercontent.com/107069287/194117101-8ed9042c-8aef-4e19-8f09-6cff0386fbbc.png)

Armazene o endereço em um bloco de notas e em seguida cole o endereço no navegador e veja o erro que irá gerar. 

![image](https://user-images.githubusercontent.com/107069287/194117339-bd8b3e0a-9666-4fb0-989d-515cb29c2d61.png)

Esse erro se deu por que o change access level que definimos está em modo Privado. 

No portal do Azure, volte a opção do nosso blobaz e vamos alterar o access level para Anonymous: 

![image](https://user-images.githubusercontent.com/107069287/194119677-e656143c-e740-4508-836f-c5ab325acd52.png)

![image](https://user-images.githubusercontent.com/107069287/194119737-1a2bf050-1e6b-4ce9-b899-12936c87fc06.png)

Clique em ok e teste novamente o link no navegador. Note que o arquivo estará acessível agora: 

![image](https://user-images.githubusercontent.com/107069287/194120065-e81cb17a-b808-44ac-9a23-5b098e885f8a.png)

*Tarefa Extra: Mude a opção para Container e gere um Token SAS para ser utilizado por um período específico. Analise os resultados.* 

Feito esta etapa, a tarefa foi concluida com sucesso. 