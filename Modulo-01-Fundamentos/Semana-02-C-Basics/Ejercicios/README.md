# Ejercicios - Semana 02: C Basics

**Módulo 1: Fundamentos - Introducción a C**

---

## Objetivo

Practicar los fundamentos de C: variables, tipos de datos, entrada/salida y condicionales.

**Tiempo estimado**: 4-6 horas total
**Prerequisitos**: Teoría de la semana completada

---

## Lista de Ejercicios

### Nivel Básico (Esenciales)

| # | Ejercicio | Conceptos | Tiempo |
|---|-----------|-----------|--------|
| 01 | [[Ejercicio-01-Hello-You|Hello You]] | printf, scanf, strings | 20 min |
| 02 | [[Ejercicio-02-Calculadora-Simple|Calculadora Simple]] | Variables, operadores, I/O | 30 min |
| 03 | [[Ejercicio-03-Par-Impar|Par o Impar]] | Condicionales, módulo | 20 min |
| 04 | [[Ejercicio-04-Mayor-Tres|Mayor de Tres]] | if/else anidados | 30 min |

### Nivel Intermedio (Recomendados)

| # | Ejercicio | Conceptos | Tiempo |
|---|-----------|-----------|--------|
| 05 | [[Ejercicio-05-Conversor-Temperatura|Conversor Temperatura]] | Fórmulas, floats | 25 min |
| 06 | [[Ejercicio-06-Calificaciones|Sistema de Calificaciones]] | switch, rangos | 35 min |
| 07 | [[Ejercicio-07-Menu-Opciones|Menú de Opciones]] | switch, múltiples inputs | 40 min |

### Nivel Avanzado (Desafío)

| # | Ejercicio | Conceptos | Tiempo |
|---|-----------|-----------|--------|
| 08 | [[Ejercicio-08-Validador-Entrada|Validador de Entrada]] | Loops (preview), validación | 45 min |
| 09 | [[Ejercicio-09-Calculadora-Cientifica|Calculadora Científica]] | math.h, funciones complejas | 50 min |
| 10 | [[Ejercicio-10-Juego-Adivinanza|Juego Adivinanza]] | rand(), lógica de juego | 60 min |

---

## Compilación

Para todos los ejercicios, usa:

```bash
# Compilar
gcc ejercicio.c -o ejercicio -Wall

# Si usas math.h (ejercicios 9, 10)
gcc ejercicio.c -o ejercicio -Wall -lm

# Ejecutar
./ejercicio
```

---

## Criterios de Completación

- [ ] Compila sin errores ni warnings
- [ ] Funciona con diferentes inputs
- [ ] Código bien comentado
- [ ] Validación de entrada básica
- [ ] Output claro y formateado

---

## Plantilla Base

Todos tus ejercicios deberían seguir esta estructura:

```c
#include <stdio.h>

int main(void) {
    // Declarar variables

    // Pedir input

    // Procesar

    // Mostrar output

    return 0;
}
```

---

## Recursos

- [[../Teoria/01-Introduccion-C|Teoría: Introducción a C]]
- [[../Teoria/02-Guia-Rapida-C|Guía Rápida]]
- [Learn-C.org](https://www.learn-c.org/)

---

## Entrega

Formato de archivo: `ejercicio##.c`

Ejemplo:
```
ejercicio01.c
ejercicio02.c
...
```

Todos en una carpeta comprimida: `M01-S02-Ejercicios-[Nombre].zip`

---

#c #ejercicios #basicos #variables #condicionales
