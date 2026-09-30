# Apuntes — Unidad 3: Aplicaciones de la Derivada
**Asignatura:** Cálculo Diferencial · CFBD243-B1
**Docente:** Katherine Paternina Sierra
**Última actualización:** 2026-09-29

---

## 1. Derivadas de Funciones Trigonométricas

### Tabla completa de derivadas trigonométricas

| f(x) | f'(x) | Nota |
|:---:|:---:|:---|
| sen(x) | cos(x) | x en radianes |
| cos(x) | -sen(x) | Signo negativo |
| tan(x) | sec²(x) = 1/cos²(x) | |
| cot(x) | -csc²(x) = -1/sen²(x) | |
| sec(x) | sec(x)·tan(x) | |
| csc(x) | -csc(x)·cot(x) | |
| arcsen(x) | 1/√(1-x²) | |x| < 1 |
| arccos(x) | -1/√(1-x²) | |x| < 1 |
| arctan(x) | 1/(1+x²) | |

### Derivación de funciones trigonométricas simples

```
a) f(x) = sen(x)
   f'(x) = cos(x)

b) f(x) = 3cos(x) - 2sen(x)
   f'(x) = -3sen(x) - 2cos(x)

c) f(x) = tan(x) + x²
   f'(x) = sec²(x) + 2x

d) f(x) = x·sen(x)         [Regla del producto]
   f'(x) = sen(x) + x·cos(x)

e) f(x) = sen(x)/cos(x) = tan(x)  [Verificación por regla del cociente]
   f = sen(x),  f' = cos(x)
   g = cos(x),  g' = -sen(x)
   f'(x) = [cos(x)·cos(x) - sen(x)·(-sen(x))] / cos²(x)
         = [cos²(x) + sen²(x)] / cos²(x)
         = 1 / cos²(x) = sec²(x)  ✓
```

---

## 2. Regla de la Cadena con Funciones Trigonométricas

La regla de la cadena se aplica cuando el argumento de la función trigonométrica es una expresión compuesta.

```
d/dx [sen(u)] = cos(u) · u'
d/dx [cos(u)] = -sen(u) · u'
d/dx [tan(u)] = sec²(u) · u'
```

### Ejemplos sistemáticos

```
a) f(x) = sen(3x)
   u = 3x,  u' = 3
   f'(x) = cos(3x) · 3 = 3cos(3x)

b) f(x) = cos(x²)
   u = x²,  u' = 2x
   f'(x) = -sen(x²) · 2x = -2x·sen(x²)

c) f(x) = tan(5x - 1)
   u = 5x - 1,  u' = 5
   f'(x) = sec²(5x - 1) · 5 = 5sec²(5x - 1)

d) f(x) = sen²(x) = [sen(x)]²
   Externa: u²,  u = sen(x),  u' = cos(x)
   f'(x) = 2sen(x) · cos(x) = sen(2x)   [identidad trigonométrica]

e) f(x) = cos(sen(x))        [cadena doble]
   Externa: cos(u),  u = sen(x),  u' = cos(x)
   f'(x) = -sen(sen(x)) · cos(x)

f) f(x) = √(sen(x)) = [sen(x)]^(1/2)
   u = sen(x),  u' = cos(x)
   f'(x) = (1/2)[sen(x)]^(-1/2) · cos(x) = cos(x) / (2√(sen(x)))
```

---

## 3. Derivación Implícita

Se usa cuando la función no está despejada en la forma y = f(x), sino en la forma F(x, y) = 0 o F(x, y) = c.

**Procedimiento:**
1. Derivar ambos lados de la ecuación respecto a x.
2. Cada vez que aparezca y, aplicar la regla de la cadena: la derivada de y es dy/dx.
3. Despejar dy/dx.

### Ejemplo 1 — Círculo de radio 5

```
Ecuación: x² + y² = 25

Derivar respecto a x (usando regla de la cadena en y²):
  d/dx[x²] + d/dx[y²] = d/dx[25]
  2x + 2y·(dy/dx) = 0

Despejar dy/dx:
  2y·(dy/dx) = -2x
  dy/dx = -2x / 2y = -x/y

Interpretación: La pendiente de la tangente al círculo en el punto (x, y) es -x/y.
```

### Ejemplo 2 — Curva implícita

```
Ecuación: x³ + y³ - 3xy = 0  (lemniscata de Bernoulli)

Derivar:
  3x² + 3y²·(dy/dx) - 3[y + x·(dy/dx)] = 0
  3x² + 3y²·(dy/dx) - 3y - 3x·(dy/dx) = 0

Agrupar términos con dy/dx:
  (dy/dx)(3y² - 3x) = 3y - 3x²
  (dy/dx) · 3(y² - x) = 3(y - x²)
  dy/dx = (y - x²) / (y² - x)
```

### Ejemplo 3 — Encontrar la tangente en un punto

