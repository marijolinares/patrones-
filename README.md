# patrones-
=>PATRONES DE DISEÑO GoF
Los Patrones de Diseño de la "Gang of Four" (GOF) son una colección de soluciones comunes a problemas recurrentes en el diseño de software orientado a objetos. Estos patrones permiten mejorar la estructura y la flexibilidad del código, haciendo que las aplicaciones sean más fáciles de mantener y extender a lo largo del tiempo.
Patrones Creacionales
se centran en la forma en que los objetos son creados. Donde su  objetivo es evitar la creación directa de objetos con "new", proporcionando formas más flexibles de crear instancias y gestionar la construcción de estos objetos. Aquí tienes una lista de los patrones creacionales más importantes:
 
•	Factory Method: Proporciona una interfaz para crear objetos, pero deja que las subclases decidan cuál es la clase a instanciar.
•	Abstract Factory: Crea familias de objetos relacionados sin especificar sus clases concretas.
•	Builder: Separa la construcción de un objeto complejo de su representación, permitiendo crear diferentes representaciones.
•	Prototype: Permite la creación de nuevos objetos copiando una instancia existente (clonación).
•	Singleton: Garantiza que una clase solo tenga una instancia, y proporciona un punto de acceso global a esa instancia.

=>Patrones Estructurales
ocupan de la composición de las clases y objetos, es decir, de cómo se pueden combinar objetos para formar estructuras más grandes y flexibles. Su objetivo es facilitar las relaciones entre entidades sin modificar sus interfaces.
 
•	Adapter: Permite que dos interfaces incompatibles trabajen juntas.
•	Bridge: Desacopla una abstracción de su implementación para que ambas puedan evolucionar independientemente.
•	Composite: Permite tratar objetos individuales y composiciones de objetos de manera uniforme.
•	Decorator: Añade responsabilidades adicionales a un objeto de manera dinámica.
•	Facade: Proporciona una interfaz simplificada para un sistema de clases.
•	Flyweight: Minimiza el uso de memoria compartiendo tantos datos como sea posible con objetos similares.
•	Proxy: Proporciona un sustituto o marcador de posición para otro objeto para controlar el acceso a este.

=>Patrones de Comportamiento
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

=>PATRONES EMERGENTES 
Un conjunto de pares atributo-valor que aparecen una cantidad de veces significativamente mayor en una clase que en el resto de las clases de un problema dado. (Milton García-Borroto, 2008)

*MVC (Model-View-Controller)

MVC divide una aplicación en tres componentes:
  Modelo (Model): representa los datos, la lógica de negocio y las reglas.
 Vista (View): se encarga de mostrar los datos (interfaz de usuario).
 Controlador (Controller): recibe las entradas del usuario (eventos, acciones), las interpreta, coordina con el modelo y selecciona la vista a mostrar.
Buscando separar claramente la interfaz de usuario de la lógica de negocio y de los datos.

Ventajas
•	Buena separación de responsabilidades, lo que facilita el mantenimiento, pruebas y evolución.
•	Permite que varias vistas usen el mismo modelo.
•	Facilita el trabajo en equipo (por ejemplo, un diseñador de UI puede trabajar en la Vista sin tocar la lógica del Modelo).
•	Es un patrón bastante conocido, con muchos frameworks que lo adoptan.

Desventajas
•	En aplicaciones muy simples puede generar sobreingeniería.
•	Si no se controla bien, la lógica puede «filtrarse» al controlador, produciendo controladores muy grandes (god controllers).
•	El flujo entre controlador → modelo → vista puede ser difícil de seguir en aplicaciones complejas.

 Ejemplo 
•	Por ejemplo, en un sistema web donde tienes páginas diferentes que muestran datos del usuario (perfil, historial, ajustes), con lógica común en el modelo y controladores que orquestan el flujo entre ellas.

*DAO (Data Access Object)

DAO es un patrón de acceso a datos: define una interfaz abstracta para operaciones de persistencia (CRUD, consultas) para un tipo específico de entidad, de modo que la lógica de acceso a datos quede encapsulada.
Generalmente se acompañan de DTO (Data Transfer Objects) para transportar datos entre capas.

