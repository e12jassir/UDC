# Apuntes — Unidad 4: Funciones y Arreglos
**Asignatura:** Algoritmos y Programación Básica · IX24013-B1
**Docente:** Heybertt Moreno Díaz
**Última actualización:** 2026-09-29

---

## 1. Métodos (Funciones) en Java

Un **método** es un bloque de código con nombre que realiza una tarea específica. Se define una vez y puede llamarse (invocarse) múltiples veces.

### Ventajas de usar métodos

- **Reutilización:** escribir el código una sola vez y usarlo muchas veces.
- **Modularidad:** dividir un problema grande en partes manejables.
- **Legibilidad:** código más claro y fácil de mantener.
- **Abstracción:** el código que llama al método no necesita saber cómo funciona internamente.

### Anatomía de un método en Java

```java
[modificadores] tipoRetorno nombreMetodo(Tipo param1, Tipo param2, ...) {
    // Cuerpo del método
    return valor;  // si tipoRetorno != void
}
```

| Componente | Descripción |
|:---|:---|
| `modificadores` | `public`, `private`, `static`, etc. |
| `tipoRetorno` | Tipo del valor que retorna (`int`, `double`, `String`, `void` si no retorna) |
| `nombreMetodo` | Identificador en camelCase |
| `parámetros` | Variables de entrada (pueden ser cero) |
| `return` | Devuelve el valor y termina el método |

---

## 2. Métodos con Retorno

```java
public class EjemplosMetodos {

    // Método que recibe dos enteros y retorna su suma
    static int sumar(int a, int b) {
        return a + b;
    }

    // Método que recibe un double y retorna el área del círculo
    static double areaCirculo(double radio) {
        return Math.PI * radio * radio;
    }

    // Método que recibe una nota y retorna la clasificación
    static String clasificarNota(double nota) {
        if (nota >= 4.5) return "Excelente";
        if (nota >= 3.5) return "Bueno";
        if (nota >= 3.0) return "Aprobado";
        return "Reprobado";
    }

    // Método que determina si un número es primo
    static boolean esPrimo(int n) {
        if (n < 2) return false;
        for (int i = 2; i <= Math.sqrt(n); i++) {
            if (n % i == 0) return false;
        }
        return true;
    }

    public static void main(String[] args) {
        System.out.println("3 + 5 = " + sumar(3, 5));
        System.out.printf("Área círculo r=4: %.2f%n", areaCirculo(4.0));
        System.out.println("Nota 4.2: " + clasificarNota(4.2));
        System.out.println("¿17 es primo? " + esPrimo(17));
    }
}
```

### Métodos void — Sin retorno

```java
// No devuelve valor; realiza una acción (impresión, modificación externa, etc.)
static void imprimirSeparador(char caracter, int longitud) {
    for (int i = 0; i < longitud; i++) {
        System.out.print(caracter);
    }
    System.out.println();
}

// Uso:
imprimirSeparador('-', 40);
// Salida: ----------------------------------------
```

---

## 3. Paso por Valor vs Paso por Referencia

**Concepto crítico:** En Java, los primitivos se pasan **por valor** (se copia el dato), mientras que los objetos y arreglos se pasan **por referencia** (se pasa la dirección de memoria).

### Paso por valor (primitivos)

```java
static void intentarModificar(int x) {
    x = x * 2;     // Modifica la COPIA local, no el original
    System.out.println("Dentro del método: x = " + x);
}

public static void main(String[] args) {
    int numero = 10;
    intentarModificar(numero);
    System.out.println("En main: numero = " + numero);  // Sigue siendo 10
}

// Salida:
// Dentro del método: x = 20
// En main: numero = 10
```

**Conclusión:** Los cambios a primitivos dentro del método no afectan la variable original.

### Paso por referencia (arreglos y objetos)

