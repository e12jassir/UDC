# Apuntes — Unidad 2: Arquitectura de Computadoras e Internet

> **Asignatura:** Introducción a la Ingeniería de Software · `IX24014-A1`  
> **Docente:** Jhon Carlos Arrieta Arrieta  
> **Última actualización:** 2026-09-29

---

## 1. Arquitectura de Computadoras — Fundamentos

### 1.1 Arquitectura Von Neumann

Propuesta por John von Neumann en 1945, describe el modelo base de prácticamente toda computadora moderna. El principio central es el **programa almacenado**: las instrucciones y los datos coexisten en la misma memoria.

```
┌──────────────────────────────────────────────────────┐
│                  COMPUTADORA                         │
│  ┌─────────────┐        ┌──────────────────────────┐ │
│  │   CPU (ALU  │◄──────►│    MEMORIA PRINCIPAL      │ │
│  │  + Unidad  │        │  (Instrucciones + Datos)  │ │
│  │  de Control│        └──────────────────────────┘ │
│  └────────┬───┘                                      │
│           │                                          │
│  ┌────────▼───────────────────────────────────────┐  │
│  │        DISPOSITIVOS E/S (Teclado, Pantalla...)  │  │
│  └────────────────────────────────────────────────┘  │
└──────────────────────────────────────────────────────┘
```

**Componentes del modelo:**

| Componente | Función | Ejemplo físico actual |
| :--- | :--- | :--- |
| **CPU (Procesador)** | Ejecuta instrucciones aritméticas y lógicas | Intel Core i9, AMD Ryzen 9 |
| **ALU** (Unidad Aritmético-Lógica) | Suma, resta, comparaciones | Parte interna del procesador |
| **Unidad de Control** | Decodifica y coordina la ejecución de instrucciones | Parte interna del procesador |
| **Registros** | Memoria ultrarrápida dentro de la CPU | RAX, RBX (x86-64) |
| **Memoria Principal (RAM)** | Almacena datos e instrucciones en uso | DDR5 32 GB |
| **Almacenamiento** | Persiste datos entre sesiones | SSD NVMe, HDD |
| **Dispositivos E/S** | Comunicación con el exterior | Teclado, pantalla, GPU |

**El cuello de botella de Von Neumann:** CPU y memoria comparten el mismo bus de datos. Si la CPU es mucho más rápida que la RAM (lo cual es el caso hoy), el procesador espera inactivo. Por eso existen las **cachés L1, L2, L3**.

### 1.2 Jerarquía de Memoria

```
Registros CPU   → ~1 ns    (bytes)
Cache L1        → ~5 ns    (KB)
Cache L2        → ~10 ns   (MB)
Cache L3        → ~30 ns   (MB)
RAM             → ~60 ns   (GB)
SSD (NVMe)      → ~0.1 ms  (TB)
HDD             → ~5-10 ms (TB)
```

> **Regla de oro:** Cuanto más rápido, más pequeño y más caro por GB. La jerarquía de memoria existe para ocultar esta diferencia de velocidad al programador.

---

## 2. RISC vs. CISC — Filosofías de Diseño de Procesadores

### CISC (Complex Instruction Set Computer)

- **Filosofía:** pocas instrucciones de alto nivel que hacen mucho trabajo cada una.
- **Ejemplo:** `MULTIPLY AX, [BX]` — carga de memoria + multiplicación en una sola instrucción.
- **Arquitectura representativa:** x86, x86-64 (Intel, AMD) — el que usa tu PC con Linux.
- **Ventaja:** programas más cortos, el hardware oculta la complejidad.
- **Desventaja:** transistores dedicados a instrucciones complejas poco usadas, calor, consumo.

### RISC (Reduced Instruction Set Computer)

- **Filosofía:** muchas instrucciones simples que el compilador combina para lograr operaciones complejas.
- **Ejemplo:** ARM necesita 3 instrucciones (cargar, multiplicar, guardar) para lo que CISC hace en 1.
- **Arquitecturas representativas:** ARM (smartphones, Raspberry Pi, Apple Silicon M1/M2/M3), RISC-V (emergente, open-source).
- **Ventaja:** menor consumo de energía, mejor disipación, más barato de fabricar.
- **Desventaja:** mayor complejidad del compilador, programas objeto más largos.

