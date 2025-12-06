**Learning Python Through Mistakes**

# Debugging mistakes using Python  

Debugging can feel frustrating at first, but it’s really just solving small puzzles step by step. Every bug teaches you something new about how Python works, from logic to syntax. Once you understand it, fixing mistakes becomes part of the fun.  

---

## Temperature Check    
This temperature program had a problem, it didn’t know what to do with numbers between 0 and 50. That meant it skipped a whole range of inputs without saying anything. The fix? Swap the last `elif` for an `else` so it catches everything that didn’t match the earlier conditions.


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
Heres a classic mix up, trying to count spaces but checking for an empty string instead. Since "" isn’t the same as " ", the loop didn’t count anything. Changing the condition to `if char == " "` made the counter do its job.


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
This one had two bugs. First, the input wasn’t converted to an integer, so the math operations failed. Second, the condition num % 2 < 0 didn’t correctly check for even numbers. You can fixing both with `int(input())` and `num % 2 == 0` made everything work smoothly.


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
 The issues here is that the print statement broke when trying to mix strings and integers. Expanding the loop and using a f‑string made the program calculate factorials correctly. 




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
## Wrap up

Debugging isn’t about being perfect, it’s about learning from the mistakes you make along the way. Every time your code breaks, you get a better idea of how Python actually works. It’s not always fun in the moment, but once you figure out the fix, it feels good like solving a puzzle.
So yeah, mistakes are part of the process. They don’t mean you’re bad at coding, they mean you’re getting better. The more bugs you run into, the more skills you pick up. That’s how you grow.

---
