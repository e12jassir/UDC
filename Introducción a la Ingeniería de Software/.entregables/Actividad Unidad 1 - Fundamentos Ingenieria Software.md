# Cuestionario de Conceptualización Fundamental sobre Bases Teóricas de la Carrera

Programa Académico: Ingeniería de Software
Asignatura: Introducción a la Ingeniería de Software (IX24014-A1)
Docente: Jhon Carlos Arrieta Arrieta
Institución: Universidad de Cartagena, Facultad de Ingeniería
Fecha: Septiembre de 2026

Subgrupo CIPAS:
Estudiante: Esteban David Marrugo Jassir (Código: 7502620036)
Enlace de Video de Sustentación Individual: https://drive.google.com/file/d/1LYkn41Nbq8P3lyiO0KVQL7IRjr-4IKhE/view?usp=drive_link

## I. Comprensión básica de la ingeniería de software

### 1. ¿Qué entiende por ingeniería de software?
Para mí, la ingeniería de software es aplicar métodos sistemáticos, herramientas científicas y criterios de diseño para crear sistemas computacionales confiables y fáciles de mantener con los años. Escribir código que funcione en la computadora de uno es relativamente sencillo. La dificultad real aparece cuando ese sistema entra a producción, atiende a miles de personas en simultáneo, cambia según nuevas reglas operativas y lo mantiene un equipo donde los desarrolladores rotan. Es la diferencia entre armar una choza improvisada en el patio y levantar un edificio con cálculo estructural, planos y normas sísmicas.

### 2. ¿Cuál es el objetivo principal de la ingeniería de software?
El objetivo central es superar los problemas de la crisis del software: entregar sistemas que realmente solucionen las necesidades del usuario, dentro del plazo y presupuesto acordados, con estabilidad técnica. En el trabajo diario, esto se traduce en evitar fallas costosas en producción y reducir el gasto de mantenimiento futuro, que suele superar el 60% del costo total de un desarrollo. El software debe poder modificarse sin obligar al equipo a rehacerlo desde cero cada vez que el entorno cambie.

### 3. ¿Qué diferencia existe entre software y hardware?
El hardware es la parte física y tangible: procesadores de silicio, circuitos, pistas de cobre, memorias y periféricos. Se desgasta con la temperatura, sufre fallas mecánicas y exige procesos de manufactura física.
El software es la parte lógica e intangible: instrucciones, algoritmos y estructuras de datos organizados para procesar información. El software no sufre fricción física ni desgaste por uso; envejece cuando queda obsoleto frente a nuevos sistemas, cuando acumula parches desordenados o cuando pierde compatibilidad. Cambiar el hardware implica reemplazar componentes físicos, mientras que el software es maleable, una flexibilidad que exige disciplina para no terminar en desorden.

### 4. ¿Por qué ambos deben trabajar de manera integrada?
Son dos partes inseparables de una misma máquina. Un procesador sin instrucciones en memoria no pasa de ser silicio que consume energía sin hacer nada útil. Del mismo modo, el mejor algoritmo queda en el papel si no hay circuitos físicos que ejecuten ciclos de reloj y cambien estados lógicos.
Esta integración permite que el software aproveche la arquitectura física (registros del procesador, hilos de ejecución o buses de datos) y que el hardware ofrezca aislamiento de memoria y control de interrupciones para evitar fallos catastróficos.

### 5. ¿Qué es un sistema informático?
Es un conjunto coordinado de hardware, software, datos y personas que siguen procedimientos definidos para capturar, procesar, almacenar y distribuir información.
No se limita a la computadora personal que tenemos en el escritorio. Abarca desde un lector de código de barras conectado a un servidor de inventario hasta la plataforma distribuida que gestiona las matrículas y notas de la universidad.

### 6. ¿Qué componentes conforman un sistema informático?
Un sistema informático integra cuatro componentes básicos:
- Hardware: la infraestructura física, como procesadores, memoria RAM, discos de estado sólido y tarjetas de red.
- Software: los programas del sistema, desde el sistema operativo y controladores hasta los gestores de bases de datos y aplicaciones de usuario.
- Datos e información: la materia prima que entra al sistema, se organiza en estructuras lógicas y genera reportes o acciones tras procesarse.
- Factor humano y protocolos: los usuarios que operan el sistema, los administradores que lo mantienen y los procedimientos que indican cómo debe fluir la información.

### 7. ¿Qué papel cumple el software dentro de un sistema informático?
El software actúa como el coordinador y cerebro del sistema. Recibe los datos que entran por los periféricos, ejecuta la lógica de negocio mediante algoritmos, gestiona el almacenamiento en disco y devuelve resultados útiles en pantalla.
Sin software, el hardware carece de instrucciones. Es la capa lógica que traduce el lenguaje de voltajes y compuertas electrónicas en interfaces claras, servicios web y herramientas de trabajo diario.

### 8. ¿Qué tipos de software existen? Describa al menos tres.
Podemos clasificarlos en tres grupos según su función:
- Software de sistema: controla los recursos físicos del equipo y da soporte a los demás programas. Incluye sistemas operativos como Linux o FreeBSD, controladores de dispositivos y sistemas de archivos.
- Software de programación: comprende las herramientas que usamos los desarrolladores para construir aplicaciones, tales como compiladores (GCC, Clang), intérpretes (Python), depuradores (GDB) y editores de texto.
- Software de aplicación: reúne los programas diseñados para tareas concretas del usuario final, como navegadores web, procesadores de texto, clientes de correo y sistemas bancarios.

### 9. ¿Por qué el software es fundamental en la sociedad actual?
Porque la operación básica de los servicios esenciales depende de programas informáticos. Las redes eléctricas, el suministro de agua, los historiales clínicos en hospitales, las torres de control aéreo y las transacciones bancarias funcionan mediante código que debe operar de forma ininterrumpida. Si estos sistemas fallan durante unas horas, el transporte se frena, las comunicaciones caen y la atención médica de urgencia entra en crisis.

### 10. ¿Qué ejemplos de software utiliza diariamente?
En mi rutina de estudio y trabajo técnico utilizo herramientas puntuales:
- Arch Linux como sistema operativo principal, configurado a medida para optimizar el rendimiento de mi portátil.
- Ghostty y Bash para interactuar con la línea de comandos, gestionar procesos y automatizar tareas.
- Neovim para programar y Obsidian para organizar mis notas académicas en Markdown.
- Zen Browser para consultar documentación técnica, repositorios y el campus virtual SIMA de la universidad.
- Git y GitHub para el control de versiones y el respaldo de mis proyectos.

## II. Ingeniería de software como disciplina

### 1. ¿Por qué el desarrollo de software requiere un enfoque de ingeniería?
Porque los sistemas de software modernos son demasiado complejos para abordarse mediante intuición o pruebas al azar. Cuando un programa pasa de unos cientos de líneas a miles de instrucciones repartidas en varios módulos, nadie puede recordar cada detalle de memoria.
El enfoque de ingeniería aporta método y control. Permite estimar costos reales, evaluar riesgos de seguridad, especificar requisitos y realizar pruebas metódicas antes del despliegue, tal como la ingeniería civil calcula cargas para evitar que un puente colapse con el tráfico.

