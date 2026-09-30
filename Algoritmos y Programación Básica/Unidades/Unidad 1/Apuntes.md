# Apuntes — Unidad 1: Introducción a la Programación
**Asignatura:** Algoritmos y Programación Básica · IX24013-B1
**Docente:** Heybertt Moreno Díaz
**Última actualización:** 2026-09-29

---

## 1. ¿Qué es un Algoritmo?

Un **algoritmo** es una secuencia finita, ordenada y precisa de instrucciones que resuelve un problema dado. No es código — es la lógica pura antes de que intervenga ningún lenguaje.

### Propiedades obligatorias de todo algoritmo

| Propiedad | Significado práctico |
|:---|:---|
| **Finito** | Debe terminar. Un ciclo infinito no es un algoritmo correcto. |
| **Definido** | Cada paso tiene una única interpretación. No hay ambigüedad. |
| **Entrada** | Puede recibir cero o más datos iniciales. |
| **Salida** | Produce al menos un resultado (en pantalla, archivo, etc.). |
| **Efectivo** | Cada paso es ejecutable en tiempo real con recursos limitados. |

> **Idea clave:** Un algoritmo es independiente del lenguaje. El mismo algoritmo de ordenamiento puede escribirse en Java, Python o C++. Lo que cambia es la sintaxis, no la lógica.

---

## 2. Pseudocódigo

El pseudocódigo es una representación textual informal del algoritmo, escrita en lenguaje natural con estructura de código. Sirve para planificar antes de programar.

### Convenciones estándar utilizadas en el curso

```
INICIO
  LEER variable
  ESCRIBIR "texto"
  SI condicion ENTONCES
    instruccion
  SINO
    instruccion
  FIN_SI
  PARA i DESDE 1 HASTA n HACER
    instruccion
  FIN_PARA
  MIENTRAS condicion HACER
    instruccion
  FIN_MIENTRAS
FIN
```

### Ejemplo completo: Calcular el promedio de tres notas

```
INICIO
  LEER nota1, nota2, nota3
  promedio <- (nota1 + nota2 + nota3) / 3
  SI promedio >= 3.0 ENTONCES
    ESCRIBIR "Aprobado con promedio: ", promedio
  SINO
    ESCRIBIR "Reprobado con promedio: ", promedio
  FIN_SI
FIN
```

### Ejemplo completo: Encontrar el mayor de dos números

```
INICIO
  LEER a, b
  SI a > b ENTONCES
    ESCRIBIR "El mayor es: ", a
  SINO
    SI b > a ENTONCES
      ESCRIBIR "El mayor es: ", b
    SINO
      ESCRIBIR "Son iguales"
    FIN_SI
  FIN_SI
FIN
```

---

## 3. Diagramas de Flujo

Los diagramas de flujo son representaciones gráficas del algoritmo. Cada figura tiene un significado específico:

| Figura | Forma | Uso |
|:---|:---:|:---|
| **Óvalo / Cápsula** | ( ) | Inicio y Fin del programa |
| **Rectángulo** | [ ] | Proceso / instrucción (cálculo, asignación) |
| **Rombo** | ◇ | Decisión (condición verdadero/falso) |
| **Paralelogramo** | // | Entrada de datos (Leer) o salida (Escribir) |
| **Flecha** | → | Flujo de control entre pasos |

### Reglas de construcción

1. Siempre hay **un solo inicio** y puede haber **uno o más finales**.
2. Las flechas nunca se cruzan sin un conector explícito.
3. Los rombos siempre tienen **exactamente dos salidas**: Sí (Verdadero) y No (Falso).
4. Los ciclos siempre tienen una condición de salida; de lo contrario, el diagrama es incorrecto.

### Herramientas recomendadas

- **draw.io / diagrams.net:** https://app.diagrams.net — gratuito, en línea, exporta a PNG/PDF.
- **Lucidchart:** https://lucidchart.com — versión gratuita suficiente para el curso.

---

## 4. Primeros Pasos en Java

### ¿Qué necesita el entorno?

| Herramienta | Descripción | Descarga |
|:---|:---|:---|
| **JDK 21 LTS** | Java Development Kit — compila y ejecuta | https://adoptium.net |
| **IntelliJ IDEA CE** | IDE recomendado, Community Edition gratuita | https://jetbrains.com/idea |
| **VS Code + Extension Pack for Java** | Alternativa ligera | https://code.visualstudio.com |

