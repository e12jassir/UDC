# Protocolo Individual — Unidad 1: Fundamentos de Programación y Algoritmos

**Asignatura:** Algoritmos y Programación Básica  
**Estudiante:** Esteban David Marrugo Jassir  
**Docente:** Heybertt Moreno Díaz  
**Fecha de Entrega:** 10 de Septiembre de 2026 (Campus Virtual SIMA)  
**Modalidad:** Individual  

---

### 1. Descripción de la Actividad
Revisión analítica de los fundamentos conceptuales de la programación estructurada y el diseño algorítmico. Analicé los principios de descomposición modular, tipos de datos primitivos, operadores aritmético-lógicos, ciclo de vida del desarrollo de software y la configuración del entorno de ejecución en Java (JDK/JVM) para la construcción de algoritmos secuenciales.

---

### 2. Palabras Clave
Pseudocódigo, Diagrama de Flujo ANSI/ISO, Bytecode, Precedencia de Operadores, Stack Memory, Compilador `javac`, Máquina Virtual JVM, Tipos Primitivos, Operadores de Cortocircuito, Asignación vs Igualdad.

---

### 3. Objetivos de Aprendizaje
- Dominar la descomposición de problemas en instrucciones secuenciales finitas y deterministas.
- Comprender con claridad el rol de `javac` y la JVM en el ciclo de ejecución de un programa en Java.
- Manejar con precisión la memoria de tipos primitivos y la jerarquía de operadores booleanos y aritméticos.

---

### 4. Conceptos Clave y Definiciones

| Concepto | Definición Técnica |
| :--- | :--- |
| **Pseudocódigo** | Representación narrativa estructurada en lenguaje natural de un algoritmo, independiente de la sintaxis rígida de un lenguaje formal. |
| **Diagrama de Flujo** | Modelado gráfico estandarizado (ANSI/ISO) que representa la secuencia, toma de decisiones y flujo de datos de un programa. |
| **Bytecode (`.class`)** | Código intermedio generado por el compilador `javac` que no depende de la arquitectura física del procesador. |
| **JVM (Java Virtual Machine)** | Entorno de ejecución que interpreta el *bytecode* y lo transforma en instrucciones nativas de la máquina huésped. |
| **Stack Memory (Tipos Primitivos)** | Espacio de memoria de acceso rápido donde residen directamente los valores escalares (`int`, `double`, `boolean`, `char`). |
| **Operadores de Cortocircuito** | Operadores lógicos (`&&`, `||`) que detienen la evaluación en cuanto el resultado de la expresión queda determinado por el primer operando. |

---

### 5. Resumen Analítico de las Lecturas

Al revisar los módulos y lecturas de esta unidad, lo primero que me quedó claro es que programar no arranca escribiendo código en el editor. El trabajo real está en el análisis previo. Si uno no divide el problema en entradas, procesos y salidas desde el papel o en pseudocódigo, termina arrastrando errores de lógica difíciles de depurar más adelante.

En Java, este proceso cobra mucho sentido cuando uno entiende cómo funciona su entorno. Escribimos el archivo fuente con extensión `.java`, el compilador `javac` lo traduce a *bytecode* en un archivo `.class`, y finalmente la máquina virtual (JVM) se encarga de ejecutarlo en el sistema operativo. Esta separación es lo que permite que el código corra en cualquier máquina sin tener que reescribirlo.

Otro punto donde puse bastante atención fue en el manejo de variables y operadores. Confundir el operador de asignación (`=`) con el de comparación relacional (`==`) es un clásico error al empezar. Además, entender la memoria de pila (*stack*) para los tipos primitivos y cómo los operadores lógicos evalúan en cortocircuito te da una base sólida para escribir código limpio y sin comportamientos inesperados.

---

### 6. Metodología de Estudio Aplicada
Para este tema revisé el módulo guía de la unidad y tomé notas en Obsidian. Antes de escribir cualquier clase en el entorno de desarrollo, hice pruebas de escritorio a mano en papel para seguir el flujo secuencial de los datos paso a paso. Luego comprobé la compilación y ejecución directa desde la terminal usando `javac` y `java`.

---

### 7. Conclusiones
- Entender la lógica algorítmica y los tipos de datos en memoria es prioritario antes de preocuparse por la sintaxis de cualquier lenguaje.
- La prueba de escritorio en papel sigue siendo la mejor herramienta para encontrar fallas lógicas antes de compilar.
- Java impone una disciplina de tipado estricto que ayuda a estructurar el pensamiento computacional desde el primer día.

---

### 8. Discusiones y Preguntas para la Tutoría
- ¿En qué casos de alta concurrencia o bajo nivel se justifica usar tipos de menor consumo en memoria (`byte`, `short`) en lugar de `int` en procesadores modernos de 64 bits?
- Al diseñar diagramas de flujo para algoritmos con muchas validaciones consecutivas, ¿qué criterio recomiendan para no saturar visualmente el esquema?

---

### 9. Bibliografía
- **Joyanes Aguilar, L.** (2020). *Fundamentos de programación: algoritmos, estructura de datos y objetos* (5.ª ed.). McGraw-Hill.
- **Wanumen Silva, L. F., et al.** (2017). *Java básico*. Ecoe Ediciones.
- **Dobrushkin, V. A.** (2012). *Métodos para análise de algoritmos*. Rio de Janeiro: LTC.
