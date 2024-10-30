# Parcial. Principios y patrones
## Link al repositorio; https://github.com/seerraa16/Principios-y-Patrones.-Parcial.git
### Autor; Alejandro Serrano Catalina

#### Pregunta 1 (1 Punto):

Explique en detalle el principio SOLID "Open/Closed" y proporcione un ejemplo de código en Python donde este principio se ha violado y cómo puede corregirlo.

#### Pregunta 2(1 Punto):

Describa el patrón de diseño "Factory". ¿En qué situaciones sería útil este patrón? Proporcione un ejemplo de cómo implementaría este patrón en Python para un problema relacionado con la ingeniería matemática, como la creación de diferentes tipos de funciones matemáticas.

#### Pregunta 3(1 Punto):

Explique el antipatrón "God Object". ¿Por qué es perjudicial este antipatrón y qué problemas puede causar en el desarrollo de software? Proporcione un ejemplo de un "God Object" en un contexto de ingeniería matemática y explique cómo podría refactorizarlo para evitar este antipatrón.

#### Pregunta 4(1 Punto):

Los principios DRY (Don't Repeat Yourself) y KISS (Keep It Simple, Stupid) son fundamentales para escribir código de alta calidad. Proporcione un ejemplo de un fragmento de código Python que viole estos principios. Describa cómo lo refactorizaría para adherirse a los principios DRY y KISS.

#### Pregunta 5(1 Punto):

El patrón de diseño "Observer" permite que un objeto notifique a otros objetos sobre los cambios en su estado. Describa una situación en el contexto de la ingeniería matemática donde este patrón sería útil. Implemente un ejemplo simple de este patrón en Python para ilustrar su respuesta.

#### Pregunta Práctica 1: Refactorización de código con Principios SOLID(2,5 Puntos)

Se le proporciona un fragmento de código Python que maneja diferentes tipos de formas geométricas. Actualmente, el código viola el Principio de Responsabilidad Única (SRP) y el Principio Abierto/Cerrado (OCP) de SOLID. Su tarea es refactorizar este código para que se adhiera a estos principios.

``` py
    class Shape:
        def __init__(self, type):
            self.type = type

    class AreaCalculator:
        def __init__(self, shapes):
            self.shapes = shapes

        def total_area(self):
            total = 0
            for shape in self.shapes:
                if shape.type == "circle":
                    radius = 1.0  # Supongamos que el radio es siempre 1 para este ejemplo
                    total += 3.14159 * radius * radius
                elif shape.type == "square":
                    side = 1.0  # Supongamos que el lado es siempre 1 para este ejemplo
                    total += side * side
            return total

    shapes = [Shape("circle"), Shape("square")]
    calculator = AreaCalculator(shapes)
    print(calculator.total_area())
```
#### Pregunta Práctica 2: Implementación de Patrón de Diseño Estrategia(2,5 Puntos)

En ingeniería matemática, es común que necesitemos intercambiar diferentes algoritmos dependiendo de la situación. Considere una aplicación que debe realizar la integración numérica de una función. Hay diferentes métodos para realizar esta integración, como el método del trapecio, el método de Simpson, la cuadratura gaussiana, entre otros.

Se le pide que implemente este escenario utilizando el patrón de diseño estrategia. Debe proporcionar una estructura que permita cambiar fácilmente el método de integración. Incluya al menos dos métodos específicos (por ejemplo, Trapecio y Simpson) y demuestre cómo se podrían cambiar estos métodos en tiempo de ejecución.

### Rúbrica para el examen:

#### regunta 1:

- Comprendiendo el principio Open/Closed y explicando correctamente (20%)
- Proporcionando un ejemplo de violación de principio en Python (30%)
- Proporcionando una solución para corregir la violación (30%)
- Calidad de la explicación (20%)

#### Pregunta 2:

- Comprendiendo y explicando correctamente el patrón de diseño "Factory" (20%)
- Proporcionando un ejemplo relevante de situación de uso (20%)
- Implementando correctamente el patrón de diseño en Python (40%)
- Relacionando la implementación con la ingeniería matemática (20%)

#### Pregunta 3:

- Comprendiendo y explicando correctamente el antipatrón "God Object" (20%)
- Identificando los problemas potenciales causados por este antipatrón (20%)
- Proporcionando un ejemplo de "God Object" en un contexto de ingeniería matemática (30%)
- Proponiendo una solución de refactorización (30%)

#### Pregunta 4:

- Comprendiendo y explicando correctamente los principios DRY y KISS (20%)
- Proporcionando un ejemplo de violación de principio en Python (30%)
-  una solución para corregir la violación (30%)
- Calidad de la explicación (20%)

#### Pregunta 5:

- Comprendiendo y explicando correctamente el patrón de diseño "Observer" (20%)
- Identificando una situación relevante en la ingeniería matemática para el uso de este patrón (20%)
- Implementando correctamente el patrón en Python (40%)
- Calidad de la explicación (20%)

#### Pregunta Práctica 1: Refactorización de código con Principios SOLID

- Identificación correcta de violaciones de los principios SOLID (30%)
- Correcta refactorización del código de acuerdo con el Principio de Responsabilidad Única (SRP) (35%)
- Correcta refactorización del código de acuerdo con el Principio Abierto/Cerrado (OCP) (35%)

#### Pregunta Práctica 2: Implementación de Patrón de Diseño Estrategia

- Entendimiento y explicación del problema (20%)
- Diseño adecuado del patrón de estrategia en el código (30%)
- Implementación correcta de al menos dos estrategias (trapecio y Simpson) (30%)
- Demostración de cambio de estrategia en tiempo de ejecución (20%)