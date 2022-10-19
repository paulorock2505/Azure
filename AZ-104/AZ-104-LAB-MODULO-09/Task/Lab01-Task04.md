# AZ-104-LAB-MOD-09

 <h2>Lab 09a - Implemente Web Apps</h2> <br>

 ***Tarefa 4:***  
    *Implante o código para o slot de testes.*

Abra o portal e acesse o cloudshell no primeiro ícone a direita do painel: 

![image](https://user-images.githubusercontent.com/107069287/196762369-5bd17050-baa5-47f2-a701-05b19a712b4f.png)

Dentro do Power Shell, copie o código abaixo e execute no Power Shell: 

git clone https://github.com/Azure-Samples/php-docs-hello-world

![image](https://user-images.githubusercontent.com/107069287/196763619-8a6ab050-ff2d-4653-9851-82558bcfa5cc.png)

Set-Location -Path $HOME/php-docs-hello-world/

![image](https://user-images.githubusercontent.com/107069287/196763860-86925c54-e5e5-444f-bc71-0de923909876.png)

Clique agora em Local Git/FTPS Credentials: 

![image](https://user-images.githubusercontent.com/107069287/196766026-d9606926-a48e-4a0c-bdf4-e81cc2e712c4.png)

Em User Scope, adicione uma credencial de sua preferência: 

![image](https://user-images.githubusercontent.com/107069287/196766199-bdccf3dd-8965-41de-8c0f-937f877df0bd.png)

Em seguida clique em Save. 

Edite o comando abaixo com os dados solicitados: 

git remote add [deployment_user_name] [git_clone_url]

Exemplo: <br>
git remote add paulorocha https://paulorocha@alpate19102022-alpatec19102022staging.scm.azurewebsites.net/alpate19102022.git

![image](https://user-images.githubusercontent.com/107069287/196766969-05a82c17-fb7e-47a8-aa62-4cc198f9c7da.png)

Edite o comando abaixo com o usuário que foi criado novamente: 

git push [deployment_user_name] master

Exemplo: <br>
git push paulorocha master

Por fim autentique com a senha que foi criada e aguarde o término do processamento. 

Faça o teste com a URL que está criada em Overview. Copie a URL e cole no navegador para fazer o teste. Apresentando a tela do Hello Word a implantação foi concluida com sucesso e a atifvidade finalizada. 




