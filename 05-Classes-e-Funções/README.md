# Introdução

## Funções

As funções são blocos de código que podem ser reutilizados várias vezes durante a execução do programa, e com isso ao 
invés do código ser reescrito basta executar a chamada da função e passar os parametros que o código será executado 
com base nos parametros passados, abaixo podemos observar alguns tipos de funções.

```
<?php

function primeira(){ // Este é o exemplo de uma função que não depende de nehum parametro para ser executada.
    echo("Eu sou uma função sem parametros!");
}

function segunda($a, $b){
    return $a + $b;  // Este exemplo é de uma função que recebe dois parametros e retorna a soma dos dois valores.
}

?>
```

As funções não se limitam a somente escrever textos ou fazer operações aritméticas, você pode desenvolver funções
do jeito que desejar, das mais básicas até as mais complexas, esta complexidade dependerá somente de você.

## Classes

A definição de uma classe começa com a palavra chave class, seguida do nome da classe, seguido de um par de chaves que englobam as definições de propriedades e métodos que pertencem à classe.

Abaixo podemos ver um exemplo de uma classe com suas propriedades e dois métodos.

```
<?php

class cliente {

    public $nome = "";
    public $idade = ""; // definição das propriedades
    public altura = "";

    public function mostraCliente(){ // Esta função escreve os dados alocados nas variáveis da instancia atual da classe
        echo("Nome: " . $this->nome . ", Idade: " . $this->idade . ", Altura: " . $this->altura . "\n");
    }

    public function limpaCliente(){ // Esta função volta o valor das variáveis para vazio
        $this->nome = "";
        $this->idade = "";
        $this->altura = "";
        echo("Variáveis resetadas!");
    }

}

$cli = new cliente(); // Instanciando a classe na variável $cli

$cli->nome = "Jolbertt"; //
$cli->idade = 29;        // Adicionando valor aos atributos da classe
$cli->altura = 1.83;     //

$cli->mostraCliente(); // Executando a primeira função da classe 

$cli->limpaCliente(); // Executando a segunda função para resetar os valores.

?>

```

Vá para [Sessão 06-Entradas-e-Saidas](../06-Entradas-e-Saidas/README.md).