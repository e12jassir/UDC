# Protocolo Individual — Unidad 2: Estructuras de Control

**Asignatura:** Algoritmos y Programación Básica — `IX24013-B1`  
**Estudiante:** Esteban David Marrugo Jassir (Cód. 7502620036)  
**Docente:** Heybertt Moreno Díaz  
**Fecha de Entrega:** Lunes, 12 de Octubre de 2026 (Campus Virtual SIMA)  
**Modalidad:** Individual  

---

### 1. Descripción del texto o actividad a realizar:
Revisión analítica del módulo oficial de la Unidad 2 sobre «Estructuras de Control» (`Estructuras de control.pdf`) y su articulación con los tipos de datos, operadores relacionales y expresiones lógicas en Java. Estudié cómo los bloques de código gobiernan el flujo de ejecución de un programa mediante la secuenciación lineal, la toma de decisiones basada en condiciones booleanas (selección simple, doble y múltiple con `if/else/switch`) y la repetición iterativa de instrucciones (bucles `while`, `do-while` y `for`).

---

### 2. Palabras claves:
Estructuras de Control, Flujo de Ejecución, Selección Condicional (`if-else`), Selección Múltiple (`switch-case`), Bucles Iterativos (`for`, `while`, `do-while`), Condición Booleana, Cortocircuito Lógico, Bucle Infinito, Ámbito de Variables (*Scope*).

---

### 3. Objetivos de las lecturas o actividad a realizar:
• Comprender el rol de las estructuras de control como mecanismo fundamental para dirigir el orden y la toma de decisiones en un programa de software.  
• Diferenciar con precisión conceptual y práctica los tres tipos de estructuras: secuenciales, de selección (bifurcación) y de repetición (iteración).  
• Analizar la evaluación de expresiones booleanas y el impacto del cortocircuito en la toma de decisiones lógicas complejas.  
• Dominar el criterio de selección entre estructuras repetitivas según se conozca previamente el número de iteraciones (`for`) o dependa de un estado dinámico (`while`, `do-while`).

---

### 4. Conceptos claves y definiciones:
• **Estructuras de control:** Bloques de código que permiten decidir qué instrucciones ejecutar y en qué orden según condiciones o criterios predefinidos, alterando el flujo secuencial por defecto de la computadora (Ramírez, 2007).  
• **Estructuras de secuencia:** Ejecución lineal instrucción tras instrucción, donde cada paso se procesa en el orden exacto en que fue escrito en el código fuente.  
• **Estructuras de selección (`if`, `else if`, `else`, `switch`):** Mecanismos de bifurcación que evalúan una expresión lógica o variable para desviar la ejecución hacia un bloque de código u otro según el resultado booleano (`true`/`false`) o el valor coincidente (Valls Ferrán y Camacho Fernández, 2003).  
• **Estructuras de repetición / Ciclos (`while`, `do-while`, `for`):** Instrucciones que ejecutan de forma repetida un conjunto de sentencias mientras una condición se mantenga verdadera; demandan una variable de control o condición de salida para evitar ciclos infinitos.  
• **Bucle pre-test (`while`, `for`) vs. post-test (`do-while`):** En el pre-test la condición se evalúa antes de entrar al bloque (pudiendo ejecutarse cero veces); en el post-test el bloque se ejecuta al menos una vez antes de verificar la condición.  
• **Ámbito de variable (*Variable Scope*):** Región del programa donde una variable es visible y accesible; en estructuras de control, variables declaradas dentro de un bloque `{}` nacen y mueren dentro de ese bloque de memoria.

---

### 5. Resumen de la(as) lecturas:
Al leer el módulo de Estructuras de Control, me encontré con la base de todo lo que hace que un programa deje de ser una simple calculadora lineal y pase a tomar decisiones reales. Por mi cuenta ya venía programando en Python y haciendo cositas en Java, así que los condicionales y los ciclos no eran conceptos extraños para mí. Sin embargo, al estudiar el módulo con detenimiento y contrastarlo con autores como Ramírez (2007) y Valls Ferrán y Camacho Fernández (2003), lo valioso fue entender qué pasa realmente por debajo en la máquina cuando el procesador evalúa estas estructuras.

