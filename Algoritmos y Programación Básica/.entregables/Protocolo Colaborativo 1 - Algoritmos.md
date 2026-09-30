# Protocolo Colaborativo — Unidad 1: Fundamentos de Programación y Diseño Algorítmico

**Programa:** Ingeniería de Software  
**Semestre:** 1  
**Asignatura:** Algoritmos y Programación Básica  
**Docente:** Heybertt Moreno Díaz  
**Universidad de Cartagena — CTEV**  
**Fecha de Entrega:** Jueves, 10 de Septiembre de 2026 (Campus Virtual SIMA)  

---

### Registro de los participantes
- Santiago Orozco Vergara
- Cristian Andrés Flórez Arboleda
- Esteban David Marrugo Jassir
- Juan Guillermo Villa Beleño
- Gabriel Antonio Molina Meza

---

### 1. Descripción del texto o actividad a realizar
Nos reunimos en equipo para confrontar y unificar los conceptos de la Unidad 1 sobre fundamentos de programación y lógica algorítmica. Analizamos el ciclo que recorre una solución desde el planteamiento abstracto del problema hasta su ejecución real: diseño en pseudocódigo y diagramas de flujo normalizados, tipado estricto en memoria y la arquitectura de compilación de Java mediante `javac` y la JVM. Contrastamos los protocolos individuales de cada integrante, resolvimos discrepancias sobre el uso de memoria y armamos acuerdos metodológicos para no sentarnos a tirar código sin una prueba de escritorio previa.

---

### 2. Palabras clave
Compilador `javac`, Máquina Virtual JVM, *Bytecode* binario, Memoria *Stack*, Tipos primitivos, Operadores de cortocircuito, Precedencia de operadores, Prueba de escritorio, Diagrama de flujo ANSI/ISO, Asignación vs Igualdad.

---

### 3. Objetivos de las lecturas o actividad a realizar
- Analizar en conjunto las etapas del ciclo algorítmico para separar el análisis lógico de la sintaxis del lenguaje.
- Comprender el flujo técnico de ejecución en Java: cómo el código fuente `.java` se compila a *bytecode* `.class` y cómo la JVM lo interpreta en cualquier arquitectura.
- Dominar el comportamiento de las variables en memoria y el orden de evaluación de operadores aritmético-lógicos.
- Establecer un flujo de trabajo riguroso dentro del CIPAS para validar algoritmos con pruebas de escritorio antes de abrir el editor.

---

### 4. Conceptos clave y definiciones
- **Algoritmo:** Secuencia ordenada, finita e inequívoca de pasos lógicos diseñada para procesar datos de entrada y producir una salida determinista.
- **Compilador `javac` y JVM:** `javac` traduce el archivo `.java` a un conjunto de instrucciones intermedias llamadas *bytecode* (`.class`). La Máquina Virtual de Java (JVM) lee ese *bytecode* y lo ejecuta traduciéndolo a instrucciones de máquina sobre el sistema operativo anfitrión.
- **Memoria *Stack* en tipos primitivos:** Zona de memoria volátil y secuencial donde residen los datos escalares directos (`int`, `double`, `boolean`, `char`). No manejan punteros ni referencias complejas; guardan el valor exacto en su propio espacio asignado.
- **Operadores de cortocircuito (`&&`, `||`):** Mecanismos lógicos donde la JVM evalúa únicamente hasta donde sea estrictamente necesario. En un `&&`, si el primer término es falso, no pierde ciclos evaluando el segundo término.
- **Asignación (`=`) frente a igualdad relacional (`==`):** La asignación traslada un valor de la derecha al contenedor de la izquierda; la igualdad compara si dos operandos tienen el mismo valor lógico o aritmético.
- **Prueba de escritorio:** Simulación manual y paso a paso del estado de las variables sobre papel. Permite verificar la lógica del algoritmo sin depender del compilador ni de herramientas de depuración.

---

### 5. Resumen de las discusiones grupales
En la mesa de trabajo pusimos en común los apuntes y códigos de prueba de cada uno. Hubo acuerdo total en que la mayor trampa al comenzar la carrera es abrir el IDE de inmediato. Cuando uno se salta la etapa de lápiz y papel, termina corrigiendo a los golpes y confunde errores de sintaxis con problemas de lógica estructural.

Revisamos a fondo el comportamiento de la JVM. Nos llamó la atención el concepto de *Write Once, Run Anywhere*. Entendimos que Java logra esa portabilidad gracias a que `javac` no le habla directamente al procesador Intel o ARM, sino a una capa abstracta estandarizada. 

