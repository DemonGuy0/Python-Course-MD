# 🐍 Curso de Python de la A a la Z

> Curso completo para estudiar **sin conexión**. Va desde "nunca he programado" hasta crear tus propios proyectos.

---

## 📖 Cómo usar este curso

1. **Lee un módulo a la vez.** No avances hasta que hayas hecho los ejercicios.
2. **Escribe el código tú mismo.** No copies y pegues: tus dedos también aprenden.
3. **Cambia los ejemplos.** Cada vez que veas un ejemplo, cambia un número, una palabra... y mira qué pasa. Romper cosas es la mejor forma de aprender.
4. **Haz los ejercicios ANTES de mirar las soluciones.** Si te trabas 10 minutos, mira la pista; si sigues trabado, mira la solución, entiéndela, cierra el archivo y vuelve a escribirla de memoria.
5. **Los errores son normales.** Todos los programadores ven errores todo el día. Un error no es un fracaso: es una pista.
6. **Repite.** Aquí cada concepto se explica varias veces y de varias maneras a propósito. Si algo no queda claro con la primera explicación, la segunda o la tercera probablemente sí.

**Símbolos que verás:**

- 💡 **Idea clave**: lo más importante a recordar.
- ⚠️ **Cuidado**: error muy común.
- 🧪 **Pruébalo**: algo para que lo experimentes tú.
- 🎯 **Ejercicios**: práctica al final de cada módulo (todos son fáciles).

**Cómo están hechos los ejercicios:** son cortos y fáciles, pero están pensados para que practiques justo lo que acabas de aprender. Al final de cada módulo están las **soluciones**.

---

## 📚 Índice

| # | Módulo | Qué aprenderás |
|---|--------|----------------|
| 0 | Antes de empezar | Qué es Python, instalación, cómo ejecutar código, cómo pensar un problema |
| 1 | Tu primer programa | `print`, comentarios, errores básicos |
| 2 | Variables y tipos de datos | Guardar información, `int`, `float`, `str`, `bool` |
| 3 | Operadores | Matemáticas, comparaciones, lógica |
| 4 | Cadenas de texto (strings) | Texto, índices, cortes, métodos, f-strings |
| 5 | Entrada de datos | `input()`, conversiones, programas interactivos |
| 6 | Condicionales | `if`, `elif`, `else`, `match` |
| 7 | Bucle `while` | Repetir mientras algo sea cierto |
| 8 | Bucle `for` y `range` | Repetir un número de veces o recorrer cosas |
| 9 | Listas | Guardar muchos datos en orden |
| 10 | Tuplas, conjuntos y desempaquetado | Otras colecciones |
| 11 | Diccionarios | Datos con nombre (clave → valor) |
| 12 | Funciones | Reutilizar código |
| 13 | Alcance y recursión | Variables locales/globales y funciones que se llaman a sí mismas |
| 14 | Comprensiones y funciones de orden superior | `lambda`, `map`, `filter`, `sorted` |
| 15 | Archivos | Leer y escribir archivos |
| 16 | Errores y excepciones | `try`, `except`, `raise` |
| 17 | Módulos y librería estándar | `math`, `random`, `datetime`, `collections`... |
| 18 | Programación orientada a objetos (I) | Clases y objetos |
| 19 | Programación orientada a objetos (II) | Herencia, métodos especiales, `@property`, `dataclass` |
| 20 | Funciones avanzadas | `*args`, `**kwargs`, generadores, decoradores |
| 21 | JSON, CSV, `pip` y entornos virtuales | Datos reales y librerías externas |
| 22 | Depuración, pruebas y buenas prácticas | Código limpio y confiable |
| 23 | Proyectos finales | Cinco programas completos |
| A | Apéndices | Chuleta rápida, errores comunes, siguientes pasos |

---

# MÓDULO 0 — Antes de empezar

## 0.1 ¿Qué es programar?

Programar es **darle instrucciones a la computadora** para que haga algo por ti. La computadora es muy rápida pero muy "literal": hace exactamente lo que le dices, ni más ni menos.

Piensa en una receta de cocina:

1. Pon agua en una olla.
2. Enciende el fuego.
3. Cuando hierva, agrega la pasta.
4. Espera 10 minutos.

Un programa es igual: una lista de pasos, en orden, escritos en un idioma que la computadora entiende. Ese idioma, en nuestro caso, se llama **Python**.

## 0.2 ¿Por qué Python?

- Se lee casi como inglés: es de los lenguajes más fáciles de aprender.
- Sirve para **muchísimo**: páginas web, automatizar tareas, análisis de datos, inteligencia artificial, juegos, bots, aplicaciones...
- Tiene una comunidad enorme: casi cualquier duda ya tiene respuesta.

## 0.3 Instalar Python

**Windows**

1. Entra a `python.org` → Downloads → descarga la última versión.
2. Al abrir el instalador, **marca la casilla "Add Python to PATH"** (muy importante) y pulsa *Install Now*.

**macOS**

- Descarga el instalador desde `python.org`, o usa Homebrew: `brew install python`.

**Linux** (Ubuntu/Debian)

- Casi siempre ya viene instalado. Si no: `sudo apt install python3 python3-pip`.

**Android (para practicar desde el celular)**

- Puedes usar apps como Pydroid 3 o Termux (`pkg install python`).

**Comprobar que funciona.** Abre una terminal (en Windows: "Símbolo del sistema" o PowerShell) y escribe:

```bash
python --version
```

En algunos sistemas (Linux/macOS) se usa `python3`:

```bash
python3 --version
```

Deberías ver algo como `Python 3.12.4`. Si lo ves, ¡listo!

> 💡 En este curso, cuando veas `python archivo.py`, en tu sistema puede que tengas que escribir `python3 archivo.py`.

## 0.4 Tres formas de ejecutar Python

### Forma 1: el intérprete interactivo (REPL)

Escribe `python` (o `python3`) en la terminal. Verás algo como:

```text
>>> 
```

Ese `>>>` significa "te escucho". Escribe una instrucción y pulsa Enter:

```python
>>> 2 + 3
5
>>> print("Hola")
Hola
```

Para salir escribe `exit()`.

**Úsalo para:** probar cosas rápidas y hacer experimentos.

### Forma 2: un archivo `.py`

1. Crea un archivo llamado `hola.py` con este contenido:

```python
print("¡Hola desde un archivo!")
```

2. En la terminal, en la carpeta donde está el archivo:

```bash
python hola.py
```

**Úsalo para:** todos tus programas "de verdad".

### Forma 3: un editor/IDE

Programas como **VS Code**, **PyCharm** o **IDLE** (viene con Python) te permiten escribir el código y ejecutarlo con un botón. VS Code es gratis y muy popular.

> 💡 **Recomendación:** usa VS Code (con la extensión de Python) o IDLE para empezar. Cualquiera sirve.

## 0.5 Cómo pensar un problema (el método de 5 pasos)

Esta es la parte más importante del curso. Programar no es memorizar comandos: es **resolver problemas**. Todo problema, fácil o difícil, se ataca igual:

1. **Entender.** ¿Qué me piden exactamente? ¿Qué datos tengo? ¿Qué debo devolver? Dilo con tus propias palabras.
2. **Ejemplos.** Inventa 2 o 3 casos pequeños y resuélvelos *a mano*. "Si me dan 3 y 4, la respuesta debe ser 7."
3. **Dividir.** Rompe el problema en pasos pequeños. Escríbelos en español (esto se llama **pseudocódigo**).
4. **Programar.** Traduce cada paso a Python, un paso a la vez, probando cada uno.
5. **Probar.** Ejecuta tu programa con tus ejemplos del paso 2. ¿Da lo que esperabas? Si no, busca el paso que falla.

**Ejemplo completo de cómo pensar:**

> *Problema:* "Calcula el área de un rectángulo."

1. **Entender:** me dan base y altura; debo mostrar el área.
2. **Ejemplos:** base 3, altura 4 → área 12. Base 5, altura 2 → 10.
3. **Dividir (pseudocódigo):**
   - Guardar la base.
   - Guardar la altura.
   - Multiplicar base por altura.
   - Mostrar el resultado.
4. **Programar:**

```python
base = 3
altura = 4
area = base * altura
print(area)
```

5. **Probar:** sale `12`. ✔️ Cambio los valores a 5 y 2 → sale `10`. ✔️

> 💡 **Regla de oro:** si no sabes cómo empezar, no empieces por el código. Empieza por el papel.

### Otro ejemplo de razonamiento

> *Problema:* "Dime si un número es par."

- Ejemplos: 4 → sí. 7 → no. 0 → sí.
- Idea: un número es par si al dividirlo entre 2 **no sobra nada**.
- Pseudocódigo: tomar el número → calcular el resto de dividir entre 2 → si el resto es 0, es par; si no, impar.

(Aún no sabemos escribir esto en Python. Lo haremos en el Módulo 6. Lo importante es ver cómo se piensa.)

## 0.6 Cómo leer un error

Cuando algo sale mal, Python te muestra un mensaje. **Léelo de abajo hacia arriba**: la última línea dice qué pasó.

```python
print(Hola)
```

```text
Traceback (most recent call last):
  File "prueba.py", line 1, in <module>
    print(Hola)
NameError: name 'Hola' is not defined
```

- `File "prueba.py", line 1` → el problema está en la **línea 1**.
- `NameError: name 'Hola' is not defined` → "no conozco ninguna cosa llamada Hola". (Faltaban las comillas.)

> 💡 No temas a los errores. Léelos con calma: casi siempre te dicen **qué** falló y **dónde**.

## 0.7 🎯 Ejercicios del Módulo 0

*(Son de pensar y comprobar, no hay código complicado.)*

**Ejercicio 0.1** — Abre la terminal y comprueba la versión de Python instalada. Anota cuál es.

**Ejercicio 0.2** — Abre el REPL (`python`) y calcula `10 + 5`, `10 - 5`, `10 * 5`. Anota los resultados.

**Ejercicio 0.3** — Crea un archivo `prueba.py` con una sola línea: `print("Estoy aprendiendo Python")`. Ejecútalo.

**Ejercicio 0.4** — Escribe en el REPL `print(Hola)` (sin comillas). Lee el error. ¿Qué tipo de error es? ¿Qué línea señala?

**Ejercicio 0.5** — Aplica el método de 5 pasos (solo en papel o en un archivo de texto) al problema: *"Dados el precio de un producto y la cantidad que compro, calcula el total a pagar."* Escribe: qué entiendo, 2 ejemplos, pseudocódigo.

**Ejercicio 0.6** — Aplica el método de 5 pasos al problema: *"Convertir una temperatura de Celsius a Fahrenheit."* (Pista: F = C × 9/5 + 32). Haz los ejemplos a mano: 0 °C y 100 °C.

**Ejercicio 0.7** — Escribe en pseudocódigo (en español) los pasos para *"preparar un vaso de agua con azúcar"*. Sé muy detallado, como si se lo explicaras a un robot.

### ✅ Soluciones del Módulo 0

**0.1** Resultado según tu instalación, por ejemplo `Python 3.12.4`.

**0.2** `15`, `5` y `50`.

**0.3** Debe aparecer: `Estoy aprendiendo Python`.

**0.4** Es un `NameError` (nombre no definido). Señala la línea 1 en el REPL (`<stdin>`, line 1).

**0.5**
- Entiendo: tengo precio y cantidad; el total es precio × cantidad.
- Ejemplos: precio 5, cantidad 3 → 15. Precio 2, cantidad 10 → 20.
- Pseudocódigo: guardar precio → guardar cantidad → multiplicar → mostrar total.

```python
precio = 5
cantidad = 3
total = precio * cantidad
print(total)   # 15
```

**0.6**
- Ejemplos: 0 °C → 0 × 9/5 + 32 = 32 °F. 100 °C → 100 × 9/5 + 32 = 212 °F.

```python
celsius = 100
fahrenheit = celsius * 9 / 5 + 32
print(fahrenheit)   # 212.0
```

**0.7** (ejemplo)
1. Tomar un vaso vacío.
2. Llenarlo con agua hasta la mitad.
3. Agregar una cucharadita de azúcar.
4. Revolver con una cuchara.
5. Probar; si no está dulce, repetir desde el paso 3.

---

# MÓDULO 1 — Tu primer programa

## 1.1 `print()`: mostrar cosas en pantalla

`print()` es una **función** que muestra en pantalla lo que le pongas entre paréntesis.

```python
print("Hola, mundo")
```

Salida:

```text
Hola, mundo
```

Descomponiéndolo:

- `print` → el nombre de la función (lo que quiero hacer: mostrar).
- `( )` → los paréntesis, donde van los datos que le doy.
- `"Hola, mundo"` → un **texto** (se llama *string*). Siempre va entre comillas.

### Varias formas de usar `print`

**Forma 1: texto con comillas dobles.**

```python
print("Me llamo Ana")
```

**Forma 2: texto con comillas simples (es lo mismo).**

```python
print('Me llamo Ana')
```

**Forma 3: números (sin comillas).**

```python
print(42)
print(3.14)
```

**Forma 4: una operación (Python la calcula primero).**

```python
print(5 + 3)
print(10 * 2)
```

Salida:

```text
8
20
```

**Forma 5: texto y operación — ¡no es lo mismo!**

```python
print("5 + 3")   # texto: se muestra tal cual
print(5 + 3)     # operación: se calcula
```

Salida:

```text
5 + 3
8
```

> 💡 **Idea clave:** lo que está entre comillas es **texto** y se muestra igual; lo que no tiene comillas, Python intenta **calcularlo o interpretarlo**.

**Forma 6: varios datos separados por coma.**

```python
print("Tengo", 15, "años")
```

Salida:

```text
Tengo 15 años
```

Python pone un espacio entre cada dato automáticamente.

## 1.2 Varias líneas = varias instrucciones

Python ejecuta tu programa **de arriba hacia abajo**, una línea después de otra.

```python
print("Primero")
print("Segundo")
print("Tercero")
```

```text
Primero
Segundo
Tercero
```

Cada `print` termina con un salto de línea. Si cambias el orden de las líneas, cambia el orden de la salida.

## 1.3 Comillas dentro de comillas

¿Y si el texto lleva comillas? Usa un tipo de comillas por fuera y el otro por dentro.

```python
print("Ella dijo: 'hola'")
print('Él respondió: "buenos días"')
```

```text
Ella dijo: 'hola'
Él respondió: "buenos días"
```

## 1.4 Caracteres especiales (secuencias de escape)

Dentro de un texto, la barra invertida `\` tiene poderes especiales:

| Escribes | Significa |
|----------|-----------|
| `\n` | salto de línea |
| `\t` | tabulador (un "espacio grande") |
| `\"` | una comilla doble |
| `\\` | una barra invertida |

```python
print("Línea 1\nLínea 2")
print("Nombre:\tAna")
print("Ella dijo \"hola\"")
print("Ruta: C:\\Users\\Ana")
```

```text
Línea 1
Línea 2
Nombre:	Ana
Ella dijo "hola"
Ruta: C:\Users\Ana
```

## 1.5 Los parámetros `sep` y `end`

`print` tiene opciones extra.

**`sep`**: lo que se pone **entre** los datos (por defecto, un espacio).

```python
print("a", "b", "c")             # a b c
print("a", "b", "c", sep="-")    # a-b-c
print("a", "b", "c", sep="")     # abc
print("2025", "01", "15", sep="/")  # 2025/01/15
```

**`end`**: lo que se pone **al final** (por defecto, un salto de línea).

```python
print("Hola", end=" ")
print("mundo")
```

```text
Hola mundo
```

```python
print("Cargando", end="...")
print("listo")
```

```text
Cargando...listo
```

## 1.6 Imprimir una línea vacía

```python
print("Arriba")
print()
print("Abajo")
```

```text
Arriba

Abajo
```

## 1.7 Multiplicar texto

Un truco divertido: multiplicar un texto lo repite.

```python
print("-" * 20)
print("=" * 10)
print("ja" * 3)
```

```text
--------------------
==========
jajaja
```

Útil para hacer separadores y decorar tu salida:

```python
print("=" * 20)
print("   MI PROGRAMA")
print("=" * 20)
```

## 1.8 Comentarios

Un **comentario** es una nota para humanos. Python lo ignora. Empieza con `#`.

```python
# Esto es un comentario: Python no lo ejecuta
print("Hola")  # También puedo comentar al final de la línea
```

Para qué sirven:

1. **Explicar** qué hace una parte del código.
2. **Desactivar** una línea temporalmente (la "comentas").

```python
print("Esta sí se ejecuta")
# print("Esta no")
```

Comentarios de varias líneas: usa un `#` en cada línea (o un texto entre tres comillas, que veremos más adelante).

```python
# Programa: saludo
# Autor: yo
# Fecha: hoy
print("Hola")
```

## 1.9 Los errores más comunes al empezar

**1. Olvidar las comillas** → `NameError`

```python
print(Hola)        # ❌ Python busca algo llamado Hola
print("Hola")      # ✔️
```

**2. Olvidar cerrar paréntesis o comillas** → `SyntaxError`

```python
print("Hola"       # ❌ falta )
print("Hola")      # ✔️
```

**3. Mayúsculas y minúsculas importan** → `NameError`

```python
Print("Hola")      # ❌ Python distingue Print de print
print("Hola")      # ✔️
```

**4. Espacios al inicio de la línea** → `IndentationError`

```python
 print("Hola")     # ❌ hay un espacio de más al inicio
print("Hola")      # ✔️
```

> ⚠️ En Python, **los espacios al inicio de una línea tienen significado** (lo verás en el Módulo 6). Por ahora, empieza todas tus líneas pegadas al borde izquierdo.

## 1.10 Resumen del Módulo 1

- `print()` muestra cosas en pantalla.
- Texto va entre comillas; números no.
- `\n` salta de línea; `\t` tabula.
- `sep` cambia el separador; `end` cambia el final.
- `"-" * 20` repite texto.
- `#` inicia un comentario.
- El código se ejecuta de arriba hacia abajo.

## 1.11 🎯 Ejercicios del Módulo 1

**Ejercicio 1.1** — Muestra en pantalla: `¡Hola, mundo!`

**Ejercicio 1.2** — Muestra tu nombre en una línea y tu ciudad en la siguiente (con dos `print`).

**Ejercicio 1.3** — Muestra en **un solo** `print` dos líneas: `Línea 1` y `Línea 2` (usa `\n`).

**Ejercicio 1.4** — Muestra el resultado de `7 * 6` usando `print` (sin escribir el 42 a mano).

**Ejercicio 1.5** — Muestra exactamente esto (con las comillas): `Ella dijo: "Me gusta Python"`

**Ejercicio 1.6** — Muestra `2025-01-15` usando `print` con `sep` y los tres datos `"2025"`, `"01"`, `"15"` por separado.

**Ejercicio 1.7** — Con dos `print` y el parámetro `end`, muestra en una sola línea: `Hola mundo`.

**Ejercicio 1.8** — Dibuja un marco con el texto en medio, usando multiplicación de texto:

```text
==============
   BIENVENIDO
==============
```

**Ejercicio 1.9** — Muestra una tabla simple con tabuladores:

```text
Nombre	Edad
Ana	20
Luis	25
```

**Ejercicio 1.10** — Este programa tiene 3 errores. Encuéntralos y corrígelos:

```python
Print("Hola)
print("Adiós"
```

**Ejercicio 1.11** — Muestra una "carita" de varias líneas con `print` (usa tu creatividad):

```text
 ^   ^
  ---
```

**Ejercicio 1.12** — Escribe un programa de 3 líneas de `print` que muestre una pequeña presentación tuya (nombre, edad, qué quieres aprender). Agrega un comentario al inicio que diga para qué sirve.

### ✅ Soluciones del Módulo 1

**1.1**

```python
print("¡Hola, mundo!")
```

**1.2**

```python
print("Ana")
print("La Habana")
```

**1.3**

```python
print("Línea 1\nLínea 2")
```

**1.4**

```python
print(7 * 6)   # 42
```

**1.5**

```python
print('Ella dijo: "Me gusta Python"')
```

**1.6**

```python
print("2025", "01", "15", sep="-")
```

**1.7**

```python
print("Hola", end=" ")
print("mundo")
```

**1.8**

```python
print("=" * 14)
print("   BIENVENIDO")
print("=" * 14)
```

**1.9**

```python
print("Nombre\tEdad")
print("Ana\t20")
print("Luis\t25")
```

**1.10** Errores: (1) `Print` debe ser `print` en minúscula; (2) falta cerrar las comillas en `"Hola)`; (3) falta el `)` en la segunda línea.

```python
print("Hola")
print("Adiós")
```

**1.11**

```python
print(" ^   ^")
print("  ---")
```

**1.12** (ejemplo)

```python
# Presentación personal
print("Me llamo Ana")
print("Tengo 20 años")
print("Quiero aprender a programar en Python")
```

---

# MÓDULO 2 — Variables y tipos de datos

## 2.1 ¿Qué es una variable?

Una **variable** es una **caja con una etiqueta** donde guardas un dato para usarlo después.

```python
edad = 15
```

Se lee: "la variable `edad` guarda el valor `15`".

- `edad` → el nombre (la etiqueta de la caja).
- `=` → **asignar** (guardar). **No** significa "igual" como en matemáticas: significa "guarda lo de la derecha en lo de la izquierda".
- `15` → el valor.

Una vez guardado, puedes usar la variable:

```python
edad = 15
print(edad)
```

```text
15
```

### La misma idea explicada de otras maneras

**Analogía 1: el casillero.** Imagina un casillero de la escuela con tu nombre. Puedes meter y sacar cosas. Si metes algo nuevo, lo anterior se va.

**Analogía 2: el celular.** El contacto "Mamá" es un nombre que apunta a un número. Si cambias el número, el nombre sigue igual.

**Analogía 3: la pizarra.** Escribes `edad = 15` en la pizarra. Si luego escribes `edad = 16`, borras el 15 y queda el 16.

```python
edad = 15
print(edad)   # 15
edad = 16     # ahora la caja guarda 16
print(edad)   # 16
```

## 2.2 Usar variables en cálculos

```python
a = 10
b = 3
suma = a + b
print(suma)   # 13
```

Una variable puede usarse en su propia actualización:

```python
puntos = 10
puntos = puntos + 5     # toma el 10, le suma 5, guarda 15
print(puntos)           # 15
```

> 💡 Lee `puntos = puntos + 5` como: "calcula `puntos + 5` y **luego** guarda el resultado en `puntos`".

Más ejemplos del mismo tipo:

```python
vidas = 3
vidas = vidas - 1
print(vidas)   # 2

precio = 100
precio = precio * 2
print(precio)  # 200

contador = 0
contador = contador + 1
contador = contador + 1
print(contador)  # 2
```

## 2.3 Reglas para nombrar variables

1. Solo letras, números y guion bajo `_`.
2. **No** puede empezar con un número.
3. **No** puede tener espacios.
4. Mayúsculas y minúsculas son distintas: `edad` ≠ `Edad`.
5. **No** uses palabras reservadas de Python (`if`, `for`, `class`, `True`...).

```python
nombre = "Ana"          # ✔️
edad_actual = 15        # ✔️ (usa guion bajo para separar palabras)
precio2 = 9.99          # ✔️
_secreto = 1            # ✔️

2precio = 5             # ❌ empieza con número
mi nombre = "Ana"       # ❌ tiene espacio
class = "A"             # ❌ palabra reservada
```

**Buenas costumbres:**

- Usa nombres que expliquen: `precio_total` es mejor que `x`.
- Estilo recomendado: minúsculas con guion bajo (`nombre_completo`). Se llama *snake_case*.

```python
# Mal
x = 25
y = 4
z = x * y

# Bien
precio = 25
cantidad = 4
total = precio * cantidad
```

## 2.4 Los tipos de datos básicos

Cada dato tiene un **tipo**. Es como la categoría del dato.

| Tipo | Nombre | Ejemplos | Para qué |
|------|--------|----------|----------|
| `int` | entero | `5`, `-3`, `0`, `1000` | contar cosas |
| `float` | decimal | `3.14`, `-0.5`, `2.0` | medir cosas |
| `str` | texto | `"hola"`, `'a'`, `"123"` | palabras y frases |
| `bool` | booleano | `True`, `False` | sí / no |
| `NoneType` | nada | `None` | "no hay valor" |

Con `type()` puedes preguntarle a Python de qué tipo es un dato:

```python
print(type(5))        # <class 'int'>
print(type(5.0))      # <class 'float'>
print(type("hola"))   # <class 'str'>
print(type(True))     # <class 'bool'>
print(type(None))     # <class 'NoneType'>
```

### `int` — números enteros

```python
manzanas = 12
temperatura = -4
cero = 0
grande = 1_000_000    # el _ ayuda a leer; vale 1000000
print(manzanas, temperatura, cero, grande)
```

### `float` — números con decimales

El decimal se escribe con **punto**, no con coma.

```python
altura = 1.75
pi = 3.14159
negativo = -0.5
print(altura, pi, negativo)
```

⚠️ `5` es `int`, pero `5.0` es `float`. Son parecidos pero distintos.

### `str` — texto

```python
nombre = "Ana"
frase = 'Me gusta Python'
vacio = ""
print(nombre, frase)
```

⚠️ **`"123"` (con comillas) es texto, no número.**

```python
a = 123      # número
b = "123"    # texto
print(type(a))   # <class 'int'>
print(type(b))   # <class 'str'>
```

### `bool` — verdadero o falso

Solo tiene dos valores: `True` y `False` (con la primera letra mayúscula).

```python
es_mayor = True
tiene_llave = False
print(es_mayor, tiene_llave)
```

Los booleanos aparecen cuando **comparas** cosas:

```python
print(5 > 3)    # True
print(5 < 3)    # False
print(5 == 5)   # True
```

### `None` — "nada"

```python
resultado = None
print(resultado)   # None
```

Se usa para decir "todavía no hay valor".

## 2.5 Asignación múltiple

**Varias variables a la vez, con distintos valores:**

```python
nombre, edad, ciudad = "Ana", 20, "Madrid"
print(nombre)   # Ana
print(edad)     # 20
print(ciudad)   # Madrid
```

**Varias variables con el mismo valor:**

```python
a = b = c = 0
print(a, b, c)   # 0 0 0
```

**Intercambiar valores (¡truco de Python!):**

```python
x = 1
y = 2
x, y = y, x
print(x, y)   # 2 1
```

En otros lenguajes necesitas una variable temporal. En Python no.

## 2.6 Conversión de tipos (casting)

A veces necesitas pasar un dato de un tipo a otro.

| Función | Hace |
|---------|------|
| `int(x)` | convierte a entero |
| `float(x)` | convierte a decimal |
| `str(x)` | convierte a texto |
| `bool(x)` | convierte a booleano |

```python
print(int("42"))      # 42      (texto → entero)
print(int(3.9))       # 3       (corta los decimales, no redondea)
print(float("2.5"))   # 2.5     (texto → decimal)
print(float(7))       # 7.0     (entero → decimal)
print(str(100))       # "100"   (número → texto)
```

**¿Por qué es importante?** Porque `"5" + "3"` y `5 + 3` dan resultados distintos:

```python
print(5 + 3)        # 8      (suma de números)
print("5" + "3")    # 53     (une textos)
```

Y mezclar tipos da error:

```python
edad = 15
print("Tengo " + edad)          # ❌ TypeError: no puedes sumar texto y número
print("Tengo " + str(edad))     # ✔️ Tengo 15
print("Tengo", edad)            # ✔️ Tengo 15 (con coma no hay problema)
```

Una conversión puede fallar:

```python
int("hola")    # ❌ ValueError: "hola" no es un número
```

### `bool()`: ¿qué es verdadero y qué es falso?

Son **falsos**: `0`, `0.0`, `""` (texto vacío), `None`, y las colecciones vacías (`[]`, `{}`...). **Todo lo demás es verdadero.**

```python
print(bool(0))        # False
print(bool(5))        # True
print(bool(""))       # False
print(bool("hola"))   # True
print(bool(None))     # False
```

## 2.7 Constantes

Python no tiene constantes "de verdad", pero por convención un nombre **EN MAYÚSCULAS** significa "no lo cambies":

```python
PI = 3.14159
IVA = 0.21
MAX_INTENTOS = 3
```

## 2.8 Ejemplos completos

**Ejemplo A: ficha de una persona**

```python
nombre = "Luis"
edad = 25
altura = 1.80
es_estudiante = True

print("Nombre:", nombre)
print("Edad:", edad)
print("Altura:", altura)
print("¿Estudiante?", es_estudiante)
```

```text
Nombre: Luis
Edad: 25
Altura: 1.8
¿Estudiante? True
```

**Ejemplo B: total de una compra**

```python
precio = 4
cantidad = 6
total = precio * cantidad
print("Total a pagar:", total)   # Total a pagar: 24
```

**Ejemplo C: promedio de tres notas**

```python
nota1 = 8
nota2 = 7
nota3 = 9
promedio = (nota1 + nota2 + nota3) / 3
print("Promedio:", promedio)   # Promedio: 8.0
```

## 2.9 ⚠️ Errores comunes

```python
print(edad)         # NameError si 'edad' no fue creada antes
nombre = Ana        # NameError: faltan comillas
precio = 3,5        # ¡No da error! Pero crea una tupla (3, 5). Usa 3.5
Edad = 5; print(edad)   # NameError: Edad ≠ edad
```

## 2.10 Resumen del Módulo 2

- Una variable guarda un dato: `nombre = valor`.
- `=` significa "guardar", no "igual".
- Tipos: `int`, `float`, `str`, `bool`, `None`.
- `type()` te dice el tipo.
- `int()`, `float()`, `str()`, `bool()` convierten.
- Nombres: minúsculas, sin espacios, con guion bajo, que expliquen.

## 2.11 🎯 Ejercicios del Módulo 2

**Ejercicio 2.1** — Crea una variable `nombre` con tu nombre y muéstrala.

**Ejercicio 2.2** — Crea las variables `edad` (entero) y `altura` (decimal) y muéstralas en una sola línea con `print`.

**Ejercicio 2.3** — Muestra el tipo (`type`) de estas cuatro cosas: `10`, `10.5`, `"10"`, `True`.

**Ejercicio 2.4** — Crea `a = 8` y `b = 5`. Calcula y muestra la suma, la resta y la multiplicación, cada una en una variable distinta.

**Ejercicio 2.5** — Crea `vidas = 3`. Réstale 1 y muestra el resultado. Hazlo otra vez y muestra de nuevo.

**Ejercicio 2.6** — Intercambia los valores de `x = "izquierda"` y `y = "derecha"` y muéstralos.

**Ejercicio 2.7** — Convierte el texto `"25"` a entero, súmale 5 y muestra el resultado.

**Ejercicio 2.8** — Convierte el número `100` a texto y únelo con `"%"` para mostrar `100%`.

**Ejercicio 2.9** — Calcula el promedio de las notas 10, 8 y 6 guardándolas en variables.

**Ejercicio 2.10** — Crea una variable `precio = 20` y `descuento = 0.25`. Calcula el precio final (precio menos el 25 %) y muéstralo.

**Ejercicio 2.11** — Con `a = b = c = 5`, cambia solo `b` a 10 y muestra las tres. ¿Qué sale? Explica por qué.

**Ejercicio 2.12** — ¿Cuáles de estos nombres son válidos? `nombre`, `2nombre`, `mi_edad`, `mi edad`, `for`, `_x`, `Precio`.

**Ejercicio 2.13** — Predice (sin ejecutar) qué muestra y luego comprueba:

```python
x = 5
x = x + 2
x = x * 3
print(x)
```

**Ejercicio 2.14** — Muestra el valor `bool()` de: `0`, `1`, `""`, `"a"`, `None`.

### ✅ Soluciones del Módulo 2

**2.1**

```python
nombre = "Ana"
print(nombre)
```

**2.2**

```python
edad = 20
altura = 1.65
print(edad, altura)
```

**2.3**

```python
print(type(10))     # int
print(type(10.5))   # float
print(type("10"))   # str
print(type(True))   # bool
```

**2.4**

```python
a = 8
b = 5
suma = a + b
resta = a - b
producto = a * b
print(suma, resta, producto)   # 13 3 40
```

**2.5**

```python
vidas = 3
vidas = vidas - 1
print(vidas)   # 2
vidas = vidas - 1
print(vidas)   # 1
```

**2.6**

```python
x = "izquierda"
y = "derecha"
x, y = y, x
print(x, y)   # derecha izquierda
```

**2.7**

```python
numero = int("25")
print(numero + 5)   # 30
```

**2.8**

```python
print(str(100) + "%")   # 100%
```

**2.9**

```python
n1 = 10
n2 = 8
n3 = 6
print((n1 + n2 + n3) / 3)   # 8.0
```

**2.10**

```python
precio = 20
descuento = 0.25
final = precio - precio * descuento
print(final)   # 15.0
```

**2.11**

```python
a = b = c = 5
b = 10
print(a, b, c)   # 5 10 5
```

Porque cada variable es una caja distinta: cambiar `b` no afecta a `a` ni a `c`.

**2.12** Válidos: `nombre`, `mi_edad`, `_x`, `Precio`. Inválidos: `2nombre` (empieza con número), `mi edad` (espacio), `for` (palabra reservada).

**2.13** `x` pasa por 5 → 7 → 21. Muestra `21`.

**2.14**

```python
print(bool(0))      # False
print(bool(1))      # True
print(bool(""))     # False
print(bool("a"))    # True
print(bool(None))   # False
```

---

# MÓDULO 3 — Operadores

Un **operador** es un símbolo que hace una operación: `+`, `-`, `*`, `>`... Los datos sobre los que actúa se llaman **operandos**. En `5 + 3`: el operador es `+`, los operandos son `5` y `3`.

## 3.1 Operadores aritméticos

| Operador | Nombre | Ejemplo | Resultado |
|----------|--------|---------|-----------|
| `+` | suma | `7 + 2` | `9` |
| `-` | resta | `7 - 2` | `5` |
| `*` | multiplicación | `7 * 2` | `14` |
| `/` | división (siempre da `float`) | `7 / 2` | `3.5` |
| `//` | división entera (descarta decimales) | `7 // 2` | `3` |
| `%` | módulo (el **resto**) | `7 % 2` | `1` |
| `**` | potencia | `7 ** 2` | `49` |

### La división: `/` vs `//` vs `%`

Imagina que reparto 7 caramelos entre 2 amigos:

- Cada uno recibe `7 // 2` = **3** caramelos (división entera).
- Sobra `7 % 2` = **1** caramelo (resto).
- Si pudiera partir el caramelo, a cada uno le tocaría `7 / 2` = **3.5**.

```python
print(7 / 2)    # 3.5
print(7 // 2)   # 3
print(7 % 2)    # 1
```

Otro ejemplo: 17 galletas en cajas de 5.

```python
print(17 // 5)   # 3  → llenas 3 cajas
print(17 % 5)    # 2  → sobran 2 galletas
```

Y otro: ¿cuántas horas completas son 200 minutos?

```python
minutos = 200
horas = minutos // 60       # 3
resto = minutos % 60        # 20
print(horas, "h", resto, "min")   # 3 h 20 min
```

### Usos famosos del `%`

**¿Es par o impar?** Si el resto de dividir entre 2 es 0, es par.

```python
print(10 % 2)   # 0 → par
print(7 % 2)    # 1 → impar
```

**¿Es múltiplo de 5?**

```python
print(25 % 5)   # 0 → sí
print(26 % 5)   # 1 → no
```

**Último dígito de un número:**

```python
print(1234 % 10)   # 4
```

**Quitar el último dígito:**

```python
print(1234 // 10)   # 123
```

### Potencias y raíces

```python
print(2 ** 3)     # 8      (2 × 2 × 2)
print(5 ** 2)     # 25     (5 × 5)
print(10 ** 0)    # 1
print(9 ** 0.5)   # 3.0    (elevar a 0.5 es sacar la raíz cuadrada)
```

## 3.2 Orden de las operaciones (precedencia)

Igual que en matemáticas, de mayor a menor prioridad:

1. Paréntesis `( )`
2. Potencia `**`
3. Multiplicación, división, `//`, `%` (de izquierda a derecha)
4. Suma y resta (de izquierda a derecha)

```python
print(2 + 3 * 4)     # 14  (primero 3*4=12, luego +2)
print((2 + 3) * 4)   # 20  (primero el paréntesis)
print(2 ** 3 * 2)    # 16  (8 * 2)
print(10 - 4 - 3)    # 3   (izquierda a derecha: (10-4)-3)
```

> 💡 **Ante la duda, usa paréntesis.** Hacen tu código más claro.

## 3.3 Operadores de asignación aumentada

Atajos para actualizar una variable:

| Atajo | Equivale a |
|-------|------------|
| `x += 5` | `x = x + 5` |
| `x -= 5` | `x = x - 5` |
| `x *= 5` | `x = x * 5` |
| `x /= 5` | `x = x / 5` |
| `x //= 5` | `x = x // 5` |
| `x %= 5` | `x = x % 5` |
| `x **= 5` | `x = x ** 5` |

```python
puntos = 10
puntos += 5
print(puntos)   # 15
puntos -= 3
print(puntos)   # 12
puntos *= 2
print(puntos)   # 24
```

