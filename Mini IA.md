# Unit2 - Kazuto Abe

## Criteria A: Planning
#### Context of the problem
This project is a program to count from 0 to 9. The preceding has been done last year with the current G12s who used the standard 7 figures to count. Therefore, this year's G11s will have to think outside the box and come up with more creative ways to create a program with the purpose of counting while using the same criteria and resources. We will dispose of:

7 LEDs
4 Buttons
Arduino
Circuits components

#### Justification of the solution



#### A sketch of the whole idea
Whaat my idea of how the numbers (0 ~ 9) are represented using 7 LEDs is "pylamid counting system" as the rough sketch shows below.
To express all numbers, each shapes follows a pattern, and (triangle, paralellogram, rectangle, etc...) are all defined as the number so that we are all allowed to recognize various numbers instantly.
![seven](https://user-images.githubusercontent.com/60457723/98828206-24170d80-247b-11eb-9fc8-965dcb34a729.jpg)

##### Figure 1 : A sketch showing how the numbers are all represented.

#### Criteria for success
1. The display should count from 0-9 properly.
2. A table showing each number 0-9 and the corresponding LEDs is included.
3. A table showing the operation of the buttons and number 0-9 is included.
4. The display uses maximum 7 LEDs and 4 buttons.


## Criteria B: Design

### Record of Tasks
The procedure of the project follows the task plan below:
| Task No |                                                    Planned Action                                                    |                                           Planned  Outcome                                           | Time Estimated | Target Completion Date  | Criterion |
|:-------:|:--------------------------------------------------------------------------------------------------------------------:|:----------------------------------------------------------------------------------------------------:|:--------------:|:-----------------------:|:---------:|
|    1    |                               Planning: Create rough sketches of an idea from scratch.                               |                             Visualize what the brief idea is on the paper                            |       1h       |        2020/11/3        |     A     |
|    2    |                                     Design: Create a online circuit on TinkerCad.                                    |                                  Connects all the wires on TinkerCad                                 |       2h       |        2020/11/5        |     B     |
|    3    |               Design: Create a system diagram shows how Arduino works and the flowchart of the program.              | 1 system diagram and 1 flowchart as an example of the entire code.(there are 9 flowcharts in total)  |     1h30min    |        2020/11/6        |     B     |
|    4    |                                      Design: Create a truth table for the LEDs.                                      |                                                                                                      |       1h       |        2020/11/6        |     B     |
|    5    |                  Design: Create K-maps for each LEDs and figure out what the boolean equations are.                  |                                    7 K-map and 7 boolean equations                                   |       2h       |        2020/11/6        |     B     |
|    6    | Development: Complete entire program and make sure that the program works properly using TinkerCad online simulator. |                                                                                                      |     2h30min    |        2020/11/8        |     C     |
|    7    |                                    Development: Build an actual Arduino platform                                     |                        Connects all stuff to Arduino (LEDs are on cardboard)                         |       3h       |        2020/11/10       |     C     |
|    8    |                                   Functionality: Create a short video how it works                                   |                          1 gif animation to show that the program works well                         |      40min     |        2020/11/12       |     D     |

### System Diagram
![Arduino_system diagram_modified 001](https://user-images.githubusercontent.com/60457723/104594309-5419a180-56b4-11eb-8c7f-d5854322bb90.jpeg)

##### Figure 2: A system diagram of the digital counter showing the main components.

The diagram above basically shows what inputs and output sources are, and how they affect on the Arduino. Arduino, open-source prototyping platform used for building elctronic project, is commonly run by C++. The platform directly connects to breadboard where 7LEDs are installed. 
In this case, 4 buttons(A,B,C,D) and laptop that executes the program on Arduino are represented as input sources.

#### Illustrate how it looks like on Tinkercad
<img width="1005" alt="Screen Shot 2020-11-03 at 21 35 45" src="https://user-images.githubusercontent.com/60457723/97986108-92752380-1e1c-11eb-9ab4-1871509010e4.png">

##### Figure 3 : A screenshot showing a digital circuit on TinkerCad

To make sure how my program works, first prototype is done by online Arduino platform called "TinkerCad"
The schreenshot above indicates that 7LEDs,resistors,buttons are all attched on the breadboad.


#### Truth Table 
![CamScanner 11-06-2020 12 14](https://user-images.githubusercontent.com/60457723/98322154-1bad7580-202a-11eb-9b51-124f6a3b1df7.jpg)
The Truth table above is based on the sketchs of the idea that shows how I defined the numbers using 7 LEDs.

##### Figure 4: A truthtable corrensponds to each LEDs (1 = LED on, 0 = LED off)


#### Boolean expression (equation) 

![Compsci_miniIA_kmap 001](https://user-images.githubusercontent.com/60457723/98428946-32fe6880-20e7-11eb-9cad-df588ccbf6b1.jpeg)
![Compsci_miniIA_kmap 002](https://user-images.githubusercontent.com/60457723/98428949-37c31c80-20e7-11eb-9781-cde98b3639eb.jpeg)
![Compsci_miniIA_kmap 003](https://user-images.githubusercontent.com/60457723/98428951-3a257680-20e7-11eb-9a84-4504d9f0a1d9.jpeg)
![Compsci_miniIA_kmap 004](https://user-images.githubusercontent.com/60457723/98428954-3bef3a00-20e7-11eb-9e6c-8dcaf26cb3d2.jpeg)

##### Figure 5: A boolean equation

Boolean expressions for each LEDs are produced by K-map above, and they are all based on the truth table that I made and generated by online platform.
(http://electronics-course.com/karnaugh-map)

The list of the all equations:
![CamScanner 11-06-2020 12 19](https://user-images.githubusercontent.com/60457723/98322380-9c6c7180-202a-11eb-8062-b0a84c30d9b1.jpg)

### Flow chart
This is an example process of the entire program, the flow chart below represents for the number 1.

![IMG_6377](https://user-images.githubusercontent.com/60457723/98966778-087d3700-254f-11eb-8153-b875a910103d.jpg)

##### Figure 6 : A flow chart showing how the program is excuted in order.

#### Testing Plan
|                                 Criteria No.                                 |                                                      Expected Outcome                                                     | Criteria met? |
|:----------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------------------:|:-------------:|
| Follow the table with number/LED's  equivalence to check each number 0 to 9. |         For example, If you press the button's combination for number 1,  the display shows pattern for number 1.         |      YES      |
|          A table is provided with LED sequences for each number 0-9.         |                              Reading the patterns of LEDs for each number 0-9 is symbolised.                              |      YES      |
|            Each shape that represent the number follows a pattern.           | Every single shape such as triangle, parallelogram, rectangle, etc... represent the number.(0-9) So it is easy to follow. |      YES      |
|                    7 LEDs and 4 buttons are all installed.                   |                    You can see no more than 7LEDs(maximum number of lights) and 4 buttons are attached.                   |      YES      |

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
This is a video how my program works, and disply the numbers (0-9)

![Videotogif](https://user-images.githubusercontent.com/60457723/98890880-4db65000-24e0-11eb-9b6d-068c770fde10.gif)


## Criteria E: Evaluation
