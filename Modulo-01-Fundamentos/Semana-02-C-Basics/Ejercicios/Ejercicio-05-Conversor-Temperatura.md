# Ejercicio 05: Conversor de Temperatura

**Nivel**: Intermedio | **Tiempo**: 25 min | **Conceptos**: Fórmulas, floats, menú

---

## Objetivo

Convertir entre Celsius, Fahrenheit y Kelvin.

---

## Fórmulas

**Celsius a Fahrenheit**: `F = C * 9/5 + 32`
**Celsius a Kelvin**: `K = C + 273.15`
**Fahrenheit a Celsius**: `C = (F - 32) * 5/9`
**Fahrenheit a Kelvin**: `K = (F - 32) * 5/9 + 273.15`
**Kelvin a Celsius**: `C = K - 273.15`
**Kelvin a Fahrenheit**: `F = (K - 273.15) * 9/5 + 32`

---

## Especificaciones

**Menú**:
```
1. Celsius a Fahrenheit
2. Fahrenheit a Celsius
3. Celsius a Kelvin
Elige opción: 1
Temperatura: 25
Resultado: 77.00°F
```

---

## Estructura

```c
#include <stdio.h>

int main(void) {
    int opcion;
    float temp, resultado;

    // Mostrar menú
    printf("1. Celsius a Fahrenheit\n");
    printf("2. Fahrenheit a Celsius\n");
    printf("3. Celsius a Kelvin\n");
    printf("Elige: ");
    scanf("%d", &opcion);

    printf("Temperatura: ");
    scanf("%f", &temp);

    switch (opcion) {
        case 1:
            resultado = temp * 9.0 / 5.0 + 32;
            printf("%.2f°C = %.2f°F\n", temp, resultado);
            break;
        // Otros casos...
    }

    return 0;
}
```

---

## Desafíos

1. **Todas las conversiones**: Implementa las 6 fórmulas
2. **Validación**: Rechaza Kelvin negativos (imposible)
3. **Tabla**: Muestra tabla de conversión (0-100°C)

---

#ejercicio #intermedio #formulas #conversiones
