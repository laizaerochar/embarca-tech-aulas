# Introdução à Automação e Sistemas de Controle

A automação consiste no uso de tecnologias para controlar processos e máquinas, visando eficiência, segurança e precisão

## 1. O que é um Sistema de Controle?
É um conjunto de dispositivos que gerencia, comanda ou regula o comportamento de outros dispositivos ou sistemas
* **Objetivo**: Manter uma variável do processo em um valor desejado (setpoint)
* **Aplicações**: Desde o controle de temperatura de uma sala até sistemas complexos de navegação aeroespacial

---

## 2. Elementos Fundamentais
Um sistema de controle é composto por quatro partes principais:
* **Sensores (Percepção)**: Medem a variável real do processo (ex: termômetro, sensor de umidade)
* **Controlador (Cérebro)**: Processa a informação do sensor e decide a ação a ser tomada (ex: Raspberry Pi Pico W)
* **Atuadores (Ação)**: Dispositivos que executam o trabalho físico para alterar o processo (ex: motores, relés, válvulas)
* **Planta ou Processo**: O sistema físico que está sendo controlado

---

## 3. Tipos de Malhas de Controle
A forma como o controlador utiliza a informação define o tipo de malha:

### Malha Aberta (Open-Loop)
* A ação de controle **não depende** da saída do sistema
* Não há feedback (retroalimentação) para corrigir erros
* **Exemplo**: Uma torradeira que funciona por um tempo fixo, independentemente do pão estar torrado ou não

### Malha Fechada (Closed-Loop)
* A saída do sistema é medida e comparada com o valor desejado
* O erro (diferença entre o desejado e o real) é usado para ajustar a ação de controle
* **Exemplo**: Um ar-condicionado que liga/desliga baseado na temperatura real medida no ambiente

---

## 4. Controle On-Off (Liga-Desliga)
É a estratégia de controle mais simples e comum:
* O controlador atua de forma binária: totalmente ligado ou totalmente desligado
* **Histerese**: É uma faixa de tolerância adicionada para evitar que o atuador ligue e desligue repetidamente em intervalos muito curtos (o que poderia danificar o equipamento)
* **Aplicação na BitDogLab**: Controle de um LED ou buzzer baseado em um limiar de sensor de luz ou temperatura

---

## 5. Prática e Implementação no curso
A Unidade 6 foca na aplicação prática de todos os conceitos aprendidos anteriormente (GPIO, ADC, PWM, Wi-Fi) para criar sistemas automáticos:
* **Integração**: Uso da Raspberry Pi Pico W para ler sensores analógicos e atuar em dispositivos via relés ou PWM
* **Projetos**: Implementação de lógicas de controle para automação residencial e monitoramento ambiental
