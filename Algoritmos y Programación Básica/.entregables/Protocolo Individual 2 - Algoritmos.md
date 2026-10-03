# Protocolo Individual — Unidad 2: Estructuras de Control

**Asignatura:** Algoritmos y Programación Básica — `IX24013-B1`  
**Estudiante:** Esteban David Marrugo Jassir (Cód. 7502620036)  
**Docente:** Heybertt Moreno Díaz  
**Fecha de Entrega:** Lunes, 12 de Octubre de 2026 (Campus Virtual SIMA)  
**Modalidad:** Individual  

---

### 1. Descripción del texto o actividad a realizar:
Revisión analítica del módulo de la Unidad 2 sobre «Estructuras de Control» (`Estructuras de control.pdf`) y su articulación práctica con los tipos de datos y operadores en Java. Contrasté los fundamentos teóricos del flujo de ejecución con mi experiencia directa desarrollando software: tanto en el proyecto formativo NOEST del SENA ADSO (donde construyo interfaces y lógica de escritorio en Java) como en mi proyecto personal Jules en Python (un asistente inteligente con flujos asincrónicos y validaciones de estado). Analicé cómo la secuenciación, la selección condicional (`if/else/switch`) y la repetición iterativa (`for/while/do-while`) determinan la estabilidad y el rendimiento de cualquier sistema real.

---

### 2. Palabras claves:
Estructuras de Control, Flujo de Ejecución, Selección Condicional (`if-else`), Selección Múltiple (`switch-case`), Bucles Iterativos (`for`, `while`, `do-while`), Cortocircuito Lógico, Ámbito de Variables (*Scope*), Proyecto NOEST, Proyecto Jules.

---

### 3. Objetivos de las lecturas o actividad a realizar:
• Comprender el rol de las estructuras de control como el mecanismo esencial que transforma instrucciones secuenciales en algoritmos capaces de evaluar condiciones y reaccionar ante eventos.  
• Contrastar la aplicación de estructuras de control entre lenguajes fuertemente tipados como Java (proyecto NOEST) y lenguajes dinámicos como Python (proyecto Jules).  
• Analizar la evaluación de expresiones booleanas y la ventaja defensiva de la evaluación en cortocircuito (`&&`, `||`) para evitar excepciones en tiempo de ejecución.  
• Establecer criterios técnicos para elegir la estructura iterativa adecuada (`for` determinista frente a `while`/`do-while` condicionados por estado).

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
Al leer la guía de Estructuras de Control, no me acerqué al tema desde cero. En el tecnólogo ADSO del SENA vengo liderando el proyecto NOEST, una aplicación de escritorio donde modelamos requisitos y flujos de usuario en Java, y por mi cuenta he venido desarrollando Jules, un proyecto en Python enfocado en automatización e inteligencia artificial. Tener código real corriendo en dos ecosistemas tan distintos cambia por completo la perspectiva sobre este módulo: uno entiende que las estructuras de control no son un capítulo teórico para memorizar antes de un examen, sino el esqueleto que sostiene la lógica de negocio.

En la teoría todo corre fluido. En la práctica, el código no perdona la improvisación. En mi proyecto Jules (Python), lidiar con respuestas de APIs o árboles de decisión exige condicionales dinámicos; sin embargo, si uno no es ordenado, la flexibilidad del lenguaje puede ocultar errores de tipo que terminan reventando en ejecución. En cambio, cuando trabajo en NOEST con Java, el compilador exige rigor desde el primer momento: la condición de un `if` solo admite valores estrictamente booleanos. Nada de evaluar enteros o cadenas vacías como verdad o falsedad. Además, en Java el operador de cortocircuito (`&&`) se vuelve una herramienta de programación defensiva indispensable: validar `objeto != null && objeto.tienePermiso()` salva al programa de un `NullPointerException` fulminante antes de que intente invocar el método.

