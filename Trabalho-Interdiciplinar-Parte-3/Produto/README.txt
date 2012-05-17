Trabalho de Projeto de Sistemas
Autores
Diego Rodrigues|Graziella Arca|Leonardo Miyamoto

Professor(a): Maria Augusta
Email: psi.si.puc@gmail.com

/*************************************************************************/

GRUPOS
Projetos de Sistemas de Informa��o
*Diego Rodrigues Alves da Silva
*Graziella Arca Guerra Alves
*Leonardo Musashi Miyamoto

Interface Homem Maquina
*Bruno Soares Romano
*Jonathan Inacio Melquiades Pimenta
*Leonardo Musashi Miyamoto
*Marcos Soares de Castro

Gerencia de Projetos
*Helton Leandro Muniz da Silveira
*Laila Cristina de Aguiar Martins	
*Livia Rosa Souza	
*Tiago Amim

Engenharia de Software II
*Luciene Teodoro
*Washington do Nascimento
*Livia Rosa Souza
*Rodrigo Ferreira
*Lucas Souza Duarte

Engenharia de Software I
*Yuri
*Ludiane
*Rodrigo
*Pedro H Morais



Sobre o Projeto
Esse projeto foi feito na linguagem PHP, utilizando o conceito de MVC com codeigniter + ORM (do pr�prio Codeigniter).
Pensamos em utilizar a arquitetura ORM com Doctrine mas achamos melhor a integra��o com o pr�prio Codeigniter.

Requisitos
Sistema Operacional: Windows ou Linux
Servidor Apache: 2.2.x
Banco de Dados MySql: 5.5.8
PHP: 5.3.5

Qualquer m�quina que tenha processadores da  Intel, AMD e VIA. N�o necessita muito de um �timo processador.
256 Mem�ria RAM - 50 Megas de HD


Organiza��o das Pastas
As pastas est�o dividas da seguinte maneira.

Os controllers: sgri\application\controllers
Os Models: sgri\application\models
As Views: sgri\application\views

Acessos: sgri\application\libraries
Regras de Acesso ao Sistema: sgri\application\libraries\access_rule.php
ORM: sgri\application\libraries\query.php
Sess�es dos Usu�rios: sgri\application\libraries\sessoes.php

Tema da Aplica��o: sgri\theme\
css: sgri\theme\css
imagens: sgri\theme\images
Javascripts: sgri\theme\js

Configura��o de Roteamento, Banco de Dados e Configura��o Geral
Roteamento: sgri\application\config\routes.php
Banco de Dados: sgri\application\config\database.php
Configura��o Geral: sgri\application\config\config.php

HTACCESS.
O arquivo HTACCESS precisa ser modificado caso o diret�rio padr�o da aplica��o seja diferente de SGRI.
O padr�o est� configurado como SGRI. Caso for instalar o sistema em outro diret�rio, modifique as linhas necess�rias dentro do arquivo HTACCESS para o diret�rio desejado. N�o esque�a de abrir o arquivo sgri\application\config\config.php 
e
na linha 17 [ $config['base_url']] colocar a URL completa.






Mod_rewrite
O sistema precisa rodar com um m�dulo do Apache Ligado(ON). 
Chamado: MOD_REWRITE
Abr� o arquivo de configura��o do APACHE (httpd.conf) e procure a linha chamada
;LoadModule rewrite_module modules/mod_rewrite.so
Basta tirar o ponto e v�rgula do in�cio(;) e reiniciar o apache novamente:
Linux: sudo /etc/init.d/apache2 restart
Pronto: O sistema est� apto a rodar sem problemas.

Exporta��o Banco de Dados
Na pasta Raiz existe um arquivo Chamado: sgri.sql.
Esse arquivo cont�m o banco de dados completo do sistema.
Voc� poder� exportar para dentro do seu Banco MySql.
Fa�a login em seu MYSQL, crie um banco de dados chamado "sgri" e logo depois exporte o arquivo sgri.sql para dentro do banco de dados criado.
Caso opte por outro nome de outro banco de dados, n�o esque�a de reconfigurar o arquivo sgri\application\config\database.php
para as novas configura��es.
