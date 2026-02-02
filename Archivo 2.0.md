
# Resumen UF2213: Modelos de Datos y Visión Conceptual de una Base de Datos

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
![[Pasted image 20260130125910.png]]
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
- ![[Pasted image 20260130130341.png]]
### 4.2 Modelo en Red
- Evolución del jerárquico.
- Un nodo puede tener múltiples padres.
- Representación mediante grafos.
![[Pasted image 20260130130610.png]]
### 4.3 Modelo Relacional
- Datos en tablas con claves únicas.
- Relaciones mediante claves foráneas.
- Uso de SQL.
- Simplicidad y flexibilidad.

**Ejemplos de entidades:**
- Cliente, Ventas, Producto.
![[Pasted image 20260130130655.png]]
### 4.4 Modelo Relacional Extendido
- Añade entidades, atributos y relaciones avanzadas.
- Soporta herencia, subtipos y supertipos.
- Mayor precisión en el modelado.
![[Pasted image 20260130130741.png]]
### 4.5 Modelo Orientado a Objetos
- Datos representados como objetos.
- Propiedades, métodos, clases e herencia.
- Encapsulamiento.
- Aplicaciones: videojuegos, SIG, simulaciones.
![[Pasted image 20260130130820.png]]

---

