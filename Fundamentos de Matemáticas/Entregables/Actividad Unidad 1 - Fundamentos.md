# Actividad de Aprendizaje — Unidad 1
## Preguntas sobre Conjuntos y Lógica Proposicional

**Asignatura:** Fundamentos de Matemáticas (`CFBD242-A1`)  
**Docente:** Atilano Arrieta Vivero  
**Estudiante:** Esteban David Marrugo Jassir  
**Código Estudiantil:** 7502620036  
**Programa:** Ingeniería de Software  
**Semestre:** 1 (2026-2)  
**Institución:** Universidad de Cartagena — Centro para la Educación Virtual y a Distancia (CTEV)  
**Fecha de Entrega:** Miércoles, 26 de Agosto de 2026 (23:59 hs)  

---

## 📌 PARTE 1: OPERACIONES Y DIAGRAMAS DE VENN

### Pregunta 1
**El diagrama de Venn que se muestra en la figura indica una operación entre los conjuntos $A$, $B$ y $C$. ¿Cuál de las siguientes operaciones se indica en el diagrama de Venn en la región sombreada?**

* **A.** $(A \cap B) \cup (A \cap C)$
* **B.** $(A - B) \cup (B - C)$
* **C.** $(A \cap B) \cap C$
* **D.** $(A \cup B) \cap C$

> **Respuesta Correcta:** **A. $(A \cap B) \cup (A \cap C)$**

#### Justificación y Demostración:
1. En el diagrama gráfico, la región sombreada cubre exactamente dos áreas contiguas:
   - La zona de intersección entre el conjunto $A$ y el conjunto $B$, denotada formalmente como $(A \cap B)$.
   - La zona de intersección entre el conjunto $A$ y el conjunto $C$, denotada formalmente como $(A \cap C)$.
2. La unión de ambas regiones representa los elementos que pertenecen simultáneamente a $A$ y $B$, o a $A$ y $C$:
   $$\text{Región sombreada} = (A \cap B) \cup (A \cap C)$$
3. Por la propiedad distributiva de la teoría de conjuntos, esta expresión es equivalente a $A \cap (B \cup C)$.

---

### Pregunta 2
**Se han definido los conjuntos $A$, $B$ y $C$ como se muestran a continuación:**
- $A = \{2, 4, 6, 8, 10, 12, 14, 16, 18, 20\}$
- $B = \{3, 6, 9, 12, 15, 18\}$
- $C = \{1, 6, 8, 12, 14, 17, 18\}$

**Los números que pertenecen al conjunto indicado con la operación $A - B$ son:**

* **A.** $\{2, 4, 10, 14, 16, 18, 20\}$
* **B.** $\{2, 4, 8, 10, 14, 15, 20\}$
* **C.** $\{2, 4, 8, 10, 14, 16, 20\}$
* **D.** $\{2, 3, 4, 8, 14, 15, 16, 20\}$

> **Respuesta Correcta:** **C. $\{2, 4, 8, 10, 14, 16, 20\}$**

#### Justificación y Desarrollo:
1. La diferencia de conjuntos $A - B$ se define como el conjunto formado por todos los elementos que pertenecen al conjunto $A$ y que **no** pertenecen al conjunto $B$:
   $$A - B = \{x \mid x \in A \land x \notin B\}$$
2. Identificamos los elementos comunes entre $A$ y $B$ ($A \cap B$):
   $$A \cap B = \{6, 12, 18\}$$
3. Sustraemos dichos elementos del conjunto original $A$:
   $$A - B = \{2, 4, 6, 8, 10, 12, 14, 16, 18, 20\} \setminus \{6, 12, 18\}$$
   $$A - B = \{2, 4, 8, 10, 14, 16, 20\}$$

---

### Pregunta 3
**Con los mismos conjuntos $A$, $B$ y $C$, los números que pertenecen al conjunto indicado con la operación $A \cap B \cap C$ son:**

* **A.** $\{6, 12, 18\}$
* **B.** $\{6, 8, 12, 14, 18\}$
* **C.** $\{2, 4, 8, 10, 14, 16, 20\}$
* **D.** $\{1, 6, 8, 12, 14, 18\}$

