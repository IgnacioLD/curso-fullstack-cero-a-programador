# Ejercicio 04: Control con Teclado

**Nivel**: Básico
**Tiempo estimado**: 30 minutos
**Conceptos**: Eventos, Condicionales, Movimiento

---

## Objetivo

Crear un sprite que se pueda mover en las 4 direcciones usando las flechas del teclado.

---

## Descripción

El gato debe moverse por la pantalla respondiendo a las teclas de dirección:
- Flecha arriba: mover hacia arriba
- Flecha abajo: mover hacia abajo
- Flecha derecha: mover hacia la derecha
- Flecha izquierda: mover hacia la izquierda

---

## Requisitos

- [ ] El programa empieza al hacer clic en la bandera verde
- [ ] El sprite se coloca en el centro al inicio (x:0, y:0)
- [ ] Responde a las 4 flechas del teclado
- [ ] Se mueve continuamente mientras presionas una flecha
- [ ] El movimiento es suave y controlable

---

## Bloques que Necesitarás

**Categorías a usar**:
- Eventos (amarillo)
- Control (naranja)
- Sensores (rojo)
- Movimiento (azul)

---

## Pistas Progresivas

### Pista 1 (Estructura General)
```
Al hacer clic en bandera verde
├─ Ir a x:0 y:0
└─ Por siempre
   ├─ [si tecla arriba presionada, mover arriba]
   ├─ [si tecla abajo presionada, mover abajo]
   ├─ [si tecla derecha presionada, mover derecha]
   └─ [si tecla izquierda presionada, mover izquierda]
```

### Pista 2 (Detectar Teclas)
Usa el sensor "¿tecla [espacio] presionada?"
- Cambia "espacio" por las flechas del teclado
- Colócalo dentro de un condicional "si <> entonces"

### Pista 3 (Mover el Sprite)
Para mover en cada dirección:
- **Arriba**: cambiar y por 10
- **Abajo**: cambiar y por -10
- **Derecha**: cambiar x por 10
- **Izquierda**: cambiar x por -10

### Pista 4 (Código Casi Completo)
```
Al hacer clic en bandera verde
├─ Ir a x:0 y:0
└─ Por siempre
   ├─ Si <¿tecla [flecha arriba] presionada?> entonces
   │  └─ Cambiar y por 10
   ├─ Si <¿tecla [flecha abajo] presionada?> entonces
   │  └─ Cambiar y por -10
   ├─ Si <¿tecla [flecha derecha] presionada?> entonces
   │  └─ Cambiar x por 10
   └─ Si <¿tecla [flecha izquierda] presionada?> entonces
      └─ Cambiar x por -10
```

---

## Conceptos Clave

### Sistema de Coordenadas

El escenario de Scratch usa coordenadas X e Y:

```
        y: 180 (arriba)
            ↑
            |
x: -240 ←---0---→ x: 240
(izquierda) |  (derecha)
            ↓
        y: -180 (abajo)
```

- **X**: Posición horizontal (izquierda-derecha)
- **Y**: Posición vertical (arriba-abajo)

### Condicionales en Loop

Al poner condicionales dentro de un loop "por siempre":
- El programa verifica constantemente si las teclas están presionadas
- Responde inmediatamente cuando presionas una tecla
- Permite movimiento fluido

---

## Criterios de Éxito

Tu ejercicio está completo cuando:

- [ ] El sprite empieza en el centro (0, 0)
- [ ] Responde a las 4 flechas correctamente
- [ ] El movimiento es fluido (no entrecortado)
- [ ] Puedes mover en diagonales presionando 2 flechas
- [ ] El sprite no desaparece al llegar a los bordes

---

## Desafíos Extras (Opcional)

### Desafío 1: Límites de Pantalla
Evita que el sprite salga del escenario usando condicionales:
```
Si posición x > 230 entonces
  └─ Fijar x a 230
```

Haz lo mismo para los 4 bordes.

### Desafío 2: Velocidad Variable
- Tecla "espacio": aumenta velocidad
- Tecla "shift": disminuye velocidad

**Pista**: Usa una variable "velocidad" en lugar de 10

### Desafío 3: Rotación del Sprite
Haz que el sprite apunte en la dirección hacia donde se mueve:
- Arriba: apuntar en dirección 0
- Derecha: apuntar en dirección 90
- Abajo: apuntar en dirección 180
- Izquierda: apuntar en dirección -90

### Desafío 4: Estela de Colores
Agrega la extensión Lápiz y haz que el sprite dibuje mientras se mueve:
- Bajar lápiz al inicio
- Cambiar color del lápiz gradualmente

### Desafío 5: Controles Alternativos
Agrega control con teclas W-A-S-D además de las flechas.

---

## Variaciones Creativas

### Variación 1: Movimiento con Física
En lugar de cambiar x/y directamente, usa:
"mover 10 pasos" + "apuntar en dirección X"

### Variación 2: Sprite que Deja Rastro
Crea clones del sprite en su posición cada cierto tiempo.

### Variación 3: Múltiples Sprites Controlables
- Sprite 1: flechas
- Sprite 2: W-A-S-D

Un juego para 2 jugadores.

---

## Debugging

### Problema: El sprite se mueve muy lento
**Solución**: Aumenta el valor de cambio (prueba con 15 o 20)

### Problema: El sprite se mueve muy rápido
**Solución**:
- Disminuye el valor de cambio (prueba con 5)
- Agrega "esperar 0.01 segundos" en el loop

### Problema: El sprite solo se mueve una vez
**Solución**: Asegúrate de que los condicionales estén DENTRO del loop "por siempre"

### Problema: El sprite desaparece
**Solución**:
- Implementa límites de pantalla (Desafío 1)
- O usa "rebotar si toca un borde"

---

## Testing

Verifica que funcione correctamente:

- [ ] Presiona cada flecha individualmente
- [ ] Presiona dos flechas simultáneamente (diagonal)
- [ ] Presiona varias flechas rápidamente
- [ ] Mantén presionada una flecha por varios segundos
- [ ] Mueve el sprite hasta los bordes de la pantalla

---

## Reflexión

**¿Por qué usamos un loop "por siempre" en lugar de eventos "al presionar tecla"?**
```
(Tu respuesta aquí)
```

**¿Qué ventajas tiene usar cambiar x/y en lugar de "mover X pasos"?**
```
(Tu respuesta aquí)
```

**¿Cómo se podría implementar aceleración y desaceleración realistas?**
```
(Tu respuesta aquí)
```

---

## Aplicaciones Reales

Este patrón de código se usa en:
- Juegos de plataformas
- Juegos de laberintos
- Simuladores de conducción
- Cualquier juego con control de jugador

Es uno de los patrones más fundamentales en desarrollo de videojuegos.

---

## Recursos Relacionados

- [[../Teoria/01-Introduccion-Pensamiento-Computacional#Condicionales|Teoría: Condicionales]]
- [[../Teoria/02-Guia-Rapida-Scratch#Sensores|Referencia: Bloques de Sensores]]
- [[../Teoria/02-Guia-Rapida-Scratch#Patrón-1-Mover-con-Teclado|Patrón: Mover con Teclado]]

---

## Siguiente Ejercicio

[[Ejercicio-05-Contador-Clicks|Ejercicio 05: Contador de Clicks]]

---

#ejercicio #basico #eventos #condicionales #movimiento #teclado
