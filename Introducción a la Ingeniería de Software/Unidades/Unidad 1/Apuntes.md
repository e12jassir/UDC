# Apuntes — Unidad 1: Fundamentos de Ingeniería de Software

> **Asignatura:** Introducción a la Ingeniería de Software · `IX24014-A1`  
> **Docente:** Jhon Carlos Arrieta Arrieta  
> **Última actualización:** 2026-09-29

---

## 1. ¿Qué es la Ingeniería de Software?

La Ingeniería de Software (IS) es la aplicación sistemática, disciplinada y cuantificable de principios de ingeniería al **desarrollo, operación y mantenimiento** de software. La palabra clave es *sistemática*: a diferencia de la programación informal, la IS impone un proceso repetible, medible y mejorable.

### Diferencia práctica: Programador vs. Ingeniero de Software

| Dimensión | Programador | Ingeniero de Software |
| :--- | :--- | :--- |
| **Enfoque** | Resolver un problema específico con código | Resolver el problema correcto de forma sostenible |
| **Horizonte temporal** | Solución inmediata | Ciclo de vida completo del producto |
| **Herramientas** | Editor + compilador | Metodologías, herramientas de gestión, pruebas, despliegue |
| **Trabajo en equipo** | Frecuentemente individual | Coordinación de equipos multidisciplinarios |
| **Consideraciones** | Funcionalidad | Funcionalidad + mantenibilidad + seguridad + escalabilidad + costo |
| **Ejemplo cotidiano** | Escribir un script que resuelve una tarea puntual | Diseñar el sistema backend de una app como Rappi con millones de usuarios |

> **Analogía útil:** Un programador es quien coloca ladrillos. Un ingeniero de software es quien diseña el edificio, coordina la obra, verifica la estructura y planifica el mantenimiento durante décadas.

### ¿Por qué existe la IS?

Surgió de la **crisis del software** de los años 1960–1970: proyectos que se entregaban tarde, con sobrecosto, llenos de errores y difíciles de mantener. El término fue acuñado en la Conferencia de la OTAN de 1968. La lección histórica es que escribir código sin proceso es como construir un puente sin planos.

---

## 2. Historia y Evolución

| Período | Hito clave | Impacto |
| :--- | :--- | :--- |
| **1940s–50s** | Primeros programas en lenguaje máquina (ENIAC) | Programación = configuración física |
| **1950s–60s** | Lenguajes de alto nivel (FORTRAN, COBOL, LISP) | Abstracción del hardware |
| **1968** | Conferencia NATO — se acuña "Software Engineering" | Nacimiento formal de la disciplina |
| **1970s** | Modelo en Cascada (Royce), programación estructurada (Dijkstra) | Primer intento de sistematizar el desarrollo |
| **1980s** | Modelos OOP (C++), primeras metodologías formales | Código reutilizable y modular |
| **1990s** | Patrones de diseño (GoF, 1994), auge del internet | Estandarización de soluciones |
| **2001** | Manifiesto Ágil | Revolución en la forma de gestionar proyectos |
| **2010s–hoy** | DevOps, microservicios, cloud-native, IA asistida | Integración continua y despliegue a escala global |

---

## 3. El Ciclo de Vida del Software (SDLC)

El **Software Development Life Cycle (SDLC)** es el marco que describe las fases que atraviesa todo sistema de software, desde la idea hasta su retiro.

### Fases del SDLC

```
┌─────────────────────────────────────────────────────────┐
│  1. Planificación  →  2. Análisis de Requisitos          │
│        ↓                        ↓                       │
│  6. Mantenimiento  ←  5. Despliegue  ←  4. Pruebas      │
│                              ↑                          │
│                     3. Diseño + Implementación           │
└─────────────────────────────────────────────────────────┘
```

