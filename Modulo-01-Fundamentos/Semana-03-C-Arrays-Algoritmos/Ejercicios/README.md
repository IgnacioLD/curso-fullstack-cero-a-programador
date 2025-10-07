# Ejercicios - Semana 03: Arrays y Algoritmos

**Módulo 1: Fundamentos - Loops, Arrays, Funciones**

---

## Objetivo

Dominar loops, arrays, funciones y algoritmos básicos.

---

## Lista de Ejercicios

### Nivel Básico

| # | Ejercicio | Conceptos | Tiempo |
|---|-----------|-----------|--------|
| 01 | [[Ejercicio-01-Suma-Array|Suma de Array]] | Loops, arrays | 20 min |
| 02 | [[Ejercicio-02-Maximo-Minimo|Máximo y Mínimo]] | Búsqueda en array | 25 min |
| 03 | [[Ejercicio-03-Invertir-Array|Invertir Array]] | Manipulación arrays | 30 min |
| 04 | [[Ejercicio-04-Contar-Pares|Contar Pares]] | Condicionales + loops | 20 min |

### Nivel Intermedio

| # | Ejercicio | Conceptos | Tiempo |
|---|-----------|-----------|--------|
| 05 | [[Ejercicio-05-Busqueda-Lineal|Búsqueda Lineal]] | Algoritmo búsqueda | 30 min |
| 06 | [[Ejercicio-06-Bubble-Sort|Bubble Sort]] | Ordenamiento | 40 min |
| 07 | [[Ejercicio-07-Funciones-Array|Funciones con Arrays]] | Funciones, paso parámetros | 35 min |

### Nivel Avanzado

| # | Ejercicio | Conceptos | Tiempo |
|---|-----------|-----------|--------|
| 08 | [[Ejercicio-08-Busqueda-Binaria|Búsqueda Binaria]] | Algoritmo optimizado | 50 min |
| 09 | [[Ejercicio-09-Estadisticas|Estadísticas Array]] | Múltiples funciones | 60 min |
| 10 | [[Ejercicio-10-Selection-Sort|Selection Sort]] | Algoritmo ordenamiento | 50 min |

---

## Plantilla Base con Arrays

```c
#include <stdio.h>

// Prototipo
void procesar_array(int arr[], int tamaño);

int main(void) {
    int arr[100];
    int n;

    printf("Cantidad elementos: ");
    scanf("%d", &n);

    for (int i = 0; i < n; i++) {
        printf("Elemento %d: ", i+1);
        scanf("%d", &arr[i]);
    }

    procesar_array(arr, n);

    return 0;
}

void procesar_array(int arr[], int tamaño) {
    // Tu código aquí
}
```

---

## Patrones Comunes

**Recorrer**:
```c
for (int i = 0; i < tamaño; i++)
    printf("%d ", arr[i]);
```

**Buscar**:
```c
for (int i = 0; i < tamaño; i++)
    if (arr[i] == objetivo)
        return i;
```

**Modificar**:
```c
for (int i = 0; i < tamaño; i++)
    arr[i] = arr[i] * 2;
```

---

## Compilación

```bash
gcc ejercicio.c -o ejercicio -Wall
./ejercicio
```

---

#c #ejercicios #arrays #loops #algoritmos
