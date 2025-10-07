# Ejercicio 01: Hello You

**Nivel**: Básico | **Tiempo**: 20 min | **Conceptos**: printf, scanf, strings

---

## Objetivo

Crear un programa que pida el nombre del usuario y lo salude.

---

## Especificaciones

**Input**:
```
¿Cómo te llamas? Juan
```

**Output**:
```
¡Hola, Juan! Bienvenido a C.
```

---

## Requisitos

- [ ] Pedir nombre al usuario
- [ ] Almacenar en variable tipo char array
- [ ] Mostrar saludo personalizado
- [ ] Formatear output correctamente

---

## Pistas

**Estructura**:
```c
#include <stdio.h>

int main(void) {
    char nombre[50];

    printf("¿Cómo te llamas? ");
    scanf("%s", nombre);

    printf("¡Hola, %s! Bienvenido a C.\n", nombre);

    return 0;
}
```

**Compilar y ejecutar**:
```bash
gcc ejercicio01.c -o ejercicio01
./ejercicio01
```

---

## Desafíos

1. **Nombre completo**: Usa `fgets` para leer nombres con espacios
2. **Edad también**: Pide nombre y edad, muestra ambos
3. **Mayúsculas**: Convierte primera letra a mayúscula

---

[[Ejercicio-02-Calculadora-Simple|Siguiente →]]

#ejercicio #basico #io #strings
