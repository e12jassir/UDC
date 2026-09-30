# Apuntes — Unidad 1: Límites y Continuidad
**Asignatura:** Cálculo Diferencial · CFBD243-B1
**Docente:** Katherine Paternina Sierra
**Última actualización:** 2026-09-29

---

## 1. Concepto Intuitivo de Límite

El límite de una función describe el comportamiento de f(x) cuando x se acerca a un valor c, sin necesariamente llegar a ese valor.

**Idea central:** No importa lo que pasa *en* x = c. Importa lo que pasa cuando x se *aproxima* a c.

### Notación

```
lim f(x) = L
x → c
```

Se lee: "El límite de f(x) cuando x tiende a c es igual a L."

### Ejemplo intuitivo

```
f(x) = (x^2 - 1) / (x - 1)

¿Qué pasa cuando x → 1?
Si sustituimos x = 1: f(1) = (1 - 1)/(1 - 1) = 0/0  → INDETERMINACIÓN

Pero si factorizamos:
  (x^2 - 1) / (x - 1) = (x - 1)(x + 1) / (x - 1) = x + 1   (para x ≠ 1)

Por lo tanto:
  lim (x^2 - 1)/(x - 1) = lim (x + 1) = 1 + 1 = 2
  x→1                      x→1
```

La función no existe en x = 1, pero su límite sí existe y vale 2.

---

## 2. Definición Formal de Límite (Definición Épsilon-Delta)

Para los cursos de ingeniería, la definición formal se presenta como marco conceptual:

```
lim f(x) = L   si y solo si:
x → c

Para todo ε > 0, existe δ > 0 tal que:
  si 0 < |x - c| < δ,  entonces  |f(x) - L| < ε
```

**Traducción práctica:** Se puede hacer f(x) tan cercana a L como se quiera, siempre que x esté suficientemente cerca de c (pero no igual a c).

> En el nivel del curso, lo que realmente se evalúa es la capacidad de calcular límites correctamente, no de demostrar épsilon-delta. La definición sirve para entender *por qué* los límites no dependen del valor en el punto.

---

## 3. Propiedades de los Límites

Si lim f(x) = L y lim g(x) = M (ambos existen y son finitos), entonces:
     x→c            x→c

| Propiedad | Fórmula | Ejemplo |
|:---|:---|:---|
| **Suma** | lim [f(x) + g(x)] = L + M | lim [x² + x] = 4 + 2 = 6 (x→2) |
| **Diferencia** | lim [f(x) - g(x)] = L - M | lim [x² - x] = 4 - 2 = 2 (x→2) |
| **Producto** | lim [f(x) · g(x)] = L · M | lim [x² · x] = 4 · 2 = 8 (x→2) |
| **Cociente** | lim [f(x)/g(x)] = L/M (si M ≠ 0) | lim [x²/x] = 4/2 = 2 (x→2) |
| **Potencia** | lim [f(x)]^n = L^n | lim [x]³ = 2³ = 8 (x→2) |
| **Raíz** | lim √f(x) = √L (si L ≥ 0) | lim √x = √4 = 2 (x→4) |
| **Constante** | lim k = k | lim 7 = 7 |
| **Identidad** | lim x = c | lim x = 3 (x→3) |

---

## 4. Técnicas para Calcular Límites

### Técnica 1: Sustitución directa

El método más simple. Si f(c) existe y no produce indeterminación, ese es el límite.

```
Calcular:  lim (3x² - 2x + 1)
           x→2

Sustituir: 3(2)² - 2(2) + 1 = 3(4) - 4 + 1 = 12 - 4 + 1 = 9

Respuesta: lim (3x² - 2x + 1) = 9
           x→2
```

### Técnica 2: Factorización (para indeterminación 0/0)

Cuando la sustitución da 0/0, factorizar numerador y denominador para cancelar el factor común.

**Ejemplo resuelto paso a paso:**
```
Calcular:  lim  (x² - 5x + 6) / (x - 3)
           x→3

Paso 1 — Verificar indeterminación:
  Sustituir x = 3: (9 - 15 + 6)/(3 - 3) = 0/0 ✓ Indeterminado

Paso 2 — Factorizar el numerador:
  x² - 5x + 6 = (x - 2)(x - 3)

Paso 3 — Cancelar el factor común (x - 3):
  (x - 2)(x - 3) / (x - 3) = (x - 2)   para x ≠ 3

Paso 4 — Evaluar el límite simplificado:
  lim (x - 2) = 3 - 2 = 1
  x→3

Respuesta: lim (x² - 5x + 6)/(x - 3) = 1
           x→3
```

