crear tabla

```
CREATE TABLE flights (
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    origin TEXT NOT NULL,
    destination TEXT NOT NULL,
    duration INTEGER NOT NULL,
);
```

insertar datos
```
INSERT INTO flights
    (origin, destination, duration) 
    VALUES ("New York", "London", 415);
```

ver datos
```
SELECT * FROM flights;
```

formatear para ver las tablas bien
```
.mode columns
.headers yes
```

filtrar contenido
```
SELECT * FROM flights WHERE origin = "New York";
SELECT * FROM flights WHERE duration > 500;
```

añadir expresiones logicas
```
SELECT * FROM flights WHERE duration > 500 AND destination = "Paris";

SELECT * FROM flights WHERE duration > 500 OR destination = "Paris";

SELECT * FROM flights WHERE origin LIKE "%a%";
```

update data 

```
UPDATE flights
   SET duration = 430 
   WHERE origin = "New York"
   AND destination = "London";
```

borrar datos
```
DELETE FROM flights WHERE destination = "Tokyo";
```

unir datos

```
SELECT first, origin, destination 
FROM flights JOIN passengers 
ON passengers.flight_id = flights.id
```

