# Capítulo 2 - Arquitetura de
Sistemas Embarcados
---

# Arquitetura de Sistemas Embarcados — Resumidamente

Um sistema embarcado é dividido em duas partes principais:

* **Hardware embarcado** → componentes físicos
* **Software embarcado** → programas que controlam o hardware 

---

## Estrutura Geral do Sistema

### Hardware

* CPU / MPU
* Memórias
* Interfaces
* Sensores e atuadores

### Software

* Sistema Operacional (RTOS)
* Firmware
* Drivers
* Aplicações

---

## Arquitetura do Hardware

Os componentes são conectados por **barramentos**:

* **Dados** → leitura/escrita
* **Endereços** → localização na memória
* **Controle (CTRL)** → comando das operações 

---

## Tipos de Arquitetura

### Arquitetura Harvard

* Memória de **dados** e **programa separadas**
* Acesso simultâneo
* Mais rápida

---

### Arquitetura Von Neumann

* Dados e instruções na **mesma memória**
* Acesso sequencial
* Mais lenta

---

## Arquitetura em Camadas

Sistema organizado em **3 camadas principais**:

### 1. Hardware

* Componentes físicos
* Pode ser:

  * **Hardwired** → fixo
  * **Softwired (FPGA)** → programável

---

### 2. Software Básico

####  Device Drivers

* Controlam o hardware
* Fazem ponte entre hardware e software

#### Núcleo (Kernel / RTOS)

* Gerencia tarefas
* Controle de tempo real
* Escalonamento

#### Protocolos e Serviços

* Comunicação (ex: TCP/IP, USB)
* Define como os dados trafegam

---

### 3. Software de Aplicação

* Implementa a função do sistema
* Ex: sistema de irrigação, controle de motor

---

## Componentes de um Sistema Embarcado

### Microcontrolador

* Integra:

  * CPU
  * Memória
  * ADC/DAC
  * Interfaces

---

### FPGA

* Hardware programável
* Pode ser reconfigurado

---

### Memórias

#### Volátil (RAM)

* Perde dados sem energia
* Ex: SRAM, DRAM

#### Não volátil (ROM)

* Mantém dados sem energia
* Ex: Flash, EEPROM

---

### Periféricos / Interfaces

* GPIO
* UART / SPI / I2C
* Timers e contadores
* ADC / DAC
* PWM

---

### Sensores

* Temperatura
* Pressão
* Proximidade
* Acelerômetro

---

### Atuadores

* Motores
* Relés
* LEDs
* Drivers

---