### Técnica 3: Racionalización (cuando hay raíces)

Multiplicar por el conjugado para eliminar la raíz del numerador o denominador.

**Ejemplo:**
```
Calcular:  lim  (√x - 2) / (x - 4)
           x→4

Paso 1 — Verificar: (√4 - 2)/(4 - 4) = 0/0 ✓

Paso 2 — Multiplicar por conjugado (√x + 2)/(√x + 2):
  [(√x - 2)(√x + 2)] / [(x - 4)(√x + 2)]
  = (x - 4) / [(x - 4)(√x + 2)]

Paso 3 — Cancelar (x - 4):
  = 1 / (√x + 2)

Paso 4 — Evaluar:
  lim 1/(√x + 2) = 1/(√4 + 2) = 1/(2 + 2) = 1/4
  x→4

Respuesta: 1/4
```

### Técnica 4: Límites con fracciones complejas

Multiplicar numerador y denominador por el mínimo común denominador de las fracciones internas.

**Ejemplo:**
```
Calcular:  lim  [1/x - 1/3] / (x - 3)
           x→3

Paso 1: Verificar → 0/0 ✓

Paso 2: Simplificar [1/x - 1/3] con denominador común 3x:
  [3/(3x) - x/(3x)] = (3 - x)/(3x)

Paso 3: Reescribir el límite:
  [(3 - x)/(3x)] / (x - 3)
  = (3 - x) / [3x(x - 3)]
  = -(x - 3) / [3x(x - 3)]
  = -1/(3x)

Paso 4: Evaluar:
  lim -1/(3x) = -1/(3·3) = -1/9
  x→3

Respuesta: -1/9
```

---

## 5. Límites Laterales

Los límites laterales evalúan el comportamiento de f(x) cuando x se aproxima a c desde un solo lado.

```
Límite por la derecha:  lim f(x)   (x → c⁺, x viene de valores mayores que c)
                        x→c⁺

Límite por la izquierda: lim f(x)  (x → c⁻, x viene de valores menores que c)
                         x→c⁻
```

### Condición de existencia del límite bilateral

```
El lim f(x) EXISTE   si y solo si:
   x→c

  lim f(x) = lim f(x) = L
  x→c⁺      x→c⁻

Si los límites laterales son diferentes, el límite bilateral NO EXISTE.
```

### Ejemplo con función a trozos

```
       { x + 1,   si x < 2
f(x) = { 5,       si x = 2
       { x² - 1,  si x > 2

Calcular lim f(x)
         x→2

Límite por la izquierda (usar x + 1):
  lim (x + 1) = 2 + 1 = 3
  x→2⁻

Límite por la derecha (usar x² - 1):
  lim (x² - 1) = (2)² - 1 = 4 - 1 = 3
  x→2⁺

Como 3 = 3, el límite existe: lim f(x) = 3
                               x→2

Nota: f(2) = 5 ≠ 3, pero el LÍMITE sí es 3. Son conceptos distintos.
```

### Ejemplo donde el límite NO existe

```
f(x) = |x| / x

lim f(x):
x→0

Por la derecha (x > 0): |x|/x = x/x = 1   → lim = 1
                                             x→0⁺
Por la izquierda (x < 0): |x|/x = -x/x = -1 → lim = -1
                                                x→0⁻
Como 1 ≠ -1, el lim |x|/x NO EXISTE.
              x→0
```

---

## 6. Límites al Infinito

Describen el comportamiento de f(x) cuando x crece sin límite (x → +∞ o x → −∞).

### Reglas básicas para límites al infinito de polinomios y racionales

```
Regla 1: Para un polinomio, solo importa el TÉRMINO DE MAYOR GRADO.
  lim (3x³ - 7x + 2) = lim 3x³ = +∞
  x→+∞                x→+∞

Regla 2: Para una función racional f(x) = P(x)/Q(x):
  - Si grado(P) < grado(Q):  límite = 0
  - Si grado(P) = grado(Q):  límite = coef. líder(P) / coef. líder(Q)
  - Si grado(P) > grado(Q):  límite = ±∞
```

**Ejemplos:**
```
a) lim  (2x + 3) / (5x - 1)     → grados iguales → 2/5
   x→∞

b) lim  (x² + 1) / (x³ - 2)    → grado num < grado den → 0
   x→∞

c) lim  (x³ + x) / (x² - 1)    → grado num > grado den → +∞
   x→∞
```

