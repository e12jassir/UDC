# UNIVERSIDAD DE CARTAGENA
## FACULTAD DE INGENIERÍA
### PROGRAMA DE INGENIERÍA DE SOFTWARE — MODALIDAD A DISTANCIA

**ACTIVIDAD DE APRENDIZAJE 1: INTRODUCCIÓN A LA PROGRAMACIÓN Y ALGORITMOS BÁSICOS**

- **Asignatura:** Algoritmos y Programación Básica (IX24013-B1)
- **Docente:** Heybertt Moreno Díaz
- **Estudiante:** Esteban David Marrugo Jassir
- **Código Estudiantil:** 7502620036
- **Centro Tutorial:** Cartagena (Sede Piedra de Bolívar)
- **Fecha:** Septiembre de 2026

---

### Ejercicio 1: Salario Neto de Empleado (Prosegur)
**Enunciado:** La empresa Prosegur tiene problema para calcular el salario neto a pagar a un empleado. Desarrollar una solución algorítmica que permita calcular e imprimir el salario total, salario neto y el 5% del salario total como retención en la fuente, ingresando por teclado el valor de la hora y el número de horas trabajadas.

- **Datos de entrada:** Valor por hora (valor_hora) y número de horas laboradas (horas_trabajadas).
- **Operaciones:**
  - Salario Total = Horas trabajadas * Valor de la hora
  - Retención (5%) = Salario Total * 0.05
  - Salario Neto = Salario Total - Retención
- **Datos de salida:** Salario total, retención aplicada y salario neto a pagar.

#### Pseudocódigo:
```text
Inicio
    Escribir "Ingrese el valor de la hora:"
    Leer valor_hora
    Escribir "Ingrese las horas trabajadas:"
    Leer horas_trabajadas

    salario_total = horas_trabajadas * valor_hora
    retencion = salario_total * 0.05
    salario_neto = salario_total - retencion

    Escribir "Salario total: $", salario_total
    Escribir "Retención en la fuente (5%): $", retencion
    Escribir "Salario neto a pagar: $", salario_neto
Fin
```

#### Código en Python:
```python
# Solicitud de datos de nómina al usuario
valor_hora = float(input("Ingrese el valor de la hora trabajada: "))
horas_trabajadas = float(input("Ingrese el número de horas trabajadas: "))

# Cálculos de nómina y deducción del 5%
salario_total = horas_trabajadas * valor_hora
retencion = salario_total * 0.05
salario_neto = salario_total - retencion

# Salida de resultados en pantalla
print("Salario total: $", salario_total)
print("Retención en la fuente (5%): $", retencion)
print("Salario neto a pagar: $", salario_neto)
```

#### Ejemplo de ejecución:
```text
> Ingrese el valor de la hora trabajada: 12000
> Ingrese el número de horas trabajadas: 40
Salario total: $ 480000.0
Retención en la fuente (5%): $ 24000.0
Salario neto a pagar: $ 456000.0
```

---

### Ejercicio 2: Valor de la Hora Trabajada
**Enunciado:** Un empleado gana en su salario total mensual $1.056.028, si trabajó un total de 36 horas, calcular una solución algorítmica que permita imprimir cuál es el valor de una hora trabajada.

- **Datos conocidos:** Salario mensual = $1.056.028 y Horas laboradas = 36.
- **Operación:** Valor por hora = Salario mensual / Horas laboradas.
- **Dato de salida:** Valor monetario de una hora trabajada.

#### Pseudocódigo:
```text
Inicio
    salario_mensual = 1056028
    horas = 36

    valor_hora = salario_mensual / horas

    Escribir "El valor de cada hora trabajada es: $", valor_hora
Fin
```

#### Código en Python:
```python
# Datos base establecidos en el enunciado
salario_mensual = 1056028
horas = 36

# Despejamos el valor unitario por hora
valor_hora = salario_mensual / horas

print("Por un salario de $1.056.028 trabajando 36 horas:")
print("El valor de una hora de trabajo es: $", round(valor_hora, 2))
```

