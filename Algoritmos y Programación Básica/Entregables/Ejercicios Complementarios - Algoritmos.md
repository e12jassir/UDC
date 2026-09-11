# Ejercicios Complementarios — Algoritmos y Programación Básica

**Estudiante:** Esteban David Marrugo Jassir  
**Código:** 7502620036  
**Profesor:** Heybertt Moreno Díaz  
**Materia:** Algoritmos y Programación Básica  
**Universidad de Cartagena** — 2026-2  

---

### Ejercicio 1: Perímetro de un Polígono Regular de 6 Lados (Hexágono)
**Enunciado:** Calcular el perímetro de un polígono regular de 6 lados usando la fórmula: P = 6 * lado.

- **Datos de entrada:** Longitud del lado (lado).
- **Operación:** perimetro = 6 * lado.
- **Dato de salida:** El perímetro del polígono.

#### Pseudocódigo:
```text
Inicio
    Escribir "Ingrese la medida del lado del polígono:"
    Leer lado

    perimetro = 6 * lado

    Escribir "El perímetro del polígono de 6 lados es: ", perimetro
Fin
```

#### Código en Python:
```python
lado = float(input("Ingrese la longitud del lado del hexágono: "))

perimetro = 6 * lado

print("El perímetro del polígono regular es:", perimetro)
```

---

### Ejercicio 2: Nómina Semanal de 5 Obreros (Empresa XYZ)
**Enunciado:** Desarrollar el algoritmo que permita calcular la nómina semanal de 5 obreros con las siguientes condiciones:
- Valor de la hora: $1.000 pesos.
- Ingresar el número de horas trabajadas en la semana por cada obrero.
- Calcular el valor a pagar a cada obrero.
- Calcular el valor total pagado a todos los obreros.

- **Datos de entrada:** Horas trabajadas por el obrero 1, obrero 2, obrero 3, obrero 4 y obrero 5.
- **Operaciones:**
  - Pago por cada obrero = Horas del obrero * 1000
  - Total nómina = Pago 1 + Pago 2 + Pago 3 + Pago 4 + Pago 5
- **Datos de salida:** Pago individual de cada obrero y el total de la nómina.

#### Pseudocódigo:
```text
Inicio
    valor_hora = 1000

    Escribir "Ingrese las horas trabajadas por el Obrero 1:"
    Leer horas1
    Escribir "Ingrese las horas trabajadas por el Obrero 2:"
    Leer horas2
    Escribir "Ingrese las horas trabajadas por el Obrero 3:"
    Leer horas3
    Escribir "Ingrese las horas trabajadas por el Obrero 4:"
    Leer horas4
    Escribir "Ingrese las horas trabajadas por el Obrero 5:"
    Leer horas5

    pago1 = horas1 * valor_hora
    pago2 = horas2 * valor_hora
    pago3 = horas3 * valor_hora
    pago4 = horas4 * valor_hora
    pago5 = horas5 * valor_hora

    total_nomina = pago1 + pago2 + pago3 + pago4 + pago5

    Escribir "Pago al Obrero 1: $", pago1
    Escribir "Pago al Obrero 2: $", pago2
    Escribir "Pago al Obrero 3: $", pago3
    Escribir "Pago al Obrero 4: $", pago4
    Escribir "Pago al Obrero 5: $", pago5
    Escribir "Total pagado en nómina a todos los obreros: $", total_nomina
Fin
```

#### Código en Python:
```python
VALOR_HORA = 1000

horas_obreros = []
pagos_obreros = []

print("--- NÓMINA SEMANAL EMPRESA XYZ ---")
for i in range(1, 6):
    horas = float(input(f"Ingrese las horas trabajadas por el obrero {i}: "))
    pago = horas * VALOR_HORA
    horas_obreros.append(horas)
    pagos_obreros.append(pago)

total_nomina = sum(pagos_obreros)

print("\n--- RESUMEN DE PAGOS ---")
for i in range(5):
    print(f"Obrero {i+1} ({horas_obreros[i]} hrs): ${pagos_obreros[i]:,.2f}")

print(f"\nValor Total Pagado a Todos los Obreros: ${total_nomina:,.2f}")
```

---

### Ejercicio 3: Descomposición de un Número en 5 Dígitos y Cuadrados
**Enunciado:** Digitar un número entero positivo de 5 dígitos, separarlo en sus 5 dígitos individuales, y elevar al cuadrado el primer y el último dígito.

