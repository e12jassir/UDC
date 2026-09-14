# Actividad de la Unidad 2: Los Momentos Metodológicos del Aprendizaje en la Educación Abierta y a Distancia

**Universidad de Cartagena — Centro de Tecnologías para la Educación Virtual (CTEV)**  
**Programa:** Ingeniería de Software  
**Semestre:** 1  
**Asignatura:** Metodologías y Estrategias de la Educación a Distancia (MEAD)  
**Docente:** Raquel Leottau Díaz  
**Equipo CIPAS:** Grupo 8  

### Integrantes:
• Esteban David Marrugo Jassir (Cód. 7502620036)  
• Cristian Andrés Flórez Arboleda  

---

# 1. Momentos Metodológicos del Aprendizaje

## 1.1. Mapa Conceptual Jerárquico

El siguiente mapa conceptual modela la articulación dialéctica y secuencial de los Tres Momentos Metodológicos del Aprendizaje en la Educación Abierta y a Distancia (EAD), basado en las tesis pedagógicas de Amaury Lora Sfer (2014):

```mermaid
flowchart TD
    A["EDUCACIÓN ABIERTA Y A DISTANCIA (EAD)<br><i>Universidad de Cartagena</i>"] -->|se estructura pedagógicamente en| B["TRES MOMENTOS METODOLÓGICOS DEL APRENDIZAJE"]

    %% Momento 1
    B -->|Momento 1: Génesis del proceso| C["ESTUDIO INDIVIDUAL Y AUTÓNOMO"]
    C -->|implica| C1["Lectura analítica del módulo institucional"]
    C -->|requiere| C2["Autorregulación y gestión del tiempo (Créditos Académicos)"]
    C -->|produce| C3["Protocolo Individual y apuntes reflexivos (Obsidian)"]

    %% Conector 1 a 2
    C3 -->|alimenta y da insumos obligatorios a| D["TRABAJO COLABORATIVO EN CIPAS"]

    %% Momento 2
    B -->|Momento 2: Interacción entre pares| D
    D -->|se fundamenta en la| D1["Co-validación dialógica (Amaury Lora Sfer)"]
    D -->|supera y elimina| D2["La fragmentación viciada de tareas"]
    D -->|utiliza herramientas de red| D3["Salas de voz en Discord y Google Docs Institucional"]
    D -->|consolida| D4["Protocolo Colaborativo y dudas complejas"]

    %% Conector 2 a 3
    D4 -->|prepara la agenda temática para| E["TUTORÍA PRESENCIAL (Sábados B)"]

    %% Momento 3
    B -->|Momento 3: Cierre y síntesis formal| E
    E -->|redefine el rol docente como| E1["Tutor mediador y co-validador académico"]
    E -->|elimina| E2["La clase magistral pasiva tradicional"]
    E -->|desarrolla| E3["Debate de dudas de fondo y socialización plenaria"]
    E -->|culmina en la| E4["Síntesis tutorial y evaluación del aprendizaje"]

    %% Cierre cíclico
    E4 -.->|retroalimenta continuamente el proceso de| F["APRENDER A APRENDER"]
    F -.->|fortalece la autonomía en el| C

    classDef main fill:#1e3a8a,stroke:#3b82f6,stroke-width:2px,color:#ffffff;
    classDef mom fill:#0f766e,stroke:#14b8a6,stroke-width:2px,color:#ffffff;
    classDef node fill:#f8fafc,stroke:#94a3b8,stroke-width:1px,color:#0f172a;
    class A,B main;
    class C,D,E mom;
    class C1,C2,C3,D1,D2,D3,D4,E1,E2,E3,E4,F node;
```

### Descripción de las Relaciones Proposicionales:
1. **La EAD se estructura en Tres Momentos:** No son eventos desconectados, sino un ciclo dialéctico donde cada etapa depende estrictamente de la anterior.
2. **Del Momento 1 al Momento 2:** El estudio individual aporta la base teórica y las notas reflexivas sin las cuales el debate en CIPAS pierde todo sentido y se convierte en una charla improvisada.
3. **Del Momento 2 al Momento 3:** La co-validación en CIPAS resuelve las dudas de nivel medio y destila las preguntas de fondo para que la tutoría del sábado con el docente sea un espacio ágil de validación y no un dictado de conceptos elementales.
4. **Retroalimentación continua:** La síntesis tutorial consolida el criterio metacognitivo del estudiante, cerrando el ciclo de "aprender a aprender".

---

## 1.2. Propuesta de Estrategia de Aprendizaje

### 1. Nombre de la Estrategia
**Estrategia 3C: Captura, Co-Validación y Consolidación (Ciclo Ágil de Aprendizaje Autónomo en EAD).**

