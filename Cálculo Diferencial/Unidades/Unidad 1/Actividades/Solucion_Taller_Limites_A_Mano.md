# 📐 Solución Oficial: Actividad #1 — Límites (Cálculo Diferencial)
**Universidad de Cartagena — Facultad de Ingeniería de Software**  
**Modalidad:** A mano (Guía de transcripción paso a paso con justificación formal)

---

## 1. Límite con Exponente Fraccionario

$$\lim_{x \to -12} (15 - x)^{4/3}$$

### Paso a paso:
1. **Evaluación por sustitución directa:**
   La función es continua en el entorno de $x = -12$. Sustituimos directamente la variable:
   $$(15 - (-12))^{4/3} = (15 + 12)^{4/3} = 27^{4/3}$$

2. **Propiedad de los exponentes racionales:**
   Recordamos que $a^{m/n} = (\sqrt[n]{a})^m$:
   $$27^{4/3} = \left(\sqrt[3]{27}\right)^4$$

3. **Cálculo de la raíz y potencia:**
   $$\sqrt[3]{27} = 3$$
   $$3^4 = 3 \times 3 \times 3 \times 3 = 81$$

**Respuesta final:**
$$\mathbf{81}$$

---

## 2. Límite Indeterminado con Radical (Conjugada)

$$\lim_{x \to 6} \frac{2 - \sqrt{x - 2}}{x^2 - 36}$$

### Paso a paso:
1. **Comprobación de indeterminación:**
   - Numerador: $2 - \sqrt{6 - 2} = 2 - \sqrt{4} = 2 - 2 = 0$
   - Denominador: $6^2 - 36 = 36 - 36 = 0$
   - Se obtiene la forma indeterminada: **$\frac{0}{0}$**.

2. **Racionalización del numerador:**
   Multiplicamos numerador y denominador por el binomio conjugado del numerador: $(2 + \sqrt{x - 2})$:
   $$\lim_{x \to 6} \frac{(2 - \sqrt{x - 2})(2 + \sqrt{x - 2})}{(x^2 - 36)(2 + \sqrt{x - 2})}$$

3. **Aplicación de diferencia de cuadrados en el numerador:**
   $$(a - b)(a + b) = a^2 - b^2$$
   $$2^2 - (\sqrt{x - 2})^2 = 4 - (x - 2) = 4 - x + 2 = 6 - x = -(x - 6)$$

4. **Factorización del denominador (diferencia de cuadrados):**
   $$x^2 - 36 = (x - 6)(x + 6)$$

5. **Reescritura y simplificación del factor común:**
   $$\lim_{x \to 6} \frac{-(x - 6)}{(x - 6)(x + 6)(2 + \sqrt{x - 2})}$$
   Cancelamos el factor $(x - 6)$ (válido ya que $x \to 6 \implies x \neq 6$):
   $$\lim_{x \to 6} \frac{-1}{(x + 6)(2 + \sqrt{x - 2})}$$

6. **Evaluación del límite:**
   $$\frac{-1}{(6 + 6)(2 + \sqrt{6 - 2})} = \frac{-1}{(12)(2 + 2)} = \frac{-1}{12 \times 4} = -\frac{1}{48}$$

**Respuesta final:**
$$\mathbf{-\frac{1}{48}}$$

---

## 3. Vaciado de una Piscina

Una piscina se vacía según la función:
$$v(t) = \frac{t^2 + 11t - 26}{t - 2}$$
donde $v$ es el volumen en $\text{m}^3$ y $t$ el tiempo en horas. ¿A qué valor se aproxima el volumen cuando $t \to 2$ horas?

$$\lim_{t \to 2} \frac{t^2 + 11t - 26}{t - 2}$$

### Paso a paso:
1. **Comprobación de indeterminación:**
   - Numerador: $2^2 + 11(2) - 26 = 4 + 22 - 26 = 0$
   - Denominador: $2 - 2 = 0$
   - Forma indeterminada: **$\frac{0}{0}$**.

2. **Factorización del trinomio de la forma $x^2 + bx + c$:**
   Buscamos dos números que multiplicados den $-26$ y sumados den $+11$:
   $$13 \times (-2) = -26$$
   $$13 + (-2) = 11$$
   Por tanto:
   $$t^2 + 11t - 26 = (t + 13)(t - 2)$$