#### Ejemplo de ejecución:
```text
Por un salario de $1.056.028 trabajando 36 horas:
El valor de una hora de trabajo es: $ 29334.11
```

---

### Ejercicio 3: Nota Mínima Requerida en el Tercer Corte (60%) de la UdeC
**Enunciado:** Un estudiante de Ingeniería de Sistemas de la UdeC tiene tres cortes de notas en una asignatura con valor de 0.0 a 5.0, el primer y segundo corte vale un 20% y el tercer corte vale 60%. Desarrollar una solución algorítmica que permita saber qué nota se debe sacar como mínimo en el 60% si conozco los primeros 20%. Tener en cuenta que para superar una asignatura debe ser igual o mayor a 3.0.

- **Datos de entrada:** Calificación del Corte 1 (corte1) y Calificación del Corte 2 (corte2).
- **Lógica del cálculo:**
  - Nota Final = (Corte 1 * 0.20) + (Corte 2 * 0.20) + (Corte 3 * 0.60)
  - Acumulado previo = (Corte 1 * 0.20) + (Corte 2 * 0.20)
  - Puntos que faltan para alcanzar 3.0 = 3.0 - Acumulado previo
  - Como el último corte pesa el 60%, dividimos entre 0.60:
    Nota mínima necesaria = (3.0 - Acumulado previo) / 0.60
- **Dato de salida:** Nota mínima requerida en la evaluación final.

#### Pseudocódigo:
```text
Inicio
    Escribir "Ingrese la nota del primer corte (20%):"
    Leer corte1
    Escribir "Ingrese la nota del segundo corte (20%):"
    Leer corte2

    acumulado = (corte1 * 0.20) + (corte2 * 0.20)
    puntos_que_faltan = 3.0 - acumulado
    nota_minima_corte3 = puntos_que_faltan / 0.60

    Escribir "Acumulado actual obtenido: ", acumulado
    Escribir "Nota mínima requerida en el 60%: ", nota_minima_corte3
Fin
```

#### Código en Python:
```python
# Lectura de notas previas (ambas del 20%)
corte1 = float(input("Ingrese la nota del primer corte (20%): "))
corte2 = float(input("Ingrese la nota del segundo corte (20%): "))

# Sumamos el 40% ya evaluado
acumulado = (corte1 * 0.20) + (corte2 * 0.20)

# Calculamos el esfuerzo restante para el 60% final
puntos_faltantes = 3.0 - acumulado
nota_requerida = puntos_faltantes / 0.60

print(f"Llevas acumulado en la materia: {acumulado:.2f}")
print(f"Para pasar la materia en 3.0 necesitas sacar: {nota_requerida:.2f}")
```

#### Ejemplo de ejecución:
```text
> Ingrese la nota del primer corte (20%): 3.5
> Ingrese la nota del segundo corte (20%): 4.0
Llevas acumulado en la materia: 1.50
Para pasar la materia en 3.0 necesitas sacar: 2.50
```

---

### Ejercicio 4: Área de un Triángulo
**Enunciado:** Calcular el área de un triángulo, sabiendo la base y la altura.

- **Datos de entrada:** Longitud de la base y de la altura (valores positivos).
- **Operación:** Área = (Base * Altura) / 2.
- **Dato de salida:** Área del triángulo.

#### Pseudocódigo:
```text
Inicio
    Escribir "Ingrese la base:"
    Leer base
    Escribir "Ingrese la altura:"
    Leer altura

    area = (base * altura) / 2

    Escribir "El área del triángulo es: ", area
Fin
```

#### Código en Python:
```python
base = float(input("Ingrese la base del triángulo: "))
altura = float(input("Ingrese la altura del triángulo: "))

# Fórmula geométrica estándar
area = (base * altura) / 2

print("El área del triángulo es:", area)
```

