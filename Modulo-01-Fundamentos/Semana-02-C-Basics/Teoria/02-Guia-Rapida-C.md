# Guía Rápida de C

> **Referencia rápida de sintaxis y patrones comunes**

---

## Tabla de Especificadores printf/scanf

| Tipo | Especificador | Ejemplo printf | Ejemplo scanf |
|------|---------------|----------------|---------------|
| int | %d | `printf("%d", num)` | `scanf("%d", &num)` |
| float/double | %f | `printf("%.2f", pi)` | `scanf("%f", &pi)` |
| char | %c | `printf("%c", letra)` | `scanf(" %c", &letra)` |
| string | %s | `printf("%s", texto)` | `scanf("%s", texto)` |
| long | %ld | `printf("%ld", grande)` | `scanf("%ld", &grande)` |
| unsigned | %u | `printf("%u", positivo)` | `scanf("%u", &positivo)` |
| hex | %x | `printf("%x", num)` | `scanf("%x", &num)` |

---

## Plantillas de Código

### Programa Básico
```c
#include <stdio.h>

int main(void) {
    // Tu código aquí

    return 0;
}
```

### Input/Output Simple
```c
#include <stdio.h>

int main(void) {
    int numero;

    printf("Ingresa un número: ");
    scanf("%d", &numero);

    printf("Ingresaste: %d\n", numero);

    return 0;
}
```

### Condicional if/else
```c
if (condicion) {
    // código
} else if (otra_condicion) {
    // código
} else {
    // código
}
```

### Switch Statement
```c
switch (variable) {
    case 1:
        // código
        break;
    case 2:
        // código
        break;
    default:
        // código
}
```

---

## Operadores Esenciales

### Aritméticos
```c
+ suma
- resta
* multiplicación
/ división
% módulo (residuo)

++ incremento
-- decremento

+= suma y asigna
-= resta y asigna
*= multiplica y asigna
/= divide y asigna
```

### Comparación
```c
== igual a
!= diferente de
> mayor que
< menor que
>= mayor o igual
<= menor o igual
```

### Lógicos
```c
&& AND (y)
|| OR (o)
! NOT (no)
```

---

## Patrones Comunes

### Validar Entrada
```c
int numero;
printf("Ingresa un número positivo: ");
scanf("%d", &numero);

if (numero <= 0) {
    printf("Error: debe ser positivo\n");
    return 1;
}
```

### Menú de Opciones
```c
char opcion;
printf("Menú:\n");
printf("a) Opción A\n");
printf("b) Opción B\n");
printf("c) Salir\n");
printf("Elige: ");
scanf(" %c", &opcion);

switch (opcion) {
    case 'a':
        printf("Ejecutando A\n");
        break;
    case 'b':
        printf("Ejecutando B\n");
        break;
    case 'c':
        printf("Saliendo...\n");
        break;
    default:
        printf("Opción inválida\n");
}
```

### Calculadora Básica
```c
float a, b, resultado;
char operador;

printf("Ingresa operación (ej: 5 + 3): ");
scanf("%f %c %f", &a, &operador, &b);

switch (operador) {
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
```

### Conversión de Temperatura
```c
float celsius, fahrenheit;

printf("Temperatura en Celsius: ");
scanf("%f", &celsius);

fahrenheit = (celsius * 9.0 / 5.0) + 32;

printf("%.2f°C = %.2f°F\n", celsius, fahrenheit);
```

### Par o Impar
```c
int numero;
printf("Ingresa un número: ");
scanf("%d", &numero);

if (numero % 2 == 0) {
    printf("%d es par\n", numero);
} else {
    printf("%d es impar\n", numero);
}
```

---

## Errores Comunes y Soluciones

### Error: Olvidar ;
```c
// INCORRECTO
printf("Hola")
int x = 5

// CORRECTO
printf("Hola");
int x = 5;
```

### Error: scanf sin &
```c
// INCORRECTO
int num;
scanf("%d", num);

// CORRECTO
int num;
scanf("%d", &num);

// EXCEPCIÓN: strings no usan &
char texto[50];
scanf("%s", texto);  // Sin &
```

### Error: División Entera
```c
// INCORRECTO (resultado = 0)
int resultado = 5 / 2;  // 2, no 2.5

// CORRECTO
float resultado = 5.0 / 2.0;  // 2.5
// O
float resultado = (float)5 / 2;  // Cast
```

### Error: Comparación con =
```c
// INCORRECTO (asignación, siempre verdadero)
if (x = 5) {
    // ...
}

// CORRECTO (comparación)
if (x == 5) {
    // ...
}
```

