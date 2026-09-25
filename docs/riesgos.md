# Riesgos del proyecto

A continuacion se identifican los principales riesgos del Sistema de Gestion de Biblioteca Universitaria.

* Perdida de datos por falta de respaldo periodico de prestamos y usuarios.
* Prestamos vencidos que no se notifican a tiempo, generando retrasos en la disponibilidad de los libros.
* Duplicidad de registros de usuarios por falta de validacion de matricula.

## Riesgos de seguridad

* Acceso no autorizado a informacion personal de los usuarios.
* Dos usuarios intentando reservar el mismo libro al mismo tiempo (concurrencia).

## Riesgo de desactualizacion

* Trabajar sobre una copia local desactualizada puede provocar diferencias respecto a la version integrada del proyecto.

### Analisis de mitigacion: Concurrencia en Reservas
Para evitar el riesgo de que dos usuarios soliciten el mismo libro al mismo tiempo, el sistema debera implementar bloqueos transaccionales en la base de datos. De no controlarse adecuadamente, se generaran falsas disponibilidades, provocando inconsistencias criticas entre el sistema y el inventario fisico.
