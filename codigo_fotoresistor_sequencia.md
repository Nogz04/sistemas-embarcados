```c#
// Definição dos pinos baseados na sua montagem
const int pinoLDR = A0;
const int ledVerde = 11;
const int ledAmarelo = 12;
const int ledVermelho = 13;

void setup() {
  // Inicia a comunicação serial para podermos ler os valores do sensor
  Serial.begin(9600);
  
  // Configura os pinos dos LEDs como saída de energia
  pinMode(ledVerde, OUTPUT);
  pinMode(ledAmarelo, OUTPUT);
  pinMode(ledVermelho, OUTPUT);
}

void loop() {
  // Lê o valor do sensor LDR (varia de 0 a 1023)
  int valorLDR = analogRead(pinoLDR);
  
  // Mostra o valor no Monitor Serial para ajudar na calibração
  Serial.print("Nivel de luz: ");
  Serial.println(valorLDR);

  // Desliga todos os LEDs antes de verificar a luz
  digitalWrite(ledVerde, LOW);
  digitalWrite(ledAmarelo, LOW);
  digitalWrite(ledVermelho, LOW);

  // Lógica de acendimento baseada no valor da luz
  // ATENÇÃO: Você pode precisar ajustar os números 300 e 600
  // dependendo da claridade do seu ambiente!
  
  if (valorLDR < 300) {
    // Se a luz for menor que 300 (Escuro)
    digitalWrite(ledVermelho, HIGH);
    
  } else if (valorLDR >= 300 && valorLDR < 600) {
    // Se a luz estiver entre 300 e 600 (Meia luz/Sombra)
    digitalWrite(ledAmarelo, HIGH);
    
  } else {
    // Se a luz for maior que 600 (Claro)
    digitalWrite(ledVerde, HIGH);
  }

  // Pequena pausa para estabilizar a leitura
  delay(100);
}
```
