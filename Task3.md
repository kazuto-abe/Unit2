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
```.py

```
