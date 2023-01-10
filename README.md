# Home-Automation
home automation controlling with my android phone
#include <SoftwareSerial.h>
SoftwareSerial bluetooth(10,11);
String data;
void setup() {
  for(int i = 2;  i <=5;  i++){
    pinMode(i,OUTPUT);
  }
  Serial.begin(9600);
  bluetooth.begin(9600);
}
void loop() {
  if(bluetooth.available()){
  data=bluetooth.readString();
  Serial.println(data);
  
  if (data== "cat" ){
     digitalWrite(2,HIGH);
  }
        
  if (data== "dog" ){
     digitalWrite(3,HIGH);
  }
  
  
  if (data== "elephant" ){
     digitalWrite(4,HIGH);
  }
        
  if (data== "tiger" ){
     digitalWrite(5,HIGH);
  }     
  
        
  if (data== "lion" ){
     digitalWrite(2,LOW);
  }
        
  if (data== "mat" ){
     digitalWrite(3,LOW);
  }      
  if (data== "rat" ){
     digitalWrite(4,LOW);
  }
        
  if (data== "tag" ){
     digitalWrite(5,LOW);
  }      
  }
}
