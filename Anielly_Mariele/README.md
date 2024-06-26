# Projeto NodeMCU Lolin V3

Este repositório contém um tutorial e exemplos de código para começar a trabalhar com o NodeMCU Lolin V3, um microcontrolador baseado no ESP8266, ideal para projetos de IoT.

![NodeMCU Lolin V3](link_para_imagem_do_nodeMCU)

## Conteúdo

- [Introdução](#introdução)
- [Pré-requisitos](#pré-requisitos)
- [Configuração do Ambiente](#configuração-do-ambiente)
- [Primeiro Projeto](#primeiro-projeto)
- [Contribuições](#contribuições)
- [Licença](#licença)

## Introdução

O NodeMCU Lolin V3 é amplamente utilizado devido ao seu tamanho compacto e capacidade de se conectar à internet sem fio. Este repositório oferece um guia passo a passo para iniciar com o NodeMCU Lolin V3 utilizando a plataforma Arduino IDE.

## Pré-requisitos

- Arduino IDE instalado no seu computador. Baixe em [arduino.cc](https://www.arduino.cc/en/software).
- Cabo USB micro para conectar o NodeMCU ao computador.
- Conhecimento básico de programação em Arduino.

## Configuração do Ambiente

1. **Adicionar suporte ao ESP8266**: Abra o Arduino IDE, vá em **Arquivo > Preferências** e no campo **URLs Adicionais de Gerenciamento de Placas**, adicione a URL:
     http://arduino.esp8266.com/stable/package_esp8266com_index.json
2. **Instalar o suporte ao ESP8266**: Vá em **Ferramentas > Placa > Gerenciador de Placas**, pesquise por "esp8266" e instale o pacote "esp8266" de **ESP8266 Community**.

3. **Selecionar a placa NodeMCU Lolin V3**: Em **Ferramentas > Placa**, selecione **NodeMCU 1.0 (ESP-12E Module)**.

4. **Configurar a porta**: Conecte o NodeMCU Lolin V3 ao seu computador via cabo USB. Em **Ferramentas > Porta**, selecione a porta COM correspondente ao NodeMCU.

## Primeiro Projeto

### Piscando um LED

1. Abra o Arduino IDE, cole o seguinte código e carregue no NodeMCU Lolin V3:

```cpp
void setup() {
  pinMode(LED_BUILTIN, OUTPUT); // Define o pino do LED como saída
}

void loop() {
  digitalWrite(LED_BUILTIN, HIGH); // Liga o LED
  delay(1000); // Aguarda 1 segundo
  digitalWrite(LED_BUILTIN, LOW); // Desliga o LED
  delay(1000); // Aguarda 1 segundo
}
