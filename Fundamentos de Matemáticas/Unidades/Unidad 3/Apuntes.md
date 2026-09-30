# Unidad 3 — Ecuaciones e Inecuaciones
**Fundamentos de Matemáticas · CFBD242-A1 · Atilano Arrieta Vivero**

---

## 🧭 Mapa de Contenidos

```
Ecuaciones
├── Ecuaciones lineales (una variable, sistemas)
├── Ecuaciones cuadráticas
│   ├── Factorización
│   ├── Completar el cuadrado
│   └── Fórmula cuadrática (−b ± √discriminante / 2a)
└── Ecuaciones con valor absoluto

Inecuaciones
├── Inecuaciones lineales
├── Inecuaciones cuadráticas
├── Representación en recta numérica
└── Inecuaciones con valor absoluto
```

---

## 1. Ecuaciones Lineales

### 1.1 Definición y Propiedades

Una **ecuación lineal** en una variable tiene la forma `ax + b = 0` (con `a ≠ 0`).

**Propiedades de igualdad** usadas al despejar:
- **Adición/Sustracción:** Si `a = b`, entonces `a + c = b + c`
- **Multiplicación/División:** Si `a = b` y `c ≠ 0`, entonces `ac = bc`

### 1.2 Procedimiento General

```
Paso 1: Eliminar paréntesis (distribución)
Paso 2: Eliminar fracciones (multiplicar por MCD)
Paso 3: Agrupar términos con variable a un lado
Paso 4: Agrupar constantes al otro lado
Paso 5: Dividir por el coeficiente de la variable
Paso 6: Verificar sustituyendo en la ecuación original
```

**Ejemplo 1 — Básico:**
```
3x − 7 = 2x + 5
3x − 2x = 5 + 7
x = 12

Verificación: 3(12) − 7 = 36 − 7 = 29  |  2(12) + 5 = 24 + 5 = 29 ✅
```

**Ejemplo 2 — Con fracciones:**
```
x/2 + 1/3 = 5/6

MCD(2,3,6) = 6 → multiplicar todo por 6:
3x + 2 = 5
3x = 3
x = 1

Verificación: 1/2 + 1/3 = 3/6 + 2/6 = 5/6 ✅
```

**Ejemplo 3 — Con paréntesis:**
```
2(3x − 1) − (x + 4) = 3(x − 2)
6x − 2 − x − 4 = 3x − 6
5x − 6 = 3x − 6
2x = 0
x = 0

Verificación: 2(−1) − (4) = −2−4 = −6  |  3(−2) = −6 ✅
```

### 1.3 Ecuaciones con Solución Especial

| Tipo | Ejemplo | Solución |
|:---|:---|:---|
| Solución única | `2x + 1 = 5` | `x = 2` |
| Sin solución (contradición) | `x + 1 = x + 2` | `∅` (1 ≠ 2) |
| Infinitas soluciones (identidad) | `2(x+1) = 2x+2` | Todo ℝ |

---

## 2. Ecuaciones Cuadráticas

### 2.1 Forma Estándar

`ax² + bx + c = 0`, con `a ≠ 0`

### 2.2 Método 1: Factorización

Aplicar casos de factorización y usar la **propiedad del producto cero**: si `A·B = 0`, entonces `A = 0` o `B = 0`.

```
x² − 5x + 6 = 0
(x − 2)(x − 3) = 0
→ x − 2 = 0  →  x = 2
→ x − 3 = 0  →  x = 3
```

```
2x² + x − 3 = 0
(2x + 3)(x − 1) = 0
→ 2x + 3 = 0  →  x = −3/2
→ x − 1 = 0   →  x = 1
```

### 2.3 Método 2: Completar el Cuadrado

**Procedimiento:**
1. Pasar la constante `c` al lado derecho.
2. Dividir todo por `a` (si `a ≠ 1`).
3. Agregar `(b/2a)²` a ambos lados.
4. El lado izquierdo es `(x + b/2a)²`.
5. Sacar raíz cuadrada y despejar `x`.

```
x² + 6x + 5 = 0
x² + 6x = −5
x² + 6x + 9 = −5 + 9    ← agregar (6/2)² = 9
(x + 3)² = 4
x + 3 = ±2
x = −3 + 2 = −1   o   x = −3 − 2 = −5
```

### 2.4 Método 3: Fórmula Cuadrática (Chicharronera)

$$x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}$$

> Esta fórmula funciona para **cualquier** ecuación cuadrática. Es el método más universal.

**Ejemplo completo paso a paso:**
```
2x² − 7x + 3 = 0

a = 2,  b = −7,  c = 3

Discriminante: Δ = b² − 4ac = (−7)² − 4(2)(3) = 49 − 24 = 25

x = (7 ± √25) / (2·2)
x = (7 ± 5) / 4

x₁ = (7 + 5)/4 = 12/4 = 3
x₂ = (7 − 5)/4 = 2/4 = 1/2
```

