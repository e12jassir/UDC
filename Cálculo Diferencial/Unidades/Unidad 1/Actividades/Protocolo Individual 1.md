# Protocolo Individual — Unidad 1: Casos de Factorización

**Asignatura:** Cálculo Diferencial  
**Estudiante:** Esteban David Marrugo Jassir  
**Docente:** Katherine Paternina Sierra  
**Fecha de Entrega:** 15 de Agosto de 2026 (SIMA - 23:59 hs)  
**Modalidad:** Elaborado a mano individualmente  

---

### 1. Descripción de la actividad
Desarrollo paso a paso de los 7 principales casos de factorización aplicados en Cálculo Diferencial. Por cada caso se resuelven 3 ejercicios estructurados en niveles de dificultad: **Básico**, **Intermedio** y **Avanzado** (21 ejercicios en total), detallando verificación de condiciones, procedimiento algebraico y respuesta final.

---

### 2. Palabras clave
Factorización, Factor Común, Agrupación de Términos, Diferencia de Cuadrados, Trinomio Cuadrado Perfecto, Trinomio Cuadrático, Cubos Perfectos.

---

### 3. Objetivo de la actividad
- Identificar con precisión la estructura algebraica de un polinomio para seleccionar el método de factorización adecuado.
- Desarrollar destreza operativa en la simplificación de expresiones algebraicas mediante ejercicios con dificultad progresiva.
- Consolidar las bases algebraicas indispensables para el cálculo de límites indeterminados y la simplificación de funciones racionales.

---

### 4. Resumen Teórico de los 7 Casos de Factorización

| # | Caso de Factorización | Condición / Identificación | Estructura / Modelo General |
|---|---|---|---|
| **1** | **Factor Común** | Coeficiente MCD o variables/paréntesis comunes en todos los términos. | $ab + ac = a(b + c)$ |
| **2** | **Factor Común por Agrupación** | Polinomios de 4, 6 o más términos pares sin factor común global. | $ax + bx + ay + by = (a+b)(x+y)$ |
| **3** | **Diferencia de Cuadrados** | Binomio con signo menos y raíces cuadradas exactas. | $a^2 - b^2 = (a - b)(a + b)$ |
| **4** | **Trinomio Cuadrado Perfecto (TCP)** | Trinomio ordenado donde el 2.º término es $2\sqrt{t_1}\sqrt{t_3}$. | $a^2 \pm 2ab + b^2 = (a \pm b)^2$ |
| **5** | **Trinomio $x^{2n} + bx^n + c$** | Coeficiente principal igual a 1; exponente del 1.º término es el doble del 2.º. | $x^2 + (p+q)x + pq = (x+p)(x+q)$ |
| **6** | **Trinomio $ax^{2n} + bx^n + c$** | Coeficiente principal $a > 1$; se multiplica y divide por $a$. | $ax^2 + bx + c = \frac{(ax+p)(ax+q)}{a}$ |
| **7** | **Suma o Diferencia de Cubos** | Binomio de raíces cúbicas exactas. | $a^3 \pm b^3 = (a \pm b)(a^2 \mp ab + b^2)$ |

---

### 5. Desarrollo Práctico del Protocolo (21 Ejercicios Resueltos)

---

#### CASO 1: Factor Común

##### 🔹 Ejercicio 1.1 (Nivel Básico)
**Enunciado:** Factorizar $6x^3 - 9x^2$

* **Paso 1 (MCD de coeficientes):** $\text{MCD}(6, 9) = 3$.
* **Paso 2 (Menor exponente de $x$):** El menor exponente es $x^2$.
* **Paso 3 (Factor común):** $\text{Factor Común} = 3x^2$.
* **Paso 4 (División de términos):**
  $$\frac{6x^3}{3x^2} = 2x, \quad \frac{-9x^2}{3x^2} = -3$$
* **Respuesta Final:** $3x^2(2x - 3)$

---

##### 🔸 Ejercicio 1.2 (Nivel Intermedio)
**Enunciado:** Factorizar $12a^2b^3c - 18ab^4c^2 + 24a^3b^2c^3$

* **Paso 1 (MCD de coeficientes):** $\text{MCD}(12, 18, 24) = 6$.
* **Paso 2 (Menor exponente de variables):** $a^1$, $b^2$, $c^1$.
* **Paso 3 (Factor común):** $\text{Factor Común} = 6ab^2c$.
* **Paso 4 (División de términos):**
  $$\frac{12a^2b^3c}{6ab^2c} = 2ab, \quad \frac{-18ab^4c^2}{6ab^2c} = -3b^2c, \quad \frac{24a^3b^2c^3}{6ab^2c} = 4a^2c^2$$