> **Respuesta Correcta:** **A. $\{6, 12, 18\}$**

#### Justificación y Desarrollo:
1. La intersección múltiple $A \cap B \cap C$ está constituida por los elementos presentes simultáneamente en los tres conjuntos:
   $$A \cap B \cap C = \{x \mid x \in A \land x \in B \land x \in C\}$$
2. Intersección $A \cap B$:
   $$A \cap B = \{6, 12, 18\}$$
3. Comprobamos la pertenencia de cada elemento en el conjunto $C = \{1, 6, 8, 12, 14, 17, 18\}$:
   - $6 \in C$ $\implies$ Cumple
   - $12 \in C$ $\implies$ Cumple
   - $18 \in C$ $\implies$ Cumple
4. Por consiguiente:
   $$A \cap B \cap C = \{6, 12, 18\}$$

---

### Pregunta 4
**¿Cuál de los siguientes diagramas de Venn representa al conjunto indicado con la operación $A \cap B \cap C$?**

* **A.** Diagrama con el círculo $A$ sombreado en su totalidad.
* **B.** Diagrama con la región inferior entre $B$ y $C$ sombreada.
* **C.** Diagrama con el conjunto $A$ rayado verticalmente.
* **D.** Diagrama con la región central compartida simultáneamente por los tres círculos ($A, B, C$) sombreada.

> **Respuesta Correcta:** **D**

#### Justificación:
La operación de intersección de tres conjuntos $A \cap B \cap C$ corresponde estrictamente a la región central del diagrama donde se solapan simultáneamente las circunferencias de $A$, $B$ y $C$, la cual está sombreada exclusivamente en la **Opción D**.

---

### Pregunta 5
**Observa el diagrama de Venn que muestra tres conjuntos $A, B$ y $C$. De acuerdo con la gráfica, ¿qué operación define la región sombreada?**

* **A.** $A \cap (B \cap C)$
* **B.** $A \cap (B \cup C)$
* **C.** $A \cup (B \cap C)$
* **D.** $A \cup (B \cup C)$

> **Respuesta Correcta:** **B. $A \cap (B \cup C)$**

#### Justificación:
La región sombreada está formada por la parte del conjunto $A$ que comparte elementos con $B$, unida a la parte de $A$ que comparte elementos con $C$. Esto corresponde exactamente a la intersección del conjunto $A$ con la unión de $B$ y $C$:
$$\text{Región sombreada} = A \cap (B \cup C) = (A \cap B) \cup (A \cap C)$$

---

### Pregunta 6
**Observa el diagrama de Venn. De acuerdo con la gráfica, ¿qué operación define la región sombreada?**

* **A.** $A - B$
* **B.** $B - C$
* **C.** $B - (A \cup B)$
* **D.** $C - B$

> **Respuesta Correcta:** **B. $B - C$**

#### Justificación:
En el diagrama, la totalidad del círculo $B$ se encuentra sombreada, a excepción de todos los sectores que quedan cubiertos por el círculo $C$ (incluyendo la zona común con $A$ que no toca a $C$). Esto representa matemáticamente la diferencia entre el conjunto $B$ y el conjunto $C$:
$$\text{Región sombreada} = B - C = \{x \mid x \in B \land x \notin C\}$$

---

## 📌 PARTE 2: APLICACIÓN PRÁCTICA DE CONJUNTOS (ENCUESTAS)

### Contexto de Preguntas 7 a 11: Encuesta de Redes Sociales
En la Universidad de Cartagena, los estudiantes de primer semestre encuestaron a los docentes sobre el uso de redes sociales, obteniendo los siguientes datos:
- $n(W) = 25$ (WhatsApp)
- $n(F) = 28$ (Facebook)
- $n(X) = 13$ (X / Twitter)
- $n(F \cap X) = 8$
- $n(W \cap F) = 19$
- $n(W \cap X) = 7$
- $n(W \cap F \cap X) = 6$ (las tres redes sociales)
- $n(\text{Ninguna}) = 2$ docentes

