5. BARE METAL BASICS
 Void setup(){
DDRB=32;
}
Void loop(){
PORTB=32;
Delay(1000);
PORTB=0;
Delay(1000);
}

This code is used to blink the led in bare metal . In this I used ARDUINO NANO. In this each point have different values.For example the point PB0 the value becomes 2 
raise to 0 ie; 1 the point PB5 becomes 32. In this bare metal the led is connected to the point PB5 that’s why in this code DDRB becomes 32 and get the output through portb =32 .


Connection: The point of PB5 is connected to the resistor and then connected to the led .The cathode is connected to the GRN of the Arduino.
