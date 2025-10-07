# Ejercicio 09: Perseguidor Automático

**Nivel**: Avanzado | **Tiempo**: 40 min | **Conceptos**: Sensores, Loops, Operadores, Movimiento

---

## Objetivo

Crear dos sprites: uno que persigue automáticamente al otro.

---

## Requisitos

- [ ] Sprite jugador controlado con teclado
- [ ] Sprite enemigo que persigue al jugador automáticamente
- [ ] El enemigo siempre apunta hacia el jugador
- [ ] Si el enemigo toca al jugador, el juego termina
- [ ] Mensaje de "Game Over"

---

## Pistas

**Sprite Jugador**:
```
Al hacer clic en bandera verde
└─ Por siempre
   └─ [mover con flechas - Ejercicio 04]
```

**Sprite Enemigo**:
```
Al hacer clic en bandera verde
└─ Por siempre
   ├─ Apuntar hacia [Jugador]
   ├─ Mover 3 pasos
   └─ Si <tocando [Jugador]?> entonces
      ├─ Decir "¡Game Over!"
      └─ Detener todo
```

---

## Desafíos

1. **Múltiples enemigos**: 3 perseguidores con diferente velocidad
2. **Poder especial**: Tecla espacio = jugador más rápido 5 segundos
3. **Sistema de vidas**: 3 toques antes de game over
4. **Enemigos inteligentes**: Evitan obstáculos
5. **Niveles**: Enemigos más rápidos cada nivel

---

[[Ejercicio-10-Sistema-Vidas|Siguiente Ejercicio]]

#ejercicio #avanzado #ia-simple #sensores #juego
