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
Instalamos ACLs extendidas dentro de ambas instancias de Packet Tracer para posteriormente verificarlas buscando que den ping y que estén bloqueadas ciertas direcciones.

Día 5 (09/3/26):
Luego de recapaticar sobre las ACLs y por qué no conseguíamos verificar el primer ping de entre el PC-A y el Thingspeak-B, nos encontramos con diferentes errores dentro de las ACLs y de la configuración de NAT. Una vez resuelto eso ya funciona el ping, así que avanzamos a la siguiente comprobación. Nos percatamos que el Home Getaway estaba creando una red propia para asignar las direcciones IP a los dispositivos IoT, así que reemplazamos el Home Getaway con un Punto de Acceso que funciona como puente y hace que los dispositivos de IoT si tengan direcciones IP dentro de la VLAN correspondiente (20).

<img width="1919" height="1079" alt="Captura de pantalla 2026-03-06 121800" src="https://github.com/user-attachments/assets/9444d4f5-f0d3-4f3d-9e9a-a935ed37e6db" />

Nos encontramos con un problema dentro de las instancias que no nos permite dar ping a direcciones IP fuera de su instancia, a pesar de que anteriormente daba ping, posiblemente es un error dado al momento de añadir las ACLs con direcciones IP incorrectas.
