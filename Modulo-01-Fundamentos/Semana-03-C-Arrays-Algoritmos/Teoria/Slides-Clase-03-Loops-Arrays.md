---
theme: black
highlightTheme: monokai
transition: slide
---

# Semana 3: Loops, Arrays y Algoritmos

**Módulo 1: Fundamentos**

Estructuras de Datos y Control de Flujo

---

## Agenda

1. Loops (for, while, do-while)
2. Arrays (arreglos)
3. Funciones
4. Algoritmos de búsqueda
5. Algoritmos de ordenamiento
6. Proyecto de la semana

---

## Repaso Semana 2

**¿Qué aprendimos?**

- Variables y tipos de datos
- printf/scanf
- Operadores
- Condicionales (if/else, switch)

**Hoy añadimos**:
- Repetición (loops)
- Colecciones (arrays)
- Reutilización (funciones)

---

# Parte 1: Loops

---

## ¿Por Qué Loops?

**Sin loop** (repetitivo):
```c
printf("1\n");
printf("2\n");
printf("3\n");
printf("4\n");
printf("5\n");
```

**Con loop** (eficiente):
```c
for (int i = 1; i <= 5; i++) {
    printf("%d\n", i);
}
```

---

## for Loop

**Sintaxis**:
```c
for (inicio; condición; incremento) {
    // código
}
```

**Ejemplo**:
```c
for (int i = 0; i < 5; i++) {
    printf("%d ", i);
}
// Output: 0 1 2 3 4
```

---

## Desglose del for

```c
for (int i = 0; i < 5; i++)
     ────┬──── ──┬─── ─┬──
         │       │      │
    Inicio   Condición  Incremento
```

1. **Inicio**: `i = 0` (una vez)
2. **Condición**: `i < 5` (antes de cada iteración)
3. **Código**: Se ejecuta si condición es verdadera
4. **Incremento**: `i++` (después de cada iteración)
5. **Repetir** desde paso 2

---

## while Loop

**Sintaxis**:
```c
while (condición) {
    // código
}
```

**Ejemplo**:
```c
int i = 0;
while (i < 5) {
    printf("%d ", i);
    i++;
}
```

**Usa while cuando**: No sabes cuántas iteraciones necesitas

---

## do-while Loop

**Sintaxis**:
```c
do {
    // código
} while (condición);
```

**Ejemplo**:
```c
int num;
do {
    printf("Ingresa positivo: ");
    scanf("%d", &num);
} while (num <= 0);
```

**Característica**: Ejecuta AL MENOS UNA VEZ

---

## Comparación Loops

| Loop | Verifica | Mín. Ejecuciones |
|------|----------|------------------|
| for | Inicio | 0 |
| while | Inicio | 0 |
| do-while | Final | 1 |

---

## break y continue

**break** - Sale del loop:
```c
for (int i = 0; i < 10; i++) {
    if (i == 5) break;
    printf("%d ", i);
}
// Output: 0 1 2 3 4
```

**continue** - Salta iteración:
```c
for (int i = 0; i < 5; i++) {
    if (i == 2) continue;
    printf("%d ", i);
}
// Output: 0 1 3 4
```

---

# Parte 2: Arrays

---

## ¿Qué es un Array?

**Definición**: Colección de elementos del mismo tipo

**Analogía**: Fila de casilleros numerados

```
  [0]   [1]   [2]   [3]   [4]
┌─────┬─────┬─────┬─────┬─────┐
│  10 │  20 │  30 │  40 │  50 │
└─────┴─────┴─────┴─────┴─────┘
```

**Índices empiezan en 0**

---

## Declarar Arrays

**Sintaxis**:
```c
tipo nombre[tamaño];
```

**Ejemplos**:
```c
int numeros[5];                  // Sin inicializar
int edades[3] = {18, 25, 30};   // Inicializar
float precios[] = {9.99, 14.50}; // Tamaño automático
```

---

## Acceder a Elementos

```c
int arr[5] = {10, 20, 30, 40, 50};

// Leer
printf("%d\n", arr[0]);  // 10
printf("%d\n", arr[4]);  // 50

// Modificar
arr[2] = 100;
printf("%d\n", arr[2]);  // 100
```

**Cuidado**: `arr[5]` es error (índice fuera de rango)

---

## Recorrer Arrays

**Pattern común**:
```c
int numeros[] = {1, 2, 3, 4, 5};
int tamaño = 5;

for (int i = 0; i < tamaño; i++) {
    printf("%d ", numeros[i]);
}
```

**Calcular tamaño**:
```c
int tamaño = sizeof(arr) / sizeof(arr[0]);
```

