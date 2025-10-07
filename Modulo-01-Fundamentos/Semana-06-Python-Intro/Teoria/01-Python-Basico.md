# Introducción a Python

> **Semana 6 - Módulo 1: Fundamentos**
> **De C a Python: Un lenguaje más amigable**

---

## Objetivos

- Instalar y configurar Python
- Entender diferencias C vs Python
- Sintaxis básica de Python
- Variables, tipos de datos, operadores
- Condicionales y loops
- Funciones y listas
- Reescribir programas C en Python

---

## Python vs C

| Característica | C | Python |
|----------------|---|--------|
| **Compilado** | Sí | No (interpretado) |
| **Tipado** | Estático | Dinámico |
| **Gestión memoria** | Manual | Automática |
| **Sintaxis** | Verbosa | Concisa |
| **Velocidad** | Muy rápido | Más lento |
| **Facilidad** | Difícil | Fácil |
| **Uso** | Sistemas, hardware | Web, data, IA |

---

## Instalación

### Python 3

**Linux/macOS**:
```bash
# Verificar si está instalado
python3 --version

# Instalar (Ubuntu)
sudo apt install python3 python3-pip

# Instalar (macOS)
brew install python3
```

**Windows**:
- Descargar de [python.org](https://python.org)
- Marcar "Add Python to PATH"
- Instalar

### Ejecutar Python

**Modo interactivo** (REPL):
```bash
python3
>>> print("Hola")
Hola
>>> 2 + 2
4
>>> exit()
```

**Ejecutar archivo**:
```bash
python3 programa.py
```

---

## Sintaxis Básica

### Hello World

**C**:
```c
#include <stdio.h>

int main(void) {
    printf("Hello, World!\n");
    return 0;
}
```

**Python**:
```python
print("Hello, World!")
```

**Diferencias**:
- Sin `#include`
- Sin `main()`
- Sin `;`
- Sin `return 0`

---

## Variables y Tipos

### Declaración

**C**:
```c
int edad = 25;
float altura = 1.75;
char nombre[] = "Ana";
```

**Python**:
```python
edad = 25
altura = 1.75
nombre = "Ana"
```

**Sin declarar tipo**, Python infiere automáticamente

### Tipos Básicos

```python
# Números
entero = 42
decimal = 3.14
complejo = 2 + 3j

# Texto
nombre = "Ana"
mensaje = 'Hola'
multilinea = """Línea 1
Línea 2
Línea 3"""

# Booleanos
verdadero = True
falso = False

# None (equivale a NULL en C)
vacio = None

# Ver tipo
print(type(edad))  # <class 'int'>
```

### Conversiones

```python
# String a int
numero = int("42")

# Int a string
texto = str(42)

# Float a int
entero = int(3.14)  # 3

# String a float
decimal = float("3.14")
```

---

## Entrada y Salida

### print()

```python
# Simple
print("Hola")

# Múltiples valores
print("Hola", "mundo")  # Hola mundo

# Sin espacio
print("Hola", "mundo", sep="")  # Holamundo

# Sin salto de línea
print("Hola", end="")
print(" mundo")  # Hola mundo

# F-strings (Python 3.6+)
nombre = "Ana"
edad = 25
print(f"Me llamo {nombre} y tengo {edad} años")

# Format antiguo
print("Me llamo {} y tengo {} años".format(nombre, edad))
```

### input()

```python
# Leer string
nombre = input("¿Tu nombre? ")
print(f"Hola, {nombre}")

# Leer número
edad = int(input("¿Tu edad? "))
print(f"Tienes {edad} años")

# Leer float
altura = float(input("¿Tu altura? "))
```

**Comparación con C**:
```c
// C
int edad;
scanf("%d", &edad);

# Python
edad = int(input())
```

---

## Operadores

### Aritméticos

```python
a = 10
b = 3

print(a + b)   # 13
print(a - b)   # 7
print(a * b)   # 30
print(a / b)   # 3.333... (siempre float)
print(a // b)  # 3 (división entera)
print(a % b)   # 1 (módulo)
print(a ** b)  # 1000 (potencia)
```

**Diferencia clave**: `/` siempre retorna float, usa `//` para entero

### Comparación

```python
a == b   # Igual
a != b   # Diferente
a > b    # Mayor
a < b    # Menor
a >= b   # Mayor o igual
a <= b   # Menor o igual
```

### Lógicos

```python
# and, or, not (en lugar de &&, ||, !)
if edad >= 18 and tiene_licencia:
    print("Puede conducir")

if es_fin_semana or es_feriado:
    print("No hay clases")

if not tiene_permiso:
    print("Acceso denegado")
```

---

## Condicionales

### if / elif / else

**C**:
```c
if (nota >= 90) {
    printf("A\n");
} else if (nota >= 80) {
    printf("B\n");
} else {
    printf("F\n");
}
```

**Python**:
```python
if nota >= 90:
    print("A")
elif nota >= 80:
    print("B")
else:
    print("F")
```

**Diferencias**:
- Sin paréntesis `()`
- Sin llaves `{}`
- Indentación obligatoria (4 espacios)
- `elif` en lugar de `else if`

### Match-Case (Python 3.10+)

```python
opcion = input("Elige (a/b/c): ")

match opcion:
    case 'a':
        print("Opción A")
    case 'b':
        print("Opción B")
    case 'c':
        print("Opción C")
    case _:
        print("Inválida")
```

---

## Loops

### for Loop

**C**:
```c
for (int i = 0; i < 5; i++) {
    printf("%d\n", i);
}
```

**Python**:
```python
for i in range(5):
    print(i)

# range(start, stop, step)
for i in range(1, 10, 2):  # 1, 3, 5, 7, 9
    print(i)
```

### while Loop

**C**:
```c
int i = 0;
while (i < 5) {
    printf("%d\n", i);
    i++;
}
```

**Python**:
```python
i = 0
while i < 5:
    print(i)
    i += 1
```

### break y continue

```python
for i in range(10):
    if i == 5:
        break
    print(i)  # 0 1 2 3 4

for i in range(5):
    if i == 2:
        continue
    print(i)  # 0 1 3 4
```

---

## Listas (Arrays)

### Crear Listas

**C**:
```c
int numeros[] = {1, 2, 3, 4, 5};
```

**Python**:
```python
numeros = [1, 2, 3, 4, 5]

# Tipos mixtos (no en C)
mixto = [1, "dos", 3.0, True]

# Lista vacía
vacia = []
```

### Acceso y Modificación

```python
numeros = [10, 20, 30, 40, 50]

# Acceso
print(numeros[0])   # 10
print(numeros[-1])  # 50 (último)
print(numeros[-2])  # 40 (penúltimo)

# Modificar
numeros[2] = 100
print(numeros)  # [10, 20, 100, 40, 50]

# Slicing
print(numeros[1:3])   # [20, 100]
print(numeros[:3])    # [10, 20, 100]
print(numeros[2:])    # [100, 40, 50]
```

### Métodos de Listas

```python
nums = [1, 2, 3]

nums.append(4)       # [1, 2, 3, 4]
nums.insert(0, 0)    # [0, 1, 2, 3, 4]
nums.remove(2)       # [0, 1, 3, 4]
nums.pop()           # [0, 1, 3] (elimina último)
nums.sort()          # Ordenar
nums.reverse()       # Invertir
len(nums)            # Longitud
```

### Iterar Listas

```python
numeros = [1, 2, 3, 4, 5]

# Forma simple
for num in numeros:
    print(num)

# Con índice
for i in range(len(numeros)):
    print(i, numeros[i])

# Con enumerate
for i, num in enumerate(numeros):
    print(i, num)
```

---

## Funciones

### Definir Funciones

**C**:
```c
int sumar(int a, int b) {
    return a + b;
}
```

**Python**:
```python
def sumar(a, b):
    return a + b

resultado = sumar(5, 3)
print(resultado)  # 8
```

### Parámetros Opcionales

```python
def saludar(nombre, saludo="Hola"):
    print(f"{saludo}, {nombre}")

saludar("Ana")              # Hola, Ana
saludar("Bob", "Buenos días")  # Buenos días, Bob
```

### Múltiples Retornos

```python
def operaciones(a, b):
    return a + b, a - b, a * b

suma, resta, producto = operaciones(10, 5)
print(suma)      # 15
print(resta)     # 5
print(producto)  # 50
```

---

## Comparación Completa: C vs Python

### Suma de Array

**C**:
```c
int suma_array(int arr[], int tamaño) {
    int suma = 0;
    for (int i = 0; i < tamaño; i++) {
        suma += arr[i];
    }
    return suma;
}

int main(void) {
    int nums[] = {1, 2, 3, 4, 5};
    printf("%d\n", suma_array(nums, 5));
    return 0;
}
```

**Python**:
```python
def suma_lista(lista):
    return sum(lista)

nums = [1, 2, 3, 4, 5]
print(suma_lista(nums))

# O directamente
print(sum(nums))
```

---

## Recursos

- [Python Official Tutorial](https://docs.python.org/3/tutorial/)
- [Learn Python](https://www.learnpython.org/)
- [Real Python](https://realpython.com/)
- [[../Ejercicios/README|Ejercicios]]

---

#python #introduccion #c-vs-python #semana6
