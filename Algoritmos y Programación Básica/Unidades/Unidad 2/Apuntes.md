# Apuntes — Unidad 2: Lenguajes de Programación
**Asignatura:** Algoritmos y Programación Básica · IX24013-B1
**Docente:** Heybertt Moreno Díaz
**Última actualización:** 2026-09-29

---

## 1. Historia de los Lenguajes de Programación

Entender el origen de Java y de los lenguajes en general ayuda a comprender por qué la sintaxis es como es y cuáles son sus ventajas reales.

### Línea del tiempo clave

| Año | Hito |
|:---:|:---|
| 1945 | **Lenguaje máquina** — instrucciones en binario puro. Solo ejecutable por la CPU específica. |
| 1949 | **Lenguaje ensamblador (ASM)** — mnemónicos como `MOV`, `ADD`. Todavía atado al hardware. |
| 1957 | **FORTRAN** (IBM) — primer lenguaje de alto nivel. Orientado al cálculo científico. |
| 1959 | **COBOL** — diseñado para negocios y procesamiento de datos. |
| 1972 | **C** (Dennis Ritchie) — lenguaje estructurado de propósito general. Base de sistemas operativos. |
| 1983 | **C++** — C con Programación Orientada a Objetos (POO). |
| 1991 | **Python** — interpretado, legibilidad máxima, multiparadigma. |
| 1995 | **Java** (Sun Microsystems) — "Write Once, Run Anywhere". Plataforma independiente. |
| 1995 | **JavaScript** — lenguaje para el navegador web (no confundir con Java). |
| 2011 | **Kotlin** — lenguaje moderno 100% interoperable con Java, hoy preferido para Android. |

### ¿Por qué Java sigue vigente?

1. **Plataforma independiente** gracias a la JVM (Java Virtual Machine).
2. **Fuertemente tipado** — detecta errores en tiempo de compilación, no en ejecución.
3. **Ecosistema masivo** — Spring, Hibernate, Maven, Android SDK.
4. **Adoptado en el mundo empresarial** — bancos, telecomunicaciones, ERP.
5. **Base para aprender POO** — conceptos transferibles a C#, Kotlin, TypeScript.

---

## 2. Paradigmas de Programación

Un **paradigma** es un enfoque o estilo para estructurar el código. Un lenguaje puede soportar varios.

| Paradigma | Concepto central | Ejemplos de lenguajes |
|:---|:---|:---|
| **Imperativo** | Le dices a la computadora **cómo** hacer la tarea, paso a paso | C, Pascal, COBOL |
| **Estructurado** | Imperativo + uso de funciones/módulos, sin GOTO | C, Pascal, Java básico |
| **Orientado a Objetos (POO)** | Organiza el código en clases y objetos con estado y comportamiento | Java, C++, Python, C# |
| **Funcional** | Las funciones son ciudadanos de primera clase; sin efectos secundarios | Haskell, Scala, Clojure, (Java 8+) |
| **Declarativo** | Le dices **qué** quieres, no cómo lograrlo | SQL, HTML, CSS |
| **Lógico** | Se basa en hechos y reglas; el motor infiere la solución | Prolog |

> **En este curso:** Java se usa en paradigma **estructurado** durante las primeras unidades, e introduce **POO** en semestres posteriores. El núcleo del curso es la lógica estructurada.

---

## 3. Java vs Otros Lenguajes — Comparación Técnica

### Java vs Python (diferencias más relevantes para el curso)

| Aspecto | Java | Python |
|:---|:---|:---|
| **Tipado** | Estático y fuerte — debes declarar el tipo | Dinámico — el tipo se infiere |
| **Compilación** | Compila a bytecode (`.class`), luego JVM ejecuta | Interpretado directamente |
| **Sintaxis** | Más verboso, requiere llaves `{}` y punto y coma `;` | Más conciso, usa indentación |
| **Velocidad** | Más rápido en tiempo de ejecución | Más lento (interpretado) |
| **Uso principal** | Empresa, Android, sistemas robustos | Ciencia de datos, IA, scripting |

```java
// Java: declaración explícita de tipo
int numero = 42;
String texto = "Hola";
```

```python
# Python: tipo inferido dinámicamente
numero = 42
texto = "Hola"
```

### Java vs C++ (similitudes y diferencias)

| Aspecto | Java | C++ |
|:---|:---|:---|
| **Gestión de memoria** | Automática (Garbage Collector) | Manual (`new` / `delete`) |
| **Punteros** | No tiene punteros explícitos | Usa punteros directamente |
| **Plataforma** | Independiente (JVM) | Depende del compilador/SO |
| **Velocidad** | Muy buena | Superior (más cercano al hardware) |

---

## 4. Variables y Tipos de Datos en Java (Profundización)

### Tipos primitivos — tabla completa

