README
======

Esse é um template de aplicação Zend Framework usado por mim para os projetos da Coderockr

Estrutura do projeto:
.htaccess - arquivo com as configurações de redirect necessárias para o projeto
config/config.ini - arquivo com as configurações do projeto como cache, banco de dados, traduções, etc
controllers/ - diretório para os controladores do projeto
data/cache - diretório para salvar cache em arquivos
doc - documentações do projeto
forms - diretório para os formulários do projeto, criados com Zend_Form
index.php - bootstrap do projeto. É necessário configurar ao menos os caminhos dos diretórios, nas linhas 33 a 40
models - modelos do projeto
views/layouts - layouts do projeto
views/scripts/ - diretórios para as visões usadas pelos controladores


VHOST
=====================

Uma forma fácil de se trabalhar com projetos é configurar um VHOST em seu Apache. No arquivo de configuração faça como no exemplo:

<VirtualHost *:80>
   DocumentRoot "/Applications/MAMP/htdocs/Template-ZF"
   ServerName zf.local
	
   SetEnv APPLICATION_ENV "development"	
	
   <Directory "/Applications/MAMP/htdocs/Template-ZF">
       Options Indexes MultiViews FollowSymLinks
       AllowOverride All
       Order allow,deny
       Allow from all
   </Directory>
</VirtualHost>