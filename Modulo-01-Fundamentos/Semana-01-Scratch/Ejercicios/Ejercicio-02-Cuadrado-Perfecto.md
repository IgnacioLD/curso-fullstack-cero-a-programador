# Ejercicio 02: Cuadrado Perfecto

**Nivel**: Básico
**Tiempo estimado**: 20 minutos
**Conceptos**: Loops, Movimiento, Rotación

---

## Objetivo

Hacer que el gato dibuje un cuadrado perfecto usando loops.

---

## Descripción

El gato debe dibujar un cuadrado en la pantalla cuando hagas clic en la bandera verde.

**Características del cuadrado**:
- Cuatro lados iguales
- Cuatro ángulos de 90 grados
- Usar un loop para evitar repetir código

---

## Requisitos

- [ ] El programa empieza al hacer clic en la bandera verde
- [ ] El gato baja el lápiz antes de empezar (para que dibuje)
- [ ] Dibuja exactamente 4 lados iguales
- [ ] Cada esquina es un giro de 90 grados
- [ ] Usa un loop "repetir" (NO copiar 4 veces el mismo código)
- [ ] Al terminar, el gato levanta el lápiz

---

## Bloques que Necesitarás

**Categorías a usar**:
- Eventos (amarillo)
- Movimiento (azul)
- Control (naranja)
- Lápiz (verde oscuro - extensión)

**Nota**: Debes agregar la extensión "Lápiz" (botón abajo a la izquierda en Scratch)

---

## Preparación

### Paso 1: Agregar Extensión Lápiz
1. En Scratch, haz clic en el botón de extensiones (abajo izquierda)
2. Selecciona "Lápiz" (Pen)
3. Ahora tendrás bloques verdes oscuros para dibujar

### Paso 2: Entender el Problema
Para dibujar un cuadrado:
- Avanzar cierta distancia (lado del cuadrado)
- Girar 90 grados
- Repetir 4 veces

---

## Pistas Progresivas

### Pista 1 (Estructura General)
```
Al hacer clic en bandera verde
├─ Borrar todo (limpiar dibujos anteriores)
├─ Bajar lápiz
├─ [repetir 4 veces: mover y girar]
└─ Subir lápiz
```

### Pista 2 (Más Detalles)
Para cada lado del cuadrado:
1. Mover X pasos (prueba con 100 pasos)
2. Girar 90 grados a la derecha

Repite esto 4 veces usando "repetir 4"

### Pista 3 (Código Casi Completo)
```
Al hacer clic en bandera verde
├─ Borrar todo
├─ Bajar lápiz
├─ Repetir 4
│  ├─ Mover 100 pasos
│  └─ Girar [sentido horario] 90 grados
└─ Subir lápiz
```

---

## Conceptos Clave

### ¿Por qué usar un Loop?

**Sin loop** (código repetitivo):
```
Mover 100 pasos
Girar 90 grados
Mover 100 pasos
Girar 90 grados
Mover 100 pasos
Girar 90 grados
Mover 100 pasos
Girar 90 grados
```

**Con loop** (código eficiente):
```
Repetir 4
├─ Mover 100 pasos
└─ Girar 90 grados
```

**Ventajas**:
- Menos código
- Más fácil de entender
- Fácil de modificar (cambias una vez, se aplica 4 veces)

---

## Criterios de Éxito

Tu ejercicio está completo cuando:

- [ ] Dibuja un cuadrado completo y cerrado
- [ ] Los 4 lados tienen el mismo tamaño
- [ ] Usa un loop "repetir 4"
- [ ] No hay líneas extras o movimientos innecesarios
- [ ] Puedes ejecutarlo múltiples veces sin errores

---

## Desafíos Extras (Opcional)

### Desafío 1: Cuadrado Personalizado
Pregunta al usuario qué tamaño de cuadrado quiere (ej: 50, 100, 200 pasos)

**Pista**: Usa una variable para guardar el tamaño

### Desafío 2: Múltiples Cuadrados
Dibuja 4 cuadrados, uno en cada esquina de la pantalla

**Pista**: Usa "ir a x: Y y: X" entre cada cuadrado

### Desafío 3: Espiral Cuadrada
Dibuja una espiral aumentando el tamaño de los lados progresivamente

**Pista**: Usa una variable que incremente en cada repetición

### Desafío 4: Otros Polígonos
Modifica tu código para dibujar:
- Triángulo (3 lados, girar 120 grados)
- Pentágono (5 lados, girar 72 grados)
- Hexágono (6 lados, girar 60 grados)

**Fórmula**: Ángulo de giro = 360 / número de lados

---

## Debugging

### Problema: El cuadrado no se cierra
**Solución**: Verifica que gires exactamente 90 grados y repitas exactamente 4 veces

### Problema: El cuadrado es muy pequeño o muy grande
**Solución**: Ajusta el número de pasos (prueba entre 50 y 150)

### Problema: No veo nada
**Solución**: Asegúrate de:
- Bajar el lápiz
- El sprite esté en una posición visible
- Usar "borrar todo" al inicio

---

## Reflexión

**¿Por qué son útiles los loops?**
```
(Tu respuesta aquí)
```

**¿Qué pasaría si necesitaras dibujar un polígono de 100 lados sin loops?**
```
(Tu respuesta aquí)
```

**¿Puedes pensar en otra situación donde un loop sería útil?**
```
(Tu respuesta aquí)
```

---

## Recursos Relacionados

- [[../Teoria/01-Introduccion-Pensamiento-Computacional#Bucles-Loops|Teoría: Bucles/Loops]]
- [[../Teoria/02-Guia-Rapida-Scratch#Movimiento|Referencia: Bloques de Movimiento]]
- [Scratch Wiki: Pen Blocks](https://en.scratch-wiki.info/wiki/Pen_Extension)

---

## Siguiente Ejercicio

[[Ejercicio-03-Cambio-Colores|Ejercicio 03: Cambio de Colores]]

---

#ejercicio #basico #loops #movimiento #geometria