* **Respuesta Final:** $6ab^2c(2ab - 3b^2c + 4a^2c^2)$

---

##### 🔻 Ejercicio 1.3 (Nivel Avanzado)
**Enunciado:** Factorizar $(2x + 1)(x - 3) - 5(x - 3) + 3x(x - 3)$

* **Paso 1 (Identificar expresión común):** El binomio $(x - 3)$ está presente en todos los términos.
* **Paso 2 (Extraer factor común polínomico):**
  $$(x - 3) \cdot \left[ (2x + 1) - 5 + 3x \right]$$
* **Paso 3 (Simplificar términos semejantes dentro del corchete):**
  $$2x + 3x + 1 - 5 = 5x - 4$$
* **Respuesta Final:** $(x - 3)(5x - 4)$

---

#### CASO 2: Factor Común por Agrupación de Términos

##### 🔹 Ejercicio 2.1 (Nivel Básico)
**Enunciado:** Factorizar $ax + bx + ay + by$

* **Paso 1 (Agrupar de a dos términos):** $(ax + bx) + (ay + by)$
* **Paso 2 (Factor común de cada grupo):** $x(a + b) + y(a + b)$
* **Paso 3 (Factor común del polinomio $(a+b)$):**
* **Respuesta Final:** $(a + b)(x + y)$

---

##### 🔸 Ejercicio 2.2 (Nivel Intermedio)
**Enunciado:** Factorizar $3x^3 - 12x^2 + 2x - 8$

* **Paso 1 (Agrupar términos):** $(3x^3 - 12x^2) + (2x - 8)$
* **Paso 2 (Factor común de cada grupo):**
  $$\text{Grupo 1: } 3x^2(x - 4)$$
  $$\text{Grupo 2: } 2(x - 4)$$
* **Paso 3 (Unir y extraer factor $(x - 4)$):** $3x^2(x - 4) + 2(x - 4)$
* **Respuesta Final:** $(x - 4)(3x^2 + 2)$

---

##### 🔻 Ejercicio 2.3 (Nivel Avanzado)
**Enunciado:** Factorizar $2ac - 5bd - 2a + 2ad + 5b - 5bc$

* **Paso 1 (Reordenar por coeficientes afines):** $(2ac - 2a + 2ad) + (-5bc + 5b - 5bd)$
* **Paso 2 (Factor común por grupo):**
  $$\text{Grupo 1: } 2a(c - 1 + d)$$
  $$\text{Grupo 2: } -5b(c - 1 + d)$$
* **Paso 3 (Extraer factor común trinomio $(c - 1 + d)$):**
* **Respuesta Final:** $(c - 1 + d)(2a - 5b)$

---

#### CASO 3: Diferencia de Cuadrados Perfectos

##### 🔹 Ejercicio 3.1 (Nivel Básico)
**Enunciado:** Factorizar $x^2 - 25$

* **Paso 1 (Extraer raíces cuadradas):** $\sqrt{x^2} = x, \quad \sqrt{25} = 5$.
* **Paso 2 (Formar binomios conjugados $(a-b)(a+b)$):**
* **Respuesta Final:** $(x - 5)(x + 5)$

---

##### 🔸 Ejercicio 3.2 (Nivel Intermedio)
**Enunciado:** Factorizar $49x^4y^2 - 64w^{10}z^{14}$

* **Paso 1 (Raíces cuadradas):**
  $$\sqrt{49x^4y^2} = 7x^2y, \quad \sqrt{64w^{10}z^{14}} = 8w^5z^7$$
* **Paso 2 (Formar producto de suma por diferencia):**
* **Respuesta Final:** $(7x^2y - 8w^5z^7)(7x^2y + 8w^5z^7)$

---

##### 🔻 Ejercicio 3.3 (Nivel Avanzado)
**Enunciado:** Factorizar $(2x + 3)^2 - (x - 1)^2$

* **Paso 1 (Identificar $A^2 - B^2$):** $A = (2x + 3)$ y $B = (x - 1)$.
* **Paso 2 (Aplicar $(A - B)(A + B)$):**
  $$\text{Resta: } (2x + 3) - (x - 1) = 2x + 3 - x + 1 = x + 4$$
  $$\text{Suma: } (2x + 3) + (x - 1) = 2x + 3 + x - 1 = 3x + 2$$