| Fase | Qué se hace | Entregable típico | Error común |
| :--- | :--- | :--- | :--- |
| **1. Planificación** | Definir alcance, recursos, tiempos y riesgos | Plan de proyecto, cronograma | Omitir el análisis de riesgos |
| **2. Análisis de Requisitos** | Levantar qué debe hacer el sistema con los stakeholders | Documento de requisitos (SRS) | Requisitos ambiguos o incompletos |
| **3. Diseño** | Arquitectura del sistema, BD, interfaces, módulos | Diagramas UML, prototipo | No considerar la escalabilidad desde el diseño |
| **4. Implementación** | Codificación del sistema | Código fuente versionado (Git) | Código sin pruebas unitarias |
| **5. Pruebas** | Verificación funcional, de rendimiento, seguridad | Reporte de defectos | Probar solo el camino feliz |
| **6. Despliegue** | Puesta en producción | Sistema funcionando en entorno real | No tener plan de rollback |
| **7. Mantenimiento** | Corrección de bugs, mejoras, adaptaciones | Actualizaciones de versión | Acumulación de deuda técnica |

### Ejemplo real — ¿Cómo aplicó Rappi el SDLC?

- **Planificación:** MVP (Producto Mínimo Viable) solo en Bogotá, 2015.
- **Requisitos:** Domicilios de restaurantes. Sin complicar con supermercados o bancos al inicio.
- **Diseño:** App móvil + backend en la nube (AWS). GPS en tiempo real.
- **Implementación:** Equipo pequeño, lanzamiento rápido.
- **Pruebas:** Beta cerrada con usuarios reales.
- **Despliegue:** Expansión ciudad por ciudad.
- **Mantenimiento:** Nuevas verticales (RappiFavor, RappiPay), corrección de bugs críticos de geolocalización.

---

## 4. Modelos de Proceso de Software

Un **modelo de proceso** define la secuencia y estructura de las actividades de desarrollo. Elegir el incorrecto puede condenar un proyecto al fracaso.

### 4.1 Modelo en Cascada (Waterfall)

Propuesto por Winston Royce (1970). Las fases se ejecutan de forma **secuencial y lineal**: no se pasa a la siguiente hasta completar la anterior.

```
Requisitos → Diseño → Implementación → Pruebas → Despliegue → Mantenimiento
```

| Ventajas | Desventajas |
| :--- | :--- |
| Simple de entender y gestionar | Inflexible ante cambios de requisitos |
| Documentación completa en cada fase | El cliente ve el producto al final |
| Adecuado cuando los requisitos son estables | Los errores de requisitos se detectan tarde y son costosos |
| Bueno para proyectos gubernamentales/militares | Poco adecuado para entornos de alta incertidumbre |

**Cuándo usarlo:** Proyectos con requisitos bien definidos y poco cambiantes (e.g., software de control de un satélite, sistema bancario legacy).

**Cuándo NO usarlo:** Startups, aplicaciones web con retroalimentación constante del usuario.

---

### 4.2 Modelo en Espiral (Boehm, 1988)

Combina elementos del Cascada con prototipos iterativos. Cada **vuelta de la espiral** pasa por cuatro cuadrantes:

```
1. Determinación de objetivos y restricciones
        ↓
2. Análisis y reducción de riesgos (PROTOTIPO)
        ↓
3. Desarrollo y validación
        ↓
4. Planificación de la siguiente vuelta
        ↑
(Repite hasta que el producto esté listo)
```

| Ventajas | Desventajas |
| :--- | :--- |
| Gestión explícita de riesgos | Costoso en análisis de riesgo |
| Adecuado para proyectos grandes y complejos | Requiere experiencia para identificar riesgos |
| El cliente ve prototipos intermedios | Difícil de escalar a proyectos pequeños |

**Cuándo usarlo:** Software de defensa, sistemas críticos de salud, proyectos con alta incertidumbre técnica.

---

### 4.3 Desarrollo Ágil (Agile)

El **Manifiesto Ágil** (2001) propuso 4 valores:

1. **Individuos e interacciones** sobre procesos y herramientas.
2. **Software funcionando** sobre documentación exhaustiva.
3. **Colaboración con el cliente** sobre negociación de contratos.
4. **Respuesta al cambio** sobre seguir un plan.

