# **Python-algorithms**  
## efficient algorithms for general tasks with good time complexity.  

------------------------------------------------------------------------------------

## **Referance:** Competetive programming with python  

------------------------------------------------------------------------------------
#### bitwise operator not {~} : (a = 10 => 1010 (Binary) => ~a = ~1010 = -(1010 + 1) = -(1011) = -11)  
#### bitwise operator xor {^}  : (n^n = 0), (n^0 = n)  
#### bitwise operator rightshift {>>} : (100 >> 2 = 25)  
#### bitwise operator leftshift {<<} : (100 << 2 = 400)  

-------------------------------------------------------------------------------------
### sum of n numbers:O(1)  
```python
def sum_total(n):
    return int(n*(n+1)/2)
```
### Odd-Even:O(1)  
```python
if n&1 == 1:
    print('odd')
else:
    print('even')
```
### Leftshift(multiply) / Rightshift(divide) by 2<sup>n</sup>:O(1)  
```python
def multpow(x,y):
    return x<<y  # x*(2^y)
def divpow(x,y):
    return x>>y # x/(2^y)
```
### Check if a number is power of 2:O(1)  
```python
def ispow(n):
    if n <= 0:
        return False
    x = n
    y = not(n & (n-1))
    return x and y
```
### count 1's in binary representation:O(log(n))  
```python
def cntbits(n):
    cnt = 0
    while n:
        cnt += 1
        n = n & (n-1)
    return cnt
```
### convert int to binary / binary to int:O(1)   
```python
def inttobin(n):
    return str(bin(n))[2:]

def bintoint(m):
    return int(m,2)
```
### check which number occurs once(or odd number of times/doesn't has it's unique identical element) in an array:O(n)
```python
def checkpair(arr): # n -> aray
    temp = arr[0]
    for i in range(1,len(arr)):
        temp = temp ^ arr[i]
    return temp
```
