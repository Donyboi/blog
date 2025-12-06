**Learning Python Through Mistakes**

# Debugging mistakes using Python  

Debugging can feel frustrating at first, but it’s really just solving small puzzles step by step. Every bug teaches you something new about how Python works, from logic to syntax. Once you understand it, fixing mistakes becomes part of the fun.  

---

## Temperature Check  
The temperature program didn’t know what to do with numbers between 0 and 50, so it skipped them entirely. That left a gap where the program gave no answer, which made it incomplete. Changing the last `elif` to `else` fixed the issue and covered all cases.  

```python
temperature = 75

if temperature > 80:
    print("It's hot")
elif temperature > 50:
    print("It's temperate")
elif temperature < 0:
    print("It's cold")
```




---

## Counting Spaces  
The space counter was broken because it was checking for an empty string instead of a space. That meant the loop never actually counted anything, even though spaces were there. Switching the condition to `if char == " "` made the program work correctly.  

```python
text = "Hello, world, my name is"
count = 0

for char in text:
    if char == "":
       count += 1

print(count)
```


---

## Even or Odd  
The even‑odd program had two problems: the input wasn’t converted to an integer, and the condition was wrong. Without fixing those, the program couldn’t do math or check numbers properly. Using `int(input())` and `num % 2 == 0` solved both issues.  

```python
print("give me a number")
n = input()

for num in range(1, n):
    if num % 2 < 0:
        print(num, "is even.")
    else:
        print(num, "is odd.")
```


---

## Factorial Function  
The factorial program stopped too early because the loop didn’t include the final number. On top of that, the print statement broke when trying to mix strings and integers. Expanding the loop and using a f‑string made the program calculate factorials correctly.  

```python
num = int(input("Enter an integer: "))

if num < -1:
  print("No negative numbers.")
else:
  result = 1
  for i in range(1, num):
    result *= i   

  print("Factorial of " + num + "is" + result)
```


---

## Password Attempts  
The password checker  didn’t stop after three tries, so you could keep guessing forever. to fix the problem you had to add a `>=` to `if attempts > 3:` which made it work the right way.  

```python
attempts = 0
correct_password = "secret"

while True:
    password = input("Enter your password: ")
    attempts += 1

    if password == "incorrect_password":
        print("Correct password!")
    else:
        print("Incorrect password")

    if attempts > 3:
        print("Too many attempts")
        break
```

---
