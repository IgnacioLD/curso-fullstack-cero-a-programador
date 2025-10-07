# Loops, Arrays y Funciones en C

> **Semana 3 - Módulo 1: Fundamentos**
> **Duración**: 8-10 horas de estudio
> **Prerequisitos**: Semana 2 completada

---

## Índice

- [[#Objetivos de Aprendizaje]]
- [[#Loops (Bucles)]]
- [[#Arrays (Arreglos)]]
- [[#Funciones]]
- [[#Combinando Conceptos]]
- [[#Recursos Adicionales]]

---

## Objetivos de Aprendizaje

Al finalizar:

- Implementar loops (for, while, do-while)
- Crear y manipular arrays
- Definir y usar funciones
- Pasar parámetros por valor
- Entender scope de variables
- Combinar loops, arrays y funciones

---

## Loops (Bucles)

### for Loop

**Sintaxis**:
```c
for (inicialización; condición; incremento) {
    // código a repetir
}
```

**Ejemplo**:
```c
for (int i = 0; i < 5; i++) {
    printf("%d\n", i);
}
// Output: 0 1 2 3 4
```

**Desglose**:
- `int i = 0`: Inicializa contador
- `i < 5`: Condición (mientras sea verdad, continúa)
- `i++`: Incremento (después de cada iteración)

### while Loop

**Sintaxis**:
```c
while (condición) {
    // código
}
```

**Ejemplo**:
```c
int i = 0;
while (i < 5) {
    printf("%d\n", i);
    i++;
}
```

**Uso**: Cuando no sabes cuántas iteraciones necesitas

### do-while Loop

**Sintaxis**:
```c
do {
    // código
} while (condición);
```

**Ejemplo**:
```c
int numero;
do {
    printf("Ingresa positivo: ");
    scanf("%d", &numero);
} while (numero <= 0);
```

**Diferencia**: Ejecuta AL MENOS UNA VEZ (verifica condición al final)

### Comparación

| Loop | Uso | Cuándo usarlo |
|------|-----|---------------|
| for | Iteraciones conocidas | "Hacer 10 veces" |
| while | Condición al inicio | "Mientras sea verdad" |
| do-while | Condición al final | "Al menos una vez" |

### break y continue

**break** - Sale del loop:
```c
for (int i = 0; i < 10; i++) {
    if (i == 5) break;
    printf("%d ", i);
}
// Output: 0 1 2 3 4
```

**continue** - Salta a siguiente iteración:
```c
for (int i = 0; i < 5; i++) {
    if (i == 2) continue;
    printf("%d ", i);
}
// Output: 0 1 3 4
```

### Loops Anidados

```c
for (int i = 1; i <= 3; i++) {
    for (int j = 1; j <= 3; j++) {
        printf("i=%d, j=%d\n", i, j);
    }
}
```

**Output**:
```
i=1, j=1
i=1, j=2
i=1, j=3
i=2, j=1
...
```

---

## Arrays (Arreglos)

### Declaración e Inicialización

**Sintaxis**:
```c
tipo nombre[tamaño];
```

**Ejemplos**:
```c
int numeros[5];                    // Declarar
int edades[3] = {18, 25, 30};     // Inicializar
float precios[] = {9.99, 14.50};  // Tamaño automático
char vocales[] = {'a', 'e', 'i', 'o', 'u'};
```

### Acceso a Elementos

**Índices empiezan en 0**:
```c
int arr[5] = {10, 20, 30, 40, 50};

printf("%d\n", arr[0]);  // 10 (primer elemento)
printf("%d\n", arr[4]);  // 50 (último elemento)

arr[2] = 100;  // Modificar tercer elemento
printf("%d\n", arr[2]);  // 100
```

### Recorrer Arrays

**Con for**:
```c
int numeros[] = {1, 2, 3, 4, 5};
int tamaño = 5;

for (int i = 0; i < tamaño; i++) {
    printf("%d ", numeros[i]);
}
```

**Calcular tamaño**:
```c
int arr[] = {10, 20, 30};
int tamaño = sizeof(arr) / sizeof(arr[0]);
// tamaño = 12 bytes / 4 bytes = 3 elementos
```

### Arrays Multidimensionales

**2D (Matrices)**:
```c
int matriz[3][3] = {
    {1, 2, 3},
    {4, 5, 6},
    {7, 8, 9}
};

printf("%d\n", matriz[1][2]);  // 6
```

**Recorrer matriz**:
```c
for (int i = 0; i < 3; i++) {
    for (int j = 0; j < 3; j++) {
        printf("%d ", matriz[i][j]);
    }
    printf("\n");
}
```

### Strings como Arrays

```c
char nombre[] = "Ana";
// Equivalente a: {'A', 'n', 'a', '\0'}

printf("%s\n", nombre);  // Ana
printf("%c\n", nombre[0]);  // A

// Modificar
nombre[0] = 'J';
printf("%s\n", nombre);  // Jna
```

**Importante**: Strings terminan con `\0` (null terminator)

---

## Funciones

### Definición Básica

**Sintaxis**:
```c
tipo_retorno nombre(parámetros) {
    // código
    return valor;
}
```

**Ejemplo**:
```c
int sumar(int a, int b) {
    return a + b;
}

int main(void) {
    int resultado = sumar(5, 3);
    printf("%d\n", resultado);  // 8
    return 0;
}
```

### Funciones void (sin retorno)

```c
void saludar(char nombre[]) {
    printf("Hola, %s!\n", nombre);
}

int main(void) {
    saludar("Ana");  // Hola, Ana!
    return 0;
}
```

### Prototipos de Funciones

**Declaración antes de main**:
```c
#include <stdio.h>

// Prototipo
int sumar(int a, int b);

int main(void) {
    printf("%d\n", sumar(5, 3));
    return 0;
}

// Definición
int sumar(int a, int b) {
    return a + b;
}
```

### Paso por Valor

**C pasa copias de variables**:
```c
void modificar(int x) {
    x = 100;
}

int main(void) {
    int num = 5;
    modificar(num);
    printf("%d\n", num);  // 5 (no cambió)
    return 0;
}
```

**Para modificar, usa punteros** (próxima semana)

### Funciones con Arrays

```c
float promedio(int arr[], int tamaño) {
    int suma = 0;
    for (int i = 0; i < tamaño; i++) {
        suma += arr[i];
    }
    return (float)suma / tamaño;
}

int main(void) {
    int notas[] = {85, 90, 78, 92};
    float prom = promedio(notas, 4);
    printf("Promedio: %.2f\n", prom);
    return 0;
}
```

### Recursión

**Función que se llama a sí misma**:
```c
int factorial(int n) {
    if (n <= 1) return 1;
    return n * factorial(n - 1);
}

int main(void) {
    printf("%d\n", factorial(5));  // 120
    return 0;
}
```

---

## Combinando Conceptos

### Ejemplo: Buscar en Array

```c
int buscar(int arr[], int tamaño, int valor) {
    for (int i = 0; i < tamaño; i++) {
        if (arr[i] == valor) {
            return i;  // Retorna índice
        }
    }
    return -1;  // No encontrado
}

int main(void) {
    int numeros[] = {10, 20, 30, 40, 50};
    int pos = buscar(numeros, 5, 30);

    if (pos != -1) {
        printf("Encontrado en posición %d\n", pos);
    } else {
        printf("No encontrado\n");
    }

    return 0;
}
```

### Ejemplo: Mayor Elemento

```c
int maximo(int arr[], int tamaño) {
    int max = arr[0];
    for (int i = 1; i < tamaño; i++) {
        if (arr[i] > max) {
            max = arr[i];
        }
    }
    return max;
}
```

### Ejemplo: Invertir Array

```c
void invertir(int arr[], int tamaño) {
    for (int i = 0; i < tamaño / 2; i++) {
        int temp = arr[i];
        arr[i] = arr[tamaño - 1 - i];
        arr[tamaño - 1 - i] = temp;
    }
}

int main(void) {
    int nums[] = {1, 2, 3, 4, 5};
    invertir(nums, 5);

    for (int i = 0; i < 5; i++) {
        printf("%d ", nums[i]);
    }
    // Output: 5 4 3 2 1

    return 0;
}
```

---

## Patrones Comunes

### 1. Sumar Elementos

```c
int suma = 0;
for (int i = 0; i < tamaño; i++) {
    suma += arr[i];
}
```

### 2. Contar Elementos que Cumplen Condición

```c
int contar_pares(int arr[], int tamaño) {
    int contador = 0;
    for (int i = 0; i < tamaño; i++) {
        if (arr[i] % 2 == 0) {
            contador++;
        }
    }
    return contador;
}
```

### 3. Copiar Array

```c
void copiar(int origen[], int destino[], int tamaño) {
    for (int i = 0; i < tamaño; i++) {
        destino[i] = origen[i];
    }
}
```

### 4. Llenar Array con Input

```c
void llenar_array(int arr[], int tamaño) {
    for (int i = 0; i < tamaño; i++) {
        printf("Elemento %d: ", i + 1);
        scanf("%d", &arr[i]);
    }
}
```

---

## Scope de Variables

### Local

```c
void funcion() {
    int x = 5;  // Local a funcion
    printf("%d\n", x);
}

int main(void) {
    printf("%d\n", x);  // ERROR: x no existe aquí
    return 0;
}
```

### Global

```c
int contador = 0;  // Global

void incrementar() {
    contador++;
}

int main(void) {
    incrementar();
    printf("%d\n", contador);  // 1
    return 0;
}
```

**Evita variables globales cuando sea posible**

---

## Errores Comunes

### 1. Índice Fuera de Rango

```c
int arr[5] = {1, 2, 3, 4, 5};
printf("%d\n", arr[5]);  // ERROR: índice 5 no existe
```

### 2. No Inicializar Array

```c
int arr[5];
printf("%d\n", arr[0]);  // Valor basura
```

### 3. Loop Infinito

```c
for (int i = 0; i < 10; i--) {  // i-- en vez de i++
    // Infinito!
}
```

### 4. Comparar Strings con ==

```c
char str1[] = "hola";
char str2[] = "hola";
if (str1 == str2)  // INCORRECTO
    printf("Iguales\n");

// CORRECTO: usar strcmp
if (strcmp(str1, str2) == 0)
    printf("Iguales\n");
```

---

## Recursos Adicionales

### Documentación
- [C Arrays - Learn-C](https://www.learn-c.org/en/Arrays)
- [C Loops - Programiz](https://www.programiz.com/c-programming/c-for-loop)
- [C Functions - GeeksforGeeks](https://www.geeksforgeeks.org/functions-in-c/)

### Visualizadores
- [Python Tutor - C](http://pythontutor.com/c.html)
- [VisuAlgo](https://visualgo.net/) - Visualizar algoritmos

### Enlaces Internos
- [[02-Algoritmos-Basicos|Algoritmos Básicos]]
- [[../Ejercicios/README|Ejercicios]]
- [[../Proyectos/README|Proyectos]]

---

## Autoevaluación

- [ ] ¿Entiendes cuándo usar for vs while?
- [ ] ¿Puedes crear y recorrer un array?
- [ ] ¿Sabes definir y llamar funciones?
- [ ] ¿Entiendes el concepto de scope?
- [ ] ¿Puedes pasar arrays a funciones?

---

#c #loops #arrays #funciones #semana3