```java
static void duplicarArreglo(int[] arr) {
    for (int i = 0; i < arr.length; i++) {
        arr[i] *= 2;  // Modifica el ARREGLO ORIGINAL (misma memoria)
    }
}

public static void main(String[] args) {
    int[] nums = {1, 2, 3, 4, 5};
    duplicarArreglo(nums);

    for (int n : nums) {
        System.out.print(n + " ");  // 2 4 6 8 10
    }
}
```

**Conclusión:** Los arreglos pasados como parámetros son modificados en la función original.

---

## 4. Sobrecarga de Métodos (Overloading)

Java permite definir múltiples métodos con el mismo nombre pero **distintos parámetros** (tipo o cantidad).

```java
public class CalculadoraOverload {

    static int sumar(int a, int b) {
        return a + b;
    }

    static double sumar(double a, double b) {
        return a + b;
    }

    static int sumar(int a, int b, int c) {
        return a + b + c;
    }

    public static void main(String[] args) {
        System.out.println(sumar(3, 4));        // Llama versión int: 7
        System.out.println(sumar(3.0, 4.5));   // Llama versión double: 7.5
        System.out.println(sumar(1, 2, 3));    // Llama versión 3 args: 6
    }
}
```

---

## 5. Recursividad

Un método es **recursivo** cuando se llama a sí mismo. Toda función recursiva necesita:
1. **Caso base:** condición que detiene la recursión.
2. **Caso recursivo:** llamada al mismo método con un problema más pequeño.

```java
// Factorial recursivo: n! = n × (n-1)!
static long factorial(int n) {
    if (n <= 1) return 1;          // Caso base
    return n * factorial(n - 1);   // Caso recursivo
}

// Fibonacci recursivo: fib(n) = fib(n-1) + fib(n-2)
static int fibonacci(int n) {
    if (n <= 1) return n;          // Caso base
    return fibonacci(n - 1) + fibonacci(n - 2);
}

public static void main(String[] args) {
    System.out.println("5! = " + factorial(5));   // 120
    System.out.println("fib(7) = " + fibonacci(7)); // 13
}
```

> **Advertencia:** La recursión sin caso base correcta produce `StackOverflowError`. Siempre verificar que la recursión converge.

---

## 6. Arreglos Unidimensionales (Vectores)

Un **arreglo** es una estructura de datos que almacena múltiples valores del mismo tipo en posiciones contiguas de memoria.

### Declaración, inicialización y acceso

```java
// Forma 1: declarar y asignar tamaño (valores por defecto: 0, false, null)
int[] notas = new int[5];      // {0, 0, 0, 0, 0}

// Forma 2: declarar e inicializar con valores
double[] precios = {15.5, 20.0, 8.75, 33.2};

// Acceso por índice (siempre desde 0 hasta length-1)
notas[0] = 85;
notas[1] = 92;
System.out.println(notas[0]);          // 85
System.out.println(precios.length);    // 4 (número de elementos)
```

### Recorrer un arreglo

```java
int[] datos = {10, 25, 8, 47, 33};

// Forma 1: for tradicional (cuando se necesita el índice)
for (int i = 0; i < datos.length; i++) {
    System.out.println("datos[" + i + "] = " + datos[i]);
}

// Forma 2: for-each (cuando solo se necesita el valor)
for (int valor : datos) {
    System.out.print(valor + " ");
}
```

### Operaciones comunes sobre arreglos

