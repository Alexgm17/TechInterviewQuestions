# Preguntas de Entrevistas Técnicas en Java

Este documento contiene una colección de preguntas frecuentes que se suelen hacer en entrevistas técnicas para desarrolladores de software que utilizan Java. Las preguntas están organizadas por temas para facilitar la preparación.

## Índice

1. [Preguntas sobre Fundamentos de Java](#fundamentos-de-java)
2. [Preguntas sobre Fundamentos de Java 17](#java-17)
3. [Preguntas sobre Programación Orientada a Objetos (OOP)](#programacion-orientada-a-objetos)
4. [Preguntas sobre Estructuras de Datos](#estructuras-de-datos)
5. [Preguntas sobre Concurrencia y Multihilo](#concurrencia-y-multihilo)
6. [Preguntas sobre Manejo de Excepciones](#manejo-de-excepciones)
7. [Preguntas sobre Streams y Lambdas](#streams-y-lambdas)
8. [Preguntas sobre JDBC y Bases de Datos](#jdbc-y-bases-de-datos)
9. [Preguntas sobre Spring Framework](#spring-framework)
10. [Preguntas sobre Spring Boot](#spring-boot)
11. [Preguntas sobre Spring WebFlux](#spring-webflux)
12. [Preguntas sobre Spring Data](#spring-data)
13. [Preguntas sobre Apache Kafka](#apache-kafka)
14. [Preguntas sobre Buenas Prácticas y Principios SOLID](#buenas-practicas-y-principios-solid)

---

## Fundamentos de Java

1. **¿Qué es la JVM y cómo funciona?**
    - La Máquina Virtual de Java (JVM) es una máquina abstracta que permite ejecutar el código Java. Explica cómo la JVM convierte el bytecode en instrucciones ejecutables por la máquina.

2. **¿Cuál es la diferencia entre `==` y `equals()` en Java?**
    - `==` compara referencias de objetos, mientras que `equals()` compara valores.

---

## Java 17

1. **¿Qué son los `sealed classes` en Java 17 y cómo se utilizan?**
    - `sealed classes` permiten que una clase o una interfaz controle qué otras clases o interfaces pueden heredar de ella. Se utilizan para restringir el conjunto de clases derivadas, proporcionando una forma más segura y explícita de manejar jerarquías de clases.

2. **¿Qué son los `record types` en Java 17 y cuáles son sus principales ventajas?**
    - Los `record types` son una nueva característica para definir clases inmutables de manera concisa. Proporcionan una manera sencilla de crear clases que solo almacenan datos, reduciendo el boilerplate code para los métodos `equals`, `hashCode`, y `toString`.

3. **¿Cómo funciona la nueva API de `Pattern Matching` en Java 17?**
    - `Pattern Matching` simplifica el trabajo con tipos de datos al combinar la coincidencia de patrones con el `instanceof` y el des-empacado de valores. Permite escribir código más legible y menos propenso a errores.

---

## Programación Orientada a Objetos

1. **¿Qué son los cuatro pilares de la programación orientada a objetos?**
    - Encapsulación, herencia, polimorfismo y abstracción.

2. **¿Cómo se implementa la herencia en Java?**
    - Utilizando la palabra clave `extends` para clases y `implements` para interfaces.

---

## Estructuras de Datos

1. **¿Qué es una `ArrayList` y en qué se diferencia de un `LinkedList`?**
    - `ArrayList` es una lista basada en un array dinámico, mientras que `LinkedList` es una lista basada en nodos enlazados.

2. **¿Cómo funciona un `HashMap` en Java?**
    - `HashMap` almacena pares clave-valor y utiliza una tabla hash para optimizar el acceso.

---

## Concurrencia y Multihilo

1. **¿Qué es un `Thread` en Java y cómo se crea uno?**
    - Un `Thread` es una unidad de ejecución independiente. Se puede crear extendiendo la clase `Thread` o implementando la interfaz `Runnable`.

2. **¿Qué es una `synchronized` y cuándo se usa?**
    - La palabra clave `synchronized` se utiliza para evitar que varios hilos accedan a un recurso compartido simultáneamente.

---

## Manejo de Excepciones

1. **¿Cuál es la diferencia entre `Exception` y `Error` en Java?**
    - `Exception` es una condición que puede ser manejada, mientras que `Error` representa un problema grave que no debería ser manejado.

2. **¿Qué es un `try-catch-finally` y cómo funciona?**
    - Bloques de código utilizados para manejar excepciones, donde `finally` se ejecuta siempre, independientemente de si se lanza una excepción o no.

---

## Streams y Lambdas

1. **¿Qué es una expresión lambda en Java?**
    - Es una función anónima que se puede usar para implementar métodos definidos en interfaces funcionales.

2. **¿Qué es un `Stream` en Java y cómo se usa?**
    - Un `Stream` es una secuencia de elementos que soporta operaciones agregadas como filtrado y mapeo.

---

## JDBC y Bases de Datos

1. **¿Cómo se conecta una aplicación Java a una base de datos usando JDBC?**
    - Utilizando la clase `DriverManager` para obtener una conexión y ejecutar consultas SQL.

2. **¿Qué es una `PreparedStatement` y por qué es preferible usarla?**
    - Es una clase que permite ejecutar consultas SQL parametrizadas de manera más segura y eficiente.

---

## Spring Framework

1. **¿Qué es Spring Framework y cuáles son sus principales módulos?**
    - Un marco de trabajo para el desarrollo de aplicaciones Java. Sus principales módulos incluyen Core, MVC, AOP, y Data Access.

2. **¿Qué es la inyección de dependencias (DI) en Spring?**
    - Es un patrón de diseño que permite gestionar las dependencias de objetos de forma automática.

---

## Spring Boot

1. **¿Qué son los `Spring Boot Starters` y cómo facilitan el desarrollo?**
    - `Spring Boot Starters` son conjuntos de dependencias preconfiguradas que simplifican la integración de tecnologías comunes en una aplicación. Cada starter proporciona una configuración básica para una tecnología específica, como `spring-boot-starter-web` para aplicaciones web.

2. **¿Cómo se gestiona la configuración externa en Spring Boot?**
    - La configuración externa se puede manejar mediante archivos `application.properties` o `application.yml`, variables de entorno, y argumentos de línea de comandos. Spring Boot soporta perfiles (`@Profile`) para manejar configuraciones específicas de entornos.

---

## Spring WebFlux

1. **¿Cómo se diferencia Spring WebFlux de Spring MVC?**
    - Spring WebFlux está diseñado para aplicaciones reactivas y no bloqueantes, utilizando el modelo de programación reactivo con `Flux` y `Mono`. Spring MVC, en cambio, es sincrónico y bloqueante, basado en el modelo de request-response tradicional.

2. **¿Qué son los `Mono` y `Flux` en el contexto de Spring WebFlux?**
    - `Mono` y `Flux` son tipos proporcionados por el proyecto Reactor para manejar flujos de datos asíncronos. `Mono` representa un flujo de datos que puede emitir 0 o 1 elemento, mientras que `Flux` puede emitir 0 a N elementos.

3. **¿Cómo se manejan los errores en una aplicación Spring WebFlux?**
    - Los errores en Spring WebFlux se pueden manejar utilizando `onErrorResume`, `onErrorReturn`, o `doOnError` para interceptar y gestionar excepciones de manera reactiva.

---

## Spring Data

1. **¿Qué es Spring Data JPA y cómo simplifica el acceso a datos?**
    - Spring Data JPA es una parte de Spring Data que proporciona una implementación simplificada de la capa de acceso a datos utilizando JPA (Java Persistence API). Ofrece una API para la creación de repositorios que eliminan la necesidad de implementar métodos de acceso a datos repetitivos.

2. **¿Cómo se usa la anotación `@Query` en Spring Data JPA?**
    - La anotación `@Query` permite definir consultas JPQL o SQL nativas en métodos de repositorios, proporcionando un control más fino sobre la ejecución de consultas y la personalización de las operaciones de base de datos.

3. **¿Qué son los `Specifications` y cómo se utilizan en Spring Data JPA?**
    - `Specifications` proporcionan una forma flexible de construir consultas dinámicas en JPA utilizando el patrón de especificación. Se utilizan para crear consultas basadas en criterios de búsqueda que pueden combinarse y reutilizarse.

---

## Apache Kafka

1. **¿Cómo se integra Spring Boot con Apache Kafka para el manejo de mensajes?**
    - Spring Boot ofrece soporte para Kafka mediante la dependencia `spring-kafka`. Proporciona una configuración automática para consumidores y productores de Kafka, así como anotaciones como `@KafkaListener` para consumir mensajes.

2. **¿Qué son los `Kafka Streams` y cómo se usan en el procesamiento de datos?**
    - `Kafka Streams` es una librería de procesamiento de flujos que permite crear aplicaciones de procesamiento de datos en tiempo real usando Kafka. Proporciona APIs para construir aplicaciones de stream processing de manera sencilla.

3. **¿Cómo se configura el manejo de particiones y réplicas en un clúster de Kafka?**
    - Las particiones y réplicas se configuran a nivel de topic en Kafka. Las particiones permiten el procesamiento paralelo y la escalabilidad, mientras que las réplicas proporcionan tolerancia a fallos. La configuración se realiza mediante propiedades en el archivo de configuración de Kafka o mediante la interfaz de administración de Kafka.

---

## Buenas Prácticas y Principios SOLID

1. **¿Qué es el principio de responsabilidad única (SRP)?**
    - Un componente debe tener una única razón para cambiar, lo que significa que debe tener una sola responsabilidad.

2. **¿Puedes explicar el principio de inversión de dependencia (DIP)?**
    - Los módulos de alto nivel no deberían depender de los módulos de bajo nivel, sino que ambos deberían depender de abstracciones.
