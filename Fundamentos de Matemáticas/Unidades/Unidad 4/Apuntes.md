# Unidad 4 — Trigonometría
**Fundamentos de Matemáticas · CFBD242-A1 · Atilano Arrieta Vivero**

---

## 🧭 Mapa de Contenidos

```
Trigonometría
├── Ángulos y medición (grados ↔ radianes)
├── Razones trigonométricas en triángulo rectángulo
│   └── sen, cos, tan, csc, sec, cot
├── Círculo unitario
│   ├── Ángulos estándar: 0°, 30°, 45°, 60°, 90°, …
│   └── Cuadrantes y signos
├── Identidades trigonométricas
│   ├── Identidades pitagóricas
│   ├── Identidades de cociente
│   └── Identidades de suma y diferencia de ángulos
└── Ecuaciones trigonométricas
```

---

## 1. Ángulos y Conversión

### 1.1 Tipos de Ángulo

| Nombre | Medida en grados | Medida en radianes |
|:---|:---:|:---:|
| Nulo | 0° | 0 |
| Agudo | 0° < θ < 90° | 0 < θ < π/2 |
| Recto | 90° | π/2 |
| Obtuso | 90° < θ < 180° | π/2 < θ < π |
| Llano | 180° | π |
| Reflejo | 180° < θ < 360° | π < θ < 2π |
| Completo | 360° | 2π |

### 1.2 Conversión Grados ↔ Radianes

**La relación fundamental:** `180° = π rad`

$$\text{Radianes} = \text{Grados} \times \frac{\pi}{180}$$

$$\text{Grados} = \text{Radianes} \times \frac{180}{\pi}$$

| Grados | Radianes | Valor decimal |
|:---:|:---:|:---:|
| 0° | 0 | 0 |
| 30° | π/6 | ≈ 0.524 |
| 45° | π/4 | ≈ 0.785 |
| 60° | π/3 | ≈ 1.047 |
| 90° | π/2 | ≈ 1.571 |
| 120° | 2π/3 | ≈ 2.094 |
| 135° | 3π/4 | ≈ 2.356 |
| 150° | 5π/6 | ≈ 2.618 |
| 180° | π | ≈ 3.14159 |
| 270° | 3π/2 | ≈ 4.712 |
| 360° | 2π | ≈ 6.283 |

---

## 2. Razones Trigonométricas en Triángulo Rectángulo

### 2.1 Las Seis Razones

Dado un triángulo rectángulo con ángulo agudo θ:
- **hip** = hipotenusa (lado opuesto al ángulo recto)
- **op** = cateto opuesto al ángulo θ
- **ad** = cateto adyacente al ángulo θ

| Razón | Definición | Inversa |
|:---:|:---|:---:|
| `sen θ` | op / hip | `csc θ = hip/op` |
| `cos θ` | ad / hip | `sec θ = hip/ad` |
| `tan θ` | op / ad | `cot θ = ad/op` |

> **Mnemotécnica SOH-CAH-TOA:**
> - **S**OH: **S**eno = **O**puesto / **H**ipotenusa
> - **C**AH: **C**oseno = **A**dyacente / **H**ipotenusa
> - **T**OA: **T**angente = **O**puesto / **A**dyacente

**Ejemplo:** Triángulo con cateto opuesto = 3, cateto adyacente = 4, hipotenusa = 5 (3-4-5)

```
sen θ = 3/5    cos θ = 4/5    tan θ = 3/4
csc θ = 5/3    sec θ = 5/4    cot θ = 4/3
```

---

## 3. El Círculo Unitario

### 3.1 Definición

El círculo unitario tiene **radio = 1** y está centrado en el origen `(0,0)`. Para un punto `P(x, y)` en el círculo con ángulo θ:

$$\cos \theta = x \qquad \sin \theta = y$$

### 3.2 Tabla Completa del Círculo Unitario

