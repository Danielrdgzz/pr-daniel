Día 1 (03/03/26):
Comenzamos por reformatear el ordenador e instalar una versión de Ubuntu Desktop (24.04.4) para posteriormente instalar Cisco Packet Tracer

<img width="821" height="516" alt="Captura desde 2026-03-03 12-14-25" src="https://github.com/user-attachments/assets/234c7d1a-b764-41ea-b10b-b5cbbcc66ccd" />

<img width="1440" height="900" alt="Captura desde 2026-03-03 12-23-51" src="https://github.com/user-attachments/assets/522949e6-6351-4f51-8da6-04ae655dbb33" />

Seguidamente procedemos a analizar el ejercicio propuesto y comenzamos con el mismo. Avanzamos hasta la fase 2 de la actividad y lo dejamos por hoy.

Día 2 (04/03/26):
Avanzamos en la actividad, logramos acabar gran parte de la fase 2, configuramos el router y el DHCP por VLAN:

<img width="1440" height="900" alt="Captura desde 2026-03-04 09-27-17" src="https://github.com/user-attachments/assets/d277c983-87d3-44e7-8de8-c2841e471ad8" />

Día 3 (05/03/26):
Tras investigar nos desatascamos en la fase 3 de la tarea y conseguimos avanzar y por fin conectamos ambas instancias de packet tracer mediante el multiuser y conseguimos realizar el DNS cruzado entre ambos servidores

<img width="1440" height="900" alt="Captura desde 2026-03-05 13-41-19" src="https://github.com/user-attachments/assets/8f23d546-4c8e-45bd-8878-bc455e1b9e03" />

Día 4 (6/03/26):
Nos dieron la opción de teletrabajar hoy día viernes así que procedí a traerme el ejercicio a casa y continuar avanzando dentro de la fase 4 que recién comenzamos el día anterior. 
Instalamos ACLs extendidas dentro de ambas instancias de Packet Tracer para posteriormente verificarlas buscando que den ping y que estén bloqueadas ciertas direcciones.Nos encontramos con un problema dentro de las instancias que no nos permite dar ping a direcciones IP fuera de su instancia, a pesar de que anteriormente daba ping, posiblemente es un error dado al momento de añadir las ACLs con direcciones IP incorrectas.

<img width="1919" height="1079" alt="Captura de pantalla 2026-03-06 121800" src="https://github.com/user-attachments/assets/9444d4f5-f0d3-4f3d-9e9a-a935ed37e6db" />

Día 5 (09/3/26):
Luego de recapaticar sobre las ACLs y por qué no conseguíamos verificar el primer ping de entre el PC-A y el Thingspeak-B, nos encontramos con diferentes errores dentro de las ACLs y de la configuración de NAT. Una vez resuelto eso ya funciona el ping, así que avanzamos a la siguiente comprobación. Nos percatamos que el Home Getaway estaba creando una red propia para asignar las direcciones IP a los dispositivos IoT, así que reemplazamos el Home Getaway con un Punto de Acceso que funciona como puente y hace que los dispositivos de IoT si tengan direcciones IP dentro de la VLAN correspondiente (20).

<img width="1374" height="727" alt="Captura desde 2026-03-09 13-43-51" src="https://github.com/user-attachments/assets/2f2366e1-9baa-4980-85f2-9cf3918fc524" />

Día 6 (11/03/26):

Una vez modificadas las ACLs y habiendo modificado la estructura, comenzamos las pruebas de pings para completar la fase 4 y luego de una pequeña correción nueva dentro de las ACLs, logramos verificar los 8 pings de manera correcta y funcionan como esperado. La razón por la que el ping P3 pasa es porque el origen y el destino pertenecen a la VLAN 20 de ambas instancias. En la ALC donde se decide es en la 20, se aplica en el Router A. Por otro lado, P4 falla de manera intencional porque se deniega, al no existir una ACL que permita el tráfico entre la VLAN 20 y la 30 de la otra instancia, se aplica un bloqueo. Este bloqueo existe en la linea 40.