### 2. ¿Qué diferencia existe entre programar y desarrollar software?
Programar es el acto puntual de escribir código en un lenguaje específico para resolver un algoritmo o tarea concreta mediante variables, bucles y funciones.
Desarrollar software con criterio de ingeniería cubre todo el ciclo de vida: entender las necesidades del usuario, negociar alcances, diseñar la arquitectura del sistema, planificar bases de datos, programar con pruebas automatizadas, desplegar en servidores y mantener el producto con los años. La programación es solo una etapa dentro de un proceso de desarrollo mucho más amplio.

### 3. ¿Qué problemas pueden surgir si el software se desarrolla sin planificación?
El resultado típico es el desorden técnico y el fracaso operativo:
- Código enredado: cada cambio para corregir un fallo genera tres problemas nuevos en partes distantes del sistema.
- Sobrecostos y entregas tardías: al no definir alcances claros, el equipo repite trabajo innecesario y agota el presupuesto antes de terminar.
- Productos inservibles: se entrega un programa que funciona bien técnicamente pero no resuelve la necesidad real del usuario.
- Abandono prematuro: cuando el código se vuelve incomprensible, corregir errores cuesta tanto que resulta más barato tirar todo a la basura.

### 4. ¿Qué etapas suelen existir en el desarrollo de software?
Con variaciones según la metodología elegida, las etapas básicas son:
- Análisis de requisitos: identificar con claridad qué problema se busca resolver y bajo qué restricciones.
- Diseño del sistema: definir la arquitectura, el modelo de datos y las interfaces entre módulos.
- Implementación: escribir el código fuente respetando estándares limpios y pruebas locales.
- Pruebas y validación: ejecutar pruebas unitarias, de integración y de seguridad para detectar defectos antes del lanzamiento.
- Despliegue: poner el software en los servidores de producción para que los usuarios puedan utilizarlo.
- Mantenimiento: corregir errores reportados, aplicar parches de seguridad y agregar funciones cuando cambien las reglas del negocio.

### 5. ¿Por qué es importante analizar los requisitos antes de programar?
Porque corregir una mala interpretación durante el análisis cuesta una fracción mínima de lo que cuesta arreglarla con el software ya en producción. Si un requisito se define mal al inicio, toda la arquitectura, las tablas de base de datos y los módulos de código se construyen sobre una base equivocada.
El análisis previo aterriza expectativas, define límites claros y evita que el equipo pierda semanas programando funciones que nadie necesita.

### 6. ¿Qué sucede cuando los requisitos de un sistema no están claros?
Aparece el desvío descontrolado del alcance (scope creep). El cliente solicita cambios constantes semana a semana porque nunca se formalizó qué debía incluir el producto y qué quedaba fuera.
Esto genera frustración en el equipo de desarrollo, atrasos sistemáticos en las fechas de entrega y un código repleto de parches apresurados. Al final, el cliente siente que gastó dinero en algo inútil y el equipo queda con un sistema frágil que nadie se atreve a modificar.

### 7. ¿Por qué es importante documentar un sistema de software?
El código muestra cómo funciona una instrucción, pero la documentación aclara por qué se tomaron ciertas decisiones de diseño. En el sector tecnológico, los programadores cambian de empresa o de proyecto con frecuencia.
Si un sistema no deja diagramas de arquitectura, especificaciones de APIs y manuales de instalación, quien llegue a mantenerlo perderá semanas deduciendo la lógica a ciegas. Documentar con claridad garantiza que el conocimiento del proyecto permanezca dentro del equipo.

### 8. ¿Qué papel cumple el análisis en el desarrollo de software?
El análisis responde a la pregunta de qué debe hacer el sistema. Su función es descomponer el problema del usuario en casos de uso, flujos de trabajo y reglas operativas, sin atarse todavía a un lenguaje de programación específico ni a un motor de base de datos.
Es el filtro técnico que toma las peticiones informales de los usuarios y las traduce en especificaciones precisas para el equipo de desarrollo.

### 9. ¿Qué papel cumple el diseño en el desarrollo de software?
El diseño responde a la pregunta de cómo se va a construir la solución. En esta etapa se deciden la estructura de módulos, los patrones arquitectónicos, el esquema de bases de datos y los protocolos de comunicación entre servicios. Un diseño adecuado previene la rigidez del código y asegura que el sistema pueda crecer de forma ordenada a medida que aumente la carga de usuarios.

### 10. ¿Qué importancia tienen las pruebas dentro del desarrollo de software?
Las pruebas verifican de forma objetiva que el sistema cumple con lo especificado y que tolera entradas inesperadas sin colapsar.
Cuando no existen pruebas automatizadas (unitarias, de integración y de carga), cada actualización a producción se convierte en una apuesta arriesgada donde los usuarios finales terminan encontrando los errores críticos. Probar el código es una disciplina continua que da confianza para refactorizar y mejorar el sistema a diario.

## III. Principios fundamentales de la ingeniería de software

### 1. ¿Qué significa abstracción en el desarrollo de software?
Es la técnica de enfocarse en las propiedades esenciales de un componente, dejando de lado los detalles operativos de bajo nivel que no hacen falta para el problema actual.
En la práctica, cuando usamos una función como `guardar_archivo()`, nos interesa almacenar la información; no necesitamos saber cómo el sistema operativo reparte los sectores en el disco de estado sólido ni cómo interactúa con el bus del sistema.

### 2. ¿Por qué la abstracción ayuda a manejar la complejidad?
Porque la mente humana tiene una capacidad de atención limitada y no puede controlar millones de variables técnicas simultáneamente.
La abstracción permite estructurar el software en capas lógicas independientes. Un programador web puede construir una plataforma de pagos usando HTTP y JSON sin tener que preocuparse por la modulación de señales en la fibra óptica. Sin abstracción, crear software moderno sería inviable.

### 3. ¿Qué es modularidad?
Es el principio de descomponer un sistema grande en partes más pequeñas, autónomas y bien delimitadas llamadas módulos. Cada módulo agrupa funciones relacionadas y se comunica con el exterior únicamente a través de interfaces definidas.
En lugar de tener un único archivo gigante con miles de líneas donde todo se cruza, el sistema se organiza en bloques claros: autenticación, facturación, notificaciones y reportes.

### 4. ¿Por qué dividir un sistema en módulos facilita su desarrollo?
La modularidad agiliza el trabajo por varias razones:
- Trabajo paralelo: varios desarrolladores pueden avanzar al mismo tiempo en módulos distintos sin generar conflictos constantes en el repositorio de código.
- Localización de errores: si falla el cálculo de un descuento, el equipo revisa puntualmente el módulo de cobros sin tener que rastrear todo el proyecto.
- Reutilización: un módulo bien resuelto, como el envío de correos o la autenticación por tokens, puede aprovecharse en proyectos futuros sin cambios mayores.

### 5. ¿Qué es la separación de responsabilidades?
Es un principio formulado por Edsger Dijkstra que establece que cada componente de un sistema debe atender una sola tarea o aspecto funcional bien delimitado.
El ejemplo tradicional es la arquitectura en tres capas: la presentación solo dibuja la interfaz gráfica; la lógica de negocio procesa las reglas y cálculos; y la capa de datos solo gestiona la comunicación con la base de datos. Ninguna capa interfiere en las funciones de las demás.

