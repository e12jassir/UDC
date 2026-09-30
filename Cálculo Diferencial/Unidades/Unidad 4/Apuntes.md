# Apuntes — Unidad 4: Optimización y Concavidad
**Asignatura:** Cálculo Diferencial · CFBD243-B1
**Docente:** Katherine Paternina Sierra
**Última actualización:** 2026-09-29

---

## 1. Criterio de la Primera Derivada — Máximos y Mínimos Locales

### Definiciones

| Término | Definición práctica |
|:---|:---|
| **Punto crítico** | x = c tal que f'(c) = 0 o f'(c) no existe |
| **Máximo local** | f(c) ≥ f(x) para x cerca de c |
| **Mínimo local** | f(c) ≤ f(x) para x cerca de c |
| **Extremo local** | Máximo o mínimo local (puede no ser el global) |

### Procedimiento — Criterio de la primera derivada

```
1. Calcular f'(x)
2. Encontrar los puntos críticos: resolver f'(x) = 0
3. Analizar el signo de f'(x) en intervalos alrededor de cada punto crítico:
   - Si f' cambia de (+) a (-) en x = c  →  MÁXIMO LOCAL en c
   - Si f' cambia de (-) a (+) en x = c  →  MÍNIMO LOCAL en c
   - Si f' no cambia de signo en x = c   →  Punto de inflexión (ni máximo ni mínimo)
```

### Ejemplo resuelto completo

```
f(x) = x³ - 3x² - 9x + 5

Paso 1 — Derivada:
  f'(x) = 3x² - 6x - 9

Paso 2 — Puntos críticos (f'(x) = 0):
  3x² - 6x - 9 = 0
  x² - 2x - 3 = 0
  (x - 3)(x + 1) = 0
  x = 3  o  x = -1

Paso 3 — Tabla de signos de f'(x):
  Intervalo      | Prueba  | f'(x)  | f comportamiento
  ───────────────┼─────────┼────────┼──────────────────
  x < -1        | x = -2  |   +    | Creciente ↑
  -1 < x < 3   | x = 0   |   -    | Decreciente ↓
  x > 3        | x = 4   |   +    | Creciente ↑

Conclusión:
  x = -1: f' cambia (+)→(-)  →  MÁXIMO LOCAL
  x = 3:  f' cambia (-)→(+)  →  MÍNIMO LOCAL

Paso 4 — Valores:
  f(-1) = (-1)³ - 3(1) - 9(-1) + 5 = -1 - 3 + 9 + 5 = 10  → máximo local
  f(3)  = 27 - 27 - 27 + 5 = -22                             → mínimo local
```

---

## 2. Criterio de la Segunda Derivada

Método alternativo para clasificar puntos críticos cuando f''(c) es fácil de calcular.

```
Si f'(c) = 0 (punto crítico) y:
  f''(c) > 0  →  MÍNIMO LOCAL  (concavidad hacia arriba ∪)
  f''(c) < 0  →  MÁXIMO LOCAL  (concavidad hacia abajo ∩)
  f''(c) = 0  →  INCONCLUSO    (usar criterio de la primera derivada)
```

**Aplicando al ejemplo anterior:**
```
f'(x)  = 3x² - 6x - 9
f''(x) = 6x - 6

En x = -1:  f''(-1) = 6(-1) - 6 = -12 < 0  →  MÁXIMO LOCAL ✓
En x = 3:   f''(3)  = 6(3)  - 6 = 12  > 0  →  MÍNIMO LOCAL ✓
```

---

## 3. Concavidad y Puntos de Inflexión

### Concavidad

| Condición | Geometría | Significado |
|:---|:---:|:---|
| f''(x) > 0 en (a, b) | ∪ | La curva es CÓNCAVA HACIA ARRIBA en (a, b) |
| f''(x) < 0 en (a, b) | ∩ | La curva es CÓNCAVA HACIA ABAJO en (a, b) |

**Regla mnemotécnica:**
- `f'' > 0`: la curva "sonríe" (cóncava arriba, como un vaso que retiene agua).
- `f'' < 0`: la curva "frunce" (cóncava abajo, como un arco invertido).

### Punto de inflexión

Un **punto de inflexión** en x = c ocurre cuando:
1. f''(c) = 0 (o f''(c) no existe).
2. f'' **cambia de signo** en x = c (la concavidad cambia).

> **Atención:** Si f''(c) = 0 pero f'' no cambia de signo, NO es punto de inflexión.

### Ejemplo resuelto

