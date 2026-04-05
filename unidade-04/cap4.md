# Interfaces de Comunicação Serial

O desenvolvimento de sistemas embarcados exige que o microcontrolador se comunique com outros dispositivos (sensores, displays, outros MCUs) de forma eficiente, utilizando o menor número possível de pinos

## 1. UART (Universal Asynchronous Receiver-Transmitter)
É um protocolo de comunicação **assíncrona**, o que significa que não compartilha um sinal de clock comum entre os dispositivos
* **Conexão**: Utiliza dois fios principais: **TX** (Transmissão) e **RX** (Recepção)
* **Configuração**: Ambos os dispositivos devem estar configurados com a mesma velocidade de transmissão (**Baud Rate**)
* **Uso Comum**: Comunicação com módulos Bluetooth, GPS e depuração via terminal no computador (Serial Monitor)
* **No RP2040**: O chip possui duas instâncias de hardware UART independentes



---

## 2. I2C (Inter-Integrated Circuit)
Protocolo de comunicação **síncrona** baseado em uma arquitetura mestre-escravo, ideal para conectar múltiplos dispositivos em distâncias curtas
* **Conexão**: Utiliza apenas dois fios: **SDA** (Dados) e **SCL** (Clock)
* **Endereçamento**: Cada dispositivo escravo possui um endereço único, permitindo que o mestre se comunique com vários componentes usando os mesmos dois fios
* **Uso Comum**: Sensores de temperatura, acelerômetros e displays OLED (como o da BitDogLab)
* **No RP2040**: Oferece suporte a taxas de dados padrão (100 kbps) e rápidas (400 kbps)

---

## 3. SPI (Serial Peripheral Interface)
Protocolo **síncrono** de alta velocidade, geralmente mais rápido que o I2C, utilizado para grandes volumes de dados
* **Conexão**: Utiliza quatro fios principais;
    * **SCK**: Sinal de Clock.
    * **MOSI**: Saída do Mestre / Entrada do Escravo.
    * **MISO**: Entrada do Mestre / Saída do Escravo.
    * **SS/CS**: Seleção do Escravo (Chip Select).
* **Performance**: Comunicação Full-Duplex (envia e recebe dados simultaneamente)
* **Uso Comum**: Cartões SD, memórias Flash externas e displays LCD de alta resolução

---

## 4. Comparativo das Interfaces

| Característica | UART | I2C | SPI |
| :--- | :--- | :--- | :--- |
| **Tipo** | Assíncrona  | Síncrona  | Síncrona  |
| **Fios** | 2 (TX/RX)  |  (SDA/SCL)  | 4+ (MOSI/MISO/SCK/CS)  |
| **Velocidade** | Baixa/Média  | Média  | Alta  |
| **Distância** | Média  | Curta  | Curta  |
| **Dispositivos** | 1 para 1  | Múltiplos (Endereço)  | Múltiplos (Pino CS)  |

---

## 5. Prática e SDK
Para utilizar essas interfaces no Raspberry Pi Pico, o SDK disponibiliza bibliotecas específicas;
* **`hardware_uart`**: Funções como `uart_init()` e `uart_print()`
* **`hardware_i2c`**: Funções como `i2c_init()` e `i2c_write_blocking()`
* **`hardware_spi`**: Funções como `spi_init()` e `spi_write_read_blocking()`
