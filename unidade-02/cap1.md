# Capítulo 1 - tipos e caracteres de sistemas embarcados

# O que é um Sistema Embarcado?
Um **Sistema Embarcado (SE)** é um sistema computacional dedicado a executar **uma função específica**, geralmente integrado a um dispositivo maior, possui:
  * **Hardware** - circuito físico com microcontrolador
  * **Firmware** - software gravado na memória
Exemplo:
* Controle de bomba d’água
* Sistema de ignição de automóveis

## Diferença entre Sistema Embarcado vs Computador

| Sistema Embarcado | Computador (Propósito Geral) |
| ----------------- | ---------------------------- |
| Função única      | Múltiplas funções            |
| Interface simples | Interface complexa           |
| Otimizado         | Flexível                     |
| Tempo real        | Nem sempre tempo real        |

---

##  Componentes Principais

* **Microcontrolador** → funciona como o 'cérebro' do sistema
* **Sensores** → captam dados do ambiente
* **Atuadores** → executam ações físicas

Exemplo:

* Sensor de temperatura → envia dados
* Motor → executa ação

---

## Modos de Funcionamento

### 1. Reativo

* Fica “esperando” um evento
* Responde quando algo acontece

Exemplo: botão ligar/desligar

---

### 2. Tempo Real

* Executa tarefas dentro de um tempo definido

Tipos:

* **Soft Real Time** → atraso tolerável
* **Hard Real Time** → atraso NÃO permitido (crítico)

Exemplo: sistema de avião

---

## Tipos de Aplicações

### 1. Propósito Geral

* Interação intensa com usuário
* Ex: videogames, caixas eletrônicos

---

### 2. Sistemas de Controle

* Controle automático com sensores
* Ex: controle de motores, usinas

---

### 3. Processamento de Sinais

* Processa dados rapidamente
* Ex: áudio, vídeo, Bluetooth

---

### 4. Comunicação e Redes

* Transmissão de dados
* Ex: sistemas de telecomunicação

---

## Características dos Sistemas Embarcados

* Função específica
* Tempo real
* Baixo custo
* Pequeno tamanho
* Baixo consumo de energia
* Firmware próprio (não reaproveitável facilmente)
* Hardware sob medida
* Integração forte entre hardware e software

---
