# Apuntes — Unidad 3: Estructuras de Control
**Asignatura:** Algoritmos y Programación Básica · IX24013-B1
**Docente:** Heybertt Moreno Díaz
**Última actualización:** 2026-09-29

---

## 1. Estructuras Condicionales

Las estructuras condicionales permiten que el programa tome decisiones y ejecute bloques de código diferentes según si se cumple o no una condición.

### 1.1 if simple

```java
if (condicion) {
    // Bloque que se ejecuta si condicion es true
}
```

**Ejemplo:**
```java
int nota = 75;
if (nota >= 60) {
    System.out.println("Aprobado");
}
```

### 1.2 if-else

```java
if (condicion) {
    // Ejecuta si condicion es true
} else {
    // Ejecuta si condicion es false
}
```

**Ejemplo — Número par o impar:**
```java
import java.util.Scanner;

public class ParOImpar {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Ingrese un número entero: ");
        int n = sc.nextInt();

        if (n % 2 == 0) {
            System.out.println(n + " es PAR");
        } else {
            System.out.println(n + " es IMPAR");
        }
        sc.close();
    }
}
```

### 1.3 if-else if-else (escalera de condiciones)

```java
if (condicion1) {
    // Caso 1
} else if (condicion2) {
    // Caso 2
} else if (condicion3) {
    // Caso 3
} else {
    // Caso por defecto
}
```

**Ejemplo — Clasificar nota académica:**
```java
import java.util.Scanner;

public class ClasificadorNota {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Ingrese la nota (0.0 - 5.0): ");
        double nota = sc.nextDouble();

        String clasificacion;

        if (nota < 0 || nota > 5) {
            clasificacion = "Nota inválida";
        } else if (nota >= 4.6) {
            clasificacion = "Excelente";
        } else if (nota >= 4.0) {
            clasificacion = "Sobresaliente";
        } else if (nota >= 3.5) {
            clasificacion = "Bueno";
        } else if (nota >= 3.0) {
            clasificacion = "Aprobado";
        } else {
            clasificacion = "Reprobado";
        }

        System.out.printf("Nota: %.1f → %s%n", nota, clasificacion);
        sc.close();
    }
}
```

### 1.4 Operador Ternario

Forma compacta de un `if-else` que retorna un valor.

```java
tipo variable = (condicion) ? valorSiTrue : valorSiFalse;

// Ejemplo:
int edad = 20;
String estado = (edad >= 18) ? "Mayor de edad" : "Menor de edad";
System.out.println(estado);  // Mayor de edad

// Equivale a:
// if (edad >= 18) estado = "Mayor de edad"; else estado = "Menor de edad";
```

### 1.5 switch-case

Ideal cuando se compara una sola variable contra múltiples valores constantes (int, char, String).

```java
switch (expresion) {
    case valor1:
        // instrucciones
        break;      // ¡OBLIGATORIO para evitar "fall-through"!
    case valor2:
        // instrucciones
        break;
    default:
        // si ningún case coincide
}
```

**Ejemplo completo — Menú de operaciones aritméticas:**
```java
import java.util.Scanner;

public class CalculadoraSwitch {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Ingrese el primer número: ");
        double a = sc.nextDouble();

        System.out.print("Ingrese el segundo número: ");
        double b = sc.nextDouble();

        System.out.println("Operación: + | - | * | /");
        System.out.print("Ingrese el operador: ");
        String op = sc.next();

        double resultado;
        boolean valido = true;

        switch (op) {
            case "+":
                resultado = a + b;
                System.out.printf("%.2f + %.2f = %.2f%n", a, b, resultado);
                break;
            case "-":
                resultado = a - b;
                System.out.printf("%.2f - %.2f = %.2f%n", a, b, resultado);
                break;
            case "*":
                resultado = a * b;
                System.out.printf("%.2f * %.2f = %.2f%n", a, b, resultado);
                break;
            case "/":
                if (b == 0) {
                    System.out.println("Error: división por cero.");
                    valido = false;
                } else {
                    resultado = a / b;
                    System.out.printf("%.2f / %.2f = %.2f%n", a, b, resultado);
                }
                break;
            default:
                System.out.println("Operador no reconocido.");
                valido = false;
        }

        sc.close();
    }
}
```

