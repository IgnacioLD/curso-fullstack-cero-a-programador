# Semana 02: Introducción a C

**Módulo 1: Fundamentos Sólidos**

---

## Bienvenida

Esta semana das el salto de Scratch (visual) a C (texto). Los conceptos son los mismos, solo cambia la sintaxis.

**Duración**: 5-7 días
**Horas totales**: 8-12 horas

---

## Contenido de la Semana

### Teoría

1. [[Teoria/01-Introduccion-C|Introducción a C]] - Historia, sintaxis básica, Hello World
2. [[Teoria/02-Guia-Rapida-C|Guía Rápida de C]] - Referencia de sintaxis
3. [[Teoria/Slides-Clase-02-Introduccion-C|Slides de Clase]] - Presentación

### Ejercicios

**Índice**: [[Ejercicios/README|Guía de Ejercicios]]

**Básicos** (completar todos):
1. [[Ejercicios/Ejercicio-01-Hello-You|Hello You]]
2. [[Ejercicios/Ejercicio-02-Calculadora-Simple|Calculadora Simple]]
3. [[Ejercicios/Ejercicio-03-Par-Impar|Par o Impar]]
4. Mayor de Tres

**Intermedios** (mínimo 2):
5. [[Ejercicios/Ejercicio-05-Conversor-Temperatura|Conversor Temperatura]]
6. Sistema de Calificaciones
7. Menú de Opciones

### Proyectos

**Índice**: [[Proyectos/README|Guía de Proyectos]]

Elige uno:
- [[Proyectos/Proyecto-01-Calculadora-IMC|Calculadora IMC]] (básico)
- Conversor Universal (básico)
- Sistema Calificaciones (intermedio)
- Calculadora Completa (intermedio)
- Juego Adivina Número (avanzado)

---

## Objetivos de Aprendizaje

Al finalizar:

- [ ] Escribir, compilar y ejecutar programas en C
- [ ] Usar variables de diferentes tipos
- [ ] Implementar printf y scanf correctamente
- [ ] Aplicar operadores aritméticos y lógicos
- [ ] Crear condicionales (if/else, switch)
- [ ] Debuggear errores de compilación

---

## Setup Técnico

### Compilador

**Linux/Mac**:
```bash
# Verificar gcc instalado
gcc --version

# Si no está, instalar:
# Mac: xcode-select --install
# Linux: sudo apt install build-essential
```

**Windows**:
- Instalar MinGW o usar WSL
- O usar IDE online: [replit.com](https://replit.com)

### Editor

Opciones:
- VS Code (recomendado)
- Vim/Neovim
- IDE online (replit, OnlineGDB)

---

## Ruta de Aprendizaje

### Día 1-2: Teoría
- Lee toda la teoría
- Escribe Hello World
- Experimenta con printf

### Día 3-4: Ejercicios Básicos
- Completa ejercicios 1-4
- Practica compilación

### Día 5: Ejercicios Intermedios
- Al menos 2 ejercicios nivel medio

### Día 6-7: Proyecto
- Elige y completa proyecto
- Documenta y entrega

---

## Comandos Esenciales

```bash
# Compilar
gcc programa.c -o programa -Wall

# Ejecutar
./programa

# Ver warnings
gcc -Wall programa.c

# Debug
gcc -g programa.c -o programa
gdb programa
```

---

## Recursos

### Documentación
- [Learn-C.org](https://www.learn-c.org/)
- [CS50 Manual](https://manual.cs50.io/)
- [C Reference](https://en.cppreference.com/w/c)

### Videos
- [CS50 Week 1](https://cs50.harvard.edu/x/2024/weeks/1/)
- [C Tutorial - freeCodeCamp](https://www.youtube.com/watch?v=KJgsSFOSQv0)

### Herramientas
- [replit.com](https://replit.com/) - IDE online
- [OnlineGDB](https://www.onlinegdb.com/online_c_compiler)
- [C Tutor](http://pythontutor.com/c.html) - Visualizador

---

## Errores Comunes

1. **Olvidar `;`** - Toda línea termina con punto y coma
2. **scanf sin `&`** - Usar `&` antes de la variable (excepto strings)
3. **`=` vs `==`** - `=` asigna, `==` compara
4. **División entera** - `5/2 = 2`, usa `5.0/2.0` para decimales
5. **Variable no inicializada** - Siempre dar valor inicial

---

## Evaluación

**Para aprobar**:
- Ejercicios (40%): Mínimo 6 ejercicios
- Proyecto (50%): 1 proyecto completo
- Participación (10%): Asistencia y preguntas

**Nota mínima**: 70/100

---

## Checklist

**Teoría**:
- [ ] Leí Introducción a C
- [ ] Revisé Guía Rápida
- [ ] Vi/asistí clase

**Setup**:
- [ ] gcc instalado
- [ ] Editor configurado
- [ ] Hello World compilado

**Ejercicios Básicos**:
- [ ] Hello You
- [ ] Calculadora Simple
- [ ] Par o Impar
- [ ] Mayor de Tres

**Ejercicios Intermedios** (mín 2):
- [ ] Conversor Temperatura
- [ ] Calificaciones
- [ ] Menú Opciones

**Proyecto**:
- [ ] Proyecto elegido
- [ ] Implementado
- [ ] Documentado
- [ ] Entregado

---

## Próxima Semana

**Semana 3: Loops, Arrays y Algoritmos**

Aprenderás:
- Bucles (for, while)
- Arrays (arreglos)
- Funciones
- Algoritmos de búsqueda y ordenamiento

---

#c #semana2 #fundamentos #introduccion

