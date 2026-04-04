## Bibliotecas e Documentação (Unidade 3 - Cap. 4)

# 1. Bibliotecas em C
Bibliotecas são coleções de arquivos que contêm funções e definições pré-escritas, permitindo a reutilização de código e a modularização de sistemas complexos, evitam que o programador precise "reinventar a roda" para tarefas comuns

### Tipos de Bibliotecas:
* **Bibliotecas Estáticas (`.lib`, `.a`):** O código da biblioteca é copiado para dentro do executável final durante a compilação
* **Bibliotecas Dinâmicas (`.dll`, `.so`):** O código permanece em um arquivo separado e é carregado apenas quando o programa é executado, economizando memória e espaço

---

# 2. Bibliotecas Padrão (C Standard Library)
A linguagem C fornece um conjunto essencial de funções através de arquivos de cabeçalho (`.h`)

| Cabeçalho | Descrição | Principais Funções |
| :--- | :--- | :--- |
| `<stdio.h>` | Entrada e saída padrão | `printf`, `scanf`, `fopen` |
| `<stdlib.h>` | Utilidades gerais e gestão de memória | `malloc`, `free`, `exit` |
| `<math.h>` | Operações matemáticas avançadas | `pow`, `sqrt`, `sin`, `cos` |
| `<string.h>` | Manipulação de cadeias de caracteres | `strcpy`, `strlen`, `strcat` |
| `<time.h>` | Manipulação de data e hora | `time`, `clock`, `ctime` |



---

# 3. Criação de Bibliotecas Próprias
Para organizar projetos grandes, o desenvolvedor pode criar suas próprias bibliotecas dividindo o código em três partes:

1.  **Arquivo de Cabeçalho (`.h`):** Contém as assinaturas das funções e definições de constantes (a "interface")
2.  **Arquivo de Implementação (`.c`):** Contém o código real das funções
3.  **Programa Principal (`main.c`):** Utiliza a diretiva `#include "minha_bib.h"` para acessar as funcionalidades

---

# 4. Documentação de Software
A documentação é o registro detalhado de como o sistema funciona, sendo vital para a manutenção e colaboração

* **Importância:** Facilita a compreensão do código por outros desenvolvedores e ajuda a equipe a manter o projeto a longo prazo
* **Documentação Interna:** Comentários inseridos diretamente no código-fonte
* **Documentação Externa:** Manuais de usuário, guias de instalação e referências de API (como arquivos README no GitHub)

---

# 5. Ferramentas de Documentação (Doxygen)
O **Doxygen** é a ferramenta padrão de mercado para gerar documentação automática a partir de comentários estruturados no código

* **Funcionamento:** Ele extrai informações de comentários que utilizam tags específicas (como `@brief`, `@param`, `@return`)
* **Saída:** Pode gerar manuais em formatos HTML, PDF ou LaTeX
* **Benefício:** Mantém a documentação sempre sincronizada com a versão mais recente do código

---

## 6. Boas Práticas de Documentação
Para garantir uma documentação de qualidade, deve-se:
* Descrever o propósito de cada função e módulo
* Explicar claramente os parâmetros de entrada e os valores de retorno
* Manter a documentação atualizada conforme o código evolui
* Utilizar ferramentas de versionamento (como Git) para gerenciar também os arquivos de documentação

---