Lo primero que salta a la vista es cómo la selección condicional rompe la ejecución secuencial. Un `if` no es más que una bifurcación en el flujo basada en una evaluación booleana estricta. En Java esto tiene una disciplina fuerte: a diferencia de lenguajes como C o Python donde un número distinto de cero cuenta como verdadero, aquí la condición debe resolverse obligatoriamente a un tipo `boolean`. Además, el uso de operadores en cortocircuito (`&&`, `||`) es clave no solo para ahorrar ciclos de cómputo, sino para evitar excepciones clásicas en tiempo de ejecución (como verificar que un objeto no sea nulo antes de consultar un método). Con el `switch`, por otro lado, entendí cuándo conviene sustituir una cadena larga de `else if` cuando evaluamos valores discretos, cuidando siempre no olvidar el `break` para no caer en el temido efecto cascada (*fall-through*).

En cuanto a las estructuras de repetición, la lectura ayuda a fijar un criterio claro para elegir la herramienta correcta. El ciclo `for` es ideal cuando de entrada conocemos el número exacto de iteraciones o recorremos rangos definidos con una variable de control. En cambio, cuando el número de repeticiones depende de un evento externo (una entrada del usuario, la lectura de un archivo o una bandera de estado), el ciclo `while` es el camino natural. El `do-while` tiene un caso de uso muy puntual pero potente: menús interactivos por consola o validaciones donde necesitamos que el bloque se ejecute al menos una primera vez antes de comprobar si el usuario ingresó un dato válido. El error más común aquí sigue siendo el olvido de actualizar la variable de control dentro del cuerpo del ciclo, lo que deriva en bucles infinitos que congelan la memoria.

---

### 6. Metodología de trabajo:
Descargué la guía `Estructuras de control.pdf` desde la plataforma SIMA, la leí de forma analítica y extraje los conceptos y ejemplos directamente en mi bóveda de notas de Obsidian. Luego cargué el documento en NotebookLM para generar preguntas de autoevaluación y escuchar el resumen en formato de audio, lo que me ayuda a fijar la lógica mientras descanso la vista de la pantalla. Para validar los conceptos, abrí mi terminal en Linux y escribí pequeños programas de prueba en Java usando `javac` y `java`, testeando el comportamiento de las bifurcaciones y los ciclos con entradas intencionalmente incorrectas para observar cómo responde el control de flujo.

---

### 7. Conclusiones de la lectura o actividad:
• Las estructuras de control son el núcleo del pensamiento algorítmico: transforman secuencias de datos pasivas en sistemas interactivos capaces de reaccionar y decidir de forma autónoma.  
• Saber elegir entre un `for`, un `while` o un `do-while` no es un tema estético, sino de diseño: cada estructura responde a una naturaleza distinta del problema (iteración determinista vs. indeterminada).  
• El tipado estricto de Java en expresiones condicionales previene errores lógicos graves en tiempo de compilación que en lenguajes dinámicos suelen explotar en producción.  
• Comprender el ámbito (*scope*) de las variables declaradas dentro de bloques de control es fundamental para gestionar bien la memoria y evitar colisiones de nombres o referencias inválidas.

---

### 8. Discusiones y recomendaciones:
• Para el docente Heybertt: En la práctica profesional moderna de software se habla mucho de evitar el anidamiento excesivo de condicionales (*arrow anti-pattern* o código flecha) usando retornos tempranos (*guard clauses*). ¿Cómo recomienda usted equilibrar esa buena práctica con la exigencia académica de diseñar diagramas de flujo estructurados que a veces piden un único punto de salida?  
• ¿En qué escenarios reales de desarrollo en Java el compilador optimiza un `switch-case` mediante tablas de salto (*tableswitch* / *lookupswitch*) haciéndolo significativamente más rápido que una cadena de `if-else`?

---

### 9. Bibliografía:
• Joyanes Aguilar, L. (2020). *Fundamentos de programación: algoritmos, estructura de datos y objetos* (5.ª ed.). McGraw-Hill.  
• Ramírez, F. (2007). *Introducción a la programación: Algoritmos y su implementación en VB.NET, C#, Java y C++*. Alfaomega Grupo Editor.  
• Trejos Buriticá, O. I. (2021). *Lógica de programación: solucionario en pseudocódigo*. Ediciones de la U.  
• Universidad de Cartagena - CTEV. (2026). *Módulo Didáctico Unidad 2: Estructuras de Control — Algoritmos y Programación Básica*. Facultad de Ingeniería, Universidad de Cartagena.  
• Valls Ferrán, J. M., & Camacho Fernández, D. (2003). *Programación, algoritmos y ejercicios resueltos en JAVA*. Pearson Educación.  
• Wanumen Silva, L. F., et al. (2017). *Java básico*. Ecoe Ediciones.
