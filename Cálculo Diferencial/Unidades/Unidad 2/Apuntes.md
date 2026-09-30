# Apuntes — Unidad 2: Derivadas y Reglas de Derivación
**Asignatura:** Cálculo Diferencial · CFBD243-B1
**Docente:** Katherine Paternina Sierra
**Última actualización:** 2026-09-29

---

## 1. Concepto de Derivada

### Definición por límite (formal)

La **derivada** de f(x) en el punto x = a es la razón de cambio instantánea de la función en ese punto:

```
         f(a + h) - f(a)
f'(a) = lim ─────────────
        h→0       h
```

Si este límite existe, se dice que f es **derivable (o diferenciable)** en x = a.

### Interpretación geométrica

La derivada f'(a) es la **pendiente de la recta tangente** a la curva y = f(x) en el punto (a, f(a)).

```
Ejemplo: f(x) = x²
         f'(x) = 2x
         
En x = 3: f'(3) = 6  → la tangente tiene pendiente 6
En x = 0: f'(0) = 0  → la tangente es horizontal (mínimo)
En x = -2: f'(-2) = -4 → la tangente tiene pendiente -4 (decrece)
```

### Interpretación física

La derivada representa la **velocidad instantánea** cuando f(x) describe posición en función del tiempo.

```
Si s(t) = posición en el tiempo t
Entonces s'(t) = velocidad instantánea en t
Y s''(t) = aceleración instantánea en t
```

### Notaciones equivalentes de la derivada

```
f'(x)           (notación de Lagrange — la más común en el curso)
dy/dx           (notación de Leibniz — útil para regla de la cadena)
d/dx [f(x)]     (operador derivada)
Df(x)           (notación de Euler)
ẏ               (notación de Newton — usada en física)
```

---

## 2. Derivada desde la Definición — Ejemplos

### Ejemplo 1: Derivar f(x) = x²

```
         f(x + h) - f(x)          (x + h)² - x²
f'(x) = lim ─────────────── = lim ────────────────
        h→0       h           h→0        h

Expandir (x + h)² = x² + 2xh + h²:

      x² + 2xh + h² - x²     2xh + h²
= lim ────────────────────── = lim ──────────
  h→0          h             h→0      h

= lim (2x + h) = 2x + 0 = 2x
  h→0

Por lo tanto: f'(x) = 2x
```

### Ejemplo 2: Derivar f(x) = 3x + 5

```
         (3(x+h) + 5) - (3x + 5)     3x + 3h + 5 - 3x - 5
f'(x) = lim ───────────────────────── = lim ─────────────────────
        h→0           h              h→0           h

        3h
= lim  ─── = lim 3 = 3
  h→0   h    h→0

Por lo tanto: f'(x) = 3
```

---

## 3. Tabla de Derivadas Fundamentales

| Función f(x) | Derivada f'(x) | Observación |
|:---:|:---:|:---|
| k (constante) | 0 | La derivada de cualquier constante es 0 |
| x | 1 | |
| x^n | n · x^(n-1) | Regla de la potencia (n cualquier real) |
| √x = x^(1/2) | 1/(2√x) | Aplicar regla de la potencia con n=1/2 |
| 1/x = x^(-1) | -1/x² | n = -1 |
| e^x | e^x | La exponencial es su propia derivada |
| a^x | a^x · ln(a) | Base a > 0, a ≠ 1 |
| ln(x) | 1/x | Solo para x > 0 |
| log_a(x) | 1/(x · ln(a)) | |
| sen(x) | cos(x) | x en radianes |
| cos(x) | -sen(x) | Notar el signo negativo |
| tan(x) | sec²(x) | Equivale a 1/cos²(x) |
| cot(x) | -csc²(x) | |
| sec(x) | sec(x)·tan(x) | |
| csc(x) | -csc(x)·cot(x) | |
| arcsen(x) | 1/√(1 - x²) | |x| < 1 |
| arccos(x) | -1/√(1 - x²) | |x| < 1 |
| arctan(x) | 1/(1 + x²) | |

---

## 4. Reglas de Derivación

### 4.1 Regla de la Constante

```
d/dx [k · f(x)] = k · f'(x)

Ejemplo: d/dx [5x³] = 5 · 3x² = 15x²
```

### 4.2 Regla de la Suma y Diferencia

```
[f(x) ± g(x)]' = f'(x) ± g'(x)

Ejemplo: d/dx [x³ + 2x² - 4x + 7]
       = 3x² + 4x - 4 + 0
       = 3x² + 4x - 4
```

### 4.3 Regla de la Potencia (Power Rule)

```
d/dx [x^n] = n · x^(n-1)

Ejemplos:
  d/dx [x⁵]    = 5x⁴
  d/dx [x^(-2)] = -2x^(-3) = -2/x³
  d/dx [x^(1/3)] = (1/3)x^(-2/3) = 1/(3x^(2/3))
  d/dx [√x]    = 1/(2√x)
```