```java
import java.util.Scanner;

public class OperacionesArreglo {

    static void leerArreglo(int[] arr) {
        Scanner sc = new Scanner(System.in);
        for (int i = 0; i < arr.length; i++) {
            System.out.printf("arr[%d] = ", i);
            arr[i] = sc.nextInt();
        }
    }

    static int calcularSuma(int[] arr) {
        int suma = 0;
        for (int v : arr) suma += v;
        return suma;
    }

    static double calcularPromedio(int[] arr) {
        return (double) calcularSuma(arr) / arr.length;
    }

    static int encontrarMaximo(int[] arr) {
        int max = arr[0];
        for (int i = 1; i < arr.length; i++) {
            if (arr[i] > max) max = arr[i];
        }
        return max;
    }

    static int encontrarMinimo(int[] arr) {
        int min = arr[0];
        for (int i = 1; i < arr.length; i++) {
            if (arr[i] < min) min = arr[i];
        }
        return min;
    }

    static void invertirArreglo(int[] arr) {
        int inicio = 0;
        int fin = arr.length - 1;
        while (inicio < fin) {
            int temp = arr[inicio];
            arr[inicio] = arr[fin];
            arr[fin] = temp;
            inicio++;
            fin--;
        }
    }

    static boolean buscarElemento(int[] arr, int objetivo) {
        for (int v : arr) {
            if (v == objetivo) return true;
        }
        return false;
    }

    public static void main(String[] args) {
        int n = 5;
        int[] datos = new int[n];

        System.out.println("Ingrese " + n + " números:");
        leerArreglo(datos);

        System.out.println("Suma:    " + calcularSuma(datos));
        System.out.printf("Promedio: %.2f%n", calcularPromedio(datos));
        System.out.println("Máximo:  " + encontrarMaximo(datos));
        System.out.println("Mínimo:  " + encontrarMinimo(datos));

        invertirArreglo(datos);
        System.out.print("Invertido: ");
        for (int v : datos) System.out.print(v + " ");

        System.out.println("\n¿Existe 10? " + buscarElemento(datos, 10));
    }
}
```

---

## 7. Arreglos Bidimensionales (Matrices)

Una **matriz** es un arreglo de arreglos — una tabla con filas y columnas.

### Declaración y acceso

```java
// Declarar una matriz de 3 filas × 4 columnas
int[][] matriz = new int[3][4];

// Inicializar con valores explícitos
int[][] tabla = {
    {1,  2,  3,  4},
    {5,  6,  7,  8},
    {9, 10, 11, 12}
};

// Acceso: [fila][columna], ambos desde 0
System.out.println(tabla[0][0]);  // 1
System.out.println(tabla[1][2]);  // 7
System.out.println(tabla[2][3]);  // 12

// Dimensiones
int filas = tabla.length;        // 3
int columnas = tabla[0].length;  // 4
```

### Recorrer una matriz

```java
int[][] m = {
    {1, 2, 3},
    {4, 5, 6},
    {7, 8, 9}
};

// Recorrido fila por fila
for (int i = 0; i < m.length; i++) {
    for (int j = 0; j < m[i].length; j++) {
        System.out.printf("%3d", m[i][j]);
    }
    System.out.println();
}
```

### Operaciones sobre matrices

```java
public class OperacionesMatriz {

    // Suma de dos matrices A + B
    static int[][] sumarMatrices(int[][] A, int[][] B) {
        int filas = A.length;
        int cols  = A[0].length;
        int[][] resultado = new int[filas][cols];

        for (int i = 0; i < filas; i++) {
            for (int j = 0; j < cols; j++) {
                resultado[i][j] = A[i][j] + B[i][j];
            }
        }
        return resultado;
    }

    // Transpuesta de una matriz
    static int[][] transponerMatriz(int[][] M) {
        int filas = M.length;
        int cols  = M[0].length;
        int[][] T = new int[cols][filas];

        for (int i = 0; i < filas; i++) {
            for (int j = 0; j < cols; j++) {
                T[j][i] = M[i][j];
            }
        }
        return T;
    }

    // Suma de la diagonal principal (solo para matrices cuadradas)
    static int trazaMatriz(int[][] M) {
        int traza = 0;
        for (int i = 0; i < M.length; i++) {
            traza += M[i][i];
        }
        return traza;
    }

    static void imprimirMatriz(int[][] M) {
        for (int[] fila : M) {
            for (int val : fila) {
                System.out.printf("%4d", val);
            }
            System.out.println();
        }
    }

    public static void main(String[] args) {
        int[][] A = {{1, 2, 3}, {4, 5, 6}, {7, 8, 9}};
        int[][] B = {{9, 8, 7}, {6, 5, 4}, {3, 2, 1}};

        System.out.println("Suma A + B:");
        imprimirMatriz(sumarMatrices(A, B));

        System.out.println("Transpuesta de A:");
        imprimirMatriz(transponerMatriz(A));

        System.out.println("Traza de A: " + trazaMatriz(A));  // 15
    }
}
```

