# Ejercicio 01: Saludo Personalizado

**Nivel**: Básico
**Tiempo estimado**: 15 minutos
**Conceptos**: Variables, Entrada/Salida, Secuencias

---

## Objetivo

Crear un programa que pregunte tu nombre y te salude de forma personalizada.

---

## Descripción

El gato de Scratch debe:
1. Preguntar "¿Cómo te llamas?"
2. Esperar la respuesta del usuario
3. Saludar usando el nombre que ingresó el usuario

**Ejemplo de ejecución**:
```
Gato: "¿Cómo te llamas?"
Usuario: [escribe "Ana"]
Gato: "¡Hola Ana! Bienvenido a Scratch"
```

---

## Requisitos

- [ ] El programa empieza al hacer clic en la bandera verde
- [ ] Hace la pregunta "¿Cómo te llamas?"
- [ ] Espera la respuesta del usuario
- [ ] Muestra un saludo personalizado que incluya el nombre
- [ ] El saludo se muestra por al menos 2 segundos

---

## Bloques que Necesitarás

**Categorías a usar**:
- Eventos (amarillo)
- Apariencia (morado)
- Sensores (rojo)
- Operadores (verde)

**Pista**: Busca el bloque de "preguntar" en Sensores y el bloque de "respuesta"

---

## Pistas Progresivas

### Pista 1 (Estructura General)
```
Al hacer clic en bandera verde
└─ [pregunta]
└─ [saludo con nombre]
```

### Pista 2 (Más Específico)
Necesitas:
1. Bloque de evento para empezar
2. Bloque "preguntar [texto] y esperar"
3. Bloque "decir [texto] por X segundos"
4. Combinar texto con el bloque "respuesta"

### Pista 3 (Casi Completo)
```
Al hacer clic en bandera verde
├─ Preguntar [¿Cómo te llamas?] y esperar
└─ Decir [unir "¡Hola " y respuesta] por 2 segundos
```

**¿Cómo unir texto?** Busca el bloque "unir" en Operadores (verde)

---

## Criterios de Éxito

Tu ejercicio está completo cuando:

- [ ] Funciona correctamente al presionar bandera verde
- [ ] Usa el nombre que escribiste en el saludo
- [ ] El mensaje es claro y amigable
- [ ] No hay errores al ejecutarlo múltiples veces

---

## Desafíos Extras (Opcional)

### Desafío 1: Más Conversación
Después del saludo, pregunta también:
- "¿Cuántos años tienes?"
- Responde: "¡Genial! [edad] años es una excelente edad para programar"

### Desafío 2: Validación Básica
Si el usuario no escribe nada (respuesta vacía), el gato dice:
"Parece que no me dijiste tu nombre, ¡qué misterioso!"

**Pista**: Usa un condicional (si/entonces) y el operador "=" para comparar respuesta con ""

### Desafío 3: Múltiples Preguntas
Crea una conversación completa:
1. Nombre
2. Edad
3. Color favorito
4. El gato responde con toda la información recopilada

---

## Reflexión

Después de completar el ejercicio, responde:

**¿Qué aprendiste?**
```
(Tu respuesta aquí)
```

**¿Qué fue lo más difícil?**
```
(Tu respuesta aquí)
```

**¿Cómo podrías mejorar este programa?**
```
(Tu respuesta aquí)
```

---

## Recursos Relacionados

- [[../Teoria/01-Introduccion-Pensamiento-Computacional#Variables|Teoría: Variables]]
- [[../Teoria/02-Guia-Rapida-Scratch#Sensores|Referencia: Bloques de Sensores]]
- [Tutorial Scratch: Getting Started](https://scratch.mit.edu/projects/editor/?tutorial=getStarted)

---

## Siguiente Ejercicio

Una vez completes este ejercicio: [[Ejercicio-02-Cuadrado-Perfecto|Ejercicio 02: Cuadrado Perfecto]]

---

#ejercicio #basico #variables #entrada-salida