También funcionan con texto:

```python
mensaje = "Hola"
mensaje += " mundo"
print(mensaje)   # Hola mundo
```

## 3.4 Operadores de comparación

Comparan dos valores y devuelven `True` o `False`.

| Operador | Significa | Ejemplo | Resultado |
|----------|-----------|---------|-----------|
| `==` | igual a | `5 == 5` | `True` |
| `!=` | distinto de | `5 != 3` | `True` |
| `>` | mayor que | `5 > 3` | `True` |
| `<` | menor que | `5 < 3` | `False` |
| `>=` | mayor o igual | `5 >= 5` | `True` |
| `<=` | menor o igual | `4 <= 3` | `False` |

⚠️ **`=` guarda, `==` compara.** Es el error #1 de los principiantes.

```python
x = 5        # guardar: x ahora vale 5
x == 5       # comparar: ¿x es igual a 5? → True
```

Más ejemplos:

```python
edad = 17
print(edad >= 18)       # False
print(edad < 18)        # True
print(edad != 17)       # False
print("a" == "a")       # True
print("a" == "A")       # False (mayúsculas importan)
print("casa" < "perro") # True (orden alfabético)
```

Comparaciones encadenadas (muy "pythónicas"):

```python
x = 5
print(1 < x < 10)   # True  (¿x está entre 1 y 10?)
print(1 < x < 3)    # False
```

## 3.5 Operadores lógicos

Combinan valores `True`/`False`.

| Operador | Significa | Cuándo da `True` |
|----------|-----------|------------------|
| `and` | y | **ambos** son verdaderos |
| `or` | o | **al menos uno** es verdadero |
| `not` | no | invierte el valor |

**Tablas de verdad:**

| A | B | `A and B` | `A or B` |
|---|---|-----------|----------|
| True | True | True | True |
| True | False | False | True |
| False | True | False | True |
| False | False | False | False |

**Ejemplos con la vida real:**

- "Puedo salir si hice la tarea **Y** limpié mi cuarto" → necesito las dos cosas (`and`).
- "Puedo pagar con tarjeta **O** con efectivo" → me basta una (`or`).
- "**No** está lloviendo" → lo contrario de "está lloviendo" (`not`).

**Con código:**

```python
edad = 20
tiene_carnet = True

print(edad >= 18 and tiene_carnet)   # True  (ambas se cumplen)
print(edad >= 18 and not tiene_carnet) # False
print(edad < 18 or tiene_carnet)     # True  (al menos una se cumple)
print(not (edad > 30))               # True
```

```python
nota = 7
print(nota >= 5 and nota <= 10)   # True: ¿está entre 5 y 10?
print(5 <= nota <= 10)            # True: lo mismo, más corto
```

```python
dia = "sábado"
print(dia == "sábado" or dia == "domingo")   # True → es fin de semana
```

## 3.6 Operadores de pertenencia: `in` y `not in`

Comprueban si algo está **dentro** de otra cosa.

```python
print("a" in "casa")        # True
print("z" in "casa")        # False
print("sol" in "el sol sale") # True
print("z" not in "casa")    # True
```

(Más adelante lo usarás con listas, diccionarios, etc.)

## 3.7 Funciones numéricas útiles

```python
print(abs(-7))           # 7        valor absoluto
print(round(3.567, 2))   # 3.57     redondear a 2 decimales
print(round(3.5))        # 4        redondear a entero
print(round(2.4))        # 2
print(max(3, 9, 5))      # 9        el mayor
print(min(3, 9, 5))      # 3        el menor
print(pow(2, 5))         # 32       2 elevado a la 5
print(divmod(17, 5))     # (3, 2)   cociente y resto a la vez
print(sum([1, 2, 3]))    # 6        suma de una lista
```

⚠️ **Decimales raros.** Los `float` pueden tener pequeños errores de precisión. No es un fallo de Python: es cómo las computadoras guardan decimales.

```python
print(0.1 + 0.2)              # 0.30000000000000004
print(round(0.1 + 0.2, 2))    # 0.3  ← usa round para mostrarlo bonito
```

## 3.8 Ejemplos completos

**Ejemplo A: convertir segundos a minutos y segundos**

```python
total = 135
minutos = total // 60      # 2
segundos = total % 60      # 15
print(minutos, "min", segundos, "s")   # 2 min 15 s
```

**Ejemplo B: precio con IVA**

```python
precio = 50
iva = 0.21
total = precio * (1 + iva)
print(total)   # 60.5
```

**Ejemplo C: ¿puede entrar al cine?**

```python
edad = 15
tiene_permiso = True
puede = edad >= 18 or tiene_permiso
print(puede)   # True
```

## 3.9 Resumen del Módulo 3

- Aritméticos: `+ - * / // % **`.
- `//` da el cociente, `%` el resto.
- Comparación: `== != > < >= <=` → dan `True`/`False`.
- Lógicos: `and`, `or`, `not`.
- `+=`, `-=`, etc. son atajos.
- `in` comprueba pertenencia.
- Ante la duda, paréntesis.

## 3.10 🎯 Ejercicios del Módulo 3

**Ejercicio 3.1** — Calcula y muestra `15 + 4`, `15 - 4`, `15 * 4`, `15 / 4`, `15 // 4`, `15 % 4`, `15 ** 2`.

**Ejercicio 3.2** — Predice y comprueba: `2 + 3 * 4 - 1`.

**Ejercicio 3.3** — Pon paréntesis para que `2 + 3 * 4` valga `20`.

**Ejercicio 3.4** — Convierte 500 segundos en minutos y segundos (muestra ambos).

**Ejercicio 3.5** — Tienes 23 manzanas y quieres hacer bolsas de 4. ¿Cuántas bolsas llenas? ¿Cuántas sobran?

**Ejercicio 3.6** — Muestra si `47` es par (usa `%` y `==`; el resultado debe ser `True` o `False`).

**Ejercicio 3.7** — Muestra el último dígito de `5982` y el número sin su último dígito.

**Ejercicio 3.8** — Con `x = 7`, muestra si `x` está entre 1 y 10 (comparación encadenada) y si `x` es mayor que 10 o menor que 3.

**Ejercicio 3.9** — Con `puntos = 100`, aplica en orden: `+= 50`, `-= 30`, `*= 2`. Muestra el resultado final.

**Ejercicio 3.10** — Calcula el área y el perímetro de un círculo de radio 5 (usa `pi = 3.14159`). Redondea a 2 decimales.

**Ejercicio 3.11** — Con `edad = 16` y `acompanado = True`, muestra si puede entrar si "es mayor de edad **o** va acompañado".

**Ejercicio 3.12** — Muestra el resultado de `"sol" in "girasol"` y de `"luna" in "girasol"`.

**Ejercicio 3.13** — Calcula cuánto es un 15 % de propina sobre una cuenta de 80.

**Ejercicio 3.14** — Se reparten 3 pizzas de 8 porciones entre 5 personas. ¿Cuántas porciones recibe cada uno (entero) y cuántas sobran?

### ✅ Soluciones del Módulo 3

**3.1**

```python
print(15 + 4)    # 19
print(15 - 4)    # 11
print(15 * 4)    # 60
print(15 / 4)    # 3.75
print(15 // 4)   # 3
print(15 % 4)    # 3
print(15 ** 2)   # 225
```

**3.2** `3 * 4 = 12`, luego `2 + 12 - 1 = 13`.

**3.3**

```python
print((2 + 3) * 4)   # 20
```

**3.4**

```python
total = 500
print(total // 60, "min", total % 60, "s")   # 8 min 20 s
```

**3.5**

```python
print(23 // 4)   # 5 bolsas
print(23 % 4)    # 3 sobran
```

**3.6**

```python
print(47 % 2 == 0)   # False
```

**3.7**

```python
n = 5982
print(n % 10)    # 2
print(n // 10)   # 598
```

**3.8**

```python
x = 7
print(1 < x < 10)        # True
print(x > 10 or x < 3)   # False
```

**3.9**

```python
puntos = 100
puntos += 50    # 150
puntos -= 30    # 120
puntos *= 2     # 240
print(puntos)   # 240
```

**3.10**

```python
pi = 3.14159
radio = 5
area = pi * radio ** 2
perimetro = 2 * pi * radio
print(round(area, 2))        # 78.54
print(round(perimetro, 2))   # 31.42
```

**3.11**

```python
edad = 16
acompanado = True
print(edad >= 18 or acompanado)   # True
```

**3.12**

```python
print("sol" in "girasol")    # True
print("luna" in "girasol")   # False
```

**3.13**

```python
cuenta = 80
propina = cuenta * 0.15
print(propina)   # 12.0
```

**3.14**

```python
porciones = 3 * 8                 # 24
print(porciones // 5)             # 4 cada uno
print(porciones % 5)              # 4 sobran
```

---

# MÓDULO 4 — Cadenas de texto (strings)

Un **string** (`str`) es una secuencia de caracteres: letras, números, símbolos, espacios. Casi todo programa trabaja con texto: nombres, mensajes, contraseñas, direcciones...

## 4.1 Crear strings

```python
a = "Hola"
b = 'Mundo'
c = "Es el libro de Ana"        # comillas dobles permiten ' dentro
d = 'Dijo "hola"'               # comillas simples permiten " dentro
vacio = ""
print(a, b, c, d, vacio)
```

**Strings de varias líneas** con tres comillas:

```python
poema = """Rosas son rojas,
violetas son azules,
Python es genial."""
print(poema)
```

## 4.2 Longitud: `len()`

`len` cuenta cuántos caracteres hay (incluyendo espacios).

```python
print(len("Hola"))         # 4
print(len("Hola mundo"))   # 10  (el espacio cuenta)
print(len(""))             # 0
```

## 4.3 Unir (concatenar) y repetir

```python
nombre = "Ana"
saludo = "Hola, " + nombre + "!"
print(saludo)   # Hola, Ana!

print("ja" * 3)       # jajaja
print("-" * 10)       # ----------
```

⚠️ Solo puedes unir `str` con `str`:

```python
edad = 20
# print("Tengo " + edad)        # ❌ TypeError
print("Tengo " + str(edad))     # ✔️ Tengo 20
```

## 4.4 Índices: acceder a un carácter

Cada carácter tiene una **posición** (índice). ¡Se empieza a contar desde **0**!

```text
 texto:   P   y   t   h   o   n
 índice:  0   1   2   3   4   5
 negativo:-6  -5  -4  -3  -2  -1
```

```python
palabra = "Python"
print(palabra[0])    # P  (primero)
print(palabra[1])    # y
print(palabra[5])    # n  (último)
print(palabra[-1])   # n  (último, contando desde atrás)
print(palabra[-2])   # o  (penúltimo)
```

Más ejemplos con otra palabra:

```python
fruta = "manzana"
print(fruta[0])    # m
print(fruta[3])    # z
print(fruta[-1])   # a
print(fruta[len(fruta) - 1])   # a  (otra forma de sacar el último)
```

⚠️ Si pides un índice que no existe: `IndexError`.

```python
print("Hola"[10])   # ❌ IndexError: string index out of range
```

## 4.5 Rebanadas (slicing): `[inicio:fin:paso]`

Sirven para sacar un **trozo** del texto. El `inicio` se incluye, el `fin` **no**.

```python
palabra = "Programar"
#          012345678

print(palabra[0:3])    # Pro     (posiciones 0,1,2)
print(palabra[3:6])    # gra
print(palabra[:3])     # Pro     (sin inicio = desde el principio)
print(palabra[3:])     # gramar  (sin fin = hasta el final)
print(palabra[:])      # Programar (todo)
print(palabra[-3:])    # mar     (los últimos 3)
print(palabra[:-1])    # Programa (todo menos el último)
```

Con **paso**:

```python
print(palabra[::2])    # Pormr    (de 2 en 2)
print(palabra[::-1])   # ramargorP (¡al revés!)
```

Otro ejemplo con números:

```python
digitos = "0123456789"
print(digitos[2:5])    # 234
print(digitos[::3])    # 0369
print(digitos[::-1])   # 9876543210
print(digitos[-4:])    # 6789
```

> 💡 `texto[::-1]` es el truco clásico para **invertir** un texto.

## 4.6 Los strings son inmutables

No puedes cambiar un carácter "por dentro":

```python
palabra = "Hola"
# palabra[0] = "J"   # ❌ TypeError
```

Lo que haces es **crear un string nuevo**:

```python
palabra = "Hola"
nueva = "J" + palabra[1:]
print(nueva)   # Jola
```

## 4.7 Métodos de strings

Un **método** es una función que "pertenece" al texto y se usa con un punto: `texto.metodo()`. **No cambian el original**: devuelven uno nuevo.

### Mayúsculas y minúsculas

```python
frase = "hola Mundo"
print(frase.upper())        # HOLA MUNDO
print(frase.lower())        # hola mundo
print(frase.capitalize())   # Hola mundo
print(frase.title())        # Hola Mundo
print(frase.swapcase())     # HOLA mUNDO
```

### Limpiar espacios

```python
sucio = "   hola   "
print(sucio.strip())    # "hola"
print(sucio.lstrip())   # "hola   "
print(sucio.rstrip())   # "   hola"
```

### Buscar

```python
frase = "me gusta programar en python"
print(frase.find("gusta"))     # 3   (posición donde empieza)
print(frase.find("java"))      # -1  (no está)
print(frase.count("a"))        # 4   (cuántas veces aparece)
print(frase.startswith("me"))  # True
print(frase.endswith("on"))    # True
print("python" in frase)       # True
```

### Reemplazar

```python
frase = "Me gusta el café"
print(frase.replace("café", "té"))    # Me gusta el té
print("a-b-c".replace("-", ""))       # abc
print("hola hola".replace("hola", "adiós", 1))  # adiós hola (solo 1 vez)
```

### Dividir (`split`) y unir (`join`)

`split` rompe un texto en una **lista** de pedazos:

```python
print("uno dos tres".split())        # ['uno', 'dos', 'tres']
print("a,b,c".split(","))            # ['a', 'b', 'c']
print("2025-01-15".split("-"))       # ['2025', '01', '15']
```

`join` hace lo contrario: une una lista con un separador:

```python
palabras = ["uno", "dos", "tres"]
print(" ".join(palabras))     # uno dos tres
print("-".join(palabras))     # uno-dos-tres
print("".join(palabras))      # unodostres
```

### Comprobar contenido

```python
print("abc".isalpha())     # True  (solo letras)
print("123".isdigit())     # True  (solo dígitos)
print("abc123".isalnum())  # True  (letras y números)
print("   ".isspace())     # True  (solo espacios)
print("HOLA".isupper())    # True
print("hola".islower())    # True
print("12a".isdigit())     # False
```

### Rellenar y alinear

```python
print("7".zfill(3))         # 007
print("hola".center(10, "*"))  # ***hola***
print("hola".ljust(8, ".") + "|")  # hola....|
print("hola".rjust(8, ".") + "|")  # ....hola|
```

## 4.8 f-strings: mezclar texto y variables (¡lo mejor!)

Pon una `f` antes de las comillas y las variables entre `{ }`:

```python
nombre = "Ana"
edad = 20
print(f"Me llamo {nombre} y tengo {edad} años")
```

```text
Me llamo Ana y tengo 20 años
```

Dentro de `{ }` puedes hacer **cálculos**:

```python
a = 4
b = 5
print(f"{a} + {b} = {a + b}")        # 4 + 5 = 9
print(f"El doble de {a} es {a * 2}")  # El doble de 4 es 8
```

**Formatos útiles:**

```python
pi = 3.14159265
print(f"{pi:.2f}")        # 3.14      (2 decimales)
print(f"{pi:.0f}")        # 3         (0 decimales)
print(f"{1234567:,}")     # 1,234,567 (separador de miles)
print(f"{0.256:.1%}")     # 25.6%     (porcentaje)
print(f"{5:03d}")         # 005       (rellenar con ceros)
print(f"{'hola':>10}")    # '      hola' (alinear a la derecha en 10)
print(f"{'hola':<10}|")   # 'hola      |' (a la izquierda)
print(f"{'hola':^10}|")   # '   hola   |' (centrado)
```

**Comparemos 4 formas de hacer lo mismo:**

```python
nombre = "Luis"
edad = 25

print("Me llamo " + nombre + " y tengo " + str(edad))   # concatenar (incómodo)
print("Me llamo", nombre, "y tengo", edad)              # con comas
print("Me llamo {} y tengo {}".format(nombre, edad))    # format (antiguo)
print(f"Me llamo {nombre} y tengo {edad}")              # f-string (¡la mejor!)
```

> 💡 **Usa f-strings casi siempre.** Son más claras y cortas.

## 4.9 Recorrer un string (adelanto)

Aunque aún no vemos bucles, así se ve cómo se recorre letra por letra:

```python
for letra in "Hola":
    print(letra)
```

```text
H
o
l
a
```

(El bucle `for` lo estudiaremos en el Módulo 8.)

## 4.10 Ejemplos completos

**Ejemplo A: iniciales de un nombre**

```python
nombre = "Ana"
apellido = "Pérez"
iniciales = nombre[0] + apellido[0]
print(iniciales)   # AP
```

**Ejemplo B: correo a partir del nombre**

```python
nombre = "  Luis García "
limpio = nombre.strip().lower().replace(" ", ".")
print(limpio + "@correo.com")   # luis.garcía@correo.com
```

**Ejemplo C: ¿es palíndromo?** (se lee igual al derecho y al revés)

```python
palabra = "reconocer"
print(palabra == palabra[::-1])   # True
```

**Ejemplo D: cambiar el formato de una fecha**

```python
fecha = "2025-03-09"
anio, mes, dia = fecha.split("-")
print(f"{dia}/{mes}/{anio}")   # 09/03/2025
```

## 4.11 ⚠️ Errores comunes

```python
texto = "hola"
texto.upper()          # ❌ no hace nada visible: el resultado se pierde
print(texto)           # hola (sigue igual)

texto = texto.upper()  # ✔️ guarda el resultado
print(texto)           # HOLA
```

```python
print("Hola"[4])       # ❌ IndexError (solo hay índices 0 a 3)
print("5" + 5)         # ❌ TypeError
```

## 4.12 Resumen del Módulo 4

- Texto entre comillas simples, dobles o triples.
- `len()` cuenta caracteres. Índices desde 0; `-1` es el último.
- Slicing: `[inicio:fin:paso]`; `[::-1]` invierte.
- Métodos: `upper`, `lower`, `strip`, `replace`, `find`, `count`, `split`, `join`...
- Los strings no cambian: los métodos devuelven uno nuevo.
- **f-strings**: `f"Hola {nombre}"`.

## 4.13 🎯 Ejercicios del Módulo 4

**Ejercicio 4.1** — Guarda tu nombre en una variable y muestra cuántas letras tiene.

**Ejercicio 4.2** — Con `palabra = "elefante"`, muestra la primera letra, la última y la tercera.

**Ejercicio 4.3** — Con `palabra = "murciélago"`, muestra los 3 primeros caracteres y los 3 últimos.

**Ejercicio 4.4** — Muestra `"python"` en mayúsculas, en minúsculas y con la primera letra en mayúscula.

**Ejercicio 4.5** — Invierte el texto `"abcdef"`.

**Ejercicio 4.6** — Dado `"   hola mundo   "`, elimina los espacios de los extremos y muestra cuántos caracteres tiene el resultado.

**Ejercicio 4.7** — Reemplaza en `"Me gusta el verde"` la palabra `verde` por `azul`.

**Ejercicio 4.8** — Cuenta cuántas veces aparece la letra `"a"` en `"banana"`.

**Ejercicio 4.9** — Con `nombre = "Carla"` y `edad = 30`, muestra con un f-string: `Carla tiene 30 años`.

**Ejercicio 4.10** — Con `precio = 12.3456`, muestra el precio con 2 decimales usando f-string.

**Ejercicio 4.11** — Divide `"manzana,pera,uva"` en una lista de frutas y muéstrala.

**Ejercicio 4.12** — Une la lista `["2025", "03", "09"]` con `/` como separador.

**Ejercicio 4.13** — Comprueba si `"anilina"` es un palíndromo.

**Ejercicio 4.14** — Dado `"12345"`, muestra si son todos dígitos y luego conviértelo a entero y súmale 1.

**Ejercicio 4.15** — Con `a = 7` y `b = 3`, muestra con un solo f-string: `7 x 3 = 21`.

**Ejercicio 4.16** — Con `correo = "ana@mail.com"`, muestra solo la parte antes de `@` (usa `split`).

### ✅ Soluciones del Módulo 4

**4.1**

```python
nombre = "Ana"
print(len(nombre))   # 3
```

**4.2**

```python
palabra = "elefante"
print(palabra[0])    # e
print(palabra[-1])   # e
print(palabra[2])    # e
```

**4.3**

```python
palabra = "murciélago"
print(palabra[:3])    # mur
print(palabra[-3:])   # ago
```

**4.4**

```python
t = "python"
print(t.upper(), t.lower(), t.capitalize())   # PYTHON python Python
```

**4.5**

```python
print("abcdef"[::-1])   # fedcba
```

**4.6**

```python
t = "   hola mundo   ".strip()
print(t, len(t))   # hola mundo 10
```

**4.7**

```python
print("Me gusta el verde".replace("verde", "azul"))
```

**4.8**

```python
print("banana".count("a"))   # 3
```

**4.9**

```python
nombre = "Carla"
edad = 30
print(f"{nombre} tiene {edad} años")
```

**4.10**

```python
precio = 12.3456
print(f"{precio:.2f}")   # 12.35
```

**4.11**

```python
frutas = "manzana,pera,uva".split(",")
print(frutas)   # ['manzana', 'pera', 'uva']
```

**4.12**

```python
print("/".join(["2025", "03", "09"]))   # 2025/03/09
```

**4.13**

```python
p = "anilina"
print(p == p[::-1])   # True
```

**4.14**

```python
t = "12345"
print(t.isdigit())      # True
print(int(t) + 1)       # 12346
```

**4.15**

```python
a = 7
b = 3
print(f"{a} x {b} = {a * b}")
```

**4.16**

```python
correo = "ana@mail.com"
print(correo.split("@")[0])   # ana
```

---

# MÓDULO 5 — Entrada de datos

Hasta ahora, tus programas "ya sabían" todos los datos. Con `input()` el programa **le pregunta al usuario**.

## 5.1 `input()`

```python
nombre = input("¿Cómo te llamas? ")
print("Hola,", nombre)
```

Cuando ejecutes esto:

```text
¿Cómo te llamas? Ana        ← esto lo escribes tú
Hola, Ana
```

- Lo que pones entre paréntesis es el **mensaje** que se muestra (se llama *prompt*).
- El programa se **detiene** y espera a que escribas y pulses Enter.
- Lo que escribes se **guarda** en la variable de la izquierda.

Dejar un espacio al final del mensaje (`"... "`) hace que se vea mejor.

## 5.2 ⚠️ `input()` siempre devuelve texto

Lo que escribe el usuario **siempre es un `str`**, aunque sean números.

```python
edad = input("¿Qué edad tienes? ")
print(type(edad))   # <class 'str'>  ← ¡texto!
```

Si escribes `15`, `edad` es `"15"` (texto), no el número 15. Por eso esto falla:

```python
edad = input("Edad: ")
print(edad + 1)   # ❌ TypeError: no puedes sumar texto y número
```

**Solución: convertir.**

```python
edad = int(input("Edad: "))   # ahora es un número
print(edad + 1)               # ✔️
```

Se lee de adentro hacia afuera: primero `input(...)` devuelve texto → `int(...)` lo convierte a entero → se guarda en `edad`.

También puedes hacerlo en dos pasos (más claro al principio):

```python
texto = input("Edad: ")
edad = int(texto)
print(edad + 1)
```

### ¿`int` o `float`?

- Para números **enteros** (edad, cantidad): `int(...)`.
- Para números **con decimales** (precio, altura): `float(...)`.

```python
precio = float(input("Precio: "))
cantidad = int(input("Cantidad: "))
print("Total:", precio * cantidad)
```

## 5.3 Varios `input` en un programa

```python
nombre = input("Nombre: ")
apellido = input("Apellido: ")
edad = int(input("Edad: "))

print(f"{nombre} {apellido} tiene {edad} años")
print(f"El año que viene tendrá {edad + 1}")
```

## 5.4 Leer varios datos en una sola línea

El usuario escribe `3 4` y tú lo separas:

```python
a, b = input("Dos números separados por espacio: ").split()
a = int(a)
b = int(b)
print("Suma:", a + b)
```

Forma abreviada (la verás mucho):

```python
a, b = map(int, input("Dos números: ").split())
print(a * b)
```

(No te preocupes por `map` aún; lo veremos en el Módulo 14.)

## 5.5 Limpiar la entrada

Los usuarios escriben cosas raras: espacios de más, mayúsculas... Normalízalo:

```python
respuesta = input("¿Continuar? (si/no) ").strip().lower()
print("Elegiste:", respuesta)
```

Si escriben `"  SI "`, queda `"si"`. Así luego comparas fácilmente.

## 5.6 Comprobar antes de convertir

Para no tener errores si el usuario escribe letras:

```python
texto = input("Escribe un número: ")
print("¿Son solo dígitos?", texto.isdigit())
```

(Más adelante, con `if` y `try/except`, aprenderás a manejar esto bien.)

## 5.7 Ejemplos completos

**Ejemplo A: calculadora de área de un rectángulo**

```python
base = float(input("Base: "))
altura = float(input("Altura: "))
area = base * altura
print(f"El área es {area}")
```

**Ejemplo B: convertir euros a dólares**

```python
euros = float(input("¿Cuántos euros? "))
tasa = 1.08
dolares = euros * tasa
print(f"{euros} euros son {dolares:.2f} dólares")
```

**Ejemplo C: edad en el futuro**

```python
nombre = input("Nombre: ")
edad = int(input("Edad: "))
anios = int(input("¿Dentro de cuántos años? "))
print(f"Dentro de {anios} años, {nombre} tendrá {edad + anios} años")
```

**Ejemplo D: dividir la cuenta**

```python
cuenta = float(input("Total de la cuenta: "))
personas = int(input("Número de personas: "))
cada_uno = cuenta / personas
print(f"Cada uno paga {cada_uno:.2f}")
```

## 5.8 Resumen del Módulo 5

- `input("mensaje")` pide un dato y lo devuelve **como texto**.
- Convierte con `int()` o `float()` si necesitas un número.
- `.strip().lower()` limpia respuestas de texto.
- Cada dato que el usuario da se guarda en una variable.

## 5.9 🎯 Ejercicios del Módulo 5

> **Nota:** para probar estos ejercicios ejecuta el programa y escribe los datos cuando te los pida.

**Ejercicio 5.1** — Pide el nombre y muestra `Hola, <nombre>`.

**Ejercicio 5.2** — Pide dos números y muestra su suma.

**Ejercicio 5.3** — Pide un número y muestra su doble y su triple.

**Ejercicio 5.4** — Pide la base y la altura de un triángulo y muestra su área (base × altura / 2).

**Ejercicio 5.5** — Pide una temperatura en Celsius y muestra los grados Fahrenheit (F = C × 9/5 + 32).

**Ejercicio 5.6** — Pide el precio de un producto y cuántas unidades se compran. Muestra el total.

**Ejercicio 5.7** — Pide el año de nacimiento y el año actual. Muestra la edad aproximada.

**Ejercicio 5.8** — Pide una palabra y muestra cuántas letras tiene y la palabra en mayúsculas.

**Ejercicio 5.9** — Pide un número entero y muestra el cuadrado y la raíz cuadrada (usa `** 0.5`).

**Ejercicio 5.10** — Pide el total de una cuenta y el número de personas. Muestra cuánto paga cada uno con 2 decimales.

**Ejercicio 5.11** — Pide minutos y muestra cuántas horas y minutos son (por ejemplo, 135 → `2 h 15 min`).

**Ejercicio 5.12** — Pide nombre y ciudad y muestra una frase: `Ana vive en Madrid`.

**Ejercicio 5.13** — Pide tres notas y muestra el promedio con un decimal.

**Ejercicio 5.14** — Pide una palabra y muestra la palabra al revés.

### ✅ Soluciones del Módulo 5

**5.1**

```python
nombre = input("Nombre: ")
print("Hola,", nombre)
```

**5.2**

```python
a = int(input("Primer número: "))
b = int(input("Segundo número: "))
print("Suma:", a + b)
```

**5.3**

```python
n = int(input("Número: "))
print("Doble:", n * 2)
print("Triple:", n * 3)
```

**5.4**

```python
base = float(input("Base: "))
altura = float(input("Altura: "))
print("Área:", base * altura / 2)
```

**5.5**

```python
c = float(input("Grados Celsius: "))
print(f"{c * 9 / 5 + 32} °F")
```

**5.6**

```python
precio = float(input("Precio: "))
unidades = int(input("Unidades: "))
print("Total:", precio * unidades)
```

**5.7**

```python
nacimiento = int(input("Año de nacimiento: "))
actual = int(input("Año actual: "))
print("Edad aproximada:", actual - nacimiento)
```

**5.8**

```python
palabra = input("Palabra: ")
print(len(palabra), palabra.upper())
```

**5.9**

```python
n = int(input("Número: "))
print("Cuadrado:", n ** 2)
print("Raíz:", n ** 0.5)
```

**5.10**

```python
total = float(input("Total: "))
personas = int(input("Personas: "))
print(f"Cada uno paga {total / personas:.2f}")
```

**5.11**

```python
minutos = int(input("Minutos: "))
print(f"{minutos // 60} h {minutos % 60} min")
```

**5.12**

```python
nombre = input("Nombre: ")
ciudad = input("Ciudad: ")
print(f"{nombre} vive en {ciudad}")
```

**5.13**

```python
n1 = float(input("Nota 1: "))
n2 = float(input("Nota 2: "))
n3 = float(input("Nota 3: "))
print(f"Promedio: {(n1 + n2 + n3) / 3:.1f}")
```

**5.14**

```python
p = input("Palabra: ")
print(p[::-1])
```

---

# MÓDULO 6 — Condicionales

Hasta ahora todo tu código se ejecutaba de arriba a abajo, sin decisiones. Los **condicionales** permiten que el programa **elija** qué hacer según la situación.

En la vida diaria: *"**Si** llueve, llevo paraguas. **Si no**, llevo gafas de sol."*

## 6.1 `if`: si pasa algo, hazlo

```python
edad = 20

if edad >= 18:
    print("Eres mayor de edad")
```

Fíjate en los 3 detalles:

1. Después de la condición va **dos puntos** `:`.
2. Las líneas que dependen del `if` van **indentadas** (con 4 espacios).
3. Si la condición es `False`, esas líneas se saltan.

```python
edad = 15

if edad >= 18:
    print("Eres mayor de edad")

print("Fin del programa")   # esto se ejecuta siempre
```

Salida:

```text
Fin del programa
```

> ⚠️ **La indentación es obligatoria en Python.** Usa 4 espacios (o la tecla Tab en tu editor). Todas las líneas del mismo bloque deben tener la **misma** indentación.

### Un `if` con varias líneas dentro

```python
temperatura = 35

if temperatura > 30:
    print("Hace calor")
    print("Bebe agua")
    print("Usa protector solar")

print("Que tengas buen día")
```

Las tres primeras solo se ejecutan si hace calor; la última siempre.

## 6.2 `if` / `else`: o esto, o lo otro

```python
edad = 15

if edad >= 18:
    print("Mayor de edad")
else:
    print("Menor de edad")
```

Salida: `Menor de edad`.

Siempre se ejecuta **exactamente uno** de los dos bloques.

Más ejemplos:

```python
numero = 7

if numero % 2 == 0:
    print("Es par")
else:
    print("Es impar")
```

```python
contrasena = "1234"

if contrasena == "1234":
    print("Acceso concedido")
else:
    print("Acceso denegado")
```

```python
nota = 4.5

if nota >= 5:
    print("Aprobado")
else:
    print("Suspenso")
```

## 6.3 `if` / `elif` / `else`: varias opciones

`elif` significa "si no, y si...". Python revisa de arriba abajo y ejecuta **el primero** que sea verdadero.

```python
nota = 8

if nota >= 9:
    print("Sobresaliente")
elif nota >= 7:
    print("Notable")
elif nota >= 5:
    print("Aprobado")
else:
    print("Suspenso")
```

Salida: `Notable`.

**¿Qué pasa por dentro con `nota = 8`?**

1. ¿`8 >= 9`? No → paso al siguiente.
2. ¿`8 >= 7`? Sí → ejecuta "Notable" y **se salta todo lo demás**.

⚠️ **El orden importa.** Si hubieras escrito primero `nota >= 5`, un 9 diría "Aprobado" y nunca llegaría a "Sobresaliente".

Otro ejemplo: el semáforo.

```python
color = "rojo"

if color == "verde":
    print("Avanza")
elif color == "amarillo":
    print("Precaución")
elif color == "rojo":
    print("Detente")
else:
    print("Color desconocido")
```

Otro: el signo de un número.

```python
n = -3

if n > 0:
    print("Positivo")
elif n < 0:
    print("Negativo")
else:
    print("Cero")
```

## 6.4 Condiciones compuestas con `and`, `or`, `not`

```python
edad = 25
tiene_entrada = True

if edad >= 18 and tiene_entrada:
    print("Puedes pasar")
else:
    print("No puedes pasar")
```

```python
dia = "sábado"

if dia == "sábado" or dia == "domingo":
    print("Fin de semana")
else:
    print("Día laboral")
```

```python
llueve = False

if not llueve:
    print("Vamos al parque")
```

Rangos:

```python
edad = 30

if 18 <= edad <= 65:
    print("Edad laboral")
```

Usando `in` (más corto cuando hay muchas opciones):

```python
dia = "domingo"

if dia in ("sábado", "domingo"):
    print("Fin de semana")

letra = "e"
if letra in "aeiou":
    print("Es vocal")
```

## 6.5 `if` anidados (uno dentro de otro)

```python
edad = 20
tiene_carnet = True

if edad >= 18:
    if tiene_carnet:
        print("Puedes conducir")
    else:
        print("Necesitas sacarte el carnet")
else:
    print("Eres menor de edad")
```

Muchas veces se puede simplificar con `and`:

```python
if edad >= 18 and tiene_carnet:
    print("Puedes conducir")
```

## 6.6 Verdadero y falso "implícito" (truthiness)

En un `if` no hace falta comparar con `True`:

```python
nombre = ""

if nombre:                 # un texto vacío cuenta como False
    print("Hola,", nombre)
else:
    print("No escribiste nombre")
```

```python
lista = [1, 2, 3]
if lista:                  # una lista con elementos cuenta como True
    print("La lista tiene elementos")
```

```python
activo = True
if activo:                 # mejor que "if activo == True:"
    print("Activo")
```

## 6.7 Operador ternario: un `if` en una línea

```python
edad = 20
estado = "adulto" if edad >= 18 else "menor"
print(estado)   # adulto
```

Forma: `valor_si_cierto if condicion else valor_si_falso`.

Otros ejemplos:

```python
n = 7
print("par" if n % 2 == 0 else "impar")      # impar

a, b = 4, 9
mayor = a if a > b else b
print(mayor)                                  # 9
```

## 6.8 `match` / `case` (Python 3.10 o superior)

Cuando comparas una variable con muchos valores concretos:

```python
dia = 3

match dia:
    case 1:
        print("Lunes")
    case 2:
        print("Martes")
    case 3:
        print("Miércoles")
    case _:
        print("Otro día")      # _ significa "cualquier otro"
```

Se pueden agrupar opciones con `|`:

```python
fruta = "fresa"

match fruta:
    case "manzana" | "pera":
        print("Fruta de árbol")
    case "fresa" | "mora":
        print("Frutos rojos")
    case _:
        print("No la conozco")
```

> 💡 Si tu Python es más antiguo que 3.10, usa `if/elif/else`: hace lo mismo.

## 6.9 `pass`: bloque vacío

Un bloque no puede quedar vacío. Si aún no sabes qué poner, usa `pass`:

```python
if True:
    pass   # "no hacer nada por ahora"
```

## 6.10 Ejemplos completos

**Ejemplo A: mayor de dos números**

```python
a = int(input("Primer número: "))
b = int(input("Segundo número: "))

if a > b:
    print("El mayor es", a)
elif b > a:
    print("El mayor es", b)
else:
    print("Son iguales")
```

**Ejemplo B: descuento según la compra**

```python
compra = float(input("Total de la compra: "))

if compra >= 100:
    descuento = 0.10
elif compra >= 50:
    descuento = 0.05
else:
    descuento = 0

total = compra * (1 - descuento)
print(f"Pagas {total:.2f}")
```

**Ejemplo C: año bisiesto**

Un año es bisiesto si es divisible entre 4, excepto los divisibles entre 100 que no lo son entre 400.

```python
anio = int(input("Año: "))

if (anio % 4 == 0 and anio % 100 != 0) or anio % 400 == 0:
    print("Bisiesto")
else:
    print("No bisiesto")
```

**Ejemplo D: contraseña**

```python
clave = input("Clave: ")

if len(clave) < 6:
    print("Muy corta")
elif clave.isdigit():
    print("No puede ser solo números")
else:
    print("Clave aceptable")
```