Con las estructuras repetitivas ocurre algo similar. En Jules uso bucles para iterar colecciones y streams de datos; en NOEST los ciclos gobiernan la lectura de registros y el procesamiento de tablas. El ciclo `for` es perfecto cuando conozco de antemano el tamaño de un lote. Pero cuando dependo de que el usuario decida salir de un menú o de que un socket reciba datos, el `while` es el rey. El módulo de la universidad y autores como Ramírez (2007) y Valls Ferrán y Camacho Fernández (2003) recalcan un punto que ya he sufrido en carne propia: olvidar la actualización de la variable de control o formular mal la condición de parada crea un bucle infinito que bloquea el hilo principal y congela la aplicación. Estudiar estas estructuras con formalismo académico me sirvió para ordenar lo que ya aplicaba por intuición y escribir código mucho más limpio y predecible.

---

### 6. Metodología de trabajo:
Descargué la guía `Estructuras de control.pdf` desde la plataforma SIMA y sinteticé los conceptos centrales en mi bóveda de Obsidian. Luego cargué el documento en NotebookLM para generar preguntas de chequeo y repasar los contrastes teóricos en audio mientras descansaba de la pantalla. Para aterrizar la lectura a código ejecutable, abrí mi terminal en Linux y comparé cómo se comportan estas estructuras en mis dos entornos reales de trabajo: escribí pruebas rápidas en Java con `javac` para evaluar el manejo estricto de tipos frente al flujo equivalente en Python, testeando bifurcaciones complejas y validaciones con operadores de cortocircuito.

---

### 7. Conclusiones de la lectura o actividad:
• Las estructuras de control son el corazón del pensamiento algorítmico: transforman datos inertes en software interactivo capaz de tomar decisiones autónomas ante eventos imprevistos.  
• Trabajar en proyectos reales como NOEST (Java) y Jules (Python) demuestra que la teoría de Ramírez (2007) y Valls Ferrán (2003) se aplica idéntica en cualquier lenguaje: lo que cambia es la sintaxis y el rigor del compilador.  
• La evaluación en cortocircuito (`&&`, `||`) no es una curiosidad técnica de los libros, sino un estándar de programación defensiva para proteger el código contra excepciones en tiempo de ejecución.  
• El control estricto del ámbito de variables (*scope*) dentro de los bloques de control previene fugas de memoria y evita efectos secundarios no deseados en aplicaciones grandes.

---

### 8. Discusiones y recomendaciones:
• Para el docente Heybertt: En proyectos medianos o grandes como NOEST y Jules, el anidamiento profundo de condicionales (*código flecha*) dificulta mucho el mantenimiento y los tests unitarios. En la industria se prefieren retornos tempranos (*guard clauses*). ¿Cómo sugiere usted equilibrar esta buena práctica de ingeniería con el modelo clásico de diagramas de flujo que suele exigir un único nodo de salida?  
• En aplicaciones de escritorio o servicios de alto rendimiento en Java, ¿en qué casos el compilador `javac` optimiza un `switch` mediante instrucciones de bytecode `tableswitch` frente a `lookupswitch`, y qué impacto real tiene esto en el tiempo de CPU?

---

### 9. Bibliografía:
• Joyanes Aguilar, L. (2020). *Fundamentos de programación: algoritmos, estructura de datos y objetos* (5.ª ed.). McGraw-Hill.  
• Ramírez, F. (2007). *Introducción a la programación: Algoritmos y su implementación en VB.NET, C#, Java y C++*. Alfaomega Grupo Editor.  
• Trejos Buriticá, O. I. (2021). *Lógica de programación: solucionario en pseudocódigo*. Ediciones de la U.  
• Universidad de Cartagena - CTEV. (2026). *Módulo Didáctico Unidad 2: Estructuras de Control — Algoritmos y Programación Básica*. Facultad de Ingeniería, Universidad de Cartagena.  
• Valls Ferrán, J. M., & Camacho Fernández, D. (2003). *Programación, algoritmos y ejercicios resueltos en JAVA*. Pearson Educación.  
• Wanumen Silva, L. F., et al. (2017). *Java básico*. Ecoe Ediciones.
