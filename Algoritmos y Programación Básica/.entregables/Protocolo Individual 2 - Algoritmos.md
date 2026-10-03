# Protocolo Individual — Unidad 2: Estructuras de Control

**Asignatura:** Algoritmos y Programación Básica — `IX24013-B1`  
**Estudiante:** Esteban David Marrugo Jassir (Cód. 7502620036)  
**Docente:** Heybertt Moreno Díaz  
**Fecha de Entrega:** Lunes, 12 de Octubre de 2026 (Campus Virtual SIMA)  
**Modalidad:** Individual  

---

### 1. Descripción del texto o actividad a realizar:
Revisión analítica del módulo de la Unidad 2 sobre «Estructuras de Control» (`Estructuras de control.pdf`) y su articulación práctica con los tipos de datos y operadores lógicos en Java. Contrasté los fundamentos teóricos del flujo de ejecución con mi experiencia directa desarrollando software: tanto en el proyecto formativo NOEST del SENA ADSO (aplicación de escritorio en Java) como en mi proyecto personal Jules en Python (asistente de automatización con flujos asincrónicos). Analicé cómo la secuenciación, la selección condicional (`if/else/switch`) y la repetición iterativa (`for/while/do-while`) determinan la estabilidad, la legibilidad y el comportamiento de un sistema en producción.

---

### 2. Palabras claves:
Estructuras de Control, Flujo de Ejecución, Selección Condicional (`if-else`), Selección Múltiple (`switch-case`), Bucles Iterativos (`for`, `while`, `do-while`), Cortocircuito Lógico, Ámbito de Variables (*Variable Scope*), Proyecto NOEST, Proyecto Jules.

---

### 3. Objetivos de las lecturas o actividad a realizar:
• Comprender el rol de las estructuras de control como el mecanismo formal que transforma instrucciones secuenciales en algoritmos capaces de evaluar condiciones y reaccionar ante eventos (Joyanes Aguilar, 2020).  
• Contrastar el comportamiento de las estructuras condicionales e iterativas entre lenguajes fuertemente tipados como Java (Wanumen Silva et al., 2017) y lenguajes dinámicos como Python.  
• Analizar la evaluación booleana y la ventaja técnica del cortocircuito lógico (`&&`, `||`) como estándar de programación defensiva frente a referencias nulas o llamadas inválidas.  
• Evaluar las diferencias en el ámbito de las variables (*scope*) entre bloques de control estructurados en Java y el alcance por función en Python.  
• Establecer criterios técnicos de selección entre estructuras repetitivas según la naturaleza del problema (iteración determinista vs. ciclos condicionados por eventos).

---

### 4. Conceptos claves y definiciones:
• **Estructuras de control:** Bloques sintácticos que permiten alterar el flujo secuencial por defecto de una computadora, determinando qué instrucciones se ejecutan y en qué orden según condiciones lógicas o estados del sistema (Ramírez, 2007; Trejos Buriticá, 2021).  
• **Estructuras de secuencia:** Ejecución lineal instrucción tras instrucción, donde el procesador avanza paso a paso en el orden estricto en que fue escrito el código fuente.  
• **Estructuras de selección (`if`, `else if`, `else`):** Mecanismos de bifurcación que evalúan una expresión relacional o lógica para desviar la ejecución hacia una rama determinada según el resultado booleano (`true`/`false`) (Valls Ferrán y Camacho Fernández, 2003).  
• **Selección múltiple (`switch-case`):** Estructura que evalúa una variable discreta frente a múltiples casos constantes; en Java requiere cláusulas `break` para evitar la ejecución en cascada (*fall-through*) hacia los casos subsiguientes (Wanumen Silva et al., 2017).  
• **Estructuras de repetición / Ciclos (`while`, `do-while`, `for`):** Instrucciones que ejecutan de forma repetida un conjunto de sentencias mientras una condición lógica se mantenga verdadera; demandan una variable de control o condición de salida explícita para evitar ciclos infinitos (Joyanes Aguilar, 2020).  
• **Bucle pre-test (`while`, `for`) vs. post-test (`do-while`):** En el pre-test la condición se verifica antes de ingresar al cuerpo del bucle (pudiendo ejecutarse cero veces); en el post-test el cuerpo se ejecuta al menos una vez antes de evaluar la condición.  
• **Ámbito de variable (*Variable Scope*):** Contexto o región del código donde una variable es visible y accesible; en Java, las variables declaradas dentro de un bloque `{}` quedan confinadas a él, evitando colisiones de nombres y efectos secundarios en el estado global.

