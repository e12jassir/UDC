# Unidad 2 — Expresiones Algebraicas y Factorización
**Fundamentos de Matemáticas · CFBD242-A1 · Atilano Arrieta Vivero**

---

## 🧭 Mapa de Contenidos

```
Expresiones Algebraicas
├── Monomios, binomios, polinomios
├── Operaciones con polinomios (suma, resta, multiplicación)
└── División de polinomios (Ruffini)

Productos Notables
├── Cuadrado de binomio (suma y diferencia)
├── Producto de suma por diferencia
├── Cubo de binomio
└── Binomio de Newton

Factorización (Casos I al X)
├── Factor común (Caso I)
├── Diferencia de cuadrados (Caso II)
├── Trinomio cuadrado perfecto (Caso III y IV)
├── Trinomio general (Caso V)
├── Suma/diferencia de cubos (Caso VI y VII)
├── Factor común por agrupamiento (Caso VIII)
├── Agrupación de 4 o más términos (Casos IX y X)
└── Fracciones algebraicas
```

---

## 1. Expresiones Algebraicas — Conceptos Base

### 1.1 Clasificación de Polinomios

| Nombre | Número de términos | Ejemplo |
|:---|:---:|:---|
| Monomio | 1 | `5x³` |
| Binomio | 2 | `x² − 4` |
| Trinomio | 3 | `x² + 5x + 6` |
| Polinomio | ≥ 4 | `x³ − 2x² + x − 1` |

**Grado** de un polinomio: el mayor exponente de la variable principal.  
Ej.: `4x⁵ − 3x² + 7` tiene grado **5**.

### 1.2 Operaciones con Polinomios

**Suma/Resta:** solo se combinan términos semejantes (mismo exponente).

```
(3x² + 2x − 1) + (x² − 5x + 4)
= (3+1)x² + (2−5)x + (−1+4)
= 4x² − 3x + 3
```

**Multiplicación (FOIL para binomios):**

```
(a + b)(c + d) = ac + ad + bc + bd

(2x + 3)(x − 1)
= 2x·x + 2x·(−1) + 3·x + 3·(−1)
= 2x² − 2x + 3x − 3
= 2x² + x − 3
```

---

## 2. Productos Notables

Los productos notables son multiplicaciones con patrones predecibles que se memorizan para agilizar la factorización.

### 2.1 Cuadrado de un Binomio

**(a + b)² = a² + 2ab + b²**

> **Estructura:** primer término al cuadrado + dos veces el producto de los dos términos + segundo término al cuadrado.

| Expresión | Desarrollo |
|:---|:---|
| `(x + 3)²` | `x² + 6x + 9` |
| `(2x − 5)²` | `4x² − 20x + 25` |
| `(3a + 4b)²` | `9a² + 24ab + 16b²` |

⚠️ **Error crítico:** `(a + b)² ≠ a² + b²`. El término medio `2ab` NUNCA se omite.

### 2.2 Producto de Suma por Diferencia

**(a + b)(a − b) = a² − b²**

| Expresión | Resultado |
|:---|:---|
| `(x + 5)(x − 5)` | `x² − 25` |
| `(3x + 2)(3x − 2)` | `9x² − 4` |
| `(a + b)(a − b)` | `a² − b²` |

> **Clave:** Los términos cruzados se cancelan. Solo queda la diferencia de cuadrados.

### 2.3 Cubo de un Binomio

**(a + b)³ = a³ + 3a²b + 3ab² + b³**  
**(a − b)³ = a³ − 3a²b + 3ab² − b³**

| Expresión | Desarrollo |
|:---|:---|
| `(x + 2)³` | `x³ + 6x² + 12x + 8` |
| `(x − 1)³` | `x³ − 3x² + 3x − 1` |

### 2.4 Binomio de Newton (Resumen)

Para `(a + b)ⁿ`, los coeficientes son los de la **fila n del triángulo de Pascal**:

```
n=0:        1
n=1:      1   1
n=2:    1   2   1
n=3:  1   3   3   1
n=4: 1   4   6   4   1
```

`(a + b)⁴ = a⁴ + 4a³b + 6a²b² + 4ab³ + b⁴`

---

## 3. Factorización — Los 10 Casos

La factorización es el proceso inverso de la multiplicación. Consiste en expresar un polinomio como **producto de factores**.

> **Regla de oro:** Siempre verificar si existe **factor común (Caso I)** antes de aplicar cualquier otro caso.

### CASO I — Factor Común

Extraer el máximo factor que divide a **todos** los términos.

```
6x³ + 9x² − 3x
= 3x(2x² + 3x − 1)    ← Factor común: 3x
```

```
4a²b − 8ab² + 12ab
= 4ab(a − 2b + 3)      ← Factor común: 4ab
```

