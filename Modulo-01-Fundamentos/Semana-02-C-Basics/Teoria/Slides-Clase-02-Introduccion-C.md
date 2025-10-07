---
theme: black
highlightTheme: monokai
transition: slide
---

# Semana 2: Introducción a C

**Módulo 1: Fundamentos**

De Scratch a C: Tu Primer Lenguaje Real

---

## Agenda

1. ¿Qué es C y por qué aprenderlo?
2. De Scratch a C
3. Tu primer programa: Hello World
4. Variables y tipos de datos
5. Entrada/Salida (printf/scanf)
6. Operadores
7. Condicionales
8. Ejercicios y proyecto

---

## Repaso Semana 1

**¿Qué aprendimos con Scratch?**

- Pensamiento computacional
- Variables
- Loops
- Condicionales
- Eventos

**Hoy**: Los mismos conceptos, nueva sintaxis

---

# Parte 1: ¿Qué es C?

---

## Historia de C

**1972** - Dennis Ritchie en Bell Labs

**Logros**:
- Creó UNIX (sistema operativo)
- Base de C++, Java, JavaScript, Python...
- Lenguaje de sistemas operativos
- Usado en hardware embebido

**Está en todas partes**: Routers, autos, aviones, satélites

---

## ¿Por Qué Aprender C?

**Pedagógicamente**:
- Entiendes cómo funciona la memoria
- Todo es explícito (sin "magia")
- Fundamentos sólidos para cualquier lenguaje

**Profesionalmente**:
- Extremadamente rápido
- Control total del sistema
- Desarrollo de sistemas operativos
- IoT y dispositivos embebidos

---

## C vs Otros Lenguajes

**Nivel de abstracción**:

```
Alto nivel (fácil)    Python, JavaScript
                      ↑
Medio                 Java, C#
                      ↑
Bajo nivel            C
                      ↑
Ensamblador (difícil) Assembly
```

**C = Balance perfecto entre control y usabilidad**

---

# Parte 2: De Scratch a C

---

## Comparación Directa

**Variable en Scratch**:
```
Crear variable "puntos"
Fijar puntos a 0
```

**Variable en C**:
```c
int puntos;
puntos = 0;
```

---

## Más Comparaciones

| Concepto | Scratch | C |
|----------|---------|---|
| Mostrar | Decir "Hola" | `printf("Hola\n");` |
| Pedir | Preguntar "¿Edad?" | `scanf("%d", &edad);` |
| If | Si <> entonces | `if (...) { }` |
| Loop | Repetir 10 | `for (i=0; i<10; i++)` |

**La lógica es idéntica**

---

# Parte 3: Hello World

---

## Tu Primer Programa en C

```c
#include <stdio.h>

int main(void) {
    printf("Hello, World!\n");
    return 0;
}
```

**¡Eso es todo!**

---

## Análisis Línea por Línea

```c
#include <stdio.h>
```
Incluye biblioteca estándar (Standard Input/Output)

```c
int main(void) {
```
Función principal (todo programa empieza aquí)

```c
    printf("Hello, World!\n");
```
Imprime en pantalla (`\n` = nueva línea)

```c
    return 0;
```
Retorna 0 = éxito

---

## Compilar y Ejecutar

**Escribir código**:
```c
// hello.c
#include <stdio.h>

int main(void) {
    printf("Hello, World!\n");
    return 0;
}
```

**Compilar**:
```bash
gcc hello.c -o hello
```

**Ejecutar**:
```bash
./hello
```

---

## Proceso de Compilación

```
Código fuente (.c)
       ↓
   Compilador (gcc)
       ↓
  Ejecutable (./a.out)
       ↓
   ¡Resultado!
```

**Diferencia clave con Scratch**: Necesitas compilar antes de ejecutar

---

# Parte 4: Variables y Tipos

---

## Declaración de Variables

**Sintaxis**:
```c
tipo nombre;
```

**Ejemplos**:
```c
int edad;           // Declarar
edad = 25;          // Asignar

int puntos = 0;     // Declarar + inicializar
```

