IC-4700 Lenguajes de programación  
Prof. Diego Munguia Molina  
IC-AL  
---
# Proyecto 2

## Objetivos de aprendizaje

1. Modelar el funcionamiento interno de los principios de programación orientada a objetos en un lenguaje de programación (III).

## Descripción

Queremos implementar una calculadora de notación polaca inversa que permita realizar las operaciones aritméticas simples de suma y multiplicación.

## Requerimientos funcionales

* La calculadora utiliza una pila para almacenar los datos a calcular.

* La persona usuaria ingresa una entrada a la vez desde `stdin` y la calculadora reacciona de acuerdo con los requerimientos aquí planteados.

```
$ bin/byodc
_
```

* La entrada puede ser un número entero, un operador aritmético `+` o `*`, o un comando de pila.

* Cada vez que la persona usuaria ingresa una entrada, esta se procesa de acuerdo con los requerimientos aquí planteados y luego la calculadora queda en espera de la siguiente entrada.

* Cuando la persona usuaria ingresa un número entero, este se agrega a la pila.

```
$ bin/byodc
1
_
```

* Cuando la persona usuaria ingresa el comando de pila `p`, se imprime el valor que está en el tope de la pila sin modificarla.

```
$ bin/byodc
3
p
3
_
```

* Cuando la persona usuaria ingresa el comando de pila `p` y la pila está vacía, se imprime un mensaje que indica que la pila está vacía.

```
$ bin/byodc
p
byodc: pila vacía
_
```

* Cuando la persona usuaria ingresa el comando de pila `n`, se saca el valor que está en el tope de la pila y se imprime.

```
$ bin/byodc
2
n
2
_
```

* Cuando la persona usuaria ingresa el comando de pila `n` y la pila está vacía, se imprime un mensaje que indica que la pila está vacía.

```
$ bin/byodc
n
byodc: pila vacía
_
```

* Cuando la persona usuaria ingresa el comando de pila `f`, se imprime todo el contenido de la pila en orden lifo sin modificarla.

```
$ bin/byodc
1
2
3
4
f
4
3
2
1
_
```

* Cuando la persona usuaria ingresa el comando de pila `c`, se vacía la pila.

```
$ bin/byodc
1
2
3
c
f
_
```

* Cuando la persona usuaria ingresa un operador aritmético `+`, se sacan los dos últimos números de la pila, se suman y el resultado se agrega a la pila.

```
$ bin/byodc
2
3
+
p
5
_
```

* Cuando la persona usuaria ingresa un operador aritmético `*`, se sacan los dos últimos números de la pila, se multiplican y el resultado se agrega a la pila.

```
$ bin/byodc
2
3
*
p
6
_
```

* Cuando la persona usuaria ingresa un operador aritmético y la pila tiene menos de dos elementos, se imprime un mensaje que indica que la pila no tiene suficientes elementos para realizar la operación y se mantiene la pila sin modificarla.

```
$ bin/byodc
3
+
byodc: no hay suficientes operandos
f
3
_
```

* Cuando la persona usuaria ingresa una expresión compleja  en una sola línea, donde cada elemento está separado por un espacio en blanco, se procesa elemento por elemento de acuerdo con los requerimientos aquí planteados.

```
$ bin/byodc
1 3 f + 2 * f n p
3
1
8
8
byodc: la pila está vacía
```

* Cuando la persona usuaria ingresa `Ctrl+D` la calculadora finaliza su ejecución.

```
$ bin/byodc
1
2
<Ctrl+D>
$ _
```

## Requerimientos no funcionales

* La calculadora debe ser fácilmente extensible. Es decir, debe ser posible agregar nuevos operadores aritméticos y comandos de pila agregando nuevos objetos pero sin modificar operaciones existentes.

* Se deben respetar los principios de programación orientada a objetos: abstracción, encapsulación, y polimorfismo.

## Metodología

* El proyecto se trabajará en equipos.
* Cada equipo designará dos personas con el rol de relatoras, estas personas tendrán la responsabilidad de tomar notas durante las reuniones de revisión que serán utilizadas posteriormente para hacer mejoras al código.
* El proyecto se desarrollará en el transcurso de dos semanas y tendrá dos entregas, una entrega parcial después de la primera semana de trabajo, y una entrega final después de la segunda semana de trabajo.
* El proyecto se desarrollará en C siguiendo el paradigma orientado a objetos.

## Rúbricas de evaluación

Disponible en el siguiente enlace:

https://docs.google.com/spreadsheets/d/1fCWvkyNOVmBsfhL12OybgaKcFvRvPvwFl6djFP2qV1Q