#### Ejemplo de ejecución:
```text
> Ingrese la base del triángulo: 12
> Ingrese la altura del triángulo: 8
El área del triángulo es: 48.0
```

---

### Ejercicio 5: Perímetro de un Triángulo
**Enunciado:** Calcular el perímetro de un triángulo sabiendo los tres lados.

- **Datos de entrada:** Medida del lado1, lado2 y lado3.
- **Operación:** Perímetro = Lado 1 + Lado 2 + Lado 3.
- **Dato de salida:** Perímetro total.

#### Pseudocódigo:
```text
Inicio
    Escribir "Ingrese los 3 lados del triángulo:"
    Leer lado1, lado2, lado3

    perimetro = lado1 + lado2 + lado3

    Escribir "El perímetro es: ", perimetro
Fin
```

#### Código en Python:
```python
lado1 = float(input("Ingrese el primer lado: "))
lado2 = float(input("Ingrese el segundo lado: "))
lado3 = float(input("Ingrese el tercer lado: "))

# Suma de las longitudes de los 3 lados
perimetro = lado1 + lado2 + lado3

print("El perímetro del triángulo es:", perimetro)
```

#### Ejemplo de ejecución:
```text
> Ingrese el primer lado: 5
> Ingrese el segundo lado: 7
> Ingrese el tercer lado: 10
El perímetro del triángulo es: 22.0
```

---

### Ejercicio 6: Conversión de Grados Celsius a Fahrenheit
**Enunciado:** Convertir en grados Fahrenheit el valor ingresado por teclado en grados Celsius.

- **Datos de entrada:** Temperatura en grados Celsius (celsius).
- **Operación:** Fahrenheit = (Celsius * 9 / 5) + 32.
- **Dato de salida:** Temperatura en grados Fahrenheit.

#### Pseudocódigo:
```text
Inicio
    Escribir "Ingrese los grados Celsius:"
    Leer celsius

    fahrenheit = (celsius * 9 / 5) + 32

    Escribir "Equivalente en Fahrenheit: ", fahrenheit
Fin
```

#### Código en Python:
```python
celsius = float(input("Ingrese la temperatura en grados Celsius: "))

# Factor de escala 9/5 y desplazamiento de 32 grados
fahrenheit = (celsius * 9 / 5) + 32

print("La temperatura en Fahrenheit es:", fahrenheit)
```

#### Ejemplo de ejecución:
```text
> Ingrese la temperatura en grados Celsius: 25
La temperatura en Fahrenheit es: 77.0
```

---

### Ejercicio 7: Conversión de Grados Fahrenheit a Celsius
**Enunciado:** Convertir en grados Celsius el valor ingresado por teclado en grados Fahrenheit.

- **Datos de entrada:** Temperatura en grados Fahrenheit (fahrenheit).
- **Operación:** Celsius = (Fahrenheit - 32) * 5 / 9.
- **Dato de salida:** Temperatura en grados Celsius.

#### Pseudocódigo:
```text
Inicio
    Escribir "Ingrese los grados Fahrenheit:"
    Leer fahrenheit

    celsius = (fahrenheit - 32) * 5 / 9

    Escribir "Equivalente en Celsius: ", celsius
Fin
```

#### Código en Python:
```python
fahrenheit = float(input("Ingrese la temperatura en grados Fahrenheit: "))

# Despeje inverso restando 32 y multiplicando por 5/9
celsius = (fahrenheit - 32) * 5 / 9

print("La temperatura en Celsius es:", round(celsius, 2))
```

#### Ejemplo de ejecución:
```text
> Ingrese la temperatura en grados Fahrenheit: 77
La temperatura en Celsius es: 25.0
```

---

### Ejercicio 8: Conversión de Millas Marinas a Metros
**Enunciado:** Un programa que lea el valor correspondiente a una distancia en millas marinas y las escriba expresadas en metros. Sabiendo que 1 milla marina equivale a 1852 metros.

