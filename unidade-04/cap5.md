# Conversores Analógico-Digitais (ADC)

O mundo real é predominantemente analógico (temperatura, luz, som), enquanto microcontroladores processam apenas sinais digitais. O **ADC** é a ponte que converte essas variações contínuas de tensão em números binários
## 1. Conceitos Fundamentais
* **Sinal Analógico**: Varia continuamente no tempo e pode assumir qualquer valor dentro de um intervalo
* **Sinal Digital**: Representação discreta do sinal original, limitada pela resolução do conversor
* **Resolução**: Define o número de níveis que o ADC pode representar. No RP2040, a resolução é de **12 bits**, o que resulta em $2^{12} = 4096$ valores possíveis (de 0 a 4095)
* **Taxa de Amostragem**: Frequência com que o sinal é medido. O RP2040 alcança até **500 ksps** (mil amostras por segundo)

---

## 2. O ADC no RP2040 (Raspberry Pi Pico)
O microcontrolador RP2040 possui um ADC interno com características específicas:
* **Canais**: Possui **5 canais de entrada** no total
    * 4 canais estão conectados aos pinos externos (**GP26, GP27, GP28 e GP29**)
    * 1 canal interno é dedicado ao **sensor de temperatura** do chip
* **Tensão de Referência**: Geralmente utiliza **3.3V**
* **Cálculo da Tensão**: Para converter o valor digital ($D$) lido em tensão ($V$), usa-se a fórmula:
  $$V = \frac{D \cdot 3.3}{4095}$$ 

---

## 3. Componentes na BitDogLab
A placa BitDogLab utiliza o ADC para ler periféricos importantes:
* **Joystick**: Possui dois potenciômetros internos para os eixos **X (GP26)** e **Y (GP27)**
* **Microfone**: Conectado ao canal **GP28**, permitindo captar variações sonoras e converter em sinais elétricos para processamento


---

## 4. Implementação no SDK (C/C++)
As funções principais para operar o ADC são:
* **`adc_init()`**: Inicializa o hardware do ADC
* **`adc_gpio_init(pin)`**: Configura o pino GPIO específico para funcionar como entrada analógica
* **`adc_select_input(input)`**: Seleciona qual canal será lido (0 a 4)
* **`adc_read()`**: Realiza a conversão e retorna o valor digital de 12 bits

---

## 5. Boas Práticas
* **Ruído**: Sinais analógicos são sensíveis a interferências eletromagnéticas; recomenda-se o uso de capacitores de desacoplamento ou médias móveis no software para estabilizar a leitura
* **Impedância**: A fonte do sinal analógico deve ter baixa impedância de saída para garantir a precisão da carga do capacitor interno do ADC
