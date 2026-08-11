# Protocolo Individual — Unidad 1

**Asignatura:** Cálculo Diferencial  
**Estudiante:** Esteban David Marrugo Jassir  
**Docente:** Katherine Paternina Sierra  
**Fecha:** 2026-08-11  

---

### 1. Descripción de la actividad
Resolución detallada del taller práctico correspondiente a la Unidad 1 sobre límites indeterminados (mediante factorización y conjugación), límites al infinito y límites infinitos.

---

### 2. Palabras clave
Límite, Indeterminación, Factorización, Conjugada, Racionalización, Límite al Infinito, Límite Infinito, Comportamiento Asintótico.

---

### 3. Objetivo de las lecturas o actividad a realizar
- Aplicar técnicas de álgebra elemental (casos de factorización y racionalización) para resolver indeterminaciones del tipo $\frac{0}{0}$.
- Analizar el comportamiento de funciones cuando la variable independiente tiende a valores extremos ($\pm\infty$) o a puntos de discontinuidad asintótica.
- Fortalecer el cálculo analítico y la rigurosidad matemática en la evaluación de límites.

---

### 4. Conceptos clave y definiciones
- **Indeterminación $\frac{0}{0}$:** Expresión que resulta de evaluar directamente un límite y que no define el valor del mismo. Requiere manipulación algebraica (factorización o multiplicación por el conjugado) para remover el factor común que produce la división por cero.
- **Racionalización (Conjugada):** Proceso algebraico que consiste en multiplicar el numerador y el denominador por la expresión conjugada de una raíz (cambiando el signo del segundo término) para eliminar radicales del numerador o denominador y simplificar la expresión.
- **Límites al Infinito:** Estudio del valor al que se aproxima una función cuando la variable independiente $x$ crece infinitamente ($x \to \infty$) o decrece infinitamente ($x \to -\infty$). Si el límite es un número real $L$, existe una asíntota horizontal $y = L$.
- **Límites Infinitos:** Situación donde los valores de la función crecen o decrecen sin límite cuando $x$ se aproxima a un valor real $c$. Si el límite tiende a $\pm\infty$, la recta $x = c$ representa una asíntota vertical.

---

### 5. Desarrollo del Taller (Solución paso a paso)

#### PARTE I: Cálculo de límites indeterminados (factorización o conjugada)

**1. $\lim_{x \to -1} \frac{x^2 - 2x - 3}{x^2 + 3x + 2}$**
* **Evaluación directa:** $\frac{(-1)^2 - 2(-1) - 3}{(-1)^2 + 3(-1) + 2} = \frac{1 + 2 - 3}{1 - 3 + 2} = \frac{0}{0}$ (Indeterminado).
* **Factorización (Trinomio $x^2 + bx + c$):**
  $$x^2 - 2x - 3 = (x - 3)(x + 1)$$
  $$x^2 + 3x + 2 = (x + 2)(x + 1)$$
* **Simplificación:**
  $$\lim_{x \to -1} \frac{(x - 3)(x + 1)}{(x + 2)(x + 1)} = \lim_{x \to -1} \frac{x - 3}{x + 2} = \frac{-1 - 3}{-1 + 2} = -4$$

**2. $\lim_{x \to 1} \frac{x^2 - 3x + 2}{x^2 + 2x - 3}$**
* **Evaluación directa:** $\frac{1^2 - 3(1) + 2}{1^2 + 2(1) - 3} = \frac{0}{0}$ (Indeterminado).
* **Factorización:**
  $$x^2 - 3x + 2 = (x - 2)(x - 1)$$
  $$x^2 + 2x - 3 = (x + 3)(x - 1)$$
* **Simplificación:**
  $$\lim_{x \to 1} \frac{(x - 2)(x - 1)}{(x + 3)(x - 1)} = \lim_{x \to 1} \frac{x - 2}{x + 3} = \frac{1 - 2}{1 + 3} = -\frac{1}{4}$$

