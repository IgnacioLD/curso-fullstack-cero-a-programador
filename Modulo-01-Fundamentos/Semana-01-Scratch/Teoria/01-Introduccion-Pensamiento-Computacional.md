#  Introducción al Pensamiento Computacional

> **Semana 1 - Módulo 1: Fundamentos**
> **Duración**: 5-7 horas de estudio
> **Prerequisitos**: Ninguno

---

##  Índice

- [[# Objetivos de Aprendizaje]]
- [[# ¿Qué es el Pensamiento Computacional?]]
- [[# Los 4 Pilares del Pensamiento Computacional]]
- [[# Introducción a Scratch]]
- [[# Conceptos Fundamentales de Programación]]
- [[# Tu Primer Programa]]
- [[# Recursos Adicionales]]
- [[# Autoevaluación]]

---

##  Objetivos de Aprendizaje

Al finalizar esta semana, serás capaz de:

-  Definir qué es el pensamiento computacional y por qué es importante
-  Aplicar los 4 pilares: descomposición, reconocimiento de patrones, abstracción y algoritmos
-  Crear programas básicos en Scratch usando bloques visuales
-  Entender conceptos fundamentales: secuencias, loops, condicionales y eventos
-  Diseñar y construir un proyecto creativo en Scratch

---

##  ¿Qué es el Pensamiento Computacional?

El **pensamiento computacional** es una forma de resolver problemas que puede ser aplicada por humanos y computadoras. No se trata solo de programar, sino de **pensar de manera estructurada** para descomponer problemas complejos en pasos manejables.

### ¿Por qué es importante?

> "El pensamiento computacional es una habilidad fundamental para el siglo XXI, como leer, escribir y hacer aritmética."
> — *Jeannette Wing, Microsoft Research*

**Aplicaciones en la vida real:**
-  Organizar una mudanza (descomponer tareas)
-  Seguir una receta (algoritmo paso a paso)
-  Desarrollar estrategias en juegos (reconocimiento de patrones)
-  Planificar un viaje (optimización de rutas)

---

##  Los 4 Pilares del Pensamiento Computacional

### 1.  Descomposición (Decomposition)

**Dividir un problema grande en problemas más pequeños y manejables.**

**Ejemplo práctico:**
- **Problema**: Hacer una pizza desde cero
- **Descomposición**:
  1. Preparar la masa
  2. Preparar la salsa
  3. Cortar ingredientes
  4. Armar la pizza
  5. Hornear

**En programación:**
```
Crear un juego de Pong
 Mover la paleta del jugador
 Mover la pelota
 Detectar colisiones
 Llevar el marcador
 Mostrar "Game Over"
```

---

### 2.  Reconocimiento de Patrones (Pattern Recognition)

**Identificar similitudes o patrones que nos ayuden a resolver problemas más eficientemente.**

**Ejemplo cotidiano:**
- Todos los días te vistes: siempre sigues el mismo orden (ropa interior → pantalón → camisa → zapatos)
- No necesitas pensar el orden cada vez, **reconociste el patrón**

**En programación:**
- Si necesitas sumar números del 1 al 100, no escribes 100 líneas
- Reconoces el **patrón**: "sumar el siguiente número hasta llegar a 100"
- Usas un **loop** (bucle)

---

### 3.  Abstracción (Abstraction)

**Enfocarse en la información importante e ignorar los detalles irrelevantes.**

**Ejemplo real:**
- Mapa del metro: solo muestra líneas y estaciones, ignora calles, edificios, distancias reales
- **Abstrae lo esencial** para que sea útil

**En programación:**
- Cuando usas un bloque de Scratch que dice "mover 10 pasos", no necesitas saber cómo la computadora calcula la nueva posición pixel por pixel
- La abstracción **oculta la complejidad**

---

### 4.  Algoritmos (Algorithms)

**Serie de pasos ordenados para resolver un problema o realizar una tarea.**

**Algoritmo cotidiano - Hacer café:**
```
1. Llenar la cafetera con agua
2. Poner filtro
3. Agregar café molido
4. Encender cafetera
5. Esperar 5 minutos
6. Servir café
```

**Características de un buen algoritmo:**
-  **Preciso**: Cada paso está claramente definido
-  **Ordenado**: Los pasos tienen una secuencia lógica
-  **Finito**: Tiene un inicio y un final
-  **Efectivo**: Logra el objetivo deseado

---

##  Introducción a Scratch

### ¿Qué es Scratch?

**Scratch** es un lenguaje de programación visual creado por el MIT Media Lab. Permite crear historias interactivas, juegos y animaciones **sin escribir código**, usando bloques visuales.

### ¿Por qué empezar con Scratch?

-  **Visual**: Arrastras bloques en lugar de escribir código
-  **Sin errores de sintaxis**: Los bloques solo encajan si tienen sentido
-  **Resultados inmediatos**: Ves tu programa correr al instante
-  **Creativo**: Puedes hacer juegos, animaciones, arte interactivo
-  **Comunidad**: Millones de proyectos para explorar

### Acceder a Scratch

 **Sitio oficial**: [https://scratch.mit.edu/](https://scratch.mit.edu/)

**Opciones:**
1. **Online** (recomendado): Crear cuenta gratis en scratch.mit.edu
2. **Offline**: Descargar Scratch Desktop para trabajar sin internet

---

##  Conceptos Fundamentales de Programación

Aunque Scratch es visual, los conceptos que aprendes son **los mismos que en cualquier lenguaje de programación**.

### 1.  Variables

**Una variable es como una caja que guarda un valor que puede cambiar.**

**En Scratch:**
```
Crear variable "puntos"
Asignar "puntos" a 0
Al tocar moneda → sumar 10 a "puntos"
```

**Analogía:**
- Variable = caja con etiqueta
- Nombre de la variable = etiqueta ("puntos")
- Valor = contenido de la caja (0, 10, 20...)

---

### 2.  Secuencias (Sequences)

**Una serie de instrucciones que se ejecutan en orden, de arriba hacia abajo.**

```
1. Al presionar bandera verde
2. Decir "Hola" por 2 segundos
3. Mover 10 pasos
4. Girar 90 grados
```

 **El orden importa**: Si cambias el orden, cambia el resultado.

---

### 3.  Bucles/Loops (Repetition)

**Repetir una acción múltiples veces sin tener que escribirla muchas veces.**

**Tipos de loops en Scratch:**

**Loop infinito:**
```
Por siempre
   Mover 10 pasos
```

**Loop con contador:**
```
Repetir 10 veces
   Mover 10 pasos
```

**Loop condicional:**
```
Repetir hasta que <tocando borde?>
   Mover 10 pasos
```

---

### 4.  Condicionales (If/Else)

**Tomar decisiones basadas en condiciones.**

**Estructura básica:**
```
Si <condición es verdadera>
   Hacer esto
Si no
   Hacer esto otro
```

**Ejemplo Scratch:**
```
Si <tecla espacio presionada?>
   Saltar
Si no
   Caminar
```

**En la vida real:**
```
Si está lloviendo
   Llevar paraguas
Si no
   Usar lentes de sol
```

---

### 5.  Eventos (Events)

**Los eventos hacen que cosas sucedan cuando ocurre algo específico.**

**Eventos comunes en Scratch:**
-  Al hacer clic en bandera verde
- ⌨ Al presionar tecla [espacio]
-  Al hacer clic en este objeto
-  Al recibir mensaje [iniciar juego]

---

##  Tu Primer Programa

### Ejercicio Guiado: "Hola Mundo en Scratch"

#### Paso 1: Crear cuenta y abrir Scratch
1. Ve a [https://scratch.mit.edu/](https://scratch.mit.edu/)
2. Haz clic en "Crear" (Create)
3. ¡Listo! Ya tienes el editor abierto

#### Paso 2: Entender la interfaz

**Scratch tiene 4 áreas principales:**

```

  1. Bloques       2. Scripts           
  (Paleta)         (Área de código)     

  3. Escenario     4. Sprites           
  (Resultado)      (Personajes)         

```

1. **Bloques (izquierda)**: Todas las piezas disponibles
2. **Scripts (centro)**: Donde arrastras y conectas bloques
3. **Escenario (arriba derecha)**: Donde se ejecuta tu programa
4. **Sprites (abajo derecha)**: Personajes y objetos

#### Paso 3: Tu primer programa

**Objetivo**: Hacer que el gato diga "¡Hola Mundo!" cuando hagas clic en la bandera verde.

**Bloques necesarios:**
1. Ve a la categoría "Eventos" (amarillo)
2. Arrastra el bloque "al hacer clic en "
3. Ve a "Apariencia" (morado)
4. Arrastra "decir [¡Hola Mundo!] por 2 segundos"
5. Conéctalos como piezas de Lego

**Código:**
```
 Al hacer clic en bandera verde
 Decir "¡Hola Mundo!" por 2 segundos
```

#### Paso 4: ¡Ejecuta!
1. Haz clic en la bandera verde (**** arriba del escenario)
2. ¡Deberías ver al gato decir "¡Hola Mundo!"!

---

###  Ejercicio 2: Movimiento Básico

**Objetivo**: Hacer que el gato camine de izquierda a derecha rebotando en los bordes.

**Bloques necesarios:**
```
 Al hacer clic en bandera verde
 Apuntar en dirección (90)
 Por siempre
    Mover 10 pasos
    Rebotar si toca un borde
```

**Desafío**: ¿Cómo harías para que vaya más rápido? ¿Y más lento?

---

##  Recursos Adicionales

###  Tutoriales Oficiales
- [Scratch - Primeros Pasos](https://scratch.mit.edu/projects/editor/?tutorial=getStarted) - Tutorial interactivo oficial
- [Scratch Tutorial Videos](https://www.youtube.com/user/ScratchTeam) - Canal oficial de Scratch

###  Documentación
- [Scratch Wiki](https://en.scratch-wiki.info/) - Enciclopedia completa de Scratch
- [Scratch Ideas](https://scratch.mit.edu/ideas) - Guías de proyectos paso a paso

###  Inspiración
- [Proyectos Destacados](https://scratch.mit.edu/explore/projects/all) - Ver qué han hecho otros
- [Estudios de Scratch](https://scratch.mit.edu/studios/) - Colecciones temáticas

###  Videos Recomendados
- [CS50 - Computational Thinking](https://www.youtube.com/watch?v=F0WoVEr0-44) - Introducción de Harvard (inglés)
- [Scratch para principiantes](https://www.youtube.com/results?search_query=scratch+tutorial+espa%C3%B1ol) - Buscar en español

###  Enlaces Internos del Curso
- [[../../Modulo-01-Fundamentos/README|Módulo 1 - Fundamentos Completo]]
- [[../Ejercicios/README|Ejercicios de la Semana]]
- [[../Proyectos/README|Proyecto Semanal]]
- [[../../Recursos/README|Recursos Generales del Módulo]]

---

##  Autoevaluación

Antes de continuar, asegúrate de poder responder:

### Conceptos Teóricos
- [ ] ¿Qué es el pensamiento computacional?
- [ ] ¿Cuáles son los 4 pilares del pensamiento computacional?
- [ ] ¿Qué es un algoritmo? Da un ejemplo de la vida cotidiana
- [ ] ¿Cuál es la diferencia entre un bucle y una secuencia?

### Práctica en Scratch
- [ ] ¿Sabes crear un proyecto nuevo en Scratch?
- [ ] ¿Puedes hacer que un sprite se mueva?
- [ ] ¿Sabes cómo usar bloques de eventos?
- [ ] ¿Puedes crear un programa con un loop?

### Desafío
- [ ] ¿Puedes explicarle a alguien qué hace este código?
```
 Al hacer clic en bandera verde
 Fijar puntos a 0
 Por siempre
    Si <tocando estrella?>
       Sumar 1 a puntos
       Decir puntos
```

---

##  Próximos Pasos

1. **Práctica**: Ve a [[../Ejercicios/README|Ejercicios de la Semana]] y completa al menos 3
2. **Proyecto**: Inicia tu [[../Proyectos/README|Proyecto Semanal]] (Juego o Animación)
3. **Explora**: Revisa [proyectos en Scratch](https://scratch.mit.edu/explore/projects/all) para inspirarte
4. **Comunidad**: Comparte tu proyecto y pide feedback

---

##  Notas del Estudiante

*Usa este espacio para tus propias anotaciones, preguntas o ideas:*

```
Tu espacio personal para notas:










```

---

**Última actualización**: 2025-10-02
**Siguiente**: [[02-Guia-Rapida-Scratch|Guía Rápida de Scratch]] →

---

#programacion #scratch #pensamiento-computacional #fundamentos #semana1