---

## Llenar Array con Input

```c
int numeros[5];

for (int i = 0; i < 5; i++) {
    printf("Elemento %d: ", i + 1);
    scanf("%d", &numeros[i]);
}
```

---

## Strings = Arrays de char

```c
char nombre[] = "Ana";
// Equivale a: {'A', 'n', 'a', '\0'}
//                              ↑
//                        Null terminator

printf("%s\n", nombre);  // Ana
printf("%c\n", nombre[0]);  // A
```

**Importante**: `\0` marca fin del string

---

# Parte 3: Funciones

---

## ¿Por Qué Funciones?

**Sin funciones** (repetitivo):
```c
// Calcular área círculo 1
float area1 = 3.14 * r1 * r1;

// Calcular área círculo 2
float area2 = 3.14 * r2 * r2;

// ...repetir muchas veces
```

**Con función** (reutilizable):
```c
float area_circulo(float radio) {
    return 3.14 * radio * radio;
}
```

---

## Anatomía de una Función

```c
int sumar(int a, int b) {
──┬── ──┬── ──────┬─────
  │     │         │
Tipo  Nombre  Parámetros
Retorno

    return a + b;
    ──────┬──────
       Retorno
}
```

---

## Ejemplo Completo

```c
#include <stdio.h>

// Prototipo
int sumar(int a, int b);

int main(void) {
    int resultado = sumar(5, 3);
    printf("%d\n", resultado);  // 8
    return 0;
}

// Definición
int sumar(int a, int b) {
    return a + b;
}
```

---

## Funciones void

**Sin retorno**:
```c
void saludar(char nombre[]) {
    printf("Hola, %s!\n", nombre);
}

int main(void) {
    saludar("Ana");  // Hola, Ana!
    return 0;
}
```

---

## Funciones con Arrays

```c
float promedio(int arr[], int tamaño) {
    int suma = 0;
    for (int i = 0; i < tamaño; i++) {
        suma += arr[i];
    }
    return (float)suma / tamaño;
}

int main(void) {
    int notas[] = {85, 90, 78, 92};
    printf("Promedio: %.2f\n", promedio(notas, 4));
    return 0;
}
```

---

# Parte 4: Algoritmos de Búsqueda

---

## Búsqueda Lineal

**Concepto**: Revisar cada elemento

```c
int buscar(int arr[], int tamaño, int objetivo) {
    for (int i = 0; i < tamaño; i++) {
        if (arr[i] == objetivo) {
            return i;
        }
    }
    return -1;
}
```

**Complejidad**: O(n)
**Uso**: Arrays no ordenados

---

## Búsqueda Binaria

**Concepto**: Divide array a la mitad

**Requisito**: Array ORDENADO

```c
int busqueda_binaria(int arr[], int tamaño, int objetivo) {
    int inicio = 0, fin = tamaño - 1;

    while (inicio <= fin) {
        int medio = inicio + (fin - inicio) / 2;

        if (arr[medio] == objetivo) return medio;

        if (arr[medio] < objetivo)
            inicio = medio + 1;
        else
            fin = medio - 1;
    }
    return -1;
}
```

---

## Visualización Búsqueda Binaria

**Buscar 7 en [1, 3, 5, 7, 9, 11, 13]**:

```
Paso 1: [1, 3, 5, │7│, 9, 11, 13]
        medio = 7 → ¡Encontrado!
```

**Buscar 11**:
```
Paso 1: [1, 3, 5, │7│, 9, 11, 13]
        7 < 11 → buscar derecha

Paso 2: [9, │11│, 13]
        11 == 11 → ¡Encontrado!
```

---

## Lineal vs Binaria

**Array de 1,000,000 elementos**:

- Lineal: hasta 1,000,000 comparaciones
- Binaria: máximo 20 comparaciones

**Binaria es ~50,000x más rápida**

---

# Parte 5: Ordenamiento

---

## Bubble Sort

**Concepto**: Compara pares adyacentes

```c
void bubble_sort(int arr[], int n) {
    for (int i = 0; i < n-1; i++) {
        for (int j = 0; j < n-i-1; j++) {
            if (arr[j] > arr[j+1]) {
                int temp = arr[j];
                arr[j] = arr[j+1];
                arr[j+1] = temp;
            }
        }
    }
}
```

---

## Visualización Bubble Sort

```
[5, 2, 8, 1]
↓ Compara 5 y 2, intercambia
[2, 5, 8, 1]
↓ 5 y 8 OK
[2, 5, 8, 1]
↓ Compara 8 y 1, intercambia
[2, 5, 1, 8]
↓ ...continúa
[1, 2, 5, 8]  ✓ Ordenado
```