**3. $\lim_{x \to -2} \frac{x^2 + 7x + 10}{x^2 - x - 6}$**
* **Evaluación directa:** $\frac{(-2)^2 + 7(-2) + 10}{(-2)^2 - (-2) - 6} = \frac{4 - 14 + 10}{4 + 2 - 6} = \frac{0}{0}$ (Indeterminado).
* **Factorización:**
  $$x^2 + 7x + 10 = (x + 5)(x + 2)$$
  $$x^2 - x - 6 = (x - 3)(x + 2)$$
* **Simplificación:**
  $$\lim_{x \to -2} \frac{(x + 5)(x + 2)}{(x - 3)(x + 2)} = \lim_{x \to -2} \frac{x + 5}{x - 3} = \frac{-2 + 5}{-2 - 3} = -\frac{3}{5}$$

**4. $\lim_{x \to 2} \frac{x^2 - 3x + 2}{x^2 - 5x + 6}$**
* **Evaluación directa:** $\frac{2^2 - 3(2) + 2}{2^2 - 5(2) + 6} = \frac{0}{0}$ (Indeterminado).
* **Factorización:**
  $$x^2 - 3x + 2 = (x - 2)(x - 1)$$;
  $$x^2 - 5x + 6 = (x - 3)(x - 2)$$
* **Simplificación:**
  $$\lim_{x \to 2} \frac{(x - 2)(x - 1)}{(x - 3)(x - 2)} = \lim_{x \to 2} \frac{x - 1}{x - 3} = \frac{2 - 1}{2 - 3} = -1$$

**5. $\lim_{x \to 4} \frac{x^2 - x - 12}{x^2 + x - 20}$**
* **Evaluación directa:** $\frac{4^2 - 4 - 12}{4^2 + 4 - 20} = \frac{0}{0}$ (Indeterminado).
* **Factorización:**
  $$x^2 - x - 12 = (x - 4)(x + 3)$$
  $$x^2 + x - 20 = (x - 4)(x + 5)$$
* **Simplificación:**
  $$\lim_{x \to 4} \frac{(x - 4)(x + 3)}{(x - 4)(x + 5)} = \lim_{x \to 4} \frac{x + 3}{x + 5} = \frac{4 + 3}{4 + 5} = \frac{7}{9}$$

**6. $\lim_{x \to 1} \frac{x^3 - 2x^2 - 5x + 6}{x - 1}$**
* **Evaluación directa:** $\frac{1^3 - 2(1^2) - 5(1) + 6}{1 - 1} = \frac{0}{0}$ (Indeterminado).
* **División Sintética (Ruffini) en el numerador con $x=1$:**
  $$x^3 - 2x^2 - 5x + 6 = (x - 1)(x^2 - x - 6)$$
* **Simplificación:**
  $$\lim_{x \to 1} \frac{(x - 1)(x^2 - x - 6)}{x - 1} = \lim_{x \to 1} (x^2 - x - 6) = 1^2 - 1 - 6 = -6$$

**7. $\lim_{x \to -2} \frac{x^3 + 2x^2 - 5x - 6}{x + 2}$**
* **Nota analítica sobre la guía:** Al evaluar directamente en $x = -2$, obtenemos:
  $$\frac{(-2)^3 + 2(-2)^2 - 5(-2) - 6}{-2 + 2} = \frac{-8 + 8 + 10 - 6}{0} = \frac{4}{0}$$
  El límite por lo tanto no existe (tiende a infinito). Evaluando los límites laterales:
  - Para $x \to -2^+$: $\frac{4}{0^+} = +\infty$
  - Para $x \to -2^-$: $\frac{4}{0^-} = -\infty$
  *(Si el límite de la guía contenía una errata y correspondía a $x \to -1$, el resultado sería $\frac{0}{1} = 0$).*

