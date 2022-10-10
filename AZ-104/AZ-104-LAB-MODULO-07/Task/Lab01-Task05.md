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






