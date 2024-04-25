# Funções

- Organiza e agrupa código
- Executa uma tarefa específica

## Definição de uma função

A definição de uma função ocorre da seguinte forma:

```java
public void func_name(arguments) {
    <func_code>
}
```

A declaração de uma função é iniciada com um modificador de acesso (*access modifier*) - `public` ou `private`.

Em seguida, é definido o tipo de retorno da função (*return type*), que define justamente o comportamento da função com relação ao que ela retorna. No caso de não haver retorno, como uma função que apenas realiza prints, define-se o tipo de retorno `void`.

Depois, surge o nome da função e o bloco de código.

```java
<access_modifier> <return_type> <func_name>() {
    <code_block>
}
```

## Parâmetros e Argumentos

Os parâmetros de entrada de uma função devem ser declarados na própria declaração da função em `func_name(arguments)` junto ao seu tipo - exemplo: `public void checkName(String name) {...`.

Ao chamar uma função e passar uma variável para a mesma, essa variável passa a ser chamada de argumento da função.

A definição de parâmetro de uma função é aquele objeto que é utilizado dentro da própria declaração da função. O argumento, por sua vez, é o valor real que é passado ao chamar uma função.
