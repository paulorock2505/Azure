# AZ-104-LAB-MOD-08

 <h2>Lab 08 - Manage Azure Storage</h2> <br>

 ***Tarefa 5:***  
    *Dimensione o tamanho do storage para Azure VM scale sets.*

No portal, no campo de pesquisa, digite scale set e clique em Virtual Machine Scale Set: 

![image](https://user-images.githubusercontent.com/107069287/196502864-18374b13-67cf-4a37-9e81-ef72c651b2dc.png)

Clique em scalesetvmtemplate, que acabamos de criar: 

![image](https://user-images.githubusercontent.com/107069287/196502997-8022a93b-1834-4368-bda7-5cbabbc30595.png)

Em seguida vá até o campo settings e clique em size: 

![image](https://user-images.githubusercontent.com/107069287/196503145-e45f4cc0-73e5-4e3e-8528-c1f76a11f677.png)

Vamos alterar o tamanho de B2s para D2s_v3: 

![image](https://user-images.githubusercontent.com/107069287/196503387-98c2f1d4-31ba-447d-812a-b08a9dbd9389.png)

*Após essa etapa o ideal é você fazer o reimage no conjunto de máquinas para aplicar as alterações em todas as máquinas:* 

![image](https://user-images.githubusercontent.com/107069287/196505186-9fbea5f9-f39a-468e-aa6b-69e754963133.png)

*Obs: Esse processo gera indisponibilidade da máquina por alguns minutos. Em ambiente de produção é interessante fazer o protocolo para executar essa etapa, bem como disparar o informe para todas as equipes que operam o sistema de maneira direta.* 

Note que após esse processo, nossa máquina já está com a estrutura nova implementada: 

![image](https://user-images.githubusercontent.com/107069287/196503877-65e6e44d-a554-41d1-b53f-c4043b278756.png)

Feito essa etapa a atividade foi concluída com sucesso. 

Para não gerar custos adicionais, delete todas as estruturas que criamos. 



