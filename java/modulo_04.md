# Loops e Arrays

## Loops

### While

`while` loops allow you to repeat an `if` condition over and over for as long as that condition remains `true`, hence the name `while`!

To create a `while` loop, simply follow the same steps like an `if` condition, but replace the `if` with a `while` to look something like this:

```java
while(condition){
    <code>
}
```

Na função acima, enquanto a condição `condition` for `true`, o código `<code>` continuará a ser executado até que a variável `condition` tenha seu valor `false`. Dessa forma, é essencial que a variável `condition` seja constantemente testada dentro do loop para que o mesmo não se torne um loop infinito no caso da variável não ser mais testada e, portanto, manter a condição `true` indefinidamente.

Exemplo

```java
while(isRaining){
   System.out.println("It's still raining outside!");
   isRaining = checkWeather();
}
System.out.println("Now it's not raining anymore");
```

This code block above will continue to print the message "It's still raining outside!" for as long as the boolean isRaining is true, once the function checkWeather() returns false isRaining will no longer be true, so the while loop would end and the message "Now it's not raining anymore" will be displayed.

Unlike if blocks however, while loops don't have else blocks, they are simply like a repeated if block that would only end when the condition becomes false.

#### Incremento

É comum ocorrer a necessidade de realizar contagens dentro de um loop para que ele se repita apenas uma determinada quantidade de vezes. Para tal, é possível realizar um incremento a cada iteração do loop, da seguinte forma.

```java
public void countOnLoop(int numOfCount) {
    int i = 1; // Contador do loop
    while (i<= numOfCount) { // Condição de teste do lop
        System.out.println("Contador: " + i);
        i++; // Incremento do loop em 1 unidade
    }
}
```

Existe um tipo de loop que realiza essa função de realizar um incremento a cada iteração, sendo esse o loop `for`.

### For

[Java docs: for Statement](https://docs.oracle.com/javase/tutorial/java/nutsandbolts/for.html)

> *The for statement provides a compact way to iterate over a range of values. Programmers often refer to it as the "for loop" because of the way in which it repeatedly loops until a particular condition is satisfied. The general form of the for statement can be expressed as follows:*

```java
for (initialization; termination; increment) {
    statement(s)
}
```

> When using this version of the for statement, keep in mind that:
>
> - The initialization expression initializes the loop; it's executed once, as the loop begins.
> - When the termination expression evaluates to false, the loop terminates.
> - The increment expression is invoked after each iteration through the loop; it is perfectly acceptable for this expression to increment or decrement a value.

### Contadores (*loop counters*)

É importante não modificar o valor do contador/iterador dentro do loop, pois essa alteração provavelmente vai quebrar o loop, uma vez que a variável será atualizada no loop e na própria iteração do `for`.

Nesse caso, é recomendado que seja atribuído o valor alterado do contador em uma nova variável. Dessa forma, o contador seguirá sendo incrementado pelo loop sem problemas.

Também é possível realizar operações no contador sem problemas, desde que seu valor não seja atualizado. Por exemplo, printar um contador multiplicado por uma constante. Embora o valor printado seja um produto do contador, a variável do contador não tem seu valor atualizado.

#### Observação

O contador nem sempre precisa conter um incremento positivo, como `i++`. Dessa forma, é possível realizar um incremento negativo como `i--`, onde o valor de `i` será subtraído de 1 a cada iteração do loop.

Além disso, nem sempre o incremento precisa ser unitário. Além disso, podem ser utilizadas outra operações além de soma e subtração. Assim, é possível realizar incrementos com funções de multiplicação, divisão, etc.

A seguir, alguns exemplos de contadores:

- `i++`
- `i--`
- `i /= N`: nesse caso, o valor de `i` será dividido por N a cada iteração
- `i *= N`: nesse caso, o valor é multiplicado por N a cada iteração

### `break`

O statement `break` encerra um loop. Dessa forma, pode ser bastante útil para ser usado em um teste de condição em que o loop deve ser encerrado.

Dessa forma, ao ser utilizado dentro de um loop, ele pode ser inserido dentro do código de um `if` positivo, de forma que será executado após um teste onde a condição "bateu" e, portanto, o loop deve ser encerrado.

Exemplo - `for`:

```java
int i = 0;
for (i=0; i<=10; i++) {
    if (i == 5) {
        System.out.println("Condição de teste estabelecida. Saindo do loop...");
        break;
    }
}
```

## Arrays

[Java Docs - arrays](https://docs.oracle.com/javase/tutorial/java/nutsandbolts/arrays.html)

- Permite o armazenamento de diversas variáveis de um mesmo tipo em uma mesma variável.
- O array é indexado com números para cada item da estrutura, inciando em 0, denominado "index" do array
- Cada item dentro de um array é denominado "célula"
- O array tem um tamanho (qtd. de células) fixo e esse valor deve ser declarado na criação da variável (declaração do array)

Declarando um array, onde `type` é o tipo de dado que o array vai armazenar, e `[]` indica que é um array sendo criado:

```java
type[] nameOfArray;
```

Dessa forma, a variável foi declarada e poderá ser inicializada, alocando a quantidade de elementos dele:

```java
nameOfArray = new type[length]
```

Onde `nameOfArray` é o array inicializado, `new` é o operador que cria o array de fato, e `length` é o número de elementos que o array deve armazenar (quantidade de células).
