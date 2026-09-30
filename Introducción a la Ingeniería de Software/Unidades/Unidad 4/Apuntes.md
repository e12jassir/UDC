# Apuntes — Unidad 4: Bases de Datos y Tendencias Tecnológicas

> **Asignatura:** Introducción a la Ingeniería de Software · `IX24014-A1`  
> **Docente:** Jhon Carlos Arrieta Arrieta  
> **Última actualización:** 2026-09-29

---

## 1. Bases de Datos — Conceptos Fundamentales

Una **base de datos** es una colección organizada de datos que permite almacenar, recuperar y manipular información de forma eficiente. El software que gestiona la base de datos se llama **SGBD (Sistema Gestor de Base de Datos)** o **DBMS** en inglés.

### ¿Por qué no usar archivos planos (CSV, TXT)?

| Problema con archivos planos | Solución con BD |
| :--- | :--- |
| Redundancia de datos (misma info repetida en múltiples archivos) | Normalización: cada dato en un solo lugar |
| Sin control de acceso concurrente (dos usuarios modifican a la vez = corrupción) | Transacciones con ACID |
| Búsquedas lentas (leer todo el archivo para encontrar un registro) | Índices: búsqueda en O(log n) |
| Sin integridad referencial (borrar cliente sin borrar sus pedidos) | Claves foráneas (FOREIGN KEY) |
| Sin backup ni recuperación integrada | El SGBD gestiona esto |

---

## 2. SQL — Bases de Datos Relacionales

**SQL (Structured Query Language)** es el lenguaje estándar para interactuar con bases de datos relacionales. Un modelo relacional organiza los datos en **tablas** con filas (registros) y columnas (atributos), y relaciona las tablas mediante **claves**.

### 2.1 Conceptos Clave

- **Tabla (Relación):** colección de datos con la misma estructura.
- **Clave Primaria (PRIMARY KEY):** identificador único de cada fila. Nunca puede ser NULL ni repetirse.
- **Clave Foránea (FOREIGN KEY):** referencia a la clave primaria de otra tabla. Garantiza integridad referencial.
- **Índice:** estructura auxiliar que acelera las búsquedas.

### 2.2 Diseño de Tablas — Ejemplo: sistema de pedidos (tipo Rappi)

```sql
-- Crear tabla de clientes
CREATE TABLE clientes (
    id          INT PRIMARY KEY AUTO_INCREMENT,
    nombre      VARCHAR(100)   NOT NULL,
    email       VARCHAR(150)   UNIQUE NOT NULL,
    telefono    VARCHAR(20),
    ciudad      VARCHAR(50)    DEFAULT 'Cartagena',
    creado_en   TIMESTAMP      DEFAULT CURRENT_TIMESTAMP
);

-- Crear tabla de restaurantes
CREATE TABLE restaurantes (
    id          INT PRIMARY KEY AUTO_INCREMENT,
    nombre      VARCHAR(100)   NOT NULL,
    categoria   VARCHAR(50),   -- 'Comida rápida', 'Pizza', etc.
    direccion   TEXT
);

-- Crear tabla de pedidos
CREATE TABLE pedidos (
    id              INT PRIMARY KEY AUTO_INCREMENT,
    cliente_id      INT NOT NULL,
    restaurante_id  INT NOT NULL,
    total           DECIMAL(10, 2) NOT NULL,
    estado          ENUM('pendiente', 'en_camino', 'entregado', 'cancelado') DEFAULT 'pendiente',
    creado_en       TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    FOREIGN KEY (cliente_id)     REFERENCES clientes(id),
    FOREIGN KEY (restaurante_id) REFERENCES restaurantes(id)
);
```

### 2.3 Operaciones CRUD con SQL

**CRUD = Create, Read, Update, Delete** — las cuatro operaciones fundamentales sobre datos.

#### CREATE (INSERT)
```sql
-- Insertar un cliente
INSERT INTO clientes (nombre, email, telefono)
VALUES ('Esteban Jaramillo', 'e12jassir@example.com', '+573001234567');

-- Insertar múltiples registros a la vez
INSERT INTO restaurantes (nombre, categoria) VALUES
    ('El Corral', 'Comida rápida'),
    ('Telepizza', 'Pizza'),
    ('La Perla', 'Mariscos');
```