**Verificación:**
```
Para x=3:  2(9) − 7(3) + 3 = 18 − 21 + 3 = 0 ✅
Para x=½: 2(¼) − 7(½) + 3 = ½ − 7/2 + 3 = 0 ✅
```

### 2.5 El Discriminante — Naturaleza de las Raíces

| Valor de `Δ = b² − 4ac` | Tipo de raíces | Cantidad |
|:---:|:---|:---:|
| `Δ > 0` | Reales distintas | 2 |
| `Δ = 0` | Real doble (repetida) | 1 |
| `Δ < 0` | Complejas (imaginarias) | 0 reales |

```
Δ = 49 − 24 = 25 > 0 → 2 raíces reales distintas (ejemplo anterior)

x² + 2x + 1 = 0
Δ = 4 − 4 = 0 → raíz doble: x = −1

x² + x + 1 = 0
Δ = 1 − 4 = −3 < 0 → no hay raíces reales
```

### 2.6 Relaciones de Vieta (Raíces y Coeficientes)

Para `ax² + bx + c = 0` con raíces `x₁` y `x₂`:
- **Suma:** `x₁ + x₂ = −b/a`
- **Producto:** `x₁ · x₂ = c/a`

> Útil para verificar raíces rápidamente sin calcular.

```
2x² − 7x + 3 = 0  → x₁=3, x₂=½
Suma: 3 + ½ = 7/2 = −(−7)/2 ✅
Producto: 3 · ½ = 3/2 = 3/2 ✅
```

---

## 3. Ecuaciones con Valor Absoluto

### 3.1 Definición

`|x| = a` significa la **distancia** de `x` al origen en la recta numérica.

`|x| = a  →  x = a  o  x = −a` (con `a ≥ 0`)

### 3.2 Procedimiento

```
|2x − 3| = 7

Caso 1: 2x − 3 = 7   →  2x = 10  →  x = 5
Caso 2: 2x − 3 = −7  →  2x = −4  →  x = −2

Solución: {−2, 5}
```

```
|x + 1| = −3  →  Sin solución (el valor absoluto nunca es negativo)
```

```
|3x + 1| = |x − 5|

Caso 1: 3x + 1 = x − 5   →  2x = −6  →  x = −3
Caso 2: 3x + 1 = −(x−5)  →  3x + 1 = −x + 5  →  4x = 4  →  x = 1
```

---

## 4. Inecuaciones

### 4.1 Propiedades de las Desigualdades

| Operación | Regla | Ejemplo |
|:---|:---|:---|
| Suma/resta | El sentido no cambia | `x < 3  →  x+2 < 5` |
| Mult./div. por positivo | El sentido no cambia | `2x < 6  →  x < 3` |
| **Mult./div. por negativo** | **El sentido SE INVIERTE** ⚠️ | `−x < 3  →  x > −3` |

### 4.2 Inecuaciones Lineales

```
2x − 5 > 3
2x > 8
x > 4

Notación de intervalo: (4, +∞)
Recta numérica: ──────○══════→
                      4
```

```
−3x + 1 ≤ 7
−3x ≤ 6
x ≥ −2    ← signo invertido por dividir entre −3

Notación de intervalo: [−2, +∞)
Recta numérica: ──────●══════→
                     −2
```

### 4.3 Inecuaciones Cuadráticas

**Procedimiento:**
1. Pasar todo a un lado: `ax² + bx + c ≷ 0`
2. Encontrar raíces (igualar a 0).
3. Trazar diagrama de signos con las raíces como puntos de división.
4. Determinar en qué intervalos la parábola está arriba/abajo del eje x.

```
x² − 5x + 6 > 0
Raíces: x = 2, x = 3
La parábola abre hacia arriba (a=1 > 0)
```

```
Diagrama de signos:
      +      −      +
───────○──────○────────→
      2       3

La expresión es POSITIVA (> 0) en: (−∞, 2) ∪ (3, +∞)
La expresión es NEGATIVA (< 0) en: (2, 3)
```

```
x² − 5x + 6 < 0  →  x ∈ (2, 3)
x² − 5x + 6 > 0  →  x ∈ (−∞, 2) ∪ (3, +∞)
x² − 5x + 6 ≥ 0  →  x ∈ (−∞, 2] ∪ [3, +∞)
```

**Regla visual para parábola `a > 0`:**
- La parábola tiene forma de **U**
- Es negativa entre las raíces
- Es positiva fuera de las raíces

### 4.4 Inecuaciones con Valor Absoluto

| Forma | Equivalencia | Tipo de conjunto |
|:---|:---|:---|
| `|x| < a` (a > 0) | `−a < x < a` | Intervalo abierto central |
| `|x| ≤ a` (a > 0) | `−a ≤ x ≤ a` | Intervalo cerrado central |
| `|x| > a` (a > 0) | `x < −a  o  x > a` | Dos rayos |
| `|x| ≥ a` (a > 0) | `x ≤ −a  o  x ≥ a` | Dos rayos cerrados |