### 6. ¿Por qué es importante dividir las funciones de un sistema?
Porque cuando una sola clase o función asume múltiples tareas (valida datos, calcula nómina y guarda en disco), cualquier ajuste en la estructura de la base de datos termina dañando la interfaz de usuario.
Dividir funciones reduce drásticamente los efectos colaterales. Hace que el código sea más legible para los nuevos miembros del equipo y permite sustituir tecnologías con menor riesgo, como cambiar de base de datos sin tocar la lógica de negocio.

### 7. ¿Qué es el ocultamiento de información?
Es el principio introducido por David Parnas que indica que cada módulo debe resguardar sus detalles internos de implementación, algoritmos y estructuras de datos, dejando visible hacia el exterior únicamente una interfaz pública limpia.
Los módulos externos conocen qué servicios ofrece ese componente, pero no tienen acceso a su lógica interna.

### 8. ¿Cómo contribuye el ocultamiento de información a la seguridad del software?
Protege los datos internos frente a modificaciones accidentales o indebidas desde otros puntos del programa. Si una cuenta bancaria mantiene su variable de saldo como privada y solo permite actualizarla mediante funciones controladas como `depositar()` o `retirar()`, se asegura que nadie pueda asignar un saldo negativo saltándose las validaciones.
Además, protege al sistema ante cambios técnicos: si luego decidimos cambiar una lista interna por un árbol binario para optimizar búsquedas, los demás módulos siguen funcionando sin enterarse, pues la interfaz pública permanece intacta.

### 9. ¿Qué es la cohesión en un componente de software?
La cohesión mide el grado de afinidad y concentración que tienen los métodos y variables dentro de un mismo módulo o clase.
Un componente tiene alta cohesión cuando todos sus elementos cooperan para cumplir un único objetivo bien delimitado. En cambio, presenta baja cohesión si acumula funciones dispersas que no guardan relación entre sí, como ocurre en las típicas clases comodín llamadas `Utilidades` o `Varios`.

### 10. ¿Por qué es deseable que un módulo tenga alta cohesión?
Porque un módulo con una responsabilidad clara resulta mucho más fácil de comprender, probar y reutilizar.
Al concentrarse en una sola función, sus métodos comparten datos internos con naturalidad, las pruebas unitarias se escriben rápido y el componente rara vez cambia por motivos ajenos a su especialidad.

## IV. Acoplamiento y diseño de sistemas

### 1. ¿Qué significa acoplamiento entre módulos?
El acoplamiento mide el grado de dependencia mutua que existe entre dos o más módulos de un programa. Describe qué tan conectado está un módulo A con los detalles internos de un módulo B.
Si el módulo de pedidos necesita leer directamente las variables privadas del módulo de clientes para operar, existe un acoplamiento fuerte. Si en cambio solo intercambian identificadores básicos mediante interfaces bien definidas, el acoplamiento es débil.

### 2. ¿Por qué el acoplamiento bajo es deseable?
Porque da libertad para evolucionar el código. Cuando los módulos están poco acoplados, podemos refactorizar, optimizar o rehacer por completo la lógica interna de uno de ellos sin que los demás módulos fallen o dejen de compilar.
Además, el acoplamiento bajo simplifica las pruebas: podemos validar el cálculo de facturas usando datos simulados sin necesidad de conectar una base de datos real en cada prueba.

### 3. ¿Qué problemas aparecen cuando el acoplamiento es alto?
Aparece el temido efecto dominó. Un pequeño cambio en el formato de fecha dentro del módulo de usuarios puede romper de forma imprevista el generador de reportes y la pasarela de pagos.
El acoplamiento alto genera sistemas quebradizos y rígidos, donde modificar una función exige tocar decenas de archivos en cadena, impidiendo además reutilizar piezas de código en otros desarrollos sin arrastrar medio sistema detrás.

### 4. ¿Cómo influyen estos principios en la calidad del software?
La combinación de alta cohesión y bajo acoplamiento es la regla central del buen diseño. Cuando un sistema se construye bajo estas pautas, su calidad mejora de forma directa:
- Mantenibilidad: encontrar y reparar un error toma minutos en vez de días de búsqueda a ciegas.
- Escalabilidad: permite desacoplar módulos con alto consumo y convertirlos en servicios independientes que corren en servidores dedicados.
- Testabilidad: cada componente puede verificarse de forma aislada mediante pruebas automatizadas rápidas.
- Vida útil: el sistema puede actualizarse a lo largo de los años sin degradarse hasta volverse inservible.

### 5. Proponga un ejemplo de sistema donde sea importante dividir el software en módulos.
El sistema de gestión académica de la Universidad de Cartagena es un caso claro. Si la plataforma fuera un solo bloque monolítico de código, las jornadas de matrícula financiera saturarían el servidor y los docentes no podrían registrar notas ni los estudiantes consultar sus materias.
Al dividir el sistema en módulos independientes:
- Admisiones y registro gestiona datos personales y matrículas académicas.
- Módulo financiero liquida pagos y concilia con los bancos.
- Control académico almacena notas y emite certificados.
- Aula virtual sostiene foros y entrega de tareas.
Cada módulo atiende su propio dominio y, si la pasarela de pagos experimenta saturación temporal, los estudiantes pueden seguir accediendo a sus clases virtuales sin interrupción.

### 6. ¿Cómo puede facilitar la modularidad el mantenimiento del software?
Facilita el mantenimiento porque reduce el área de impacto de cualquier falla. Si los estudiantes reportan que el certificado de notas sale con un error en el cálculo del promedio acumulado, el desarrollador no necesita revisar todo el sistema; acude directamente al módulo de control académico.
También permite sustituciones limpias de proveedores. Si la universidad decide cambiar el proveedor de pasarela de pago, solo se actualiza el adaptador del módulo financiero, dejando el resto de la plataforma intacto.

### 7. ¿Por qué es importante que un sistema pueda modificarse con facilidad?
Porque el software modela actividades humanas y de negocio que están en constante cambio. Las normas tributarias varían, los reglamentos académicos se actualizan y las necesidades de los usuarios evolucionan mes a mes.
Un sistema rígido pierde utilidad con rapidez. Si implementar un ajuste sencillo toma seis meses y cuesta una cifra desmedida en horas de desarrollo, la organización termina descartando el software y buscando alternativas externas.

### 8. ¿Qué relación existe entre diseño y mantenimiento del software?
Existe una relación directa y verificable: la calidad del diseño inicial determina el costo y la dificultad del mantenimiento futuro.
El mantenimiento consume la mayor parte del presupuesto a lo largo de la vida de un sistema. Si en el diseño se toman atajos técnicos por entregar con prisa, cada nuevo requerimiento será más costoso y peligroso de implementar. Dedicar tiempo a un diseño ordenado y desacoplado garantiza que las modificaciones futuras sean viables y económicas.

### 9. ¿Qué impacto tiene un mal diseño en un sistema informático?
Un mal diseño perjudica tanto la estabilidad técnica como la rentabilidad de las organizaciones. En el plano técnico, genera fugas de memoria, lentitud en consultas, bloqueos por concurrencia y vulnerabilidades de seguridad. En el plano del equipo de trabajo, desmotiva a los desarrolladores, que gastan sus jornadas apagando incendios en un código inmanejable, y provoca pérdidas económicas cuando las plataformas caen en momentos de alta demanda.

### 10. ¿Cómo puede un buen diseño mejorar la vida útil del software?
Un buen diseño protege al sistema frente a la obsolescencia técnica. Al mantener la lógica de negocio desacoplada de herramientas específicas como librerías, frameworks o motores de bases de datos, es posible actualizar dependencias, migrar a servidores en la nube o renovar la interfaz de usuario sin tener que rehacer las reglas operativas de la organización.
Los sistemas bien diseñados pueden operar durante décadas con actualizaciones incrementales sin requerir demoliciones completas de código.

