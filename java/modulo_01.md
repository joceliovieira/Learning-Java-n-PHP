# Variáveis e Tipos

- Cada variável tem um nome e um 'valor' atribuído
- O 'valor' (objeto armazenado na variável) pode mudar, enquanto o nome da variável não muda
- Ao definir o tipo a ser armazenado na variável, a mesma só será capaz de armazenar objetos daquele tipo
- As variáveis devem ser declaradas antes de serem usadas com tipo definido e, de forma opcional, seu valor também pode ser atribuído na declaração;

## Variáveis Inteiras

É uma representação de um número inteiro.

### Declaração

```java
int var_name;
```

### Inicialização e atribuição de valores

```java
var_name = 0;
```

**Exemplo**: considerando a quantiade de passageiros em um veículo

```java
passageiros = 0;
```

### Atualizando uma variável (valor)

Atualizando a variável: basta atribuir um novo valor na variável, podendo ser utilizada a própria variável para tal.

> When changing a variable value, you could either set it to a new value all together, or update it based on its previous value.

```java
passageiros = passageiros + 2;
```

> Obs.: A possibilidade de atualizar o valor da variável com base nela mesmo, como no exemplo anterior, surge da forma que o computador executa o código. Primeiro, é realizada a execução da parte do lado direito da igualdade `passageiros + 2`. Após realizar tal operação, é atribuído o resultado à variável do lado esquerdo da igualdade.

## Strings

### Declaração, inicialização e atualização

- Representação: `String`
- Requisitos: o valor atribuído (caracteres) deve estar contido entre aspas duplas.

```java
String driver;
driver = "John";
```

> Obs.: a parte do código que armazena de fato o valor é chamada de variável (no caso, `driver`). A string de fato que fica entre aspas (`John`) é chamada de *string literal*.

### Métodos para Strings

#### Contando a quantidade de caracteres de uma string

Sendo `var` a variável:

```java
var.length()
```

##### Exemplo

```java
String nome = "jocelio";
int len = nome.length();
System.out.println(nome);
System.out.println(len);
```

#### Convertendo todos os caracteres para maíusculo/minúsculo

```java
var.toUpperCase()
var.toLowerCase()
```

##### Exemplo

```java
String upper = nome.toUpperCase();
String lower = nome.toLowerCase();
System.out.println(upper);
System.out.println(lower);
```

#### Concatenando strings

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

## Tipos

Referência: [Oracle Java Docs.: Primitive Data Types](https://docs.oracle.com/javase/tutorial/java/nutsandbolts/datatypes.html)

> *The Java programming language is statically-typed, which means that all variables must first be declared before they can be used. This involves stating the variable's type and name.*
> *A variable's data type determines the values it may contain, plus the operations that may be performed on it.*

Existindo diferentes tipos de dados para uma mesma classe de tipo (numéricos, strings, etc), e sendo necessário defini-lo na declaração da variável, então essa escolha é importante tendo impactos como: economia de memória, melhor desempenho de processamento, etc.  Portanto, é importante definir o melhor tipo de dado para a variável no momento de desenvolvimento do código.

### Números

- Short
  - Representação: `short`
  - Valor inteiro de 16 bits
  - Limite: -32768 $\rightarrow$ 32767 (equivale-se em $(\frac{2^{16}}{2}$)
  - Uso: pode ser utilizado para economizar memória em grandes arrays, em casos onde economia de memória é uma prioridade
- Inteiro (integer)
  - Representação: `int`
  - Limite: valor máximo limitado em $\plusmn{\frac{2^{32}}{2}}$ ou 2147483648 $\rightarrow$ 2147483647
- Long
  - Representação: `long`
  - É basicamente um inteiro maior, com 64 bits.
  - Limite: $-2^{63} \rightarrow 2^{63}-1$
- Float
  - Representação: `float`
  - É um valor do tipo ponto flutuante (número real) de single-precision, ocupando 32 bits
  - É um tipo de tamanho menor do que o `double`. Portanto, deve ser escolhido o `float` quando houver necessidade de otimização.
- Double
  - Representação: `double`
  - É um valor de ponto flutuante com double-precision
  - Possui maior tamanho do que o `float`, com 64 bits
  - Embora seja maior do que o `float`, ele é considerado o padrão para valores decimais

> Observação: Os tipos `float` e `double` **nunca** devem ser usados para representação de variáveis que necessitam de uma grande precisão, como valores de dinheiro e afins.

### Texto

- String
  - Representação: `String`
  - Seu valor deve ser contido em **aspas duplas**
- Char
  - Representação: `char`
  - Armazena um caracter único
  - Seu valor deve ser contido em **aspas simples**

### Booleano

- Booleano
  - Representação: `boolean`
  - É uma representação para true/false
  - Representa um bit de informação

## Aritmética

As operações aritméticas/matemáticas em Java são realizadas através de seus operadores comuns (+, -, *, /).

Entretanto, é importante fazer considerações sobre os tipos envolvidos nas operações.

Ao realizar uma operação entre 2 valores inteiros e armazenar esse resultado em um double ou float, o resultado não será um valor real (com decimal). Isso ocorre porque os 2 valores da operação são inteiros. Para que o resultado seja realmente um valor real (decimal), então pelo menos uma das 2 variáveis envolvidas na operação deve ser também `double`. Caso sejam 2 inteiros na operação, então o resultado, mesmo sendo armazenado em double ou float, será um valor inteiro.

## Casting (conversão)

Para realizar a conversão de um valor ou variável de um tipo para outro, então basta passar, antes do seu valor/variável, qual o tipo que ele deve ser convertido entre parênteses.

Exemplo: `double var = (double) 5/2`

## Comentários

Representações:

- Linha única: `//`
- Múltiplas linhas: início `/*` e fim `*/`
