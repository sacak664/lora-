# lora-gönderici/alıcı adressiz
void setup() {
  Serial.begin(9600);
  Serial1.begin(9600);

  Serial.println("GONDERICI HAZIR");
}

void loop() {

  if (Serial.available()) {

    String mesaj = Serial.readStringUntil('\n');

    Serial1.println(mesaj);

    Serial.print("GONDERILDI: ");
    Serial.println(mesaj);
  }
}
*******************************
void setup() {
  Serial.begin(9600);
  Serial1.begin(9600);

  Serial.println("ALICI HAZIR");
}

void loop() {

  while (Serial1.available()) {

    char c = Serial1.read();

    Serial.write(c);
  }
}
