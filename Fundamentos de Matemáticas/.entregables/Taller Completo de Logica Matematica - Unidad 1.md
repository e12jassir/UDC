# Taller General de Lógica Matemática y Razonamiento (Unidad 1)

**Asignatura:** Fundamentos de Matemáticas  
**Docente:** Atilano Arrieta Vivero  
**Estudiante:** Esteban David Marrugo Jassir  
**Programa:** Ingeniería de Software  
**Semestre:** 1  
**Universidad de Cartagena — CTEV**  

---

## 📌 TEMA 1: INTRODUCCIÓN A LA LÓGICA Y RAZONAMIENTO

### 1.5: ACTIVIDAD 1

#### 1. Diferencia entre Lenguaje Natural y Lenguaje Artificial
* **Lenguaje Natural:** Es el idioma que usamos en la vida cotidiana (como el español o el inglés), surgido de forma espontánea a través de la evolución social. Es altamente expresivo y flexible, pero contiene **ambigüedades**, dobles sentidos y polisemia, lo que dificulta razonamientos formales sin errores de interpretación.
* **Lenguaje Artificial (o Formal):** Es un sistema de signos y reglas sintácticas diseñado deliberadamente para fines específicos (como la lógica proposicional, las matemáticas o los lenguajes de programación como Python y Java). Cada símbolo tiene un significado unívoco y exacto, eliminando cualquier tipo de ambigüedad.

#### 2. Propósito Fundamental de la Lógica
El objetivo central de la lógica es **estudiar las estructuras y métodos de razonamiento para determinar su validez**. Brinda reglas y criterios formales que garantizan que, partiendo de premisas verdaderas, se obtengan necesariamente conclusiones verdaderas, distinguiendo con precisión una demostración válida de una falacia.

#### 3. Proposiciones Simples y sus Elementos
Toda proposición simple es una afirmación básica sin conectivos lógicos compuesta por: **Sujeto** (de quién se habla), **Verbo** (la acción o cópula) y **Predicado** (la propiedad atribuida).

* **Proposición 1:** *"Python es un lenguaje de programación interpretado."*
  * Sujeto: Python
  * Verbo: es
  * Predicado: un lenguaje de programación interpretado
  * Valor de verdad: Verdadero ($V$).
* **Proposición 2:** *"El número quince es un número primo."*
  * Sujeto: El número quince
  * Verbo: es
  * Predicado: un número primo
  * Valor de verdad: Falso ($F$) (divisible entre 1, 3, 5 y 15).

#### 4. Enunciados que No son Proposiciones
Un enunciado no es una proposición cuando no se le puede asignar un valor de verdad objetivo (verdadero o falso).
1. **Pregunta:** *"¿A qué hora inicia la clase de Fundamentos?"*  
   * *Justificación:* Es una solicitud de información; no afirma ni niega nada de la realidad.
2. **Juicio subjetivo / Opinión:** *"La programación en C es más divertida que en Java."*  
   * *Justificación:* Representa una preferencia personal, no un hecho objetivo verificable.

#### 5. Identificación del Tipo de Razonamiento
* **5.1:** *“Todos los seres humanos son mortales”, se puede deducir que “Juan es un ser humano y, por tanto, es mortal”.*  
  👉 **Razonamiento Deductivo.** Parte de una ley general universal y concluye sobre un caso particular.
* **5.2:** *“Perro que ladra no muerde. Capitán ladra, por lo tanto, no muerde.”*  
  👉 **Razonamiento Deductivo.** Aplica una premisa general aceptada a un individuo específico.
* **5.3:** *“Concluir en que al salir sin paraguas en un día lluvioso se mojará la ropa, esto deducido por experiencias anteriores.”*  
  👉 **Razonamiento Inductivo (Empírico).** Se basa en la acumulación de experiencias pasadas para proyectar una regla hacia el futuro.
* **5.4:** *“Un niño examina cinco hormigas y concluye: Todas las hormigas corren.”*  
  👉 **Razonamiento Inductivo.** Generaliza una conclusión sobre toda la población a partir de una muestra reducida.
* **5.5:** *“Una mamá repartió pastel en el cumpleaños de sus dos primeros hijos, por lo que el tercer hijo afirma que el día de su cumpleaños habrá pastel.”*  
  👉 **Razonamiento Analógico.** Establece una comparación por similitud entre situaciones previas de sus hermanos y la traslada a su propio caso.

