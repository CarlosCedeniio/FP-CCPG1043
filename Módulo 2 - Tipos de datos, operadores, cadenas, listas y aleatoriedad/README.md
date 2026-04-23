# Módulo 2 - Tipos de datos, operadores, cadenas, listas y aleatoriedad

Este módulo cubre los tipos de datos fundamentales en Python, el uso de operadores aritméticos y lógicos, la manipulación de cadenas de texto con f-strings y métodos de string, el manejo de listas, búsquedas dentro de ellas, y la generación de valores aleatorios.

## Contenido

| Archivo | Descripción |
|---------|-------------|
| [2.1 Variables y tipos de datos](2.1%20Variables%20y%20tipos%20de%20datos.html) | Declaración de variables, tipos primitivos (`int`, `float`, `str`, `bool`) y conversión de tipos |
| [2.2 f-strings](2.2%20f-strings.html) | Interpolación de variables en cadenas usando f-strings y formato de salida |
| [2.3 Manipulación de Strings](2.3%20Manipulaci%C3%B3n%20de%20Strings.html) | Métodos de strings: `upper`, `lower`, `strip`, `split`, `replace`, indexación y slicing |
| [2.4 Listas](2.4%20Listas.html) | Creación, acceso, modificación y operaciones básicas con listas |
| [2.5 Métodos en Listas](2.5%20Metodos%20en%20Listas.html) | Métodos de listas: `append`, `remove`, `sort`, `pop`, `insert`, entre otros |
| [2.6 Búsquedas en listas](2.6%20Busquedas%20en%20listas.html) | Búsqueda de elementos con `in`, `index`, y recorrido con bucles |
| [2.7 Aleatoriedad](2.7%20Aleatoriedad.html) | Uso del módulo `random`: `random()`, `randint()`, `choice()`, `shuffle()` |

## Shortcuts de Python útiles en este módulo

### Tipos de datos

```python
# Conversión de tipos
int("42")        # str → int
float("3.14")    # str → float
str(100)         # int → str
bool(0)          # 0, "", [], None → False

# Verificar tipo
type(variable)
isinstance(x, int)
```

### Operadores

```python
# Aritméticos
+  -  *  /    # suma, resta, multiplicación, división (float)
//            # división entera
%             # módulo (resto)
**            # potencia

# Comparación
==  !=  <  >  <=  >=

# Lógicos
and  or  not
```

### f-strings

```python
nombre = "Ana"
edad = 20
print(f"Hola, {nombre}. Tienes {edad} años.")

# Formato numérico
pi = 3.14159
print(f"{pi:.2f}")        # → 3.14
print(f"{1000:,}")        # → 1,000
print(f"{0.75:.0%}")      # → 75%
```

### Strings

```python
s = "  Hola Mundo  "

s.upper()          # → "  HOLA MUNDO  "
s.lower()          # → "  hola mundo  "
s.strip()          # → "Hola Mundo"
s.replace("Hola", "Adiós")
s.split(" ")       # → lista de palabras
s.startswith("H")
s.endswith("o")
len(s)

# Indexación y slicing
s[0]       # primer carácter
s[-1]      # último carácter
s[1:4]     # caracteres del índice 1 al 3
s[::-1]    # string invertido
```

### Listas

```python
lista = [1, 2, 3, 4, 5]

lista.append(6)        # agregar al final
lista.insert(0, 0)     # insertar en posición
lista.remove(3)        # eliminar por valor
lista.pop()            # eliminar y retornar el último
lista.pop(i)           # eliminar en posición i
lista.sort()           # ordenar in-place
sorted(lista)          # retorna nueva lista ordenada
lista.reverse()
lista.index(2)         # índice del valor 2
len(lista)

# Slicing
lista[1:3]     # sublista del índice 1 al 2
lista[::-1]    # lista invertida
```

### Búsquedas en listas

```python
lista = ["a", "b", "c"]

"a" in lista           # True
"z" not in lista       # True
lista.index("b")       # → 1
lista.count("a")       # → 1

# Recorrer con índice
for i, v in enumerate(lista):
    print(i, v)
```

### Aleatoriedad

```python
import random

random.random()            # float en [0.0, 1.0)
random.randint(1, 10)      # int entre 1 y 10 (inclusive)
random.choice(lista)       # elemento aleatorio de una lista
random.choices(lista, k=3) # k elementos con reemplazo
random.sample(lista, k=2)  # k elementos sin reemplazo
random.shuffle(lista)      # mezcla la lista in-place
random.seed(42)            # fijar semilla para reproducibilidad
```

## Recursos adicionales

- [Página oficial de la materia](http://programacion.espol.edu.ec/)
- [Ejercicios y exámenes resueltos](http://blog.espol.edu.ec/ccpg1001/)
- [Documentación Python - Tipos built-in](https://docs.python.org/3/library/stdtypes.html)
- [Documentación Python - Módulo random](https://docs.python.org/3/library/random.html)
- [CS50 Python Harvard <- Muy recomendado](https://cs50.harvard.edu/python/weeks/0/)
