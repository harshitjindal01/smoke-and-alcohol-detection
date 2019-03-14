int analogpin = A0;
int SensorValue = 0;

void setup() {
  Serial.begin(9600);
  pinMode(analogpin , INPUT);
  Serial.println("using Smoke Sensor with Arduino");
  Serial. println("coding by harshit jindal");
  Serial.println();
}

void loop() {

  SensorValue = analogRead(analogpin);
  Serial.println(SensorValue);
  delay(500);
  if(SensorValue>200)
  {
    Serial.println("safe");
  }
  if(SensorValue<250)
  {
    Serial.println("smoke detected");
  }
}