## V. Modelos de desarrollo de software

### 1. ¿Qué es un modelo de desarrollo de software?
Es una guía estructurada que organiza las actividades, etapas, roles y entregables necesarios para construir un sistema de software desde su concepción inicial hasta su salida de servicio.
Un modelo establece la forma de trabajo del equipo: indica qué tareas deben completarse primero, qué condiciones permiten avanzar de etapa, cómo se verifican los avances y cómo se gestionan los cambios durante el proyecto.

### 2. ¿Por qué se utilizan modelos en el desarrollo de software?
Porque desarrollar sistemas informáticos exige coordinar diferentes perfiles técnicos, presupuestos y tiempos bajo condiciones de incertidumbre. Sin un modelo formal, el trabajo se vuelve caótico e improvisado.
Los modelos aportan un marco común de trabajo: permiten planificar entregas, estimar recursos con datos objetivos, evaluar la calidad en puntos de control específicos y ofrecer transparencia a los usuarios sobre el estado real del proyecto.

### 3. ¿En qué consiste el modelo en cascada?
Propuesto formalmente por Winston Royce en 1970, el modelo en cascada es un enfoque secuencial donde el avance fluye en una sola dirección a través de fases ordenadas.
Su regla principal es que cada etapa debe completarse y aprobarse documentalmente antes de pasar a la siguiente. No se empieza a programar hasta contar con los documentos de diseño aprobados, y las pruebas generales no inician hasta que la codificación completa del sistema esté terminada.

### 4. ¿Qué etapas incluye el modelo en cascada?
En su planteamiento clásico comprende cinco fases consecutivas:
- Levantamiento y análisis de requisitos: recopilación detallada de lo que el sistema debe hacer, congelando las especificaciones en documentos formales.
- Diseño del sistema: estructuración de la arquitectura general, bases de datos y módulos lógicos.
- Implementación y codificación: escritura del código fuente y pruebas de módulos individuales según las especificaciones previas.
- Integración y pruebas: ensamble de todos los componentes y verificación integral del sistema con base en los requisitos acordados.
- Despliegue y mantenimiento: entrega del producto al cliente y resolución de errores que surjan durante su uso cotidiano.

### 5. ¿Qué ventajas tiene el modelo en cascada?
- Claridad de organización: su avance lineal es fácil de entender y de coordinar, con entregables e hitos claros para cada fase.
- Control documental: al exigir revisiones formales antes de avanzar, genera un registro técnico detallado de cada decisión tomada.
- Facilidad de contratación: encaja bien en proyectos donde los contratos exigen un precio cerrado y un alcance fijo desde el primer día.

### 6. ¿Qué limitaciones puede presentar el modelo en cascada?
- Rigidez frente al cambio: asume que los usuarios conocen todas sus necesidades al inicio y que los requisitos se mantendrán estables por meses. En proyectos reales, los usuarios descubren necesidades clave cuando interactúan con pantallas reales.
- Demora en la entrega de valor: el usuario no ve el software funcionando hasta las fases finales. Si hubo un error de interpretación en la primera fase, se detecta un año después con el presupuesto ya comprometido.
- Bloqueos entre etapas: si el análisis se retrasa, los programadores y evaluadores quedan a la espera sin poder avanzar en su parte.

### 7. ¿Qué es el modelo en espiral?
Formulado por Barry Boehm en 1986, el modelo en espiral combina la estructura iterativa con una fuerte orientación hacia la identificación y mitigación de riesgos.
El proyecto avanza en ciclos concéntricos. En cada vuelta de la espiral se determinan objetivos y restricciones, se analizan y mitigan riesgos mediante prototipos rápidos, se construye y valida una versión del software y se planifica la siguiente iteración con la retroalimentación obtenida.

### 8. ¿Qué problema intenta resolver el modelo en espiral?
Busca resolver el punto débil de la cascada: acumular incertidumbre y riesgos no resueltos hasta el final del desarrollo.
En sistemas grandes o con tecnologías novedosas, existen dudas sobre la velocidad de respuesta, la viabilidad de la base de datos o la adaptación de los usuarios. El modelo en espiral ataca estas dudas construyendo prototipos en los primeros ciclos. Si un riesgo técnico resulta insuperable, el proyecto puede ajustarse o detenerse a tiempo sin incurrir en pérdidas millonarias.

### 9. ¿Qué diferencia existe entre modelos tradicionales y metodologías ágiles?
La diferencia radica en su forma de afrontar el cambio y la incertidumbre:
- Modelos tradicionales: son predictivos. Intentan planificar cada detalle con meses de anticipación mediante documentación extensa, contratos cerrados y control estricto de variaciones sobre el plan original.
- Metodologías ágiles: son adaptativas. Trabajan en ciclos cortos de pocas semanas, entregan incrementos de software funcional con frecuencia y priorizan la comunicación directa con el cliente, aceptando los cambios de requisitos como ajustes normales para mejorar el producto.

### 10. ¿En qué situaciones podría ser adecuado utilizar un modelo tradicional?
Los enfoques tradicionales siguen siendo adecuados en escenarios específicos:
- Proyectos con requisitos estables y definidos por ley: por ejemplo, implementar un protocolo bancario internacional estandarizado donde las especificaciones técnicas no admiten variaciones.
- Sistemas críticos donde la seguridad humana está en juego: controles de vuelo en aeronáutica, equipos biomédicos o software para reactores nucleares, donde cada línea de código debe verificarse formalmente bajo normas estrictas de certificación.
- Licitaciones públicas con alcance y presupuesto cerrados: donde las condiciones contractuales exigen cronogramas y entregables definidos antes de adjudicar los fondos.

## VI. Metodologías ágiles

### 1. ¿Qué son las metodologías ágiles?
Son marcos de gestión y desarrollo de software basados en los valores del Manifiesto Ágil de 2001. En lugar de ejecutar planes largos y rígidos, dividen el proyecto en ciclos iterativos de pocas semanas para entregar versiones utilizables de forma continua.
Su dinámica prioriza el trabajo en equipo, la autonomía técnica y la colaboración estrecha con el usuario, ajustando el rumbo según los resultados obtenidos en cada iteración.

### 2. ¿Por qué surgieron las metodologías ágiles?
Nacieron como respuesta al alto porcentaje de fracaso de los métodos burocráticos y pesados en las décadas de 1980 y 1990. En esa época, muchos proyectos gastaban meses redactando manuales y especificaciones teóricas, y cuando el sistema se terminaba años después, los requisitos habían cambiado y el software resultaba inútil.
En 2001, un grupo de referentes de la industria se reunió en Utah y redactó un manifiesto para reorientar el desarrollo hacia lo esencial: entregar software que funcione y genere valor tangible para el usuario.

### 3. ¿Qué características tienen los métodos ágiles?
- Entregas iterativas e incrementales: el software crece en bloques funcionales que se revisan cada una a cuatro semanas.
- Apertura al cambio: los requerimientos pueden ajustarse al comienzo de cada ciclo sin trámites burocráticos destructivos.
- Equipos multidisciplinarios y autónomos: desarrolladores, evaluadores y diseñadores colaboran a diario con capacidad de tomar decisiones técnicas.
- Validación frecuente: cada entrega se demuestra directamente al cliente para incorporar sus observaciones de inmediato.

