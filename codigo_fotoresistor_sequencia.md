```c#
// Pinos baseados na sua montagem
const int pinoLDR = A0;
const int ledVerde = 11;
const int ledAmarelo = 12;
const int ledVermelho = 13;

void setup() {
  Serial.begin(9600);
  pinMode(ledVerde, OUTPUT);
  pinMode(ledAmarelo, OUTPUT);
  pinMode(ledVermelho, OUTPUT);
}

void loop() {
  int valorLDR = analogRead(pinoLDR);
  
  Serial.print("Nivel de luz: ");
  Serial.println(valorLDR);

  // Primeiro, apagamos todos os LEDs no início de cada ciclo.
  // Se estiver totalmente escuro, ele vai pular todos os 'if' abaixo e os LEDs continuarão apagados.
  digitalWrite(ledVerde, LOW);
  digitalWrite(ledAmarelo, LOW);
  digitalWrite(ledVermelho, LOW);

  // Lógica de "Barra de Progresso"
  // (Lembre-se de ajustar os valores 200, 500 e 800 conforme o Monitor Serial do seu quarto!)

  if (valorLDR > 100) {
    // Se tiver um pouquinho de luz, acende o Verde
    digitalWrite(ledVerde, HIGH); 
  }
  
  if (valorLDR > 300) {
    // Se a luz aumentar mais, acende o Amarelo (o Verde continua aceso porque também é > 200)
    digitalWrite(ledAmarelo, HIGH); 
  }
  
  if (valorLDR > 500) {
    // Se estiver muito claro, acende o Vermelho (agora os 3 estarão acesos!)
    digitalWrite(ledVermelho, HIGH); 
  }

  delay(100);
}

```
