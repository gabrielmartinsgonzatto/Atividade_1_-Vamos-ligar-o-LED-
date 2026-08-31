# IOT Atividades 

Potenciômetro + Servo Motor

Discente: Gabriel Martins Gonzatto  
Sala: TDSM5  

https://www.tinkercad.com/things/jPAUvI9Mupc-daring-duup/editel?returnTo=https%3A%2F%2Fwww.tinkercad.com%2Fdashboard%2Fdesigns%2Fall


## Enunciado: Controle do Servo Motor com Potenciômetro

O projeto utiliza um potenciômetro como entrada para controlar a posição de um servo motor como saída. Ao girar o potenciômetro, o Arduino lê o valor analógico e transforma essa leitura em um ângulo, fazendo com que o servo motor se movimente proporcionalmente.

- O Arduino lê o valor do potenciômetro pelo pino **A0**
- Controla o servo motor pelo pino **9**
- O potenciômetro permite controlar o ângulo do servo motor de aproximadamente **0° a 180°**


## 🛠️ Materiais necessários

| Qtd | Componente |
| :---: | :--- |
| 1 | Placa Arduino UNO |
| 1 | Cabo USB |
| 1 | Protoboard |
| 1 | LED |
| 1 | Push Button (Botão) |
| 2 | Resistores |
| — | Fios de jumper macho-macho |

// C++ code
//
int buttonPin = 7;
int ledPin = 10;
bool estadoLed = false;

void setup() {
pinMode (ledPin, OUTPUT);
pinMode (buttonPin, INPUT);
}

void loop() {
  if (digitalRead(buttonPin) == HIGH) {
  estadoLed = !estadoLed;
    digitalWrite(ledPin, estadoLed);
    delay(500);
  }
}
