# Desenvolvimento em Microcontroladores

### 1. Visão Geral do Desenvolvimento
O desenvolvimento de software para microcontroladores (sistemas embarcados) difere de sistemas convencionais devido a:
* **Recursos Limitados:** Poder de processamento e memória RAM/Flash restritos
* **Baixo Nível:** Frequentemente envolve manipulação direta de hardware e registradores
* **Tempo Real:** Necessidade de controle preciso de tempo e resposta a eventos físicos
* **Interação Física:** Sincronização constante com sensores e atuadores (mundo físico)
* 
### 2. Kit de Desenvolvimento: BitDogLab
* **Coração da Placa:** Utiliza o microcontrolador **Raspberry Pi Pico W**
* **Componentes Integrados:**
    * Display OLED (128x64), Matriz de LEDs 5x5, Joystick e Botões
    * Microfone, Buzzer e amplificador de áudio.
    * Bateria de íon-lítio para operação autônoma e conectores de expansão

### 3. O Microcontrolador RP2040
É o primeiro MCU projetado pela Raspberry Pi, oferecendo alta performance e baixo custo
* **Arquitetura:** Dual-Core ARM Cortex-M0+ operando a **133 MHz**
* **Memória:** 256 KB de SRAM interna
* **Periféricos:** Possui 30 pinos GPIO, 2x UART, 2x SPI, 2x I2C, 16 canais PWM e 4 canais ADC (12 bits)
* **Diferencial PIO:** O módulo *Programmable I/O* permite emular interfaces de hardware personalizadas sem sobrecarregar a CPU

### 4. SDK e Ambiente de Software
O **Raspberry Pi Pico C/C++ SDK** abstrai a complexidade do hardware através de APIs
* **Organização das Bibliotecas:**
    * `pico_xxx`: Bibliotecas de alto nível (ex: `pico_time` para temporização)
    * `hardware_xxx`: Bibliotecas de baixo nível para acesso direto aos periféricos
* **Sistema de Build (CMake):** Utiliza o arquivo `CMakeLists.txt` para gerenciar a compilação, definir o nome do projeto e vincular as bibliotecas necessárias (como a `pico_stdlib`)

### 5. Exemplo Prático: Aplicação Blink
Um programa básico em C para microcontroladores geralmente segue este fluxo:
1.  **Inclusão:** `#include "pico/stdlib.h"`
2.  **Inicialização:** Uso de `gpio_init()` e `gpio_set_dir()` para configurar pinos (ex: pino 12 para o LED)
3.  **Loop Infinito:** `while(true)` para manter a lógica de ligar/desligar o LED com `gpio_put()` e pausas com `sleep_ms()`
