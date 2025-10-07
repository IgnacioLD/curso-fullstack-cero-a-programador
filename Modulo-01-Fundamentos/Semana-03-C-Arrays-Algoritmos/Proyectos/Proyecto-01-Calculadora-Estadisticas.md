# Proyecto 01: Calculadora de Estadísticas

**Nivel**: Básico | **Tiempo**: 3 horas

---

## Descripción

Programa que calcula estadísticas descriptivas de un conjunto de números.

---

## Funcionalidades

1. Pedir N números
2. Calcular media
3. Calcular mediana
4. Calcular moda
5. Encontrar mínimo y máximo
6. Mostrar datos ordenados

---

## Especificaciones

**Input**:
```
Cantidad de números: 5
Número 1: 10
Número 2: 20
Número 3: 10
Número 4: 30
Número 5: 20
```

**Output**:
```
Datos: 10 20 10 30 20
Ordenados: 10 10 20 20 30

Media: 18.00
Mediana: 20
Moda: 10 y 20
Mínimo: 10
Máximo: 30
```

---

## Funciones Requeridas

```c
float calcular_media(int arr[], int n);
int calcular_mediana(int arr[], int n);  // Requiere ordenar
void encontrar_moda(int arr[], int n);
int encontrar_minimo(int arr[], int n);
int encontrar_maximo(int arr[], int n);
void ordenar(int arr[], int n);
```

---

## Estructura

```c
#include <stdio.h>

// Prototipos
float calcular_media(int arr[], int n);
// ... otros

int main(void) {
    int datos[100], n;

    printf("Cantidad: ");
    scanf("%d", &n);

    for (int i = 0; i < n; i++) {
        printf("Número %d: ", i+1);
        scanf("%d", &datos[i]);
    }

    // Calcular y mostrar estadísticas

    return 0;
}

// Implementaciones
float calcular_media(int arr[], int n) {
    int suma = 0;
    for (int i = 0; i < n; i++)
        suma += arr[i];
    return (float)suma / n;
}

// ... otras funciones
```

---

## Desafíos

1. **Rango**: Calcular rango (max - min)
2. **Varianza**: Implementar varianza y desviación estándar
3. **Percentiles**: Calcular percentil 25, 50, 75
4. **Gráfico**: Mostrar histograma ASCII

---

#proyecto #basico #estadisticas #arrays
