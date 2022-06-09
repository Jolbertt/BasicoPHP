# Introdução

Neste módulo falaremos sobre os operadores lógicos e o operador tenário e também sobre estruturas de controle de fluxo como o if.

## Operadores


Os operadores são simbolos utilizados para comparações, tomada de decisões, atribuição, operações aritiméticas dentre outras coisas durante a execução do código, abaixo podemos ver algumas listas dos operadores lógicos mais usados.

### Operadores lógicos

| Exemplo   | Nome                  | Descrição                                                   |
|-----------|-----------------------|-------------------------------------------------------------|
|  $a or $b |    or, \|\| - OU      | Verdadeiro se $a ou $b são verdadeiros.                     |
| $a and $b |  and, && - E lógico   | Verdadeiro se tanto $a quanto $b são verdadeiros.           |

### Operadores de Comparação

| Exemplo   | Nome                  | Descrição                                                   |
|-----------|-----------------------|-------------------------------------------------------------|
|  $a > $b  |   > - Maior que       | Verdadeiro se o primeiro valor é maior que o segundo.       |
|  $a >= $b |   >= - Maior igual    | Verdadeiro se o primeiro valor é maior ou igual ao segundo. |
|  $a < $b  |   < - Menor que       | Verdadeiro se o primeiro valor é menor que o segundo.       |
|  $a <= $b |   <= - Menor igual    | Verdadeiro se o primeiro valor é menor ou igual ao segundo. |
|  $a == $b |   == - Igual          | Verdadeiro se $a e $b forem iguais.                         |
| $a === $b |  === - Igual          | Verdadeiro se $a e $b forem iguais de valor e tipo.         |
|  $a != $b |  !=, <> - Diferente   | Verdadeiro se $a e $b forem diferentes.                     |
| $a !== $b |  !== - Igual          | Verdadeiro se $a e $b forem diferentes de valor e tipo.     |

### Operadores Aritméticos

| Exemplo   | Nome                  | Descrição                  |
|-----------|-----------------------|----------------------------|
|  $a - $b  |       Subtração       | Diferença entre $a e $b.   |
|  $a + $b  |         Adição        | Soma de $a e $b.           |
|  $a / $b  |       Subtração       | Quociente de $a e $b.      |
|  $a * $b  |     Multiplicação     | Produto de $a e $b.        |

### Operadores de Atribuição

O operador básico de atribuição é o = (igual) e dele divergem vários outros para manipulação de variáveis inteiras ou strings, acompanhe abaixo laguns trechos de código que exemplificam algumas dessas manipulações.

```
<?php

$a = 5; // A variável $a recebe o valor 5

$a += 4; // com essa modificação o valor da variável vai para 9 pois é como se fosse somado 4 ao valor já existente na variável;

$a -= 3; // após esta modificação a variável $a passa a conter o valor 6 pois o 3 é subitraído da variável $a que está com o valor 9 após a soma da ultima operação.

$b = "Hello"; // neste exemplo a variável $b está recebendo uma string

$b .= " World"; // Este operador irá concatenar (juntar) a string " World" ao final da string já existente na variável e após esta operação o valor de $b será "Hello World"

?>

```

### Operadores de Incremente e Decremento

Em PHP temos operadores de pre incremento e Pós incremento como em C, a seguir você poderá ver uma tabela de exemplo:

| Exemplo  | Nome                  | Descrição                                  |
|----------|-----------------------|--------------------------------------------|
|   ++$a   |    Pré incremento     | Incrementa $a em um, e então retorna $a.   |
|   $a++   |    Pós-incremento     | Retorna $a, e então incrementa $a em um.   |
|   --$a   |    Pré-decremento     | Decrementa $a em um, e então retorna $a.   |
|   $a--   |    Pós-decremento     | Retorna $a, e então decrementa $a em um.   |


Vá para [Sessão 02-Operadores-e-Controle-de-Fluxo](../03-Controle-de-fluxo/README.md).