### CASO II — Diferencia de Cuadrados

`a² − b² = (a + b)(a − b)`

**Requisito:** dos cuadrados perfectos con signo negativo entre ellos.

| Expresión | Factorización |
|:---|:---|
| `x² − 9` | `(x + 3)(x − 3)` |
| `4x² − 25` | `(2x + 5)(2x − 5)` |
| `x⁴ − 16` | `(x² + 4)(x + 2)(x − 2)` |
| `a² − b²c²` | `(a + bc)(a − bc)` |

> **Truco:** Identifica `a` y `b` tomando raíz cuadrada de cada término.

### CASO III — Trinomio Cuadrado Perfecto (coef. 1)

`x² + bx + c = (x + p)(x + q)` donde `p + q = b` y `p · q = c`

```
x² + 5x + 6
Busco p, q tal que p+q=5 y p·q=6 → p=2, q=3
= (x + 2)(x + 3)
```

```
x² − 7x + 12
p+q=−7, p·q=12 → p=−3, q=−4
= (x − 3)(x − 4)
```

### CASO IV — Trinomio Cuadrado Perfecto (coef. ≠ 1)

`ax² + bx + c`

**Método de la cruz (factorización cruzada):**

```
2x² + 7x + 3
a·c = 6 → busco pares que sumen 7: (1, 6)
2x² + x + 6x + 3
= x(2x + 1) + 3(2x + 1)
= (x + 3)(2x + 1)
```

**Verificación:** `(x+3)(2x+1) = 2x² + x + 6x + 3 = 2x² + 7x + 3` ✅

### CASO V — Diferencia/Suma de Cubos

| Fórmula | Factorización |
|:---|:---|
| `a³ − b³` | `(a − b)(a² + ab + b²)` |
| `a³ + b³` | `(a + b)(a² − ab + b²)` |

**Mnemotécnica SOAP:** Sign, Opposite, Always Positive
- `(a − b)`: mismo signo que el original
- `(a² + ab + b²)`: el signo del medio es opuesto, el último siempre positivo

| Expresión | Factorización |
|:---|:---|
| `x³ − 8` | `(x − 2)(x² + 2x + 4)` |
| `x³ + 27` | `(x + 3)(x² − 3x + 9)` |
| `8a³ − 125b³` | `(2a − 5b)(4a² + 10ab + 25b²)` |

### CASO VI — Factor Común por Agrupamiento (4 términos)

```
ax + ay + bx + by
= a(x + y) + b(x + y)
= (a + b)(x + y)
```

```
x³ − x² + x − 1
= x²(x − 1) + 1(x − 1)
= (x² + 1)(x − 1)
```

### CASO VII — Cuadrado Perfecto con Factor Común

```
2x² + 8x + 8
= 2(x² + 4x + 4)
= 2(x + 2)²
```

### CASO VIII — Diferencia de Cuadrados con Factor Previo

```
5x⁴ − 5y⁴
= 5(x⁴ − y⁴)
= 5(x² + y²)(x² − y²)
= 5(x² + y²)(x + y)(x − y)
```

### CASOS IX y X — Polinomios de Grado Superior

Para polinomios de grado 3 o 4, se pueden usar:
- **División sintética (Ruffini):** probar raíces racionales `±p/q`
- **Teorema del factor:** `(x − r)` es factor si `f(r) = 0`

```
Factorizar: x³ − 6x² + 11x − 6
Candidatos: ±1, ±2, ±3, ±6
Pruebo x=1: 1 − 6 + 11 − 6 = 0 ✅
División sintética:
  1 | 1  -6  11  -6
    |    1  -5   6
    | 1  -5   6   0
→ (x − 1)(x² − 5x + 6)
→ (x − 1)(x − 2)(x − 3)
```

---

## 4. Tabla Resumen — Casos de Factorización

| Caso | Nombre | Forma a Identificar | Resultado |
|:---:|:---|:---|:---|
| I | Factor común | Todo término divisible por un factor | `k·(…)` |
| II | Diferencia de cuadrados | `a² − b²` | `(a+b)(a−b)` |
| III | Trinomio coef. 1 | `x² + bx + c` | `(x+p)(x+q)` |
| IV | Trinomio coef. ≠ 1 | `ax² + bx + c` | Método cruzado |
| V | Suma de cubos | `a³ + b³` | `(a+b)(a²−ab+b²)` |
| V | Diferencia de cubos | `a³ − b³` | `(a−b)(a²+ab+b²)` |
| VI | Agrupamiento 4t. | `ax+ay+bx+by` | `(a+b)(x+y)` |
| VII | Cuadrado con F.C. | `k(a²+2ab+b²)` | `k(a+b)²` |
| VIII | Doble diferencia | `k(a⁴−b⁴)` | `k(a²+b²)(a+b)(a−b)` |
| IX-X | Grado superior | Polinomios cúbicos/cuárticos | Ruffini + casos anteriores |

