# Python 

# For-loopar

---

# Exempel 1

--

```python [ ]
for number in range(1, 3):
    answer = number + number
    print(f"{number} + {number} = {answer}")

print("\nUtanför loopen")
```

Vad kommer resultatet att bli?

--

```text [ ]
1 + 1 = 2
2 + 2 = 4  
   
Utanför loopen
```

**range(1, 3)** = Ett till tre, **INTE** ett till och med tre.

---

# Exempel 2

--

```python [ ]
for number in range(3):
    answer = number + number
    print(f"{number} + {number} = {answer}")

print("\nUtanför loopen")
```

Vad kommer resultatet att bli?

--

```text [ ]
0 + 0 = 0
1 + 1 = 2     
2 + 2 = 4
     
Utanför loopen
```

**range(3)** = Noll till tre, dvs fyra varv.

---

# Exempel 3

--

```python [ ]
for number in range(1, 10, 2):
    print(number)

print("\nUtanför loopen")
```

Vad kommer resultatet att bli?

--

```text [ ]
1
3
5
7
9

Utanför loopen
```

**range(1, 10, 2)** = Ett till tio och stegvärde på två.

---

# Exempel 4

--

```python [ ]
for number in range(0, 10, 2):
    print(number)

print("\nUtanför loopen")
```

Vad kommer resultatet att bli?

--

```text [ ]
0
2
4
6
8

Utanför loopen
```

**range(0, 10, 2)** = Noll till tio och stegvärde på två.

---


# Exempel 5

--

```python [ ]
for number in range(5, -1, -1):
    print(number)

print("\nUtanför loopen")
```

Vad kommer resultatet att bli?

--

```text [ ]
5
4
3
2
1
0

Utanför loopen
```

**range(5, -1, -1)** = Fem till minus ett och stegvärde på minus ett.

---

# Exempel 6

--

```python [ ]
start = 1
stop = 10
step = 2

for number in range(start, stop, step):
    print(number)

print("\nUtanför loopen")
```

Vad kommer resultatet att bli?

--

```text [ ]
1
3
5
7
9

Utanför loopen
```

---

# Exempel 7

--

```python [ ]
text = "Teknik"

for char in text:
    print(char)

print("\nUtanför loopen")
```

Vad kommer resultatet att bli?

--

```text [ ]
T
e
k
n
i
k

Utanför loopen
```

---

# Exempel 8

--

```python [ ]
for i in range(3):
    print(i)
else:
    print("Klar!")

print("\nUtanför loopen")
```

Vad kommer resultatet att bli?

--

```text [ ]
0
1
2
Klar!

Utanför loopen
```

---

# Exempel 9

--

```python [ ]
for student in ["Kurt", "Ada", "Bengt", "Eva"]:
    print(f"- {student}")

print("\nUtanför loopen")
```

Vad kommer resultatet att bli?

--

```text [ ]
- Kurt
- Ada
- Bengt
- Eva

Utanför loopen
```

---

# SLUT!