### 4. ¿Qué es Scrum?
Scrum es el marco ágil más utilizado en el sector para coordinar el desarrollo de productos complejos. Define un conjunto de eventos, artefactos y roles que facilitan la transparencia, la inspección metódica y la adaptación del equipo.
El trabajo se organiza en bloques de tiempo fijos llamados Sprints, donde el equipo se compromete a transformar una lista priorizada de requerimientos en una mejora funcional terminada.

### 5. ¿Qué roles existen en Scrum?
Scrum establece tres roles con responsabilidades diferenciadas:
- Product Owner: representa la visión del negocio y de los usuarios. Se encarga de gestionar y priorizar el Product Backlog para que el equipo trabaje en lo más valioso.
- Scrum Master: actúa como facilitador del equipo. Elimina los obstáculos que frenan el avance, protege al equipo de interrupciones externas y vela por el cumplimiento de los acuerdos de trabajo.
- Desarrolladores: son los profesionales técnicos encargados de convertir los requerimientos del backlog en software probado y listo para usarse.

### 6. ¿Qué es un Sprint?
Es la unidad básica de trabajo en Scrum: un ciclo cerrado de tiempo, usualmente de dos semanas, en el que se construye un incremento de software funcional y probado.
Al iniciar el Sprint se fija un objetivo concreto que no debe cambiarse durante esas semanas. Al finalizar el ciclo, se realiza una sesión de demostración con los interesados y una reunión interna de retrospectiva para evaluar mejoras en la dinámica de trabajo antes de iniciar el siguiente Sprint.

### 7. ¿Qué es Kanban?
Es un método de gestión visual del flujo de trabajo adaptado al desarrollo de software por David J. Anderson a partir del sistema de producción de Toyota.
A diferencia de Scrum, no impone ciclos cerrados con fechas fijas ni roles obligatorios. Su principio central consiste en visualizar las etapas del trabajo en un tablero con columnas (por ejemplo: Pendiente, En Desarrollo, En Pruebas, Listo) y limitar la cantidad de tareas abiertas al mismo tiempo.

### 8. ¿Cómo ayuda Kanban a organizar el trabajo?
Ayuda estableciendo un límite estricto al trabajo en progreso (WIP por sus siglas en inglés). Si se fija que en la columna de desarrollo no puede haber más de tres tareas activas, el equipo debe terminar las tareas en curso antes de tomar una nueva.
Esto saca a la luz de inmediato los cuellos de botella: si varias tareas se acumulan en revisión, los desarrolladores ayudan a desatascar esa fase en vez de abrir más trabajo incompleto, logrando un flujo de entrega regular y sostenible.

### 9. ¿Qué es Extreme Programming (XP)?
Es una metodología ágil formulada por Kent Beck que pone el foco en las prácticas técnicas de ingeniería y la calidad del código fuente. Mientras Scrum se enfoca en la gestión de tareas, XP se enfoca en cómo programar bien.
Sus prácticas más conocidas incluyen:
- Desarrollo guiado por pruebas (TDD): escribir las pruebas automatizadas antes de programar la lógica del sistema.
- Programación en parejas: dos desarrolladores trabajan frente a un mismo problema para mejorar el diseño y detectar errores en el momento.
- Refactorización regular: limpiar y simplificar el código existente sin alterar su comportamiento externo.
- Integración continua: subir y validar los cambios en la rama principal varias veces al día con pruebas automáticas.

### 10. ¿Por qué las metodologías ágiles son ampliamente utilizadas actualmente?
Porque las organizaciones necesitan responder con rapidez a un entorno tecnológico que cambia de prisa. Esperar dos años para validar si un producto digital funciona implica un riesgo económico excesivo.
La agilidad permite lanzar versiones iniciales básicas en poco tiempo, obtener métricas reales de los usuarios y ajustar el rumbo según datos concretos. Además, promueve equipos técnicos con mayor sentido de pertenencia y compromiso al darles autonomía y permitirles ver el resultado de su esfuerzo en producción de forma continua.

## VII. Industria del software

### 1. ¿Cómo surgió la industria del software?
Durante las décadas de 1950 y 1960, el software no se comercializaba de manera independiente; los fabricantes de computadoras como IBM lo entregaban como un complemento gratuito para que los clientes pudieran utilizar sus computadoras centrales.
El cambio definitivo ocurrió en 1969, cuando IBM, presionada por investigaciones antimonopolio del gobierno estadounidense, decidió separar la venta del software y los servicios respecto al hardware. Esta decisión abrió el camino para que surgieran empresas dedicadas exclusivamente a desarrollar y comercializar programas informáticos.

### 2. ¿Qué impacto tuvieron los primeros computadores en el desarrollo del software?
Máquinas pioneras como ENIAC o los primeros modelos de tubos de vacío se programaban mediante conexiones físicas de cables o usando tarjetas perforadas con código de máquina.
Estas limitaciones obligaban a los ingenieros a cuidar cada ciclo de reloj y cada byte disponible. La enorme dificultad de programar a tan bajo nivel impulsó la búsqueda urgente de lenguajes y herramientas que permitieran expresar instrucciones sin tener que manipular directamente los circuitos de la máquina.

### 3. ¿Qué papel jugaron los lenguajes de programación en el crecimiento del software?
Permitieron democratizar el acceso a la computación. La creación de lenguajes de alto nivel como Fortran para cálculo científico y COBOL para aplicaciones de gestión permitió redactar algoritmos usando palabras en inglés y fórmulas matemáticas comprensibles.
Los compiladores se encargaron de traducir esa lógica humana a instrucciones binarias. Esto aceleró el desarrollo de aplicaciones, redujo los fallos de codificación y permitió que los programas pudieran ejecutarse en equipos de diferentes fabricantes con ajustes mínimos.

### 4. ¿Cómo influyó la aparición de los microprocesadores?
La llegada del Intel 4004 en 1971 y de sus sucesores concentró la unidad central de procesamiento en una sola pastilla de silicio.
Esto eliminó la necesidad de salas refrigeradas exclusivas para albergar computadoras. Redujo los costos de producción y permitió que la capacidad de cómputo llegara a talleres, oficinas y hogares particulares, sentando las bases de la revolución de la informática personal.

### 5. ¿Qué impacto tuvo la popularización de las computadoras personales?
Con la salida al mercado de equipos como el Apple II y la IBM PC en las décadas de 1970 y 1980, las computadoras pasaron a formar parte de la vida de millones de personas.
Esto generó una demanda masiva de software de consumo y oficina: hojas de cálculo como VisiCalc y Lotus 1-2-3, procesadores de texto, sistemas contables y videojuegos. El software dejó de ser una disciplina confinada a centros de investigación y se transformó en un sector comercial de gran escala liderado por firmas como Microsoft, Apple y Adobe.

### 6. ¿Cómo influyó Internet en el desarrollo del software?
Internet transformó el software, pasando de programas aislados que se instalaban mediante disquetes o discos compactos a un ecosistema conectado en red.
Facilitó que las aplicaciones intercambiaran datos a escala global mediante protocolos estandarizados, impulsó el crecimiento colaborativo del software libre y de proyectos como Linux, y modificó los canales de distribución: las actualizaciones y parches dejaron de enviarse por correo postal y pasaron a descargarse por la red en pocos segundos.

