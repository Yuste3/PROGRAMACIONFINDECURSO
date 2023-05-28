# COSAS A TENER EN CUENTA

El proyecyto que empieza con el numero 01 es el proyecto con ficheros
EL proyecto que empieza con el numero 02 es el proyecto conectado a la base de datos


En el proyecto 02 (base de datos) el puerto de la conexion con la base de datos tiene que ser el 3307 por cuestiones de configuracion con el localHost en Windows

En el proyecto 01 (ficheros) creo que sinceramente esta todo controlado excepto si a la hora de crear un nuevo usuario usas poner "  " (dos espacios).
Digo que creo que esta todo controlado porque mi codigo paso por muchisima gente a la que pedi que intentase sacar el maximo numero de errores posibles y a base de corregir esos errores puedo decir lo que dije anteriormente.


En el proyecto 02 (base de datos) no me dio tiempo a controlar tantos errores en comparacion con el 01 (ficheros) asique tener en cuenta las siguientes cosas

1. Para que funcione la partida tiene que haber en el rankingHistorico el registro de una CPU1, una CPU2, una CPU3 y una CPU4 dado que coge la informacion de ahi y sino existen en la tabla da error.

2. Si hay registros de CPU en la tabla historico y esa parte (punto numero 1) la podemos "obviar" estaria guay si se pudiesen mover un par de lineas de la clase "Partida" dado que sino solo coge la CPU1 como jugadora en ciertos casos y claro, luego a la hora de insertar los datos en la tabla historicos se repite la primary key con el nombre "CPU1". Es una cosa que tendre arreglada para el examen, pero por si acaso quieres mover las 2 lineas necesarias de lugar para ver que todo lo demas funciona correctamente puedes coger las lineas 234 y 235 y sacarlas fuera del while(rs.next()) y ponerlas a continuacion de este.

3. En el proyecto 02 (base de datos) el ranking Historico lo pinta de forma que la primera linea es la partida mas reciente y la ultima la mas antigua y los jugadores de cada partida estan ordenador de tal forma que el primer jugador de la partida es el que era el ultimo de la ronda y el ultimo que aparece en la partida es el primero en el ranking historico de cada partida