### 2. Objetivo
Estructurar un método sistemático y medible para que los integrantes del CIPAS gestionen el estudio autónomo, contrasten sus comprensiones mediante debate sincrónico entre pares y co-validen sus conocimientos con el tutor, fortaleciendo la autorregulación y la retención conceptual a largo plazo en Ingeniería de Software.

### 3. Justificación
En la modalidad a distancia, el mayor peligro radica en confundir la flexibilidad horaria con desorganización, y el trabajo en equipo con la fragmentación mecánica de entregables ("yo hago la mitad y tú la otra"). Esta estrategia se justifica porque introduce una rutina ágil inspirada en metodologías de desarrollo de software: obliga a que cada estudiante estudie de manera previa, confronta los modelos mentales en equipo para eliminar sesgos y asegura que el tiempo presencial con el docente se aproveche al máximo en la resolución de problemas complejos.

### 4. Descripción de la Estrategia
La *Estrategia 3C* es un circuito semanal continuo dividido en tres fases interdependientes:
- **Captura:** El estudiante procesa individualmente el módulo de estudio y genera notas analíticas en su gestor personal.
- **Co-validación:** El CIPAS se reúne en red mediante plataformas colaborativas para contrastar apuntes, resolver discrepancias y redactar acuerdos en un documento compartido.
- **Consolidación:** El equipo presenta sus conclusiones y dudas críticas en la tutoría presencial de los sábados, integrando la retroalimentación del docente a su sistema de estudio.

### 5. Pasos o Fases para su Aplicación

```
   ┌────────────────────────────────────────────────────────────────────────┐
   │ FASE 1: CAPTURA AUTÓNOMA (Lunes a Miércoles)                          │
   │ • Lectura activa del módulo de la unidad en SIMA.                     │
   │ • Procesamiento con Técnica Feynman (explicar con palabras propias).   │
   │ • Registro en Obsidian de conceptos y dudas para el protocolo indiv.  │
   └───────────────────────────────────┬────────────────────────────────────┘
                                       │ (Insumo individual obligatorio)
                                       ▼
   ┌────────────────────────────────────────────────────────────────────────┐
   │ FASE 2: CO-VALIDACIÓN EN CIPAS (Jueves a Viernes)                     │
   │ • Sesión sincrónica de 60-90 min por Discord.                         │
   │ • Rueda de contrastación: comparar notas y debatir diferencias.       │
   │ • Redacción en vivo del Protocolo Colaborativo en Google Docs oficial. │
   │ • Filtro de "Dudas Semilla" que requieren mediación del tutor.         │
   └───────────────────────────────────┬────────────────────────────────────┘
                                       │ (Agenda temática depurada)
                                       ▼
   ┌────────────────────────────────────────────────────────────────────────┐
   │ FASE 3: CONSOLIDACIÓN TUTORIAL (Sábado presencial)                    │
   │ • Participación activa en la sesión plenaria con el docente tutor.     │
   │ • Planteamiento de las dudas complejas filtradas por el CIPAS.        │
   │ • Registro de la síntesis tutorial y cierre de la unidad.             │
   └────────────────────────────────────────────────────────────────────────┘
```

### 6. Papel de los Integrantes del CIPAS
Para garantizar que todos participen y nadie se recueste sobre el trabajo ajeno, los roles rotan en cada unidad:
- **Moderador de Sesión:** Abre la llamada en Discord, controla los tiempos de intervención (máximo 5 minutos por concepto) y asegura que se discuta la totalidad de la guía.
- **Relator de Síntesis (Compilador):** Registra en tiempo real los acuerdos y desacuerdos en el Google Docs institucional mientras el equipo debate de viva voz.
- **Revisor Técnico:** Comprueba la ortografía, la coherencia de la redacción, las citas bibliográficas en normas APA y la concordancia con la rúbrica de SIMA antes de enviar.
- **Compromiso innegociable:** Nadie puede entrar a la Fase 2 sin haber completado y mostrado su protocolo individual de la Fase 1.

### 7. Recursos y Herramientas Digitales
- **Obsidian / Logseq:** Entorno local en Markdown para la toma de notas atómicas y estructuración del protocolo individual.
- **Discord (Canales de Voz y Pantalla Compartida):** Espacio sincrónico para la reunión del CIPAS, donde se discuten los temas sin la frialdad de los mensajes de texto.
- **Google Docs (Cuentas `@unicartagena.edu.co`):** Espacio compartido de co-edición en tiempo real donde queda el registro transparente de las aportaciones de cada miembro.
- **Google Calendar / Time-blocking:** Bloques de 2 horas programados en la semana para cumplir con la equivalencia de horas por crédito académico (2 a 3 horas autónomas por crédito).