| Ángulo (°) | Ángulo (rad) | cos θ | sen θ | tan θ |
|:---:|:---:|:---:|:---:|:---:|
| 0° | 0 | 1 | 0 | 0 |
| 30° | π/6 | √3/2 | 1/2 | √3/3 = 1/√3 |
| 45° | π/4 | √2/2 | √2/2 | 1 |
| 60° | π/3 | 1/2 | √3/2 | √3 |
| 90° | π/2 | 0 | 1 | ∞ (indefinida) |
| 120° | 2π/3 | −1/2 | √3/2 | −√3 |
| 135° | 3π/4 | −√2/2 | √2/2 | −1 |
| 150° | 5π/6 | −√3/2 | 1/2 | −√3/3 |
| 180° | π | −1 | 0 | 0 |
| 210° | 7π/6 | −√3/2 | −1/2 | √3/3 |
| 225° | 5π/4 | −√2/2 | −√2/2 | 1 |
| 240° | 4π/3 | −1/2 | −√3/2 | √3 |
| 270° | 3π/2 | 0 | −1 | ∞ (indefinida) |
| 300° | 5π/3 | 1/2 | −√3/2 | −√3 |
| 315° | 7π/4 | √2/2 | −√2/2 | −1 |
| 330° | 11π/6 | √3/2 | −1/2 | −√3/3 |
| 360° | 2π | 1 | 0 | 0 |

### 3.3 Truco para Memorizar sen y cos de Ángulos Estándar

Para los ángulos de 0°, 30°, 45°, 60°, 90°:

$$\sin \theta = \frac{\sqrt{0}}{2},\ \frac{\sqrt{1}}{2},\ \frac{\sqrt{2}}{2},\ \frac{\sqrt{3}}{2},\ \frac{\sqrt{4}}{2}$$

$$\cos \theta = \frac{\sqrt{4}}{2},\ \frac{\sqrt{3}}{2},\ \frac{\sqrt{2}}{2},\ \frac{\sqrt{1}}{2},\ \frac{\sqrt{0}}{2}$$

> El **seno aumenta** de 0° a 90°; el **coseno decrece**. Son complementarios.

### 3.4 Signos por Cuadrante — "All Students Take Calculus"

| Cuadrante | Ángulos | sen | cos | tan |
|:---:|:---:|:---:|:---:|:---:|
| I (All) | 0° – 90° | + | + | + |
| II (Students) | 90° – 180° | + | − | − |
| III (Take) | 180° – 270° | − | − | + |
| IV (Calculus) | 270° – 360° | − | + | − |

> **Mnemotécnica:** "All Students Take Calculus" → en cada cuadrante, la primera letra indica qué función es positiva (A=All, S=Sin, T=Tan, C=Cos).

---

## 4. Identidades Trigonométricas

### 4.1 Identidades Pitagóricas

$$\boxed{\sin^2\theta + \cos^2\theta = 1}$$

$$1 + \tan^2\theta = \sec^2\theta$$

$$1 + \cot^2\theta = \csc^2\theta$$

> La primera es la más importante. Las otras dos se derivan dividiendo la primera por cos²θ o sen²θ respectivamente.

**Derivaciones útiles:**
```
sin²θ = 1 − cos²θ
cos²θ = 1 − sin²θ
tan²θ = sec²θ − 1
```

### 4.2 Identidades de Cociente

$$\tan\theta = \frac{\sin\theta}{\cos\theta} \qquad \cot\theta = \frac{\cos\theta}{\sin\theta}$$

### 4.3 Identidades de Recíproco

$$\csc\theta = \frac{1}{\sin\theta} \qquad \sec\theta = \frac{1}{\cos\theta} \qquad \cot\theta = \frac{1}{\tan\theta}$$

### 4.4 Identidades de Suma y Diferencia de Ángulos

$$\sin(A \pm B) = \sin A \cos B \pm \cos A \sin B$$

$$\cos(A \pm B) = \cos A \cos B \mp \sin A \sin B$$

$$\tan(A \pm B) = \frac{\tan A \pm \tan B}{1 \mp \tan A \tan B}$$

### 4.5 Identidades de Ángulo Doble

$$\sin 2\theta = 2\sin\theta\cos\theta$$

$$\cos 2\theta = \cos^2\theta - \sin^2\theta = 1 - 2\sin^2\theta = 2\cos^2\theta - 1$$