---

## 2. Estructuras de Repetición (Ciclos)

### 2.1 Ciclo while — "Mientras"

Se usa cuando **no se sabe de antemano** cuántas veces va a repetirse.

```java
while (condicion) {
    // Cuerpo del ciclo
    // Debe modificarse algo para que la condicion eventualmente sea false
}
```

**Ejemplo — Validar entrada del usuario:**
```java
import java.util.Scanner;

public class ValidadorEntrada {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int numero = -1;

        while (numero < 0) {
            System.out.print("Ingrese un número positivo: ");
            numero = sc.nextInt();
            if (numero < 0) {
                System.out.println("El número debe ser positivo. Intente de nuevo.");
            }
        }

        System.out.println("Número aceptado: " + numero);
        sc.close();
    }
}
```

**Ejemplo — Suma de dígitos de un número:**
```java
import java.util.Scanner;

public class SumaDigitos {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Ingrese un número entero positivo: ");
        int n = sc.nextInt();
        int suma = 0;
        int temp = n;

        while (temp > 0) {
            suma += temp % 10;  // Extraer último dígito
            temp /= 10;         // Eliminar último dígito
        }

        System.out.println("Suma de dígitos de " + n + " = " + suma);
        sc.close();
    }
}
```

### 2.2 Ciclo for — "Para"

Se usa cuando **se conoce de antemano** el número de iteraciones.

```java
for (inicializacion; condicion; incremento) {
    // Cuerpo del ciclo
}
```

**Estructura de ejecución:**
1. Se ejecuta `inicializacion` (solo una vez).
2. Se evalúa `condicion`. Si es false, el ciclo termina.
3. Se ejecuta el cuerpo.
4. Se ejecuta `incremento`.
5. Volver al paso 2.

**Ejemplo — Tabla de multiplicar:**
```java
import java.util.Scanner;

public class TablaMultiplicar {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Ingrese un número para ver su tabla: ");
        int n = sc.nextInt();

        System.out.println("\n--- Tabla del " + n + " ---");
        for (int i = 1; i <= 10; i++) {
            System.out.printf("%2d × %2d = %3d%n", n, i, n * i);
        }
        sc.close();
    }
}
```

**Ejemplo — Sumatoria y factorial:**
```java
public class SumatoriaYFactorial {
    public static void main(String[] args) {
        int n = 10;

        // Sumatoria 1 + 2 + ... + n
        int suma = 0;
        for (int i = 1; i <= n; i++) {
            suma += i;
        }
        System.out.println("Suma 1 a " + n + " = " + suma);  // 55

        // Factorial de n (n!)
        long factorial = 1;
        for (int i = 2; i <= n; i++) {
            factorial *= i;
        }
        System.out.println(n + "! = " + factorial);  // 3628800
    }
}
```

### 2.3 Ciclo do-while — "Haga-Mientras"

Similar al `while`, pero **garantiza al menos una ejecución** del cuerpo, porque la condición se evalúa al final.

```java
do {
    // Cuerpo — se ejecuta mínimo UNA VEZ
} while (condicion);
```

**Ejemplo — Menú interactivo:**
```java
import java.util.Scanner;

public class MenuInteractivo {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int opcion;

        do {
            System.out.println("\n=== MENÚ ===");
            System.out.println("1. Saludar");
            System.out.println("2. Mostrar fecha");
            System.out.println("0. Salir");
            System.out.print("Opción: ");
            opcion = sc.nextInt();

            switch (opcion) {
                case 1:
                    System.out.println("¡Hola, usuario!");
                    break;
                case 2:
                    System.out.println("Fecha: 2026-09-29");
                    break;
                case 0:
                    System.out.println("¡Hasta luego!");
                    break;
                default:
                    System.out.println("Opción no válida.");
            }
        } while (opcion != 0);

        sc.close();
    }
}
```

