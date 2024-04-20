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