- **Dato de entrada:** Un número entero positivo de 5 dígitos (ejemplo: 54321).
- **Lógica de descomposición matemática:**
  - En base 10 podemos aislar cada cifra usando división entera (//) y residuo (%):
    - Dígito 1 (decenas de mil): numero // 10000
    - Dígito 2 (unidades de mil): (numero // 1000) % 10
    - Dígito 3 (centenas): (numero // 100) % 10
    - Dígito 4 (decenas): (numero // 10) % 10
    - Dígito 5 (unidades): numero % 10
  - Cuadrado del primero = Dígito 1 * Dígito 1
  - Cuadrado del último = Dígito 5 * Dígito 5
- **Datos de salida:** Cada uno de los 5 dígitos, el cuadrado del primero y el cuadrado del último.

#### Pseudocódigo:
```text
Inicio
    Escribir "Ingrese un número entero positivo de 5 dígitos:"
    Leer num

    d1 = num / 10000 (entero)
    d2 = (num / 1000) % 10
    d3 = (num / 100) % 10
    d4 = (num / 10) % 10
    d5 = num % 10

    cuadrado_primero = d1 * d1
    cuadrado_ultimo = d5 * d5

    Escribir "Dígitos separados: ", d1, ", ", d2, ", ", d3, ", ", d4, ", ", d5
    Escribir "El cuadrado del primer dígito (", d1, ") es: ", cuadrado_primero
    Escribir "El cuadrado del último dígito (", d5, ") es: ", cuadrado_ultimo
Fin
```

#### Código en Python:
```python
numero = int(input("Ingrese un número entero positivo de 5 dígitos: "))

# Descomponemos matemáticamente cada posición
d1 = numero // 10000
d2 = (numero // 1000) % 10
d3 = (numero // 100) % 10
d4 = (numero // 10) % 10
d5 = numero % 10

# Calculamos los cuadrados pedidos
cuadrado_primero = d1 ** 2
cuadrado_ultimo = d5 ** 2

print(f"\nDígitos separados: {d1} - {d2} - {d3} - {d4} - {d5}")
print(f"Cuadrado del primer dígito ({d1}^2): {cuadrado_primero}")
print(f"Cuadrado del último dígito ({d5}^2): {cuadrado_ultimo}")
```

---

### Ejercicio 4: Conversión de Décadas a Días
**Enunciado:** Realizar un algoritmo que convierta una cantidad de décadas (1 década = 10 años) a días (considerando 365 días por año).

- **Dato de entrada:** Cantidad de décadas.
- **Operaciones:**
  - Años = Décadas * 10
  - Días = Años * 365 (o directamente: Días = Décadas * 10 * 365)
- **Dato de salida:** Cantidad total de días.

#### Pseudocódigo:
```text
Inicio
    Escribir "Ingrese la cantidad de décadas:"
    Leer decadas

    anios = decadas * 10
    dias = anios * 365

    Escribir decadas, " décadas equivalen a: ", dias, " días."
Fin
```

#### Código en Python:
```python
decadas = float(input("Ingrese la cantidad de décadas: "))

anios = decadas * 10
dias = anios * 365

print(f"{decadas} décadas equivalen a {anios:.0f} años y aproximadamente {dias:,.0f} días.")
```

---

### Ejercicio 5: Cálculo de la Masa de Aire
**Enunciado:** La presión, el volumen y la temperatura de una masa de aire se relacionan por la fórmula:  
masa = (presión * volumen) / (0.37 * (temperatura + 460))

- **Datos de entrada:** Presión, volumen y temperatura.
- **Operación:**
  - masa = (presion * volumen) / (0.37 * (temperatura + 460))
- **Dato de salida:** Masa de aire calculada.

#### Pseudocódigo:
```text
Inicio
    Escribir "Ingrese la presión:"
    Leer presion
    Escribir "Ingrese el volumen:"
    Leer volumen
    Escribir "Ingrese la temperatura:"
    Leer temperatura

    masa = (presion * volumen) / (0.37 * (temperatura + 460))

    Escribir "La masa de aire es: ", masa
Fin
```

#### Código en Python:
```python
presion = float(input("Ingrese la presión del aire: "))
volumen = float(input("Ingrese el volumen: "))
temperatura = float(input("Ingrese la temperatura: "))

masa = (presion * volumen) / (0.37 * (temperatura + 460))

print(f"La masa de aire calculada es: {masa:.4f}")
```

---

### Ejercicio 6: Pulsaciones Cardíacas por Ejercicio
**Enunciado:** Calcular el número de pulsaciones que una persona debe tener por cada 10 segundos de ejercicio según la fórmula:  
num_pulsaciones = (220 - edad) / 10

- **Dato de entrada:** Edad de la persona (en años).
- **Operación:** num_pulsaciones = (220 - edad) / 10
- **Dato de salida:** Número de pulsaciones recomendadas cada 10 segundos.

#### Pseudocódigo:
```text
Inicio
    Escribir "Ingrese la edad de la persona en años:"
    Leer edad

    num_pulsaciones = (220 - edad) / 10

    Escribir "El número de pulsaciones por cada 10 segundos de ejercicio es: ", num_pulsaciones
Fin
```

#### Código en Python:
```python
edad = int(input("Ingrese su edad (en años): "))

num_pulsaciones = (220 - edad) / 10

print(f"Para una persona de {edad} años:")
print(f"Debe tener aproximadamente {num_pulsaciones:.1f} pulsaciones por cada 10 segundos de ejercicio.")
```