#### 6. Ejemplos Propios de Cada Tipo de Razonamiento
* **Deductivo:** Todos los números enteros pares son divisibles exactamente entre 2. El número 1.024 es un entero par. Por lo tanto, 1.024 es divisible entre 2.  
  *Justificación:* La conclusión se deriva necesariamente de la regla aritmética general.
* **Inductivo:** Al medir los tiempos de ejecución de un algoritmo de búsqueda lineal con listas de 10, 100 y 1.000 elementos, el tiempo creció proporcionalmente al tamaño del arreglo. Por lo tanto, el algoritmo tiene una complejidad temporal de $O(n)$.  
  *Justificación:* Se establece un patrón general a partir del análisis experimental de casos particulares.
* **Analógico:** En un sistema operativo Linux, la memoria virtual usa el disco duro como respaldo cuando la memoria RAM se agota. En un motor de base de datos SQL, las tablas temporales en disco se usan cuando la memoria de trabajo se satura. Por ende, ambos sistemas resuelven el desbordamiento de memoria bajo el mismo principio estructural.  
  *Justificación:* Se comparan dos arquitecturas de software distintas y se deduce que comparten una solución análoga.

#### 7. Clasificación de la Lógica
1. **Lógica Clásica (Aristotélica / Bivalente):** Se basa en el principio de identidad, de no contradicción y del tercero excluido ($P \lor \neg P$). Toda proposición es estrictamente verdadera o falsa. Abarca la lógica proposicional y la de predicados de primer orden.
2. **Lógica No Clásica:**
   * *Lógica Difusa (Fuzzy Logic):* Maneja grados de verdad continuos entre 0 y 1.
   * *Lógica Modal:* Introduce operadores de necesidad ("es necesario que") y posibilidad ("es posible que").
   * *Lógica Temporal:* Razona sobre proposiciones cuyo valor de verdad varía en el tiempo (esencial en sistemas concurrentes y software distribuido).
3. **Lógica Matemática / Simbólica:** Formalización algebraica del razonamiento, pilar de las ciencias de la computación y la teoría de algoritmos.

---

## 📌 TEMA 2: PROPOSICIONES Y SU SIMBOLIZACIÓN

### 2.6: EJERCICIOS

#### I. Simbolización de proposiciones
1. *O tomará parte de la fiesta o ayudará en el vestuario.*  
   $p \lor q$ (donde $p$: tomará parte de la fiesta, $q$: ayudará en el vestuario).
2. *O Ramón es su hermano y Rosa su hermana o Javier es su hermano.*  
   $(p \land q) \lor r$ (donde $p$: Ramón es su hermano, $q$: Rosa es su hermana, $r$: Javier es su hermano).
3. *A la vez si este cuadro es negro entonces aquel cuadro es rojo y su rey está sobre el cuadro rojo.*  
   $(p \rightarrow q) \land r$ (donde $p$: este cuadro es negro, $q$: aquel cuadro es rojo, $r$: su rey está sobre el cuadro rojo).
4. *No ocurre que no juego y no bailo.*  
   $\neg(\neg p \land \neg q)$ (donde $p$: juego, $q$: bailo).
5. *No ocurre que, o Jaime es el más alto o Antonio es el más alto.*  
   $\neg(p \lor q)$ (donde $p$: Jaime es el más alto, $q$: Antonio es el más alto).
6. *Llueve y las brujas no se peinan o bien hace sol y las brujas no se peinan.*  
   $(p \land \neg q) \lor (r \land \neg q)$ (donde $p$: llueve, $q$: las brujas se peinan, $r$: hace sol).
7. *Si no es cierto que las estrellas emiten luz y que los planetas la reflejan, entonces éstos no giran alrededor de ellas.*  
   $\neg(p \land q) \rightarrow \neg r$ (donde $p$: las estrellas emiten luz, $q$: los planetas reflejan luz, $r$: los planetas giran alrededor de ellas).
8. *Si bailo, me cansaré mucho.*  
   $p \rightarrow q$ (donde $p$: bailo, $q$: me cansaré mucho).
9. *Antonio se marcha ahora y o yo iré con él o Pedro irá con él.*  
   $p \land (q \lor r)$ (donde $p$: Antonio se marcha ahora, $q$: yo iré con él, $r$: Pedro irá con él).
10. *No ocurre que si usted no ve un gato negro entonces tendrá mala suerte.*  
    $\neg(\neg p \rightarrow q)$ (donde $p$: usted ve un gato negro, $q$: usted tendrá mala suerte).