#### READ (SELECT)
```sql
-- Seleccionar todos los clientes
SELECT * FROM clientes;

-- Seleccionar columnas específicas con condición
SELECT nombre, email
FROM clientes
WHERE ciudad = 'Cartagena';

-- Ordenar y limitar resultados
SELECT nombre, total
FROM pedidos
ORDER BY total DESC
LIMIT 10;

-- Búsqueda con LIKE (texto parcial)
SELECT * FROM restaurantes
WHERE nombre LIKE '%pizza%';    -- case-insensitive en MySQL

-- Conteo y agrupación
SELECT restaurante_id, COUNT(*) AS total_pedidos, AVG(total) AS promedio
FROM pedidos
GROUP BY restaurante_id
HAVING total_pedidos > 5;       -- filtro sobre el resultado del GROUP BY
```

#### UPDATE
```sql
-- Actualizar el estado de un pedido
UPDATE pedidos
SET estado = 'en_camino'
WHERE id = 42;

-- ⚠️ Siempre usar WHERE en UPDATE, si no actualizas TODOS los registros
UPDATE clientes
SET ciudad = 'Barranquilla'
WHERE id = 7;
```

#### DELETE
```sql
-- Eliminar un registro específico
DELETE FROM pedidos WHERE id = 99;

-- ⚠️ Nunca: DELETE FROM tabla; (borra TODO sin recuperación)
-- Mejor usar soft delete:
ALTER TABLE pedidos ADD COLUMN eliminado BOOLEAN DEFAULT FALSE;
UPDATE pedidos SET eliminado = TRUE WHERE id = 99;
```

### 2.4 JOINs — Combinar Tablas

Los JOINs permiten consultar datos de múltiples tablas relacionadas.

```sql
-- INNER JOIN: solo registros que coinciden en ambas tablas
SELECT c.nombre AS cliente, r.nombre AS restaurante, p.total, p.estado
FROM pedidos p
INNER JOIN clientes c     ON p.cliente_id = c.id
INNER JOIN restaurantes r ON p.restaurante_id = r.id
WHERE p.estado = 'entregado';

-- LEFT JOIN: todos los clientes, con o sin pedidos
SELECT c.nombre, COUNT(p.id) AS num_pedidos
FROM clientes c
LEFT JOIN pedidos p ON c.id = p.cliente_id
GROUP BY c.id, c.nombre;
```

**Tipos de JOIN:**
```
INNER JOIN → solo registros que coinciden en ambas tablas
LEFT JOIN  → todos los de la izq. + coincidentes de la der.
RIGHT JOIN → todos los de la der. + coincidentes de la izq.
FULL JOIN  → todos de ambas (no soportado en MySQL, usar UNION)
```

### 2.5 Transacciones y ACID

Una **transacción** es un conjunto de operaciones que se ejecutan como una unidad atómica.

**ACID:**
- **Atomicidad:** todo o nada. Si falla una operación, se revierte todo.
- **Consistencia:** la BD pasa de un estado válido a otro estado válido.
- **Aislamiento:** las transacciones concurrentes no se interfieren.
- **Durabilidad:** una vez confirmada, la transacción persiste incluso ante fallo del sistema.

```sql
-- Ejemplo: transferencia bancaria (clásico de ACID)
START TRANSACTION;

UPDATE cuentas SET saldo = saldo - 100000 WHERE id = 1;  -- Débito
UPDATE cuentas SET saldo = saldo + 100000 WHERE id = 2;  -- Crédito

-- Si todo está bien:
COMMIT;
-- Si algo falla:
-- ROLLBACK;
```

### 2.6 SGBD Relacionales Populares

