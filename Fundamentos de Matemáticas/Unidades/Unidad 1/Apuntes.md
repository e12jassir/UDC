# Unidad 1 — Lógica Proposicional y Conjuntos
**Fundamentos de Matemáticas · CFBD242-A1 · Atilano Arrieta Vivero**

---

## 🧭 Mapa de Contenidos

```
Lógica Proposicional
├── Proposiciones (simples y compuestas)
├── Conectores lógicos (¬, ∧, ∨, →, ↔)
├── Tablas de verdad
├── Tautologías, contradicciones, contingencias
├── Equivalencias lógicas
└── Reglas de inferencia

Teoría de Conjuntos
├── Notación (extensión, comprensión, Venn)
├── Tipos especiales (∅, U, subconjuntos)
├── Operaciones (∪, ∩, A', A−B)
└── Producto cartesiano y relaciones
```

---

## 1. Lógica Proposicional

### 1.1 Proposición

Una **proposición** es cualquier enunciado declarativo al que se puede asignar un valor de verdad (**V** o **F**), pero nunca ambos simultáneamente.

| Tipo | Ejemplo | Proposición |
|:---|:---|:---:|
| Declarativo verdadero | "El número 2 es par" | ✅ Sí |
| Declarativo falso | "Todo número primo es impar" | ✅ Sí |
| Pregunta | "¿Cuánto es 2 + 2?" | ❌ No |
| Exclamación | "¡Qué bien!" | ❌ No |
| Mandato | "Cierra la puerta" | ❌ No |
| Paradoja | "Esta oración es falsa" | ❌ No |

> **Clave práctica:** Si puedes responder «es verdadero» o «es falso» al enunciado, es proposición. Si duda, es porque no lo es.

### 1.2 Conectores Lógicos

| Símbolo | Nombre | Lectura | Tipo |
|:---:|:---|:---|:---|
| `¬` o `~` | Negación | "No es el caso que…" | Unario |
| `∧` | Conjunción | "…y…" | Binario |
| `∨` | Disyunción inclusiva | "…o…" (o ambos) | Binario |
| `∨̄` / `⊕` | Disyunción exclusiva | "…o… (pero no ambos)" | Binario |
| `→` | Condicional (implicación) | "Si… entonces…" | Binario |
| `↔` | Bicondicional | "…si y solo si…" | Binario |

### 1.3 Tablas de Verdad Completas

#### Negación `¬p`
| p | ¬p |
|:---:|:---:|
| V | F |
| F | V |

#### Conjunción `p ∧ q`
| p | q | p ∧ q |
|:---:|:---:|:---:|
| V | V | **V** |
| V | F | F |
| F | V | F |
| F | F | F |

> **Regla mnemotécnica:** La conjunción es verdadera **solo cuando AMBAS** son verdaderas. "Todas las condiciones deben cumplirse."

#### Disyunción `p ∨ q`
| p | q | p ∨ q |
|:---:|:---:|:---:|
| V | V | V |
| V | F | V |
| F | V | V |
| F | F | **F** |

> **Regla mnemotécnica:** La disyunción es falsa **solo cuando AMBAS** son falsas. "Basta que una se cumpla."

#### Condicional `p → q`
| p | q | p → q |
|:---:|:---:|:---:|
| V | V | V |
| V | F | **F** |
| F | V | V |
| F | F | V |

> ⚠️ **Error más común:** Creer que si `p` es falsa, la implicación debe ser falsa. Un condicional con antecedente falso es **siempre verdadero** (vacuamente verdadero). Ejemplo: "Si llueve _en el sol_, entonces los peces vuelan" es una proposición verdadera.

#### Bicondicional `p ↔ q`
| p | q | p ↔ q |
|:---:|:---:|:---:|
| V | V | V |
| V | F | F |
| F | V | F |
| F | F | V |

> **Regla:** El bicondicional es verdadero cuando **p y q tienen el mismo valor de verdad**.

### 1.4 Tautología, Contradicción y Contingencia

| Tipo | Definición | Ejemplo |
|:---|:---|:---|
| **Tautología** | Siempre V, sin importar valores | `p ∨ ¬p` |
| **Contradicción** | Siempre F, sin importar valores | `p ∧ ¬p` |
| **Contingencia** | Depende de los valores de las variables | `p ∧ q` |

