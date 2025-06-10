# Projeto-nodeMCU

from pathlib import Path

readme_content = """# Projeto NodeMCU + MQTT - Controle de LED via Tópicos

## Sumário

1. [Visão Geral](#visão-geral)  
2. [Estrutura de Pastas](#estrutura-de-pastas)  
3. [Pré-requisitos](#pré-requisitos)  
4. [Instalação e Configuração](#instalação-e-configuração)  
   - [Drivers do NodeMCU](#drivers-do-nodemcu)  
   - [PlatformIO](#platformio)  
   - [Mosquitto (Broker MQTT)](#mosquitto-broker-mqtt)  
   - [MQTT Explorer (Cliente Gráfico)](#mqtt-explorer-cliente-gráfico)  
5. [Código Fonte](#código-fonte)  
   - [Configurações Wi-Fi e MQTT](#configurações-wi-fi-e-mqtt)  
   - [Callback e Controle do LED](#callback-e-controle-do-led)  
   - [Estrutura de Tópicos](#estrutura-de-tópicos)  
6. [Como Compilar e Carregar](#como-compilar-e-carregar)  
7. [Testes e Exemplos](#testes-e-exemplos)  
8. [Estrutura de Tópicos por Cômodo](#estrutura-de-tópicos-por-cômodo)  
9. [Contribuindo](#contribuindo)  

---

## 1. Visão Geral

Este projeto utiliza um NodeMCU (ESP8266) para controle de um LED por meio de comandos via protocolo MQTT...
<!-- conteúdo continua, conforme gerado acima -->
"""

# Salva o conteúdo no arquivo
readme_path = Path("README_NodeMCU_MQTT.md")
readme_path.write_text(readme_content, encoding="utf-8")
print(f"Arquivo salvo como: {readme_path}")