**En C debes especificar el TIPO**

---

## Tipos de Datos Básicos

**Enteros**:
```c
int edad = 25;              // -2 mil millones a 2 mil millones
short pequeño = 100;        // Números pequeños
long grande = 1000000;      // Números grandes
```

**Decimales**:
```c
float precio = 19.99;       // 6-7 decimales
double pi = 3.14159265359;  // 15-16 decimales
```

**Caracteres**:
```c
char letra = 'A';           // Un solo carácter
char nombre[] = "Ana";      // String (texto)
```

---

## Tabla de Tipos

| Tipo | Tamaño | Uso |
|------|--------|-----|
| `char` | 1 byte | Caracteres |
| `int` | 4 bytes | Enteros estándar |
| `float` | 4 bytes | Decimales (evitar) |
| `double` | 8 bytes | Decimales (preferir) |
| `long` | 8 bytes | Enteros muy grandes |

---

## Reglas de Nombres

**Válido**:
```c
int edad;
int numero_estudiantes;
int contador1;
int _temporal;
```

**Inválido**:
```c
int 1contador;    // Empieza con número
int mi-edad;      // Usa guión
int int;          // Palabra reservada
```

**Convención**: `snake_case` o `camelCase`

---

# Parte 5: Entrada y Salida

---

## printf - Mostrar en Pantalla

**Sintaxis**:
```c
printf("formato", variables);
```

**Especificadores**:
```c
int edad = 25;
printf("Edad: %d\n", edad);           // %d = entero

float altura = 1.75;
printf("Altura: %.2f\n", altura);     // %f = decimal

char nombre[] = "Ana";
printf("Nombre: %s\n", nombre);       // %s = string
```

---

## Especificadores Comunes

| Tipo | Especificador | Ejemplo |
|------|---------------|---------|
| int | %d | `printf("%d", num)` |
| float/double | %f | `printf("%.2f", pi)` |
| char | %c | `printf("%c", letra)` |
| string | %s | `printf("%s", texto)` |

---

## Caracteres Especiales

```c
printf("Línea 1\n");       // \n = nueva línea
printf("Línea 2\n");

printf("Tab\taquí\n");     // \t = tabulación

printf("Dice \"Hola\"\n"); // \" = comilla literal
```

**Resultado**:
```
Línea 1
Línea 2
Tab    aquí
Dice "Hola"
```

---

## scanf - Leer Input

**Sintaxis**:
```c
scanf("formato", &variable);
```

**Nota importante**: `&` antes de la variable

**Ejemplos**:
```c
int edad;
printf("¿Tu edad? ");
scanf("%d", &edad);

float altura;
printf("¿Tu altura? ");
scanf("%f", &altura);
```

---

## ¿Por Qué el &?

**`&` = dirección de memoria**

```c
int edad;
scanf("%d", &edad);
```

**scanf necesita saber DÓNDE guardar el valor**

**Excepción - Strings**:
```c
char nombre[50];
scanf("%s", nombre);  // SIN &
```

---

## Ejemplo Completo

```c
#include <stdio.h>

int main(void) {
    char nombre[50];
    int edad;

    printf("¿Tu nombre? ");
    scanf("%s", nombre);

    printf("¿Tu edad? ");
    scanf("%d", &edad);

    printf("\nHola %s, tienes %d años\n", nombre, edad);

    return 0;
}
```

---

## DEMO en Vivo

Vamos a escribir, compilar y ejecutar este programa juntos

---

# Parte 6: Operadores

---

## Operadores Aritméticos

```c
int a = 10, b = 3;

a + b   // 13 - Suma
a - b   // 7  - Resta
a * b   // 30 - Multiplicación
a / b   // 3  - División
a % b   // 1  - Módulo (residuo)
```

**Cuidado**: `10 / 3 = 3` (división entera, no 3.33)

---

## División: Truco Importante

**División entera**:
```c
int resultado = 10 / 3;  // 3
```

**División decimal**:
```c
float resultado = 10.0 / 3.0;  // 3.333...
```