3. **Simplificación de la expresión:**
   $$\lim_{t \to 2} \frac{(t + 13)(t - 2)}{t - 2} = \lim_{t \to 2} (t + 13)$$

4. **Evaluación:**
   $$2 + 13 = 15$$

**Respuesta e interpretación:**
Cuando el tiempo se aproxima a $2$ horas, el volumen de agua de la piscina se aproxima a:
$$\mathbf{15\text{ m}^3}$$

---

## 4. Tiempo de una Motocicleta (Límite al Infinito con Radical)

El tiempo $t$ (en horas) está dado por:
$$t(x) = \frac{\sqrt{4x^4 + x^2 + 1}}{x^2 + 1}$$
donde $x$ es el espacio recorrido en metros. ¿A qué valor se aproxima el tiempo cuando $x \to \infty$?

$$\lim_{x \to \infty} \frac{\sqrt{4x^4 + x^2 + 1}}{x^2 + 1}$$

### Paso a paso:
1. **Identificación de la indeterminación:**
   Al evaluar cuando $x \to \infty$, se obtiene la forma **$\frac{\infty}{\infty}$**.

2. **División por la mayor potencia del denominador:**
   La mayor potencia del denominador es $x^2$. Dividimos numerador y denominador entre $x^2$:
   - Para el numerador: como $x > 0$, introducimos $x^2$ dentro de la raíz cuadrada como $\sqrt{x^4}$:
     $$\frac{\sqrt{4x^4 + x^2 + 1}}{x^2} = \sqrt{\frac{4x^4 + x^2 + 1}{x^4}} = \sqrt{4 + \frac{1}{x^2} + \frac{1}{x^4}}$$
   - Para el denominador:
     $$\frac{x^2 + 1}{x^2} = 1 + \frac{1}{x^2}$$

3. **Reescritura del límite:**
   $$\lim_{x \to \infty} \frac{\sqrt{4 + \frac{1}{x^2} + \frac{1}{x^4}}}{1 + \frac{1}{x^2}}$$

4. **Aplicación del teorema de límites al infinito ($\lim_{x \to \infty} \frac{k}{x^n} = 0$):**
   $$\frac{\sqrt{4 + 0 + 0}}{1 + 0} = \frac{\sqrt{4}}{1} = \frac{2}{1} = 2$$

**Respuesta e interpretación:**
A medida que el espacio recorrido tiende al infinito, el tiempo se aproxima asintóticamente a:
$$\mathbf{2\text{ horas}}$$

---

## 5. Tiempo de una Motocicleta (Funciones Racionales al Infinito)

$$t(x) = \frac{2x^2 + 3x - 1}{5x^2 + x - 1}$$
¿A qué valor se aproxima el tiempo cuando $x \to \infty$?

$$\lim_{x \to \infty} \frac{2x^2 + 3x - 1}{5x^2 + x - 1}$$

### Paso a paso:
1. **Identificación:**
   Límite racional con indeterminación **$\frac{\infty}{\infty}$**.

2. **División entre la mayor potencia del denominador ($x^2$):**
   $$\lim_{x \to \infty} \frac{\frac{2x^2}{x^2} + \frac{3x}{x^2} - \frac{1}{x^2}}{\frac{5x^2}{x^2} + \frac{x}{x^2} - \frac{1}{x^2}} = \lim_{x \to \infty} \frac{2 + \frac{3}{x} - \frac{1}{x^2}}{5 + \frac{1}{x} - \frac{1}{x^2}}$$

3. **Evaluación de límites nulos al infinito:**
   $$\frac{2 + 0 - 0}{5 + 0 - 0} = \frac{2}{5}$$

**Respuesta e interpretación:**
Cuando el espacio tiende a infinito, el tiempo se aproxima a:
$$\mathbf{\frac{2}{5}\text{ horas}}\quad (\text{equivalente a } 24\text{ minutos})$$

---

## 6. Diferencia de Expresiones Racionales al Infinito

$$\lim_{x \to \infty} \left( \frac{x^2}{x - 1} - \frac{x^2 + 1}{x - 2} \right)$$

### Paso a paso:
1. **Identificación de la forma indeterminada:**
   Cada término tiende a $\infty$, generando la forma **$\infty - \infty$**.