| Tipo | Tamaño | Rango | Valor por defecto | Ejemplo |
|:---|:---:|:---|:---:|:---|
| `byte` | 8 bits | −128 a 127 | 0 | `byte b = 100;` |
| `short` | 16 bits | −32,768 a 32,767 | 0 | `short s = 1000;` |
| `int` | 32 bits | −2.1×10⁹ a 2.1×10⁹ | 0 | `int n = 50000;` |
| `long` | 64 bits | ±9.2×10¹⁸ | 0L | `long l = 99L;` |
| `float` | 32 bits | ±3.4×10³⁸ (7 dígitos) | 0.0f | `float f = 3.14f;` |
| `double` | 64 bits | ±1.7×10³⁰⁸ (15 dígitos) | 0.0 | `double d = 3.14;` |
| `char` | 16 bits | '\u0000' a '\uFFFF' | '\u0000' | `char c = 'A';` |
| `boolean` | 1 bit lógico | true / false | false | `boolean ok = true;` |

### Tipos de referencia (no primitivos)

```java
String nombre = "María";        // Inmutable, clase especial
int[] numeros = {1, 2, 3};     // Arreglo (referencia a un objeto)
// Las clases, interfaces, etc. también son tipos de referencia
```

### Conversión de tipos (Casting)

```java
// Conversión implícita (widening) — sin pérdida de información
int entero = 100;
double decimal = entero;       // OK: int → double automático

// Conversión explícita (narrowing/casting) — posible pérdida
double pi = 3.14159;
int truncado = (int) pi;       // truncado = 3 (se pierde .14159)

// String a número
String sNum = "42";
int n = Integer.parseInt(sNum);     // String → int
double d = Double.parseDouble("3.14"); // String → double

// Número a String
String s = String.valueOf(42);     // int → String
String s2 = Integer.toString(42);  // equivalente
```

### Constantes

```java
// Se declaran con final — convención: TODO_EN_MAYÚSCULAS
final double PI = 3.14159265;
final int MAX_INTENTOS = 3;

// PI = 4.0;  // ERROR DE COMPILACIÓN — no se puede reasignar
```

---

## 5. Operadores en Java

### Aritméticos

```java
int a = 10, b = 3;
System.out.println(a + b);  // 13
System.out.println(a - b);  // 7
System.out.println(a * b);  // 30
System.out.println(a / b);  // 3  (división ENTERA porque ambos son int)
System.out.println(a % b);  // 1  (módulo — resto de 10 ÷ 3)

// Para obtener resultado decimal:
System.out.println((double) a / b);  // 3.3333...
System.out.println(a / (double) b);  // igual resultado
```

### Incremento / Decremento

```java
int x = 5;
x++;   // x = 6 (post-incremento)
++x;   // x = 7 (pre-incremento)
x--;   // x = 6 (post-decremento)
--x;   // x = 5 (pre-decremento)

// Diferencia entre pre y post en una expresión:
int a = 5;
int b = a++;  // b = 5, luego a = 6
int c = ++a;  // a = 7, c = 7
```

### Asignación compuesta

```java
int n = 10;
n += 5;   // n = 15  (n = n + 5)
n -= 3;   // n = 12
n *= 2;   // n = 24
n /= 4;   // n = 6
n %= 4;   // n = 2
```

### Operadores de comparación y lógicos

```java
// Comparación — retornan boolean
5 == 5    // true
5 != 3    // true
5 > 3     // true
5 <= 5    // true

// Lógicos
true && false  // false (AND)
true || false  // true  (OR)
!true          // false (NOT)

// Cortocircuito: && no evalúa el segundo operando si el primero es false
// Útil para evitar NullPointerException:
if (objeto != null && objeto.getValor() > 0) { ... }
```

---

## 6. Concatenación de Strings y Formato de Salida

```java
String nombre = "Ana";
int edad = 22;

// Concatenación con +
System.out.println("Nombre: " + nombre + ", Edad: " + edad);

// printf (formateo estilo C)
System.out.printf("Nombre: %s, Edad: %d%n", nombre, edad);
System.out.printf("Promedio: %.2f%n", 4.567);  // → 4.57

// String.format (construye un String formateado)
String mensaje = String.format("Hola, %s. Tienes %d años.", nombre, edad);
System.out.println(mensaje);
```

**Especificadores de formato:**

| Especificador | Tipo | Ejemplo |
|:---:|:---|:---|
| `%d` | Entero decimal | `%d` → `42` |
| `%f` | Decimal | `%.2f` → `3.14` |
| `%s` | String | `%s` → `"Hola"` |
| `%c` | char | `%c` → `A` |
| `%b` | boolean | `%b` → `true` |
| `%n` | Salto de línea portátil | — |

---

## 7. Programa Integrador: Conversor de Temperatura y Moneda

