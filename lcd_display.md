3. LCD DISPLAY
    Here I used a 9v battery , a potentiometer , resistors , dip switches (for input to the lcd screen, resistors, on off slide switches  for the connections.
The lcd connections are VSS is connected to the GND (ground) and the VDD is the power connection .
The dip switches are connected to the LCD through DB0 to DB7 (total 8 slots) which is used to input 8 bits of character. All the connections of the dip switches 
are short circuited to a single one and connected to the battery’s  positive terminal .The other side of the connection is to the resistors and it is then connected 
to the GND of the LCD. The anode(-ve) of the battery to the GND of the LCD .The potential meter’s terminal one is connected to the anode (-ve ) and the terminal 2 is
connected to the cathode(+ve) of the battery. The centre pin of the potential meter is connected to the contrast of the LCD. The slider switch’s centre pin is connected
to the Resister select .The both side of then is connected to the anode and cathode of battery respectively. 
The another slider switch is connected to the Enable of the LCD to the centre pin . The both side is connected to +ve and -ve of battery .But here we use only 4 bit .And
the LCD’s +ve and _ve to the respective battery +and-ve.
 At  the time of inputting first divide the binary of the character into two for eg: the binary is  01001000. We divide it as 2 as 0100 and 1000.And the method of input is 
first we turn off the slide switch and enter the set of binary at first that is 0010 0000 and turn the other slider switch on and off then change the binary as 0000 0000 in
the position as 01234567. And then 00010000 ,00000000 ,00100000 ,00000000 , 11000000.After that we need to on the first slider switch to on position. And change the RS slider
to on position and enter the character 4bit code .The binary code for H is 01001000.Then divide it into 2 ie; 0100 and 1000 . We input the 4bit in the position of 1 as on position
of dip switch 0100 as the position 4321 in the dip switches and all other switches as off position after completing 2 such input one character will show .