Ventajas
•	Oculta los detalles de persistencia (SQL, librerías, conexiones) al resto del sistema.
•	Promueve la separación entre lógica de negocio y acceso a datos.
•	Facilita cambiar la implementación de persistencia (por ejemplo, cambiar de base de datos relacional a NoSQL) sin afectar la lógica de negocio.
•	Facilita pruebas unitarias (puedes sustituir DAOs por mocks o stubs).

Desventajas
•	Añade una capa extra de abstracción, lo que puede ser percibido como sobrecarga en proyectos pequeños.
•	Si no se diseña bien, los DAOs pueden volverse muy genéricos o muy especializados, perdiendo coherencia.
•	En consultas complejas con muchas uniones o lógica específica, puede que la abstracción “DAO estándar” no sea suficiente y el DAO tenga que incluir lógica compleja (rompiendo la responsabilidad única).

Ejemplo
•	En casi cualquier aplicación con persistencia de datos que desees estructurar bien: aplicaciones empresariales, APIs, microservicios.
•	Por ejemplo, en un sistema que maneje usuarios, productos, pedidos: puedes tener UserDAO, ProductDAO, OrderDAO con operaciones que encapsulan SQL u ORM.

*CQRS (Command Query Responsibility Segregation)

CQRS propone separar las operaciones de escritura / comandos (Commands) de las operaciones de lectura / consulta (Queries). En lugar de tener un único modelo que sirva tanto para lectura como para escritura, se utilizan modelos distintos optimizados para cada propósito. Bajo este patrón puedes tener una parte del sistema especializada en manejar comandos (modificaciones de estado) y otra especializada en consultas (proyecciones, vistas optimizadas).

Ventajas
•	Permite optimizar las lecturas y las escrituras de forma independiente (por ejemplo, consultas muy rápidas con vistas materializadas).
•	Bajo carga de lectura intensa, puedes escalar la parte de consulta sin afectar la parte de escritura.
•	Facilita el diseño claro de límites y responsabilidades.
•	Mejora la claridad en el dominio, pues los comandos y consultas tienen responsabilidades distintas.

Desventajas
•	Aumenta la complejidad del sistema: tienes dos modelos, sincronización entre ellos, posibles latencias de actualización entre comando → lectura.
•	Requiere manejar consistencia eventual (no siempre inmediata).
•	No es necesario ni recomendable para sistemas simples o de baja carga.
•	La implementación puede ser más difícil: debes pensar en cómo mantener las proyecciones sincronizadas.

Ejemplo
•	En dominios complejos donde escribir y consultar tienen requisitos muy distintos (por ejemplo, dashboards con consultas avanzadas, pero también transacciones complejas).

=> DDD (Domain-Driven Design)

DDD es más que un patrón: es una metodología o conjunto de principios para diseñar software centrado en el dominio del negocio que se enfoca en conceptualizar el dominio real (problema de negocio) mediante un lenguaje ubicuo (ubiquitous language) compartido entre desarrolladores y expertos en el dominio. Introduce conceptos como Entity, Value Object, Aggregate, Bounded Context, Domain Services, Domain Events, etc.
La arquitectura resultante suele estar aislada del resto mediante capas (por ejemplo capa de aplicación, capa de dominio, infraestructura) o estilos como Hexagonal, Onion, Clean.

Ventajas
•	El software refleja mejor el dominio: es más expresivo y entendible para el negocio.
•	Facilita el mantenimiento y evolución porque las reglas de negocio están agrupadas con claridad.
•	En sistemas complejos permite delimitar contextos y reducir acoplamiento.
•	En combinación con CQRS u otras arquitecturas, puede escalar bien en proyectos grandes.
•	Algunos estudios muestran mejoras reales cuando se aplica bien. arXiv

Desventajas
•	Curva de aprendizaje pronunciada, especialmente para equipos no acostumbrados.
•	Puede resultar excesivo para sistemas simples o con dominio poco complejo (overengineering).
•	Requiere disciplina en la definición del lenguaje ubicuo y seguirlo.
•	Si no está bien delimitado, puede generar fronteras mal definidas entre contextos.