---

## Selection Sort

**Concepto**: Encuentra mínimo, coloca al inicio

```c
void selection_sort(int arr[], int n) {
    for (int i = 0; i < n-1; i++) {
        int min_idx = i;
        for (int j = i+1; j < n; j++) {
            if (arr[j] < arr[min_idx])
                min_idx = j;
        }
        // Intercambiar
        int temp = arr[i];
        arr[i] = arr[min_idx];
        arr[min_idx] = temp;
    }
}
```

---

## Complejidad Temporal

| Algoritmo | Mejor | Promedio | Peor |
|-----------|-------|----------|------|
| Bubble | O(n) | O(n²) | O(n²) |
| Selection | O(n²) | O(n²) | O(n²) |
| Insertion | O(n) | O(n²) | O(n²) |
| Búsq. Lineal | O(1) | O(n) | O(n) |
| Búsq. Binaria | O(1) | O(log n) | O(log n) |

---

## Big O Visual

**n = 100 elementos**:

- O(1): 1 operación
- O(log n): ~7 operaciones
- O(n): 100 operaciones
- O(n²): 10,000 operaciones

**La diferencia es ENORME en arrays grandes**

---

# Ejercicio en Clase

---

## Desafío: Sistema de Notas

Crear programa que:
1. Pida 5 notas
2. Las almacene en array
3. Calcule promedio
4. Ordene de menor a mayor
5. Muestre mediana

**15 minutos**

---

## Solución

```c
#include <stdio.h>

void ordenar(int arr[], int n) {
    for (int i = 0; i < n-1; i++) {
        for (int j = i+1; j < n; j++) {
            if (arr[i] > arr[j]) {
                int temp = arr[i];
                arr[i] = arr[j];
                arr[j] = temp;
            }
        }
    }
}

int main(void) {
    int notas[5];
    int suma = 0;

    for (int i = 0; i < 5; i++) {
        printf("Nota %d: ", i+1);
        scanf("%d", &notas[i]);
        suma += notas[i];
    }

    printf("Promedio: %.2f\n", (float)suma/5);

    ordenar(notas, 5);

    printf("Ordenadas: ");
    for (int i = 0; i < 5; i++) {
        printf("%d ", notas[i]);
    }
    printf("\nMediana: %d\n", notas[2]);

    return 0;
}
```

---

# Proyecto de la Semana

---

## Opciones

**Básico**:
- Sistema de inventario simple
- Calculadora de estadísticas

**Intermedio**:
- Buscador en lista de contactos
- Analizador de texto

**Avanzado**:
- Implementar todos los algoritmos
- Comparador de rendimiento

---

## Requisitos

- [ ] Usar arrays
- [ ] Implementar al menos 1 algoritmo de búsqueda
- [ ] Implementar al menos 1 algoritmo de ordenamiento
- [ ] Crear mínimo 2 funciones propias
- [ ] Menú interactivo

---

# Resumen

---

## Lo que Aprendimos

1. **Loops**: for, while, do-while
2. **Arrays**: Colecciones de datos
3. **Funciones**: Reutilización de código
4. **Búsqueda**: Lineal y binaria
5. **Ordenamiento**: Bubble, Selection
6. **Complejidad**: Big O notation

---

## Patrones Clave

**Recorrer array**:
```c
for (int i = 0; i < tamaño; i++)
    usar arr[i]
```

**Buscar elemento**:
```c
for cada elemento
    if elemento == objetivo
        return índice
```

**Ordenar**:
```c
for cada posición
    encontrar/colocar elemento correcto
```

---

## Próxima Semana

**Semana 4: Git & GitHub**

- Control de versiones
- Repositorios
- Commits, push, pull
- Colaboración

**Preparación**: Crear cuenta en GitHub

---

## Recursos

**Documentación**:
- [[01-Loops-Arrays-Funciones]]
- [[02-Algoritmos-Basicos]]

**Visualizadores**:
- [VisuAlgo](https://visualgo.net/)
- [Python Tutor - C](http://pythontutor.com/c.html)

---

# ¿Preguntas?

**Dudas sobre**:
- Loops
- Arrays
- Funciones
- Algoritmos
- El proyecto

---

# ¡A Programar!

**Esta semana practica**:
- Escribir muchos loops
- Manipular arrays
- Crear funciones
- Implementar algoritmos

**El dominio viene con la práctica**

---

# ¡Gracias!

**Recursos**:
- [[../Ejercicios/README]]
- [[../Proyectos/README]]

**Happy coding!**
