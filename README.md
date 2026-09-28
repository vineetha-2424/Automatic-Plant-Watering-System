int sensor = A0;
int relay = 7;

void setup() {
  pinMode(relay, OUTPUT);
  Serial.begin(9600);
}

void loop() {
  int moisture = analogRead(sensor);
  Serial.println(moisture);

  // Example for active-LOW relay
  if (moisture > 600)
    digitalWrite(relay, LOW);  // Pump ON
  else
    digitalWrite(relay, HIGH); // Pump OFF

  delay(1000);
}# Automatic-Plant-Watering-System