---

## 8. Clase Arrays — Utilidades Estándar

```java
import java.util.Arrays;

int[] arr = {5, 3, 8, 1, 9, 2};

Arrays.sort(arr);                 // Ordena en ascendente: {1,2,3,5,8,9}
System.out.println(Arrays.toString(arr));  // [1, 2, 3, 5, 8, 9]

int pos = Arrays.binarySearch(arr, 5);    // Búsqueda binaria (requiere ordenado)
System.out.println("Posición de 5: " + pos);

int[] copia = Arrays.copyOf(arr, arr.length);   // Copia completa
int[] parcial = Arrays.copyOfRange(arr, 1, 4);  // Elementos [1, 4) → {2,3,5}

Arrays.fill(arr, 0);  // Llena todo el arreglo con 0
```

---

## 9. Programa Integrador — Sistema de Notas con Métodos y Arreglos

```java
import java.util.Scanner;
import java.util.Arrays;

/**
 * Sistema de gestión de notas que utiliza:
 * - Métodos con y sin retorno
 * - Paso de arreglos por referencia
 * - Operaciones sobre arreglos
 * - Arreglos 2D para materias × notas
 */
public class SistemaNotas {

    static final int NUM_MATERIAS = 3;
    static final int NUM_NOTAS    = 4;
    static final String[] MATERIAS = {"Algoritmos", "Cálculo", "Metodología"};

    static void ingresarNotas(double[][] notas) {
        Scanner sc = new Scanner(System.in);
        for (int i = 0; i < NUM_MATERIAS; i++) {
            System.out.println("\n--- " + MATERIAS[i] + " ---");
            for (int j = 0; j < NUM_NOTAS; j++) {
                double nota;
                do {
                    System.out.printf("  Nota %d (0.0-5.0): ", j + 1);
                    nota = sc.nextDouble();
                } while (nota < 0 || nota > 5);
                notas[i][j] = nota;
            }
        }
    }

    static double promedioFila(double[] fila) {
        double suma = 0;
        for (double v : fila) suma += v;
        return suma / fila.length;
    }

    static void imprimirReporte(double[][] notas) {
        System.out.println("\n========== REPORTE DE NOTAS ==========");
        System.out.printf("%-15s | %-5s %-5s %-5s %-5s | %-8s | %-12s%n",
                          "Materia", "N1", "N2", "N3", "N4", "Promedio", "Estado");
        System.out.println("-".repeat(65));

        for (int i = 0; i < NUM_MATERIAS; i++) {
            double prom = promedioFila(notas[i]);
            String estado = (prom >= 3.0) ? "Aprobado" : "Reprobado";
            System.out.printf("%-15s | %-5.1f %-5.1f %-5.1f %-5.1f | %-8.2f | %-12s%n",
                              MATERIAS[i],
                              notas[i][0], notas[i][1], notas[i][2], notas[i][3],
                              prom, estado);
        }

        System.out.println("=" .repeat(65));
    }

    public static void main(String[] args) {
        double[][] notas = new double[NUM_MATERIAS][NUM_NOTAS];
        ingresarNotas(notas);
        imprimirReporte(notas);
    }
}
```

---

## 10. Errores Comunes