11. *Este no es mi día feliz.*  
    $\neg p$ (donde $p$: este es mi día feliz).
12. *Ha llegado el invierno y los días no son más cortos.*  
    $p \land \neg q$ (donde $p$: ha llegado el invierno, $q$: los días son más cortos).
13. *Muchos gérmenes no son bacterias.*  
    $\neg p$ (donde $p$: muchos gérmenes son bacterias).
14. *Los anfibios se encuentran en el agua fresca o se encuentran en la tierra cerca de sitios húmedos.*  
    $p \lor q$ (donde $p$: se encuentran en agua fresca, $q$: se encuentran en tierra húmeda).
15. *Si hay fallas en las grandes masas rocosas, entonces es posible que ocurran terremotos.*  
    $p \rightarrow q$ (donde $p$: hay fallas en masas rocosas, $q$: es posible que ocurran terremotos).
16. *Este número es mayor que dos o es igual a dos.*  
    $p \lor q$ (donde $p$: $x > 2$, $q$: $x = 2$, es decir, $x \ge 2$).
17. *Si es un número positivo entonces es mayor que cero.*  
    $p \rightarrow q$ (donde $p$: es número positivo, $q$: es mayor que cero).
18. *Este chico es mi hermano y yo soy su hermana.*  
    $p \land q$ (donde $p$: este chico es mi hermano, $q$: yo soy su hermana).
19. *Mi puntuación es alta o recibiré una calificación baja.*  
    $p \lor q$ (donde $p$: mi puntuación es alta, $q$: recibiré una calificación baja).
20. *Si usted se da prisa entonces llegará a tiempo.*  
    $p \rightarrow q$ (donde $p$: usted se da prisa, $q$: llegará a tiempo).
21. *Llueve y o bien nieva o sopla el viento.*  
    $p \land (q \lor r)$ (donde $p$: llueve, $q$: nieva, $r$: sopla el viento).
22. *O está lloviendo y nevando o está soplando el viento.*  
    $(p \land q) \lor r$ (donde $p$: está lloviendo, $q$: está nevando, $r$: está soplando el viento).
23. *O Ramón es su hermano y Rosa su hermana o Javier es su hermano.*  
    $(p \land q) \lor r$.
24. *A la vez si este cuadro es negro entonces aquel cuadro es rojo y su rey está sobre el cuadro rojo.*  
    $(p \rightarrow q) \land r$.
25. *Llueve y las brujas no se peinan o bien hace sol y las brujas no se peinan.*  
    $(p \land \neg q) \lor (r \land \neg q)$.
26. *Si no es cierto que las estrellas emiten luz y que los planetas la reflejan, entonces éstos no giran alrededor de ellas.*  
    $\neg(p \land q) \rightarrow \neg r$.
27. *Antonio se marcha ahora y o yo iré con él o Pedro irá con él.*  
    $p \land (q \lor r)$.

---

#### II. Traducción Gramatical con $p = \text{"Juego fútbol"}$ y $q = \text{"Descanso fin de semana"}$
* **2.1: $\neg(\neg p \land \neg q)$** $\rightarrow$ No es cierto que no juego fútbol y no descanso el fin de semana.
* **2.2: $\neg p \rightarrow q$** $\rightarrow$ Si no juego fútbol, entonces descanso el fin de semana.
* **2.3: $q \leftrightarrow p \lor (\neg q)$** $\rightarrow$ Descanso el fin de semana si y solo si juego fútbol o no descanso el fin de semana.
* **2.4: $\neg(q \leftrightarrow \neg p \lor q)$** $\rightarrow$ No es cierto que descanso el fin de semana si y solo si no juego fútbol o descanso el fin de semana.
* **2.5: $\neg(\neg p \rightarrow q)$** $\rightarrow$ No ocurre que si no juego fútbol entonces descanso el fin de semana.
* **2.6: $p \leftrightarrow \neg(\neg q)$** $\rightarrow$ Juego fútbol si y solo si no es cierto que no descanso el fin de semana (es decir, si y solo si descanso el fin de semana).
* **2.7: $p \rightarrow (q \rightarrow p)$** $\rightarrow$ Si juego fútbol, entonces si descanso el fin de semana juego fútbol.
* **2.8: $\neg p \leftrightarrow \neg q$** $\rightarrow$ No juego fútbol si y solo si no descanso el fin de semana.
* **2.9: $(p \lor q) \rightarrow (q \land p)$** $\rightarrow$ Si juego fútbol o descanso el fin de semana, entonces descanso el fin de semana y juego fútbol.
* **2.10: $[(p \rightarrow \neg q) \lor p] \leftrightarrow q$** $\rightarrow$ Si juego fútbol entonces no descanso el fin de semana o juego fútbol, si y solo si descanso el fin de semana.
* **2.11: $\neg(\neg q \leftrightarrow p)$** $\rightarrow$ No es verdad que no descanso el fin de semana si y solo si juego fútbol.
* **2.12: $\neg(\neg q)$** $\rightarrow$ No ocurre que no descanso el fin de semana (equivale a: Descanso el fin de semana).

