# Interrupções e Temporizadores (RP2040)

## 1. O Conceito de Interrupções (IRQ)
As interrupções permitem que o microcontrolador responda a eventos externos ou internos de forma imediata, sem a necessidade de verificar constantemente o estado de um pino (técnica de *polling*)
* **Funcionamento**: Quando ocorre um evento, o processador pausa a execução do programa principal, executa uma função específica chamada **ISR (Interrupt Service Routine)** e depois retorna ao ponto onde parou.
* **Vantagens**: Aumenta a eficiência do sistema, reduz a latência de resposta e economiza energia, pois permite que o processador execute outras tarefas ou entre em modo de baixo consumo enquanto espera o evento.

---

## 2. Tipos de Interrupções no RP2040
No Raspberry Pi Pico, as interrupções podem ser acionadas por diversos eventos;
* **Eventos de GPIO**: Acionadas por mudança de estado nos pinos (borda de subida, borda de descida, nível alto ou nível baixo)
* **Interrupções de Temporizador**: Geradas quando um contador atinge um valor predeterminado, útil para tarefas periódicas
* **Outros Periféricos**: UART, I2C, SPI e DMA também podem gerar interrupções para sinalizar a conclusão de uma transferência ou chegada de dados.



---

## 3. Temporizadores (Timers) e Alarmes
O RP2040 possui um temporizador de hardware de 64 bits que conta microssegundos desde a inicialização
* **Alarmes**: Podem ser configurados para gerar uma interrupção após um intervalo específico ou em um momento exato.
* **Funções Repetitivas**: O SDK permite configurar *callbacks* repetitivos para executar código em intervalos fixos (ex: ler um sensor a cada 100ms)

---

## 4. Implementação no SDK (C/C++)
As principais funções utilizadas para configurar esses recursos são;
* **`gpio_set_irq_enabled_with_callback()`**: Configura uma interrupção em um pino específico e define qual função (ISR) será chamada
* **`add_alarm_in_ms()`**: Agenda um evento único para ocorrer após um tempo determinado em milissegundos
* **`add_repeating_timer_ms()`**: Configura uma tarefa recorrente que executa uma função de retorno periodicamente

---

## 5. Cuidados e Boas Práticas (ISR)
Como as ISRs interrompem o fluxo principal, elas devem seguir regras rígidas para não travar o sistema;
* **Breve e Rápida**: A função deve fazer o mínimo possível (ex: apenas mudar o valor de uma variável global).
* **Não usar funções lentas**: Evite usar `printf()` ou `sleep_ms()` dentro de uma interrupção, pois isso pode causar comportamentos imprevisíveis.
* **Variáveis Voláteis**: Variáveis compartilhadas entre a ISR e o programa principal devem ser declaradas como `volatile` para garantir que o compilador sempre leia o valor mais recente da memória.
