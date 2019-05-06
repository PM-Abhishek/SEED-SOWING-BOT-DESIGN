*** 
SUBSYSTEM NAME: MOVEMENT AND OBSTACLE DETECTION 

FABRICATION PLAN: In this sprint we mainly focus on the movement and obstacle detection of the bot. For the movement the wheels are required which are run by the dc motors. two wheels in precise are attached to the dc motors and the other two are attached to the dc motor shafts which facilitate the movement and allows easy movement of the bot. all the movements are in turn attached to the Bluetooth device which is controlled by the app in the mobile. The dc motors that we have used here are 60 rpm. and is powered by the battery. It is in turn attached to the aurdino which is programmed in such a way for easy user interaction. The aurdino is programmed in such a way that the bot can move forward, backward, move left or right while moving forward or backward. the other parts that we use here are 3mm nuts and bolts, relay for machine control, bread board and jumper wires
***

***
INTERACTION ASPECT DETAILS

1)Material Interaction: Components and chassis, Arduino Mega 2560, 4 channel relay, 2 DC Motors(60 rpm), 2 DC motor shafts, Jumper Wires for connection, Bread Board, Bluetooth Module.
***
2)Data Interaction: Program uploaded on Arduino IDE and App created using MIT Inventor App through which commands can be given to move forward, backwards, right, left or stop.
***
3)Energy Interaction: 12 V Battery gives the power supply to the motors.

***
PROGRAM CODE:
 int data=0;
const int trigpin=6;
const int echopin=4;
void setup() {
  Serial.begin(9600);
  pinMode(trigpin,OUTPUT);
  pinMode(echopin,INPUT);
  pinMode(8,OUTPUT);
  pinMode(9,OUTPUT);
  pinMode(11,OUTPUT);
  pinMode(13,OUTPUT);
  
}

void loop() {
  char data;

  float duration,distance;
  digitalWrite(trigpin,LOW);
  digitalWrite(trigpin,HIGH);
  delayMicroseconds(10);
  digitalWrite(trigpin,LOW);
  duration=pulseIn(echopin,HIGH);
  distance=duration*0.017;
  Serial.println(distance);

  data=Serial.read();
  
if(distance>=11)
{
  if(data=='F')
  {
   
    
      digitalWrite(8,HIGH);
      digitalWrite(9,LOW);
      digitalWrite(11,HIGH);
      digitalWrite(13,LOW);
      Serial.println("MOVING FORWARD!!");
    
  }
  if(data=='B')
  {
    digitalWrite(8,LOW);
    digitalWrite(9,HIGH);
    digitalWrite(11,LOW);
    digitalWrite(13,HIGH);
    Serial.println("TAKING REVERSE!!");
  }
   if(data=='L')
  {
    digitalWrite(8,HIGH);
    digitalWrite(9,LOW);
    digitalWrite(11,LOW);
    digitalWrite(13,HIGH);
    Serial.println("TURNING LEFT!!");
  }
  if(data=='R')
  {
    digitalWrite(8,LOW);
    digitalWrite(9,HIGH);
    digitalWrite(11,HIGH);
    digitalWrite(13,LOW);
    Serial.println("TURNING RIGHT!!");
  }

}


 