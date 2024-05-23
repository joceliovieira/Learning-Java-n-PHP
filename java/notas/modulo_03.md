# Funções

- Organiza e agrupa código
- Executa uma tarefa específica

## Definição de uma função

A definição de uma função ocorre da seguinte forma:

```java
<access_modifier> <return_type> <func_name>(<arguments>) {
    <code_block>
}
```

A declaração de uma função é iniciada com um modificador de acesso (*access modifier*) - `public` ou `private`.

Em seguida, é definido o tipo de retorno da função (*return type*), que define justamente o comportamento da função com relação ao que ela retorna. No caso de não haver retorno, como uma função que apenas realiza prints, define-se o tipo de retorno `void`.

Depois, surge o nome da função e o bloco de código.

Exemplo:

```java
public void func_name(arguments) {
    <func_code>
}
```

## Parâmetros e Argumentos

Os parâmetros de entrada de uma função devem ser declarados na própria declaração da função em `func_name(arguments)` junto ao seu tipo - exemplo: `public void checkName(String name) {...`.

Ao chamar uma função e passar uma variável para a mesma, essa variável passa a ser chamada de argumento da função.

A definição de parâmetro de uma função é aquele objeto que é utilizado dentro da própria declaração da função. O argumento, por sua vez, é o valor real que é passado ao chamar uma função.

## Parâmetros Múltiplos

Para passar mais de um parâmetro em uma função, basta separá-los por vírgula na declaração da função.

Ao passar os argumentos quando chamar a função, eles serão associados na mesma ordem e tipo dos parâmetros que foram declarados na construção (declaração) da função. Isso significa que os argumentos devem ser ordenados de acordo com o que a função espera. Além disso, os argumentos passados devem ter os tipos de acordo, também, com o que já foi definido nos parâmetros da função.

## Return

Além de receber os parâmetros, uma função também pode devolver valores. Dessa forma, o return type dessa função que retorna valores não será mais o `void`, visto que esse é utilizado em uma função que não retorna nada.

Para definir uma função que retorne algum tipo de dado, basta passar o tipo no próprio return type, substituindo o anterior `void`, e incluir um return statement igual ao do Python, isto é, uma linha com `return <value>;`.

Exemplo:

```java
public String functionName( ) {
    <code>;
    return value;
}
```

## Usando função de uma "classe nativa"

### `Math.random()`

Class Math

> "*The class Math contains methods for performing basic numeric operations such as the elementary exponential, logarithm, square root, and trigonometric functions.*"

[Java Docs: Class Math](https://docs.oracle.com/javase/8/docs/api/java/lang/Math.html)

#### Usando a função para gerar números aleatórios

A função `Math.random()` retorna um decimal no intervalo $[0, 1)$ (inclui o zero, mas não inclui o 1).

```java
double random = Math.random();
```

Escalando o valor para um aleatório em $[0, 10)$:

```java
double random = Math.random();
randomTen = random * 10;
```

Transformando o resultado em um inteiro:

```java
double random = Math.random(); // Obtendo um número 
randomTen = random * 10; // Gerando o range em [0,10)
randomTen = (int) randomTen; // Casting (int) - transformando o tipo
```

#### Simulando resultados de dois dados

Obs.: ao realizar o casting na variável `randomShifted`, que tem range de 1 até 6.999... a parte decimal é ignorada, de forma que o range vá de 1 a 6, sem arredondar.

```java
public class Main
{
    public static int rollDice() {
        double randomSeed = Math.random();
        System.out.println("Random seed: " + randomSeed);
        double randomScaled = randomSeed * 6;
        System.out.println("Random scaled: " + randomScaled);
        double randomShifted = randomScaled + 1;
        System.out.println("Random shifted: " + randomShifted);
        int result = (int) randomShifted;
        System.out.println("Result: " + result);
        return result;
    }
    public static void main(String[] args) {
        int firstDice = rollDice();
        int secDice = rollDice();
        System.out.println("****************************************");
        System.out.println("First dice: " + firstDice);
        System.out.println("Second dice: " + secDice);
    }
}
```

## Java Documentation Comments

Existem diversas formas de documentar uma função, mas há um padrão para o Java.

```java
/** 
 * General description of a function.
 * 
 * @param a first input parameter, named a
 * @param b second parameter, named b
 * 
 * @return description of return value
*/
```
