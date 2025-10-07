# Ejercicio 05: Contador de Clicks

**Nivel**: Intermedio
**Tiempo estimado**: 25 minutos
**Conceptos**: Variables, Eventos, Operadores

---

## Objetivo

Crear un programa que cuente cuántas veces haces clic en el sprite y muestre el contador.

---

## Descripción

Cuando hagas clic en el sprite:
1. El contador aumenta en 1
2. El sprite dice cuántos clicks lleva acumulados
3. Al presionar la bandera verde, el contador se resetea a 0

---

## Requisitos

- [ ] El programa empieza al hacer clic en la bandera verde
- [ ] Crea una variable llamada "clicks" o "contador"
- [ ] La variable empieza en 0
- [ ] Cada click en el sprite aumenta el contador en 1
- [ ] El sprite muestra el número actual de clicks
- [ ] La variable es visible en pantalla

---

## Bloques que Necesitarás

**Categorías a usar**:
- Eventos (amarillo)
- Variables (naranja)
- Apariencia (morado)
- Operadores (verde)

**Nota**: Primero debes crear una variable nueva (botón "Hacer una variable")

---

## Pistas Progresivas

### Pista 1 (Crear Variable)
1. Ve a la categoría Variables
2. Haz clic en "Hacer una variable"
3. Nómbrala "clicks"
4. Asegúrate que esté marcada para que se vea en pantalla

### Pista 2 (Estructura General)
Necesitas DOS scripts separados:

**Script 1**: Al presionar bandera verde
- Resetear contador a 0

**Script 2**: Al hacer clic en el sprite
- Aumentar contador
- Mostrar el número

### Pista 3 (Más Específico)
```
Script 1:
Al hacer clic en bandera verde
└─ Fijar clicks a 0

Script 2:
Al hacer clic en este objeto
├─ Cambiar clicks por 1
└─ Decir [clicks] por 1 segundos
```

### Pista 4 (Mejora Visual)
En lugar de decir solo el número, puedes unir texto:
```
Decir [unir "Total: " y clicks] por 1 segundos
```

---

## Conceptos Clave

### Variables

Una variable es un espacio en memoria que guarda un valor que puede cambiar.

**Operaciones básicas**:
- `Fijar [var] a X` → Establece valor inicial
- `Cambiar [var] por X` → Suma/resta al valor actual
- `Variable [var]` → Lee el valor actual

### Múltiples Eventos

Un sprite puede tener varios scripts que empiezan con diferentes eventos:
- Uno con "al hacer clic en bandera verde"
- Otro con "al hacer clic en este objeto"
- Ambos funcionan independientemente

---

## Criterios de Éxito

Tu ejercicio está completo cuando:

- [ ] Cada click aumenta el contador correctamente
- [ ] El contador se muestra en pantalla
- [ ] Al presionar bandera verde, el contador vuelve a 0
- [ ] Puedes hacer múltiples ciclos (bandera → clicks → bandera → clicks)
- [ ] El número que se dice corresponde al número en la variable

---

## Desafíos Extras (Opcional)

### Desafío 1: Objetivo de Clicks
- Pregunta al usuario cuántos clicks quiere hacer
- Cuando alcance ese número, el sprite dice "¡Objetivo alcanzado!"
- El sprite toca un sonido de victoria

### Desafío 2: Clicks por Segundo
- Crea una segunda variable "tiempo"
- Muestra cuántos clicks haces en 10 segundos
- Al finalizar, muestra el promedio (clicks / 10)

### Desafío 3: Doble Click
- Si haces click 2 veces en menos de 0.5 segundos, suma 2 puntos en lugar de 1
- El sprite dice "¡Doble click!"

**Pista**: Usa un temporizador y condicionales

### Desafío 4: Record Personal
- Crea variable "record"
- Si superas tu record anterior, el sprite lo anuncia
- El record se guarda entre ejecuciones

### Desafío 5: Diferentes Zonas
Crea varios sprites con diferentes valores:
- Sprite azul: +1 click
- Sprite verde: +5 clicks
- Sprite rojo: -3 clicks

---

## Variaciones Creativas

### Variación 1: Clicker Game
- Cada click genera "monedas"
- Compra mejoras que aumentan monedas por click
- Compra auto-clickers que generan monedas automáticamente

### Variación 2: Whack-a-Mole
- El sprite aparece en posiciones aleatorias
- Solo cuenta si haces click cuando está visible
- Límite de tiempo

### Variación 3: Reacción Visual
El sprite cambia:
- De tamaño (más grande con más clicks)
- De color (color diferente cada 5 clicks)
- De disfraz (animación cada cierto número)

---

## Debugging

### Problema: El contador no aumenta
**Solución**:
- Verifica que uses "cambiar por 1", no "fijar a 1"
- Asegúrate que el evento sea "al hacer clic en ESTE objeto"

### Problema: El contador no se resetea
**Solución**:
- Verifica que tengas "fijar clicks a 0" bajo "al hacer clic en bandera verde"

### Problema: La variable no se ve
**Solución**:
- En la categoría Variables, marca el checkbox junto a "clicks"

### Problema: El sprite dice "clicks" en lugar del número
**Solución**:
- Usa el bloque ovalado "clicks" (valor de la variable)
- No escribas la palabra "clicks" en el bloque de texto

---

## Experimentación

Prueba diferentes configuraciones:

| Modificación | Efecto |
|--------------|--------|
| Cambiar por 2 | Cuenta de 2 en 2 |
| Cambiar por -1 | Cuenta regresiva |
| Fijar a número aleatorio | Valor random |

**Anota qué descubriste**:
```



```

---

## Reflexión

**¿Cuál es la diferencia entre "fijar a" y "cambiar por"?**
```
(Tu respuesta aquí)
```

**¿Por qué necesitamos resetear a 0 al inicio del programa?**
```
(Tu respuesta aquí)
```

**¿Qué otros usos tienen las variables en programación?**
```
(Tu respuesta aquí)
```

---

## Aplicaciones Reales

Este patrón se usa en:
- Sistemas de puntuación en juegos
- Contadores de likes en redes sociales
- Carrito de compras (cantidad de productos)
- Estadísticas de aplicaciones

Las variables son fundamentales en TODA la programación.

---

## Recursos Relacionados

- [[../Teoria/01-Introduccion-Pensamiento-Computacional#Variables|Teoría: Variables]]
- [[../Teoria/02-Guia-Rapida-Scratch#Variables|Referencia: Bloques de Variables]]
- [[../Teoria/02-Guia-Rapida-Scratch#Patrón-5-Contador-de-Clicks|Patrón: Contador]]

---

## Siguiente Ejercicio

[[Ejercicio-06-Detector-Bordes|Ejercicio 06: Detector de Bordes]]

---

#ejercicio #intermedio #variables #eventos #operadores
