# Modulação por Largura de Pulso (PWM)

O **PWM (Pulse Width Modulation)** é uma técnica poderosa que permite controlar a quantidade de energia entregue a uma carga variando a largura de pulsos digitais. Com ele, é possível simular variações analógicas usando apenas sinais ligados e desligados

## 1. Conceitos Fundamentais
* **Ciclo de Trabalho (Duty Cycle):** É a razão entre o tempo que o sinal permanece em nível alto ($T_{on}$) e o período total da onda ($T$)
    * **0%:** Sinal sempre desligado (0V médio)
    * **50%:** Sinal ligado metade do tempo (1.65V médio em um sistema de 3.3V)
    * **100%:** Sinal sempre ligado (3.3V médio).
* **Frequência:** Define a rapidez com que o ciclo se repete. Frequências altas são usadas para evitar oscilações visíveis em LEDs ou ruídos audíveis em motores

---

## 2. O Controlador PWM no RP2040
O microcontrolador da Raspberry Pi possui um hardware de PWM altamente flexível;
* **8 Slices (Fatias):** Cada fatia possui dois canais (A e B), totalizando **16 canais PWM** independentes
* **Atribuição de Pinos:** Todos os pinos GPIO do RP2040 podem ser configurados para uma das saídas PWM
* **Resolução:** Utiliza contadores de **16 bits**, permitindo um controle muito fino do ciclo de trabalho (de 0 a 65535)

---

## 3. Aplicações Práticas na BitDogLab
O PWM é essencial para controlar os periféricos da placa que exigem variação de intensidade ou movimento;
* **Controle de Brilho (LED RGB):** Permite criar milhões de cores ao variar a intensidade individual dos LEDs Vermelho, Verde e Azul
* **Servomotores:** O PWM é o padrão para controlar a posição do eixo de servos (muito comum em robótica)
* **Buzzer:** Ao variar a frequência do PWM, é possível gerar diferentes notas musicais e tons de alerta

---

## 4. Implementação no SDK (C/C++)
As etapas principais no código para configurar o PWM são:
1.  **`gpio_set_function(pin, GPIO_FUNC_PWM)`**: Configura o pino para operar no modo PWM
2.  **`pwm_get_default_config()`**: Obtém uma estrutura de configuração padrão
3.  **`pwm_config_set_clkdiv()`**: Ajusta o divisor de clock para definir a frequência desejada
4.  **`pwm_init(slice, config, true)`**: Inicializa e liga a fatia de PWM
5.  **`pwm_set_gpio_level(pin, level)`**: Define o nível (duty cycle) atual da saída

---

## 5. Vantagens do PWM
* **Eficiência Energética:** Como os transistores operam totalmente ligados ou desligados, há menos desperdício de energia na forma de calor em comparação com reguladores lineares
* **Simplicidade de Hardware:** Permite controle de potência usando apenas saídas digitais comuns do microcontrolador
