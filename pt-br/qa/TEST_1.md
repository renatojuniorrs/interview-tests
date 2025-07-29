## 🧪 Exercício de QA - Validação da Função Fibonacci (Java)

### Objetivo

Testar uma função pronta que calcula o n-ésimo número da sequência de Fibonacci e identificar se ela está correta e robusta.

Abaixo está uma função Java chamada `fibonacci(int n)` que retorna o n-ésimo número da sequência de Fibonacci.

Você **não precisa implementar** a função — ela já está feita.
Seu papel é atuar como **QA**, criando testes e validando se a implementação está correta, cobrindo:

* Casos comuns
* Casos de borda (como `n = 0` ou `n` negativo)
* Casos maiores (performance e limites)

---

### Ambiente de Teste

Recomenda-se usar o compilador online:
👉 [https://www.onlinegdb.com/online\_java\_compiler](https://www.onlinegdb.com/online_java_compiler)

---

### Código fornecido

Copie e cole este código no editor para começar:

```java
public class Main {
    public static void main(String[] args) {
        testFibonacci();
    }

    // Função fornecida para teste
    public static int fibonacci(int n) {
        if (n <= 0) return 0;
        if (n == 1) return 1;

        int a = 0;
        int b = 1;
        int result = 0;

        for (int i = 2; i <= n; i++) {
            result = a + b;
            a = b;
            b = result;
        }

        return result;
    }

    // Função de testes (incompleta) - você deve completá-la!
    public static void testFibonacci() {
        // TODO: Adicione aqui os seus testes
        // Exemplo:
        System.out.println("fibonacci(5) = " + fibonacci(5)); // Esperado: 5
    }
}
```

---

### Tarefas do QA

1. **Crie múltiplos testes em `testFibonacci()`**, cobrindo:

   * Entradas normais (`fibonacci(0)` até `fibonacci(10)`)
   * Números negativos (`fibonacci(-1)`, `fibonacci(-5)`)
   * Valores grandes (`fibonacci(30)`, `fibonacci(50)`)
   * Consistência de resultados

2. **Verifique**:

   * A função retorna os valores corretos?
   * Ela trata bem entradas inválidas?
   * Há erros de performance, overflow ou comportamento inesperado?

3. **Documente** (em comentários ou fora do código):

   * Quais testes passaram
   * Quais testes falharam (se houver)
   * Possíveis melhorias ou bugs identificados

---

### Exemplo de Saída Esperada

```
fibonacci(0) = 0
fibonacci(1) = 1
fibonacci(2) = 1
fibonacci(5) = 5
fibonacci(10) = 55
fibonacci(-1) = 0
...
```

---

### 🎯 Desafio Extra (Opcional)

Implemente uma função `assertEqual(expected, actual, description)` para automatizar a verificação dos testes e melhorar a leitura dos resultados.

