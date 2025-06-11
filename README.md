# Projeto NodeMCU com MQTT

Este projeto utiliza um NodeMCU para controlar LEDs via MQTT. Os LEDs podem ser ligados e desligados através de tópicos específicos no broker MQTT.

## Descrição

O código conecta o NodeMCU a uma rede Wi-Fi e se comunica com um broker MQTT. Ele assina tópicos para receber comandos de controle e publica o estado dos LEDs.

## Requisitos

* NodeMCU (ESP8266)
* Biblioteca PubSubClient
* Biblioteca ESP8266WiFi

## Configuração

1. *Instalação do PlatformIO*: Certifique-se de ter o PlatformIO instalado.
2. **Configuração do platformio.ini**:
    ini
    [env:nodemcuv2]
    platform = espressif8266
    board = nodemcuv2
    framework = arduino

    lib_deps =
        knolleary/PubSubClient
    

4. *Alterar credenciais Wi-Fi e MQTT*: No arquivo main.cpp, ajuste as seguintes linhas com suas informações:
    cpp
    const char* ssid = "SEU_SSID";
    const char* password = "SUA_SENHA";
    const char* mqtt_server = "ENDERECO_DO_BROKER";
    const int mqtt_port = PORTA_DO_BROKER;
    

## Tópicos MQTT

### Tópicos de Assinatura

Os seguintes tópicos podem ser usados para controlar os LEDs:

* casa/sala/led/set
* casa/cozinha/led/set
* casa/quarto1/led/set
* casa/quarto2/led/set
* casa/varanda/led/set

### Tópicos de Publicação

Os estados dos LEDs são publicados nos seguintes tópicos:

* casa/sala/led/status
* casa/cozinha/led/status
* casa/quarto1/led/status
* casa/quarto2/led/status
* casa/varanda/led/status

## Como Usar

1. *Compilar e Fazer o Upload*: Utilize o PlatformIO para compilar e fazer o upload do código para o NodeMCU.
2. *Publicar Comandos*: Envie mensagens ON ou OFF para os tópicos de assinatura correspondentes para controlar os LEDs.

## Imagens do Projeto

### Circuito com LEDs
![CircuitocomLEDs](https://github.com/user-attachments/assets/4257bef2-71f4-4212-97df-6e50c29c305d)

### Circuito com LEDs (Alternativa)
![CircuitocomLEDs(Alternativa)](https://github.com/user-attachments/assets/a0c72f8b-f873-4753-ac16-422fb3528fed)

### MQTT Explorer
![MQTTExplorer](https://github.com/user-attachments/assets/ef49cdd2-2494-46a6-bd1d-c1f5452a043f)


## Contribuições

Contribuições são bem-vindas! Sinta-se à vontade para abrir uma issue ou um pull request.

## Licença

Este projeto está licenciado sob a MIT License - veja o arquivo [LICENSE](LICENSE) para mais detalhes.