```
|2x − 1| < 5
−5 < 2x − 1 < 5
−4 < 2x < 6
−2 < x < 3

Solución: x ∈ (−2, 3)
```

```
|3x + 2| ≥ 4
3x + 2 ≥ 4  o  3x + 2 ≤ −4
3x ≥ 2       o  3x ≤ −6
x ≥ 2/3      o  x ≤ −2

Solución: x ∈ (−∞, −2] ∪ [2/3, +∞)
```

### 4.5 Notación — Intervalos

| Notación | Significado | Recta numérica |
|:---:|:---|:---|
| `(a, b)` | Abierto: `a < x < b` | Círculos vacíos en a y b |
| `[a, b]` | Cerrado: `a ≤ x ≤ b` | Círculos rellenos en a y b |
| `[a, b)` | Semiabierto: `a ≤ x < b` | Relleno en a, vacío en b |
| `(−∞, b]` | `x ≤ b` | Flecha izquierda, relleno en b |
| `(a, +∞)` | `x > a` | Círculo vacío en a, flecha derecha |

---

## 5. Errores Comunes

| Error | Descripción | Corrección |
|:---|:---|:---|
| No invertir signo | Dividir por negativo sin invertir `<`/`>` | Si divides por `−k`, invierte el signo de desigualdad |
| `x² = 9 → x = 3` | Omitir la raíz negativa | `x = ±3` siempre |
| `√(x²) = x` | Ignorar el valor absoluto | `√(x²) = |x|`, no necesariamente `x` |
| `|x+y| = |x| + |y|` | Aplicar incorrectamente | Solo si `x` e `y` tienen el mismo signo |
| Discriminante negativo con raíces | Calcular raíces cuando `Δ < 0` | No hay raíces reales; la ecuación no tiene solución en ℝ |
| Verificar solo una raíz | Probar solo `x₁` en la ecuación original | Siempre verificar AMBAS raíces |
| Intervalo abierto vs. cerrado | Usar `(` cuando debería ser `[` | Si la inecuación incluye `=`, usar intervalo cerrado `[` o `]` |

---

## 6. Técnicas de Estudio

### Active Recall — Preguntas de Autoevaluación

1. Sin ver la fórmula, escribe la fórmula cuadrática de memoria.
2. Resuelve `3x² − 5x − 2 = 0` usando los tres métodos (factorización, completar cuadrado, fórmula).
3. ¿Cuándo tiene solución única una ecuación cuadrática? ¿Qué pasa con el discriminante?
4. Resuelve la inecuación `x² − 4 ≤ 0` y grafica en la recta numérica.
5. Resuelve `|x − 3| ≤ 5` y expresa en notación de intervalo.

### Feynman: La Fórmula Cuadrática

Explica de dónde viene la fórmula cuadrática: completar el cuadrado en la ecuación general `ax²+bx+c=0` paso a paso. Si puedes derivarla tú mismo, nunca la olvidarás.

```
ax² + bx + c = 0
x² + (b/a)x = −c/a
x² + (b/a)x + (b/2a)² = −c/a + b²/4a²
(x + b/2a)² = (b² − 4ac)/4a²
x + b/2a = ±√(b²−4ac) / 2a
x = (−b ± √(b²−4ac)) / 2a  ∎
```

---

## 7. Recursos Externos

| Recurso | Descripción | URL |
|:---|:---|:---|
| **Matemóvil** (YouTube) | Ecuaciones cuadráticas paso a paso | https://www.youtube.com/@matemovil |
| **Khan Academy ES** — Cuadráticas | Videos + ejercicios interactivos | https://es.khanacademy.org/math/algebra/x2f8bb11595b61c86:quadratic-functions-equations |
| **Profesor Leonard** (YouTube, inglés) | Solving Quadratic Equations — muy detallado | https://www.youtube.com/c/ProfessorLeonard |
| **GeoGebra** | Graficar parábolas e inecuaciones interactivamente | https://www.geogebra.org/graphing |
| **Symbolab** | Verificar ecuaciones e inecuaciones paso a paso | https://www.symbolab.com/ |

---

## 8. Referencia Rápida

```
FÓRMULA CUADRÁTICA:
x = (−b ± √(b²−4ac)) / 2a

DISCRIMINANTE (Δ = b²−4ac):
Δ > 0 → 2 raíces reales
Δ = 0 → 1 raíz doble
Δ < 0 → sin raíces reales

VALOR ABSOLUTO:
|x| < a  ↔  −a < x < a         (intervalo central)
|x| > a  ↔  x < −a  o  x > a  (dos rayos)

INECUACIÓN CUADRÁTICA (a > 0):
ax² + bx + c < 0  → x entre las raíces
ax² + bx + c > 0  → x fuera de las raíces

RELACIONES DE VIETA:
x₁ + x₂ = −b/a
x₁ · x₂ = c/a
```
