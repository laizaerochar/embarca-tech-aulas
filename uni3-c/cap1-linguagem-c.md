## Linguagem C (Unidade 3)

# 1. Lógica de Programação e Algoritmos
A construção de um software eficiente segue um método de análise dividido em três fases fundamentais:
* **Dados de Entrada:** Definição do que o programa irá receber
* **Processamento:** Ações e cálculos realizados sobre as entradas
* **Saída:** O resultado final apresentado ao usuário

---

# 2. Estrutura de um Programa em C
A organização hierárquica é essencial para a compilação e execução correta do código

### Componentes Gerais:
* **Diretivas de Pré-processador:** Instruções processadas antes da compilação (ex: `#include <stdio.h>`)
* **Variáveis e Constantes:** Espaços de memória para armazenar valores
* **Funções:** Blocos de código que realizam tarefas específicas
* **Bloco Principal (`main`):** O ponto de entrada onde a execução começa

---

# 3. Tipos de Dados e Variáveis
C é uma linguagem de **tipagem estática**, onde o tipo de valor deve ser declarado

| Tipo | Descrição | Exemplo de Uso |
| :--- | :--- | :--- |
| `char` | Armazena caracteres individuais. | `char inicial = 'L';` |
| `int` | Armazena números inteiros. | `int idade = 22;` |
| `float` | Ponto flutuante (números decimais). | `float nota = 9.5;` |
| `double` | Ponto flutuante com maior precisão. | `double pi = 3.14159265;` |

### Modificadores de Tipo:
* `signed`/`unsigned`: Controlam se o valor aceita sinais negativos
* `const`: Define valores fixos que não podem ser alterados
* `static`: Mantém o valor da variável entre chamadas de funções

---

## 4. Entrada e Saída (I/O)
A interação com o usuário é feita principalmente através da biblioteca `stdio.h`

* **`printf` (Saída):** Exibe informações formatadas na tela
* **`scanf` (Entrada):** Coleta dados inseridos pelo usuário através de endereços de memória (`&`)
### Formatadores Comuns:
* `%d`: Inteiro decimal
* `%f`: Ponto flutuante
* `%s`: String (texto)
* `\n`: Nova linha

---

## 5. Estruturas de Controle e Repetição
Controlam o fluxo de execução do programa com base em condições lógicas

### Controle de Fluxo:
* **`if...else`**: Executa um bloco se a condição for verdadeira; caso contrário, executa o `else`
* **`switch...case`**: Seleciona um bloco de código entre várias opções possíveis
### Laços de Repetição:
* **`while`**: Repete enquanto a condição for verdadeira (pré-validação)
* **`do-while`**: Executa o código ao menos uma vez antes de validar a condição
* **`for`**: Estrutura simples para repetições com limites definidos (inicialização; condição; incremento)

---

## 6. Funções e Structs
Conceitos avançados para organização e criação de tipos personalizados.

* **Funções:** Proporcionam modularidade, reusabilidade e melhor legibilidade do código
* **`struct`:** Permite agrupar diferentes tipos de dados em uma única unidade (ex: dados de um aluno)
* **`typedef`:** Define novos nomes para tipos de dados já existentes

---