```
f(x) = x⁴ - 4x³

Paso 1 — Derivadas:
  f'(x)  = 4x³ - 12x²
  f''(x) = 12x² - 24x = 12x(x - 2)

Paso 2 — Puntos de inflexión (f''(x) = 0):
  12x(x - 2) = 0  →  x = 0  o  x = 2

Paso 3 — Tabla de signos de f''(x):
  Intervalo  | Prueba  | f''(x) | Concavidad
  ───────────┼─────────┼────────┼──────────────
  x < 0     | x = -1  |   +    | Cóncava ↑ (∪)
  0 < x < 2 | x = 1   |   -    | Cóncava ↓ (∩)
  x > 2     | x = 3   |   +    | Cóncava ↑ (∪)

Paso 4 — Verificar cambio de signo:
  x = 0: f'' cambia (+)→(-)  →  PUNTO DE INFLEXIÓN
  x = 2: f'' cambia (-)→(+)  →  PUNTO DE INFLEXIÓN

Paso 5 — Coordenadas:
  f(0) = 0    →  inflexión en (0, 0)
  f(2) = 16 - 32 = -16  →  inflexión en (2, -16)

Paso 6 — Análisis de extremos con f'(x) = 4x³ - 12x² = 4x²(x - 3):
  Puntos críticos: x = 0 (doble) y x = 3
  f''(0) = 0  →  INCONCLUSO (usar criterio 1)
  f''(3) = 12(9) - 24(3) = 108 - 72 = 36 > 0  →  MÍNIMO LOCAL
  f(3) = 81 - 108 = -27
```

---

## 4. Análisis Completo de una Función (Trazado de Curva)

Para analizar completamente una función se estudian todos estos elementos:

```
1. Dominio de la función
2. Interceptos (intersecciones con ejes x e y)
3. Simetría (par, impar, ni par ni impar)
4. Asíntotas (verticales, horizontales, oblicuas)
5. Intervalos de crecimiento/decrecimiento (f')
6. Máximos y mínimos locales (f' = 0)
7. Concavidad e inflexiones (f'')
8. Gráfico
```

### Análisis completo — Ejemplo

```
f(x) = x³ - 6x² + 9x + 1

1. DOMINIO: (-∞, +∞) — polinomio, siempre definido.

2. INTERCEPTOS:
   y: f(0) = 1  →  (0, 1)
   x: x³ - 6x² + 9x + 1 = 0  (difícil de factorizar; omitir o usar calculadora)

3. DERIVADA PRIMERA:
   f'(x) = 3x² - 12x + 9 = 3(x² - 4x + 3) = 3(x - 1)(x - 3)
   
   Puntos críticos: x = 1  y  x = 3

   Signos de f'(x):
   x < 1:   f'(0) = 3(1)(−3) = −9 < 0  →  Decreciente... espera:
   x < 1:   f'(0) = 9 > 0  →  Creciente ↑
   1 < x < 3: f'(2) = 3(1)(−1) < 0  →  Decreciente ↓
   x > 3:   f'(4) = 3(3)(1) > 0  →  Creciente ↑

   Extremos:
   x = 1: (+)→(−)  →  MÁXIMO LOCAL   f(1) = 1 - 6 + 9 + 1 = 5
   x = 3: (−)→(+)  →  MÍNIMO LOCAL   f(3) = 27 - 54 + 27 + 1 = 1

4. DERIVADA SEGUNDA:
   f''(x) = 6x - 12

   Inflexiones (f'' = 0): 6x - 12 = 0  →  x = 2
   f''(2) = 0 ✓ (punto candidato)
   
   Signos: x < 2: f''(1) = -6 < 0 (cóncava ↓)
           x > 2: f''(3) =  6 > 0 (cóncava ↑)
   f'' cambia de signo  →  PUNTO DE INFLEXIÓN en x = 2
   f(2) = 8 - 24 + 18 + 1 = 3  →  inflexión en (2, 3)

5. RESUMEN:
   - Crece en (-∞, 1) y (3, +∞)
   - Decrece en (1, 3)
   - Máximo local: (1, 5)
   - Mínimo local: (3, 1)
   - Cóncava abajo en (-∞, 2)
   - Cóncava arriba en (2, +∞)
   - Punto de inflexión: (2, 3)
```

---

## 5. Problemas de Optimización

La optimización usa las derivadas para encontrar el **máximo o mínimo absoluto** de una función en un contexto de aplicación real.

### Procedimiento general