---

## 3. Control de Flujo: break y continue

```java
// break — termina el ciclo completamente
for (int i = 0; i < 10; i++) {
    if (i == 5) break;      // Sale del for cuando i = 5
    System.out.println(i);  // Imprime 0, 1, 2, 3, 4
}

// continue — salta al siguiente ciclo (omite el resto del cuerpo)
for (int i = 0; i < 10; i++) {
    if (i % 2 == 0) continue; // Salta los pares
    System.out.println(i);    // Imprime 1, 3, 5, 7, 9
}
```

---

## 4. Ciclos Anidados

Un ciclo dentro de otro. Común para trabajar con matrices o patrones.

**Ejemplo — Tabla de multiplicar completa (10×10):**
```java
public class TablaCompleta {
    public static void main(String[] args) {
        System.out.printf("%5s", "");
        for (int j = 1; j <= 10; j++) {
            System.out.printf("%5d", j);
        }
        System.out.println();

        for (int i = 1; i <= 10; i++) {
            System.out.printf("%5d", i);          // Encabezado de fila
            for (int j = 1; j <= 10; j++) {
                System.out.printf("%5d", i * j);  // Producto
            }
            System.out.println();
        }
    }
}
```

**Ejemplo — Patrón de triángulo con asteriscos:**
```java
public class Triangulo {
    public static void main(String[] args) {
        int filas = 5;

        for (int i = 1; i <= filas; i++) {
            for (int j = 1; j <= i; j++) {
                System.out.print("* ");
            }
            System.out.println();
        }
        /*
        Salida:
        *
        * *
        * * *
        * * * *
        * * * * *
        */
    }
}
```

---

## 5. Ejemplo Integrador — Estructuras Combinadas

```java
import java.util.Scanner;

/**
 * Programa que lee N notas de un estudiante, calcula el promedio,
 * clasifica el resultado y cuenta cuántas notas son mayores al promedio.
 */
public class AnalizadorNotas {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("¿Cuántas notas desea ingresar? ");
        int n = sc.nextInt();

        if (n <= 0) {
            System.out.println("Error: debe ingresar al menos 1 nota.");
            sc.close();
            return;
        }

        double[] notas = new double[n];
        double suma = 0;

        // Leer notas con validación
        for (int i = 0; i < n; i++) {
            do {
                System.out.printf("Nota %d (0.0 - 5.0): ", i + 1);
                notas[i] = sc.nextDouble();
                if (notas[i] < 0 || notas[i] > 5) {
                    System.out.println("  Nota inválida. Ingrese entre 0.0 y 5.0.");
                }
            } while (notas[i] < 0 || notas[i] > 5);
            suma += notas[i];
        }

        double promedio = suma / n;

        // Clasificar
        String clasificacion;
        if (promedio >= 4.5)      clasificacion = "Excelente";
        else if (promedio >= 3.5) clasificacion = "Bueno";
        else if (promedio >= 3.0) clasificacion = "Aprobado";
        else                      clasificacion = "Reprobado";

        // Contar notas mayores al promedio
        int mayorAlPromedio = 0;
        for (double nota : notas) {
            if (nota > promedio) mayorAlPromedio++;
        }

        System.out.printf("%n--- RESULTADOS ---%n");
        System.out.printf("Promedio: %.2f → %s%n", promedio, clasificacion);
        System.out.printf("Notas por encima del promedio: %d de %d%n",
                          mayorAlPromedio, n);

        sc.close();
    }
}
```

---

## 6. Errores Comunes