**8. $\lim_{x \to -3} \frac{x^3 + 2x^2 - 17x + 15}{x^2 - x - 6}$**
* **Evaluación directa:**
  $$\frac{(-3)^3 + 2(-3)^2 - 17(-3) + 15}{(-3)^2 - (-3) - 6} = \frac{-27 + 18 + 51 + 15}{9 + 3 - 6} = \frac{57}{6} = \frac{19}{2}$$
  *(En caso de que el límite proyectado fuera para $x \to 3$, la expresión daría $\frac{9}{0}$, por lo cual el límite no existiría al divergir lateralmente a $\pm\infty$).*

**9. $\lim_{x \to -2} \frac{x^3 + 2x^2 - x - 2}{x^3 + 2x^2 - 9x - 18}$**
* **Evaluación directa:** $\frac{(-2)^3 + 2(-2)^2 - (-2) - 2}{(-2)^3 + 2(-2)^2 - 9(-2) - 18} = \frac{0}{0}$ (Indeterminado).
* **Factorización por agrupación de términos:**
  - Numerador: $x^2(x + 2) - 1(x + 2) = (x^2 - 1)(x + 2) = (x - 1)(x + 1)(x + 2)$
  - Denominador: $x^2(x + 2) - 9(x + 2) = (x^2 - 9)(x + 2) = (x - 3)(x + 3)(x + 2)$
* **Simplificación:**
  $$\lim_{x \to -2} \frac{(x - 1)(x + 1)(x + 2)}{(x - 3)(x + 3)(x + 2)} = \lim_{x \to -2} \frac{(x - 1)(x + 1)}{(x - 3)(x + 3)} = \frac{(-3)(-1)}{(-5)(1)} = -\frac{3}{5}$$

**10. $\lim_{x \to 4} \frac{x^4 - 5x^3 + 20x - 16}{x^4 - 3x^3 - 8x^2 + 12x + 16}$**
* **Evaluación directa:** $\frac{0}{0}$ (Indeterminado).
* **Factorización mediante Ruffini con la raíz conocida $x=4$:**
  - Numerador: $(x - 4)(x^3 - x^2 - 4x + 4) = (x - 4)(x^2(x - 1) - 4(x - 1)) = (x - 4)(x - 1)(x - 2)(x + 2)$
  - Denominador: $(x - 4)(x^3 + x^2 - 4x - 4) = (x - 4)(x^2(x + 1) - 4(x + 1)) = (x - 4)(x + 1)(x - 2)(x + 2)$
* **Simplificación:**
  $$\lim_{x \to 4} \frac{(x - 4)(x - 1)(x - 2)(x + 2)}{(x - 4)(x + 1)(x - 2)(x + 2)} = \lim_{x \to 4} \frac{x - 1}{x + 1} = \frac{4 - 1}{4 + 1} = \frac{3}{5}$$

**11. $\lim_{x \to 8} \frac{\sqrt{x+1}-3}{x-8}$**
* **Evaluación directa:** $\frac{0}{0}$ (Indeterminado).
* **Multiplicación por la conjugada ($\sqrt{x+1}+3$):**
  $$\frac{(\sqrt{x+1}-3)(\sqrt{x+1}+3)}{(x-8)(\sqrt{x+1}+3)} = \frac{(x+1) - 9}{(x-8)(\sqrt{x+1}+3)} = \frac{x-8}{(x-8)(\sqrt{x+1}+3)}$$
* **Simplificación:**
  $$\lim_{x \to 8} \frac{1}{\sqrt{x+1}+3} = \frac{1}{\sqrt{8+1}+3} = \frac{1}{6}$$

**12. $\lim_{x \to 5} \frac{\sqrt{2x-1}-3}{x-5}$**
* **Evaluación directa:** $\frac{0}{0}$ (Indeterminado).
* **Multiplicación por la conjugada ($\sqrt{2x-1}+3$):**
  $$\frac{(\sqrt{2x-1}-3)(\sqrt{2x-1}+3)}{(x-5)(\sqrt{2x-1}+3)} = \frac{(2x-1) - 9}{(x-5)(\sqrt{2x-1}+3)} = \frac{2(x-5)}{(x-5)(\sqrt{2x-1}+3)}$$