### 8. Forma de Seguimiento y Evaluación
El CIPAS evalúa el funcionamiento de la estrategia mediante dos instrumentos concretos:
1. **Pase de Entrada al CIPAS (Filtro individual):** Al iniciar la llamada de Discord, cada integrante comparte pantalla 30 segundos mostrando su lectura realizada y sus notas. Quien no haya leído, pasa a calidad de oyente y no firma el protocolo de la semana.
2. **Lista de Chequeo de Co-validación:** Antes de cerrar el documento colaborativo, el equipo verifica:
   - ¿Discutimos todos los puntos de la guía? (Sí/No)
   - ¿Quedó registrada al menos una discrepancia o duda real del grupo? (Sí/No)
   - ¿Tenemos listas 1 o 2 preguntas de alto nivel para hacerle al profesor el sábado? (Sí/No)

### 9. Resultados Esperados
- Eliminación total de la entrega de tareas copiadas o fragmentadas a última hora.
- Reducción del estrés en semanas de parciales, al tener notas procesadas semanalmente.
- Dominio conceptual profundo evidenciado en calificaciones superiores a 4.5 en SIMA.
- Formación de disciplina y hábitos de comunicación asertiva indispensables para el trabajo en equipo en la industria del software.

### 10. Relación con el Proceso de "Aprender a Aprender" en la EAD
"Aprender a aprender" significa dejar de ser un receptor pasivo de información y convertirse en el arquitecto del propio conocimiento. La *Estrategia 3C* materializa este principio porque:
- Desarrolla la **metacognición**: el estudiante detecta activamente qué no entiende durante la Fase 1 antes de que un examen se lo demuestre con una mala nota.
- Fomenta la **co-construcción social**: al explicarle un concepto al compañero de CIPAS en la Fase 2, se produce el fenómeno pedagógico más potente: "quien enseña, aprende dos veces".
- Transforma la **interacción docente**: el alumno llega a la tutoría con preguntas precisas, transformando la educación a distancia en un diálogo formativo de alto nivel.

---

# 2. Sustentación de la Estrategia (Guion de Diapositivas)

Estructura diseñada para presentación en Canva, Google Slides o PowerPoint:

### Diapositiva 1: Portada
- **Título:** Estrategia 3C: Captura, Co-Validación y Consolidación
- **Subtítulo:** Modelo Ágil de Aprendizaje Autónomo en la Educación a Distancia
- **Asignatura:** Metodología de la Educación a Distancia
- **CIPAS:** Grupo 8 — Esteban David Marrugo Jassir & Cristian Andrés Flórez Arboleda
- **Institución:** Universidad de Cartagena — Facultad de Ingeniería

### Diapositiva 2: El Problema en la EAD y la Justificación
- **El desafío:** El riesgo del aislamiento, la procrastinación y la mala práctica de dividirse los talleres como retazos.
- **Nuestra propuesta:** Pasar del trabajo fragmentado al ciclo dialéctico propuesto por Amaury Lora Sfer.
- **La solución 3C:** Un método de tres fases continuas que sincroniza el trabajo individual, el debate grupal y la tutoría presencial.

### Diapositiva 3: Los Tres Momentos y el Mapa Conceptual
- **Visual:** Diagrama simplificado del Mapa Conceptual.
- **Momento 1 (Individual):** Estudio autónomo y lectura profunda (insumo de entrada).
- **Momento 2 (CIPAS):** Co-validación dialógica en red (construcción social).
- **Momento 3 (Tutoría):** Validación experta y resolución de dudas complejas con el docente.

### Diapositiva 4: Fases Operativas y Herramientas Digitales
- **Fase 1 - Captura (Lun-Mié):** Módulos SIMA + Notas en Obsidian.
- **Fase 2 - Co-validación (Jue-Vie):** Reunión sincrónica en Discord + Redacción compartida en Google Docs.
- **Fase 3 - Consolidación (Sábados):** Participación activa y resolución de dudas con el tutor en el CTEV.
- **Roles rotativos:** Moderador, Relator y Revisor Técnico.

### Diapositiva 5: Seguimiento, Evaluación y Resultados
- **Filtros de control:** "Pase de entrada" al CIPAS (revisión de lectura previa) y lista de chequeo de co-validación.
- **Resultados medibles:** Cero tareas improvisadas, comprensión profunda antes de los exámenes y calificaciones excelentes.

### Diapositiva 6: Conclusión: ¿Cómo fortalece el "Aprender a Aprender"?
- **Autonomía:** Responsabilidad sobre el propio horario según el sistema de créditos.
- **Metacognición:** Capacidad de identificar vacíos conceptuales a tiempo.
- **Frase de cierre:** *"En la educación a distancia, quien no estudia no aprende; pero quien aprende a co-validar en equipo, lidera su formación universitaria."*

---

# 3. Guion Oficial del Video de Sustentación

**Modalidad:** Grabación en pareja (ambos integrantes aparecen en pantalla y hablan 50% - 50%).  
**Plataforma sugerida:** Google Meet o Discord con cámaras encendidas y diapositivas compartidas.  
**Duración objetivo:** 3:30 a 4:00 minutos.  

