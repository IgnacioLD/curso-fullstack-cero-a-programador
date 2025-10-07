# Kit Hardware ESP32: Guía Completa de Compra y Setup

## 📦 Índice
- [¿Por qué ESP32?](#por-qué-esp32)
- [Kit Básico](#kit-básico-30-40)
- [Kit Intermedio](#kit-intermedio-opcional-20)
- [Kit Avanzado](#kit-avanzado-proyectos-especiales-30)
- [Dónde Comprar](#dónde-comprar)
- [Setup Software](#setup-software)
- [Primer Proyecto](#primer-proyecto-blink-led)
- [Troubleshooting](#troubleshooting)
- [Cuidado del Hardware](#cuidado-del-hardware)

---

## 🤔 ¿Por qué ESP32?

### Ventajas del ESP32

| Característica | Beneficio |
|----------------|-----------|
| **WiFi + Bluetooth integrados** | Proyectos IoT sin hardware extra |
| **Dual-core** | Más potente que Arduino Uno |
| **Bajo coste** | 5-8€ por unidad |
| **Muchos GPIO** | 30+ pins disponibles |
| **Compatible Arduino** | Fácil de programar |
| **Comunidad enorme** | Tutoriales y soporte |
| **Low power** | Proyectos con batería |

### ESP32 vs. Arduino Uno

| Feature | ESP32 | Arduino Uno |
|---------|-------|-------------|
| Processor | Dual-core 240MHz | Single-core 16MHz |
| RAM | 520KB | 2KB |
| Flash | 4MB | 32KB |
| WiFi | ✅ Built-in | ❌ Necesita módulo |
| Bluetooth | ✅ Built-in | ❌ Necesita módulo |
| Precio | ~6€ | ~20€ |
| Voltaje | 3.3V | 5V |

**Conclusión**: ESP32 es mucho más potente y económico.

---

## 🛒 Kit Básico (~30-40€)

Este kit te permite hacer el 80% de los proyectos de la Fase 3.

### Lista de Componentes

| Cantidad | Componente | Precio aprox. | Uso |
|----------|------------|---------------|-----|
| 1 | ESP32 DevKit V1 (30 pines) | 6-8€ | Microcontrolador principal |
| 1 | Protoboard 830 puntos | 3€ | Montar circuitos sin soldar |
| 1 | Set cables Dupont (M-M, M-F, F-F) | 3€ | Conectar componentes |
| 10 | LEDs (rojo, amarillo, verde, azul, blanco) | 1€ | Salidas visuales |
| 10 | Resistencias 220Ω (1/4W) | 0.50€ | Limitar corriente LEDs |
| 10 | Resistencias 10kΩ (1/4W) | 0.50€ | Pull-up/pull-down |
| 5 | Pulsadores (push buttons) | 1€ | Entradas digitales |
| 1 | Sensor DHT11 o DHT22 | 3-5€ | Temperatura y humedad |
| 1 | Servo SG90 (micro servo) | 3€ | Motor con control posición |
| 1 | Cable micro-USB | 2€ | Programar y alimentar ESP32 |
| | | |
| | **TOTAL** | **~30-40€** | |

### Desglose por Categoría

#### Microcontrolador
- **ESP32 DevKit V1** (30 pines)
  - Chip: ESP32-WROOM-32
  - Dual-core Xtensa 32-bit LX6
  - WiFi 802.11 b/g/n
  - Bluetooth 4.2
  - 30 GPIO pins
  - USB-to-Serial integrado (CP2102 o CH340)

#### Protoboard
- **830 puntos** (recomendado)
  - Medidas: ~16.5 x 5.5 cm
  - Filas centrales: 63 columnas x 2 bloques
  - Buses laterales: + y -
  - Sin soldadura necesaria

#### Cables
- **Dupont cables** (pack de 120-140 cables):
  - 40x Male-Male (M-M)
  - 40x Male-Female (M-F)
  - 40x Female-Female (F-F)
  - Longitud: ~20cm
  - Colores variados (ayuda a organizar)

#### LEDs
- **5 colores** x 2 unidades cada uno:
  - Rojo (proyectos de alerta)
  - Amarillo (warnings)
  - Verde (OK status)
  - Azul (WiFi status)
  - Blanco (iluminación)
- Especificaciones típicas:
  - 5mm diffused
  - Forward voltage: 2-3.2V
  - Forward current: 20mA

#### Resistencias
- **220Ω** (10 unidades):
  - Para LEDs (limitar corriente)
  - Código colores: Rojo-Rojo-Marrón
- **10kΩ** (10 unidades):
  - Pull-up/pull-down para botones
  - Código colores: Marrón-Negro-Naranja

#### Sensores
- **DHT11** (económico) o **DHT22** (mejor precisión):

  | Spec | DHT11 | DHT22 |
  |------|-------|-------|
  | Temperatura | 0-50°C ±2°C | -40-80°C ±0.5°C |
  | Humedad | 20-90% ±5% | 0-100% ±2% |
  | Precio | ~2-3€ | ~4-5€ |
  | Sampling | 1Hz | 0.5Hz |

  **Recomendación**: DHT11 es suficiente para aprender.

#### Actuadores
- **Servo SG90**:
  - Micro servo 9g
  - Torque: 1.8 kg/cm
  - Rango: 0-180°
  - Voltaje: 4.8-6V
  - Perfecto para principiantes

---

## 📦 Kit Intermedio (Opcional +20€)

Si quieres ampliar tus proyectos:

| Cantidad | Componente | Precio | Proyectos |
|----------|------------|--------|-----------|
| 1 | Sensor ultrasónico HC-SR04 | 2€ | Medir distancia, parking sensor |
| 1 | Módulo relé 1 canal (5V) | 2€ | Controlar AC (lámpara, ventilador) |
| 1 | LED RGB (cátodo común) | 2€ | Mezcla de colores |
| 1 | Display OLED 0.96" I2C | 5€ | Mostrar texto/gráficos |
| 1 | Sensor de luz LDR + resistencias | 1€ | Detectar luz ambiental |
| 1 | Buzzer piezo | 1€ | Sonidos, alarmas |
| 5 | Resistencias 330Ω | 0.50€ | LEDs RGB |
| 5 | Resistencias 1kΩ | 0.50€ | Divisores de voltaje |
| 1 | Potenciómetro 10kΩ | 1€ | Entrada analógica variable |
| 1 | Breadboard power supply (3.3V/5V) | 2€ | Alimentar protoboard |
| | | |
| | **TOTAL** | **~20€** | |

---

## 🚀 Kit Avanzado (Proyectos Especiales +30€)

Para proyectos más complejos:

| Componente | Precio | Uso |
|------------|--------|-----|
| ESP32-CAM | 7€ | Visión por computadora, streaming |
| Motor DC + L298N driver | 5€ | Robots, movimiento |
| Sensor temperatura DS18B20 | 3€ | Temperatura precisa (waterproof) |
| Matrix LED 8x8 MAX7219 | 4€ | Displays animados |
| Sensor PIR HC-SR501 | 2€ | Detección movimiento |
| Neopixels WS2812B (strip 1m) | 8€ | LEDs direccionables RGB |
| RTC DS3231 | 3€ | Reloj en tiempo real |
| Sensor humedad tierra | 2€ | Proyectos plantas |

---

## 🛍️ Dónde Comprar

### España / Europa

#### Amazon España
- **URL**: https://www.amazon.es/
- **Pros**:
  - Envío rápido (1-2 días con Prime)
  - Devoluciones fáciles
  - Descripciones en español
- **Contras**:
  - Algo más caro que AliExpress
- **Recomendación**: Busca "ESP32 DevKit kit" - hay kits completos por 25-35€

#### AliExpress
- **URL**: https://es.aliexpress.com/
- **Pros**:
  - Muy económico
  - Gran variedad
  - Kits completos baratos
- **Contras**:
  - Envío lento (3-6 semanas)
  - Descripciones a veces confusas
- **Recomendación**: Compra con antelación, busca vendedores con buenas reviews

#### Tiendas Especializadas España

**BricoGeek**
- URL: https://tienda.bricogeek.com/
- Español, envío rápido, buen soporte

**Electan**
- URL: https://www.electan.com/
- Componentes electrónicos, envío España

**Cooking Hacks**
- URL: https://www.cooking-hacks.com/
- Kits educativos

#### Internacional (envío a España)

**SparkFun**
- URL: https://www.sparkfun.com/
- Componentes de calidad, buenos tutoriales
- Envío internacional disponible

**Adafruit**
- URL: https://www.adafruit.com/
- Componentes premium, excelentes tutoriales
- Envío internacional

### Kits Pre-armados Recomendados

Busca en Amazon/AliExpress:
- "ESP32 Starter Kit"
- "ESP32 Development Kit"
- "ESP32 Learning Kit"

**Ejemplo de kit completo (~30€)**:
- ESP32 x1
- Protoboard
- Cables
- LEDs y resistencias
- Sensores (DHT, ultrasónico)
- Servo
- Botones
- Buzzer
- (A veces incluye caja organizadora)

---

## 💻 Setup Software

### Opción 1: Arduino IDE (Recomendado para principiantes)

#### 1. Instalar Arduino IDE

**Windows/Mac/Linux**:
1. Descarga de: https://www.arduino.cc/en/software
2. Instala (siguiente, siguiente...)
3. Abre Arduino IDE

#### 2. Instalar Soporte ESP32

1. Arduino IDE → Preferencias (Ctrl+,)
2. En "Gestor de URLs Adicionales de Tarjetas", añade:
   ```
   https://dl.espressif.com/dl/package_esp32_index.json
   ```
3. OK
4. Herramientas → Placa → Gestor de Tarjetas
5. Busca "esp32"
6. Instala "esp32 by Espressif Systems" (última versión)

#### 3. Seleccionar Placa ESP32

1. Herramientas → Placa → ESP32 Arduino → **"ESP32 Dev Module"**
2. Herramientas → Puerto → Selecciona el puerto COM/tty.usb que aparezca

#### 4. Instalar Drivers USB (si es necesario)

Si el ESP32 no aparece en Puertos:

**CP2102 Driver**:
- Windows: https://www.silabs.com/developers/usb-to-uart-bridge-vcp-drivers
- Mac: Incluido en sistema
- Linux: `sudo apt-get install cp210x`

**CH340 Driver**:
- Windows: http://www.wch-ic.com/downloads/CH341SER_EXE.html
- Mac: https://github.com/adrianmihalko/ch340g-ch34g-ch34x-mac-os-x-driver
- Linux: Kernel incluye driver

**Verificar**:
1. Conecta ESP32 con cable USB
2. LED rojo en ESP32 debería encender
3. En Arduino IDE → Herramientas → Puerto → Debería aparecer COM# o /dev/ttyUSB#

---

### Opción 2: PlatformIO (Avanzado)

**Ventajas**:
- Mejor gestión de librerías
- Proyectos organizados
- Integración con VS Code
- Debugging avanzado

**Setup**:
1. Instala VS Code
2. Extensión: "PlatformIO IDE"
3. PlatformIO → New Project
4. Board: "Espressif ESP32 Dev Module"
5. Framework: "Arduino"

---

## 🔌 Conexiones Básicas

### Pinout ESP32 DevKit V1

```
                     ┌─────────┐
                     │   USB   │
                     └─────────┘
    EN              ┌───────────┐              D23
    VP (ADC)        │           │              D22
    VN (ADC)        │           │              TX0
    D34 (Input)     │           │              RX0
    D35 (Input)     │           │              D21
    D32             │           │              GND
    D33             │   ESP32   │              D19
    D25             │           │              D18
    D26             │           │              D5
    D27             │           │              D17
    D14             │           │              D16
    D12             │           │              D4
    GND             │           │              D0
    D13             │           │              D2
    D9              │           │              D15
    D10             │           │              3V3
    D11             │           │              GND
    VIN             │           │              D8
    5V              └───────────┘              D7
                                               D6
```

### Leyenda Pins

- **GPIO**: Pines programables (D2, D4, D5, etc.)
- **GND**: Tierra (Ground) - 0V
- **3V3**: Salida 3.3V (max 500mA)
- **VIN**: Entrada voltaje 5-12V
- **EN**: Enable (reset si conecta a GND)
- **ADC**: Analog-to-Digital Converter
- **TX/RX**: Serial communication

### ⚠️ Precauciones

1. **ESP32 es 3.3V**, NO 5V
2. Pins ADC1 (32-39) no funcionan con WiFi activo
3. Pins 6, 7, 8, 9, 10, 11 → FLASH (no usar)
4. Pins solo INPUT: 34, 35, 36, 39

---

## 💡 Primer Proyecto: Blink LED

### Circuito

```
ESP32          Protoboard
┌─────┐
│     │
│  D2 ├──────────┐
│     │          │
│ GND ├───┐      │
│     │   │      │
└─────┘   │      │
          │      │
          │    ┌─┴─┐
          │    │LED│ (pata larga a D2)
          │    └─┬─┘
          │      │
          │   ┌──┴──┐
          │   │ 220Ω│ Resistencia
          │   └──┬──┘
          │      │
          └──────┘ GND
```

### Código

```cpp
// Blink LED - Tu primer programa ESP32

// Define el pin del LED
const int LED_PIN = 2;  // GPIO 2 (built-in LED en muchos ESP32)

void setup() {
  // Configura el pin como salida
  pinMode(LED_PIN, OUTPUT);

  // Inicia comunicación serial (para debugging)
  Serial.begin(115200);
  Serial.println("ESP32 Blink Started!");
}

void loop() {
  // Enciende LED
  digitalWrite(LED_PIN, HIGH);
  Serial.println("LED ON");
  delay(1000);  // Espera 1 segundo

  // Apaga LED
  digitalWrite(LED_PIN, LOW);
  Serial.println("LED OFF");
  delay(1000);  // Espera 1 segundo
}
```

### Pasos para Subir el Código

1. Conecta ESP32 a USB
2. Copia el código en Arduino IDE
3. Herramientas → Placa → ESP32 Dev Module
4. Herramientas → Puerto → Selecciona puerto
5. Click en **→** (Upload)
6. Espera "Hard resetting via RTS pin..."
7. LED debería parpadear cada 1 segundo

### Si no sube el código:

1. Mantén presionado botón **BOOT** en ESP32
2. Click Upload
3. Cuando dice "Connecting...", suelta BOOT

---

## 🛠️ Troubleshooting

### Problema 1: ESP32 no aparece en puertos

**Soluciones**:
1. Instala drivers USB (CP2102 o CH340)
2. Prueba otro cable USB (algunos son solo carga)
3. Prueba otro puerto USB en PC
4. Reinicia PC después de instalar drivers

### Problema 2: "Failed to connect"

**Soluciones**:
1. Presiona y mantén botón BOOT al subir
2. Reduce velocidad upload: Herramientas → Upload Speed → 115200
3. Verifica puerto seleccionado
4. Desconecta otros dispositivos USB

### Problema 3: Código sube pero no funciona

**Soluciones**:
1. Abre Serial Monitor (Herramientas → Monitor Serie)
2. Configura baud rate a 115200
3. Presiona botón EN (reset) en ESP32
4. Lee mensajes de error

### Problema 4: WiFi no conecta

**Soluciones**:
1. Verifica SSID y password
2. Asegúrate WiFi es 2.4GHz (no 5GHz)
3. Acércate al router
4. Prueba hotspot de móvil

### Problema 5: LED no enciende

**Soluciones**:
1. Verifica polaridad LED (pata larga a GPIO)
2. Verifica resistencia (220Ω)
3. Prueba otro pin GPIO
4. Prueba LED built-in (GPIO 2)
5. Verifica conexión GND

---

## 📏 Cuidado del Hardware

### Buenas Prácticas

1. **Desconecta antes de modificar circuito**
   - Siempre desconecta USB antes de cambiar cables

2. **Polaridad correcta**
   - LEDs: pata larga = +
   - Electrolíticos: marca - en negativo

3. **No corto circuitos**
   - Nunca conectes 3V3 directo a GND
   - Usa resistencias con LEDs

4. **Voltaje correcto**
   - ESP32 = 3.3V
   - Si usas 5V, usa divisor de voltaje

5. **Organización**
   - Usa colores consistentes:
     - Rojo = VCC/3V3
     - Negro = GND
     - Otros = señales

### Guardar Componentes

- **Caja organizadora** con compartimentos
- **Bolsas antiestáticas** para ESP32
- **Etiqueta** resistencias por valor
- **Envuelve** LEDs para no doblar patas

### Vida Útil

| Componente | Durabilidad |
|------------|-------------|
| ESP32 | Años (si no quemas) |
| Protoboard | Años (500+ inserciones) |
| Cables Dupont | Años |
| LEDs | 50,000+ horas |
| Resistencias | Indefinido |
| Sensores | 2-5 años (DHT11) |
| Servo | 1-2 años uso intensivo |

---

## 📚 Recursos para Aprender

### Tutoriales Básicos

1. **Random Nerd Tutorials**:
   - [ESP32 Getting Started](https://randomnerdtutorials.com/getting-started-with-esp32/)
   - [ESP32 Pinout Reference](https://randomnerdtutorials.com/esp32-pinout-reference-gpios/)

2. **YouTube**:
   - Andreas Spiess - "ESP32 Tutorial Series"
   - DroneBot Workshop - "ESP32 for Beginners"

### Proyectos Ejemplo

- Blink LED
- Button input
- PWM LED (fade)
- DHT11 temperature
- Servo control
- Web server
- WiFi scanner
- MQTT client

---

## ✅ Checklist de Compra

Imprime o guarda esto cuando vayas a comprar:

### Kit Mínimo (~30€)
- [ ] 1x ESP32 DevKit V1 (30 pines)
- [ ] 1x Protoboard 830 puntos
- [ ] 1x Set cables Dupont (120 pcs: M-M, M-F, F-F)
- [ ] 10x LEDs (mix colores)
- [ ] 10x Resistencias 220Ω
- [ ] 10x Resistencias 10kΩ
- [ ] 5x Pulsadores
- [ ] 1x Sensor DHT11 o DHT22
- [ ] 1x Servo SG90
- [ ] 1x Cable micro-USB

### Extras Recomendados (+10€)
- [ ] Sensor ultrasónico HC-SR04
- [ ] Módulo relé 1 canal
- [ ] LED RGB
- [ ] Display OLED 0.96"
- [ ] Caja organizadora componentes

### Software (Gratis)
- [ ] Arduino IDE instalado
- [ ] Soporte ESP32 instalado
- [ ] Drivers USB (CP2102 o CH340)
- [ ] Primer Blink funcionando

---

## 🎓 Próximos Pasos

Después de recibir tu kit:

1. ✅ Instala Arduino IDE y drivers
2. ✅ Sube Blink a ESP32
3. ✅ Prueba Serial Monitor
4. ✅ Conecta un LED externo
5. ✅ Prueba un botón
6. ✅ Lee sensor DHT11
7. ✅ Mueve el servo
8. ✅ Conecta a WiFi
9. ✅ Crea un web server simple
10. ✅ Empieza proyectos de Fase 3 del currículum

---

## 💬 Comunidad y Soporte

### Si tienes problemas:

1. **Documentación oficial**: https://docs.espressif.com/
2. **Random Nerd Tutorials**: https://randomnerdtutorials.com/
3. **Arduino Forum - ESP32**: https://forum.arduino.cc/
4. **ESP32 Forum**: https://www.esp32.com/
5. **Reddit r/esp32**: https://reddit.com/r/esp32
6. **Stack Overflow** con tag [esp32]

---

## 📝 Notas Finales

### ¿Vale la pena?

**Absolutamente SÍ**:
- Inversión pequeña (~30-50€)
- Aprendizaje enorme (hardware + software)
- Proyectos tangibles y divertidos
- Diferenciador en portfolio
- IoT es campo en crecimiento

### ¿Es necesario para ser Full Stack Developer?

**No es obligatorio**, pero:
- Te hace destacar
- Entiendes abstracción mejor
- Proyectos más creativos
- Descanso mental de web puro

### Alternativas

Si no quieres comprar hardware:
- **Simuladores**: Wokwi (https://wokwi.com/) - ESP32 simulator online
- **Skip Fase 3**: Salta a Fase 4 Full Stack directamente
- **Arduino virtual**: Tinkercad Circuits

Pero realmente, **30€ bien gastados** vale mucho la pena.

---

**¡Disfruta construyendo! 🔧🚀**

**Última actualización**: 2025-10-01
