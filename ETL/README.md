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

<img src="Images/Ex05/05.2.png" width="500"/>

##### Step 03: Run Talend job

<img src="Images/Ex05/05.3.png" width="500"/>

##### Step 04: Check the results

<img src="Images/Ex05/05.4.png" width="500"/>


