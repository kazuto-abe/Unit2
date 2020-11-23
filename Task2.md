### Task 2:  Boolean Logic


The questions below are from previous IB CS papers #1. You have the opportunity to experience the question format and develop confidence in solving them. 

1. Consider the boolean expression 
![boolean_1](https://user-images.githubusercontent.com/60457723/99178666-d0494480-2758-11eb-9ef1-3233f6c37dc9.jpg)

2. Construct the truth table for the following Boolean expression.
![boolean_2](https://user-images.githubusercontent.com/60457723/99178665-cfb0ae00-2758-11eb-994a-0acfd9178ae0.jpg)

3. Construct a truth table for the following Boolean expression.
4. Construct a truth table for the following Boolean expression.
5. In an 8-bit register, state the binary representation of the hexadecimal number x3B.
![boolean_345](https://user-images.githubusercontent.com/60457723/99178663-cde6ea80-2758-11eb-97e7-f0446b818d68.jpg)

6. Construct a truth table for the Boolean expression 
![boolean_6](https://user-images.githubusercontent.com/60457723/99178660-c7f10980-2758-11eb-815a-58a29740f696.jpg)



### Activities on Snakify
#### Practical work on Snakify

I was working on how while loop and list works on Python.

#### Extract even number from the list

ex) [1, 2, 3, 4, 5]

```.py

test_list = [1,2,3,4,5]
odd_i = []
even_i = []

print("Original input list: {}".format(str(test_list)))
for i in range(0, len(test_list)):
    if i % 2:
        even_i.append(test_list[i])
    else:
        odd_i.append(test_list[i])

print("Even elements are extracted: {}".format(str(even_i)))

```
→Output [2,4]

#### List of Squares (By using WHILE loop)
