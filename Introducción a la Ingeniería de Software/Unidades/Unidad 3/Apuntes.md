# Apuntes — Unidad 3: Sistemas Operativos y Redes

> **Asignatura:** Introducción a la Ingeniería de Software · `IX24014-A1`  
> **Docente:** Jhon Carlos Arrieta Arrieta  
> **Última actualización:** 2026-09-29  
> **Entregable pendiente:** Análisis de metadatos y cabeceras de archivos — 30 Oct 2026

---

## 1. ¿Qué es un Sistema Operativo?

Un **Sistema Operativo (SO)** es el software que actúa como intermediario entre el hardware y los programas de usuario. Sin SO, cada programa tendría que comunicarse directamente con el hardware — algo inviable cuando hay múltiples programas y dispositivos.

### Funciones principales del SO

| Función | Descripción | Ejemplo concreto (Linux) |
| :--- | :--- | :--- |
| **Gestión de procesos** | Crear, pausar, terminar y planificar procesos | `ps aux`, `kill`, `top` |
| **Gestión de memoria** | Asignar RAM a procesos, evitar colisiones | Memoria virtual, swap |
| **Sistema de archivos** | Organizar datos en disco, permisos, rutas | ext4, btrfs, `/proc`, `/sys` |
| **Gestión de E/S** | Controlar teclado, disco, red, pantalla | Drivers de dispositivos |
| **Seguridad y permisos** | Usuarios, grupos, control de acceso | `chmod`, `chown`, `/etc/passwd` |
| **Interfaz de usuario** | CLI o GUI para interactuar | Bash, GNOME, KDE |
| **Gestión de red** | Configurar interfaces, DNS, firewall | `ip`, `NetworkManager`, `iptables` |

### El núcleo (Kernel)

El **kernel** es el componente central del SO que corre con privilegios máximos (modo kernel). Todo lo demás (aplicaciones, shell) corre en modo usuario.

```
┌──────────────────────────────────────┐
│  Modo Usuario: Aplicaciones, Shell   │
├──────────────────────────────────────┤
│  Modo Kernel: Kernel del SO          │
│  (Gestión de procesos, memoria, E/S) │
├──────────────────────────────────────┤
│  Hardware (CPU, RAM, Disco, Red)     │
└──────────────────────────────────────┘
```

---

## 2. Tipos de Sistemas Operativos y Comparativa

### 2.1 Windows

- **Núcleo:** Windows NT (kernel híbrido).
- **Uso principal:** escritorios corporativos, gaming, software especializado (AutoCAD, Adobe).
- **Sistema de archivos:** NTFS (con journaling, permisos ACL).
- **Ventajas:** amplia compatibilidad de software comercial, soporte de fabricantes.
- **Desventajas:** mayor superficie de ataque (malware), licencia de pago, menor control sobre el sistema.
- **Versiones relevantes:** Windows 10 (aún dominante en empresas), Windows 11.

### 2.2 Linux

- **Núcleo:** Linux (monolítico modular, open-source — Linus Torvalds, 1991).
- **Distribuciones populares:** Ubuntu, Fedora, Arch Linux, Debian, RHEL (empresarial).
- **Uso principal:** servidores web (>96% del mercado), desarrollo de software, investigación, IoT.
- **Sistema de archivos:** ext4, btrfs, XFS.
- **Ventajas:** gratuito y open-source, altamente configurable, seguro, base de todos los servidores modernos.
- **Desventajas:** curva de aprendizaje, menor soporte de software comercial de escritorio.

> **Relevancia para ti (Esteban):** Usas Linux en tu máquina de desarrollo. Esto significa que tienes acceso nativo a las mismas herramientas que usan los servidores en producción: `bash`, `ssh`, `curl`, `grep`, `awk`, `systemctl`, etc. Tu flujo de trabajo es directamente transferible a entornos profesionales.

```bash
# Comandos Linux esenciales para un ingeniero de software
uname -r               # Versión del kernel
lscpu                  # Info del procesador
free -h                # Uso de memoria RAM
df -h                  # Espacio en disco
ps aux | grep proceso  # Ver procesos activos
top / htop             # Monitor de procesos en tiempo real
systemctl status nginx # Estado de un servicio
journalctl -u nginx    # Logs de un servicio
```

### 2.3 macOS

- **Núcleo:** XNU (híbrido entre Mach microkernel + BSD Unix). Open-source parcialmente (Darwin).
- **Uso principal:** desarrollo de software, diseño gráfico, edición de video.
- **Ventajas:** UNIX subyacente (compatible con herramientas de desarrollo), integración con ecosistema Apple.
- **Desventajas:** solo compatible con hardware Apple, costoso.
- **Relación con Linux:** comparten raíces UNIX. Los comandos del terminal son muy similares.

### 2.4 Android

