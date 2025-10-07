# Ejercicio 06: Bubble Sort

**Nivel**: Intermedio | **Tiempo**: 40 min | **Conceptos**: Algoritmo ordenamiento

---

## Objetivo

Implementar algoritmo Bubble Sort para ordenar array.

---

## Concepto

Compara elementos adyacentes y los intercambia si están en orden incorrecto.

---

## Pseudocódigo

```
para i desde 0 hasta n-1:
    para j desde 0 hasta n-i-1:
        si arr[j] > arr[j+1]:
            intercambiar arr[j] y arr[j+1]
```

---

## Código Base

```c
#include <stdio.h>

void bubble_sort(int arr[], int n) {
    // Tu implementación aquí
}

void imprimir(int arr[], int n) {
    for (int i = 0; i < n; i++)
        printf("%d ", arr[i]);
    printf("\n");
}

int main(void) {
    int arr[] = {64, 34, 25, 12, 22, 11, 90};
    int n = 7;

    printf("Original: ");
    imprimir(arr, n);

    bubble_sort(arr, n);

    printf("Ordenado: ");
    imprimir(arr, n);

    return 0;
}
```

---

## Solución

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

## Desafíos

1. **Optimizar**: Early stop si no hay intercambios
2. **Contador**: Cuenta número de intercambios
3. **Descendente**: Ordena de mayor a menor
4. **Visualizar**: Imprime array después de cada pasada

---

#ejercicio #intermedio #bubble-sort #algoritmos