**Verificación de tautología — Ejemplo completo:**

Verificar que `(p → q) ↔ (¬p ∨ q)` es tautología:

| p | q | ¬p | p→q | ¬p∨q | (p→q)↔(¬p∨q) |
|:---:|:---:|:---:|:---:|:---:|:---:|
| V | V | F | V | V | **V** |
| V | F | F | F | F | **V** |
| F | V | V | V | V | **V** |
| F | F | V | V | V | **V** |

Todas las filas son V → es **tautología** ✅

### 1.5 Equivalencias Lógicas Fundamentales

| Nombre | Equivalencia |
|:---|:---|
| Doble negación | `¬(¬p) ≡ p` |
| Leyes de De Morgan | `¬(p ∧ q) ≡ ¬p ∨ ¬q` |
| Leyes de De Morgan | `¬(p ∨ q) ≡ ¬p ∧ ¬q` |
| Condicional como disyunción | `p → q ≡ ¬p ∨ q` |
| Contrarrecíproco | `p → q ≡ ¬q → ¬p` |
| Bicondicional | `p ↔ q ≡ (p→q) ∧ (q→p)` |
| Absorción | `p ∧ (p ∨ q) ≡ p` |
| Distribución | `p ∧ (q ∨ r) ≡ (p ∧ q) ∨ (p ∧ r)` |

> **Las Leyes de De Morgan** son las más utilizadas en evaluaciones. Memorizar: **la negación de una conjunción es la disyunción de las negaciones**, y viceversa.

### 1.6 Formas del Condicional

Dado `p → q`:
- **Recíproco:** `q → p`
- **Inverso:** `¬p → ¬q`
- **Contrarrecíproco:** `¬q → ¬p` ← equivalente al original

> ⚠️ El recíproco y el inverso NO son equivalentes al original. Solo el contrarrecíproco lo es.

### 1.7 Reglas de Inferencia Básicas

| Nombre | Esquema | Significado |
|:---|:---|:---|
| **Modus Ponens** | `p → q`, `p` ∴ `q` | Si se cumple el antecedente, se cumple el consecuente |
| **Modus Tollens** | `p → q`, `¬q` ∴ `¬p` | Si no se cumple el consecuente, no se cumple el antecedente |
| **Silogismo Hipotético** | `p→q`, `q→r` ∴ `p→r` | Transitividad de la implicación |
| **Silogismo Disyuntivo** | `p ∨ q`, `¬p` ∴ `q` | Si una alternativa falla, la otra debe cumplirse |

---

## 2. Teoría de Conjuntos

### 2.1 Formas de Representar un Conjunto

| Método | Notación | Ejemplo |
|:---|:---|:---|
| **Extensión** (lista) | `{a, b, c, …}` | `A = {1, 2, 3, 4}` |
| **Comprensión** (regla) | `{x | P(x)}` | `A = {x ∈ ℤ | 1 ≤ x ≤ 4}` |
| **Diagrama de Venn** | Figura | Círculos superpuestos |

### 2.2 Conjuntos Especiales

| Símbolo | Nombre | Descripción |
|:---:|:---|:---|
| `∅` o `{}` | Conjunto vacío | Sin elementos. `∅ ⊆ A` para todo A |
| `U` | Conjunto universal | Contiene todos los elementos del contexto |
| `ℕ` | Naturales | `{0, 1, 2, 3, …}` |
| `ℤ` | Enteros | `{…, -2, -1, 0, 1, 2, …}` |
| `ℚ` | Racionales | Cociente de enteros, denominador ≠ 0 |
| `ℝ` | Reales | Todos los puntos en la recta numérica |

### 2.3 Relaciones entre Conjuntos

