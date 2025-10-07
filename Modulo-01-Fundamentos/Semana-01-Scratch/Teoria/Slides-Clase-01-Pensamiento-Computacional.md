---
theme: black
highlightTheme: monokai
transition: slide
---

# Semana 1: Pensamiento Computacional

**Módulo 1: Fundamentos**

De Cero a Full Stack Developer

---

## Agenda de Hoy

1. ¿Qué es el Pensamiento Computacional?
2. Los 4 Pilares Fundamentales
3. Introducción a Scratch
4. Conceptos Básicos de Programación
5. Tu Primer Programa
6. Proyecto de la Semana

---

## Antes de empezar...

### Pregunta para reflexionar:

**¿Qué significa "programar"?**

<!-- pause -->

**Spoiler**: No es solo escribir código

---

# Parte 1: Pensamiento Computacional

---

## ¿Qué es el Pensamiento Computacional?

> "Una forma de resolver problemas que puede ser aplicada por humanos y computadoras"

**No se trata solo de programar**

Se trata de **pensar de manera estructurada** para resolver problemas

---

## ¿Por qué es importante?

"El pensamiento computacional es una habilidad fundamental para el siglo XXI, como leer, escribir y hacer aritmética."

— *Jeannette Wing, Microsoft Research*

---

## En la vida cotidiana

**Ya usas pensamiento computacional:**

- Organizar una mudanza
- Seguir una receta de cocina
- Planificar un viaje
- Desarrollar estrategias en juegos
- Resolver un cubo de Rubik

---

# Los 4 Pilares del Pensamiento Computacional

---

## 1. Descomposición

**Dividir un problema grande en problemas más pequeños**

---

## Ejemplo: Hacer una Pizza

**Problema grande**: Hacer una pizza desde cero

**Descomposición**:
1. Preparar la masa
2. Preparar la salsa
3. Cortar ingredientes
4. Armar la pizza
5. Hornear

---

## Descomposición en Programación

**Crear un juego de Pong**

```
Pong
├── Mover la paleta del jugador
├── Mover la pelota
├── Detectar colisiones
├── Llevar el marcador
└── Mostrar "Game Over"
```

Cada parte es más fácil de resolver por separado

---

## 2. Reconocimiento de Patrones

**Identificar similitudes que nos ayuden a resolver problemas**

---

## Ejemplo Cotidiano

**Vestirse cada día:**

Siempre sigues el mismo orden:
1. Ropa interior
2. Pantalón
3. Camisa
4. Zapatos

No necesitas pensarlo cada vez

**Reconociste el patrón**

---

## Patrones en Programación

**Problema**: Sumar números del 1 al 100

**Sin reconocer patrón**: Escribir 100 líneas
```
suma = 1 + 2 + 3 + 4 + 5 + ...
```

**Reconociendo patrón**: Usar un bucle
```
para cada número del 1 al 100:
    sumar al total
```

---

## 3. Abstracción

**Enfocarse en lo importante e ignorar detalles irrelevantes**

---

## Ejemplo: Mapa del Metro

Un mapa del metro:
- Muestra líneas y estaciones
- Ignora calles, edificios, distancias reales

**Abstrae lo esencial** para ser útil

---

## Abstracción en Programación

Cuando usas un bloque "mover 10 pasos" en Scratch:

- No necesitas saber cómo se calculan píxeles
- No necesitas entender trigonometría
- Solo necesitas el concepto: "mover"

**La abstracción oculta la complejidad**

---

## 4. Algoritmos

**Serie de pasos ordenados para resolver un problema**

---

## Algoritmo Cotidiano

**Hacer café:**

```
1. Llenar la cafetera con agua
2. Poner filtro
3. Agregar café molido
4. Encender cafetera
5. Esperar 5 minutos
6. Servir café
```

---

## Características de un Buen Algoritmo

- **Preciso**: Cada paso está claramente definido
- **Ordenado**: Los pasos tienen secuencia lógica
- **Finito**: Tiene inicio y final
- **Efectivo**: Logra el objetivo deseado

---

## Ejercicio Rápido

**¿Puedes escribir un algoritmo para cepillarte los dientes?**

<!-- pause -->

Piensa en:
- Orden de los pasos
- Qué tan específicos deben ser
- ¿Funciona para cualquier persona?