* **Respuesta Final:** $(x + 4)(3x + 2)$

---

#### CASO 4: Trinomio Cuadrado Perfecto (TCP)

##### 🔹 Ejercicio 4.1 (Nivel Básico)
**Enunciado:** Factorizar $x^2 + 6x + 9$

* **Paso 1 (Raíces del 1.º y 3.er término):** $\sqrt{x^2} = x, \quad \sqrt{9} = 3$.
* **Paso 2 (Verificar doble producto):** $2 \cdot x \cdot 3 = 6x$ (Coincide con el 2.º término).
* **Paso 3 (Expresar como binomio al cuadrado con el signo del 2.º término):**
* **Respuesta Final:** $(x + 3)^2$

---

##### 🔸 Ejercicio 4.2 (Nivel Intermedio)
**Enunciado:** Factorizar $4x^2 + 12xy^2 + 9y^4$

* **Paso 1 (Raíces extremas):** $\sqrt{4x^2} = 2x, \quad \sqrt{9y^4} = 3y^2$.
* **Paso 2 (Verificar doble producto):** $2(2x)(3y^2) = 12xy^2$ (Correcto).
* **Paso 3 (Armar el binomio):**
* **Respuesta Final:** $(2x + 3y^2)^2$

---

##### 🔻 Ejercicio 4.3 (Nivel Avanzado)
**Enunciado:** Factorizar $25m^4 - 40m^2 + 16$

* **Paso 1 (Raíces extremas):** $\sqrt{25m^4} = 5m^2, \quad \sqrt{16} = 4$.
* **Paso 2 (Verificar doble producto):** $2(5m^2)(4) = 40m^2$ (Coincide con el término central).
* **Paso 3 (Signo negativo del 2.º término):** $(5m^2 - 4)^2$.
* **Respuesta Final:** $(5m^2 - 4)^2$

---

#### CASO 5: Trinomio de la forma $x^{2n} + bx^n + c$

##### 🔹 Ejercicio 5.1 (Nivel Básico)
**Enunciado:** Factorizar $x^2 - 7x + 12$

* **Paso 1 (Raíz del primer término):** $\sqrt{x^2} = x$.
* **Paso 2 (Definir signos):** Paréntesis 1: $(-)$, Paréntesis 2: $(-) \cdot (+) = (-)$.
* **Paso 3 (Buscar dos números que multiplicados den $12$ y sumados den $-7$):** Se eligen $-4$ y $-3$.
* **Respuesta Final:** $(x - 4)(x - 3)$

---

##### 🔸 Ejercicio 5.2 (Nivel Intermedio)
**Enunciado:** Factorizar $x^4 + 11x^2 + 28$

* **Paso 1 (Raíz del primer término):** $\sqrt{x^4} = x^2$.
* **Paso 2 (Signos):** Ambos son positivos $(+)(+)$.
* **Paso 3 (Números que multiplicados den $28$ y sumados den $11$):** $7$ y $4$.
* **Respuesta Final:** $(x^2 + 7)(x^2 + 4)$

---

##### 🔻 Ejercicio 5.3 (Nivel Avanzado)
**Enunciado:** Factorizar $(x + 2)^2 - 5(x + 2) - 14$

* **Paso 1 (Sustitución de variable):** Sea $u = (x + 2) \implies u^2 - 5u - 14$.
* **Paso 2 (Factorizar trinomio en $u$):** $(u - 7)(u + 2)$ (multiplicados $-14$, sumados $-5$).
* **Paso 3 (Restituir $u = x + 2$):**
  $$(x + 2 - 7)(x + 2 + 2) = (x - 5)(x + 4)$$
* **Respuesta Final:** $(x - 5)(x + 4)$

---

#### CASO 6: Trinomio de la forma $ax^{2n} + bx^n + c$ ($a > 1$)

##### 🔹 Ejercicio 6.1 (Nivel Básico)
**Enunciado:** Factorizar $2x^2 + 5x + 3$

* **Paso 1 (Multiplicar y dividir por $a = 2$):**
  $$\frac{2(2x^2 + 5x + 3)}{2} = \frac{(2x)^2 + 5(2x) + 6}{2}$$
* **Paso 2 (Factorizar el numerador como Caso 5):** Dos números que multiplicados den $6$ y sumados den $5 \implies 3$ y $2$.
  $$\frac{(2x + 3)(2x + 2)}{2}$$
* **Paso 3 (Extraer factor común para simplificar el denominador $2$):**
  $$\frac{(2x + 3) \cdot 2(x + 1)}{2} = (2x + 3)(x + 1)$$