| Símbolo | Significado | Ejemplo |
|:---:|:---|:---|
| `a ∈ A` | `a` pertenece a `A` | `3 ∈ {1, 2, 3}` |
| `a ∉ A` | `a` no pertenece a `A` | `5 ∉ {1, 2, 3}` |
| `A ⊆ B` | `A` es subconjunto de `B` (incluido) | `{1,2} ⊆ {1,2,3}` |
| `A ⊂ B` | `A` es subconjunto propio de `B` | `{1,2} ⊂ {1,2,3}` |
| `A = B` | `A` y `B` son iguales | `{1,2} = {2,1}` |
| `|A|` o `n(A)` | Cardinalidad (número de elementos) | `|{a,b,c}| = 3` |

> ⚠️ **Error crítico:** Confundir `∈` (pertenencia, elemento a conjunto) con `⊆` (inclusión, conjunto a conjunto). Ejemplo: `{1} ⊆ {1,2,3}` es correcto, pero `{1} ∈ {1,2,3}` es **falso** (el elemento `1`, no el conjunto `{1}`, pertenece al otro).

### 2.4 Operaciones entre Conjuntos

| Operación | Símbolo | Definición | Diagrama de Venn |
|:---|:---:|:---|:---|
| **Unión** | `A ∪ B` | Elementos en A, en B, o en ambos | Ambos círculos completos |
| **Intersección** | `A ∩ B` | Solo elementos comunes | Solo la parte solapada |
| **Diferencia** | `A − B` | Elementos de A que no están en B | A menos la parte solapada |
| **Complemento** | `A'` o `Aᶜ` | Elementos del universo no en A | Todo lo que está fuera de A |
| **Diferencia simétrica** | `A △ B` | `(A−B) ∪ (B−A)` | Ambos círculos sin la intersección |

**Ejemplo numérico resuelto:**

Sea `U = {1,2,3,4,5,6,7,8}`, `A = {1,2,3,4}`, `B = {3,4,5,6}`.

| Operación | Resultado |
|:---|:---|
| `A ∪ B` | `{1,2,3,4,5,6}` |
| `A ∩ B` | `{3,4}` |
| `A − B` | `{1,2}` |
| `B − A` | `{5,6}` |
| `A'` | `{5,6,7,8}` |
| `A △ B` | `{1,2,5,6}` |

### 2.5 Leyes del Álgebra de Conjuntos

| Ley | Para Unión | Para Intersección |
|:---|:---|:---|
| **Conmutativa** | `A ∪ B = B ∪ A` | `A ∩ B = B ∩ A` |
| **Asociativa** | `(A∪B)∪C = A∪(B∪C)` | `(A∩B)∩C = A∩(B∩C)` |
| **Distributiva** | `A∪(B∩C) = (A∪B)∩(A∪C)` | `A∩(B∪C) = (A∩B)∪(A∩C)` |
| **Identidad** | `A ∪ ∅ = A` | `A ∩ U = A` |
| **Complemento** | `A ∪ A' = U` | `A ∩ A' = ∅` |
| **De Morgan** | `(A ∪ B)' = A' ∩ B'` | `(A ∩ B)' = A' ∪ B'` |

### 2.6 Producto Cartesiano

`A × B = {(a, b) | a ∈ A y b ∈ B}`

- `|A × B| = |A| · |B|`
- `A × B ≠ B × A` (en general)

**Ejemplo:** `A = {1, 2}`, `B = {x, y}`

```
A × B = {(1,x), (1,y), (2,x), (2,y)}    → 4 pares
B × A = {(x,1), (x,2), (y,1), (y,2)}    → 4 pares (distintos)
```

### 2.7 Número de Subconjuntos

Si `|A| = n`, entonces `A` tiene exactamente **2ⁿ** subconjuntos (incluyendo `∅` y `A` mismo).

Ejemplo: `A = {a, b, c}` → `2³ = 8` subconjuntos:  
`∅, {a}, {b}, {c}, {a,b}, {a,c}, {b,c}, {a,b,c}`

---

## 3. Errores Comunes y Cómo Evitarlos

