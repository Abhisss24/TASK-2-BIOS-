```1.	  A, LED TASK
 int a[5];
void setup() {
  // put your setup code here, to run once:
 
  a[0]=23;
  a[1]=22;
  a[2]=19;
  a[3]=18;
  a[4]=21;
  //[23,22,19,18,21]
  for (int i =0;i<5;i++){
    pinMode(a[i], OUTPUT);
  }
}

void loop() {
  // put your main code here, to run repeatedly:

  for(int b=0;b<=5;b++){
    digitalWrite(a[b], HIGH);
    delay(200);
    digitalWrite(a[b], LOW);
    delay(200);
     }
  for(int c =4;c>=0;c--){
    digitalWrite(a[c], HIGH);
    delay(200);
    digitalWrite(a[c], LOW);
    delay(200);
   }
  

  
  delay(10); // this speeds up the simulation
}
```

Firstly I initialize a array  named a contains 5 elements. The elements are the output pins of the ESP32, and using a for loop initialized that array of a is the output for the ESP32 .
The ouput pins are connected to the each leds in a specific order .And used a for loop for repetition of blinking of led in a specific order firstly light up a led and turn off the led
and set a delay of 200ms for light up and turn off . The first loop is for light up right to left and used a another for loop for blink the light from left to right .Used the digitalwrite(high)
to light up and for turn off use the digitalwrite(low).
Connection : All the led’s anode is connected to the ESP32’s output pins.And the led’s cathode is connected to the resistors and then connected to the ground.