**Ejemplo resuelto con división:**
```
Calcular:  lim  (4x² - 3x + 1) / (2x² + x - 5)
           x→∞

Dividir todo por x² (el mayor grado):
  = (4 - 3/x + 1/x²) / (2 + 1/x - 5/x²)

Cuando x → ∞: los términos con /x y /x² → 0

  = (4 - 0 + 0) / (2 + 0 - 0) = 4/2 = 2

Respuesta: 2
```

---

## 7. Indeterminaciones Frecuentes

| Forma | Nombre | Técnica recomendada |
|:---:|:---|:---|
| 0/0 | Indeterminado tipo 0/0 | Factorizar, racionalizar, simplificar |
| ∞/∞ | Indeterminado tipo ∞/∞ | Dividir por el mayor grado, L'Hôpital* |
| 0 · ∞ | Producto indeterminado | Reescribir como cociente |
| ∞ - ∞ | Diferencia indeterminada | Racionalizar o combinar fracciones |
| 1^∞ | Forma indeterminada 1 elevado a infinito | Logaritmo + exponencial |
| 0^0 | Forma indeterminada cero a la cero | Logaritmo + exponencial |

*L'Hôpital se verá en unidades posteriores.

---

## 8. Continuidad

Una función f es **continua en x = c** si y solo si se cumplen las tres condiciones simultáneamente:

```
Condición 1: f(c) está definida (el punto existe)
Condición 2: lim f(x) existe (los límites laterales son iguales)
             x→c
Condición 3: lim f(x) = f(c)  (el límite coincide con el valor)
             x→c
```

Si falla **cualquiera** de las tres, hay discontinuidad en x = c.

### Tipos de discontinuidades

| Tipo | Descripción | Ejemplo visual |
|:---|:---|:---|
| **Evitable (Removible)** | El límite existe pero f(c) no está definida o f(c) ≠ lim | Función con "hueco" |
| **De salto** | Los límites laterales existen pero son distintos | Función escalón |
| **Infinita (Esencial)** | El límite es ±∞ (asíntota vertical) | f(x) = 1/x en x = 0 |

### Ejemplo de verificación de continuidad

```
f(x) = (x² - 4) / (x - 2)

En x = 2:
  Condición 1: f(2) = (4-4)/(2-2) = 0/0 → NO DEFINIDA ✗

  El límite:
  lim (x²-4)/(x-2) = lim (x-2)(x+2)/(x-2) = lim (x+2) = 4
  x→2                x→2                      x→2

Conclusión: f NO es continua en x = 2 (discontinuidad evitable).
Si definimos f(2) = 4, la función se vuelve continua en ese punto.
```

### Funciones continuas en todo su dominio

Las siguientes funciones son continuas en cada punto de su dominio natural:
- Polinomios (todo R)
- Funciones racionales (excepto donde el denominador = 0)
- Raíces cuadradas (donde el radicando ≥ 0)
- sen(x), cos(x) (todo R)
- e^x, ln(x) (donde estén definidas)

---

## 9. Ejemplos Resueltos Completos

### Ejemplo 1 — Límite con indeterminación, factorización

```
lim  (x² + x - 6) / (x² - 4)
x→2

Paso 1: Sustituir x = 2 → (4 + 2 - 6)/(4 - 4) = 0/0 → indeterminado

Paso 2: Factorizar
  Numerador: x² + x - 6 = (x + 3)(x - 2)
  Denominador: x² - 4 = (x - 2)(x + 2)

Paso 3: Simplificar
  (x + 3)(x - 2) / [(x - 2)(x + 2)] = (x + 3)/(x + 2)

Paso 4: Evaluar
  lim (x + 3)/(x + 2) = (2 + 3)/(2 + 2) = 5/4
  x→2

Respuesta: 5/4
```

### Ejemplo 2 — Límite al infinito

```
lim  (3x³ - 2x + 7) / (6x³ + x² - 1)
x→∞

Dividir por x³:
  = (3 - 2/x² + 7/x³) / (6 + 1/x - 1/x³)

Cuando x → ∞, todos los términos fraccionarios → 0:
  = 3/6 = 1/2

Respuesta: 1/2
```

### Ejemplo 3 — Verificación de continuidad en función a trozos