```java
import java.util.Scanner;

/**
 * Programa que convierte temperatura (Celsius a Fahrenheit y Kelvin)
 * y convierte una cantidad de pesos colombianos a dólares USD.
 * Unidad 2 — Tipos de datos, operadores, formato de salida.
 */
public class ConversorIntegrador {
    
    // Constante: tasa de cambio ficticia para el ejercicio
    static final double TASA_COP_USD = 4200.0;

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        // --- Conversión de temperatura ---
        System.out.print("Ingrese temperatura en Celsius: ");
        double celsius = sc.nextDouble();

        double fahrenheit = (celsius * 9.0 / 5.0) + 32;
        double kelvin     = celsius + 273.15;

        System.out.printf("%.2f °C = %.2f °F = %.2f K%n",
                           celsius, fahrenheit, kelvin);

        // --- Conversión de moneda ---
        System.out.print("Ingrese monto en COP (pesos): ");
        double montoCOP = sc.nextDouble();

        double montoUSD = montoCOP / TASA_COP_USD;

        System.out.printf("%.2f COP = %.4f USD (tasa: %.0f COP/USD)%n",
                           montoCOP, montoUSD, TASA_COP_USD);

        // --- Información del tipo de dato ---
        System.out.println("\n--- Tipos de datos usados ---");
        System.out.println("celsius es de tipo double: " + celsius);
        System.out.println("fahrenheit es de tipo double: " + fahrenheit);

        sc.close();
    }
}
```

---

## 8. Errores Comunes en esta Unidad

| Error | Descripción | Corrección |
|:---|:---|:---|
| División entera inesperada | `int a = 5, b = 2; double r = a/b;` da 2.0 | Castear: `(double) a / b` |
| Sufijo olvidado en `long` | `long x = 9999999999;` → error | `long x = 9999999999L;` |
| Sufijo olvidado en `float` | `float f = 3.14;` → error | `float f = 3.14f;` |
| Comparar Strings con `==` | `str1 == str2` compara referencias, no contenido | Usar `str1.equals(str2)` |
| Overflow silencioso en `int` | `int x = 2147483647 + 1;` da número negativo | Usar `long` para valores grandes |
| `parseInt` en String no numérico | `Integer.parseInt("3a")` lanza excepción | Validar el input antes de convertir |

---

## 9. Métodos de Estudio

### Active Recall — Preguntas

1. ¿En qué año y por qué empresa fue creado Java?
2. Nombra 4 paradigmas de programación y un lenguaje representativo de cada uno.
3. ¿Cuál es la diferencia entre `int` y `long`? ¿Cuándo usarías cada uno?
4. Explica con un ejemplo concreto qué ocurre con la división entera en Java.
5. ¿Por qué no se deben comparar Strings con `==`?
6. ¿Qué hace `Integer.parseInt()`? ¿Y `String.valueOf()`?

### Ejercicio de repaso

Escribe un programa Java que:
1. Lea el nombre, la edad y el salario mensual de una persona.
2. Calcule el salario anual (salario * 12).
3. Calcule el impuesto (19% del salario anual si supera 50 millones, 0% si no).
4. Muestre todos los datos con formato `printf`.

---

## 10. Recursos Externos

| Recurso | Descripción | URL |
|:---|:---|:---|
| **Píldoras Informáticas — Java** | Playlist completa de Java desde cero, capítulos de tipos de datos y operadores | https://www.youtube.com/@pildorasinformaticas |
| **CódigoFacilito** | Tutoriales de variables y tipos en Java | https://www.youtube.com/@codigofacilito |
| **Oracle — Java Language Specification** | Especificación oficial de tipos primitivos (Cap. 4) | https://docs.oracle.com/javase/specs/ |
| **W3Schools Java** | Referencia rápida de tipos, operadores y casting | https://www.w3schools.com/java/java_data_types.asp |

---

## 11. Referencia Rápida

```
JERARQUÍA DE TIPOS (widening automático)
  byte → short → int → long → float → double

REGLA DE DIVISIÓN
  int   / int   → int  (trunca decimales)
  double / int  → double
  int   / double → double

CASTING EXPLÍCITO
  (tipo) expresion    Ej: (int) 3.9 → 3

CONVERSIÓN String ↔ número
  int n = Integer.parseInt("42");
  double d = Double.parseDouble("3.14");
  String s = String.valueOf(42);
  String s = Integer.toString(42);

CONSTANTES
  final TIPO NOMBRE = valor;

COMPARACIÓN DE STRINGS
  s1.equals(s2)           // Contenido igual
  s1.equalsIgnoreCase(s2) // Ignora mayúsculas
  s1.compareTo(s2)        // Orden lexicográfico

MÉTODOS ÚTILES DE STRING
  s.length()           // Longitud
  s.toUpperCase()      // MAYÚSCULAS
  s.toLowerCase()      // minúsculas
  s.trim()             // Elimina espacios extremos
  s.charAt(i)          // Carácter en posición i
  s.substring(i, j)    // Subcadena [i, j)
  s.contains("x")      // ¿Contiene "x"?
```