---

### 5. Resumen de la(as) lecturas:
Al estudiar la guía de Estructuras de Control (CTEV, 2026), no abordé el tema de manera abstracta. En el tecnólogo ADSO del SENA lidero el desarrollo del proyecto NOEST, una aplicación de escritorio donde modelamos interfaces y reglas de negocio en Java, mientras que de forma paralela desarrollo Jules, un proyecto en Python orientado a la automatización e inteligencia artificial. Comparar el comportamiento del código en dos plataformas con filosofías tan distintas permite entender que las estructuras de control no son un requisito académico aislado, sino el andamiaje sobre el cual se sustenta la lógica de cualquier software (Joyanes Aguilar, 2020).

La primera diferencia crítica aparece en la selección condicional. En Python (Jules), el lenguaje permite evaluar directamente la veracidad implícita (*truthiness*) de cualquier objeto. Por ejemplo, al validar una respuesta de un servicio mediante `if respuesta:`, si la variable contiene una lista vacía `[]`, un diccionario vacío `{}` o el valor numérico `0`, Python interpreta la condición como falsa. Esto resulta cómodo para escribir scripts rápidos, pero puede camuflar comportamientos imprevistos si una respuesta vacía era válida en el flujo del sistema. En contraste, cuando implemento validaciones en NOEST con Java, el compilador impone un tipado estricto (Wanumen Silva et al., 2017): la condición dentro de un `if` debe resolverse forzosamente como un tipo primitivo `boolean`. Validaciones como `if (respuesta)` provocan un error inmediato en tiempo de compilación; el desarrollador está obligado a escribir `if (respuesta != null && !respuesta.isEmpty())`. Aquí el operador de cortocircuito (`&&`) actúa como una barrera de programación defensiva esencial, deteniendo la evaluación si la primera parte es falsa y previniendo excepciones críticas de puntero nulo (*NullPointerException*).

En cuanto a la selección múltiple, el módulo formaliza el uso de la estructura `switch-case` (Ramírez, 2007; Valls Ferrán y Camacho Fernández, 2003). En aplicaciones de escritorio como NOEST, donde se gestionan opciones de menú por consola o estados fijos de un módulo, encadenar múltiples `else if` genera un código extenso y difícil de mantener. El `switch` organiza la bifurcación de manera más legible al evaluar valores discretos (`int`, `char`, `String` o enumeraciones). Sin embargo, exige una atención rigurosa a la sentencia `break`, ya que su omisión produce la ejecución consecutiva no deseada de los bloques siguientes (*fall-through*), un error lógico clásico que no es detectado por el compilador.

Un aspecto fundamental que vincula estas estructuras con la gestión del estado es el ámbito de las variables (*variable scope*). En Java, una variable de control declarada en el encabezado de un bucle `for (int i = 0; i < limite; i++)` tiene un ciclo de vida estrictamente acotado al cuerpo del ciclo; intentar acceder a `i` fuera de las llaves produce un error sintáctico. En Python, en cambio, la variable iteradora de un ciclo `for item in coleccion:` sobrevive a la finalización del bucle y permanece accesible en el resto de la función, lo que puede provocar sobreescrituras accidentales de variables si se reutiliza el mismo identificador. Comprender esta distinción permite estructurar métodos más seguros y evitar efectos secundarios indeseados (Trejos Buriticá, 2021).

Finalmente, frente a las estructuras de repetición, la teoría establece un criterio técnico riguroso de selección. El ciclo `for` es la opción adecuada cuando se conoce de antemano el número de iteraciones o se procesa un conjunto acotado de elementos. Por el contrario, el ciclo `while` resulta la alternativa idónea cuando las repeticiones dependen de una condición dinámica o de un evento externo, como esperar la conexión de un socket o la confirmación del usuario. La estructura `do-while` cubre un caso específico pero relevante: la validación de entradas por consola, asegurando que el bloque se ejecute al menos una vez antes de verificar la condición. Autores como Ramírez (2007) y Joyanes Aguilar (2020) enfatizan la necesidad de garantizar la modificación de la variable de control dentro del cuerpo del bucle, evitando condiciones de parada inalcanzables que deriven en bucles infinitos y bloqueen la ejecución del programa.