---

# Parte 2: Introducción a Scratch

---

## ¿Qué es Scratch?

**Lenguaje de programación visual** creado por MIT Media Lab

Permite crear:
- Historias interactivas
- Juegos
- Animaciones

**Sin escribir código** (usando bloques visuales)

---

## ¿Por qué empezar con Scratch?

- **Visual**: Arrastras bloques como LEGO
- **Sin errores de sintaxis**: Los bloques solo encajan si tienen sentido
- **Resultados inmediatos**: Ves tu programa ejecutarse al instante
- **Creativo**: Haz lo que imagines
- **Comunidad**: 100+ millones de proyectos compartidos

---

## Acceder a Scratch

**Sitio oficial**: https://scratch.mit.edu/

**Dos opciones:**

1. **Online** (recomendado): Crear cuenta gratis
2. **Offline**: Descargar Scratch Desktop

**DEMO**: Vamos a abrir Scratch juntos

---

## Interfaz de Scratch

```
┌─────────────────────────────────────┐
│  Bloques    │  Scripts              │
│  (Paleta)   │  (Tu código)          │
├─────────────┼───────────────────────┤
│  Escenario  │  Sprites              │
│  (Preview)  │  (Personajes)         │
└─────────────────────────────────────┘
```

---

## Las 4 Áreas

1. **Bloques** (izquierda): Todas las piezas disponibles
2. **Scripts** (centro): Donde arrastras y conectas bloques
3. **Escenario** (arriba derecha): Donde se ejecuta tu programa
4. **Sprites** (abajo derecha): Personajes y objetos

---

# Parte 3: Conceptos Básicos de Programación

---

## Los Conceptos Son Universales

Lo que aprendas en Scratch **se aplica a TODOS los lenguajes**:

- Python
- JavaScript
- C
- Java
- ...y cualquier otro

---

## 1. Secuencias

**Serie de instrucciones que se ejecutan en orden**

```
1. Al presionar bandera verde
2. Decir "Hola" por 2 segundos
3. Mover 10 pasos
4. Girar 90 grados
```

**El orden importa**

---

## 2. Bucles (Loops)

**Repetir una acción múltiples veces**

**Sin loop**:
```
Mover 10 pasos
Mover 10 pasos
Mover 10 pasos
Mover 10 pasos
...100 veces más
```

**Con loop**:
```
Repetir 100 veces
  └─ Mover 10 pasos
```

---

## Tipos de Loops

**Loop infinito**:
```
Por siempre
  └─ Mover 10 pasos
```

**Loop con contador**:
```
Repetir 10 veces
  └─ Mover 10 pasos
```

**Loop condicional**:
```
Repetir hasta que <tocando borde>
  └─ Mover 10 pasos
```

---

## 3. Condicionales (If/Else)

**Tomar decisiones basadas en condiciones**

```
Si <está lloviendo>
  └─ Llevar paraguas
Si no
  └─ Usar lentes de sol
```

---

## Condicionales en Scratch

```
Si <tecla espacio presionada>
  └─ Saltar
Si no
  └─ Caminar
```

**El programa "decide" qué hacer**

---

## 4. Variables

**Una "caja" que guarda un valor que puede cambiar**

```
Crear variable "puntos"
Fijar "puntos" a 0
Al tocar moneda → sumar 10 a "puntos"
```

**Analogía**: Variable = caja con etiqueta

---

## 5. Eventos

**Los eventos hacen que cosas sucedan cuando ocurre algo específico**

Eventos comunes:
- Al hacer clic en bandera verde
- Al presionar tecla [espacio]
- Al hacer clic en este objeto
- Al recibir mensaje [iniciar juego]

---

# Parte 4: Tu Primer Programa

---

## Hola Mundo en Scratch

**Objetivo**: Hacer que el gato diga "Hola Mundo" cuando hagas clic en la bandera

---

## Paso 1: Abrir Scratch

1. Ve a https://scratch.mit.edu/
2. Haz clic en "Crear"
3. ¡Ya tienes el editor abierto!

**DEMO en vivo**

---

## Paso 2: Arrastrar Bloques

**Bloques necesarios:**

1. Categoría "Eventos" (amarillo)
   → "al hacer clic en bandera verde"

2. Categoría "Apariencia" (morado)
   → "decir [Hola Mundo] por 2 segundos"

