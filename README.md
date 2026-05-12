\# Prueba Práctica Avanzada - Oracle SQL



\## Datos del estudiante



\*\*Nombre:\*\* Lara Fernández Andrew Johan  

\*\*Asignatura:\*\* Bases de Datos  

\*\*Docente:\*\* José Caiza  

\*\*Universidad:\*\* Universidad Técnica de Ambato  

\*\*Facultad:\*\* Ingeniería en Sistemas  



\## Escenario asignado



El escenario asignado corresponde a \*\*Agencia Espacial\*\*.



La base de datos está compuesta por las siguientes entidades:



\- NAVE

\- MISION

\- ASTRONAUTA

\- ROL\_TRIPULACION

\- TRIPULACION



La integridad referencial aplicada es \*\*ON DELETE CASCADE\*\*.



\## Descripción del modelo



El modelo representa una agencia espacial que administra naves, misiones, astronautas y roles dentro de cada tripulación.



Una nave puede participar en varias misiones.  

Una misión puede tener varios astronautas asignados.  

Un astronauta puede participar en varias misiones.  

Cada astronauta dentro de una misión cumple un rol específico.  



La tabla `TRIPULACION` funciona como tabla intermedia entre `MISION`, `ASTRONAUTA` y `ROL\_TRIPULACION`.



\## Archivos SQL



En la carpeta `sql/` se encuentran los scripts utilizados para la creación y prueba de la base de datos:



\- `01\_create\_tables.sql`: contiene las sentencias CREATE TABLE.

\- `02\_insert\_datos.sql`: contiene los INSERT válidos.

\- `03\_integridad\_ora\_02291.sql`: contiene la prueba del error ORA-02291.

\- `04\_update\_delete.sql`: contiene UPDATE seguro y DELETE con CASCADE.

\- `05\_consultas.sql`: contiene consultas con IN, LIKE, BETWEEN, AVG, MAX y JOIN.



\## Restricciones implementadas



Se implementaron las siguientes restricciones:



\- PRIMARY KEY

\- FOREIGN KEY

\- NOT NULL

\- UNIQUE

\- CHECK

\- ON DELETE CASCADE



\## Prueba de integridad



Se provocó el error ORA-02291 al intentar insertar una misión con una nave inexistente.



Esto ocurre porque la tabla `MISION` tiene una clave foránea hacia `NAVE`, por lo que no se puede registrar una misión usando un `id\_nave` que no exista previamente.



\## Consultas realizadas



Se realizaron consultas usando:



\- IN

\- LIKE

\- BETWEEN

\- AVG

\- MAX

\- JOIN



\## Evidencias



Las evidencias se encuentran en la carpeta `evidencias/` e incluyen:



\- Fotos del desarrollo manual.

\- Capturas de ejecución en Oracle.

\- Capturas del error ORA-02291.

\- Capturas de las consultas SQL ejecutadas.



\## Conclusión



La práctica permitió aplicar modelado lógico, creación de tablas en Oracle SQL, restricciones de integridad, manipulación de datos, pruebas de errores referenciales y consultas SQL. Además, se comprobó el funcionamiento de `ON DELETE CASCADE` dentro del escenario Agencia Espacial.

