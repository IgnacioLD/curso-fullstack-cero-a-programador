# Proyecto 01: Calculadora de IMC

**Nivel**: Básico | **Tiempo**: 2 horas

---

## Descripción

Calculadora de Índice de Masa Corporal (IMC) que determina categoría de peso según OMS.

---

## Fórmula

**IMC = peso (kg) / altura² (m)**

**Categorías OMS**:
- < 18.5: Bajo peso
- 18.5 - 24.9: Normal
- 25.0 - 29.9: Sobrepeso
- 30.0 - 34.9: Obesidad Grado 1
- 35.0 - 39.9: Obesidad Grado 2
- >= 40: Obesidad Grado 3

---

## Especificaciones

**Input**:
```
Peso (kg): 70
Altura (m): 1.75
```

**Output**:
```
Tu IMC es: 22.86
Categoría: Peso normal
```

---

## Estructura Base

```c
#include <stdio.h>

int main(void) {
    float peso, altura, imc;

    // Input
    printf("Peso (kg): ");
    scanf("%f", &peso);

    printf("Altura (m): ");
    scanf("%f", &altura);

    // Cálculo
    imc = peso / (altura * altura);

    // Mostrar IMC
    printf("\nTu IMC es: %.2f\n", imc);

    // Determinar categoría con if/else
    if (imc < 18.5) {
        printf("Categoría: Bajo peso\n");
    } else if (imc < 25.0) {
        printf("Categoría: Peso normal\n");
    }
    // Continuar con otras categorías...

    return 0;
}
```

---

## Validaciones

- [ ] Peso > 0
- [ ] Altura > 0 y < 3.0 (razonable)
- [ ] Manejar inputs inválidos

---

## Mejoras Opcionales

1. **Consejo**: Da recomendación según categoría
2. **Peso ideal**: Calcula rango de peso saludable
3. **Historial**: Permite múltiples cálculos
4. **Unidades**: Opción para libras/pies

---

#proyecto #basico #imc #salud
