1. Una empresa desea crear una red social basada en almacenamiento de imágenes. Se plantean distintas opciones a la dirección de la empresa, que debe decidir por cuál de ellas opta. La dirección desea lograr la mayor eficiencia, funcionalidad y calidad del producto, teniendo en cuenta una salida a producción al cabo de un año. 

    ### 1.1.- Explique razonadamente qué procesos y metodologías de gestión desearía implantar. 
    
    Una de las principales metodologías a integrar en el desarrollo de la aplicación es la gestión de la configuración, que nos permite realizar un control de cambios durante el desarrollo de la red social, almacenando las diferentes funcionalidades desarrolladas a través de un control de versiones. Esto nos permite realizar un mantenimiento del producto, tanto en fases de desarrollo como mejoras a añadir sobre un producto finalizado.
    
    Una vez se tiene almacenado el código y se comienza el desarrollo, la incorporación de procesos de mejora e integración continua sobre el código es fundamental, ya que nos permite realizar procesos automatizados, ahorrando tiempo a los desarrolladores y obteniendo menores riesgos que en un desarrollo tradicional donde puede haber errores de desarrollo.
    
    Durante todo el desarrollo del producto recalco además la importancia de realizar buenas prácticas como por ejemplo estandarizar reglas de desarrollo, definir estilos de código, documentar de manera clara, etc. Así se obtiene un producto unificado, aunque diversos desarrolladores hayan participado en la implementación.
    
    Como procesos a realizar, se presentaría una planificación del trabajo que conllevaría el desarrollo de la aplicación, obteniendo un informe de tareas a realizar y recursos necesarios para ello. A esta parte sería conveniente añadir estimaciones de coste y tiempo para definir una viabilidad sobre el proyecto.
    
    Destaco por último la elección de una correcta metodología para el desarrollo de la aplicación, sobre todo una basada en metodología ágil, ya que nos permite hacer iteraciones sobre productos o entregas funcionales, así se va desarrollado el producto de manera incremental. Además, en proyectos de desarrollo software suele ser común el cambio o aumento de requisitos Esto proporcionaría un seguimiento y control del trabajo realizado, obteniendo un resultado del estado del proyecto.

    ### 1.2.- Detalle las herramientas que utilizaría para cada uno de los procesos y cómo las haría interoperar entre sí para cumplir lo que espera la dirección.

    En cuanto a los procesos de gestión de configuración y control de cambios generalmente suelen ir unidas en herramientas del tipo repositorios como, por ejemplo, GitHub, GitLab, por lo que la interacción entre ellas se realizaría de manera directa.

    En cuanto a la mejora e integración continua, existen ciertas herramientas que también lo integran junto con las metodologías anteriores, por lo que en el caso de una solución tan grande como la proporcionada, escogería alguna que integre todos los procesos. De otro modo, únicamente haría falta comunicar el repositorio de código deseado con la herramienta utilizada.

    Para el seguimiento de la metodología ágil escogida existen múltiples herramientas disponibles, por lo que habría que estudiar costes, licencias y funcionalidades de cada una de ellas. En esta herramienta se podría incluir la planificación general del trabajo a realizar, junto con sus estimaciones.

    ### 1.3.- Explique razonadamente por qué solución se decantaría para la infraestructura: cloud pública, cloud privada, cloud híbrida, CPD.

    Como se trata de un gran desarrollo que se prevé con grandes volúmenes de peticiones, en mi caso optaría por una cloud pública. Las ventajas sobre el CPD son muy directas, ya que se ahorran costes iniciales de infraestructuras, compra de recursos y contratación. Además de que no es necesario preocuparse por la seguridad de donde alojes tu aplicación, ya que el proveedor se tiene que encargar de ello.  A costa de muchas ventajas, el control y la gestión no es propia, por lo que en ciertos casos no puedes realizar todas las operaciones que requerirías, tanto hardware como software es externo.

    En un periodo temprano de la aplicación optaría por una cloud pública antes que una privada por rapidez de integración, ya que no debemos realizar mantenimiento. También, el coste sería relativamente inferior, ya que durante el inicio de la aplicación el gasto ocasionado probablemente sería mínimo si no se presentan usuarios, y conforme se vaya dando a conocer aumentaría la necesidad de escalar. Si el producto va creciendo rápidamente haría el cambio a una cloud privada, ya que tendríamos mayor flexibilidad, control y la escalabilidad sería ligeramente superior. Además de presentar una cantidad mínima de ingresos que nos ayudarían en la gestión de esta.

    ### 1.4.- Poniéndose en el rol de la dirección. Enumere los factores de decisión para evaluar la propuesta realizada en los puntos anteriores.
        
        1.	Uso de una metodología ágil
        2.	Buenas prácticas
        3.	Herramientas de gestión de la metodología
        4.	Herramientas de gestión de la configuración y control de versiones
        5.	Realización de documentación
        6.	Integración y mejora continua
        7.	Despliegue continuo
        8.	Uso de microservicios basados en Docker

    ### 1.5.- Una vez implantada la solución, detalle los indicadores de rendimiento necesarios (tanto operativos como de negocio) para evaluar el correcto funcionamiento de la red social.

    En cuanto a datos operativos podemos presentar información de uso de la red, el tráfico que presenta, el nivel de disco y CPU que contienen las máquinas en las que nos alojamos, las peticiones que se realizan sobre los servicios, como por ejemplo BBDD. Número de usuarios que se registran en nuestra aplicación, que se dan de baja, etc, en general la tasa de utilización.

    En cuanto a datos de negocio se podría incluir el número de peticiones hechas por los clientes, número de servicios que tenemos funcionando, localización de peticiones.
    
    ### 1.6 Detalle la arquitectura de recolección de métricas y logs para los indicadores anteriores.

    Haría falta la presentación de los sistemas, uno para la recolección de métricas y otra para la recolección de logs. En cada máquina que alojara un servicio/microservicio sería necesario presentar instancias de cada uno de estos sistemas, que posteriormente se analizarían de manera conjunta en una herramienta del tipo Elasticsearch. Para una visualización de manera Dashboard se podría hacer uno de herramientas como Kibana.

