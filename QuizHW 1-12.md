#### Quizzes homework:
Solve them again, program them, draw flow diagram, test them. Add it to your repo for Unit 2


## Quiz 1
Given 2 numbers, A and B, Output TRUE if one if them is 10 or if their sum is 10.

Examples <br>
Makes10(9, 10) → TRUE <br>
Makes10(9, 9) → FALSE <br>
Makes10(1, 9) → TRUE <br>

#### Pseudocode & Flowchart
![IMG_6892](https://user-images.githubusercontent.com/60457723/103271199-ebb49a00-49fc-11eb-91af-ad954344f039.jpeg)

#### Python Code

```.py
def Makes10():
    A = int(input("please enter an integer A: "))
    B = int(input("please enter an integer B: "))
    sum = A + B
    if A == 10 or B == 10 or sum == 10:
        print(True)
    else:
        print(False)

Makes10()
```

#### Test result

<img width="630" alt="Screen Shot 2020-12-30 at 15 55 29" src="https://user-images.githubusercontent.com/60457723/103335756-55927980-4ab9-11eb-9701-85160482a9f3.png">

## Quiz 2
Given three int values, A, B, and C, output the largest.

Examples <br>
IntMax(1, 2, 3) → 3 <br>
IntMax(1, 3, 2) → 3 <br>
IntMax(3, 2, 1) → 3 <br>

#### Pseudocode & Flowchart
![IMG_6893](https://user-images.githubusercontent.com/60457723/103271207-f0794e00-49fc-11eb-9c3e-39cb0d466220.jpeg)

#### Python Code

```.py
def IntMax():
    A = int(input("Please enter an integer A: "))
    B = int(input("Please enter an integer B: "))
    C = int(input("Please enter an integer C: "))
    max_int = 0
    if A >= B and A >= C :
        max_int += A
    if B >= A and B >= C :
        max_int += B
    if C >= B and C >= A :
        max_int += C
    print(max_int)

IntMax()
```

#### Test result

<img width="661" alt="Screen Shot 2020-12-30 at 16 13 14" src="https://user-images.githubusercontent.com/60457723/103335945-f5e89e00-4ab9-11eb-862a-0a7866ff6191.png">

## Quiz 3
Given an integer N, print all the integers from 0 to N. 

[HL] show also the addition of the numbers.

Example<br>
rangeN(6)   → 0, 1, 2, 3, 4, 5, 6 <br>
				    → 21 <br>

#### Pseudocode & Flowchart
![IMG_6894](https://user-images.githubusercontent.com/60457723/103271208-f1aa7b00-49fc-11eb-9a48-c857231d960f.jpeg)

#### Python Code

```.py
def rangeN ():
    N = int(input("please enter an integer N: "))
    sum_num = 0
    for i in range(0, N + 1):
        print(i)
        sum_num += i
    print(sum_num)
    
rangeN()   
```

#### Test result

<img width="656" alt="Screen Shot 2020-12-30 at 16 27 45" src="https://user-images.githubusercontent.com/60457723/103336576-f84bf780-4abb-11eb-8f97-04fe38689189.png">

## Quiz 4
Given an integer N, show all its factors. 

[HL] show also the addition of the factors show if the result is the same as N

Example <br>
perfectN(6)   → 1, 2, 3 <br>
				      → “Sum of factors is:” 6, True <br>
              
#### Pseudocode
![IMG_6895](https://user-images.githubusercontent.com/60457723/103271209-f2431180-49fc-11eb-91c6-72e1e9eb5158.jpeg)

#### Flowchart
![IMG_6896](https://user-images.githubusercontent.com/60457723/103271210-f2dba800-49fc-11eb-9ec9-c40ea7e73197.jpeg)

#### Python Code

```.py
def perfectN():
    N = int(input("Please enter an integer N: "))
    sum_factors = 0
    for i in range(1, N-1):
        if N % i == 0:
            print(i)
            sum_factors += i
    
    if sum_factors == N :
        print("Sum of the factors is: {}, True".format(sum_factors))
    else:
        print("Sum of the factors is: {}, False".format(sum_factors))
        
perfectN()
```
#### Test result

<img width="677" alt="Screen Shot 2020-12-30 at 17 13 46" src="https://user-images.githubusercontent.com/60457723/103338665-74493e00-4ac2-11eb-9cbf-48f9ec4a5a59.png">

## Quiz 5
Given an integer N, show the multiplication table. 

Example <br>
tableM(2)   → 2x1=2 <br>
		2x2=4 <br>
		2x3=6 <br>
		2×9=18 
          
#### Pseudocode & Flowchart
![IMG_6898](https://user-images.githubusercontent.com/60457723/103271211-f3743e80-49fc-11eb-84d6-e55d2bf3353b.jpeg)

#### Python Code

```.py
def tableM():
    N = int(input("please enter an integer N: "))
    multipul_num = 0
    for i in range(1,10):
        multipul_num = i * N
        print("{} × {} = {}".format(N,i,multipul_num))
    
tableM()
```

#### Test result

<img width="683" alt="Screen Shot 2020-12-30 at 17 25 39" src="https://user-images.githubusercontent.com/60457723/103339187-13bb0080-4ac4-11eb-986f-473618c03db1.png">

## Quiz 6
Output TRUE if the given string begins with 'mix', except the 'm' can be anything, so 'pix', '9ix'..all count.

Examples <br>
MixStart('mix snacks') → TRUE <br>
MixStart('pix snacks') → TRUE <br>
MixStart('piz snacks') → FALSE <br>

#### Pseudocode & Flowchart
![IMG_6899](https://user-images.githubusercontent.com/60457723/103271213-f40cd500-49fc-11eb-9b32-ada3d3099c7b.jpeg)

#### Python Code

```.py
def MixStart():
    string_x = input("please enter a string: ")
    if string_x[1] == "i" and string_x[2] == "x" :
        print(True)
    else:
        print(False)

MixStart()
```

#### Test result
<img width="682" alt="Screen Shot 2020-12-30 at 17 34 08" src="https://user-images.githubusercontent.com/60457723/103339720-837dbb00-4ac5-11eb-92c6-bc19eb07b935.png">


## Quiz 7
Given a string, output each letter with its index:

Example: <br>
letters('hello') → 0 -> h <br>
						1 -> e <br>
						2 -> l <br>
						3 -> l <br>
						4 -> 0 <br>

#### Pseudocode & Flowchart

![07](https://user-images.githubusercontent.com/60457723/103354712-a45b0600-4aef-11eb-9f37-9ea852e2af03.jpg)

#### Python Code

```.py
def letters():
    string_x = input("please enter a string: ")
    length = len(string_x)
    for i in range(length):
        print(i, " →  " ,string_x[i])
        
letters()
```

#### Test result

<img width="677" alt="Screen Shot 2020-12-30 at 21 58 10" src="https://user-images.githubusercontent.com/60457723/103352660-25170380-4aea-11eb-9fa0-b7008f577439.png">

## Quiz 8
Given an array of integers, find the largest absolute value.  Tip: you can use the abs() function.
 
Example: <br>
maxAbs([-4, 5, 6, -7]) → “max absolute is 7”  <br>
maxAbs([-1, 0, 1]) → “max absolute is 1” <br>
maxAbs([-100, 0, 3,-200]) → “max absolute is 200” <br>

#### Pseudocode & Flowchart

![08](https://user-images.githubusercontent.com/60457723/103354709-a3c26f80-4aef-11eb-9df6-4380d9617e2b.jpg)

#### Python Code

```.py
def maxAbs (arrayx):
    max_value = 0
    length = len(arrayx)
    for i in range(length):
        if abs(int(arrayx[i])) > max_value:
            max_value = abs(int(arrayx[i]))
    print("max absolute is ...  {}". format(max_value))
maxAbs(arrayx = [-4,5,6,-7])
maxAbs(arrayx = [-1, 0, 1])
maxAbs(arrayx = [-100, 0, 3,-200])
```

#### Test result

<img width="677" alt="Screen Shot 2020-12-30 at 22 51 39" src="https://user-images.githubusercontent.com/60457723/103355455-a3c36f00-4af1-11eb-91ef-e3c2ca5ee0c8.png">

## Quiz 9
Given an array of sorted integers, find the missing number.
 
Example: <br>
missingNumber([1, 2, 3, 5, 6, 7]) → 4 missingNumber([4, 5, 6, 8, 9, 10]) → 7 <br>
missingNumber([73, 74, 75, 76, 78, 79]) → 77  <br>

#### Pseudocode & Flowchart

![09](https://user-images.githubusercontent.com/60457723/103354704-a329d900-4aef-11eb-9be6-2fe6b0080451.jpg)

#### Python Code

```.py
def missingNumber(arrayx):
    length = len(arrayx)
    for i in range(0, length - 1):
        if arrayx[i] != arrayx[i+1] - 1:
            print("You are missing ... {}". format(arrayx[i] + 1))

missingNumber(arrayx = [1,2,3,5,6,7,8,9])
missingNumber(arrayx = [4,5,6,8,9,10])
missingNumber(arrayx = [73,74,75,76,78,79])
```

#### Test result

<img width="678" alt="Screen Shot 2020-12-30 at 23 12 20" src="https://user-images.githubusercontent.com/60457723/103356846-239f0880-4af5-11eb-87fa-1bc222060528.png">


## Quiz 10
Given an array of sorted integers, find the largest difference between neighbouring numbers.
 
Example: <br>
BigNeighbour([1, 2, 3, 5, 6, 7]) → 2 (because 3 to 5) <br>
BigNeighbour([0, 5, 6, 10]) → 5 (because 0 to 5) <br>
BigNeighbour([73, 74, 174, 76, 78, 79]) → 100 <br>

#### Pseudocode

![010-1](https://user-images.githubusercontent.com/60457723/103354702-a1f8ac00-4aef-11eb-93ef-4f53b235304e.jpg)

#### Flowchart

![010-2](https://user-images.githubusercontent.com/60457723/103354699-a0c77f00-4aef-11eb-93ed-2f1a7c076aa4.jpg)

#### Python Code

```.py
def BigNeighbour(arrayx):
    largestgap = 0
    length = len(arrayx)
    for i in range(0, length - 1):
        gap = abs(arrayx[i] - arrayx[i+1])
        if gap > largestgap:
            largestgap = gap
    print("the largest difference between neighboring nums is ... {}".format(largestgap))

BigNeighbour(arrayx = [1,2,3,4,5,7])
BigNeighbour(arrayx = [0, 5, 6, 10])
BigNeighbour(arrayx = [73, 74, 174, 76, 78, 7])
```

#### Test result

<img width="680" alt="Screen Shot 2020-12-30 at 23 24 03" src="https://user-images.githubusercontent.com/60457723/103357276-1fbfb600-4af6-11eb-9f32-df5dceb1fc15.png">

## Quiz 11

## Quiz 12