**Aplicación completa:**
```
f(x) = 4x⁵ - 3x³ + 2x - 7

f'(x) = 4·5x⁴ - 3·3x² + 2·1 - 0
      = 20x⁴ - 9x² + 2
```

### 4.4 Regla del Producto

```
[f(x) · g(x)]' = f'(x) · g(x) + f(x) · g'(x)

Mnemotécnico: "Prima·segunda + primera·prima"
```

**Ejemplo resuelto:**
```
h(x) = (3x² + 1)(x³ - 2x)

Identificar:
  f(x) = 3x² + 1  →  f'(x) = 6x
  g(x) = x³ - 2x  →  g'(x) = 3x² - 2

Aplicar:
  h'(x) = 6x(x³ - 2x) + (3x² + 1)(3x² - 2)
        = 6x⁴ - 12x² + 9x⁴ - 6x² + 3x² - 2
        = 15x⁴ - 15x² - 2
```

### 4.5 Regla del Cociente

```
[f(x) / g(x)]' = [f'(x)·g(x) - f(x)·g'(x)] / [g(x)]²

Mnemotécnico: "Prima·baja menos alta·prima, sobre baja al cuadrado"
              (Numerador: prima-baja - alta-prima; Denominador: baja²)
```

**Ejemplo resuelto:**
```
h(x) = (2x + 1) / (x² - 3)

  f(x) = 2x + 1   →  f'(x) = 2
  g(x) = x² - 3   →  g'(x) = 2x

  h'(x) = [2(x² - 3) - (2x + 1)(2x)] / (x² - 3)²
         = [2x² - 6 - 4x² - 2x] / (x² - 3)²
         = [-2x² - 2x - 6] / (x² - 3)²
         = -2(x² + x + 3) / (x² - 3)²
```

### 4.6 Regla de la Cadena (Chain Rule)

Para funciones compuestas f(g(x)):

```
d/dx [f(g(x))] = f'(g(x)) · g'(x)

Notación Leibniz: dy/dx = (dy/du) · (du/dx)
donde u = g(x) (función interna)
```

**Pasos para aplicar la regla de la cadena:**
1. Identificar la función externa f y la interna g.
2. Derivar f respecto a g(x): f'(g(x)).
3. Multiplicar por la derivada de g(x): g'(x).

**Ejemplos:**
```
a) h(x) = (x² + 3)⁵
   Externa: u⁵  →  derivada: 5u⁴
   Interna: u = x² + 3  →  u' = 2x
   h'(x) = 5(x² + 3)⁴ · 2x = 10x(x² + 3)⁴

b) h(x) = √(3x - 1) = (3x - 1)^(1/2)
   Externa: u^(1/2)  →  derivada: (1/2)u^(-1/2)
   Interna: u = 3x - 1  →  u' = 3
   h'(x) = (1/2)(3x - 1)^(-1/2) · 3 = 3/(2√(3x-1))

c) h(x) = e^(x² + 1)
   Externa: e^u  →  derivada: e^u
   Interna: u = x² + 1  →  u' = 2x
   h'(x) = e^(x² + 1) · 2x = 2x·e^(x² + 1)

d) h(x) = ln(5x³ - 2)
   Externa: ln(u)  →  derivada: 1/u
   Interna: u = 5x³ - 2  →  u' = 15x²
   h'(x) = 1/(5x³ - 2) · 15x² = 15x²/(5x³ - 2)
```

---

## 5. Ejemplos Resueltos Combinados

### Ejemplo 1 — Todas las reglas combinadas

```
f(x) = (x² + 1)³ / (2x - 3)

Paso 1 — Identificar estructura: cociente entre (x² + 1)³ y (2x - 3)

Paso 2 — Numerador = (x² + 1)³:
  Derivada por cadena: 3(x² + 1)² · 2x = 6x(x² + 1)²

Paso 3 — Denominador = (2x - 3):
  Derivada: 2

Paso 4 — Aplicar regla del cociente:
  f'(x) = [6x(x² + 1)²(2x - 3) - (x² + 1)³ · 2] / (2x - 3)²

Paso 5 — Factorizar (x² + 1)²:
  f'(x) = (x² + 1)² · [6x(2x - 3) - 2(x² + 1)] / (2x - 3)²
         = (x² + 1)² · [12x² - 18x - 2x² - 2] / (2x - 3)²
         = (x² + 1)² · [10x² - 18x - 2] / (2x - 3)²
         = 2(x² + 1)²(5x² - 9x - 1) / (2x - 3)²
```

### Ejemplo 2 — Derivada de función con raíz y producto

