Vagrant-Setup 
===========

Servidor LAMP (Linux, Apache, MySQL, PHP)

Configuração do Vagrant (com provisionamento em Shell Script) para criar uma máquina virtual (Ubuntu Server 14.04 64 Bits) de desenvolvimento em PHP.

### Pacotes Inclusos:

- PHP 7.1
- MySQL 5.5
- Git
- PhpMyAdmin 
- Composer
- cURL
- Vim
- Redis
(Para mais detalhes consulte arquivo setup.sh)


Você vai precisar: 
==============

- Virtualbox - https://www.virtualbox.org/
- Vagrant - http://www.vagrantup.com/
- Git - http://git-scm.com 

-> Instale o Virtualbox e o Vagrant de acordo com seu sistema operacional. 


Modo de Uso
===========

Instalação inicial:

* git clone https://github.com/especializati/vagrant-setup-php.git 

* Entre no diretório do Projeto/* (Nome do Projeto) 

* Inicie a máquina virtual: vagrant up 



Após este comando 'vagrant up', o Vagrant ficará responsavel por baixar o sistema operacional ( neste caso Ubuntu Server 64 ), configurar a máquina virtual no VirtualBox e posteriormente baixar, instalar e configurar todos os pacotes do script 'setup.sh' (Sim! A primeira vez realmente é um pouco mais demorado).

Quando tudo estiver pronto, um servidor web estará disponível no endereço http://localhost:8080, e a instalação do PHPMyAdmin está em http://localhost:8080/phpmyadmin, para acessar utilize:

- Login: root
- Senha: vagrant
obs:(A senha padrão para todos os serviços é vagrant).

Coloque seu código no diretório "www". 
Acesse a url http://localhost:8080 e veja se aparece as informações de serviço do PHP

Para desligar a máquina virtual utilize o comando:
- vagrant halt

Para religar novamente utilize:
- vagrant up

Caso queira destruir a máquina virtual (o conteúdo do www não será excluido):
- vagrant destroy
