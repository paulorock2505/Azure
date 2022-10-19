# AZ-104-LAB-MOD-09

 <h2>Lab 09a - Manage Azure Storage</h2> <br>

 ***Tarefa 1:***  
    *Criar um Azure web app.*

No portal do Azure, no campo de pesquisa, digite Resource Group: 

![image](https://user-images.githubusercontent.com/107069287/196706423-acc4b500-346a-4d05-8abf-0e2d54b7f3ed.png)

Clique em + Create: 

![image](https://user-images.githubusercontent.com/107069287/196706684-8e8d3068-1667-436e-8ea6-77ab8efc638a.png)

Em basics, crie o recurso com os parametros mencionado abaixo: 

![image](https://user-images.githubusercontent.com/107069287/196706957-09263d9c-92e5-4299-b940-634f13704f6b.png)

Em TAGs, configure utilizando os parametros como no exemplo abaixo: 

![image](https://user-images.githubusercontent.com/107069287/196707827-bd2adf2e-03f5-47ce-9ef6-8fe31c0e53c2.png)

Em seguida clique em Review + Create e em seguida Create. 

Concluido essa etapa, volte a home do Azure e no campo de pesquisa digite App Services: 

![image](https://user-images.githubusercontent.com/107069287/196708786-ca866d63-871f-4d0e-8daf-05b71c6640f7.png)

Clique em + Create: 

![image](https://user-images.githubusercontent.com/107069287/196710214-5e74817d-7620-421b-a7f8-0d4a256b7702.png)

Configure conforme a imagem abaixo: <br>
***OBS: No campo name, utilize um nome único, pois esse nome será utilizado para realizar o acesso ao aplicativo e não pode ter nenhum outro existente na plataforma Azure.***

![image](https://user-images.githubusercontent.com/107069287/196710895-a0cbdfde-ee9d-4db4-b96a-fac179e0a0e3.png)

Em SKU and Size, clique em Change Size: 

![image](https://user-images.githubusercontent.com/107069287/196712188-cf4d4d58-012b-41ff-9a49-74205ab90b64.png)

Selecione o Plano Standard S1: 

![image](https://user-images.githubusercontent.com/107069287/196714120-7028ee20-2463-4b3d-b966-241c8ffef229.png)

Clique em Next. 

Em Deployment vamos manter o continous deployment desabilitado: 

![image](https://user-images.githubusercontent.com/107069287/196714507-620903ec-b6fb-4fef-acd9-1f19c224bcfd.png)

Clique em Next. 

Em Networking, manteremos também o padrão recomendado: 

![image](https://user-images.githubusercontent.com/107069287/196715217-ffce6d87-549f-4124-826f-c9f9666cb029.png)

Clique em Next. 

Em monitoring manteremos novamente o padrão: 

![image](https://user-images.githubusercontent.com/107069287/196715500-66d8c0b1-9014-49d9-a84a-8abdef96deb0.png)

Clique em Next. 

Em TAGs, preencha o campo conforme a imagem abaixo: 

![image](https://user-images.githubusercontent.com/107069287/196716408-dbcab523-784e-4a1e-89e5-d4b00f69d0d7.png)

Em seguida clique em Review + Create e em seguida Create. 

Ao término dessa etapa, em Overview, copie o link e teste o acesso da aplicação. 

Feito essa etapa, a tarefa foi concluida. 