2. **Operación algebraica (resta de fracciones):**
   El mínimo común denominador es $(x - 1)(x - 2)$:
   $$\frac{x^2(x - 2) - (x^2 + 1)(x - 1)}{(x - 1)(x - 2)}$$

3. **Desarrollo de los numeradores:**
   - Término izquierdo: $x^2(x - 2) = x^3 - 2x^2$
   - Término derecho: $(x^2 + 1)(x - 1) = x^3 - x^2 + x - 1$
   - Resta completa:
     $$(x^3 - 2x^2) - (x^3 - x^2 + x - 1) = x^3 - 2x^2 - x^3 + x^2 - x + 1 = -x^2 - x + 1$$

4. **Desarrollo del denominador:**
   $$(x - 1)(x - 2) = x^2 - 3x + 2$$

5. **Reexpresión del límite:**
   $$\lim_{x \to \infty} \frac{-x^2 - x + 1}{x^2 - 3x + 2}$$

6. **Cálculo dividiendo entre la mayor potencia ($x^2$):**
   $$\lim_{x \to \infty} \frac{-1 - \frac{1}{x} + \frac{1}{x^2}}{1 - \frac{3}{x} + \frac{2}{x^2}} = \frac{-1 - 0 + 0}{1 - 0 + 0} = \frac{-1}{1} = -1$$

**Respuesta final:**
$$\mathbf{-1}$$

---

## 7. Límite al Infinito con Radical en el Denominador

$$\lim_{x \to \infty} \frac{4 - 3x^3}{\sqrt{x^6 + 16}}$$

### Paso a paso:
1. **Identificación de la forma:** Indeterminación **$-\frac{\infty}{\infty}$**.

2. **División por la mayor potencia:**
   La potencia efectiva dominante en el denominador es $\sqrt{x^6} = x^3$ (para $x > 0$).
   Dividimos numerador y denominador por $x^3$:
   - Numerador:
     $$\frac{4 - 3x^3}{x^3} = \frac{4}{x^3} - 3$$
   - Denominador:
     $$\frac{\sqrt{x^6 + 16}}{x^3} = \sqrt{\frac{x^6 + 16}{x^6}} = \sqrt{1 + \frac{16}{x^6}}$$

3. **Evaluación del límite:**
   $$\lim_{x \to \infty} \frac{\frac{4}{x^3} - 3}{\sqrt{1 + \frac{16}{x^6}}} = \frac{0 - 3}{\sqrt{1 + 0}} = \frac{-3}{1} = -3$$

**Respuesta final:**
$$\mathbf{-3}$$

---

## 8. Límite Racional con Grados Distintos

$$\lim_{x \to \infty} \frac{2x^3 + 3x^2 + 4x + 1}{x^4 + 3x^3 + 2}$$

### Paso a paso:
1. **Análisis de grados:**
   - Grado del numerador: $3$
   - Grado del denominador: $4$
   - Cuando el grado del denominador es mayor que el del numerador, el denominador crece mucho más rápido, por lo que el límite tiende a $0$.

2. **Demostración formal dividiendo por la mayor potencia del denominador ($x^4$):**
   $$\lim_{x \to \infty} \frac{\frac{2x^3}{x^4} + \frac{3x^2}{x^4} + \frac{4x}{x^4} + \frac{1}{x^4}}{\frac{x^4}{x^4} + \frac{3x^3}{x^4} + \frac{2}{x^4}} = \lim_{x \to \infty} \frac{\frac{2}{x} + \frac{3}{x^2} + \frac{4}{x^3} + \frac{1}{x^4}}{1 + \frac{3}{x} + \frac{2}{x^4}}$$

3. **Evaluación de términos:**
   $$\frac{0 + 0 + 0 + 0}{1 + 0 + 0} = \frac{0}{1} = 0$$

**Respuesta final:**
$$\mathbf{0}$$

---

## 9. Escalabilidad de un Servicio en la Nube

Modelo de rendimiento:
$$R(n) = \frac{n^3 - 8n^2 + 16n}{n^2 - 8n + 16}$$
donde $n$ es el número de centenas de solicitudes simultáneas. Se analiza la carga aproximándose a $400$ solicitudes ($n \to 4$).