- **Dato de entrada:** Distancia en millas marinas (millas).
- **Constante:** 1 milla marina = 1852 metros.
- **Operación:** Metros = Millas * 1852.
- **Dato de salida:** Distancia en metros.

#### Pseudocódigo:
```text
Inicio
    Escribir "Ingrese la distancia en millas marinas:"
    Leer millas

    metros = millas * 1852

    Escribir "Distancia en metros: ", metros
Fin
```

#### Código en Python:
```python
millas = float(input("Ingrese la distancia en millas marinas: "))

# Conversión lineal por factor constante
metros = millas * 1852

print("Equivale a:", metros, "metros")
```

#### Ejemplo de ejecución:
```text
> Ingrese la distancia en millas marinas: 5
Equivale a: 9260.0 metros
```

---

### Ejercicio 9: Porcentaje de Descuento en una Compra
**Enunciado:** Un programa que escribe el porcentaje descontado en una compra, introduciendo por teclado el precio de la tarifa y el precio pagado.

- **Datos de entrada:** Precio de lista o tarifa (precio_tarifa) y precio abonado (precio_pagado).
- **Operaciones:**
  - Monto descontado = Precio tarifa - Precio pagado
  - Porcentaje de descuento = (Monto descontado / Precio tarifa) * 100
- **Dato de salida:** Porcentaje de descuento comercial aplicado.

#### Pseudocódigo:
```text
Inicio
    Escribir "Ingrese el precio de tarifa (original):"
    Leer precio_tarifa
    Escribir "Ingrese el precio pagado:"
    Leer precio_pagado

    descuento = precio_tarifa - precio_pagado
    porcentaje = (descuento / precio_tarifa) * 100

    Escribir "El porcentaje de descuento fue de: ", porcentaje, "%"
Fin
```

#### Código en Python:
```python
precio_tarifa = float(input("Ingrese el precio original de tarifa: "))
precio_pagado = float(input("Ingrese el precio pagado: "))

# Cálculo de la diferencia y su proporción porcentual
descuento = precio_tarifa - precio_pagado
porcentaje_descuento = (descuento / precio_tarifa) * 100

print(f"El porcentaje de descuento aplicado fue del: {porcentaje_descuento:.1f}%")
```

#### Ejemplo de ejecución:
```text
> Ingrese el precio original de tarifa: 150000
> Ingrese el precio pagado: 120000
El porcentaje de descuento aplicado fue del: 20.0%
```

---

### Ejercicio 10: Cálculo del IVA de un Artículo
**Enunciado:** Un programa que reciba por teclado el precio de un artículo y calcule cuál es el valor pagado por el IVA de ese artículo (aplicando la tasa colombiana estándar del 19%).

- **Dato de entrada:** Precio base del artículo (precio).
- **Operaciones:**
  - Valor IVA = Precio * 0.19
  - Precio Total = Precio + Valor IVA
- **Datos de salida:** Valor del IVA y precio final con IVA incluido.

#### Pseudocódigo:
```text
Inicio
    Escribir "Ingrese el precio del artículo:"
    Leer precio

    iva = precio * 0.19
    precio_final = precio + iva

    Escribir "Valor del IVA (19%): $", iva
    Escribir "Total a pagar: $", precio_final
Fin
```

#### Código en Python:
```python
precio = float(input("Ingrese el precio del artículo: "))

# Tarifa de impuesto al valor agregado (19%)
iva = precio * 0.19
total = precio + iva

print("Valor del IVA (19%): $", round(iva, 2))
print("Precio total con IVA: $", round(total, 2))
```

#### Ejemplo de ejecución:
```text
> Ingrese el precio del artículo: 80000
Valor del IVA (19%): $ 15200.0
Precio total con IVA: $ 95200.0
```

---

### Ejercicio 11: Operaciones Aritméticas Básicas entre Dos Enteros
**Enunciado:** Un programa que pida por teclado dos números enteros y muestre su suma, resta, multiplicación, división y el resto (módulo) de la división.

