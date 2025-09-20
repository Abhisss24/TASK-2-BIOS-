```1.B, LED REPRESENTATION FOR BINARY NUMBERS.
     int a[5];
 int x[10][5]={
  {0,0,0,0,0},
  {0,0,0,0,1},
  {0,0,0,1,0},
  {0,0,0,1,1},
  {0,0,1,0,0},
  {0,0,1,0,1},
  {0,0,1,1,0},
  {0,0,1,1,1},
  {0,1,0,0,0},
  {0,1,0,0,1}
 };
 
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

  for(int b=0;b<10;b++){
    for(int c=0;c<5;c++){
      if (x[b][c]==1) {
        digitalWrite(a[c], HIGH);
        delay(200);
      }
    }
    for(int d=0;d<5;d++){
    digitalWrite(a[d], LOW);
    delay(200);
    }
 }
  
}
```

Firstly I initialize a list named a contains 5 elements, also initialize a set contains 10 elements in each set contains 5 elements.And the 5 elements were the binary representation
for each number till 9. The list a contains the output pins of the ESP32 and the outpins are connected to the each leds in a order . And introduced a for loop  and inside the loop used
another loop . Used the array to define it as variable [][] so that and compare each element to 1 if the element is 1 then set to light up that led’s position . And turn off all the
led’s and repeat the for loop .
Connection : All the led’s anode is connected to the ESP32’s output pins.And the led’s cathode is connected to the resistors and then connected to the ground.
