***
SUBSYSTEM NAME: TILLING AND PLOUGHING

***

FABRICATION PLAN: We tried to avoid the sophisticated use of the tilling and ploughing. Unlike others where the process of tilling is continous and no proper distance is maintained. In our bot we primarly focus on tilling at a particular spot and then sowing the seed. So in this process we have used acryclic sheet and with the help of laser cutting crafted it into a motor holder and fixed a tiller which is properly incarnated so as to dig the hole at the right depth in the soil. This whole process requires one DC motor which is which is controlled through a one channel relay the human intervention is possible and then this is powered through a battery.

***

SYSTEM INTERACTION DETAILS

MATERIAL INTERACTION:  The materials are properly interlinked through nuts and bolts, the DC motor is connected to the relay and is inturn attached to Aurdino Mega 2560 for easy human intervention and control through the bluetooth device.

***

PROGRAM CODE:
 int data=0;
const int trigpin=6;
const int echopin=4;
void setup() {
  Serial.begin(9600);
  pinMode(trigpin,OUTPUT);
  pinMode(echopin,INPUT);
  pinMode(5,OUTPUT);
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


  if(data=='P')
  {
    digitalWrite(5,HIGH);
    Serial.println("Tilling And Sowing started");
  }

  if(data=='O')
  {
    digitalWrite(5,LOW);
    Serial.println("Tilling And Sowing stopped");
  }
   if(data=='S')
  {
    digitalWrite(8,HIGH);
    digitalWrite(9,HIGH);
    digitalWrite(11,HIGH);
    digitalWrite(13,HIGH);
    Serial.println("STOPPED!!");
  }

}
else
{
  digitalWrite(5,LOW);
  digitalWrite(8,HIGH);
    digitalWrite(9,HIGH);
    digitalWrite(11,HIGH);
    digitalWrite(13,HIGH);
    Serial.println("STOPPED!! due to sensor");
  }
}

 