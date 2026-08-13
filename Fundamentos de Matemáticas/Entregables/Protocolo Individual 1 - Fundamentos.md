# Protocolo Individual — Unidad 1: Lógica Proposicional y Teoría de Conjuntos

**Asignatura:** Fundamentos de Matemáticas  
**Código:** `CFBD242-A1`  
**Estudiante:** Esteban David Marrugo Jassir  
**Docente:** Atilano Arrieta Vivero  
**Fecha de Entrega:** Lunes, 24 de Agosto de 2026 (SIMA - 23:59 hs)  
**Modalidad:** Individual  

---

## 1. Descripción del Tema de la Unidad

Esta unidad aborda las bases formales del razonamiento matemático: la **lógica proposicional** y la **teoría intuitiva de conjuntos**. Analicé el concepto de proposición como unidad fundamental que posee un único valor de verdad (verdadero o falso), los operadores lógicos (negación, conjunción, disyunción, condicional y bicondicional), la construcción de tablas de verdad para clasificar fórmulas en tautologías, contradicciones o contingencias, y los métodos de determinación de conjuntos por extensión y comprensión junto a sus relaciones de pertenencia e inclusión.

---

## 2. Palabras Clave

*Proposición lógica, Conectivos lógicos, Tautología, Contradicción, Equivalencia lógica, Relación de pertenencia ($x \in A$), Determinación por comprensión, Tablas de verdad.*

---

## 3. Objetivos de Aprendizaje

1. Identificar proposiciones simples y compuestas, determinando su valor de verdad mediante el uso riguroso de conectivos lógicos.
2. Construir tablas de verdad para evaluar la validez de esquemas proposicionales y comprobar equivalencias lógicas.
3. Describir y manipular conjuntos utilizando notación formal por extensión y comprensión con predicados.
4. Conectar el rigor de la lógica simbólica con el diseño de condiciones y estructuras de control en ingeniería de software.

---

## 4. Síntesis y Comprensión del Contenido

### A. Proposiciones y Conectivos Lógicos

Una proposición es un enunciado declarativo que es verdadero ($V$) o falso ($F$), sin ambigüedad. A partir de proposiciones atómicas ($P, Q, R$) construimos proposiciones moleculares mediante conectivos:

1. **Negación ($\neg P$ / $\sim P$):** Invierte el valor de verdad.
2. **Conjunción ($P \land Q$):** Verdadera únicamente si ambas proposiciones son verdaderas. En programación equivale al operador `&&`.
3. **Disyunción ($P \lor Q$):** Verdadera si al menos una componente es verdadera; solo es falsa si ambas son falsas (`||`).
4. **Condicional o Implicación ($P \Rightarrow Q$):** Solo resulta falsa cuando el antecedente ($P$) es verdadero y el consecuente ($Q$) es falso. En cualquier otro caso es verdadera.
5. **Bicondicional o Doble Implicación ($P \Leftrightarrow Q$):** Verdadera cuando ambas componentes comparten el mismo valor de verdad ($V \Leftrightarrow V$ o $F \Leftrightarrow F$).

### B. Evaluación mediante Tablas de Verdad

Para un esquema con $n$ variables proposicionales, existen $2^n$ combinaciones posibles de valores de verdad. La evaluación final clasifica la proposición en:

* **Tautología:** La última columna es exclusivamente verdadera en todos los casos posibles (ej. $P \lor \neg P$).
* **Contradicción:** La última columna es falsa en todas las combinaciones (ej. $P \land \neg P$).
* **Contingencia:** El resultado contiene al menos un valor verdadero y al menos un valor falso.

Dos proposiciones $P$ y $Q$ son **lógicamente equivalentes** ($P \equiv Q$) cuando la fórmula $P \Leftrightarrow Q$ constituye una tautología, lo que significa que poseen tablas de verdad idénticas en todas sus filas.

### C. Fundamentos de la Teoría de Conjuntos

Un conjunto es una colección bien definida de objetos llamados elementos. 

* **Pertenencia vs. Inclusión:** Si $x$ forma parte de $A$, escribimos $x \in A$. Si todos los elementos de un conjunto $B$ están dentro de $A$, se trata de inclusión: $B \subseteq A$.
* **Formas de descripción:**
  1. *Por Extensión:* Enumerando explícitamente cada elemento: $A = \{2, 4, 6, 8\}$.
  2. *Por Comprensión:* Definiendo un predicado $P(x)$ que caracteriza exclusivamente a sus miembros: $A = \{x \in \mathbb{Z} \mid x \text{ es par } \land 1 \le x \le 8\}$.

---

## 5. Reflexión y Aplicación Práctica en Ingeniería de Software

Al estudiar esta unidad, lo que más me llamó la atención es cómo la lógica proposicional no es simplemente teoría abstracta, sino el núcleo mismo de la arquitectura del software. En el código que escribimos a diario, cada instrucción condicional (`if`, `while`, filtros booleanos) ejecuta exactamente estas operaciones.

Comprender las leyes de la lógica y las tablas de verdad permite simplificar expresiones booleanas complejas, evitar errores de ejecución por condiciones mal anidadas y optimizar algoritmos. Por ejemplo, entender la implicación lógica ayuda a razonar sobre precondiciones y postcondiciones en funciones y pruebas unitarias. La notación de conjuntos, por su parte, es el lenguaje universal que estructura las bases de datos relacionales y el modelado de datos.

---

## 6. Referencias Bibliográficas

- Jiménez René, M. (2018). *Matemáticas 1*. Pearson Educación.
- Miller, C. D., Heeren, V. E., & Hornsby, J. (2013). *Matemática: Razonamiento y aplicaciones* (12.ª ed.). Pearson Educación.
- Escudero Trujillo, R. (2016). *Matemáticas básicas*. Pearson Educación.
- Universidad de Cartagena. (2026). *Módulo de la unidad 1: Fundamentos de matemáticas*. Facultad de Ingeniería.
