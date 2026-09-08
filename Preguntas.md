# Bases de Datos No Relacionales

## 1. ¿Qué es una Base de Datos No Relacional?

Una **Base de Datos No Relacional**, también llamada **NoSQL (Not Only SQL)**, es un sistema de almacenamiento que no organiza necesariamente la información mediante tablas, filas y columnas relacionadas entre sí como ocurre en las bases de datos relacionales.

Las bases NoSQL están diseñadas para trabajar con datos que pueden ser **flexibles, semi-estructurados o no estructurados**, y generalmente permiten modificar la estructura de los datos sin tener que cambiar un esquema rígido.

Existen distintos tipos de bases NoSQL, por ejemplo:

* **Documentales:** MongoDB, CouchDB.
* **Clave-valor:** Redis.
* **Columnas:** Cassandra.
* **Grafos:** Neo4j.

Por ejemplo, MongoDB almacena la información como **documentos BSON**, que tienen una estructura similar a JSON.

---

## 2. ¿Las BBDD NoSQL permiten operaciones CRUD?

Sí. Las bases de datos NoSQL permiten realizar operaciones **CRUD**, al igual que las bases de datos relacionales.

**CRUD significa:**

* **CREATE** → Crear
* **READ** → Leer
* **UPDATE** → Actualizar
* **DELETE** → Eliminar

En MongoDB, por ejemplo:

```text
CREATE → insertOne()
READ   → find()
UPDATE → updateOne()
DELETE → deleteOne()
```

---

## 3. ¿Qué es un Replica Set?

Un **Replica Set** es un conjunto de servidores de MongoDB que mantienen copias del mismo conjunto de datos.

Su principal objetivo es proporcionar:

* **Redundancia:** existen varias copias de los datos.
* **Alta disponibilidad:** si un servidor falla, otro puede asumir su función.
* **Tolerancia a fallos.**

---

## 4. ¿En BBDD NoSQL se escala verticalmente u horizontalmente?

Las bases NoSQL pueden utilizar **ambos tipos de escalabilidad**, pero una de sus principales ventajas es la **escalabilidad horizontal**.

### Escalabilidad vertical

Consiste en ampliar la capacidad del **hardware existente**.

Por ejemplo:

* Agregar más RAM.
* Agregar un procesador más potente.
* Aumentar el almacenamiento.

### Escalabilidad horizontal

Consiste en **agregar más servidores** para repartir la carga y los datos.

---

## 5. ¿Cómo está compuesta una Base de Datos NoSQL de documentos? ¿Usa tablas, filas, registros?

Una base de datos documental como MongoDB **no utiliza tablas y filas** como una base de datos SQL tradicional.

Utiliza **colecciones**, las cuales almacenan varios **documentos**.

Podemos relacionarlo de la siguiente manera:

| Base de Datos Relacional | MongoDB   |
| ------------------------ | --------- |
| Tabla                    | Colección |
| Registro / Fila          | Documento |
| Columna                  | Campo     |

Es decir, podemos considerar que las **colecciones actúan como tablas** y que los **documentos que contienen actúan como registros**.

---

## 6. ¿En qué casos conviene usar BBDD Relacionales y BBDD NoSQL?

No existe una base de datos que sea siempre mejor que la otra. La elección depende del **tipo de aplicación y de los datos**.

### Bases de datos relacionales

Conviene utilizar una base relacional como **MySQL, PostgreSQL, SQL Server u Oracle** cuando:

* Los datos tienen una estructura bien definida.
* Existen muchas relaciones entre entidades.
* Se necesitan consultas complejas con `JOIN`.
* Se requiere una fuerte consistencia de los datos.
* Las transacciones son importantes.
* Por ejemplo: sistemas bancarios, sistemas contables, sistemas de facturación o gestión empresarial.

### Bases de datos NoSQL

Conviene utilizar una base NoSQL cuando:

* Los datos tienen una estructura flexible o cambiante.
* Se manejan grandes cantidades de información.
* Se necesita escalar horizontalmente.
* Se requieren altas tasas de lectura/escritura.
* Se trabaja con datos en tiempo real.
* Los datos se representan naturalmente como documentos.
* Se desarrollan aplicaciones donde el esquema puede cambiar frecuentemente.