$$\lim_{n \to 4} \frac{n^3 - 8n^2 + 16n}{n^2 - 8n + 16}$$

### a. Comprobación de la indeterminación:
Sustituyendo directamente $n = 4$:
- Numerador:
  $$4^3 - 8(4^2) + 16(4) = 64 - 8(16) + 64 = 64 - 128 + 64 = 0$$
- Denominador:
  $$4^2 - 8(4) + 16 = 16 - 32 + 16 = 0$$
- **Conclusión:** Se obtiene la forma indeterminada **$\frac{0}{0}$**.

### b. Factorización completa:
- **Numerador:** Extraemos factor común $n$:
  $$n^3 - 8n^2 + 16n = n(n^2 - 8n + 16)$$
  El paréntesis es un trinomio cuadrado perfecto: $(n - 4)^2$.
  $$\text{Numerador} = n(n - 4)^2$$
- **Denominador:** Es el mismo trinomio cuadrado perfecto:
  $$n^2 - 8n + 16 = (n - 4)^2$$

### c. Simplificación y cálculo del límite:
Para todo $n \neq 4$:
$$\frac{n(n - 4)^2}{(n - 4)^2} = n$$
Calculamos el límite:
$$\lim_{n \to 4} R(n) = \lim_{n \to 4} n = 4$$

### d. Explicación contextual:
Que el modelo original no esté definido exactamente en $n = 4$ significa que el punto $n = 4$ representa una **singularidad o discontinuidad evitable** (una división por cero en la ecuación que matemáticamente no produce un número real; por ejemplo, un bloqueo transitorio o indeterminación de hilos en el procesador). Sin embargo, que exista el límite ($\lim_{n \to 4} R(n) = 4$) garantiza que el rendimiento del sistema se comporta de manera **estable y predecible** en la vecindad de las 400 solicitudes: tanto si la carga sube desde 395 como si baja desde 405 solicitudes, el indicador converge de manera suave a 4.

---

## 10. Tiempo de Respuesta de una API

Modelo de tiempo de respuesta:
$$T(x) = \frac{x^3 - 27}{x^2 - 9}$$
donde $x$ es el nivel normalizado de carga. Se estudia el comportamiento cuando $x \to 3$.

$$\lim_{x \to 3} \frac{x^3 - 27}{x^2 - 9}$$

### a. Indeterminación:
Al evaluar directamente en $x = 3$:
- Numerador: $3^3 - 27 = 27 - 27 = 0$
- Denominador: $3^2 - 9 = 9 - 9 = 0$
- **Resultado:** Indeterminación de la forma **$\frac{0}{0}$**.

### b. Factorización completa:
- **Numerador (Diferencia de cubos, $a^3 - b^3 = (a - b)(a^2 + ab + b^2)$):**
  $$x^3 - 27 = x^3 - 3^3 = (x - 3)(x^2 + 3x + 9)$$
- **Denominador (Diferencia de cuadrados, $a^2 - b^2 = (a - b)(a + b)$):**
  $$x^2 - 9 = (x - 3)(x + 3)$$

### c. Simplificación y cálculo:
Para $x \neq 3$, cancelamos el factor común $(x - 3)$:
$$\lim_{x \to 3} \frac{(x - 3)(x^2 + 3x + 9)}{(x - 3)(x + 3)} = \lim_{x \to 3} \frac{x^2 + 3x + 9}{x + 3}$$
Evaluamos sustituyendo $x = 3$:
$$\frac{3^2 + 3(3) + 9}{3 + 3} = \frac{9 + 9 + 9}{6} = \frac{27}{6} = \frac{9}{2} = 4.5$$

### d. Explicación teórica y contextual:
Sería incorrecto concluir que $T(3)$ necesariamente existe porque **el valor de un límite estudia la tendencia de la función en la vecindad inmediata (alrededor de un punto), pero no describe el estado en el punto exacto**. En $x = 3$, la función evalúa a $\frac{0}{0}$, lo cual no está definido en el dominio de los números reales (geométricamente es un agujero o discontinuidad removible). Por ende, el límite nos dice a qué valor tiende el tiempo de respuesta conforme nos acercamos al nivel de carga 3, pero no implica que en $x = 3$ exacto el servicio responda sin fallar.
