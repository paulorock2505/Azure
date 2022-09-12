<h2>Lab 02 - Manage Azure resources with templates</h2> 

<h3>Lab Scenario</h3> 

Agora que você explorou os recursos básicos de administração do Azure associados ao provisionamento de recursos e à organização com base em grupos de recursos usando o portal do Azure, é necessário executar a tarefa equivalente usando os modelos do Azure Resource Manager. 

<h3>Objetivos:</h3>

<table border="1">    
  <tr>
    <th colspan="1">Tarefa 1:</th>  	              
    <th colspan="2">Implante um modelo ARM usando um deploy seu como base.</th>
  </tr>
<td>Tarefa 2:</td>
    <td>Implante recursos através de um ARM diretamente do GitHub.</td>
  </tr>
 </table>
 
 <table border="1">    
  <tr>
    <th colspan="1">Resource Group</th> 
</table>

<table border="1">    
  <tr>
    <th colspan="1">Setting</th>  	              
    <th colspan="2">Value</th>
  </tr>
<td>Resource Group</td>
    <td>RG-LAB-01</td>
  </tr>
  <tr>
    <td>Region </td>
    <td>East US 2</td>
  </tr>
  <td>Name</td>
    <td>VM-ARM-01</td>
  </tr>
  <tr>
    <td>Image</td>
    <td>Linux Ubuntu</td>
  </tr>
  <tr>
    <td>Size</td>
    <td>B2s</td>
  </tr>
 </table>
 <h6><i>OBS: Para este Laboratório, utilizaremos os mesmos Grupos de Recursos das tasks anteriores.</i></h6>

No portal do azure, no campo de pesquisa, digite Resource Groups:

![image](https://user-images.githubusercontent.com/107069287/189681759-ed7d2108-5464-4dee-adb7-0e8985e488db.png)

Verifique os grupos de recursos criados: 

![image](https://user-images.githubusercontent.com/107069287/189683287-171e9d44-c1ac-41d5-a470-d26205a51479.png)

Na sequência iremos criar as máquinas virtuais que serão utilizadas nesse laboratório. 

Vá até a página inicial do Azure, no campo de pesquisa digite Virtual Machines: 

![image](https://user-images.githubusercontent.com/107069287/189683533-ed1bd2aa-d8f8-4074-aed8-9d19583487fd.png)

Em virtual Machine, clique em + Create e em seguida Azure Virtual Machine: 

![image](https://user-images.githubusercontent.com/107069287/189683823-7cb99cb3-2e34-4be3-9747-acdacfb9f58b.png)

Vamos alterar preencher os campos seguindo o modelo adotado: 
- Em Resource Group utilizaremos o RG-LAB-01; 
- Em Virtual Machine Name utilizaremos o nome VM-ARM01
- Image pesquisaremos em See All Images por Ubuntu 16.04 gen1; 
- Size utilizaremos o B2s 
- Utilizaremos em authentication type a opção password
- Por fim criaremos um usuário e senha para o administrador 

Veja imagem abaixo: 

![image](https://user-images.githubusercontent.com/107069287/189685030-75ab7e2d-38cc-4e4b-a5d1-0da692af9f53.png)
![image](https://user-images.githubusercontent.com/107069287/189685095-8a7d8519-f75b-4a05-a76e-acb7943583b2.png)
![image](https://user-images.githubusercontent.com/107069287/189685404-bde9c515-a6ca-40cc-9fac-bf9e3e8e35d0.png)