**O usar cast**:
```c
float resultado = (float)10 / 3;  // 3.333...
```

---

## Incremento y Decremento

```c
int contador = 5;

contador++;     // 6 (incrementa)
contador--;     // 5 (decrementa)

contador += 3;  // contador = contador + 3
contador -= 2;  // contador = contador - 2
contador *= 2;  // contador = contador * 2
contador /= 2;  // contador = contador / 2
```

---

## Operadores de Comparación

```c
int a = 10, b = 5;

a == b   // false (igual a)
a != b   // true  (diferente de)
a > b    // true  (mayor que)
a < b    // false (menor que)
a >= b   // true  (mayor o igual)
a <= b   // false (menor o igual)
```

**Nota**: `==` compara, `=` asigna

---

## Operadores Lógicos

```c
// AND - ambos verdaderos
if (edad >= 18 && tiene_licencia) {
    printf("Puede conducir\n");
}

// OR - al menos uno verdadero
if (es_fin_semana || es_feriado) {
    printf("No hay clases\n");
}

// NOT - invierte
if (!tiene_permiso) {
    printf("Acceso denegado\n");
}
```

---

# Parte 7: Condicionales

---

## if / else

**Sintaxis**:
```c
if (condición) {
    // código si verdadero
} else {
    // código si falso
}
```

**Ejemplo**:
```c
int edad = 20;

if (edad >= 18) {
    printf("Mayor de edad\n");
} else {
    printf("Menor de edad\n");
}
```

---

## else if - Múltiples Condiciones

```c
int nota = 85;

if (nota >= 90) {
    printf("A - Excelente\n");
} else if (nota >= 80) {
    printf("B - Muy bien\n");
} else if (nota >= 70) {
    printf("C - Bien\n");
} else if (nota >= 60) {
    printf("D - Suficiente\n");
} else {
    printf("F - Reprobado\n");
}
```

---

## switch - Múltiples Casos

**Sintaxis**:
```c
switch (variable) {
    case valor1:
        // código
        break;
    case valor2:
        // código
        break;
    default:
        // código por defecto
}
```

---

## Ejemplo switch

```c
char opcion;
printf("Elige (a/b/c): ");
scanf(" %c", &opcion);

switch (opcion) {
    case 'a':
        printf("Opción A\n");
        break;
    case 'b':
        printf("Opción B\n");
        break;
    case 'c':
        printf("Opción C\n");
        break;
    default:
        printf("Inválida\n");
}
```

---

## if vs switch

**Usa if cuando**:
- Condiciones complejas
- Rangos de valores
- Comparaciones múltiples

**Usa switch cuando**:
- Valores exactos (enteros o char)
- Múltiples casos simples
- Menús de opciones

---

# Ejercicio en Clase

---

## Ejercicio: Calculadora Simple

Crear programa que:
1. Pida dos números
2. Pida operación (+, -, *, /)
3. Muestre resultado

**10 minutos para intentarlo**

---

## Solución

```c
#include <stdio.h>

int main(void) {
    float a, b, resultado;
    char op;

    printf("Ingresa operación (ej: 5 + 3): ");
    scanf("%f %c %f", &a, &op, &b);

    switch (op) {
        case '+':
            resultado = a + b;
            break;
        case '-':
            resultado = a - b;
            break;
        case '*':
            resultado = a * b;
            break;
        case '/':
            if (b != 0) {
                resultado = a / b;
            } else {
                printf("Error: división por cero\n");
                return 1;
            }
            break;
        default:
            printf("Operador inválido\n");
            return 1;
    }

    printf("Resultado: %.2f\n", resultado);
    return 0;
}
```

---

# Errores Comunes

---

## Error 1: Olvidar ;

```c
// INCORRECTO
printf("Hola")
int x = 5

// CORRECTO
printf("Hola");
int x = 5;
```

**Toda instrucción termina con `;`**

---

## Error 2: scanf sin &