### Estructura mínima de un programa Java

```java
// NombreArchivo.java  (el archivo DEBE llamarse igual que la clase)
public class HolaMundo {
    public static void main(String[] args) {
        // Punto de entrada de todo programa Java
        System.out.println("Hola, mundo");
    }
}
```

**Anatomía de cada parte:**

| Elemento | ¿Qué significa? |
|:---|:---|
| `public class HolaMundo` | Declara una clase pública llamada HolaMundo |
| `public static void main(String[] args)` | Método principal — la JVM siempre empieza aquí |
| `System.out.println(...)` | Imprime texto en consola con salto de línea |
| `System.out.print(...)` | Imprime texto en consola SIN salto de línea |

### Compilar y ejecutar desde la terminal

```bash
# Compilar (genera HolaMundo.class)
javac HolaMundo.java

# Ejecutar (carga la JVM y corre la clase)
java HolaMundo
```

### Variables y tipos primitivos básicos (introducción)

```java
public class VariablesBasicas {
    public static void main(String[] args) {
        int edad = 20;           // Entero (−2^31 a 2^31 − 1)
        double precio = 15.99;   // Decimal de doble precisión
        char letra = 'A';        // Un carácter Unicode (comillas simples)
        boolean activo = true;   // Solo true o false
        String nombre = "Juan";  // Texto (no es primitivo, es objeto)

        System.out.println("Nombre: " + nombre);
        System.out.println("Edad: " + edad);
        System.out.println("Precio: " + precio);
    }
}
```

### Lectura de datos por consola (Scanner)

```java
import java.util.Scanner;  // Importar la clase Scanner

public class LecturaConsola {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);  // Crear objeto Scanner

        System.out.print("Ingrese su nombre: ");
        String nombre = sc.nextLine();        // Leer String completo

        System.out.print("Ingrese su edad: ");
        int edad = sc.nextInt();              // Leer entero

        System.out.println("Hola " + nombre + ", tienes " + edad + " años.");
        sc.close();  // Cerrar el recurso
    }
}
```

**Métodos del Scanner más usados:**

| Método | Tipo que lee |
|:---|:---|
| `sc.nextInt()` | `int` |
| `sc.nextDouble()` | `double` |
| `sc.nextLine()` | `String` (con espacios) |
| `sc.next()` | `String` (hasta espacio) |
| `sc.nextBoolean()` | `boolean` |

> **Trampa clásica:** Si usas `nextInt()` y luego `nextLine()`, la segunda lectura captura el salto de línea residual y devuelve una cadena vacía. Solución: agregar un `sc.nextLine()` de limpieza entre ambas llamadas.

---

## 5. Ejemplo integrador: Pseudocódigo + Java

**Problema:** Calcular el área y el perímetro de un rectángulo dado su base y altura.

**Pseudocódigo:**
```
INICIO
  LEER base, altura
  area    <- base * altura
  perimetro <- 2 * (base + altura)
  ESCRIBIR "Área: ", area
  ESCRIBIR "Perímetro: ", perimetro
FIN
```

**Código Java:**
```java
import java.util.Scanner;

public class Rectangulo {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Base (cm): ");
        double base = sc.nextDouble();

        System.out.print("Altura (cm): ");
        double altura = sc.nextDouble();

        double area = base * altura;
        double perimetro = 2 * (base + altura);

        System.out.printf("Área: %.2f cm²%n", area);
        System.out.printf("Perímetro: %.2f cm%n", perimetro);

        sc.close();
    }
}
```

> **Nota:** `printf` permite formateo con especificadores como `%.2f` (decimal con 2 cifras) y `%n` (salto de línea portátil).

---

## 6. Errores Comunes en esta Unidad

| Error | Ejemplo incorrecto | Corrección |
|:---|:---|:---|
| Archivo con nombre distinto a la clase | `Main.java` con `public class Hola` | El archivo debe llamarse `Hola.java` |
| Olvidar `import java.util.Scanner` | Usar `Scanner` sin importar | Agregar `import java.util.Scanner;` al inicio |
| Confundir `=` con `==` | `if (x = 5)` | `if (x == 5)` |
| Punto y coma faltante | `int x = 5` | `int x = 5;` |
| Usar `System.out.println` en minúscula | `system.out.println(...)` | Java es case-sensitive: `System` con S mayúscula |
| Mezcla de `nextInt()` + `nextLine()` | Scanner capta salto de línea vacío | Agregar `sc.nextLine()` de limpieza |

