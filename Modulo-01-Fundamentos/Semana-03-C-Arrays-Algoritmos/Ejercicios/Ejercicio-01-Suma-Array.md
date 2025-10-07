# Ejercicio 01: Suma de Array

**Nivel**: Básico | **Tiempo**: 20 min | **Conceptos**: Loops, arrays

---

## Objetivo

Sumar todos los elementos de un array.

---

## Especificaciones

**Input**:
```
Cantidad: 5
Elemento 1: 10
Elemento 2: 20
Elemento 3: 30
Elemento 4: 40
Elemento 5: 50
```

**Output**:
```
Suma total: 150
```

---

## Código Base

```c
#include <stdio.h>

int main(void) {
    int arr[100], n, suma = 0;

    printf("Cantidad: ");
    scanf("%d", &n);

    for (int i = 0; i < n; i++) {
        printf("Elemento %d: ", i+1);
        scanf("%d", &arr[i]);
    }

    // Tu código: sumar elementos

    printf("Suma total: %d\n", suma);
    return 0;
}
```

---

## Pista

```c
for (int i = 0; i < n; i++) {
    suma += arr[i];
}
```

---

## Desafíos

1. **Promedio**: Calcula también el promedio
2. **Función**: Crea función `int sumar(int arr[], int n)`
3. **Positivos**: Suma solo números positivos

---

#ejercicio #basico #arrays #suma
