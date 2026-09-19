# 🗺️ Mapa Conceptual de Arquitectura: Ecosistema Rappi y Fundamentos de Computación

> Este mapa conceptual esquematiza las cinco dimensiones evaluadas en la Unidad 1 de **Introducción a la Ingeniería de Software** en la Universidad de Cartagena. Se renderiza de forma nativa en **Obsidian** y en cualquier visor de Markdown compatible con Mermaid.

---

```mermaid
flowchart TD
    %% Estilos Generales
    classDef core fill:#ff441f,stroke:#fff,stroke-width:2px,color:#fff;
    classDef sw fill:#1f6feb,stroke:#58a6ff,stroke-width:2px,color:#fff;
    classDef ind fill:#8957e5,stroke:#bc8cff,stroke-width:2px,color:#fff;
    classDef hw fill:#238636,stroke:#3fb950,stroke-width:2px,color:#fff;
    classDef per fill:#d29922,stroke:#f0883e,stroke-width:2px,color:#fff;
    classDef evo fill:#da3633,stroke:#f85149,stroke-width:2px,color:#fff;

    %% NODO CENTRAL
    RAPPI["Plataforma Multilateral Rappi<br/><i>(On-Demand Quick-Commerce)</i>"]:::core

    %% SUBGRAFO 1: INGENIERÍA DE SOFTWARE
    subgraph EJE_1["⚙️ Eje 1: Ingeniería de Software"]
        direction TB
        MICRO["Arquitectura de Microservicios<br/><i>(Desacoplamiento Operativo)</i>"]:::sw
        COHESION["Alta Cohesión & Bajo Acoplamiento<br/><i>(Aislamiento de Fallos)</i>"]:::sw
        CIRCUIT["Patrón Circuit Breaker<br/><i>(Degradación Elegante)</i>"]:::sw
        CAP["Teorema CAP<br/><i>(Disponibilidad en Catálogo vs ACID en Pagos)</i>"]:::sw
        SQUADS["Células Ágiles (Squads)<br/><i>(Móvil, Backend, SRE, ML)</i>"]:::sw
        CRISIS["Mitigación Crisis del Software<br/><i>(Mantenibilidad > 60% ciclo de vida)</i>"]:::sw

        MICRO --> COHESION
        MICRO --> CIRCUIT
        MICRO --> CAP
        MICRO --> SQUADS
        MICRO --> CRISIS
    end

    %% SUBGRAFO 2: INDUSTRIA DEL SOFTWARE
    subgraph EJE_2["💼 Eje 2: Industria del Software"]
        direction TB
        SECTOR["Sector de Convergencia<br/><i>(Quick-Commerce + Gig Economy + Fintech)</i>"]:::ind
        MONETIZACION["Modelo de Monetización Multicanal<br/><i>(Comisiones + Tarifas + Prime + Ads + Fintech)</i>"]:::ind
        EVENT["Arquitectura Event-Driven<br/><i>(Streaming de Eventos con Apache Kafka)</i>"]:::ind
        ELASTIC["Computación Elástica<br/><i>(Autoescalado en AWS / GCP)</i>"]:::ind

        SECTOR --> MONETIZACION
        SECTOR --> EVENT
        SECTOR --> ELASTIC
    end

    %% SUBGRAFO 3: ARQUITECTURA DE COMPUTACIÓN
    subgraph EJE_3["🖥️ Eje 3: Arquitectura de Computación"]
        direction TB
        ARM["SoC Móvil ARM (big.LITTLE)<br/><i>(Núcleos Eficientes para Tracking GPS)</i>"]:::hw
        GPU["GPU Móvil<br/><i>(Renderizado Vectorial de Mapas 60 FPS)</i>"]:::hw
        CACHE["Jerarquía de Memoria Local<br/><i>(Caché L1/L2/L3 en Nanosegundos)</i>"]:::hw
        REDIS["Clúster en Memoria RAM (Redis)<br/><i>(Telemetría en Vivo de Flota: 50-100 ns)</i>"]:::hw
        SERVIDORES["Servidores Cloud (x86 & AWS Graviton)<br/><i>(Concurrencia Masiva y Ruteo Óptimo)</i>"]:::hw

        ARM --> CACHE
        GPU --> CACHE
        SERVIDORES --> REDIS
    end

    %% SUBGRAFO 4: PERIFÉRICOS Y ENTRADA
    subgraph EJE_4["📡 Eje 4: Periféricos y Sistemas de Entrada"]
        direction TB
        AGPS["Sensor A-GPS / GNSS<br/><i>(Ondas Electromagnéticas a Coordenadas Lat/Long)</i>"]:::per
        TOUCH["Pantalla Táctil Capacitiva<br/><i>(Distorsión Electrostática: Toque y Gestos)</i>"]:::per
        CMOS["Cámara CMOS & Biometría Facial<br/><i>(Prueba de Entrega & Autenticación)</i>"]:::per
        HAPTIC["Motor Háptico de Salida<br/><i>(Vibración Sensorial para Domiciliario en Moto)</i>"]:::per
        CONTEXTUAL["Captura Contextual Automatizada<br/><i>(Batería, Señal de Red, Ubicación Pasiva)</i>"]:::per

        AGPS --> CONTEXTUAL
        TOUCH --> CONTEXTUAL
    end

    %% SUBGRAFO 5: EVOLUCIÓN HISTÓRICA
    subgraph EJE_5["⏳ Eje 5: Evolución Tecnológica"]
        direction TB
        ANALOG["Hace 30 Años (1995)<br/><i>(Teléfono Fijo, Libreta Papel Carbón, Guía Roji, Efectivo)</i>"]:::evo
        CONVERGENCIA["Motores del Cambio<br/><i>(Smartphone + 4G/5G + Nube Elástica + Pasarelas API)</i>"]:::evo
        FUTURO["Próxima Década (2026-2035)<br/><i>(Drones Autónomos, LiDAR, Edge AI, Logística Predictiva)</i>"]:::evo

        ANALOG --> CONVERGENCIA
        CONVERGENCIA --> FUTURO
    end

    %% CONEXIONES DE RAPPI CON CADA EJE
    RAPPI ==> EJE_1
    RAPPI ==> EJE_2
    RAPPI ==> EJE_3
    RAPPI ==> EJE_4
    RAPPI ==> EJE_5

    %% CONEXIONES TRANSVERSALES CLAVE
    AGPS -. "Telemetría Continua" .-> ARM
    ARM -. "Peticiones HTTPS / WebSockets" .-> SERVIDORES
    REDIS -. "Copia de Seguridad Persistente" .-> ELASTIC
    EVENT -. "Desacoplamiento de Órdenes" .-> MICRO
    FUTURO -. "Inferencia en el Dispositivo" .-> ARM
```

---

## 🧭 ¿Cómo visualizar e interactuar con este mapa?

1. **En Obsidian (Modo Lectura / Vista Previa):**
   - Abre este archivo directamente en Obsidian. La plataforma compila Mermaid de forma nativa, permitiéndote hacer zoom, resaltar nodos y seguir las líneas de conexión.
2. **En Obsidian Canvas (Lienzo Infinito):**
   - En tu carpeta de entregables tienes el archivo [`Mapa_Conceptual_Rappi.canvas`](file:///home/e12jassir/Documentos/UDC/Introducci%C3%B3n%20a%20la%20Ingenier%C3%ADa%20de%20Software/Entregables/Mapa_Conceptual_Rappi.canvas). Al abrirlo en Obsidian verás un tablero interactivo con fichas arrastrables, colores y flechas visuales.
3. **En Formato Imagen Vectorial (SVG):**
   - En [`Mapa_Conceptual_Rappi.svg`](file:///home/e12jassir/Documentos/UDC/Introducci%C3%B3n%20a%20la%20Ingenier%C3%ADa%20de%20Software/Entregables/Mapa_Conceptual_Rappi.svg) tienes el gráfico vectorial renderizado en alta definición, listo para exportar a PDF o pegar en diapositivas.