#### Determinación de las Regiones Disjuntas del Diagrama de Venn:
1. **Intersección triple (las tres redes):**
   $$n(W \cap F \cap X) = 6$$
2. **Intersecciones dobles exclusivas:**
   - Solo WhatsApp y Facebook: $n(W \cap F) - 6 = 19 - 6 = 13$
   - Solo WhatsApp y X: $n(W \cap X) - 6 = 7 - 6 = 1$
   - Solo Facebook y X: $n(F \cap X) - 6 = 8 - 6 = 2$
3. **Uso exclusivo de una sola red social:**
   - Solo WhatsApp: $25 - (13 + 1 + 6) = 25 - 20 = 5$
   - Solo Facebook: $28 - (13 + 2 + 6) = 28 - 21 = 7$
   - Solo X: $13 - (1 + 2 + 6) = 13 - 9 = 4$
4. **Total de docentes que usan al menos una red social ($W \cup F \cup X$):**
   $$n(W \cup F \cup X) = 5 + 7 + 4 + 13 + 1 + 2 + 6 = 38$$

---

### Pregunta 7
**De acuerdo con los resultados de la encuesta, ¿cuántos docentes fueron encuestados?**

* **A.** 40
* **B.** 66
* **C.** 42
* **D.** 38

> **Respuesta Correcta:** **A. 40**

#### Justificación:
El universo total de docentes encuestados comprende la unión de los docentes que usan al menos una red social más los que no usan ninguna:
$$\text{Total Encuestados} = n(W \cup F \cup X) + n(\text{Ninguna}) = 38 + 2 = 40\text{ docentes}$$

---

### Pregunta 8
**¿Cuántos docentes usan únicamente WhatsApp?**

* **A.** 25
* **B.** 7
* **C.** 6
* **D.** 5

> **Respuesta Correcta:** **D. 5**

#### Justificación:
Se calcula restando del total de usuarios de WhatsApp ($25$) aquellos que comparten la aplicación con Facebook, X o ambas ($13 + 1 + 6 = 20$):
$$n(\text{Solo } W) = 25 - 20 = 5\text{ docentes}$$

---

### Pregunta 9
**¿Cuántos docentes usan exclusivamente Facebook o X?**

* **A.** 11
* **B.** 8
* **C.** 4
* **D.** 7

> **Respuesta Correcta:** **A. 11**

#### Justificación:
La disyunción exclusiva entre los que usan únicamente Facebook y los que usan únicamente X es la suma directa de sus regiones simples:
$$\text{Docentes} = n(\text{Solo } F) + n(\text{Solo } X) = 7 + 4 = 11\text{ docentes}$$

---

### Pregunta 10
**Al nombrar a los conjuntos de redes sociales de la siguiente manera: $F$: Facebook, $W$: WhatsApp y $X$, ¿cuál operación entre dichos conjuntos tiene como elemento un solo docente?**

* **A.** $(W \cup X) - F$
* **B.** $(W \cap X) - F$
* **C.** $(F \cap X) - W$
* **D.** $(W \cap F) - X$

> **Respuesta Correcta:** **B. $(W \cap X) - F$**

#### Justificación:
Analizamos la cardinalidad de cada opción:
- **A.** $n((W \cup X) - F) = n(\text{Solo } W) + n(\text{Solo } X) + n(\text{Solo } W \cap X) = 5 + 4 + 1 = 10$
- **B.** $n((W \cap X) - F) = n(W \cap X) - n(W \cap F \cap X) = 7 - 6 = \mathbf{1\text{ docente}}$
- **C.** $n((F \cap X) - W) = 8 - 6 = 2\text{ docentes}$
- **D.** $n((W \cap F) - X) = 19 - 6 = 13\text{ docentes}$

---

### Pregunta 11
**¿Cuántos docentes tendría la siguiente operación $(W \cap F) \cup (F \cap X)$?**

* **A.** 9
* **B.** 20
* **C.** 21
* **D.** 13

> **Respuesta Correcta:** **C. 21**

