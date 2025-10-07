# Ejercicios - Semana 05: Hardware Teoría

---

## Ejercicios Conceptuales

Esta semana NO hay programación, solo comprensión de conceptos.

### Básicos

1. **Identificar Componentes**: Diagrama de computadora, identificar partes
2. **Binario**: Convertir números decimales a binario y viceversa
3. **Unidades**: Convertir entre KB, MB, GB, TB
4. **RAM vs Almacenamiento**: Explicar diferencias

### Intermedios

5. **Especificaciones**: Analizar specs de laptop, explicar cada componente
6. **Fetch-Decode-Execute**: Trazar ejecución de instrucción simple
7. **Hexadecimal**: Convertir entre binario, decimal, hex
8. **Comparar CPUs**: Investigar Intel vs AMD vs ARM

### Avanzados

9. **Optimización**: Explicar por qué C es más rápido que Python
10. **Bottlenecks**: Identificar cuellos de botella en sistemas

---

## Actividades Prácticas

### 1. Investigación de Tu Computadora

Descubre especificaciones de tu máquina:

**Linux**:
```bash
lscpu              # CPU info
free -h            # RAM
lsblk              # Discos
```

**macOS**:
```bash
sysctl -n machdep.cpu.brand_string  # CPU
system_profiler SPHardwareDataType  # Todo
```

**Windows**:
- Task Manager → Performance
- System Information

### 2. Benchmark Simple

Comparar velocidad SSD vs HDD (si tienes ambos):

**Linux/macOS**:
```bash
time dd if=/dev/zero of=test.file bs=1M count=1000
```

---

#hardware #ejercicios #conceptual
