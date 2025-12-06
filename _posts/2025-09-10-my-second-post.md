**Learning Python Through Mistakes**

# Debugging mistakes using Python  

Debugging can feel frustrating at first, but it’s really just solving small puzzles step by step. Every bug teaches you something new about how Python works, from logic to syntax. Once you get into the rhythm, fixing mistakes becomes part of the fun.  

---

## Temperature Check  
The temperature program didn’t know what to do with numbers between 0 and 50, so it skipped them entirely. That left a gap where the program gave no answer, which made it incomplete. Changing the last `elif` to `else` fixed the issue and covered all cases.  

<img src="/blog/images/temp.png" alt="picture" width="500 length=250 ">

---

## Counting Spaces  
The space counter was broken because it was checking for an empty string instead of a space. That meant the loop never actually counted anything, even though spaces were there. Switching the condition to `if char == " "` made the program work correctly.  

<img src="/blog/images/text.png" alt="picture" width="500 length=250 ">

---

## Even or Odd  
The even‑odd program had two problems: the input wasn’t converted to an integer, and the condition was wrong. Without fixing those, the program couldn’t do math or check numbers properly. Using `int(input())` and `num % 2 == 0` solved both issues.  

<img src="/blog/images/number.png" alt="picture" width="500 length=250">

---

## Factorial Function  
The factorial program stopped too early because the loop didn’t include the final number. On top of that, the print statement broke when trying to mix strings and integers. Expanding the loop and using an f‑string made the program calculate factorials correctly.  

<img src="/blog/images/integer.png" alt="picture" width="500 length=250">

---

## Password Attempts  
The password checker was comparing against the wrong string, which made it impossible to log in. It also didn’t stop after three tries, so you could keep guessing forever. Fixing the condition and adding a limit made it behave like a real login system.  

<img src="/blog/images/attempts.png" alt="picture" width="500 length=250">

---