* **Respuesta Final:** $(2x + 3)(x + 1)$

---

##### 🔸 Ejercicio 6.2 (Nivel Intermedio)
**Enunciado:** Factorizar $6x^2 + 5x - 4$

* **Paso 1 (Multiplicar y dividir por $a = 6$):**
  $$\frac{(6x)^2 + 5(6x) - 24}{6}$$
* **Paso 2 (Factorizar numerador):** Multiplicados $-24$ y restados $+5 \implies +8$ y $-3$.
  $$\frac{(6x + 8)(6x - 3)}{6}$$
* **Paso 3 (Factor común en ambos paréntesis y simplificación):**
  $$\frac{2(3x + 4) \cdot 3(2x - 1)}{6} = \frac{6(3x + 4)(2x - 1)}{6}$$
* **Respuesta Final:** $(3x + 4)(2x - 1)$

---

##### 🔻 Ejercicio 6.3 (Nivel Avanzado)
**Enunciado:** Factorizar $12x^2 - 7x - 10$

* **Paso 1 (Multiplicar y dividir por $a = 12$):**
  $$\frac{(12x)^2 - 7(12x) - 120}{12}$$
* **Paso 2 (Buscar números que multiplicados den $-120$ y sumados $-7$):** $-15$ y $+8$.
  $$\frac{(12x - 15)(12x + 8)}{12}$$
* **Paso 3 (Extraer MCD de los paréntesis):** $\text{MCD}(12, 15) = 3$ y $\text{MCD}(12, 8) = 4$.
  $$\frac{3(4x - 5) \cdot 4(3x + 2)}{12} = \frac{12(4x - 5)(3x + 2)}{12}$$
* **Respuesta Final:** $(4x - 5)(3x + 2)$

---

#### CASO 7: Suma y Diferencia de Cubos Perfectos

##### 🔹 Ejercicio 7.1 (Nivel Básico)
**Enunciado:** Factorizar $x^3 - 8$

* **Paso 1 (Raíces cúbicas):** $\sqrt[3]{x^3} = x, \quad \sqrt[3]{8} = 2$.
* **Paso 2 (Estructura $(a - b)(a^2 + ab + b^2)$):**
  $$(x - 2)(x^2 + (x)(2) + 2^2)$$
* **Respuesta Final:** $(x - 2)(x^2 + 2x + 4)$

---

##### 🔸 Ejercicio 7.2 (Nivel Intermedio)
**Enunciado:** Factorizar $27x^3 + 125y^9$

* **Paso 1 (Raíces cúbicas):** $\sqrt[3]{27x^3} = 3x, \quad \sqrt[3]{125y^9} = 5y^3$.
* **Paso 2 (Estructura $(a + b)(a^2 - ab + b^2)$):**
  $$(3x + 5y^3)\left[(3x)^2 - (3x)(5y^3) + (5y^3)^2\right]$$
* **Respuesta Final:** $(3x + 5y^3)(9x^2 - 15xy^3 + 25y^6)$

---

##### 🔻 Ejercicio 7.3 (Nivel Avanzado)
**Enunciado:** Factorizar $64p^{15} - 343t^6$

* **Paso 1 (Raíces cúbicas):** $\sqrt[3]{64p^{15}} = 4p^5, \quad \sqrt[3]{343t^6} = 7t^2$.
* **Paso 2 (Estructura $(a - b)(a^2 + ab + b^2)$):**
  $$(4p^5 - 7t^2)\left[(4p^5)^2 + (4p^5)(7t^2) + (7t^2)^2\right]$$
* **Respuesta Final:** $(4p^5 - 7t^2)(16p^{10} + 28p^5t^2 + 49t^4)$

---

### 6. Conclusiones y Reflexión
- La solución rigurosa a mano de los 7 casos fundamentales de factorización permite afianzar el reconocimiento visual de patrones algebraicos.
- Clasificar los ejercicios por nivel de dificultad (Básico, Intermedio y Avanzado) ayuda a estructurar una metodología analítica para abordar problemas más complejos en Cálculo Diferencial, como la resolución de indeterminaciones y la integración por fracciones parciales.

---

### 7. Bibliografía
- **Ortiz Campos, F. J., & Ortiz Cerecedo, F. J.** (2019). *Cálculo diferencial* (3.ª ed.). Grupo Editorial Patria.
- **Ríos Gallego, J. A.** (JulioProfe). *Resumen de Principales Casos de Factorización*. julioprofe.net.
