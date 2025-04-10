# DC-EXPERIMENT08
## AIM:
  To calculate the entropy, average codeword length, efficiency, redundancy, and variance of a given source using Huffman or Shannon-Fano coding.
## APPARATUS REQUIRED:
   1.Python 3.x installed
   2.GitHub account
   3.Git installed
   4.VS Code / any IDE
## PROCEDURE:
1.Start the Python environment: Open any Python IDE or terminal with Python installed.
2.Create a Python file: Name it as source_coding_analysis.py.
3.Write the code: Copy and paste the following Python code into the file.
4.Save and run the program.
5.When prompted, input:
  The total number of symbols/samples.
  The probability of each symbol.
  The codeword length for each symbol (from Huffman or Shannon-Fano encoding).
6.Observe the output: The program will calculate and display:
  Average Codeword Length (L)
  Entropy (H)
  Efficiency (η)
  Redundancy (R)
  Variance (σ²)

## CODE:
HUFFMAN and SHANON-FANO
import numpy as np
import math 
L  = 0
hs = 0
p = []
lk = []
n = int(input("Enter the number of Samples : "))
for i in range (n): 
    pr = float(input(f"Enter the probability of sample values {i + 1}: "))  
    p.append(pr)
for j in range (n): 
    l = float(input(f"Enter the length of the sample values {j + 1}: "))  
    lk.append(l)
for k in range (n):
    Avg1 = p[k] * lk[k]
    L = L + Avg1
for k in range (n):
    e = p[k] * math.log(1 / p[k], 2)
    hs = hs + e
hs = round(hs,3)
eff =  (hs / L)*100
eff = round(eff,3)
red =  round(100 - eff,3) 
var = 0
for k in range(n):
    var1 = p[k] * (lk[k]-L)**2
    var = var + var1
var = round(var,3)
print(f"Average Codeword Length is : {L}")
print(f"Entropy is : {hs}")
print(f"Efficiency is : {eff}")
print(f"Redudancy is : {red}")
print(f"Variance is : {var}")

## SAMPLE INPUT/OUTPUT:
![image](https://github.com/user-attachments/assets/d0dc5062-6e3c-425a-9c3f-c2f90131f691)

## RESULT:
The code successfully calculates entropy, average codeword length, efficiency, redundancy, and variance for the input source. These metrics can be used to evaluate the performance of source coding techniques like Huffman and Shannon-Fano coding.




