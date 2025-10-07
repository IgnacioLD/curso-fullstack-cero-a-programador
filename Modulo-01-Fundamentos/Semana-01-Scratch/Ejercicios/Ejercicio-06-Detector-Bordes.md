# Ejercicio 06: Detector de Bordes

**Nivel**: Intermedio | **Tiempo**: 30 min | **Conceptos**: Condicionales, Sensores, Lógica

---

## Objetivo

Crear un sprite que cambie de color cuando toque los bordes de la pantalla.

---

## Requisitos

- [ ] El sprite se mueve continuamente en una dirección
- [ ] Detecta cuando toca el borde superior, inferior, izquierdo o derecho
- [ ] Cambia a un color específico según el borde tocado
- [ ] Rebota al tocar un borde

---

## Pistas

**Estructura**:
```
Al hacer clic en bandera verde
├─ Apuntar en dirección aleatoria
└─ Por siempre
   ├─ Mover 5 pasos
   ├─ Si <tocando borde?> entonces
   │  ├─ Rebotar
   │  └─ Cambiar color según posición
   ```

**Detectar qué borde**:
- Borde superior: y > 160
- Borde inferior: y < -160
- Borde derecho: x > 220
- Borde izquierdo: x < -220

---

## Desafíos

1. **Contador de toques**: Variable que cuenta cuántas veces tocó bordes
2. **Sonidos diferentes**: Cada borde reproduce un sonido distinto
3. **Mensaje en pantalla**: El sprite dice "¡Toqué el borde superior!" etc.

---

[[Ejercicio-07-Animacion-Caminando|Siguiente Ejercicio]]

#ejercicio #intermedio #condicionales #sensores
