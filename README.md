# auladelinux F
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
#!/bin/bash

echo "Criando diretórios..."

mkdir /publico
mkdir /adm
mkdir /ven
mkdir /sec

echo "Criando grupos..."

groupadd GRP_ADM
groupadd GRP_VEN
groupadd GRP_SEC

echo "Criando usuários do grupo ADM..."

useradd carlos -m -s /bin/bash -G GRP_ADM
useradd maria -m -s /bin/bash -G GRP_ADM
useradd joao -m -s /bin/bash -G GRP_ADM

echo "Criando usuários do grupo VEN..."

useradd debora -m -s /bin/bash -G GRP_VEN
useradd sebastiana -m -s /bin/bash -G GRP_VEN
useradd roberto -m -s /bin/bash -G GRP_VEN

echo "Criando usuários do grupo SEC..."

useradd josefina -m -s /bin/bash -G GRP_SEC
useradd amanda -m -s /bin/bash -G GRP_SEC
useradd rogerio -m -s /bin/bash -G GRP_SEC

echo "Definindo senhas padrão..."

echo "carlos:Senha123" | chpasswd
echo "maria:Senha123" | chpasswd
echo "joao:Senha123" | chpasswd
echo "debora:Senha123" | chpasswd
echo "sebastiana:Senha123" | chpasswd
echo "roberto:Senha123" | chpasswd
echo "josefina:Senha123" | chpasswd
echo "amanda:Senha123" | chpasswd
echo "rogerio:Senha123" | chpasswd

echo "Configurando permissões dos diretórios..."

chown root:GRP_ADM /adm
chown root:GRP_VEN /ven
chown root:GRP_SEC /sec

chmod 770 /adm
chmod 770 /ven
chmod 770 /sec
chmod 777 /publico

echo "Fim..."



chmod +x iac.sh 
sudo ./iac.sh 

Conclusão 

A utilização de Infraestrutura como Código (IaC) permite padronizar configurações,
facilitar a administração de ambientes Linux e manter os scripts versionados no GitHub para futuras implementações. 