- **Datos de entrada:** Número entero A (num1) y Número entero B (num2).
- **Operaciones:** Suma (+), Resta (-), Multiplicación (*), División (/) y Módulo (%).
- **Datos de salida:** Resultados individuales de cada operación matemática.

#### Pseudocódigo:
```text
Inicio
    Escribir "Ingrese el primer número entero:"
    Leer num1
    Escribir "Ingrese el segundo número entero:"
    Leer num2

    Escribir "Suma: ", num1 + num2
    Escribir "Resta: ", num1 - num2
    Escribir "Multiplicación: ", num1 * num2
    Si num2 <> 0 Entonces
        Escribir "División: ", num1 / num2
        Escribir "Módulo (Resto): ", num1 % num2
    Sino
        Escribir "No se puede dividir entre cero."
    FinSi
Fin
```

#### Código en Python:
```python
num1 = int(input("Ingrese el primer número entero: "))
num2 = int(input("Ingrese el segundo número entero: "))

# Operaciones directas
print("Suma:", num1 + num2)
print("Resta:", num1 - num2)
print("Multiplicación:", num1 * num2)

# Verificación de división por cero
if num2 != 0:
    print("División:", num1 / num2)
    print("Módulo (Resto):", num1 % num2)
else:
    print("No se puede dividir entre cero.")
```

#### Ejemplo de ejecución:
```text
> Ingrese el primer número entero: 15
> Ingrese el segundo número entero: 4
Suma: 19
Resta: 11
Multiplicación: 60
División: 3.75
Módulo (Resto): 3
```

---

### Ejercicio 12: Última Cifra de un Número Entero
**Enunciado:** Un programa que obtiene la última cifra de un número introducido.

- **Dato de entrada:** Un número entero cualquiera (numero).
- **Principio matemático:** En base 10, la operación de residuo entre 10 (% 10) aísla exactamente el dígito de las unidades.
- **Dato de salida:** La última cifra.

#### Pseudocódigo:
```text
Inicio
    Escribir "Ingrese un número entero:"
    Leer numero

    ultima_cifra = abs(numero) % 10

    Escribir "La última cifra es: ", ultima_cifra
Fin
```

#### Código en Python:
```python
numero = int(input("Ingrese un número entero: "))

# El residuo de dividir entre 10 siempre da la última cifra
# Usamos abs() para asegurar que números negativos den cifra positiva
ultima_cifra = abs(numero) % 10

print("La última cifra del número es:", ultima_cifra)
```

#### Ejemplo de ejecución:
```text
> Ingrese un número entero: 4789
La última cifra del número es: 9
```

---

### Ejercicio 13: Conversión de Centímetros a Pulgadas
**Enunciado:** Un programa que tras introducir una medida expresada en centímetros la convierta en pulgadas (1 pulgada = 2,54 centímetros).

- **Dato de entrada:** Medida en centímetros (cm).
- **Operación:** Pulgadas = Centímetros / 2.54.
- **Dato de salida:** Medida equivalente en pulgadas.

#### Pseudocódigo:
```text
Inicio
    Escribir "Ingrese la medida en centímetros:"
    Leer cm

    pulgadas = cm / 2.54

    Escribir "Equivale a: ", pulgadas, " pulgadas"
Fin
```

#### Código en Python:
```python
cm = float(input("Ingrese la medida en centímetros: "))

# 1 pulgada equivale exactamente a 2.54 centímetros
pulgadas = cm / 2.54

print("La medida en pulgadas es:", round(pulgadas, 2))
```

#### Ejemplo de ejecución:
```text
> Ingrese la medida en centímetros: 50.8
La medida en pulgadas es: 20.0
```

---

### Ejercicio 14: Descomposición de Segundos a Horas, Minutos y Segundos
**Enunciado:** Un programa que exprese en horas, minutos y segundos un tiempo expresado en segundos.