- **Núcleo:** Linux (kernel Linux modificado por Google).
- **Capa encima:** Android Runtime (ART), Java/Kotlin APIs.
- **Uso:** smartphones, tablets, smartwatches, TVs, IoT.
- **Open-source:** AOSP (Android Open Source Project). Las apps de Google son propietarias.
- **Modelo de permisos:** granular por permiso (cámara, GPS, contactos — el usuario los aprueba).

### 2.5 iOS / iPadOS

- **Núcleo:** Darwin (mismo que macOS, basado en XNU).
- **Uso:** iPhone, iPad, Apple Watch.
- **Cerrado:** no existe ROM personalizable como en Android.
- **Modelo de seguridad:** muy restrictivo, sandboxing total de apps, App Store review obligatorio.

---

### Tabla Comparativa General

| Característica | Windows | Linux | macOS | Android | iOS |
| :--- | :---: | :---: | :---: | :---: | :---: |
| **Núcleo** | NT Híbrido | Linux monolítico | XNU híbrido | Linux | XNU híbrido |
| **Open-source** | ❌ | ✅ | Parcial | Parcial | ❌ |
| **Licencia** | De pago | Gratuita | Incluida con Mac | Gratuita | Incluida |
| **Cuota de mercado (servidores)** | ~20% | >70% | ~1% | — | — |
| **Cuota de mercado (móviles)** | — | — | — | ~72% | ~28% |
| **Seguridad (desktop)** | 🟡 Media | ✅ Alta | ✅ Alta | 🟡 Media | ✅ Muy Alta |
| **Personalización** | 🟡 Media | ✅ Total | 🟡 Media | ✅ Alta | ❌ Baja |
| **Uso en desarrollo profesional** | ✅ | ✅ | ✅ | — | — |

---

## 3. Gestión de Procesos y Planificación

Un **proceso** es un programa en ejecución. El SO mantiene para cada proceso un **Bloque de Control de Proceso (PCB)** con: ID, estado, contador de programa, registros, memoria asignada.

### Estados de un Proceso

```
              ┌──────────────────────────────────────────────┐
   nuevo ────►│ Listo ──► En ejecución ──► Terminado         │
              │   ▲            │                             │
              │   │   (bloqueado por E/S o semáforo)         │
              │   └── Bloqueado ◄────────────────────────    │
              └──────────────────────────────────────────────┘
```

### Algoritmos de Planificación (Scheduling)

El **planificador** (scheduler) decide qué proceso usa la CPU:

| Algoritmo | Descripción | Ventaja | Desventaja |
| :--- | :--- | :--- | :--- |
| **FIFO / FCFS** | Primero en llegar, primero en ejecutarse | Simple | Convoy problem (proceso largo bloquea a cortos) |
| **Round Robin** | Cada proceso recibe un quantum de tiempo (e.g., 20ms) | Justo, buen tiempo de respuesta | Overhead por cambios de contexto |
| **Shortest Job First (SJF)** | Ejecuta primero el proceso más corto | Minimiza tiempo promedio | Inanición de procesos largos |
| **CFS (Linux)** | Completely Fair Scheduler — basado en tiempo de CPU acumulado | Justicia real, adaptativo | Complejo de implementar |

> El kernel Linux usa **CFS** por defecto. Es el que planifica todos los procesos en tu máquina.

---

## 4. Sistema de Archivos — Permisos y Metadatos

### Estructura de directorios en Linux (FHS)

```
/
├── bin/     → Binarios esenciales (ls, cp, mv)
├── etc/     → Configuraciones del sistema
├── home/    → Directorios de usuarios (/home/e12jassir)
├── var/     → Datos variables (logs, caches)
├── proc/    → Info del kernel en tiempo real (sistema de archivos virtual)
├── sys/     → Interfaz con el hardware
├── dev/     → Dispositivos como archivos (/dev/sda, /dev/null)
├── tmp/     → Archivos temporales (se limpian al reiniciar)
├── usr/     → Aplicaciones y utilidades de usuario
└── mnt/     → Puntos de montaje de dispositivos externos
```

### Permisos en Linux (modo octal)

```bash
ls -l archivo.txt
# -rw-r--r-- 1 e12jassir users 4096 Sep 29 archivo.txt
#  │││││││││
#  │││└──┴──── Otros: solo lectura (r--)  = 4
#  │││
#  │└─┴──── Grupo: solo lectura (r--)     = 4
#  │
#  └─┴── Propietario: lec + escr (rw-)    = 6

# Cambiar permisos
chmod 644 archivo.txt     # rw-r--r--
chmod 755 script.sh       # rwxr-xr-x
chmod +x script.sh        # añadir ejecución al propietario
chown e12jassir:users archivo.txt  # cambiar dueño
```

### Metadatos de Archivos

