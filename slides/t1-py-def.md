# Python 

# Funktioner

---

# Exempel på en funktion


--


```python []
# Exempel på en funktion med två parametrar och type hints
def skriv_summa(x: int, y: int) -> None:
    summa: int = x + y
    print(f"Summan är: {summa}")

# Huvudprogram
if __name__ == "__main__":
    a: int = 3
    b: int = 4
    skriv_summa(a, b)
```

```html
Summan är: 7
```

--

<span class="fragment">En funktion skapas genom att man definierar (**dfn**) den med **namn**, **parametrar** inom parentes, och **kolon**.</span>

<span class="fragment">Det följande programblocket (indenterat precis som vanligt efter ett kolon) tillhör funktionen.</span>

<span class="fragment">Sedan skriver vi vårt huvudprogram precis som vanligt, och anropar där vår nya funktion med argument.</span>

--

## Vad händer i anropet?

<span class="fragment">Parametrarna **x**, **y** och variabeln **summa** är lokala i funktionen och kan inte ses utanför funktionen.</span>

<span class="fragment">Värdet av argumenten i funktionsanropet kopieras till parametrarna.</span>

<span class="fragment">Funktionen exekveras.</span>

<span class="fragment">När anropet avslutats fortsätter programmet efter funktionsanropet.</span>

---

# Defaultvärden på parametrarna

--

```python []
# Exempel på en funktion med två parametrar (en med standardvärde)
def skriv_summa(x: int, y: int = 1) -> None:
    summa: int = x + y
    print(f"Summan är: {summa}")

# Huvudprogram
if __name__ == "__main__":
    a: int = 3
    b: int = 4

    skriv_summa(a, b)
    skriv_summa(b)
```

```html []
Summan är: 7
Summan är: 5
```

--

<span class="fragment">Det finns ibland anledning att utlämna vissa parametrar som oftast antar ett specifikt värde.</span>

<span class="fragment">Den möjligheten kan man ange i parameterlistan genom att sätta ett visst default-värde på en parameter.</span>

<span class="fragment">De parametrar som kan ha default-värde **måste ligga längst till höger i listan**, annars vet inte Pyhton vilken man har angett och vilka som ska få default-värden.</span>

---

# Funktioner som returnerar värden

--

```python []
# Exempel på en funktion som returnerar ett värde
def medelvarde(x: float, y: float) -> float:
    medel: float = (x + y) / 2
    return medel

# Huvudprogram
if __name__ == "__main__":
    a: int = 3
    b: int = 4
    m: float = medelvarde(a, b)

    print(f"Medelvärdet är: {m}")
```

```html []
Medelvärdet är: 3.5
```

--

Väldigt vanligt är att vi vill ha tillbaka något från funktionsanropet, dvs att det skall returnera något värde.

Detta gör vi med **return**, och värdet "förs över" till utanför funktionsanropet och sparas lokalt.

--

```python []
# Exempel på en funktion som returnerar ett värde
def medelvarde(x: float, y: float) -> float:
    """Returnerar medelvärdet av parametrarna x och y"""
    medel: float = (x + y) / 2
    return medel
    
# Huvudprogram
if __name__ == "__main__":
    a: int = 3
    b: int = 4
    m: float = medelvarde(a, b)

    # print(f"Medelvärdet är: {m}")

    help(medelvarde)
```

--


```html []
medelvarde(x, y)
    Returnerar medelvärdet av parametrarna x och y
```

--

```python []
# Exempel på en funktion som returnerar ett värde
def medelvarde(x: float, y: float) -> float:
    """Returnerar medelvärdet av parametrarna x och y"""
    return (x + y) / 2
    
# Huvudprogram
if __name__ == "__main__":
    a: int = 3
    b: int = 4
    m: float = medelvarde(a, b)

    print(f"Medelvärdet är: {m}")
```

---

# Docstring

--

```python []
"""Förklarande text om vad funktionen gör

Args:
    kaka (float): Beskrivande text
    bulle (int): Beskrivande text (default is 10)

Returns:
    fika (list): Beskrivande text
"""
```

Vi skriver givetvis docstring:en på engelska

---

# SLUT
