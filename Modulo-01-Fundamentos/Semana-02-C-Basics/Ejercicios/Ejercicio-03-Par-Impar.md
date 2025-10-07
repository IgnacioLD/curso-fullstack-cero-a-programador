# Ejercicio 03: Par o Impar

**Nivel**: Básico | **Tiempo**: 20 min | **Conceptos**: Condicionales, módulo

---

## Objetivo

Determinar si un número es par o impar.

---

## Especificaciones

**Input**: `14`
**Output**: `14 es par`

**Input**: `7`
**Output**: `7 es impar`

---

## Requisitos

- [ ] Leer un número entero
- [ ] Determinar si es par o impar
- [ ] Mostrar resultado claro

---

## Conceptos Clave

**Operador módulo** (`%`):
```c
10 % 2 = 0  // Par
11 % 2 = 1  // Impar
```

**Un número es par si** `numero % 2 == 0`

---

## Solución

```c
#include <stdio.h>

int main(void) {
    int numero;

    printf("Ingresa un número: ");
    scanf("%d", &numero);

    if (numero % 2 == 0) {
        printf("%d es par\n", numero);
    } else {
        printf("%d es impar\n", numero);
    }

    return 0;
}
```

---

## Desafíos

1. **Múltiplo de 3**: Verifica si es múltiplo de 3
2. **Rango**: Pide 10 números y cuenta cuántos son pares
3. **Tabla**: Muestra tabla de pares del 1 al 20

---

#ejercicio #basico #condicionales #modulo