### 7. ¿Qué impacto tienen las aplicaciones web en la actualidad?
Han convertido al navegador en una plataforma de ejecución universal. Herramientas de diseño complejas como Figma, procesadores de texto en línea y plataformas de gestión corren directamente en la web sin requerir instalaciones locales complejas.
Para los equipos de ingeniería, el modelo web simplifica el despliegue: actualizar una función en los servidores permite que todos los usuarios accedan a la mejora con solo recargar la página, evitando lidiar con versiones obsoletas instaladas en los equipos de los clientes.

### 8. ¿Qué importancia tienen las aplicaciones móviles?
Desde la adopción generalizada de los teléfonos inteligentes a partir de 2007, el software pasó a estar presente en el bolsillo de las personas durante todo el día.
Las aplicaciones móviles impulsaron modelos de negocio basados en geolocalización, pagos digitales y servicios bajo demanda. Esto exigió a los ingenieros diseñar interfaces táctiles claras, optimizar el uso de la batería y construir aplicaciones capaces de operar con conexiones de red inestables.

### 9. ¿Qué nuevas áreas de desarrollo han surgido en la industria del software?
En los últimos años han cobrado relevancia campos técnicos especializados:
- Inteligencia artificial e ingeniería de datos: entrenamiento de modelos de aprendizaje automático, redes neuronales y procesamiento de lenguaje natural.
- Ciberseguridad: análisis de vulnerabilidades, auditoría de código, protección de infraestructuras y criptografía aplicada.
- DevOps e infraestructura en la nube: automatización de despliegues, infraestructura como código y gestión de contenedores con herramientas como Docker y Kubernetes.
- Sistemas embebidos e Internet de las cosas: desarrollo de firmware para microcontroladores y dispositivos interconectados en tiempo real.
- Sistemas distribuidos: protocolos punto a punto y registros descentralizados basados en criptografía.

### 10. ¿Por qué la industria del software continúa creciendo?
Porque el software tiene una característica económica particular: una vez escrito el programa, el costo de reproducirlo y distribuirlo a miles de usuarios adicionales es prácticamente nulo.
Además, sectores tradicionales como la agricultura, la medicina, la manufactura y la logística requieren incorporar sistemas digitales para optimizar procesos y reducir costos. Las organizaciones que no integran software en sus operaciones pierden competitividad frente a alternativas más automatizadas.

## VIII. Tecnologías actuales

### 1. ¿Qué es la computación en la nube?
Es un modelo que permite acceder a recursos computacionales como servidores, almacenamiento, redes y bases de datos a través de Internet, bajo un esquema de pago por consumo.
En lugar de comprar servidores físicos para instalarlos en cuartos refrigerados propios y costear su mantenimiento eléctrico, las organizaciones alquilan capacidad de procesamiento a proveedores especializados como AWS, Google Cloud o Azure.

### 2. ¿Qué ventajas ofrece la computación en la nube?
- Escalabilidad elástica: si una plataforma de compras pasa de mil a medio millón de visitas por un evento comercial, la infraestructura suma servidores en minutos y los apaga cuando la demanda desciende.
- Optimización de costos: evita la compra inicial de hardware costoso; se pagan únicamente las horas de procesamiento, almacenamiento y ancho de banda consumidos.
- Respaldo geográfico: los datos se replican en diferentes centros de datos, lo que evita que un corte de energía local tumbe el servicio completo.

### 3. ¿Qué es el Internet de las cosas (IoT)?
Es la conexión digital de objetos físicos cotidianos e industriales a través de sensores, actuadores y programas embebidos, permitiéndoles recopilar y transmitir datos por la red sin intervención manual continua.
Incluye desde sensores de humedad en cultivos y medidores eléctricos residenciales hasta boyas marítimas y monitores de presión en tuberías industriales.

### 4. ¿Qué tipo de software requieren los dispositivos IoT?
Requieren software embebido de bajo nivel y tiempo real, como firmware o sistemas operativos livianos (RTOS).
Este software se programa habitualmente en lenguajes como C, C++ o Rust para controlar el uso de memoria y aprovechar microcontroladores con recursos mínimos (procesadores modestos y pocos kilobytes de RAM). Su diseño prioriza tres factores: consumo de batería mínimo, resistencia a pérdidas de señal y uso de protocolos de red livianos como MQTT o CoAP.

### 5. ¿Qué es la inteligencia artificial aplicada al software?
Es la incorporación de modelos estadísticos y redes neuronales en programas computacionales para resolver problemas no deterministas, como reconocer patrones visuales, clasificar textos o anticipar tendencias a partir de datos históricos.
En vez de escribir manualmente reglas condicionales para cada situación imaginable, el modelo aprende patrones analizando conjuntos extensos de datos de entrenamiento.

### 6. ¿Qué aplicaciones actuales utilizan inteligencia artificial?
- Asistencia en programación: herramientas que sugieren complementos de código según el contexto del archivo, detectan fallos de sintaxis y ayudan a escribir consultas a bases de datos.
- Diagnóstico médico: sistemas de visión computacional que revisan resonancias o tomografías para señalar anomalías antes de que el ojo humano las distinga con claridad.
- Prevención de fraudes bancarios: algoritmos que evalúan transacciones de tarjetas en milisegundos, bloqueando movimientos que no concuerdan con el patrón de uso habitual del cliente.
- Automatización de vehículos: procesamiento de señales de radar y cámaras para mantener el carril y activar frenos ante imprevistos.

### 7. ¿Qué es DevOps?
Es una cultura de trabajo y un conjunto de prácticas de ingeniería orientadas a coordinar a los equipos que programan el software con los equipos encargados de la infraestructura y los servidores.
Su propósito es acelerar el ciclo de entregas, pasando de desplegar actualizaciones dos veces al año a liberar mejoras pequeñas y seguras de forma frecuente.

### 8. ¿Qué problema busca resolver DevOps?
Resuelve la clásica división de culpas entre áreas técnicas: los programadores daban por buena una función porque corría en sus computadoras de trabajo y se desentendían de los fallos en los servidores, mientras el equipo de operaciones frenaba cualquier actualización por temor a desestabilizar la plataforma.
DevOps integra ambas responsabilidades: los desarrolladores asumen el comportamiento del código en producción y el equipo de operaciones colabora desde el comienzo automatizando entornos de prueba idénticos a los reales.

### 9. ¿Por qué es importante la integración entre desarrollo y operaciones?
Porque automatizar las tareas repetitivas reduce los errores humanos y ahorra tiempo. A través de flujos de integración y despliegue continuo (CI/CD), cada ajuste aprobado en el código se compila, se verifica con pruebas automáticas y se publica en producción sin requerir configuraciones manuales propensas a descuidos.
Esto agiliza la corrección de fallas y asegura que los sistemas mantengan un comportamiento predecible.

### 10. ¿Cómo influyen estas tecnologías en el futuro del software?
El software ha dejado de ser un programa aislado que corre en un solo disco para convertirse en una red distribuida de servicios interconectados.
Un desarrollo actual puede combinar servicios en la nube, recepción de telemetría desde sensores remotos, inferencia de modelos de aprendizaje automático y despliegues automatizados mediante tuberías de entrega continua. Por ello, el ingeniero de software debe dominar tanto la lógica de programación como el manejo de datos, la seguridad y la infraestructura donde opera su código.

