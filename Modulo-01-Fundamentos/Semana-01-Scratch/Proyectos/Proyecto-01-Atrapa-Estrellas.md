# Proyecto 01: Atrapa las Estrellas

**Nivel**: Básico | **Tiempo estimado**: 2-3 horas

---

## Descripción del Juego

El jugador controla un personaje que debe atrapar estrellas que caen del cielo. Cada estrella atrapada suma puntos. El juego continúa hasta que se pierdan todas las vidas o se alcance cierto puntaje.

---

## Mecánicas Principales

1. **Jugador**: Se mueve horizontalmente con las flechas izquierda/derecha
2. **Estrellas**: Caen desde arriba en posiciones aleatorias
3. **Puntuación**: +1 punto por cada estrella atrapada
4. **Vidas**: -1 vida si una estrella toca el suelo
5. **Game Over**: Cuando las vidas llegan a 0

---

## Requisitos Mínimos

- [ ] Sprite jugador (puede usar uno existente o dibujar)
- [ ] Sprite estrella
- [ ] Variable "puntos" (empieza en 0)
- [ ] Variable "vidas" (empieza en 3)
- [ ] Movimiento del jugador con flechas
- [ ] Estrellas que caen desde arriba
- [ ] Detección de colisión: estrella toca jugador
- [ ] Detección de colisión: estrella toca el suelo
- [ ] Pantalla de Game Over

---

## Guía de Implementación

### Paso 1: Configurar Jugador

**Sprite Jugador - Script 1: Inicialización**
```
Al hacer clic en bandera verde
├─ Ir a x: 0 y: -140
├─ Fijar puntos a 0
└─ Fijar vidas a 3
```

**Sprite Jugador - Script 2: Movimiento**
```
Al hacer clic en bandera verde
└─ Por siempre
   ├─ Si <tecla [flecha derecha] presionada?> entonces
   │  └─ Cambiar x por 10
   └─ Si <tecla [flecha izquierda] presionada?> entonces
      └─ Cambiar x por -10
```

### Paso 2: Configurar Estrella

**Sprite Estrella - Script Principal**
```
Al hacer clic en bandera verde
└─ Por siempre
   ├─ Ir a x: [al azar -220 a 220] y: 180
   ├─ Mostrar
   ├─ Repetir hasta que <y < -180>
   │  ├─ Cambiar y por -5
   │  └─ Si <tocando [Jugador]?> entonces
   │     ├─ Cambiar puntos por 1
   │     ├─ Tocar sonido [pop]
   │     └─ Ir a x: [al azar] y: 180
   ├─ Cambiar vidas por -1
   └─ Si <vidas = 0> entonces
      ├─ Decir "Game Over"
      └─ Detener todo
```

---

## Características Opcionales (Mejoras)

### Mejora 1: Velocidad Progresiva
Las estrellas caen más rápido con más puntos:
```
Cambiar y por [puntos / 10] * -1
```

### Mejora 2: Diferentes Tipos de Objetos
- Estrellas doradas: +5 puntos
- Cometas: +10 puntos
- Bombas: -1 vida

### Mejora 3: Power-ups
- Corazón: +1 vida
- Escudo: Invulnerabilidad temporal
- Imán: Atrae estrellas automáticamente

### Mejora 4: Sistema de Niveles
Cada 20 puntos = nuevo nivel con mayor dificultad

### Mejora 5: Efectos Visuales
- Partículas al atrapar estrellas
- Cambio de fondo según puntuación
- Animación del jugador

---

## Desafíos Técnicos

### Desafío 1: Múltiples Estrellas Simultáneas
Usa clones para tener varias estrellas cayendo al mismo tiempo:
```
Al hacer clic en bandera verde
└─ Por siempre
   ├─ Esperar 2 segundos
   └─ Crear clon de [mí mismo]

Al comenzar como clon
├─ Ir a x: [al azar] y: 180
├─ Repetir hasta que <y < -180>
│  └─ Cambiar y por -5
└─ Borrar este clon
```

### Desafío 2: High Score
Guarda el mejor puntaje usando variables:
```
Si <puntos > record> entonces
  └─ Fijar record a puntos
```

### Desafío 3: Temporizador
Limita el juego a 60 segundos:
```
Variable: tiempo
Por siempre
├─ Esperar 1 segundo
├─ Cambiar tiempo por -1
└─ Si <tiempo = 0> entonces game over
```

---

## Aspectos de Game Design

### Balance de Dificultad

**Muy fácil**: El jugador se aburre
- Estrellas caen muy lento
- Demasiadas vidas

**Muy difícil**: El jugador se frustra
- Estrellas caen muy rápido desde el inicio
- Una sola vida

**Equilibrado**:
- Empieza fácil
- Dificultad aumenta gradualmente
- El jugador siente progresión

### Feedback al Jugador

**Bueno**:
- Sonido al atrapar estrella
- Efecto visual
- Actualización inmediata del puntaje

**Malo**:
- Nada pasa al atrapar estrella
- No está claro qué hacer
- Cambios invisibles

---

## Testing

Prueba estos escenarios:

- [ ] Atrapar 10 estrellas seguidas
- [ ] Dejar que caigan 3 estrellas (perder todas las vidas)
- [ ] Mover jugador a los bordes extremos
- [ ] No mover el jugador (todas las estrellas caen)
- [ ] Jugar hasta 50+ puntos
- [ ] Reiniciar el juego múltiples veces

---

## Rúbrica Específica

**Funcionalidad (40pts)**
- Jugador se mueve: 10pts
- Estrellas caen: 10pts
- Detección de colisiones: 10pts
- Sistema de vidas funciona: 10pts

**Creatividad (30pts)**
- Sprites personalizados: 10pts
- Efectos de sonido: 10pts
- Características extra: 10pts

**Código (20pts)**
- Organizado y limpio: 10pts
- Uso correcto de conceptos: 10pts

**Presentación (10pts)**
- Instrucciones claras: 5pts
- Descripción completa: 5pts

---

## Recursos

**Sprites**:
- Scratch library: Busca "star", "player", "character"
- O dibuja los tuyos propios en el editor

**Sonidos**:
- Scratch library: "pop", "coin", "boing"
- [Freesound.org](https://freesound.org/) para más opciones

**Inspiración**:
- Busca "catch game" en Scratch Explore

---

## Extensiones Creativas

**Cambia el tema**:
- Atrapar manzanas cayendo de un árbol
- Recolectar gotas de lluvia
- Atrapar pelotas de béisbol
- Recoger monedas

**Añade historia**:
- Intro: "Las estrellas están cayendo del cielo, ¡sálvalas!"
- Final diferente según puntuación

**Multiplayer**:
- Dos jugadores: uno con flechas, otro con W-A-S-D
- Competencia: ¿quién atrapa más?

---

[[Proyecto-02-Laberinto|Siguiente Proyecto: Laberinto Simple]]

#proyecto #basico #juego #colisiones #variables