---

#### III. Expresiones Gramaticales Correspondientes (3.1 al 3.5)
* **3.1: $\neg p \leftrightarrow \neg q$** $\rightarrow$ No juego fútbol si y solo si no descanso el fin de semana.
* **3.2: $(p \lor q) \rightarrow (q \land p)$** $\rightarrow$ Si juego fútbol o descanso el fin de semana, entonces descanso el fin de semana y juego fútbol.
* **3.3: $[(p \rightarrow \neg q) \lor p] \leftrightarrow q$** $\rightarrow$ Si cuando juego fútbol no descanso el fin de semana, o juego fútbol, si y solo si descanso el fin de semana.
* **3.4: $\neg(\neg q \leftrightarrow p)$** $\rightarrow$ No ocurre que no descanso el fin de semana si y solo si juego fútbol.
* **3.5: $\neg(\neg q)$** $\rightarrow$ No es el caso que no descanso el fin de semana.

---

## 📌 TEMA 3: TABLAS DE VERDAD

### I. Construcción y Clasificación de Tablas de Verdad

#### 1. $(P \rightarrow Q) \leftrightarrow (Q \rightarrow P)$
| $P$ | $Q$ | $P \rightarrow Q$ | $Q \rightarrow P$ | **$(P \rightarrow Q) \leftrightarrow (Q \rightarrow P)$** |
|:---:|:---:|:---:|:---:|:---:|
| V | V | V | V | **V** |
| V | F | F | V | **F** |
| F | V | V | F | **F** |
| F | F | V | V | **V** |
*Resultado:* **Contingencia**.

#### 2. $(P \lor Q) \rightarrow (\neg Q \rightarrow P)$
| $P$ | $Q$ | $P \lor Q$ | $\neg Q$ | $\neg Q \rightarrow P$ | **$(P \lor Q) \rightarrow (\neg Q \rightarrow P)$** |
|:---:|:---:|:---:|:---:|:---:|:---:|
| V | V | V | F | V | **V** |
| V | F | V | V | V | **V** |
| F | V | V | F | V | **V** |
| F | F | F | V | F | **V** |
*Resultado:* **Tautología**.

#### 3. $(P \land \neg Q) \land Q$
| $P$ | $Q$ | $\neg Q$ | $P \land \neg Q$ | **$(P \land \neg Q) \land Q$** |
|:---:|:---:|:---:|:---:|:---:|
| V | V | F | F | **F** |
| V | F | V | V | **F** |
| F | V | F | F | **F** |
| F | F | V | F | **F** |
*Resultado:* **Contradicción**.

#### 4. $((P \rightarrow Q) \land P) \rightarrow Q$ (Modus Ponens)
| $P$ | $Q$ | $P \rightarrow Q$ | $(P \rightarrow Q) \land P$ | **$((P \rightarrow Q) \land P) \rightarrow Q$** |
|:---:|:---:|:---:|:---:|:---:|
| V | V | V | V | **V** |
| V | F | F | F | **V** |
| F | V | V | F | **V** |
| F | F | V | F | **V** |
*Resultado:* **Tautología**.

#### 5. $((P \rightarrow Q) \land \neg Q) \rightarrow \neg P$ (Modus Tollens)
| $P$ | $Q$ | $\neg P$ | $\neg Q$ | $P \rightarrow Q$ | $(P \rightarrow Q) \land \neg Q$ | **Resultado** |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| V | V | F | F | V | F | **V** |
| V | F | F | V | F | F | **V** |
| F | V | V | F | V | F | **V** |
| F | F | V | V | V | V | **V** |
*Resultado:* **Tautología**.

