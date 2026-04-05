# Introdução à Internet das Coisas (IoT)

A **Internet das Coisas (IoT)** é a rede de objetos físicos incorporados com sensores, software e outras tecnologias com o objetivo de conectar e trocar dados com outros dispositivos e sistemas pela internet

## 1. Pilares da IoT
O funcionamento de uma solução de IoT baseia-se em três pilares fundamentais:
* **Coisas (Dispositivos):** Objetos físicos equipados com sensores e atuadores para interagir com o ambiente
* **Conectividade:** Meios de comunicação (Wi-Fi, Bluetooth, LoRa, etc.) que permitem que as "coisas" enviem e recebam dados
* **Inteligência (Nuvem/Dados):** Processamento e análise das informações coletadas para a tomada de decisões ou automação

---

## 2. A Placa Raspberry Pi Pico W
No contexto deste curso, a **Raspberry Pi Pico W** é a ferramenta central para o desenvolvimento de projetos IoT
* **Conectividade Integrada:** Diferente da versão básica, a versão "W" possui o chip **Infineon CYW43439**, que oferece suporte a **Wi-Fi 4 (802.11n)** e **Bluetooth 5.2**
* **Segurança:** Suporta protocolos de segurança como **WPA3**, garantindo conexões mais seguras para dispositivos domésticos e industriais
* **Antena:** Possui uma antena licenciada a bordo, o que facilita o design de projetos sem a necessidade de componentes externos complexos para rádio

---

## 3. Arquitetura de Comunicação
Para que um dispositivo IoT funcione, ele precisa seguir um fluxo de comunicação:
* **Protocolos de Rede:** O uso do conjunto **TCP/IP** é essencial para a comunicação na internet
* **Stack de Redes:** A Raspberry Pi Pico W utiliza bibliotecas específicas (como a **lwIP**) integradas ao SDK para gerenciar a pilha de protocolos de rede de forma eficiente
* **Interface:** A comunicação entre o microcontrolador RP2040 e o chip Wi-Fi ocorre via interface **SPI** interna

---

## 4. Aplicações Práticas
A IoT transforma diversos setores através da coleta de dados em tempo real:
* **Cidades Inteligentes:** Monitoramento de tráfego, iluminação pública eficiente e gestão de resíduos
* **Saúde (IoMT):** Monitoramento remoto de pacientes e dispositivos médicos conectados
* **Indústria 4.0:** Manutenção preditiva e controle de estoque automatizado
* **Agricultura de Precisão:** Sensores de umidade e solo integrados a sistemas de irrigação automática; OBS: EU TRABALHO COM ISSO USANDO ESP32, CASO TENHA MAIS INTERESSE, SÓ CHAMAR NO DISCORD!

---

## 5. Prática no SDK
As primeiras etapas para transformar a Pico W em um dispositivo IoT envolvem:
* **Configuração do Wi-Fi:** Uso de funções para escanear redes e conectar-se a um ponto de acesso (Access Point) fornecendo SSID e senha
* **Gerenciamento de Estados:** Implementação de lógicas para tratar quedas de conexão e tentativas de reconexão automática
