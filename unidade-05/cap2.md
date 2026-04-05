#  Arquitetura da Internet das Coisas (IoT)

A arquitetura de IoT define como os dispositivos, redes e sistemas de processamento se estruturam para transformar dados brutos em informações úteis para o usuário final

## 1. Modelos de Arquitetura
Existem diferentes abordagens para organizar um sistema IoT, variando em complexidade:
* **Arquitetura de 3 Camadas:** O modelo mais básico, composto pelas camadas de Percepção (sensores), Rede (transmissão) e Aplicação (interface com o usuário)
* **Arquitetura de 5 Camadas:** Um modelo mais detalhado que adiciona as camadas de Processamento (middleware) e Negócios (gestão do sistema e privacidade)



---

## 2. Descrição das Camadas (Modelo de 5 Camadas)
* **Camada de Percepção:** É o nível físico onde os sensores e atuadores coletam dados do ambiente (temperatura, umidade, movimento)
* **Camada de Rede:** Responsável por enviar os dados coletados para a próxima etapa através de tecnologias como Wi-Fi, Bluetooth, ZigBee ou redes celulares
* **Camada de Processamento (Middleware):** Armazena, analisa e processa as informações recebidas, muitas vezes utilizando bancos de dados e computação em nuvem
* **Camada de Aplicação:** Entrega os serviços e informações ao usuário final por meio de smartphones, smartwatches ou dashboards web
* **Camada de Negócios:** Gerencia todo o sistema, incluindo modelos de negócios, privacidade do usuário e análise de viabilidade

---

## 3. Tecnologias de Conectividade
A escolha da tecnologia de rede depende do alcance e do consumo de energia necessários para a aplicação:
* **Curto Alcance:** Bluetooth (PAN) e Wi-Fi (LAN), ideais para casas inteligentes
* **Longo Alcance:** LoRaWAN e Sigfox (LPWAN), ideais para agricultura e monitoramento urbano devido ao baixo consumo

---

## 4. Desafios da Arquitetura IoT
Projetar sistemas IoT exige atenção a pontos críticos para o sucesso da solução:
* **Segurança e Privacidade:** Proteção contra acessos não autorizados e vazamento de dados sensíveis
* **Escalabilidade:** Capacidade de o sistema crescer e suportar milhares de novos dispositivos conectados
* **Interoperabilidade:** Garantir que dispositivos de diferentes fabricantes consigam se comunicar entre si

---

## 5. Prática e Implementação
No contexto da **Raspberry Pi Pico W**, a arquitetura foca na integração do hardware com protocolos de rede robustos;
* **Processamento:** O microcontrolador RP2040 atua na camada de percepção e processamento local
* **Comunicação:** O chip Wi-Fi integrado gerencia a camada de rede para enviar dados para servidores ou brokers MQTT
