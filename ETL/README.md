![Logo](https://n3m5z7t4.rocketcdn.me/wp-content/plugins/edem-shortcodes/public/img/logo-Edem.png)

# ELT Exercises

- Professor :   [Pedro Nieto](https://github.com/a10pepo)
- Student:      [Javier Briones](https://github.com/jabrio)

## Exercise 01

```
Leer un archivo CSV y escribirlo a fichero JSON en la misma carpeta.
```

### Solution

##### Step 01: Load the CSV file as "File Delimited"

<img src="Images/Ex01/01.1.png" width="500"/>

##### Step 02: Set CSV file properties

<img src="Images/Ex01/01.2.png" width="500"/>

##### Step 03: Put the input and output file on the workspace

<img src="Images/Ex01/01.3.png" width="500"/>
<img src="Images/Ex01/01.4.png" width="500"/>

##### Step 04: Run talend job

<img src="Images/Ex01/01.5.png" width="500"/>

##### Step 05: Check the result

<img src="Images/Ex01/01.6.png" width="500"/>
<img src="Images/Ex01/01.7.png" width="500"/>

## Exercise 02

```
Debéis leer un fichero CSV y reemplazar Portugal por “Pt” y France por “Fr”.
```

##### Step 01: Put "ALUMNOS.csv" as input file and a JSON as output file on the workspace

<img src="Images/Ex02/02.1.png" width="500"/>

##### Step 02: Drag a tReplace component on the work space and set their properties

<img src="Images/Ex02/02.2.png" width="500"/>

##### Step 03: Run Talend job

<img src="Images/Ex02/02.3.png" width="500"/>

##### Step 04: Check the result

<img src="Images/Ex02/02.4.png" width="500"/>

## Exercise 03

```
Leer la tabla “Actores” y volcarlo a un fichero JSON.
```

##### Step 01: Drag "Actor" from dvdrental database as input file and a JSON as output file on the workspace

<img src="Images/Ex03/03.1.png" width="500"/>

##### Step 02: Sync the input and output schema

<img src="Images/Ex03/03.2.png" width="500"/>

##### Step 03: Run Talend job

<img src="Images/Ex03/03.3.png" width="500"/>

##### Step 04: Check the result

<img src="Images/Ex03/03.4.png" width="500"/>

## Exercise 04

```
Agregar las películas por rating y mostrar un count, volcar a JSON el resultado.
```

##### Step 01: Drag "Film" from dvdrental database as input file and a JSON as output file on the workspace

<img src="Images/Ex04/04.1.png" width="500"/>

##### Step 02: Drag "tAggregateRow" component on the workspace and set required properties

<img src="Images/Ex04/04.2.png" width="500"/>

##### Step 03: Set required operations

<img src="Images/Ex04/04.3.png" width="500"/>

##### Step 04: Run Talend job

<img src="Images/Ex04/04.4.png" width="500"/>

##### Step 05: Check the results

<img src="Images/Ex04/04.5.png" width="500"/>

## Exercise 05

```
Realizar un JOIN entre Actor | Film | Film_Actor y volcar a JSON un fichero con los campos: Nombre, Apellido y Película.
```

##### Step 01: Drag required tables from dvdrental database as input file and a JSON as output file on the workspace

<img src="Images/Ex05/05.1.png" width="500"/>

##### Step 02: Drag "tMap" component on the workspace and set required operations

<img src="Images/Ex05/05.3.png" width="500"/>

##### Step 03: Run Talend job

<img src="Images/Ex05/05.4.png" width="500"/>

##### Step 04: Check the results

<img src="Images/Ex05/05.5.png" width="500"/>


## Exercise 06

```
Cargar una tabla con el dinero gastado por usuario, nombre y apellido.
```

##### Step 01: From PgAdmin, create a table with required result

<img src="Images/Ex06/06.1.png" width="500"/>

##### Step 02: Drag required tables from dvdrental database as input file and the new created table as output file on the workspace

<img src="Images/Ex06/06.2.png" width="500"/>

##### Step 03: Drag "tMap" component on the workspace and set required operations

<img src="Images/Ex06/06.3.png" width="500"/>

##### Step 04: Drag "tAggregateRow" component on the workspace and set required properties

<img src="Images/Ex06/06.4.png" width="500"/>

##### Step 05: Run Talend job

<img src="Images/Ex06/06.5.png" width="500"/>

##### Step 06: Check the results on PgAdmin

<img src="Images/Ex06/06.6.png" width="500"/>


## Exercise 07

```
Cargar una tabla con el número de veces que se ha alquilado cada película, solo con aquellas que han sido alquiladas al menos una vez.
```

##### Step 01: From PgAdmin, create a table with required result

<img src="Images/Ex07/07.2.png" width="500"/>

##### Step 02: Drag required tables from dvdrental database as input file and the new created table as output file on the workspace

<img src="Images/Ex07/07.1.png" width="500"/>

##### Step 03: Drag "tMap" component on the workspace and set required operations

<img src="Images/Ex07/07.4.png" width="500"/>

##### Step 04: Drag "tAggregateRow" component on the workspace and set required properties

<img src="Images/Ex07/07.5.png" width="500"/>

##### Step 05: Drag "tSortRow" component on the workspace and set required properties

<img src="Images/Ex07/07.3.png" width="500"/>

##### Step 06: Run Talend job

<img src="Images/Ex07/07.6.png" width="500"/>

##### Step 07: Check the results on PgAdmin

<img src="Images/Ex07/07.7.png" width="500"/>


## Exercise 08

```
BigQuery to Talend, filtrando algún elemento.
```
### Option A: CData Driver

[CData instructions](https://www.cdata.com/kb/tech/bigquery-jdbc-talend.rst)

##### Step 01: Update BigQuery database connection through downloaded driver

<img src="Images/Ex08/08.1.png" width="500"/>

##### Step 02: Extract database schema

<img src="Images/Ex08/08.2.png" width="500"/>

##### Step 03: Drag required table from BigQuery database as input file and JSON as output file on the workspace

<img src="Images/Ex08/08.3.png" width="500"/>

##### Step 04: Make the query to obtain the result

<img src="Images/Ex08/08.4.png" width="500"/>

##### Step 05: Run Talend job and check the result

<img src="Images/Ex08/08.5.png" width="500"/>

### Option B

[BigQuery Service Account instructions](https://www.progress.com/tutorials/jdbc/connect-and-query-google-bigquery-using-jdbc-connector)

##### Step 01: Create a service account in GCP, as BigQuery Admin, and then create a key

<img src="Images/Ex08/08.6.png" width="500"/>

##### Step 02: Drag "tBigQueryInput" component as input file and JSON as output file on the workspace

<img src="Images/Ex08/08.7.png" width="500"/>

##### Step 03: Run Talend Job

<img src="Images/Ex08/08.8.png" width="500"/>

##### Step 04: Check the result

<img src="Images/Ex08/08.5.png" width="500"/>