<img width="1365" height="623" alt="P6" src="https://github.com/user-attachments/assets/2ec7efe8-6ad8-41fa-99e6-3508621cccb4" />

Una vez obtenidas todas las verificaciones de la fase 4, la damos por finalizada y comenzamos con la fase 5. Registramos los dispositivos IoT dentro de los servidores como se nos indicó:

<img width="748" height="509" alt="Captura desde 2026-03-11 12-31-11" src="https://github.com/user-attachments/assets/d90f879e-54e8-4d0d-a8e3-2cb72425f4da" />

<img width="748" height="509" alt="Captura desde 2026-03-11 12-46-47" src="https://github.com/user-attachments/assets/1fb143ec-3a79-49da-b594-1c2080adc24a" />

Día 7 (12/03/26):

Luego de registrar los dispositivos IoT, comenzamos a añadir condicionales y a cambiarlos de dirección de tal forma que ahora la sirena de la casa B se activa cuando se detecta movimiento o se abre la puerta en la casa A, y viceversa.

<img width="1375" height="761" alt="Captura desde 2026-03-12 10-24-39" src="https://github.com/user-attachments/assets/88f7200b-18c0-4f77-9707-d1e89188d7b1" />

<img width="1375" height="761" alt="Captura desde 2026-03-12 10-25-04" src="https://github.com/user-attachments/assets/7f81c895-a5f0-4395-9b2d-8b05728de996" />

Una vez hecho la verificación, procedemos a realizar las ultimas preguntas y cuestiones de teoría sobre la práctica.

Día 8 (13/03/26):

Una vez terminado todas las actividades de Packet Tracer, procedemos a comenzar con el planteamiento y el comienzo de la realización de nuestra nueva tarea en la que nos encargamos de crear un BACKEND utilizando MYSQL y PHP. Comenzamos por ver un curso de OpenWebinars sobre Sitios dinámicos con PHP y MYSQL. De momento el curso estoy colocando lo básico, tanto la base de datos como las herramientas a utilizar dentro.

Día 9 (16/03/26):

Continuamos el curso de OpenWebinars y seguimos avanzando en consolidar temario y contenidos para poder realizar el Backend utilizando PHP y MYSQL.

<img width="1372" height="864" alt="Captura desde 2026-03-16 13-07-31" src="https://github.com/user-attachments/assets/a82f6344-1afc-4d21-968a-bc24907e4a56" />

Día 10 (17/03/26):

Seguimos avanzando el curso de OpenWebinars para prepararnos en la realización del Backend. Hemos hecho la conexión de PHP con MYSQL y estamos tratando con funciones básicas de base de datos para consolidar temario.

<img width="1376" height="826" alt="Captura desde 2026-03-17 13-42-01" src="https://github.com/user-attachments/assets/f42797fe-f7e1-4d68-94f5-ba230b5d93e7" />

Día 11, 12 y 13 (18-20/03/26):

Al dar por canceladas las clases por el temporal y dar la jornada de forma telemática, procedí a continuar con el curso de openwebinars para completarlo y así tener más claro como realizar el backend de la página web.

Día 14 (23/03/26):
Aproveché mi cumpleaños en la empresa pasándo todo lo que había aprendido de casa del curso y colocandolo en la máquina con ubuntu para posteriormente el próximo día comenzar con la creación del backend.

<img width="1372" height="820" alt="imagen" src="https://github.com/user-attachments/assets/1705cdc0-8efe-4192-9b47-8decd0f05d61" />

Día 15 (24/03/26) DÍA DE VISITA AL INSTITUTO

Día 16 (25/03/26):
Al haber tormenta, alerta y al haber puesto las clases de forma telemática, aproveché en casa para seguir consolidando para poder comenzar con seguridad el backend de la empresa.

Día 17 (26/03/26):
Tuvimos una reunión donde comentamos todo lo que se necesitaba tanto del backend como del frontend de la web. Hicimos un esquema de las tablas que había que tener en la base de datos junto con sus relaciones además de pruebas para futuras consultas sobre las actuaciones o servicios de los profesionales.

