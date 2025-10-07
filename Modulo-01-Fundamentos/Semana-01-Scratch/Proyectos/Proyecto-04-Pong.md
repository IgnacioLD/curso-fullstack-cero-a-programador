# Proyecto 04: Pong

**Nivel**: Intermedio | **Tiempo estimado**: 3-4 horas

---

## Descripción del Juego

Recrea el clásico juego Pong: dos paletas que golpean una pelota. Puede ser para 1 jugador (vs computadora) o 2 jugadores.

---

## Mecánicas Principales

1. **Paleta Jugador 1**: Controlada con W/S o flechas arriba/abajo
2. **Paleta Jugador 2**: Controlada con flechas o IA simple
3. **Pelota**: Rebota en paletas y bordes superior/inferior
4. **Puntuación**: Punto cuando la pelota pasa una paleta
5. **Victoria**: Primero en llegar a 5 puntos

---

## Requisitos Mínimos

- [ ] 2 sprites de paletas
- [ ] 1 sprite de pelota
- [ ] Variables "puntos_j1" y "puntos_j2"
- [ ] Movimiento de paletas
- [ ] Pelota que rebota correctamente
- [ ] Detección de goles
- [ ] Reinicio después de cada gol
- [ ] Pantalla de victoria

---

## Guía de Implementación

### Paso 1: Paleta Jugador 1

```
Al hacer clic en bandera verde
├─ Ir a x: -220 y: 0
└─ Por siempre
   ├─ Si <tecla [flecha arriba] presionada?> entonces
   │  └─ Cambiar y por 10
   └─ Si <tecla [flecha abajo] presionada?> entonces
      └─ Cambiar y por -10
```

### Paso 2: Paleta Jugador 2 (IA Simple)

```
Al hacer clic en bandera verde
├─ Ir a x: 220 y: 0
└─ Por siempre
   ├─ Si <y de [Pelota] > y position> entonces
   │  └─ Cambiar y por 5
   └─ Si <y de [Pelota] < y position> entonces
      └─ Cambiar y por -5
```

### Paso 3: Pelota

**Inicialización**:
```
Al hacer clic en bandera verde
├─ Fijar puntos_j1 a 0
├─ Fijar puntos_j2 a 0
└─ Enviar mensaje [nueva_pelota]
```

**Movimiento**:
```
Al recibir [nueva_pelota]
├─ Ir a x: 0 y: 0
├─ Apuntar en dirección [al azar entre -45 y 45]
└─ Por siempre
   ├─ Mover 5 pasos
   ├─ Rebotar si toca borde superior/inferior
   ├─ Si <tocando [Paleta1]?> entonces
   │  └─ Apuntar en dirección [(180 - dirección)]
   ├─ Si <tocando [Paleta2]?> entonces
   │  └─ Apuntar en dirección [(180 - dirección)]
   ├─ Si <x < -240> entonces
   │  ├─ Cambiar puntos_j2 por 1
   │  └─ Enviar mensaje [nueva_pelota]
   └─ Si <x > 240> entonces
      ├─ Cambiar puntos_j1 por 1
      └─ Enviar mensaje [nueva_pelota]
```

---

## Mejoras Opcionales

### Mejora 1: Efectos de Rebote
Cambia ángulo según dónde golpea la pelota en la paleta

### Mejora 2: Velocidad Progresiva
La pelota va más rápido con cada rebote

### Mejora 3: Power-ups
Aparecen aleatoriamente:
- Paleta más grande
- Pelota más lenta
- Doble puntos

### Mejora 4: IA Inteligente
- Fácil: IA lenta
- Medio: IA normal
- Difícil: IA perfecta

### Mejora 5: Efectos Visuales
- Estela de la pelota
- Partículas al rebotar
- Shake screen al anotar

---

## Desafíos Técnicos

### Desafío 1: Multibola
Después de 3 puntos, añade segunda pelota

### Desafío 2: Modo 2 Jugadores
Ambas paletas controladas por humanos:
- J1: W/S
- J2: Flechas arriba/abajo

### Desafío 3: Obstáculos
Bloques en el medio que modifican trayectoria

---

## Physics del Rebote

**Rebote simple** (básico):
```
Apuntar en dirección (180 - dirección)
```

**Rebote avanzado** (según posición en paleta):
```
Si pelota toca arriba de paleta → ángulo hacia arriba
Si pelota toca abajo de paleta → ángulo hacia abajo
Si pelota toca centro → rebote recto
```

---

## Testing

- [ ] Pelota rebota correctamente en todas las superficies
- [ ] Goles se detectan correctamente
- [ ] Puntuación se actualiza
- [ ] Juego termina al llegar a 5 puntos
- [ ] IA no es imposible de vencer
- [ ] Pelota no se "atasca" en paletas

---

[[Proyecto-05-Esquiva-Obstaculos|Siguiente Proyecto]]

#proyecto #intermedio #pong #fisica #ia