## 6.11 ⚠️ Errores comunes

```python
if edad = 18:        # ❌ SyntaxError: usa == para comparar
    ...

if edad >= 18        # ❌ falta el ":"
    ...

if edad >= 18:
print("hola")        # ❌ IndentationError: falta indentar

if x > 5:
    print("a")
  print("b")         # ❌ indentación inconsistente
```

## 6.12 Resumen del Módulo 6

- `if` ejecuta un bloque solo si la condición es verdadera.
- `else` cubre "todo lo demás". `elif` añade más condiciones.
- Se revisa de arriba hacia abajo; se ejecuta solo la primera que cumple.
- La **indentación** (4 espacios) y los **dos puntos** son obligatorios.
- `==` compara; `=` guarda.
- Ternario: `a if cond else b`.
- `match/case` para muchos valores fijos.

## 6.13 🎯 Ejercicios del Módulo 6

**Ejercicio 6.1** — Pide un número y di si es positivo, negativo o cero.

**Ejercicio 6.2** — Pide un número y di si es par o impar.

**Ejercicio 6.3** — Pide la edad y di si la persona es mayor de edad (18 o más).

**Ejercicio 6.4** — Pide una nota (0–10) y muestra: `Suspenso` (<5), `Aprobado` (5–6.9), `Notable` (7–8.9), `Sobresaliente` (9–10).

**Ejercicio 6.5** — Pide dos números y muestra cuál es el mayor (o que son iguales).

**Ejercicio 6.6** — Pide una letra y di si es vocal o no (minúscula o mayúscula).

**Ejercicio 6.7** — Pide una contraseña y di `Acceso permitido` si es igual a `"python123"`; si no, `Acceso denegado`.

**Ejercicio 6.8** — Pide un número del 1 al 7 y muestra el día de la semana (usa `if/elif` o `match`).

**Ejercicio 6.9** — Pide tres números y muestra el mayor.

**Ejercicio 6.10** — Pide la temperatura y muestra: `Frío` (menos de 15), `Agradable` (15 a 25), `Calor` (más de 25).

**Ejercicio 6.11** — Pide un año y di si es bisiesto.

**Ejercicio 6.12** — Pide la edad: si es menor de 12 `Niño`, de 12 a 17 `Adolescente`, de 18 a 64 `Adulto`, desde 65 `Mayor`.

**Ejercicio 6.13** — Pide un número y di si es múltiplo de 3, de 5, de ambos o de ninguno.

**Ejercicio 6.14** — Calcula el precio de una entrada: menores de 5 años gratis, de 5 a 12 años 5 €, de 13 a 64 años 10 €, 65 o más 6 €.

**Ejercicio 6.15** — Pide un texto y di si está vacío o no, usando solo `if texto:`.

**Ejercicio 6.16** — Usa el operador ternario para mostrar `"Aprobado"` o `"Suspenso"` según una nota guardada en una variable.

### ✅ Soluciones del Módulo 6

**6.1**

```python
n = float(input("Número: "))
if n > 0:
    print("Positivo")
elif n < 0:
    print("Negativo")
else:
    print("Cero")
```

**6.2**

```python
n = int(input("Número: "))
if n % 2 == 0:
    print("Par")
else:
    print("Impar")
```

**6.3**

```python
edad = int(input("Edad: "))
if edad >= 18:
    print("Mayor de edad")
else:
    print("Menor de edad")
```

**6.4**

```python
nota = float(input("Nota: "))
if nota < 5:
    print("Suspenso")
elif nota < 7:
    print("Aprobado")
elif nota < 9:
    print("Notable")
else:
    print("Sobresaliente")
```

**6.5**

```python
a = float(input("A: "))
b = float(input("B: "))
if a > b:
    print("Mayor:", a)
elif b > a:
    print("Mayor:", b)
else:
    print("Son iguales")
```

**6.6**

```python
letra = input("Letra: ").lower()
if letra in "aeiou":
    print("Vocal")
else:
    print("No es vocal")
```

**6.7**

```python
clave = input("Contraseña: ")
if clave == "python123":
    print("Acceso permitido")
else:
    print("Acceso denegado")
```

**6.8**

```python
n = int(input("Número (1-7): "))
match n:
    case 1:
        print("Lunes")
    case 2:
        print("Martes")
    case 3:
        print("Miércoles")
    case 4:
        print("Jueves")
    case 5:
        print("Viernes")
    case 6:
        print("Sábado")
    case 7:
        print("Domingo")
    case _:
        print("Número fuera de rango")
```

**6.9**

```python
a = float(input("A: "))
b = float(input("B: "))
c = float(input("C: "))
if a >= b and a >= c:
    print("Mayor:", a)
elif b >= a and b >= c:
    print("Mayor:", b)
else:
    print("Mayor:", c)
```

**6.10**

```python
t = float(input("Temperatura: "))
if t < 15:
    print("Frío")
elif t <= 25:
    print("Agradable")
else:
    print("Calor")
```

**6.11**

```python
anio = int(input("Año: "))
if (anio % 4 == 0 and anio % 100 != 0) or anio % 400 == 0:
    print("Bisiesto")
else:
    print("No bisiesto")
```

**6.12**

```python
edad = int(input("Edad: "))
if edad < 12:
    print("Niño")
elif edad < 18:
    print("Adolescente")
elif edad < 65:
    print("Adulto")
else:
    print("Mayor")
```

**6.13**

```python
n = int(input("Número: "))
if n % 3 == 0 and n % 5 == 0:
    print("Múltiplo de ambos")
elif n % 3 == 0:
    print("Múltiplo de 3")
elif n % 5 == 0:
    print("Múltiplo de 5")
else:
    print("De ninguno")
```

**6.14**

```python
edad = int(input("Edad: "))
if edad < 5:
    precio = 0
elif edad <= 12:
    precio = 5
elif edad <= 64:
    precio = 10
else:
    precio = 6
print(f"Precio de la entrada: {precio} €")
```

**6.15**

```python
texto = input("Escribe algo: ")
if texto:
    print("Escribiste algo")
else:
    print("Está vacío")
```

**6.16**

```python
nota = 6
print("Aprobado" if nota >= 5 else "Suspenso")
```

---

# MÓDULO 7 — El bucle `while`

Un **bucle** repite instrucciones. Imagina que tu profesor te dice: *"Escribe 100 veces: no hablaré en clase"*. En vez de escribirlo 100 veces, programas un bucle.

## 7.1 `while`: repetir MIENTRAS algo sea cierto

```python
contador = 1

while contador <= 5:
    print("Vuelta", contador)
    contador += 1

print("Fin")
```

Salida:

```text
Vuelta 1
Vuelta 2
Vuelta 3
Vuelta 4
Vuelta 5
Fin
```

**Cómo funciona paso a paso:**

1. `contador` vale 1. ¿`1 <= 5`? Sí → entra, muestra, `contador` pasa a 2.
2. ¿`2 <= 5`? Sí → entra, muestra, pasa a 3.
3. ... así hasta que `contador` vale 6.
4. ¿`6 <= 5`? **No** → el bucle termina, y sigue con `print("Fin")`.

**Las 3 piezas de un `while`:**

```python
contador = 1               # 1) inicializar
while contador <= 5:       # 2) condición
    print(contador)
    contador += 1          # 3) actualizar (¡muy importante!)
```

### La misma idea con "recorrido por una escalera"

Imagina que subes una escalera de 5 escalones. Empiezas en el 1 (inicio). Mientras no hayas llegado al 5 (condición), subes uno (actualización). Si olvidaras subir, te quedarías en el mismo escalón para siempre.

## 7.2 ⚠️ Bucle infinito

Si la condición **nunca** se vuelve falsa, el programa no termina nunca:

```python
contador = 1
while contador <= 5:
    print(contador)
    # ❌ se nos olvidó contador += 1  → imprime 1 para siempre
```

**Si te pasa:** pulsa `Ctrl + C` en la terminal para detener el programa.

> 💡 Cuando escribas un `while`, pregúntate siempre: **"¿qué cambia dentro del bucle para que algún día termine?"**

## 7.3 Variantes del conteo

**Contar hacia atrás:**

```python
n = 5
while n > 0:
    print(n)
    n -= 1
print("¡Despegue!")
```

```text
5
4
3
2
1
¡Despegue!
```

**Contar de 2 en 2:**

```python
n = 0
while n <= 10:
    print(n)
    n += 2
```

**Tabla de multiplicar:**

```python
i = 1
while i <= 10:
    print(f"7 x {i} = {7 * i}")
    i += 1
```

## 7.4 Acumuladores y contadores

Un **acumulador** va guardando un resultado que crece (suma, producto...). Un **contador** cuenta cuántas veces pasa algo.

**Sumar los números del 1 al 10:**

```python
suma = 0        # acumulador empieza en 0
n = 1
while n <= 10:
    suma += n   # acumulo
    n += 1
print("Suma:", suma)   # 55
```

**Factorial de 5** (5 × 4 × 3 × 2 × 1):

```python
resultado = 1   # el producto empieza en 1 (no en 0)
n = 5
while n > 1:
    resultado *= n
    n -= 1
print(resultado)   # 120
```

**Contar cuántos dígitos tiene un número:**

```python
numero = 12345
digitos = 0
while numero > 0:
    numero //= 10     # quita el último dígito
    digitos += 1
print(digitos)   # 5
```

## 7.5 Bucles controlados por el usuario

Muy usados: repetir hasta que el usuario decida parar.

```python
respuesta = ""

while respuesta != "salir":
    respuesta = input("Escribe algo (o 'salir'): ")
    print("Escribiste:", respuesta)

print("Adiós")
```

**Validar una entrada** (repetir hasta que sea correcta):

```python
edad = int(input("Edad (0-120): "))

while edad < 0 or edad > 120:
    print("Edad no válida")
    edad = int(input("Edad (0-120): "))

print("Edad guardada:", edad)
```

**Adivinar un número:**

```python
secreto = 7
intento = 0

while intento != secreto:
    intento = int(input("Adivina el número: "))

print("¡Correcto!")
```

## 7.6 `break`: salir del bucle YA

```python
while True:                          # "mientras sea verdadero" = infinito a propósito
    texto = input("Escribe 'fin' para terminar: ")
    if texto == "fin":
        break                        # sale del bucle inmediatamente
    print("Dijiste:", texto)

print("Terminado")
```

`while True` + `break` es un patrón muy común cuando **no sabes de antemano** cuántas veces repetirás.

## 7.7 `continue`: saltar a la siguiente vuelta

`continue` se salta lo que queda de **esta** vuelta y pasa a la siguiente.

```python
n = 0
while n < 10:
    n += 1
    if n % 2 == 0:
        continue          # si es par, salta el print
    print(n)
```

```text
1
3
5
7
9
```

## 7.8 `while ... else` (poco común)

El `else` se ejecuta si el bucle terminó **sin** `break`.

```python
n = 1
while n <= 3:
    print(n)
    n += 1
else:
    print("Terminó normalmente")
```

## 7.9 Menús con `while`

Un programa típico: mostrar un menú hasta que el usuario elija salir.

```python
opcion = ""

while opcion != "3":
    print("\n--- MENÚ ---")
    print("1. Saludar")
    print("2. Despedirse")
    print("3. Salir")
    opcion = input("Elige una opción: ")

    if opcion == "1":
        print("¡Hola!")
    elif opcion == "2":
        print("¡Adiós!")
    elif opcion == "3":
        print("Saliendo...")
    else:
        print("Opción no válida")
```

## 7.10 Ejemplos completos

**Ejemplo A: suma hasta que escriban 0**

```python
total = 0
numero = int(input("Número (0 para terminar): "))

while numero != 0:
    total += numero
    numero = int(input("Número (0 para terminar): "))

print("Total:", total)
```

**Ejemplo B: tres intentos para la clave**

```python
intentos = 3

while intentos > 0:
    clave = input("Clave: ")
    if clave == "abc":
        print("Bienvenido")
        break
    intentos -= 1
    print(f"Incorrecta. Te quedan {intentos} intentos")
else:
    print("Cuenta bloqueada")
```

**Ejemplo C: promedio de las notas que escriba el usuario**

```python
suma = 0
cantidad = 0

nota = float(input("Nota (-1 para terminar): "))
while nota != -1:
    suma += nota
    cantidad += 1
    nota = float(input("Nota (-1 para terminar): "))

if cantidad > 0:
    print("Promedio:", suma / cantidad)
else:
    print("No hay notas")
```

## 7.11 Resumen del Módulo 7

- `while condición:` repite mientras la condición sea `True`.
- Necesitas: **inicializar**, **condición**, **actualizar**.
- Cuidado con los bucles infinitos (`Ctrl + C` para parar).
- `break` sale del bucle; `continue` salta a la siguiente vuelta.
- Acumulador: suma/producto que crece. Contador: cuenta eventos.

## 7.12 🎯 Ejercicios del Módulo 7

**Ejercicio 7.1** — Muestra los números del 1 al 10.

**Ejercicio 7.2** — Muestra los números del 10 al 1 (cuenta atrás).

**Ejercicio 7.3** — Muestra los números pares del 2 al 20.

**Ejercicio 7.4** — Muestra la tabla de multiplicar del número que elija el usuario.

**Ejercicio 7.5** — Calcula la suma de los números del 1 al 100.

**Ejercicio 7.6** — Pide números al usuario hasta que escriba `0` y muestra cuántos escribió (sin contar el 0).

**Ejercicio 7.7** — Pide una contraseña hasta que el usuario escriba la correcta (`"python"`).

**Ejercicio 7.8** — Pide números hasta que escriba `0`; muestra la suma y el mayor número.

**Ejercicio 7.9** — Calcula el factorial de un número que pida al usuario.

**Ejercicio 7.10** — Muestra los 10 primeros múltiplos de 3.

**Ejercicio 7.11** — Pide una edad hasta que sea un valor entre 0 y 120.

**Ejercicio 7.12** — Cuenta cuántos dígitos tiene un número entero positivo que escriba el usuario.

**Ejercicio 7.13** — Muestra un menú con 3 opciones (1: sumar 1 al contador, 2: ver contador, 3: salir). Repite hasta salir.

**Ejercicio 7.14** — Pide un número y muestra su suma de dígitos (por ejemplo, 123 → 6).

**Ejercicio 7.15** — Duplica un valor inicial de 1 una y otra vez hasta superar 1000. Muestra cada valor.

**Ejercicio 7.16** — Juego: el programa tiene un número secreto (por ejemplo, 5). Pide al usuario adivinar y dile si el intento es mayor o menor, hasta acertar.

### ✅ Soluciones del Módulo 7

**7.1**

```python
n = 1
while n <= 10:
    print(n)
    n += 1
```

**7.2**

```python
n = 10
while n >= 1:
    print(n)
    n -= 1
```

**7.3**

```python
n = 2
while n <= 20:
    print(n)
    n += 2
```

**7.4**

```python
num = int(input("Tabla del: "))
i = 1
while i <= 10:
    print(f"{num} x {i} = {num * i}")
    i += 1
```

**7.5**

```python
suma = 0
n = 1
while n <= 100:
    suma += n
    n += 1
print(suma)   # 5050
```

**7.6**

```python
cantidad = 0
n = int(input("Número (0 para terminar): "))
while n != 0:
    cantidad += 1
    n = int(input("Número (0 para terminar): "))
print("Escribiste", cantidad, "números")
```

**7.7**

```python
clave = ""
while clave != "python":
    clave = input("Contraseña: ")
print("Acceso permitido")
```

**7.8**

```python
suma = 0
mayor = None
n = int(input("Número (0 para terminar): "))
while n != 0:
    suma += n
    if mayor is None or n > mayor:
        mayor = n
    n = int(input("Número (0 para terminar): "))
print("Suma:", suma)
print("Mayor:", mayor)
```

**7.9**

```python
n = int(input("Número: "))
resultado = 1
while n > 1:
    resultado *= n
    n -= 1
print("Factorial:", resultado)
```

**7.10**

```python
i = 1
while i <= 10:
    print(3 * i)
    i += 1
```

**7.11**

```python
edad = int(input("Edad: "))
while edad < 0 or edad > 120:
    print("Edad no válida")
    edad = int(input("Edad: "))
print("Edad correcta:", edad)
```

**7.12**

```python
n = int(input("Número: "))
digitos = 0
if n == 0:
    digitos = 1
while n > 0:
    n //= 10
    digitos += 1
print("Dígitos:", digitos)
```

**7.13**

```python
contador = 0
opcion = ""
while opcion != "3":
    print("\n1. Sumar 1")
    print("2. Ver contador")
    print("3. Salir")
    opcion = input("Opción: ")
    if opcion == "1":
        contador += 1
    elif opcion == "2":
        print("Contador:", contador)
    elif opcion == "3":
        print("Adiós")
    else:
        print("Opción inválida")
```

**7.14**

```python
n = int(input("Número: "))
suma = 0
while n > 0:
    suma += n % 10     # último dígito
    n //= 10           # quitar último dígito
print("Suma de dígitos:", suma)
```

**7.15**

```python
v = 1
while v <= 1000:
    print(v)
    v *= 2
print("Pasó de 1000, ahora vale", v)
```

**7.16**

```python
secreto = 5
intento = 0
while intento != secreto:
    intento = int(input("Adivina: "))
    if intento < secreto:
        print("Es mayor")
    elif intento > secreto:
        print("Es menor")
print("¡Acertaste!")
```

---

# MÓDULO 8 — El bucle `for` y `range`

El `while` repite *mientras* algo sea cierto. El `for` repite **recorriendo cosas** (o un número fijo de veces). Es el bucle que más usarás.

## 8.1 `for` para recorrer un texto

```python
for letra in "Hola":
    print(letra)
```

```text
H
o
l
a
```

Se lee: **"para cada `letra` en `"Hola"`, haz esto"**. En cada vuelta, la variable `letra` vale un carácter distinto.

La variable (`letra`) la nombras tú; usa un nombre que tenga sentido:

```python
for caracter in "Python":
    print(caracter.upper())

for c in "abc":
    print(c * 3)    # aaa, bbb, ccc
```

## 8.2 `for` con `range()`: repetir N veces

`range(n)` genera los números `0, 1, 2, ..., n-1`.

```python
for i in range(5):
    print(i)
```

```text
0
1
2
3
4
```

⚠️ Empieza en **0** y **no incluye** el 5.

Si solo quieres repetir algo 3 veces (sin usar el número):

```python
for _ in range(3):
    print("Hola")
```

(El `_` es una convención: "no me importa esta variable".)

### Las tres formas de `range`

| Forma | Genera | Ejemplo |
|-------|--------|---------|
| `range(fin)` | de 0 a fin-1 | `range(4)` → 0,1,2,3 |
| `range(inicio, fin)` | de inicio a fin-1 | `range(2, 6)` → 2,3,4,5 |
| `range(inicio, fin, paso)` | saltando de `paso` en `paso` | `range(0, 10, 3)` → 0,3,6,9 |

```python
for i in range(1, 6):        # 1 al 5
    print(i)

for i in range(0, 11, 2):    # pares del 0 al 10
    print(i)

for i in range(10, 0, -1):   # cuenta atrás: 10 al 1
    print(i)

for i in range(5, 0, -2):    # 5, 3, 1
    print(i)
```

> 💡 Para que `range(a, b)` incluya el `b`, escribe `range(a, b + 1)`.

```python
for i in range(1, 11):       # del 1 al 10 (incluye el 10)
    print(i)
```

## 8.3 Ver `for` y `while` lado a lado

Mismo resultado, dos formas:

```python
# while
i = 1
while i <= 5:
    print(i)
    i += 1

# for
for i in range(1, 6):
    print(i)
```

El `for` es más corto porque **inicializa, comprueba y actualiza por ti**. Úsalo cuando sepas cuántas vueltas son o cuando recorras una colección. Usa `while` cuando dependa de una condición que no sabes cuándo se cumplirá.

## 8.4 Acumuladores con `for`

**Suma del 1 al 10:**

```python
suma = 0
for n in range(1, 11):
    suma += n
print(suma)   # 55
```

**Producto (factorial de 5):**

```python
f = 1
for n in range(1, 6):
    f *= n
print(f)   # 120
```

**Contar vocales de un texto:**

```python
frase = "murcielago"
vocales = 0
for letra in frase:
    if letra in "aeiou":
        vocales += 1
print(vocales)   # 5
```

**Construir un texto letra por letra (invertirlo):**

```python
palabra = "hola"
reves = ""
for letra in palabra:
    reves = letra + reves
print(reves)   # aloh
```

## 8.5 `break` y `continue` en `for`

Funcionan igual que en `while`.

```python
for n in range(1, 10):
    if n == 5:
        break          # sale cuando llega a 5
    print(n)           # 1 2 3 4
```

```python
for n in range(1, 8):
    if n % 2 == 0:
        continue       # se salta los pares
    print(n)           # 1 3 5 7
```

**`for ... else`:** el `else` corre si el bucle terminó **sin** `break`.

```python
numero = 7
for i in range(2, numero):
    if numero % i == 0:
        print("No es primo")
        break
else:
    print("Es primo")
```

## 8.6 Bucles anidados (un bucle dentro de otro)

Por cada vuelta del bucle externo, el interno da **todas** sus vueltas. Piensa en un reloj: por cada hora, pasan 60 minutos.

```python
for i in range(1, 4):
    for j in range(1, 4):
        print(i, j)
```

```text
1 1
1 2
1 3
2 1
2 2
2 3
3 1
3 2
3 3
```

**Todas las tablas de multiplicar:**

```python
for tabla in range(1, 4):
    print(f"Tabla del {tabla}")
    for n in range(1, 6):
        print(f"  {tabla} x {n} = {tabla * n}")
```

### Dibujar figuras con texto

**Un rectángulo de asteriscos:**

```python
for fila in range(3):
    print("*" * 5)
```

```text
*****
*****
*****
```

**Un triángulo:**

```python
for fila in range(1, 6):
    print("*" * fila)
```

```text
*
**
***
****
*****
```

**Triángulo con bucle anidado (la forma "larga"):**

```python
for fila in range(1, 5):
    for col in range(fila):
        print("*", end="")
    print()           # salto de línea al terminar la fila
```

**Triángulo de números:**

```python
for fila in range(1, 5):
    print(str(fila) * fila)
```

```text
1
22
333
4444
```

**Pirámide centrada:**

```python
altura = 4
for fila in range(1, altura + 1):
    espacios = " " * (altura - fila)
    estrellas = "*" * (2 * fila - 1)
    print(espacios + estrellas)
```

```text
   *
  ***
 *****
*******
```

## 8.7 `enumerate()`: índice y valor a la vez

Cuando necesitas **la posición** y **el elemento**:

```python
for i, letra in enumerate("abc"):
    print(i, letra)
```

```text
0 a
1 b
2 c
```

Empezar a contar desde 1:

```python
for i, letra in enumerate("abc", start=1):
    print(f"{i}. {letra}")
```

```text
1. a
2. b
3. c
```

## 8.8 `zip()`: recorrer dos cosas a la vez

```python
nombres = ["Ana", "Luis", "Eva"]
notas = [8, 6, 9]

for nombre, nota in zip(nombres, notas):
    print(f"{nombre} sacó {nota}")
```

```text
Ana sacó 8
Luis sacó 6
Eva sacó 9
```

(Las listas las verás a fondo en el siguiente módulo; aquí es solo un adelanto.)

## 8.9 Ejemplos completos

**Ejemplo A: tabla de multiplicar con formato**

```python
n = int(input("Tabla del: "))
for i in range(1, 11):
    print(f"{n} x {i:2} = {n * i:3}")
```

**Ejemplo B: media de N números**

```python
cantidad = int(input("¿Cuántos números? "))
suma = 0
for i in range(cantidad):
    n = float(input(f"Número {i + 1}: "))
    suma += n
print("Media:", suma / cantidad)
```

**Ejemplo C: contar letras específicas**

```python
texto = input("Texto: ").lower()
a_count = 0
for c in texto:
    if c == "a":
        a_count += 1
print("Hay", a_count, "letras 'a'")
```

**Ejemplo D: FizzBuzz (un clásico)**

```python
for n in range(1, 16):
    if n % 3 == 0 and n % 5 == 0:
        print("FizzBuzz")
    elif n % 3 == 0:
        print("Fizz")
    elif n % 5 == 0:
        print("Buzz")
    else:
        print(n)
```

## 8.10 Resumen del Módulo 8

- `for x in algo:` recorre elemento por elemento.
- `range(fin)`, `range(inicio, fin)`, `range(inicio, fin, paso)`; el `fin` **no** se incluye.
- `break`, `continue` y `else` funcionan como en `while`.
- Bucles anidados: el interno completa todas sus vueltas por cada vuelta del externo.
- `enumerate` da índice + valor; `zip` junta dos secuencias.

## 8.11 🎯 Ejercicios del Módulo 8

**Ejercicio 8.1** — Muestra los números del 1 al 10 con un `for`.

**Ejercicio 8.2** — Muestra los números del 10 al 1.

**Ejercicio 8.3** — Muestra los números impares del 1 al 19.

**Ejercicio 8.4** — Muestra cada letra de tu nombre en una línea distinta.

**Ejercicio 8.5** — Pide un número y muestra su tabla de multiplicar (del 1 al 10).

**Ejercicio 8.6** — Suma todos los números del 1 al 50.

**Ejercicio 8.7** — Pide un texto y cuenta cuántas vocales tiene.

**Ejercicio 8.8** — Muestra `Hola` cinco veces.

**Ejercicio 8.9** — Pide un número N y calcula el factorial de N con un `for`.

**Ejercicio 8.10** — Dibuja este triángulo con asteriscos (5 filas):

```text
*****
****
***
**
*
```

**Ejercicio 8.11** — Pide N y muestra los N primeros múltiplos de 5.

**Ejercicio 8.12** — Muestra los cuadrados de los números del 1 al 10 (`1 -> 1`, `2 -> 4`, ...).

**Ejercicio 8.13** — Pide un texto y muéstralo con un guion entre cada letra (`hola` → `h-o-l-a`) usando `for`.

**Ejercicio 8.14** — Imprime la tabla del 1 al 3 completa (cada tabla hasta ×5) con bucles anidados.

**Ejercicio 8.15** — Haz FizzBuzz del 1 al 20, pero para múltiplos de 2 muestra `Par` y para múltiplos de 3 muestra `Tres` (si es de ambos `Par-Tres`; en otro caso, el número).

**Ejercicio 8.16** — Usa `enumerate` para mostrar una lista de la compra numerada: `["pan", "leche", "huevos"]` → `1. pan`, `2. leche`...

**Ejercicio 8.17** — Pide un número y comprueba con un `for` si es primo.

**Ejercicio 8.18** — Dibuja un cuadrado hueco de 5×5 con asteriscos (solo el borde).

### ✅ Soluciones del Módulo 8

**8.1**

```python
for i in range(1, 11):
    print(i)
```

**8.2**

```python
for i in range(10, 0, -1):
    print(i)
```

**8.3**

```python
for i in range(1, 20, 2):
    print(i)
```

**8.4**

```python
for letra in "Ana":
    print(letra)
```

**8.5**

```python
n = int(input("Número: "))
for i in range(1, 11):
    print(f"{n} x {i} = {n * i}")
```

**8.6**

```python
suma = 0
for n in range(1, 51):
    suma += n
print(suma)   # 1275
```

**8.7**

```python
texto = input("Texto: ").lower()
vocales = 0
for c in texto:
    if c in "aeiouáéíóú":
        vocales += 1
print("Vocales:", vocales)
```

**8.8**

```python
for _ in range(5):
    print("Hola")
```

**8.9**

```python
n = int(input("N: "))
f = 1
for i in range(1, n + 1):
    f *= i
print(f)
```

**8.10**

```python
for fila in range(5, 0, -1):
    print("*" * fila)
```

**8.11**

```python
n = int(input("N: "))
for i in range(1, n + 1):
    print(5 * i)
```

**8.12**

```python
for i in range(1, 11):
    print(i, "->", i ** 2)
```

**8.13**

```python
texto = input("Texto: ")
resultado = ""
for c in texto:
    resultado += c + "-"
print(resultado[:-1])   # quitamos el último guion
```

**8.14**

```python
for tabla in range(1, 4):
    print(f"Tabla del {tabla}")
    for i in range(1, 6):
        print(f"  {tabla} x {i} = {tabla * i}")
```

**8.15**

```python
for n in range(1, 21):
    if n % 2 == 0 and n % 3 == 0:
        print("Par-Tres")
    elif n % 2 == 0:
        print("Par")
    elif n % 3 == 0:
        print("Tres")
    else:
        print(n)
```

**8.16**

```python
compra = ["pan", "leche", "huevos"]
for i, producto in enumerate(compra, start=1):
    print(f"{i}. {producto}")
```

**8.17**

```python
n = int(input("Número: "))
es_primo = n > 1
for i in range(2, n):
    if n % i == 0:
        es_primo = False
        break
print("Primo" if es_primo else "No primo")
```

**8.18**

```python
for fila in range(5):
    if fila == 0 or fila == 4:
        print("*" * 5)
    else:
        print("*" + " " * 3 + "*")
```

---

# MÓDULO 9 — Listas

Hasta ahora una variable guardaba **un** dato. Una **lista** guarda **muchos** datos, en orden, en una sola variable.

Piensa en una lista de la compra, una lista de invitados, o las notas de toda la clase.

## 9.1 Crear listas

Con corchetes `[ ]` y elementos separados por comas:

```python
numeros = [10, 20, 30, 40]
frutas = ["manzana", "pera", "uva"]
mezcla = [1, "hola", 3.5, True]   # puede mezclar tipos
vacia = []                         # lista vacía
```

```python
print(frutas)        # ['manzana', 'pera', 'uva']
print(type(frutas))  # <class 'list'>
print(len(frutas))   # 3
```

Otras formas de crear listas:

```python
a = list("hola")          # ['h', 'o', 'l', 'a']
b = list(range(5))        # [0, 1, 2, 3, 4]
c = [0] * 5               # [0, 0, 0, 0, 0]
d = "a b c".split()       # ['a', 'b', 'c']
```

## 9.2 Índices (¡igual que en los strings!)

```text
 lista:   "manzana"  "pera"  "uva"  "kiwi"
 índice:      0         1       2      3
 negativo:   -4        -3      -2     -1
```

```python
frutas = ["manzana", "pera", "uva", "kiwi"]
print(frutas[0])    # manzana
print(frutas[2])    # uva
print(frutas[-1])   # kiwi
print(frutas[-2])   # uva
```

## 9.3 Las listas SÍ se pueden modificar (mutables)

A diferencia de los strings:

```python
frutas = ["manzana", "pera", "uva"]
frutas[1] = "naranja"
print(frutas)   # ['manzana', 'naranja', 'uva']
```

```python
numeros = [1, 2, 3]
numeros[0] = numeros[0] + 10
print(numeros)   # [11, 2, 3]
```

## 9.4 Slicing en listas (igual que en strings)

```python
n = [10, 20, 30, 40, 50, 60]
print(n[1:4])    # [20, 30, 40]
print(n[:3])     # [10, 20, 30]
print(n[3:])     # [40, 50, 60]
print(n[::2])    # [10, 30, 50]
print(n[::-1])   # [60, 50, 40, 30, 20, 10]
print(n[-2:])    # [50, 60]
```

## 9.5 Añadir elementos

```python
lista = [1, 2, 3]

lista.append(4)          # añade AL FINAL
print(lista)             # [1, 2, 3, 4]

lista.insert(0, 99)      # inserta en la posición 0
print(lista)             # [99, 1, 2, 3, 4]

lista.extend([5, 6])     # añade VARIOS al final
print(lista)             # [99, 1, 2, 3, 4, 5, 6]
```

Diferencia importante:

```python
a = [1, 2]
a.append([3, 4])   # añade la lista como UN elemento
print(a)           # [1, 2, [3, 4]]

b = [1, 2]
b.extend([3, 4])   # añade cada elemento
print(b)           # [1, 2, 3, 4]
```

También se pueden unir con `+`:

```python
print([1, 2] + [3, 4])   # [1, 2, 3, 4]
print([0] * 3)           # [0, 0, 0]
```

## 9.6 Quitar elementos

```python
lista = ["a", "b", "c", "b", "d"]

lista.remove("b")        # quita la primera "b"
print(lista)             # ['a', 'c', 'b', 'd']

ultimo = lista.pop()     # quita y devuelve el último
print(ultimo)            # d
print(lista)             # ['a', 'c', 'b']

primero = lista.pop(0)   # quita y devuelve el de la posición 0
print(primero)           # a
print(lista)             # ['c', 'b']

del lista[0]             # borra por posición
print(lista)             # ['b']

lista.clear()            # vacía la lista
print(lista)             # []
```

## 9.7 Buscar y contar

```python
nums = [5, 3, 8, 3, 1]

print(3 in nums)          # True
print(9 in nums)          # False
print(nums.count(3))      # 2    (cuántas veces aparece)
print(nums.index(8))      # 2    (en qué posición está)
```

⚠️ `index` da error si el elemento no existe. Comprueba antes con `in`:

```python
if 9 in nums:
    print(nums.index(9))
else:
    print("No está")
```

## 9.8 Ordenar e invertir

```python
n = [5, 2, 9, 1]

n.sort()                 # ordena la propia lista (la modifica)
print(n)                 # [1, 2, 5, 9]

n.sort(reverse=True)     # de mayor a menor
print(n)                 # [9, 5, 2, 1]

n.reverse()              # invierte el orden actual
print(n)                 # [1, 2, 5, 9]
```

`sorted()` **no** modifica la original; devuelve una copia ordenada:

```python
original = [3, 1, 2]
ordenada = sorted(original)
print(original)   # [3, 1, 2]
print(ordenada)   # [1, 2, 3]
```

Con texto se ordena alfabéticamente:

```python
print(sorted(["pera", "uva", "manzana"]))   # ['manzana', 'pera', 'uva']
print(sorted(["pera", "uva", "kiwi"], key=len))  # ['uva', 'pera', 'kiwi'] (por longitud)
```

## 9.9 Funciones útiles con listas

```python
n = [4, 8, 1, 7]

print(len(n))    # 4
print(sum(n))    # 20
print(min(n))    # 1
print(max(n))    # 8
print(sum(n) / len(n))   # 5.0  (promedio)
```

## 9.10 Recorrer listas

**Por elemento:**

```python
frutas = ["manzana", "pera", "uva"]
for fruta in frutas:
    print(fruta)
```

**Por índice (cuando necesitas la posición):**

```python
for i in range(len(frutas)):
    print(i, frutas[i])
```

**Con `enumerate` (más elegante):**

```python
for i, fruta in enumerate(frutas):
    print(i, fruta)
```

**Modificar elementos mientras recorres (usa índices):**

```python
precios = [10, 20, 30]
for i in range(len(precios)):
    precios[i] = precios[i] * 2
print(precios)   # [20, 40, 60]
```

> ⚠️ Si en un `for x in lista:` haces `x = x * 2`, **no** cambias la lista: solo cambias la variable `x`.

## 9.11 Construir listas con bucles

```python
cuadrados = []
for n in range(1, 6):
    cuadrados.append(n ** 2)
print(cuadrados)   # [1, 4, 9, 16, 25]
```

```python
pares = []
for n in range(1, 11):
    if n % 2 == 0:
        pares.append(n)
print(pares)   # [2, 4, 6, 8, 10]
```

```python
# Pedir datos y guardarlos
notas = []
for i in range(3):
    n = float(input(f"Nota {i + 1}: "))
    notas.append(n)
print(notas)
print("Promedio:", sum(notas) / len(notas))
```

## 9.12 Copiar listas (¡cuidado!)

```python
a = [1, 2, 3]
b = a            # ❌ NO es una copia: ambas apuntan a la MISMA lista
b.append(4)
print(a)         # [1, 2, 3, 4]  ← ¡a también cambió!
```

Piensa en `b = a` como darle a la lista **un segundo nombre**, no una segunda lista.

Para copiar de verdad:

```python
a = [1, 2, 3]
b = a.copy()     # ✔️ copia real
c = a[:]         # ✔️ otra forma
d = list(a)      # ✔️ otra más

b.append(4)
print(a)   # [1, 2, 3]
print(b)   # [1, 2, 3, 4]
```

## 9.13 Listas anidadas (listas dentro de listas)

Sirven para representar tablas o matrices.

```python
tabla = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9],
]

print(tabla[0])       # [1, 2, 3]       (primera fila)
print(tabla[1][2])    # 6               (fila 1, columna 2)
print(tabla[2][0])    # 7
```

Recorrerla:

```python
for fila in tabla:
    for valor in fila:
        print(valor, end=" ")
    print()
```

```text
1 2 3 
4 5 6 
7 8 9 
```

Suma de cada fila:

```python
for fila in tabla:
    print(sum(fila))   # 6, 15, 24
```

## 9.14 Desempaquetar listas

```python
a, b, c = [10, 20, 30]
print(a, b, c)   # 10 20 30

primero, *resto = [1, 2, 3, 4]
print(primero)   # 1
print(resto)     # [2, 3, 4]
```

## 9.15 Ejemplos completos

**Ejemplo A: nota máxima, mínima y promedio**