Los **metadatos** son datos sobre el archivo, no el contenido en sí:

```bash
# Ver metadatos completos de un archivo
stat archivo.txt
# Muestra: tamaño, tipo, permisos, inode, timestamps (atime, mtime, ctime)

# Ver metadatos de imagen (EXIF)
exiftool foto.jpg
# Muestra: cámara, fecha, GPS, resolución, software usado

# Ver cabecera de un PDF
file documento.pdf       # identifica el tipo real por magic bytes
xxd documento.pdf | head # muestra bytes crudos en hexadecimal

# Cabecera (magic bytes) de formatos comunes:
# PDF:  %PDF-1.x  (bytes: 25 50 44 46)
# JPEG: ÿØÿà      (bytes: FF D8 FF E0)
# PNG:  ‰PNG      (bytes: 89 50 4E 47)
# ZIP:  PK         (bytes: 50 4B 03 04)
```

> **Relevante para el entregable de metadatos (30 Oct):** El análisis de metadatos y cabeceras consiste en examinar la información que los archivos contienen más allá de su contenido visible. En Linux puedes hacerlo con `stat`, `file`, `xxd`, `exiftool`.

---

## 5. IoT — Internet de las Cosas

El **Internet de las Cosas (IoT)** es la red de dispositivos físicos embebidos con sensores, software y conectividad que les permite recopilar e intercambiar datos sin intervención humana directa.

### Componentes de un sistema IoT

```
Sensor/Actuador ──► Gateway IoT ──► Internet ──► Cloud/Servidor ──► Aplicación
(Termómetro,         (Raspberry Pi,                (AWS IoT,          (Dashboard,
 cámara, GPS)         Router LoRa)                  Azure IoT Hub)     app móvil)
```

### Casos de Uso Reales

| Sector | Caso de uso | Tecnología clave |
| :--- | :--- | :--- |
| **Salud** | Monitoreo continuo de pacientes (glucómetros IoT, marcapasos conectados) | Bluetooth LE, ZigBee |
| **Ciudad inteligente** | Semáforos adaptativos, basureros que notifican cuando están llenos | LoRaWAN, NB-IoT |
| **Agricultura** | Sensores de humedad del suelo, drones para riego automático | WiFi, LoRa, MQTT |
| **Industria (IIoT)** | Mantenimiento predictivo de máquinas mediante vibración/temperatura | OPC-UA, MQTT |
| **Hogar inteligente** | Termostato Nest, Alexa/Google Home, luces Philips Hue | WiFi, Zigbee, Z-Wave |
| **Logística** | Rastreo GPS de camiones en tiempo real, monitoreo de cadena de frío | GPS + LTE + MQTT |
| **Energía** | Medidores inteligentes (Smart Meters) de luz y gas | PLC, RF, NB-IoT |

### Protocolos de IoT

| Protocolo | Capa | Descripción | Uso |
| :--- | :--- | :--- | :--- |
| **MQTT** | Aplicación | Publish/subscribe, muy ligero | Sensores con poca batería |
| **CoAP** | Aplicación | Como HTTP pero para dispositivos restringidos | IoT sobre UDP |
| **HTTP/REST** | Aplicación | Estándar web | Gateways con buena conectividad |
| **Zigbee** | Física + Enlace | Malla de corto alcance, bajo consumo | Domótica |
| **LoRaWAN** | Física + Enlace | Largo alcance (km), bajo consumo | Ciudades inteligentes, campo |
| **Bluetooth LE** | Física + Enlace | Corto alcance, muy bajo consumo | Wearables, salud |

### Desafíos de seguridad en IoT

- **Superficie de ataque enorme:** millones de dispositivos, muchos sin actualizaciones.
- **Contraseñas por defecto:** la botnet Mirai (2016) infectó 600.000 cámaras con contraseñas como `admin/admin`.
- **Actualizaciones difíciles:** un termómetro industrial no tiene pantalla ni teclado.
- **Privacidad:** un asistente de voz escucha constantemente; un router puede ser espía.

---

## 6. Virtualización y Contenedores

### Máquinas Virtuales (VM)

Una VM emula un hardware completo. El **hipervisor** (e.g., VirtualBox, VMware, KVM) corre entre el hardware y las VMs.

```
┌─────────────┐  ┌─────────────┐
│ VM Ubuntu   │  │ VM Windows  │
│ (SO + Apps) │  │ (SO + Apps) │
├─────────────┴──┴─────────────┤
│       Hipervisor (KVM)       │
├──────────────────────────────┤
│      Hardware físico         │
└──────────────────────────────┘
```

### Contenedores (Docker)

Los contenedores comparten el kernel del SO host pero aíslan el proceso, el sistema de archivos y la red.