- **Dato de entrada:** Total de segundos (total_segundos).
- **Lógica paso a paso:**
  - 1 hora tiene 3600 segundos -> Horas = Segundos // 3600
  - Tomamos los segundos sobrantes -> Resto = Segundos % 3600
  - Con ese sobrante calculamos los minutos -> Minutos = Resto // 60
  - Los segundos finales son el último residuo -> Segundos finales = Resto % 60
- **Datos de salida:** Horas, minutos y segundos resultantes.

#### Pseudocódigo:
```text
Inicio
    Escribir "Ingrese la cantidad de segundos:"
    Leer total_segundos

    horas = total_segundos / 3600 (entero)
    resto = total_segundos % 3600
    minutos = resto / 60 (entero)
    segundos = resto % 60

    Escribir horas, " horas, ", minutos, " minutos y ", segundos, " segundos."
Fin
```

#### Código en Python:
```python
total_segundos = int(input("Ingrese el tiempo en segundos: "))

# // realiza división entera y % extrae el residuo sobrante
horas = total_segundos // 3600
resto = total_segundos % 3600
minutos = resto // 60
segundos = resto % 60

print(f"{total_segundos} segundos equivalen a: {horas} horas, {minutos} minutos y {segundos} segundos.")
```

#### Ejemplo de ejecución:
```text
> Ingrese el tiempo en segundos: 7385
7385 segundos equivalen a: 2 horas, 3 minutos y 5 segundos.
```

---

### Ejercicio 15: Valor Total de una Venta
**Enunciado:** Se desea saber cuál es el valor total para pagar de un artículo, sabiendo su valor por unidad y la cantidad de artículos a llevar. Desarrollar un programa que, dado el valor de unidad de un artículo y la cantidad de artículos, calcule el valor total y lo imprima.

- **Datos de entrada:** Precio unitario (precio_unidad) y cantidad adquirida (cantidad).
- **Operación:** Total a pagar = Precio unitario * Cantidad.
- **Dato de salida:** Total monetario a pagar.

#### Pseudocódigo:
```text
Inicio
    Escribir "Ingrese el valor por unidad del artículo:"
    Leer precio_unidad
    Escribir "Ingrese la cantidad de artículos:"
    Leer cantidad

    total = precio_unidad * cantidad

    Escribir "El total a pagar es: $", total
Fin
```

#### Código en Python:
```python
precio_unidad = float(input("Ingrese el precio por unidad del artículo: "))
cantidad = int(input("Ingrese la cantidad de artículos: "))

# Producto simple de costo por volumen
total = precio_unidad * cantidad

print("El valor total a pagar es: $", total)
```

#### Ejemplo de ejecución:
```text
> Ingrese el precio por unidad del artículo: 4500
> Ingrese la cantidad de artículos: 6
El valor total a pagar es: $ 27000.0
```

---

### Ejercicio 16: Área de un Círculo dado su Radio
**Enunciado:** Desarrollar un algoritmo que dado el radio de un círculo calcule e imprima el área.

- **Dato de entrada:** Radio del círculo (radio).
- **Fórmula:** Área = π * (Radio ^ 2).
- **Dato de salida:** Área de la superficie circular.

#### Pseudocódigo:
```text
Inicio
    Escribir "Ingrese el radio del círculo:"
    Leer radio

    area = 3.1416 * (radio * radio)

    Escribir "El área del círculo es: ", area
Fin
```

#### Código en Python:
```python
import math

radio = float(input("Ingrese el radio del círculo: "))

# Usamos la constante math.pi para máxima precisión
area = math.pi * (radio ** 2)

print("El área del círculo es:", round(area, 2))
```

#### Ejemplo de ejecución:
```text
> Ingrese el radio del círculo: 7
El área del círculo es: 153.94
```

---

### Ejercicio 17: Perímetro y Área de un Rectángulo
**Enunciado:** Desarrollar un algoritmo que calcule e imprima el perímetro y el área de un rectángulo dada la longitud de dos de sus lados:  
P = 2 · a + 2 · b  
A = a · b

