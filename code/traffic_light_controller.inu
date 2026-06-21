// C++ code
enum TrafficState {
  RED,
  GREEN,
  YELLOW
};

int redPin = 8;
int yellowPin = 9;
int greenPin = 10;
int buttonPin =2;

TrafficState currentState;
unsigned long stateStartTime;

bool pedestrianRequest = false;
bool lastButton = HIGH;


void setup() {
pinMode(redPin,OUTPUT);
  pinMode(yellowPin,OUTPUT);
  pinMode(greenPin,OUTPUT); 
  pinMode(buttonPin,INPUT_PULLUP);
currentState = RED;
stateStartTime = millis();
}

void loop() {
  bool button = digitalRead(buttonPin);


  if(lastButton =HIGH && button == LOW) {
  pedestrianRequest = true;
}

  switch(currentState) {

      case RED : 
digitalWrite(redPin,HIGH);
digitalWrite(yellowPin,LOW);
digitalWrite(greenPin,LOW);
if(millis() - stateStartTime >= 5000) {
currentState = GREEN;
stateStartTime = millis();
}
break ;
     case GREEN :
digitalWrite(redPin,LOW);
digitalWrite(greenPin,HIGH);
digitalWrite(yellowPin,LOW);
if(pedestrianRequest == true && millis() - stateStartTime >= 2000) {
      currentState = YELLOW;
      stateStartTime = millis();
      pedestrianRequest = false;
    }
 else if(millis() - stateStartTime >= 5000) {
      currentState =YELLOW;
      stateStartTime = millis();
    }
break;
    case YELLOW :
digitalWrite(redPin,LOW);
digitalWrite(greenPin,LOW);
digitalWrite(yellowPin,HIGH);
if(millis() - stateStartTime >= 2000) {
currentState =RED;
stateStartTime = millis();

}
break;

}
}
