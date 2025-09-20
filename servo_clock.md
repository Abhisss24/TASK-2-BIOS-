```4. Servo clock
#include <ESP32Servo.h>
Servo abhi1;
Servo abhi2;
void setup() {
  // put your setup code here, to run once:
  abhi1.attach(23);
  abhi2.attach(22);
  Serial.begin(115200);
  Serial.println("Hello, ESP32!");
}

void loop() {
  float x=0;
  int y=0;
  // put your main code here, to run repeatedly:
 if (Serial.available()>0){
   int hour=Serial.parseInt();
   if (Serial.available()){
      int mins=Serial.parseInt();
      x=hour*15;
      y=mins*3;
      abhi1.write(x);
      abhi2.write(y);
   }
  }
 }
```
I included one libraries named “ESP32SERVO” and used a servo variables  as  abhi1 for the  hour hand and abhi2 for the mins hand and initialized the position of the ESP32 as servo variable
with  the output point (abhi1.attach(point)).Give an option to the user to input the time to show it in servo motor . The input must be in the format hour _mins(hour space mins) . If the user
input 6 30 it will convert into the angle in the servo and shown in the servo clock ie, multiply the hour with the 15 to get the angle in servo and multiply the mins with 3 to get the angle of
the mins servo and give the data to the servo by variable name with write with the value.(abhi1.write(x). 

Connection : The PWN point of both servo’s is connected to the output points of ESP32 also the GRN of both servos is connected to the ESP 32 ‘s ground .The power of both servo’s is connected 
to the 5v of ESP32  .