| Error | Descripción | Corrección |
|:---|:---|:---|
| Olvidar `break` en `switch` | "Fall-through": ejecuta todos los casos siguientes | Agregar `break;` al final de cada `case` |
| Punto y coma después del `for` o `while` | `for (int i=0; i<10; i++);` — cuerpo vacío | Eliminar el `;` suelto |
| Ciclo infinito | Condición nunca se vuelve false | Asegurarse de que el cuerpo modifique la variable de control |
| Confundir `=` con `==` en condición | `if (x = 5)` — asignación, no comparación | `if (x == 5)` |
| Off-by-one en bucle | `for (int i=1; i<=n; i++)` vs `i<n` | Definir claramente si el rango es cerrado o abierto |
| Variable no inicializada antes del ciclo | Usar `suma` sin inicializar en 0 | `int suma = 0;` antes del ciclo |

---

## 7. Cuándo Usar Cada Estructura

| Situación | Estructura recomendada |
|:---|:---|
| Condición simple verdadero/falso | `if-else` |
| Múltiples valores posibles de una variable | `switch-case` |
| Número de iteraciones conocido | `for` |
| Número de iteraciones desconocido | `while` |
| Se necesita al menos una ejecución (menús) | `do-while` |
| Ciclo que puede terminar antes bajo condición | `while` + `break` |

---

## 8. Métodos de Estudio

### Active Recall — Preguntas

1. ¿Cuál es la diferencia entre `while` y `do-while`? Da un caso de uso para cada uno.
2. ¿Qué pasa si olvidas el `break` en un `switch`?
3. Traza manualmente el siguiente código (escribe los valores de i y suma en cada iteración):
   ```java
   int suma = 0;
   for (int i = 1; i <= 5; i++) suma += i;
   ```
4. ¿Cuándo usarías `continue` en lugar de `break`?
5. Escribe de memoria el esqueleto de un menú con `do-while` y `switch`.

### Ejercicios de práctica

1. Calcular e imprimir los primeros 15 números de la serie de Fibonacci.
2. Leer números del usuario hasta que ingrese 0; mostrar la suma, el promedio y el mayor.
3. Imprimir todos los números primos entre 1 y 100.
4. Imprimir el patrón: columna de * que aumenta y luego decrece (pirámide centrada).

---

## 9. Recursos Externos

| Recurso | Descripción | URL |
|:---|:---|:---|
| **Píldoras Informáticas — Java** | Videos específicos de `if`, `switch`, `for`, `while` con ejercicios | https://www.youtube.com/@pildorasinformaticas |
| **CódigoFacilito** | Playlist de Java básico — estructuras de control explicadas visualmente | https://www.youtube.com/@codigofacilito |
| **W3Schools — Java** | Referencia de sintaxis de estructuras de control con ejemplos ejecutables | https://www.w3schools.com/java/java_conditions.asp |
| **Exercism — Java Track** | Ejercicios de práctica por nivel, con retroalimentación de mentores | https://exercism.org/tracks/java |

---

## 10. Referencia Rápida

```
CONDICIONALES
  if (cond) { }
  if (cond) { } else { }
  if (cond1) { } else if (cond2) { } else { }
  var = (cond) ? valorTrue : valorFalse;

  switch (var) {
      case val: ... break;
      default:  ...
  }

CICLOS
  while (cond) { }                   // 0 o más iteraciones
  do { } while (cond);               // 1 o más iteraciones
  for (init; cond; incr) { }         // N iteraciones conocidas
  for (Tipo item : coleccion) { }    // foreach (arreglos / colecciones)

CONTROL
  break;     // Termina el ciclo / case actual
  continue;  // Salta a la siguiente iteración

ANIDAMIENTO
  for (int i = ...) {
      for (int j = ...) {
          // Se ejecuta n×m veces
      }
  }

TRUCO — Divisibilidad
  n % 2 == 0  → par
  n % 3 == 0  → divisible por 3
  n % k == 0  → divisible por k
```