| Error | Descripción | Corrección |
|:---|:---|:---|
| `ArrayIndexOutOfBoundsException` | Acceder a índice fuera de rango (ej: arr[5] en arr de longitud 5) | Usar índices de 0 a `arr.length - 1` |
| Confundir paso por valor con por referencia | Esperar que un int cambió al salir del método | Los primitivos no cambian; usar return o arreglos |
| Iterar un arreglo 2D con `arr.length` incorrecto | Usar `matriz.length` para columnas | `matriz.length` = filas; `matriz[0].length` = columnas |
| `NullPointerException` al no inicializar el arreglo | `int[] arr; arr[0] = 5;` | `int[] arr = new int[N]; arr[0] = 5;` |
| Método sin `return` cuando el tipo no es `void` | Compilador reporta error | Agregar `return valor;` o cambiar tipo a `void` |
| Recursión infinita | Olvidar o definir mal el caso base | Verificar siempre la condición de parada |

---

## 11. Métodos de Estudio

### Active Recall — Preguntas

1. Escribe la firma (signature) de un método que recibe dos doubles y retorna un boolean.
2. ¿Por qué un arreglo sí se modifica dentro de un método, pero un `int` no?
3. ¿Cuál es la diferencia entre un método `void` y uno con retorno?
4. Traza manualmente `factorial(4)` mostrando cada llamada recursiva.
5. ¿Qué hace `Arrays.sort()` y cuál es su condición para que `binarySearch()` funcione?

### Ejercicios de práctica

1. Escribir un método `esPalindromo(String s)` que devuelva `true` si el String es igual al revés.
2. Escribir un método `ordenarBurbuja(int[] arr)` que ordene el arreglo usando el algoritmo de burbuja.
3. Crear una clase con métodos para multiplicar dos matrices 3×3 y mostrar el resultado.
4. Escribir un método recursivo que calcule la potencia `base^exp` sin usar `Math.pow`.

---

## 12. Recursos Externos

| Recurso | Descripción | URL |
|:---|:---|:---|
| **Píldoras Informáticas** | Videos específicos de métodos, arreglos y matrices en Java | https://www.youtube.com/@pildorasinformaticas |
| **CódigoFacilito** | Arreglos y métodos con ejercicios aplicados | https://www.youtube.com/@codigofacilito |
| **Liang — Introduction to Java Programming** | Cap. 5 (Métodos), Cap. 7 (Arreglos 1D), Cap. 8 (Matrices) | Biblioteca UDC / PDF |
| **W3Schools Java Arrays** | Referencia rápida de arreglos con ejemplos ejecutables en línea | https://www.w3schools.com/java/java_arrays.asp |
| **Exercism — Java** | Ejercicios de práctica con retroalimentación, muchos sobre arreglos y métodos | https://exercism.org/tracks/java |

---

## 13. Referencia Rápida

```
DEFINICIÓN DE MÉTODO
  static tipoRetorno nombre(Tipo param) {
      return valor;  // omitir si void
  }

LLAMADA A MÉTODO
  tipo resultado = nombre(argumento);
  nombre(argumento);  // si es void

ARREGLO 1D
  int[] arr = new int[N];
  int[] arr = {v1, v2, v3};
  arr[i]           // acceso
  arr.length       // tamaño

ARREGLO 2D (MATRIZ)
  int[][] m = new int[filas][cols];
  int[][] m = {{...}, {...}};
  m[i][j]          // acceso
  m.length          // número de filas
  m[0].length       // número de columnas

RECORRIDO ARREGLO
  for (int i = 0; i < arr.length; i++) { arr[i] }
  for (int v : arr) { v }

RECORRIDO MATRIZ
  for (int i = 0; i < m.length; i++)
      for (int j = 0; j < m[i].length; j++)
          m[i][j]

UTILIDADES Arrays
  Arrays.sort(arr)                  // orden ascendente
  Arrays.toString(arr)             // "[1, 2, 3]"
  Arrays.copyOf(arr, n)            // copia primeros n
  Arrays.copyOfRange(arr, i, j)    // copia [i, j)
  Arrays.fill(arr, val)            // llena con val
  Arrays.binarySearch(arr, val)    // búsqueda binaria

PASO POR VALOR vs REFERENCIA
  Primitivos (int, double, etc.) → copia → no cambia el original
  Arreglos / Objetos             → referencia → SÍ cambia el original
```