| Característica | CISC (x86) | RISC (ARM) |
| :--- | :--- | :--- |
| Instrucciones | Pocas, complejas | Muchas, simples |
| Ciclos por instrucción | Variable (1–20+) | Generalmente 1 |
| Longitud de instrucción | Variable | Fija (32 bits) |
| Registros | Pocos (8 en modo 32-bit) | Muchos (16-32) |
| Uso típico | Computadoras de escritorio/servidores | Smartphones, tablets, IoT |
| Consumo energético | Alto | Bajo |
| Ejemplo moderno | AMD Ryzen 9 9900X | Apple M3, Snapdragon 8 Gen 3 |

> **Curiosidad Linux:** En tu máquina con Linux probablemente usas x86-64 (CISC). Si compilas algo con `gcc`, el compilador genera instrucciones x86-64 optimizadas. Si usaras una Raspberry Pi, el mismo código se compilaría para ARM (RISC).

---

## 3. Cómo Funciona Internet — De la Petición al Navegador

Internet es una **red de redes** que conecta millones de dispositivos usando protocolos estandarizados. Vamos a seguir el viaje de una petición desde tu navegador hasta el servidor y de vuelta.

### 3.1 El Modelo en Capas — TCP/IP

El modelo TCP/IP organiza los protocolos de red en 4 capas (o 5 en la versión extendida):

```
┌─────────────────────────────────┐
│ 4. Aplicación  (HTTP, DNS, SMTP)│  ← Tu navegador habla aquí
├─────────────────────────────────┤
│ 3. Transporte  (TCP, UDP)       │  ← Divide datos en segmentos
├─────────────────────────────────┤
│ 2. Internet    (IP)             │  ← Dirige paquetes por la red
├─────────────────────────────────┤
│ 1. Acceso a Red (Ethernet, WiFi)│  ← Bits por el cable/aire
└─────────────────────────────────┘
```

**Analogía postal:** Imagina que envías una caja grande a través del correo.
- **Capa de Aplicación:** escribes la carta (contenido).
- **Capa de Transporte:** el correo divide la caja en paquetes más pequeños y les pone número de orden.
- **Capa de Internet:** cada paquete lleva la dirección de destino (IP) y puede tomar rutas distintas.
- **Capa de Red:** el correo físico la lleva por carretera, avión o barco.

---

### 3.2 Protocolo IP — Direccionamiento

Cada dispositivo en Internet tiene una **dirección IP** (Internet Protocol). Es como la dirección postal de tu computadora.

- **IPv4:** 32 bits → `192.168.1.1` (formato decimal con puntos). ~4.300 millones de direcciones (ya agotadas).
- **IPv6:** 128 bits → `2001:db8::1` (hexadecimal). ~340 undecillones de direcciones.

**IP pública vs. IP privada:**
- **Privada:** Solo existe dentro de tu red local (e.g., `192.168.x.x`). Tu router la asigna.
- **Pública:** Visible en Internet. Tu proveedor de internet (Claro, ETB, Tigo) la asigna a tu router.

```bash
# En Linux: ver tu IP local
ip addr show
# o
hostname -I

# Ver tu IP pública
curl ifconfig.me
```

---

### 3.3 TCP vs. UDP

| Característica | TCP | UDP |
| :--- | :--- | :--- |
| **Confiabilidad** | ✅ Garantiza entrega y orden | ❌ No garantiza nada |
| **Velocidad** | 🟡 Más lento (handshake + ACKs) | ✅ Más rápido |
| **Conexión** | Orientado a conexión (3-way handshake) | Sin conexión |
| **Uso típico** | Web (HTTP/HTTPS), correo, descarga de archivos | Streaming de video, videojuegos en línea, DNS, VoIP |

**El 3-way handshake de TCP:**
```
Cliente                    Servidor
  │──── SYN ─────────────►│   "¿Puedo conectarme?"
  │◄─── SYN-ACK ──────────│   "Sí, adelante."
  │──── ACK ─────────────►│   "Gracias, inicio conexión."
  │ [Intercambio de datos] │
  │──── FIN ─────────────►│   "Terminé."
```

---

### 3.4 DNS — El Sistema de Nombres de Dominio

