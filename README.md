#  Mean and variance of a discrete  distribution


# Aim : 

To find mean and variance of arrival of objects from the feeder using probability distribution


# Software required :  

Python and Visual components tool

# Theory:

The expectation or the mean of a discrete random variable is a weighted average of all possible
values of the random variable. The weights are the probabilities associated with the corresponding values. 
It is calculated as,

![image](https://user-images.githubusercontent.com/103921593/192938463-e34177f4-f188-48a0-bda2-8f6d1d660ed2.png)

The variance of a random variable shows the variability or the scatterings of the random variables.
It shows the distance of a random variable from its mean. It is calcualted as

![image](https://user-images.githubusercontent.com/103921593/192938695-99fedc01-34d5-4d36-84df-5880e766ed0c.png)


# Procedure :

1. Construct frequency distribution for the data

2. Find the  probability distribution from frequency distribution.

3. Calculate mean using 
   
   ![image](https://user-images.githubusercontent.com/103921593/192940431-03b81777-c54d-4286-b4f4-82dfe7666b4c.png)

4. Find  
   
      ![image](https://user-images.githubusercontent.com/103921593/192940255-2d9dd746-6875-4a6d-877b-6da6cdb96ab1.png)

5.  Calculate variance using 
  
      ![image](https://user-images.githubusercontent.com/103921593/192942852-913550a9-fabe-4a55-b956-0487b18bbd97.png)


# Experiment :

![image](https://user-images.githubusercontent.com/103921593/229993174-5b67e57e-3e01-4ac4-9f83-410a932b22bf.png)

# Program :

## Developed by : Jayendhiran
## Reg no : 212225230115

## Declaring the value of n
```^c
import numpy as np
n = int(input("Enter the value of n : "))
print("Value of n =", n)

```
## Getting the inputs
```
InputVal = {}
for i in range(1, n+1):
    val = int(input(f"Enter the value no {i} : "))
    try:
        InputVal[val] += 1
    except:
        InputVal[val] = 1
print(f"{i} Values Collected Successfully")

```
## Finding Mean
```
mean = 0
for key, val in InputVal.items():
    mean += key*(val/n)
print(f"Mean = {mean:.3f}")
```

## Finding Variance
```
ex2 = 0
for key, val in InputVal.items():
    ex2 += ((key**2) * val/n)
var = ex2 - mean**2
print(f"Variance : {var:.3f}")
```
## Finding Standard Deviation
```
from math import sqrt
sdtDeviation = sqrt(var)
print(f"Standard Deviation = {sdtDeviation:.3f}")
```

# Output : 
## Refer to the following images to view the output of the program

<img width="490" height="170" alt="image" src="https://github.com/user-attachments/assets/6d007ddb-21bc-4324-b232-7c7493a5c862" />

<img width="490" height="256" alt="image-1" src="https://github.com/user-attachments/assets/4f7bc996-c9a4-42c0-bb38-7bb0bd3819c9" />

<img width="491" height="175" alt="image-2" src="https://github.com/user-attachments/assets/23a75af2-725d-4458-a7ef-a4ce7e22b83c" />

<img width="490" height="201" alt="image-3" src="https://github.com/user-attachments/assets/261a4dfc-72bf-4d56-b929-d86e2e974f15" />

<img width="487" height="164" alt="image-4" src="https://github.com/user-attachments/assets/8ec2caf3-c8aa-4728-b210-b54d35c2f056" />


# Results :
The mean and variance of arrivals of objects from feeder using probability distribution are calculated.