```
1. Leer el problema e identificar: ¿qué se quiere maximizar o minimizar?
2. Definir variables y escribir la función objetivo.
3. Si hay restricción, expresar una variable en términos de la otra.
4. Derivar la función objetivo.
5. Encontrar los puntos críticos (f' = 0).
6. Verificar con f'' o tabla de signos si es máximo o mínimo.
7. Calcular el valor de la función en ese punto.
8. Interpretar el resultado en el contexto del problema.
```

### Ejemplo 1 — Área máxima con perímetro fijo

```
Problema: Un agricultor tiene 200 m de cerca y quiere cercar un área rectangular.
¿Cuáles son las dimensiones que maximizan el área?

Paso 1 — Variables:
  Largo = x,  Ancho = y
  Función objetivo: A = x · y   (maximizar)
  Restricción: 2x + 2y = 200  →  x + y = 100  →  y = 100 - x

Paso 2 — Sustituir en la función objetivo:
  A(x) = x(100 - x) = 100x - x²

Paso 3 — Derivar y encontrar punto crítico:
  A'(x) = 100 - 2x = 0
  x = 50

Paso 4 — Verificar con segunda derivada:
  A''(x) = -2 < 0  →  MÁXIMO ✓

Paso 5 — Dimensiones y área:
  x = 50 m,  y = 100 - 50 = 50 m
  A = 50 × 50 = 2500 m²

Respuesta: El cuadrado de 50 m × 50 m maximiza el área (2500 m²).
```

### Ejemplo 2 — Costo mínimo de fabricación

```
Problema: Una lata cilíndrica debe contener 500π cm³.
El material de la tapa y base cuesta el doble que el lateral.
¿Qué dimensiones minimizan el costo total?

Fórmulas:
  Volumen:     V = π·r²·h = 500π  →  h = 500/r²
  Área lateral: A_lat = 2π·r·h
  Área base+tapa: A_bt = 2π·r²

  Costo (costo lateral = c, base/tapa = 2c):
  C = c·2π·r·h + 2c·2π·r²  (factorizamos c)
  C(r) = 2πc·r·(500/r²) + 4πc·r²
       = 1000πc/r + 4πc·r²

  Derivar respecto a r:
  C'(r) = -1000πc/r² + 8πc·r = 0
  8πc·r = 1000πc/r²
  8r³ = 1000
  r³ = 125
  r = 5 cm

  h = 500/r² = 500/25 = 20 cm

  C''(r) = 2000πc/r³ + 8πc > 0  →  MÍNIMO ✓

Respuesta: r = 5 cm, h = 20 cm minimizan el costo.
```

### Ejemplo 3 — Distancia mínima

```
Problema: ¿Qué punto de la parábola y = x² está más cerca al punto (3, 0)?

La distancia al cuadrado (más fácil de minimizar):
  D² = (x - 3)² + (y - 0)² = (x - 3)² + (x²)²

  f(x) = (x - 3)² + x⁴

  f'(x) = 2(x - 3) + 4x³ = 0
  4x³ + 2x - 6 = 0
  2x³ + x - 3 = 0

Probar x = 1: 2(1) + 1 - 3 = 0 ✓

  El punto es (1, 1²) = (1, 1)
  Distancia = √((1-3)² + 1²) = √(4 + 1) = √5 ≈ 2.24
```

---

## 6. Máximos y Mínimos Absolutos en un Intervalo Cerrado [a, b]

**Teorema de valor extremo:** Si f es continua en [a, b], entonces f alcanza un máximo absoluto y un mínimo absoluto en ese intervalo.

### Procedimiento

```
1. Encontrar todos los puntos críticos en el interior (a, b) donde f'(x) = 0 o f'(x) no existe.
2. Evaluar f en los puntos críticos y en los extremos del intervalo: a y b.
3. El valor más grande es el MÁXIMO ABSOLUTO; el más pequeño es el MÍNIMO ABSOLUTO.
```

### Ejemplo

```
f(x) = x³ - 3x + 2    en    [-2, 3]

f'(x) = 3x² - 3 = 3(x² - 1) = 3(x - 1)(x + 1) = 0
Puntos críticos: x = -1 y x = 1 (ambos en [-2, 3])

Evaluar:
  f(-2) = -8 + 6 + 2 = 0
  f(-1) = -1 + 3 + 2 = 4      ← Máximo absoluto
  f(1)  =  1 - 3 + 2 = 0
  f(3)  = 27 - 9 + 2 = 20     ← Máximo absoluto

  Mínimo absoluto: 0 (en x = -2 y x = 1)
  Máximo absoluto: 20 (en x = 3)
```

---

## 7. Errores Comunes