* **Simplificación:**
  $$\lim_{x \to 5} \frac{2}{\sqrt{2x-1}+3} = \frac{2}{\sqrt{2(5)-1}+3} = \frac{2}{6} = \frac{1}{3}$$

**13. $\lim_{x \to 0} \frac{\sqrt{2+x}-\sqrt{2}}{x}$**
* **Evaluación directa:** $\frac{0}{0}$ (Indeterminado).
* **Multiplicación por la conjugada ($\sqrt{2+x}+\sqrt{2}$):**
  $$\frac{(\sqrt{2+x}-\sqrt{2})(\sqrt{2+x}+\sqrt{2})}{x(\sqrt{2+x}+\sqrt{2})} = \frac{(2+x) - 2}{x(\sqrt{2+x}+\sqrt{2})} = \frac{x}{x(\sqrt{2+x}+\sqrt{2})}$$
* **Simplificación:**
  $$\lim_{x \to 0} \frac{1}{\sqrt{2+x}+\sqrt{2}} = \frac{1}{2\sqrt{2}} = \frac{\sqrt{2}}{4}$$

---

#### PARTE II: Límites infinitos y al infinito

**1. $\lim_{x \to 2} \frac{5}{(x-2)^2}$**
* Como $x \to 2$, el término $(x-2)^2$ se aproxima a $0$ por valores estrictamente positivos (debido al exponente par). Una constante positiva sobre un valor infinitesimal positivo tiende a $+\infty$.
* **Resultado:** $+\infty$

**2. $\lim_{x \to 0} \frac{1}{x^2}$**
* Análogamente, cuando $x \to 0$, $x^2 \to 0^+$.
* **Resultado:** $+\infty$

**3. $\lim_{x \to 0} \left(-\frac{1}{x^2}\right)$**
* Multiplicando el comportamiento del límite anterior por $-1$:
* **Resultado:** $-\infty$

**4. $\lim_{x \to \infty} \frac{3}{x}$**
* Por propiedad, el límite de una constante dividida por una variable que crece sin límite es igual a $0$.
* **Resultado:** $0$

**5. $\lim_{x \to -\infty} \frac{5}{x}$**
* De igual manera, constante dividido entre una variable que decrece infinitamente tiende a $0$.
* **Resultado:** $0$

**6. $\lim_{x \to \infty} (5x^2 - 2x + 3)$**
* En polinomios al infinito, el término de mayor grado domina el comportamiento.
* $$\lim_{x \to \infty} 5x^2 = +\infty$$

**7. $\lim_{x \to -\infty} (4x^2 + 3x - 1)$**
* El término de mayor grado es $4x^2$. Dado que $x \to -\infty$, $x^2 \to +\infty$.
* **Resultado:** $+\infty$

**8. $\lim_{x \to \infty} (4x^3 + 2x - 7)$**
* El término dominante es $4x^3$.
* **Resultado:** $+\infty$

**9. $\lim_{x \to -\infty} (7x^3 - 8x + 5)$**
* El término dominante es $7x^3$. Al evaluar una potencia impar con una base que tiende a $-\infty$, el resultado es negativo.
* **Resultado:** $-\infty$

**10. $\lim_{x \to \infty} (-3x^2 + 5x - 7)$**
* El término dominante es $-3x^2$. Como $x^2 \to +\infty$, al multiplicarse por $-3$, el resultado tiende a $-\infty$.
* **Resultado:** $-\infty$

**11. $\lim_{x \to \infty} \frac{x^2 + 3x + 2}{x + 3}$**
* Dado que el grado del numerador (2) es mayor que el del denominador (1), el límite diverge. Al dividir por la mayor potencia del denominador ($x$):
  $$\lim_{x \to \infty} \frac{x + 3 + \frac{2}{x}}{1 + \frac{3}{x}} = \frac{\infty + 3 + 0}{1 + 0} = +\infty$$

