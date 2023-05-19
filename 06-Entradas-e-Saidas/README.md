# Introdução

As entradas e saídas são os pontos de interação com o frontend ou com outro programa ou até mesmo diretamente com o usuário,
neste módulo vamos conhecer e explorar alguns desse pontos.

## Entradas

Quando estamos desenvolvendo para web exite alguns jeitos de conseguir-mos captar as informações de input, abaixo podemos
observar alguns desses métodos.

- GET - este tipo de input quem estiver consumindo a api deve enviar os parametros na URL junto ao caminho para o arquivo. 

```
<?php

#http://localhost/teste.php?teste=estudandoPHP - Assim é enviado algum parametro via GET

$parametro = $_GET["teste"]; // para ser captado o valor do parametro GET devemos utilizar a variável global $_GET

?>
```

- POST - Diferente do GET os parametros e valores não ficam a vista do usuário, estes dados vão junto ao cabeçalho da requisição.

```
<?php

# curl -X POST -d "teste=estudandoPOST" http://localhost/teste.php // Este é um exemplo de uma requisição 

$parametro = $_POST["teste"]; // No caso do POST é usado a variável $_POST.

?>
```

- BODY - Uma outra maneira de se enviar dados sem elas ficarem visiveis para o usuário comum é enviar um json no corpo da requisição.

```
<?php

# curl -X POST --data-raw '{"teste":"estudandoPOST"}' http://localhost/teste.php

$input = file_get_contents("php://input"); // Metodo de como capturar os dados enviados no corpo da requisição.

?>

```

- HEADER - Outra forma de enviar dados para o servidor e que não ficam visiveis para o usuário final.

```
<?php

# curl -X POST --header "teste=testeDeDadosNoHeader" http://localhost/teste.php

$header = $_SERVER["teste"];

?>

``` 

- SYSARGS - E por ultimo temos os arqgumentos do sistema.

```
<?php

# php teste.php arg1 arg2

$primeiroArgumento = $argv[1];
$segundoArgumento  = $argv[2];

?>

```

## Saídas

Quando estamos programando podemos escrever o resultado do programa em três lugares, podemos escrever como retorno na web,
no caso em que o código estará em um servidor web ou no terminal caso o código esteja rodando via CLI ou em um arquivo,
abaixo poderemos ver alguns exemplos das duas maneiras.

- Web/Terminal - Para essas duas opções basta chamar a função **echo** ou a função **print_r** 

  - ##### echo
  Esta função é utilizada para mostrar strings no terminal ou na web

  - ##### print_r
  esta função também é utilizada para mostrar strings no terminal e na web mas não somente strings como o echo mas tambem qualquer 
  objeto como arrays.

- Arquivo - Para a utilização da saida em aruivos temos que entender como trabalhar com arquivos.
  
  - Modos de abertur de arquivo.
  Existem vários modos de se abrir um arquivo em php, mas os mais utilizados são:
    - w - Este modo nós conseguimos criar/escrever em um arquivo, toda vez que um arquivo é aberto com este modo ele é sobrescrito.
    - r - Ao utilizar este modo é possível ler o conteudo do arquivo contudo não é possível modificar o conteudo do mesmo.
    - a+ - Este é o modo de abertura de arquivo que eu mais uso, pois com ele é possível ler, criar e adicionar ao final do arquivo.
  
  ```
    <?php

    $arq = fopen("teste.txt","a+"); // Nesta linha é feito a abertura do arquivo em modo "a+".
    fwrite($arq, "teste de texto"); // Aqui estamos escrevendo no final do arquivo.
    fclose($arq);                   // Nesta ultima linha estamos fechando o handle do arquivo.

    ?>
  ```
  - Funções para manipulação de arquivos:
  Em PHP temos várias formas de manipular um arquivo, abaixo eu tratarei duas maneiras com funções diferentes.

    - Primeiramente temos as principais funções:
      - fopen - Esta função é utilizada para abrir o arquivo e retorna um handle do arquivo que será utilizado para a manipulação.
      - fwrite - Com esta função nós conseguimos escrever strings dentro do arquivo.
      - fread - Utilizamos esta função para capturar/ler os dados do arquivo.
      - fclose - O fclose é utilizado para finalizar o handle do fopen e liberar o arquivo.
    - Agora o meu metodo amsi utilizado:
      - file_get_contents - Esta função lê todo o arquivo e retorna o conteudo como string.
      - file_put_contents - Esta função cria/escreve em arquivos, para escrever no fim do arquivo esta função depende da flag FILE_APPEND
    
    ```
    <?php
    
    $arq = fopen("arq.txt","a+");
    fwrite($arq, "Escrevendo em arquivo com fwrite"); // Exemplo de escrita em arquivo
    fclose($arq);

    $arq = fopen("arq.txt","a+");
    $conteudo = fread($arq,4098); // Lendo 4098 bytes do arquivo e escrevendo na tela
    echo($conteudo);
    fclose($arq);

    file_put_contents("arq2.txt","Escrevendo em arquivo com file_put_contents"); // Exemplo de escrita em arquivo
    $conteudo = file_get_contents("arq2.txt"); // Exemplo de leitura de arquivo
    echo($conteudo);

    ?>

    ```

Vá para [Sessão 07-Includes-e-Requires](../07-Includes-e-Requires/README.md).