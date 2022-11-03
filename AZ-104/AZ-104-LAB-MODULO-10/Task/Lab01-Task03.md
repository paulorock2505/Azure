# AZ-104-LAB-MOD-10

 <h2>Lab 10 - Azure Backup</h2> <br>

 ***Tarefa 3:***  
    *Implementar backup de arquivos e pastas em máquinas on-premisses com cliente MARS.*

No portal do Azure, no campo de pesquisa, digite Recovery Services Vault e em seguida clique na opção marcada na imagem: 

![image](https://user-images.githubusercontent.com/107069287/199734882-ecb340c4-6faa-40ff-ba78-4f345838c749.png)

Em seguida clique no recurso rsv-az104 que criamos nas atividades anteriores: 

![image](https://user-images.githubusercontent.com/107069287/199735065-34abd28f-dda5-4337-b5df-e0ff29e02cec.png)

Clique na opção + Backup: 

![image](https://user-images.githubusercontent.com/107069287/199735262-6c13f80b-5f2b-488a-b009-fb5e0339c396.png)

Marque as opções conforme a imagem abaixo e clique em prepare infrastructure: 

![image](https://user-images.githubusercontent.com/107069287/199736209-9c8b2622-cf58-4453-8063-dd5374c43ddb.png)

Em seguida clique em Download Agent for Windows Server or Windows Client e execute o agent: 

![image](https://user-images.githubusercontent.com/107069287/199738107-1589c34c-735e-4b3b-8a99-00a05862c286.png)

Execute o agent e faça a instalação: 

![image](https://user-images.githubusercontent.com/107069287/199738607-fe2a96a6-95a2-4b24-a45b-f73549dd6d99.png)

Clique em próximo. 

Nesta janela de configuração, ele mostra as opções de fazer as configurações utilizando um serviço de proxy. Caso aja alguma necessidade você pode utilizar esse campo e configurar o proxy de sua infraestrutura. No entanto, para este laboratório, não utilizaremos essas configurações. 

![image](https://user-images.githubusercontent.com/107069287/199738997-a90efea4-b087-4b18-b63e-34984b9a3550.png)

Clique em próximo novamente. 

Note que alguns requisitos foram solicitados como Net.Framework 4.5 e o Windows Power Shell. Caso sua máquina tenha os dois recursos irá habilitar o botão de instalação. Clique em instalar: 

![image](https://user-images.githubusercontent.com/107069287/199739761-3bcef6b2-c00b-4cf6-a816-8dffeaa26591.png)

Aguarde até concluir a instalação. 

Na sequência clique em Prosseguir com o registro: 

![image](https://user-images.githubusercontent.com/107069287/199754123-830d69b2-1b94-4aba-bb3e-2e19db4bbcb7.png)

![image](https://user-images.githubusercontent.com/107069287/199754371-abb4efe5-69f6-44de-9a26-ad6047539e56.png)

Volte ao portal do Azure, marque a opção Already downloaded or using the latest Recovery Services Agent e faça o Download da credencial do cofre: 

![image](https://user-images.githubusercontent.com/107069287/199754736-5c2c1c06-c4b8-48c5-ab4c-3fd2929f5503.png)

Volte para o Assistente de instalação do Agente de Serviços de Recuperação do Microsoft Azure, clique em procurar e localize em seu computador a pasta que foi feito o download do arquivo VaultCredentials. No pc que estou utilizando para esse laboratório o arquivo está na pasta Download: 

![image](https://user-images.githubusercontent.com/107069287/199755618-2b98daf8-0968-4c21-aad9-57ab5e8f3a6a.png)

![image](https://user-images.githubusercontent.com/107069287/199755726-2c08a7aa-aeb3-486b-907d-bb12dadcec8f.png)

![image](https://user-images.githubusercontent.com/107069287/199755788-39bedeb8-855f-488d-9591-7f4e7ae4fe9a.png)

Clique em próximo. 

Em seguida insira uma senha de no minimo 16 digitos para posteriormente, caso precise reinstalar o agente, você possa acessar a pasta de recuperação. Em seguida defina um local para guardar esse arquivo que será gerado, de preferência utilize um local seguro para evitar qualquer tipo de falha acidental: 

![image](https://user-images.githubusercontent.com/107069287/199757377-b0c9b70c-da23-4829-a409-6d6a7ee113be.png)

Em seguida clique em concluir. 

![image](https://user-images.githubusercontent.com/107069287/199757649-8ce2521d-c188-4662-ba7a-65eef9bb79ea.png)

![image](https://user-images.githubusercontent.com/107069287/199757969-70470543-f553-4152-86be-777207e4e6d6.png)

Em seguida clique em fechar e inicie o Agent do MARS. 

Em seguida, no campo direito, clique em Backup Agendado para criarmos o primeiro job de backup: 

![image](https://user-images.githubusercontent.com/107069287/199758661-8d78a2ba-a865-4ced-bb2b-cde297d1019a.png)

Na tela de introdução pode clicar em próximo: 

![image](https://user-images.githubusercontent.com/107069287/199758811-be436942-7692-47ed-9a14-62a475bf7b18.png)

Clique em Adicionar itens e escolha a pasta que você queira fazer o backup de sua máquina: 

![image](https://user-images.githubusercontent.com/107069287/199759298-1da4eba9-f767-4680-acf7-d1c2abe86b07.png)

![image](https://user-images.githubusercontent.com/107069287/199759607-71eff06e-a288-42aa-ad7d-2fe133b5f955.png)

Para este laboratório você pode escolher qualquer diretório de pastas da sua escolha. 

Feito a escolha clique em próximo: 

![image](https://user-images.githubusercontent.com/107069287/199759848-6c310854-0f2b-46ed-81da-b61efdada55e.png)

Em seguida especifique um agendamento da sua escolha: 

![image](https://user-images.githubusercontent.com/107069287/199760250-c3d29609-1349-4a6e-936d-28da6b788506.png)

***OBS: O MARS só permite executar até três agendamentos por dia. Nesse exemplo iremos utilizar duas vezes***

Clique em próximo. 

Em seguida selecione a política de retensão semanal que você queira utilizar, neste laboratório iremos usar apenas a política de 30 dias. No entanto é importante ressaltar que para ambientes de produção é sempre importante criar uma política mais ampla de retensão de dados: 

![image](https://user-images.githubusercontent.com/107069287/199761177-f1127f99-c4c6-4a42-9097-4bf29e2d93e4.png)

Clique em próximo. 

Na sequência, temos a opção de envio. Note que além da transferência online também temos as opções de envio pelo Microsoft Databox ou por disco próprio. Nesse laboratório utilizaremos a opção de envio online: 

![image](https://user-images.githubusercontent.com/107069287/199762082-3110a4ce-f841-45e8-8771-9feb1afd6252.png)

Em confirmação apenas clique em concluir: 

![image](https://user-images.githubusercontent.com/107069287/199762270-10febad8-52a9-48e4-9e39-3656fd23ad1f.png)

E aguarde até o término do processo de criação do agendamento: 

![image](https://user-images.githubusercontent.com/107069287/199762393-20315799-977d-42d7-9a1b-f5759a20da0c.png)

Feito essa etapa clique em Fechar e em seguida clique em Realizar o Backup Agora: 

![image](https://user-images.githubusercontent.com/107069287/199765067-f92a19c6-d530-46fb-a9fc-4c62ed095b1d.png)

Em reter o backup até, note que a política de retenção está informando a data de 30 dias após a criação. Apenas clique em próximo: 

![image](https://user-images.githubusercontent.com/107069287/199765708-f2909ee9-7bbf-4008-891b-9a2243c099b7.png)

Em seguida clique em Back up e inicie o processo: 

![image](https://user-images.githubusercontent.com/107069287/199765836-223dc5f6-2256-4364-b595-47df903d94e9.png)

Após concluir apenas clique em Fechar: 

![image](https://user-images.githubusercontent.com/107069287/199766659-65119281-0f4a-4e5f-b3ac-4b5f9f38762b.png)

Feito essa etapa a atividade foi concluída com sucesso. 
