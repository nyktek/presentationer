# Python - Random

---

# Importera random

--

```python []
import random
```

```python []
from random import randint
```

Vi använder slumptal i Python genom att importera modulen **random**

---

# random()

--

Ger ett flyttal i intervallet **0 - 1.0**

Blir _aldrig_ exakt **0** eller **1**.

--

```python []
import random

r = random.random()
print(r)
```

```python []
0.33244833625067194
```

--

```python []
from random import random

r = random()
print(r)
```

```python []
0.14875270475440316
```

---

# randrange()

--

Ger ett slumptal (heltal) i motsvarande range

--

```python []
# 1-10 heltal
from random import randrange

r = randrange(1, 10 + 1)
print(r)
```

```python []
3
```

--

```python []
# 1-10 udda heltal
from random import randrange

r = randrange(1, 10, 2)
print(r)
```

```python []
9
```

--

```python []
# 1-10 udda heltal
from random import randrange

for i in range(10):
    r = randrange(1, 10, 2)
    print(r, end=" ")
```

```python []
9 7 9 7 9 3 7 3 7 1
```

--

```python []
# 0-10 jämna heltal
from random import randrange

r = randrange(0, 10, 2)
print(r)
```

```python []
4
```

--

```python []
# 0-10 jämna heltal
from random import randrange

for i in range(10):
    r = randrange(0, 10, 2)
    print(r, end=" ")
```

```python []
2 0 8 4 6 8 8 0 4 2
```

--

```python []
# 0-10 jämna heltal
from random import randrange

listan = [randrange(0, 10, 2) for _ in range(10)]

print(*listan, sep=', ')
```

```python []
8, 0, 0, 2, 4, 0, 0, 4, 4, 4
```

---

# randint()

--

Ger ett heltal mellan **a** och **b**.

Utdatan kan verkligen anta extremvärdet.

--

```python []
# 1-10 heltal = alias till randrange(a, b+1)
from random import randint

r = randint(1, 10)
print(r)
```

```python []
10
```

---

# choice()

--

Väljer slumpmässigt ett element ur en sekvens, t.ex. en sträng, lista, tippel eller en range

--

```python []
# Väljer ett slumpmässigt element ur en sekvens
from random import choice

text = "ABCDE"
r = choice(text)

print(r)
```

```python []
B
```

--

```python []
# Väljer ett slumpmässigt element ur en sekvens
from random import choice

lista = ['Kalle', 'Ada', 'Humle', 'Dumle']
r = choice(lista)

print(r)
```

```python []
Ada
```

--

```python
# Väljer ett slumpmässigt element ur en sekvens
from random import choice

listan  = 'Kalle', 'Ada', 'Humle', 'Dumle'
r = choice(listan)

print(r)
```

```python []
Dumle
```

--

```python []
# Väljer ett slumpmässigt element ur en sekvens
from random import choice

numbers = range(50, 60 +1)
r = choice(numbers)

print(r)
```

```python []
57
```

---

# shuffle()

--

Blandar sekvensen _x_ på plats.

--

```python []
from random import shuffle

listan = [7, 65, 5, 42, 45, 12]
shuffle(listan)
print(listan)
```

```python []
[12, 45, 42, 7, 65, 5]
```

--

```python []
from random import shuffle

listan = [7, 65, 5, 42, 45, 12]
slumpad = listan.copy()
shuffle(slumpad)

print(listan, slumpad, sep="\n")
```

```python []
[7, 65, 5, 42, 45, 12]
[45, 12, 65, 7, 42, 5]
```

---

# sample()

--

Drar slumpmässigt _k_ st element ur en population.

--

```python []
from random import sample

listan = ['Kalle', 'Ada', 'Pelle', 'Marie', 'Elina', 'Olle']

val = sample(listan, k=2)

print(val)
```

```python []
['Marie', 'Kalle']
```

---

# Slut!
