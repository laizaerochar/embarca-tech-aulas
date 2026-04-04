# Depuração e Versionamento (Unidade 3 - Cap. 3)

# 1. Depuração de Código (Debugging)
A depuração é o processo sistemático de identificar, analisar e remover "bugs" ou defeitos de um software para garantir sua estabilidade e funcionalidade

### O Ciclo da Depuração:
* **Entendimento dos sintomas:** Analisar relatórios de erro, logs ou o comportamento inesperado do sistema
* **Identificação da causa:** Seguir o fluxo de execução para isolar a linha ou seção de código problemática
* **Correção do erro:** Realizar os ajustes necessários no código-fonte
* **Testes de software:** Validar se a correção foi eficaz e se não gerou novos problemas

---

# 2. Ferramentas de Depuração no VS Code
O VS Code oferece um ambiente robusto para depurar programas em C, permitindo monitorar o estado interno da aplicação em tempo real

### Principais Recursos:
* **Breakpoints (Pontos de Parada):** Pontos definidos pelo programador onde a execução do programa é pausada para análise
* **Inspeção de Variáveis:** Visualização dos valores armazenados em memória durante a execução
* **Watch Expressions:** Criação de expressões lógicas para monitorar condições específicas (ex: saber quando uma variável atinge um valor determinado)
* **Call Stack (Pilha de Chamadas):** Rastreamento das funções que foram chamadas até o ponto atual

### Comandos de Controle:
| Comando | Função |
| :--- | :--- |
| **Step Over** | Executa a próxima linha sem entrar nos detalhes de funções internas |
| **Step Into** | Entra nos detalhes da próxima função para execução linha por linha |
| **Step Out** | Finaliza a função atual e retorna imediatamente ao ponto de chamada |
| **Restart/Stop** | Reinicia ou finaliza completamente o processo de depuração |

---

# 3. Versionamento com Git e GitHub
O versionamento permite gerenciar mudanças no código, recuperar versões anteriores e facilitar o trabalho colaborativo

* **Git:** Sistema de controle de versão distribuído que rastreia o histórico de alterações nos arquivos
* **GitHub:** Plataforma baseada em nuvem que hospeda repositórios Git e promove a colaboração entre equipes

---

# 4. Conceitos Fundamentais do Git
A estrutura do Git baseia-se em estados e comandos que organizam a evolução do projeto.

| Termo | Definição |
| :--- | :--- |
| **Repositório** | Diretório onde o projeto e todo o seu histórico de revisões são armazenados |
| **Commit** | Um "savepoint" ou snapshot que registra o estado do código em um momento específico |
| **Branch** | Linha independente de desenvolvimento, permitindo criar novas funcionalidades sem afetar o código principal |
| **Merge** | Processo de combinar as alterações de uma branch (como uma correção) na branch principal (`main` ou `master`) |
| **Staging Area** | Ambiente de preparação onde as mudanças aguardam antes de serem confirmadas por um commit |

---

# 5. Comandos Essenciais do Terminal
A utilização prática do Git envolve uma sequência lógica de comandos para sincronizar o trabalho local com o servidor remoto

### Gerenciamento Local:
* `git init`: Inicializa um novo repositório na pasta atual
* `git add`: Adiciona arquivos ao ambiente de preparação
* `git commit -m "mensagem"`: Salva as alterações permanentemente no histórico local
* `git checkout -b nome_branch`: Cria e alterna para uma nova linha de desenvolvimento

### Sincronização Remota:
* `git clone`: Cria uma cópia local de um repositório que já existe no GitHub
* `git push`: Envia os commits realizados localmente para o servidor remoto
* `git pull`: Busca e integra as mudanças do repositório remoto para a sua máquina

---

# 6. Boas Práticas: Clean Code e Testes
Para facilitar tanto a depuração quanto o versionamento, o desenvolvedor deve adotar:
* **Clean Code:** Filosofia de escrita que visa tornar o código fácil de ler, manter e evoluir
  **Teste Unitário:** Verificação automática de pequenas partes isoladas do código para garantir que funcionam como o esperado
* **Pull/Merge Request:** Pedido formal para integrar mudanças, permitindo que a equipe discuta as alterações antes da aplicação final