## IX. Arquitectura de computación

### 1. ¿Qué es la arquitectura de la computación?
Es el diseño estructural y conceptual que describe cómo interactúan los componentes físicos y lógicos de un computador para procesar datos y ejecutar programas.
Establece la relación entre la CPU, los canales de comunicación y la memoria, definiendo además el conjunto de instrucciones (ISA, como x86 o ARM) que el hardware reconoce y que los compiladores y sistemas operativos utilizan para trabajar.

### 2. ¿Qué componentes forman parte de la arquitectura de un computador?
Tomando como base el modelo tradicional de Von Neumann y sus evoluciones, los componentes centrales son:
- Unidad central de procesamiento (CPU): contiene la unidad de control, la unidad aritmético-lógica y los registros internos.
- Memoria principal y jerarquía de cachés: guarda instrucciones y datos de uso inmediato.
- Buses del sistema: líneas de datos, direcciones y control que comunican los módulos entre sí.
- Sistema de entrada y salida: controladores y puertos que gestionan la interacción con discos, pantallas y redes.

### 3. ¿Qué función cumple el procesador (CPU)?
La CPU es el circuito encargado de ejecutar las instrucciones de los programas mediante un ciclo constante de tres pasos:
- Búsqueda (Fetch): lee la siguiente instrucción almacenada en la memoria RAM apuntada por el contador de programa.
- Decodificación (Decode): la unidad de control interpreta la operación binaria y prepara las rutas de datos necesarias.
- Ejecución (Execute): la unidad aritmético-lógica realiza la operación matemática o lógica y escribe el resultado en un registro o dirección de memoria.

### 4. ¿Qué función cumple la memoria en un sistema informático?
Actúa como la mesa de trabajo del procesador. Almacena de forma temporal las instrucciones del sistema operativo y de los programas en uso, así como los datos que estas aplicaciones manipulan en cada instante.
Sin memoria, la CPU no tendría de dónde cargar instrucciones para procesar, ya que sus registros internos solo pueden guardar un número muy reducido de datos a la vez.

### 5. ¿Qué diferencia existe entre memoria principal y memoria secundaria?
- Memoria principal (RAM): es rápida, de tecnología semiconductora y volátil. Cuando el equipo se apaga o pierde energía, su contenido se borra por completo. La CPU accede a ella de forma directa a través del bus del sistema.
- Memoria secundaria (discos de estado sólido o mecánicos): es más lenta que la RAM pero no volátil. Mantiene la información almacenada de forma indefinida aunque el equipo esté desconectado. La CPU no ejecuta código directamente desde la memoria secundaria; primero debe cargarlo en la memoria principal.

### 6. ¿Qué es la memoria caché?
Es una memoria de tamaño reducido y velocidad muy alta construida con tecnología SRAM, ubicada dentro del mismo procesador entre los registros y la memoria RAM principal.
Guarda los datos e instrucciones que la CPU consulta con mayor frecuencia, apoyándose en los principios de localidad temporal y espacial. Al encontrar la información en la caché, el procesador no tiene que esperar los ciclos más lentos de lectura de la RAM principal, evitando caídas de rendimiento.

### 7. ¿Qué papel cumplen los dispositivos de entrada y salida?
Conectan el entorno físico externo con el procesamiento digital del computador:
- Dispositivos de entrada (teclado, ratón, cámaras, sensores): capturan acciones o señales analógicas y las traducen a flujos de datos binarios que el sistema operativo puede procesar.
- Dispositivos de salida (monitores, impresoras, actuadores): toman los datos binarios procesados por la máquina y los muestran como texto, imágenes o movimientos mecánicos útiles para el usuario.

### 8. ¿Cómo interactúa el software con el hardware?
La comunicación se realiza a través de niveles de abstracción organizados:
- La aplicación solicita una acción, como abrir o escribir un archivo en disco.
- Esta petición se convierte en una llamada al sistema (syscall) dirigida al kernel del sistema operativo.
- El kernel verifica los permisos de seguridad y delega la instrucción al controlador del dispositivo (driver).
- El driver envía señales y comandos directos a los registros del hardware mediante interrupciones o canales de acceso directo a memoria (DMA), provocando los cambios de voltaje necesarios en los circuitos físicos.

### 9. ¿Por qué es importante comprender la arquitectura de computación para desarrollar software?
Porque el software se ejecuta sobre componentes físicos con límites de velocidad, capacidad y energía.
Un programador que no conoce cómo funciona la jerarquía de memoria puede escribir bucles que causen fallos de caché continuos, haciendo que el programa corra mucho más lento sin necesidad. Conocer la arquitectura permite aprovechar la ejecución concurrente, evitar bloqueos entre hilos y escribir código que aproveche los recursos del hardware de forma eficiente.

### 10. ¿Qué avances han ocurrido en la arquitectura de los computadores?
- Procesadores con múltiples núcleos y núcleos mixtos: combinación de núcleos rápidos de alto rendimiento con núcleos de bajo consumo para optimizar la batería en teléfonos y portátiles (como en arquitecturas ARM y Apple Silicon).
- Unidades de aceleración especializada (GPUs, NPUs): circuitos diseñados para cálculos matriciales masivos, usados en procesamiento gráfico y ejecución de modelos de inteligencia artificial.
- Arquitecturas abiertas (RISC-V): estándar de instrucciones libre que permite a universidades y empresas diseñar chips propios sin pagar licencias cerradas.
- Computación cuántica experimental: uso de cúbits y principios de superposición para resolver problemas específicos de física y criptografía que desbordarían a las computadoras clásicas.

## X. Reflexión, análisis y propuesta

### 1. Analice cómo el software influye en actividades cotidianas como educación, comercio o comunicación.
El software ha cambiado la manera en que estudiamos, compramos y nos comunicamos:
- Educación: posibilita programas universitarios a distancia como el nuestro en la Universidad de Cartagena. A través del campus virtual SIMA y plataformas de estudio, podemos organizar horarios y revisar material técnico sin depender de la presencia diaria en un aula física.
- Comercio: facilita que pequeños negocios y artesanos vendan en todo el país mediante plataformas web y cobros electrónicos con PSE, Transfiya o billeteras móviles.
- Comunicación: permite coordinar proyectos académicos en tiempo real mediante mensajería encriptada, repositorios en red y videollamadas con personas en diferentes ciudades.

### 2. Proponga un ejemplo de problema cotidiano que podría resolverse con un sistema de software.
En Cartagena y varias ciudades de la costa Caribe, el transporte colectivo en busetas opera sin rutas visibles ni tiempos de llegada predecibles. Los pasajeros pasan media hora o más esperando en la calle sin saber si el vehículo ya pasó, si viene lleno o cuánto demorará en llegar.
Esto puede abordarse con una aplicación móvil conectada a dispositivos GPS de bajo costo instalados en los buses. La aplicación mostraría en un mapa sencillo la ubicación del vehículo en tiempo real, el tiempo estimado para llegar a la parada más cercana y el costo del pasaje, evitando tiempos de espera innecesarios bajo el sol.

