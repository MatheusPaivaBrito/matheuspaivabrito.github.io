# Sistema para Vinícola

## Visão geral

O **Sistema para Vinícola** é um projeto de monitoramento em tempo real desenvolvido para acompanhar a temperatura de barris em uma operação de vinícola.

O projeto foi desenvolvido integralmente de forma independente, cobrindo desde a integração com o hardware até o backend, frontend, comunicação em tempo real e hospedagem em nuvem.

A solução utiliza sensores físicos conectados a uma placa **ESP32/M5Stack**, comunicação via **MQTT**, backend em **Python com Flask**, frontend em **React** e infraestrutura em nuvem na **Google Cloud**.

A proposta principal é permitir que a temperatura dos barris seja coletada automaticamente e exibida em uma interface web, facilitando o acompanhamento operacional e reduzindo a dependência de verificações manuais.

!!! warning "Projeto em reformulação"
    Este projeto está atualmente em reforma. A versão pública será disponibilizada como uma demonstração controlada, utilizando dados mockados para simular as leituras dos sensores sem depender do ambiente físico real.

---

## Contexto

Em uma vinícola, o controle de temperatura é uma informação importante para acompanhar condições de armazenamento, fermentação e operação dos barris.

Antes de uma solução automatizada, esse tipo de acompanhamento pode depender de verificações manuais, registros separados ou medições sem visualização centralizada.

Este projeto foi criado para explorar uma solução de monitoramento baseada em **IoT**, permitindo que sensores físicos enviassem dados para um servidor em nuvem e que essas informações fossem exibidas em uma aplicação web.

---

## Problema

O acompanhamento manual de temperatura pode gerar dificuldades como:

- falta de visualização em tempo real;
- dependência de medições manuais;
- dificuldade para centralizar dados;
- menor agilidade para identificar variações;
- ausência de histórico organizado;
- pouca integração entre sensores físicos e sistemas web.

---

## Solução

Foi desenvolvido um sistema capaz de coletar temperaturas por meio de sensores conectados a uma placa ESP32/M5Stack e enviar essas informações para um servidor utilizando comunicação MQTT.

No backend, os dados eram recebidos, processados e disponibilizados para o frontend. A interface web permitia visualizar as temperaturas dos barris em tempo real, oferecendo uma visão clara do ambiente monitorado.

A versão pública do projeto será adaptada para rodar com **dados mockados**, simulando leituras de temperatura sem expor credenciais, endpoints privados ou depender dos sensores físicos.

---

## Minha atuação

Este projeto foi desenvolvido totalmente por mim, de ponta a ponta.

Minha atuação envolveu todas as etapas técnicas da solução, incluindo hardware, comunicação, backend, frontend e cloud.

As principais responsabilidades foram:

- integração da ESP32/M5Stack com sensor de temperatura;
- uso do sensor **DS18B20** para leitura de temperatura;
- configuração do envio de dados utilizando **MQTT**;
- desenvolvimento do backend em **Python com Flask**;
- criação da integração entre o backend e o fluxo de dados vindo dos sensores;
- desenvolvimento do frontend em **React**;
- exibição das temperaturas em tempo real na interface web;
- configuração do ambiente em nuvem na **Google Cloud**;
- organização da arquitetura da solução;
- preparação do projeto para futura demonstração pública com dados mockados.

Esse projeto demonstra minha capacidade de construir uma solução completa, conectando dispositivos físicos a uma aplicação web funcional.

---

## Tecnologias utilizadas

- Python
- Flask
- React
- MQTT
- ESP32
- M5Stack
- Sensor DS18B20
- Google Cloud
- IoT
- Dados em tempo real

---

## Arquitetura em alto nível

```text
Sensor DS18B20
        ↓
ESP32 / M5Stack
        ↓
Comunicação MQTT
        ↓
Servidor em nuvem
        ↓
Backend Flask
        ↓
Frontend React
        ↓
Dashboard em tempo real
```

---

## Fluxo de funcionamento

```text
Leitura da temperatura no barril
        ↓
Envio dos dados pelo dispositivo IoT
        ↓
Recebimento das mensagens via MQTT
        ↓
Processamento no backend
        ↓
Disponibilização para a interface web
        ↓
Visualização em tempo real pelo usuário
```

---

## Demonstração pública

A versão pública do projeto será apresentada como uma demonstração controlada, utilizando dados simulados para representar o comportamento do sistema.

Essa abordagem permite demonstrar a arquitetura, a interface e o funcionamento geral da solução sem depender dos sensores físicos ou expor configurações privadas do ambiente original.

A demonstração poderá incluir:

- dashboard com temperaturas simuladas;
- atualização visual em tempo real;
- identificação de barris ou pontos monitorados;
- histórico fictício de leituras;
- alertas simulados de variação de temperatura;
- interface web navegável;
- backend preparado para receber dados reais futuramente.

---

## Impacto técnico

O projeto demonstra a construção de uma solução completa envolvendo hardware, comunicação entre dispositivos, backend, frontend e cloud.

Mais do que uma aplicação web tradicional, o sistema mostra a integração entre o mundo físico e o digital, permitindo que dados capturados por sensores sejam enviados, processados e visualizados em tempo real.

Esse tipo de solução é aplicável em cenários de monitoramento industrial, agrícola, logístico e operacional, onde sensores precisam alimentar sistemas de acompanhamento e decisão.

---

## Competências demonstradas

- Desenvolvimento completo de solução ponta a ponta
- Desenvolvimento backend com Flask
- Desenvolvimento frontend com React
- Integração com dispositivos IoT
- Comunicação via MQTT
- Leitura de dados com sensor DS18B20
- Uso de ESP32/M5Stack
- Deploy e integração com Google Cloud
- Processamento de dados em tempo real
- Construção de dashboard operacional
- Organização de arquitetura
- Preparação de ambiente demonstrativo com dados mockados

---

## Status do projeto

O projeto está atualmente em reformulação.

A próxima versão pública será adaptada para funcionar com dados mockados, permitindo demonstrar a experiência de uso e a arquitetura da solução sem depender do hardware físico.

---

## Repositório

Em breve.

---

## Demonstração

Em breve.