| Error | Descripción | Corrección |
|:---|:---|:---|
| Confundir máximo local con absoluto | El máximo local puede no ser el mayor valor global | Evaluar en todo el dominio o en [a,b] |
| Olvidar verificar el cambio de signo de f'' | f''(c) = 0 no implica punto de inflexión | Verificar que f'' cambia de signo |
| No evaluar en extremos del intervalo | Encontrar solo puntos críticos interiores | Siempre evaluar f en a y b también |
| Confundir puntos críticos con puntos de inflexión | f'(c) = 0 puede ser máximo, mínimo o inflexión | Analizar f'' o la tabla de signos |
| Error en optimización: no validar dominio | Radio o longitud negativos | Establecer restricciones de dominio antes de derivar |

---

## 8. Métodos de Estudio

### Active Recall — Preguntas

1. Enuncia el criterio de la segunda derivada para clasificar puntos críticos.
2. ¿Cuándo existe un punto de inflexión en x = c?
3. ¿Cuál es la diferencia entre un extremo local y uno absoluto?
4. ¿Por qué en la optimización hay que evaluar también los extremos del intervalo?
5. Traza la gráfica aproximada de f(x) = x³ - 6x² + 9x usando solo la información de f' y f''.

### Ejercicios de práctica

```
1. Encontrar extremos locales de f(x) = 2x³ + 3x² - 12x + 1
   [Resp: Máx local (−2, 21), Mín local (1, −6)]

2. Encontrar puntos de inflexión de f(x) = x⁴ - 6x²
   [Resp: inflexiones en x = ±1]

3. Maximizar el área de un triángulo rectángulo con hipotenusa fija h.
   [Resp: triángulo isósceles, cada cateto = h/√2]

4. Una empresa produce x unidades a un costo C(x) = 2x² - 8x + 20.
   ¿Cuántas unidades minimizan el costo? ¿Cuál es ese costo mínimo?
   [Resp: x = 2, C_min = 12]
```

---

## 9. Recursos Externos

| Recurso | Descripción | URL |
|:---|:---|:---|
| **Matemáticas profe Alex** | Máximos y mínimos, concavidad, problemas de optimización resueltos | https://www.youtube.com/@matematicasprofealex |
| **Math2Me** | Optimización y trazado de curvas con ejemplos de examen | https://www.youtube.com/@math2me |
| **Salvador FI** | Análisis completo de funciones — crecimiento, concavidad, inflexiones | https://www.youtube.com/@SalvadorFI |
| **Mateguapo** | Optimización desde nivel básico, enfoque en comprensión lógica | https://www.youtube.com/@mateguapo |
| **Desmos** | Graficar funciones para verificar resultados visualmente | https://www.desmos.com/calculator |
| **Stewart — Cálculo Cap. 4** | Valores extremos, regla de L'Hôpital, optimización | Biblioteca UDC |

---

## 10. Referencia Rápida

```
CLASIFICACIÓN DE PUNTOS CRÍTICOS

  Criterio de la 1ª derivada:
    f' cambia (+)→(−) en c  →  Máximo local
    f' cambia (−)→(+) en c  →  Mínimo local
    f' no cambia de signo    →  Ni máximo ni mínimo

  Criterio de la 2ª derivada:
    f'(c) = 0 y f''(c) < 0  →  Máximo local
    f'(c) = 0 y f''(c) > 0  →  Mínimo local
    f'(c) = 0 y f''(c) = 0  →  Inconcluso (usar criterio 1)

CONCAVIDAD
  f''(x) > 0 en (a,b)  →  Cóncava hacia arriba ∪
  f''(x) < 0 en (a,b)  →  Cóncava hacia abajo ∩

PUNTO DE INFLEXIÓN EN x = c
  Condición: f''(c) = 0  Y  f'' cambia de signo en c

MÁXIMOS/MÍNIMOS ABSOLUTOS en [a, b]
  1. Puntos críticos en (a, b)
  2. Evaluar f en críticos, a y b
  3. Mayor valor = máximo absoluto
     Menor valor = mínimo absoluto

OPTIMIZACIÓN — PASOS CLAVE
  1. Variable a optimizar (función objetivo)
  2. Restricción → expresar en una sola variable
  3. Derivar e igualar a 0
  4. Verificar que es máximo/mínimo
  5. Calcular todos los valores e interpretar

CRECIMIENTO / DECRECIMIENTO
  f'(x) > 0  →  f creciente en ese intervalo
  f'(x) < 0  →  f decreciente en ese intervalo
  f'(x) = 0  →  f constante en ese punto (posible extremo)
```
