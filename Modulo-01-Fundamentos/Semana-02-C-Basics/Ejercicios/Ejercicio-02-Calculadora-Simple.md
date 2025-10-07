# Ejercicio 02: Calculadora Simple

**Nivel**: Básico | **Tiempo**: 30 min | **Conceptos**: Variables, operadores, I/O

---

## Objetivo

Crear calculadora que realice operaciones básicas (+, -, *, /).

---

## Especificaciones

**Input**:
```
Ingresa operación (ej: 5 + 3): 10 * 2
```

**Output**:
```
Resultado: 20.00
```

---

## Requisitos

- [ ] Leer dos números y un operador
- [ ] Realizar la operación correspondiente
- [ ] Manejar división por cero
- [ ] Mostrar resultado con 2 decimales

---

## Código Base

```c
#include <stdio.h>

int main(void) {
    float num1, num2, resultado;
    char operador;

    printf("Ingresa operación (ej: 5 + 3): ");
    scanf("%f %c %f", &num1, &operador, &num2);

    // Tu código aquí: switch con cada operación

    printf("Resultado: %.2f\n", resultado);
    return 0;
}
```

---

## Pistas

**División por cero**:
```c
case '/':
    if (num2 != 0) {
        resultado = num1 / num2;
    } else {
        printf("Error: división por cero\n");
        return 1;
    }
    break;
```

---

## Desafíos

1. **Más operaciones**: Añade potencia (^) y módulo (%)
2. **Validación**: Rechaza operadores inválidos
3. **Múltiples cálculos**: Pregunta si quiere otra operación

---

[[Ejercicio-03-Par-Impar|Siguiente →]]

#ejercicio #basico #calculadora #switch
