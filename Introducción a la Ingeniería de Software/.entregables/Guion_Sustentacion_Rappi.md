# Guion de sustentación: Rappi (13 diapositivas)

Duración estimada: unos 12 minutos hablando a ritmo normal. El mínimo que exige la actividad es 10, así que te queda margen para pausas.

Cómo usarlo: no lo recites. Léelo dos o tres veces, pásalo a tu propia forma de hablar y cambia lo que no te suene natural. Donde hay corchetes tienes que llenar tú. Las cifras sí déjalas tal cual, porque están verificadas. Las fuentes ya no van en una diapositiva: ponlas en el PDF.

---

## 1. Portada (30 segundos)

Buenas. Me llamo Esteban David Marrugo Jassir, estudio Ingeniería de Software en la Universidad de Cartagena y para esta actividad de Introducción a la Ingeniería de Software, con el docente Jhon Carlos Arrieta Arrieta, escogí Rappi como caso de estudio.

La elegí porque casi todos la hemos usado y casi nadie se pregunta qué hay detrás de pedir un almuerzo. Eso es lo que voy a desarmar en los próximos minutos, desde la ingeniería de software hasta el celular que tienes en la mano.

## 2. El caso (60 segundos)

Rappi nació en Bogotá en 2015. La fundaron tres colombianos, Simón Borrero, Sebastián Mejía y Felipe Villamarín, que venían de Grability, una empresa que hacía software de e-commerce para supermercados. Probaron el marketplace en Bogotá y en seis meses ya tenían 200 mil usuarios registrados.

Hoy opera en nueve países, en más de 250 ciudades, y según el dato de 2024 supera los 30 millones de usuarios. Procesa más de 28 millones de órdenes al mes. Y ya no es solo comida: desde la misma pantalla puedes pedir mercado, medicinas, un hotel o una tarjeta de crédito. Por eso se le llama super-app.

Voy a seguir el orden de la guía: ingeniería de software, industria, arquitectura de computación, periféricos y evolución tecnológica. Abajo de cada diapositiva ven una ruta que avanza hasta la casa, para que sepan cuánto falta.

## 3. Problema que resuelve y tipo de software (75 segundos)

Piensen en tres personas que no se conocen. Un usuario que quiere algo y lo quiere ya. Un comercio que quiere vender, pero no quiere montar su propia flota de domiciliarios. Y un repartidor independiente, que en Rappi se llama rappitendero, que busca ingresos flexibles.

Sin una plataforma, cada restaurante tendría que armar su app, su flota y su cobro. Rappi pone el software en el medio: recibe el pedido, lo asigna a un repartidor, cobra y le muestra al usuario el recorrido en el mapa. Ese es el problema de fondo, coordinar a tres actores en minutos.

Y aquí viene la respuesta al tipo de software. Rappi no es un programa, son cuatro trabajando juntos. La app del usuario, móvil para Android e iOS y también web. La app del rappitendero, que recibe el pedido y lo guía hasta la entrega. La herramienta del comercio, una tablet o un panel web donde acepta órdenes y actualiza el menú. Y el backend, en la nube, que asigna repartidores, calcula tarifas y procesa pagos. Yo lo clasifico como software de plataforma, un marketplace, apoyado en un sistema empresarial distribuido.

## 4. Principios de ingeniería de software (60 segundos)

Para que algo así funcione hay cinco principios que no se pueden descuidar.

Modularidad: Rappi usa microservicios, así que cada función corre por separado y se puede lanzar sin tocar el resto. Escalabilidad: tiene que aguantar los picos de demanda y más de 28 millones de órdenes al mes. Seguridad: usa más de 20 servicios de seguridad de AWS y, solo en Colombia, bloquea cerca de un millón de intentos de ataque cada semana.

Calidad y pruebas: en sus ofertas de empleo piden pruebas unitarias, de integración, TDD y revisión de código. Y mantenibilidad: con integración y despliegue continuos se cambia el sistema mientras sigue atendiendo pedidos. Nadie puede apagar Rappi un rato para actualizarlo.

## 5. El equipo (40 segundos)

Construir esto requiere equipos distintos. Producto y diseño, que deciden qué se hace y cómo se ve. Desarrollo móvil para las apps. Backend, donde sus ofertas piden Go, Java y Kotlin. Datos e inteligencia artificial, con ciencia de datos y machine learning. Nube y seguridad, con AWS y Kubernetes. Y calidad y operación, para que nada se caiga.

Algo que me pareció interesante es que se organizan por vertical de negocio, por ejemplo Ads o Affordability, y cada equipo responde por sus propios servicios.

## 6. Sector y modelo de negocio (90 segundos)

Rappi vende domicilios, pero lo que construye es software de plataforma. Por eso yo la ubico en el comercio bajo demanda, y en realidad toca cuatro sectores a la vez: plataformas y marketplaces, fintech, logística de última milla y publicidad digital. Eso es lo que hace a una super-app: un solo punto de entrada para servicios que en otros países viven en aplicaciones separadas.

Su modelo de negocio no es uno solo, son varios. La fuente principal es la comisión que cobra a los comercios por cada venta. Después están las tarifas de envío y de servicio que paga el usuario, y que cambian según la distancia y la demanda. También Rappi Prime, una membresía con envíos gratis y otros beneficios.

A eso se suma la publicidad: marcas y comercios pagan por aparecer mejor ubicados dentro de la app. Y la parte fintech, con RappiPay, una billetera que crearon en 2019 con Davivienda, y la tarjeta RappiCard. Abrir la cuenta es gratis, y el dinero llega por comisión, suscripción, publicidad y servicios financieros.

