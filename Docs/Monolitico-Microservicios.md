# Monolítico vs Microservicios

## Monolito

### Ventajas
  * Facilidad de despliegue: El despliegue de una aplicación monolítica es muy simple, no requiere de orquestación ni gestión con otros componentes ni aplicaciones.

  * Fácil de someter a pruebas y debug : Todo el código está en una misma aplicación lo cual es fácil de testear, debug y monitorizar.

  * Menor latencia: Debido a que un monolito (a diferencia de los microservicios) no requiere tanta comunicación/dependencia con otros componentes/servicios, la latencia es menor.

  * Agilidad: En algunos casos, por razones de time-to-market, se opta por desarrollar una aplicación en modo monolith first y posteriormente se van migrando aquellos casos de uso que se justifiquen hacia microservicios.

### Desventajas
  * Compleja de mantener: Si un monolito no está bien diseñado en módulos y lo suficientemente desacoplado, según va creciendo el tamaño de la aplicación puede llegar a representar un alto coste por la complejidad del mantenimiento del código (deuda técnica).

  * Escalabilidad: Para escalar un monolito se debe desplegar toda la aplicación, con lo cual requerimos más infraestructura aun cuando la escalabilidad solo sea requerida por unos pocos casos de uso. Por otra parte, la aplicación debe estar diseñada para ser desplegada en clustering (sin sesiones pegajosas, sin procesos concurrentes que se solapen, etc.).

  * Atada a la tecnología: Cuando se desarrolla un monolito, se establece una tecnología/framework y todo el equipo queda atado a dicha tecnología, lo cual imposibilita el hecho de poder utilizar distintas soluciones tecnológicas (frameworks, librerías, etc.,) en función de cada caso de uso y sus requisitos.
  
  * Punto único de fallo: En caso de que algo falle en el monolito, podría llegar a afectar a toda la aplicación, lo cual se conoce como un single point of failure (SPOF).

## Microservicios

### Ventajas
  * Son más fáciles de mantener y testear, puesto que son servicios pequeños que hacen una sóla cosa, pero lo hacen bien.

  * No están integrados en el sistema principal (loosely coupled), por tanto son más fáciles de desarrollar y desplegar. Pueden tener una escalabilidad independiente y se pueden aislar los fallos a un microservicio en concreto, en vez de una sección o funcionamiento de la aplicación.

  * Organizado en torno a las capacidades empresariales. No son necesarios cambios radicales en el stack de tecnología que se utiliza, sino que para cada servicio se puede utilizar la tecnología más adecuada.

  * A nivel de un equipo de desarrolladores, es más fácil entrar y empezar a ser productivo, ya que se tiene que entender el funcionamiento de varios servicios pequeños en vez de uno grande. Por tanto, tenemos un desarrollo más alineado con las metodologías DevOps y Agile.

### Desventajas
  * Hay que lidiar con la complejidad adicional de los sistemas distribuidos. Implementar comunicación interna entre los servicios, implementar dependencias de un servicio hacía el otro, solicitudes que pueden extenderse a varios servicios, etc.

  * La complejidad del despliegue en sí. Es muy difícil gestionar microservicios. Mantener esa armonía requiere una coordinación perfecta, que de hecho es imposible sin soluciones como kubernetes.

  * Mayor consumo de recursos. Puesto que cada microservicio tiene su propio Sistema Operativo y dependencias, al final sale más caro a nivel de recursos usar microservicios que un monolito; que es un Sistema Operativo, y sus dependencias.