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
