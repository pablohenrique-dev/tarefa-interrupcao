# Sistema de Interrupções e Controle de LEDs com BitDogLab

Este projeto explora o uso de interrupções no microcontrolador RP2040 e a funcionalidade da placa BitDogLab para manipular LEDs comuns e LEDs endereçáveis WS2812.

## 🔧 Componentes Utilizados

- **Placa de desenvolvimento**: BitDogLab (RP2040)
- **Matriz de LEDs WS2812**: 5x5 (endereçáveis) conectada à GPIO 7
- **LED RGB**: conectado às GPIOs 11, 12 e 13
- **Botões**:
  - **Botão A**: conectado à GPIO 5
  - **Botão B**: conectado à GPIO 6

## 🛠️ Funcionamento do Sistema

1. O **LED vermelho** do LED RGB deve piscar continuamente 5 vezes por segundo.
2. O **botão A** incrementa o número exibido na matriz de LEDs.
3. O **botão B** decrementa o número exibido na matriz de LEDs.
4. A **matriz de LEDs WS2812** exibe números de 0 a 9 em um formato fixo ou estilizado, desde que legível.

## 📜 Implementação

O código utiliza:

- **Interrupções** para capturar eventos de pressionamento dos botões.
- **Debounce via software** para evitar leituras incorretas dos botões.
- **Uso de resistores de pull-up internos** para os botões de acionamento.

## 📌 Configuração dos Pinos

| Componente         | GPIO |
| ------------------ | ---- |
| Matriz WS2812      | 7    |
| LED Vermelho (RGB) | 11   |
| LED Azul (RGB)     | 12   |
| LED Verde (RGB)    | 13   |
| Botão A            | 5    |
| Botão B            | 6    |

## Como Rodar o Projeto

### Pré-requisitos:

- **Extensão Raspberry Pi Pico** instalada no ambiente de desenvolvimento.
- **Extensão Wokwi** para simulação no VSCode.

### Passos para Compilar e Executar o Código:

1. **Compilar o código**:

   - Clique no botão **Compile** na parte inferior da tela.
   - Após a compilação, abra o arquivo `diagram.json`.

2. **Simulação**:

   - Execute a simulação para visualizar o comportamento dos LEDs e botões no ambiente virtual do Wokwi.

3. **Executar na Placa BitDogLab**:
   - Coloque a placa em **modo BOOTSEL** (mantenha pressionado o botão BOOTSEL enquanto conecta ao computador).
   - Transfira o código compilado para a placa e execute-o.

Agora seu projeto está pronto para explorar o funcionamento de interrupções e controle de LEDs com a BitDogLab! 🚀

## Vídeo sobre o projeto

[Link do vídeo](https://youtu.be/kcPQGhOJCg0)
