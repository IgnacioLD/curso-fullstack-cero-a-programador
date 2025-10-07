# Semana 03: Arrays y Algoritmos

**Módulo 1: Fundamentos Sólidos**

---

## Bienvenida

Esta semana aprendes las estructuras de datos fundamentales (arrays) y algoritmos clásicos (búsqueda y ordenamiento).

**Duración**: 5-7 días
**Horas totales**: 10-14 horas

---

## Contenido

### Teoría

1. [[Teoria/01-Loops-Arrays-Funciones|Loops, Arrays y Funciones]]
2. [[Teoria/02-Algoritmos-Basicos|Algoritmos Básicos]]
3. [[Teoria/Slides-Clase-03-Loops-Arrays|Slides de Clase]]

### Ejercicios

**Índice**: [[Ejercicios/README|Guía de Ejercicios]]

**Básicos** (todos):
1. [[Ejercicios/Ejercicio-01-Suma-Array|Suma de Array]]
2. Máximo y Mínimo
3. Invertir Array
4. Contar Pares

**Intermedios** (mín 2):
5. Búsqueda Lineal
6. [[Ejercicios/Ejercicio-06-Bubble-Sort|Bubble Sort]]
7. Funciones con Arrays

**Avanzados** (opcional):
8. Búsqueda Binaria
9. Estadísticas
10. Selection Sort

### Proyectos

**Índice**: [[Proyectos/README|Guía de Proyectos]]

Opciones:
- [[Proyectos/Proyecto-01-Calculadora-Estadisticas|Calculadora Estadísticas]] (básico)
- Lista de Tareas (básico)
- Agenda Contactos (intermedio)
- Comparador Algoritmos (avanzado)

---

## Objetivos

Al finalizar:

- [ ] Dominar for, while, do-while
- [ ] Crear y manipular arrays
- [ ] Definir y usar funciones
- [ ] Implementar búsqueda lineal y binaria
- [ ] Implementar bubble sort y selection sort
- [ ] Entender complejidad Big O

---

## Conceptos Clave

### Loops

```c
for (int i = 0; i < n; i++)    // Iteraciones conocidas
while (condicion)               // Condición al inicio
do { } while (condicion);       // Al menos una vez
```

### Arrays

```c
int arr[5] = {1, 2, 3, 4, 5};
arr[0]  // Primer elemento
arr[4]  // Último elemento
```

### Funciones

```c
int sumar(int a, int b) {
    return a + b;
}
```

---

## Algoritmos Esenciales

**Búsqueda Lineal**: O(n)
```c
for (int i = 0; i < n; i++)
    if (arr[i] == objetivo)
        return i;
```

**Búsqueda Binaria**: O(log n) - Array ordenado
```c
while (inicio <= fin) {
    medio = (inicio + fin) / 2;
    if (arr[medio] == objetivo) return medio;
    // ...
}
```

**Bubble Sort**: O(n²)
```c
for (i...) {
    for (j...) {
        if (arr[j] > arr[j+1])
            swap(arr[j], arr[j+1]);
    }
}
```

---

## Ruta de Aprendizaje

### Día 1-2: Loops y Arrays
- Teoría completa
- Ejercicios 1-4
- Práctica con loops

### Día 3: Funciones
- Crear múltiples funciones
- Ejercicios 5-7

### Día 4: Algoritmos
- Implementar búsqueda
- Implementar ordenamiento
- Ejercicios 8-10

### Día 5-7: Proyecto
- Diseño
- Implementación
- Testing y documentación

---

## Recursos

### Visualizadores
- [VisuAlgo](https://visualgo.net/) - Ver algoritmos en acción
- [Python Tutor - C](http://pythontutor.com/c.html)

### Documentación
- [C Arrays - Learn-C](https://www.learn-c.org/en/Arrays)
- [Sorting Algorithms](https://www.toptal.com/developers/sorting-algorithms)

---

## Errores Comunes

1. **Índice fuera de rango**: `arr[5]` en array de 5 elementos
2. **Loop infinito**: Olvidar incrementar contador
3. **Modificar array sin pasar tamaño**: Siempre pasar `n`
4. **Ordenar antes de buscar**: Binaria requiere array ordenado

---

## Evaluación

**Ejercicios (40%)**:
- 4 básicos + 2 intermedios: 70%
- Todos básicos + avanzado: 85%
- Todos: 100%

**Proyecto (50%)**:
- Cumple requisitos: 70%
- Con mejoras: 85%
- Excepcional: 100%

**Participación (10%)**

---

## Checklist

**Teoría**:
- [ ] Loops, Arrays, Funciones
- [ ] Algoritmos Básicos
- [ ] Clase/Slides

**Ejercicios Básicos**:
- [ ] Suma Array
- [ ] Máximo/Mínimo
- [ ] Invertir Array
- [ ] Contar Pares

**Ejercicios Intermedios** (mín 2):
- [ ] Búsqueda Lineal
- [ ] Bubble Sort
- [ ] Funciones Arrays

**Proyecto**:
- [ ] Diseñado
- [ ] Implementado
- [ ] Documentado
- [ ] Entregado

---

## Próxima Semana

**Semana 4: Git & GitHub**

No más programación en C por ahora. Aprenderás:
- Control de versiones
- Repositorios
- Colaboración en código

**Preparar**: Cuenta en GitHub

---

#c #arrays #loops #algoritmos #semana3
