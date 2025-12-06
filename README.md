# lora-gönderici 
#include "LoRa_E32.h"

LoRa_E32 e32ttl(10, 11);   // (RX, TX) pinlerini kendine göre düzenle

void setup() {
  Serial.begin(9600);
  e32ttl.begin();
}

void loop() {
  String msg = "Merhaba Alıcı!";
  ResponseStatus rs = e32ttl.sendFixedMessage(44, 18, 18, msg);
  
  Serial.print("Gönderildi: ");
  Serial.println(msg);
  
  delay(1000);
}