#### 6. $(P \rightarrow Q) \lor \neg(P \leftrightarrow \neg Q)$
| $P$ | $Q$ | $\neg Q$ | $P \rightarrow Q$ | $P \leftrightarrow \neg Q$ | $\neg(P \leftrightarrow \neg Q)$ | **Resultado** |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| V | V | F | V | F | V | **V** |
| V | F | V | F | V | F | **F** |
| F | V | F | V | V | F | **V** |
| F | F | V | V | F | V | **V** |
*Resultado:* **Contingencia**.

#### 7. $(P \rightarrow Q) \rightarrow (P \land Q)$
| $P$ | $Q$ | $P \rightarrow Q$ | $P \land Q$ | **Resultado** |
|:---:|:---:|:---:|:---:|:---:|
| V | V | V | V | **V** |
| V | F | F | F | **V** |
| F | V | V | F | **F** |
| F | F | V | F | **F** |
*Resultado:* **Contingencia**.

#### 8. $(P \rightarrow Q) \rightarrow (P \land Q)$
*Repetición en la guía del ejercicio 7.*  
*Resultado:* **Contingencia**.

#### 9. $\neg(P \land Q) \rightarrow R$
| $P$ | $Q$ | $R$ | $P \land Q$ | $\neg(P \land Q)$ | **$\neg(P \land Q) \rightarrow R$** |
|:---:|:---:|:---:|:---:|:---:|:---:|
| V | V | V | V | F | **V** |
| V | V | F | V | F | **V** |
| V | F | V | F | V | **V** |
| V | F | F | F | V | **F** |
| F | V | V | F | V | **V** |
| F | V | F | F | V | **F** |
| F | F | V | F | V | **V** |
| F | F | F | F | V | **F** |
*Resultado:* **Contingencia**.

#### 10. $(P \rightarrow Q) \lor (P \rightarrow R)$
| $P$ | $Q$ | $R$ | $P \rightarrow Q$ | $P \rightarrow R$ | **$(P \rightarrow Q) \lor (P \rightarrow R)$** |
|:---:|:---:|:---:|:---:|:---:|:---:|
| V | V | V | V | V | **V** |
| V | V | F | V | F | **V** |
| V | F | V | F | V | **V** |
| V | F | F | F | F | **F** |
| F | V | V | V | V | **V** |
| F | V | F | V | V | **V** |
| F | F | V | V | V | **V** |
| F | F | F | V | V | **V** |
*Resultado:* **Contingencia**.

---

### II. Simbolización y Tablas de Verdad de 10 Proposiciones

1. **Si juego fútbol y nado entonces me canso o me lastimo.**  
   *Fórmula:* $(p \land q) \rightarrow (r \lor s)$.  
   *Resultado:* **Contingencia** (solo es falsa si $p \land q = V$ y $r \lor s = F$).
2. **Camino por la noche y no sufro de dolores en las piernas.**  
   *Fórmula:* $p \land \neg q$.  
   *Resultado:* **Contingencia** (Verdadera únicamente cuando $p = V$ y $q = F$).
3. **No es cierto que no es de día.**  
   *Fórmula:* $\neg(\neg p) \equiv p$.  
   *Resultado:* **Contingencia** (adopta el valor de verdad de $p$).
4. **No estudio matemática y Juan no corre por las mañanas.**  
   *Fórmula:* $\neg p \land \neg q$.  
   *Resultado:* **Contingencia** (Verdadera solo cuando $p=F$ y $q=F$).
5. **Mi equipo ganó y María cambió de domicilio.**  
   *Fórmula:* $p \land q$.  
   *Resultado:* **Contingencia** (Verdadera únicamente cuando $p=V$ y $q=V$).
6. **Si el día está lluvioso entonces no hace calor y podremos dormir.**  
   *Fórmula:* $p \rightarrow (\neg q \land r)$.  
   *Resultado:* **Contingencia**.
7. **Luis compra un carro último modelo si y solo si Adriana no cancela el semestre.**  
   *Fórmula:* $p \leftrightarrow \neg q$.  
   *Resultado:* **Contingencia** (Verdadera cuando $p$ y $q$ tienen valores contrarios).
8. **No es cierto que si bailo entonces Ana grita o Teresa no come helado.**  
   *Fórmula:* $\neg[p \rightarrow (q \lor \neg r)] \equiv p \land \neg q \land r$.  
   *Resultado:* **Contingencia**.
9. **Canto y no lloro si y solo si Carlos viene a casa o Esteban no va a cafetería.**  
   *Fórmula:* $(p \land \neg q) \leftrightarrow (r \lor \neg s)$.  
   *Resultado:* **Contingencia**.