$$\tan 2\theta = \frac{2\tan\theta}{1 - \tan^2\theta}$$

### 4.6 Identidades de Ángulo Negativo

$$\sin(-\theta) = -\sin\theta \qquad \text{(función impar)}$$

$$\cos(-\theta) = \cos\theta \qquad \text{(función par)}$$

$$\tan(-\theta) = -\tan\theta$$

### 4.7 Verificación de Identidades — Procedimiento

Para demostrar que `LHS = RHS`:
1. Trabajar **solo un lado** (preferiblemente el más complejo).
2. Usar identidades conocidas para transformarlo.
3. No pasar términos de un lado al otro.
4. No verificar sustituyendo un valor numérico (eso no es demostración).

**Ejemplo:** Demostrar `tan θ · cos θ = sin θ`

```
LHS = tan θ · cos θ
    = (sin θ / cos θ) · cos θ    ← identidad de cociente
    = sin θ                       ← cos θ se cancela
    = RHS  ∎
```

**Ejemplo:** Demostrar `(1 − cos²θ)/sin θ = sin θ`

```
LHS = (1 − cos²θ)/sin θ
    = sin²θ / sin θ              ← identidad pitagórica: 1−cos²θ = sin²θ
    = sin θ
    = RHS  ∎
```

---

## 5. Ecuaciones Trigonométricas

### 5.1 Procedimiento General

1. Aislar la función trigonométrica.
2. Encontrar el ángulo de referencia (en el primer cuadrante).
3. Determinar en qué cuadrantes la función tiene ese valor (según el signo).
4. Escribir la solución general con el período.
5. Si se pide en `[0°, 360°)`, filtrar las soluciones.

**Período de las funciones:**
- `sin θ` y `cos θ`: período `2π` (360°)
- `tan θ` y `cot θ`: período `π` (180°)

### 5.2 Ejemplos Resueltos

**Ejemplo 1:** `2 sin θ − 1 = 0` en `[0°, 360°)`

```
sin θ = 1/2
Ángulo de referencia: 30° (sen 30° = 1/2)
Cuadrantes donde sen > 0: I y II
θ₁ = 30°
θ₂ = 180° − 30° = 150°
Solución: {30°, 150°}
```

**Ejemplo 2:** `2 cos²θ − cos θ − 1 = 0` en `[0°, 2π)`

```
Sea u = cos θ:
2u² − u − 1 = 0
(2u + 1)(u − 1) = 0
u = −1/2  o  u = 1

Para cos θ = 1:    θ = 0
Para cos θ = −1/2: ángulo de ref. = 60° (π/3)
  Cuadrantes donde cos < 0: II y III
  θ = π − π/3 = 2π/3
  θ = π + π/3 = 4π/3

Solución: {0, 2π/3, 4π/3}
```

**Ejemplo 3:** `tan θ = √3` en `[0°, 360°)`

```
Ángulo de referencia: 60° (tan 60° = √3)
Cuadrantes donde tan > 0: I y III
θ₁ = 60°
θ₂ = 60° + 180° = 240°
Solución: {60°, 240°}
```

### 5.3 Solución General (con período)

| Ecuación | Solución general |
|:---|:---|
| `sin θ = k` | `θ = arcsin(k) + 2πn`  o  `θ = π − arcsin(k) + 2πn` |
| `cos θ = k` | `θ = ±arccos(k) + 2πn` |
| `tan θ = k` | `θ = arctan(k) + πn` |

---

## 6. Funciones Trigonométricas — Gráficas

| Función | Dominio | Rango | Período | Amplitud |
|:---|:---|:---|:---:|:---:|
| `y = sin x` | ℝ | [−1, 1] | 2π | 1 |
| `y = cos x` | ℝ | [−1, 1] | 2π | 1 |
| `y = tan x` | ℝ − {π/2 + nπ} | ℝ | π | — |

**Forma general:** `y = A sin(Bx + C) + D`
- `A`: amplitud (altura máxima desde el eje)
- `B`: frecuencia angular → período = `2π/|B|`
- `C`: desfase horizontal (fase)
- `D`: desplazamiento vertical (línea media)

---

## 7. Errores Comunes

