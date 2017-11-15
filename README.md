## Fixture Mundial 2018

Este proyecto será para hacer una página web para todos los participantes del mundial de Rusia 2018.
El mismo será desarrollado en ASP.NET y servirá como experiencia de desarrollo.

_**Premisas:**_

**Participantes:** se esperan alrededor de 100 participantes, basados en la experiencia que el mundial anterior fueron 85.<br/>
Cada uno deberá ingresar los resultados de todos los partidos de cada grupo, y luego de las llaves de octavos, cuartos, semifinales, tercer y cuarto puesto y final. <br/>
**Aporte:** se propuso que cada participante aporte $ 500. <br/>
**Premios:** todavía no se determinó, pero una posibilidad es que sólo se otorgue 1 premio al ganador por el total del pozo.  <br/>
**Resultados:** los participantes tendrán una fecha límite hasta la cual podrán cargar los resultados proyectados en sus respectivas cuentas.<br/>
Luego los resultados reales se irán ingresando y así se armará el ranking de los participantes. <br/>
**Puntos**: los participantes sumarán puntos con la lógica que será determinada por Waly (a coordinar), pero tentativamente será para la primera ronda
1 punto por acertar el resultado (victoria de un equipo u otro o empate) o 2 puntos por acertar el resultado junto con la cantidad exacta de goles.


_**Ideas:**_

Crear usuarios de dos tipos:

usuario administrador: será 1 que solo cargará los resultados oficiales de los partidos a medida que vayan ocurriendo y marcar que usuario pagó su aporte.

usuario participante: serán todo el resto que participan, que podrán ingresar los resultados proyectados hasta la fecha límite,
y luego podrán consultar el ranking y el estado de su fixture para ver como van.

En el sistema se debe guardar también quién pagó y cuanto, ya que se van a poder hacer pagos parciales.

Cada usuario tendrá un nombre de usuario (que puede ser un email para simplificar) y una contraseña.

El sistema puede enviar notificaciones a los participantes a medida que el administrador cargue los resultados.

Reporte Ranking: es el reporte principal, en donde podrá verse el ranking de los participantes según puntos.

Clases:

grupo - propiedades: id, nombre

equipo - propiedades: id, nombre, grupo del tipo grupo, bandera del tipo imagen

partido - propiedades: id, equipoA del tipo equipo, equipoB del tipo equipo, golesA, golesB, fase del tipo enum ronda

Enumeración de rondas: primera, octavos, cuartos, semifinales, tercercuartopuesto, final

Tablas:

Pantallas:

Pantalla principal del Participante:

Luego del login, el participante entra a una pantalla donde se ve su nombre, posición en el ranking, cantidad de dinero recaudado, cantidad de dinero de cada premio, si pagó o o no (sino, cuanto debe), botón de acceso al ranking completo, botón de acceso a su fixture completo, el cual solo se prodra editar si no venció la fecha tope para completar, y botón de acceso a los resultados reales como se vienen dando.

Foro de participación, donde se podrán dejar mensajes para que vean todos los usuarios (esto va a ser muy popular porque van a aparecer un gran número de cargadas). 

Pantalla del administrador:

Funciones:<br/>
Carga de resultados <br/>
Carga de pagos <br/>
Consulta de deudores <br/>