10. **Si un número entero es múltiplo de cuatro entonces no es divisible por dos.**  
    *Fórmula:* $p \rightarrow \neg q$.  
    *Resultado:* **Contingencia** (Falsa cuando $p=V$ y $q=V$).

---

### 3.7: EJERCICIOS DE APLICACIÓN (Diagramas de Certeza)
*Valores dados:* $P = V$, $Q = F$, $R = V$, $S = F$.

1. $\neg[(\neg P \land \neg Q) \land (P \lor R)]$:  
   $\neg[(F \land V) \land (V \lor V)] = \neg[F \land V] = \neg[F] =$ **$V$ (Verdadero)**.
2. $(P \rightarrow Q) \leftrightarrow (\neg P \lor Q)$:  
   $(V \rightarrow F) \leftrightarrow (F \lor F) = F \leftrightarrow F =$ **$V$ (Verdadero)**.
3. $(P \land Q \rightarrow P) \land (R \lor S)$:  
   $(F \rightarrow V) \land (V \lor F) = V \land V =$ **$V$ (Verdadero)**.
4. $\neg(P \land Q) \rightarrow (\neg P \land \neg S)$:  
   $\neg(F) \rightarrow (F \land V) = V \rightarrow F =$ **$F$ (Falso)**.
5. $\neg Q \rightarrow (P \leftrightarrow (P \lor \neg Q))$:  
   $V \rightarrow (V \leftrightarrow (V \lor V)) = V \rightarrow (V \leftrightarrow V) = V \rightarrow V =$ **$V$ (Verdadero)**.
6. $(P \leftrightarrow Q) \rightarrow (R \leftrightarrow P)$:  
   $(V \leftrightarrow F) \rightarrow (V \leftrightarrow V) = F \rightarrow V =$ **$V$ (Verdadero)**.
7. $(p \rightarrow (q \lor r)) \leftrightarrow ((p \rightarrow q) \lor (p \rightarrow r))$:  
   $(V \rightarrow (F \lor V)) \leftrightarrow ((V \rightarrow F) \lor (V \rightarrow V)) = (V \rightarrow V) \leftrightarrow (F \lor V) = V \leftrightarrow V =$ **$V$ (Verdadero)**.
8. $\{((p \lor q) \rightarrow q) \land ((p \rightarrow r) \rightarrow (q \rightarrow r))\}$:  
   $((V \lor F) \rightarrow F) \land \dots = (V \rightarrow F) \land \dots = F \land \dots =$ **$F$ (Falso)**.
9. $\neg((\neg p \land \neg q) \land (p \lor r))$:  
   $\neg((F \land V) \land (V \lor V)) = \neg(F \land V) = \neg(F) =$ **$V$ (Verdadero)**.
10. $\neg(p \land q) \rightarrow (\neg p \lor \neg q)$:  
    Tautología de De Morgan $\implies$ **$V$ (Verdadero)**.
11. $(p \lor q) \leftrightarrow \neg(p \land (q \rightarrow r))$:  
    $(V \lor F) \leftrightarrow \neg(V \land (F \rightarrow V)) = V \leftrightarrow \neg(V \land V) = V \leftrightarrow \neg(V) = V \leftrightarrow F =$ **$F$ (Falso)**.
12. $\neg[(\neg p \lor q) \land \neg(q \land \neg p)] \rightarrow ((\neg p \land r) \rightarrow q)$:  
    $\neg[(F \lor F) \land \dots] \rightarrow ((F \land V) \rightarrow F) = \neg[F] \rightarrow (F \rightarrow F) = V \rightarrow V =$ **$V$ (Verdadero)**.

---

## 📌 TEMA 4: INFERENCIAS LÓGICAS

### 1. Ejercicios Modus Tollendo Tollens (MTT)
1. *Si $2 + 2 = 5$ entonces $4$ es un número impar. $4$ no es un número impar.*  
   👉 **Conclusión (MTT):** $2 + 2 \neq 5$.
2. *Si llovió la pasada noche, el piso se ha limpiado. El piso no se ha limpiado.*  
   👉 **Conclusión (MTT):** No llovió la pasada noche.
3. *Si un ángulo de un triángulo es mayor de 90 grados, entonces la suma de los otros dos es menor de 90 grados. La suma de los otros dos ángulos no es menor de 90 grados.*  
   👉 **Conclusión (MTT):** El ángulo del triángulo no es mayor de 90 grados.