#### Scrum (el framework ágil más usado)

```
Product Backlog → Sprint Planning → Sprint (1-4 semanas)
                                          ↓
                              Sprint Review + Retrospectiva
                                          ↓
                                   (Siguiente Sprint)
```

**Roles en Scrum:**
- **Product Owner:** Prioriza el backlog según valor de negocio.
- **Scrum Master:** Facilita el proceso, elimina impedimentos.
- **Dev Team:** Auto-organizado, multifuncional.

**Artefactos:**
- **Product Backlog:** Lista priorizada de funcionalidades.
- **Sprint Backlog:** Funcionalidades comprometidas para el sprint.
- **Incremento:** Producto funcional al final de cada sprint.

---

### 4.4 Comparativa Final de Modelos

| Criterio | Cascada | Espiral | Ágil (Scrum) |
| :--- | :---: | :---: | :---: |
| Flexibilidad al cambio | ❌ Baja | 🟡 Media | ✅ Alta |
| Visibilidad del cliente | ❌ Solo al final | 🟡 En prototipos | ✅ Cada sprint |
| Gestión de riesgos | ❌ Implícita | ✅ Explícita | 🟡 Iterativa |
| Documentación | ✅ Completa | 🟡 Parcial | ❌ Mínima necesaria |
| Adecuado para startups | ❌ | ❌ | ✅ |
| Adecuado para proyectos grandes | 🟡 | ✅ | 🟡 |
| Adecuado para requisitos estables | ✅ | 🟡 | ❌ |

### Startups vs. Empresas grandes — ¿Qué modelo usan?

**Startup (ej: una nueva app de delivery local):**
- Ágil/Scrum: Sprints de 2 semanas, lanzar MVP rápido, iterar según feedback de usuarios reales.
- Herramientas: Trello/Jira para backlog, GitHub para código, Vercel para despliegue.

**Empresa grande (ej: Bancolombia desarrollando un módulo de pagos):**
- Pueden combinar Cascada para la parte regulatoria (cumplimiento legal) con Ágil para las interfaces.
- Muchos equipos simultáneos requieren frameworks como SAFe (Scaled Agile Framework).
- Procesos de auditoría obligan a documentación exhaustiva (más cercano a Cascada o Espiral).

---

## 5. Requisitos de Software

Los requisitos son la descripción de **qué debe hacer** el sistema (funcionalidad) y **cómo debe comportarse** (restricciones).

| Tipo | Descripción | Ejemplo |
| :--- | :--- | :--- |
| **Funcionales** | Qué debe hacer el sistema | "El usuario puede iniciar sesión con email y contraseña" |
| **No funcionales** | Cómo debe comportarse | "El sistema debe responder en menos de 2 segundos" |
| **De dominio** | Reglas del negocio | "Los precios deben incluir IVA del 19%" |

**Formato de Historia de Usuario (Agile):**
```
Como [tipo de usuario],
quiero [funcionalidad],
para [beneficio/objetivo].

Ejemplo:
Como cliente de Rappi,
quiero rastrear mi pedido en tiempo real,
para saber cuándo llega el domiciliario.
```

---

## 6. Calidad del Software

La calidad no es solo "que funcione". ISO/IEC 25010 define los atributos de calidad:

| Atributo | Significado práctico |
| :--- | :--- |
| **Funcionalidad** | Hace lo que se especificó |
| **Fiabilidad** | No falla en condiciones normales |
| **Usabilidad** | El usuario puede usarlo sin manual de 100 páginas |
| **Eficiencia** | Usa bien los recursos (CPU, memoria, red) |
| **Mantenibilidad** | Se puede modificar sin romper todo |
| **Portabilidad** | Funciona en distintas plataformas/entornos |
| **Seguridad** | Resiste ataques, protege datos |

---

## 7. Errores Comunes y Cómo Evitarlos

