# Teoria parcial

## **Pregunta 1 (1 Punto):**

### Explique en detalle el principio SOLID **"Open/Closed"** y proporcione un ejemplo de código en Python donde este principio se ha violado y cómo puede corregirlo.
El principo "Open/Closed" de SOLID nos explica que los modulos de software deben ser abiertos para su extension pero cerrados para su modificación. Que es lo que esto significa?
- Abierto para la extensión: Hablando pronto y mal significa que podemos cambiar lo que hace el modulo, pero usando un lenguaje tecnico esto significa que el comportamiento del modulo puede extenderse. Por ejemplo si los requisitos de la aplicacion van cambiando, el modulo permite su modificación para así satisfacer los cambios.
- Cerrado para su modificación: Un modulo se dice que esta cerrado si tiene una interface estable y bien definida. Es decir que si el modulo es modificado, este no debe modificar el codigo anterior.

Y esa es realmente la esencia de este principio. Debería ser fácil cambiar
el comportamiento de un módulo sin cambiar el código fuente de ese
módulo. Esto no significa que nunca cambiará el código fuente. Lo que
significa es que debemos esforzarnos por lograr que nuestro código esté
estructurado de forma que, cuando el comportamiento cambie de la
manera esperada, no debamos hacer cambios radicales en todos los
módulos del sistema. Idealmente, podremos agregar el nuevo
comportamiento, añadiendo código nuevo y cambiando poco o nada del
código antiguo.
La forma de implementar este principio en el mundo práctico, es a
través del polimorfismo, ya sea por interfaces o clases abstractas.

Ejemplo con código en python.
$$
from django.contrib.auth.models import AbstractUser
from django.db import models
class User(AbstractUser):
 bio = models.TextField(max_length=500, blank=True)
 location = models.CharField(max_length=30, blank=True)
 birth_date = models.DateField(null=True, blank=True)
$$
Explicación del codigo; 
En el codigo anterior, importamos desde django la clase AbstractUser y después, ampliamos la clase con bio, location y birth_date, pero esto lo hacemos sin modificar la clase anterior de "AbstractUser", sino que lo hacemos heredando dicha clase. Cumpliendo asi con el principio de Open/Close