**12. $\lim_{x \to -\infty} \frac{x + 3}{x^2 + 3x + 2}$**
* El grado del denominador (2) es mayor que el del numerador (1). Al dividir todos los términos entre la mayor potencia del denominador ($x^2$):
  $$\lim_{x \to -\infty} \frac{\frac{1}{x} + \frac{3}{x^2}}{1 + \frac{3}{x} + \frac{2}{x^2}} = \frac{0 + 0}{1 + 0 + 0} = 0$$

**13. $\lim_{x \to -3} \frac{7}{x+3}$**
* Límite de la forma $\frac{c}{0}$. Evaluando límites laterales:
  - $\lim_{x \to -3^+} \frac{7}{x+3} = \frac{7}{0^+} = +\infty$
  - $\lim_{x \to -3^-} \frac{7}{x+3} = \frac{7}{0^-} = -\infty$
* **Resultado:** El límite no existe al divergir a infinito con distinto signo por los laterales.

**14. $\lim_{x \to \infty} \frac{2x^3 + 3x - 2}{4x^2 + 2x - 3}$**
* Comparación de grados: grado del numerador (3) mayor que el del denominador (2).
  $$\lim_{x \to \infty} \frac{2x^3\left(1 + \frac{3}{2x^2} - \frac{1}{x^3}\right)}{4x^2\left(1 + \frac{1}{2x} - \frac{3}{4x^2}\right)} = \lim_{x \to \infty} \frac{x}{2} \cdot \frac{1}{1} = +\infty$$

**15. $\lim_{x \to -\infty} \frac{x^2 + x + 5}{2x^2 + 7}$**
* Al tener el mismo grado (2) en numerador y denominador, el límite es el cociente de los coeficientes principales:
  $$\lim_{x \to -\infty} \frac{x^2\left(1 + \frac{1}{x} + \frac{5}{x^2}\right)}{x^2\left(2 + \frac{7}{x^2}\right)} = \frac{1}{2}$$

**16. $\lim_{x \to -\infty} \frac{2x^4 + x^2 + 5}{3x^5 + x^3 - x}$**
* Grado del denominador (5) es mayor que el del numerador (4).
* **Resultado:** $0$

---

### 6. Metodología de trabajo
1. Revisé las bases teóricas de límites indeterminados del módulo provisto por la cátedra.
2. Utilicé la tabla resumen de factorización de expresiones polinómicas (`RESUMEN FACT.pdf`) para agilizar la identificación de binomios y trinomios factorizables.
3. Resolví de forma secuencial y manuscrita los 29 límites propuestos en el taller, validando indeterminaciones y analizando detalladamente los comportamientos laterales para aquellos de la forma $\frac{c}{0}$.
4. Registré la estructura de resolución directamente en mi espacio de apuntes de Obsidian para posterior asimilación mediante *active recall*.

---

### 7. Conclusiones
- La correcta resolución de indeterminaciones algebraicas requiere un dominio óptimo de la factorización.
- El comportamiento de límites que involucran al infinito está determinado de forma exclusiva por las potencias de mayor grado en expresiones polinómicas racionales.
- Identificar y diferenciar entre asintonías horizontales y verticales a partir de la resolución analítica es crucial para la interpretación gráfica de funciones.

---

### 8. Discusiones y recomendaciones
Se recomienda prestar particular atención al verificar que se está ante una indeterminación antes de realizar operaciones de factorización o conjugación, puesto que sustituir directamente es el primer paso metodológico indispensable.

---

### 9. Bibliografía
- **Ortiz Campos, F. J., & Ortiz Cerecedo, F. J.** (2019). *Cálculo diferencial* (3.ª ed.). Grupo Editorial Patria.
- **Universidad de Cartagena.** (2026). *Módulo de la unidad 1: Cálculo diferencial*. Facultad de Ingeniería. Cartagena, Colombia.
