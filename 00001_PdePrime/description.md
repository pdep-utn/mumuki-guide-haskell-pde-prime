<img src="https://raw.githubusercontent.com/pdep-utn/mumuki-guide-haskell-pde-prime/master/assets/Screen%20Shot%202020-08-07%20at%2023_1596854492790.41.12.png" alt="Screen Shot 2020-08-07 at 23_1596854492790.41.12.png" width="auto" height="auto">

_Nos contactaron para hacer un sistema que ayude a tomar decisiones sobre series de TV a producir en un nuevo servicio llamado PdePrime Video._

En el sistema vamos a trabajar con series, de las cuales queremos saber cual es el nombre de la misma, quienes actúan en ella (y el orden de importancia), su presupuesto anual, cantidad de temporadas estimadas, el rating promedio que tiene y si está cancelada o no.
También, de cada actor o actriz conocemos el nombre, cuál es su sueldo pretendido (anual) y qué restricciones tiene a la hora de trabajar. Por ejemplo, sabemos que el sueldo pretendido de Paul Rudd es de 41 millones al año y que sus restricciones son no actuar en bata y comer ensalada de rúcula todos los días.

Resolver los siguientes requerimientos, maximizando el uso de **composición**,** aplicación parcial** y **orden superior**.

**Parte A**

Vamos a conocer un poco a nuestras series.

1. Saber si la serie **estaEnRojo**, esto es si el presupuesto no alcanza a cubrir lo que quieren cobrar todos los actores.
2. Saber si una serie **esProblemática**, esto ocurre si tienen más de 3 actores o actrices con más de 1 restricción.

**Parte B**

Queremos modelar diferentes tipos de productores, que evalúan qué se hace con las series.

1. **conFavoritismos**: elimina a los dos primeros actores de la serie y los reemplaza por sus actores favoritos.
2. **timBurton**: es un caso particular de un productor con favoritismos, siempre reemplaza a los primeros dos actores por johnny depp y helena bonham carter, cuyos sueldos pretendidos anuales son $20000000 y $15000000 respectivamente, y no tienen ninguna restricción.
3. **gatopardeitor**: no cambia nada de la serie.
4. **estireitor**: duplica la cantidad de temporadas estimada de la serie.
5. **desespereitor**: hace un combo de alguna de las anteriores ideas, mínimo 2.
6. **canceleitor**: si la serie está en rojo o el rating baja de una cierta cifra, la serie se cancela.

**Parte C**

Lo creas o no las series tienen un bienestar.

1. Calcular el **bienestar** de una serie, en base a la sumatoria de estos conceptos:
  * Si la serie tiene estimadas más de 4 temporadas, su bienestar es 5, de lo contrario es (10 - cantidad de temporadas estimadas) * 2.
  * Si la serie tiene menos de 10 actores, su bienestar es 3, de lo contrario es (10 - cantidad de actores que tienen restricciones), con un mínimo de 2.
  * Aparte de lo mencionado arriba, si la serie está cancelada, su bienestar es 0 más allá de cómo diesen el bienestar por longitud y por reparto.

2. Algunos productores buscan llevar bienestar a las series. Para ellos queremos saber si un grupo de grupo de productores **sonBeneficiosos** para una serie. Esto sucede cuando cada uno le da su toque y la serie termina con un bienestar mayor a 4.

**Aclaraciones**

* Todas las funciones deberán estar tipadas.
* NO repetir lógica.
* Usar composición siempre que sea posible.
* Enviar la solución a Mumuki cada ~30 minutos o a medida que vayas resolviendo cada punto.

**También podés ver el examen desde [acá](https://docs.google.com/document/d/1bl8bFyRZy6hI4LT6BI-86sUikhhbcjr5u5s4UChii_4/edit?usp=sharing).**

