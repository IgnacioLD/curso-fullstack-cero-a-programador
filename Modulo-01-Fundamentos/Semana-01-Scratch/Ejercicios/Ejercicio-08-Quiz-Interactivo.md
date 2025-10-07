# Ejercicio 08: Quiz Interactivo

**Nivel**: Avanzado | **Tiempo**: 45 min | **Conceptos**: Variables, Condicionales, Operadores, Input

---

## Objetivo

Crear un quiz de 5 preguntas que evalúe respuestas y muestre puntuación final.

---

## Requisitos

- [ ] Mínimo 5 preguntas
- [ ] Variable "puntos" para llevar la cuenta
- [ ] Evalúa si la respuesta es correcta o incorrecta
- [ ] Feedback inmediato (correcto/incorrecto)
- [ ] Muestra puntuación final al terminar

---

## Pistas

**Estructura**:
```
Al hacer clic en bandera verde
├─ Fijar puntos a 0
├─ Pregunta 1
│  ├─ Preguntar "¿Cuál es la capital de Francia?"
│  ├─ Si <respuesta = "París"> entonces
│  │  ├─ Decir "¡Correcto!"
│  │  └─ Cambiar puntos por 1
│  └─ Si no
│     └─ Decir "Incorrecto, era París"
├─ Pregunta 2...
└─ Decir [unir "Puntuación: " y puntos]
```

**Comparar respuestas**:
- Usa operador "=" para comparar
- Considera mayúsculas/minúsculas (París vs parís)

---

## Desafíos

1. **Ignore mayúsculas**: Convierte respuesta a minúsculas
2. **Preguntas aleatorias**: Orden diferente cada vez
3. **Vidas limitadas**: 3 errores = game over
4. **Temporizador**: Límite de tiempo por pregunta
5. **Niveles**: Fácil, medio, difícil

---

[[Ejercicio-09-Perseguidor-Automatico|Siguiente Ejercicio]]

#ejercicio #avanzado #variables #condicionales #quiz