3. Conectarlos como LEGO

---

## El Código

```
Al hacer clic en bandera verde
└─ Decir "¡Hola Mundo!" por 2 segundos
```

**¡ESO ES TODO!**

Ahora haz clic en la bandera verde

---

## ¡Lo lograste!

**Acabas de crear tu primer programa**

Felicidades, eres un programador

---

## Ejercicio 2: Movimiento

**Objetivo**: Hacer que el gato camine rebotando en los bordes

```
Al hacer clic en bandera verde
├─ Apuntar en dirección (90)
└─ Por siempre
   ├─ Mover 10 pasos
   └─ Rebotar si toca un borde
```

**Intentémoslo juntos**

---

## Desafío

**¿Cómo harías para que vaya más rápido?**

<!-- pause -->

**Respuesta**: Cambiar "10 pasos" a "20 pasos"

**¿Y más lento?**

<!-- pause -->

**Respuesta**: Cambiar a "5 pasos"

---

# Parte 5: Proyecto de la Semana

---

## Tu Misión

**Crear un juego o animación en Scratch**

**Debe incluir:**
- Al menos 2 sprites
- Movimiento con teclado O automático
- Un bucle (loop)
- Un condicional (if)
- Una variable (para puntos, vidas, etc.)

---

## Ideas de Proyectos

**Nivel Básico:**
- Perseguir el mouse
- Evita los obstáculos
- Animación de baile

**Nivel Intermedio:**
- Atrapa las estrellas
- Laberinto simple
- Quiz interactivo

**Nivel Avanzado:**
- Plataformas básico
- Pong para dos jugadores

---

## Recursos para Ayudarte

**Tutoriales oficiales**:
- https://scratch.mit.edu/projects/editor/?tutorial=getStarted

**Proyectos para inspirarte**:
- https://scratch.mit.edu/explore/projects/all

**¿Atascado?** Haz clic en "Ver Dentro" de proyectos que te gusten

---

## Fechas Importantes

**Plazo del proyecto**: Final de la semana

**Debe estar**:
- Subido a tu cuenta de Scratch
- Link compartido en la plataforma del curso
- Incluir instrucciones de cómo jugarlo

---

# Resumen de Hoy

---

## Lo que Aprendimos

1. Pensamiento Computacional y sus 4 pilares
2. Qué es Scratch y por qué es útil
3. Conceptos fundamentales: secuencias, loops, condicionales, variables, eventos
4. Cómo crear tu primer programa
5. Proyecto de la semana

---

## Próximos Pasos

**Hoy después de clase:**
1. Crear cuenta en Scratch (si no tienes)
2. Experimentar con bloques por 30 min
3. Empezar a planear tu proyecto

**Esta semana:**
1. Completar ejercicios prácticos
2. Trabajar en tu proyecto
3. Explorar proyectos de otros para ideas

---

## Autoevaluación

**Pregúntate:**

- ¿Puedo explicar los 4 pilares del pensamiento computacional?
- ¿Sé cómo crear un programa básico en Scratch?
- ¿Entiendo qué hace un loop?
- ¿Sé la diferencia entre secuencia y condicional?

Si respondiste "sí" a todo, ¡vas muy bien!

---

## Recursos para la Semana

**Documentación del curso:**
- Introducción al Pensamiento Computacional (MD)
- Guía Rápida de Scratch (referencia)

**Online:**
- CS50 Semana 0 (Scratch)
- Scratch Wiki
- Tutoriales interactivos

---

## Preguntas

**¿Dudas sobre:**

- Pensamiento computacional?
- Scratch?
- El proyecto?
- Cualquier concepto?

---

# ¡A Crear!

**Tu viaje como programador empieza hoy**

**Recuerda**: Todos los programadores empezaron donde tú estás ahora

**La diferencia**: Ellos no se rindieron

---

## Próxima Semana

**Semana 2: Introducción a C**

- Primer lenguaje de programación "real"
- Variables, tipos de datos
- Entrada/salida
- Condicionales en código

**Nos vemos la próxima clase**

---

# ¡Gracias!

**¿Preguntas finales?**

Recursos:
- Material del curso en la plataforma
- Scratch: https://scratch.mit.edu/
- Comunidad del curso

**¡Happy coding!**
