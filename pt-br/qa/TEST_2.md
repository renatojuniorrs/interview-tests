## 🧪 Exercício de QA - Validação da Função Fibonacci (Javascript Node)

### Objetivo

Testar uma função pronta que calcula o n-ésimo número da sequência de Fibonacci e identificar se ela está correta e robusta.

Abaixo está uma função Javascript chamada `fibonacci(int n)` que retorna o n-ésimo número da sequência de Fibonacci.

Você **não precisa implementar** a função — ela já está feita.
Seu papel é atuar como **QA**, criando testes e validando se a implementação está correta, cobrindo:

* Casos comuns
* Casos de borda (como `n = 0` ou `n` negativo)
* Casos maiores (performance e limites)

---

### Ambiente de Teste

Recomenda-se usar o compilador online:
👉 [https://www.onlinegdb.com/](https://www.onlinegdb.com/)

---

### Código fornecido

Copie e cole este código no editor para começar:

```javascript
function fibonacci(n) {
    if (n <= 0) return 0;
    if (n === 1) return 1;

    let a = 0;
    let b = 1;
    let result = 0;

    for (let i = 2; i <= n; i++) {
        result = a + b;
        a = b;
        b = result;
    }

    return result;
}

// Função de testes
function testFibonacci() {
    console.log("Teste aqui");
}

// Execução
testFibonacci();

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

