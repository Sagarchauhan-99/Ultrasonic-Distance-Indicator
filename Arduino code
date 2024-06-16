# define echoPin 2
# define trigPin 3

int maximumRange = 300;
int minimumRange = 00;
long duration,distance;

void setup(){
  Serial.begin(9600);
  pinMode(trigPin,OUTPUT);
  pinMode(echoPin,INPUT);
  pinMode(9,OUTPUT);
  pinMode(10,OUTPUT);
  pinMode(11,OUTPUT);
}

void loop(){
  digitalWrite(trigPin,LOW);
  delayMicroseconds(2);
  digitalWrite(trigPin,HIGH);
  delayMicroseconds(10);
  digitalWrite(trigPin,LOW);
  duration =pulseIn(echoPin,HIGH);


 distance=duration/58.2;

 if (distance >= maximumRange || distance <= minimumRange){
   Serial.println("Out of Range");
  }
 else{
  Serial.print(" Distance : ");
  Serial.print(distance);
  Serial.println(" cm");

  delay(1000); 
 }
 if(distance < 100){
  digitalWrite(11,HIGH);
  digitalWrite(10,LOW);
  digitalWrite(9,LOW);
 }

 if(distance >= 100 && distance < 200 ){
  digitalWrite(11,LOW);
  digitalWrite(10,HIGH);
  digitalWrite(9,LOW);
 }

 if(distance >= 200){
  digitalWrite(11,LOW);
  digitalWrite(10,LOW);
  digitalWrite(9,HIGH);
 }
} 
