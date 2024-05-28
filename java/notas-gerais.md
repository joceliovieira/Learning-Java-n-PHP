# Notas

- Java é *case sensitive*, isto é, sensível a letras maiúsculas/minúsculas
- As instruções de código devem finalizar com `;`

## Funções básicas

- Print: `System.out.println("Java Rocks!");`

## Erros

1. Syntax Error (compile-time errors)
   - Ocorre quando há violação das regras gramaticais do Java
   - Nesse, o código não chega nem a ser compilado
2. Runtime Error
   - Ocorre durante a execução do programa
   - Nesse, o programa quebra (*crash*)
3. Bugs
   - São considerados erros lógicos
   - Ocorrem no caso do programa não funcionar de maneira esperada, sem necessariamente quebrar a execução

## Debugging

O debug permite que todas as variáveis sejam visualizadas enquanto o programa é executado, facilitando o processo de verificação.

É possível parar o programa em uma determinada linha e após isso executar as seguintes linhas uma por uma. Para tal, basta adicionar um *breakpoint* na linha que deve ser pausada a execução. Após isso, deve-se executar o programa em modo debug para que seja realizar a execução linha a linha.

Além disso, é possível inserir mais de um breakpoint e executar os blocos de código entre eles, em vez de passar linha a linha.