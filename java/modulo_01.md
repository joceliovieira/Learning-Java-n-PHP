# Variáveis e Tipos

- Cada variável tem um nome e um 'valor' atribuído
- O 'valor' (objeto armazenado na variável) pode mudar, enquanto o nome da variável não muda
- Ao definir o tipo a ser armazenado na variável, a mesma só será capaz de armazenar objetos daquele tipo
- As variáveis devem ser declaradas antes de serem usadas com tipo definido e, de forma opcional, seu valor também pode ser atribuído na declaração;

## Variáveis Inteiras

É uma representação de um número inteiro.

Declaração

```java
int var_name;
```

Inicializando a variável e atribuindo-a um valor:

```java
var_name = 0;
```

Exemplo: considerando a quantiade de passageiros em um veículo

```java
passageiros = 0;
```

Atualizando a variável: basta atribuir um novo valor na variável, podendo ser utilizada a própria variável para tal.
> When changing a variable value, you could either set it to a new value all together, or update it based on its previous value.

```java
passageiros = passageiros + 2;
```

> Obs.: A possibilidade de atualizar o valor da variável com base nela mesmo, como no exemplo anterior, surge da forma que o computador executa o código. Primeiro, é realizada a execução da parte do lado direito da igualdade `passageiros + 2`. Após realizar tal operação, é atribuído o resultado à variável do lado esquerdo da igualdade.

## Strings

Declarando e inicializando/atualizando

- Representação: `String`
- Requisitos: o valor atribuído (caracteres) deve estar contido entre aspas duplas.

```java
String driver;
driver = "John";
```

> Obs.: a parte do código que armazena de fato o valor é chamada de variável (no caso, `driver`). A string de fato que fica entre aspas (`John`) é chamada de *string literal*.

Contando a quantidade de caracteres de uma string: `<var_name>.length()`

```java
String nome = "jocelio";
int len = nome.length();
System.out.println(nome);
System.out.println(len);
```

Convertendo todos os caracteres para maíusculo/minúsculo: `.toUpperCase()`, `.toLowerCase()`

```java
String upper = nome.toUpperCase();
String lower = nome.toLowerCase();
System.out.println(upper);
System.out.println(lower);
```

Concatenando strings

A concatenação pode ocorrer entre literais e/ou variáveis,

```java
String upper = nome.toUpperCase();
String lower = nome.toLowerCase();
String concatenadas = upper + " " + lower;
System.out.println(upper);
System.out.println(lower);
```

> No exemplo acima, temos duas variáveis e um literar (`" "`) concatenados.

## Nomes de Variáveis

É utilizado comumente, em Java, o padrão `lowerCamelCase` para atribuir nomes para as variáveis.

Nesse padrão, a primeira letra do nome da variável é sempre minúscula, enquanto, em caso de 'nome composto', as iniciais das demais palavras são maiúsuculas.

Exemplos:

- `apiResponseBody`
- `inputData`
- `driverFirstName`
- etc.
