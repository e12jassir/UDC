# 🎬 Mapa Visual y Hoja de Ruta — Sustentación Ing. de Software U1

```mermaid
flowchart LR
    subgraph BLOQUE1["1. INTRO & DIFERENCIA (40s)"]
        direction TB
        A1["👋 Saludo & Nombre<br>Esteban Marrugo (7502620036)"] --> A2["👨‍💻 Programador vs Ingeniero"]
        A2 --> A3["💡 EJEMPLO SIMA UDC<br>Programador: boton guardar<br>Ingeniero: 10.000 usuarios sin colapso"]
        A3 --> A4["⚠️ Crisis del Software 1968<br>+60% costo en mantenimiento"]
    end

    subgraph BLOQUE2["2. METODOLOGÍAS (45s)"]
        direction TB
        B1["🏛️ Cascada (Tradicional)"] --> B2["🏃‍♂️ Scrum / Ágiles"]
        B1 -.->|"Tiro en el pie si cambia el cliente"| B3["💡 EJEMPLO WHATSAPP"]
        B2 -->|"Sprints de 2 semanas"| B3
        B3 --> B4["Cascada: WhatsApp completo en 2009<br>Scrum: Texto ➔ Notas ➔ Llamadas"]
    end

    subgraph BLOQUE3["3. ARQUITECTURA (45s)"]
        direction TB
        C1["🎯 Alta Cohesión"] --> C2["💡 EJEMPLO APPS<br>Calculadora solo calcula<br>Camara solo toma fotos"]
        C3["🔗 Bajo Acoplamiento"] --> C4["💡 EJEMPLO BICI / AUDÍFONOS<br>Cambias el pedal o el audifono<br>sin desarmar la bici ni la laptop"]
    end

    subgraph BLOQUE4["4. ÉTICA & CIERRE (20s)"]
        direction TB
        D1["🛡️ Responsabilidad Ética"] --> D2["Salud, finanzas y transporte"]
        D2 --> D3["Un bug en produccion pone<br>en riesgo vidas y privacidad"]
        D3 --> D4["🙏 Cierre y Agradecimiento"]
    end

    BLOQUE1 --> BLOQUE2 --> BLOQUE3 --> BLOQUE4
```

---

## 📌 Guía Rápida de Palabras Clave (Para mirar de reojo)

| Bloque | Qué decir (Disparador) | Ejemplo Clave |
| :--- | :--- | :--- |
| **1. Programador vs. Ingeniero** | *El programador traduce código; el ingeniero diseña estabilidad a futuro.* | **SIMA UDC:** Que 10.000 estudiantes entren a las 11:59 p.m. sin tirar el servidor. |
| **2. Cascada vs. Scrum** | *Cascada es fijo (plano de ing. civil); Scrum es ágil por Sprints.* | **WhatsApp:** Lanzar primero texto y luego sumar notas de voz y llamadas. |
| **3. Cohesión vs. Acoplamiento** | *Cohesión = Cada módulo una sola tarea.<br>Acoplamiento = Módulos independientes.* | **Bicicleta / Apps:** Cambiar los pedales sin desarmar la bici / Calculadora solo calcula. |
| **4. Ética & Cierre** | *Rigor técnico porque el software controla datos reales.* | *Salud, banca y privacidad ciudadana.* |

---

> [!TIP]
> **Consejo para grabar:** Pon este diagrama arriba en tu pantalla dividida justo debajo de la webcam. Al mirar los bloques, no estás leyendo, estás siguiendo el mapa mental.