## 7. Tendencias (50 segundos)

La tendencia más marcada es la entrega ultrarrápida. Turbo funciona con dark stores, que son tiendas que solo despachan domicilios, y promete entregar en menos de 10 minutos. Turbo Restaurantes arrancó en Bogotá en enero de 2024: el restaurante cocina en menos de 5 minutos y el repartidor recorre no más de 2 kilómetros. Ahí cada minuto de margen se calcula con tecnología.

Las otras tres son la super-app, que pasó de domicilios a tarjetas y hoteles; los datos y la inteligencia artificial, con modelos de predicción y atención al cliente con Amazon Connect; y la nube con microservicios. Según el reporte que hicieron con AWS, mejoras de georreferenciación bajaron más de 55% el costo de Turbo.

## 8. Arquitectura (65 segundos)

Aquí está la parte de arquitectura de computación. En un extremo hay tres tipos de dispositivos: el celular del usuario, el celular del rappitendero con su GPS y la tablet del comercio. Todos hablan por internet con el servidor mediante una API REST.

Del otro lado está la nube. Cerca del 95% de la infraestructura de Rappi corre en AWS. Adentro hay microservicios en contenedores Docker, orquestados con Kubernetes, que se hablan entre sí por gRPC. Hay una capa de mensajería, con Kafka o RabbitMQ, para pasar eventos como un pedido nuevo. Hay bases de datos SQL, como PostgreSQL y MySQL, y NoSQL para datos de acceso rápido. Y una caché en memoria con Redis.

Una aclaración honesta: estos componentes concretos los saqué de sus ofertas de empleo, no de documentación oficial de su arquitectura. La arquitectura en sí, un cliente-servidor distribuido sobre la nube, sí está confirmada por lo que Rappi y AWS publicaron.

## 9. Procesador y memoria (60 segundos)

El procesador y la memoria cumplen papeles distintos en el celular y en la nube. En el celular, la CPU ejecuta la interfaz, dibuja el mapa y procesa cada toque. La RAM guarda lo que estás usando en ese momento: el carrito, la pantalla abierta. Y el almacenamiento conserva la sesión y las imágenes ya descargadas.

En la nube la CPU atiende muchas solicitudes a la vez, y Rappi usa procesadores AWS Graviton, diseñados por Amazon, con los que ganó cerca de 15% de eficiencia. La RAM se usa para cachés como Redis, que guardan las respuestas frecuentes para no consultar la base de datos cada vez. Y las bases de datos guardan de forma permanente pedidos, usuarios y pagos.

Cuando tocas Pedir pasa esto: el celular arma la petición, viaja por internet, un microservicio la valida y usa la caché, y el pedido se guarda en la base de datos.

## 10. Periféricos y entrada (50 segundos)

En un celular los periféricos vienen dentro del mismo equipo. La pantalla táctil es la entrada principal. El teclado en pantalla y el micrófono sirven para escribir la dirección o dictar una búsqueda. El GPS ubica al usuario y sigue al repartidor en tiempo real. La cámara puede escanear códigos o subir fotos, y la biometría, huella o rostro, puede confirmar el ingreso y los pagos. Del lado del comercio, la tablet avisa con sonido cuando llega un pedido.

Y el flujo de un pedido es este: buscas, eliges producto y cantidad, el GPS propone la dirección y la corriges si hace falta, pagas con tarjeta, billetera o efectivo, y sigues el pedido en el mapa hasta la puerta.

## 11. Hace 20 o 30 años (40 segundos)

Hagamos el ejercicio de imaginar esto entre 1996 y 2006. Pedías por teléfono fijo, con el menú en papel. Dictabas la dirección y esperabas que la entendieran. Pagabas en efectivo. Y si el pedido demoraba, volvías a llamar a preguntar si ya había salido. El sistema era un computador local, o ninguno, cada negocio por su cuenta.

Ni siquiera existía el smartphone: el primer iPhone salió en 2007. Hoy lo mismo se resuelve en una nube compartida que atiende millones de pedidos.

## 12. Qué cambió (50 segundos)

Hay una línea de tiempo que explica ese salto. En 2006 AWS lanzó sus primeros servicios en la nube, y en 2007 salió el primer iPhone. En 2008 abrieron las tiendas de aplicaciones para iOS y Android. Sin esas tres cosas, Rappi no era posible.

Después vienen sus hitos. Nace en 2015, entra a Y Combinator en 2016, en 2018 cierra una ronda de 200 millones de dólares y se vuelve el primer unicornio colombiano. En 2019 lanza RappiPay con Davivienda, y en 2024 llega Turbo Restaurantes y entra a la lista TIME100 de las compañías más influyentes.

## 13. Hacia dónde puede ir y cierre (60 segundos)

Separo lo que ya está pasando de lo que creo que podría pasar. Ya está en marcha la inteligencia artificial en atención al cliente, con Amazon Connect, los modelos de predicción de sus equipos de datos y las entregas de radio corto.

Lo que sigue es hipótesis mía: automatizar la última milla con vehículos eléctricos, robots o drones, que hoy siguen en pruebas en varios países; y más servicios financieros dentro de la misma app, con un ajuste más fino por barrio, porque la plataforma ya se adapta por país, ciudad y barrio y la IA podría afinar precios y tiempos.

Lo que me llevo de este caso es que pedir un almuerzo en Rappi son dos toques. Detrás hay un celular con su procesador y su memoria, un GPS, microservicios y una nube que aguanta millones de órdenes. Para mí la ingeniería de software está justo ahí, en que nada de eso se note. Muchas gracias por la atención.