```c
// INCORRECTO
int edad;
scanf("%d", edad);

// CORRECTO
int edad;
scanf("%d", &edad);
```

**Excepción**: Strings no usan `&`

---

## Error 3: = vs ==

```c
// INCORRECTO (asigna, no compara)
if (x = 5) {
    // Siempre verdadero
}

// CORRECTO
if (x == 5) {
    // Compara
}
```

---

## Error 4: División Entera

```c
// INCORRECTO
int resultado = 5 / 2;  // 2, no 2.5

// CORRECTO
float resultado = 5.0 / 2.0;  // 2.5
```

---

## Error 5: Variable no Inicializada

```c
// INCORRECTO (valor basura)
int x;
printf("%d", x);  // ???

// CORRECTO
int x = 0;
printf("%d", x);  // 0
```

---

# Proyecto de la Semana

---

## Opciones de Proyecto

**Básico**:
- Calculadora completa
- Conversor de unidades
- Calculadora de IMC

**Intermedio**:
- Sistema de calificaciones
- Conversor de bases (decimal, binario, hex)
- Calculadora científica

**Avanzado**:
- Juego de adivinanza de números
- Sistema de login simple
- Cifrado César

---

## Requisitos Mínimos

Tu proyecto debe:
- [ ] Usar variables de al menos 2 tipos diferentes
- [ ] Pedir input al usuario (scanf)
- [ ] Mostrar output formateado (printf)
- [ ] Usar al menos un condicional (if o switch)
- [ ] Funcionar sin errores
- [ ] Tener código bien comentado

---

## Fechas Importantes

**Ejercicios**: Día 4
**Proyecto**: Día 7 (fin de semana)

**Entrega**: Código fuente (.c) + breve explicación

---

# Resumen

---

## Lo que Aprendimos

1. C: lenguaje histórico y fundamental
2. Estructura básica de un programa en C
3. Variables y tipos de datos
4. printf y scanf (I/O)
5. Operadores (aritméticos, comparación, lógicos)
6. Condicionales (if/else, switch)
7. Compilación con gcc

---

## Conceptos Clave

**Diferencia con Scratch**:
- Tipado explícito
- Compilación requerida
- Sintaxis estricta

**Similitud con Scratch**:
- Misma lógica
- Mismos conceptos fundamentales
- Pensamiento computacional idéntico

---

## Próximos Pasos

**Hoy/Esta semana**:
1. Practicar ejercicios básicos
2. Experimentar con printf/scanf
3. Escribir pequeños programas

**Próxima semana**:
- Loops (for, while)
- Arrays
- Funciones
- Algoritmos básicos

---

## Recursos

**Documentación**:
- [[01-Introduccion-C|Teoría completa]]
- [[02-Guia-Rapida-C|Guía rápida]]

**Online**:
- [Learn-C.org](https://www.learn-c.org/)
- [CS50 Manual](https://manual.cs50.io/)
- [replit.com](https://replit.com/) - IDE online

---

## Autoevaluación

**Pregúntate**:
- [ ] ¿Puedo escribir Hello World desde cero?
- [ ] ¿Entiendo la diferencia entre int y float?
- [ ] ¿Sé cuándo usar & en scanf?
- [ ] ¿Puedo crear un programa con if/else?
- [ ] ¿Entiendo qué hace el compilador?

---

# ¿Preguntas?

**Dudas sobre**:
- Sintaxis de C
- printf/scanf
- Condicionales
- El proyecto
- Compilación

---

# ¡A Programar!

**Recuerda**:
- Errores son normales
- Google es tu amigo
- Practica diariamente
- Pide ayuda cuando la necesites

**El camino de programador empieza con C**

---

## Próxima Clase

**Semana 3: Loops y Arrays**

- for, while, do-while
- Arrays (arreglos)
- Funciones básicas
- Algoritmos de búsqueda

**Nos vemos la próxima semana**

---

# ¡Gracias!

**Recursos**:
- Material del curso
- Ejercicios: [[../Ejercicios/README]]
- Proyectos: [[../Proyectos/README]]

**Happy coding!**