Ejemplo
•	En arquitecturas de microservicios donde cada microservicio puede corresponder a un Bounded Context.
•	Ejemplo: un sistema de comercio electrónico grande: dominio de órdenes, dominio de inventario, dominio de pagos, cada uno como contexto separado.

=>MVVM (Model-View-ViewModel)
MVVM es un patrón muy común en aplicaciones modernas con binding de datos (por ejemplo, aplicaciones de GUI con frameworks que soportan enlace de datos).
Los componentes son:
 • Modelo (Model): datos del dominio o lógica de negocio.
 • Vista (View): la interfaz de usuario, que se enlaza con propiedades del ViewModel.
 • ViewModel: actúa como mediador entre la Vista y el Modelo; expone propiedades y comandos que la Vista puede enlazar (binding), y maneja la lógica de presentación.
La Vista observa (bind) propiedades del ViewModel, reactualizándose automáticamente cuando cambian.

Ventajas
•	Desacopla la vista de la lógica de presentación (el ViewModel no tiene conocimiento de elementos visuales concretos).
•	Facilita la prueba del ViewModel (sin UI).
•	En frameworks que soportan binding, reduce el código del “pegamento” entre UI y lógica.
•	Buena escalabilidad para aplicaciones cliente modernas (desktop, móviles, SPA) donde hay muchas interacciones en la UI.

Desventajas
•	Si no se estructura bien, los ViewModels pueden volverse muy grandes (violando la responsabilidad única).
•	El binding automático puede complicar el rastreo de errores o el rendimiento si no se controla bien.
•	En aplicaciones sin soporte de binding robusto, puede ser engorroso implementarlo manualmente.
•	No siempre tiene sentido en aplicaciones muy simples.

Ejemplo
•	En aplicaciones de escritorio (WPF, Xamarin, .NET MAUI), móviles (MVVM en frameworks como Android MVVM, iOS con binding) o tecnologías web con binding (como algunas variantes de frameworks JS).


=>Anti-patrones
Un anti-patrón es una solución común pero ineficiente o dañina que suele surgir por falta de conciencia o por simplificación excesiva.

¿por qué son perjudiciales y cómo evitarlos?
Dos de las más comunes  son:

God Object / God Class
Consiste en una clase o módulo que acumula demasiada responsabilidad: lógica de negocio, acceso a datos, validaciones, lógica de presentación, etc. En lugar de distribuir responsabilidades, todo “cae” en esa clase central.
Por qué es dañino
•	Dificulta el mantenimiento: cualquier cambio puede afectar muchas partes del sistema.
•	Dificulta las pruebas unitarias: la clase es tan grande y cohesiva que es difícil aislarla.
•	Genera alto acoplamiento: muchas dependencias cruzadas.
•	Violación de principio de responsabilidad única (SRP).
Cómo evitarlo
•	Aplicar principios SOLID (especialmente SRP).
•	Refactorizar en capas bien definidas.
•	Dividir la clase “god” en módulos más pequeños con responsabilidades claras.
•	Utilizar patrones de diseño adecuados (DAO, servicios, controladores, etc.) para segregar responsabilidades.

Spaghetti Code (Código espagueti)
Código desordenado, sin estructura clara, con muchas dependencias cruzadas, saltos (gotos o estructuras de control dispersas), funciones enormes con múltiples responsabilidades.
Difícil de leer, entender o modificar.
Por qué es dañino
•	Cada cambio pequeño puede introducir errores imprevistos.
•	Alta probabilidad de dependencias ocultas o efectos colaterales.
•	Difícil de escalar o evolucionar.
•	Dificulta el trabajo en equipo (difícil para nuevos desarrolladores entender el flujo).
Cómo evitarlo
•	Diseñar con principios de arquitectura desde el inicio: modularidad, separación de responsabilidades.
•	Aplicar patrones de diseño (MVC, capas, servicios).
•	Refactorizar continuamente cuando se detectan zonas “difíciles”.
•	Escribir pruebas unitarias para permitir cambios seguros.
•	Mantener código limpio, con funciones pequeñas y legibles.


