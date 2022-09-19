<h2>Lab 04 - Implement Virtual Networking</h2>
 
<h3>Task 6: Configurar o DNS do Azure para resolução de nomes externos</h3>

Validar o domínio: https://www.godaddy.com/domains/domain-name-search

<table border="1">    
  <tr>
    <th colspan="1">DNS Externo</th> 
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
    <td>Name</td>
    <td>alpatec.com.br</td>
  </tr>
  </table>
   
<table border="1">    
  <tr>
    <th colspan="1">Registro VM0</th> 
</table>

<table border="1">    
  <tr>
    <th colspan="1">Setting</th>  	              
    <th colspan="2">Value</th>
  </tr>
<td>Name</td>
    <td>az104-04-vm0</td>
  </tr>
  <tr>
    <td>Type</td>
    <td>A</td>
  </tr>
   <tr>
    <td>TTL</td>
    <td>1</td>
  </tr>
   <tr>
    <td>TTL unit</td>
    <td>Hours</td>
  </tr>
   <tr>
    <td>Ip address</td>
    <td>the public IP address of az104-04-vm0</td>
  </tr>
  </table>

  <table border="1">    
  <tr>
    <th colspan="1">Registro VM1</th> 
</table>

<table border="1">    
  <tr>
    <th colspan="1">Setting</th>  	              
    <th colspan="2">Value</th>
  </tr>
<td>Name</td>
    <td>az104-04-vm1</td>
  </tr>
  <tr>
    <td>Type</td>
    <td>A</td>
  </tr>
   <tr>
    <td>TTL</td>
    <td>1</td>
  </tr>
   <tr>
    <td>TTL unit</td>
    <td>Hours</td>
  </tr>
   <tr>
    <td>Ip address</td>
    <td>the public IP address of az104-04-vm0</td>
  </tr>
  </table>

  