```python
notas = [7, 9, 5, 8, 10]
print("Máxima:", max(notas))
print("Mínima:", min(notas))
print("Promedio:", sum(notas) / len(notas))
```

**Ejemplo B: quitar duplicados manteniendo el orden**

```python
datos = [1, 2, 2, 3, 1, 4]
sin_repetir = []
for d in datos:
    if d not in sin_repetir:
        sin_repetir.append(d)
print(sin_repetir)   # [1, 2, 3, 4]
```

**Ejemplo C: lista de la compra interactiva**

```python
compra = []
while True:
    producto = input("Producto (o 'fin'): ")
    if producto == "fin":
        break
    compra.append(producto)

print("Tu lista:")
for i, p in enumerate(compra, start=1):
    print(f"{i}. {p}")
```

**Ejemplo D: separar pares e impares**

```python
numeros = [1, 2, 3, 4, 5, 6, 7]
pares = []
impares = []
for n in numeros:
    if n % 2 == 0:
        pares.append(n)
    else:
        impares.append(n)
print(pares)     # [2, 4, 6]
print(impares)   # [1, 3, 5, 7]
```

## 9.16 Resumen del Módulo 9

- `[ ]` crea listas; índices desde 0; slicing igual que strings.
- Mutables: `lista[i] = valor`.
- Añadir: `append`, `insert`, `extend`. Quitar: `remove`, `pop`, `del`, `clear`.
- `sort()` modifica; `sorted()` devuelve una copia ordenada.
- `len`, `sum`, `min`, `max`, `in`, `count`, `index`.
- `b = a` **no** copia; usa `a.copy()`.
- Listas anidadas = tablas.

## 9.17 🎯 Ejercicios del Módulo 9

**Ejercicio 9.1** — Crea una lista con 5 números y muestra el primero, el último y la cantidad de elementos.

**Ejercicio 9.2** — Dada `["rojo", "verde", "azul"]`, cambia `"verde"` por `"amarillo"` y muestra la lista.

**Ejercicio 9.3** — Añade `"negro"` al final de la lista anterior e inserta `"blanco"` al principio.

**Ejercicio 9.4** — Quita el último elemento de una lista con `pop` y muestra qué elemento salió.

**Ejercicio 9.5** — Con `[4, 8, 15, 16, 23, 42]` muestra la suma, el mayor, el menor y el promedio.

**Ejercicio 9.6** — Recorre `["Ana", "Luis", "Eva"]` y muestra `Hola, <nombre>` para cada uno.

**Ejercicio 9.7** — Ordena `[5, 1, 4, 2, 3]` de menor a mayor y luego de mayor a menor.

**Ejercicio 9.8** — Crea una lista con los cuadrados de los números del 1 al 10 usando un `for` y `append`.

**Ejercicio 9.9** — Pide 5 números al usuario, guárdalos en una lista y muestra la lista, su suma y su promedio.

**Ejercicio 9.10** — Dada una lista de números, crea otra lista solo con los mayores que 10.

**Ejercicio 9.11** — Comprueba si el número `7` está en la lista `[3, 5, 7, 9]` y en qué posición.

**Ejercicio 9.12** — Cuenta cuántas veces aparece el `2` en `[1, 2, 2, 3, 2, 4]`.

**Ejercicio 9.13** — Crea la lista `[1, 2, 3]`, haz una copia, añade un 4 a la copia y comprueba que la original no cambió.

**Ejercicio 9.14** — Dada `[1, 2, 3, 4, 5]`, muestra solo los 3 primeros, los 2 últimos y la lista invertida.

**Ejercicio 9.15** — Con la tabla `[[1, 2], [3, 4], [5, 6]]`, muestra la suma de todos sus números.

**Ejercicio 9.16** — Pide palabras hasta que el usuario escriba `fin`. Muestra cuántas palabras escribió y la lista ordenada alfabéticamente.

**Ejercicio 9.17** — Dada una lista de números, muestra el mayor **sin** usar `max` (con un `for`).

**Ejercicio 9.18** — Invierte una lista **sin** usar `reverse()` ni slicing (crea una lista nueva con un `for`).

### ✅ Soluciones del Módulo 9

**9.1**

```python
n = [3, 6, 9, 12, 15]
print(n[0], n[-1], len(n))   # 3 15 5
```

**9.2**

```python
colores = ["rojo", "verde", "azul"]
colores[1] = "amarillo"
print(colores)
```

**9.3**

```python
colores.append("negro")
colores.insert(0, "blanco")
print(colores)   # ['blanco', 'rojo', 'amarillo', 'azul', 'negro']
```

**9.4**

```python
lista = [1, 2, 3]
salio = lista.pop()
print(salio, lista)   # 3 [1, 2]
```

**9.5**

```python
n = [4, 8, 15, 16, 23, 42]
print(sum(n), max(n), min(n), sum(n) / len(n))   # 108 42 4 18.0
```

**9.6**

```python
for nombre in ["Ana", "Luis", "Eva"]:
    print("Hola,", nombre)
```

**9.7**

```python
n = [5, 1, 4, 2, 3]
n.sort()
print(n)   # [1, 2, 3, 4, 5]
n.sort(reverse=True)
print(n)   # [5, 4, 3, 2, 1]
```

**9.8**

```python
cuadrados = []
for n in range(1, 11):
    cuadrados.append(n ** 2)
print(cuadrados)
```

**9.9**

```python
numeros = []
for i in range(5):
    numeros.append(float(input(f"Número {i + 1}: ")))
print(numeros)
print("Suma:", sum(numeros))
print("Promedio:", sum(numeros) / len(numeros))
```

**9.10**

```python
numeros = [4, 12, 7, 25, 10, 33]
grandes = []
for n in numeros:
    if n > 10:
        grandes.append(n)
print(grandes)   # [12, 25, 33]
```

**9.11**

```python
lista = [3, 5, 7, 9]
if 7 in lista:
    print("Está en la posición", lista.index(7))   # 2
```

**9.12**

```python
print([1, 2, 2, 3, 2, 4].count(2))   # 3
```

**9.13**

```python
a = [1, 2, 3]
b = a.copy()
b.append(4)
print(a)   # [1, 2, 3]
print(b)   # [1, 2, 3, 4]
```

**9.14**

```python
n = [1, 2, 3, 4, 5]
print(n[:3])    # [1, 2, 3]
print(n[-2:])   # [4, 5]
print(n[::-1])  # [5, 4, 3, 2, 1]
```

**9.15**

```python
tabla = [[1, 2], [3, 4], [5, 6]]
total = 0
for fila in tabla:
    total += sum(fila)
print(total)   # 21
```

**9.16**

```python
palabras = []
while True:
    p = input("Palabra (o 'fin'): ")
    if p == "fin":
        break
    palabras.append(p)
print("Escribiste", len(palabras), "palabras")
print(sorted(palabras))
```

**9.17**

```python
numeros = [4, 19, 7, 12]
mayor = numeros[0]
for n in numeros:
    if n > mayor:
        mayor = n
print(mayor)   # 19
```

**9.18**

```python
original = [1, 2, 3, 4]
reves = []
for n in original:
    reves.insert(0, n)
print(reves)   # [4, 3, 2, 1]
```

---

# MÓDULO 10 — Tuplas, conjuntos y desempaquetado

Además de las listas, Python tiene otras colecciones. Cada una sirve para algo distinto.

## 10.1 Tuplas: listas que NO se pueden modificar

Se escriben con paréntesis `( )`:

```python
punto = (3, 4)
colores = ("rojo", "verde", "azul")
un_solo = (5,)       # ¡con una coma! sin ella, (5) es solo el número 5
vacia = ()

print(punto)         # (3, 4)
print(type(punto))   # <class 'tuple'>
```

Se accede igual que a una lista:

```python
colores = ("rojo", "verde", "azul")
print(colores[0])       # rojo
print(colores[-1])      # azul
print(colores[1:])      # ('verde', 'azul')
print(len(colores))     # 3
print("rojo" in colores)  # True

for c in colores:
    print(c)
```

Pero **no** se puede modificar (inmutable):

```python
colores[0] = "negro"    # ❌ TypeError
colores.append("x")     # ❌ AttributeError
```

### ¿Para qué sirve una tupla?

- Para datos que **no deben cambiar**: coordenadas `(x, y)`, un RGB `(255, 0, 0)`, una fecha `(2025, 3, 9)`.
- Para **devolver varios valores** de una función (lo verás pronto).
- Son un poco más rápidas y ocupan menos memoria.

Métodos (solo dos):

```python
t = (1, 2, 2, 3, 2)
print(t.count(2))   # 3
print(t.index(3))   # 3
```

Convertir:

```python
l = list((1, 2, 3))    # tupla → lista
t = tuple([1, 2, 3])   # lista → tupla
```

## 10.2 Desempaquetado

Sacar los valores de una colección a variables sueltas:

```python
punto = (3, 4)
x, y = punto
print(x)   # 3
print(y)   # 4
```

```python
nombre, edad, ciudad = ("Ana", 20, "Madrid")
print(nombre, edad, ciudad)
```

Con `*` para "recoger el resto":

```python
primero, *medio, ultimo = [1, 2, 3, 4, 5]
print(primero)   # 1
print(medio)     # [2, 3, 4]
print(ultimo)    # 5
```

Intercambio de variables (ya lo conoces; en realidad usa tuplas):

```python
a, b = 1, 2
a, b = b, a
print(a, b)   # 2 1
```

Recorrer una lista de tuplas:

```python
alumnos = [("Ana", 8), ("Luis", 6), ("Eva", 9)]
for nombre, nota in alumnos:
    print(f"{nombre}: {nota}")
```

## 10.3 Conjuntos (`set`): colecciones sin repetidos

Se escriben con llaves `{ }` y **no tienen orden ni elementos repetidos**.

```python
numeros = {1, 2, 3, 3, 2, 1}
print(numeros)   # {1, 2, 3}   (los duplicados desaparecen)

vacio = set()     # ⚠️ {} crea un diccionario, no un conjunto vacío
```

**Su uso estrella: quitar duplicados.**

```python
lista = [1, 2, 2, 3, 3, 3]
sin_repetir = list(set(lista))
print(sin_repetir)   # [1, 2, 3]  (el orden puede variar)
```

**Contar elementos distintos:**

```python
print(len(set("abracadabra")))   # 5  (a, b, r, c, d)
```

### Operaciones con conjuntos

```python
a = {1, 2, 3, 4}
b = {3, 4, 5, 6}

print(a | b)    # unión: {1, 2, 3, 4, 5, 6}
print(a & b)    # intersección (lo común): {3, 4}
print(a - b)    # diferencia (en a pero no en b): {1, 2}
print(a ^ b)    # lo que no es común: {1, 2, 5, 6}
```

Ejemplo de la vida real:

```python
clase_a = {"Ana", "Luis", "Eva"}
clase_b = {"Luis", "Pedro", "Eva"}

print("En ambas:", clase_a & clase_b)           # {'Luis', 'Eva'}
print("Todos:", clase_a | clase_b)
print("Solo en A:", clase_a - clase_b)          # {'Ana'}
```

### Métodos de conjuntos

```python
s = {1, 2}
s.add(3)        # añadir uno
s.remove(1)     # quitar (error si no existe)
s.discard(99)   # quitar (sin error si no existe)
print(s)        # {2, 3}
print(2 in s)   # True  (¡muy rápido!)
```

## 10.4 Comparativa rápida

| Colección | Símbolo | Orden | Repetidos | Se modifica |
|-----------|---------|-------|-----------|-------------|
| Lista | `[ ]` | sí | sí | sí |
| Tupla | `( )` | sí | sí | no |
| Conjunto | `{ }` | no | no | sí |
| Diccionario | `{k: v}` | sí* | claves no | sí |

\*Desde Python 3.7 los diccionarios conservan el orden de inserción.

**¿Cuál uso?**

- ¿Datos en orden que cambian? → **lista**.
- ¿Datos fijos? → **tupla**.
- ¿Quiero eliminar repetidos o comprobar pertenencia rápido? → **conjunto**.
- ¿Datos con nombre? → **diccionario** (siguiente módulo).

## 10.5 Ejemplos completos

**Ejemplo A: palabras únicas de una frase**

```python
frase = "el gato y el perro y el pez"
palabras = frase.split()
unicas = set(palabras)
print(len(palabras), "palabras,", len(unicas), "únicas")   # 8 palabras, 5 únicas
```

**Ejemplo B: ¿hay elementos repetidos en una lista?**

```python
datos = [1, 2, 3, 2]
print(len(datos) != len(set(datos)))   # True → hay repetidos
```

**Ejemplo C: coordenadas**

```python
puntos = [(0, 0), (3, 4), (6, 8)]
for x, y in puntos:
    print(f"Punto en x={x}, y={y}")
```

**Ejemplo D: vocales distintas en un texto**

```python
texto = "murcielago"
vocales = set(texto) & set("aeiou")
print(vocales)   # {'i', 'e', 'a', 'o', 'u'}  (orden variable)
```

## 10.6 Resumen del Módulo 10

- Tupla `( )`: ordenada e inmutable; ideal para datos fijos.
- Desempaquetar: `a, b = (1, 2)`; con `*` recoges el resto.
- Conjunto `{ }`: sin orden y sin repetidos; operaciones `| & - ^`.
- `set(lista)` quita repetidos.

## 10.7 🎯 Ejercicios del Módulo 10

**Ejercicio 10.1** — Crea una tupla con tu día, mes y año de nacimiento y muéstrala.

**Ejercicio 10.2** — Desempaqueta `("Ana", 20)` en dos variables `nombre` y `edad` y muéstralas.

**Ejercicio 10.3** — Dada la tupla `(5, 3, 8, 1)`, muestra su longitud, el mayor y el menor.

**Ejercicio 10.4** — Convierte la tupla `(1, 2, 3)` en lista, añade un 4 y vuelve a convertirla en tupla.

**Ejercicio 10.5** — Con `primero, *resto = [10, 20, 30, 40]` muestra `primero` y `resto`.

**Ejercicio 10.6** — Quita los repetidos de `[4, 4, 5, 6, 6, 6, 7]`.

**Ejercicio 10.7** — Dados `a = {1, 2, 3, 4}` y `b = {3, 4, 5}`, muestra la unión, la intersección y la diferencia `a - b`.

**Ejercicio 10.8** — Cuenta cuántas letras distintas tiene `"mississippi"`.

**Ejercicio 10.9** — Recorre la lista de tuplas `[("pan", 2), ("leche", 1)]` y muestra `2 x pan`, `1 x leche`.

**Ejercicio 10.10** — Pide una frase y muestra cuántas palabras distintas contiene (ignora mayúsculas).

**Ejercicio 10.11** — Dadas dos listas de números, muestra los que aparecen en las dos.

**Ejercicio 10.12** — Intercambia los valores de dos variables usando desempaquetado de tuplas.

### ✅ Soluciones del Módulo 10

**10.1**

```python
nacimiento = (15, 3, 2005)
print(nacimiento)
```

**10.2**

```python
nombre, edad = ("Ana", 20)
print(nombre, edad)
```

**10.3**

```python
t = (5, 3, 8, 1)
print(len(t), max(t), min(t))   # 4 8 1
```

**10.4**

```python
t = (1, 2, 3)
l = list(t)
l.append(4)
t = tuple(l)
print(t)   # (1, 2, 3, 4)
```

**10.5**

```python
primero, *resto = [10, 20, 30, 40]
print(primero)   # 10
print(resto)     # [20, 30, 40]
```

**10.6**

```python
print(list(set([4, 4, 5, 6, 6, 6, 7])))   # [4, 5, 6, 7]
```

**10.7**

```python
a = {1, 2, 3, 4}
b = {3, 4, 5}
print(a | b)   # {1, 2, 3, 4, 5}
print(a & b)   # {3, 4}
print(a - b)   # {1, 2}
```

**10.8**

```python
print(len(set("mississippi")))   # 4  (m, i, s, p)
```

**10.9**

```python
for producto, cantidad in [("pan", 2), ("leche", 1)]:
    print(f"{cantidad} x {producto}")
```

**10.10**

```python
frase = input("Frase: ").lower()
print(len(set(frase.split())))
```

**10.11**

```python
a = [1, 2, 3, 4]
b = [3, 4, 5, 6]
print(list(set(a) & set(b)))   # [3, 4]
```

**10.12**

```python
x = 10
y = 20
x, y = y, x
print(x, y)   # 20 10
```

---

# MÓDULO 11 — Diccionarios

Una lista accede por **posición** (`lista[0]`). Un **diccionario** accede por **nombre** (clave). Es como un diccionario real: buscas una palabra (clave) y encuentras su definición (valor).

También es como la agenda del celular: buscas "Mamá" (clave) y obtienes su teléfono (valor).

## 11.1 Crear diccionarios

Con llaves y pares `clave: valor`:

```python
persona = {
    "nombre": "Ana",
    "edad": 20,
    "ciudad": "Madrid"
}

print(persona)
print(type(persona))   # <class 'dict'>
print(len(persona))    # 3
```

Más ejemplos:

```python
notas = {"mates": 8, "lengua": 7, "historia": 9}
precios = {"manzana": 1.5, "pera": 2.0, "uva": 3.2}
vacio = {}
```

Las **claves** suelen ser textos o números, y **no se pueden repetir**. Los **valores** pueden ser de cualquier tipo.

## 11.2 Acceder a un valor

```python
persona = {"nombre": "Ana", "edad": 20}

print(persona["nombre"])   # Ana
print(persona["edad"])     # 20
```

Si la clave no existe → `KeyError`:

```python
print(persona["telefono"])   # ❌ KeyError: 'telefono'
```

**`.get()` es la forma segura** (devuelve `None` o un valor por defecto):

```python
print(persona.get("telefono"))            # None
print(persona.get("telefono", "no tiene"))  # no tiene
print(persona.get("nombre"))              # Ana
```

## 11.3 Añadir, modificar y borrar

```python
persona = {"nombre": "Ana", "edad": 20}

persona["ciudad"] = "Madrid"     # añadir (clave nueva)
persona["edad"] = 21             # modificar (clave existente)
print(persona)   # {'nombre': 'Ana', 'edad': 21, 'ciudad': 'Madrid'}

del persona["ciudad"]            # borrar
print(persona)   # {'nombre': 'Ana', 'edad': 21}

edad = persona.pop("edad")       # borrar y devolver el valor
print(edad)      # 21
print(persona)   # {'nombre': 'Ana'}
```

> 💡 La misma sintaxis `d[clave] = valor` sirve para **añadir** y para **modificar**: si la clave existe, cambia; si no, se crea.

## 11.4 Comprobar si existe una clave

```python
persona = {"nombre": "Ana", "edad": 20}

print("nombre" in persona)      # True
print("telefono" in persona)    # False
print("telefono" not in persona)  # True

if "edad" in persona:
    print("Edad:", persona["edad"])
```

⚠️ `in` mira las **claves**, no los valores. Para valores: `20 in persona.values()`.

## 11.5 Recorrer un diccionario

```python
notas = {"mates": 8, "lengua": 7, "historia": 9}

# 1) Recorrer las claves
for materia in notas:
    print(materia)

# 2) Recorrer las claves con .keys() (igual)
for materia in notas.keys():
    print(materia)

# 3) Recorrer los valores
for nota in notas.values():
    print(nota)

# 4) Recorrer clave y valor a la vez (¡la más útil!)
for materia, nota in notas.items():
    print(f"{materia}: {nota}")
```

```text
mates: 8
lengua: 7
historia: 9
```

Utilidades:

```python
print(list(notas.keys()))     # ['mates', 'lengua', 'historia']
print(list(notas.values()))   # [8, 7, 9]
print(sum(notas.values()))    # 24
print(max(notas.values()))    # 9
print(sum(notas.values()) / len(notas))   # 8.0
```

## 11.6 Más métodos

```python
a = {"x": 1, "y": 2}
b = {"y": 99, "z": 3}

a.update(b)              # mezcla b dentro de a
print(a)                 # {'x': 1, 'y': 99, 'z': 3}

a.setdefault("w", 0)     # añade "w" solo si no existía
print(a)                 # {'x': 1, 'y': 99, 'z': 3, 'w': 0}

copia = a.copy()         # copia independiente
a.clear()                # vacía el diccionario
print(a)                 # {}
print(copia)
```

## 11.7 Diccionarios con listas y diccionarios dentro

**Valores que son listas:**

```python
alumno = {
    "nombre": "Luis",
    "notas": [7, 8, 9]
}
print(alumno["notas"][0])               # 7
print(sum(alumno["notas"]) / 3)         # 8.0
alumno["notas"].append(10)
print(alumno["notas"])                  # [7, 8, 9, 10]
```

**Lista de diccionarios** (¡muy común, como una tabla de base de datos!):

```python
alumnos = [
    {"nombre": "Ana", "nota": 8},
    {"nombre": "Luis", "nota": 6},
    {"nombre": "Eva", "nota": 9},
]

for a in alumnos:
    print(f"{a['nombre']} sacó {a['nota']}")

print(alumnos[1]["nombre"])   # Luis
```

**Diccionario de diccionarios:**

```python
contactos = {
    "Ana":  {"tel": "111", "email": "ana@mail.com"},
    "Luis": {"tel": "222", "email": "luis@mail.com"},
}
print(contactos["Ana"]["tel"])        # 111
contactos["Eva"] = {"tel": "333", "email": "eva@mail.com"}
```

> 💡 Dentro de un f-string con comillas dobles, usa comillas simples para la clave: `f"{a['nombre']}"`.

## 11.8 Patrones muy usados

**Contar cuántas veces aparece cada cosa:**

```python
texto = "banana"
conteo = {}
for letra in texto:
    if letra in conteo:
        conteo[letra] += 1
    else:
        conteo[letra] = 1
print(conteo)   # {'b': 1, 'a': 3, 'n': 2}
```

Versión más corta con `get`:

```python
conteo = {}
for letra in "banana":
    conteo[letra] = conteo.get(letra, 0) + 1
print(conteo)   # {'b': 1, 'a': 3, 'n': 2}
```

**Contar palabras:**

```python
frase = "el gato y el perro"
conteo = {}
for palabra in frase.split():
    conteo[palabra] = conteo.get(palabra, 0) + 1
print(conteo)   # {'el': 2, 'gato': 1, 'y': 1, 'perro': 1}
```

**Crear un diccionario desde dos listas:**

```python
claves = ["a", "b", "c"]
valores = [1, 2, 3]
d = dict(zip(claves, valores))
print(d)   # {'a': 1, 'b': 2, 'c': 3}
```

**Agrupar:**

```python
palabras = ["sol", "luna", "mar", "cielo", "tierra"]
por_longitud = {}
for p in palabras:
    n = len(p)
    if n not in por_longitud:
        por_longitud[n] = []
    por_longitud[n].append(p)
print(por_longitud)
# {3: ['sol', 'mar'], 4: ['luna'], 5: ['cielo'], 6: ['tierra']}
```

**Invertir clave ↔ valor:**

```python
d = {"a": 1, "b": 2}
inv = {v: k for k, v in d.items()}   # (comprensión, la verás en el Módulo 14)
print(inv)   # {1: 'a', 2: 'b'}
```

## 11.9 Ejemplos completos

**Ejemplo A: traductor mini**

```python
diccionario = {"hola": "hello", "adiós": "goodbye", "gato": "cat"}
palabra = input("Palabra en español: ").lower()
print(diccionario.get(palabra, "No la conozco"))
```

**Ejemplo B: tienda sencilla**

```python
precios = {"pan": 1.2, "leche": 0.9, "huevos": 2.5}
total = 0
for producto in ["pan", "leche", "pan"]:
    total += precios[producto]
print(f"Total: {total:.2f}")   # Total: 3.30
```

**Ejemplo C: agenda de contactos**

```python
agenda = {}
agenda["Ana"] = "111-222"
agenda["Luis"] = "333-444"

nombre = input("¿A quién buscas? ")
if nombre in agenda:
    print("Teléfono:", agenda[nombre])
else:
    print("No está en la agenda")
```

## 11.10 ⚠️ Errores comunes

```python
d = {"a": 1}
print(d["b"])         # ❌ KeyError → usa d.get("b")
d = {["x"]: 1}        # ❌ una lista no puede ser clave (es mutable)
d = {"a": 1, "a": 2}  # no da error, pero queda solo {"a": 2}
```

## 11.11 Resumen del Módulo 11

- `{clave: valor}`; se accede con `d[clave]` o `d.get(clave)`.
- `d[clave] = valor` añade o modifica; `del d[clave]` / `pop` borran.
- `in` comprueba claves; `.keys()`, `.values()`, `.items()` para recorrer.
- Patrón `conteo[x] = conteo.get(x, 0) + 1` para contar.
- Se pueden anidar: listas de diccionarios, diccionarios de diccionarios.

## 11.12 🎯 Ejercicios del Módulo 11

**Ejercicio 11.1** — Crea un diccionario con tu `nombre`, `edad` y `ciudad` y muéstralo.

**Ejercicio 11.2** — Muestra solo el valor de `edad` de ese diccionario.

**Ejercicio 11.3** — Añade la clave `"profesion"` y cambia la edad a un valor distinto.

**Ejercicio 11.4** — Borra la clave `"ciudad"` y muestra el diccionario.

**Ejercicio 11.5** — Con `{"mates": 8, "lengua": 6, "arte": 10}` recorre con `.items()` y muestra `materia: nota`.

**Ejercicio 11.6** — Con el mismo diccionario, calcula el promedio de las notas.

**Ejercicio 11.7** — Con el mismo diccionario, muestra el nombre de la materia con la mejor nota.

**Ejercicio 11.8** — Pide una clave al usuario y muestra su valor del diccionario `{"rojo": "red", "azul": "blue"}`; si no existe, muestra `No encontrada`.

**Ejercicio 11.9** — Cuenta cuántas veces aparece cada letra en `"abracadabra"`.

**Ejercicio 11.10** — Cuenta cuántas veces aparece cada palabra en `"si si no si no no si"`.

**Ejercicio 11.11** — Dadas las listas `["pan", "leche"]` y `[1.2, 0.9]`, crea un diccionario de precios con `zip`.

**Ejercicio 11.12** — Con una lista de diccionarios de 3 alumnos (nombre y nota), muestra los que tengan 7 o más.

**Ejercicio 11.13** — Crea un programa con un diccionario `inventario = {"manzanas": 10, "peras": 5}`. Pide un producto y una cantidad, y réstala del inventario (si hay suficiente).

**Ejercicio 11.14** — Pide al usuario 3 nombres y 3 teléfonos y guárdalos en un diccionario (agenda). Luego muestra la agenda completa.

### ✅ Soluciones del Módulo 11

**11.1**

```python
persona = {"nombre": "Ana", "edad": 20, "ciudad": "Madrid"}
print(persona)
```

**11.2**

```python
print(persona["edad"])
```

**11.3**

```python
persona["profesion"] = "estudiante"
persona["edad"] = 21
print(persona)
```

**11.4**

```python
del persona["ciudad"]
print(persona)
```

**11.5**

```python
notas = {"mates": 8, "lengua": 6, "arte": 10}
for materia, nota in notas.items():
    print(f"{materia}: {nota}")
```

**11.6**

```python
print(sum(notas.values()) / len(notas))   # 8.0
```

**11.7**

```python
mejor = None
for materia, nota in notas.items():
    if mejor is None or nota > notas[mejor]:
        mejor = materia
print(mejor)   # arte
```

**11.8**

```python
d = {"rojo": "red", "azul": "blue"}
clave = input("Color: ")
print(d.get(clave, "No encontrada"))
```

**11.9**

```python
conteo = {}
for letra in "abracadabra":
    conteo[letra] = conteo.get(letra, 0) + 1
print(conteo)   # {'a': 5, 'b': 2, 'r': 2, 'c': 1, 'd': 1}
```

**11.10**

```python
conteo = {}
for palabra in "si si no si no no si".split():
    conteo[palabra] = conteo.get(palabra, 0) + 1
print(conteo)   # {'si': 4, 'no': 3}
```

**11.11**

```python
precios = dict(zip(["pan", "leche"], [1.2, 0.9]))
print(precios)
```

**11.12**

```python
alumnos = [
    {"nombre": "Ana", "nota": 8},
    {"nombre": "Luis", "nota": 6},
    {"nombre": "Eva", "nota": 9},
]
for a in alumnos:
    if a["nota"] >= 7:
        print(a["nombre"])
```

**11.13**

```python
inventario = {"manzanas": 10, "peras": 5}
producto = input("Producto: ")
cantidad = int(input("Cantidad a retirar: "))

if producto in inventario:
    if inventario[producto] >= cantidad:
        inventario[producto] -= cantidad
        print("Listo:", inventario)
    else:
        print("No hay suficiente")
else:
    print("Ese producto no existe")
```

**11.14**

```python
agenda = {}
for i in range(3):
    nombre = input("Nombre: ")
    tel = input("Teléfono: ")
    agenda[nombre] = tel

for nombre, tel in agenda.items():
    print(f"{nombre}: {tel}")
```

---

# MÓDULO 12 — Funciones

Una **función** es un bloque de código con un **nombre** que puedes usar muchas veces. Es como una **máquina**: le metes algo, hace su trabajo, y (a veces) te devuelve algo.

Ya has usado funciones de Python: `print()`, `len()`, `input()`, `int()`... Ahora aprenderás a **crear las tuyas**.

**¿Para qué sirven?**

1. **No repetir código.** Escribes algo una vez y lo usas cien veces.
2. **Organizar.** Dividir un programa grande en piezas pequeñas.
3. **Probar y entender mejor.** Una función pequeña con un nombre claro es fácil de leer.

## 12.1 Definir y llamar una función

```python
def saludar():
    print("¡Hola!")
    print("Bienvenido")

saludar()    # llamar (usar) la función
saludar()    # se puede llamar muchas veces
```

```text
¡Hola!
Bienvenido
¡Hola!
Bienvenido
```

- `def` → palabra para **definir** una función.
- `saludar` → el nombre que tú eliges (reglas iguales que las variables).
- `()` → paréntesis (aquí vacíos).
- `:` y el bloque **indentado** → el cuerpo de la función.

⚠️ **Definir** no ejecuta. Solo cuando la **llamas** (`saludar()`) se ejecuta.

```python
def despedirse():
    print("Adiós")

# Si no escribo despedirse(), nunca se imprime nada
despedirse()   # ahora sí
```

## 12.2 Parámetros: darle datos a la función

Un **parámetro** es una variable que la función recibe para trabajar.

```python
def saludar(nombre):
    print(f"Hola, {nombre}")

saludar("Ana")     # Hola, Ana
saludar("Luis")    # Hola, Luis
```

- `nombre` es el **parámetro** (el "hueco" que la función espera).
- `"Ana"` es el **argumento** (el dato real que le das al llamarla).

**Varios parámetros:**

```python
def presentar(nombre, edad):
    print(f"{nombre} tiene {edad} años")

presentar("Ana", 20)
presentar("Luis", 25)
```

El **orden** importa: el primer argumento va al primer parámetro.

```python
presentar(20, "Ana")   # funciona pero sale mal: "20 tiene Ana años"
```

**Explicado de otra forma:** piensa en una **licuadora**. Los parámetros son los "ingredientes que entran" (fruta, leche). Cada vez que la usas con ingredientes distintos, obtienes un batido distinto, pero el procedimiento es el mismo.

## 12.3 `return`: devolver un resultado

`print` **muestra** algo en pantalla. `return` **devuelve** un valor para que lo uses después.

```python
def sumar(a, b):
    return a + b

resultado = sumar(3, 4)
print(resultado)         # 7
print(sumar(10, 5))      # 15
print(sumar(1, 2) * 10)  # 30   ← puedo usar el resultado en otro cálculo
```

**Diferencia entre `print` y `return`:**

```python
def doble_print(n):
    print(n * 2)       # solo muestra, no devuelve nada

def doble_return(n):
    return n * 2       # devuelve el valor

x = doble_print(5)     # imprime 10
print(x)               # None  ← no devolvió nada

y = doble_return(5)    # no imprime nada
print(y)               # 10
```

> 💡 **Regla general:** las funciones que **calculan** deberían `return`ar el resultado; quien las llama decide qué hacer con él (mostrarlo, guardarlo...).

**`return` termina la función inmediatamente:**

```python
def es_mayor(edad):
    if edad >= 18:
        return True
    return False       # solo se llega aquí si el if no se cumplió

print(es_mayor(20))   # True
print(es_mayor(15))   # False
```

(Esa función se puede escribir aún más corto: `return edad >= 18`.)

**Funciones sin `return`** devuelven `None`.

## 12.4 Ejemplos de funciones sencillas (varias formas)

```python
def cuadrado(n):
    return n ** 2

def es_par(n):
    return n % 2 == 0

def area_rectangulo(base, altura):
    return base * altura

def mayor(a, b):
    if a > b:
        return a
    return b

def inicial(nombre):
    return nombre[0].upper()

print(cuadrado(5))              # 25
print(es_par(8))                # True
print(area_rectangulo(3, 4))    # 12
print(mayor(7, 3))              # 7
print(inicial("ana"))           # A
```

## 12.5 Parámetros con valor por defecto

```python
def saludar(nombre, saludo="Hola"):
    print(f"{saludo}, {nombre}")

saludar("Ana")                 # Hola, Ana
saludar("Ana", "Buenos días")  # Buenos días, Ana
```

Si no pasas el argumento, usa el valor por defecto.

```python
def potencia(base, exponente=2):
    return base ** exponente

print(potencia(5))      # 25   (2 por defecto)
print(potencia(5, 3))   # 125
```

⚠️ Los parámetros con valor por defecto van **después** de los obligatorios:

```python
# def f(a=1, b):   # ❌ SyntaxError
def f(b, a=1):      # ✔️
    pass
```

## 12.6 Argumentos por nombre (keyword arguments)

Puedes indicar el nombre del parámetro y así el orden ya no importa:

```python
def presentar(nombre, edad, ciudad):
    print(f"{nombre}, {edad} años, de {ciudad}")

presentar("Ana", 20, "Madrid")                      # por posición
presentar(ciudad="Lima", nombre="Luis", edad=30)    # por nombre (cualquier orden)
presentar("Eva", ciudad="Quito", edad=22)           # mezcla
```

Es muy útil para que el código sea **legible**:

```python
crear_cuenta("Ana", 1000, True)               # ¿qué significa True?
crear_cuenta("Ana", saldo=1000, activa=True)  # mucho más claro
```

## 12.7 Devolver varios valores

En realidad devuelves una **tupla**:

```python
def minmax(lista):
    return min(lista), max(lista)

menor, mayor = minmax([4, 9, 2, 7])
print(menor, mayor)   # 2 9
```

```python
def dividir(a, b):
    cociente = a // b
    resto = a % b
    return cociente, resto

c, r = dividir(17, 5)
print(c, r)   # 3 2
```

## 12.8 Docstrings: documentar una función

Un texto entre triples comillas justo debajo de `def` explica qué hace:

```python
def area_circulo(radio):
    """Calcula el área de un círculo.

    radio: el radio del círculo (número).
    Devuelve el área (float).
    """
    return 3.14159 * radio ** 2

print(area_circulo(2))     # 12.56636
help(area_circulo)         # muestra la documentación
```

## 12.9 Funciones que llaman a otras funciones

Divide tus programas en piezas pequeñas:

```python
def cuadrado(n):
    return n * n

def suma_de_cuadrados(a, b):
    return cuadrado(a) + cuadrado(b)

print(suma_de_cuadrados(3, 4))   # 25
```

```python
def es_par(n):
    return n % 2 == 0

def contar_pares(lista):
    contador = 0
    for n in lista:
        if es_par(n):
            contador += 1
    return contador

print(contar_pares([1, 2, 3, 4, 6]))   # 3
```

## 12.10 Funciones con listas, strings y diccionarios

```python
def promedio(notas):
    return sum(notas) / len(notas)

def contar_vocales(texto):
    total = 0
    for letra in texto.lower():
        if letra in "aeiou":
            total += 1
    return total

def invertir(texto):
    return texto[::-1]

def es_palindromo(texto):
    return texto == texto[::-1]

def contar_palabras(frase):
    conteo = {}
    for p in frase.split():
        conteo[p] = conteo.get(p, 0) + 1
    return conteo

print(promedio([8, 6, 10]))            # 8.0
print(contar_vocales("Murcielago"))    # 5
print(invertir("hola"))                # aloh
print(es_palindromo("reconocer"))      # True
print(contar_palabras("a b a"))        # {'a': 2, 'b': 1}
```

## 12.11 Funciones que modifican listas

Las listas se pasan "por referencia": si la función las cambia, **cambian fuera también**.

```python
def agregar_uno(lista):
    lista.append(1)

mi_lista = [5, 6]
agregar_uno(mi_lista)
print(mi_lista)   # [5, 6, 1]
```

En cambio, con números y textos no pasa (son inmutables):

```python
def sumar_uno(n):
    n = n + 1       # solo cambia la copia local
    return n

x = 5
sumar_uno(x)
print(x)            # 5  (no cambió)
x = sumar_uno(x)    # si quiero guardar el cambio, uso el return
print(x)            # 6
```

