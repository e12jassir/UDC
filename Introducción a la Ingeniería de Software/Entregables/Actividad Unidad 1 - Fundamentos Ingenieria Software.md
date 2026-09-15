# Cuestionario de Conceptualización Fundamental sobre Bases Teóricas de la Carrera

**Programa Académico:** Ingeniería de Software  
**Asignatura:** Introducción a la Ingeniería de Software (`IX24014-A1`)  
**Docente:** Jhon Carlos Arrieta Arrieta  
**Institución:** Universidad de Cartagena — Facultad de Ingeniería  
**Fecha:** Septiembre de 2026  

---

### Presentación de Integrantes (Subgrupo CIPAS — Máximo 3)

| Nombre Completo | Código Estudiantil | Enlace de Video de Sustentación Individual |
| :--- | :---: | :--- |
| **Esteban David Marrugo Jassir** | `7502620036` | [Video de Sustentación Individual](https://drive.google.com/file/d/1LYkn41Nbq8P3lyiO0KVQL7IRjr-4IKhE/view?usp=drive_link) |
| **Cristian Andrés Flórez Arboleda** | `75026200XX` | `[Enlace Pendiente - Google Drive / YouTube Institucional]` |
| *(Tercer integrante a definir)* | `75026200XX` | `[Enlace Pendiente - Google Drive / YouTube Institucional]` |

---

## I. Comprensión básica de la ingeniería de software

### 1. ¿Qué entiende por ingeniería de software?
Para mí, la ingeniería de software es la aplicación rigurosa de métodos científicos, principios de diseño y estándares de ingeniería para construir sistemas computacionales que sean confiables, escalables y fáciles de mantener a lo largo del tiempo. 

No se trata simplemente de escribir líneas de código para que una máquina haga algo en el momento. La ingeniería entra en juego cuando ese sistema debe operar en entornos reales, soportar cambios continuos de requerimientos, ser mantenido por equipos de varias personas y no colapsar cuando crece la carga de usuarios o datos. Es la diferencia entre construir un cobertizo en el patio de la casa y diseñar un edificio sismorresistente con planos, cálculo estructural y control de calidad.

### 2. ¿Cuál es el objetivo principal de la ingeniería de software?
Su objetivo central es resolver la llamada "crisis del software": producir sistemas que cumplan exactamente con los requisitos del usuario, entregados dentro del presupuesto y tiempo acordados, garantizando calidad funcional y técnica. 

En la práctica, esto significa minimizar los fallos en producción, reducir el costo del mantenimiento futuro (que históricamente representa más del 60% del costo total de un proyecto) y asegurar que el software pueda evolucionar sin tener que reescribirlo desde cero cada vez que las necesidades del entorno cambien.

### 3. ¿Qué diferencia existe entre software y hardware?
El hardware es la base física y tangible del sistema: silicio, compuertas lógicas, pistas de cobre, memorias, transistores y periféricos mecánicos o electrónicos. Se desgasta con el uso, sufre deterioro térmico y requiere manufactura física.

El software es el conjunto lógico e intangible de instrucciones, estructuras de datos y algoritmos organizados para que ese hardware ejecute tareas útiles. El software no se gasta por fricción física; en cambio, envejece por degradación conceptual (obsolescencia frente a nuevas tecnologías, fallos de diseño acumulados o falta de adaptación al entorno). Mientras que modificar el hardware suele requerir cambiar piezas físicas, el software es maleable por naturaleza, aunque esa misma flexibilidad lo vuelve propenso a desordenarse si no se diseña con disciplina.

### 4. ¿Por qué ambos deben trabajar de manera integrada?
Porque son dos caras inseparables de una misma moneda funcional. Un procesador sin instrucciones cargadas en memoria no es más que un bloque inerte de silicio consumiendo corriente; a su vez, el algoritmo más sofisticado del mundo no sirve de nada si no existe un medio físico que ejecute los ciclos de reloj y conmute los estados lógicos.

La integración asegura que el software aproveche de forma óptima las capacidades del hardware (como registros de la CPU, paralelismo multihilo o buses de memoria) y que el hardware proporcione los mecanismos de protección, direccionamiento e interrupción que el software necesita para operar de manera segura sin corromper el sistema.

### 5. ¿Qué es un sistema informático?
Es un ecosistema integrado compuesto por hardware, software, datos y personas (el componente humano o *peopleware*) organizados bajo un conjunto de procedimientos para capturar, procesar, almacenar y distribuir información con un fin determinado.

Un sistema informático no se reduce a la computadora que tenemos en el escritorio; abarca desde una terminal en un punto de venta conectada a una base de datos remota hasta la infraestructura distribuida de servidores que gestiona las notas de nuestra universidad.

### 6. ¿Qué componentes conforman un sistema informático?
Un sistema informático opera mediante cuatro componentes esenciales:
- **Hardware:** La infraestructura física (procesador, memoria RAM, buses, unidades de estado sólido, pantallas, tarjetas de red).
- **Software:** La lógica del sistema, dividida entre software de base (sistemas operativos, controladores) y software de aplicación (navegadores, bases de datos, suites ofimáticas).
- **Datos e Información:** Los elementos en bruto que ingresan al sistema, se estructuran en memorias o bases de datos y se transforman en conocimiento útil tras el procesamiento.
- **Factor Humano y Procedimientos:** Los usuarios que interactúan con el sistema, los administradores que lo mantienen y los protocolos operativos que dictan cómo y cuándo se procesa la información.

### 7. ¿Qué papel cumple el software dentro de un sistema informático?
El software actúa como el cerebro y mediador del sistema. Es quien toma los datos que ingresan por los periféricos, decide qué transformaciones aplicarles mediante algoritmos lógicos, coordina la interacción con la memoria y el almacenamiento persistente, y genera las respuestas que el usuario percibe.

Sin software, el hardware carece de propósito y directriz. Es el software el que abstrae la complejidad de los voltajes y señales eléctricas, convirtiéndolas en interfaces comprensibles, servicios en red y herramientas de trabajo para las personas.

### 8. ¿Qué tipos de software existen? Describa al menos tres.
Podemos clasificar el software en tres grandes familias según su nivel de abstracción y propósito:

1. **Software de Sistema:** Es la capa base que gestiona directamente el hardware y sirve de plataforma para que los demás programas funcionen. Incluye los sistemas operativos (Linux, FreeBSD, Windows), los cargadores de arranque (*bootloaders*), los controladores de dispositivos (*drivers*) y los sistemas de archivos. Su prioridad es la eficiencia, la gestión de memoria y el control de accesos.
2. **Software de Programación y Desarrollo:** Son las herramientas que los ingenieros usamos para construir otro software. Abarca compiladores (GCC, Clang), intérpretes (Python, Node.js), depuradores (*debuggers* como GDB), editores de código y entornos de desarrollo integrados (Neovim, VS Code).
3. **Software de Aplicación:** Son los programas diseñados para que el usuario final resuelva problemas concretos o realice tareas específicas en su vida cotidiana o laboral. Aquí entran los navegadores web (Firefox, Chromium), los gestores de bases de datos, las hojas de cálculo, los reproductores multimedia y los sistemas bancarios.

### 9. ¿Por qué el software es fundamental en la sociedad actual?
Porque la infraestructura crítica del planeta entero corre sobre software. Las redes eléctricas, las torres de control aéreo, los sistemas de agua potable, los quirófanos de los hospitales y los mercados financieros globales dependen de millones de líneas de código que deben operar las 24 horas sin fallar.

El software dejó de ser un simple accesorio para automatizar cálculos de oficina y se convirtió en el tejido conectivo de la civilización moderna. Si los sistemas informáticos se apagan por completo durante 24 horas, el comercio internacional se detiene, las comunicaciones colapsan y los servicios de emergencia quedan a ciegas.

### 10. ¿Qué ejemplos de software utiliza diariamente?
En mi rutina académica y técnica diaria como estudiante de ingeniería de software utilizo:
- **Linux (Kernel y herramientas GNU):** El sistema operativo base en mi portátil, donde gestiono procesos, permisos y el sistema de archivos desde la terminal Bash.
- **Neovim / Obsidian:** Mis entornos principales para edición de código y gestión de notas y documentación técnica mediante archivos planos en Markdown.
- **Git:** El sistema de control de versiones distribuido con el que rastreo y aseguro cada cambio en mis repositorios y proyectos.
- **Firefox / Brave:** Navegadores web para consultar documentación técnica, portales académicos de la UDC (SIMA) y repositorios en GitHub.
- **Compiladores e intérpretes (Java OpenJDK, Python, GCC):** Para compilar y ejecutar los algoritmos, talleres de programación y scripts de automatización que desarrollamos en la carrera.

---

## II. Ingeniería de software como disciplina

### 1. ¿Por qué el desarrollo de software requiere un enfoque de ingeniería?
Porque construir sistemas complejos no es una labor intuitiva ni artesanal. Cuando un proyecto pasa de unas cuantas líneas a miles o millones de instrucciones, la mente humana no puede retener todas las variables en la cabeza al mismo tiempo.

Sin procesos formales de ingeniería —como estimación de costos, análisis de riesgos, especificación formal y pruebas sistemáticas— el desarrollo termina siendo una lotería. La ingeniería aporta previsibilidad y rigor: permite construir sistemas garantizando que no fallen en condiciones críticas, tal como un ingeniero civil calcula vigas para que un puente soporte el tráfico pesado sin venirse abajo.

### 2. ¿Qué diferencia existe entre programar y desarrollar software?
Programar es el acto específico de traducir una lógica o algoritmo a un lenguaje entendible por la máquina (sintaxis, variables, bucles y funciones). Es una habilidad técnica puntual.

Desarrollar software bajo un enfoque de ingeniería abarca el ciclo de vida completo. Involucra entender el problema de negocio del cliente, negociar y filtrar requisitos, diseñar la arquitectura del sistema, elegir las estructuras de datos adecuadas, escribir pruebas automatizadas, desplegar en servidores y mantener el sistema vivo durante años. Un programador escribe código; un desarrollador de software diseña soluciones sostenibles donde el código es solo una de las fases finales.

### 3. ¿Qué problemas pueden surgir si el software se desarrolla sin planificación?
El síntoma clásico es el caos operativo y la deuda técnica descontrolada:
- **Efecto espagueti:** El código se vuelve un enredo monolítico donde tocar una función para corregir un error desata tres fallos nuevos en módulos que parecían no tener relación.
- **Sobrecostos y retrasos masivos:** Al no definir alcances claros, el equipo trabaja a ciegas, repite trabajo ya hecho y se le acaba el presupuesto a mitad de camino.
- **Software inútil para el usuario:** Se entrega un producto técnicamente funcional pero que resuelve un problema que el cliente nunca tuvo.
- **Abandono del proyecto:** Cuando el código original se vuelve imposible de leer y mantener, hasta los mismos autores prefieren botarlo y empezar de cero.

### 4. ¿Qué etapas suelen existir en el desarrollo de software?
Aunque las metodologías varían en su ritmo (cascada, iterativo o ágil), las etapas esenciales siempre están presentes:
1. **Levantamiento y Análisis de Requisitos:** Entender a fondo qué problema existe y qué restricciones impone el entorno.
2. **Diseño de Arquitectura y Componentes:** Definir cómo se organizará el sistema, sus interfaces, bases de datos y patrones de comunicación.
3. **Implementación o Codificación:** Escribir el código fuente siguiendo estándares limpios y pruebas locales.
4. **Pruebas y Validación (QA):** Someter el sistema a pruebas unitarias, de integración, de carga y de seguridad para cazar errores antes del despliegue.
5. **Despliegue y Puesta en Producción:** Montar el software en servidores reales para que los usuarios finales lo utilicen.
6. **Mantenimiento y Evolución:** Corregir errores residuales, parchar vulnerabilidades y agregar nuevas funciones a medida que el negocio cambia.

### 5. ¿Por qué es importante analizar los requisitos antes de programar?
Porque corregir un error en la fase de análisis cuesta una fracción mínima de lo que cuesta corregirlo cuando el sistema ya está en producción. Si un requisito se entendió mal en la etapa de levantamiento, todo el diseño, las tablas de base de datos y miles de líneas de código se construyen sobre una premisa falsa.

Analizar los requisitos permite delimitar el alcance real del proyecto, aterrizar expectativas irreales del cliente y asegurarse de que el equipo entiende el negocio antes de sentarse frente al teclado a quemar horas de programación innecesarias.

### 6. ¿Qué sucede cuando los requisitos de un sistema no están claros?
Aparece el llamado *Scope Creep* (corrimiento del alcance). El cliente pide cambios sobre la marcha todas las semanas porque nunca se acordó qué hacía y qué no hacía el software. 

Esto genera frustración en el equipo, desgaste mental, entregas aplazadas indefinidamente y un código parchado a la fuerza. Al final, el cliente siente que pagó por algo que no le sirve, y los desarrolladores quedan con un sistema frágil que nadie quiere tocar por miedo a que se rompa.

### 7. ¿Por qué es importante documentar un sistema de software?
El código dice *cómo* hace las cosas la máquina, pero la documentación explica *por qué* se diseñó de esa manera. En la industria, los desarrolladores rotan de empresa o cambian de proyecto con frecuencia. 

Si un sistema no cuenta con diagramas de arquitectura, contratos de interfaces (APIs) y guías de configuración, el nuevo programador que llegue gastará semanas descifrando código a ciegas. Documentar es un acto de respeto técnico hacia el equipo y la única garantía de que el conocimiento del sistema no desaparezca cuando alguien renuncia.

### 8. ¿Qué papel cumple el análisis en el desarrollo de software?
El análisis responde a la pregunta: **¿QUÉ debe hacer el sistema?** 

Su función es descomponer la complejidad del problema del cliente en casos de uso, flujos de datos y reglas de negocio sin preocuparse todavía por el lenguaje de programación ni por la base de datos que se usará. Es el filtro que separa lo esencial de lo accesorio y traduce el lenguaje informal de los usuarios a especificaciones técnicas rigurosas.

### 9. ¿Qué papel cumple el diseño en el desarrollo de software?
El diseño responde a la pregunta: **¿CÓMO se va a construir el sistema?** 

Aquí se toman las decisiones estructurales críticas: cómo se organizarán los módulos, qué patrones arquitectónicos se aplicarán, cómo se normalizarán las tablas de base de datos y qué protocolos comunicarán los servicios. Un buen diseño previene la rigidez del código y garantiza que el software pueda crecer sin que su estructura colapse.

### 10. ¿Qué importancia tienen las pruebas dentro del desarrollo de software?
Las pruebas son la red de seguridad del ingeniero. Permiten verificar de forma objetiva que el sistema se comporta exactamente como se especificó y que soporta escenarios extremos sin romperse.

Sin pruebas automatizadas (unitarias, de integración y de regresión), cada despliegue a producción se convierte en un acto de fe donde los usuarios finales terminan siendo los conejillos de indias que descubren los errores críticos. Probar software no es un lujo que se hace al final si sobra tiempo; es una disciplina continua que da confianza para modificar y mejorar el código todos los días.

---

## III. Principios fundamentales de la ingeniería de software

### 1. ¿Qué significa abstracción en el desarrollo de software?
La abstracción consiste en enfocarse en las características esenciales de un objeto o componente, ocultando o ignorando los detalles secundarios o de bajo nivel que no son relevantes para el contexto actual.

En programación, cuando usamos una interfaz o llamamos a una función como `guardar_archivo()`, nos concentramos en lo que esa función hace por nosotros, sin necesidad de saber cómo el sistema operativo administra los sectores del disco, los bloques de memoria o los permisos a nivel de kernel.

### 2. ¿Por qué la abstracción ayuda a manejar la complejidad?
Porque la capacidad de procesamiento de la mente humana es limitada; no podemos lidiar con cientos de detalles de hardware y lógica al mismo tiempo. 

La abstracción nos permite construir sistemas por capas superpuestas. Un desarrollador web puede crear una aplicación bancaria compleja trabajando sobre protocolos de alto nivel (como HTTP y JSON) sin tener que preocuparse por cómo viajan los paquetes TCP/IP por la fibra óptica o cómo el silicio de la tarjeta de red commuta voltajes. Sin abstracción, el desarrollo moderno de software sería matemáticamente imposible de abordar.

### 3. ¿Qué es modularidad?
Es la propiedad de diseñar un sistema dividiéndolo en partes más pequeñas, lógicas e independientes llamadas módulos. Cada módulo agrupa funciones y datos estrechamente relacionados y se comunica con el resto del sistema mediante interfaces explícitas.

En vez de tener un archivo monolítico gigante de diez mil líneas de código donde todo está mezclado, el sistema se particiona en módulos especializados: autenticación, facturación, notificaciones, inventario, etc.

### 4. ¿Por qué dividir un sistema en módulos facilita su desarrollo?
- **Trabajo en paralelo:** Permite que varios ingenieros o equipos trabajen al mismo tiempo en módulos distintos sin pisarse el trabajo ni generar conflictos en el repositorio.
- **Facilidad de depuración:** Cuando ocurre un fallo en el cálculo de impuestos, no se revisa todo el sistema; se va directo al módulo de facturación.
- **Reutilización de código:** Un módulo bien empaquetado (por ejemplo, el de envío de correos electrónicos) puede utilizarse en varios proyectos distintos sin necesidad de reescribirlo.

### 5. ¿Qué es la separación de responsabilidades?
Es un principio arquitectónico formulado por Edsger Dijkstra que postula que un sistema debe descomponerse de tal manera que cada componente atienda una única preocupación o aspecto del problema.

El ejemplo más claro es el patrón arquitectónico por capas: la capa de presentación solo se encarga de mostrar la interfaz de usuario; la capa de dominio o negocio solo aplica las reglas de cálculo y validación; y la capa de persistencia solo sabe cómo interactuar con la base de datos. Ninguna capa asume las tareas de las otras.

### 6. ¿Por qué es importante dividir las funciones de un sistema?
Porque cuando una sola función o clase hace de todo (calcula nómina, valida formatos, dibuja pantallas y guarda en disco), cualquier cambio mínimo en la base de datos puede romper la interfaz de usuario.

Dividir funciones reduce drásticamente los efectos colaterales indeseados. Facilita la comprensión del código para quien entra nuevo al proyecto y permite reemplazar componentes enteros (por ejemplo, cambiar MySQL por PostgreSQL) afectando únicamente al módulo responsable de los datos.

### 7. ¿Qué es el ocultamiento de información?
Es el principio propuesto por David Parnas que establece que cada módulo debe ocultar celosamente sus decisiones internas de diseño, sus estructuras de datos privadas y sus algoritmos, exponiendo hacia afuera únicamente una interfaz pública y estable.

Los demás módulos saben *qué* servicio les ofrece ese componente, pero tienen prohibido saber o depender de *cómo* lo resuelve por dentro.

### 8. ¿Cómo contribuye el ocultamiento de información a la seguridad del software?
Contribuye blindando el estado interno de los datos contra modificaciones arbitrarias o indebidas desde el exterior. Si un objeto bancario mantiene privada su variable de saldo y solo permite modificarla a través de métodos controlados como `consignar()` o `retirar()`, se garantiza que nadie pueda inyectar un saldo negativo o saltarse las validaciones de auditoría.

Además, desde el punto de vista del mantenimiento, el ocultamiento protege al software de dependencias frágiles: si el día de mañana decido cambiar una estructura interna de lista a un árbol binario para ganar velocidad, los demás módulos ni se enteran ni se rompen, porque su interfaz pública no cambió.

### 9. ¿Qué es la cohesión en un componente de software?
La cohesión mide el grado de relación, afinidad y enfoque que tienen los elementos que residen dentro de un mismo módulo o clase. 

Un módulo tiene alta cohesión cuando todas sus variables, funciones y métodos trabajan juntos hacia un único propósito bien definido. Por el contrario, un módulo tiene baja cohesión si acumula una mezcla caótica de funciones que no guardan relación lógica entre sí (las típicas clases "cajón de sastre" llamadas `Utilidades` o `Manager`).

### 10. ¿Por qué es deseable que un módulo tenga alta cohesión?
Porque un módulo enfocado en una sola cosa es mucho más fácil de entender, probar y reutilizar. 

Cuando una clase tiene alta cohesión, sus métodos comparten datos internos de forma natural, tiene pocas razones para cambiar a lo largo del tiempo y sus pruebas unitarias son directas y rápidas. Si un componente solo hace lo que le corresponde, el sistema se vuelve robusto y predecible.

---

## IV. Acoplamiento y diseño de sistemas

### 1. ¿Qué significa acoplamiento entre módulos?
El acoplamiento mide el grado de interdependencia que existe entre dos o más módulos de un sistema. En términos prácticos, indica qué tan "amarrado" está el módulo A respecto a los detalles internos del módulo B.

Si para que el módulo de pagos funcione necesita acceder directamente a las variables privadas de la base de datos de usuarios o conocer cómo están estructuradas sus tablas en memoria, decimos que existe un acoplamiento estrecho. Si, por el contrario, se comunican pasándose únicamente un identificador simple a través de un contrato o interfaz definida, el acoplamiento es débil o bajo.

### 2. ¿Por qué el acoplamiento bajo es deseable?
Porque otorga libertad de cambio. Cuando los módulos están débilmente acoplados, podemos modificar, optimizar, refactorizar o incluso reescribir por completo la lógica interna de un módulo sin miedo a que el resto del sistema deje de compilar o empiece a fallar de forma silenciosa.

Además, el acoplamiento bajo permite aislar las pruebas: puedo probar el motor de liquidación de facturas usando datos simulados (*mocks* o *stubs*) sin necesidad de tener levantado el servidor de base de datos de producción.

### 3. ¿Qué problemas aparecen cuando el acoplamiento es alto?
Aparece el temido "efecto dominó". Haces un cambio de una sola línea en el módulo de autenticación para cambiar el formato de una fecha, y de repente colapsa el módulo de reportes y la pasarela de pagos.

El acoplamiento alto genera sistemas quebradizos (*fragility*), rígidos (*rigidity*, donde cada cambio exige una cascada interminable de modificaciones en todo el proyecto) y no reutilizables (*immobility*, porque resulta imposible extraer una función útil para llevarla a otro proyecto sin tener que arrastrar la mitad del sistema consigo).

### 4. ¿Cómo influyen estos principios en la calidad del software?
La regla de oro de la arquitectura de software es: **alta cohesión y bajo acoplamiento**. 

Cuando un sistema respeta estos dos pilares, la calidad se dispara en todas las métricas que importan:
- **Mantenibilidad:** Encontrar y reparar un error toma minutos en vez de días.
- **Escalabilidad:** Se pueden separar módulos pesados y convertirlos en microservicios independientes que escalan en servidores distintos.
- **Testabilidad:** Cada pieza se verifica por separado con pruebas unitarias rápidas y confiables.
- **Longevidad:** El software puede sobrevivir diez o quince años adaptándose a nuevas tecnologías sin volverse obsoleto.

### 5. Proponga un ejemplo de sistema donde sea importante dividir el software en módulos.
Pensemos en el sistema académico de una universidad como la Universidad de Cartagena (SIMA / SMA). 

Si todo estuviera en un solo bloque de código, el día de matrículas financieras el sistema colapsaría por completo y no dejaría que los profesores suban notas ni que los estudiantes consulten material en el aula virtual. 

Al modularizarlo, separamos:
- **Módulo de Admisiones y Registro:** Gestiona inscripciones y datos personales.
- **Módulo Financiero y Facturación:** Liquida matrículas y valida pagos bancarios.
- **Módulo de Control Académico:** Registra calificaciones y calcula promedios.
- **Módulo de Campus Virtual (LMS):** Aloja foros, tareas y material didáctico.

Cada módulo tiene su propia base de datos o esquema, se comunican por APIs seguras y, si el módulo de pagos se satura durante dos horas, el campus virtual sigue funcionando sin interrupciones.

### 6. ¿Cómo puede facilitar la modularidad el mantenimiento del software?
Facilita el mantenimiento porque acota el "radio de explosión" de cualquier error. Si un usuario reporta que las constancias de estudio salen con el membrete descuadrado, el mantenedor no tiene que inspeccionar 50.000 líneas de código; va directo al componente generador de PDFs del módulo académico.

Asimismo, la modularidad permite la sustitución limpia: si mañana la universidad cambia de proveedor de pasarela de pago (de PSE a Wompi o PayU), solo se reescribe el adaptador del módulo financiero, dejando el 95% restante del software intacto.

### 7. ¿Por qué es importante que un sistema pueda modificarse con facilidad?
Porque el software existe para modelar el mundo real, y el mundo real nunca es estático. Las leyes tributarias cambian, los modelos de negocio evolucionan, surgen nuevos competidores y los requerimientos de los usuarios mutan mes a mes.

Un software que no se puede modificar con facilidad es un software muerto. Si cada cambio solicitado por el cliente tarda seis meses y cuesta una fortuna en parches, la empresa u organización pierde competitividad y termina desechando el sistema por caro e ineficiente.

### 8. ¿Qué relación existe entre diseño y mantenimiento del software?
Existe una relación directa y causal: el diseño de hoy determina el dolor del mantenimiento de mañana.

El mantenimiento consume entre el 60% y el 80% del presupuesto total a lo largo de la vida de un sistema. Si en la etapa de diseño nos saltamos los principios básicos por entregar rápido (generando deuda técnica), el costo de cada nuevo requerimiento crecerá de forma exponencial. Invertir tiempo en un diseño desacoplado y limpio es la única manera de asegurar que el mantenimiento futuro sea económico, rápido y seguro.

### 9. ¿Qué impacto tiene un mal diseño en un sistema informático?
Un mal diseño no solo hace lento el desarrollo; mata la rentabilidad de las empresas y degrada la confianza del usuario. 

Técnicamente, produce fugas de memoria, cuellos de botella de rendimiento, fallos de concurrencia y huecos graves de seguridad. En el plano humano y financiero, desmotiva a los desarrolladores —que terminan renunciando por el estrés de lidiar con un código inmanejable— y provoca pérdidas millonarias cuando el sistema se cae en fechas clave de facturación o transacciones.

### 10. ¿Cómo puede un buen diseño mejorar la vida útil del software?
Un buen diseño protege al sistema contra el cambio tecnológico. Si la lógica del negocio está desacoplada de la tecnología concreta que se usa hoy (el framework, la base de datos o el sistema operativo), podemos actualizar las librerías viejas, migrar a la nube o cambiar la interfaz visual sin tener que reprogramar las reglas fundamentales de la empresa.

Sistemas con buena arquitectura pueden durar décadas operando de forma continua porque están diseñados como piezas intercambiables, evolucionando gradualmente sin necesidad de demoliciones totales.

---

## V. Modelos de desarrollo de software

### 1. ¿Qué es un modelo de desarrollo de software?
Es una representación abstracta y estructurada de las actividades, fases, roles y artefactos que guían la construcción de un sistema desde su concepción inicial hasta su retiro definitivo.

Un modelo de desarrollo establece las reglas del juego para el equipo: define qué se hace primero, qué criterios deben cumplirse para pasar a la siguiente etapa, cómo se validan los resultados y cómo se gestionan los cambios que surgen en el camino.

### 2. ¿Por qué se utilizan modelos en el desarrollo de software?
Porque el desarrollo de software involucra múltiples disciplinas, plazos y personas coordinadas bajo presión. Sin un modelo claro, el equipo cae en la improvisación y el caos.

Los modelos proporcionan un marco de referencia común: permiten prever recursos, estimar tiempos y costos con base empírica, controlar la calidad en puntos de control específicos y darle visibilidad al cliente sobre el estado real del avance del proyecto.

### 3. ¿En qué consiste el modelo en cascada?
Propuesto formalmente por Winston Royce en 1970, el modelo en cascada (*Waterfall*) es un enfoque secuencial y lineal donde el desarrollo fluye estrictamente hacia abajo a través de fases ordenadas. 

La premisa fundamental de la cascada es que cada fase debe completarse, documentarse y firmarse formalmente antes de que pueda comenzar la siguiente. No se escribe una sola línea de código sin haber terminado y aprobado todos los documentos de diseño, y no se prueba nada hasta haber codificado todo el sistema.

### 4. ¿Qué etapas incluye el modelo en cascada?
En su versión clásica comprende cinco etapas secuenciales:
1. **Análisis y definición de requisitos:** Levantamiento exhaustivo y congelamiento de especificaciones en documentos formales.
2. **Diseño del sistema y del software:** Definición de la arquitectura global y el diseño detallado de módulos e interfaces.
3. **Implementación y pruebas de módulos (Codificación):** Programación de cada unidad de software de acuerdo con los planos previos.
4. **Integración y pruebas del sistema:** Ensamble de todos los módulos y validación del sistema completo para verificar que cumple los requisitos.
5. **Operación y mantenimiento:** Puesta en marcha en el entorno del cliente y corrección de defectos encontrados durante el uso real.

### 5. ¿Qué ventajas tiene el modelo en cascada?
- **Simplicidad y claridad:** Su estructura lineal es muy fácil de entender y administrar; cada fase tiene entregables y revisiones bien delimitadas.
- **Control y disciplina:** Facilita la gestión contractual y la supervisión del proyecto, ya que los hitos de avance están definidos sobre fechas y documentos específicos.
- **Documentación exhaustiva:** Al exigir especificaciones completas antes de codificar, deja un registro histórico detallado de cada decisión técnica tomada.

### 6. ¿Qué limitaciones puede presentar el modelo en cascada?
- **Inflexibilidad absoluta ante el cambio:** Asume que los usuarios saben exactamente lo que necesitan desde el primer día y que los requerimientos no van a cambiar en un año. En el mundo real, los clientes descubren lo que realmente quieren cuando ven el sistema funcionando.
- **Entrega de valor tardía:** El cliente no ve una sola pantalla interactiva hasta las fases finales del proyecto. Si hubo un error conceptual en los requisitos del mes uno, se descubre en el mes doce, cuando ya se gastó todo el presupuesto.
- **Bloqueo de fases:** Si la etapa de análisis se retrasa dos meses, los programadores y evaluadores se quedan de brazos cruzados esperando su turno.

### 7. ¿Qué es el modelo en espiral?
Diseñado por Barry Boehm en 1986, el modelo en espiral es un proceso de desarrollo iterativo guiado explícitamente por el **análisis y gestión de riesgos**.

En lugar de avanzar en línea recta, el proyecto avanza en ciclos concéntricos (espirales). Cada vuelta de la espiral pasa por cuatro cuadrantes: determinar objetivos y restricciones, evaluar alternativas e identificar/mitigar riesgos (generalmente mediante prototipos rápidos), desarrollar y verificar el producto de esa fase, y planificar el siguiente ciclo con retroalimentación del cliente.

### 8. ¿Qué problema intenta resolver el modelo en espiral?
Intenta resolver el talón de Aquiles de la cascada: la acumulación de incertidumbre y riesgos no evaluados hasta el final del proyecto.

En proyectos grandes o innovadores, hay tecnologías no probadas, requisitos difusos o dudas sobre la viabilidad comercial. El modelo en espiral ataca esos riesgos desde las primeras iteraciones: si hay duda de si una base de datos soportará diez mil transacciones por segundo, se construye un prototipo de prueba en el primer ciclo. Si el riesgo es insalvable, el proyecto se detiene a tiempo sin quemar millones de dólares.

### 9. ¿Qué diferencia existe entre modelos tradicionales y metodologías ágiles?
La diferencia radica en su filosofía frente a la incertidumbre y el cambio:
- **Modelos tradicionales (Predictivos):** Buscan predecir y planificar todo con meses de anticipación. Priorizan el cumplimiento riguroso de planes preestablecidos, procesos formales y contratos con especificaciones cerradas.
- **Metodologías ágiles (Adaptativas):** Asumen que el cambio es inevitable y bienvenido. Trabajan en ciclos muy cortos (semanas), entregando software funcional de manera continua, priorizando la colaboración directa con el cliente sobre la documentación excesiva y adaptando el rumbo del proyecto según los resultados reales obtenidos en cada entrega.

### 10. ¿En qué situaciones podría ser adecuado utilizar un modelo tradicional?
El modelo tradicional no está muerto; sigue siendo la mejor opción cuando se cumplen tres condiciones:
1. **Requisitos 100% conocidos, estables y no negociables:** Por ejemplo, la implementación de un protocolo de comunicaciones estándar regulado por normas internacionales (como un procesador de tramas bancarias ISO 8583).
2. **Sistemas críticos donde la vida o la seguridad están en juego:** En software embebido para marcapasos, controles de vuelo aeroespacial o sistemas de apagado de reactores nucleares, donde cada requisito debe verificarse matemáticamente y la documentación formal es exigida por entes reguladores.
3. **Contrataciones públicas de precio fijo y alcance cerrado:** Donde los términos contractuales exigen planos y especificaciones inalterables antes de liberar cualquier partida presupuestal.

---

## VI. Metodologías ágiles

### 1. ¿Qué son las metodologías ágiles?
Son marcos de trabajo y filosofías de gestión de proyectos fundamentados en el Manifiesto Ágil de 2001. En lugar de intentar predecir el futuro a meses vista, abordan el desarrollo mediante ciclos iterativos e incrementales de corta duración.

Su enfoque pone en el centro la entrega continua de valor, la autoorganización del equipo técnico y la comunicación directa y frecuente con el cliente o usuario final, aceptando los cambios de requisitos como algo natural y positivo para la competitividad del producto.

### 2. ¿Por qué surgieron las metodologías ágiles?
Surgieron como una rebelión necesaria de los ingenieros contra la burocracia paralizante de los modelos pesados de los años 80 y 90. En esa época, más de la mitad de los proyectos de software fracasaban estrepitosamente: se gastaban presupuestos millonarios en redactar manuales y diagramas interminables, y cuando por fin se entregaba el software dos o tres años después, el mercado ya había cambiado y el sistema quedaba obsoleto antes de nacer.

Un grupo de 17 líderes de la industria (entre ellos Martin Fowler, Kent Beck y Robert C. Martin) se reunió en Utah para decir: *"Basta de procesos pesados; centrémonos en lo que de verdad importa: software funcionando y valor para el usuario"*.

### 3. ¿Qué características tienen los métodos ágiles?
- **Desarrollo iterativo e incremental:** El producto no se entrega de golpe al final; crece bloque a bloque en iteraciones de 1 a 4 semanas.
- **Flexibilidad ante el cambio:** Los requerimientos pueden evolucionar y reordenarse al inicio de cada ciclo sin penalizaciones contractuales destructivas.
- **Equipos multidisciplinarios y autónomos:** Desarrolladores, evaluadores y diseñadores trabajan hombro a hombro con la autoridad para tomar decisiones técnicas cotidianas.
- **Retroalimentación constante:** Al final de cada ciclo se muestra software real funcionando al cliente, recogiendo sus opiniones para ajustar el siguiente paso.

### 4. ¿Qué es Scrum?
Scrum es el marco de trabajo ágil más extendido en la industria para gestionar y desarrollar productos complejos. No es una metodología prescriptiva paso a paso, sino un conjunto de principios, roles, eventos y artefactos diseñados para fomentar la transparencia, la inspección y la adaptación continua.

En Scrum, el trabajo se organiza en bloques de tiempo fijos (*timeboxes*) llamados Sprints, donde el equipo se compromete a transformar una lista priorizada de necesidades en un incremento de producto potencialmente utilizable.

### 5. ¿Qué roles existen en Scrum?
Scrum define con precisión tres roles esenciales:
1. **Product Owner (Dueño del Producto):** Es la voz del negocio y del cliente. Es el único responsable de maximizar el valor del producto y de gestionar y priorizar el *Product Backlog* (la lista de cosas por hacer).
2. **Scrum Master:** Es un líder servicial y facilitador del proceso. Su misión es eliminar los impedimentos u obstáculos que frenan al equipo, protegerlo de interrupciones externas y asegurar que los principios de Scrum se entiendan y apliquen.
3. **Developers (Equipo de Desarrollo):** Son los profesionales técnicos (programadores, arquitectos, evaluadores, diseñadores) que ejecutan el trabajo práctico y se autoorganizan para convertir los elementos del backlog en código real probado.

### 6. ¿Qué es un Sprint?
Es el corazón operativo de Scrum: un ciclo de tiempo cerrado (habitualmente de dos semanas) durante el cual el equipo construye un incremento de software terminado y funcional.

Cada Sprint tiene un objetivo claro (*Sprint Goal*) que no puede alterarse una vez iniciado. Al terminar esas dos semanas, el equipo realiza una demostración (*Sprint Review*) con los interesados y una sesión interna de mejora continua (*Sprint Retrospective*) antes de arrancar el siguiente ciclo.

### 7. ¿Qué es Kanban?
Kanban es un método de gestión del flujo de trabajo originado en las plantas de producción de Toyota y adaptado al software por David J. Anderson. 

A diferencia de Scrum, Kanban no tiene ciclos fijos con fechas límite (no hay Sprints obligatorios ni roles predefinidos). Su principio básico es "hacer visible el trabajo invisible" a través de un tablero de columnas (por ejemplo: *Por Hacer*, *En Progreso*, *En Pruebas*, *Terminado*) y restringir la cantidad de tareas que pueden estar abiertas simultáneamente.

### 8. ¿Cómo ayuda Kanban a organizar el trabajo?
Ayuda aplicando el límite de Trabajo en Progreso (WIP - *Work In Progress*). Al fijar, por ejemplo, que en la columna "En Progreso" no puede haber más de tres tareas a la vez, se obliga al equipo a terminar lo que empezó antes de abrir un nuevo frente de trabajo ("*Stop starting, start finishing*").

Esto expone de inmediato los cuellos de botella del equipo (si hay cinco tareas atascadas en revisión de código, nadie programa nada nuevo hasta desatorar la revisión) y asegura un flujo constante y predecible de entrega sin sobrecargar a los desarrolladores.

### 9. ¿Qué es Extreme Programming (XP)?
Es una metodología ágil creada por Kent Beck enfocada de lleno en la **excelencia técnica y las prácticas de ingeniería** de código limpio. Mientras Scrum se enfoca en la gestión, XP se mete hasta la cocina del código.

Sus prácticas bandera incluyen:
- **TDD (Test-Driven Development):** Escribir las pruebas automatizadas antes de tirar el código de producción.
- **Pair Programming (Programación en Pareja):** Dos desarrolladores frente a una sola pantalla, uno escribiendo y el otro revisando la arquitectura en tiempo real.
- **Refactorización continua:** Limpiar y optimizar el diseño del código a diario sin cambiar su comportamiento externo.
- **Integración continua:** Subir y fusionar cambios al repositorio común varias veces al día con pruebas automáticas.

### 10. ¿Por qué las metodologías ágiles son ampliamente utilizadas actualmente?
Porque el mercado tecnológico actual se mueve a una velocidad brutal. Las empresas no pueden permitirse esperar dieciocho meses para saber si una idea de negocio funciona.

La agilidad reduce el riesgo financiero: permite lanzar un Producto Mínimo Viable (MVP) en dos meses, probarlo con usuarios reales en el mercado y pivotar la estrategia si los datos demuestran que hay que cambiar de rumbo. Además, fomenta equipos técnicos mucho más motivados y comprometidos, ya que tienen autonomía y ven el impacto de su trabajo reflejado en producción cada dos semanas.

---

## VII. Industria del software

### 1. ¿Cómo surgió la industria del software?
En los años 50 y 60, el software no existía como producto comercial independiente; era un accesorio gratuito que los fabricantes de hardware (como IBM) regalaban para que los clientes pudieran operar sus gigantescas computadoras centrales (*mainframes*).

El quiebre histórico ocurrió en 1969, cuando IBM —enfrentando presiones antimonopolio del Departamento de Justicia de EE. UU.— decidió "desempaquetar" (*unbundling*) el software y los servicios del hardware, empezando a cobrar licencias separadas por los programas. Ese hito abrió las puertas para que nacieran las primeras empresas dedicadas exclusivamente a escribir y vender código.

### 2. ¿Qué impacto tuvieron los primeros computadores en el desarrollo del software?
Equipos como el ENIAC o los primeros IBM requerían programarse a nivel de cableado físico o directamente en lenguaje de máquina y tarjetas perforadas binarias. 

Ese entorno tan restrictivo forzó a los pioneros a optimizar cada bit de memoria y cada ciclo de procesamiento. La dificultad titánica de programar esas máquinas gigantescas evidenció la necesidad imperiosa de crear niveles más altos de abstracción que liberaran a los científicos de lidiar con las válvulas de vacío y los relés.

### 3. ¿Qué papel jugaron los lenguajes de programación en el crecimiento del software?
Jugaron un papel revolucionario: democratizaron la informática. La invención de los lenguajes de alto nivel como Fortran (1957) para cálculo científico y COBOL (1959) para negocios permitió a los humanos escribir instrucciones usando palabras en inglés y álgebra comprensible.

El compilador se encargaba de traducir esa lógica humana a ceros y unos para el procesador. Esto multiplicó por diez la velocidad de desarrollo, redujo drásticamente los errores y permitió que el código fuera portátil entre computadoras de distintos fabricantes.

### 4. ¿Cómo influyó la aparición de los microprocesadores?
El lanzamiento del Intel 4004 en 1971 y sus sucesores (8080 y la familia x86) comprimió la Unidad Central de Procesamiento completa en una sola pastilla de silicio.

Esto destruyó la necesidad de tener cuartos refrigerados enteros para operar una computadora. Permitió abaratar los costos de fabricación de forma exponencial y puso procesadores potentes al alcance de pequeñas empresas, laboratorios y entusiastas en sus casas, sembrando la semilla de la informática personal.

### 5. ¿Qué impacto tuvo la popularización de las computadoras personales?
En los años 70 y 80, con la llegada del Apple II, la IBM PC y el sistema operativo MS-DOS, las computadoras entraron a los hogares y escritorios de millones de personas comunes.

Esto detonó una explosión masiva en la demanda de software: nacieron las hojas de cálculo (VisiCalc, Lotus 1-2-3), los procesadores de texto, los videojuegos y los sistemas contables. El software pasó de ser una curiosidad de ingenieros a una industria comercial multimillonaria liderada por gigantes como Microsoft, Apple y Adobe.

### 6. ¿Cómo influyó Internet en el desarrollo del software?
Internet transformó el software de un artefacto aislado que se instalaba mediante disquetes o CD-ROMs a un ecosistema interconectado y vivo.

Permitió que las aplicaciones se comunicaran entre continentes mediante sockets y protocolos estándar, sentó las bases de la colaboración global abierta (facilitando el auge del software libre y Linux) y cambió radicalmente la forma de distribuir programas: las actualizaciones ya no requerían enviar discos por correo postal; se descargaban en segundos por la red.

### 7. ¿Qué impacto tienen las aplicaciones web en la actualidad?
Han convertido al navegador web en el sistema operativo universal de facto. Hoy en día, herramientas de diseño complejas (como Figma), suites ofimáticas (Google Docs, Office 365) o entornos de administración empresarial corren directamente en la web sin requerir instalaciones pesadas en local.

Para los ingenieros, las aplicaciones web cambiaron las reglas: permiten desplegar una mejora en el servidor central y que millones de usuarios la reciban al instante simplemente refrescando su pestaña, eliminando los problemas de compatibilidad con versiones obsoletas en los equipos de los clientes.

### 8. ¿Qué importancia tienen las aplicaciones móviles?
Con la masificación de los teléfonos inteligentes (Android e iOS) a partir de 2007, el software pasó a estar en el bolsillo de cada ser humano las 24 horas del día.

Las aplicaciones móviles cambiaron la economía global: crearon industrias enteras basadas en geolocalización, pagos móviles y transporte bajo demanda (Uber, delivery, banca digital). Exigieron a los ingenieros de software especializarse en interfaces táctiles intuitivas, optimización extrema de consumo de batería y tolerancia a conexiones intermitentes de red.

### 9. ¿Qué nuevas áreas de desarrollo han surgido en la industria del software?
En las últimas dos décadas la industria se ha diversificado en ramas de altísima especialización:
- **Ingeniería de Datos e Inteligencia Artificial:** Modelado de aprendizaje automático, redes neuronales profundas y procesamiento de lenguaje natural.
- **Ciberseguridad Ofensiva y Defensiva:** Protección de infraestructura crítica, auditoría de código, análisis de vulnerabilidades y criptografía.
- **Cloud Computing y DevOps:** Automatización de infraestructura como código, orquestación de contenedores (Docker, Kubernetes) y canalizaciones CI/CD.
- **Sistemas Embebidos e IoT:** Programación de microcontroladores y dispositivos inteligentes conectados en tiempo real.
- **Tecnologías Descentralizadas:** Criptografía aplicada, contratos inteligentes y arquitecturas distribuidas entre pares (*peer-to-peer*).

### 10. ¿Por qué la industria del software continúa creciendo?
Porque el software tiene una propiedad económica única: una vez escrito el código, el costo marginal de duplicarlo y distribuirlo a un millón de personas adicionales es prácticamente cero.

Además, todos los sectores tradicionales —desde la agricultura con sensores de riego y la medicina con diagnóstico por imagen hasta los vehículos eléctricos autónomos— se están digitalizando. Como sentenció Marc Andreessen: *"El software se está comiendo al mundo"*. Cualquier empresa que no adopte soluciones de software eficientes termina siendo desplazada por competidores más ágiles y tecnificados.

---

## VIII. Tecnologías actuales

### 1. ¿Qué es la computación en la nube?
Es un modelo de entrega de recursos computacionales (servidores, almacenamiento, bases de datos, redes y software) bajo demanda a través de Internet, con un esquema de pago por uso.

En lugar de que una empresa gaste miles de dólares comprando servidores físicos para instalarlos en su sótano y pagar aire acondicionado y mantenimiento eléctrico, alquila capacidad elástica a proveedores globales como AWS, Google Cloud o Microsoft Azure.

### 2. ¿Qué ventajas ofrece la computación en la nube?
- **Elasticidad y escalabilidad instantánea:** Si una tienda en línea pasa de mil a un millón de visitas en el Black Friday, la nube aprovisiona servidores adicionales en minutos y los apaga cuando el tráfico baja.
- **Reducción drástica de costos iniciales (CapEx a OpEx):** No se requiere inversión de capital en hardware físico; se paga mes a mes solo por los recursos de CPU, RAM y disco efectivamente consumidos.
- **Alta disponibilidad y redundancia:** Los datos se replican en múltiples centros de datos repartidos por el planeta, garantizando que un corte de energía en una ciudad no bote el servicio.

### 3. ¿Qué es el Internet de las cosas (IoT)?
Es la interconexión digital de objetos físicos cotidianos e industriales mediante sensores, circuitos electrónicos y software embebido, permitiéndoles recolectar y transmitir datos a través de Internet sin intervención humana directa.

Abarca desde termostatos hogareños y relojes inteligentes hasta sensores de presión en oleoductos, boyas marítimas o sistemas de riego agrícola automatizado.

### 4. ¿Qué tipo de software requieren los dispositivos IoT?
Requieren software embebido de bajo nivel y tiempo real (*firmware* o RTOS - *Real-Time Operating Systems*). 

Este software debe estar escrito en lenguajes de alto rendimiento y control de memoria (como C, C++ o Rust), ya que opera sobre microcontroladores con recursos sumamente limitados (pocos kilobytes de memoria RAM y procesadores lentos). Su diseño exige optimización extrema en tres aspectos: consumo ultra-bajo de batería, resiliencia a pérdidas de señal inalámbrica y protocolos de red ligeros como MQTT o CoAP.

### 5. ¿Qué es la inteligencia artificial aplicada al software?
Es la integración de modelos de aprendizaje automático (*Machine Learning*) y redes neuronales en aplicaciones de software para que los sistemas resuelvan problemas no deterministas: reconocer patrones complejos, clasificar imágenes, predecir tendencias o procesar lenguaje humano natural.

En lugar de que un ingeniero escriba manualmente millones de reglas condicionales (`if-else`) para contemplar cada escenario posible, el modelo aprende de forma estadística a partir de grandes volúmenes de datos de entrenamiento.

### 6. ¿Qué aplicaciones actuales utilizan inteligencia artificial?
- **Desarrollo y análisis de código:** Asistentes en el editor y compilador que sugieren autocompletados basados en contexto, detectan vulnerabilidades de seguridad y optimizan consultas SQL.
- **Diagnóstico médico por imagen:** Sistemas de visión por computador que analizan tomografías o radiografías detectando anomalías celulares antes de que sean visibles para el ojo humano.
- **Detección de fraudes financieros:** Motores que analizan millones de transacciones de tarjetas de crédito por segundo, bloqueando pagos sospechosos en milisegundos según el comportamiento habitual del usuario.
- **Vehículos autónomos:** Cámaras y sensores LiDAR procesados en tiempo real por redes neuronales convolucionales para guiar el auto y frenar ante peatones.

### 7. ¿Qué es DevOps?
Es una cultura organizacional y un conjunto de prácticas de ingeniería que derriba la barrera histórica entre los equipos que escriben el software (**Dev**elopment) y los equipos encargados de mantener los servidores e infraestructura (**Op**erations).

Su objetivo es acortar el ciclo de vida del desarrollo, pasando de desplegar software dos veces al año a liberar actualizaciones seguras y continuas varias veces al día.

### 8. ¿Qué problema busca resolver DevOps?
Resuelve el clásico choque tóxico de responsabilidades: los desarrolladores terminaban una función y decían *"en mi máquina funciona, si falla en el servidor es problema del equipo de infraestructura"*; mientras los de operaciones se resistían a cualquier cambio porque cada despliegue ponía en riesgo la estabilidad del servidor.

DevOps unifica la responsabilidad: los desarrolladores asumen el comportamiento de su código en producción, y el equipo de operaciones colabora desde el día uno automatizando el aprovisionamiento de entornos idénticos de prueba y producción.

### 9. ¿Por qué es importante la integración entre desarrollo y operaciones?
Porque la velocidad de entrega en el mercado actual exige automatización absoluta. Mediante canalizaciones CI/CD (*Continuous Integration / Continuous Delivery*), cada cambio aprobado en el repositorio se compila, pasa pruebas automáticas y se despliega en producción sin manipulación manual propensa a errores.

Esto elimina los fallos de configuración humana, reduce el tiempo medio de recuperación ante caídas (MTTR) y asegura que las aplicaciones operen de manera predecible.

### 10. ¿Cómo influyen estas tecnologías en el futuro del software?
Están redefiniendo la frontera del desarrollo: el software ya no es un programa estático instalado en un disco duro, sino un ecosistema vivo, distribuido y adaptativo. 

Un sistema moderno combina microservicios en la nube, ingesta de telemetría desde sensores IoT, inferencia de modelos de inteligencia artificial en el borde (*Edge AI*) y despliegues automatizados mediante DevOps. El ingeniero de software del futuro debe pensar de forma holística: dominar la lógica de código tanto como la infraestructura, los datos y la seguridad.

---

## IX. Arquitectura de computación

### 1. ¿Qué es la arquitectura de la computación?
Es el diseño conceptual, la estructura lógica y el modelo operativo que define cómo interactúan los componentes funcionales de un computador para ejecutar programas.

Determina cómo se comunican la CPU, los buses de datos, los registros y los subsistemas de memoria, estableciendo el conjunto de instrucciones (ISA - *Instruction Set Architecture* como x86 o ARM) que el hardware entiende y pone a disposición de los compiladores y sistemas operativos.

### 2. ¿Qué componentes forman parte de la arquitectura de un computador?
Bajo el modelo clásico de Von Neumann y sus extensiones modernas, los componentes fundamentales son:
- **Unidad Central de Procesamiento (CPU):** Conformada por la Unidad de Control (UC), la Unidad Aritmético-Lógica (ALU) y el banco de registros internos.
- **Subsistema de Memoria:** Memoria primaria (RAM/ROM) y jerarquía de cachés (L1, L2, L3).
- **Sistema de Buses:** Bus de datos, bus de direcciones y bus de control por donde viajan las señales y voltajes.
- **Subsistema de Entrada/Salida (E/S):** Controladores, puertos y dispositivos periféricos que comunican al computador con el exterior.

### 3. ¿Qué función cumple el procesador (CPU)?
La CPU es el motor de cálculo y control del sistema. Su trabajo se resume en el ciclo ininterrumpido de **Búsqueda, Decodificación y Ejecución** (*Fetch-Decode-Execute*):
1. **Fetch:** Trae la siguiente instrucción almacenada en memoria RAM apuntada por el contador de programa (*Program Counter*).
2. **Decode:** La Unidad de Control interpreta qué operación matemática, lógica o movimiento de datos exige esa instrucción binaria.
3. **Execute:** La ALU ejecuta el cálculo o activa las compuertas lógicas correspondientes y guarda el resultado en un registro o dirección de memoria.

### 4. ¿Qué función cumple la memoria en un sistema informático?
Cumple la función de espacio de trabajo activo. Almacena temporalmente tanto las instrucciones del programa que la CPU está ejecutando como los datos y variables que esos programas necesitan para operar.

Sin memoria, el procesador no tendría de dónde alimentar su ciclo de instrucciones, ya que la CPU no tiene espacio físico interno para almacenar aplicaciones completas.

### 5. ¿Qué diferencia existe entre memoria principal y memoria secundaria?
- **Memoria Principal (RAM):** Es semiconductora, extremadamente rápida y **volátil**. Pierde absolutamente toda la información en cuanto se corta la corriente eléctrica. La CPU accede a ella de forma directa a través del bus del sistema.
- **Memoria Secundaria (SSD, NVMe, Disco Duro):** Es magnética o de estado sólido (*NAND Flash*), mucho más lenta que la RAM pero **no volátil**. Retiene los datos de forma permanente (archivos, programas instalados, sistema operativo) incluso con el equipo apagado. La CPU no puede ejecutar instrucciones directamente desde el disco; primero debe cargarlas en memoria RAM.

### 6. ¿Qué es la memoria caché?
Es una memoria ultrarrápida y de capacidad reducida construida con tecnología SRAM (*Static RAM*), ubicada dentro del mismo encapsulado del procesador, entre los registros de la CPU y la memoria RAM principal.

Su función es almacenar las instrucciones y datos que el procesador utiliza de forma más frecuente o repetitiva, aprovechando los principios de localidad temporal y espacial. Al consultar primero la caché, la CPU evita esperar los lentos ciclos de acceso a la RAM principal, eliminando cuellos de botella de rendimiento.

### 7. ¿Qué papel cumplen los dispositivos de entrada y salida?
Son el puente de comunicación entre el mundo analógico exterior y el entorno binario de la computadora:
- **Dispositivos de Entrada (Teclado, ratón, micrófonos, cámaras, sensores):** Convierten estímulos físicos y acciones humanas en trenes de pulsos digitales comprensibles para el sistema operativo.
- **Dispositivos de Salida (Pantallas, monitores, altavoces, actuadores):** Toman los resultados binarios procesados por la máquina y los traducen a representaciones visuales, sonoras o mecánicas comprensibles para las personas.

### 8. ¿Cómo interactúa el software con el hardware?
La interacción ocurre a través de una jerarquía estricta de capas de abstracción:
1. El software de aplicación realiza una solicitud (por ejemplo, escribir un archivo).
2. La aplicación invoca una llamada al sistema (*syscall*) dirigida al núcleo del sistema operativo (Kernel).
3. El Kernel verifica los permisos de seguridad y delega la orden al **controlador de dispositivo (*driver*)** correspondiente.
4. El *driver* escribe en los registros de control de hardware del dispositivo mediante interrupciones de hardware (*IRQs*) o acceso directo a memoria (*DMA*), activando los voltajes físicos en el bus.

### 9. ¿Por qué es importante comprender la arquitectura de computación para desarrollar software?
Porque el software no corre en un vacío teórico; corre sobre silicio real con restricciones físicas. 

Un ingeniero que desconoce la jerarquía de memoria escribe código que provoca constantes fallos de caché (*cache misses*), ralentizando el sistema cien veces más de lo necesario. Entender la arquitectura permite optimizar la concurrencia multihilo, evitar condiciones de carrera, aprovechar instrucciones vectoriales (SIMD) y escribir programas eficientes en consumo de recursos energéticos y de memoria.

### 10. ¿Qué avances han ocurrido en la arquitectura de los computadores?
- **Procesadores multinúcleo y heterogéneos:** Transición de un solo núcleo rápido a múltiples núcleos coordinados, combinando núcleos de alto rendimiento con núcleos de alta eficiencia energética (arquitecturas ARM big.LITTLE / Apple Silicon).
- **Aceleradores dedicados (GPUs, TPUs, NPUs):** Procesamiento masivamente paralelo optimizado para operaciones matriciales y tensores de inteligencia artificial.
- **Arquitecturas abiertas (RISC-V):** Un conjunto de instrucciones libre y modular que rompe el monopolio de x86 y ARM, permitiendo a universidades e industrias diseñar sus propios chips a la medida.
- **Computación Cuántica:** Salto conceptual de los bits clásicos (0 o 1) a los cúbits con superposición y entrelazamiento cuántico, capaces de resolver problemas criptográficos y de simulación molecular inalcanzables para los supercomputadores actuales.

---

## X. Reflexión, análisis y propuesta

### 1. Analice cómo el software influye en actividades cotidianas como educación, comercio o comunicación.
El software ha reestructurado por completo las dinámicas sociales:
- **Educación:** Permite la existencia de programas universitarios a distancia como el nuestro en la Universidad de Cartagena, donde a través de plataformas virtuales (SIMA) y herramientas de gestión rompemos la barrera geográfica y el horario rígido de aula.
- **Comercio:** Ha democratizado el acceso a mercados globales; cualquier artesano o comerciante local puede vender productos internacionalmente mediante una tienda web y pasarelas de pago instantáneas como PSE, Transfiya o Nequi.
- **Comunicación:** Ha eliminado la distancia física en tiempo real; los canales de chat encriptados, videollamadas y protocolos descentralizados permiten coordinar trabajo colaborativo internacional al instante.

### 2. Proponga un ejemplo de problema cotidiano que podría resolverse con un sistema de software.
En muchas ciudades de la región Caribe colombiana, el transporte público colectivo (buses y busetas) opera sin trazabilidad de rutas ni horarios predecibles. Los usuarios gastan entre 40 y 60 minutos esperando bajo el sol en esquinas sin saber si la ruta ya pasó, si viene llena o a qué distancia se encuentra.

Este problema puede resolverse mediante un **Sistema Inteligente de Monitoreo de Rutas Urbanas**: una plataforma móvil y web respaldada por módulos GPS de bajo costo instalados en los buses, que transmite en tiempo real la ubicación y velocidad al servidor. El usuario consulta en su teléfono una aplicación ligera que le indica con precisión cuántos minutos faltan para que el bus llegue al paradero, la ocupación estimada y el valor del pasaje.

### 3. Imagine que debe diseñar un sistema informático para su universidad. ¿Qué problema resolvería?
Diseñaría el **Sistema Unificado de Gestión de Espacios Académicos y Reserva de Laboratorios (SUGAR-UDC)** para la Sede Piedra de Bolívar y el Claustro de San Agustín.

Actualmente, el préstamo de salas de informática (como las salas de informática del Bloque F y laboratorios del Bloque G) y la reserva de aulas para asesorías de CIPAS o tutorías extraordinarias se realiza mediante trámites en papel o planillas dispersas. Esto genera choques de horarios entre asignaturas, salas vacías subutilizadas por falta de aviso y pérdida de tiempo para los estudiantes que necesitan un espacio con buena conectividad para trabajar entre clases.

### 4. ¿Qué funcionalidades debería tener ese sistema?
- **Catálogo interactivo de espacios físicos:** Mapa en tiempo real de la sede indicando disponibilidad, número de puestos, tomas de corriente y equipos instalados.
- **Módulo de reservas para CIPAS:** Autenticación institucional para que los grupos de estudio reserven cubículos o salas por bloques de 1 a 2 horas.
- **Control de acceso mediante código QR / Carnet estudiantil:** Validación automática de ingreso en la puerta de la sala.
- **Monitoreo de inventario y reporte de incidencias:** Opción para que el estudiante o docente reporte de inmediato si un teclado, monitor o punto de red presenta fallas, alertando al área de soporte técnico.
- **Métricas de ocupación:** Panel de administración (*dashboard*) para que la coordinación académica analice qué bloques y horarios presentan mayor saturación.

### 5. ¿Qué tipo de usuarios utilizarían ese sistema?
1. **Estudiantes:** Para consultar disponibilidad de salas, reservar espacios de trabajo para sus CIPAS y reportar novedades de hardware.
2. **Docentes:** Para agendar prácticas de laboratorio, talleres evaluativos y tutorías de acompañamiento sincrónico o presencial.
3. **Monitores y Administradores de Laboratorio:** Para validar el ingreso, controlar el inventario de máquinas e inspeccionar el estado de los periféricos.
4. **Coordinación de Programa y Decanatura:** Para tomar decisiones de inversión en infraestructura con base en datos reales de uso.

### 6. ¿Qué dispositivos utilizarían los usuarios para interactuar con el sistema?
- **Teléfonos inteligentes (Android / iOS):** Mediante una aplicación web progresiva (PWA) optimizada y rápida donde los estudiantes consultan y reservan sobre la marcha.
- **Computadores portátiles y de escritorio (Linux / Windows / Mac):** A través del navegador web institucional para labores administrativas y docentes.
- **Tablets o terminales fijas táctiles:** Instaladas a la entrada de los bloques F y G para registro rápido de entrada y salida mediante escáner óptico.

### 7. ¿Qué periféricos o sistemas de entrada serían necesarios?
- **Lectores ópticos de códigos de barras y QR:** Para escanear el carnet institucional físico o digital desde la pantalla del celular.
- **Cámaras web / Terminales de escaneo:** Para reconocimiento y validación biométrica en salas de servidores o laboratorios especializados.
- **Teclados, ratones y pantallas táctiles:** En los puntos de autoservicio para consulta de horarios y disponibilidad.
- **Sensores de presencia IoT (infrarrojos pasivos PIR):** En cada aula para detectar automáticamente si el espacio reservado está siendo ocupado o si quedó libre por inasistencia.

### 8. ¿Qué tecnologías podrían utilizarse para desarrollar ese sistema?
- **Backend y Lógica de Negocio:** Una arquitectura desacoplada basada en microservicios o modular monolito construida con Go (Golang) o Java Spring Boot por su alta concurrencia y bajo consumo de memoria.
- **Frontend y Capa de Presentación:** Interfaz web desarrollada con TypeScript y un framework reactivo (React o Svelte) empaquetada como Progressive Web App (PWA) con diseño accesible y ligero para conexiones móviles universitarias.
- **Bases de Datos:** PostgreSQL para la persistencia relacional transaccional (usuarios, reservas, horarios) y Redis como almacén en memoria para gestionar bloqueos concurrentes y sesiones activas en tiempo real.
- **Infraestructura y Despliegue:** Contenedores Docker orquestados con Kubernetes en servidores propios o en la nube, con canalizaciones automatizadas CI/CD mediante GitHub Actions.

### 9. ¿Qué habilidades debe desarrollar un estudiante para convertirse en ingeniero de software?
- **Bases matemáticas y pensamiento algorítmico formal:** Capacidad de descomponer problemas complejos en pasos lógicos rigurosos, analizar la complejidad temporal/espacial y modelar soluciones abstractas antes de tocar el teclado.
- **Fundamentos sólidos de arquitectura y diseño limpio:** Comprensión profunda de patrones de diseño, principios SOLID, cohesión, bajo acoplamiento y modelado de datos antes de casarse con cualquier framework de moda.
- **Habilidades de comunicación y empatía:** Saber escuchar activamente al usuario, negociar requerimientos y explicar conceptos técnicos a clientes sin formación en sistemas.
- **Disciplina de trabajo en equipo y control de versiones:** Manejo avanzado de Git, revisiones de código cruzadas (*pull requests*), documentación técnica clara y metodologías ágiles.
- **Curiosidad y aprendizaje autodidacta continuo:** La tecnología evoluciona a un ritmo vertiginoso; la habilidad de leer documentación técnica en inglés, experimentar con nuevas herramientas y aprender por cuenta propia es la que define la longevidad profesional.

### 10. Desde su perspectiva como estudiante que inicia la carrera, ¿cómo cree que la ingeniería de software contribuirá al desarrollo de la sociedad en el futuro?
La ingeniería de software será la disciplina que articule las soluciones a los retos más críticos de nuestra civilización. 

En un país como Colombia y en nuestra región Caribe, el software no debe verse solo como una fuente de empleo corporativo, sino como una herramienta de equidad y transformación social. Mediante sistemas eficientes podemos optimizar la distribución de recursos en hospitales públicos, monitorear la calidad del agua en comunidades rurales, transparentar la contratación estatal eliminando la corrupción y modernizar los sistemas productivos locales. 

Como ingenieros de software en formación, no solo aprendemos a programar máquinas; asumimos la responsabilidad ética de diseñar sistemas seguros, éticos y accesibles que mejoren la calidad de vida de las personas y empujen el desarrollo de nuestra sociedad.

---

## Referencias Bibliográficas

- Comer, D. E. (2015). *Redes de computadoras e Internet* (6.ª ed.). Pearson Educación.
- Fowler, M. (2018). *Refactoring: Improving the Design of Existing Code* (2.ª ed.). Addison-Wesley.
- Incencio Piñeiro, E., et al. (2022). *Dimensión Construcción Lógica en Ingeniería de Software*. Revista Científica EBSCO.
- Martin, R. C. (2017). *Clean Architecture: A Craftsman's Guide to Software Structure and Design*. Prentice Hall.
- Ortiz Campos, F. J., & Ortiz Cerecedo, F. J. (2019). *Cálculo diferencial* (3.ª ed.). Grupo Editorial Patria.
- Patterson, D. A., & Hennessy, J. L. (2018). *Computer Organization and Design: The Hardware/Software Interface* (RISC-V Edition). Morgan Kaufmann.
- Pressman, R. S. (2010). *Ingeniería del software: un enfoque práctico* (7.ª ed.). McGraw-Hill Interamericana.
- Sommerville, I. (2011). *Ingeniería de software* (9.ª ed.). Pearson Educación.
- Weber, R. (2020). *Fundamentos de informática y arquitectura de computadores*. Editorial eLibro.

---
