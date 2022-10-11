# AZ-104-LAB-MOD-07

 <h2>Lab 07 - Manage Azure Storage</h2> <br>

 ***Tarefa 5:***  
    *Configurar o Azure File Sync*

Diagrama da atividade: 

![image](https://user-images.githubusercontent.com/107069287/194920055-ebda2b06-c11e-412c-b1cb-b51e99ef8c72.png)

Acesse o portal e na parte superior clique em PowerShell: 

![image](https://user-images.githubusercontent.com/107069287/194921923-e7a16f83-2952-4703-b32e-66da554ac7a0.png)

Caso queira, abra o PowerShell em uma aba separada: 

![image](https://user-images.githubusercontent.com/107069287/194922308-3adb13b8-65f1-4fd0-985a-253a1819a3bc.png)

Para esta atividade utilize o código abaixo: 

![image](https://user-images.githubusercontent.com/107069287/194922537-e690bd99-5ab1-4ab5-9824-2bbb46f990d8.png)

Copie e cole o primeiro comando no PowerShell: 

![image](https://user-images.githubusercontent.com/107069287/194922744-189b2529-a5aa-459c-a1a6-8a93310fb5de.png)

Pressione enter. 

Em seguida, faça o mesmo procedimento para o segundo comando: 

![image](https://user-images.githubusercontent.com/107069287/194922926-9dea3c6b-cac0-43ff-92b9-1028637ae2bd.png)

E o mesmo processo para o terceiro comando: 

![image](https://user-images.githubusercontent.com/107069287/194923092-ef75fa84-baeb-4a8b-b291-92fa8a8ebf09.png)

Por fim, sete o comando abaixo: 

![image](https://user-images.githubusercontent.com/107069287/194923210-36cd044e-4a2c-4e13-a64f-f74ae5c9ea06.png)

*Opcional: Confira todos os processo criados.*

Feito esta etapa, iremos criar uma máquina virtual. 

No portal, no campo de pesquisa, procure por Virtual Machine: 

![image](https://user-images.githubusercontent.com/107069287/194923890-55a574b0-953f-44ad-8d2c-31f07021b260.png)

Em seguida clique em + Create e em seguida Azure Virtual Machine: 

![image](https://user-images.githubusercontent.com/107069287/194924053-825e0f5d-64c3-4b84-a6d4-c795d7031ea8.png)

Em Basics, configure a Virtual Machine conforme os valores abaixo: 

![image](https://user-images.githubusercontent.com/107069287/194926894-64e87a21-d57c-4edd-b788-aaaf31f15315.png)

Configure o nome de usuário e senha de sua preferência. 

![image](https://user-images.githubusercontent.com/107069287/194926949-b0ce3285-6e1f-4e43-8ac7-80b8bf7ac660.png)

Mantenha a porta 3389 liberada: 

![image](https://user-images.githubusercontent.com/107069287/194928240-ab4d4964-4bfa-40a1-937e-acecaf2ac41b.png)

Clique em Next. 

Em Disks, pode manter o padrão sugerido pelo Azure: 

![image](https://user-images.githubusercontent.com/107069287/194928479-b51c4e72-8fab-4448-af24-880d8253d769.png)

Em seguida clique em Next. 

Em networking vamos manter o padrão sugerido pelo portal do Azure: 

![image](https://user-images.githubusercontent.com/107069287/194929299-3c8a2373-b230-44c7-9acb-95915eb5e722.png)

![image](https://user-images.githubusercontent.com/107069287/194929365-c0e616c2-4ed4-4bfd-8555-07c6fd042a68.png)

E em seguida clicamos em next para a próxima etapa. 

Em advanced, não faremos nenhuma alteração: 

![image](https://user-images.githubusercontent.com/107069287/194929514-faf00229-5054-4f7c-b57a-223cff922115.png)

Clique em Next. 

Em monitoring, apenas iremos desabilitar o boot diagnostics: 

![image](https://user-images.githubusercontent.com/107069287/194929780-846c53ab-cd0a-486f-8664-a4ad2d00c72c.png)

Em seguida clique em next. 

Não vamos alterar nada em Advanced: 

![image](https://user-images.githubusercontent.com/107069287/194929994-3a32b5ce-a54e-4b39-99e3-2f181e8be874.png)

Clique em Next. 

Em Tags, preencha conforme a imagem abaixo: 

![image](https://user-images.githubusercontent.com/107069287/194930089-4a052a31-833d-4e92-a2d3-b431d50f5efd.png)

Clique em seguida em Review + Create e em seguida Create. 

Ao término clique em Go to Resource: 

![image](https://user-images.githubusercontent.com/107069287/194930943-b9abae93-2be0-412f-8203-e4f7f6bf2d82.png)

Em Overview, clique em connect e em seguida RDP: 

![image](https://user-images.githubusercontent.com/107069287/194931077-0937250f-355d-469f-9918-1eeb118eaa71.png)

Faça o Download do cliente RDPe se conecte na máquina virtual que acabamos de criar: 

![image](https://user-images.githubusercontent.com/107069287/194931224-32d787b8-74d2-4073-85b3-1720dde4aa63.png)

Digite os dados do usuário que foi preenchido na criação da máquina: 

![image](https://user-images.githubusercontent.com/107069287/194931260-83103edf-997c-4896-b071-cde7a7435063.png)

![image](https://user-images.githubusercontent.com/107069287/194931352-63248085-8f18-44e2-8cb9-b6ed98a9f1e4.png)

Volte ao portal do Azure, ainda na aba de Virtual Machine, acesse a opção Disks: 

![image](https://user-images.githubusercontent.com/107069287/194931970-731053a6-6f9c-4614-95d7-d7968dab4490.png)

Clique em + Create and attach a new disk: 

![image](https://user-images.githubusercontent.com/107069287/194932133-56a54287-60ff-4130-a132-b9b29d3e95b9.png)

Preencha as informações do disco conforme a imagem e em seguida clique em Save: 

![image](https://user-images.githubusercontent.com/107069287/194932458-9a52caea-ab31-447c-94c3-b5f1c1dc0b9f.png)

Em seguida vá novamente ao acesso RDP da máquina, clique com o botão direito no iniciar do Windows e selecione a opção Disk Management: 

![image](https://user-images.githubusercontent.com/107069287/194932778-395d4762-ac6a-4b6d-ae80-593f841faffb.png)

Pode manter o disco GPT e clicar em ok: 

![image](https://user-images.githubusercontent.com/107069287/194932916-e65c0943-2668-4806-b19a-38f2573a5bfe.png)

Clique com o botão direito no disco não alocado e clique em New Simple Volume: 

![image](https://user-images.githubusercontent.com/107069287/194933092-f8cc454e-0995-4662-aa6d-fb045a23531f.png)

Na primeira tela clique em Next: 

![image](https://user-images.githubusercontent.com/107069287/194933207-89742cc7-c13c-4586-b861-d57779d7fc9b.png)

Nesta etapa utilizaremos apenas 1 GB do disco. Preencha conforme a imagem e clique em Next: 

![image](https://user-images.githubusercontent.com/107069287/194933587-76e6107b-4cc3-43c5-831e-dd4318e17aeb.png)

Pode manter a unidade com a letra F mesmo: 

![image](https://user-images.githubusercontent.com/107069287/194933711-57708a1b-bdec-4423-8432-1c027b1ba9ad.png)

Altere o nome da partição para Dadose clique em Next: 

![image](https://user-images.githubusercontent.com/107069287/194933853-2e351f55-bbe2-46c0-b5a7-f445d9a5e933.png)

Em seguida clique em Finish para completarmos o processo. 

![image](https://user-images.githubusercontent.com/107069287/194933930-7de682ee-f37b-4549-b455-8a2f30c7af46.png)

![image](https://user-images.githubusercontent.com/107069287/194933975-32f91902-aba2-4f69-a8eb-24ae48140269.png)

Vá até o Wndows Explorer e acesse a partição que acabamos de criar: 

![image](https://user-images.githubusercontent.com/107069287/194934845-fc7734e1-7e01-4087-baaf-3e572c0b3ac0.png)

Dentro dela, crie a estrutura de pastas conforme a imagem abaixo: 

![image](https://user-images.githubusercontent.com/107069287/194935351-4bfa52cc-9275-418f-8ca2-dfe21b79222e.png)

![image](https://user-images.githubusercontent.com/107069287/194935414-8b81b8b2-d574-490b-ab51-6b7161e191af.png)

Após criada a estrutura de pastas, populem as pastas com arquivos armazenado em sua própria máquina para preenchemos os espaços. Podem utilizar arquivos de imagem, pdf, texto, word ou excel. 

Feito essa etapa, volte ao portal e vá até a home do azure. No campo de pesquisa, digite Azure File Sync: 

![image](https://user-images.githubusercontent.com/107069287/194939196-641ebe22-c147-4af0-a658-f012612d1e16.png)

Em basics, preencha os campos como a imagem abaixo: 

![image](https://user-images.githubusercontent.com/107069287/194939390-3889c6a2-bbc5-4b10-899a-b5fac3abf53d.png)

Clique em Next. 

Em Network, pode manter o padrão como imagem abaixo: 

![image](https://user-images.githubusercontent.com/107069287/194939471-e2586443-6452-4969-8e25-da7e26a77bce.png)

Clique em Next. 

Em TAGs, preencha conforme utilizamos nos recursos anteriores: 

![image](https://user-images.githubusercontent.com/107069287/194939685-64390c3a-5612-43bb-b974-bfc5ff0b375c.png)

Em seguida clique em Review + Create e em seguida Create. 

Após criarmos o recurso, clique em go to resource: 

![image](https://user-images.githubusercontent.com/107069287/194940108-4274232c-4d10-42ec-b9f9-73a2a20fadd9.png)

Em seguida, clique em + Sync Group para criarmos o grupo de sincronização: 

![image](https://user-images.githubusercontent.com/107069287/194940295-d1709be6-9a36-4d44-8d0b-0ec334fe1dab.png)

Preencha o nome do grupo de sinconização conforme a imagem: 

![image](https://user-images.githubusercontent.com/107069287/194940473-a1f9352f-1351-4e17-8a26-d5e31d2c85da.png)

Em seguida clique em select storage account: 

![image](https://user-images.githubusercontent.com/107069287/194940557-0872b60d-d759-4927-a749-2aa469631fbd.png)

Selecione o storage account que criamos: 

![image](https://user-images.githubusercontent.com/107069287/194940625-b3d3cc79-caa0-41a4-8ab5-aec47b468db9.png)

Em seguida clique no File Share que criamos: 

![image](https://user-images.githubusercontent.com/107069287/194940699-eb600df2-ef6e-42b5-91fb-77198f3fcd24.png)

Em seguida clique em Create. 

Após essa etapa, nós precisamos registrar o nosso servidor. 

Volte para a meno principal do storage que criamos e clique em Registered Servers: 

![image](https://user-images.githubusercontent.com/107069287/195107374-d4854301-a9a4-48fb-a7aa-7b7914632c79.png)

Clique com o botão direito em Azure File Sync Agent e copie o link: 

![image](https://user-images.githubusercontent.com/107069287/195107633-d2fb41ff-5f5d-438e-a9a7-99a8903fd842.png)

Cole o link no navegador da Virtual Machine. <br>

![image](https://user-images.githubusercontent.com/107069287/195156241-51fca3f2-ec3b-482e-9d85-ab4c01dee7fc.png)

*OBS: Para que o navegador não fique bloqueando todos os links de internet vá até o Server Manager, Clique em Local Server e na opção IE Enhanced Security Configuration marque Off: 

![image](https://user-images.githubusercontent.com/107069287/195156052-0a285425-c86a-46cf-baf9-e4598c2383ba.png)

Feito isso, atente-se para fazer o download da versão correta do sistema operacional para que todas as funcionalidades fiquem ativas no sistema operacional: 

![image](https://user-images.githubusercontent.com/107069287/195156998-2226ccbc-51da-4edf-809c-c5b80dd25076.png)

Feito o download do Agent, você será direcionado ao Wizard de instalação. Na primeira tela de boas vindas pode clicar em Next: 

![image](https://user-images.githubusercontent.com/107069287/195157218-bf13fb50-5f49-4787-bfdb-2e03f65f92b5.png)

Aceite os termos de uso e clique em Next: 

![image](https://user-images.githubusercontent.com/107069287/195157309-a6898b34-d927-4313-9d58-a792ea9d8452.png)

A partir daqui todas as opções que escolheremos será default mesmo: 

![image](https://user-images.githubusercontent.com/107069287/195158121-3a4dfa87-74cc-4e55-83b8-6ef386a49364.png)

![image](https://user-images.githubusercontent.com/107069287/195158169-8caa4864-37a3-43e0-a930-e699f9116c50.png)

![image](https://user-images.githubusercontent.com/107069287/195158254-34c4d41e-f405-41a3-90fa-93403e912616.png)

![image](https://user-images.githubusercontent.com/107069287/195158312-bd58b30a-af84-4ccd-ba3e-fa312560f326.png)

Aguarde até o término da instalação e clique em finish. 

Fnalizado essa etapa, agora faremos a parte do registro. 

Nessa primeira tela clique em Ok: 

![image](https://user-images.githubusercontent.com/107069287/195159206-3ca0d41f-444d-4d22-9afa-c2d83124c8f9.png)

Escolha o Azure Cloud e clique em Sign in: 

![image](https://user-images.githubusercontent.com/107069287/195159357-66742f44-c86b-4924-b89e-e71510ff9ffb.png)

Logue com sua conta azure: 

![image](https://user-images.githubusercontent.com/107069287/195159447-3789c108-1879-42c1-a96b-8c0d0a81ffad.png)

Após o login faça o registro de sua conta e preencha os campos conforme estruturamos em nosso laboratório. Em seguida clique em Register: 

![image](https://user-images.githubusercontent.com/107069287/195161103-4be13a34-2487-40b0-9af8-99b181bd191a.png)

Aguarde até finalizar o registro e aparecer a mensagem Registration Successfull: 

![image](https://user-images.githubusercontent.com/107069287/195162212-07b28723-b332-4eae-af77-e901c47e327e.png)

Feito essa etapa, volte ao portal do Azure e aguarde até o servidor aparecer na lista de servidores registrados: 

![image](https://user-images.githubusercontent.com/107069287/195162405-5e324de4-d84f-43fa-ac77-889dd08d8d15.png)

Em seguida clique em Sync Groups: 

![image](https://user-images.githubusercontent.com/107069287/195162566-844d9740-6188-4b1e-899c-97b316c7baea.png)

Clique em Group-FS: 

![image](https://user-images.githubusercontent.com/107069287/195162775-a1c14a97-d737-43d4-84be-766877549593.png)

Clique em Add Server Endpoint: 

![image](https://user-images.githubusercontent.com/107069287/195162924-1b6e5b31-09f9-451d-a7f1-3de8fc70e96a.png)

Em seguida configure a política conforme a imagem abaixo: 

![image](https://user-images.githubusercontent.com/107069287/195164364-896d7e53-657d-41f5-b926-159260ade602.png)

Em seguida clique em Create. 

Aguarde até que a sincronização seja concluida: 

![image](https://user-images.githubusercontent.com/107069287/195165949-6507561c-b8dc-44ba-92b0-0c7cec83caa0.png)

Feito essa etapa a tarefa foi concluída com sucesso. 

*Tarefa Optativa: Vá até o blob que criamos e confira se toda a estrutura da pasta de arquivos que criamos no servidor consta no blob e navegue entre elas. Note que todos os arquivos que foram enviados estão replicados no file share que criamos.*










