# Ejercicio 10: Sistema de Vidas

**Nivel**: Avanzado | **Tiempo**: 50 min | **Conceptos**: Variables, Condicionales, Game Over, Lógica de Juego

---

## Objetivo

Implementar un sistema completo de vidas en un mini-juego.

---

## Requisitos

- [ ] Variable "vidas" que empieza en 3
- [ ] Sprite jugador y sprite enemigo/obstáculo
- [ ] Al tocar enemigo: pierde 1 vida
- [ ] Muestra vidas restantes en pantalla
- [ ] Game Over cuando vidas = 0
- [ ] Opción de reiniciar

---

## Pistas

**Estructura principal**:
```
Al hacer clic en bandera verde
├─ Fijar vidas a 3
├─ Mostrar variable vidas
└─ Por siempre
   ├─ [movimiento del jugador]
   └─ Si <tocando enemigo?> entonces
      ├─ Cambiar vidas por -1
      ├─ Tocar sonido [hurt]
      ├─ Esperar 1 segundo (invulnerabilidad temporal)
      └─ Si <vidas = 0> entonces
         ├─ Decir "Game Over"
         └─ Detener todo
```

**Feedback visual**:
- Cambiar color del sprite cuando pierde vida
- Efecto de parpadeo (invulnerabilidad)
- Sprites en pantalla mostrando vidas restantes

---

## Desafíos

1. **Vidas extra**: Recolectar corazones da +1 vida
2. **Dificultad progresiva**: Enemigos más rápidos con menos vidas
3. **Barra de salud visual**: En lugar de número
4. **Diferentes daños**: Algunos enemigos quitan 2 vidas
5. **Pantalla de Game Over**: Con estadísticas (tiempo jugado, enemigos evitados)

---

## Conceptos de Game Design

**Invulnerabilidad temporal**: Después de recibir daño, el jugador es invulnerable brevemente
- Evita perder todas las vidas instantáneamente
- Da tiempo al jugador para reaccionar

**Feedback claro**:
- Sonido de daño
- Cambio visual
- Actualización inmediata de UI

---

[[../Proyectos/README|Continuar con Proyectos]]

#ejercicio #avanzado #game-design #vidas #variables