### Error: Variable no Inicializada
```c
// INCORRECTO (valor basura)
int x;
printf("%d", x);

// CORRECTO
int x = 0;
printf("%d", x);
```

### Error: scanf con char sin espacio
```c
// INCORRECTO (puede leer enter previo)
char letra;
scanf("%c", &letra);

// CORRECTO (espacio antes de %c)
char letra;
scanf(" %c", &letra);
```

---

## Convenciones de Estilo

### Nombres de Variables
```c
// snake_case (recomendado en C)
int edad_usuario;
float precio_total;

// camelCase (alternativa)
int edadUsuario;
float precioTotal;

// CONSTANTES (mayúsculas)
#define PI 3.14159
#define MAX_USUARIOS 100
```

### Indentación
```c
// Consistente (4 espacios o 1 tab)
if (condicion) {
    printf("Verdadero\n");
    if (otra) {
        printf("Anidado\n");
    }
}
```

### Comentarios
```c
// Comentario de una línea

/*
 * Comentario de
 * múltiples líneas
 */

int edad = 25;  // Comentario inline
```

---

## Compilación Rápida

### Comandos gcc
```bash
# Básico
gcc programa.c
./a.out

# Con nombre
gcc programa.c -o programa
./programa

# Con warnings
gcc -Wall programa.c -o programa

# Debug mode
gcc -g -Wall programa.c -o programa

# Múltiples archivos
gcc main.c funciones.c -o programa
```

### Debugging con gdb
```bash
# Compilar con -g
gcc -g programa.c -o programa

# Ejecutar con gdb
gdb programa

# Comandos básicos gdb
(gdb) run              # Ejecutar
(gdb) break main       # Breakpoint en main
(gdb) next             # Siguiente línea
(gdb) print variable   # Ver valor
(gdb) quit             # Salir
```

---

## Formato printf Avanzado

### Controlar Decimales
```c
float pi = 3.14159;

printf("%.2f\n", pi);   // 3.14 (2 decimales)
printf("%.4f\n", pi);   // 3.1416 (4 decimales)
printf("%f\n", pi);     // 3.141590 (6 default)
```

### Ancho de Campo
```c
int num = 42;

printf("%5d\n", num);   //    42 (5 caracteres)
printf("%-5d\n", num);  // 42    (alineado izq)
printf("%05d\n", num);  // 00042 (padding ceros)
```

### Combinaciones
```c
float precio = 19.99;

printf("$%8.2f\n", precio);   // $   19.99
printf("$%-8.2f\n", precio);  // $19.99
printf("$%08.2f\n", precio);  // $0019.99
```

---

## Caracteres Especiales

```c
\n   // Nueva línea
\t   // Tabulación
\"   // Comillas dobles
\'   // Comilla simple
\\   // Backslash
\0   // Null (fin de string)
%%   // % literal en printf
```

---

## Macros Comunes

```c
#define PI 3.14159
#define MAX 100
#define MIN(a,b) ((a) < (b) ? (a) : (b))
#define MAX(a,b) ((a) > (b) ? (a) : (b))
#define SQUARE(x) ((x) * (x))
```

---

## Trucos y Tips

### Swap sin Variable Temporal
```c
// Con temporal (claro)
int temp = a;
a = b;
b = temp;

// Sin temporal (tricky)
a = a + b;
b = a - b;
a = a - b;
```

### Valor Absoluto
```c
int abs_valor = (num < 0) ? -num : num;
```

### Máximo de Dos Números
```c
int max = (a > b) ? a : b;
```

### Limitar Valor en Rango
```c
if (valor < 0) valor = 0;
if (valor > 100) valor = 100;
```

---

## Checklist de Debugging

Cuando tu programa no funciona:

- [ ] ¿Compiló sin errores?
- [ ] ¿Compiló sin warnings? (`-Wall`)
- [ ] ¿Todas las variables están inicializadas?
- [ ] ¿Los `scanf` tienen `&`?
- [ ] ¿Usas `==` para comparar (no `=`)?
- [ ] ¿Hay un `break` en cada caso del `switch`?
- [ ] ¿Las divisiones usan `float`/`double`?
- [ ] ¿Los `printf` tienen `\n` donde corresponde?

---

## Recursos Relacionados

- [[01-Introduccion-C|Introducción a C]]
- [[../Ejercicios/README|Ejercicios Prácticos]]
- [[../Proyectos/README|Proyectos]]

**Documentación Externa**:
- [C Reference](https://en.cppreference.com/w/c)
- [CS50 Manual](https://manual.cs50.io/)
- [Learn-C.org](https://www.learn-c.org/)

---

#c #referencia #guia-rapida #sintaxis
