# Huffman-Shannon_fano
# Aim:
Consider a discrete memoryless source with symbols and statistics {0.125, 0.0625, 0.25, 0.0625, 0.125, 0.125, 0.25} for its output. 
Apply the Huffman and Shannon-Fano to this source. 
Show that by drawing the tree diagram, and 
Calculate the average code word length, entropy, variance, redundancy, and efficiency.

# Tools Required:
Python with NumPy and SciPy libraries, Google Colab.

# Program:
```
# Huffman and Shannon-Fano Coding
import numpy as np
import math 

L  = 0
hs = 0
p = []
lk = []
n = int(input("Enter the number of Samples: "))

for i in range(n): 
    pr = float(input(f"Enter the probability of sample {i + 1}: "))  
    p.append(pr)

for j in range(n): 
    l = float(input(f"Enter the length of sample {j + 1}: "))  
    lk.append(l)

# Average Codeword Length
for k in range(n):
    Avg1 = p[k] * lk[k]
    L += Avg1

# Entropy Calculation
for k in range(n):
    e = p[k] * math.log(1 / p[k], 2)
    hs += e
hs = round(hs, 3)

# Efficiency Calculation
eff = round(hs / L, 3)

# Redundancy Calculation
red = round(1 - eff, 3)

# Variance Calculation
var = 0
for k in range(n):
    var1 = p[k] * (lk[k] - L) ** 2
    var += var1
var = round(var, 3)

print(f"Average Codeword Length: {L}")
print(f"Entropy: {hs}")
print(f"Efficiency: {eff}")
print(f"Redundancy: {red}")
print(f"Variance: {var}")
```
# Calculation:
![image 1](https://github.com/user-attachments/assets/a12050bf-6c27-4491-8ca4-138c0b2f0866)
![image 2](https://github.com/user-attachments/assets/99e3f1ca-b37a-4511-b22a-d2cd344bc348)
![imafe 3](https://github.com/user-attachments/assets/645ae22a-f15b-4b3c-88db-140fc0e2c4a2)
![image 4](https://github.com/user-attachments/assets/19890c90-5af0-421f-9732-aee6e5b0cb6b)


# Output
<img width="468" height="454" alt="image" src="https://github.com/user-attachments/assets/8520adb5-808a-48cc-b22e-5c40a55293b2" />```
 
# Results:

The Huffman and Shannon-Fano coding techniques have been successfully applied to the given source. The average codeword length, entropy, variance, redundancy, and efficiency have been computed.

