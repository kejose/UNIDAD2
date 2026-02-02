# hola
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

- **Soporte de transacciones,** debe proporcionar un mecanismo que garantice que todas las actualizaciones correspondientes a una determinada transacción se realicen, o que no se realice ninguna.
Una transacción es un conjunto de acciones que cambian el contenido de la base de datos.

- **Servicios de control de concurrencia,** proporciona un mecanismo que asegure que la base de datos se actualice correctamente cuando varios usuarios la están actualizando concurrentemente. Uno de los principales objetivos de los SGBD es el permitir que varios usuarios tengan acceso concurrente a los datos que comparten. El acceso concurrente es relativamente fácil de gestionar si todos los usuarios se dedican a leer datos, ya que no pueden interferir unos con otros.
Sin embargo, cuando dos o más usuarios están accediendo a la base de datos y al menos uno de ellos está actualizando datos, pueden interferir de modo que se produzcan inconsistencias en la base de datos. El SGBD se debe encargar de que estas interferencias no se produzcan en el acceso simultáneo.

- **Servicios de recuperación,** mecanismo capaz de recuperar la base de datos en caso de que ocurra algún suceso que la dañe.
  
- **Servicios de autorización,** Garantizar que sólo los usuarios autorizados pueden acceder a la base de datos. La protección debe ser contra accesos no autorizados, tanto intencionados como accidentales.
  
- **Soporte para la tramitación de datos,** Un SGBD debe ser capaz de integrarse con algún software de comunicación. Muchos usuarios acceden a la base de datos desde terminales. En ocasiones estos terminales se encuentran conectados directamente a la máquina sobre la que funciona el SGBD. En otras ocasiones los terminales están en lugares remotos, por lo que la comunicación con la máquina que alberga al SGBD se debe hacer a través de una red. En cualquiera de los dos casos, el SGBD recibe peticiones en forma de mensajes y responde de modo similar. Todas estas transmisiones de mensajes las maneja el gestor de comunicaciones de datos. Aunque este gestor no forma parte del SGBD, es necesario que el SGBD se pueda integrar con él para que el sistema sea comercialmente viable.

- **Servicios de integridad,** Son los medios necesarios para garantizar que tanto los datos de la base de datos, como los cambios que se realizan sobre estos datos, sigan ciertas reglas. Se puede considerar como otro modo de proteger la base de datos, pero además de tener que ver con la seguridad. La integridad se ocupa de la calidad de los datos. Normalmente se expresa mediante restricciones, que son una serie de reglas que la base de datos no puede violar.

- **Servicios para mejorar la independencia de los datos,** Permitir que se mantenga la independencia entre los programas y la estructura de la base de datos. La independencia de datos se alcanza mediante las vistas o subesquemas. La independencia de datos física es más fácil de alcanzar, de hecho hay varios tipos de cambios que se pueden realizar sobre la estructura física de la base de datos sin afectar a las vistas. Sin embargo, lograr una completa independencia de datos lógica es más difícil. Añadir una nueva entidad, un atributo o una relación puede ser sencillo, pero no es tan sencillo eliminarlos.

- **Servicios de utilidad,** Un SGBD debe proporcionar una serie de herramientas que permitan administrar la base de datos de modo efectivo. Algunas herramientas trabajan a nivel externo, por lo que habrán sido producidas por el administrador de la base de datos. Las herramientas que trabajan a nivel interno deben ser proporcionadas por el distribuidor del SGBD. Algunas de ellas son:

  - Herramientas para importar y exportar datos.
  - Herramientas para monitorizar el uso y el funcionamiento de la base de datos.
  - Programas de análisis estadístico para examinar las prestaciones o las estadísticas de utilización.
  - Herramientas para reorganización de índices.
  - Herramientas para aprovechar el espacio dejado en el almacenamiento físico** por los registros borrados y que consoliden el espacio liberado para reutilizarlo cuando sea necesario.

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

![carpeta](https://github.com/kejose/UNIDAD2/blob/main/Captura%20de%20pantalla%202026-01-30%20125025.png)

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
![CARPETA](https://github.com/kejose/UNIDAD2/blob/main/Captura%20de%20pantalla%202026-01-30%20125627.png)
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
  
![CARPETA](https://github.com/kejose/UNIDAD2/blob/main/Captura%20de%20pantalla%202026-01-30%20130323.png)
### 4.2 Modelo en Red
- Evolución del jerárquico.
- Un nodo puede tener múltiples padres.
- Representación mediante grafos.
  
![CARPETA](https://github.com/kejose/UNIDAD2/blob/main/Captura%20de%20pantalla%202026-01-30%20130558.png)
### 4.3 Modelo Relacional
- Datos en tablas con claves únicas.
- Relaciones mediante claves foráneas.
- Uso de SQL.
- Simplicidad y flexibilidad.

**Ejemplos de entidades:**
- Cliente, Ventas, Producto.

![CARPETA](https://github.com/kejose/UNIDAD2/blob/main/Captura%20de%20pantalla%202026-01-30%20130631.png)
### 4.4 Modelo Relacional Extendido
- Añade entidades, atributos y relaciones avanzadas.
- Soporta herencia, subtipos y supertipos.
- Mayor precisión en el modelado.
  
![CARPETA](https://github.com/kejose/UNIDAD2/blob/main/Captura%20de%20pantalla%202026-01-30%20130724.png)
### 4.5 Modelo Orientado a Objetos
- Datos representados como objetos.
- Propiedades, métodos, clases e herencia.
- Encapsulamiento.
- Aplicaciones: videojuegos, SIG, simulaciones.
  
![CARPETA](https://github.com/kejose/UNIDAD2/blob/main/Captura%20de%20pantalla%202026-01-30%20130806.png)

---
