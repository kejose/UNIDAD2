
- **Gestor transaccional:** Controla y gestiona las transacciones. Se asegura de que todas las operaciones se completen correctamente o se deshagan si ocurre un error. Utiliza un registro de transacciones para mantener el estado de las operaciones. Garantiza concurrencia y consistencia.

- **Gestor de memoria intermedia:** Administra la memoria temporal (caché) para reducir operaciones de entrada/salida y mejorar el rendimiento. Usa algoritmos para decidir qué datos almacenar en caché y cuáles eliminar. Garantiza la integridad de los datos en caché y su correcta escritura en disco.

- **Metadatos o diccionario de datos (DD):** Información que describe la estructura y contenido de la base de datos: tablas, columnas, índices, procedimientos, restricciones, relaciones. Se usan para validación, gestión de transacciones, optimización y garantizar integridad.
---
### El procesador de consultas

El procesador de consultas en un SGBD se encarga de ejecutar las consultas realizadas por los usuarios en la base de datos.

- **Intérprete del DDL:** procesa y ejecuta comandos DDL. Verifica sintaxis y los convierte en comandos de bajo nivel. Gestiona objetos como tablas, índices, restricciones y vistas.

- **Compilador del LMD:** procesa y ejecuta comandos de manipulación de datos (DML). Traduce comandos escritos por el usuario en lenguaje entendible por el SGBD. Analiza sintaxis y semántica para generar un plan de ejecución óptimo.

- **Motor de evaluación de consultas:** traduce la consulta en un plan de ejecución. Optimiza el plan evaluando estrategias para recuperar datos. Ejecuta el plan y devuelve resultados.
---
### Características del SGBD

- **Independencia física,** el nivel físico puede ser modificado independientemente del nivel conceptual. El usuario no puede ver todos los componentes.

- **Independencia lógica,** el nivel conceptual puede ser modificado independientemente del nivel físico

- **Facilidad de uso**: usuarios sin conocimientos técnicos pueden consultar datos fácilmente.

- **Acceso rápido**: recuperación eficiente mediante algoritmos optimizados.

- **Administración centralizada**: manipulación y verificación de integridad desde un punto central.

- **Redundancia controlada**: evita duplicación de datos para minimizar errores y ahorrar memoria.

- **Verificación de integridad**: coherencia entre elementos relacionados.

- **Uso compartido**: acceso simultáneo por múltiples usuarios.

- **Seguridad de los datos**: control de acceso por usuario.

---

### Funciones 

- **Almacenamiento, extracción y actualización de datos**: permite guardar, consultar y modificar datos ocultando la estructura física.

- **Catálogo accesible por el usuario**: diccionario de datos con descripciones accesibles por los usuarios.

- **Soporte de transacciones**: garantiza que todas las acciones de una transacción se realicen o ninguna.

- **Control de concurrencia**: asegura actualizaciones correctas cuando varios usuarios acceden simultáneamente.

- **Servicios de recuperación**: permite restaurar la base de datos ante fallos.

- **Servicios de autorización**: protege contra accesos no autorizados.

- **Tramitación de datos**: integración con software de comunicación para terminales locales o remotos.

- **Servicios de integridad,** Son los medios necesarios para garantizar que tanto los datos de la base de datos, como los cambios que se realizan sobre estos datos, sigan ciertas reglas. Se puede considerar otro modo de proteger la base de datos.

Garantizan que los datos y sus modificaciones respeten reglas definidas. Se expresan mediante restricciones que no deben violarse.

- **Servicios para independencia de datos,** Permiten mantener independencia entre programas y estructura de la base de datos. Se logra mediante vistas o subesquemas. La independencia física es más fácil de alcanzar que la lógica.

- **Servicios de utilidad,** Un SGBD debe proporcionar una serie de herramientas que permitan administrar la base de datos de modo efectivo.
	- Importar y exportar datos.
	- Monitorizar uso y funcionamiento.
	- Análisis estadístico.
	- Reorganización de índices. 

- **Aprovechamiento del espacio liberado en almacenamiento físico** por los registros borrados y que consoliden el espacio liberado para reutilizarlo cuando sea necesario

---

### Terminología de SGDB

- **Campo - Field**

  Identifica solo un elemento dentro de la tabla con características específicas
como tipo de datos, longitud, número de decimales, etc.


- **Consulta - Query**


  Identifica una instrucción propia del motor de base de datos que interactúa con los datos 
almacenados en esta. Generalmente son instrucciones de lectura, aun que muchas veces se utiliza el término Query para cualquier instrucción (escritura, procesamiento o administración).


- **Tabla - Table**
  Identifica un objeto contenedor de información estructurada, esta estructura
se repite en todos los registros en ella.


- **Vista - View**
  Identifica una consulta residente en el servidor que puede ejecutarse con
una instrucción simple como si fuera otra tabla de la base de datos.


- **Gestión de índices**

  El índice de una base de datos es una estructura de datos que mejora la velocidad de las 
operaciones, permitiendo un rápido acceso a los registros de una tabla en una base de datos. Al aumentar drásticamente la velocidad de acceso, se suelen usar sobre aquellos campos sobre los cuales se hacen frecuentes búsquedas.

