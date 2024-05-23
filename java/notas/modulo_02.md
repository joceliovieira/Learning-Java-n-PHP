# Fluxo de Controle e Condicionais

## `if`

- Condição de teste: condição que é analisada em true/false
- `boolean` é uma boa escolha de variável para ser analisada numa condição de teste visto que ela só apresenta valores true/false.
- Para finalizar um statement `if` não é utilzado `;` ao fim do seu código. Isso ocorre porque dentro do if, há um bloco de código que é executado, então o if serve como um verificador da condição que executa o bloco de código que ele carrega entre as chaves.

### Formato

```java
if(condition) { // condition é a condição de teste
    <code>; // bloco de código a ser executado
    <code>; // bloco de código a ser executado
    <code>; // bloco de código a ser executado
} // sem necessidade de ;
```

## `else`

De forma complementar ao `if`, executa um bloco de código caso a verificação seja negativa (false).

### Formato

```java
if(condition) {
    <code>; // Code for true condition
} else {
    <code>; // code for false condition
}
```

## `else-if`

Ocorre no caso de haver mais de uma condição a ser verificada. Nesse caso, haverá uma verificação também de true/false, porém em uma segunda variável, de maneira incremental ao `if`/`else`.

Será executado apenas um bloco de código independente de quantas condições a ser verificadas.

O bloco de código a ser executado será aquele primeiro a ocorrer a condição true, ou então o else caso nenhuma condição de teste seja positiva.

### Formato

```java
if (condition01) {
    <code>;
} else if (condition02) {
    <code>;
}
else {
    <code>;
}
```

## Variable Scope

O escopo de uma variável é a definição do espaço/bloco de código onde ela pode ser utilizada. Isso significa que a variável só estará definida e poderá ser utilizada em seu escopo.

**Um conjunto de chaves `{ }` define o escopo de uma variável.**

### Exemplo

No exemplo abaixo, temos as variáveis `check` e `msg`.  

A variável `check` está contida no escopo "global" de todo o código, e pode ser acessada dentro ou fora da condição `if`.  
A variável `msg`, por sua vez, é declarada dentro da condição `if` e portanto só poderá ser usada no bloco de código do `if`.

```java
boolean check = true;

if(check) {
    String msg = "Print dentro do if";
    System.out.println(msg)
}
```

## Expressões Booleanas

Um booleano pode ser diretamente atribuído a uma variável (`boolean var = true;`) ou ser resultado de um teste comparativo, isso é, resultado de uma expressão booleana.

### Operadores booleanos

`<`, `>`, `<=`, `>=`, `==`, `!=`

## Operadores Lógicos

- AND: `&&`
- OR: `||`
- NOT: `!`

O operador NOT transforma um valor em seu oposto, de forma a negar aquela condição.

### Ordem de Operações

De forma análoga às operações aritméticas/matemáticas, os operadores booleanos também tem uma ordem de execução definida.

A ordem dos operadores é a seguinte:

1. NOT (`!`)
2. AND (`&&`)
3. OR (`||`)

Caso existam múltiplos operadores do mesmo tipo, então eles são executados na sequência natural da leitura (esquerda p/ direita).

Para alterar a ordem de execução dos operadores, pode-se utilizar de parênteses, que irão fazer com que o que esteja entre parênteses seja 'executado' primeiro.

### Lógica

#### NOT

O resultado será o valor booleano oposto ao da expressão.

|Expressão|Resultado|
|:--:|:--:|
|!(true)|false|
|!(false)|true|

#### AND

O resultado será true se as duas condições comparadas forem true.

|Expressão|Resultado|
|:--:|:--:|
|true && true|true|
|true && false|false|
|false && false|false|

#### OR

O resultado será true se pelo menos uma das condições comparadas for true.

|Expressão|Resultado|
|:--:|:--:|
|true \|\| true|true|
|true \|\| false|true|
|false \|\| false|false|

## Nested if statements (ifs aninhados)

No caso de haver múltiplas condições de testes que possa vir a tornar a implementação dessa lógica de comparação muito complexa, surge o que é chamado de *nested ifs* ou ifs aninhados, que é basicamente a compreensão de uma verificação if dentro de outro if.

Exemplo:
```java
if (cond1 && cond2) {
    System.out.println("Condição 1 e condição 2 check!")
    if (cond3) {
        System.out.println("Condição 3 check!")
    }
    else if (cond4) {
        System.out.println("Condição 4 check!")
    }
}
```

## `switch`

A expressão `switch` testa o valor de uma variável comparando-o a uma lista de possibilidades de valores.

O objetivo dessa expressão é realizar uma comparação de uma variável com diversos valores sem precisar fazer uma comparação por vez. Dessa forma, em vez de utilizar uma sequência de ifs para testar cada condição, o `switch` é capaz de realizar essa comparação apenas uma vez e, assim, ganhar tempo.

Para essa expressão `switch`, cada valor associado a um teste condicional é chamado de `case`.

### Formato

```java
switch(var) {
    case cond01: <code>;
        break;
    case cond02: <code>;
        break;
    case cond03: <code>;
        break;
    default : <code>;
        break;
}
```

Onde `var` é a variável a ser testada e `cond01`, `cond02` e `cond03` são os valores a serem testados.

Após uma condição positiva ser testada, então executa-se o código seguido pelo `break`, que encerra a verificação e executa o código após o bloco de código do próprio `switch`.

Caso não seja inserido o `break` após o bloco de código do case, o Java seguirá executando o código e realizando as demais verificações, incluindo o `default` ao fim do `switch` ou o próximo `break`.

Por fim, o bloco de código após o `default` será executado se nenhum dos teste anteriores for positivo (análogo ao `else`).