### 3. Imagine que debe diseñar un sistema informático para su universidad. ¿Qué problema resolvería?
Diseñaría la aplicación móvil institucional UDC App para la Universidad de Cartagena.
Actualmente, los estudiantes debemos lidiar con la dispersión de servicios y trámites presenciales o páginas desactualizadas. Cuando necesitamos un certificado, consultar un préstamo de biblioteca, enterarnos de avisos oficiales o apartar una sala de cómputo en la sede Piedra de Bolívar o San Agustín, el proceso implica trámites en papel, filas en ventanilla o formularios extensos y tediosos. La UDC App resolvería esta desconexión centralizando la vida universitaria en el teléfono: trámites ágiles, catálogo bibliotecario, noticias oficiales al instante, carnet digital y un sistema rápido para apartar laboratorios de computación sin cuestionarios tediosos ni papeleo.

### 4. ¿Qué funcionalidades debería tener ese sistema?
La UDC App contaría con las siguientes funciones clave:
- Carnet digital estudiantil: identificación visual y código QR dinámico para el acceso en las porterías de los campus y el registro en eventos universitarios.
- Módulo para apartar laboratorios y salas de cómputo: visualización de máquinas y horarios disponibles en bloques de Piedra de Bolívar (como Bloque F y G), permitiendo apartar un puesto de trabajo en dos toques, sin llenar cuestionarios tediosos ni formularios repetitivos.
- Módulo de trámites académicos y solicitudes: expedición de certificados de estudio, paz y salvos y seguimiento de solicitudes en tiempo real sin acudir a ventanillas físicas.
- Biblioteca integrada: consulta del catálogo de libros físicos y digitales, reserva de ejemplares y notificaciones automáticas antes del vencimiento de préstamos.
- Canal oficial de noticias y eventos: avisos institucionales filtrados por facultad, sede y programa académico para evitar cadenas falsas en grupos de mensajería.
- Inicio de sesión por roles: acceso diferenciado con credenciales institucionales para estudiantes, docentes y personal administrativo.

### 5. ¿Qué tipo de usuarios utilizarían ese sistema?
- Estudiantes: para identificarse con el carnet digital, tramitar certificados, consultar noticias de su facultad, revisar libros de biblioteca y apartar laboratorios y computadores sin cuestionarios tediosos ni trabas burocráticas.
- Docentes: para apartar laboratorios de cómputo destinados a prácticas de clase, consultar su programación académica y publicar avisos directos a sus asignaturas.
- Personal de biblioteca y administradores de laboratorios: para validar préstamos de libros, controlar el aforo en las salas y revisar el estado de los equipos.
- Funcionarios administrativos y admisiones: para responder y tramitar solicitudes estudiantiles en una bandeja unificada.
- Personal de vigilancia en portería: para escanear el carnet digital QR al ingreso de las sedes universitarias.

### 6. ¿Qué dispositivos utilizarían los usuarios para interactuar con el sistema?
- Teléfonos inteligentes con Android e iOS: canal principal mediante la aplicación móvil nativa o multiplataforma donde los estudiantes consultan su carnet, noticias y reservas.
- Computadores de escritorio y portátiles: acceso mediante panel web para docentes y personal administrativo que gestiona solicitudes, horarios y configuración general.
- Terminales o tabletas en porterías y recepciones: dispositivos asignados al personal de seguridad y biblioteca para escanear códigos QR de carnetización y préstamos.

### 7. ¿Qué periféricos o sistemas de entrada serían necesarios?
- Cámaras de teléfonos y lectores ópticos de códigos QR: para escanear el carnet institucional y validar ingresos en portería o biblioteca.
- Pantallas táctiles y teclados: en terminales de consulta rápida ubicadas en los pasillos de las sedes.
- Sensores de presencia o lectores en salas de cómputo: para registrar el uso efectivo de los puestos reservados y liberar automáticamente los equipos si el usuario no se presenta en los primeros quince minutos.

### 8. ¿Qué tecnologías podrían utilizarse para desarrollar ese sistema?
- Aplicación móvil: Flutter o React Native para mantener una sola base de código compatible con Android e iOS, ofreciendo fluidez en interfaces móviles.
- Panel web administrativo: React o Svelte con TypeScript para la interfaz de gestión de docentes y funcionarios.
- Backend y APIs: servicios desarrollados en Python (FastAPI) o Go por su eficiencia en consumo de memoria y facilidad para manejar peticiones concurrentes.
- Base de datos: PostgreSQL para la gestión relacional de usuarios, solicitudes y reservas, complementado con Redis para el manejo de sesiones activas y bloqueos de horarios en tiempo real.
- Notificaciones y despliegue: Firebase Cloud Messaging para alertas móviles y contenedores Docker desplegados con integración continua mediante GitHub Actions.

### 9. ¿Qué habilidades debe desarrollar un estudiante para convertirse en ingeniero de software?
- Pensamiento lógico y bases algorítmicas: capacidad para descomponer problemas complejos en pasos claros, evaluar la eficiencia de las soluciones y modelar datos con rigor.
- Criterio de arquitectura y código limpio: dominar principios de desacoplamiento, modularidad y pruebas automatizadas antes de atarse a herramientas o librerías de turno.
- Comunicación clara y trabajo en equipo: saber escuchar las necesidades de usuarios no técnicos, documentar decisiones y colaborar mediante control de versiones en Git.
- Hábitos de aprendizaje autodidacta: el software evoluciona con rapidez; la disposición a leer documentación técnica en inglés y probar nuevas tecnologías por cuenta propia es lo que permite mantenerse vigente profesionalmente.

### 10. Desde su perspectiva como estudiante que inicia la carrera, ¿cómo cree que la ingeniería de software contribuirá al desarrollo de la sociedad en el futuro?
Como estudiante que comienza su formación en la Universidad de Cartagena, veo la ingeniería de software como una herramienta práctica para resolver problemas concretos de nuestra comunidad. Proyectos como la UDC App demuestran que el software tiene un impacto directo en nuestra vida diaria: reduce la burocracia en nuestras instituciones, evita filas innecesarias, agiliza trámites, biblioteca y la reserva de laboratorios, y le devuelve tiempo valioso a las personas.
En nuestra región Caribe, aplicar ingeniería de software permite mejorar la gestión en hospitales públicos, transparentar procesos administrativos y ofrecer herramientas útiles a estudiantes y trabajadores. Nuestra responsabilidad ética como futuros ingenieros es diseñar sistemas accesibles, estables y respetuosos con los usuarios, aplicando la tecnología para mejorar las condiciones de vida de la sociedad en la que vivimos.

## Referencias Bibliográficas

- Comer, D. E. (2015). *Redes de computadoras e Internet* (6.ª ed.). Pearson Educación.
- Fowler, M. (2018). *Refactoring: Improving the Design of Existing Code* (2.ª ed.). Addison-Wesley.
- Incencio Piñeiro, E., et al. (2022). Dimensión Construcción Lógica en Ingeniería de Software. *Revista Científica EBSCO*, 15(2), 45-58.
- Martin, R. C. (2017). *Clean Architecture: A Craftsman's Guide to Software Structure and Design*. Prentice Hall.
- Patterson, D. A., & Hennessy, J. L. (2018). *Computer Organization and Design: The Hardware/Software Interface* (RISC-V Edition). Morgan Kaufmann.
- Pressman, R. S. (2010). *Ingeniería del software: un enfoque práctico* (7.ª ed.). McGraw-Hill Interamericana.
- Sommerville, I. (2011). *Ingeniería de software* (9.ª ed.). Pearson Educación.
- Weber, R. (2020). *Fundamentos de informática y arquitectura de computadores*. Editorial eLibro.