El índice tiene un funcionamiento similar al índice de un libro, guardando parejas de 
elementos: el elemento que se desea indexar y su posición en la base de datos. Para buscar un elemento que esté indexado, sólo hay que buscar en el índice dicho elemento para, una vez encontrado, devolver el registro que se encuentre en la posición marcada por el índice.

Los índices pueden ser creados usando una o más columnas, proporcionando la base 
tanto para búsquedas rápidas al azar como de un ordenado acceso a
registros eficiente.

  Los índices pueden ser definidos como únicos o no únicos. Un índice único actúa como 
una restricción en la tabla previniendo filas idénticas en el índice

---
#### Seguridad

![[Pasted image 20260130125053.png]]
#### Medidas de seguridad en bases de datos

-  Físicas: controlar el acceso al equipo. Tarjetas de acceso, etc.
-  Personal: acceso sólo del personal autorizado. Evitar sobornos, etc.
-  SO: seguridad a nivel de SO
-  SGBD: uso herramientas de seguridad que proporcione el SGBD. Perfiles de usuario, vistas, restricciones de uso de vistas, etc.


   Un BDMS es un programa de software diseñado para gestionar y
administrar bases de datos se conoce como un Sistema Manejador de Bases de Datos. Su propósito principal es permitir a los usuarios crear, modificar y eliminar bases de datos, así como también acceder a los datos almacenados en ellas de forma eficiente y segura.

   Estos sistemas ofrecen una amplia gama de herramientas y funcionalidades para la 
gestión de bases de datos, como la creación y modificación de tablas, la definición de relaciones entre ellas, el control de acceso a los datos, la ejecución de consultas y la generación de informes y estadísticas. Existen diferentes tipos de BDMS, desde los más sencillos y orientados a usuarios sin experiencia en programación hasta los más complejos y diseñados para entornos empresariales de alto rendimiento. Algunos ejemplos comunes de BDMS son MySQL, Oracie, Microsoft SQL Server, PostgreSQL y MongoDB.

## Funciones de un SGBD

- **Identificación y autorización de usuarios**:
  - Códigos de acceso, contraseñas, biometría (huellas, voz, retina).
- **Gestión de permisos**:
  - Según terminal, operación o franja horaria.
- **Cifrado de datos**:
  - Protección en bases distribuidas o con acceso por red/Internet.
- **Tipos de cuentas**:
  - Administración de cuentas, privilegios y niveles de seguridad.
- **Control de sesiones**:
  - Registro de operaciones por usuario en bitácora para auditoría.

---

## Respaldos de Bases de Datos

- **Definición**: Copia de seguridad ante pérdida, daño o robo.
- **Usos principales**:
  - Recuperación ante fallos del sistema.
  - Protección contra virus y malware.
  - Prevención de errores humanos.
  - Cumplimiento de normativas.
  - Migración de datos.
- **Importancia**: Garantiza la continuidad del negocio ante eventos adversos.

---

## Replicación de Bases de Datos

- **Concepto**: Copia y sincronización entre BD principal y secundarias.
- **Objetivos**:
  - Mejorar rendimiento.
  - Aumentar disponibilidad.
  - Facilitar recuperación ante desastres.
- **Tipos**:
  - Maestro–esclavo.
  - En anillo.
  - En árbol.
- **Ventajas**:
  - Alta disponibilidad.
  - Escalabilidad.
  - Reducción del tiempo de inactividad.
- **Desafíos**:
  - Complejidad en configuración y administración.
  - Riesgo de corrupción si no se gestiona correctamente.

---

## Definición de Transacción

- **Concepto**: Conjunto de órdenes ejecutadas como unidad indivisible (atómica).
- **SGBD transaccional**:
  - Mantiene integridad de datos.
  - Evita estados intermedios.
  - Si falla, revierte al punto de integridad como si no se hubiera ejecutado.
---

## 2. Evolución de los Sistemas de Bases de Datos
- **1950**: Cintas magnéticas.
- **1960**: Discos; modelos jerárquico y en red.
- **1970**: Modelo relacional (Codd), SQL, Oracle.
- **1980**: Popularización de bases relacionales.
- **1990**: Consolidación de SQL y expansión con la WWW.

---

## 3. Objetivos y Servicios de los SGBD
- Abstracción e independencia de datos.
- Consistencia e integridad.
- Seguridad y control de acceso.
- Manejo de transacciones.
- Optimización del rendimiento.

---

## 4. Modelos Lógicos de Bases de Datos

### 4.1 Modelo Jerárquico
- Estructura en árbol.
- Relación padre–hijo única.
- Ejemplo: organigramas empresariales.

### 4.2 Modelo en Red
- Evolución del jerárquico.
- Un nodo puede tener múltiples padres.
- Representación mediante grafos.

### 4.3 Modelo Relacional
- Datos en tablas con claves únicas.
- Relaciones mediante claves foráneas.
- Uso de SQL.
- Simplicidad y flexibilidad.

**Ejemplos de entidades:**
- Cliente, Ventas, Producto.

### 4.4 Modelo Relacional Extendido
- Añade entidades, atributos y relaciones avanzadas.
- Soporta herencia, subtipos y supertipos.
- Mayor precisión en el modelado.

### 4.5 Modelo Orientado a Objetos
- Datos representados como objetos.
- Propiedades, métodos, clases e herencia.
- Encapsulamiento.
- Aplicaciones: videojuegos, SIG, simulaciones.