```
g(x) = x² · √(x + 1)

Producto:  f = x²,  f' = 2x
           g = (x + 1)^(1/2),  g' = 1/(2√(x+1))

g'(x) = 2x · √(x + 1) + x² · 1/(2√(x+1))
      = 2x√(x+1) + x²/(2√(x+1))

Simplificando (factor común 1/(2√(x+1))):
      = [4x(x+1) + x²] / (2√(x+1))
      = [4x² + 4x + x²] / (2√(x+1))
      = (5x² + 4x) / (2√(x+1))
      = x(5x + 4) / (2√(x+1))
```

---

## 6. Derivadas de Orden Superior

```
f(x)   →  función original
f'(x)  →  primera derivada
f''(x) →  segunda derivada = derivada de f'(x)
f'''(x) → tercera derivada
f^(n)(x) → derivada de orden n

Notación Leibniz: d²y/dx², d³y/dx³, d^n·y/dx^n
```

**Ejemplo:**
```
f(x) = x⁴ - 3x² + 2x - 5

f'(x)  = 4x³ - 6x + 2
f''(x) = 12x² - 6
f'''(x) = 24x
f^(4)(x) = 24
f^(5)(x) = 0
```

---

## 7. Errores Comunes

| Error | Ejemplo incorrecto | Corrección |
|:---|:---|:---|
| Derivar el producto como producto de derivadas | (fg)' = f'g' | (fg)' = f'g + fg' |
| Olvidar la regla de la cadena | d/dx[(3x+1)⁵] = 5(3x+1)⁴ | = 5(3x+1)⁴ · 3 = 15(3x+1)⁴ |
| Signo en derivada de cos | d/dx[cos(x)] = sen(x) | = -sen(x) (signo negativo) |
| No simplificar raíces como potencias | d/dx[√x] como caso aparte | Usar x^(1/2) y regla de potencia |
| Constante aditiva tiene derivada no nula | d/dx[x² + 5] = 2x + 5 | = 2x + 0 = 2x |
| Error en regla del cociente: orden del numerador | f'g + fg' (signo equivocado) | f'g − fg' en el numerador |

---

## 8. Métodos de Estudio

### Active Recall — Preguntas

1. Escribe la definición de derivada como límite, sin mirar los apuntes.
2. ¿Cuál es la derivada de x^n, sen(x), cos(x), e^x, ln(x)?
3. Explica con palabras propias la regla del producto.
4. ¿En qué se diferencia la regla de la cadena de las otras reglas?
5. Sin calcular, ¿cuántas derivadas se necesitan hasta llegar a 0 para f(x) = x⁵?

### Ejercicios de práctica (resolver sin ver solución)

```
1. f(x) = 3x⁴ - 5x² + 7x - 2        [Resp: 12x³ - 10x + 7]
2. g(x) = (x + 2)(x² - 3)             [Resp: 3x² + 4x - 3]
3. h(x) = x / (x² + 1)               [Resp: (1 - x²)/(x² + 1)²]
4. k(x) = (2x³ - 1)⁴                 [Resp: 24x²(2x³-1)³]
5. m(x) = √(x² + 4)                  [Resp: x/√(x² + 4)]
6. p(x) = e^(3x) · x²                [Resp: x²·3e^(3x) + 2x·e^(3x)]
```

---

## 9. Recursos Externos

| Recurso | Descripción | URL |
|:---|:---|:---|
| **Matemáticas profe Alex** | Playlist completa de derivadas: regla de la potencia, producto, cociente y cadena | https://www.youtube.com/@matematicasprofealex |
| **Math2Me** | Videos de derivadas con ejercicios de examen | https://www.youtube.com/@math2me |
| **Salvador FI** | Derivadas nivel ingeniería con enfoque técnico riguroso | https://www.youtube.com/@SalvadorFI |
| **Khan Academy Español** | Ejercicios interactivos de derivadas con pista y solución | https://es.khanacademy.org/math/calculus-1 |
| **WolframAlpha** | Verificar derivadas paso a paso | https://www.wolframalpha.com |

---

## 10. Referencia Rápida

```
DEFINICIÓN
  f'(x) = lim [f(x+h) - f(x)] / h
          h→0

REGLAS BÁSICAS
  [k]'        = 0
  [x^n]'      = n·x^(n-1)
  [k·f]'      = k·f'
  [f ± g]'    = f' ± g'
  [f·g]'      = f'g + fg'
  [f/g]'      = (f'g - fg') / g²
  [f(g(x))]'  = f'(g(x)) · g'(x)

DERIVADAS ESENCIALES
  [x^n]'   = n·x^(n-1)
  [e^x]'   = e^x
  [ln x]'  = 1/x
  [a^x]'   = a^x·ln(a)
  [sen x]' = cos x
  [cos x]' = -sen x
  [tan x]' = sec²x

REGLA DE LA CADENA (forma práctica)
  Función compuesta: externa(interna)
  Derivada: [der. externa evaluada en interna] × [der. interna]

  (f∘g)' = f'(g)·g'
```
