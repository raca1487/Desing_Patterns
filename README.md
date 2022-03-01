# PATRONES DE DISEÑO

## PATRONES CREACIONALES

### SINGLETON
Patrón de **diseño creacional** que nos permite asegurarnos de que una clase tenga una única instancia, a la vez que proporciona un punto de acceso global a dicha instancia.

La solución tiene dos pasos a seguir comunes:
* Hacer privado el constructor por defecto para evitar que otros objetos utilicen el operador `new` con la clase Singleton.
* Crear un método de creación estático que actúe como constructor.
> Tras bambalinas, este método invoca al constructor privado para crear un objeto y lo guarda en un campo estático. Las siguientes llamadas a este método devuelven el objeto almacenado en caché.

### FACTORY METHOD
Patrón de **diseño creacional** que proporciona una interfaz para crear objetos en una superclase, mientras permite a las subclases alterar el tipo de objetos que se crearán.
Dicho de otro modo, se trata de efinir una *interface* para crear un objeto, dejando a las subclases decidir de que tipo de clase se realizará la instancia en tiempo de ejecución.

La solución sugiere que, en lugar de llamar al operador `new` (reducir su uso) para construir objetos directamente, se invoque a un método fábrica especial.

![Factory](https://github.com/raca1487/Desing_Patterns/wiki/img/factory_pattern.PNG)

### ABSTRACT METHOD
Patrón de **diseño creacional** que nos permite producir familias de objetos relacionados sin especificar sus clases concretas.
Funcionan en torno a una superfábrica que crea otras fábricas.

La solución que sugiere el patrón ***Abstract Factory*** es:
* Declarar de forma explícita interfaces para cada producto diferente de la familia de productos.
* Declarar la *Fábrica abstracta* (una interfaz con una lista de métodos de creación para todos los productos que son parte de la familia de productos).

![Abstract Factory](https://github.com/raca1487/Desing_Patterns/wiki/img/abstract_pattern.PNG)


## PATRONES ESTRUCTURALES

### ADAPTER
Patrón de **diseño estructural** que permite la colaboración entre objetos con interfaces incompatibles.
Este patrón involucra una sola clase que es responsable de unir funcionalidades de interfaces independientes o incompatibles.

Los adaptadores no solo convierten datos a varios formatos, sino que también ayudan a objetos con distintas interfaces a colaborar. Funciona así:
* El adaptador obtiene una interfaz compatible con uno de los objetos existentes.
* Utilizando esta interfaz, el objeto existente puede invocar con seguridad los métodos del adaptador.
* Al recibir una llamada, el adaptador pasa la solicitud al segundo objeto, pero en un formato y orden que ese segundo objeto espera.

![Adapter](https://github.com/raca1487/Desing_Patterns/wiki/img/adapter_pattern.PNG)

### FACADE
Patrón de **diseño estructural** que proporciona una interfaz simplificada a una biblioteca, un framework o cualquier otro grupo complejo de clases. Este patrón oculta las complejidades del sistema y proporciona una interfaz para el cliente mediante la cual el cliente puede acceder al sistema.

Una fachada es una clase que proporciona una interfaz simple a un subsistema complejo que contiene muchas partes móviles. Puede proporcionar una funcionalidad limitada en comparación con trabajar directamente con el subsistema. Sin embargo, tan solo incluye las funciones realmente importantes para los clientes.

> Tener una fachada resulta útil cuando tienes que integrar tu aplicación con una biblioteca sofisticada con decenas de funciones, de la cual sólo necesitas una pequeña parte.

![Facade](https://github.com/raca1487/Desing_Patterns/wiki/img/facade_pattern.PNG)

### DECORATOR
Patrón de **diseño estructural** que te permite añadir funcionalidades a objetos colocando estos objetos dentro de objetos encapsuladores especiales que contienen estas funcionalidades.

Este patrón crea una clase de decorador que envuelve la clase original y proporciona una funcionalidad adicional que mantiene intacta la firma de los métodos de clase.

![Decorator](https://github.com/raca1487/Desing_Patterns/wiki/img/decorator_pattern.PNG)

### PROXY
Patrón de **diseño estructural** que permite proporcionar un sustituto o marcador de posición para otro objeto. Un proxy controla el acceso al objeto original, permitiendo hacer algo antes o después de que la solicitud llegue al objeto original.

En este patrón, una clase representa la funcionalidad de otra clase, es decir, se crea un objeto que tiene un objeto original para interconectar su funcionalidad con el mundo exterior.

![Proxy](https://github.com/raca1487/Desing_Patterns/wiki/img/proxy_pattern.PNG)

### BRIDGE
Patrón de **diseño estructural** que te permite dividir una clase grande, o un grupo de clases estrechamente relacionadas, en dos jerarquías separadas (abstracción e implementación) que pueden desarrollarse independientemente la una de la otra.

Este patrón involucra una interfaz que actúa como un puente que hace que la funcionalidad de las clases concretas sea independiente de las clases del implementador de la interfaz. Ambos tipos de clases se pueden alterar estructuralmente sin afectarse entre sí.

![Bridge](https://github.com/raca1487/Desing_Patterns/wiki/img/bridge_pattern.PNG)