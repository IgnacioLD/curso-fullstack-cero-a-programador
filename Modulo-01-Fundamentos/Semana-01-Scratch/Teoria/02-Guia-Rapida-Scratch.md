#  Guía Rápida de Scratch

> **Referencia visual de bloques y conceptos esenciales**

---

##  Categorías de Bloques

Scratch organiza sus bloques en **9 categorías** por colores:

| Color | Categoría | Función |
|-------|-----------|---------|
| 🟡 Amarillo | **Eventos** | Iniciar programas (ej: al hacer clic) |
| 🟣 Morado | **Apariencia** | Cambiar cómo se ve (decir, cambiar disfraz) |
|  Azul | **Movimiento** | Mover y rotar sprites |
| 🟢 Verde | **Sonido** | Reproducir sonidos y música |
| 🟠 Naranja | **Control** | Loops, if/else, esperar |
|  Rojo | **Sensores** | Detectar toques, teclas, mouse |
| 🟢 Verde oscuro | **Operadores** | Matemáticas, comparaciones, lógica |
| 🟠 Naranja | **Variables** | Crear y usar variables |
| 🟪 Morado oscuro | **Mis Bloques** | Crear tus propios bloques personalizados |

---

##  Bloques Esenciales para Principiantes

### 🟡 Eventos (Empezar tu código)

```
 Al hacer clic en bandera verde
   → El evento más usado, inicia tu programa

⌨ Al presionar tecla [espacio]
   → Responde a teclas del teclado

 Al hacer clic en este objeto
   → Cuando haces clic en el sprite

 Al recibir [mensaje1]
   → Comunicación entre sprites
```

---

###  Movimiento

```
→ Mover (10) pasos
   Mueve el sprite hacia adelante

↻ Girar ↻ (15) grados
   Rota en sentido horario

↺ Girar ↺ (15) grados
   Rota en sentido antihorario

→ Apuntar en dirección (90)
   0=arriba, 90=derecha, 180=abajo, -90=izquierda

↶ Rebotar si toca un borde
   Rebota al llegar al límite del escenario

→ Ir a x: (0) y: (0)
   Mover a coordenada específica
```

**Coordenadas del escenario:**
```
        y: 180
          ↑
          
x: -240 ←→ x: 240
          
          ↓
        y: -180
```

---

### 🟣 Apariencia

```
 Decir [Hola] por (2) segundos
   Muestra texto en bocadillo temporal

 Decir [Hola]
   Muestra texto permanente (hasta cambiar)

 Pensar [Hmm...] por (2) segundos
   Igual que decir pero con nube de pensamiento

 Mostrar
   Hace visible el sprite

 Esconder
   Hace invisible el sprite

 Cambiar disfraz a [disfraz2]
   Cambia apariencia (para animaciones)

 Cambiar tamaño por (10)
   Agranda o achica (+10 = más grande, -10 = más pequeño)
```

---

### 🟠 Control (Loops y Decisiones)

#### Loops (Repetición)

```
 Por siempre
    [bloques aquí]

   Repite infinitamente (usar con bandera verde)
```

```
 Repetir (10)
    [bloques aquí]

   Repite número específico de veces
```

```
 Repetir hasta que <condición>
    [bloques aquí]

   Repite hasta que algo sea verdadero
```

#### Condicionales (Decisiones)

```
 Si <condición> entonces
    [bloques aquí]

   Ejecuta solo si la condición es verdadera
```

```
 Si <condición> entonces
    [bloques aquí]
   Si no
    [otros bloques]

   Una cosa u otra, nunca ambas
```

#### Otros

```
⏸ Esperar (1) segundos
   Pausa el programa

⏹ Detener [todo]
   Termina el programa
```

---

###  Sensores (Detectar cosas)

```
 ¿Tocando [puntero del ratón]?
   Detecta si toca mouse, otro sprite, color, etc.

⌨ ¿Tecla [espacio] presionada?
   Detecta si una tecla está presionada

 Distancia a [puntero del ratón]
   Qué tan lejos está de algo

 ¿Pregunta [¿Cómo te llamas?] y esperar
   Pide input del usuario

 Respuesta
   Almacena lo que el usuario escribió
```

---

### 🟢 Operadores (Matemáticas y Lógica)

#### Matemáticas
```
 (1) + (1) = 2
 (5) - (3) = 2
 (4) * (2) = 8
 (10) / (2) = 5

 Número al azar entre (1) y (10)
   Genera número random
```

#### Comparaciones
```
= (5) = (5)  → verdadero si iguales
< (3) < (5)  → verdadero si menor que
> (7) > (5)  → verdadero si mayor que
```

#### Lógica
```
Y <> y <>    → ambas condiciones verdaderas
O <> o <>    → al menos una verdadera
NO <>        → invierte verdadero/falso
```

---

### 🟠 Variables (Guardar Datos)

