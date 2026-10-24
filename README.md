# Vinheria Agnello — Edge Computing

## Sobre o Projeto

Este projeto tem como objetivo desenvolver um sistema de Internet das Coisas (IoT) para a Vinheria Agnello, utilizando sensores para monitorar condições ambientais e transmitir os dados para um servidor IoT por meio do protocolo MQTT.

Inicialmente, foi preparada a infraestrutura do servidor IoT com os serviços necessários para receber e gerenciar informações. Agora, o objetivo é conectar o sistema desenvolvido no ESP32 a esse servidor, permitindo a leitura e o envio de dados de temperatura, umidade e luminosidade.

## Tecnologias Utilizadas

- **FIWARE Orion Context Broker:** gerenciamento de informações de contexto.
- **IoT Agent MQTT:** comunicação entre dispositivos IoT e a plataforma FIWARE.
- **STH-Comet:** armazenamento e consulta de dados históricos.
- **MongoDB:** banco de dados utilizado pelos serviços.
- **Mosquitto:** broker responsável pela comunicação MQTT.
- **Linux:** ambiente de execução do servidor IoT.
- **ESP32:** microcontrolador utilizado no projeto.
- **Wokwi:** simulador para desenvolvimento e testes do circuito.
- **DHT22:** sensor de temperatura e umidade.
- **LDR:** sensor de luminosidade.
- **MyMQTT:** aplicativo para leitura e publicação de mensagens MQTT.
- **Postman:** ferramenta para verificar o funcionamento dos serviços do servidor.

## Servidor IoT

O servidor IoT é responsável por receber e gerenciar os dados enviados pelos dispositivos conectados. A infraestrutura utiliza os seguintes serviços:

- Orion Context Broker;
- IoT Agent MQTT;
- STH-Comet;
- MongoDB;
- Mosquitto MQTT Broker.

O ambiente foi preparado em uma máquina Linux, com os serviços executados em containers. Para verificar o funcionamento da infraestrutura, são utilizados health checks pelo Postman.

## Sistema IoT

O sistema utiliza um ESP32 simulado no Wokwi, conectado a sensores responsáveis pela coleta de informações ambientais.

### Funcionalidades:

- Leitura de temperatura com o sensor DHT22.
- Leitura de umidade com o sensor DHT22.
- Leitura de luminosidade com o sensor LDR.
- Envio dos dados coletados ao servidor IoT por meio do protocolo MQTT.
- Leitura e publicação de mensagens utilizando o aplicativo MyMQTT.

### Comunicação MQTT

O protocolo MQTT permite a troca de mensagens entre o ESP32 e o servidor IoT por meio de um broker. Para realizar a comunicação, é necessário configurar corretamente o endereço do broker, a porta de conexão e os tópicos utilizados para publicação e recebimento das mensagens.

## ▶️ Como Executar

### Simulação no Wokwi

1. Abra o projeto no Wokwi.
2. Verifique as conexões do ESP32 com os sensores DHT22 e LDR.
3. Configure os parâmetros de conexão MQTT.
4. Inicie a simulação.
5. Utilize o MyMQTT para publicar e receber mensagens.
6. Verifique o envio dos dados dos sensores ao servidor IoT.

**Link da simulação no Wokwi:** [[Clique aqui](https://wokwi.com/projects/478628063048558593)]

## Vídeo Demonstrativo

**Link:** [[Clique aqui](https://youtu.be/GRCbH43icaM?is=QVi_5B1h-MC4g1Dj)]

## Integrantes

- Amanda Oliveira Lourenço — RM: 572572
- Giovanna Lopes Scalzone — RM: 572285
- Nayra Sousa Duarte — RM: 573815
- Paloma do Carmo Dantas — RM: 569995