2. Una empresa está valorando crear microservicios a partir de una aplicación monolítica desarrollada en Java que se encarga de la gestión de coches de alquiler. 


    ### 2.1.- ¿Cuáles son las ventajas y desventajas de desarrollar estos microservicios? 

    Se proporciona escalabilidad en el sistema, por lo que se permite añadir más recursos, y por ende más componentes del mismo servicio.

    Añade agilidad en los cambios, ya que no es necesario modificar componentes de manera completa, sino funcionalidades separadas. Del mismo modo proporciona una trazabilidad de fallos importante, separando el flujo del programa en secciones de servicios.

    Un punto muy importante en la mejora de caídas, ya que no finaliza el servicio en completo, sino componentes, de los cuales podemos presentar más instancias e incluso ni notar el fallo.

    En cuanto al desarrollo proporciona adaptabilidad al trabajo en equipo, ya que el grupo de desarrollo puede trabajar en paralelo y no en un mismo documento, lo único que haría falta sería definir una correcta integración entre servicios.

    Como desventajas podemos encontrar que el consumo de memoria es mayor al tener más número de procesos activos. Además, se necesita un tiempo extra para desarrollar una arquitectura dividida en microservicios.

    Si aumenta considerablemente el número de servicios en los que se divide la aplicación puede llegar a un nivel de complejidad mayor, sobre todo de entendimiento por parte del gestor del proyecto o ante nuevas incorporaciones que deban comprender el funcionamiento y cada servicio de la aplicación.

    ### 2.2.- Ahora mismo, los clientes de la aplicación reciben dos actualizaciones anuales. Los clientes se quejan de que con esta cadencia tienen que convivir con bugs y errores durante mucho tiempo. ¿Qué procesos de mejora de calidad implantaría para solucionar este problema? 					

    De manera directa una integración y entrega continua, ya que su objetivo principal es realizar una entrega de manera rápida y ágil, realizando testeos automáticos sobre los posibles fallos o bugs ocasionados. Si además incluimos despliegue continuo nos estaríamos ahorrando la intervención humana y la realización de ello de manera automática.

    Además, disminuiría el periodo de entregables a clientes.
    
    ### 2.3.- Debido a la complejidad de la aplicación, los ingenieros de software de esta empresa tienen que acudir a las oficinas de los clientes a hacer los despliegues y los consiguientes mantenimientos. Este hecho está quitando mucho tiempo de desarrollo a los ingenieros de software de la empresa. El director del departamento de informática se ha dado cuenta de que el estado actual no es escalable. Como arquitecto de software ¿Qué solución propone? 					                        (3 puntos)

    Realizar despliegue continuo. Si se integra un pipeline sobre el desarrollo, en cada funcionalidad o cambio que un equipo de desarrollo integre al proyecto, se despliega el sistema de manera automática, generando informes de fallos si se da el caso.

3. Se desea desplegar una aplicación web en AWS mediante contenedores Docker ¿Qué infraestructura y servicios gestionados de AWS se requieren para desplegarla siguiendo una arquitectura en HA (alta disponibilidad) o Multi-AZ?

    En primer lugar, una VPC para alojar todas las redes. Dentro de ella se pueden integrar subnets públicas y privadas para dar diferentes niveles de accesos a los usuarios finales.

    Como componentes principales para proporcionar alta disponibilidad se encontraría la utilización de varias zonas de disponibilidad, por lo que el sistema debería encontrarse replicado en ambas. Destaco la necesidad de ser dos zonas muy diferenciadas entre ellas y lo suficientemente lejanas para no se realicen caídas simultaneas y se pierda de manera general el servicio.

    Evidentemente el uso de instancias con EC2 que contendrían tareas alojadas en ECS, a su vez en servicios y en clusters, con contenedores usando imágenes pertenecientes de ECR.

    El uso de balanceadores de carga proporcionaría al sistema una distribución de las peticiones ante una demanda alta.

    Y la ventaja ante caídas de servicios se podría conseguir con grupos de AutoScaling que controlen cantidad de servicios actuales que se presentan en tiempo real.

    Para el control de la auditoría y autenticación existe el Api Gateway, aunque también puede hacerse un desarrollo propio.

    Si es necesario alojar algún tipo de documento que deba ser accesible por las máquinas, existe el repositorio S3.