```
       { 2x + 1,   si x ≤ 1
f(x) = { x² + 2,   si x > 1

¿Es continua en x = 1?

Cond. 1: f(1) = 2(1) + 1 = 3 ✓ (definida)

Cond. 2:
  lim  = lim (2x + 1) = 3      (izquierda)
  x→1⁻
  lim  = lim (x² + 2) = 1 + 2 = 3  (derecha)
  x→1⁺
  Como ambos = 3, el límite existe y = 3 ✓

Cond. 3: lim = 3 = f(1) ✓

Conclusión: f ES CONTINUA en x = 1.
```

---

## 10. Errores Comunes

| Error | Descripción | Corrección |
|:---|:---|:---|
| Ignorar la indeterminación | Hacer lim directamente sin verificar si da 0/0 | Siempre sustituir primero para clasificar el caso |
| Cancelar factores sin restricción | Cancelar sin anotar "para x ≠ c" | El límite opera cuando x → c, no en c. La cancelación es válida. |
| Confundir límite con valor de función | Creer que lim f(x) = f(c) siempre | El límite puede existir aunque f(c) no esté definida |
| Olvidar verificar límites laterales | Concluir que el límite existe sin verificar ambos lados | Siempre verificar lim⁺ y lim⁻ en funciones a trozos |
| Dividir erróneamente al infinito | Dividir por x en vez de x^n (grado máximo) | Dividir por el monomio de mayor grado |

---

## 11. Métodos de Estudio

### Active Recall — Preguntas

1. ¿Cuáles son las tres condiciones de continuidad? Escríbelas de memoria.
2. ¿En qué se diferencian los límites laterales del límite bilateral?
3. ¿Qué tipo de indeterminación produce la función (x²-4)/(x-2) en x=2?
4. ¿Qué técnica usas cuando el límite produce ∞/∞?
5. ¿Cuándo es una discontinuidad "evitable"? Pon un ejemplo.
6. ¿Por qué es válido cancelar el factor (x-c) si x ≠ c en un límite?

### Hoja de práctica recomendada

Resolver los siguientes límites (mínimo 10 minutos cada uno sin ver soluciones):

```
1. lim (x² - 9)/(x - 3)                          [Resp: 6]
   x→3

2. lim (x² + 2x - 8)/(x - 2)                     [Resp: 6]
   x→2

3. lim (√x - 3)/(x - 9)                          [Resp: 1/6]
   x→9

4. lim (5x² - 3x + 1)/(2x² + x - 4)             [Resp: 5/2]
   x→∞

5. lim (2x³ - x) / (x² + 1)                      [Resp: +∞]
   x→∞
```

---

## 12. Recursos Externos

| Recurso | Descripción | URL |
|:---|:---|:---|
| **Math2Me** | Canal en español, playlist de límites con ejercicios resueltos paso a paso | https://www.youtube.com/@math2me |
| **Matemáticas profe Alex** | Explicaciones de límites, indeterminaciones y continuidad con muchos ejemplos de examen | https://www.youtube.com/@matematicasprofealex |
| **Khan Academy Español** | Ruta estructurada de límites con ejercicios interactivos | https://es.khanacademy.org/math/calculus-1 |
| **Stewart — Cálculo (Cap. 2)** | Límites y continuidad — la referencia estándar del curso | Biblioteca física UDC / PDF académico |
| **Desmos** | Graficar funciones para visualizar límites y discontinuidades | https://www.desmos.com/calculator |
| **WolframAlpha** | Verificar límites calculados | https://www.wolframalpha.com |

---

## 13. Referencia Rápida

```
NOTACIÓN
  lim f(x) = L     límite bilateral
  x→c
  lim f(x)         límite por la derecha (x > c)
  x→c⁺
  lim f(x)         límite por la izquierda (x < c)
  x→c⁻

EXISTENCIA DEL LÍMITE
  lim f(x) existe  ⟺  lim⁺ = lim⁻ = L
  x→c                  x→c    x→c

INDETERMINACIONES → TÉCNICA
  0/0   → factorizar, racionalizar, simplificar
  ∞/∞   → dividir por mayor potencia de x

LÍMITES AL INFINITO (función racional)
  grado num < grado den  →  0
  grado num = grado den  →  ratio de coeficientes líderes
  grado num > grado den  →  ±∞

CONTINUIDAD EN x = c (las 3 condiciones)
  1. f(c) existe
  2. lim f(x) existe
     x→c
  3. lim f(x) = f(c)
     x→c

TIPOS DE DISCONTINUIDAD
  Evitable  → lim existe, pero f(c) ≠ lim o no está definida
  Salto     → lim⁺ ≠ lim⁻ (ambos finitos)
  Infinita  → lim = ±∞ (asíntota vertical)
```
