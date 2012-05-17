Trabalho de Projeto de Sistemas
Autores
Diego Rodrigues|Graziella Arca|Leonardo Miyamoto

Professor(a): Maria Augusta
Email: psi.si.puc@gmail.com

/*************************************************************************/

GRUPOS
Projetos de Sistemas de Informação
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
Esse projeto foi feito na linguagem PHP, utilizando o conceito de MVC com codeigniter + ORM (do próprio Codeigniter).
Pensamos em utilizar a arquitetura ORM com Doctrine mas achamos melhor a integração com o próprio Codeigniter.

Requisitos
Sistema Operacional: Windows ou Linux
Servidor Apache: 2.2.x
Banco de Dados MySql: 5.5.8
PHP: 5.3.5

Qualquer máquina que tenha processadores da  Intel, AMD e VIA. Não necessita muito de um ótimo processador.
256 Memória RAM - 50 Megas de HD


Organização das Pastas
As pastas estão dividas da seguinte maneira.

Os controllers: sgri\application\controllers
Os Models: sgri\application\models
As Views: sgri\application\views

Acessos: sgri\application\libraries
Regras de Acesso ao Sistema: sgri\application\libraries\access_rule.php
ORM: sgri\application\libraries\query.php
Sessões dos Usuários: sgri\application\libraries\sessoes.php

Tema da Aplicação: sgri\theme\
css: sgri\theme\css
imagens: sgri\theme\images
Javascripts: sgri\theme\js

Configuração de Roteamento, Banco de Dados e Configuração Geral
Roteamento: sgri\application\config\routes.php
Banco de Dados: sgri\application\config\database.php
Configuração Geral: sgri\application\config\config.php

HTACCESS.
O arquivo HTACCESS precisa ser modificado caso o diretório padrão da aplicação seja diferente de SGRI.
O padrão está configurado como SGRI. Caso for instalar o sistema em outro diretório, modifique as linhas necessárias dentro do arquivo HTACCESS para o diretório desejado. Não esqueça de abrir o arquivo sgri\application\config\config.php 
e
na linha 17 [ $config['base_url']] colocar a URL completa.






Mod_rewrite
O sistema precisa rodar com um módulo do Apache Ligado(ON). 
Chamado: MOD_REWRITE
Abrá o arquivo de configuração do APACHE (httpd.conf) e procure a linha chamada
;LoadModule rewrite_module modules/mod_rewrite.so
Basta tirar o ponto e vírgula do início(;) e reiniciar o apache novamente:
Linux: sudo /etc/init.d/apache2 restart
Pronto: O sistema está apto a rodar sem problemas.

Exportação Banco de Dados
Na pasta Raiz existe um arquivo Chamado: sgri.sql.
Esse arquivo contém o banco de dados completo do sistema.
Você poderá exportar para dentro do seu Banco MySql.
Faça login em seu MYSQL, crie um banco de dados chamado "sgri" e logo depois exporte o arquivo sgri.sql para dentro do banco de dados criado.
Caso opte por outro nome de outro banco de dados, não esqueça de reconfigurar o arquivo sgri\application\config\database.php
para as novas configurações.