#### Justificación:
Aplicamos el principio de inclusión-exclusión para la unión de dos conjuntos:
$$n((W \cap F) \cup (F \cap X)) = n(W \cap F) + n(F \cap X) - n((W \cap F) \cap (F \cap X))$$
$$n((W \cap F) \cup (F \cap X)) = 19 + 8 - n(W \cap F \cap X)$$
$$n((W \cap F) \cup (F \cap X)) = 19 + 8 - 6 = 21\text{ docentes}$$

---

### Contexto de Preguntas 12 y 13: Encuesta de Gaseosas
En una encuesta sobre consumo de gaseosas entre estudiantes universitarios se registraron los siguientes resultados:
- $n(C) = 28$ (Coca-Cola)
- $n(M) = 22$ (Manzana)
- $n(K) = 25$ (Colombiana)
- $n(C \cap M) = 11$
- $n(C \cap K) = 15$
- $n(M \cap K) = 14$
- $n(C \cap M \cap K) = 8$ (las tres gaseosas)

#### Regiones Disjuntas:
1. **Triple consumo:** $n(C \cap M \cap K) = 8$
2. **Dobles exclusivas:**
   - Solo Coca-Cola y Manzana: $11 - 8 = 3$
   - Solo Coca-Cola y Colombiana: $15 - 8 = 7$
   - Solo Manzana y Colombiana: $14 - 8 = 6$
3. **Consumo exclusivo de una sola marca:**
   - Solo Coca-Cola: $28 - (3 + 7 + 8) = 28 - 18 = 10$
   - Solo Manzana: $22 - (3 + 6 + 8) = 22 - 17 = 5$
   - Solo Colombiana: $25 - (7 + 6 + 8) = 25 - 21 = 4$

---

### Pregunta 12
**¿Cuántos estudiantes fueron encuestados?**

* **A.** 35
* **B.** 39
* **C.** 43
* **D.** 31

> **Respuesta Correcta:** **C. 43**

#### Justificación:
Calculamos la cardinalidad de la unión total $C \cup M \cup K$:
$$n(C \cup M \cup K) = n(C) + n(M) + n(K) - n(C \cap M) - n(C \cap K) - n(M \cap K) + n(C \cap M \cap K)$$
$$n(C \cup M \cup K) = 28 + 22 + 25 - 11 - 15 - 14 + 8$$
$$n(C \cup M \cup K) = 75 - 40 + 8 = 43\text{ estudiantes}$$
Sumando las regiones disjuntas: $10 + 5 + 4 + 3 + 7 + 6 + 8 = 43$.

---

### Pregunta 13
**¿Cuántos estudiantes prefieren tomar Coca-Cola o Manzana ($C \cup M$)?**

* **A.** 35
* **B.** 39
* **C.** 33
* **D.** 22

> **Respuesta Correcta:** **B. 39**

#### Justificación y Aclaración Técnica:
1. El enunciado solicita la cantidad de estudiantes que prefieren Coca-Cola o Manzana (la unión $C \cup M$).
2. Aplicamos la fórmula de la unión de dos conjuntos:
   $$n(C \cup M) = n(C) + n(M) - n(C \cap M)$$
   $$n(C \cup M) = 28 + 22 - 11 = 39\text{ estudiantes}$$
3. *(Nota aclaratoria: Si se interpretara como intersección literal $C \cap M$, el valor es $11$; sin embargo, al contrastar con las opciones del examen $\{35, 39, 33, 22\}$, la pregunta evalúa la unión inclusiva de ambos conjuntos cuyo resultado es **39**).*

---

## 📌 PARTE 3: LÓGICA PROPOSICIONAL Y TABLAS DE VERDAD

### Pregunta 14
**La tabla de verdad que se presenta en la figura:**

| $p$ | $q$ | $(p \lor q)$ | $\sim(p \lor q)$ | $(p \lor q) \iff \sim(p \lor q)$ |
| :---: | :---: | :---: | :---: | :---: |
| $V$ | $V$ | $V$ | $F$ | **$F$** |
| $V$ | $F$ | $V$ | $F$ | **$F$** |
| $F$ | $V$ | $V$ | $F$ | **$F$** |
| $F$ | $F$ | $F$ | $V$ | **$F$** |

**Muestra una proposición que corresponde a una:**

