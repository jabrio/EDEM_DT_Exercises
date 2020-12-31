![Logo](https://n3m5z7t4.rocketcdn.me/wp-content/plugins/edem-shortcodes/public/img/logo-Edem.png)

# SQL Exercises

- Professor :   [Pedro Nieto](https://github.com/a10pepo)
- Student:      [Javier Briones](https://github.com/jabrio)

## Exercise 01

```
Proporciona una SQL que muestre los siguiente datos:
- Nombre del Actor
- Apellido del Actor

```

### Solution

```
SELECT first_name,last_name FROM actor
```
<img src="SQL/Images/01.png" width="300"/>

## Exercise 02

```
Proporciona una SQL que muestre los siguiente datos:
- Nombre del Actor
- Título de la Película

```

### Solution

```
SELECT actor.first_name, film.title 
FROM actor JOIN (film JOIN film_actor ON film.film_id=film_actor.film_id) ON actor.actor_id=film_actor.actor_id
```
<img src="SQL/Images/02.png" width="500"/>

## Exercise 03

```
Proporciona una SQL que muestre los siguiente datos:
- Nombre del Actor
- Número de películas
- Ordenar de mayor a menor

```

### Solution

```
SELECT actor.first_name, count (film_actor.actor_id) 
FROM actor JOIN (film JOIN film_actor ON film.film_id=film_actor.film_id) ON actor.actor_id=film_actor.actor_id 
GROUP BY actor.actor_id 
ORDER BY COUNT DESC
```
<img src="SQL/Images/03.png" width="500"/>

## Exercise 04

```
Proporciona una SQL que muestre los siguiente datos:
- Nombre de la película
- Número de veces alquilada

```

### Solution

```
SELECT film.title, count (distinct rental.rental_id)
FROM film JOIN (inventory JOIN rental ON rental.inventory_id=inventory.inventory_id) ON film.film_id=inventory.film_id
GROUP BY film.film_id
```
<img src="SQL/Images/04.png" width="500"/>

## Exercise 05

```
Proporciona una SQL que muestre los siguiente datos:
- Nombre de la película
- Dinero recaudado por película

```

### Solution

```
SELECT film.title, SUM (payment.amount)
FROM film JOIN (inventory JOIN (rental JOIN payment ON payment.rental_id=rental.rental_id)
ON rental.inventory_id=inventory.inventory_id) ON film.film_id=inventory.film_id
GROUP BY film.film_id
```
<img src="SQL/Images/05.png" width="500"/>

## Exercise 06

```
Proporciona una SQL que muestre los siguiente datos:
- Nombre del cliente que ha efectuado mayor gasto

```

### Solution

```
SELECT customer.customer_id, customer.first_name, customer.last_name, SUM(payment.amount)
FROM customer JOIN payment ON customer.customer_id=payment.customer_id
GROUP BY customer.customer_id 
ORDER BY SUM DESC
LIMIT 1
```
<img src="SQL/Images/06_A.png" width="500"/>
<img src="SQL/Images/06_B.png" width="500"/>

## Exercise 07

```
Proporciona una SQL que muestre los siguiente datos:
- Nombre del cliente que ha efectuado un mayor número de reservas

```

### Solution

```
SELECT customer.customer_id, customer.first_name, customer.last_name, count (distinct rental.rental_id)
FROM customer JOIN rental ON customer.customer_id=rental.customer_id
GROUP BY customer.customer_id
ORDER BY COUNT DESC
LIMIT 1
```
<img src="SQL/Images/07_A.png" width="500"/>
<img src="SQL/Images/07_B.png" width="500"/>