| Error | Descripción | Corrección |
|:---|:---|:---|
| `p → q` con `p=F` | Creer que la implicación es falsa | Con `p=F`, la implicación es **siempre V** |
| `¬(p ∧ q)` = `¬p ∧ ¬q` | Distribuir mal la negación | Aplicar De Morgan: `¬p ∨ ¬q` |
| `{1} ∈ {1, 2, 3}` | Confundir el conjunto `{1}` con el elemento `1` | `1 ∈ {1,2,3}` pero `{1} ⊆ {1,2,3}` |
| `A − B = B − A` | Creer que la diferencia es conmutativa | La diferencia NO es conmutativa |
| Calcular `|A ∪ B|` sumando sin restar | Doble conteo | `|A ∪ B| = |A| + |B| − |A ∩ B|` (principio de inclusión-exclusión) |
| Olvidar que `∅ ⊆ A` para todo A | Ignorar el conjunto vacío | El conjunto vacío es subconjunto de cualquier conjunto |

---

## 4. Técnicas de Estudio Recomendadas

### Active Recall — Preguntas de Autoevaluación

1. Sin mirar la tabla, construye la tabla de verdad de `p → q` con las 4 combinaciones.
2. ¿Cuál es el contrarrecíproco de "Si estudio, entonces apruebo"? ¿Es equivalente al original?
3. Dado `U = {1..10}`, `A = {2,4,6,8}`, `B = {1,2,3,4}`, calcula `(A ∪ B)'`.
4. ¿Cuántos subconjuntos tiene `{p, q, r, s}`?
5. Aplica De Morgan a `¬(llueve ∧ hace frío)`.

### Técnica de Feynman

Toma la **Ley de De Morgan** y explícala como si se la estuvieras enseñando a alguien que nunca ha visto lógica: usa ejemplos cotidianos ("No es cierto que (tengo carro Y tengo moto)" = "No tengo carro O no tengo moto").

### Método de Práctica Espaciada

- Día 1: Lee y construye tablas de verdad a mano.
- Día 3: Reproduce las equivalencias lógicas sin ver los apuntes.
- Día 7: Resuelve 5 ejercicios de operaciones de conjuntos nuevos.
- Día 14: Repaso completo + ejercicios mixtos.

---

## 5. Recursos Externos Reales

| Recurso | Tipo | URL / Canal |
|:---|:---|:---|
| **Khan Academy en Español — Lógica y Conjuntos** | Videos interactivos | https://es.khanacademy.org/math/statistics-probability/probability-library |
| **Matemóvil** (YouTube) | Canal en español, tablas de verdad | https://www.youtube.com/@matemovil |
| **Juanito Matemáticas** (YouTube) | Canal colombiano, conjuntos y lógica | https://www.youtube.com/@JuanitoMatematicas |
| **Profe en Casa** (YouTube) | Conjuntos, operaciones, Venn | https://www.youtube.com/@ProfeEnCasa |
| **Symbolic Logic (Whitman College)** | Texto libre en inglés | https://www.whitman.edu/mathematics/higher_math_online/section01.01.html |
| **Libro: Fundamentos de Matemáticas Discretas — Rosen** | Capítulos 1 y 2 | Disponible en biblioteca institucional |

---

## 6. Referencia Rápida

### Tablas de Conectores (Resumen)

```
¬p: invierte el valor
p ∧ q: V solo si ambas V
p ∨ q: F solo si ambas F  
p → q: F solo si V→F
p ↔ q: V si mismo valor
```

### Propiedades de Conjuntos (Cheat Sheet)

```
A ∪ ∅ = A          A ∩ U = A
A ∪ U = U          A ∩ ∅ = ∅
A ∪ A' = U         A ∩ A' = ∅
(A')' = A
(A ∪ B)' = A' ∩ B'    ← De Morgan
(A ∩ B)' = A' ∪ B'    ← De Morgan
|A ∪ B| = |A| + |B| - |A ∩ B|
```

### Símbolos para escribir en documentos

| Símbolo | Unicode | Descripción |
|:---:|:---:|:---|
| `∧` | U+2227 | Conjunción (Y) |
| `∨` | U+2228 | Disyunción (O) |
| `¬` | U+00AC | Negación |
| `→` | U+2192 | Condicional |
| `↔` | U+2194 | Bicondicional |
| `∈` | U+2208 | Pertenencia |
| `⊆` | U+2286 | Subconjunto |
| `∪` | U+222A | Unión |
| `∩` | U+2229 | Intersección |
| `∅` | U+2205 | Conjunto vacío |