* **A.** Tautología
* **B.** Contradicción
* **C.** Falacia
* **D.** Contingencia

> **Respuesta Correcta:** **B. Contradicción**

#### Justificación:
- En lógica proposicional, una fórmula bicondicional de la forma $A \iff \sim A$ siempre evalúa a falso ($F$), ya que una proposición y su negación estricta jamás pueden poseer valores de verdad idénticos.
- Puesto que la columna final contiene exclusivamente valores de Falso ($F$) para todas las combinaciones posibles de las premisas, se clasifica como una **Contradicción**.

---

### Pregunta 15
**La proposición compuesta $[(p \to q) \land p] \land \sim q$ es:**

* **A.** Una contingencia
* **B.** Una contradicción
* **C.** Una tautología
* **D.** Imposible determinar su valor de verdad

> **Respuesta Correcta:** **B. Una contradicción**

#### Justificación mediante Tabla de Verdad y Leyes Lógicas:

#### 1. Tabla de Verdad Completa:
| $p$ | $q$ | $p \to q$ | $(p \to q) \land p$ | $\sim q$ | $[(p \to q) \land p] \land \sim q$ |
| :---: | :---: | :---: | :---: | :---: | :---: |
| $V$ | $V$ | $V$ | $V$ | $F$ | **$F$** |
| $V$ | $F$ | $F$ | $F$ | $V$ | **$F$** |
| $F$ | $V$ | $V$ | $F$ | $F$ | **$F$** |
| $F$ | $F$ | $V$ | $F$ | $V$ | **$F$** |

#### 2. Demostración por Álgebra Proposicional:
$$[(p \to q) \land p] \land \sim q$$
1. Aplicando la equivalencia del condicional $p \to q \equiv \sim p \lor q$:
   $$[(\sim p \lor q) \land p] \land \sim q$$
2. Por ley de absorción / distributividad, $(\sim p \lor q) \land p \equiv p \land q$:
   $$(p \land q) \land \sim q$$
3. Por asociatividad y ley de no contradicción ($q \land \sim q \equiv F_0$):
   $$p \land (q \land \sim q) \equiv p \land F_0 \equiv F_0$$

Al ser el resultado final una constante falsa ($F_0$) en todos los casos, la proposición es una **Contradicción**.

---

## 📊 Tabla Resumen de Respuestas

| N.º | Enunciado / Tema | Opción | Respuesta / Resultado |
| :---: | :--- | :---: | :--- |
| **1** | Operación sombreada en diagrama de 3 conjuntos | **A** | $(A \cap B) \cup (A \cap C)$ |
| **2** | Diferencia de conjuntos $A - B$ | **C** | $\{2, 4, 8, 10, 14, 16, 20\}$ |
| **3** | Intersección múltiple $A \cap B \cap C$ | **A** | $\{6, 12, 18\}$ |
| **4** | Diagrama de Venn para $A \cap B \cap C$ | **D** | Región central común a los 3 círculos |
| **5** | Operación de la región sombreada | **B** | $A \cap (B \cup C)$ |
| **6** | Operación de la región sombreada en $B$ | **B** | $B - C$ |
| **7** | Total de docentes encuestados (Redes Sociales) | **A** | $40\text{ docentes}$ |
| **8** | Docentes que usan únicamente WhatsApp | **D** | $5\text{ docentes}$ |
| **9** | Docentes que usan exclusivamente Facebook o X | **A** | $11\text{ docentes}$ |
| **10** | Operación con cardinalidad igual a 1 docente | **B** | $(W \cap X) - F$ |
| **11** | Cardinalidad de $(W \cap F) \cup (F \cap X)$ | **C** | $21\text{ docentes}$ |
| **12** | Total de estudiantes encuestados (Gaseosas) | **C** | $43\text{ estudiantes}$ |
| **13** | Estudiantes que toman Coca-Cola o Manzana | **B** | $39\text{ estudiantes}$ |
| **14** | Tipo de proposición: $(p \lor q) \iff \sim(p \lor q)$ | **B** | Contradicción |
| **15** | Tipo de proposición: $[(p \to q) \land p] \land \sim q$ | **B** | Una contradicción |
