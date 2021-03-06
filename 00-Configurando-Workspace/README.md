# Início

Primeiramente faremos a configuração do nosso workspace para a utilização neste curso.

Utilizaremos o Ubuntu 20.04 PHP 7.4.3 e o apache 2.4.41

## Um pouco de história

O PHP como é conhecido hoje, é na verdade o sucessor para um produto chamado PHP/FI. Criado em 1994 por Rasmus Lerdof, a primeira encarnação do PHP foi um simples conjunto de binários Common Gateway Interface (CGI) escrito em linguagem de programação C. Originalmente usado para acompanhamento de visitas para seu currículo online, ele nomeou o conjunto de scripts de "Personal Home Page Tools" mais frequentemente referenciado como "PHP Tools." Ao longo do tempo, mais funcionalidades foram desejadas, e Rasmus reescreveu o PHP Tools, produzindo uma maior e rica implementação. Este novo modelo foi capaz de interações com Banco de Dados e mais, fornecendo uma estrutura no qual os usuários poderiam desenvolver simples e dinâmicas aplicações web, como um livros de visitas. Em Junho de 1995, Rasmus » liberou o código fonte do PHP Tools para o público, o que permitiu que desenvolvedores usassem da forma como desejassem. Isso permitiu - e encorajou - usuários a fornecerem correções para bugs no código, e em geral, aperfeiçoá-lo.(https://www.php.net/manual/pt_BR/history.php)

## Como baixar e fazer instalação dos pacotes

Neste curso utilizaremos um recurso do windows chamado wsl, onde atravez da loja da microsoft instalaremos uma vm ubuntu, e para isso basta seguir o passo a passo:

1 - Abra o menu iniciar e procure pelo aplicativo Microsoft Store.

2 - Após executar, ele abrirá uma tela com vários aplicativos, na barra de pesquisa procure por ubuntu e clique em adquirir (não se preocupe, esta função é gratuita).

3 - Depois de instalado, no menu iniciar procure pelo ubuntu, abra e execute os seguintes comandos:

3.1 - sudo apt update

3.2 - sudo apt install apache2 -y

3.3 - sudo apt install php php-mysql php-xml php-json libapache2-mod-php -y

3.4 - sudo rm /var/www/html/index.html

3.5 - echo "Curso PHP" > /var/www/html/index.php

4 - Quando acabar de executar os comandos, reinicie o computador para aplicação das configurações.

## Observações

Como estamos utilizando o linux, aqui vão alguns comandos que você precisará saber:

- sudo service apache2 restart - comando utilizado para reiniciar o apache

- sudo nano /var/www/html/caminho-do-arquivo.php - caso você precise editar algum dos arquivos via linux

- Para criarmos nossos arquivos para estudo utilizaremos o seguinte caminho - \\\\wsl.localhost\Ubuntu\var\www\html no qual é o caminho para o diretório raiz do nosso apache.

- Para testar-mos os códigos desenvolvidos basta criar o arquivo de exemplo na pasta especificada no caminho acima e acessar em seu browser favorito o link http://localhost/nome-do-arquivo.php 

Vá para [Sessão 01 - Sintaxe e Variáveis](../01-Sintaxe-e-Variáveis/README.md).