Día 18 (27/03/26):
Pasé gran parte del día haciendo pruebas de consultas SQL, al mismo tiempo que realicé una prueba de conversión de formato de php a JSON para poder mandar los datos de las tablas de la base de datos al frontend.

<img width="1372" height="801" alt="imagen" src="https://github.com/user-attachments/assets/e99761e1-0d5d-44fd-82f6-8718fb64f761" />

Día 19 (06/04/26):
El día consistió en filtrar los datos de la base de datos en el JSON para que se mostrasen únicamente ciertos datos en específico. Además, Nasser nos puso la tarea de construir un formulario para que los profesionales sean capaces de añadir nuevas actuaciones dentro de la base de datos, esto con una consulta SQL con los datos del formularios importados directamente al script para que haga el cambio. El único inconveniente es conseguir que desde el frontend se pueda sincronizar la "sesión" de dicho profesional con la ID de la base de datos, para que así los profesionales no puedan añadir actuaciones o servicios a diferentes profesionales.

<img width="1380" height="876" alt="imagen" src="https://github.com/user-attachments/assets/814f8b37-b024-4ea5-a8fb-018c6d72485c" />

Día 20 (07/04/26):

Seguimos montando el backend, realicé una estructura más ordenada ya que me informaron que no hacía falta el login por token asignado a la sesión para mandar a la base de datos. Añadí las estadísticas de horas totales impartidas por profesional y horas totales recibidas por usuario y separé el .php principal de la api y lo dividí en controller, models y api, para que, en caso de que falle algo, el error sea más fácil de encontrar. También añadí una carpeta llamada "old" donde tengo guardados los antiguos scripts php por si en algún momento necesito hacer uso de alguno más adelante.

<img width="1375" height="781" alt="image" src="https://github.com/user-attachments/assets/4ecd6e0d-28ed-46e9-afb2-d6f8e0c9239e" />

Día 21 (08/04/26):

Mientras termino las funciones principales del backend, he decidido añadir dentro de la base de datos la tabla de talleres, ya que Nerea nos comentó que quería poder ver los talleres, el tipo de taller, el profesional que la imparte y los usuarios beneficiaros por el taller. Lo completamos de manera ordenada dentro de cada carpeta y añadimos un ejemplo para verificarlo dentro de la página en JSON. También hemos añadido más usuarios, más profesionales y más ejemplos para que la base de datos se vea con contenido.

<img width="1128" height="459" alt="image" src="https://github.com/user-attachments/assets/a393b207-04f0-46d9-919d-35aaacc3a96b" />

<img width="1376" height="817" alt="image" src="https://github.com/user-attachments/assets/38d48b81-6146-41fd-bf7f-38792d266b77" />

Día 22 (09/04/26):

El día consistió en verificar que la base de datos estuviese completa y que no hubiesen ningún error de sintaxis o de escritura en general. Quedo a la espera del frontend para poder unirlo y confirmar que los datos funcionen correctamente y que la base de datos también lo haga.


Día 23 (10/04/26):

Hoy seguí revisando fallos del backend y a su vez me encargué de añadir lineas dentro para asegurar que la conexión con el frontend sea segura. Hoy comenzamos a preparar el frontend y a analizar cómo juntarlos para poder realizar pruebas sin necesidad de moverse mucho entre un ordenador a otro.


Día 24 (13/04/26):

El día de hoy el aula se estuvo utilizando para una clase, así que tuve que moverme a otro ordenador sin la base de datos ni el backend, pero no hubo problema ya que mi parte del proyecto ya estaba terminada y, a no ser que estuviese mi compañera conmigo no podía adaptar el backend, ya que ella se encarga del frontend. Aproveché el tiempo y me puse a trabajar con herramientas de google con inteligencia artificial y propuse la situación de la empresa para ver cuáles otros métodos para solucionarlo existían. Llegué a trabajar con Google AI Studio y con Firebase, la solución y la APP que me generó fue bastante interesante, aunque me fijé más en la estética del frontend que propuso para, si es posible, implementarla dentro de nuestro proyecto.

