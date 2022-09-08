![Diagrama Azure](https://user-images.githubusercontent.com/107069287/184007627-6ee47d6a-54f3-46c8-bced-bacbfaa4893a.PNG)
# Microsoft-Azure-Aplication-Gateway-com-SSL-Offloading
Neste projeto baseado em um cenário real realizei a implantação do serviço Application Gateway com SSL Offload para hospedar duas aplicações baseadas em Linux.  O intuito desse projeto era manter o acesso via porta segura com os usuários da internet mantendo a perfomance de comunicação internamente entre o Application Gateway e as aplicações hospedadas nas Virtuais Machines. 

Abaixo segue os passos que realizei: 

1- Criei o Resource Group: RG-ALPA (East US). 

2- Criei 2 Virtual Network: VNET-APP e VNET-DATABASE, todas hospedadas dentro do Resource Group: RG-ALPA

3- Criei 4 Subnets (uma para cada Pool de máquina Virtual) e mais uma para o Application Gateway conforme é sugerido na documentação de implantação. Foram elas: SUB-VM-01, SUB-VM-02, SUB-DB E SUB-APPGW. 

4- Criei também 3 NSGs (neste caso utilizei uma para cada máquina virtual). Criei uma regra de negação fechando todas as portas e mantive apenas as portas de comunicação das aplicações. Entre a SUB-DB e a SUB-VM-01 e SUB-VM-02 habilitei a comunicação pela porta 3306 e entre a SUB-APPGW e SUB-VM-01 e SUB-VM-02 habilitei o acesso pela porta 80. 

5- Fiz um peering entre a VNET-APP e VNET-DB para conseguir efetivar a comunicação entre as VNETs. 

6- Criei as 3 VMs conforme o Diagrama utilizando um Debian 10. 

7- Após criada as máquinas instalei o MariaDB na máquina destinada ao Banco de Dados e o Apache nas máquinas que são destinadas a aplicação, bem como o PHP conforme exigida na documentação das plataformas. 

8- Instalei as plataformas conforme o escopo. 

9- Criei o Application Gateway na mesma VNET que os Webservices e na sequência criei a SUBNET isolada para o Application Gateway. 

10- Após criado e configurado, instalei o certificado no Application Gateway e fiz o teste de conexão com as aplicações utilizando a porta 443. 

Implantação concluida com sucesso. 

![WhatsApp Image 2022-08-01 at 09 21 46](https://user-images.githubusercontent.com/107069287/184012556-fc46dba8-86de-45e0-9e14-7b3f31825ca0.jpeg)