| Error | Por qué ocurre | Cómo evitarlo |
| :--- | :--- | :--- |
| Confundir IS con programación | El curso se llama "Ingeniería de Software" pero se reduce a código | Recordar que IS incluye proceso, gestión, pruebas y mantenimiento |
| Creer que Ágil = sin documentación | Mala lectura del Manifiesto Ágil | Ágil dice "documentación suficiente", no cero documentación |
| Elegir el modelo de proceso incorrecto | No analizar el contexto del proyecto | Evaluar: requisitos estables vs. cambiantes, tamaño del equipo, riesgo |
| Saltar directamente a codificar | Presión por resultados rápidos | Dedicar tiempo al análisis de requisitos; cambiar un requisito en código es 100× más costoso que en papel |
| Ignorar el mantenimiento | Se piensa solo en el lanzamiento | El 60-80% del costo del software es mantenimiento (Pressman) |

---

## 8. Referencia Rápida

```
IS = Proceso + Personas + Producto

SDLC: Plan → Análisis → Diseño → Impl. → Prueba → Despliegue → Mant.

Modelos:
  Cascada  → secuencial, requisitos estables
  Espiral  → iterativo con gestión de riesgo
  Ágil     → iterativo, adaptativo, cliente involucrado

Scrum roles: Product Owner | Scrum Master | Dev Team
Scrum ciclo: Sprint (1-4 sem) → Review → Retrospectiva → Siguiente Sprint

Requisitos:
  Funcionales: QUÉ hace
  No funcionales: CÓMO se comporta
  De dominio: reglas del negocio
```

---

## 9. Recursos Externos Específicos

### Videos / Canales
- **Fireship** (YouTube): [`Software Development Life Cycle (SDLC) explained`](https://www.youtube.com/c/Fireship) — Explicaciones de 10 minutos, muy concretas, en inglés con subtítulos.
- **Fazt Code** (YouTube): Canal en español con explicaciones de metodologías ágiles y proyectos reales. Buscar: "Metodologías ágiles Scrum explicado".
- **freeCodeCamp** (YouTube): [`What is Agile?`](https://www.youtube.com/watch?v=Z9QbYZh1YXY) — Profundidad sin complicaciones.

### Libros (capítulos específicos)
- **Pressman & Maxim — Ingeniería de Software (9.ª ed.):**
  - Cap. 1: *El software y la ingeniería de software* — Definición y contexto histórico.
  - Cap. 2: *Modelos de proceso del software* — Cascada, Espiral, Ágil.
  - Cap. 3: *Desarrollo Ágil* — Scrum, XP, Kanban.
- **Sommerville — Ingeniería de Software (10.ª ed.):**
  - Cap. 2: *Procesos del software* — Descripción técnica comparada.

### Sitios web
- [agilemanifesto.org](https://agilemanifesto.org/iso/es/manifesto.html) — El manifiesto original en español.
- [scrum.org/resources/what-is-scrum](https://www.scrum.org/resources/what-is-scrum) — Guía oficial de Scrum en inglés/español.

---

## 10. Preguntas de Active Recall

Usa estas preguntas para estudiar sin releer pasivamente:

1. ¿Cuál es la diferencia fundamental entre un programador y un ingeniero de software? Da un ejemplo concreto.
2. ¿Por qué surgió la IS? Describe la "crisis del software" en dos oraciones.
3. Dibuja el SDLC con sus 7 fases de memoria. ¿Qué entregable produce cada una?
4. ¿En qué escenario elegirías el modelo en Cascada sobre Scrum? Justifica.
5. ¿Cuáles son los 4 valores del Manifiesto Ágil? ¿Qué significa que priorizan X "sobre" Y?
6. Define los tres roles de Scrum y su responsabilidad principal.
7. ¿Cuál es la diferencia entre un requisito funcional y uno no funcional? Da un ejemplo de cada uno para una app de transporte.
8. Nombra 3 atributos de calidad de software (ISO 25010) y explica cómo se miden en la práctica.