| SGBD | Licencia | Uso típico | Característica destacada |
| :--- | :--- | :--- | :--- |
| **PostgreSQL** | Open-source | Startups, empresas | Más estricto con SQL estándar, extensible |
| **MySQL / MariaDB** | Open-source | Web (WordPress, Laravel) | Velocidad de lectura, ampliamente soportado |
| **SQLite** | Open-source | Apps móviles, local | Sin servidor, archivo único, ideal para Android |
| **SQL Server** | Propietario (Microsoft) | Empresas con .NET | Integración perfecta con ecosistema Microsoft |
| **Oracle DB** | Propietario | Banca, gobierno | Escalabilidad masiva, carísimo |

---

## 3. NoSQL — Bases de Datos No Relacionales

Las bases de datos **NoSQL (Not Only SQL)** surgieron para resolver limitaciones de las relacionales en escenarios de **alta escala, datos no estructurados o esquemas flexibles**.

### 3.1 Tipos de NoSQL

#### 3.1.1 Documentales (MongoDB, CouchDB)

Almacenan datos como **documentos JSON/BSON**. No requieren esquema fijo.

```json
// Documento de usuario en MongoDB
{
  "_id": "507f1f77bcf86cd799439011",
  "nombre": "Esteban Jaramillo",
  "email": "e12jassir@example.com",
  "pedidos": [
    {
      "restaurante": "El Corral",
      "total": 25000,
      "estado": "entregado",
      "items": ["Hamburguesa", "Papas", "Gaseosa"]
    },
    {
      "restaurante": "Telepizza",
      "total": 45000,
      "estado": "pendiente"
    }
  ],
  "metadata": {
    "ultima_conexion": "2026-09-29T21:00:00Z",
    "dispositivo": "Android"
  }
}
```

**Ventaja:** un solo documento puede contener toda la info de un usuario (sin JOINs).
**Desventaja:** datos duplicados (el nombre del restaurante se repite en cada pedido).

#### 3.1.2 Clave-Valor (Redis, DynamoDB)

Almacenan pares `clave → valor`. Extremadamente rápidos (en memoria).

```bash
# Ejemplo con Redis (desde terminal Linux)
redis-cli
SET sesion:usuario123 "token_jwt_abc123"
GET sesion:usuario123
EXPIRE sesion:usuario123 3600    # expira en 1 hora

# Caso de uso: caché de consultas frecuentes
SET cache:productos:categoria:frutas '{"data": [...], "expires": "..."}'
```

**Uso típico:** caché (acelerar respuestas), sesiones de usuario, colas de mensajes, contadores.

#### 3.1.3 Columnares (Cassandra, HBase)

Organizan datos por columnas en lugar de filas. Optimizados para escrituras masivas y consultas analíticas.

```sql
-- CQL (Cassandra Query Language) — similar a SQL
CREATE TABLE sensor_data (
    sensor_id  UUID,
    timestamp  TIMESTAMP,
    temperatura FLOAT,
    humedad    FLOAT,
    PRIMARY KEY (sensor_id, timestamp)
) WITH CLUSTERING ORDER BY (timestamp DESC);
```

**Uso típico:** series de tiempo, telemetría de IoT, análisis de logs masivos (Netflix, Instagram).

#### 3.1.4 Grafos (Neo4j, Amazon Neptune)

Almacenan nodos y relaciones entre ellos. Ideales para datos altamente conectados.

```cypher
// Consulta en Cypher (Neo4j)
// ¿Qué amigos de Esteban también pidieron en 'El Corral'?
MATCH (e:Usuario {nombre: 'Esteban'})-[:AMIGO_DE]->(amigo:Usuario)
      -[:REALIZÓ_PEDIDO]->(:Pedido)-[:EN]->(r:Restaurante {nombre: 'El Corral'})
RETURN amigo.nombre
```

**Uso típico:** redes sociales, motores de recomendación, detección de fraude, mapas de conocimiento.

---

### 3.2 SQL vs. NoSQL — Cuándo Usar Cada Uno