---

### 6. Metodología de trabajo:
Descargué la guía `Estructuras de control.pdf` desde la plataforma SIMA (CTEV, 2026) y sinteticé los conceptos centrales en mi bóveda de Obsidian. Luego cargué el documento en NotebookLM para formular preguntas de autoevaluación y contrastar las definiciones de los autores en formato de audio. Para consolidar el aprendizaje, utilicé la terminal en Linux y ejecuté pruebas de código comparativas: programé rutinas de prueba en Java utilizando `javac` para verificar la rigidez del tipado booleano y el aislamiento de variables dentro de bloques `{}` en NOEST, contrastándolo con el comportamiento dinámico de los bucles y condicionales en mi proyecto Jules en Python.

---

### 7. Conclusiones de la lectura o actividad:
• Las estructuras de control constituyen el núcleo del pensamiento algorítmico estructurado: transforman secuencias pasivas de instrucciones en sistemas adaptativos capaces de bifurcar y repetir procesos según el estado de los datos (Joyanes Aguilar, 2020; Trejos Buriticá, 2021).  
• El tipado estricto en Java (Wanumen Silva et al., 2017) frente al tipado dinámico en Python impone estilos de programación distintos: mientras que Python prioriza la concisión con evaluaciones implícitas de veracidad, Java exige evaluaciones booleanas explícitas que ayudan a detectar inconsistencias lógicas desde la fase de compilación.  
• La evaluación lógica en cortocircuito (`&&`, `||`) representa una técnica indispensable de programación defensiva para proteger el software contra excepciones en tiempo de ejecución al interactuar con referencias a objetos.  
• El control del ámbito de las variables (*variable scope*) dentro de los bloques de control previene la contaminación de nombres y evita mutaciones accidentales del estado en aplicaciones complejas.  
• La selección entre `for`, `while` y `do-while` debe obedecer a criterios de ingeniería: determinar si la iteración es conocida a priori o si depende de estados asincrónicos o eventos de entrada.

---

### 8. Discusiones y recomendaciones:
• Para el docente Heybertt: En el desarrollo de software actual (tanto en proyectos en Java como NOEST o en Python como Jules) se recomienda ampliamente evitar el anidamiento excesivo de condicionales (*código flecha*) mediante retornos tempranos (*guard clauses*). ¿Cómo sugiere usted conciliar este patrón de diseño con la enseñanza tradicional de diagramas de flujo estructurados que habitualmente requieren un único nodo de salida?  
• En entornos de producción con Java, ¿en qué condiciones el compilador `javac` optimiza una sentencia `switch` mediante la instrucción de bytecode `tableswitch` (para valores contiguos) frente a `lookupswitch` (para valores dispersos), y cuál es su impacto real en el rendimiento de la CPU?

---

### 9. Bibliografía:
• Joyanes Aguilar, L. (2020). *Fundamentos de programación: algoritmos, estructura de datos y objetos* (5.ª ed.). McGraw-Hill.  
• Ramírez, F. (2007). *Introducción a la programación: Algoritmos y su implementación en VB.NET, C#, Java y C++*. Alfaomega Grupo Editor.  
• Trejos Buriticá, O. I. (2021). *Lógica de programación: solucionario en pseudocódigo*. Ediciones de la U.  
• Universidad de Cartagena - CTEV. (2026). *Módulo Didáctico Unidad 2: Estructuras de Control — Algoritmos y Programación Básica*. Facultad de Ingeniería, Universidad de Cartagena.  
• Valls Ferrán, J. M., & Camacho Fernández, D. (2003). *Programación, algoritmos y ejercicios resueltos en JAVA*. Pearson Educación.  
• Wanumen Silva, L. F., et al. (2017). *Java básico*. Ecoe Ediciones.
