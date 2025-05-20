# Notas que tomo en el curso de Fad Azure Data Fundamentals DP-900


- **IAAS**: Infrastucture as a service
- **PAAS**: Platform as a service
- **SAAS**: Software as a service


Datos operativos

Datos analíticos

## Roles en el mundo de los datos

1. **ADMINISTRADOR DE BASE DE DATOS**: es el responsable del diseño, la implementación, el mantenimiento, optimización, rendimiento y os aspectos operativos de los sistemas de bases de datos. También son los reponsables de administrar seguridad en la base de datos, conceder privilegios o denegar acceso a los usuarios.

2. **INGENIERO DE DATOS**: es el responsable de diseñar e implementar cargas de trabajo relacionadas con los datos, incluidas canalizaciones de ingesta de datos, actividades de limpieza y transformación, y almacenes de datos para cargas de trabajo analíticas.

3. **ANALISTA DE DATOS**: permite a las empresas maximizar el valor de sus recursos de datos. Explora los datos, identifica tendencias y relaciones, diseña e implementa modelos analíticos, habilita funcionalidades de análisis mediante informes y visualizaciones.


## Servicios en la nube de de Microsoft Azure
<img width="1077" alt="Captura de pantalla 2025-05-18 a las 13 46 08" src="https://github.com/user-attachments/assets/2afff3d5-ce21-4c3e-a2c7-9f28796f5d37" />


### ¿Qué es la normalización de datos?
La normalización es el proceso de diseño de esquemas que minimiza la duplicación de datos y exige la integridad de los mismos. Aunque hay muchas reglas complejas que definen este proceso de refactorización de datos en varios niveles, una definición sencilla cumple los siguientes fines:
1. Separar cad entidad en su propia tabla
2. Separar cada atributio discreto en su propia columna
3. Identificar de forma única cada instancia de entidad mediante una clave principal (id)
4. Usar columnas de clave externa para vincular entidades relacionadas (foreign key)

#### Tabla sin normalizar

<img width="636" alt="Captura de pantalla 2025-05-18 a las 12 45 14" src="https://github.com/user-attachments/assets/fd10e220-e9c4-49dc-8009-1c8e764a4009" />

#### Tabla normalizada

<img width="583" alt="Captura de pantalla 2025-05-18 a las 12 45 46" src="https://github.com/user-attachments/assets/d32a2ca9-1d15-42be-adbd-8f9529aa9ab5" />

Cada entidad representada en los datos (cliente, producto, pedido de ventas y elemento de linea) se alma ena en su propia tabla y cada atributo discreto de esas entidades se encuentra en su propia columna. Con estos pasos eliminaríamos duplicados, y si por ejemplo un cliente neesita cambiar su dirección, lo cambiaríamos solo en la tabla "Customer" y sus respectivas columnas "Adress" y "City".

### ¿Qué es SQL/Bases de datos RELACIONALES?

SQL (Structured query language) es el lenguaje estándar para os sistemas de administración de bases de datos relaciones. Se usan para actualizar, recuperar, eliminar datos de la base de datos. Algunos sistemas que utilian SQL son:
1. Microsoft SQL Server
2. MySQL
3. PostgreSQL
4. MariaDB
5. Oracle

Las instrucciones SQL son:
1. SELECT
2. INSERT
3. UPDATE
4. DELETE
5. CREATE
6. DROP

#### Tipos de instrucciones SQL:
Las instrucciones SQL se agrupan en tres grupos lógicos principales:

- **Lenguaje de definición de datos (DDL)**: Las instrucciones más habituales son: CREATE, ALTER, DROP Y RENAME:
    ```
    # Crear una tabla con las columnas id, name, price y decirle el tipo de dato
    CREATE TABLE Product
    (
        ID INT PRIMARY KEY,
        Name VARCHAR(20) NOT NULL,
        Price DECIMAL NULL
    );
    ```
- **Lenguaje de control de datos (DCL)**: Los administradores de bases de datos suelen usar instrucciones DCL para administrar el acceso a objetos de una base de datos concediéndoles, denegando o revocando permisos a usuarios o grupos específicos. Las 3 instrucciones que existen son: GRANT, DENY, REVOKE
  ```
  # Permite a un usuario denominado user1 leer, insertar y modificar datos en la tabla Product .
  GRANT SELECT, INSERT, UPDATE
  ON Product
  TO user1;
  ```
