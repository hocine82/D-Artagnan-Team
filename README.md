D-Artagnan-Team
===============

A-pod Hexapod
H

//Hocine Hamidouche
#include <Servo.h> 
 
void setup() 
{ 
  Serial.begin(115200); // begin communication
  while(!Serial){ ;} // wait while connecting
} 
 
void loop() 
{   
Serial.println("#12P1888");
Serial.println("#13P646");
Serial.println("#147733");
Serial.println("#28P1267");
Serial.println("#29P1160");

//Open the grippers to grab an object
Serial.println("#28P1092");//open the
Serial.println("#29P1335");//the grippers
  delay(4000);//wait for 4 seconds to grab an object
Serial.println("#28P1257");// Close 
Serial.println("#29P1189");// the grippers
  delay(1000);
  
//Move the grippers horizontally
Serial.println("#12P1481");//swing to the left
  delay(1000);
Serial.println("#12P2180");//swing to the right
  delay(1000);
Serial.println("#12P1888");//swing to the middle
  delay(1000);

//Move the grippers vertically
Serial.println("#14P1354");//move up
  delay(1000);
Serial.println("#14P2296");//move down
  delay(1000);
Serial.println("#14P1733");//move to the middle
  delay(1000);

//Rotate the grippers
Serial.println("#13P1704");// rotate on the clockwise direction
  delay(1000);
Serial.println("#13P646");// rotate on the opposite direction
    // delay(2000);
} 