---

## 7. Métodos de Estudio para esta Unidad

### Active Recall — Preguntas de autoevaluación

1. Sin mirar apuntes: ¿cuáles son las 5 propiedades de un algoritmo? Escríbelas.
2. Dibuja el diagrama de flujo de un algoritmo que lea un número y diga si es positivo, negativo o cero.
3. Escribe el pseudocódigo para calcular el factorial de un número entero positivo.
4. Escribe de memoria la estructura mínima de un programa Java (sin copiar).
5. ¿Cuál es la diferencia entre `print` y `println`? ¿Y entre `nextLine()` y `next()`?

### Técnica Feynman aplicada

Toma un concepto (por ejemplo, "variable") y explícalo como si se lo dijeras a alguien que nunca ha programado. Si tropiezas en algún punto, ahí está la laguna a revisar.

### Ejercicio de práctica recomendado

Escribe el pseudocódigo, luego el diagrama de flujo (en papel), y finalmente el código Java de estos problemas:
1. Leer dos números enteros e imprimir su suma, resta, producto y cociente.
2. Leer la temperatura en Celsius y convertirla a Fahrenheit: `F = (C × 9/5) + 32`.
3. Leer el nombre y la nota de un estudiante, e imprimir si aprobó (nota ≥ 3.0) o reprobó.

---

## 8. Recursos Externos

### YouTube

| Canal | Descripción | URL |
|:---|:---|:---|
| **Píldoras Informáticas** | Curso Java desde cero, explicaciones muy claras. Playlist: "Curso Java Desde Cero" | https://www.youtube.com/@pildorasinformaticas |
| **CódigoFacilito** | Tutoriales modernos de Java y lógica de programación | https://www.youtube.com/@codigofacilito |
| **Programando en JAVA** | Canal especializado en Java, incluye pseudocódigo y ejercicios | https://www.youtube.com/@programandoenjava |

### Libros y sitios

| Recurso | Capítulo / Sección relevante |
|:---|:---|
| Liang, Y. D. — *Introduction to Java Programming* | Cap. 1: Introduction to Computers, Programs, and Java |
| Joyanes Aguilar — *Fundamentos de Programación* | Cap. 1–3: Algoritmos, diagramas de flujo, pseudocódigo |
| **w3schools Java** | https://www.w3schools.com/java — referencia rápida de sintaxis |
| **Oracle Java Tutorials** | https://docs.oracle.com/javase/tutorial/ — documentación oficial |
| **MOOC Java — Univ. Helsinki** | https://java-programming.mooc.fi — ejercicios interactivos en inglés |

---

## 9. Referencia Rápida

```
TIPOS PRIMITIVOS JAVA
  byte    → −128 a 127
  short   → −32,768 a 32,767
  int     → −2,147,483,648 a 2,147,483,647
  long    → muy grande (sufijo L: 100L)
  float   → decimal simple precisión (sufijo f: 3.14f)
  double  → decimal doble precisión (default para decimales)
  char    → un carácter ('A', '1', '\n')
  boolean → true / false

OPERADORES ARITMÉTICOS
  +  suma          -  resta
  *  multiplicación  /  división (entera si ambos son int)
  %  módulo (resto de la división entera)

OPERADORES RELACIONALES
  ==  igual a        !=  distinto de
  >   mayor que      <   menor que
  >=  mayor o igual  <=  menor o igual

OPERADORES LÓGICOS
  &&  AND (ambas condiciones verdaderas)
  ||  OR  (al menos una verdadera)
  !   NOT (negación)

SALIDA EN CONSOLA
  System.out.print("texto");        // sin salto
  System.out.println("texto");      // con salto
  System.out.printf("%.2f%n", x);  // formato

SCANNER — LECTURA
  import java.util.Scanner;
  Scanner sc = new Scanner(System.in);
  int    n = sc.nextInt();
  double d = sc.nextDouble();
  String s = sc.nextLine();
  sc.close();
```