Al repasar los tipos de datos y operadores, vimos situaciones donde un mal planteamiento de precedencia o un desbordamiento de enteros altera por completo el resultado esperado. Discutimos ejemplos prácticos de cómo los operadores de cortocircuito ahorran tiempo de procesamiento y evitan errores si se estructuran con criterio dentro de las condiciones.

---

### 6. Encuentros conceptuales
- Coincidimos en que el pseudocódigo y los diagramas de flujo ANSI/ISO no son tareas burocráticas: son el plano arquitectónico indispensable de cualquier programa antes de implementar.
- Confirmamos que la prueba de escritorio ahorra horas de depuración. Seguir a mano el rastreo de variables en una tabla permite detectar ciclos infinitos o valores fuera de rango antes de tocar la terminal.
- Todos validamos la importancia de internalizar la tabla de precedencia de operadores para no llenar el código de paréntesis innecesarios, manteniendo a la vez la claridad del algoritmo.

---

### 7. Desencuentros conceptuales
- Tuvimos un debate fuerte sobre cuándo vale la pena usar tipos primitivos de menor tamaño como `byte` o `short` frente al estándar `int`. Unos sostenían que en hardware moderno de 64 bits optimizar memoria a ese nivel es innecesario y complica el código por conversiones forzadas (*casting*). Otros argumentaban que en procesamiento masivo de datos o desarrollo embebido la economía de memoria sigue siendo prioritaria. Llegamos al consenso de que para el alcance de este curso `int` es el estándar sensato, pero conociendo siempre el límite de cada tipo.
- Discutimos la diferencia entre un error en tiempo de compilación y uno en tiempo de ejecución. Al principio algunos compañeros consideraban que si el compilador no arrojaba alertas, el programa ya estaba bien resuelto. Aclaramos que `javac` solo vigila la sintaxis y las reglas del lenguaje; un error de lógica corre limpio, pero entrega un resultado desastroso.

---

### 8. Metodología de trabajo (Cómo se realizó la actividad colaborativa)
Organizamos una sesión de trabajo sincrónica por Discord con pantalla compartida. Cada integrante abrió su protocolo individual y sus apuntes de Obsidian. Tomamos como base los ejercicios prácticos de la guía de la Unidad 1 y contrastamos las respuestas. 

A medida que surgieron diferencias conceptuales, abrimos terminales en Linux y Windows para compilar fragmentos mínimos con `javac` y comprobar directamente en la JVM el comportamiento de los tipos y operadores. Luego redactamos las secciones de este protocolo de forma consensuada, asegurándonos de que reflejara la voz y el análisis de todo el equipo.

---

### 9. Conclusiones
- El pensamiento algorítmico precede a la herramienta: quien sabe diseñar lógica estructurada puede implementarla en Java, C o cualquier otro lenguaje formal.
- Comprender el binomio `javac` + JVM es indispensable para entender qué hace realmente la máquina cuando ejecutamos un archivo `.class`.
- La disciplina de trabajo en equipo dentro de un CIPAS de software requiere unificar criterios técnicos claros y hablar el mismo vocabulario desde el primer semestre.

---

### 10. Discusiones y recomendaciones
Consideramos muy acertado el enfoque de arrancar con Java por el rigor que impone su tipado estricto. Sin embargo, recomendamos que en las tutorías presenciales de los sábados en Piedra de Bolívar se dedique más tiempo a resolver pruebas de escritorio complejas en el tablero con variables acumuladoras y banderas booleanas, antes de pasar a las guías de código en laboratorio.

A nivel interno del CIPAS, acordamos institucionalizar el uso de pruebas de escritorio cruzadas: que un compañero revise la lógica del otro antes de dar por cerrada cualquier entrega práctica.

---

### 11. Bibliografía
- **Joyanes Aguilar, L.** (2020). *Fundamentos de programación: algoritmos, estructura de datos y objetos* (5.ª ed.). McGraw-Hill.
- **Wanumen Silva, L. F., et al.** (2017). *Java básico*. Ecoe Ediciones.
- **Dobrushkin, V. A.** (2012). *Métodos para análise de algoritmos*. Rio de Janeiro: LTC.
- **Universidad de Cartagena - CTEV.** (2026). *Módulo de Estudio Unidad 1: Fundamentos de Programación y Algoritmos*. Facultad de Ingeniería, Universidad de Cartagena.