---

**[0:00 - 0:45] Introducción y Contexto**  
*Cámaras encendidas de Esteban y Cristian. Diapositiva 1 en pantalla.*

**Esteban:**  
"Un cordial saludo para la docente Raquel Leottau Díaz y compañeros del curso. Somos el CIPAS Grupo 8, conformado por Cristian Andrés Flórez Arboleda y mi persona, Esteban David Marrugo Jassir, del primer semestre de Ingeniería de Software de la Universidad de Cartagena. Hoy venimos a presentar nuestra propuesta metodológica de la Unidad 2: la **Estrategia 3C**, un modelo estructurado para vivir de manera real y efectiva los tres momentos metodológicos del aprendizaje en la educación a distancia."

**Cristian:**  
"Esta estrategia nace de una necesidad real que identificamos en nuestro proceso formativo. Muchas veces se tiene la falsa idea de que estudiar a distancia consiste únicamente en dividirse las preguntas de un taller a última hora. Como bien señala el pedagogo Amaury Lora Sfer, la educación a distancia no funciona como un mosaico de partes pegadas, sino como un proceso dialéctico donde el estudio individual, el debate en CIPAS y la tutoría presencial están estrechamente articulados."

---

**[0:45 - 1:45] Los Tres Momentos y el Mapa Conceptual**  
*Diapositivas 2 y 3 en pantalla.*

**Esteban:**  
"Para ilustrar esta articulación, construimos nuestro mapa conceptual jerárquico. En la cúspide se encuentra la Educación a Distancia de la Universidad de Cartagena, que se ramifica en los tres momentos obligatorios:
El **primer momento** es el estudio individual y autónomo. Aquí el estudiante analiza el módulo institucional, gestiona sus horarios de acuerdo a los créditos académicos y produce sus notas reflexivas.
Este estudio individual es el insumo indispensable que alimenta al **segundo momento**: el trabajo colaborativo en CIPAS. Aquí no venimos a repartirnos párrafos, venimos a co-validar; es decir, a contrastar qué entendió cada uno y redactar nuestro protocolo colaborativo."

**Cristian:**  
"Y de esa discusión en equipo surge el insumo para el **tercer momento**: la tutoría presencial de los sábados. El tutor en el salón no llega a dictar una clase magistral desde cero; llega a cumplir su rol de mediador pedagógico, resolviendo aquellas dudas complejas que el CIPAS no pudo destrabar solo. Cuando la tutoría concluye, esa síntesis retroalimenta nuevamente la autonomía del estudiante, completando el ciclo virtuoso de aprender a aprender."

---

**[1:45 - 3:00] Fases de la Estrategia 3C y Herramientas Digitales**  
*Diapositivas 4 y 5 en pantalla.*

**Esteban:**  
"Para llevar esto a la práctica diaria de un estudiante de Ingeniería de Software, creamos la **Estrategia 3C: Captura, Co-validación y Consolidación**.
La primera fase, **Captura**, ocurre de lunes a miércoles. Cada integrante lee el módulo de la unidad y procesa los conceptos en Obsidian con la técnica Feynman, explicando cada tema con palabras propias. Nadie puede saltarse esta fase."

**Cristian:**  
"La segunda fase, **Co-validación**, se realiza entre jueves y viernes. Nos conectamos por un canal de voz en Discord y abrimos un Google Docs institucional. Mediante roles rotativos —un moderador de tiempo y un relator— comparamos los apuntes de cada uno, resolvemos discrepancias y redactamos el protocolo colaborativo. Si surge una duda donde ninguno de los dos llega a un acuerdo, la marcamos como 'Duda Semilla' para llevarla a clase."

**Esteban:**  
"La tercera fase, **Consolidación**, se vive el sábado presencial en la tutoría. Allí participamos activamente exponiendo las conclusiones del equipo y consultando nuestras dudas semilla con la profesora Raquel. Para evaluar que la estrategia funcione, implementamos una regla de oro: un 'Pase de Entrada' al CIPAS; el compañero que no haya realizado su lectura individual previa no puede firmar la entrega colaborativa."

---

**[3:00 - 3:45] Conclusiones y Cierre**  
*Diapositiva 6 en pantalla. Cámaras de ambos.*

**Cristian:**  
"Esta estrategia impacta directamente en el principio de 'aprender a aprender', porque nos enseña a ser autocríticos con nuestro tiempo, a detectar vacíos conceptuales antes de las evaluaciones y a entender que el aprendizaje en equipo se construye mediante el diálogo y la responsabilidad compartida."

**Esteban:**  
"Como conclusión final, entendemos que la flexibilidad de la educación a distancia no es tiempo libre para postergar, sino la libertad para autogestionar el conocimiento con rigor profesional. Muchas gracias por su atención."
