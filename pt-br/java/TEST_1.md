## Função Fibonacci (Java)

### Objetivo

Implementar e testar uma função que retorna o n-ésimo número da sequência de Fibonacci.

### Descrição

Você deve completar a função `fibonacci(int n)` para retornar o valor correto da sequência de Fibonacci e criar uma função `testFibonacci()` para validar seu funcionamento com diferentes casos de teste.

A sequência de Fibonacci começa assim:

```
0, 1, 1, 2, 3, 5, 8, 13, 21, 34, ...
```

Ou seja:

* `fibonacci(0)` → 0
* `fibonacci(1)` → 1
* `fibonacci(2)` → 1
* `fibonacci(3)` → 2
* e assim por diante.

---

### Ambiente de Teste

Recomenda-se usar o compilador online em:
👉 [https://www.onlinegdb.com/online\_java\_compiler](https://www.onlinegdb.com/online_java_compiler)

---

### Casos de Teste Recomendados

| Entrada `n` | Saída esperada |
| ----------- | -------------- |
| 0           | 0              |
| 1           | 1              |
| 2           | 1              |
| 3           | 2              |
| 4           | 3              |
| 5           | 5              |
| 6           | 8              |
| 7           | 13             |
| 10          | 55             |

---

### Código Inicial (Boilerplate)

Copie e cole o código abaixo no editor Java do [OnlineGDB](https://www.onlinegdb.com/online_java_compiler) e complete a função `fibonacci` e a função de teste:

```java
public class Main {
    public static void main(String[] args) {
        testFibonacci();
    }

    // Função que retorna o n-ésimo número de Fibonacci (completar)
    public static int fibonacci(int n) {
        // TODO: Implementar lógica iterativa da sequência de Fibonacci
        return -1; // valor provisório
    }

    // Função de teste
    public static void testFibonacci() {

    }
}
```

---

### ✅ Critérios de Aceitação

* A função `fibonacci(int n)` deve ser **iterativa**, não recursiva.
* Todos os testes devem passar com as saídas corretas.
* O código deve compilar e rodar sem erros no OnlineGDB.


