# Loops

## While

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

### Incremento

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

## For

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

## Contadores (*loop counters*)

É importante não modificar o valor do contador/iterador dentro do loop, pois essa alteração provavelmente vai quebrar o loop, uma vez que a variável será atualizada no loop e na própria iteração do `for`.

Nesse caso, é recomendado que seja atribuído o valor alterado do contador em uma nova variável. Dessa forma, o contador seguirá sendo incrementado pelo loop sem problemas.

Também é possível realizar operações no contador sem problemas, desde que seu valor não seja atualizado. Por exemplo, printar um contador multiplicado por uma constante. Embora o valor printado seja um produto do contador, a variável do contador não tem seu valor atualizado.