## 12.12 Ejemplos completos

**Ejemplo A: una calculadora con funciones**

```python
def sumar(a, b):
    return a + b

def restar(a, b):
    return a - b

def multiplicar(a, b):
    return a * b

def dividir(a, b):
    if b == 0:
        return "No se puede dividir entre cero"
    return a / b

print(sumar(6, 3))        # 9
print(restar(6, 3))       # 3
print(multiplicar(6, 3))  # 18
print(dividir(6, 3))      # 2.0
print(dividir(6, 0))      # No se puede dividir entre cero
```

**Ejemplo B: ¿es primo?**

```python
def es_primo(n):
    if n < 2:
        return False
    for i in range(2, n):
        if n % i == 0:
            return False
    return True

for numero in range(1, 21):
    if es_primo(numero):
        print(numero, end=" ")
# 2 3 5 7 11 13 17 19
```

**Ejemplo C: clasificar una nota**

```python
def clasificar(nota):
    if nota >= 9:
        return "Sobresaliente"
    elif nota >= 7:
        return "Notable"
    elif nota >= 5:
        return "Aprobado"
    return "Suspenso"

for n in [10, 7.5, 5, 3]:
    print(n, "→", clasificar(n))
```

**Ejemplo D: pedir un número válido**

```python
def pedir_entero(mensaje):
    texto = input(mensaje)
    while not texto.isdigit():
        print("Escribe solo dígitos")
        texto = input(mensaje)
    return int(texto)

edad = pedir_entero("Edad: ")
print("Tienes", edad)
```

## 12.13 ⚠️ Errores comunes

```python
def doble(n):
    return n * 2

doble            # ❌ no la llamaste: falta ()
doble()          # ❌ TypeError: falta el argumento
doble(1, 2)      # ❌ TypeError: sobran argumentos
```

```python
def f():
    x = 5
print(x)         # ❌ NameError: x solo existe dentro de f
```

```python
def suma(a, b):
    print(a + b)       # ❌ si luego quieres usar el resultado, necesitas return

total = suma(1, 2) + 10   # TypeError (None + 10)
```

## 12.14 Resumen del Módulo 12

- `def nombre(parámetros):` define; `nombre(argumentos)` llama.
- `return` devuelve un valor y termina la función.
- Parámetros por defecto: `def f(x, y=2)`. Por nombre: `f(y=3, x=1)`.
- Puedes devolver varios valores (tupla).
- Documenta con docstrings. Divide tareas en funciones pequeñas.

## 12.15 🎯 Ejercicios del Módulo 12

**Ejercicio 12.1** — Crea una función `saludar()` que muestre `¡Hola, mundo!` y llámala 3 veces.

**Ejercicio 12.2** — Crea `saludar(nombre)` que muestre `Hola, <nombre>`.

**Ejercicio 12.3** — Crea `doble(n)` que devuelva el doble de un número.

**Ejercicio 12.4** — Crea `area_rectangulo(base, altura)` que devuelva el área.

**Ejercicio 12.5** — Crea `es_par(n)` que devuelva `True` si el número es par.

**Ejercicio 12.6** — Crea `mayor(a, b)` que devuelva el mayor de dos números.

**Ejercicio 12.7** — Crea `mayor_de_tres(a, b, c)` que devuelva el mayor de tres números.

**Ejercicio 12.8** — Crea `celsius_a_fahrenheit(c)` y úsala con 0, 37 y 100.

**Ejercicio 12.9** — Crea `promedio(lista)` y úsala con `[8, 6, 10]`.

**Ejercicio 12.10** — Crea `contar_vocales(texto)` que devuelva cuántas vocales tiene.

**Ejercicio 12.11** — Crea `es_palindromo(texto)` y pruébala con `"ana"`, `"python"`, `"oso"`.

**Ejercicio 12.12** — Crea `potencia(base, exponente=2)` y llámala con y sin el segundo argumento.

**Ejercicio 12.13** — Crea `factorial(n)` que devuelva n!. Pruébala con 5 y 0 (el factorial de 0 es 1).

**Ejercicio 12.14** — Crea `suma_digitos(n)` que devuelva la suma de los dígitos de un número (123 → 6).

**Ejercicio 12.15** — Crea `min_y_max(lista)` que devuelva ambos valores a la vez.

**Ejercicio 12.16** — Crea `contar_letra(texto, letra)` que cuente cuántas veces aparece una letra.

**Ejercicio 12.17** — Crea `solo_pares(lista)` que devuelva una nueva lista con los números pares.

**Ejercicio 12.18** — Crea `tabla(n)` que muestre la tabla de multiplicar de `n` (del 1 al 10).

**Ejercicio 12.19** — Crea `es_bisiesto(anio)` y pruébala con 2000, 1900, 2024 y 2023.

**Ejercicio 12.20** — Crea un mini programa con tres funciones: `pedir_numero()`, `calcular_iva(precio)` (21 %) y `mostrar(precio, total)`. Haz que se llamen en orden.

### ✅ Soluciones del Módulo 12

**12.1**

```python
def saludar():
    print("¡Hola, mundo!")

saludar()
saludar()
saludar()
```

**12.2**

```python
def saludar(nombre):
    print(f"Hola, {nombre}")

saludar("Ana")
```

**12.3**

```python
def doble(n):
    return n * 2

print(doble(7))   # 14
```

**12.4**

```python
def area_rectangulo(base, altura):
    return base * altura

print(area_rectangulo(3, 5))   # 15
```

**12.5**

```python
def es_par(n):
    return n % 2 == 0

print(es_par(4), es_par(7))   # True False
```

**12.6**

```python
def mayor(a, b):
    if a > b:
        return a
    return b

print(mayor(3, 9))   # 9
```

**12.7**

```python
def mayor_de_tres(a, b, c):
    mayor = a
    if b > mayor:
        mayor = b
    if c > mayor:
        mayor = c
    return mayor

print(mayor_de_tres(4, 9, 2))   # 9
```

**12.8**

```python
def celsius_a_fahrenheit(c):
    return c * 9 / 5 + 32

for t in (0, 37, 100):
    print(t, "→", celsius_a_fahrenheit(t))   # 32.0, 98.6, 212.0
```

**12.9**

```python
def promedio(lista):
    return sum(lista) / len(lista)

print(promedio([8, 6, 10]))   # 8.0
```

**12.10**

```python
def contar_vocales(texto):
    total = 0
    for c in texto.lower():
        if c in "aeiou":
            total += 1
    return total

print(contar_vocales("Murcielago"))   # 5
```

**12.11**

```python
def es_palindromo(texto):
    return texto == texto[::-1]

print(es_palindromo("ana"), es_palindromo("python"), es_palindromo("oso"))
# True False True
```

**12.12**

```python
def potencia(base, exponente=2):
    return base ** exponente

print(potencia(4))      # 16
print(potencia(2, 5))   # 32
```

**12.13**

```python
def factorial(n):
    resultado = 1
    for i in range(1, n + 1):
        resultado *= i
    return resultado

print(factorial(5))   # 120
print(factorial(0))   # 1
```

**12.14**

```python
def suma_digitos(n):
    total = 0
    while n > 0:
        total += n % 10
        n //= 10
    return total

print(suma_digitos(123))   # 6
```

**12.15**

```python
def min_y_max(lista):
    return min(lista), max(lista)

menor, mayor = min_y_max([4, 1, 9])
print(menor, mayor)   # 1 9
```

**12.16**

```python
def contar_letra(texto, letra):
    total = 0
    for c in texto:
        if c == letra:
            total += 1
    return total

print(contar_letra("banana", "a"))   # 3
```

**12.17**

```python
def solo_pares(lista):
    pares = []
    for n in lista:
        if n % 2 == 0:
            pares.append(n)
    return pares

print(solo_pares([1, 2, 3, 4, 5, 6]))   # [2, 4, 6]
```

**12.18**

```python
def tabla(n):
    for i in range(1, 11):
        print(f"{n} x {i} = {n * i}")

tabla(7)
```

**12.19**

```python
def es_bisiesto(anio):
    return (anio % 4 == 0 and anio % 100 != 0) or anio % 400 == 0

for a in (2000, 1900, 2024, 2023):
    print(a, es_bisiesto(a))   # True False True False
```

**12.20**

```python
def pedir_numero():
    return float(input("Precio sin IVA: "))

def calcular_iva(precio):
    return precio * 1.21

def mostrar(precio, total):
    print(f"Precio: {precio:.2f} | Con IVA: {total:.2f}")

p = pedir_numero()
t = calcular_iva(p)
mostrar(p, t)
```

---

# MÓDULO 13 — Alcance (scope) y recursión

## 13.1 Variables locales y globales

Una variable creada **dentro** de una función es **local**: solo existe ahí. Una variable creada **fuera** es **global**: se puede leer en todo el programa.

```python
mensaje = "Soy global"

def mostrar():
    local = "Soy local"
    print(mensaje)    # ✔️ puede leer la global
    print(local)

mostrar()
print(mensaje)        # ✔️
# print(local)        # ❌ NameError: local solo existe dentro de mostrar()
```

**Analogía:** las funciones son habitaciones con puerta. Lo que haces dentro de la habitación (variable local) se queda ahí. Pero desde la habitación puedes mirar por la ventana y ver el salón (global).

### Misma variable, distinto lugar

```python
x = 10

def f():
    x = 99            # esto crea OTRA x, local a f
    print("dentro:", x)

f()
print("fuera:", x)
```

```text
dentro: 99
fuera: 10
```

Los parámetros también son variables locales:

```python
def doble(n):
    n = n * 2
    return n

n = 5
print(doble(n))   # 10
print(n)          # 5  (la n global no cambió)
```

## 13.2 La palabra `global` (úsala con cuidado)

Para **modificar** una global desde dentro de una función:

```python
contador = 0

def incrementar():
    global contador
    contador += 1

incrementar()
incrementar()
print(contador)   # 2
```

> ⚠️ Sin `global`, `contador += 1` daría error (`UnboundLocalError`), porque Python pensaría que `contador` es local.

> 💡 **Buena práctica:** evita `global`. Es mejor que la función reciba datos como parámetros y devuelva resultados con `return`.

```python
# Mejor así:
def incrementar(valor):
    return valor + 1

contador = 0
contador = incrementar(contador)
contador = incrementar(contador)
print(contador)   # 2
```

## 13.3 Funciones dentro de funciones (y `nonlocal`)

```python
def externa():
    mensaje = "hola"

    def interna():
        print(mensaje)   # la interna puede leer la variable de la externa

    interna()

externa()   # hola
```

Para **modificar** la variable de la función externa, `nonlocal`:

```python
def contador():
    cuenta = 0

    def sumar():
        nonlocal cuenta
        cuenta += 1
        return cuenta

    return sumar

c = contador()
print(c())   # 1
print(c())   # 2
print(c())   # 3
```

(Esto se llama *closure*: la función interna "recuerda" la variable.)

## 13.4 Recursión: una función que se llama a sí misma

Una función **recursiva** se llama a sí misma para resolver un problema más pequeño del mismo tipo.

**Analogía de las muñecas rusas:** abres una muñeca y dentro hay otra muñeca más pequeña, y dentro otra... hasta que llegas a la última, que ya no se abre. Esa última es el **caso base**.

Toda función recursiva necesita:

1. **Caso base:** cuándo parar (la respuesta directa, sin llamarse).
2. **Caso recursivo:** llamarse a sí misma con un problema **más pequeño**.

### Ejemplo 1: cuenta atrás

```python
def cuenta_atras(n):
    if n == 0:                 # caso base
        print("¡Despegue!")
    else:                      # caso recursivo
        print(n)
        cuenta_atras(n - 1)    # problema más pequeño

cuenta_atras(3)
```

```text
3
2
1
¡Despegue!
```

### Ejemplo 2: factorial

`5! = 5 × 4!`, y `4! = 4 × 3!`, ... hasta `1! = 1`.

```python
def factorial(n):
    if n <= 1:                    # caso base
        return 1
    return n * factorial(n - 1)   # caso recursivo

print(factorial(5))   # 120
```

**Cómo se "desenrolla" `factorial(3)`:**

```text
factorial(3)
= 3 * factorial(2)
= 3 * (2 * factorial(1))
= 3 * (2 * 1)
= 6
```

### Ejemplo 3: suma de 1 a n

```python
def suma(n):
    if n == 0:
        return 0
    return n + suma(n - 1)

print(suma(4))   # 4 + 3 + 2 + 1 + 0 = 10
```

### Ejemplo 4: invertir un texto

```python
def invertir(texto):
    if len(texto) <= 1:
        return texto
    return invertir(texto[1:]) + texto[0]

print(invertir("hola"))   # aloh
```

### Ejemplo 5: Fibonacci

Cada número es la suma de los dos anteriores: 0, 1, 1, 2, 3, 5, 8, 13...

```python
def fib(n):
    if n < 2:
        return n
    return fib(n - 1) + fib(n - 2)

for i in range(8):
    print(fib(i), end=" ")   # 0 1 1 2 3 5 8 13
```

### Ejemplo 6: sumar los elementos de una lista

```python
def suma_lista(lista):
    if not lista:                 # lista vacía: caso base
        return 0
    return lista[0] + suma_lista(lista[1:])

print(suma_lista([1, 2, 3, 4]))   # 10
```

## 13.5 ⚠️ Cuidado con la recursión

Sin caso base (o con uno que nunca se alcanza) la función se llama sin fin y Python lanza `RecursionError`:

```python
def mala(n):
    return mala(n + 1)    # ❌ nunca para
```

Python limita la profundidad (unas 1000 llamadas). Para problemas grandes, un bucle es más seguro y rápido. **Casi todo lo recursivo se puede hacer con bucles**; la recursión es una herramienta más para pensar ciertos problemas.

## 13.6 Resumen del Módulo 13

- Variable **local**: vive dentro de la función. **Global**: fuera.
- `global` y `nonlocal` permiten modificar; mejor evitarlos.
- **Recursión** = función que se llama a sí misma; necesita **caso base** y un paso que acerque a él.

## 13.7 🎯 Ejercicios del Módulo 13

**Ejercicio 13.1** — Predice qué muestra este código y comprueba:

```python
x = 1
def f():
    x = 2
    return x
print(f())
print(x)
```

**Ejercicio 13.2** — Crea una variable global `total = 0` y una función `sumar(n)` que use `global` para sumarle `n`. Llámala tres veces y muestra el total.

**Ejercicio 13.3** — Reescribe el ejercicio anterior **sin** `global` (con parámetros y `return`).

**Ejercicio 13.4** — Crea una función recursiva `cuenta_atras(n)` que muestre de `n` a 1 y luego `Fin`.

**Ejercicio 13.5** — Crea una función recursiva `suma_hasta(n)` que sume 1 + 2 + ... + n.

**Ejercicio 13.6** — Crea una función recursiva `potencia(base, exp)` (sin usar `**`).

**Ejercicio 13.7** — Crea una función recursiva `contar_digitos(n)` (pista: `n // 10`).

**Ejercicio 13.8** — Crea una función recursiva `es_palindromo(texto)` que compare primera y última letra.

**Ejercicio 13.9** — Muestra los 10 primeros números de Fibonacci con la función recursiva `fib`.

**Ejercicio 13.10** — Crea una función recursiva `maximo(lista)` que devuelva el mayor elemento.

**Ejercicio 13.11** — Usa un *closure*: crea `crear_multiplicador(n)` que devuelva una función que multiplique por `n`. Úsala para crear `doble` y `triple`.

### ✅ Soluciones del Módulo 13

**13.1** Muestra `2` y luego `1`: la `x` de la función es local y no cambia la global.

**13.2**

```python
total = 0

def sumar(n):
    global total
    total += n

sumar(5)
sumar(10)
sumar(3)
print(total)   # 18
```

**13.3**

```python
def sumar(total, n):
    return total + n

total = 0
total = sumar(total, 5)
total = sumar(total, 10)
total = sumar(total, 3)
print(total)   # 18
```

**13.4**

```python
def cuenta_atras(n):
    if n == 0:
        print("Fin")
    else:
        print(n)
        cuenta_atras(n - 1)

cuenta_atras(5)
```

**13.5**

```python
def suma_hasta(n):
    if n == 0:
        return 0
    return n + suma_hasta(n - 1)

print(suma_hasta(10))   # 55
```

**13.6**

```python
def potencia(base, exp):
    if exp == 0:
        return 1
    return base * potencia(base, exp - 1)

print(potencia(2, 5))   # 32
```

**13.7**

```python
def contar_digitos(n):
    if n < 10:
        return 1
    return 1 + contar_digitos(n // 10)

print(contar_digitos(12345))   # 5
```

**13.8**

```python
def es_palindromo(texto):
    if len(texto) <= 1:
        return True
    if texto[0] != texto[-1]:
        return False
    return es_palindromo(texto[1:-1])

print(es_palindromo("reconocer"))   # True
print(es_palindromo("hola"))        # False
```

**13.9**

```python
def fib(n):
    if n < 2:
        return n
    return fib(n - 1) + fib(n - 2)

for i in range(10):
    print(fib(i), end=" ")   # 0 1 1 2 3 5 8 13 21 34
```

**13.10**

```python
def maximo(lista):
    if len(lista) == 1:
        return lista[0]
    resto = maximo(lista[1:])
    return lista[0] if lista[0] > resto else resto

print(maximo([3, 9, 4, 7]))   # 9
```

**13.11**

```python
def crear_multiplicador(n):
    def multiplicar(x):
        return x * n
    return multiplicar

doble = crear_multiplicador(2)
triple = crear_multiplicador(3)
print(doble(5))    # 10
print(triple(5))   # 15
```

---

# MÓDULO 14 — Comprensiones y funciones de orden superior

Aquí aprenderás formas **cortas y elegantes** de hacer cosas que ya sabes hacer con bucles.

## 14.1 Comprensión de listas

Fíjate en este patrón que ya conoces:

```python
cuadrados = []
for n in range(1, 6):
    cuadrados.append(n ** 2)
print(cuadrados)   # [1, 4, 9, 16, 25]
```

Se puede escribir en **una línea**:

```python
cuadrados = [n ** 2 for n in range(1, 6)]
print(cuadrados)   # [1, 4, 9, 16, 25]
```

**Receta:** `[ expresión   for variable in secuencia ]`

Léelo como: *"dame `n ** 2` para cada `n` en `range(1, 6)`"*.

### Más ejemplos

```python
print([n * 2 for n in [1, 2, 3]])            # [2, 4, 6]
print([c.upper() for c in "hola"])           # ['H', 'O', 'L', 'A']
print([len(p) for p in ["sol", "luna"]])     # [3, 4]
print([f"Hola {n}" for n in ["Ana", "Luis"]]) # ['Hola Ana', 'Hola Luis']
print([0 for _ in range(4)])                 # [0, 0, 0, 0]
print([n for n in range(5)])                 # [0, 1, 2, 3, 4]
```

### Con condición (`if` al final = filtrar)

**Receta:** `[ expresión   for variable in secuencia   if condición ]`

```python
numeros = [1, 2, 3, 4, 5, 6, 7, 8]

pares = [n for n in numeros if n % 2 == 0]
print(pares)   # [2, 4, 6, 8]

grandes = [n for n in numeros if n > 5]
print(grandes)   # [6, 7, 8]

cuadrados_pares = [n ** 2 for n in numeros if n % 2 == 0]
print(cuadrados_pares)   # [4, 16, 36, 64]
```

Versión larga vs corta:

```python
# Larga
palabras_cortas = []
for p in ["sol", "luna", "cielo", "mar"]:
    if len(p) <= 3:
        palabras_cortas.append(p)

# Corta
palabras_cortas = [p for p in ["sol", "luna", "cielo", "mar"] if len(p) <= 3]
print(palabras_cortas)   # ['sol', 'mar']
```

### Con `if/else` (cambia la expresión; va **antes** del `for`)

```python
numeros = [1, 2, 3, 4]
etiquetas = ["par" if n % 2 == 0 else "impar" for n in numeros]
print(etiquetas)   # ['impar', 'par', 'impar', 'par']
```

### Comprensión con dos bucles

```python
pares = [(a, b) for a in [1, 2] for b in ["x", "y"]]
print(pares)   # [(1, 'x'), (1, 'y'), (2, 'x'), (2, 'y')]
```

**Aplanar una lista de listas:**

```python
tabla = [[1, 2], [3, 4], [5, 6]]
plana = [valor for fila in tabla for valor in fila]
print(plana)   # [1, 2, 3, 4, 5, 6]
```

> 💡 Si la comprensión se vuelve difícil de leer, **usa un bucle normal**. La claridad manda.

## 14.2 Comprensión de diccionarios y conjuntos

**Diccionario:** `{clave: valor for ...}`

```python
cuadrados = {n: n ** 2 for n in range(1, 6)}
print(cuadrados)   # {1: 1, 2: 4, 3: 9, 4: 16, 5: 25}

longitudes = {p: len(p) for p in ["sol", "luna", "cielo"]}
print(longitudes)  # {'sol': 3, 'luna': 4, 'cielo': 5}

precios = {"pan": 1, "leche": 2}
con_iva = {k: v * 1.21 for k, v in precios.items()}
print(con_iva)

aprobados = {n: nota for n, nota in {"Ana": 8, "Luis": 4}.items() if nota >= 5}
print(aprobados)   # {'Ana': 8}
```

**Conjunto:** `{expresión for ...}`

```python
letras = {c for c in "abracadabra"}
print(letras)   # {'a', 'b', 'r', 'c', 'd'}  (orden variable)
```

## 14.3 Funciones lambda (funciones anónimas)

Una **lambda** es una función diminuta de una sola línea y sin nombre.

```python
def doble(x):
    return x * 2

# Equivale a:
doble = lambda x: x * 2

print(doble(5))   # 10
```

**Forma:** `lambda parámetros: expresión` (devuelve la expresión automáticamente).

```python
suma = lambda a, b: a + b
print(suma(3, 4))   # 7

es_par = lambda n: n % 2 == 0
print(es_par(10))   # True

saludar = lambda nombre: f"Hola, {nombre}"
print(saludar("Ana"))
```

Las lambdas brillan cuando se **pasan a otras funciones** (siguientes secciones).

## 14.4 `sorted()` y `.sort()` con `key`

`key` indica **por qué criterio** ordenar.

```python
palabras = ["pera", "uva", "manzana", "kiwi"]

print(sorted(palabras))               # alfabético
print(sorted(palabras, key=len))      # por longitud: ['uva', 'pera', 'kiwi', 'manzana']
print(sorted(palabras, key=lambda p: p[-1]))   # por la última letra
print(sorted(palabras, reverse=True)) # al revés
```

**Ordenar listas de diccionarios o tuplas:**

```python
alumnos = [("Ana", 8), ("Luis", 6), ("Eva", 9)]
por_nota = sorted(alumnos, key=lambda a: a[1])
print(por_nota)   # [('Luis', 6), ('Ana', 8), ('Eva', 9)]

mejores_primero = sorted(alumnos, key=lambda a: a[1], reverse=True)
print(mejores_primero)   # [('Eva', 9), ('Ana', 8), ('Luis', 6)]
```

```python
personas = [{"nombre": "Ana", "edad": 30}, {"nombre": "Luis", "edad": 22}]
print(sorted(personas, key=lambda p: p["edad"]))
```

También `max` y `min` aceptan `key`:

```python
print(max(["sol", "luna", "cielo"], key=len))   # cielo
print(min(alumnos, key=lambda a: a[1]))         # ('Luis', 6)
```

## 14.5 `map()`: aplicar una función a todos

```python
numeros = [1, 2, 3, 4]
dobles = map(lambda x: x * 2, numeros)
print(list(dobles))   # [2, 4, 6, 8]
```

(`map` devuelve un objeto "perezoso"; conviértelo con `list(...)`.)

```python
textos = ["1", "2", "3"]
enteros = list(map(int, textos))
print(enteros)   # [1, 2, 3]

print(list(map(str.upper, ["a", "b"])))   # ['A', 'B']
print(list(map(len, ["sol", "luna"])))    # [3, 4]
```

**Misma idea con comprensión (suele ser más legible):**

```python
print([x * 2 for x in numeros])
print([int(t) for t in textos])
```

## 14.6 `filter()`: quedarse con los que cumplen

```python
numeros = [1, 2, 3, 4, 5, 6]
pares = filter(lambda x: x % 2 == 0, numeros)
print(list(pares))   # [2, 4, 6]

palabras = ["sol", "", "luna", ""]
print(list(filter(None, palabras)))   # ['sol', 'luna']  (quita las vacías)
```

Con comprensión:

```python
print([x for x in numeros if x % 2 == 0])
```

## 14.7 `any()`, `all()`, `sum()`, `zip()` y compañía

```python
numeros = [2, 4, 6, 7]

print(any(n % 2 == 1 for n in numeros))   # True  (¿ALGUNO es impar?)
print(all(n % 2 == 0 for n in numeros))   # False (¿TODOS son pares?)
print(sum(n for n in numeros if n > 3))   # 17
print(sum(1 for n in numeros if n % 2 == 0))  # 3  (cuenta los pares)
```

`zip` junta secuencias:

```python
nombres = ["Ana", "Luis"]
edades = [20, 25]
print(list(zip(nombres, edades)))   # [('Ana', 20), ('Luis', 25)]
print(dict(zip(nombres, edades)))   # {'Ana': 20, 'Luis': 25}
```

`enumerate`, `reversed`:

```python
print(list(enumerate(["a", "b"])))   # [(0, 'a'), (1, 'b')]
print(list(reversed([1, 2, 3])))     # [3, 2, 1]
```

## 14.8 Ejemplos completos

**Ejemplo A: notas aprobadas**

```python
notas = [4, 8, 5, 3, 10]
aprobadas = [n for n in notas if n >= 5]
print(aprobadas)                 # [8, 5, 10]
print(len(aprobadas), "aprobadas")
```

**Ejemplo B: limpiar una lista de textos**

```python
sucios = ["  Ana ", "LUIS", " eva"]
limpios = [s.strip().capitalize() for s in sucios]
print(limpios)   # ['Ana', 'Luis', 'Eva']
```

**Ejemplo C: producto más caro**

```python
productos = [("pan", 1.2), ("leche", 0.9), ("queso", 4.5)]
caro = max(productos, key=lambda p: p[1])
print(caro)   # ('queso', 4.5)
```

**Ejemplo D: tabla de multiplicar en una línea**

```python
print([7 * i for i in range(1, 11)])
```

## 14.9 Resumen del Módulo 14

- `[expr for x in seq if cond]` → listas en una línea. También `{}` para dicts/sets.
- `lambda x: expr` → mini-función sin nombre.
- `sorted(..., key=...)`, `max/min(..., key=...)`.
- `map` aplica; `filter` selecciona (casi siempre una comprensión es más claro).
- `any` / `all` / `zip` / `enumerate` son muy útiles.

## 14.10 🎯 Ejercicios del Módulo 14

**Ejercicio 14.1** — Crea con una comprensión la lista de los números del 1 al 10 multiplicados por 3.

**Ejercicio 14.2** — Crea con una comprensión la lista de los números pares del 1 al 30.

**Ejercicio 14.3** — Dada `["ana", "luis", "eva"]`, crea una lista con los nombres en mayúscula.

**Ejercicio 14.4** — Dada `["sol", "luna", "mar", "estrella"]`, crea una lista con las longitudes.

**Ejercicio 14.5** — De `[3, -1, 4, -5, 9, -2]`, saca una lista solo con los positivos.

**Ejercicio 14.6** — Con una comprensión de diccionario crea `{n: n*n}` para n del 1 al 5.

**Ejercicio 14.7** — Crea una lambda `cubo` que devuelva el cubo de un número y pruébala.

**Ejercicio 14.8** — Ordena `["pera", "kiwi", "manzana", "uva"]` por longitud (de menor a mayor).

**Ejercicio 14.9** — Ordena `[("Ana", 8), ("Luis", 6), ("Eva", 9)]` por nota de mayor a menor.

**Ejercicio 14.10** — Con `map`, convierte `["4", "8", "15"]` a enteros y súmalos.

**Ejercicio 14.11** — Con `filter`, deja solo los números mayores que 10 de `[5, 12, 8, 20, 3]`.

**Ejercicio 14.12** — Con `any` comprueba si hay algún número negativo en una lista; con `all`, si todos son positivos.

**Ejercicio 14.13** — Aplana `[[1, 2], [3], [4, 5, 6]]` en una sola lista con una comprensión.

**Ejercicio 14.14** — Dada `["a1", "b22", "c333"]`, crea una lista con solo la parte numérica convertida a entero.

**Ejercicio 14.15** — Con `zip` y una comprensión, suma elemento a elemento `[1, 2, 3]` y `[10, 20, 30]`.

### ✅ Soluciones del Módulo 14

**14.1**

```python
print([n * 3 for n in range(1, 11)])
```

**14.2**

```python
print([n for n in range(1, 31) if n % 2 == 0])
```

**14.3**

```python
print([n.upper() for n in ["ana", "luis", "eva"]])
```

**14.4**

```python
print([len(p) for p in ["sol", "luna", "mar", "estrella"]])   # [3, 4, 3, 8]
```

**14.5**

```python
print([n for n in [3, -1, 4, -5, 9, -2] if n > 0])   # [3, 4, 9]
```

**14.6**

```python
print({n: n * n for n in range(1, 6)})
```

**14.7**

```python
cubo = lambda x: x ** 3
print(cubo(3))   # 27
```

**14.8**

```python
print(sorted(["pera", "kiwi", "manzana", "uva"], key=len))
# ['uva', 'pera', 'kiwi', 'manzana']
```

**14.9**

```python
alumnos = [("Ana", 8), ("Luis", 6), ("Eva", 9)]
print(sorted(alumnos, key=lambda a: a[1], reverse=True))
```

**14.10**

```python
nums = list(map(int, ["4", "8", "15"]))
print(sum(nums))   # 27
```

**14.11**

```python
print(list(filter(lambda n: n > 10, [5, 12, 8, 20, 3])))   # [12, 20]
```

**14.12**

```python
lista = [3, -2, 5]
print(any(n < 0 for n in lista))   # True
print(all(n > 0 for n in lista))   # False
```

**14.13**

```python
print([v for fila in [[1, 2], [3], [4, 5, 6]] for v in fila])
```

**14.14**

```python
print([int(t[1:]) for t in ["a1", "b22", "c333"]])   # [1, 22, 333]
```

**14.15**

```python
a = [1, 2, 3]
b = [10, 20, 30]
print([x + y for x, y in zip(a, b)])   # [11, 22, 33]
```

---

# MÓDULO 15 — Archivos

Hasta ahora, cuando el programa terminaba, **todos los datos desaparecían**. Con archivos puedes **guardar** información en el disco y **recuperarla** después.

## 15.1 Escribir en un archivo

```python
archivo = open("saludo.txt", "w")
archivo.write("Hola, archivo\n")
archivo.write("Segunda línea\n")
archivo.close()
```

Esto crea (o **sobrescribe**) `saludo.txt` en la carpeta donde ejecutas el programa.

- `open(nombre, modo)` abre el archivo.
- Modo `"w"` = **w**rite (escribir; borra lo anterior).
- `\n` es el salto de línea: `write` **no** lo pone solo.
- `close()` cierra el archivo (¡no te olvides!).

### Modos de apertura

| Modo | Significa | Efecto |
|------|-----------|--------|
| `"r"` | leer (read) | el archivo debe existir |
| `"w"` | escribir (write) | crea o **borra y reescribe** |
| `"a"` | añadir (append) | agrega al final sin borrar |
| `"r+"` | leer y escribir | el archivo debe existir |

## 15.2 La forma correcta: `with`

`with` cierra el archivo **automáticamente**, aunque haya errores. **Úsalo siempre.**

```python
with open("saludo.txt", "w", encoding="utf-8") as archivo:
    archivo.write("Hola, archivo\n")
    archivo.write("Segunda línea\n")
# aquí el archivo ya se cerró solo
```

> 💡 Agrega `encoding="utf-8"` para que las tildes y la ñ se guarden bien en cualquier sistema.

## 15.3 Leer un archivo

**Todo de golpe (un solo string):**

```python
with open("saludo.txt", "r", encoding="utf-8") as f:
    contenido = f.read()
print(contenido)
```

**Línea por línea (lo más común y eficiente):**

```python
with open("saludo.txt", "r", encoding="utf-8") as f:
    for linea in f:
        print(linea.strip())    # strip quita el \n del final
```

**Todas las líneas en una lista:**

```python
with open("saludo.txt", "r", encoding="utf-8") as f:
    lineas = f.readlines()
print(lineas)   # ['Hola, archivo\n', 'Segunda línea\n']

# o sin los \n:
with open("saludo.txt", "r", encoding="utf-8") as f:
    lineas = f.read().splitlines()
print(lineas)   # ['Hola, archivo', 'Segunda línea']
```

**Una sola línea:**

```python
with open("saludo.txt", encoding="utf-8") as f:
    primera = f.readline()
```

(Si no pones modo, por defecto es `"r"`.)

## 15.4 Añadir al final (`"a"`)

```python
with open("registro.txt", "a", encoding="utf-8") as f:
    f.write("Nueva entrada\n")
```

Cada vez que ejecutes esto, se **agrega** una línea sin borrar las anteriores.

## 15.5 Guardar listas y datos

**Una línea por elemento:**

```python
frutas = ["manzana", "pera", "uva"]

with open("frutas.txt", "w", encoding="utf-8") as f:
    for fruta in frutas:
        f.write(fruta + "\n")
```

**Leerlas de vuelta a una lista:**

```python
with open("frutas.txt", encoding="utf-8") as f:
    frutas = [linea.strip() for linea in f]
print(frutas)   # ['manzana', 'pera', 'uva']
```

**Números (recuerda: se leen como texto):**

```python
with open("numeros.txt", "w") as f:
    for n in [10, 20, 30]:
        f.write(f"{n}\n")

with open("numeros.txt") as f:
    numeros = [int(linea) for linea in f]
print(numeros)       # [10, 20, 30]
print(sum(numeros))  # 60
```

**Varios datos por línea (separados por coma):**

```python
alumnos = [("Ana", 8), ("Luis", 6)]
with open("alumnos.txt", "w", encoding="utf-8") as f:
    for nombre, nota in alumnos:
        f.write(f"{nombre},{nota}\n")

with open("alumnos.txt", encoding="utf-8") as f:
    for linea in f:
        nombre, nota = linea.strip().split(",")
        print(nombre, "→", int(nota))
```

## 15.6 Comprobar si un archivo existe

```python
import os

if os.path.exists("saludo.txt"):
    print("Existe")
else:
    print("No existe")
```

Con `pathlib` (forma moderna):

```python
from pathlib import Path

ruta = Path("saludo.txt")
print(ruta.exists())          # True/False

ruta.write_text("Hola\n", encoding="utf-8")   # escribir de una vez
print(ruta.read_text(encoding="utf-8"))       # leer de una vez
```

Otros comandos útiles:

```python
import os
os.remove("saludo.txt")        # borrar un archivo
os.rename("a.txt", "b.txt")    # renombrar
print(os.listdir("."))         # lista lo que hay en la carpeta actual
```

## 15.7 Errores con archivos

Si abres para leer un archivo que no existe:

```python
open("no_existe.txt")   # ❌ FileNotFoundError
```

Se maneja con `try/except` (módulo 16):

```python
try:
    with open("no_existe.txt") as f:
        print(f.read())
except FileNotFoundError:
    print("El archivo no existe")
```

## 15.8 Ejemplos completos

**Ejemplo A: diario simple**

```python
texto = input("Escribe tu entrada del diario: ")
with open("diario.txt", "a", encoding="utf-8") as f:
    f.write(texto + "\n")
print("Guardado")
```

**Ejemplo B: contar líneas y palabras de un archivo**

```python
lineas = 0
palabras = 0
with open("saludo.txt", encoding="utf-8") as f:
    for linea in f:
        lineas += 1
        palabras += len(linea.split())
print(f"{lineas} líneas y {palabras} palabras")
```

**Ejemplo C: lista de tareas persistente**

```python
from pathlib import Path

ARCHIVO = Path("tareas.txt")

def cargar():
    if not ARCHIVO.exists():
        return []
    return ARCHIVO.read_text(encoding="utf-8").splitlines()

def guardar(tareas):
    ARCHIVO.write_text("\n".join(tareas), encoding="utf-8")

tareas = cargar()
nueva = input("Nueva tarea: ")
tareas.append(nueva)
guardar(tareas)
print("Tus tareas:", tareas)
```

## 15.9 Resumen del Módulo 15

- `open(nombre, modo)`; modos `r`, `w`, `a`.
- **Usa `with`** para cerrar solos los archivos.
- `read()`, `readline()`, `readlines()`, o recorrer con `for linea in f`.
- `write()` no pone salto de línea: añade `\n` tú.
- `os.path.exists` / `Path.exists` para comprobar.
- Todo lo leído es **texto**: convierte con `int()` / `float()`.

## 15.10 🎯 Ejercicios del Módulo 15

**Ejercicio 15.1** — Crea un archivo `mi_nombre.txt` que contenga tu nombre.

**Ejercicio 15.2** — Lee `mi_nombre.txt` y muéstralo por pantalla.

