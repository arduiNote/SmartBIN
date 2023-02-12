#include <HCSR04.h>
#include <Servo.h>

#define bin_depth 13

Servo myservo;

UltraSonicDistanceSensor OpenBIN(10, 11);
UltraSonicDistanceSensor WasteLevel(6, 5);

void setup() {
  // put your setup code here, to run once:
  Serial.begin(9600);
  myservo.attach(3);
  myservo.write(0);
}

void loop() {
  // put your main code here, to run repeatedly:
  Serial.println("Current Wastelevel :");
  Serial.println(-(WasteLevel.measureDistanceCm()-bin_depth));

  if(OpenBIN.measureDistanceCm() <= 10)
  {
    myservo.write(180);
    delay(4000);
  }
  else
  {
    myservo.write(0); 
  }
  delay(500);
}