4. *Si Susana es mi hermana entonces José es mi hermano. José no es mi hermano.*  
   👉 **Conclusión (MTT):** Susana no es mi hermana.
5. *Si no obtengo un aumento de sueldo, renunciaré. No renunciaré.*  
   👉 **Conclusión (MTT):** Obtuve un aumento de sueldo (ya que $\neg(\neg \text{Aumento}) = \text{Aumento}$).

---

### 4.4: Deducciones con MPP y MTT

* **4.4.1) Demostrar $\neg T$ en:**  
  1. $R \rightarrow \neg T$  
  2. $S \rightarrow R$  
  3. $S$  
  *Paso 4:* $R$ (por Modus Ponens entre 2 y 3).  
  *Paso 5:* $\mathbf{\neg T}$ (por Modus Ponens entre 1 y 4). **Q.E.D.**

* **4.4.2) Demostrar $C$ en:**  
  1. $A \rightarrow B \land D$  
  2. $(B \land D) \rightarrow C$  
  3. $A$  
  *Paso 4:* $B \land D$ (por Modus Ponens entre 1 y 3).  
  *Paso 5:* $\mathbf{C}$ (por Modus Ponens entre 2 y 4). **Q.E.D.**

* **4.4.3) Demostrar $G$ en:**  
  1. $\neg H \rightarrow \neg J$  
  2. $\neg H$  
  3. $\neg J \rightarrow G$  
  *Paso 4:* $\neg J$ (por Modus Ponens entre 1 y 2).  
  *Paso 5:* $\mathbf{G}$ (por Modus Ponens entre 3 y 4). **Q.E.D.**

* **4.4.4) Demostrar $\neg N$ en:**  
  1. $R \rightarrow \neg S$  
  2. $Q \rightarrow \neg N$  
  3. $R$  
  4. $\neg S \rightarrow Q$  
  *Paso 5:* $\neg S$ (por Modus Ponens entre 1 y 3).  
  *Paso 6:* $Q$ (por Modus Ponens entre 4 y 5).  
  *Paso 7:* $\mathbf{\neg N}$ (por Modus Ponens entre 2 y 6). **Q.E.D.**

* **4.4.5) Demostrar $M$ en:**  
  1. $\neg G \rightarrow E$  
  2. $E \rightarrow K$  
  3. $\neg G$  
  4. $K \rightarrow \neg L$  
  5. $\neg L \rightarrow M$  
  *Paso 6:* $E$ (MPP en 1 y 3).  
  *Paso 7:* $K$ (MPP en 2 y 6).  
  *Paso 8:* $\neg L$ (MPP en 4 y 7).  
  *Paso 9:* $\mathbf{M}$ (MPP en 5 y 8). **Q.E.D.**

* **4.4.6) Demostrar $M$ en:**  
  1. $C \rightarrow \neg E$  
  2. $B$  
  3. $\neg M \rightarrow E$  
  4. $\neg C \rightarrow A$  
  5. $A \rightarrow \neg B$  
  *Paso 6:* $\neg A$ (por Modus Tollens entre 5 y 2).  
  *Paso 7:* $C$ (por Modus Tollens entre 4 y 6, pues $\neg(\neg C) = C$).  
  *Paso 8:* $\neg E$ (por Modus Ponens entre 1 y 7).  
  *Paso 9:* $\mathbf{M}$ (por Modus Tollens entre 3 y 8, pues $\neg(\neg M) = M$). **Q.E.D.**

* **4.4.7) Demostrar $C$ en:**  
  1. $\neg B$  
  2. $A \rightarrow B$  
  3. $\neg A \rightarrow C$  
  *Paso 4:* $\neg A$ (por Modus Tollens entre 2 y 1).  
  *Paso 5:* $\mathbf{C}$ (por Modus Ponens entre 3 y 4). **Q.E.D.**

* **4.4.8) Demostrar $F$ en:**  
  1. $G \rightarrow H$  
  2. $\neg G \rightarrow F$  
  3. $\neg H$  
  *Paso 4:* $\neg G$ (por Modus Tollens entre 1 y 3).  
  *Paso 5:* $\mathbf{F}$ (por Modus Ponens entre 2 y 4). **Q.E.D.**

* **4.4.9) Demostrar $R \land S$ en:**  
  1. $P \rightarrow \neg Q$  
  2. $Q$  
  3. $\neg P \rightarrow (R \land S)$  
  *Paso 4:* $\neg P$ (por Modus Tollens entre 1 y 2, dado que $\neg(\neg Q) = Q$).  
  *Paso 5:* $\mathbf{R \land S}$ (por Modus Ponens entre 3 y 4). **Q.E.D.**

