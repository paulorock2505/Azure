<h2>Lab 04 - Implement Virtual Networking</h2>

<p>Task 01: Crie um RG, uma VNET e duas Subnets.</p>

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
    <td>RG-MOD04</td>
  </tr>
  <tr>
    <td>Region </td>
    <td>East US 2</td>
  </tr>
 </table> 
 
 <table border="1">    
  <tr>
    <th colspan="1">VNET</th> 
</table>

<table border="1">    
  <tr>
    <th colspan="1">Setting</th>  	              
    <th colspan="2">Value</th>
  </tr>
<td>VNET Name</td>
    <td>az104-04-vnet1</td>
  </tr>
  <tr>
    <td>Region </td>
    <td>East US 2</td>
  </tr>
  <tr>
    <td>Address</td>
    <td>10.40.0.0/20</td>
  </tr>
 </table> 
 
 <table border="1">    
  <tr>
    <th colspan="1">Subnet0</th> 
</table>

<table border="1">    
  <tr>
    <th colspan="1">Setting</th>  	              
    <th colspan="2">Value</th>
  </tr>
<td>Subnet Name</td>
    <td>subnet0</td>
  </tr>
  <tr>
    <td>Address</td>
    <td>10.40.0.0/24</td>
  </tr>
 </table> 
 
 <table border="1">    
  <tr>
    <th colspan="1">Subnet1</th> 
</table>

<table border="1">    
  <tr>
    <th colspan="1">Setting</th>  	              
    <th colspan="2">Value</th>
  </tr>
<td>Subnet Name</td>
    <td>subnet1</td>
  </tr>
  <tr>
    <td>Address</td>
    <td>10.40.0.0/24</td>
  </tr>
 </table> 

Abra o portal do Azure e no campo de pesquisa busque por Resource Group: 

![image](https://user-images.githubusercontent.com/107069287/190425063-189df598-896c-492b-8a13-f7f7dcfa1534.png)

Clique em + Create: 

![image](https://user-images.githubusercontent.com/107069287/190425174-b6544753-1998-4693-851b-8f124d53d162.png)

Em Resource Group, vamos criar o recurso de acordo com a tabela acima: 

![image](https://user-images.githubusercontent.com/107069287/190425535-33ca6276-c852-41fc-b33a-57dfedd51e6e.png)

Clique em Next. 

Vamos criar uma TAG mantendo o padrão utilizado anteriormente, utilize as TAGs conforme a imagem abaixo: 

![image](https://user-images.githubusercontent.com/107069287/190426041-a327f853-3833-4715-ada6-fa968fc54829.png)

Clique em Review + Create e em seguida Create para criar o grupo de recursos. 