**Problema:** los humanos recordamos `google.com`, pero las computadoras se comunican con IPs como `142.250.184.206`. El DNS actúa como la guía telefónica de Internet.

**Jerarquía del DNS:**
```
google.com.
│
├─ . (Root)
├─ .com (TLD — Top Level Domain)
├─ google (Dominio de segundo nivel)
└─ www (Subdominio)
```

**Proceso de resolución DNS (paso a paso):**

```
Tu navegador               DNS Resolver          DNS Raíz       DNS .com      DNS Google
    │                      (ISP / 8.8.8.8)
    │──"¿IP de google.com?"──►│
    │                         │──"¿Quién maneja .com?"──►│
    │                         │◄──"ns1.google.com"────────│
    │                         │──────────────────────────────────►│
    │                         │◄──────────────"216.58.x.x"────────│
    │◄─"216.58.x.x"──────────│
    │──────────────────────────────────────────── TCP/HTTPS ───────►│
```

```bash
# En Linux: consultar DNS manualmente
dig google.com
nslookup google.com

# Ver qué DNS usa tu sistema
cat /etc/resolv.conf
```

**DNS público común:**
- `8.8.8.8` y `8.8.4.4` — Google Public DNS
- `1.1.1.1` — Cloudflare (más privado)
- `9.9.9.9` — Quad9 (con filtro de malware)

---

### 3.5 HTTP y HTTPS — El Protocolo de la Web

**HTTP (HyperText Transfer Protocol)** es el lenguaje que usan navegadores y servidores para comunicarse. **HTTPS** agrega una capa de cifrado (TLS/SSL).

**Estructura de una petición HTTP:**
```http
GET /api/productos?categoria=frutas HTTP/1.1
Host: www.tienda.com
User-Agent: Mozilla/5.0
Accept: application/json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9...
```

**Estructura de una respuesta HTTP:**
```http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 248

{"productos": [{"id": 1, "nombre": "Mango", "precio": 3500}]}
```

**Métodos HTTP y su significado:**

| Método | Acción | Ejemplo de uso |
| :--- | :--- | :--- |
| `GET` | Leer recurso (sin modificar) | Ver perfil de usuario |
| `POST` | Crear nuevo recurso | Registrar nuevo usuario |
| `PUT` | Actualizar recurso completo | Editar perfil completo |
| `PATCH` | Actualizar campos específicos | Cambiar solo el avatar |
| `DELETE` | Eliminar recurso | Borrar una publicación |

**Códigos de estado HTTP:**

| Código | Significado | Cuándo ocurre |
| :--- | :--- | :--- |
| `200 OK` | Todo bien | Solicitud exitosa |
| `201 Created` | Recurso creado | POST exitoso |
| `301/302` | Redirección | URL cambió |
| `400 Bad Request` | El cliente envió mal la petición | Campos faltantes |
| `401 Unauthorized` | No autenticado | Token inválido |
| `403 Forbidden` | Autenticado pero sin permisos | Usuario sin acceso admin |
| `404 Not Found` | Recurso no existe | URL equivocada |
| `500 Internal Server Error` | Error en el servidor | Bug en el backend |

**HTTPS y TLS:**
- TLS (Transport Layer Security) cifra la comunicación entre cliente y servidor.
- Usa **criptografía asimétrica** (clave pública/privada) para intercambiar una **clave simétrica** de sesión.
- Visible en el navegador: candado 🔒 + `https://`

```bash
# En Linux: probar conexión HTTPS
curl -v https://www.google.com 2>&1 | head -40
# Ver el certificado TLS de un sitio
openssl s_client -connect google.com:443 -brief
```

---

### 3.6 El Viaje Completo de una Petición Web

Cuando escribes `https://www.rappi.com.co` y presionas Enter:

```
1. Navegador → busca "rappi.com.co" en caché DNS local → no encontrado
2. Navegador → consulta al DNS Resolver (8.8.8.8)
3. DNS Resolver → consulta al DNS raíz → .co → rappi.com.co → IP: 34.123.x.x
4. Navegador → TCP 3-way handshake con 34.123.x.x:443
5. TLS handshake → establece canal cifrado
6. Navegador → GET / HTTP/1.1 (por el canal cifrado)
7. Servidor → responde con HTML + CSS + JS
8. Navegador → parsea HTML, solicita más recursos (imágenes, scripts)
9. Página renderizada en pantalla
```