=>CI / CD (Integración continua / Entrega continua / Despliegue continuo)
¿Qué es CI/CD? ¿Cuál es la diferencia entre CI, CD (Delivery) y CD (Deployment)?

CI (Continuous Integration / Integración continua)
	Práctica de fusionar frecuentemente (múltiples veces al día) los cambios de código de los desarrolladores a la rama principal.
	Cada fusión dispara automáticamente un proceso de compilación + pruebas (unitarias, integración) para validar que no se rompa la aplicación.
	Así se detectan errores temprano y se reduce el “dolor” de integrar grandes cambios.

CD (Continuous Delivery / Entrega continua)
	Implica que tras la etapa de CI (compilar + probar), el artefacto resultante esté listo para desplegarse en cualquier momento a producción, pero el propio despliegue no es automático: puede requerir aprobación manual, validaciones adicionales, etc.
	La idea: el software siempre está en un estado que puede lanzarse.

CD (Continuous Deployment / Despliegue continuo)
Va un paso más allá: una vez pasadas todas las pruebas y validaciones, el despliegue a producción es automático, sin intervención humana.
Esto requiere tener una alta confianza en las pruebas y en la infraestructura.

Concepto  	          Qué automatiza	                                  ¿Se despliega automáticamente a producción?
CI	         Compilación + pruebas al fusionar código	                  No necesariamente
CD          (Entrega)	Prepara artefacto listo para producción	         Depende: puede requerir intervención
CD         (Despliegue continuo)	Incluye despliegue automático	        Sí, en producción tras aprobación automática

=> Herramientas más usadas 

Algunas herramientas muy populares en CI/CD incluyen:
•	GitHub Actions — sistema de automatización integrado a GitHub.
•	GitLab CI / GitLab CI/CD — sistema de CI/CD integrado en GitLab.
•	Jenkins — servidor de automatización muy flexible y extensible por plugins.
•	CircleCI — servicio en la nube (y también autoalojado) de CI/CD.
•	Travis CI — muy usado para proyectos open source, integrado con GitHub.
•	Azure Pipelines — parte de Azure DevOps, soporta repositorios externos como GitHub.
•	Bamboo — de Atlassian, se integra con Jira / Bitbucket.
•	GoCD — plataforma de CI/CD de código abierto para canalizaciones complejas.
•	Spinnaker, Tekton, Concourse — otras alternativas especializadas.


Ejemplos de pipelines típicos en proyectos reales

algunos escenarios de pipeline que suelen usarse:
•	Proyecto web backend + frontend
 1. CI: al hacer push a rama develop / feature → ejecutar pruebas unitarias del backend + frontend, análisis estático de código.
 2. Build: compilar el backend (por ejemplo empaquetado de una API), construir el frontend (bundle, minificación).
 3. Pruebas de integración / E2E.
 4. Deploy a entorno de staging / pruebas.
 5. Validación manual / pruebas adicionales.
 6. Luego, con merge a main, CD: desplegar a producción automáticamente o tras aprobación.
•	Microservicios con contenedores / Kubernetes
 1. CI: cada microservicio compila su imagen Docker, pruebas unitarias.
 2. Registrar imagen en un registry (Docker Hub, AWS ECR, etc.).
 3. Pruebas de integración entre microservicios (posiblemente con test en entorno contenedor).
 4. Deploy automático con herramientas como Helm / Kubernetes en entorno staging.
 5. Validaciones, monitoreo, luego promover a producción (automático o manual).
 
•	Pipeline simple para API REST
 yaml
 stages:
  - build
  - test
 - deploy
build:
  script:
  - npm install
  - npm run build
test:
  script:
  - npm test
