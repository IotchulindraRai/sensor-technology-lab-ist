# sensor-technology-lab-ist
iThis reprository contain lab of  1,2,3,4,5 lab of 5th  semenster 
#ultrasonic lab c++ code:

Program:-

#define pingTrig 6
#define pingEcho 7
#define ldrvalue 0

int led = 13 ; void setup()
{Serial.begin(9600); pinMode(pingTrig, OUTPUT); pinMode(pingEcho, INPUT); delay(200);
pinMode(led, OUTPUT);
}

void loop()
{
long duration, inches, cm,value; digitalWrite(pingTrig, LOW); delayMicroseconds(2); digitalWrite(pingTrig, HIGH); delayMicroseconds(10); digitalWrite(pingTrig, LOW);

duration = pulseIn(pingEcho, HIGH);

cm = duration / 29 / 2; inches=cm/2.5;

Serial.print("-->");Serial.println(cm); Serial.print("-->");Serial.println(inches); if(cm < 30 )
{
digitalWrite(led,HIGH); delay(200); digitalWrite(led,LOW); delay(200);
}}

#for temperature sensor
int val; 
int tempPin = 1; 
 
void setup() 
{ Serial.begin(9600); 
} 
void loop() 
{ 
val = analogRead(tempPin); float mv = ( val/1024.0)*5000; float cel = mv/10; 
float farh = (cel*9)/5 + 32; float kel=273+cel; 
Serial.print("TEMPRATURE in Celsius= "); Serial.print(cel); 
Serial.print("*C"); Serial.println(); delay(1000); 
Serial.print("TEMPRATURE in Fahrenheit = "); Serial.print(farh); 
Serial.print("*F"); Serial.println(); 
Serial.print("TEMPRATURE in Kelvin = "); Serial.print(kel); 
Serial.print("*k"); 
Serial.println();
delay(1000); 
} 
 