**Ejercicio 15.3** — Escribe en `numeros.txt` los números del 1 al 10, uno por línea.

**Ejercicio 15.4** — Lee `numeros.txt` y muestra la suma de todos los números.

**Ejercicio 15.5** — Añade (`"a"`) la línea `fin` al final de `numeros.txt` sin borrar lo anterior.

**Ejercicio 15.6** — Pide al usuario 3 frases y guárdalas en `frases.txt`, una por línea.

**Ejercicio 15.7** — Lee `frases.txt` y muestra cada línea numerada (`1. ...`).

**Ejercicio 15.8** — Cuenta cuántas líneas tiene `frases.txt`.

**Ejercicio 15.9** — Haz un programa que compruebe si existe `datos.txt`; si no existe, que lo cree con el texto `vacío`.

**Ejercicio 15.10** — Guarda una lista de tuplas `[("Ana", 20), ("Luis", 25)]` en un archivo con formato `nombre,edad`, y vuelve a leerla y mostrarla.

**Ejercicio 15.11** — Lee un archivo y muestra solo las líneas que contengan la letra `a`.

**Ejercicio 15.12** — Haz un contador de visitas: un archivo `visitas.txt` guarda un número; cada vez que se ejecuta el programa, se lee, se suma 1, se guarda y se muestra.

### ✅ Soluciones del Módulo 15

**15.1**

```python
with open("mi_nombre.txt", "w", encoding="utf-8") as f:
    f.write("Ana\n")
```

**15.2**

```python
with open("mi_nombre.txt", encoding="utf-8") as f:
    print(f.read())
```

**15.3**

```python
with open("numeros.txt", "w") as f:
    for n in range(1, 11):
        f.write(f"{n}\n")
```

**15.4**

```python
with open("numeros.txt") as f:
    total = 0
    for linea in f:
        total += int(linea)
print(total)   # 55
```

**15.5**

```python
with open("numeros.txt", "a") as f:
    f.write("fin\n")
```

(Ojo: ahora la línea `fin` rompería el ejercicio 15.4 si hicieras `int("fin")`.)

**15.6**

```python
with open("frases.txt", "w", encoding="utf-8") as f:
    for i in range(3):
        f.write(input(f"Frase {i + 1}: ") + "\n")
```

**15.7**

```python
with open("frases.txt", encoding="utf-8") as f:
    for i, linea in enumerate(f, start=1):
        print(f"{i}. {linea.strip()}")
```

**15.8**

```python
with open("frases.txt", encoding="utf-8") as f:
    print(len(f.readlines()))
```

**15.9**

```python
import os

if not os.path.exists("datos.txt"):
    with open("datos.txt", "w") as f:
        f.write("vacío")
    print("Archivo creado")
else:
    print("Ya existía")
```

**15.10**

```python
personas = [("Ana", 20), ("Luis", 25)]
with open("personas.txt", "w", encoding="utf-8") as f:
    for nombre, edad in personas:
        f.write(f"{nombre},{edad}\n")

with open("personas.txt", encoding="utf-8") as f:
    for linea in f:
        nombre, edad = linea.strip().split(",")
        print(nombre, int(edad))
```

**15.11**

```python
with open("frases.txt", encoding="utf-8") as f:
    for linea in f:
        if "a" in linea:
            print(linea.strip())
```

**15.12**

```python
import os

if os.path.exists("visitas.txt"):
    with open("visitas.txt") as f:
        visitas = int(f.read())
else:
    visitas = 0

visitas += 1
with open("visitas.txt", "w") as f:
    f.write(str(visitas))
print("Visitas:", visitas)
```

---

# MÓDULO 16 — Errores y excepciones

Cuando algo sale mal mientras el programa corre, Python lanza una **excepción** y el programa se detiene. Con `try/except` puedes **atrapar** el error y reaccionar sin que el programa se caiga.

## 16.1 Tipos de error más comunes

| Error | Cuándo ocurre | Ejemplo |
|-------|---------------|---------|
| `SyntaxError` | escribiste mal el código | `print("hola"` |
| `NameError` | usas una variable que no existe | `print(x)` |
| `TypeError` | operación con tipos incorrectos | `"a" + 1` |
| `ValueError` | valor correcto en tipo pero inválido | `int("abc")` |
| `ZeroDivisionError` | dividir entre cero | `5 / 0` |
| `IndexError` | índice fuera de rango | `[1, 2][5]` |
| `KeyError` | clave inexistente en diccionario | `{}["a"]` |
| `FileNotFoundError` | archivo que no existe | `open("x.txt")` |
| `AttributeError` | método/atributo que no existe | `"a".foo()` |
| `IndentationError` | mala indentación | línea con espacios de más |

## 16.2 `try` / `except`

```python
try:
    numero = int(input("Escribe un número: "))
    print("El doble es", numero * 2)
except ValueError:
    print("Eso no es un número")
```

**Cómo funciona:**

1. Python intenta ejecutar el bloque `try`.
2. Si **no** hay error → ignora el `except`.
3. Si hay un error del tipo indicado → salta al `except` y sigue el programa.

Comparación sin y con `try`:

```python
# Sin try: si escribes "hola", el programa se cae con ValueError
n = int(input("Número: "))

# Con try: el programa sigue vivo
try:
    n = int(input("Número: "))
except ValueError:
    print("No era un número")
```

## 16.3 Varios `except`

```python
try:
    a = int(input("A: "))
    b = int(input("B: "))
    print(a / b)
except ValueError:
    print("Debes escribir números enteros")
except ZeroDivisionError:
    print("No se puede dividir entre cero")
```

Un solo `except` para varios errores:

```python
try:
    ...
except (ValueError, TypeError):
    print("Dato inválido")
```

Atrapar cualquier error y ver cuál fue:

```python
try:
    x = 10 / 0
except Exception as e:
    print("Ocurrió un error:", e)       # division by zero
    print("Tipo:", type(e).__name__)    # ZeroDivisionError
```

> ⚠️ Evita `except:` sin tipo (atrapa **todo**, incluso errores que no esperabas y es difícil depurar). Sé específico siempre que puedas.

## 16.4 `else` y `finally`

```python
try:
    n = int(input("Número: "))
except ValueError:
    print("Inválido")
else:
    print("Todo bien, el número es", n)     # solo si NO hubo error
finally:
    print("Esto se ejecuta SIEMPRE")        # con o sin error
```

- `else`: se ejecuta si el `try` terminó sin errores.
- `finally`: se ejecuta **siempre** (útil para cerrar cosas, limpiar...).

## 16.5 Repetir hasta que el dato sea válido

Patrón **muy** usado:

```python
while True:
    try:
        edad = int(input("Edad: "))
        if edad < 0:
            print("No puede ser negativa")
            continue
        break
    except ValueError:
        print("Escribe un número entero")

print("Tu edad es", edad)
```

Convertido en función reutilizable:

```python
def pedir_entero(mensaje):
    while True:
        try:
            return int(input(mensaje))
        except ValueError:
            print("Entrada no válida, inténtalo de nuevo")

a = pedir_entero("Primer número: ")
b = pedir_entero("Segundo número: ")
print(a + b)
```

## 16.6 `raise`: lanzar tus propios errores

```python
def dividir(a, b):
    if b == 0:
        raise ValueError("El divisor no puede ser cero")
    return a / b

try:
    print(dividir(10, 0))
except ValueError as e:
    print("Error:", e)
```

```python
def validar_edad(edad):
    if edad < 0:
        raise ValueError("La edad no puede ser negativa")
    if edad > 120:
        raise ValueError("Edad poco realista")
    return edad
```

Errores propios (excepciones personalizadas):

```python
class SaldoInsuficiente(Exception):
    pass

def retirar(saldo, cantidad):
    if cantidad > saldo:
        raise SaldoInsuficiente("No tienes suficiente saldo")
    return saldo - cantidad

try:
    retirar(50, 100)
except SaldoInsuficiente as e:
    print(e)
```

## 16.7 `assert`: comprobar suposiciones

```python
def raiz_cuadrada(n):
    assert n >= 0, "n debe ser positivo"
    return n ** 0.5

print(raiz_cuadrada(9))   # 3.0
# raiz_cuadrada(-1)       # AssertionError: n debe ser positivo
```

## 16.8 Ejemplos completos

**Ejemplo A: calculadora a prueba de errores**

```python
try:
    a = float(input("A: "))
    b = float(input("B: "))
    print("Resultado:", a / b)
except ValueError:
    print("Escribe números válidos")
except ZeroDivisionError:
    print("No se puede dividir entre 0")
```

**Ejemplo B: leer un archivo de forma segura**

```python
nombre = input("Archivo a leer: ")
try:
    with open(nombre, encoding="utf-8") as f:
        print(f.read())
except FileNotFoundError:
    print("No encontré ese archivo")
except PermissionError:
    print("No tengo permiso para leerlo")
```

**Ejemplo C: convertir una lista de textos ignorando los inválidos**

```python
datos = ["10", "abc", "30", "", "50"]
numeros = []
for d in datos:
    try:
        numeros.append(int(d))
    except ValueError:
        print(f"Ignoro '{d}'")
print(numeros)   # [10, 30, 50]
```

**Ejemplo D: acceder a un índice con seguridad**

```python
lista = [1, 2, 3]
try:
    print(lista[5])
except IndexError:
    print("Ese índice no existe")
```

## 16.9 Resumen del Módulo 16

- `try` intenta; `except TipoError` reacciona.
- `else` si no hubo error; `finally` siempre.
- Sé específico con el tipo de error.
- `raise` lanza errores propios.
- Patrón: `while True` + `try` + `break` para validar entradas.

## 16.10 🎯 Ejercicios del Módulo 16

**Ejercicio 16.1** — Pide un número y muestra su doble. Si el usuario escribe algo que no es número, muestra `Número no válido`.

**Ejercicio 16.2** — Pide dos números y muestra el cociente; maneja la división entre cero y los valores no numéricos con dos `except`.

**Ejercicio 16.3** — Dada `lista = [10, 20, 30]`, pide un índice y muestra ese elemento. Si no existe, muestra `Índice fuera de rango`.

**Ejercicio 16.4** — Dado un diccionario de precios, pide un producto y muestra su precio; si no existe, muestra `Producto no encontrado` (hazlo con `try/except KeyError`).

**Ejercicio 16.5** — Haz una función `pedir_entero(mensaje)` que repita hasta que el usuario escriba un entero válido.

**Ejercicio 16.6** — Haz una función `pedir_entero_en_rango(mensaje, minimo, maximo)` que pida hasta que el número esté dentro del rango.

**Ejercicio 16.7** — Intenta abrir un archivo que pida el usuario y, si no existe, muestra un mensaje amable.

**Ejercicio 16.8** — Convierte esta lista a enteros ignorando los que no se puedan convertir: `["1", "dos", "3", "4.5", "5"]`.

**Ejercicio 16.9** — Crea una función `raiz(n)` que lance `ValueError` si `n < 0`; úsala dentro de un `try/except`.

**Ejercicio 16.10** — Escribe un programa con `try/except/else/finally` que pida un número y, pase lo que pase, muestre `Fin del programa`.

**Ejercicio 16.11** — Crea la excepción personalizada `EdadInvalida` y una función `registrar(edad)` que la lance si la edad no está entre 0 y 120.

### ✅ Soluciones del Módulo 16

**16.1**

```python
try:
    n = float(input("Número: "))
    print("Doble:", n * 2)
except ValueError:
    print("Número no válido")
```

**16.2**

```python
try:
    a = float(input("A: "))
    b = float(input("B: "))
    print(a / b)
except ValueError:
    print("Escribe números")
except ZeroDivisionError:
    print("No se puede dividir entre cero")
```

**16.3**

```python
lista = [10, 20, 30]
try:
    i = int(input("Índice: "))
    print(lista[i])
except IndexError:
    print("Índice fuera de rango")
except ValueError:
    print("Escribe un entero")
```

**16.4**

```python
precios = {"pan": 1.2, "leche": 0.9}
producto = input("Producto: ")
try:
    print(precios[producto])
except KeyError:
    print("Producto no encontrado")
```

**16.5**

```python
def pedir_entero(mensaje):
    while True:
        try:
            return int(input(mensaje))
        except ValueError:
            print("Debe ser un entero")

print(pedir_entero("Número: "))
```

**16.6**

```python
def pedir_entero_en_rango(mensaje, minimo, maximo):
    while True:
        try:
            n = int(input(mensaje))
        except ValueError:
            print("Debe ser un entero")
            continue
        if minimo <= n <= maximo:
            return n
        print(f"Debe estar entre {minimo} y {maximo}")

edad = pedir_entero_en_rango("Edad (0-120): ", 0, 120)
```

**16.7**

```python
nombre = input("Archivo: ")
try:
    with open(nombre, encoding="utf-8") as f:
        print(f.read())
except FileNotFoundError:
    print("Ese archivo no existe, revisa el nombre")
```

**16.8**

```python
resultado = []
for t in ["1", "dos", "3", "4.5", "5"]:
    try:
        resultado.append(int(t))
    except ValueError:
        pass
print(resultado)   # [1, 3, 5]
```

**16.9**

```python
def raiz(n):
    if n < 0:
        raise ValueError("No hay raíz real de un negativo")
    return n ** 0.5

try:
    print(raiz(16))
    print(raiz(-4))
except ValueError as e:
    print("Error:", e)
```

**16.10**

```python
try:
    n = int(input("Número: "))
except ValueError:
    print("No es un número")
else:
    print("Perfecto:", n)
finally:
    print("Fin del programa")
```

**16.11**

```python
class EdadInvalida(Exception):
    pass

def registrar(edad):
    if not 0 <= edad <= 120:
        raise EdadInvalida(f"La edad {edad} no es válida")
    print("Edad registrada:", edad)

try:
    registrar(25)
    registrar(300)
except EdadInvalida as e:
    print(e)
```

---

# MÓDULO 17 — Módulos y librería estándar

Python viene con una enorme colección de herramientas ya hechas (su **librería estándar**). Para usarlas, las **importas**.

## 17.1 Importar módulos

Un **módulo** es un archivo con funciones, variables y clases listas para usar.

```python
import math

print(math.sqrt(16))   # 4.0
print(math.pi)         # 3.141592653589793
```

**Formas de importar:**

```python
import math                    # usas math.sqrt(...)
from math import sqrt, pi      # usas sqrt(...) directamente
from math import *             # importa todo (¡evítalo!)
import math as m               # alias: m.sqrt(...)
```

```python
from math import sqrt
print(sqrt(25))    # 5.0

import random as r
print(r.randint(1, 6))
```

> 💡 Escribe siempre los `import` al **principio** del archivo.

Para ver qué tiene un módulo: `dir(math)` y `help(math.sqrt)`.

## 17.2 `math`: matemáticas

```python
import math

print(math.sqrt(49))        # 7.0   raíz cuadrada
print(math.pi)              # 3.14159...
print(math.e)               # 2.71828...
print(math.ceil(4.1))       # 5     redondea hacia arriba
print(math.floor(4.9))      # 4     redondea hacia abajo
print(math.factorial(5))    # 120
print(math.gcd(12, 18))     # 6     máximo común divisor
print(math.pow(2, 3))       # 8.0
print(math.sin(math.pi/2))  # 1.0
print(math.log10(1000))     # 3.0
print(math.hypot(3, 4))     # 5.0   hipotenusa
```

Ejemplo: área de un círculo.

```python
import math

radio = 3
area = math.pi * radio ** 2
print(round(area, 2))   # 28.27
```

## 17.3 `random`: números al azar

```python
import random

print(random.randint(1, 10))          # entero entre 1 y 10 (ambos incluidos)
print(random.random())                # decimal entre 0 y 1
print(random.uniform(1.5, 5.5))       # decimal entre 1.5 y 5.5

colores = ["rojo", "verde", "azul"]
print(random.choice(colores))         # uno al azar
print(random.sample(colores, 2))      # 2 distintos al azar
random.shuffle(colores)               # mezcla la lista (la modifica)
print(colores)
```

Simular un dado y una moneda:

```python
import random

print("Dado:", random.randint(1, 6))
print("Moneda:", random.choice(["cara", "cruz"]))
```

Para resultados repetibles (útil para probar):

```python
random.seed(42)
print(random.randint(1, 100))   # siempre el mismo número con esta semilla
```

## 17.4 `datetime`: fechas y horas

```python
from datetime import datetime, date, timedelta

ahora = datetime.now()
print(ahora)                          # 2025-03-09 14:30:12.345678
print(ahora.year, ahora.month, ahora.day)
print(ahora.hour, ahora.minute)

hoy = date.today()
print(hoy)                            # 2025-03-09
print(hoy.strftime("%d/%m/%Y"))       # 09/03/2025
print(hoy.strftime("%A"))             # día de la semana (en inglés)
```

Códigos de formato más usados: `%d` día, `%m` mes, `%Y` año (4 dígitos), `%H` hora, `%M` minutos, `%S` segundos.

**Sumar y restar fechas:**

```python
from datetime import date, timedelta

hoy = date.today()
en_una_semana = hoy + timedelta(days=7)
print(en_una_semana)

navidad = date(2025, 12, 25)
faltan = navidad - hoy
print(faltan.days, "días para Navidad")
```

**Crear una fecha desde texto:**

```python
from datetime import datetime

f = datetime.strptime("15/08/2025", "%d/%m/%Y")
print(f.year, f.month, f.day)   # 2025 8 15
```

**Calcular la edad:**

```python
from datetime import date

nacimiento = date(2000, 5, 20)
hoy = date.today()
edad = hoy.year - nacimiento.year
if (hoy.month, hoy.day) < (nacimiento.month, nacimiento.day):
    edad -= 1
print("Edad:", edad)
```

## 17.5 `time`

```python
import time

print("Espera 2 segundos...")
time.sleep(2)
print("¡Listo!")

inicio = time.time()
suma = sum(range(1_000_000))
fin = time.time()
print(f"Tardó {fin - inicio:.4f} segundos")
```

## 17.6 `collections`: colecciones especiales

**`Counter`: contar elementos fácilmente**

```python
from collections import Counter

c = Counter("abracadabra")
print(c)                      # Counter({'a': 5, 'b': 2, 'r': 2, 'c': 1, 'd': 1})
print(c["a"])                 # 5
print(c.most_common(2))       # [('a', 5), ('b', 2)]

palabras = "el gato y el perro y el pez".split()
print(Counter(palabras).most_common(1))   # [('el', 3)]
```

**`defaultdict`: diccionario con valor por defecto**

```python
from collections import defaultdict

grupos = defaultdict(list)
for palabra in ["sol", "luna", "mar", "cielo"]:
    grupos[len(palabra)].append(palabra)
print(dict(grupos))   # {3: ['sol', 'mar'], 4: ['luna'], 5: ['cielo']}
```

**`deque`: cola eficiente**

```python
from collections import deque

cola = deque([1, 2, 3])
cola.append(4)         # añade a la derecha
cola.appendleft(0)     # añade a la izquierda
print(cola)            # deque([0, 1, 2, 3, 4])
print(cola.popleft())  # 0  (saca por la izquierda)
```

## 17.7 `itertools` (un vistazo)

```python
from itertools import permutations, combinations

print(list(permutations([1, 2, 3], 2)))
# [(1, 2), (1, 3), (2, 1), (2, 3), (3, 1), (3, 2)]

print(list(combinations([1, 2, 3], 2)))
# [(1, 2), (1, 3), (2, 3)]
```

## 17.8 `os` y `sys`

```python
import os
import sys

print(os.getcwd())               # carpeta actual
print(os.listdir("."))           # archivos de la carpeta
print(sys.version)               # versión de Python
print(sys.argv)                  # argumentos al ejecutar el script
```

## 17.9 `string`

```python
import string

print(string.ascii_lowercase)   # abcdefghijklmnopqrstuvwxyz
print(string.ascii_uppercase)
print(string.digits)            # 0123456789
print(string.punctuation)       # !"#$%&'()*+,-./:;<=>?@[\]^_`{|}~
```

Generador de contraseñas:

```python
import random
import string

caracteres = string.ascii_letters + string.digits
clave = "".join(random.choice(caracteres) for _ in range(10))
print(clave)
```

## 17.10 Crear tu propio módulo

Cualquier archivo `.py` es un módulo. Crea `utilidades.py`:

```python
# utilidades.py
def saludar(nombre):
    return f"Hola, {nombre}"

def cuadrado(n):
    return n ** 2

PI = 3.14159
```

En otro archivo, **en la misma carpeta**, `principal.py`:

```python
import utilidades

print(utilidades.saludar("Ana"))
print(utilidades.cuadrado(4))
print(utilidades.PI)

# o también:
from utilidades import saludar
print(saludar("Luis"))
```

### `if __name__ == "__main__":`

Sirve para que cierto código se ejecute **solo cuando corres el archivo directamente**, no cuando lo importas:

```python
# utilidades.py
def saludar(nombre):
    return f"Hola, {nombre}"

if __name__ == "__main__":
    # Esto solo corre si ejecutas: python utilidades.py
    print(saludar("prueba"))
```

Es la forma estándar de estructurar un programa:

```python
def main():
    print("Mi programa")

if __name__ == "__main__":
    main()
```

## 17.11 Ejemplos completos

**Ejemplo A: adivina el número (con azar)**

```python
import random

secreto = random.randint(1, 20)
intentos = 0

while True:
    intento = int(input("Adivina (1-20): "))
    intentos += 1
    if intento < secreto:
        print("Más alto")
    elif intento > secreto:
        print("Más bajo")
    else:
        print(f"¡Acertaste en {intentos} intentos!")
        break
```

**Ejemplo B: piedra, papel o tijera**

```python
import random

opciones = ["piedra", "papel", "tijera"]
jugador = input("piedra, papel o tijera: ").lower()
pc = random.choice(opciones)
print("La computadora eligió", pc)

if jugador == pc:
    print("Empate")
elif (jugador, pc) in [("piedra", "tijera"), ("papel", "piedra"), ("tijera", "papel")]:
    print("¡Ganaste!")
else:
    print("Perdiste")
```

**Ejemplo C: días hasta tu cumpleaños**

```python
from datetime import date

hoy = date.today()
cumple = date(hoy.year, 12, 31)
if cumple < hoy:
    cumple = date(hoy.year + 1, 12, 31)
print("Faltan", (cumple - hoy).days, "días")
```

**Ejemplo D: palabra más repetida**

```python
from collections import Counter

texto = "el sol sale y el sol se oculta y el cielo se pinta"
mas_comun = Counter(texto.split()).most_common(1)[0]
print(mas_comun)   # ('el', 3)
```

## 17.12 Resumen del Módulo 17

- `import modulo` / `from modulo import cosa` / `import modulo as alias`.
- `math`, `random`, `datetime`, `time`, `collections`, `os`, `string`: herramientas listas para usar.
- Tus propios archivos `.py` son módulos.
- `if __name__ == "__main__":` separa "ejecutar" de "importar".

## 17.13 🎯 Ejercicios del Módulo 17

**Ejercicio 17.1** — Calcula la raíz cuadrada de 144 y el factorial de 6 con `math`.

**Ejercicio 17.2** — Pide el radio y muestra el área y el perímetro de un círculo con `math.pi` (2 decimales).

**Ejercicio 17.3** — Redondea hacia arriba y hacia abajo el número `7.3` con `math`.

**Ejercicio 17.4** — Simula 5 tiradas de un dado y muéstralas.

**Ejercicio 17.5** — Elige un nombre al azar de `["Ana", "Luis", "Eva", "Pedro"]`.

**Ejercicio 17.6** — Genera una lista de 5 números aleatorios entre 1 y 100 y muestra el mayor.

**Ejercicio 17.7** — Muestra la fecha de hoy en formato `dd/mm/aaaa`.

**Ejercicio 17.8** — Calcula cuántos días faltan para el 1 de enero del próximo año.

**Ejercicio 17.9** — Usa `Counter` para saber cuál es la letra más repetida de `"mississippi"`.

**Ejercicio 17.10** — Genera una contraseña aleatoria de 8 caracteres con letras y números.

**Ejercicio 17.11** — Crea un módulo `mate.py` con funciones `suma`, `resta` y `es_par`, e impórtalo desde otro archivo para probarlas.

**Ejercicio 17.12** — Haz un programa que simule el lanzamiento de 100 monedas y cuente cuántas veces salió cara y cruz.

**Ejercicio 17.13** — Mide cuánto tarda en sumarse `sum(range(5_000_000))` con `time`.

### ✅ Soluciones del Módulo 17

**17.1**

```python
import math
print(math.sqrt(144))      # 12.0
print(math.factorial(6))   # 720
```

**17.2**

```python
import math
r = float(input("Radio: "))
print(f"Área: {math.pi * r ** 2:.2f}")
print(f"Perímetro: {2 * math.pi * r:.2f}")
```

**17.3**

```python
import math
print(math.ceil(7.3))    # 8
print(math.floor(7.3))   # 7
```

**17.4**

```python
import random
for _ in range(5):
    print(random.randint(1, 6))
```

**17.5**

```python
import random
print(random.choice(["Ana", "Luis", "Eva", "Pedro"]))
```

**17.6**

```python
import random
numeros = [random.randint(1, 100) for _ in range(5)]
print(numeros)
print("Mayor:", max(numeros))
```

**17.7**

```python
from datetime import date
print(date.today().strftime("%d/%m/%Y"))
```

**17.8**

```python
from datetime import date
hoy = date.today()
proximo = date(hoy.year + 1, 1, 1)
print((proximo - hoy).days)
```

**17.9**

```python
from collections import Counter
print(Counter("mississippi").most_common(1))   # [('i', 4)] (empata con 's', sale la primera vista)
```

**17.10**

```python
import random, string
caracteres = string.ascii_letters + string.digits
print("".join(random.choice(caracteres) for _ in range(8)))
```

**17.11**

`mate.py`:

```python
def suma(a, b):
    return a + b

def resta(a, b):
    return a - b

def es_par(n):
    return n % 2 == 0
```

`prueba.py`:

```python
import mate
print(mate.suma(2, 3))     # 5
print(mate.resta(9, 4))    # 5
print(mate.es_par(10))     # True
```

**17.12**

```python
import random
caras = 0
cruces = 0
for _ in range(100):
    if random.choice(["cara", "cruz"]) == "cara":
        caras += 1
    else:
        cruces += 1
print("Caras:", caras, "Cruces:", cruces)
```

**17.13**

```python
import time
inicio = time.time()
total = sum(range(5_000_000))
print(total)
print(f"Tardó {time.time() - inicio:.3f} s")
```

---

# MÓDULO 18 — Programación orientada a objetos (I): clases y objetos

Hasta ahora usabas funciones y datos por separado. En la **programación orientada a objetos (POO)** juntas **datos** y **funciones** en una sola cosa: un **objeto**.

## 18.1 La idea con un ejemplo cotidiano

Piensa en un **plano de una casa** y en **las casas** construidas con ese plano.

- El **plano** = la **clase** (la plantilla, la receta, el molde).
- Cada **casa construida** = un **objeto** (o *instancia*).

De un mismo plano puedes construir muchas casas: cada una con su propio color, dueño, dirección (sus **atributos**), pero con las mismas capacidades (abrir puerta, encender luz: sus **métodos**).

Otro ejemplo: la clase `Perro`.

- **Atributos** (lo que tiene): nombre, edad, raza.
- **Métodos** (lo que hace): ladrar, comer, dormir.
- **Objetos**: `mi_perro` (Toby, 3 años), `tu_perro` (Luna, 5 años).

Ya usas objetos sin saberlo: un `str` es un objeto con métodos (`"hola".upper()`) y una `list` también (`lista.append(3)`).

## 18.2 Tu primera clase

```python
class Perro:
    pass          # clase vacía

toby = Perro()    # creamos un objeto
print(type(toby))   # <class '__main__.Perro'>
```

Una clase de verdad lleva un **constructor** (`__init__`) para dar datos iniciales:

```python
class Perro:
    def __init__(self, nombre, edad):
        self.nombre = nombre
        self.edad = edad

toby = Perro("Toby", 3)
luna = Perro("Luna", 5)

print(toby.nombre)   # Toby
print(luna.edad)     # 5
```

**Desglosado:**

- `class Perro:` → define la plantilla (el nombre de las clases se escribe con **MayúsculaInicial**).
- `__init__` → método especial que se ejecuta **automáticamente** al crear el objeto.
- `self` → "este objeto en particular". Siempre es el primer parámetro de los métodos. **No** lo pasas tú al llamar: Python lo pone.
- `self.nombre = nombre` → guarda el dato **dentro del objeto** (es un atributo).

Cuando escribes `Perro("Toby", 3)`, Python hace algo como:

1. Crea un objeto vacío.
2. Llama a `__init__(objeto, "Toby", 3)`.
3. Lo devuelve.

## 18.3 Métodos

Un **método** es una función dentro de una clase.

```python
class Perro:
    def __init__(self, nombre, edad):
        self.nombre = nombre
        self.edad = edad

    def ladrar(self):
        print(f"{self.nombre} dice: ¡Guau!")

    def cumplir_anios(self):
        self.edad += 1

    def presentarse(self):
        return f"Soy {self.nombre} y tengo {self.edad} años"

toby = Perro("Toby", 3)
toby.ladrar()                # Toby dice: ¡Guau!
toby.cumplir_anios()
print(toby.presentarse())    # Soy Toby y tengo 4 años
```

Cada objeto tiene **sus propios datos**:

```python
luna = Perro("Luna", 5)
luna.ladrar()                # Luna dice: ¡Guau!
print(toby.edad, luna.edad)  # 4 5
```

## 18.4 Atributos: leer y cambiar

```python
toby = Perro("Toby", 3)

print(toby.nombre)     # leer
toby.nombre = "Tobi"   # modificar
toby.color = "negro"   # (Python permite crear atributos nuevos al vuelo)
print(toby.color)
```

## 18.5 Atributos por defecto

```python
class Jugador:
    def __init__(self, nombre):
        self.nombre = nombre
        self.vida = 100          # valor inicial fijo
        self.puntos = 0
        self.inventario = []     # cada jugador tiene SU lista

    def recibir_dano(self, cantidad):
        self.vida -= cantidad
        if self.vida < 0:
            self.vida = 0

    def ganar_puntos(self, n):
        self.puntos += n

    def recoger(self, objeto):
        self.inventario.append(objeto)

    def estado(self):
        return f"{self.nombre}: vida={self.vida}, puntos={self.puntos}, objetos={self.inventario}"

j = Jugador("Ana")
j.recibir_dano(30)
j.ganar_puntos(50)
j.recoger("espada")
print(j.estado())   # Ana: vida=70, puntos=50, objetos=['espada']
```

## 18.6 `__str__`: cómo se muestra un objeto

Sin él, `print(objeto)` muestra algo feo:

```python
class Punto:
    def __init__(self, x, y):
        self.x = x
        self.y = y

p = Punto(3, 4)
print(p)    # <__main__.Punto object at 0x...>
```

Con `__str__` decides cómo se ve:

```python
class Punto:
    def __init__(self, x, y):
        self.x = x
        self.y = y

    def __str__(self):
        return f"({self.x}, {self.y})"

p = Punto(3, 4)
print(p)           # (3, 4)
print(f"El punto es {p}")
```

## 18.7 Atributos de clase vs atributos de instancia

```python
class Gato:
    especie = "Felis catus"      # atributo de CLASE: compartido por todos

    def __init__(self, nombre):
        self.nombre = nombre     # atributo de INSTANCIA: propio de cada gato

a = Gato("Misu")
b = Gato("Tom")
print(a.especie, b.especie)    # Felis catus Felis catus
print(a.nombre, b.nombre)      # Misu Tom
```

Contar cuántos objetos se han creado:

```python
class Coche:
    total = 0

    def __init__(self, marca):
        self.marca = marca
        Coche.total += 1

Coche("Toyota")
Coche("Ford")
print(Coche.total)   # 2
```

## 18.8 Ejemplo completo: cuenta bancaria

```python
class CuentaBancaria:
    def __init__(self, titular, saldo=0):
        self.titular = titular
        self.saldo = saldo

    def depositar(self, cantidad):
        if cantidad <= 0:
            print("La cantidad debe ser positiva")
            return
        self.saldo += cantidad

    def retirar(self, cantidad):
        if cantidad > self.saldo:
            print("Saldo insuficiente")
            return
        self.saldo -= cantidad

    def mostrar(self):
        print(f"Titular: {self.titular} | Saldo: {self.saldo}")

cuenta = CuentaBancaria("Ana", 100)
cuenta.depositar(50)
cuenta.retirar(30)
cuenta.retirar(500)     # Saldo insuficiente
cuenta.mostrar()        # Titular: Ana | Saldo: 120
```

## 18.9 Más ejemplos de clases

**Rectángulo**

```python
class Rectangulo:
    def __init__(self, base, altura):
        self.base = base
        self.altura = altura

    def area(self):
        return self.base * self.altura

    def perimetro(self):
        return 2 * (self.base + self.altura)

r = Rectangulo(3, 5)
print(r.area())        # 15
print(r.perimetro())   # 16
```

**Contador**

```python
class Contador:
    def __init__(self):
        self.valor = 0

    def sumar(self):
        self.valor += 1

    def reiniciar(self):
        self.valor = 0

c = Contador()
c.sumar()
c.sumar()
print(c.valor)   # 2
c.reiniciar()
print(c.valor)   # 0
```

**Estudiante**

```python
class Estudiante:
    def __init__(self, nombre):
        self.nombre = nombre
        self.notas = []

    def agregar_nota(self, nota):
        self.notas.append(nota)

    def promedio(self):
        if not self.notas:
            return 0
        return sum(self.notas) / len(self.notas)

e = Estudiante("Luis")
e.agregar_nota(8)
e.agregar_nota(6)
print(e.promedio())   # 7.0
```

## 18.10 ⚠️ Errores comunes

```python
class A:
    def __init__(nombre):          # ❌ falta self
        ...

class B:
    def __init__(self, nombre):
        nombre = nombre            # ❌ no guarda nada: falta self.
        # correcto: self.nombre = nombre

class C:
    def saludar():                 # ❌ falta self: TypeError al llamarlo
        print("hola")
```

## 18.11 Resumen del Módulo 18

- **Clase** = plantilla. **Objeto** = ejemplar creado a partir de ella.
- `__init__` es el constructor; `self` es "este objeto".
- **Atributos**: datos del objeto (`self.x`). **Métodos**: funciones del objeto.
- `__str__` define cómo se imprime.
- Cada objeto tiene sus propios datos.

## 18.12 🎯 Ejercicios del Módulo 18

**Ejercicio 18.1** — Crea una clase `Persona` con `nombre` y `edad`. Crea dos personas y muestra sus nombres.

**Ejercicio 18.2** — Agrega a `Persona` un método `saludar()` que muestre `Hola, soy <nombre>`.

**Ejercicio 18.3** — Agrega a `Persona` el método `cumplir_anios()` que sume 1 a la edad. Compruébalo.

**Ejercicio 18.4** — Crea una clase `Circulo` con `radio` y métodos `area()` y `perimetro()`.

**Ejercicio 18.5** — Crea una clase `Cuadrado` con `lado` y métodos `area()` y `perimetro()`.

**Ejercicio 18.6** — Crea una clase `Producto` (nombre, precio) y un método `con_descuento(porcentaje)` que devuelva el precio con descuento.

**Ejercicio 18.7** — Añade `__str__` a `Producto` para que `print(producto)` muestre `Pan - 1.20 €`.

**Ejercicio 18.8** — Crea una clase `Contador` con `incrementar()`, `decrementar()` y `valor`.

**Ejercicio 18.9** — Crea una clase `Libro` con título, autor y páginas; un método `descripcion()` que devuelva un texto con los tres datos.

**Ejercicio 18.10** — Crea la clase `CuentaBancaria` del módulo, pero con un historial: cada depósito o retiro se guarda en una lista `movimientos`.

**Ejercicio 18.11** — Crea una clase `Lista_Compra` con una lista de productos, un método `agregar`, `quitar` y `mostrar`.

**Ejercicio 18.12** — Crea una clase `Termostato` con una temperatura inicial y métodos `subir(grados)` y `bajar(grados)` que no permitan bajar de 5 ni subir de 35.

### ✅ Soluciones del Módulo 18

**18.1**

```python
class Persona:
    def __init__(self, nombre, edad):
        self.nombre = nombre
        self.edad = edad

p1 = Persona("Ana", 20)
p2 = Persona("Luis", 25)
print(p1.nombre, p2.nombre)
```

**18.2**

```python
class Persona:
    def __init__(self, nombre, edad):
        self.nombre = nombre
        self.edad = edad

    def saludar(self):
        print(f"Hola, soy {self.nombre}")

Persona("Ana", 20).saludar()
```

**18.3**

```python
class Persona:
    def __init__(self, nombre, edad):
        self.nombre = nombre
        self.edad = edad

    def cumplir_anios(self):
        self.edad += 1

p = Persona("Ana", 20)
p.cumplir_anios()
print(p.edad)   # 21
```

**18.4**

```python
import math

