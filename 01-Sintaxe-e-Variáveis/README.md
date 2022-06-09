# Introdução

Neste módulo falaremos sobre como funciona a sintaxe e as variáveis do PHP.

## Sintaxe

A sintaxe do PHP é bem semelhante à sintaxe de C/C++ com algumas peculiaridades como o início, todo início de script php deve iniciar com a declaração do marcador <?php e sendo opcional a declaração da marcação final do arquivo ?> como a parte do código a seguir.

Exemplo.php
```
<?php
echo("Hello World");  //Este exemplo sendo declarado o fim da parte de código 
?>
```

Exemplo2.php
```
<?php
echo("Hello World");  //Este exemplo não sendo declarado o fim da parte de código 

```

Os dois trechos de código gerarão o mesmo resultado.

Ainda falando de sintaxe toda linha deve ser finalizada com ";" assim como já citado em C/C++ as funções, classes, controles de fluxo e loops devem ser iniciados com { e finalizados com } e toda variável deve obrigatóriamente ser declarada com um $ (cifrão) antes de seu nome, como podemos observar no trecho de código a seguir:

```
<?php
$a = 1; // atribui o valor 1 à variável $a
$b = 2; // atribui o valor 2 à variável $b

if ($a > $b){ // verificação se $a é maior que $b
    echo("A é maior que B"); // escreve a string se $a for maio que $b
}else{
    echo("B é maior que A"); // escreve a string se $b for maior que $a
}

?>
```

No exemplo acima podemos perceber bem claramente como são feitas as declarações de variáveis, atribuição de valores e até mesmo um controle de fluxo com um if

## Variáveis

Em PHP não temos uma tipagem explicita das variáveis, os tipos que mais utilizaremos serão 7.

Quatro tipos de dados básicos:
- Integer - $a = 1
- Float - $a = 0.1
- String - $a = "Esta é uma string"
- boolean - $a = True

Dois tipos compostos:
- Array - $a = array()
- Object - $a = new mysqli()

Um tipo especial:
- null - $a = null

### Quoting

Nesta parte gostaria de abordar um pouco sobre as aspas ou quoting. Em PHP nós podemos usar as aspas para vários objetivos, seguem alguns exemplos:

```
<?php

$a = 1;
$b = 2;

echo("$a$b"); // Exemplo de concatenação de duas variáveis em uma string
echo($a . " - " . $b); // Aqui vemos uma concatenação das duas variáveis em um string com um hífen separando as duas (Muito utilizado para logs)
echo('$a$b'); // Neste exemplo será impresso $a$b e não seus valores

?>

```

Vá para [Sessão 02-Operadores-e-Controle-de-Fluxo](../02-Operadores-e-Controle-de-Fluxo/README.md).