Tiempo total típico: **< 500 ms** para una conexión rápida.

---

## 4. Errores Comunes

| Error conceptual | Realidad |
| :--- | :--- |
| "Internet es lo mismo que la web" | Internet es la infraestructura. La web (HTTP/HTTPS) es un servicio que corre sobre ella. También corren correo, SSH, FTP, etc. |
| "Mi IP es `192.168.1.x`" | Esa es tu IP privada local. Tu IP pública es la que ve el servidor al que te conectas. |
| "DNS solo traduce nombres a IPs" | También gestiona mail (registros MX), alias (CNAME), verificación de dominio (TXT), etc. |
| "HTTPS hace que el sitio sea seguro" | HTTPS solo cifra la comunicación. Un sitio puede tener HTTPS y aun así ser malicioso o tener vulnerabilidades. |
| "TCP siempre es mejor que UDP" | UDP es preferible cuando la velocidad importa más que la exactitud (streaming, juegos en tiempo real). |

---

## 5. Referencia Rápida

```
RISC (ARM): instrucciones simples, bajo consumo → móviles, IoT
CISC (x86): instrucciones complejas, alto rendimiento → PC, servidores

TCP/IP capas: Aplicación | Transporte | Internet | Acceso a Red
TCP: confiable, ordenado, lento | UDP: rápido, sin garantías

DNS: dominio → IP (jerarquía: Raíz → TLD → Dominio → Subdominio)
HTTP métodos: GET(leer) POST(crear) PUT(actualizar) DELETE(borrar)
HTTPS = HTTP + TLS (cifrado)

Comandos Linux útiles:
  ip addr show          → IP local
  curl ifconfig.me      → IP pública
  dig dominio.com       → consulta DNS
  curl -v https://url   → ver headers HTTP
```

---

## 6. Recursos Externos Específicos

### Videos / Canales
- **Computerphile** (YouTube): [`How Does the Internet Work?`](https://www.youtube.com/watch?v=7_LPdttKXPc) — Explicación visual y profunda del funcionamiento de internet, nivel universitario.
- **ByteByteGo** (YouTube): [`How does HTTPS work?`](https://www.youtube.com/watch?v=AlE5X1NlHgg) — Animaciones claras sobre TLS y HTTPS.
- **Dot CSV** (YouTube, español): Canal en español sobre arquitecturas y tecnología — buscar "cómo funciona internet".

### Libros
- **Pressman & Maxim — Ingeniería de Software (9.ª ed.):**
  - Cap. 28: *Ingeniería de software de sistemas web* — Cómo se construyen apps web sobre esta infraestructura.
- **Tanenbaum, A. S. — Redes de Computadoras (5.ª ed.):**
  - Cap. 1: *Introducción* — Historia y estructura de internet.
  - Cap. 7: *Capa de Aplicación* — HTTP, DNS, correo.

### Sitios web
- [howdns.works](https://howdns.works/) — Explicación visual de DNS con cómics, gratuito.
- [MDN Web Docs — HTTP](https://developer.mozilla.org/es/docs/Web/HTTP/Overview) — Referencia completa de HTTP en español.
- [Cloudflare Learning Center](https://www.cloudflare.com/es-es/learning/) — Artículos técnicos sobre DNS, TLS, DDoS, etc.

---

## 7. Preguntas de Active Recall

1. Dibuja el modelo Von Neumann de memoria. ¿Cuál es el cuello de botella y cómo se mitiga?
2. Explica la diferencia entre RISC y CISC. ¿Por qué los smartphones usan ARM y no x86?
3. ¿Cuáles son las 4 capas del modelo TCP/IP? Da un ejemplo de protocolo en cada capa.
4. ¿Qué diferencia hay entre TCP y UDP? Da un ejemplo de aplicación para cada uno.
5. Describe el proceso de resolución DNS desde que escribes una URL hasta obtener la IP.
6. ¿Qué hace cada método HTTP (GET, POST, PUT, DELETE)? Da un ejemplo con una app de tareas.
7. ¿Qué agrega HTTPS sobre HTTP? ¿Garantiza que el sitio es seguro? Explica.
8. Traza el camino completo de una petición a `https://moodle.unicartagena.edu.co` desde tu computadora con Linux.