deploy:
  script:
  - deploy-script.sh
  when: manual
 ```
Ese pipeline realiza compilación, pruebas y deja la tarea de despliegue como manual (modo CD de entrega). En proyectos reales se agregan etapas de análisis de código (lint, SonarQube), escaneo de seguridad (SAST), etc.

Beneficios del CI/CD en equipos de desarrollo profesional
•	Detección temprana de errores: los problemas se descubren tan pronto como se integra código, lo que reduce costos de corrección.
•	Entrega continua / rápida de características: el tiempo entre desarrollar y poner en producción se acorta.
•	Mayor calidad del software: con pruebas automatizadas y validaciones constantes.
•	Menos errores humanos: muchas tareas repetitivas se automatizan.
•	Confianza en los despliegues: al tener pipelines confiables, los equipos pueden liberar versiones frecuentemente sin miedo.
•	Mejor feedback al cliente / usuario: los cambios llegan más rápido y se pueden ajustar con base en retroalimentación.
•	Escalabilidad del equipo: al estandarizar procesos, varios desarrolladores pueden integrarse de forma más fluida.

Ejemplo de YAML de pipeline 
Aquí un ejemplo 
stages:
  - build
  - test
  - deploy

variables:
  APP_NAME: mi-api
  ENV: staging

# Etapa de construcción
build:
  stage: build
  image: node:18
  script:
    - echo "Instalando dependencias"
    - npm install
    - echo "Construyendo proyecto"
    - npm run build
  artifacts:
    paths:
      - dist/

# Etapa de pruebas
test:
  stage: test
  image: node:18
  script:
    - echo "Ejecutando pruebas unitarias"
    - npm test

# Etapa de despliegue
deploy_staging:
  stage: deploy
  image: alpine:latest
  script:
    - echo "Desplegando en entorno de staging"
    - ./scripts/deploy.sh $ENV
  only:
    - main
Explicación:
•	stages: define las etapas del pipeline: primero build, luego test, luego deploy.
•	variables: son variables que pueden usarse en todo el pipeline (APP_NAME, ENV).
•	Job build: en etapa build, usa imagen Docker de Node 18, ejecuta comandos para instalar dependencias y construir el proyecto. Los artefactos generados (por ejemplo la carpeta dist/) se guardan para etapas posteriores.
•	Job test: en etapa test, usa también Node 18, corre npm test.
•	Job deploy_staging: en etapa deploy, usa imagen ligera de Alpine, y corre el script de despliegue con variable ENV. Solo se ejecuta cuando la rama es main.

Este pipeline realiza construcción → pruebas → despliegue a staging. En un pipeline real se pueden agregar más etapas: análisis de código, escaneo de seguridad, pruebas de integración, aprobación manual, despliegue a producción, rollback, monitoreo, etc.


SELECCION PERSONAL / EJEMPLO INTEGRADO  DE 3 A 4 SEMANAS DE TABAJO 
basandome en lo mas comun o frecuente al realizar tareas seleccione.

=> Patrón Creacional: Factory Method
Justificación:
El patrón Factory Method permite crear objetos sin especificar la clase exacta del objeto que se va a crear. Esto se logra mediante una interfaz que define un método para crear un objeto, dejando a las subclases decidir qué clase concreta instanciar.
En sistemas donde se manejan diferentes tipos de entidades (usuarios, doctores, pacientes, medicamentos, etc.), este patrón facilita la creación dinámica de objetos según el tipo de dato o rol.
Integración en el sistema:
En el sistema trabajado, el Factory Method podría aplicarse al módulo de autenticación o registro.
Por ejemplo:
•	Al registrar o iniciar sesión, la fábrica puede decidir si debe crear un objeto de tipo Administrador, Doctor o Usuario según las credenciales ingresadas.
•	Esto mejora la extensibilidad: si en el futuro se agregan más roles (por ejemplo, “Farmacéutico”), solo se agrega una nueva subclase sin modificar el código existente.
Beneficios:
•	Evita múltiples condiciones if/else o switch para crear objetos.
•	Hace más limpia la creación de instancias según el tipo de usuario.
•	Facilita mantenimiento y pruebas.

=>Patrón Estructural: Adapter
Justificación:
El patrón Adapter permite que dos clases con interfaces incompatibles trabajen juntas. Es útil cuando se necesita integrar componentes nuevos con código o librerías existentes.
Integración en el sistema:
En el sistema de control de medicamentos (o pase de lista), este patrón puede aplicarse al módulo de conexión con la base de datos o con un servicio externo (como Firebase o API REST).
Por ejemplo:
•	Si el sistema fue diseñado inicialmente para usar una base de datos local (SQLite o MySQL) y después se decide migrar a Firebase, el Adapter puede actuar como traductor entre la interfaz de acceso a datos original (DAO) y la nueva API de Firebase.
Beneficios:
•	Permite cambiar de tecnología (por ejemplo, base de datos o servicio de almacenamiento) sin alterar el resto del sistema.
•	Aumenta la reutilización del código existente.
•	Facilita la integración con nuevas herramientas o módulos.

=>Patrón de Comportamiento: Observer
Justificación:
El patrón Observer define una relación de dependencia “uno a muchos”: cuando un objeto cambia de estado, notifica automáticamente a todos los objetos dependientes.
Este patrón es ideal cuando se necesita mantener sincronizados varios componentes o vistas con los datos de un modelo.
Integración en el sistema:
En el sistema, este patrón podría aplicarse en el módulo de registro de actividades o notificaciones.
Por ejemplo:
•	Cuando un usuario registra un medicamento o pasa lista, el sistema podría notificar automáticamente al administrador o actualizar una vista de historial en tiempo real.
•	Si se integra con Firebase, se pueden usar “listeners” que actualizan automáticamente la interfaz cuando hay nuevos datos (esto es literalmente un Observer implementado por la base de datos en tiempo real).
Beneficios:
•	Mejora la interactividad en tiempo real.
•	Evita que la interfaz dependa directamente del modelo.
•	Facilita la expansión (más vistas u observadores sin modificar la lógica central).

=> Patrón Emergente: MVC (Model-View-Controller)
Justificación:
El patrón MVC es uno de los más utilizados para separar la interfaz de usuario, la lógica de negocio y los datos.
Divide la aplicación en tres componentes principales:
•	Modelo: datos y lógica de negocio.
•	Vista: interfaz que muestra los datos.
•	Controlador: intermediario que gestiona entradas y coordina entre vista y modelo.
Integración en el sistema:
En el sistema trabajado, MVC puede aplicarse de forma natural:
•	Modelo: las clases que representan los usuarios, medicamentos o registros (y que se comunican con la base de datos).
•	Vista: las pantallas HTML/CSS (o interfaz de usuario en la Raspberry Pi o app móvil).
•	Controlador: los scripts JS o Python que reciben la interacción del usuario y coordinan las acciones con el modelo.
Por ejemplo:
•	Cuando el usuario inicia sesión, el Controlador recibe los datos del formulario, los envía al Modelo para validarlos, y luego actualiza la Vista mostrando el mensaje de bienvenida o error.
Beneficios:
•	Separación clara de responsabilidades.
•	Facilita el mantenimiento (modificar la vista sin tocar la lógica del modelo).
•	Permite trabajo en paralelo entre desarrolladores de backend, frontend y diseño.


REFERENCIAS 
atlassian. (2024). atlassian. Obtenido de https://www.atlassian.com/es/devops/devops-tools/cicd-tools
Carlos A. Guerrero, J. M. (2013). scielo. Obtenido de https://www.scielo.cl/scielo.php?script=sci_arttext&pid=S0718-07642013000300012
Microsoft Ignite. (17 de noviembre de 2025). Microsoft Ignite. Obtenido de https://learn.microsoft.com/es-es/dotnet/architecture/microservices/microservice-ddd-cqrs-patterns/ddd-oriented-microservice
Milton García-Borroto, J. F.-T. (2008). INAOE. Obtenido de https://ccc.inaoep.mx/Reportes/CCC-08-002.pdf
nayeliortiz. (2024). github. Obtenido de https://github.com/nayeliortizg/Pros-y-Contras-de-los-Patrones-de-Dise-o-GOF/
Platero, C. (2017). upm. Obtenido de https://blogs.upm.es/ieef/wp-content/uploads/sites/389/2017/03/Dise%C3%B1o-orientado-a-objetos-II.pdf
redhat. ( 11 de mayo de 2022). redhat. Obtenido de https://www.redhat.com/es/topics/devops/what-is-ci-cd
UNIVERSOJAVA. (22 de NOVIEMBRE de 2024). UNIVERSOJAVA. Obtenido de https://www.universojava.com/2024/11/patrones-de-diseno-gof-gang-of-four.html












