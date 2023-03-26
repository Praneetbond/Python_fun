# Python_fun (Basic)
## Just enjoy some basic codes for Python 3


### Swap Alphabets for Upper to Lower to Upper.
```python
# Try any mixter of upper and lower character.
def swap_case(s):
    y = []
    for i in s:
        if i >= "a" and i <= "z":
            y.append(chr(ord(i)-32))
        elif i >= "A" and i <= "Z":
            y.append(chr(ord(i)+32))
        else: y.append(i)
    return "".join(y)


if __name__ == '__main__':
    s = input("Try your thing: ")
    result = swap_case(s)
    print(result)
```


### You need only unique characters in you list
```python
# Try with multi inputs at a time ofcourse!!.
from ast import literal_eval
user_defined = input("Enter you numbers: ")
x = literal_eval(user_defined)
y = set(x)
x = list(y)
print (x)
```


### Pattern Printing
```python
# You love stars in a pattern. You are lucky...
n = int(input("How large you want: "))

# For Piramid one.
for i in range (1, n+1):
    for j in range (n-i):
        print (" ", end = '')
    for k in range (i-1):
        print ("*_", end = '')
    print ("*")

# For Right one.
for i in range (1, n+1):
    for j in range (n-n):
        print (" ", end = '')
    for k in range (i-1):
        print ("*_", end = '')
    print ("*")
    
# For Left one.
for i in range (1, n+1):
    for j in range ((n-i)*2):
        print (" ", end = '')
    for k in range (i-1):
        print ("*_", end = '')
    print ("*")
```


### Armstrong Number  
```python
# A number that is the sum of its own digits each raised to the power of the number of digits.
def armstrong_number(n):
    sum1 = 0
    power = len(str(n))
    org = n
    while (n>0):
        x = n%10
        y = x**int(power)
        n = n//10
        sum1 += y
    if (org==sum1):
        print("Yeah!!",m, "is an Armstrong Number")
    else: print("Sorry!! You found wrong number")
        
m = int(input("Try a number and find out: "))
armstrong_number(m)
```


### Reverse the number
```python
# Reverse it from back to front and complicate your calculation. Enjoy..
num = int(input("Why you are doing this: "))

def reverse_it (num):
    Rev = 0
    if (num <= 0):
        pass
    else:
        while (num != 0):
            digit = num%10
            Rev = Rev*10 + digit
            num = num//10
        return Rev

print (reverse_it(num))
```


### Use of if-elif statement. Have fun...
```python
### Try any integer positive or negative even zero to enjoy
number = input("Tell me the number ")

if (int(number) < 0) : print ("OH! You are on negative side")
elif (int(number) > 0) : print ("Hmm, positive side it is")
else : print ("Congrats Its Zero")
```


### Alarm Clock
### Need a clock while you are on break from office work. Buy one.
```python
### Its an alarm clock for fun. Put a week number and 1 if you are on vacation else 0
week = int(input("Number of week followed by Vacatation status: "))
vacation = bool(input() =="0")
weekdays = [1,2,3,4,5]
weekend = [6,7]

print([week,vacation])
if (week in weekdays):
    if (not vacation):
        print("Wake up it's 7'O Clock")
    else : print ("You are on vacation but it's 10:00")
elif (week in weekend):
    if (not vacation):
        print ("It's weekend but wake up boss It's 10:00")
    else: print ("Sleep Tight!! SHhhhhh")
else: print ("You forget the week ?? Try again")
```