| Criterio | SQL (Relacional) | NoSQL |
| :--- | :--- | :--- |
| **Estructura de datos** | Bien definida y estable | Flexible, cambiante o no estructurada |
| **Integridad de datos** | Alta (ACID, claves foráneas) | Variable (eventual consistency) |
| **Escalabilidad** | Vertical (máquina más potente) | Horizontal (más máquinas) |
| **Consultas complejas** | ✅ Excelente (JOINs múltiples) | ❌ Limitadas |
| **Velocidad de escritura masiva** | 🟡 Media | ✅ Alta (Cassandra, Redis) |
| **Casos de uso** | Finanzas, ERP, e-commerce tradicional | Redes sociales, IoT, tiempo real, big data |
| **Herramientas** | PostgreSQL, MySQL, Oracle | MongoDB, Redis, Cassandra, Neo4j |

**Ejemplo real:** Rappi usa ambos:
- **PostgreSQL** para la lógica de negocio (pedidos, usuarios, pagos) — necesita transacciones ACID.
- **Redis** para caché de menús frecuentemente consultados y sesiones de usuario.
- **Cassandra/similar** para logs de tracking en tiempo real de millones de usuarios simultáneos.

---

## 4. Introducción a Redes Neuronales Artificiales

### 4.1 Contexto: ¿Qué es la Inteligencia Artificial?

```
IA (Inteligencia Artificial)
└── Machine Learning (ML) — sistemas que aprenden de datos
    └── Deep Learning — ML con redes neuronales profundas
        ├── Visión por computadora (reconocimiento de imágenes)
        ├── Procesamiento de lenguaje natural (ChatGPT, traducción)
        └── Series de tiempo (predicción de precios, demanda)
```

### 4.2 ¿Qué es una Red Neuronal Artificial?

Una red neuronal artificial (RNA) es un modelo computacional inspirado en el funcionamiento del cerebro humano. Está compuesta de **nodos (neuronas)** organizados en **capas** que procesan información.

```
     Capa de Entrada    Capas Ocultas      Capa de Salida
     (features)         (Hidden Layers)    (predicción)

Pixel 1 ─────►○─────►○─────►○────► ○
Pixel 2 ─────►○─────►○─────►○────► Gato (0.95)
Pixel 3 ─────►○─────►○─────►○────► Perro (0.04)
  ...                               Pájaro (0.01)
```

**Cada neurona:**
1. Recibe valores de entrada (`x₁, x₂, ..., xₙ`).
2. Los pondera con **pesos** (`w₁, w₂, ..., wₙ`).
3. Suma todo + **sesgo** (bias `b`).
4. Aplica una **función de activación** (e.g., ReLU, Sigmoid).
5. Produce una salida que se propaga a la siguiente capa.

```
salida = activación(w₁x₁ + w₂x₂ + ... + wₙxₙ + b)
```

### 4.3 Proceso de Entrenamiento (Sin Matemáticas Avanzadas)

El entrenamiento de una RNA es como enseñar a un niño con ejemplos:

1. **Se le muestran ejemplos** (e.g., miles de fotos de gatos y perros con su etiqueta).
2. **La red hace una predicción** (al inicio, aleatoria y mala).
3. **Se mide el error** (¿cuánto se equivocó? — función de pérdida o *loss*).
4. **Se ajustan los pesos** para reducir el error (algoritmo *backpropagation* + *gradient descent*).
5. **Se repite** millones de veces hasta que el error sea aceptablemente pequeño.

```
Datos de entrenamiento → Predicción → Error → Ajuste de pesos → (Repite)
                            ↑____________________________________________|
                                      Ciclo de entrenamiento
```

**Concepto de época (epoch):** una pasada completa por todo el conjunto de entrenamiento.

### 4.4 Tipos de Aprendizaje

| Tipo | Descripción | Ejemplo |
| :--- | :--- | :--- |
| **Supervisado** | Aprende con datos etiquetados (X → Y conocida) | Clasificar spam/no spam |
| **No supervisado** | Encuentra patrones sin etiquetas | Agrupar clientes similares (clustering) |
| **Por refuerzo** | Aprende por prueba/error con recompensas | AlphaGo, robots autónomos |

### 4.5 Aplicaciones de IA en Software Moderno