- **Lenguaje de manipulación de datos (DML)**: Las instrucciones DML se usan para manipular las filas de las tablas. Estas instrucciones permiten recuperar (consultar) datos, insertar nuevas filas o modificar filas existentes. También puede eliminar filas si ya no las necesita. Las instrucciones más habituales son: SELECT, INSERT, UPDATE, DELETE:
  ```
  # Recuperar/Mostrar las columnas "FirstName", "LastName", "Address", "City" de la dabla Customer
  SELECT FirstName, LastName, Address, City
  FROM Customer
  WHERE City = 'Seattle';
  ```

**¿Qué es una vista?**: Es una tabla virtual basada en los resultados de una consulta SELECT.

**¿Qué es un procedimiento almacenado?**: Es una instrucción/función SQL que creamos y guardamos para poder usarlo más tarde. Es como una automatización, por ejemplo podemos crear una función para cambiar el nombre de un producto directamente desde su id:
```
# creamos la función para cambiar el nombre de un producto por su ID
CREATE PROCEDURE RenameProduct
	@ProductID INT,
	@NewName VARCHAR(20)
AS
UPDATE Product
SET Name = @NewName
WHERE ID = @ProductID;
```
```
# ahora llamamos a la función con el ID que queramos y le pasamos el nuevo nombre
EXEC RenameProduct 201, 'Spanner';
```
De esta manera, hemos cambiado el nombre del producto con ID 201 a "Spanner"

**¿Qué es un ínidce?**: Es el índice de una fila, que nos puede ayudar a buscar datos en nuestra tabla. Un índice (index) no aparece en la tabla como una columna, sino que es una estructura que se construye para acelerar búsquedas.
```
CREATE INDEX idx_CustomerName
ON Customer(Name);
```

Index no es lo mismo que ID:
| Concepto                     | ID                    | INDEX                                         |
| ---------------------------- | --------------------- | --------------------------------------------- |
| ¿Qué es?                     | Columna de datos      | Estructura de búsqueda                        |
| ¿Visible al usuario?         | Sí, en la tabla       | No, es interno                                |
| ¿Identifica filas?           | Sí, típicamente única | No                                            |
| ¿Acelera búsquedas?          | Solo si se indexa     | Sí, ese es su propósito                       |
| ¿Se actualiza con los datos? | Sí                    | Sí, pero tiene un coste extra                 |
| ¿Se crea con `CREATE TABLE`? | Sí (como una columna) | No necesariamente, se crea con `CREATE INDEX` |

Azure permite la administración de diferentes tipos de bases de datos relacionales: SQL Server, PostgreSQL y MySQl. Las opciones SQL server de Azure son:

| Opción                         | Tipo de Servicio | Uso Principal                                     | Ventajas Clave                                               | Nivel de Compatibilidad con SQL Server |
| ------------------------------ | ---------------- | ------------------------------------------------- | ------------------------------------------------------------ | -------------------------------------- |
| **SQL Server en Azure VM**     | IaaS             | Migración *lift-and-shift* desde entornos locales | Control total, configuración personalizada                   | Total                                  |
| **Azure SQL Managed Instance** | PaaS             | Modernización con compatibilidad avanzada         | Administración automática, alta compatibilidad               | Casi total                             |
| **Azure SQL Database**         | PaaS             | Nuevas aplicaciones cloud-native                  | Escalable, alta disponibilidad, mantenimiento automatizado   | Parcial (no todas las características) |
| **Azure SQL Edge**             | Motor embebido   | Escenarios IoT y procesamiento en el borde        | Optimizado para tiempo real y análisis local en dispositivos | Limitado (enfocado a IoT)              |


### Servicios de bases de datos de código abierto en Azure

Azure ofrece servicios gestionados para bases de datos relacionales de código abierto populares como MySQL, MariaDB y PostgreSQL, facilitando la migración de aplicaciones locales a la nube sin cambios significativos.

| Servicio                          | Descripción y ventajas principales                                                                                                                                                  |
| --------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Azure Database for MySQL**      | PaaS basado en MySQL Community. Alta disponibilidad, escalabilidad, seguridad y backups automáticos. Pago por uso.                                                                  |
| **Azure Database for MariaDB**    | PaaS basado en MariaDB Community. Gestión total por Azure, alta disponibilidad, seguridad, escalabilidad y backups automáticos.                                                     |
| **Azure Database for PostgreSQL** | PaaS basado en PostgreSQL. Alta disponibilidad, escalabilidad, seguridad y supervisión. Algunas extensiones avanzadas no disponibles. Soporta servidor flexible para mayor control. |



