# Loops

Os loops ou laços de repetição, são estruturas que o proprio nome explica, estruturas para a repetição de um bloco de código, nestemódulo falaremos de algumas dessas estruturas, como o for e o while.

## FOR

Este laço de repetição tem sua sintaxe bem simples e é uma estrutura muito utilizada.

```

<?php

$a = [1,3,5,7,9,33,66];

for($i = 0; $i < count($a); $i++){ // o for é composto por 3 partes, a primeira parte é a declaração e inicialização 
                                   // da variável que será nosso indice atual, a segunda parte é a operação lógica que
                                   // validará se o laço será executado ou não e a teceira parte é o incremento do nosso 
                                   // indice.
    echo($a[$i]);
}


?>
```

## FOREACH

No caso do foreach sua sintaxe é um pouco mais simples do que o for, acompanhe no exemplo.

```
<?php

$a = [1,3,5,7,9,33,66];

foreach($a as $item){ // Nesta estrutura teremos duas variáveis o array e o iterator que é a variável que iremos iteragir
    echo($item);
}

?>

```

## CONTINUE

O continue é uma função que pode ser usada em qualquer estrutura de repetição para saltar a repetição atual,
vamos observar no exemplo anterior como ele ficaria com um continue para saltar algum item do array.


```
<?php

$a = [1,3,5,7,9,33,66];

foreach($a as $item){ 
    if($item == 9){
        continue; // Neste caso o código irá pular o item com valor 9
    }
    echo($item);
}

?>

```

## WHILE

Quando estamos trabalhando com o while(enquanto) temos que ficar atentos em algumas coisas como sempre incrementar o nosso 
contador e também definirmos uma condição para o final do laço, ao contrário podemos correr um grande risco de ficarmos 
em uma repetição infinita, abaixo vamos ver alguns exemplos de laço while.

```
<?php

$a = [1,3,5,7,9,33,66];
$c = 0; // Contador

while($c < count($a)){ // Definindo a condição de enquanto o nosso contador for menor que o tamanho do array
    echo($a[$c]); // Será escrito o valor de array na posição em que estiver nosso contador
    $c++; // ao final do bloco de código é feito o incremento do nosso contador, sem este incremento ficaremos prezos em um 
          // laço infinito de repetição
}

while(1==1){ // Este é um exemplo clássico de laço infinito
    echo("Eu sou um laço infinito!");
}


```

## DO-WHILE

Assim como o while o do-while(faça enquanto) é uma estrutura que necessita de um contador e sempre executará ao menos uma
vez e ao final da execução fará a validação da condição de execução do laço e como o while também existe o risco de cairmos 
em um laço infinito caso a expressão sempre reotne verdadeiro.

```
<?php

$a = [1,3,5,7,9,33,66];
$c = 0; // Contador

do{
    echo($a[$c]);
    $c++;
}while($c < count($a));

```

Vá para [Sessão 05-Classes-e-Funções](../05-Classes-e-Funções/README.md).