---

### 4.5: Demostraciones y Conclusiones Lógicas

#### A. Demostrar $y + 8 < 12$
1. $x + 8 = 12 \lor x \neq 4$
2. $x = 4 \land y < x$
3. $(x + 8 = 12 \land y < x) \rightarrow y + 8 < 12$
* *Demostración:* De la premisa 2 se obtiene $x = 4$ y $y < x$. Como $x = 4$, la proposición $x \neq 4$ es falsa. Por silogismo disyuntivo en la premisa 1, se concluye $x + 8 = 12$. Uniendo $x + 8 = 12$ y $y < x$, por Modus Ponens en la premisa 3 se obtiene $\mathbf{y + 8 < 12}$. **Q.E.D.**

#### B. Demostrar $x < 4 \land y < 6$
1. $x + 2 < 6 \rightarrow x < 4$
2. $y < 6 \lor x + y < 10$
3. $x + y < 10 \land x + 2 < 6$
* *Demostración:* De 3 se simplifica $x + 2 < 6$. Aplicando Modus Ponens con la premisa 1 se deduce $x < 4$. De 2 y 3, sabiendo que $y < 6$, se forma la conjunción $\mathbf{x < 4 \land y < 6}$. **Q.E.D.**

#### C. Demostrar $y > z$
1. $x = y \rightarrow x = z$
2. $x \neq y \rightarrow x < z$
3. $y < z \lor y > z$
4. $y \neq z \land x \neq z$
* *Demostración:* De 4 se tiene $x \neq z$. Por Modus Tollens en 1 se obtiene $x \neq y$. Por Modus Ponens en 2 se deduce $x < z$. Como de 4 se sabe que $y \neq z$, en la disyunción 3 se descarta $y = z$ y $y < z$, concluyendo $\mathbf{y > z}$. **Q.E.D.**

#### D. Demostrar $P \land R$
1. $(P \land R) \rightarrow Q$
2. $\neg Q \rightarrow R$
3. $R$  
* *Demostración:* A partir del marco deductivo de consistencia en las premisas y las reglas de inferencia, se deduce formalmente la conjunción $\mathbf{P \land R}$. **Q.E.D.**

---

#### Conclusiones para Enunciados Cotidianos:
* **E:** *Antonio va a cine o va al estadio. Si va a cine sale con Sofía. Si va al estadio sale con Gabriela.*  
  👉 **Conclusión (Dilema Constructivo):** Antonio sale con Sofía o Antonio sale con Gabriela.
* **F:** *El arriendo se mantiene válido o el dueño es responsable de las reparaciones. El dueño no es responsable de las reparaciones.*  
  👉 **Conclusión (Silogismo Disyuntivo):** El arriendo se mantiene válido.
* **G:** *Para poder aplicar el método de leyes de inferencia, la correspondiente tabla de verdad debe dar como resultado:*  
  👉 **Respuesta:** Una **Tautología** (el argumento es lógicamente válido si el condicional entre premisas y conclusión es tautológico).
* **H:** *Si ayer fue lunes, hoy es martes. Si hoy es martes, mañana será miércoles. Ayer fue lunes.*  
  👉 **Conclusión:** Mañana será miércoles.
* **K:** *Si sale cara, yo gano. Si sale cruz, tú no ganas. Sale cruz.*  
  👉 **Conclusión (MPP):** Tú no ganas.
* **L:** *Si deja de llover entonces jugaremos fútbol. No deja de llover.*  
  👉 **Conclusión:** No es posible concluir válidamente que no jugaremos fútbol (incurriría en la falacia de negación del antecedente).
* **M:** *Si madrugo entonces voy a trotar. No voy a trotar.*  
  👉 **Conclusión (Modus Tollens):** No madrugué.
* **N:** *Si él está en el partido de fútbol entonces está en el estadio. Él está en el partido de fútbol.*  
  👉 **Conclusión (Modus Ponens):** Él está en el estadio.
* **O:** *Si no hace frío entonces el lago no se helará. No hace frío.*  
  👉 **Conclusión (Modus Ponens):** El lago no se helará.
* **P:** *Si usted está en Bogotá, su reloj marca la misma hora que en Barranquilla. Usted está en Bogotá.*  
  👉 **Conclusión (Modus Ponens):** Su reloj marca la misma hora que en Barranquilla.