<img width="1254" height="927" alt="image" src="https://github.com/user-attachments/assets/0af0157c-1279-4cb6-b563-e0269395a4e3" />


Día 25 (14/04/26):
VISITA AL INSTITUTO

Día 26 (15/04/26):

Hicimos retoques al frontend ya que tuvimos que cambiar un poco la estructura, también se tuvo que agregar más detalles y ejemplos al backend, debido a que no teníamos datos necesarios para realizar pruebas y tampoco teníamos un filtro de profesionales y actuaciones (es decir, que el fisioterapeuta podía colocar un servicio que no estaba asociado a los suyos o a sus usuarios).

<img width="1535" height="828" alt="imagen" src="https://github.com/user-attachments/assets/022fc2e5-823f-4d57-bae2-4cf3f58f89b8" />

Día 27 (16/04/26):

Cambiamos gran parte de la estructura, creamos nuevas partes de la API e hicimos una estructura diferente para el frontend. El mayor logro de este día fue poder conectar el frontend con el backend.

Día 28 (17/04/26):

Tuvimos que reestructurar diferentes partes del frontend, crear nuevos archivos .php y por fin, el formulario del frontend da la información correcta sobre los usuarios de la base de datos, es el mayor avance que hemos hecho hasta el momento, lo siguiente que queda es preparar el sistema de loggeo para que, posteriormente, se pueda registrar una actuación dentro de la base de datos.

Día 29 (20/04/26):

Gran parte de la jornada nos la pasamos averiguando el por qué al momento de mandar el formulario mediante una consulta POST llegaba al backend pero no a la base de datos, así que poco a poco estamos averiguando el problema hasta que lo solucionemos por completo y podamos finalizar la prueba.

Día 30 (21/04/26):

Procedimos a crear un filtro para que, una vez los profesionales inicien su sesión, les aparezca sus respectivos usuarios y sus respectivos servicios para realizar el formulario de manera individual, también se modificó la estructura de la base de datos y se agregó un archivo php para filtrar estos usuarios y servicios.
<img width="1526" height="887" alt="imagen" src="https://github.com/user-attachments/assets/fdd783c7-4385-4ab4-b9fb-44e79022e550" />

Día 31 (22/04/26):

Hoy aprovechamos el día para optimizar todos los archivos, simplificar algunas consultas y así evitar errores futuros. 

Día 32-33 (23-24/04/26):
Al haber nadie en la empresa para supervisar, se nos recomendó realizar teletrabajo, por lo que aproveché para buscar formas de optimizar el PHP y también hice varios planteamientos sobre diferentes situaciones de cómo implementar este proyecto al sistema de la empresa.

Día 34 (27/04/26):

Hoy al no tener a mi compañera (y, por ende, no tener el frontend), me dediqué a plantear el cómo integrar el sistema de tokens por login a nuestro proyecto.

Día 35 (28/04/26):
VISITA AL INSTITUTO

Día 36, 37 y 38 (29-04/0/26):
Nasser nos comunicó que, debido a un viaje, no iba a poder estar en la empresa, por lo que nos tocó hacer teletrabajo. Estuve analizando la estructura del backend y de cómo conseguir que podamos hacer pruebas con tokens e IDs sin necesidad de cargarnos el esquema que tenemos ya creado.

Día 39 (05/04/26):
Luego del puente, decidimos poner a prueba nuestro sistema e implementarlo a la base de datos real de la empresa. Resolvimos un pequeño problema que no dejaba registrar actuaciones de otros profesionales ya que la actividad no estaba vinculada a ningún servicio, pero se resolvió rápido.

Día 40 (07/04/26):
Comenzamos por crear una dashboard para el administrador y para los profesionales donde salga de forma más detallada la información tanto de usuarios como de actuaciones.
<img width="1539" height="827" alt="image" src="https://github.com/user-attachments/assets/984821a3-70fb-4655-9cfb-ce677fbb0e5e" />
