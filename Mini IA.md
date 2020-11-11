# Unit2

## Criteria A: Planning
#### Context of the problem


#### Justification of the solution



#### A sketch of the whole idea
![seven](https://user-images.githubusercontent.com/60457723/98828206-24170d80-247b-11eb-9fc8-965dcb34a729.jpg)


#### Criteria for success
1. Provides correct outputs to show every numbers using 7 LEDs. (This leads to the usablity)
2. There are no bugs in the code.
3. Decent speed of responces to avoid letting user be frustrated. 
4. Brightness of the LED is precisely adjusted to inidicate outputs properly.


## Criteria B: Design

### Record of Tasks
The procedure of the project follows the task plan below:

| Task No |                                                    Planned Action                                                    |                                           Planned  Outcome                                           | Time Estimated | Target Completion Date  | Criterion |
|:-------:|:--------------------------------------------------------------------------------------------------------------------:|:----------------------------------------------------------------------------------------------------:|:--------------:|:-----------------------:|:---------:|
|    1    |                               Planning: Discuss what the problem is and its solutions.                               |                                    Write a context of the problem                                    |       1h       |        2020/11/3        |     A     |
|    2    |                               Planning: Create rough sketches of an idea from scratch.                               |                             Visualize what the brief idea is on the paper                            |       1h       |        2020/11/3        |     A     |
|    3    |                                     Design: Create a online circuit on TinkerCad.                                    |                                  Connects all the wires on TinkerCad                                 |       2h       |        2020/11/5        |     B     |
|    4    |               Design: Create a system diagram shows how Arduino works and the flowchart of the program.              | 1 system diagram and 1 flowchart as an example of the entire code.(there are 9 flowcharts in total)  |     1h30min    |        2020/11/6        |     B     |
|    5    |                                      Design: Create a truth table for the LEDs.                                      |                                                                                                      |       1h       |        2020/11/6        |     B     |
|    6    |                  Design: Create K-maps for each LEDs and figure out what the boolean equations are.                  |                                    7 K-map and 7 boolean equations                                   |       2h       |        2020/11/6        |     B     |
|    7    | Development: Complete entire program and make sure that the program works properly using TinkerCad online simulator. |                                                                                                      |     2h30min    |        2020/11/8        |     C     |
|    8    |                                    Development: Build an actual Arduino platform                                     |                        Connects all stuff to Arduino (LEDs are on cardboard)                         |       3h       |        2020/11/10       |     C     |
|    9    |                                                                                                                      |                                 

### System Diagram
![Compsci_miniIA_systemdiagram 001](https://user-images.githubusercontent.com/60457723/98455432-e0d74900-21b3-11eb-8ea6-33ddaf349386.jpeg)
The diagram above basically shows what inputs and output sources are, and how they affect on the Arduino. Arduino, open-source prototyping platform used for building elctronic project, is commonly run by C++. The platform directly connects to breadboard where 7LEDs are installed. 
In this case, 4 buttons(A,B,C,D) and laptop that executes the program on Arduino are represented as input sources.

#### Illustrate how it looks like on Tinkercad
<img width="1005" alt="Screen Shot 2020-11-03 at 21 35 45" src="https://user-images.githubusercontent.com/60457723/97986108-92752380-1e1c-11eb-9ab4-1871509010e4.png">
To make sure how my program works, first prototype is done by online Arduino platform called "TinkerCad"
The schreenshot above indicates that 7LEDs,resistors,buttons are all attched on the breadboad.


#### Truth Table 
![CamScanner 11-06-2020 12 14](https://user-images.githubusercontent.com/60457723/98322154-1bad7580-202a-11eb-9b51-124f6a3b1df7.jpg)
The Truth table above is based on the sketchs of the idea that shows how I defined the numbers using 7 LEDs.


#### Boolean expression (equation) 

![Compsci_miniIA_kmap 001](https://user-images.githubusercontent.com/60457723/98428946-32fe6880-20e7-11eb-9cad-df588ccbf6b1.jpeg)
![Compsci_miniIA_kmap 002](https://user-images.githubusercontent.com/60457723/98428949-37c31c80-20e7-11eb-9781-cde98b3639eb.jpeg)
![Compsci_miniIA_kmap 003](https://user-images.githubusercontent.com/60457723/98428951-3a257680-20e7-11eb-9a84-4504d9f0a1d9.jpeg)
![Compsci_miniIA_kmap 004](https://user-images.githubusercontent.com/60457723/98428954-3bef3a00-20e7-11eb-9e6c-8dcaf26cb3d2.jpeg)

Boolean expressions for each LEDs are produced by K-map above, and they are all based on the truth table that I made and generated by online platform.
(http://electronics-course.com/karnaugh-map)

The list of the all equations:
![CamScanner 11-06-2020 12 19](https://user-images.githubusercontent.com/60457723/98322380-9c6c7180-202a-11eb-8062-b0a84c30d9b1.jpg)

### Flow chart

#### Testing Plan
## Criteria C: Development

```.c++
//inidicates each ports for LEDs
int led1 = 2;
int led2 = 3;
int led3 = 4;
int led4 = 5;
int led5 = 6;
int led6 = 7;
int led7 = 8;
//indicates each ports for BUTTONS
int port_btnA = 12;
int port_btnB = 11;
int port_btnC = 10;
int port_btnD = 9;
//define each valuables for BUTTONS
int val_btn1 = 0;
int val_btn2 = 0;
int val_btn3 = 0;
int val_btn4 = 0;


//setup function, outputs and their ports have to be defined inside of the brackets.
// in this case, buttons are input source so this doesnt include them.
void setup()
{
  pinMode(2, OUTPUT);
  pinMode(3, OUTPUT);
  pinMode(4, OUTPUT);
  pinMode(5, OUTPUT);
  pinMode(6, OUTPUT);
  pinMode(7, OUTPUT);
  pinMode(8, OUTPUT);

}

//loop function, the program inside loops back everytime when input sources are detected.
void loop()
{
  val_btn1 = digitalRead(port_btnA);
  val_btn2 = digitalRead(port_btnB);
  val_btn3 = digitalRead(port_btnC);
  val_btn4 = digitalRead(port_btnD);
  //each equations for LEDs are applied here 
  int led1_eq = (!val_btn2 && !val_btn3)||(!val_btn1 && val_btn3 && val_btn4) || (!val_btn1 && !val_btn3 && !val_btn4) ;
  digitalWrite(led1, led1_eq);
  int led2_eq = (!val_btn1 && !val_btn2) || (!val_btn1 && val_btn4) || (!val_btn1 && val_btn3) || (!val_btn2 && !val_btn3 && val_btn4);
  digitalWrite(led2, led2_eq);
  int led3_eq = (!val_btn1 && val_btn3 && val_btn4) || (!val_btn1 && !val_btn2 && val_btn4) || (!val_btn1 && !val_btn2 && val_btn3) || (!val_btn1 && val_btn2 && !val_btn3 && !val_btn4) || (val_btn1 && !val_btn2 && !val_btn3 && !val_btn4);
  digitalWrite(led3, led3_eq);
  int led4_eq = (!val_btn1 && !val_btn3) || (!val_btn1 && !val_btn4) || (!val_btn2 && !val_btn3);
  digitalWrite(led4, led4_eq);
  int led5_eq = (!val_btn1 && val_btn2 && val_btn4) || (val_btn1 && !val_btn2 && !val_btn3 && val_btn4);
  digitalWrite(led5, led5_eq);
  int led6_eq = (!val_btn1 && val_btn2) || (!val_btn1 && val_btn3) || (!val_btn1 && !val_btn4) || (val_btn1 && !val_btn2 && !val_btn3);
  digitalWrite(led6, led6_eq);
  int led7_eq = (val_btn1 && !val_btn2 && !val_btn3) || (!val_btn1 && val_btn2 && val_btn3 && !val_btn4);
  digitalWrite(led7, led7_eq);
}
```
### Build a tangible prototype
![compsci_prototype](https://user-images.githubusercontent.com/60457723/98666019-c5c13080-238f-11eb-8add-1bc7f2ac734c.jpg)

Afterwards, I've eventually created actual arduino platform using cardboard (the photo above)
Arduino conncects to the laptop through usb cable in order to run the program (Arduino IDE) inside as well as power supply.

## Criteria D: Functionality
## Criteria E: Evaluation