```bash
# Ejemplo básico de Docker en Linux
docker run -d -p 80:80 nginx        # Levantar servidor web nginx
docker ps                           # Ver contenedores corriendo
docker exec -it <id> bash           # Entrar al contenedor
docker stop <id>                    # Detener
```

**VM vs. Contenedor:**

| Característica | VM | Contenedor (Docker) |
| :--- | :--- | :--- |
| **Kernel** | Propio (completo) | Compartido con el host |
| **Peso** | GBs | MBs |
| **Tiempo de arranque** | Minutos | Segundos |
| **Aislamiento** | Fuerte | Moderado |
| **Uso típico** | Entornos completamente aislados | Microservicios, CI/CD |

---

## 7. Errores Comunes

| Error | Realidad |
| :--- | :--- |
| "Linux es para expertos" | Existen distribuciones como Ubuntu y Mint diseñadas para principiantes. La mayoría de servidores del mundo corren Linux. |
| "Android es Java puro" | Android usa el kernel Linux y la capa de aplicación originalmente en Java/Dalvik, hoy en Kotlin/ART. |
| "IoT es solo domotica" | IoT abarca manufactura, medicina, logística, agricultura, infraestructura crítica. |
| "Los contenedores reemplazan a las VMs" | Son complementarios: se usan VMs para aislar sistemas y contenedores dentro de ellas para microservicios. |
| "Los metadatos no importan" | Periodistas han sido identificados por metadatos EXIF de fotos. Documentos legales filtran autoría por metadatos de Word. |

---

## 8. Referencia Rápida

```
SO = kernel + utilidades + interfaz de usuario
Kernel = componente central con acceso privilegiado al hardware

Tipos de SO:
  Windows → NT kernel, mayor compatibilidad de software comercial
  Linux   → kernel monolítico open-source, dominante en servidores
  macOS   → XNU (Mach+BSD), solo hardware Apple
  Android → kernel Linux + ART, 72% de móviles
  iOS     → XNU, ecosistema cerrado Apple

Permisos Linux: r=4, w=2, x=1 → chmod 755 = rwxr-xr-x

IoT: sensores → gateway → internet → cloud → aplicación
Protocolos IoT: MQTT (pub/sub), CoAP, LoRaWAN, Zigbee, BLE

Metadatos: stat, file, xxd, exiftool (Linux)
Magic bytes: PDF=25504446 | JPEG=FFD8FF | PNG=89504E47
```

---

## 9. Recursos Externos Específicos

### Videos / Canales
- **The Linux Foundation** (YouTube): [`Introduction to Linux`](https://www.youtube.com/c/LinuxFoundation) — Cursos gratuitos sobre Linux a nivel técnico.
- **NetworkChuck** (YouTube): [`Linux for Hackers`](https://www.youtube.com/c/NetworkChuck) — Comandos Linux con contexto de seguridad, muy entretenido.
- **IBM Technology** (YouTube): [`What is IoT?`](https://www.youtube.com/watch?v=h0gWfVCSGQQ) — Explicación clara y profesional del ecosistema IoT.

### Libros
- **Pressman & Maxim — Ingeniería de Software (9.ª ed.):**
  - Cap. 13: *Estrategias de Pruebas de Software* — Pruebas en sistemas con SO subyacente.
- **Tanenbaum, A. S. — Sistemas Operativos Modernos (4.ª ed.):**
  - Cap. 1: *Introducción* — Historia y estructura del SO.
  - Cap. 2: *Procesos e Hilos* — Planificación y comunicación entre procesos.

### Sitios web / Cursos
- [linuxcommand.org](https://linuxcommand.org/lc3_learning_the_shell.php) — Tutorial gratuito de la línea de comandos Linux.
- [OverTheWire: Bandit](https://overthewire.org/wargames/bandit/) — Juego de CTF para aprender comandos Linux de forma práctica.
- [Eclipse Mosquitto](https://mosquitto.org/) — Broker MQTT open-source para experimentar con IoT.

---

## 10. Preguntas de Active Recall

1. ¿Cuáles son las 5 funciones principales de un SO? Da un ejemplo de comando Linux para cada una.
2. ¿En qué se diferencia el kernel de Windows NT del kernel Linux? ¿Cuál es la ventaja de cada uno?
3. Explica qué es el CFS de Linux y por qué es diferente a FIFO o Round Robin.
4. Dibuja la jerarquía de directorios de Linux (FHS). ¿Qué contiene `/proc`? ¿Y `/dev`?
5. ¿Qué son los metadatos de un archivo? Nombra 3 herramientas en Linux para analizarlos.
6. ¿Qué es el "magic byte" de un archivo y para qué sirve?
7. Describe un caso de uso de IoT en el sector salud o agrícola. ¿Qué protocolo usarías y por qué?
8. ¿Cuál es la diferencia entre una VM y un contenedor Docker? ¿Cuándo usarías cada uno?
