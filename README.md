# auladelinux
aula de linux

Projeto Infraestrutura como Código (IaC) 

Descrição do Projeto 
Este projeto tem como objetivo automatizar a criação da infraestrutura de usuários, grupos, diretórios e permissões em ambientes Linux por meio de Shell Script. Após a execução do script, 
uma nova máquina virtual estará pronta para uso, reduzindo erros manuais e agilizando o processo de configuração. 

Recursos Utilizados 

Ubunto sever 

Shell Script (Bash) 

Git 

GitHub 

Estrutura Criada 

Diretórios: /publico, /adm, /ven e /sec 

Grupos: GRP_ADM, GRP_VEN e GRP_SEC 

Usuários organizados por departamento e associados aos respectivos grupos. 

Permissões 

/adm - acesso exclusivo do grupo administrativo. 

/ven - acesso exclusivo do grupo de vendas. 

/sec - acesso exclusivo do grupo de secretaria. 

/publico - acesso liberado para todos os usuários. 

Execução 

chmod +x iac.sh 
sudo ./iac.sh 

Conclusão 

A utilização de Infraestrutura como Código (IaC) permite padronizar configurações,
facilitar a administração de ambientes Linux e manter os scripts versionados no GitHub para futuras implementações. 
