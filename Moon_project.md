## Criteria A: Planning

### Context of the problem
This project is a program to communicate between the earth and the moon in signals. Focusing on the earth's side sending messages to the moon's side, our program inputs English text on an LCD and outputs messages in Morse Code using an LED. We will dispose of:

* 1 LED
* 2 Buttons
* Arduino
* Circuits components
* 1 LCD

### Justification of the solution

We will create a program dsiplayed on 1 LED and 1 LCD which gets inputs by pressing 2 buttons. As for hardware, we are using 1 LED, 1 LCD, 2 buttons and an Arduino. The product enables us to input messages in English using the right button to cycle through the English alphabet and 2 commands "SEND" and "DELETE". The left button enables us to select letters or commands. The message, then, is converted into Morse Code which is displayed through an LED. Moreover, we will be using C++ as a software language since it is the primary coding language for the Arduino and we have had practise sessions during class in that language. In fact in 2017, C++ ranked 4th among 24 other programming languages in September [1] due to its fast processing and several built-in functions. The program will be first run on the simulator Tinkercad to avoid damaging the physical components when testing the solution.

[1] Ramasubramanian, Sowmya. “C++ Is Now the Fastest-Growing Programming Language, Report Says.” The Hindu, The Hindu, 11 Sept. 2020, www.thehindu.com/sci-tech/technology/c-is-now-the-fastest-growing-programming-language/article32580426.ece.

T.E.L.O.S. Study:<br>
T-Technical-Is the project technically possible? ... We dispose of a computer, Arduino, TinkerCat simulator, Arduino IDE for C++ code and circuits components. All technical necessities for this project are satisfied.<br>
E-Economic- Can the project be afforded? Will it increase profit? ... This project is developed for free by UWC ISAK Japan students. Thanks to the funding provided to our school, we can afford all of the components necessary for the project. We also have a budget of 1 trillion moons according to our client.<br>
L-Legal- Is the project legal? ... The project is completely legal as the 1947 Japanese constitution does not criminalize small digital projects like ours.<br>
O-Operational- How will the current operations support the change? ... The project will operate on computers and Arduino. The process does not have any errors and is perfectly operational.<br>
S-Scheduling- Can the project be done in time? ... We are given 3 weeks to complete this project and the tasks have been regularly distributed to assure that it is completed by Friday, December 18th, 2020.


### Sucess Criteria
- The product allows the user to enter messages in English and send messages in Morse Code.
- The product contains all the alphabet and numbers
- The product contains special commands like send and delete
- The display uses maximum 1 LED, 1 LCD and 2 buttons.

## Criteria B: Design



### System Diagram

