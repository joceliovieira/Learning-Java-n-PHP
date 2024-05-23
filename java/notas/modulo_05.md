# IntelliJ and Debugging

## Java Development Kit (JDK)

O JDK é um conjunto de ferramentas necessárias para executar código Java.

1. JavaRuntime Environment (JRE)
    Inclui todo o necessário para execução dos tipos e funções nativas, junto a uma máquina virtual que executa o Java - Java virtual Machine (JVM)
2. Compilador Java (javac)

De forma resumida, a interação entre esses componentes inicia-se com a escrita do código no host. Após isso, esse código é enviado ao compilador javac que transforma esse em código binário. Finalmente, o código compilado é executado na JVM.

## Executando Código Java

É necessário que o arquivo do código tenha o mesmo nome de sua classe 'mãe' pública.

No exemplo abaixo, o nome do arquivo deve ser `helloWorld.java`.

```java
public class helloWorld {
    public static void main(String[] args) {
        System.out.println("Hello world :)");
    }
}
```

- Para compilar o código: `javac helloWorld.java`
- Para executar o programa: `java helloWorld`

Caso sejam realizadas alterações no código, então o mesmo deve ser compilado novamente.
