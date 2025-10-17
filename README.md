# Tarea7
## Punto 1: ¿Cuál es el significado de la información que me expone htop? y ¿cómo la puedo complementar con glances, ifconfig, nmap y lynis?
### Significado de la información que muestra htop
`htop` presenta en tiempo real el estado del sistema operativo.\
Muestra:
+ El uso de CPU, RAM y memoria swap.
+ La carga promedio del sistema (cuántos procesos están activos).
+ El tiempo de actividad del equipo.
+ Una lista de procesos en ejecución, indicando cuánta CPU y memoria consume cada uno, a qué usuario pertenece y qué comando los inició.
  
**Básicamente este comando sirve para supervisar el rendimiento y detectar procesos que saturan recursos.**

Para arch-linux el comando para ejecutar htop es:\
<img width="643" height="36" alt="image" src="https://github.com/user-attachments/assets/d2c01c06-7ca2-4a3a-abd0-906114fd5d98" />\
Lo que se ve cuando ejecutamos:
<img width="1300" height="736" alt="image" src="https://github.com/user-attachments/assets/20b8e9b4-cb30-4a18-a0f4-3b0096f3554d" />
En la parte superior lo que se observa es:
+ **CPU**: la barra de colores muestra el porcentaje de uso del procesador; en este caso, el uso es muy bajo (~0.6%).
+ **Mem**: indica el uso de memoria RAM (389 MB de 1.9 GB usados).
+ **Swp**: memoria de intercambio (swap), que está en 0, osea que no se está usando.
+ **Tasks**: cantidad de tareas (77 procesos, 168 hilos, 1 en ejecución).
+ **Load average**: promedio de carga del sistema en los últimos 1, 5 y 15 minutos (muy bajo: 0.16, 0.22, 0.11 → el sistema está relajado).
+ **Uptime**: tiempo que lleva encendido el sistema (5 minutos y 17 segundos).

En la lista de procesos, se ven las columnas donde se obtiene esta información:
+ **PID**: identificador del proceso.
+ **USER**: usuario que ejecuta el proceso.
+ **PRI / NI**: prioridad y valor nice del proceso.
+ **VIRT, RES, SHR**: uso de memoria virtual, residente y compartida.
+ **%CPU / %MEM**: porcentaje de CPU y memoria que consume.
+ **TIME+**: tiempo total de CPU usado desde que inició.
+ **COMMAND**: el comando o programa que se está ejecutando.

### Cómo complementar esa información con otras herramientas
* `glances`: amplía la información de htop, mostrando en una sola vista el uso de CPU, memoria, disco, red, sensores, procesos y servicios. Ofrece una visión general más completa del sistema.
* `ifconfig`: permite ver la configuración y estado de las interfaces de red (direcciones IP, tráfico, errores). Complementa a htop y glances al diagnosticar el rendimiento o fallos de red.
* `nmap`: analiza equipos y puertos abiertos en la red. Se usa para detectar servicios activos o vulnerables, complementando la información de procesos que se comunican por la red.
* `lynis`: realiza una auditoría de seguridad del sistema, revisando configuraciones, permisos, servicios y nivel de protección. Complementa las otras herramientas al ofrecer un análisis de seguridad y recomendaciones.

`ifconfig`:  
<img width="655" height="342" alt="image" src="https://github.com/user-attachments/assets/c581377c-685b-4593-a188-29bd606b27d6" />\
`nmap`:
<img width="987" height="495" alt="Captura de pantalla 2025-10-17 124520" src="https://github.com/user-attachments/assets/0358f658-e3ba-4083-aad3-d56faeae694b" />
(tomado de: Nmap - Port Scanner - BlackArch Linux #30, YouTube)\
`lynis`:
<img width="1300" height="736" alt="image" src="https://github.com/user-attachments/assets/b0ac0657-eb7c-413b-8723-35184c8ec61d" />



