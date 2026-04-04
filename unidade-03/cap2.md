# Ambiente de Desenvolvimento (Unidade 3 - Cap. 2)

# 1. Visual Studio Code (VS Code)
O VS Code é um editor de código leve, potente e multiplataforma,é a ferramenta principal para a escrita, depuração e integração de código neste módulo

* **Multilinguagem:** Suporta C, C++, Python, Java, HTML, entre outras
* **Extensibilidade:** Permite instalar plugins oficiais e da comunidade para turbinar o desenvolvimento
* **Integração:** Possui suporte nativo para Git, terminais integrados e ferramentas de build

---

# 2. Configuração do Ambiente para C
Para transformar o VS Code em uma IDE (Ambiente de Desenvolvimento Integrado) funcional para C, é necessário seguir três passos fundamentais:

### Passo 1: Instalação da Extensão
* É necessário instalar a extensão oficial **C/C++ da Microsoft** no Marketplace (ícone de quadrados na barra lateral)
* Ela oferece recursos como **IntelliSense** (autocompletar código) e suporte à depuração

### Passo 2: O Compilador (Essencial)
O VS Code é apenas um editor de texto; ele não compila código sozinho
* **Windows:** Recomenda-se o **TDM-GCC** ou **MinGW**
* **Linux:** Utiliza-se o **GCC** (via `sudo apt-get install build-essential`)
* **macOS:** Utiliza-se o **Clang** ou **GCC** (via Homebrew ou Xcode)

### Passo 3: Extensões de Apoio
* **C/C++ Compile Run:** Facilita a execução com um único clique ou atalho (F6/F7), automatizando o comando no terminal

---

# 3. Fluxo de Trabalho e Execução
A criação de um programa segue um ciclo simples dentro do ambiente configurado:

1.  **Pasta do Projeto:** Criar uma pasta dedicada para organizar os arquivos `.c`
2.  **Criação do Arquivo:** Salvar o arquivo com a extensão correta (ex: `hello.c`)
3.  **Compilação e Execução:** Abrir o terminal integrado (`Ctrl + '`) e digitar os comandos de compilação ou usar o atalho da extensão instalada


---

# 4. Atalhos de Produtividade
O domínio dos atalhos é essencial para otimizar o tempo de programação
| Categoria | Atalho | Função |
| :--- | :--- | :--- |
| **Navegação** | `Ctrl + P` | Busca rápida de arquivos no projeto |
| **Edição** | `Ctrl + D` | Seleciona a próxima ocorrência da palavra |
| **Linhas** | `Ctrl + Shift + K` | Deleta a linha atual instantaneamente |
| **Arquivos** | `Ctrl + S` | Salva o arquivo atual (obrigatório antes de compilar) |
| **Terminal** | `Ctrl + '` | Abre ou fecha o terminal integrado |
| **Geral** | `F1` ou `Ctrl + Shift + P` | Abre a Paleta de Comandos |

---

# 5. Versionamento com Git
O plano de aula destaca a importância de integrar o VS Code com sistemas de controle de versão
* **Branching:** Permite trabalhar em diferentes versões do código (Main, Hotfix, Features) sem comprometer a versão estável
* **Interface:** O VS Code possui uma aba dedicada ao Git que facilita o *commit*, *push* e *pull* de alterações diretamente para o GitHub


---

## 6. Dicas de Customização
O ambiente pode ser personalizado para melhorar o conforto visual e a organização:
* **Temas:** É possível escolher entre temas claros, escuros e de alto contraste (ex: *GitHub Dark*, *Abyss*, *Solarized*
* **Layout:** Personalização da barra lateral e do posicionamento das janelas de edição