class Circulo:
    def __init__(self, radio):
        self.radio = radio

    def area(self):
        return math.pi * self.radio ** 2

    def perimetro(self):
        return 2 * math.pi * self.radio

c = Circulo(2)
print(round(c.area(), 2), round(c.perimetro(), 2))   # 12.57 12.57
```

**18.5**

```python
class Cuadrado:
    def __init__(self, lado):
        self.lado = lado

    def area(self):
        return self.lado ** 2

    def perimetro(self):
        return 4 * self.lado

c = Cuadrado(4)
print(c.area(), c.perimetro())   # 16 16
```

**18.6**

```python
class Producto:
    def __init__(self, nombre, precio):
        self.nombre = nombre
        self.precio = precio

    def con_descuento(self, porcentaje):
        return self.precio * (1 - porcentaje / 100)

p = Producto("Pan", 2)
print(p.con_descuento(25))   # 1.5
```

**18.7**

```python
class Producto:
    def __init__(self, nombre, precio):
        self.nombre = nombre
        self.precio = precio

    def __str__(self):
        return f"{self.nombre} - {self.precio:.2f} €"

print(Producto("Pan", 1.2))   # Pan - 1.20 €
```

**18.8**

```python
class Contador:
    def __init__(self):
        self.valor = 0

    def incrementar(self):
        self.valor += 1

    def decrementar(self):
        self.valor -= 1

c = Contador()
c.incrementar()
c.incrementar()
c.decrementar()
print(c.valor)   # 1
```

**18.9**

```python
class Libro:
    def __init__(self, titulo, autor, paginas):
        self.titulo = titulo
        self.autor = autor
        self.paginas = paginas

    def descripcion(self):
        return f"'{self.titulo}' de {self.autor} ({self.paginas} páginas)"

print(Libro("Don Quijote", "Cervantes", 900).descripcion())
```

**18.10**

```python
class CuentaBancaria:
    def __init__(self, titular, saldo=0):
        self.titular = titular
        self.saldo = saldo
        self.movimientos = []

    def depositar(self, cantidad):
        self.saldo += cantidad
        self.movimientos.append(f"+{cantidad}")

    def retirar(self, cantidad):
        if cantidad > self.saldo:
            print("Saldo insuficiente")
            return
        self.saldo -= cantidad
        self.movimientos.append(f"-{cantidad}")

c = CuentaBancaria("Ana", 100)
c.depositar(50)
c.retirar(30)
print(c.saldo, c.movimientos)   # 120 ['+50', '-30']
```

**18.11**

```python
class ListaCompra:
    def __init__(self):
        self.productos = []

    def agregar(self, producto):
        self.productos.append(producto)

    def quitar(self, producto):
        if producto in self.productos:
            self.productos.remove(producto)

    def mostrar(self):
        for i, p in enumerate(self.productos, start=1):
            print(f"{i}. {p}")

lista = ListaCompra()
lista.agregar("pan")
lista.agregar("leche")
lista.quitar("pan")
lista.mostrar()   # 1. leche
```

**18.12**

```python
class Termostato:
    def __init__(self, temperatura=20):
        self.temperatura = temperatura

    def subir(self, grados):
        self.temperatura = min(35, self.temperatura + grados)

    def bajar(self, grados):
        self.temperatura = max(5, self.temperatura - grados)

t = Termostato()
t.subir(30)
print(t.temperatura)   # 35
t.bajar(100)
print(t.temperatura)   # 5
```

---

# MÓDULO 19 — Programación orientada a objetos (II)

## 19.1 Herencia: clases que heredan de otras

Una clase **hija** puede **heredar** todo lo de una clase **padre** y añadir o cambiar cosas. Es como en una familia: un hijo hereda rasgos de sus padres pero también tiene los suyos.

```python
class Animal:
    def __init__(self, nombre):
        self.nombre = nombre

    def comer(self):
        print(f"{self.nombre} está comiendo")

    def hacer_sonido(self):
        print("...")

class Perro(Animal):                 # Perro hereda de Animal
    def hacer_sonido(self):
        print("¡Guau!")

class Gato(Animal):
    def hacer_sonido(self):
        print("¡Miau!")

toby = Perro("Toby")
misu = Gato("Misu")

toby.comer()           # Toby está comiendo      (heredado de Animal)
toby.hacer_sonido()    # ¡Guau!                  (propio de Perro)
misu.hacer_sonido()    # ¡Miau!
```

- `class Perro(Animal):` → `Perro` hereda de `Animal`.
- `Perro` no definió `__init__` ni `comer`: los **heredó**.
- `hacer_sonido` se **sobrescribió** (override): cada hijo lo hace a su manera.

## 19.2 `super()`: reutilizar lo del padre

Si la hija necesita más datos, llama al constructor del padre con `super()`:

```python
class Animal:
    def __init__(self, nombre):
        self.nombre = nombre

class Perro(Animal):
    def __init__(self, nombre, raza):
        super().__init__(nombre)     # el padre guarda el nombre
        self.raza = raza             # la hija guarda la raza

    def presentarse(self):
        print(f"Soy {self.nombre}, un {self.raza}")

d = Perro("Toby", "labrador")
d.presentarse()   # Soy Toby, un labrador
```

También se usa para **extender** un método en vez de reemplazarlo:

```python
class Empleado:
    def __init__(self, nombre, sueldo):
        self.nombre = nombre
        self.sueldo = sueldo

    def describir(self):
        return f"{self.nombre} cobra {self.sueldo}"

class Jefe(Empleado):
    def __init__(self, nombre, sueldo, equipo):
        super().__init__(nombre, sueldo)
        self.equipo = equipo

    def describir(self):
        base = super().describir()
        return f"{base} y dirige a {len(self.equipo)} personas"

j = Jefe("Marta", 3000, ["Ana", "Luis"])
print(j.describir())   # Marta cobra 3000 y dirige a 2 personas
```

## 19.3 Polimorfismo: distintos objetos, mismo método

"Muchas formas": puedes tratar objetos distintos de la misma manera si todos tienen el mismo método.

```python
class Figura:
    def area(self):
        return 0

class Cuadrado(Figura):
    def __init__(self, lado):
        self.lado = lado
    def area(self):
        return self.lado ** 2

class Rectangulo(Figura):
    def __init__(self, base, altura):
        self.base = base
        self.altura = altura
    def area(self):
        return self.base * self.altura

class Circulo(Figura):
    def __init__(self, radio):
        self.radio = radio
    def area(self):
        return 3.14159 * self.radio ** 2

figuras = [Cuadrado(2), Rectangulo(3, 4), Circulo(1)]
for f in figuras:
    print(type(f).__name__, "→", round(f.area(), 2))
```

```text
Cuadrado → 4
Rectangulo → 12
Circulo → 3.14
```

No importa el tipo concreto: todos responden a `.area()`.

## 19.4 `isinstance` e `issubclass`

```python
toby = Perro("Toby", "labrador")
print(isinstance(toby, Perro))     # True
print(isinstance(toby, Animal))    # True  (un Perro ES un Animal)
print(isinstance(toby, str))       # False
print(issubclass(Perro, Animal))   # True
```

## 19.5 Métodos especiales ("mágicos" o *dunder*)

Son métodos con doble guion bajo que permiten que tus objetos funcionen con operadores y funciones de Python.

| Método | Se activa con |
|--------|---------------|
| `__init__` | `Clase(...)` |
| `__str__` | `print(obj)`, `str(obj)` |
| `__repr__` | representación técnica (consola, depuración) |
| `__len__` | `len(obj)` |
| `__add__` | `obj1 + obj2` |
| `__eq__` | `obj1 == obj2` |
| `__lt__` | `obj1 < obj2` |
| `__getitem__` | `obj[i]` |
| `__contains__` | `x in obj` |

```python
class Vector:
    def __init__(self, x, y):
        self.x = x
        self.y = y

    def __str__(self):
        return f"Vector({self.x}, {self.y})"

    def __add__(self, otro):
        return Vector(self.x + otro.x, self.y + otro.y)

    def __eq__(self, otro):
        return self.x == otro.x and self.y == otro.y

    def __mul__(self, n):
        return Vector(self.x * n, self.y * n)

a = Vector(1, 2)
b = Vector(3, 4)
print(a + b)         # Vector(4, 6)
print(a * 3)         # Vector(3, 6)
print(a == Vector(1, 2))   # True
```

Otro ejemplo: una colección propia.

```python
class Playlist:
    def __init__(self):
        self.canciones = []

    def agregar(self, cancion):
        self.canciones.append(cancion)

    def __len__(self):
        return len(self.canciones)

    def __getitem__(self, i):
        return self.canciones[i]

    def __contains__(self, cancion):
        return cancion in self.canciones

p = Playlist()
p.agregar("Tema A")
p.agregar("Tema B")
print(len(p))            # 2
print(p[0])              # Tema A
print("Tema B" in p)     # True
for c in p:              # funciona gracias a __getitem__
    print(c)
```

`__repr__`:

```python
class Punto:
    def __init__(self, x, y):
        self.x, self.y = x, y

    def __repr__(self):
        return f"Punto({self.x}, {self.y})"

lista = [Punto(1, 2), Punto(3, 4)]
print(lista)   # [Punto(1, 2), Punto(3, 4)]
```

## 19.6 Encapsulación: atributos "privados"

Por convención, un nombre que empieza con `_` significa "es interno, no lo toques". Con `__` (doble guion bajo) Python lo "esconde" más.

```python
class Cuenta:
    def __init__(self, saldo):
        self.__saldo = saldo      # "privado"

    def ver_saldo(self):
        return self.__saldo

    def depositar(self, n):
        if n > 0:
            self.__saldo += n

c = Cuenta(100)
c.depositar(50)
print(c.ver_saldo())    # 150
# print(c.__saldo)      # ❌ AttributeError
```

## 19.7 `@property`: atributos con control

Permite que un método se use **como si fuera un atributo**, para validar o calcular:

```python
class Persona:
    def __init__(self, nombre, edad):
        self.nombre = nombre
        self._edad = edad

    @property
    def edad(self):
        return self._edad

    @edad.setter
    def edad(self, valor):
        if valor < 0:
            raise ValueError("La edad no puede ser negativa")
        self._edad = valor

p = Persona("Ana", 20)
print(p.edad)     # 20   (se usa como atributo)
p.edad = 21       # llama al setter
# p.edad = -5     # ValueError
```

Propiedad calculada:

```python
class Rectangulo:
    def __init__(self, base, altura):
        self.base = base
        self.altura = altura

    @property
    def area(self):
        return self.base * self.altura

r = Rectangulo(3, 4)
print(r.area)   # 12  (sin paréntesis)
```

## 19.8 Métodos de clase y estáticos

```python
class Fecha:
    def __init__(self, dia, mes, anio):
        self.dia, self.mes, self.anio = dia, mes, anio

    @classmethod
    def desde_texto(cls, texto):          # otra forma de crear objetos
        d, m, a = texto.split("/")
        return cls(int(d), int(m), int(a))

    @staticmethod
    def es_bisiesto(anio):                # no usa ni self ni cls
        return (anio % 4 == 0 and anio % 100 != 0) or anio % 400 == 0

f = Fecha.desde_texto("15/08/2025")
print(f.dia, f.mes, f.anio)       # 15 8 2025
print(Fecha.es_bisiesto(2024))    # True
```

## 19.9 `dataclass`: clases de datos sin escribir tanto

```python
from dataclasses import dataclass

@dataclass
class Punto:
    x: int
    y: int

p = Punto(3, 4)
print(p)                 # Punto(x=3, y=4)
print(p.x)               # 3
print(p == Punto(3, 4))  # True
```

Con valores por defecto:

```python
from dataclasses import dataclass, field

@dataclass
class Alumno:
    nombre: str
    nota: float = 0.0
    materias: list = field(default_factory=list)

a = Alumno("Ana")
a.materias.append("mates")
print(a)   # Alumno(nombre='Ana', nota=0.0, materias=['mates'])
```

`@dataclass` genera `__init__`, `__repr__` y `__eq__` por ti.

## 19.10 Composición: "tiene un" en vez de "es un"

No todo es herencia. Si un objeto **tiene** otros objetos, usa composición:

```python
class Motor:
    def encender(self):
        return "Motor encendido"

class Coche:
    def __init__(self):
        self.motor = Motor()      # un coche TIENE un motor

    def arrancar(self):
        return self.motor.encender()

print(Coche().arrancar())   # Motor encendido
```

> 💡 Pregunta clave: ¿"Un perro **es un** animal"? → herencia. ¿"Un coche **tiene un** motor"? → composición.

## 19.11 Ejemplo completo: tienda con objetos

```python
class Producto:
    def __init__(self, nombre, precio):
        self.nombre = nombre
        self.precio = precio

    def __str__(self):
        return f"{self.nombre} ({self.precio:.2f} €)"

class Carrito:
    def __init__(self):
        self.items = []

    def agregar(self, producto, cantidad=1):
        self.items.append((producto, cantidad))

    def total(self):
        return sum(p.precio * c for p, c in self.items)

    def mostrar(self):
        for p, c in self.items:
            print(f"{c} x {p}")
        print(f"TOTAL: {self.total():.2f} €")

carrito = Carrito()
carrito.agregar(Producto("Pan", 1.2), 2)
carrito.agregar(Producto("Leche", 0.9))
carrito.mostrar()
```

```text
2 x Pan (1.20 €)
1 x Leche (0.90 €)
TOTAL: 3.30 €
```

## 19.12 Resumen del Módulo 19

- **Herencia:** `class Hija(Padre):`; `super()` accede al padre.
- **Polimorfismo:** mismo método, distinto comportamiento.
- Métodos especiales: `__str__`, `__repr__`, `__len__`, `__add__`, `__eq__`...
- `@property` para atributos controlados; `@classmethod` / `@staticmethod`.
- `@dataclass` para clases que solo guardan datos.
- **Composición** cuando un objeto "tiene" otros.

## 19.13 🎯 Ejercicios del Módulo 19

**Ejercicio 19.1** — Crea `Vehiculo` (marca) con un método `describir()`, y `Coche` que herede de él y añada `puertas`.

**Ejercicio 19.2** — Crea `Animal` con `hacer_sonido()` y las hijas `Vaca` (`Muuu`) y `Pato` (`Cuac`). Recorre una lista con una de cada una.

**Ejercicio 19.3** — Crea `Empleado` (nombre, sueldo) y `Gerente` que herede y añada un `bonus`; el método `sueldo_total()` del gerente devuelve sueldo + bonus.

**Ejercicio 19.4** — Crea `Figura` con `area()` y las hijas `Triangulo` y `Cuadrado`. Muestra el área de una lista de figuras.

**Ejercicio 19.5** — Añade `__str__` a una clase `Fraccion` (numerador, denominador) para mostrar `3/4`.

**Ejercicio 19.6** — Añade `__add__` a `Fraccion` para sumar dos fracciones con el mismo denominador.

**Ejercicio 19.7** — Crea una clase `Libro` con `__len__` que devuelva el número de páginas.

**Ejercicio 19.8** — Crea una clase `Termometro` con una propiedad `fahrenheit` que se calcule a partir de `celsius`.

**Ejercicio 19.9** — Crea una `dataclass` llamada `Pelicula` con título, año y nota (por defecto 0).

**Ejercicio 19.10** — Crea una clase `CuentaAhorro` que herede de `CuentaBancaria` y añada un método `aplicar_interes(porcentaje)`.

**Ejercicio 19.11** — Con composición, crea una clase `Equipo` que contenga una lista de objetos `Jugador` y un método que devuelva el número de jugadores.

**Ejercicio 19.12** — Usa `isinstance` para recorrer `[1, "hola", 3.5, [1, 2]]` y mostrar el tipo de cada elemento en texto (`entero`, `texto`, `decimal`, `lista`).

### ✅ Soluciones del Módulo 19

**19.1**

```python
class Vehiculo:
    def __init__(self, marca):
        self.marca = marca

    def describir(self):
        return f"Vehículo marca {self.marca}"

class Coche(Vehiculo):
    def __init__(self, marca, puertas):
        super().__init__(marca)
        self.puertas = puertas

    def describir(self):
        return f"Coche {self.marca} de {self.puertas} puertas"

print(Coche("Toyota", 4).describir())
```

**19.2**

```python
class Animal:
    def hacer_sonido(self):
        print("...")

class Vaca(Animal):
    def hacer_sonido(self):
        print("Muuu")

class Pato(Animal):
    def hacer_sonido(self):
        print("Cuac")

for a in [Vaca(), Pato()]:
    a.hacer_sonido()
```

**19.3**

```python
class Empleado:
    def __init__(self, nombre, sueldo):
        self.nombre = nombre
        self.sueldo = sueldo

class Gerente(Empleado):
    def __init__(self, nombre, sueldo, bonus):
        super().__init__(nombre, sueldo)
        self.bonus = bonus

    def sueldo_total(self):
        return self.sueldo + self.bonus

print(Gerente("Marta", 2000, 500).sueldo_total())   # 2500
```

**19.4**

```python
class Figura:
    def area(self):
        return 0

class Triangulo(Figura):
    def __init__(self, base, altura):
        self.base, self.altura = base, altura
    def area(self):
        return self.base * self.altura / 2

class Cuadrado(Figura):
    def __init__(self, lado):
        self.lado = lado
    def area(self):
        return self.lado ** 2

for f in [Triangulo(4, 3), Cuadrado(5)]:
    print(f.area())   # 6.0  25
```

**19.5**

```python
class Fraccion:
    def __init__(self, num, den):
        self.num = num
        self.den = den

    def __str__(self):
        return f"{self.num}/{self.den}"

print(Fraccion(3, 4))   # 3/4
```

**19.6**

```python
class Fraccion:
    def __init__(self, num, den):
        self.num = num
        self.den = den

    def __str__(self):
        return f"{self.num}/{self.den}"

    def __add__(self, otra):
        return Fraccion(self.num + otra.num, self.den)

print(Fraccion(1, 5) + Fraccion(2, 5))   # 3/5
```

**19.7**

```python
class Libro:
    def __init__(self, titulo, paginas):
        self.titulo = titulo
        self.paginas = paginas

    def __len__(self):
        return self.paginas

print(len(Libro("Python", 300)))   # 300
```

**19.8**

```python
class Termometro:
    def __init__(self, celsius):
        self.celsius = celsius

    @property
    def fahrenheit(self):
        return self.celsius * 9 / 5 + 32

print(Termometro(100).fahrenheit)   # 212.0
```

**19.9**

```python
from dataclasses import dataclass

@dataclass
class Pelicula:
    titulo: str
    anio: int
    nota: float = 0

print(Pelicula("Matrix", 1999))
```

**19.10**

```python
class CuentaBancaria:
    def __init__(self, titular, saldo=0):
        self.titular = titular
        self.saldo = saldo

class CuentaAhorro(CuentaBancaria):
    def aplicar_interes(self, porcentaje):
        self.saldo += self.saldo * porcentaje / 100

c = CuentaAhorro("Ana", 1000)
c.aplicar_interes(5)
print(c.saldo)   # 1050.0
```

**19.11**

```python
class Jugador:
    def __init__(self, nombre):
        self.nombre = nombre

class Equipo:
    def __init__(self):
        self.jugadores = []

    def fichar(self, jugador):
        self.jugadores.append(jugador)

    def cantidad(self):
        return len(self.jugadores)

e = Equipo()
e.fichar(Jugador("Ana"))
e.fichar(Jugador("Luis"))
print(e.cantidad())   # 2
```

**19.12**

```python
for x in [1, "hola", 3.5, [1, 2]]:
    if isinstance(x, int):
        print("entero")
    elif isinstance(x, str):
        print("texto")
    elif isinstance(x, float):
        print("decimal")
    elif isinstance(x, list):
        print("lista")
```

---

# MÓDULO 20 — Funciones avanzadas

## 20.1 `*args`: número variable de argumentos

¿Y si no sabes cuántos argumentos te van a pasar? Con `*args` la función los recibe todos como una **tupla**.

```python
def sumar_todos(*numeros):
    print(numeros)           # (1, 2, 3)
    return sum(numeros)

print(sumar_todos(1, 2, 3))          # 6
print(sumar_todos(10, 20))           # 30
print(sumar_todos())                 # 0
print(sumar_todos(1, 2, 3, 4, 5))    # 15
```

(El nombre `args` es convención; lo importante es el `*`.)

Más ejemplos:

```python
def mayor(*valores):
    return max(valores)

def unir(*palabras):
    return " ".join(palabras)

print(mayor(4, 9, 2))              # 9
print(unir("Hola", "a", "todos"))  # Hola a todos
```

Combinar con parámetros normales (los normales van **antes**):

```python
def saludar(saludo, *nombres):
    for n in nombres:
        print(f"{saludo}, {n}")

saludar("Hola", "Ana", "Luis", "Eva")
```

### Operador `*` al llamar: "desempaquetar"

```python
numeros = [1, 2, 3]
print(sumar_todos(*numeros))   # igual que sumar_todos(1, 2, 3)

print(*numeros)                # 1 2 3  (print recibe tres argumentos)
```

## 20.2 `**kwargs`: argumentos con nombre variables

Los recibe como un **diccionario**.

```python
def mostrar_datos(**datos):
    print(datos)
    for clave, valor in datos.items():
        print(f"{clave}: {valor}")

mostrar_datos(nombre="Ana", edad=20, ciudad="Madrid")
```

```text
{'nombre': 'Ana', 'edad': 20, 'ciudad': 'Madrid'}
nombre: Ana
edad: 20
ciudad: Madrid
```

Combinando todo (el orden debe ser: normales, `*args`, `**kwargs`):

```python
def funcion(a, b, *args, **kwargs):
    print("a =", a)
    print("b =", b)
    print("args =", args)
    print("kwargs =", kwargs)

funcion(1, 2, 3, 4, x=10, y=20)
```

```text
a = 1
b = 2
args = (3, 4)
kwargs = {'x': 10, 'y': 20}
```

Desempaquetar un diccionario al llamar con `**`:

```python
persona = {"nombre": "Ana", "edad": 20}

def presentar(nombre, edad):
    print(f"{nombre} tiene {edad}")

presentar(**persona)   # igual que presentar(nombre="Ana", edad=20)
```

## 20.3 Iteradores: lo que hay detrás de un `for`

Un **iterable** es cualquier cosa que se puede recorrer (listas, strings, diccionarios...). El `for` usa por detrás `iter()` y `next()`:

```python
lista = [10, 20, 30]
it = iter(lista)
print(next(it))   # 10
print(next(it))   # 20
print(next(it))   # 30
# print(next(it)) # ❌ StopIteration: ya no quedan elementos
```

## 20.4 Generadores: valores "bajo demanda" con `yield`

Un **generador** es una función que, en vez de `return`, usa `yield`. Entrega un valor, **se pausa**, y continúa donde se quedó la próxima vez.

```python
def contar_hasta(n):
    i = 1
    while i <= n:
        yield i
        i += 1

for numero in contar_hasta(3):
    print(numero)    # 1, 2, 3
```

Paso a paso con `next`:

```python
g = contar_hasta(2)
print(next(g))   # 1
print(next(g))   # 2
# print(next(g)) # StopIteration
```

**¿Por qué sirven?** No guardan todos los datos en memoria; los producen uno a uno. Con `range(1_000_000_000)` o un archivo enorme, esto ahorra muchísima memoria.

```python
def cuadrados(n):
    for i in range(n):
        yield i ** 2

print(list(cuadrados(5)))   # [0, 1, 4, 9, 16]
```

**Fibonacci infinito (y tomamos los que queramos):**

```python
def fibonacci():
    a, b = 0, 1
    while True:
        yield a
        a, b = b, a + b

gen = fibonacci()
primeros = [next(gen) for _ in range(10)]
print(primeros)   # [0, 1, 1, 2, 3, 5, 8, 13, 21, 34]
```

**Expresiones generadoras** (como una comprensión pero con paréntesis):

```python
cuadrados = (n ** 2 for n in range(5))
print(next(cuadrados))     # 0
print(sum(n ** 2 for n in range(1, 4)))   # 14
```

**Leer un archivo grande línea a línea:**

```python
def lineas_largas(nombre, minimo):
    with open(nombre, encoding="utf-8") as f:
        for linea in f:
            if len(linea) >= minimo:
                yield linea.strip()
```

## 20.5 Las funciones son objetos

En Python una función se puede guardar en una variable, pasar como argumento o devolver.

```python
def saludar(nombre):
    return f"Hola, {nombre}"

otra = saludar            # ¡sin paréntesis! no la llamamos, la copiamos
print(otra("Ana"))        # Hola, Ana
```

**Pasar una función como argumento:**

```python
def aplicar(funcion, valor):
    return funcion(valor)

print(aplicar(len, "hola"))          # 4
print(aplicar(str.upper, "hola"))    # HOLA
print(aplicar(lambda x: x + 1, 5))   # 6
```

**Devolver una función:**

```python
def crear_sumador(n):
    def sumar(x):
        return x + n
    return sumar

suma5 = crear_sumador(5)
print(suma5(10))   # 15
```

**Lista de funciones:**

```python
operaciones = {
    "suma": lambda a, b: a + b,
    "resta": lambda a, b: a - b,
    "mult": lambda a, b: a * b,
}
print(operaciones["suma"](6, 2))   # 8
print(operaciones["mult"](6, 2))   # 12
```

## 20.6 Decoradores

Un **decorador** es una función que **envuelve** a otra para añadirle comportamiento, sin tocar su código.

```python
def con_mensaje(funcion):
    def envoltura():
        print("Antes de la función")
        funcion()
        print("Después de la función")
    return envoltura

def saludar():
    print("¡Hola!")

saludar = con_mensaje(saludar)    # decoramos "a mano"
saludar()
```

```text
Antes de la función
¡Hola!
Después de la función
```

La **sintaxis con `@`** hace lo mismo, más corto:

```python
@con_mensaje
def despedirse():
    print("¡Adiós!")

despedirse()
```

**Decorador que acepta cualquier argumento y devuelve el resultado:**

```python
def registrar(funcion):
    def envoltura(*args, **kwargs):
        print(f"Llamando a {funcion.__name__} con {args} {kwargs}")
        resultado = funcion(*args, **kwargs)
        print(f"Resultado: {resultado}")
        return resultado
    return envoltura

@registrar
def sumar(a, b):
    return a + b

sumar(3, 4)
```

```text
Llamando a sumar con (3, 4) {}
Resultado: 7
```

**Decorador para medir el tiempo:**

```python
import time

def cronometro(funcion):
    def envoltura(*args, **kwargs):
        inicio = time.time()
        resultado = funcion(*args, **kwargs)
        print(f"{funcion.__name__} tardó {time.time() - inicio:.4f} s")
        return resultado
    return envoltura

@cronometro
def lenta():
    return sum(range(2_000_000))

lenta()
```

> 💡 No te agobies si los decoradores cuestan al principio. Son un tema "avanzado": con entender la idea (una función que envuelve a otra) es suficiente por ahora.

## 20.7 Anotaciones de tipo (type hints)

Son **pistas** sobre qué tipo espera/devuelve cada cosa. Python no las obliga, pero ayudan a leer y a que tu editor te avise.

```python
def sumar(a: int, b: int) -> int:
    return a + b

def saludar(nombre: str, veces: int = 1) -> str:
    return ("Hola, " + nombre + ". ") * veces

nombres: list[str] = ["Ana", "Luis"]
edades: dict[str, int] = {"Ana": 20}
```

Valores opcionales:

```python
def buscar(lista: list[int], x: int) -> int | None:
    if x in lista:
        return lista.index(x)
    return None
```

## 20.8 Ejemplos completos

**Ejemplo A: calculadora con diccionario de funciones**

```python
def sumar(a, b): return a + b
def restar(a, b): return a - b
def multiplicar(a, b): return a * b
def dividir(a, b): return a / b

operaciones = {"+": sumar, "-": restar, "*": multiplicar, "/": dividir}

a = float(input("A: "))
op = input("Operación (+ - * /): ")
b = float(input("B: "))

if op in operaciones:
    print(operaciones[op](a, b))
else:
    print("Operación no válida")
```

**Ejemplo B: media de cualquier cantidad de notas**

```python
def media(*notas):
    if not notas:
        return 0
    return sum(notas) / len(notas)

print(media(8, 6, 10))   # 8.0
print(media(5))          # 5.0
```

**Ejemplo C: generador de números primos**

```python
def primos():
    n = 2
    while True:
        if all(n % d != 0 for d in range(2, int(n ** 0.5) + 1)):
            yield n
        n += 1

g = primos()
print([next(g) for _ in range(8)])   # [2, 3, 5, 7, 11, 13, 17, 19]
```

## 20.9 Resumen del Módulo 20

- `*args` (tupla) y `**kwargs` (diccionario) permiten cantidad variable de argumentos.
- `*` y `**` también **desempaquetan** al llamar.
- Un **generador** usa `yield` y produce valores uno a uno.
- Las funciones son objetos: se pasan, se devuelven, se guardan.
- Un **decorador** envuelve a una función (`@nombre`).
- Las **type hints** documentan los tipos.

## 20.10 🎯 Ejercicios del Módulo 20

**Ejercicio 20.1** — Crea `multiplicar_todos(*numeros)` que devuelva el producto de todos los argumentos.

**Ejercicio 20.2** — Crea `mayor_y_menor(*numeros)` que devuelva ambos valores.

**Ejercicio 20.3** — Crea `describir(**datos)` que muestre cada par `clave = valor`.

**Ejercicio 20.4** — Crea una función `unir(separador, *palabras)` que junte las palabras con el separador.

**Ejercicio 20.5** — Llama a `sumar_todos` pasándole una lista con `*`.

**Ejercicio 20.6** — Crea un generador `pares(limite)` que produzca los pares hasta `limite`.

**Ejercicio 20.7** — Crea un generador `cuenta_atras(n)` que produzca de `n` a 1.

**Ejercicio 20.8** — Usa una expresión generadora para sumar los cuadrados de 1 a 100.

**Ejercicio 20.9** — Crea una función `aplicar_a_lista(funcion, lista)` que devuelva una lista nueva aplicando la función a cada elemento. Pruébala con `lambda x: x * 10`.

**Ejercicio 20.10** — Crea un decorador `anunciar` que imprima `Iniciando...` antes y `Terminado` después de ejecutar la función.

**Ejercicio 20.11** — Crea un decorador `doble_resultado` que multiplique por 2 lo que devuelva la función decorada.

**Ejercicio 20.12** — Escribe una función con type hints `area_rectangulo(base: float, altura: float) -> float`.

### ✅ Soluciones del Módulo 20

**20.1**

```python
def multiplicar_todos(*numeros):
    total = 1
    for n in numeros:
        total *= n
    return total

print(multiplicar_todos(2, 3, 4))   # 24
```

**20.2**

```python
def mayor_y_menor(*numeros):
    return max(numeros), min(numeros)

print(mayor_y_menor(4, 9, 1))   # (9, 1)
```

**20.3**

```python
def describir(**datos):
    for k, v in datos.items():
        print(f"{k} = {v}")

describir(nombre="Ana", edad=20)
```

**20.4**

```python
def unir(separador, *palabras):
    return separador.join(palabras)

print(unir("-", "a", "b", "c"))   # a-b-c
```

**20.5**

```python
def sumar_todos(*numeros):
    return sum(numeros)

print(sumar_todos(*[1, 2, 3, 4]))   # 10
```

**20.6**

```python
def pares(limite):
    for n in range(2, limite + 1, 2):
        yield n

print(list(pares(10)))   # [2, 4, 6, 8, 10]
```

**20.7**

```python
def cuenta_atras(n):
    while n > 0:
        yield n
        n -= 1

print(list(cuenta_atras(5)))   # [5, 4, 3, 2, 1]
```

**20.8**

```python
print(sum(n ** 2 for n in range(1, 101)))   # 338350
```

**20.9**

```python
def aplicar_a_lista(funcion, lista):
    return [funcion(x) for x in lista]

print(aplicar_a_lista(lambda x: x * 10, [1, 2, 3]))   # [10, 20, 30]
```

**20.10**

```python
def anunciar(funcion):
    def envoltura(*args, **kwargs):
        print("Iniciando...")
        resultado = funcion(*args, **kwargs)
        print("Terminado")
        return resultado
    return envoltura

@anunciar
def trabajar():
    print("Trabajando")

trabajar()
```

**20.11**

```python
def doble_resultado(funcion):
    def envoltura(*args, **kwargs):
        return funcion(*args, **kwargs) * 2
    return envoltura

@doble_resultado
def sumar(a, b):
    return a + b

print(sumar(2, 3))   # 10
```

**20.12**

```python
def area_rectangulo(base: float, altura: float) -> float:
    return base * altura

print(area_rectangulo(3, 4.5))   # 13.5
```

---

# MÓDULO 21 — JSON, CSV, `pip` y entornos virtuales

## 21.1 JSON: guardar datos estructurados

**JSON** es un formato de texto para guardar datos (diccionarios, listas, textos, números) que casi todos los lenguajes entienden. Se parece mucho a los diccionarios de Python.

```python
import json

persona = {
    "nombre": "Ana",
    "edad": 20,
    "aficiones": ["leer", "correr"],
    "activa": True
}

# De Python a texto JSON
texto = json.dumps(persona, indent=2, ensure_ascii=False)
print(texto)
```

```text
{
  "nombre": "Ana",
  "edad": 20,
  "aficiones": [
    "leer",
    "correr"
  ],
  "activa": true
}
```

(`True` en Python se vuelve `true` en JSON; `None` → `null`.)

```python
# De texto JSON a Python
datos = json.loads('{"x": 1, "y": [2, 3]}')
print(datos["y"][1])    # 3
print(type(datos))      # <class 'dict'>
```

**Guardar a un archivo y cargar de un archivo:**

```python
import json

# Guardar
with open("persona.json", "w", encoding="utf-8") as f:
    json.dump(persona, f, indent=2, ensure_ascii=False)

# Cargar
with open("persona.json", encoding="utf-8") as f:
    cargada = json.load(f)
print(cargada["nombre"])   # Ana
```

Regla mnemotécnica: la **s** de `dumps`/`loads` es de **s**tring (texto); sin `s` trabajan con archivos.

**Guardar una lista de diccionarios (como una pequeña base de datos):**

```python
import json
from pathlib import Path

ARCHIVO = Path("contactos.json")

def cargar():
    if ARCHIVO.exists():
        return json.loads(ARCHIVO.read_text(encoding="utf-8"))
    return []

def guardar(contactos):
    ARCHIVO.write_text(
        json.dumps(contactos, indent=2, ensure_ascii=False),
        encoding="utf-8",
    )

contactos = cargar()
contactos.append({"nombre": "Luis", "tel": "123"})
guardar(contactos)
print(contactos)
```

⚠️ JSON solo guarda tipos básicos. Para guardar objetos propios, conviértelos antes a diccionario:

```python
class Persona:
    def __init__(self, nombre, edad):
        self.nombre = nombre
        self.edad = edad

p = Persona("Ana", 20)
print(json.dumps(p.__dict__))   # {"nombre": "Ana", "edad": 20}
```

## 21.2 CSV: tablas en texto

**CSV** (*comma-separated values*) es el formato de las hojas de cálculo simples:

```text
nombre,edad,ciudad
Ana,20,Madrid
Luis,25,Lima
```

**Escribir:**

```python
import csv

filas = [
    ["nombre", "edad", "ciudad"],
    ["Ana", 20, "Madrid"],
    ["Luis", 25, "Lima"],
]

with open("gente.csv", "w", newline="", encoding="utf-8") as f:
    escritor = csv.writer(f)
    escritor.writerows(filas)
```

**Leer (como listas):**

```python
with open("gente.csv", newline="", encoding="utf-8") as f:
    lector = csv.reader(f)
    for fila in lector:
        print(fila)    # ['nombre', 'edad', 'ciudad'] ...
```

**Leer como diccionarios (¡muy cómodo!):**

```python
with open("gente.csv", newline="", encoding="utf-8") as f:
    for persona in csv.DictReader(f):
        print(persona["nombre"], persona["edad"])   # la edad viene como texto
```

**Escribir diccionarios:**

```python
datos = [
    {"nombre": "Eva", "edad": 30},
    {"nombre": "Pedro", "edad": 28},
]
with open("otra.csv", "w", newline="", encoding="utf-8") as f:
    escritor = csv.DictWriter(f, fieldnames=["nombre", "edad"])
    escritor.writeheader()
    escritor.writerows(datos)
```

**Ejemplo: media de edades de un CSV**

```python
with open("gente.csv", newline="", encoding="utf-8") as f:
    edades = [int(fila["edad"]) for fila in csv.DictReader(f)]