```
Ecuación: x² + xy + y² = 7    en el punto (1, 2)

Paso 1 — Verificar que el punto está en la curva:
  1² + (1)(2) + 2² = 1 + 2 + 4 = 7 ✓

Paso 2 — Derivar implícitamente:
  2x + [y + x·(dy/dx)] + 2y·(dy/dx) = 0
  2x + y + x·(dy/dx) + 2y·(dy/dx) = 0
  (dy/dx)(x + 2y) = -(2x + y)
  dy/dx = -(2x + y)/(x + 2y)

Paso 3 — Evaluar en (1, 2):
  dy/dx = -(2·1 + 2)/(1 + 2·2) = -(4)/(5) = -4/5

Paso 4 — Ecuación de la tangente (y - y0 = m(x - x0)):
  y - 2 = -4/5·(x - 1)
  y = -4/5·x + 4/5 + 2
  y = -4/5·x + 14/5
```

---

## 4. Derivadas de Funciones Exponenciales y Logarítmicas

```
d/dx [e^x]      = e^x
d/dx [a^x]      = a^x · ln(a)
d/dx [e^(u)]    = e^u · u'        [cadena]
d/dx [ln(x)]    = 1/x
d/dx [ln(u)]    = u'/u            [cadena — muy útil]
d/dx [log_a(x)] = 1/(x·ln(a))
```

### Ejemplos con funciones exponenciales y logarítmicas

```
a) f(x) = e^(2x + 3)
   f'(x) = e^(2x + 3) · 2 = 2e^(2x + 3)

b) f(x) = 3^(x²)
   f'(x) = 3^(x²) · ln(3) · 2x = 2x·ln(3)·3^(x²)

c) f(x) = ln(x² + 1)
   u = x² + 1,  u' = 2x
   f'(x) = 2x / (x² + 1)

d) f(x) = ln[sen(x)]
   u = sen(x),  u' = cos(x)
   f'(x) = cos(x)/sen(x) = cot(x)

e) f(x) = x²·e^x                 [producto]
   f'(x) = 2x·e^x + x²·e^x = e^x(2x + x²) = xe^x(x + 2)
```

### Logaritmación Implícita (para simplificar productos/cocientes)

Útil cuando la función tiene productos, cocientes y potencias complejas.

```
Derivar: f(x) = (x² + 1)³ · √(x + 2) / (x³ - 1)²

Paso 1 — Aplicar logaritmo natural a ambos lados:
  ln[f(x)] = 3·ln(x² + 1) + (1/2)·ln(x + 2) - 2·ln(x³ - 1)

Paso 2 — Derivar ambos lados respecto a x:
  f'(x)/f(x) = 3·(2x)/(x² + 1) + (1/2)·1/(x + 2) - 2·(3x²)/(x³ - 1)
             = 6x/(x² + 1) + 1/(2(x + 2)) - 6x²/(x³ - 1)

Paso 3 — Multiplicar por f(x):
  f'(x) = f(x) · [6x/(x² + 1) + 1/(2(x + 2)) - 6x²/(x³ - 1)]
```

---

## 5. Ecuación de la Recta Tangente y Normal

### Recta tangente

La recta tangente a y = f(x) en el punto (a, f(a)) es:

```
y - f(a) = f'(a) · (x - a)
```

**Ejemplo:**
```
f(x) = x³ - 2x² + 1  en x = 2

f(2)  = 8 - 8 + 1 = 1           → punto (2, 1)
f'(x) = 3x² - 4x
f'(2) = 12 - 8 = 4              → pendiente = 4

Tangente: y - 1 = 4(x - 2)  →  y = 4x - 7
```

### Recta normal

La recta normal es perpendicular a la tangente en el mismo punto:

```
Pendiente de la normal = -1/f'(a)   (si f'(a) ≠ 0)

y - f(a) = [-1/f'(a)] · (x - a)
```

**Continuando el ejemplo anterior:**
```
Pendiente de la normal = -1/4

Normal: y - 1 = -1/4·(x - 2)  →  y = -x/4 + 3/2
```

---

## 6. Ejemplos Resueltos Completos

### Ejercicio 1 — Derivada con regla de la cadena + trigonometría

```
f(x) = sen³(2x + 1)  =  [sen(2x + 1)]³

Paso 1 — Identificar capas:
  Capa externa: u³    →  der: 3u²
  Capa media: sen(v)  →  der: cos(v)
  Capa interna: v = 2x + 1  →  der: 2

Paso 2 — Aplicar cadena de afuera hacia adentro:
  f'(x) = 3[sen(2x + 1)]² · cos(2x + 1) · 2
        = 6·sen²(2x + 1)·cos(2x + 1)

Simplificación con identidad sen(2θ) = 2·sen(θ)·cos(θ):
  = 3·sen(2(2x + 1))  = 3·sen(4x + 2)
```

### Ejercicio 2 — Derivación implícita con trigonometría

```
sen(x + y) = y² · cos(x)

Derivar ambos lados respecto a x:
  cos(x + y) · (1 + dy/dx) = 2y·(dy/dx)·cos(x) + y²·(-sen(x))

Expandir:
  cos(x + y) + cos(x + y)·(dy/dx) = 2y·cos(x)·(dy/dx) - y²·sen(x)

Agrupar dy/dx:
  (dy/dx)[cos(x + y) - 2y·cos(x)] = -y²·sen(x) - cos(x + y)

Despejar:
  dy/dx = [-y²·sen(x) - cos(x + y)] / [cos(x + y) - 2y·cos(x)]
```

