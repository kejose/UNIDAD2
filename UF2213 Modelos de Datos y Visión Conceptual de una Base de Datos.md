
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

#### Campo (Field)
- Elemento dentro de una tabla con tipo de dato, longitud, decimales, etc.
#### Consulta (Query)
- Instrucción para interactuar con los datos, generalmente de lectura.
#### Tabla (Table)
- Objeto contenedor de información estructurada.
#### Vista (View)
- Consulta residente que se ejecuta como si fuera una tabla.
#### Gestión de índices
- Estructura que mejora la velocidad de acceso a registros. Funciona como el índice de un libro, relacionando elementos con su posición.

Los índices pueden ser creados con una o más columnas, y pueden ser únicos o no únicos. Un índice único previene filas idénticas.

---
### Seguridad
### Medidas de seguridad en bases de datos

- **Físicas**: control de acceso al equipo (tarjetas, etc.).
- **Personales**: acceso solo a personal autorizado.
- **Sistema Operativo**: seguridad a nivel de SO.
- **SGBD**: herramientas como perfiles, vistas, restricciones.

Un BDMS (Sistema Manejador de Bases de Datos) es un software diseñado para gestionar bases de datos. Permite crear, modificar, eliminar y consultar datos de forma eficiente y segura.

Ofrece herramientas para:

- Crear y modificar tablas.
- Definir relaciones.
- Controlar acceso.
- Ejecutar consultas.
- Generar informes y estadísticas.

Ejemplos: MySQL, Oracle, SQL Server, PostgreSQL, MongoDB.
