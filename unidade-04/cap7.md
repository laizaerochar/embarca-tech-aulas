# Máquinas de Estados Finitos (FSM)

As **Máquinas de Estados Finitos (FSM)** são um modelo matemático e de design fundamental para organizar a lógica de sistemas embarcados complexos, permitindo que o sistema alterne entre comportamentos específicos baseados em eventos. 

## 1. Conceitos Fundamentais
* **Estado**: Representa uma condição ou situação específica em que o sistema se encontra em um determinado momento (ex: "Ligado", "Desligado", "Aguardando"). 
* **Transição**: É a mudança de um estado para outro, disparada por um evento ou condição específica. 
* **Evento (Input)**: Um estímulo externo (como o pressionar de um botão) ou interno (como um temporizador) que pode causar uma transição. 
* **Ação (Output)**: A resposta do sistema ao estar em um estado ou ao realizar uma transição (ex: acender um LED). 


---

## 2. Tipos de Máquinas de Estados
Existem dois modelos principais utilizados em sistemas digitais:
* **Máquina de Mealy**: As saídas dependem tanto do estado atual quanto das entradas atuais. 
* **Máquina de Moore**: As saídas dependem exclusivamente do estado atual do sistema. 

---

## 3. Vantagens do uso de FSM
* **Organização**: Substitui estruturas de decisão (`if/else`) complexas e "macarrônicas" por uma lógica clara e determinística. 
* **Facilidade de Manutenção**: Adicionar novos comportamentos torna-se mais simples ao inserir novos estados e transições. 
* **Previsibilidade**: Como o sistema só pode estar em um estado por vez, o comportamento do software torna-se mais fácil de testar e validar. 
---

## 4. Implementação em C (SDK)
A forma mais comum e eficiente de implementar uma FSM em C é utilizando as estruturas `enum` e `switch-case`:
1.  **`enum`**: Define os nomes dos estados possíveis de forma legível. 
2.  **Variável de Estado**: Armazena o estado atual do sistema. 
3.  **`switch(estado_atual)`**: Estrutura que decide quais ações executar e quais condições verificar para mudar de estado. 

---

## 5. Exemplo Prático na BitDogLab
* **Semáforo**: Alternar entre os estados Verde, Amarelo e Vermelho com base em temporizadores. 
* **Controle de LEDs por Botão**: Alternar estados de animação ou cores do LED RGB a cada clique, tratando o *debouncing* dentro da lógica da máquina.