```
1. Hacer variable → Crea nueva variable
2. Fijar [puntos] a (0) → Da valor inicial
3. Cambiar [puntos] por (10) → Suma/resta
4. Mostrar variable → Se ve en pantalla
5. Esconder variable → No se ve
```

**Ejemplo completo de sistema de puntos:**
```
 Al hacer clic en bandera verde
 Fijar puntos a 0
 Por siempre
    Si <tocando moneda?>
       Cambiar puntos por 10
       Tocar sonido [coin]
```

---

##  Patrones Comunes

### Patrón 1: Mover con Teclado

```
 Al hacer clic en bandera verde
 Por siempre
    Si <tecla [flecha derecha] presionada?> entonces
      Cambiar x por (10)
    Si <tecla [flecha izquierda] presionada?> entonces
      Cambiar x por (-10)
    Si <tecla [flecha arriba] presionada?> entonces
      Cambiar y por (10)
    Si <tecla [flecha abajo] presionada?> entonces
       Cambiar y por (-10)
```

---

### Patrón 2: Animación Simple

```
 Al hacer clic en bandera verde
 Por siempre
    Siguiente disfraz
    Esperar (0.1) segundos
```

---

### Patrón 3: Seguir al Mouse

```
 Al hacer clic en bandera verde
 Por siempre
    Apuntar hacia [puntero del ratón]
    Mover (10) pasos
```

---

### Patrón 4: Rebote en Bordes

```
 Al hacer clic en bandera verde
 Apuntar en dirección (90)
 Por siempre
    Mover (5) pasos
    Rebotar si toca un borde
```

---

### Patrón 5: Contador de Clicks

```
 Al hacer clic en bandera verde
 Fijar clicks a 0

 Al hacer clic en este objeto
 Cambiar clicks por 1
 Decir [clicks] por (1) segundos
```

---

### Patrón 6: Game Over Simple

```
 Al hacer clic en bandera verde
 Por siempre
    Si <tocando [enemigo]?> entonces
       Decir [Game Over!] por (2) segundos
       Detener [todo]
```

---

##  Tips y Trucos

###  Debugging (Encontrar errores)

**Problema**: Mi sprite no se mueve
-  ¿Hay un bloque de evento al inicio? (bandera verde, tecla, etc.)
-  ¿Los bloques están conectados?
-  ¿El sprite está visible? (no escondido)

**Problema**: El loop no funciona
-  ¿El bloque de loop contiene otros bloques dentro?
-  ¿Está dentro de un evento?

**Problema**: El condicional nunca se ejecuta
-  Revisa la condición con bloques de "decir" para ver valores
-  ¿La condición puede llegar a ser verdadera?

---

###  Mejores Prácticas

1. **Empieza simple**: Un bloque de evento + un bloque de acción
2. **Prueba frecuentemente**: Haz clic en  después de cada cambio
3. **Comenta tu código**: Usa "decir" temporalmente para ver qué pasa
4. **Guarda versiones**: Usa "Guardar como copia" antes de cambios grandes
5. **Explora otros proyectos**: Haz clic en "Ver Dentro" de proyectos que te gusten

---

###  Checklist de Proyecto

Antes de compartir tu proyecto:
- [ ] Funciona sin errores al hacer clic en 
- [ ] Tiene instrucciones claras (cómo jugar/usar)
- [ ] Los sprites tienen nombres descriptivos
- [ ] El código está organizado (no todos los bloques amontonados)
- [ ] Tiene un objetivo claro (qué hace el proyecto)

---

##  Referencias

### Documentación Oficial
- [Scratch Blocks Reference](https://en.scratch-wiki.info/wiki/Blocks) - Todos los bloques explicados
- [Scratch Tutorial](https://scratch.mit.edu/projects/editor/?tutorial=getStarted) - Tutorial interactivo

### Enlaces Internos
- [[01-Introduccion-Pensamiento-Computacional|← Introducción al Pensamiento Computacional]]
- [[../Ejercicios/README|Ejercicios Prácticos]]
- [[../Proyectos/README|Proyecto de la Semana]]

---

##  Glosario Rápido

| Término | Definición |
|---------|------------|
| **Sprite** | Personaje u objeto en tu proyecto |
| **Escenario** | Fondo donde se mueven los sprites (Stage) |
| **Disfraz** | Diferente apariencia de un sprite (para animaciones) |
| **Bloque** | Pieza de código que arrastra |
| **Script** | Conjunto de bloques conectados |
| **Fondo** | Imagen de fondo del escenario (Backdrop) |
| **Bucle** | Bloque que repite acciones (Loop) |
| **Evento** | Bloque amarillo que inicia un script |

---

**¿Listo para crear?**
 Abre [Scratch](https://scratch.mit.edu/) y empieza a experimentar!

---

#scratch #referencia #guia-rapida #bloques
