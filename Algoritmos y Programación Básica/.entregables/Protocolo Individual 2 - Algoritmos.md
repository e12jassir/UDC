# Protocolo Individual — Unidad 2: Estructuras de Control

**Asignatura:** Algoritmos y Programación Básica — `IX24013-B1`  
**Estudiante:** Esteban David Marrugo Jassir (Cód. 7502620036)  
**Docente:** Heybertt Moreno Díaz  
**Fecha de Entrega:** Lunes, 12 de Octubre de 2026 (Campus Virtual SIMA)  
**Modalidad:** Individual  

---

### 1. Descripción del texto o actividad a realizar:
Revisé a fondo el módulo de la Unidad 2 sobre estructuras de control (`Estructuras de control.pdf`) y me puse a contrastarlo con lo que vivo todos los días tirando código: por un lado en el SENA ADSO con el proyecto NOEST, donde armamos una aplicación de escritorio en Java, y por el otro con Jules, mi proyecto personal en Python enfocado en automatización. Me interesaba ver cómo la teoría clásica sobre secuencias, condicionales (`if/else/switch`) y ciclos (`for/while/do-while`) se aterriza en dos lenguajes con filosofías tan distintas, y cómo entender esto a bajo nivel te evita dolores de cabeza con errores en tiempo de ejecución.

---

### 2. Palabras claves:
Estructuras de control, flujo de ejecución, selección condicional, evaluación booleana, cortocircuito lógico, ciclos iterativos, scope de variables, proyecto NOEST, proyecto Jules.

---

### 3. Objetivos de las lecturas o actividad a realizar:
• Entender cómo las estructuras de control dirigen el flujo de un programa y por qué son la base para que un algoritmo tome decisiones reales (Joyanes Aguilar, 2020).  
• Contrastar la rigidez del tipado estático de Java en NOEST (Wanumen Silva et al., 2017) frente a la flexibilidad dinámica de Python en Jules.  
• Analizar el cortocircuito lógico (`&&`, `||`) como un escudo indispensable para proteger el código contra excepciones de puntero nulo.  
• Ver en la práctica cómo cambia el alcance de las variables (*scope*) entre las llaves de Java y los bloques de Python (Trejos Buriticá, 2021).  
• Saber con claridad cuándo meter un `for`, un `while` o un `do-while` según la naturaleza de la tarea y no por simple costumbre.

---

### 4. Conceptos claves y definiciones:
• **Estructuras de control:** Instrucciones que rompen la lectura lineal de la computadora para decidir qué bloque se ejecuta y cuándo, según las condiciones que le pasemos (Ramírez, 2007; Trejos Buriticá, 2021).  
• **Secuencia:** El flujo por defecto donde el procesador ejecuta una instrucción detrás de otra, en el mismo orden en que las dejamos escritas.  
• **Selección condicional (`if`, `else if`, `else`):** Caminos alternativos en el código. Evalúan una condición lógica y saltan a un bloque si es verdadera o a otro si es falsa (Valls Ferrán y Camacho Fernández, 2003).  
• **Selección múltiple (`switch-case`):** Estructura para comparar una variable contra varios valores puntuales. En Java necesita el `break` en cada caso para que no se siga de largo ejecutando lo que viene abajo (Wanumen Silva et al., 2017).  
• **Ciclos o bucles (`for`, `while`, `do-while`):** Bloques que repiten una tarea mientras se cumpla una condición. Obligan a tener una condición de salida clara para no dejar la máquina pegada en un bucle infinito (Joyanes Aguilar, 2020).  
• **Pre-test (`while`, `for`) vs. Post-test (`do-while`):** En el pre-test revisas la condición antes de entrar (puede que no entre nunca); en el post-test ejecutas al menos una vez antes de preguntar.  
• **Alcance de variable (*Scope*):** La zona del programa donde una variable existe y se puede usar. Si la declaras dentro de un bloque, debe morir ahí para no ensuciar el resto del programa ni chocar con otros datos.

---

### 5. Resumen de la(as) lecturas:
Cuando abrí la guía de estructuras de control (CTEV, 2026), los conceptos no me tomaron por sorpresa. En el SENA vengo trabajando en el proyecto formativo NOEST, donde desarrollamos una aplicación de escritorio en Java, y por mi cuenta llevo meses metido en Jules, mi proyecto en Python para automatizar tareas e interactuar con modelos de IA. Lo interesante de leer este módulo no fue aprenderme la sintaxis de memoria, sino comparar cómo reacciona cada lenguaje cuando pones a prueba la lógica (Joyanes Aguilar, 2020).

La diferencia más brava la viví con los condicionales. En Python todo es muy flexible: el lenguaje evalúa la "veracidad" (*truthiness*) de las cosas de forma automática. En Jules, por ejemplo, si meto un `if respuesta:`, y la variable me llega como una lista vacía `[]`, un diccionario `{}` o un simple `0`, Python asume enseguida que eso es falso. Al principio parece una maravilla porque ahorra líneas, pero en proyectos reales te puede ocultar errores gravísimos si una lista vacía era una respuesta válida de la API. En Java la historia es a otro precio: en NOEST el compilador no te deja pasar una sola (Wanumen Silva et al., 2017). Si pones `if (respuesta)`, el compilador te frena de una porque exige un tipo `boolean` explícito. Toca escribir `if (respuesta != null && !respuesta.isEmpty())`. Y ahí es donde entra la magia del cortocircuito lógico (`&&`): si `respuesta` es nula, Java ni siquiera intenta revisar el segundo pedazo, salvándote de un clásico `NullPointerException` que te congelaría la interfaz de la aplicación.