### Ejercicio 3 — Problema de tasa de cambio relacionada

```
Un globo esférico se infla de modo que su volumen aumenta a 100 cm³/s.
¿A qué tasa crece el radio cuando r = 5 cm?

Datos:
  V = (4/3)·π·r³
  dV/dt = 100 cm³/s
  Buscar: dr/dt cuando r = 5

Derivar V respecto a t:
  dV/dt = 4π·r² · dr/dt

Despejar dr/dt:
  dr/dt = (dV/dt) / (4π·r²)
        = 100 / (4π·25)
        = 100 / (100π)
        = 1/π ≈ 0.318 cm/s
```

---

## 7. Errores Comunes

| Error | Descripción | Corrección |
|:---|:---|:---|
| Olvidar la derivada del argumento | d/dx[sen(x²)] = cos(x²) | = cos(x²)·2x (regla de la cadena) |
| Signo en cos | d/dx[cos(x)] = sen(x) | = -sen(x) (signo negativo) |
| Error en derivada implícita | Tratar y como constante | y es función de x; su derivada es dy/dx |
| No despejar dy/dx | Dejar la ecuación sin aislar dy/dx | Factorizar dy/dx y dividir |
| Multiplicar en vez de componer | [sen(x)]² ≠ sen(x²) | Son expresiones diferentes |

---

## 8. Métodos de Estudio

### Active Recall — Preguntas

1. Escribe la derivada de sen(x), cos(x) y tan(x) de memoria.
2. ¿Cuál es la derivada de sen(5x³ - 2)? Aplica la regla de la cadena paso a paso.
3. Explica con palabras el procedimiento para la derivación implícita.
4. Dado x² + y² = r², encuentra dy/dx por derivación implícita.
5. ¿Cuándo conviene usar la logaritmación implícita en lugar de derivar directamente?

### Ejercicios de práctica

```
1. f(x) = cos(3x² - x + 1)       [Resp: -(6x-1)·sen(3x²-x+1)]
2. f(x) = e^(sen(x))             [Resp: cos(x)·e^(sen(x))]
3. f(x) = ln(cos(x))             [Resp: -tan(x)]
4. x² - 2xy + y³ = 8  →  dy/dx  [Resp: (2x-2y)/(2x-3y²)]
5. f(x) = tan²(4x)              [Resp: 8·tan(4x)·sec²(4x)]
```

---

## 9. Recursos Externos

| Recurso | Descripción | URL |
|:---|:---|:---|
| **Matemáticas profe Alex** | Derivadas de funciones trigonométricas y regla de la cadena | https://www.youtube.com/@matematicasprofealex |
| **Math2Me** | Derivación implícita explicada con múltiples ejemplos | https://www.youtube.com/@math2me |
| **Salvador FI** | Derivadas con enfoque de ingeniería — cadena doble, implícita, trig | https://www.youtube.com/@SalvadorFI |
| **WolframAlpha** | Verificar derivadas y ver pasos intermedios | https://www.wolframalpha.com |
| **Symbolab** | Calculadora de derivadas con solución paso a paso (gratuita) | https://www.symbolab.com/solver/derivative-calculator |

---

## 10. Referencia Rápida

```
DERIVADAS TRIGONOMÉTRICAS
  [sen(x)]'  = cos(x)
  [cos(x)]'  = -sen(x)
  [tan(x)]'  = sec²(x)
  [cot(x)]'  = -csc²(x)
  [sec(x)]'  = sec(x)·tan(x)
  [csc(x)]'  = -csc(x)·cot(x)

REGLA DE LA CADENA CON TRIG
  [sen(u)]' = cos(u)·u'
  [cos(u)]' = -sen(u)·u'
  [tan(u)]' = sec²(u)·u'

DERIVADAS EXPONENCIALES Y LOGARÍTMICAS
  [e^x]'    = e^x
  [e^u]'    = e^u·u'
  [a^x]'    = a^x·ln(a)
  [ln(x)]'  = 1/x
  [ln(u)]'  = u'/u

DERIVACIÓN IMPLÍCITA — PASOS
  1. Derivar ambos lados respecto a x
  2. Derivada de y = dy/dx (regla de la cadena)
  3. Agrupar todos los términos con dy/dx
  4. Factorizar y despejar dy/dx

RECTA TANGENTE
  y - f(a) = f'(a) · (x - a)

RECTA NORMAL
  y - f(a) = -1/f'(a) · (x - a)

IDENTIDADES TRIGONOMÉTRICAS ÚTILES
  sen²(x) + cos²(x) = 1
  sen(2x) = 2·sen(x)·cos(x)
  cos(2x) = cos²(x) - sen²(x)
  1 + tan²(x) = sec²(x)
  1 + cot²(x) = csc²(x)
```
