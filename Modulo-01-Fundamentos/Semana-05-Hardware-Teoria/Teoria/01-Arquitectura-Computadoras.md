# Arquitectura de Computadoras

> **Semana 5 - Módulo 1: Fundamentos**
> **Cómo funciona una computadora por dentro**

---

## Objetivos

- Entender componentes principales de una computadora
- Comprender CPU, RAM, almacenamiento
- Aprender sistema binario
- Conocer arquitectura Von Neumann
- Entender diferencia hardware vs software

---

## Componentes Principales

### 1. CPU (Procesador)

**Función**: Cerebro de la computadora, ejecuta instrucciones

**Componentes**:
- **ALU** (Arithmetic Logic Unit): Operaciones matemáticas y lógicas
- **Control Unit**: Coordina operaciones
- **Registers**: Memoria ultrarrápida dentro CPU
- **Cache**: Memoria muy rápida cerca de CPU

**Especificaciones**:
- **Cores**: Núcleos de procesamiento (2, 4, 8, 16...)
- **Clock Speed**: GHz (3.2 GHz = 3,200,000,000 ciclos/segundo)
- **Cache**: L1, L2, L3 (más cerca = más rápido)

**Marcas**: Intel, AMD, Apple (M-series), ARM

---

### 2. RAM (Memoria)

**Función**: Almacenamiento temporal mientras computadora está encendida

**Características**:
- **Volátil**: Se borra al apagar
- **Rápida**: Acceso en nanosegundos
- **Limitada**: 8GB, 16GB, 32GB típico

**Tipos**:
- DDR4, DDR5 (actuales)
- LPDDR (laptops, móviles - bajo consumo)

**Analogía**: Mesa de trabajo
- Más RAM = más proyectos abiertos simultáneamente
- Poca RAM = computadora lenta (swap a disco)

---

### 3. Almacenamiento

**Persistente**: No se borra al apagar

**HDD (Hard Disk Drive)**:
- Discos magnéticos giratorios
- Lento (~100 MB/s)
- Barato
- Alta capacidad (1-8 TB)

**SSD (Solid State Drive)**:
- Sin partes móviles (chips)
- Rápido (500-7000 MB/s)
- Más caro
- Menor capacidad por precio

**NVMe**:
- SSD conectado directamente a PCIe
- Ultrarrápido (hasta 7000 MB/s)
- Estándar actual en laptops modernas

---

### 4. Motherboard (Placa Base)

**Función**: Conecta todos los componentes

**Incluye**:
- Socket para CPU
- Slots para RAM
- Conectores para almacenamiento
- PCIe slots (GPU, expansión)
- Puertos (USB, HDMI, Ethernet, audio)
- BIOS/UEFI

---

### 5. GPU (Tarjeta Gráfica)

**Función**: Procesamiento de gráficos

**Tipos**:
- **Integrada**: Dentro de CPU (Intel UHD, AMD Radeon)
- **Dedicada**: Tarjeta separada (NVIDIA, AMD)

**Uso**:
- Gaming
- Edición video
- Machine Learning/IA
- Renderizado 3D

---

### 6. PSU (Fuente de Poder)

**Función**: Convertir AC (pared) a DC (componentes)

**Especificaciones**:
- Wattage (500W, 750W, etc.)
- Efficiency (80+ Bronze, Gold, Platinum)

---

## Arquitectura Von Neumann

**Modelo básico** (1945):

```
┌─────────┐
│   CPU   │
└────┬────┘
     │
┌────┴────┐
│ Memory  │ (programa + datos)
└────┬────┘
     │
┌────┴────┐
│  I/O    │ (input/output)
└─────────┘
```

**Características**:
- Programa almacenado en memoria
- Misma memoria para datos e instrucciones
- Ejecución secuencial

---

## Sistema Binario

### Bits y Bytes

**Bit**: Unidad mínima (0 o 1)
**Byte**: 8 bits

```
1 Byte = 8 bits
1 KB = 1,024 bytes
1 MB = 1,024 KB
1 GB = 1,024 MB
1 TB = 1,024 GB
```

### Representación

**Decimal a Binario**:
```
13 en decimal = 1101 en binario

8  4  2  1
1  1  0  1
8 + 4 + 0 + 1 = 13
```

**Hexadecimal** (base 16):
- 0-9, A-F
- Usado en programación (colores, direcciones memoria)
- `0xFF = 255 decimal = 11111111 binario`

---

## Ciclo de Ejecución (Fetch-Decode-Execute)

```
1. FETCH: Traer instrucción de memoria
     ↓
2. DECODE: Decodificar qué hacer
     ↓
3. EXECUTE: Ejecutar operación
     ↓
4. STORE: Guardar resultado
     ↓
   (Repetir)
```

**Ejemplo**:
```c
int a = 5 + 3;

1. Fetch: Leer instrucción "a = 5 + 3"
2. Decode: Identificar suma, destino 'a'
3. Execute: ALU calcula 5 + 3 = 8
4. Store: Guardar 8 en ubicación de 'a'
```

---

## Hardware vs Software

**Hardware**: Físico, tangible
- CPU, RAM, disco, teclado, monitor

**Software**: Instrucciones, programas
- Sistema operativo, aplicaciones, juegos

**Firmware**: Software en hardware
- BIOS/UEFI, drivers

**Relación**:
```
Software (C, Python)
    ↓ compilador/intérprete
Assembly (bajo nivel)
    ↓ ensamblador
Machine Code (binario)
    ↓
Hardware (CPU ejecuta)
```

---

## Niveles de Abstracción

```
Alto nivel:    Python, JavaScript
  ↓
Medio nivel:   C, Rust
  ↓
Bajo nivel:    Assembly
  ↓
Machine Code:  01001010...
  ↓
Hardware:      Transistores
```

**Por qué importa**:
- C está cerca del hardware (eficiente)
- Python está lejos (fácil pero más lento)

---

## Recursos

- [How Computers Work](https://www.youtube.com/watch?v=QZwneRb-zqA) - Video explicativo
- [CPU Simulator](https://schweigi.github.io/assembler-simulator/) - Visualizar ejecución
- [[../Ejercicios/README|Ejercicios Conceptuales]]

---

#hardware #arquitectura #cpu #memoria #binario