Con el `switch` me pasó algo parecido. En NOEST, cuando tengo que manejar opciones fijas de un menú o estados del sistema, meter cinco o seis `else if` seguidos vuelve el código una sábana ilegible. El `switch-case` deja todo mucho más limpio al evaluar valores concretos (Ramírez, 2007; Valls Ferrán y Camacho Fernández, 2003). Pero tiene su trampa: si te tragas un `break`, el flujo se rueda y ejecuta los casos siguientes (*fall-through*). Es de esos errores donde el programa compila perfecto, pero hace cualquier locura en pantalla.

El otro tema que me llamó mucho la atención fue el alcance de las variables (*scope*). En Java, cuando armas un ciclo `for (int i = 0; i < total; i++)`, esa variable `i` nace y muere dentro de las llaves del bucle. Si intentas llamarla afuera, el compilador te dice que no existe. En Python no es así: si haces `for item in coleccion:`, la variable `item` se queda viva en la función incluso después de que el ciclo termina. Si más abajo usas una variable con el mismo nombre creyendo que estaba limpia, te puedes ganar un comportamiento raro muy difícil de rastrear. Entender esto te enseña a cuidar el estado de tus datos y evitar colisiones tontas entre variables (Trejos Buriticá, 2021).

Por último, con los ciclos la guía te da una regla de oro para no dudar al programar. Si ya sabes cuántas veces vas a repetir algo (como recorrer una lista fija de usuarios en NOEST), usas un `for`. Si dependes de algo externo que no controlas (esperar que el usuario presione un botón, que un socket responda o que llegue un paquete en Jules), te vas con un `while`. Y el `do-while` queda perfecto para esos menús donde necesitas mostrar las opciones al menos una primera vez antes de pedir el dato. El peligro de siempre, como recalcan Ramírez (2007) y Joyanes Aguilar (2020), es olvidarse de actualizar la variable de control dentro del cuerpo del ciclo. Dejar un ciclo infinito en el hilo principal te tumba la aplicación de escritorio al instante.

---

### 6. Metodología de trabajo:
Descargué el archivo `Estructuras de control.pdf` desde SIMA (CTEV, 2026), lo leí con calma y fui sacando mis apuntes limpios en Obsidian. Luego subí el material a NotebookLM para escuchar el resumen en audio y hacerme preguntas rápidas, que es el método que mejor me sirve para repasar sin quemarme la vista. Con la teoría clara, me fui a la terminal en Linux: abrí mis carpetas de NOEST y Jules y me puse a probar casos borde con `javac` y `python`, testeando cómo se comportaban las condiciones vacías, los bucles anidados y el cortocircuito para ver en vivo la diferencia de rigor entre ambos mundos.

---

### 7. Conclusiones de la lectura o actividad:
• Las estructuras de control son las que le dan vida al código: sin ellas, un programa no es más que una lista estática de instrucciones que no sabe reaccionar a nada (Joyanes Aguilar, 2020; Trejos Buriticá, 2021).  
• Trabajar en paralelo con Java (NOEST) y Python (Jules) me demostró que la teoría es la misma en todos lados, pero el compilador de Java te educa a ser mucho más disciplinado y defensivo desde el día uno (Wanumen Silva et al., 2017).  
• El cortocircuito (`&&`, `||`) no es una simple optimización de velocidad: es una regla de seguridad básica para no reventar la ejecución al consultar métodos en variables que puedan llegar nulas.  
• El scope de las variables importa y mucho: saber qué datos mueren dentro de un bloque `{}` en Java y cuáles sobreviven en Python evita sobreescrituras accidentales y te ahorra horas de depuración.  
• Escoger entre `for`, `while` o `do-while` es una decisión de arquitectura sencilla: depende de si conoces el límite de antemano o si estás esperando un evento del usuario o del sistema.

---

### 8. Discusiones y recomendaciones:
• Para el profe Heybertt: En proyectos reales de software (tanto en Java como en Python) uno trata de no amontonar condicionales hacia la derecha (*código flecha*) y prefiere usar retornos tempranos (*guard clauses*). ¿Cómo recomienda usted manejar eso en clase frente a los diagramas de flujo tradicionales, que casi siempre piden tener un único punto de salida al final?  
• En Java empresarial, ¿en qué situaciones el compilador genera un `tableswitch` frente a un `lookupswitch` al procesar un `switch`, y qué tanto influye eso en el rendimiento del procesador cuando manejamos miles de peticiones?

---

### 9. Bibliografía:
• Joyanes Aguilar, L. (2020). *Fundamentos de programación: algoritmos, estructura de datos y objetos* (5.ª ed.). McGraw-Hill.  
• Ramírez, F. (2007). *Introducción a la programación: Algoritmos y su implementación en VB.NET, C#, Java y C++*. Alfaomega Grupo Editor.  
• Trejos Buriticá, O. I. (2021). *Lógica de programación: solucionario en pseudocódigo*. Ediciones de la U.  
• Universidad de Cartagena - CTEV. (2026). *Módulo Didáctico Unidad 2: Estructuras de Control — Algoritmos y Programación Básica*. Facultad de Ingeniería, Universidad de Cartagena.  
• Valls Ferrán, J. M., & Camacho Fernández, D. (2003). *Programación, algoritmos y ejercicios resueltos en JAVA*. Pearson Educación.  
• Wanumen Silva, L. F., et al. (2017). *Java básico*. Ecoe Ediciones.