---

## 5. Fracciones Algebraicas

### 5.1 Simplificación

Factorizar numerador y denominador, luego cancelar factores comunes.

```
(x² − 4) / (x² + 2x)
= (x+2)(x−2) / x(x+2)
= (x−2) / x    (con x ≠ 0 y x ≠ −2)
```

### 5.2 Suma y Resta de Fracciones Algebraicas

Igual que con fracciones numéricas: encontrar el **mínimo común denominador (MCD)**.

```
  2       3
----- + -----
x+1     x−1

MCD = (x+1)(x−1)

= 2(x−1) + 3(x+1)
  ─────────────────
     (x+1)(x−1)

= 2x−2+3x+3
  ─────────
  (x+1)(x−1)

= 5x+1
  ─────────
  x²−1
```

### 5.3 Multiplicación y División

```
Multiplicación: (a/b) · (c/d) = ac/bd

División: (a/b) ÷ (c/d) = (a/b) · (d/c) = ad/bc
```

---

## 6. Errores Comunes

| Error | Descripción | Corrección |
|:---|:---|:---|
| `(a+b)² = a²+b²` | Omitir el término medio | `(a+b)² = a²+2ab+b²` |
| Signo en cubo de binomio | `(a−b)³` con signos incorrectos | Los signos alternan: `+, −, +, −` |
| No extraer factor común primero | Saltar al Caso II sin verificar | Siempre Caso I primero |
| Cancelar sumas en fracciones | `(x+2)/(x+3) = 2/3` (incorrecto) | Solo se cancelan **factores**, no sumandos |
| `a³−b³ = (a−b)³` | Confundir diferencia de cubos con cubo de diferencia | `a³−b³ = (a−b)(a²+ab+b²)` |
| Olvidar restricciones en fracciones | Simplificar sin indicar `x ≠ …` | Siempre indicar los valores excluidos |

---

## 7. Técnicas de Estudio

### Active Recall

1. Escribe de memoria las fórmulas de los 5 productos notables principales.
2. Dado `x² + 7x + 10`, aplica Caso III sin ver las notas.
3. Factoriza completamente `2x⁴ − 32` (respuesta: `2(x²+4)(x+2)(x−2)`).
4. Simplifica `(x²−9)/(x²−x−6)` sin calculadora.
5. ¿Cuál es la diferencia entre `(a+b)²` y `a²+b²`? Da un contraejemplo numérico.

### Técnica de Feynman para Factorización

Enseña el Caso IV (trinomio con coeficiente) a un compañero usando solo números concretos. Si no puedes explicar el "porqué" del método cruzado, es que aún no lo has comprendido del todo. El proceso: reescribir `ax² + bx + c` como `ax² + px + qx + c` donde `p+q=b` y `p·q=ac`.

---

## 8. Recursos Externos Reales

| Recurso | Descripción | URL |
|:---|:---|:---|
| **Matemóvil** (YouTube) | Factorización casos con ejemplos detallados | https://www.youtube.com/@matemovil |
| **Tareasplus** (YouTube) | Canal latinoamericano con todos los casos | https://www.youtube.com/@tareasplus |
| **Khan Academy ES** | Módulo de álgebra, factorización interactiva | https://es.khanacademy.org/math/algebra/x2f8bb11595b61c86:quadratics-multiplying-factoring |
| **Mathway** | Verificador de factorizaciones paso a paso | https://www.mathway.com/Algebra |
| **Libro: Álgebra — Baldor** | Capítulos 8-12: Productos Notables y Factorización | Referencia clásica latinoamericana |

---

## 9. Referencia Rápida

```
PRODUCTOS NOTABLES
(a+b)²   = a² + 2ab + b²
(a−b)²   = a² − 2ab + b²
(a+b)(a−b) = a² − b²
(a+b)³   = a³ + 3a²b + 3ab² + b³
(a−b)³   = a³ − 3a²b + 3ab² − b³
a³+b³    = (a+b)(a²−ab+b²)
a³−b³    = (a−b)(a²+ab+b²)

VERIFICACIÓN SIEMPRE:
Multiplica el resultado factorizado → debe dar el polinomio original.
```

### Cuadrados Perfectos para Reconocer Rápido

```
1, 4, 9, 16, 25, 36, 49, 64, 81, 100, 121, 144, 169, 196, 225
```

### Cubos Perfectos para Reconocer Rápido

```
1, 8, 27, 64, 125, 216, 343, 512, 729, 1000
```
