# Introdução

Agora falaremos um pouco sobre estruturas de tomada de decisão como o if e o switch.

## IF

O if é uma das estruturas mais importantes em linguagens de programação, pois ele te possibilita tomar decisão a partir de uma expressão lógica, a seguir podemos ver alguns exemplos de if/else, elseif e operador ternário.

```
<?php

$a = 10;
$b = 20;

// IF

if ($a > $b)
    echo("a é maior que b"); // Quando existe a necesidade de utilizar somente uma linha após a validação o uso de chaves se torna opcional

// IF/ELSE

if ($a < $b){ // Esta sem dúvidas é a forma mais comum do if que você encontrará, onde tem a operação lógica 
    echo("a é menor que b"); // a ação se o resultado da operação for verdadeiro 
}else{ // senão
    echo("a é maior que b"); // a ação se o resultado for falso
}

// IF/ELSEIF/ELSE

if ($a < $b){ // Esta forma também comum, quando precisamos de fazer outra validação caso do primeiro if retorne falso
    echo("a é menor que b");
}elseif($a == $b){ // Neste caso, esta é a segunda condição
    echo("a é igual b");
}else{ // Se as consições anteriores retornarem falso será executado o código contido no else
    echo("a é maior que b");
}

// Operador ternário ?

$c = $a == 10 ? $a + $b : $a - $b; // Neste caso o operador ternário ele funciona como um if de uma linha só, 
                                   // onde o primeiro campo antes da interrogação é a condição ($a == 10) que se 
                                   // for verdadeira executará o segundo campo ($a + $b) senão executará o terceiro 
                                   // campo ($a - $b);

?>
```

## Switch

O swtch se aplica em casos que seriam utilizados vários elseif ao invés disso podemos utilizar um switch 
com vários cases para que o código fique mais limpo e de fácil entendimento como o exemplo abaixo.

```
<?php

$a = 5;

if($a == 1){
    echo("a é igual a 1");
}elseif ($a == 2){
    echo("a é igual a 2");
}elseif($a == 3){
    echo("a é igual a 3");
}elseif($a == 4){
    echo("a é igual a 4");
}elseif($a == 5){
    echo("a é igual a 5");
}else{
    echo("a não está na lista ")
}

switch($a){ // nesta linha está a declaração do sitch e a variável que será avaliada
    case 1: // este é o primeiro case onde é verificado se a variável de foco é igual ao valor
        echo("a é igual a 1"); // Se verdadeiro ele executará o blóco de código 
        break; // ao fim da execução é necessário a utilização do break para que seja encerrado o switch
    case 2:
        echo("a é igual a 2");
        break;
    case 3:
        echo("a é igual a 3");
        break;
    case 4:
        echo("a é igual a 4");
        break;
    case 5:
        echo("a é igual a 5");
        break;
    default: // A definição default é opcional, se ela existir e todas as opções retornarem falso será executado o blóco de código contido na opção default e se ela não existir nada será executado e ele sairá do switch.
        echo("a não está na lista");
}

?>
```

Vá para [Sessão 04-Loops](../04-Loops/README.md).