# Introducción a C

> **Semana 2 - Módulo 1: Fundamentos**
> **Duración**: 6-8 horas de estudio
> **Prerequisitos**: Semana 1 - Scratch completada

---

## Índice

- [[#Objetivos de Aprendizaje]]
- [[#¿Qué es C y Por Qué Aprenderlo?]]
- [[#Tu Primer Programa en C]]
- [[#Variables y Tipos de Datos]]
- [[#Entrada y Salida]]
- [[#Operadores]]
- [[#Condicionales]]
- [[#Compilación y Ejecución]]
- [[#Recursos Adicionales]]
- [[#Autoevaluación]]

---

## Objetivos de Aprendizaje

Al finalizar esta semana, serás capaz de:

- Explicar qué es C y su importancia histórica
- Escribir, compilar y ejecutar programas básicos en C
- Declarar y usar variables de diferentes tipos
- Implementar entrada/salida con printf y scanf
- Usar operadores aritméticos, lógicos y de comparación
- Implementar estructuras condicionales (if, else, switch)

---

## ¿Qué es C y Por Qué Aprenderlo?

### Historia

**C** fue creado en 1972 por Dennis Ritchie en Bell Labs. Es uno de los lenguajes más influyentes en la historia de la computación.

**Datos importantes**:
- Usado para crear UNIX (sistema operativo)
- Base de C++, C#, Java, JavaScript, y muchos otros
- Lenguaje de sistemas operativos (Linux, Windows kernel)
- Usado en dispositivos embebidos y hardware

### ¿Por Qué Aprender C Primero?

**Ventajas pedagógicas**:
- **Control total**: Entiendes cómo funciona la memoria
- **Sin "magia"**: Todo es explícito, nada oculto
- **Fundamentos sólidos**: Si entiendes C, entenderás cualquier lenguaje
- **Rendimiento**: Extremadamente rápido
- **Ubicuidad**: Está en todas partes (routers, autos, aviones)

**Desventajas** (que aprenderás a manejar):
- Manejo manual de memoria
- Sintaxis estricta
- Menos abstracciones que lenguajes modernos

### De Scratch a C

| Concepto | Scratch | C |
|----------|---------|---|
| Variable | Crear variable "puntos" | `int puntos;` |
| Asignar | Fijar puntos a 0 | `puntos = 0;` |
| Mostrar | Decir puntos | `printf("%d", puntos);` |
| Condicional | Si... entonces | `if (...) { }` |
| Loop | Repetir 10 | `for (i=0; i<10; i++)` |

**La lógica es idéntica, solo cambia la sintaxis.**

---

## Tu Primer Programa en C

### Hello World

```c
#include <stdio.h>

int main(void) {
    printf("Hello, World!\n");
    return 0;
}
```

### Análisis Línea por Línea

**`#include <stdio.h>`**
- Incluye la biblioteca estándar de entrada/salida
- `stdio` = Standard Input/Output
- Necesario para usar `printf`

**`int main(void)`**
- Función principal (toda ejecución empieza aquí)
- `int` = retorna un entero
- `main` = nombre de la función
- `void` = no recibe parámetros

**`printf("Hello, World!\n");`**
- Función que imprime en pantalla
- `\n` = salto de línea (newline)
- `;` = termina cada instrucción

**`return 0;`**
- Retorna 0 al sistema operativo
- 0 = éxito, cualquier otro número = error

### Compilar y Ejecutar

**En terminal**:
```bash
# Compilar
gcc hello.c -o hello

# Ejecutar
./hello
```

**Desglose**:
- `gcc` = GNU C Compiler
- `hello.c` = archivo fuente
- `-o hello` = nombre del ejecutable
- `./hello` = ejecutar el programa

---

## Variables y Tipos de Datos

### Declaración de Variables

**Sintaxis**:
```c
tipo nombre;
```

**Ejemplos**:
```c
int edad;           // Declarar
edad = 25;          // Asignar

int puntos = 0;     // Declarar e inicializar
```

### Tipos de Datos Básicos

**Números enteros**:
```c
int edad = 25;              // Entero estándar (-2B a 2B)
short pequeño = 100;        // Entero corto
long grande = 1000000L;     // Entero largo
unsigned int positivo = 50; // Solo positivos
```

**Números decimales**:
```c
float precio = 19.99f;      // Precisión simple
double pi = 3.14159265359;  // Precisión doble (recomendado)
```

**Caracteres**:
```c
char letra = 'A';           // Un solo carácter
char grado = 'B';
```

**Cadenas de texto** (arrays de caracteres):
```c
char nombre[] = "Ana";      // String
char mensaje[] = "Hola mundo";
```

### Tabla de Tipos

| Tipo | Tamaño | Rango | Uso |
|------|--------|-------|-----|
| `char` | 1 byte | -128 a 127 | Caracteres |
| `int` | 4 bytes | -2B a 2B | Enteros estándar |
| `float` | 4 bytes | 6-7 decimales | Decimales (evitar) |
| `double` | 8 bytes | 15-16 decimales | Decimales (preferir) |
| `long` | 8 bytes | -9E18 a 9E18 | Enteros muy grandes |

### Reglas de Nombres

**Válido**:
- Letras, números, guión bajo
- Debe empezar con letra o `_`
- Case-sensitive (`edad` ≠ `Edad`)

**Ejemplos válidos**:
```c
int edad;
int numero_estudiantes;
int contador1;
int _temporal;
```

**Ejemplos inválidos**:
```c
int 1contador;    // Empieza con número
int mi-edad;      // Usa guión (no válido)
int int;          // Palabra reservada
```

**Convención** (buenas prácticas):
- Variables: `snake_case` o `camelCase`
- Constantes: `MAYUSCULAS`
- Descriptivos: `edad_usuario` (no `x`)

---

## Entrada y Salida

### printf (Salida)

**Sintaxis básica**:
```c
printf("formato", variables...);
```

**Especificadores de formato**:
```c
int edad = 25;
float altura = 1.75;
char inicial = 'A';
char nombre[] = "Ana";

printf("Edad: %d\n", edad);           // %d = entero
printf("Altura: %.2f\n", altura);     // %f = float/double
printf("Inicial: %c\n", inicial);     // %c = carácter
printf("Nombre: %s\n", nombre);       // %s = string
```

**Múltiples valores**:
```c
printf("Me llamo %s, tengo %d años\n", nombre, edad);
```

**Caracteres especiales**:
```c
printf("Línea 1\n");        // \n = nueva línea
printf("Tab\taquí\n");      // \t = tabulación
printf("Comilla: \"\n");    // \" = comilla literal
printf("Backslash: \\\n");  // \\ = backslash literal
```

### scanf (Entrada)

**Sintaxis**:
```c
scanf("formato", &variable);
```

**Nota importante**: Se usa `&` antes de la variable (dirección de memoria)

**Ejemplos**:
```c
int edad;
printf("¿Cuál es tu edad? ");
scanf("%d", &edad);

float altura;
printf("¿Cuál es tu altura? ");
scanf("%f", &altura);

char inicial;
printf("¿Tu inicial? ");
scanf(" %c", &inicial);  // Espacio antes de %c
```

**String (cuidado con espacios)**:
```c
char nombre[50];
printf("¿Tu nombre? ");
scanf("%s", nombre);  // NO usar & con strings
// Problema: solo lee hasta el primer espacio
```

**Leer línea completa con espacios**:
```c
char nombre_completo[100];
printf("Nombre completo: ");
fgets(nombre_completo, 100, stdin);
```

### Ejemplo Completo

```c
#include <stdio.h>

int main(void) {
    char nombre[50];
    int edad;
    float altura;

    // Entrada
    printf("¿Cómo te llamas? ");
    scanf("%s", nombre);

    printf("¿Cuántos años tienes? ");
    scanf("%d", &edad);

    printf("¿Cuál es tu altura (m)? ");
    scanf("%f", &altura);

    // Salida
    printf("\nResumen:\n");
    printf("Nombre: %s\n", nombre);
    printf("Edad: %d años\n", edad);
    printf("Altura: %.2f metros\n", altura);

    return 0;
}
```

---

## Operadores

### Aritméticos

```c
int a = 10, b = 3;

printf("%d\n", a + b);  // 13 - Suma
printf("%d\n", a - b);  // 7  - Resta
printf("%d\n", a * b);  // 30 - Multiplicación
printf("%d\n", a / b);  // 3  - División entera
printf("%d\n", a % b);  // 1  - Módulo (residuo)
```

**Cuidado con división**:
```c
int resultado = 10 / 3;        // 3 (división entera)
float resultado = 10.0 / 3.0;  // 3.333... (división real)
```

### Incremento y Decremento

```c
int contador = 5;

contador++;     // contador = contador + 1 (ahora 6)
contador--;     // contador = contador - 1 (ahora 5)

contador += 3;  // contador = contador + 3
contador -= 2;  // contador = contador - 2
contador *= 2;  // contador = contador * 2
contador /= 2;  // contador = contador / 2
```

### Comparación

```c
int a = 10, b = 5;

a == b   // false (igual a)
a != b   // true  (diferente de)
a > b    // true  (mayor que)
a < b    // false (menor que)
a >= b   // true  (mayor o igual)
a <= b   // false (menor o igual)
```

### Lógicos

```c
int edad = 20;
int tiene_permiso = 1;  // 1 = true, 0 = false

// AND (ambos deben ser verdaderos)
if (edad >= 18 && tiene_permiso) {
    printf("Puede conducir\n");
}

// OR (al menos uno verdadero)
if (edad < 18 || !tiene_permiso) {
    printf("No puede conducir\n");
}

// NOT (invierte el valor)
if (!tiene_permiso) {
    printf("Sin permiso\n");
}
```

---

## Condicionales

### if / else

**Sintaxis básica**:
```c
if (condición) {
    // código si es verdadero
}
```

**Con else**:
```c
if (condición) {
    // si es verdadero
} else {
    // si es falso
}
```

**Ejemplos**:
```c
int edad = 20;

if (edad >= 18) {
    printf("Eres mayor de edad\n");
} else {
    printf("Eres menor de edad\n");
}
```

### else if (múltiples condiciones)

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

### switch (múltiples casos)

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
        // código si ningún caso coincide
}
```

**Ejemplo**:
```c
char opcion;
printf("Elige (a/b/c): ");
scanf(" %c", &opcion);

switch (opcion) {
    case 'a':
        printf("Opción A seleccionada\n");
        break;
    case 'b':
        printf("Opción B seleccionada\n");
        break;
    case 'c':
        printf("Opción C seleccionada\n");
        break;
    default:
        printf("Opción inválida\n");
}
```

**Importante**: Sin `break`, continúa al siguiente caso (fall-through)

### Operador Ternario

**Sintaxis**:
```c
variable = (condición) ? valor_si_true : valor_si_false;
```

**Ejemplo**:
```c
int edad = 20;
char *categoria = (edad >= 18) ? "Adulto" : "Menor";
printf("%s\n", categoria);
```

---

## Compilación y Ejecución

### Proceso de Compilación

1. **Código fuente** (`programa.c`)
2. **Preprocesador** (expande `#include`, macros)
3. **Compilador** (genera código objeto `.o`)
4. **Linker** (une con bibliotecas, genera ejecutable)
5. **Ejecutable** (`programa` o `programa.exe`)

### gcc - GNU C Compiler

**Comandos básicos**:
```bash
# Compilar simple
gcc programa.c

# Ejecutar (Linux/Mac)
./a.out

# Especificar nombre
gcc programa.c -o mi_programa
./mi_programa

# Con warnings (recomendado)
gcc -Wall programa.c -o programa

# Modo debug
gcc -g programa.c -o programa
```

**Flags importantes**:
- `-o nombre`: Nombre del ejecutable
- `-Wall`: Muestra todos los warnings
- `-g`: Incluye información de debug
- `-std=c99`: Usa estándar C99

### Errores Comunes

**Error de compilación**:
```c
// Olvidar punto y coma
printf("Hola")  // ERROR
printf("Hola"); // CORRECTO
```

**Error de ejecución**:
```c
int x;
printf("%d", x);  // Variable no inicializada (basura)
```

**Error lógico**:
```c
int resultado = 10 / 3;  // 3, no 3.33 (división entera)
```

---

## Recursos Adicionales

### Documentación
- [Learn C](https://www.learn-c.org/) - Tutorial interactivo
- [CS50 Manual Pages](https://manual.cs50.io/) - Referencia de funciones
- [C Reference](https://en.cppreference.com/w/c) - Documentación completa

### Video Tutoriales
- [CS50 - C Week 1](https://cs50.harvard.edu/x/2024/weeks/1/) - Harvard
- [C Programming Tutorial](https://www.youtube.com/watch?v=KJgsSFOSQv0) - freeCodeCamp

### Herramientas Online
- [replit.com](https://replit.com/) - IDE online para C
- [OnlineGDB](https://www.onlinegdb.com/online_c_compiler) - Compilador online
- [C Tutor](http://www.pythontutor.com/c.html) - Visualizar ejecución

### Enlaces Internos
- [[../Semana-01-Scratch/Teoria/01-Introduccion-Pensamiento-Computacional|Semana 1: Pensamiento Computacional]]
- [[02-Guia-Rapida-C|Guía Rápida de C]]
- [[../Ejercicios/README|Ejercicios de la Semana]]
- [[../Proyectos/README|Proyectos de la Semana]]

---

## Autoevaluación

### Conceptos Teóricos
- [ ] ¿Qué es C y por qué es importante?
- [ ] ¿Cuál es la diferencia entre `int` y `float`?
- [ ] ¿Para qué sirve `#include <stdio.h>`?
- [ ] ¿Cuál es la diferencia entre `=` y `==`?

### Práctica
- [ ] ¿Puedes escribir un "Hello World" desde cero?
- [ ] ¿Sabes declarar e inicializar variables?
- [ ] ¿Puedes pedir input al usuario con `scanf`?
- [ ] ¿Entiendes la diferencia entre `if` y `switch`?

### Debugging
- [ ] ¿Qué pasa si olvidas el `;`?
- [ ] ¿Por qué `scanf` usa `&` pero `printf` no?
- [ ] ¿Qué hace `return 0` en `main`?

---

## Próximos Pasos

1. **Práctica**: [[../Ejercicios/README|Ejercicios de la Semana]]
2. **Proyecto**: [[../Proyectos/README|Calculadora o Conversor]]
3. **Profundizar**: [[02-Guia-Rapida-C|Guía Rápida de C]]

---

**Última actualización**: 2025-10-02
**Siguiente**: [[02-Guia-Rapida-C|Guía Rápida de C]] →

---

#c #programacion #fundamentos #semana2 #variables #tipos-datos
