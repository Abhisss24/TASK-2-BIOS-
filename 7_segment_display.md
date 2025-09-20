``` 2.  7-Segment Display
int a[10][7]={
  {1,1,1,1,1,1,0},
  {0,1,1,0,0,0,0},
  {1,1,0,1,1,0,1},
  {1,1,1,1,0,0,1},
  {0,1,1,0,0,1,1},
  {1,0,1,1,0,1,1},
  {1,0,1,1,1,1,1},
  {1,1,1,0,0,0,0},
  {1,1,1,1,1,1,1},
  {1,1,1,0,0,1,1}
};
int point[]={15,2,4,5,14,19,21};
void setup() {
  // put your setup code here, to run once:
  Serial.begin(115200);
  Serial.println("Hello, ESP32!");
  for (int i=0;i<8;i++){
    pinMode(point[i], OUTPUT);
  }
}

void loop() {
  // put your main code here, to run repeatedly:
  for(int b=0;b<10;b++){
    for (int c =0;c<7;c++){
      if (a[b][c]==1){
        digitalWrite(point[c], LOW);
      }
      else{
        digitalWrite(point[c], HIGH);
      }
  }
  delay(1000);
  }
   // this speeds up the simulation
}
```

In this task I used array contains 10 elements in each 7 entities are there .Then initialized the output points of the ESP32 then used pinmode output command for the each output points 
of microcontroller .Used a for loop and inside that loop used another for loop and to get the each elemnts in the array used the array variable with[][] for get the element .Compared
each element of the array with 1 if it found to be 1 then light it up and the other’s turn off as it.(In this the anode and cathode connection is inverted so I turned to turn off when 
the element becomes 1 and turn on when it is turn off ).In this the each position of the 7 segment display have different name like (a-g) we need to identify it by a-g.I set the array
like that the position of 1 be set as in (0,1,1,0,0,0,0).
Connection : The common point of the 7 segment display is connected to the resistor and then connected to the 3V3 (on board voltage regulator) . The each point of the display is connected 
to the output points of the ESP32 .