print(sum(edades) / len(edades))
```

## 21.3 `pip`: instalar librerías de terceros

Además de la librería estándar, hay cientos de miles de librerías creadas por la comunidad en **PyPI** (pypi.org). Se instalan con `pip` desde la **terminal** (no dentro de Python):

```bash
pip install requests          # instalar
pip install requests==2.31.0  # versión concreta
pip uninstall requests        # desinstalar
pip list                      # ver lo instalado
pip show requests             # info de un paquete
pip install --upgrade requests
```

(En algunos sistemas: `python -m pip install ...` o `pip3 install ...`.)

> ⚠️ Necesitas conexión a internet **solo para instalar**. Una vez instalada, la librería funciona sin conexión.

### Librerías populares (para que sepas por dónde seguir)

| Librería | Para qué |
|----------|----------|
| `requests` | hablar con páginas y APIs web |
| `beautifulsoup4` | extraer datos de páginas HTML |
| `pandas` | análisis de datos / tablas |
| `numpy` | cálculo numérico |
| `matplotlib` | gráficas |
| `flask` / `django` / `fastapi` | páginas y servicios web |
| `pygame` | videojuegos 2D |
| `tkinter` | ventanas (viene con Python) |
| `pytest` | pruebas |
| `openpyxl` | leer/escribir Excel |

Ejemplo (necesita `pip install requests` e internet):

```python
import requests

r = requests.get("https://api.github.com")
print(r.status_code)   # 200 si todo va bien
print(r.json())        # los datos como diccionario
```

## 21.4 `requirements.txt`

Lista de librerías que necesita tu proyecto:

```text
requests==2.31.0
pandas>=2.0
```

Para instalarlas todas:

```bash
pip install -r requirements.txt
```

Para generar la lista de lo instalado:

```bash
pip freeze > requirements.txt
```

## 21.5 Entornos virtuales (`venv`)

Cada proyecto puede necesitar versiones distintas de las librerías. Un **entorno virtual** es una "burbuja" aislada por proyecto.

**Crear (una vez por proyecto):**

```bash
python -m venv venv
```

**Activar:**

- Windows (PowerShell): `venv\Scripts\Activate.ps1`
- Windows (cmd): `venv\Scripts\activate.bat`
- Linux / macOS: `source venv/bin/activate`

Verás `(venv)` al inicio de la línea de comandos. Ahora `pip install` instala **solo ahí**.

**Desactivar:**

```bash
deactivate
```

> 💡 Hábito recomendado: **un entorno virtual por proyecto**.

## 21.6 Argumentos desde la terminal

```python
# saludo.py
import sys

if len(sys.argv) < 2:
    print("Uso: python saludo.py <nombre>")
else:
    print(f"Hola, {sys.argv[1]}")
```

```bash
python saludo.py Ana      # Hola, Ana
```

Con `argparse` (más completo):

```python
import argparse

parser = argparse.ArgumentParser(description="Saluda a alguien")
parser.add_argument("nombre", help="nombre de la persona")
parser.add_argument("--veces", type=int, default=1, help="cuántas veces saludar")
args = parser.parse_args()

for _ in range(args.veces):
    print(f"Hola, {args.nombre}")
```

```bash
python saludo.py Ana --veces 3
```

## 21.7 Variables de entorno (idea básica)

Datos de configuración (claves secretas) que **no** se escriben en el código:

```python
import os

clave = os.environ.get("MI_CLAVE", "sin clave")
print(clave)
```

## 21.8 Resumen del Módulo 21

- `json.dump/load` (archivos) y `json.dumps/loads` (texto).
- `csv.reader/writer` y `DictReader/DictWriter`.
- `pip install nombre` instala librerías externas (necesita internet solo para instalar).
- `venv` aísla las dependencias de cada proyecto.
- `sys.argv` / `argparse` para recibir argumentos desde la terminal.

## 21.9 🎯 Ejercicios del Módulo 21

**Ejercicio 21.1** — Convierte el diccionario `{"producto": "pan", "precio": 1.2}` a texto JSON y muéstralo.

**Ejercicio 21.2** — Convierte el texto `'{"a": 1, "b": [1, 2, 3]}'` a diccionario y muestra la suma de la lista `b`.

**Ejercicio 21.3** — Guarda una lista de 3 tareas (como texto) en `tareas.json` y vuelve a leerla.

**Ejercicio 21.4** — Crea un archivo CSV con 3 alumnos (nombre y nota) y léelo mostrando cada uno.

**Ejercicio 21.5** — Lee el CSV del ejercicio anterior y calcula el promedio de las notas.

**Ejercicio 21.6** — Haz un programa que guarde una lista de contactos en `contactos.json`: al ejecutarlo pide un contacto nuevo, lo añade y guarda.

**Ejercicio 21.7** — Crea un entorno virtual llamado `venv` en una carpeta nueva, actívalo y comprueba con `pip list` que está casi vacío.

**Ejercicio 21.8** — Instala `requests` con `pip` dentro del entorno virtual y comprueba con `pip show requests` que está instalado.

**Ejercicio 21.9** — Haz un script que reciba un número por la terminal (`python doble.py 5`) y muestre su doble.

**Ejercicio 21.10** — Crea un `requirements.txt` con una librería y explica con tus palabras para qué sirve.

### ✅ Soluciones del Módulo 21

**21.1**

```python
import json
print(json.dumps({"producto": "pan", "precio": 1.2}))
# {"producto": "pan", "precio": 1.2}
```

**21.2**

```python
import json
d = json.loads('{"a": 1, "b": [1, 2, 3]}')
print(sum(d["b"]))   # 6
```

**21.3**

```python
import json
tareas = ["estudiar", "hacer ejercicio", "leer"]
with open("tareas.json", "w", encoding="utf-8") as f:
    json.dump(tareas, f, ensure_ascii=False)
with open("tareas.json", encoding="utf-8") as f:
    print(json.load(f))
```

**21.4**

```python
import csv
with open("alumnos.csv", "w", newline="", encoding="utf-8") as f:
    w = csv.writer(f)
    w.writerow(["nombre", "nota"])
    w.writerows([["Ana", 8], ["Luis", 6], ["Eva", 9]])

with open("alumnos.csv", newline="", encoding="utf-8") as f:
    for fila in csv.DictReader(f):
        print(fila["nombre"], fila["nota"])
```

**21.5**

```python
import csv
with open("alumnos.csv", newline="", encoding="utf-8") as f:
    notas = [float(fila["nota"]) for fila in csv.DictReader(f)]
print(sum(notas) / len(notas))   # 7.666666666666667
```

**21.6**

```python
import json
from pathlib import Path

ARCHIVO = Path("contactos.json")
contactos = json.loads(ARCHIVO.read_text(encoding="utf-8")) if ARCHIVO.exists() else []

nombre = input("Nombre: ")
tel = input("Teléfono: ")
contactos.append({"nombre": nombre, "tel": tel})

ARCHIVO.write_text(json.dumps(contactos, indent=2, ensure_ascii=False), encoding="utf-8")
print("Contactos:", len(contactos))
```

**21.7** En la terminal:

```bash
mkdir proyecto
cd proyecto
python -m venv venv
source venv/bin/activate      # Windows: venv\Scripts\activate
pip list
```

**21.8**

```bash
pip install requests
pip show requests
```

**21.9**

```python
# doble.py
import sys
n = float(sys.argv[1])
print(n * 2)
```

```bash
python doble.py 5    # 10.0
```

**21.10** Archivo `requirements.txt`:

```text
requests==2.31.0
```

Sirve para que cualquiera pueda instalar exactamente las mismas librerías con `pip install -r requirements.txt`.

---

# MÓDULO 22 — Depuración, pruebas y buenas prácticas

## 22.1 Depurar (encontrar errores)

Un **bug** es un error en tu programa. **Depurar** (*debug*) es encontrarlo y arreglarlo. Es una habilidad que se aprende.

### Técnica 1: `print` en puntos clave

```python
def promedio(lista):
    print("lista recibida:", lista)       # ← ¿qué llegó?
    total = sum(lista)
    print("total:", total)                # ← ¿qué da la suma?
    return total / len(lista)

promedio([8, 6, 10])
```

Añade `print`s para ver los valores intermedios; cuando encuentres el paso donde "se tuerce", ahí está el error. Luego quita los `print`s.

### Técnica 2: leer el *traceback*

Lee de **abajo hacia arriba**: la última línea es el error; las de arriba indican **dónde** (archivo y línea).

```text
Traceback (most recent call last):
  File "prueba.py", line 8, in <module>
    resultado = promedio([])
  File "prueba.py", line 4, in promedio
    return total / len(lista)
ZeroDivisionError: division by zero
```

→ El error es una división entre cero en la línea 4 de `promedio`, llamada desde la línea 8 con una lista vacía.

### Técnica 3: el depurador `breakpoint()`

```python
def f(a, b):
    resultado = a + b
    breakpoint()          # el programa se detiene aquí y abre el depurador
    return resultado * 2

f(2, 3)
```

Comandos útiles dentro del depurador (`pdb`): `n` (siguiente línea), `s` (entrar en función), `c` (continuar), `p variable` (ver valor), `q` (salir). En VS Code puedes poner puntos de interrupción (breakpoints) haciendo clic a la izquierda del número de línea y pulsando F5.

### Técnica 4: el "patito de goma"

Explica tu código **en voz alta**, línea por línea, a un patito de goma (o a una persona, o a una mascota). Muchas veces descubres el error mientras lo explicas.

### Técnica 5: reducir el problema

Si algo falla en un programa grande, aísla la parte que falla en un archivo pequeño con el mínimo código posible. Eso te dice dónde está el problema.

## 22.2 Errores lógicos típicos

Son los que **no** dan error pero dan un **resultado incorrecto**:

```python
# Promedio mal calculado (falta el paréntesis)
a, b, c = 8, 6, 10
print(a + b + c / 3)        # ❌ 17.33...
print((a + b + c) / 3)      # ✔️ 8.0

# Off-by-one (uno de más o de menos)
for i in range(1, 10):      # llega a 9, no a 10
    pass
for i in range(1, 11):      # ✔️ llega a 10
    pass

# Comparar con = en vez de ==, o usar "is" para valores
if "a" is "a":              # ❌ mal hábito; usa ==
    pass

# Modificar una lista mientras la recorres
nums = [1, 2, 3, 4]
for n in nums:
    if n % 2 == 0:
        nums.remove(n)      # ❌ salta elementos
# ✔️ mejor:
nums = [n for n in nums if n % 2 != 0]
```

## 22.3 Probar tu código

**Probar** es comprobar que tu código hace lo que debe. La forma más simple: `assert`.

```python
def es_par(n):
    return n % 2 == 0

assert es_par(4) == True
assert es_par(7) == False
assert es_par(0) == True
print("¡Todas las pruebas pasaron!")
```

Si alguna falla, el programa se detiene con `AssertionError` y sabes cuál.

**Piensa en casos límite:** el 0, números negativos, listas vacías, textos vacíos, un solo elemento, valores muy grandes.

```python
def promedio(lista):
    if not lista:
        return 0
    return sum(lista) / len(lista)

assert promedio([2, 4]) == 3
assert promedio([5]) == 5
assert promedio([]) == 0        # caso límite
```

### `unittest` (viene con Python)

```python
import unittest

def suma(a, b):
    return a + b

class PruebasSuma(unittest.TestCase):
    def test_positivos(self):
        self.assertEqual(suma(2, 3), 5)

    def test_negativos(self):
        self.assertEqual(suma(-1, -1), -2)

    def test_cero(self):
        self.assertEqual(suma(0, 0), 0)

if __name__ == "__main__":
    unittest.main()
```

Ejecutar: `python archivo.py`.

### `pytest` (muy popular; `pip install pytest`)

```python
# test_ejemplo.py
def suma(a, b):
    return a + b

def test_suma():
    assert suma(2, 3) == 5
    assert suma(-1, 1) == 0
```

Ejecutar: `pytest` en la terminal.

## 22.4 Buenas prácticas (PEP 8)

**PEP 8** es la guía de estilo oficial. Lo esencial:

1. **Nombres claros:** `precio_total`, no `pt`.
   - Variables y funciones: `snake_case`.
   - Clases: `PascalCase` (`CuentaBancaria`).
   - Constantes: `MAYUSCULAS` (`MAX_INTENTOS`).
2. **4 espacios** de indentación (nunca mezcles espacios y tabs).
3. **Líneas de máximo ~79–88 caracteres.**
4. **Espacios** alrededor de operadores: `a = b + c`, no `a=b+c`.
5. **Dos líneas en blanco** entre funciones/clases de nivel superior.
6. `import` al principio, uno por línea.
7. **Comentarios** que expliquen el **por qué**, no lo obvio:

```python
# Mal: dice lo que ya se ve
x = x + 1   # suma 1 a x

# Bien: explica la razón
x = x + 1   # compensa el índice que empieza en 0
```

### Principios útiles

- **Una función = una tarea.** Si hace dos cosas, sepárala en dos funciones.
- **No te repitas (DRY):** si copias y pegas código, haz una función.
- **Evita "números mágicos":**

```python
# Mal
if edad >= 18: ...

# Mejor
MAYORIA_DE_EDAD = 18
if edad >= MAYORIA_DE_EDAD: ...
```

- **Sal pronto de las funciones** (cláusulas de guarda) para evitar anidar demasiado:

```python
# Muy anidado
def descuento(precio, es_socio):
    if precio > 0:
        if es_socio:
            return precio * 0.9
        else:
            return precio
    else:
        return 0

# Más plano y legible
def descuento(precio, es_socio):
    if precio <= 0:
        return 0
    if es_socio:
        return precio * 0.9
    return precio
```

- **Haz que funcione, luego que sea limpio, luego (solo si hace falta) que sea rápido.**

## 22.5 Estructura de un proyecto pequeño

```text
mi_proyecto/
├── main.py              ← punto de entrada
├── utilidades.py        ← funciones auxiliares
├── modelos.py           ← clases
├── datos/               ← archivos de datos (json, csv)
├── tests/
│   └── test_utilidades.py
├── requirements.txt
└── README.md            ← qué hace y cómo se usa
```

Plantilla de `main.py`:

```python
def main():
    print("Hola, proyecto")

if __name__ == "__main__":
    main()
```

## 22.6 Cómo resolver un problema cuando estás bloqueado

1. **Relee el enunciado.** ¿Entendiste de verdad lo que piden?
2. **Haz un ejemplo a mano** con números pequeños.
3. **Escribe el pseudocódigo** en español.
4. **Resuelve primero un caso más simple** (con 1 elemento, con 2...).
5. **Divide** en funciones pequeñas y prueba cada una.
6. **Imprime** valores intermedios.
7. **Busca el mensaje de error** exacto (en tu cabeza o en internet).
8. **Descansa 10 minutos.** El cerebro sigue trabajando.
9. **Explícaselo a alguien** (o a un patito de goma).

## 22.7 Resumen del Módulo 22

- Depurar: `print`, leer el traceback, `breakpoint()`, aislar el problema.
- Probar con `assert`, `unittest` o `pytest`; no olvides los casos límite.
- PEP 8: nombres claros, 4 espacios, funciones pequeñas, nada de números mágicos.
- Cuando te bloquees: ejemplo a mano → pseudocódigo → casos simples.

## 22.8 🎯 Ejercicios del Módulo 22

**Ejercicio 22.1** — Este código tiene un error lógico. Encuéntralo y corrígelo:

```python
def promedio(a, b, c):
    return a + b + c / 3
```

**Ejercicio 22.2** — Este código debería mostrar del 1 al 5, pero muestra del 1 al 4. Corrígelo:

```python
for i in range(1, 5):
    print(i)
```

**Ejercicio 22.3** — Escribe 4 `assert` para probar una función `es_impar(n)`.

**Ejercicio 22.4** — Escribe una función `maximo(lista)` y pruébala con `assert` incluyendo un caso con un solo elemento y otro con negativos.

**Ejercicio 22.5** — Convierte estos nombres a un estilo PEP 8 correcto: `NombreCompleto` (variable), `calcularIVA` (función), `claseperro` (clase), `maxintentos` (constante).

**Ejercicio 22.6** — Reescribe esta función con cláusulas de guarda para que tenga menos anidación:

```python
def categoria(edad):
    if edad >= 0:
        if edad < 18:
            return "menor"
        else:
            return "adulto"
    else:
        return "inválida"
```

**Ejercicio 22.7** — Usa `print` para depurar: ¿por qué esta función no suma bien? Corrígela.

```python
def suma_lista(lista):
    total = 0
    for n in lista:
        total = n
    return total
```

**Ejercicio 22.8** — Escribe una prueba con `unittest` para una función `es_palindromo(texto)`.

**Ejercicio 22.9** — Reemplaza el "número mágico" de esta línea por una constante con nombre: `precio_final = precio * 1.21`.

### ✅ Soluciones del Módulo 22

**22.1** Falta el paréntesis: `/` se calcula antes que `+`.

```python
def promedio(a, b, c):
    return (a + b + c) / 3
```

**22.2** `range(1, 5)` no incluye el 5. Debe ser `range(1, 6)`.

**22.3**

```python
def es_impar(n):
    return n % 2 == 1

assert es_impar(3) == True
assert es_impar(4) == False
assert es_impar(0) == False
assert es_impar(-3) == True
print("OK")
```

**22.4**

```python
def maximo(lista):
    mayor = lista[0]
    for n in lista:
        if n > mayor:
            mayor = n
    return mayor

assert maximo([3, 9, 2]) == 9
assert maximo([5]) == 5
assert maximo([-5, -2, -9]) == -2
print("OK")
```

**22.5** `nombre_completo`, `calcular_iva`, `ClasePerro` (o `Perro`), `MAX_INTENTOS`.

**22.6**

```python
def categoria(edad):
    if edad < 0:
        return "inválida"
    if edad < 18:
        return "menor"
    return "adulto"
```

**22.7** Error: `total = n` reemplaza el total en vez de acumular. Debe ser `total += n`.

```python
def suma_lista(lista):
    total = 0
    for n in lista:
        total += n
    return total
```

**22.8**

```python
import unittest

def es_palindromo(texto):
    return texto == texto[::-1]

class PruebasPalindromo(unittest.TestCase):
    def test_si(self):
        self.assertTrue(es_palindromo("ana"))

    def test_no(self):
        self.assertFalse(es_palindromo("hola"))

    def test_vacio(self):
        self.assertTrue(es_palindromo(""))

if __name__ == "__main__":
    unittest.main()
```

**22.9**

```python
IVA = 0.21
precio_final = precio * (1 + IVA)
```

---

# MÓDULO 23 — Proyectos finales

Es hora de juntar todo. Cada proyecto tiene un **enunciado**, una **guía de pasos**, y una **solución de referencia**. **Intenta hacerlo tú primero** siguiendo la guía; usa la solución solo para comparar o si te atascas.

---

## Proyecto 1: Adivina el número

**Qué hace:** el programa elige un número al azar del 1 al 50; el jugador intenta adivinarlo con pistas de "más alto / más bajo" y un máximo de 7 intentos.

**Guía de pasos:**

1. Importa `random` y elige el número secreto.
2. Crea un bucle que se repita hasta 7 veces.
3. En cada vuelta, pide un número (valida que sea entero).
4. Compara con el secreto y da la pista.
5. Si acierta, felicítalo y termina; si se acaban los intentos, revela el número.

**Solución de referencia:**

```python
import random

MAX_INTENTOS = 7

def pedir_entero(mensaje):
    while True:
        try:
            return int(input(mensaje))
        except ValueError:
            print("Escribe un número entero")

def jugar():
    secreto = random.randint(1, 50)
    print("Pensé un número del 1 al 50. Tienes", MAX_INTENTOS, "intentos.")

    for intento in range(1, MAX_INTENTOS + 1):
        numero = pedir_entero(f"Intento {intento}: ")
        if numero == secreto:
            print(f"¡Acertaste en {intento} intentos!")
            return
        elif numero < secreto:
            print("Más alto")
        else:
            print("Más bajo")

    print(f"Se acabaron los intentos. Era el {secreto}")

if __name__ == "__main__":
    jugar()
```

**Mejoras para practicar:** pregunta si quiere jugar de nuevo; añade niveles de dificultad (rango y número de intentos distintos); guarda la mejor puntuación en un archivo.

---

## Proyecto 2: Agenda de contactos (con JSON)

**Qué hace:** menú para añadir, buscar, listar y borrar contactos, guardándolos en un archivo para no perderlos.

**Guía de pasos:**

1. Define funciones `cargar()` y `guardar()` con JSON.
2. Define las operaciones: `agregar`, `buscar`, `listar`, `borrar`.
3. Crea el menú principal con `while True`.
4. Llama a `guardar` después de cada cambio.

**Solución de referencia:**

```python
import json
from pathlib import Path

ARCHIVO = Path("agenda.json")

def cargar():
    if ARCHIVO.exists():
        return json.loads(ARCHIVO.read_text(encoding="utf-8"))
    return {}

def guardar(agenda):
    ARCHIVO.write_text(
        json.dumps(agenda, indent=2, ensure_ascii=False),
        encoding="utf-8",
    )

def agregar(agenda):
    nombre = input("Nombre: ").strip()
    if not nombre:
        print("El nombre no puede estar vacío")
        return
    telefono = input("Teléfono: ").strip()
    agenda[nombre] = telefono
    guardar(agenda)
    print("Contacto guardado")

def buscar(agenda):
    texto = input("Buscar: ").strip().lower()
    encontrados = {n: t for n, t in agenda.items() if texto in n.lower()}
    if not encontrados:
        print("No se encontró nada")
    for nombre, tel in encontrados.items():
        print(f"{nombre}: {tel}")

def listar(agenda):
    if not agenda:
        print("La agenda está vacía")
        return
    for nombre in sorted(agenda):
        print(f"{nombre}: {agenda[nombre]}")

def borrar(agenda):
    nombre = input("Nombre a borrar: ").strip()
    if nombre in agenda:
        del agenda[nombre]
        guardar(agenda)
        print("Contacto borrado")
    else:
        print("Ese contacto no existe")

def main():
    agenda = cargar()
    while True:
        print("\n--- AGENDA ---")
        print("1. Añadir  2. Buscar  3. Listar  4. Borrar  5. Salir")
        opcion = input("Elige: ").strip()

        if opcion == "1":
            agregar(agenda)
        elif opcion == "2":
            buscar(agenda)
        elif opcion == "3":
            listar(agenda)
        elif opcion == "4":
            borrar(agenda)
        elif opcion == "5":
            print("¡Hasta luego!")
            break
        else:
            print("Opción no válida")

if __name__ == "__main__":
    main()
```

**Mejoras:** guardar también email y cumpleaños (diccionario por contacto); editar contactos; evitar duplicados.

---

## Proyecto 3: Control de gastos

**Qué hace:** registra gastos con categoría y monto, muestra el total y el total por categoría.

**Guía de pasos:**

1. Cada gasto es un diccionario: `{"descripcion": ..., "categoria": ..., "monto": ...}`.
2. Guarda todos en una lista y en un archivo JSON.
3. Crea funciones: `agregar_gasto`, `total`, `resumen_por_categoria`.
4. Menú principal.

**Solución de referencia:**

```python
import json
from pathlib import Path

ARCHIVO = Path("gastos.json")

def cargar():
    if ARCHIVO.exists():
        return json.loads(ARCHIVO.read_text(encoding="utf-8"))
    return []

def guardar(gastos):
    ARCHIVO.write_text(json.dumps(gastos, indent=2, ensure_ascii=False), encoding="utf-8")

def pedir_monto():
    while True:
        try:
            monto = float(input("Monto: "))
            if monto <= 0:
                print("Debe ser positivo")
                continue
            return monto
        except ValueError:
            print("Escribe un número")

def agregar_gasto(gastos):
    descripcion = input("Descripción: ").strip()
    categoria = input("Categoría (comida, transporte, ocio...): ").strip().lower()
    monto = pedir_monto()
    gastos.append({"descripcion": descripcion, "categoria": categoria, "monto": monto})
    guardar(gastos)
    print("Gasto registrado")

def total(gastos):
    return sum(g["monto"] for g in gastos)

def resumen_por_categoria(gastos):
    resumen = {}
    for g in gastos:
        cat = g["categoria"]
        resumen[cat] = resumen.get(cat, 0) + g["monto"]
    return resumen

def mostrar_resumen(gastos):
    if not gastos:
        print("Aún no hay gastos")
        return
    print(f"\nTotal gastado: {total(gastos):.2f}")
    for cat, monto in sorted(resumen_por_categoria(gastos).items(),
                             key=lambda par: par[1], reverse=True):
        print(f"  {cat:<12} {monto:>8.2f}")

def main():
    gastos = cargar()
    while True:
        print("\n1. Añadir gasto  2. Ver resumen  3. Salir")
        opcion = input("Elige: ")
        if opcion == "1":
            agregar_gasto(gastos)
        elif opcion == "2":
            mostrar_resumen(gastos)
        elif opcion == "3":
            break
        else:
            print("Opción no válida")

if __name__ == "__main__":
    main()
```

**Mejoras:** añadir la fecha de cada gasto (`datetime`); filtrar por mes; exportar a CSV.

---

## Proyecto 4: Lista de tareas con clases

**Qué hace:** gestiona tareas pendientes/completadas usando programación orientada a objetos.

**Guía de pasos:**

1. Clase `Tarea` con título y estado (hecha o no).
2. Clase `GestorTareas` que contiene una lista de tareas y métodos para agregar, completar, borrar y listar.
3. Un menú que use el gestor.

**Solución de referencia:**

```python
class Tarea:
    def __init__(self, titulo):
        self.titulo = titulo
        self.hecha = False

    def completar(self):
        self.hecha = True

    def __str__(self):
        marca = "x" if self.hecha else " "
        return f"[{marca}] {self.titulo}"


class GestorTareas:
    def __init__(self):
        self.tareas = []

    def agregar(self, titulo):
        self.tareas.append(Tarea(titulo))

    def completar(self, numero):
        if 1 <= numero <= len(self.tareas):
            self.tareas[numero - 1].completar()
            return True
        return False

    def borrar(self, numero):
        if 1 <= numero <= len(self.tareas):
            self.tareas.pop(numero - 1)
            return True
        return False

    def mostrar(self):
        if not self.tareas:
            print("No hay tareas")
            return
        for i, t in enumerate(self.tareas, start=1):
            print(f"{i}. {t}")

    def pendientes(self):
        return [t for t in self.tareas if not t.hecha]


def main():
    gestor = GestorTareas()
    while True:
        print("\n1. Añadir  2. Completar  3. Borrar  4. Ver  5. Salir")
        opcion = input("Elige: ")

        if opcion == "1":
            gestor.agregar(input("Tarea: "))
        elif opcion == "2":
            if not gestor.completar(int(input("Número: "))):
                print("Número inválido")
        elif opcion == "3":
            if not gestor.borrar(int(input("Número: "))):
                print("Número inválido")
        elif opcion == "4":
            gestor.mostrar()
            print("Pendientes:", len(gestor.pendientes()))
        elif opcion == "5":
            break
        else:
            print("Opción no válida")

if __name__ == "__main__":
    main()
```

**Mejoras:** guardar y cargar las tareas con JSON; añadir prioridad y fecha límite; usar `try/except` para los números.

---

## Proyecto 5: Mini banco con clases y errores

**Qué hace:** simula cuentas bancarias con depósito, retiro y transferencia, usando excepciones propias.

**Solución de referencia:**

```python
class SaldoInsuficiente(Exception):
    pass

class MontoInvalido(Exception):
    pass


class Cuenta:
    def __init__(self, titular, saldo=0):
        self.titular = titular
        self.saldo = saldo
        self.movimientos = []

    def depositar(self, monto):
        if monto <= 0:
            raise MontoInvalido("El monto debe ser positivo")
        self.saldo += monto
        self.movimientos.append(("depósito", monto))

    def retirar(self, monto):
        if monto <= 0:
            raise MontoInvalido("El monto debe ser positivo")
        if monto > self.saldo:
            raise SaldoInsuficiente(f"Saldo insuficiente: tienes {self.saldo}")
        self.saldo -= monto
        self.movimientos.append(("retiro", monto))

    def transferir(self, destino, monto):
        self.retirar(monto)
        destino.depositar(monto)

    def extracto(self):
        print(f"--- Extracto de {self.titular} ---")
        for tipo, monto in self.movimientos:
            print(f"{tipo:<10} {monto:>8}")
        print(f"Saldo: {self.saldo}")


ana = Cuenta("Ana", 100)
luis = Cuenta("Luis")

try:
    ana.depositar(50)
    ana.transferir(luis, 120)
    ana.retirar(500)           # lanza SaldoInsuficiente
except (SaldoInsuficiente, MontoInvalido) as e:
    print("Error:", e)

ana.extracto()
luis.extracto()
```

**Mejoras:** clase `Banco` que contenga varias cuentas; guardado en JSON; PIN para cada cuenta; intereses mensuales.

---

## Ideas para más proyectos (de fácil a más difícil)

| Idea | Conceptos que practicas |
|------|-------------------------|
| Conversor de unidades | funciones, `if`, diccionarios |
| Calculadora de propinas | `input`, matemáticas, f-strings |
| Generador de contraseñas | `random`, `string`, bucles |
| Piedra, papel o tijera | `random`, condicionales, bucles |
| Ahorcado | strings, listas, bucles, `random` |
| Quiz de preguntas | diccionarios, listas, bucles |
| Contador de palabras de un archivo | archivos, diccionarios, `Counter` |
| Tres en raya (consola) | listas anidadas, funciones |
| Biblioteca de libros | clases, JSON |
| Inventario de tienda | clases, diccionarios, archivos |
| Bot de Telegram simple | librerías externas, APIs |
| Web scraping sencillo | `requests`, `beautifulsoup4` |
| Pequeña web con Flask | web, plantillas, rutas |
| Análisis de datos con `pandas` | CSV, gráficas con `matplotlib` |

---

# APÉNDICES

## Apéndice A — Chuleta rápida (cheat sheet)

### Tipos y conversiones

```python
int("5")   float("2.5")   str(10)   bool(0)   list("abc")   tuple([1,2])   set([1,1,2])
type(x)    isinstance(x, int)
```

### Operadores

```text
+  -  *  /  //  %  **          aritméticos
== != < > <= >=                comparación
and  or  not                   lógicos
in  not in                     pertenencia
+=  -=  *=  /=  //=  %=  **=   asignación aumentada
```

### Strings

```python
len(s)  s.upper()  s.lower()  s.strip()  s.replace(a, b)  s.split(",")  ",".join(lista)
s.find(x)  s.count(x)  s.startswith(x)  s.endswith(x)  s[::-1]  f"{x:.2f}"
```

### Listas

```python
l.append(x)  l.insert(i, x)  l.extend(otra)  l.remove(x)  l.pop()  l.pop(i)  del l[i]
l.sort()  sorted(l)  l.reverse()  l.index(x)  l.count(x)  len(l)  sum(l)  min(l)  max(l)
l[1:4]  l[::-1]  l.copy()
```

### Diccionarios

```python
d[k] = v   d[k]   d.get(k, defecto)   del d[k]   d.pop(k)   k in d
d.keys()   d.values()   d.items()   d.update(otro)   len(d)
```

### Conjuntos

```python
s.add(x)  s.remove(x)  s.discard(x)  a | b  a & b  a - b  a ^ b
```

### Control de flujo

```python
if cond: ...  elif cond: ...  else: ...
while cond: ...
for x in secuencia: ...
for i in range(inicio, fin, paso): ...
break   continue   pass
try: ...  except Error as e: ...  else: ...  finally: ...
```

### Funciones

```python
def f(a, b=0, *args, **kwargs):
    return a + b
lambda x: x * 2
```

### Clases

```python
class A(Padre):
    def __init__(self, x):
        super().__init__()
        self.x = x
    def __str__(self):
        return f"A({self.x})"
```

### Archivos

```python
with open("f.txt", "r", encoding="utf-8") as f:
    contenido = f.read()
```

### Comprensiones

```python
[x * 2 for x in lista if x > 0]
{k: v for k, v in pares}
{x for x in lista}
(x for x in lista)
```

## Apéndice B — Los errores más comunes y qué significan

| Mensaje | Qué pasó | Cómo arreglarlo |
|---------|----------|-----------------|
| `SyntaxError: invalid syntax` | Escribiste algo que Python no entiende | Revisa paréntesis, comillas y `:` en la línea indicada y la anterior |
| `IndentationError` | Indentación incorrecta | Usa 4 espacios; no mezcles tabs y espacios |
| `NameError: name 'x' is not defined` | Usaste algo que no existe | Revisa mayúsculas, ortografía y que la hayas creado antes |
| `TypeError: can only concatenate str...` | Mezclaste texto y números | Convierte con `str()` o usa f-strings |
| `TypeError: ... takes 2 positional arguments but 3 were given` | Número de argumentos incorrecto | Revisa la definición de la función |
| `ValueError: invalid literal for int()` | Intentaste convertir texto no numérico | Valida antes o usa `try/except` |
| `IndexError: list index out of range` | Índice demasiado grande | Recuerda que el último índice es `len(l) - 1` |
| `KeyError: 'x'` | La clave no existe | Usa `d.get("x")` o comprueba con `in` |
| `ZeroDivisionError` | Dividiste entre 0 | Comprueba el divisor antes |
| `AttributeError: 'X' object has no attribute 'y'` | El objeto no tiene ese método/atributo | Revisa el nombre y el tipo del objeto |
| `FileNotFoundError` | El archivo no existe | Revisa nombre y carpeta; usa `os.path.exists` |
| `ModuleNotFoundError` | Módulo no instalado/mal escrito | `pip install nombre` o revisa el nombre |
| `RecursionError` | Recursión sin fin | Revisa el caso base |
| `UnboundLocalError` | Usas una variable local antes de asignarla | Revisa `global` o pasa el dato como parámetro |

## Apéndice C — Glosario

- **Algoritmo:** serie de pasos para resolver un problema.
- **Argumento:** dato que se pasa a una función al llamarla.
- **Atributo:** variable que pertenece a un objeto.
- **Bucle:** estructura que repite instrucciones.
- **Bug:** error en un programa.
- **Clase:** plantilla para crear objetos.
- **Comentario:** nota ignorada por Python (`#`).
- **Condicional:** estructura que decide qué ejecutar (`if`).
- **Constructor:** método `__init__` que prepara un objeto nuevo.
- **Excepción:** error que ocurre mientras el programa corre.
- **Función:** bloque de código con nombre y reutilizable.
- **Iterable:** algo que se puede recorrer con `for`.
- **Método:** función que pertenece a un objeto o clase.
- **Módulo:** archivo `.py` con código reutilizable.
- **Objeto:** ejemplar creado a partir de una clase.
- **Parámetro:** variable en la definición de una función.
- **Variable:** nombre que guarda un dato.
- **Tipo:** categoría de un dato (`int`, `str`, `list`...).
- **Mutable / inmutable:** que se puede / no se puede modificar después de creado.

## Apéndice D — Plan de estudio sugerido

| Semana | Módulos | Objetivo |
|--------|---------|----------|
| 1 | 0 – 3 | Tener Python funcionando y manejar variables y operadores |
| 2 | 4 – 6 | Texto, entrada de datos y decisiones |
| 3 | 7 – 8 | Bucles |
| 4 | 9 – 11 | Listas, tuplas, conjuntos, diccionarios |
| 5 | 12 – 13 | Funciones y recursión |
| 6 | 14 – 16 | Comprensiones, archivos y errores |
| 7 | 17 – 19 | Módulos y programación orientada a objetos |
| 8 | 20 – 22 | Funciones avanzadas, JSON/CSV, pruebas y buenas prácticas |
| 9+ | 23 | Proyectos propios |

Con **45–60 minutos al día** es perfectamente realista. La constancia importa más que las maratones.

**Rutina diaria recomendada:**

1. 10 min: repasar lo del día anterior (reescribe un ejercicio de memoria).
2. 25 min: módulo nuevo (teoría + escribir los ejemplos).
3. 20 min: ejercicios.
4. 5 min: anota qué no entendiste para mañana.

## Apéndice E — Siguientes pasos

Cuando termines este curso, elige **un camino** según lo que te guste:

- **Automatización:** scripts para organizar archivos, enviar correos, rellenar hojas de cálculo (`os`, `shutil`, `openpyxl`, `smtplib`).
- **Web:** `Flask` o `Django` (backend), y aprender HTML/CSS/JavaScript básicos.
- **Datos:** `pandas`, `numpy`, `matplotlib`; SQL básico.
- **Bots y APIs:** `requests`, bots de Telegram/Discord.
- **Juegos:** `pygame`.
- **Inteligencia artificial:** primero matemáticas básicas y `numpy`; luego `scikit-learn`.
- **Algoritmos y estructuras de datos:** pilas, colas, árboles, búsqueda y ordenación; plataformas con retos de práctica.

**Consejos finales:**

1. **Programa todos los días**, aunque sea 20 minutos.
2. **Construye proyectos** que te interesen; ahí es donde de verdad aprendes.
3. **Lee código de otros** y trata de entenderlo.
4. **No memorices**: entiende. La sintaxis se busca; la lógica se piensa.
5. **No te compares** con nadie. Compara tu "yo" de hoy con tu "yo" de hace un mes.
6. **Los errores son tus maestros.** Cada bug que resuelves te hace mejor.
7. **Cuando algo no salga, vuelve al método de 5 pasos** del Módulo 0.

---

# 🎓 ¡Terminaste!

Si llegaste hasta aquí haciendo los ejercicios, ya sabes más Python de lo que crees. Ahora **crea cosas**. Un programa que resuelva un problema real tuyo vale más que cien ejercicios.

**¡A programar!** 🐍