![Arduino_moon_system diagram  001](https://user-images.githubusercontent.com/60457723/103166503-f25cd900-4865-11eb-812c-b29b08023c25.jpeg)

Input: Users are able to enter the alphabet using two buttons (A and B) installed on the breadboard, and the LCD displays whats input afterwards.
One is to change the characters, one is to select the options (it includes "send" and "delete")

Output: Morse code, the detailed system of dots and dashes used to represent the alphabets, is transferred to the LED so that we can instantly know what the messages are. 

![international morse code](https://user-images.githubusercontent.com/60457723/103167080-677edd00-486b-11eb-8745-b39f15ff4b5c.png)



### Prototype on TinkerCad
<img width="1217" alt="Screen Shot 2020-12-18 at 16 44 50" src="https://user-images.githubusercontent.com/60457723/102588375-b1234580-4150-11eb-8473-04623dab7774.png">

The screenshot above shows each components and the program
TinkerCad, a free online service for creating a digital prototypes of components, is commonly used for rapid prototyping before buiding a physical circuit. Due to well-visualized platform for all developers and commonly used all over the world, our initial online prototype is done by tinkerCad. Eventhough this is just a beggining of the project, prototyping, the most important phase, is indispensable in order to instantly modify the program. Once online circuit is built and working properly, we manually started buidling a physical circuit using a digital arduino as a reference - connects all wires, installs all components on a breadboad, copies and upload the code on Arduino, andd make sure that LCDS lights up clearly (because LED is relatively fragile).

### Flow chart


## Criteria C: Development



```.c++
// include the library code:
#include <LiquidCrystal.h>
int index = 0; 
// add all the letters and digits to the keyboard
String keyboard[]={"SEND", "DEL","A", "B", "C", "D","E","F","G","H","I","J","K","L","M","N","O","P","Q","R","S","T","U","V","W","X","Y","Z"};
String text = "";
int numOptions = 28;

// definitions of components
int led=10;
int btn_right=2;
int btn_left=3;
  
// initialize the library with the numbers of the interface pins
LiquidCrystal lcd(12, 11, 5, 4, 9, 8);

void setup() {
  // set up the LCD's number of columns and rows:
  lcd.begin(16, 2);
  Serial.begin(9600);
  // Print a message to the LCD.

  // These two commands create interruptions for the buttons.
  // Interruptions are a way of telling the arduino to pay 
  // attention to specific events, in this case the buttons
  attachInterrupt(0, changeLetter, RISING);//button A in port 2
  attachInterrupt(1, selected, RISING);//button B in port 3
  pinMode(13, OUTPUT);
}

void loop() {
  // set the cursor to column 0, line 1
  // (note: line 1 is the second row, since counting begins with 0):
  lcd.clear();
  lcd.setCursor(0, 0);
  lcd.print(keyboard[index]);
  lcd.setCursor(0, 1);
  lcd.print(text);
  delay(100);
}

//This function changes the letter in the keyboard
void changeLetter(){
   index++;
//check for the max row number
  if(index==numOptions){
    index=0; //loop back to first row
  } 
}

//this function adds the letter to the text or send the msg
void selected(){
  String key = keyboard[index];
  if (key == "DEL")
  {
      int len = text.length();
      text.remove(len-1);
  }
  else if(key == "SEND")
  {
      En2Morse();
  }
  else{
      text += key;
  }
      index = 0; //restart the index

}
// definition of the dash and dot functions for the Morse Language
void dash(){
    Serial.println("sending a dash");
    digitalWrite(led, HIGH);
    Serial.println("led on");
    delay(200000);
    digitalWrite(led, LOW);
    Serial.println("led off");
    delay(200000);
}

void dot(){
    Serial.println("sending a dot");
    digitalWrite(led, HIGH);
    Serial.println("led on");
    delay(20000);
    digitalWrite(led, LOW);
    Serial.println("led off");
    delay(20000);
}

// equivalent of the English alphabet in Morse Code
void En2Morse(){
  Serial.print(text);
  for(int i=0; i<text.length(); i++){
    if(text[i]=='A'){
    dot();
    dash();}    
    else if(text[i]=='B'){
    dash();
    dot();
    dot();
    dot();}
    else if(text[i]=='C'){
    dot();
    dot();
    dot();}
    else if(text[i]=='D'){
    dash();
    dot();
    dot();}
    else if(text[i]=='E'){
    dot();}
    else if(text[i]=='F'){
    dot();
    dash();
    dot();}
    else if(text[i]=='G'){
    dash();
    dash();
    dot();}
    else if(text[i]=='H'){
    dot();
    dot();
    dot();
    dot();}
    else if(text[i]=='I'){
    dot();
    dot();}
    else if(text[i]=='J'){
    dash();
    dot();
    dash();
    dot();}
    else if(text[i]=='K'){
    dash();
    dot();
    dash();}
    else if(text[i]=='L'){
    dot();
    dash();
    dot();
    dot();}
    else if(text[i]=='M'){
    dash();
    dash();}
    else if(text[i]=='N'){
    dash();
    dot();}
    else if(text[i]=='O'){
    dash();
    dash();
    dash();}
    else if(text[i]=='P'){
    dot();
    dash();
    dash();
    dot();}
    else if(text[i]=='Q'){
    dash();
    dash();
    dot();
    dash();}
    else if(text[i]=='R'){
    dot();
    dash();
    dot();}
    else if(text[i]=='S'){
    dot();
    dot();
    dot();}
    else if(text[i]=='T'){
    dash();}
    else if(text[i]=='U'){
    dot();
    dot();
    dash();}
    else if(text[i]=='V'){
    dot();
    dot();
    dot();
    dash();}
    else if(text[i]=='W'){
    dot();
    dash();
    dash();}
    else if(text[i]=='X'){
    dash();
    dot();
    dot();
    dash();}
    else if(text[i]=='Y'){
    dash();
    dot();
    dash();
    dash();}
    else if(text[i]=='Z'){
    dash();
    dash();
    dot();
    dot();}
  }
  
}

```

## Criteria D: Functionality

![moon project](https://user-images.githubusercontent.com/60457723/102588441-cbf5ba00-4150-11eb-8bf1-18653708faee.jpg)

## Criteria E: Evaluation

