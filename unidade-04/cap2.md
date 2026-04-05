# Interfaces de Entrada e Saída (GPIO)

## 1. Visão Geral do GPIO no RP2040
As interfaces de **Entrada e Saída de Propósito Geral (GPIO)** permitem que o microcontrolador interaja diretamente com componentes externos, no caso do chip **RP2040**, utilizado na BitDogLab, as principais características são;
* **Quantidade:** Possui **30 pinos GPIO** multifuncionais
* **Flexibilidade:** Cada pino pode ser configurado individualmente como entrada ou saída digital
* **Níveis de Tensão:** Opera com sinais digitais de **0V (baixo/low)** e **3.3V (alto/high)**
* **Multiplexação:** Um mesmo pino físico pode desempenhar diferentes funções (como UART, SPI, I2C ou PWM) dependendo da configuração do software

---

## 2. Configuração de Software (SDK)
Para manipular os pinos GPIO usando o C/C++ SDK do Raspberry Pi Pico, as funções fundamentais são;
* **`gpio_init(pin)`**: Inicializa o pino para uso
* **`gpio_set_dir(pin, mode)`**: Define se o pino será uma entrada (`GPIO_IN`) ou saída (`GPIO_OUT`)
* **`gpio_put(pin, value)`**: Define o estado lógico de um pino configurado como saída (1 para ligado, 0 para desligado)
* **`gpio_get(pin)`**: Lê o estado lógico atual de um pino configurado como entrada

---

## 3. Resistores de Pull-up e Pull-down
Quando um pino é configurado como **entrada**, ele pode flutuar e causar leituras erradas se não estiver conectado a nada. O RP2040 possui resistores internos para resolver isso;
* **Pull-up:** Mantém o pino em nível lógico alto (3.3V) por padrão; a leitura vai para 0V quando o botão é pressionado
* **Pull-down:** Mantém o pino em nível lógico baixo (0V) por padrão; a leitura vai para 3.3V ao pressionar o botão
* **Função:** No código, utiliza-se `gpio_pull_up(pin)` ou `gpio_pull_down(pin)`

---

## 4. Debouncing (Tratamento de Ruído)
Botões mecânicos geram ruídos elétricos (oscilações rápidas) ao serem pressionados, o que o microcontrolador pode interpretar como múltiplos cliques
* **Solução:** O "debouncing" pode ser feito via hardware (filtros) ou via **software** (adicionando um pequeno atraso de tempo após detectar a primeira mudança de estado)

---

## 5. Prática na BitDogLab
O capítulo foca na utilização dos componentes integrados na placa para testar esses conceitos;
* **Entrada:** Uso dos **Botões A (GP5)** e **B (GP6)** para capturar comandos do usuário
* **Saída:** Controle dos LEDs do **LED RGB (GPs 11, 12 e 13)** para fornecer feedback visual
* **Atividade Proposta:** Criar um programa onde o LED RGB mude de cor conforme o botão pressionado, aplicando as configurações de pull-up e lógica de controle
