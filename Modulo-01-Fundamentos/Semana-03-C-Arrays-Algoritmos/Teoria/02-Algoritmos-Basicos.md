# Algoritmos Básicos

> **Búsqueda y Ordenamiento en C**

---

## Índice

- [[#Algoritmos de Búsqueda]]
- [[#Algoritmos de Ordenamiento]]
- [[#Complejidad Temporal]]
- [[#Aplicaciones Prácticas]]

---

## Algoritmos de Búsqueda

### Búsqueda Lineal

**Concepto**: Revisar cada elemento hasta encontrar el objetivo

```c
int busqueda_lineal(int arr[], int tamaño, int objetivo) {
    for (int i = 0; i < tamaño; i++) {
        if (arr[i] == objetivo) {
            return i;  // Encontrado
        }
    }
    return -1;  // No encontrado
}
```

**Complejidad**: O(n)
**Uso**: Arrays no ordenados

### Búsqueda Binaria

**Concepto**: Divide el array a la mitad repetidamente
**Requisito**: Array DEBE estar ordenado

```c
int busqueda_binaria(int arr[], int tamaño, int objetivo) {
    int inicio = 0;
    int fin = tamaño - 1;

    while (inicio <= fin) {
        int medio = inicio + (fin - inicio) / 2;

        if (arr[medio] == objetivo) {
            return medio;
        }

        if (arr[medio] < objetivo) {
            inicio = medio + 1;
        } else {
            fin = medio - 1;
        }
    }

    return -1;
}
```

**Complejidad**: O(log n)
**Uso**: Arrays ordenados, mucho más rápido

**Ejemplo**:
```
Array: [1, 3, 5, 7, 9, 11, 13]
Buscar: 7

Paso 1: medio = 7 (índice 3) → 7 == 7 ✓
```

---

## Algoritmos de Ordenamiento

### Bubble Sort (Ordenamiento Burbuja)

**Concepto**: Compara pares adyacentes, intercambia si están en orden incorrecto

```c
void bubble_sort(int arr[], int tamaño) {
    for (int i = 0; i < tamaño - 1; i++) {
        for (int j = 0; j < tamaño - i - 1; j++) {
            if (arr[j] > arr[j + 1]) {
                // Intercambiar
                int temp = arr[j];
                arr[j] = arr[j + 1];
                arr[j + 1] = temp;
            }
        }
    }
}
```

**Complejidad**: O(n²)
**Ventaja**: Simple de entender
**Desventaja**: Muy lento para arrays grandes

**Visualización**:
```
[5, 2, 8, 1]
[2, 5, 8, 1]  (compara 5 y 2, intercambia)
[2, 5, 1, 8]  (compara 8 y 1, intercambia)
[2, 1, 5, 8]  (compara 5 y 1, intercambia)
[1, 2, 5, 8]  (compara 2 y 1, intercambia)
```

### Selection Sort (Ordenamiento por Selección)

**Concepto**: Encuentra el mínimo, lo coloca al inicio, repite

```c
void selection_sort(int arr[], int tamaño) {
    for (int i = 0; i < tamaño - 1; i++) {
        int min_idx = i;

        // Encontrar mínimo en resto del array
        for (int j = i + 1; j < tamaño; j++) {
            if (arr[j] < arr[min_idx]) {
                min_idx = j;
            }
        }

        // Intercambiar con posición actual
        int temp = arr[i];
        arr[i] = arr[min_idx];
        arr[min_idx] = temp;
    }
}
```

**Complejidad**: O(n²)
**Ventaja**: Menos intercambios que Bubble Sort

### Insertion Sort (Ordenamiento por Inserción)

**Concepto**: Construye array ordenado elemento por elemento

```c
void insertion_sort(int arr[], int tamaño) {
    for (int i = 1; i < tamaño; i++) {
        int key = arr[i];
        int j = i - 1;

        // Mover elementos mayores una posición adelante
        while (j >= 0 && arr[j] > key) {
            arr[j + 1] = arr[j];
            j--;
        }

        arr[j + 1] = key;
    }
}
```

**Complejidad**: O(n²)
**Ventaja**: Eficiente para arrays pequeños o casi ordenados

---

## Complejidad Temporal

### Notación Big O

| Complejidad | Nombre | Ejemplo |
|-------------|--------|---------|
| O(1) | Constante | Acceso a array[i] |
| O(log n) | Logarítmica | Búsqueda binaria |
| O(n) | Lineal | Búsqueda lineal |
| O(n log n) | Linearítmica | Merge sort (próxima semana) |
| O(n²) | Cuadrática | Bubble sort |
| O(2^n) | Exponencial | Problemas recursivos |

**Comparación con n=1000**:
- O(1): 1 operación
- O(log n): ~10 operaciones
- O(n): 1,000 operaciones
- O(n²): 1,000,000 operaciones

### Cuándo Usar Cada Algoritmo

**Búsqueda Lineal**:
- Array no ordenado
- Array pequeño
- Búsqueda única

**Búsqueda Binaria**:
- Array ordenado
- Múltiples búsquedas
- Array grande

**Bubble Sort**:
- Aprendizaje
- Arrays muy pequeños (<10 elementos)

**Insertion Sort**:
- Arrays casi ordenados
- Arrays pequeños

---

## Aplicaciones Prácticas

### Ejemplo Completo: Sistema de Calificaciones

```c
#include <stdio.h>

void ordenar_notas(int notas[], int tamaño) {
    // Insertion sort
    for (int i = 1; i < tamaño; i++) {
        int key = notas[i];
        int j = i - 1;
        while (j >= 0 && notas[j] > key) {
            notas[j + 1] = notas[j];
            j--;
        }
        notas[j + 1] = key;
    }
}

float promedio(int notas[], int tamaño) {
    int suma = 0;
    for (int i = 0; i < tamaño; i++) {
        suma += notas[i];
    }
    return (float)suma / tamaño;
}

int mediana(int notas[], int tamaño) {
    // Asume array ordenado
    if (tamaño % 2 == 0) {
        return (notas[tamaño/2 - 1] + notas[tamaño/2]) / 2;
    }
    return notas[tamaño/2];
}

int main(void) {
    int notas[] = {85, 92, 78, 90, 88};
    int tamaño = 5;

    printf("Notas originales: ");
    for (int i = 0; i < tamaño; i++) {
        printf("%d ", notas[i]);
    }
    printf("\n");

    ordenar_notas(notas, tamaño);

    printf("Notas ordenadas: ");
    for (int i = 0; i < tamaño; i++) {
        printf("%d ", notas[i]);
    }
    printf("\n");

    printf("Promedio: %.2f\n", promedio(notas, tamaño));
    printf("Mediana: %d\n", mediana(notas, tamaño));
    printf("Menor nota: %d\n", notas[0]);
    printf("Mayor nota: %d\n", notas[tamaño-1]);

    return 0;
}
```

---

## Desafíos

1. Implementa búsqueda binaria recursiva
2. Modifica bubble sort para optimizar (early stop)
3. Crea función que ordene strings alfabéticamente
4. Implementa contador de comparaciones en cada algoritmo

---

## Recursos

- [VisuAlgo](https://visualgo.net/en/sorting) - Visualizar algoritmos
- [Big O Cheat Sheet](https://www.bigocheatsheet.com/)
- [[01-Loops-Arrays-Funciones|Loops y Arrays]]
- [[../Ejercicios/README|Ejercicios Prácticos]]

---

#algoritmos #busqueda #ordenamiento #complejidad
