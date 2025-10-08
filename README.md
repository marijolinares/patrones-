# patrones-
PATRONES DE DISEÑO GoF
Los Patrones de Diseño de la "Gang of Four" (GOF) son una colección de soluciones comunes a problemas recurrentes en el diseño de software orientado a objetos. Estos patrones permiten mejorar la estructura y la flexibilidad del código, haciendo que las aplicaciones sean más fáciles de mantener y extender a lo largo del tiempo.
Patrones Creacionales
se centran en la forma en que los objetos son creados. Donde su  objetivo es evitar la creación directa de objetos con "new", proporcionando formas más flexibles de crear instancias y gestionar la construcción de estos objetos. Aquí tienes una lista de los patrones creacionales más importantes:
 
•	Factory Method: Proporciona una interfaz para crear objetos, pero deja que las subclases decidan cuál es la clase a instanciar.
•	Abstract Factory: Crea familias de objetos relacionados sin especificar sus clases concretas.
•	Builder: Separa la construcción de un objeto complejo de su representación, permitiendo crear diferentes representaciones.
•	Prototype: Permite la creación de nuevos objetos copiando una instancia existente (clonación).
•	Singleton: Garantiza que una clase solo tenga una instancia, y proporciona un punto de acceso global a esa instancia.

Patrones Estructurales
ocupan de la composición de las clases y objetos, es decir, de cómo se pueden combinar objetos para formar estructuras más grandes y flexibles. Su objetivo es facilitar las relaciones entre entidades sin modificar sus interfaces.
 
•	Adapter: Permite que dos interfaces incompatibles trabajen juntas.
•	Bridge: Desacopla una abstracción de su implementación para que ambas puedan evolucionar independientemente.
•	Composite: Permite tratar objetos individuales y composiciones de objetos de manera uniforme.
•	Decorator: Añade responsabilidades adicionales a un objeto de manera dinámica.
•	Facade: Proporciona una interfaz simplificada para un sistema de clases.
•	Flyweight: Minimiza el uso de memoria compartiendo tantos datos como sea posible con objetos similares.
•	Proxy: Proporciona un sustituto o marcador de posición para otro objeto para controlar el acceso a este.

Patrones de Comportamiento
se centran en la comunicación entre objetos, la forma en que interactúan y se delegan responsabilidades. Estos patrones facilitan las interacciones complejas, pero de manera flexible y reutilizable.
 
•	Chain of Responsibility: Pasa una solicitud a lo largo de una cadena de gestores hasta que uno de ellos la procese.
•	Command: Encapsula una solicitud como un objeto, permitiendo parametrizar a los clientes con diferentes solicitudes.
•	Interpreter: Proporciona una manera de evaluar sentencias en un lenguaje.
•	Iterator: Proporciona una manera de acceder secuencialmente a los elementos de un objeto agregado sin exponer su representación interna.
•	Mediator: Reduce la complejidad de la comunicación entre múltiples objetos al centralizarla en un solo objeto mediador.
•	Memento: Permite capturar y restaurar el estado de un objeto sin violar su encapsulamiento.
•	Observer: Define una dependencia uno a muchos entre objetos, de modo que cuando uno cambie de estado, todos sus dependientes sean notificados.
•	State: Permite que un objeto altere su comportamiento cuando su estado interno cambia.
•	Strategy: Permite seleccionar un algoritmo en tiempo de ejecución.
•	Template Method: Define el esqueleto de un algoritmo en una operación, dejando algunos pasos para que las subclases los implementen.
•	Visitor: Representa una operación que se realiza sobre los elementos de una estructura de objetos. (UNIVERSOJAVA, 2024)

Ventajas 
	Mejora de la estructura y flexibilidad del código: Permiten crear aplicaciones más estructuradas y fáciles de mantener y extender a lo largo del tiempo. 
	Reutilización de código: Proporcionan soluciones reutilizables que pueden ser aplicadas a problemas de diseño comunes, ahorrando tiempo y esfuerzo. 
	Facilitación del trabajo en equipo: Los patrones guían a los desarrolladores hacia una mejor arquitectura, lo que facilita la colaboración y la comunicación entre ellos. 
	Optimización del rendimiento: Algunos patrones, como el patrón de factoría, ayudan a mejorar el rendimiento de la gestión de la memoria y la creación de objetos. 
	Mejora de la calidad del código: Al aplicar patrones, se logra un código más limpio y organizado, lo que facilita la comprensión y mantenimiento del software. 

Desventajas 
×	Sobrecarga de Complejidad
×	Curva de Aprendizaje
×	Rigidez en la Aplicación
×	Tendencia a Sobre ingeniería

Ejemplos de uso en la industria 
Problema: ¿Cómo resolver interfaces incompatibles, o proporcionar una interfaz 
estable para componentes parecidos con diferentes interfaces? 
Solución: Convierta la interfaz original de una componente en otra, mediante un 
objeto adaptador intermedio. 
El propósito de este patrón es convertir la interfaz de una clase en otra interfaz 
que es la que esperan los clientes. Este patrón permite que cooperen clases que de otra forma no podrían colaborar por no tener compatibilidad entre ellas. 
Debería usarse el patrón Adaptador cuando: 
•	Se quiere utilizar una clase existente y su interfaz no concuerda con lo 
que se espera. 
•	Se quiere crear una clase reutilizable que coopere con clases no 
relacionadas o que no han sido previstas, i.e. clases que no tienen por qué 
tener interfaces compatibles. 

Los participantes en este patrón realizan los siguientes roles: 
•	Objetivo: define los servicios del dominio que usa el cliente. Representa 
un interfaz estable con los servicios tal cual espera el cliente. 
•	Cliente: utiliza los servicios del paquete a través del interfaz Objetivo. 
•	Adaptable: Implementa los servicios del paquete. 
•	Adaptador: adapta la interfaz de Adaptable a la interfaz Objetivo. 
Los clientes llaman a operaciones a través de la interfase estable. A su vez el 
adaptador llama a operaciones de Adaptable que son las que satisfacen las peticiones. 
En una implementación en C++ de un adaptador de clases, Adaptador debería 
heredar públicamente de objetivo y tener como atributo privado a un objeto de la clase 
Adaptable. 
Nótese que los nombres de los tipos incluyen el nombre de patrón “Adaptador”. 
La aplicación del Adaptador es una especialización de Variaciones Protegidas, 
Indirección y Polimorfismo. En GRASP es el polimorfismo, aquí es una especialización 
que se llama Adaptador. Se puede analizar muchos patrones más complejos y 
especializados en función de la familia GRASP. Existen muchos publicados y es el 
alfabeto del DOO. (Platero, 2017)

PATRONES EMERGENTES 
Un conjunto de pares atributo-valor que aparecen una cantidad de veces significativamente mayor en una clase que en el resto de las clases de un problema dado. (Milton García-Borroto, 2008)