| Área | Aplicación concreta | Tecnología |
| :--- | :--- | :--- |
| **NLP** | Chatbots, traducción automática, resumen de textos | GPT-4, BERT, LLaMA |
| **Visión** | Reconocimiento facial, detección de objetos, OCR | CNN, YOLO, ResNet |
| **Recomendación** | Netflix, Spotify, TikTok — "qué ver/escuchar después" | Collaborative Filtering |
| **Generación de código** | GitHub Copilot, ChatGPT, Gemini | LLMs (Large Language Models) |
| **Detección de fraude** | Bloqueo automático de transacciones sospechosas | Redes LSTM, Autoencoders |
| **Diagnóstico médico** | Detección de tumores en radiografías | CNN sobre imágenes médicas |
| **Conducción autónoma** | Tesla Autopilot, Waymo | Fusión sensorial + DL |

---

## 5. Tendencias Actuales del Sector

### 5.1 Cloud Computing y Serverless

- **Cloud:** infraestructura bajo demanda (AWS, GCP, Azure). Sin inversión en hardware propio.
- **Serverless (FaaS):** el desarrollador despliega funciones, no servidores. El proveedor gestiona el escalado.

```bash
# Ejemplo: función serverless en AWS Lambda (Python)
def lambda_handler(event, context):
    nombre = event.get('nombre', 'Mundo')
    return {"statusCode": 200, "body": f"Hola, {nombre}!"}
# Se escala de 0 a millones de invocaciones automáticamente
```

### 5.2 DevOps y CI/CD

**DevOps** integra los equipos de desarrollo y operaciones para acelerar la entrega de software:

```
Commit de código → Tests automáticos → Build → Deploy → Monitoreo
(CI: Integración Continua)          (CD: Despliegue Continuo)
```

Herramientas: GitHub Actions, GitLab CI, Jenkins, Docker, Kubernetes.

### 5.3 Microservicios

En lugar de una aplicación monolítica, el sistema se divide en **servicios independientes** que se comunican por APIs.

```
Monolito:                   Microservicios:
┌──────────────────┐        ┌─────────────┐ ┌─────────────┐
│  Usuarios        │        │ Svc Usuarios │ │ Svc Pagos   │
│  Pagos           │        └──────┬──────┘ └──────┬──────┘
│  Inventario      │               │ API            │ API
│  Notificaciones  │        ┌──────▼──────┐ ┌──────▼──────┐
└──────────────────┘        │ Svc Inventario│ │ Svc Notif. │
Un solo proceso             └─────────────┘ └─────────────┘
                            Procesos independientes
```

### 5.4 Resumen de Tendencias Clave 2025-2026

| Tendencia | Descripción | Impacto en IS |
| :--- | :--- | :--- |
| **IA Generativa** | LLMs (GPT, Gemini, LLaMA) para generar código, texto, imágenes | El ingeniero pasa de escribir código a revisar y orquestar IA |
| **Edge Computing** | Procesamiento cerca del origen de datos (vs. cloud centralizado) | Crucial para IoT, VR, vehículos autónomos |
| **Web3 / Blockchain** | Contratos inteligentes, datos descentralizados | Nuevos paradigmas de confianza sin intermediarios |
| **Quantum Computing** | Computación cuántica — rompe criptografía RSA actual | Impacto en seguridad a largo plazo |
| **Low-code / No-code** | Plataformas que permiten construir apps sin código | Democratización del desarrollo |
| **Ciberseguridad** | Superficie de ataque creciente con IoT, cloud, móviles | IS debe integrar seguridad desde el diseño (DevSecOps) |

---

## 6. Errores Comunes

| Error | Realidad |
| :--- | :--- |
| "NoSQL es mejor que SQL" | Son herramientas para diferentes problemas. Un error común es usar MongoDB para datos altamente relacionados. |
| "AI/ML es solo para científicos de datos" | Los IS deben integrar APIs de ML en sus sistemas, gestionar pipelines de datos y comprender los límites de los modelos. |
| "`SELECT *` siempre" | En producción, seleccionar todas las columnas en tablas grandes degrada el rendimiento. Selecciona solo lo necesario. |
| "Las transacciones son opcionales" | Operaciones financieras o de inventario sin transacciones producen inconsistencias imposibles de auditar. |
| "El modelo de ML resuelve todo solo" | Los modelos aprenden patrones de datos históricos. Si los datos tienen sesgos o son de mala calidad, el modelo falla (GIGO: Garbage In, Garbage Out). |