- **Datos de entrada:** Medida del lado A (lado_a) y lado B (lado_b).
- **Operaciones:**
  - Perímetro = 2 * Lado A + 2 * Lado B
  - Área = Lado A * Lado B
- **Datos de salida:** Perímetro y área del rectángulo.

#### Pseudocódigo:
```text
Inicio
    Escribir "Ingrese la longitud del lado A:"
    Leer lado_a
    Escribir "Ingrese la longitud del lado B:"
    Leer lado_b

    perimetro = (2 * lado_a) + (2 * lado_b)
    area = lado_a * lado_b

    Escribir "Perímetro: ", perimetro
    Escribir "Área: ", area
Fin
```

#### Código en Python:
```python
lado_a = float(input("Ingrese la longitud del lado A: "))
lado_b = float(input("Ingrese la longitud del lado B: "))

perimetro = (2 * lado_a) + (2 * lado_b)
area = lado_a * lado_b

print("El perímetro del rectángulo es:", perimetro)
print("El área del rectángulo es:", area)
```

#### Ejemplo de ejecución:
```text
> Ingrese la longitud del lado A: 8
> Ingrese la longitud del lado B: 5
El perímetro del rectángulo es: 26.0
El área del rectángulo es: 40.0
```

---

### Ejercicio 18: Perímetro y Área de un Cuadrado
**Enunciado:** Desarrollar un algoritmo que calcule e imprima el perímetro y el área de un cuadrado dado uno de sus lados:  
P = 4 · a  
A = a²

- **Dato de entrada:** Longitud del lado (lado).
- **Operaciones:**
  - Perímetro = 4 * Lado
  - Área = Lado * Lado
- **Datos de salida:** Perímetro y área del cuadrado.

#### Pseudocódigo:
```text
Inicio
    Escribir "Ingrese el lado del cuadrado:"
    Leer lado

    perimetro = 4 * lado
    area = lado * lado

    Escribir "Perímetro: ", perimetro
    Escribir "Área: ", area
Fin
```

#### Código en Python:
```python
lado = float(input("Ingrese el valor del lado del cuadrado: "))

perimetro = 4 * lado
area = lado ** 2

print("El perímetro del cuadrado es:", perimetro)
print("El área del cuadrado es:", area)
```

#### Ejemplo de ejecución:
```text
> Ingrese el valor del lado del cuadrado: 6
El perímetro del cuadrado es: 24.0
El área del cuadrado es: 36.0
```

---

### Ejercicio 19: Evaluación de la Expresión Algebraica A = 2x²y³z
**Enunciado:** Desarrollar un algoritmo que, dado el valor de x, y, z calcule e imprima el valor de A según la siguiente fórmula:  
A = 2 · x² · y³ · z

- **Datos de entrada:** Valores numéricos de x, y y z.
- **Operaciones:**
  - Se calculan las potencias: x al cuadrado (x**2) y y al cubo (y**3)
  - Se multiplican todos los términos: A = 2 * (x**2) * (y**3) * z
- **Dato de salida:** Valor final de A.

#### Pseudocódigo:
```text
Inicio
    Escribir "Ingrese el valor de x:"
    Leer x
    Escribir "Ingrese el valor de y:"
    Leer y
    Escribir "Ingrese el valor de z:"
    Leer z

    a = 2 * (x ^ 2) * (y ^ 3) * z

    Escribir "El resultado de A es: ", a
Fin
```

#### Código en Python:
```python
x = float(input("Ingrese el valor de x: "))
y = float(input("Ingrese el valor de y: "))
z = float(input("Ingrese el valor de z: "))

# Potencias evaluadas antes del producto
a = 2 * (x ** 2) * (y ** 3) * z

print("El valor resultante de A es:", a)
```

#### Ejemplo de ejecución:
```text
> Ingrese el valor de x: 3
> Ingrese el valor de y: 2
> Ingrese el valor de z: 4
El valor resultante de A es: 576.0
```
