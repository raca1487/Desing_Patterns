# PATRONES DE DISEÑO

## PATRONES CREACIONALES

### SINGLETON
Patrón de diseño creacional que nos permite asegurarnos de que una clase tenga una única instancia, a la vez que proporciona un punto de acceso global a dicha instancia.

La solución tiene dos pasos a seguir comunes:
* Hacer privado el constructor por defecto para evitar que otros objetos utilicen el operador `new` con la clase Singleton.
* Crear un método de creación estático que actúe como constructor.
> Tras bambalinas, este método invoca al constructor privado para crear un objeto y lo guarda en un campo estático. Las siguientes llamadas a este método devuelven el objeto almacenado en caché.

### FACTORY METHOD
Patrón de diseño creacional que proporciona una interfaz para crear objetos en una superclase, mientras permite a las subclases alterar el tipo de objetos que se crearán.
Dicho de otro modo, se trata de efinir una *interface* para crear un objeto, dejando a las subclases decidir de que tipo de clase se realizará la instancia en tiempo de ejecución.

La solución sugiere que, en lugar de llamar al operador `new` (reducir su uso) para construir objetos directamente, se invoque a un método fábrica especial.

![Factory](https://github.com/raca1487/Desing_Patterns/wiki/img/factory_pattern.PNG)

### ABSTRACT METHOD
Patrón de diseño creacional que nos permite producir familias de objetos relacionados sin especificar sus clases concretas.
Funcionan en torno a una superfábrica que crea otras fábricas.

La solución que sugiere el patrón ***Abstract Factory*** es:
* Declarar de forma explícita interfaces para cada producto diferente de la familia de productos.
* Declarar la *Fábrica abstracta* (una interfaz con una lista de métodos de creación para todos los productos que son parte de la familia de productos).

![Abstract Factory](https://github.com/raca1487/Desing_Patterns/wiki/img/abstract_pattern.PNG)