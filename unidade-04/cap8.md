# Módulo de PIO (Programmable I/O)

O **PIO** é uma inovação exclusiva do microcontrolador **RP2040**. Ele permite a criação de interfaces de hardware personalizadas que operam de forma independente dos núcleos principais da CPU, garantindo alta precisão de tempo

## 1. O que é o PIO?
* É um subsistema de hardware versátil que pode emular diversos protocolos de comunicação (como SPI, I2C, UART) ou criar protocolos totalmente novos
* **Independência:** O PIO executa suas próprias instruções sem interromper os núcleos ARM Cortex-M0+
* **Precisão:** É ideal para aplicações que exigem temporização rigorosa (deterministmo), como o controle de fitas de LED endereçáveis (WS2812B)

---

## 2. Arquitetura do PIO
O RP2040 possui **dois blocos PIO**, cada um contendo:
* **4 Máquinas de Estados (State Machines):** Cada uma pode executar um programa de forma independente
* **Memória de Instruções:** Espaço compartilhado para armazenar até 32 instruções por bloco
* **FIFOs (First-In, First-Out):** Filas de dados que permitem a comunicação eficiente entre a CPU e as máquinas de estados do PIO

---

## 3. Linguagem Assembly do PIO
Os programas para o PIO são escritos em uma linguagem de montagem simplificada, composta por apenas **9 instruções fundamentais**:
1.  **JMP:** Desvio de fluxo
2.  **WAIT:** Aguarda um evento ou pino
3.  **IN:** Move dados para o registrador de entrada
4.  **OUT:** Move dados para os pinos ou outros registradores
5.  **PUSH:** Envia dados para a CPU via FIFO
6.  **PULL:** Recebe dados da CPU via FIFO
7.  **MOV:** Move dados entre registradores
8.  **IRQ:** Gera ou limpa uma interrupção
9.  **SET:** Define valores diretamente nos pinos ou registradores

---

## 4. Integração no Projeto (SDK)
Para utilizar o PIO no VS Code com o C/C++ SDK, o fluxo de trabalho envolve:
* **Arquivo `.pio`:** Contém o código Assembly e instruções de configuração para o compilador `pioasm`
* **Compilação:** O `pioasm` converte o código em um arquivo de cabeçalho (`.h`) que pode ser incluído no projeto C
* **Funções de Hardware:** Uso da biblioteca `hardware_pio` para carregar o programa e gerenciar as máquinas de estados

---

## 5. Exemplo de Aplicação na BitDogLab
O uso mais comum demonstrado é o controle da **Matriz de LEDs 5x5 (WS2812B)**:
* O PIO gera os pulsos de nanosegundos precisos exigidos pelo protocolo "One-Wire" desses LEDs
* Permite controlar cores e brilho de forma fluida sem sobrecarregar o processador principal