---

## 7. Referencia Rápida

```sql
-- SQL básico de referencia
SELECT col1, col2 FROM tabla WHERE condición ORDER BY col1 LIMIT 10;
INSERT INTO tabla (col1, col2) VALUES (val1, val2);
UPDATE tabla SET col1 = val1 WHERE condición;
DELETE FROM tabla WHERE condición;  -- ¡SIEMPRE CON WHERE!

-- Aggregate functions
COUNT(*) | SUM(col) | AVG(col) | MIN(col) | MAX(col)
-- Agrupación
GROUP BY col HAVING condición_sobre_agregado

-- JOINs
INNER JOIN → intersección | LEFT JOIN → todos de la izq.

-- Transacciones
START TRANSACTION; ... COMMIT; | ROLLBACK;
```

```
NoSQL tipos:
  Documentos: MongoDB  → JSON flexible, sin esquema fijo
  Clave-Valor: Redis   → caché, sesiones, rapidísimo
  Columnar: Cassandra  → IoT, series de tiempo, big data
  Grafos: Neo4j        → redes sociales, recomendaciones

RNA (conceptual):
  Capas: Entrada → Ocultas → Salida
  Entrenamiento: ejemplos → predicción → error → ajuste → repite
  Tipos: Supervisado | No supervisado | Refuerzo
```

---

## 8. Recursos Externos Específicos

### Videos / Canales
- **Midudev** (YouTube, español): [SQL en 1 hora](https://www.youtube.com/c/midudev) — SQL completo con ejemplos prácticos en español.
- **3Blue1Brown** (YouTube): [`Neural Networks`](https://www.youtube.com/watch?v=aircAruvnKk) — Serie de 4 videos explicando redes neuronales con visualizaciones geométricas sin matemáticas avanzadas. **Imprescindible.**
- **Fireship** (YouTube): [`SQL vs NoSQL in 100 Seconds`](https://www.youtube.com/watch?v=W2Z7fbCLSTw) — Comparativa rápida y concreta.

### Libros
- **Pressman & Maxim — Ingeniería de Software (9.ª ed.):**
  - Cap. 24: *Gestión de Configuración del Software* — Incluye bases de datos de configuración.
- **Ramakrishnan, R. & Gehrke, J. — Database Management Systems (3.ª ed.):**
  - Cap. 1: *Introducción* — Motivación para usar SGBD.
  - Cap. 4 y 5: *Álgebra relacional y SQL*.

### Sitios web
- [SQLBolt](https://sqlbolt.com/) — Tutoriales interactivos de SQL gratis, directamente en el navegador.
- [MongoDB University](https://learn.mongodb.com/) — Cursos gratuitos oficiales de MongoDB.
- [fast.ai](https://www.fast.ai/) — Curso gratuito de Deep Learning para desarrolladores de software (sin matemáticas avanzadas).
- [Kaggle Learn](https://www.kaggle.com/learn) — Cursos cortos gratuitos de SQL, ML y Python con notebooks ejecutables.

---

## 9. Preguntas de Active Recall

1. ¿Por qué son preferibles las bases de datos sobre los archivos CSV para datos empresariales? Da 3 razones.
2. Escribe una consulta SQL que obtenga el nombre y el total de pedidos de los 5 clientes que más gastaron.
3. ¿Qué significa ACID? Da un ejemplo de por qué cada propiedad importa en un sistema bancario.
4. ¿Cuáles son los 4 tipos de NoSQL? Describe el caso de uso ideal para cada uno.
5. ¿En qué escenario elegirías MongoDB sobre PostgreSQL? ¿Y Redis sobre MongoDB?
6. Explica en términos simples cómo aprende una red neuronal. Sin usar ecuaciones.
7. ¿Qué diferencia hay entre aprendizaje supervisado y no supervisado? Da un ejemplo de aplicación de cada uno.
8. Nombra 3 tendencias tecnológicas actuales y explica cómo cada una impacta el rol del ingeniero de software.
