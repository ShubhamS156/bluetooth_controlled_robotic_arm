#include<Servo.h>
int incoming_Int;
char incoming_Char;

Servo claw_Servo;
Servo wrist_Servo;
Servo elbow_Servo;
Servo should1_Servo;
Servo should2_Servo;
void claw_Active(int claw_Pos) {
  Serial.println("<<<<Claw>>>");
  claw_Servo.write(claw_Pos);
  Serial.println(claw_Pos);
}
void wrist_Active(int wrist_Pos) {
  Serial.println("<<<<Wrist>>>");
  wrist_Servo.write(wrist_Pos);
  Serial.println(wrist_Pos);
  }
  
void elbow_Active(int elbow_Pos){
 Serial.println("<<<<Elbow>>>>");
 elbow_Servo.write(elbow_Pos);
  }
  void should1_Active(int should1_Pos){
    Serial.println("<<<<First Shoulder>>>>");
    should1_Servo.write(should1_Pos);
    Serial.println(should1_Pos); 
    }
     void should2_Active(int should2_Pos){
    Serial.println("<<<<Second Shoulder>>>>");
    should1_Servo.write(should2_Pos);
    Serial.println(should2_Pos); 
    }

void setup() {
  Serial.begin(9600);
  claw_Servo.attach(9);
  pinMode(13, OUTPUT);
}
void loop() {
  if (Serial.available() > 0) {
    incoming_Char = Serial.read();
    if (incoming_Char == 'C') {
      incoming_Int = Serial.parseInt();
      claw_Active(incoming_Int);
    }
    else if (incoming_Char == 'c') {
      Serial.println("<<<<Claw Inactive>>>>");
    }
    else if (incoming_Char == 'W') {
      incoming_Int = Serial.parseInt();
      wrist_Active(incoming_Int);
    }
    else if (incoming_Char == 'w') {
      Serial.println("<<<<Wrist Inactive>>>>");
    }
    else if(incoming_Char=='E'){
      incoming_Int=Serial.parseInt();
      elbow_Active(incoming_Int);
      }
      else if(incoming_Char=='e'){
        Serial.println("<<<<Elbow Inactive>>>>");
        }
       else if(incoming_Char=='S'){
        incoming_Int=Serial.parseInt();
        should1_Active(incoming_Int);
        }
  }
}
