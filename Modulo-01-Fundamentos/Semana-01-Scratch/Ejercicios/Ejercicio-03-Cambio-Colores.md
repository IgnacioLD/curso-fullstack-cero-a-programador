# Ejercicio 03: Cambio de Colores

**Nivel**: Básico
**Tiempo estimado**: 20 minutos
**Conceptos**: Loops, Apariencia, Efectos de Color

---

## Objetivo

Crear un programa que cambie el color del sprite continuamente usando loops y efectos.

---

## Descripción

El gato debe cambiar de color automáticamente de forma infinita cuando se presione la bandera verde, creando un efecto de arcoíris o disco.

---

## Requisitos

- [ ] El programa empieza al hacer clic en la bandera verde
- [ ] El sprite cambia de color continuamente
- [ ] Usa un loop infinito "por siempre"
- [ ] Los cambios de color son visibles (no muy rápidos)
- [ ] El programa puede detenerse haciendo clic en el botón de stop

---

## Bloques que Necesitarás

**Categorías a usar**:
- Eventos (amarillo)
- Apariencia (morado)
- Control (naranja)

**Pista**: Busca el bloque "cambiar efecto color por X" en Apariencia

---

## Pistas Progresivas

### Pista 1 (Estructura General)
```
Al hacer clic en bandera verde
└─ Por siempre
   ├─ [cambiar color]
   └─ [esperar un poco]
```

### Pista 2 (Más Específico)
El bloque "cambiar efecto color por X" cambia el tinte del sprite.
- Valores positivos: cambian hacia colores diferentes
- Prueba con valores entre 10 y 50

No olvides agregar "esperar" para que no cambie demasiado rápido.

### Pista 3 (Código Casi Completo)
```
Al hacer clic en bandera verde
└─ Por siempre
   ├─ Cambiar efecto [color] por 25
   └─ Esperar 0.1 segundos
```

---

## Conceptos Clave

### Loops Infinitos

Un loop "por siempre" continúa ejecutándose hasta que:
- Presionas el botón de stop
- Usas un bloque "detener todo"

**Uso común**: Animaciones, juegos, detección continua

### Efectos de Apariencia

Scratch ofrece varios efectos visuales:
- **Color**: Cambia el tinte
- **Ojo de pez**: Deforma la imagen
- **Remolino**: Tuerce el sprite
- **Pixelar**: Pixela la imagen
- **Brillo**: Ajusta luminosidad

---

## Criterios de Éxito

Tu ejercicio está completo cuando:

- [ ] El sprite cambia de color continuamente
- [ ] El cambio es suave y visible
- [ ] Usa un loop "por siempre"
- [ ] No cambia tan rápido que no se pueda ver
- [ ] Funciona correctamente al presionar bandera verde

---

## Desafíos Extras (Opcional)

### Desafío 1: Resetear Colores
Antes de empezar el loop, asegúrate de que los efectos estén en 0 usando:
"quitar efectos gráficos"

### Desafío 2: Velocidad Controlada
Pregunta al usuario qué tan rápido quiere que cambien los colores:
- "rápido" = esperar 0.05 segundos
- "normal" = esperar 0.2 segundos
- "lento" = esperar 0.5 segundos

**Pista**: Usa condicionales para comparar la respuesta

### Desafío 3: Múltiples Efectos
Combina múltiples efectos:
- Cambiar color
- Cambiar tamaño gradualmente
- Cambiar brillo

### Desafío 4: Arcoíris Completo
Después de llegar a cierto valor de color (ej: 200), resetea el efecto a 0 para que el ciclo se vea más limpio.

**Pista**: Usa "fijar efecto color a 0" cuando alcance cierto valor

---

## Variaciones Creativas

### Variación 1: Cambio con Click
En lugar de loop infinito, cambia de color cada vez que hagas clic en el sprite.

### Variación 2: Control con Teclado
- Tecla "derecha" = aumenta color
- Tecla "izquierda" = disminuye color
- Tecla "espacio" = resetea a original

### Variación 3: Múltiples Sprites
Crea 3 sprites que cambien de color a diferentes velocidades.

---

## Debugging

### Problema: Cambia demasiado rápido
**Solución**: Aumenta el tiempo de espera (prueba con 0.2 segundos)

### Problema: No veo cambios
**Solución**:
- Verifica que uses "cambiar efecto COLOR"
- Aumenta el valor del cambio (prueba con 50)

### Problema: El sprite se ve extraño después de ejecutar
**Solución**: Agrega "quitar efectos gráficos" al inicio del programa

---

## Experimentación

Prueba cambiar estos valores y observa qué pasa:

| Parámetro | Valor Bajo | Valor Alto | Efecto |
|-----------|------------|------------|--------|
| Cambio de color | 5 | 50 | Velocidad de transición |
| Espera | 0.01s | 1s | Velocidad de animación |

**Anota tus observaciones**:
```
Mejor combinación que encontré:




```

---

## Reflexión

**¿Qué es un loop infinito y cuándo es útil?**
```
(Tu respuesta aquí)
```

**¿Qué otros efectos visuales podrías usar para hacer animaciones?**
```
(Tu respuesta aquí)
```

**¿Cómo detendrías el loop desde dentro del código (sin el botón stop)?**
```
(Tu respuesta aquí)
```

---

## Recursos Relacionados

- [[../Teoria/01-Introduccion-Pensamiento-Computacional#Bucles-Loops|Teoría: Bucles]]
- [[../Teoria/02-Guia-Rapida-Scratch#Apariencia|Referencia: Bloques de Apariencia]]

---

## Siguiente Ejercicio

[[Ejercicio-04-Control-Teclado|Ejercicio 04: Control con Teclado]]

---

#ejercicio #basico #loops #apariencia #efectos