| Error | Descripción | Corrección |
|:---|:---|:---|
| `sin(A+B) = sinA + sinB` | Distribuir incorrectamente | Usar identidad: `sin(A+B) = sinA·cosB + cosA·sinB` |
| `sin²θ = sin(θ²)` | Confundir notación | `sin²θ = (sin θ)²`, no `sin(θ²)` |
| Ignorar cuadrantes | Dar solo una solución en `[0°,360°)` | Verificar siempre cuáles cuadrantes tienen el signo correcto |
| Mezclar grados y radianes | Calcular `sin(45) = sin(45°)` usando modo rad | Verificar el modo de la calculadora |
| `tan 90° = 0` | Confundir tangente con seno en 90° | `tan 90°` es **indefinida**; `sin 90° = 1`, `cos 90° = 0` |
| `1/sin θ = sin⁻¹ θ` | Confundir recíproco con inversa | `1/sin θ = csc θ`; `sin⁻¹ θ = arcsin θ` (función inversa) |

---

## 8. Técnicas de Estudio

### Active Recall — Preguntas de Autoevaluación

1. Reproduce de memoria la tabla del círculo unitario para 0°, 30°, 45°, 60°, 90°.
2. ¿Cuál es el signo de `cos 200°`? ¿Y de `sin 300°`?
3. Demuestra que `sec²θ − tan²θ = 1` usando solo identidades básicas.
4. Resuelve `√2 sin θ = 1` en `[0°, 360°)`.
5. Convierte 210° a radianes y 7π/4 a grados.
6. Calcula sin 75° usando la identidad de suma: `sin(45° + 30°)`.

### Técnica de Feynman

Explica el círculo unitario como si el eje x fuera el coseno y el eje y el seno: en 0° estás en el punto (1, 0); al girar al eje y llegas a (0, 1) en 90°; a las 10 en punto del reloj serían 300°. Esto conecta la geometría con los valores que calculas.

---

## 9. Recursos Externos

| Recurso | Descripción | URL |
|:---|:---|:---|
| **Khan Academy ES** — Trigonometría | Videos y ejercicios del círculo unitario | https://es.khanacademy.org/math/trigonometry |
| **Matemóvil** (YouTube) | Identidades trigonométricas en español | https://www.youtube.com/@matemovil |
| **Profesor Leonard** (YouTube) | Trigonometry Full Course — muy completo | https://www.youtube.com/c/ProfessorLeonard |
| **GeoGebra — Círculo Unitario** | Applet interactivo del círculo unitario | https://www.geogebra.org/m/ZnNTvHeS |
| **Paul's Online Math Notes** | Trig cheat sheets PDF descargables | https://tutorial.math.lamar.edu/pdf/Trig_Cheat_Sheet.pdf |
| **Libro: Precálculo — Stewart** | Capítulos 5-7: Trigonometría completa | Referencia principal del curso |

---

## 10. Referencia Rápida

### Identidades Esenciales

```
PITAGÓRICAS:
sin²θ + cos²θ = 1
1 + tan²θ = sec²θ
1 + cot²θ = csc²θ

COCIENTE:
tan θ = sin θ / cos θ
cot θ = cos θ / sin θ

RECÍPROCOS:
csc θ = 1/sin θ
sec θ = 1/cos θ
cot θ = 1/tan θ

ÁNGULO DOBLE:
sin 2θ = 2 sin θ cos θ
cos 2θ = cos²θ − sin²θ
```

### Valores Críticos del Círculo Unitario (Cheat Sheet)

```
     90° = π/2
      (0,1)
       |
60° = π/3      30° = π/6
(-½,√3/2)      (√3/2,½)
       \       /
180°=(−1,0)──O──(1,0)=0°/360°
       /       \
(−√3/2,−½)    (√3/2,−½)
 240° = 4π/3  300° = 5π/3
       |
      (0,−1)
     270° = 3π/2
```

### Cuadrantes y Signos

```
       II  |  I
  S(+) C(-)|S(+) C(+)
  T(−)     |T(+)
  ─────────────────
  S(−) C(-)|S(−) C(+)
  T(+)     |T(−)
      III  | IV
```
