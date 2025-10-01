# Gustavo-Roberto-SPRINT-3-Disruptive-Architectures-

Este projeto implementa uma solução IoT para monitoramento em tempo real utilizando ESP32 com dois sensores ultrassônicos (HC-SR04) e LEDs indicadores, com comunicação via MQTT para integração com Node-RED.

O sistema coleta distâncias medidas pelos sensores, envia para um broker MQTT e exibe os dados em um dashboard interativo no Node-RED, incluindo gráficos históricos para análise.

- Tecnologias Utilizadas

ESP32 – Microcontrolador responsável pela coleta dos dados e envio via MQTT.

Sensores HC-SR04 – Medição de distância.

LEDs – Indicadores visuais locais (verde = seguro, vermelho = alerta).

MQTT (PubSubClient) – Protocolo de comunicação leve para IoT.

Broker MQTT Público – broker.hivemq.com:1883 (pode ser trocado por Mosquitto local).

Node-RED – Plataforma de integração para visualizar e processar os dados.

Node-RED Dashboard – Exibição de gráficos em tempo real.

Wokwi – Simulador online de ESP32 e sensores.

- Como Executar
 1. No ESP32 (Wokwi ou real)

Abra o Wokwi

Monte o circuito com:

2 sensores HC-SR04 conectados aos pinos do ESP32.

LEDs conectados para indicar status.

Copie e cole o código sketch.ino.

Compile e rode.

O ESP32 começará a publicar mensagens MQTT nos tópicos:

esp32/sensor1

esp32/sensor2

2. No Node-RED

Instale o Node-RED (via npm ou Docker).

Instale o pacote node-red-dashboard:

cd ~/.node-red
npm install node-red-dashboard


Importe o fluxo JSON fornecido (Menu → Import → Clipboard).

Versão 1: dois gráficos separados.

Versão 2: gráfico comparativo (dois sensores na mesma curva).

Configure o broker MQTT para broker.hivemq.com porta 1883.

Acesse o dashboard em:

http://localhost:1880/ui

- Resultados Parciais

Conseguiu-se estabelecer comunicação em tempo real entre o ESP32 e o Node-RED via MQTT.

Os sensores ultrassônicos publicam dados em dois tópicos distintos.

O Node-RED dashboard exibe:

Valores instantâneos de distância de cada sensor.

Gráficos de histórico (tempo real).

O sistema funciona tanto em simulação (Wokwi) quanto em hardware real.


- LINK DO VIDEO:

https://youtu.be/BrUIUD2w6ak?si=dk4GCKPA4ANSjakT
