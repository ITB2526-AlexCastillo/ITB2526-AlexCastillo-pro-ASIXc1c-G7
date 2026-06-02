**PROYECTO TRANSVERSAL ASIXc 2025\_2026**









**CREACIÓN DE CPD PARA INNOVATE TECH**



































**indice**



















































**DESCRIPCION**



Aquí tienes la descripción completa del proyecto traducida al castellano de forma clara y profesional:

## **Descripción del Proyecto: Innovate Tech**

El proyecto nace de la necesidad de **Innovate Tech**, una empresa dedicada a la prestación de servicios tecnológicos, de modernizar su capacidad operativa y comunicativa. El crecimiento de la actividad de ventas en línea y la demanda de soporte técnico requieren una base tecnológica sólida que integre la gestión del personal con servicios multimedia avanzados.

El objetivo central es diseñar e implementar un **Centro de Procesamiento de Datos (CPD)** eficiente, que actúe como el corazón de las operaciones de la empresa, garantizando la continuidad del negocio y la calidad del servicio en un entorno empresarial exigente.

### **Arquitectura e Infraestructura en la Nube**

Para responder a estas necesidades, la propuesta arquitectónica está **orientada a la nube mediante AWS**, priorizando la sostenibilidad y la seguridad. Se plantea una infraestructura que soporte:

* La distribución de contenidos de **audio y vídeo en streaming**.
* Sistemas de **videoconferencia** para la formación y la comunicación interna.
Este despliegue se acompaña de **pruebas de ancho de banda** para asegurar una transmisión fluida y sin degradación, optimizando el uso de recursos para minimizar el impacto ambiental y calcular la huella ecológica de los procesos.

### **Gestión de Datos y Seguridad**

Finalmente, el proyecto incluye la implementación de una **base de datos integral** para gestionar la estructura organizativa y el registro de actividad. Este sistema incorpora:

* Un **control de acceso estricto** mediante roles.
* **Automatización de tareas** con *scripts*.
* *Triggers* (disparadores) de **auditoría** para proteger la información sensible.
**Gestión y Despliegue:** Toda la infraestructura se gestiona con herramientas de configuración como **Ansible** y se documenta en formato **Markdown en GitHub**, asegurando una solución tecnológica escalable, segura y alineada con la normativa internacional de protección de datos.

















































1. **Propuesta CDP**
  1. **Ubicación física**
    1. **Situación física de la sala y el edificio**
El Centro de Procesamiento de Datos (CPD) se ha ubicado estratégicamente en la **planta sótano -1** del edificio corporativo. Se ha seleccionado un espacio interior central, libre de paredes acristaladas o fachadas con orientación directa a la vía pública. Esta localización ofrece dos ventajas críticas:

* **Aislamiento Térmico:** Maximiza la inercia térmica de la estructura, minimizando el impacto de la radiación solar exterior en la carga de refrigeración de la sala.
* **Seguridad Física (Mitigación de Sabotajes):** Al no disponer de ventanas transitables, se reduce drásticamente la superficie de exposición frente a intrusiones perimetrales o vandalismo físico.
    1. **Sistemas de climatización y control ambiental**
Para la disipación del calor generado por la infraestructura activa se han desplegado dos unidades de aire acondicionado de precisión para salas de servidores, denominadas **CRAC 1 y CRAC 2** (*Computer Room Air Conditioner*), configuradas en régimen de **redundancia $N+1$**. Ambas unidades monitorizan y regulan las variables ambientales del CPD bajo los siguientes estándares normativos internacionales (ASHRAE):

* **Temperatura:** Mantención de un punto de consigna constante de  21 ºC +- 2ºC en el pasillo frío.
* **Humedad Relativa:** Regulada estrictamente entre el **$40% y el $55%**. Un valor inferior incrementaría el riesgo de descargas electrostáticas (ESD), mientras que un valor superior provocaría condensación y fenómenos de corrosión en las placas base de los servidores.
* **Pureza del Aire:** Los sistemas CRAC integran etapas de filtrado mecánico de partículas para asegurar la renovación constante del aire, manteniendo la sala libre de micropartículas de polvo en suspensión que puedan obstruir los disipadores internos del hardware.




    1. **Medidas para dificultar la identificación de la sala**
Con el objetivo de dificultar la identificación de la sala por parte de personal no autorizado o atacantes internos, se ha aplicado una política de **seguridad por ocultación**. La puerta de acceso al recinto carece de cualquier rotulación corporativa o indicación técnica (como "Sala de Servidores", "Sistemas" o "CPD"). Físicamente se presenta como una puerta de servicio estándar, integrada estéticamente en el pasillo común, ocultando la existencia de la infraestructura crítica tras ella.

    1. **Distribución y gestión del cableado**
Bajo la superficie transitable se distribuye una infraestructura de cableado estructurado mediante bandejas de rejilla metálica electrozincadas. Para mitigar las interferencias electromagnéticas (EMI) y cumplir con la normativa de segregación de servicios, se han desplegado dos canalizaciones físicamente separadas:

* **Canalización A (Datos):** Aloja de manera ordenada los mazos de cableado de par trenzado UTP Categoría 6A para la LAN interna y los latiguillos de fibra óptica para los enlaces ascendentes (*uplinks*).
* **Canalización B (Potencia):** Conduce de forma aislada las líneas de fuerza eléctrica con aislamiento ignífugo desde los cuadros de distribución y los SAIs hacia las regletas de alimentación de los racks.


    1. **Suelo técnico y semicierre de techo técnico**


La sala dispone de una solución de **suelo técnico sobreelevado** a una altura de 40cm mediante pedestales de acero regulables y baldosas modulares de alta resistencia mecánica. Este espacio inferior (plenum) actúa como cámara de sobrepresión para impulsar de forma homogénea el aire frío generado por los CRACs hacia las baldosas perforadas del pasillo central. Asimismo, se dispone de un falso **techo técnico** que oculta los conductos de extracción de aire, el cableado de los sensores ambientales y el sistema de tuberías microperforadas para la inundación del gas extintor.



**Plano de Planta de Distribución General:**

![Imagen Extraída 1](images/image_1.png)

Este diagrama describe la distribución espacial de la sala, la ubicación perimetral de las cámaras CCTV, los tanques de gas NOVEC, los motores de climatización y las dimensiones de seguridad en los pasillos de mantenimiento.

    1. **Estructuración de los racks**
La capacidad de cómputo y almacenamiento se distribuye en dos armarios físicos (**RACK 1 y RACK 2**) de formato estándar de 19 pulgadas y 42U de altura. Ambos racks se han dispuesto de forma paralela y enfrentada para hacer posible el confinamiento de pasillos descrito anteriormente. La estructuración interna se ha planificado de forma simétrica bajo un criterio estricto de **Alta Disponibilidad (HA)**, duplicando de manera exacta los servidores y la electrónica de red en ambos armarios para asegurar la tolerancia a fallos del CPD.





  1. **Infraestructura IT (Equipamiento activo de los racks)**
La arquitectura de red interna del CPD se ha diseñado bajo un criterio estricto de **Alta Disponibilidad (HA)** y eliminación de puntos únicos de fallo (SPOF). Cada uno de los dos armarios instalados cuenta con una réplica exacta de la electrónica y la potencia de cálculo para asegurar la tolerancia a fallos del sistema.



![Imagen Extraída 2](images/image_2.png)



    1. **Inventario y modelo de distribución en unidad de rack**
Los armarios seleccionados son de formato estándar de 19 pulgadas con una altura útil de 42U. Como se detalla en el diagrama técnico anterior, la distribución vertical de los componentes sigue una lógica de estratificación por peso, disipación térmica y función:

* **Paneles de Parcheo (Patch Panels):** Ubicados en el extremo superior de ambos racks. Tienen la función de recibir mecánicamente el cableado de par trenzado UTP Categoría 6A procedente del suelo técnico, facilitando un peinado, organización y guiado estructurado antes de su interconexión con la electrónica activa.
* **Electrónica de Red y Seguridad (Switches y Firewalls):**
  * **RACK 1:** Despliega el **Firewall / Router** perimetral encargado de las políticas de seguridad (ACLs) y el enrutamiento hacia la WAN, junto al **Network Switch 0** (conmutador local de este rack).
  * **RACK 2:** Integra un entorno redundante de capa de enlace compuesto por dos conmutadores: el **Network Switch 1** y el **Network Switch 2**. Ambos equipos están interconectados mediante agregación de enlaces (*Link Aggregation / EtherChannel*).
* **Servidores de Cómputo de Alta Densidad (Server A al E):** Chasis modulares de tipo rack con formato 2U. Cada servidor implementa hardware redundante dotado de bahías frontales de almacenamiento con configuración **RAID hot-swap** (extracción en caliente) y ventiladores de alta presión estática por cartucho. El inventario simétrico consta de:
  * **Server A (Web / SFTP):** Nodo encargado de publicar el servicio HTTP corporativo y la pasarela de transferencia de archivos segura cifrada.
  * **Server B (Active Directory):** Controlador de dominio centralizado (Samba4) para la gestión de identidades y políticas de seguridad de la organización.
  * **Server C (Logs Centralized):** Instancia dedicada a la recolección, indexación y auditoría de los ficheros de eventos generados por el resto de la infraestructura (Stack ELK).
  * **Server D (Servicios Multimedia):** Servidor optimizado para la codificación y transmisión de flujos de audio y vídeo para las herramientas colaborativas (streaming y videoconferencia).
  * **Server E (Base de Datos):** Motor relacional centralizado donde residen los repositorios de información críticos del resto de aplicaciones.
* **Sistemas de Control Local (KVM Console Tray):** Bandeja desplegable integrada con teclado, ratón y monitor analógico que permite la gestión local directa sobre el chasis de los servidores en caso de pérdida de conectividad remota por red.
* **Sistemas de Distribución Eléctrica y Respaldo (PDU y UPS/SAI):** Aloja las regletas de alimentación inteligente (*Power Distribution Unit*) y el módulo de baterías del SAI para el soporte contra cortes de tensión.


    1. **Diseño logico**


Para la conexión lógica de los distintos equipos, hemos optado por una arquitectura tipo red jerárquica separada por vlans, con un bucle  entre 2 switches 2960 y 1 switch capa 3 3560-24PS y un router ISR 4331 para la salida al exterior.

![Imagen Extraída 3](images/image_3.png)

Los distintos racks se han separado lógicamente en las vlans 10 y 20 (10 para rack 1, 20 para rack 2) para tener una leve capa de seguridad extra y para mejorar la gestión de tráfico y para permitir la ampliación a más CPD a futuro sin causar problemas de remodelar.



* **Conexión interna**
Para la conexión interna entre los dos Racks, hemos usado las vlans 10 y 20, con el rango de ip 192.168.10.x y 192.168.20.x. Además, para ajustar los puertos trunk hemos creado la vlan 99 NATIVE\_TRUNK de forma que ningún puerto activo se quede en la vlan default. Además hemos ajustado STP para que todo el tráfico pase por el switch core, dejando un cable como respaldo.



* **Conexión externa**
Para la salida al exterior, hemos decidido usar el protocolo NAT/PAT (o NAT Overload). De esta forma, creamos una ACL que permita salir a los dos racks, y todo lo que pase que coincida con la lista, lo traduce a una ip pública disponible de la red del router

![Imagen Extraída 4](images/image_4.png)

![Imagen Extraída 5](images/image_5.png)





    1. **Justificación de Arquitectura de Conmutación (Spanning tree)**
Como se especifica en el diseño lógico de la infraestructura, la presencia de dos conmutadores independientes en el Rack 2 responde a una necesidad de redundancia técnica justificada bajo los siguientes criterios:

* **Evitación de Bucles de Capa 2 (STP):** La interconexión física redundante entre los switches activa de forma automática el protocolo **Spanning Tree Protocol (STP)**. Este protocolo mantiene uno de los enlaces en estado de reserva (*blocking*), listo para activarse en milisegundos si el conmutador principal sufre una avería, evitando tormentas de broadcast que tumbarían la LAN plana (10.10.10.0/24).
* **Mitigación de Cuellos de Botella (Router):** Al concentrar la redundancia y el tráfico de conmutación local directamente en la electrónica de los switches del Rack 2, se evita la saturación por sobreprocesamiento en el Router perimetral. De este modo, el Router se dedica exclusivamente a sus funciones críticas: el filtrado de paquetes (*Firewall/ACL*) y la traducción de direcciones (*NAT*).
* **Simplicidad de Direccionamiento:** Mantener un único enrutador en la cabecera del Rack 1 evita la complejidad de gestionar dos pasarelas residiendo en redes lógicas separadas, simplificando la sincronización de servicios y la coherencia de la tabla de rutas.
    1. ** Sistema de Alimentación Ininterrumpida (SAI) **
Para mitigar cortes de suministro eléctrico en la infraestructura local, se ha integrado un SAI de tecnología On-Line (Doble Conversión). Este sistema proporciona un tiempo de transferencia de 0 ms, garantizando una alimentación limpia de ruidos eléctricos directamente desde las baterías de forma permanente.

1. **Carga Crítica:** Dimensionado para soportar 1500W de electrónica perimetral local.
1. **Autonomía:** Dispone de 30 minutos de respaldo a media carga.
1. **Automatización:** Incorpora conectividad mediante tarjeta SNMP para lanzar un script de apagado ordenado (*graceful shutdown*) en caso de que el corte de energía supere los 15 de minutos.


  1. **Seguridad física y lógica**
    1. **Seguridad física**
1. ** Elementos de control de acceso a incorporar en el CPD y Videovigilància**
Para mitigar el riesgo de intrusismo, sabotaje o acceso de personal no autorizado a la sala crítica, se han implementado dos capas de seguridad perimetral coordinadas:

* **Control de Acceso:** La puerta principal de la sala cuenta con un **Lector de Tarjetas RFID combinado con un sistema de verificación biométrica (huella dactilar)**. Cualquier intento de apertura (exitoso o fallido) genera un registro automático e inalterable en una base de datos local que almacena la identidad del operario, la fecha y la hora exacta.
* **Videovigilancia:** Como se ha definido en el plano de planta, se dispone de un circuito cerrado de televisión (**CCTV**) compuesto por **tres cámaras IP** con resolución 4K y visión nocturna por infrarrojos. Su disposición cruzada está diseñada estratégicamente para eliminar cualquier punto ciego en la sala, cubriendo tanto el acceso exterior como los pasillos técnicos de mantenimiento de ambos armarios. Las grabaciones se almacenan cifradas en un almacenamiento dedicado durante un mínimo de 30 días.
1. **Sistemas prevención, detección y de extinción de incendios**
El CPD dispone de un sistema de extinción automática mediante inundación de agente limpio, diseñado específicamente para no dañar el hardware eléctrico activo y evitar cortocircuitos colaterales:

* **Detección:** Se ha instalado un **Detector de Humo Óptico** de alta sensibilidad en el techo técnico, conectado de forma directa a la central de alarmas del edificio.
* **Extinción Automática (Gas NOVEC 1230):** En caso de confirmarse una alerta de incendio por doble lazo de sensores, el sistema activa la descarga de los cilindros de gas **NOVEC 1230** a través de las tuberías microperforadas. Este gas extingue el fuego por enfriamiento térmico a nivel molecular en pocos segundos sin dejar ningún tipo de residuo, no es conductor de la electricidad y es totalmente seguro para la integridad física de los operarios que se encuentren en la sala.
* **Extinción Manual:** Junto a la puerta de entrada se dispone de un **extintor manual de CO²** para sofocar pequeñas emergencias localizadas antes de activar la inundación global.


1. **Vias de evacuacion**
La puerta de acceso al recinto del CPD cuenta con sentido de apertura hacia el exterior de la sala y está dotada de una **barra antipánico** de apertura mecánica inmediata. El recorrido de evacuación interior está señalizado mediante luminarias de emergencia LED autónomas que guían al personal de forma segura hacia las salidas de emergencia generales de la planta sótano -1 del edificio.



    1. **Seguridad lógica**
1. **Restricción d’accés per autorització**
En toda la infraestructura se aplica de forma estricta el **principio del menor privilegio**. Los usuarios comunes de la corporación carecen de permisos de administración sobre la red o el hardware. Toda la gestión de identidades y autorizaciones se centraliza en el **Server B (Directorio Activo)** a través de Samba4, creando grupos de seguridad restringidos (como SysAdmins) a los que solo pertenecen los técnicos debidamente autorizados.

1. **Firewalls**
La frontera perimetral de la red está custodiada por el **Router/Firewall** de cabecera situado en la parte superior del Rack 1. Este dispositivo implementa políticas de filtrado mediante listas de control de acceso (ACL) que bloquean por defecto todo el tráfico entrante desde la WAN (*Implicit Deny*), permitiendo única y exclusivamente las conexiones dirigidas a los puertos de los servicios esenciales publicados (HTTP, HTTPS, SFTP).

* *Nota:* Los diagramas de la topología y las evidencias del filtrado de paquetes se validan en el entorno simulado de **Cisco Packet Tracer** dentro del Bloque 2 de este proyecto.


1. ** Monitorització**
Para garantizar la proactividad del equipo técnico ante anomalías o caídas de servicio, se ha configurado el **Server C (Logs Centralized)** mediante el despliegue del *Stack ELK* (Elasticsearch, Logstash y Kibana). Este servidor recolecta en tiempo real todos los eventos de syslog del resto de máquinas mediante el demonio rsyslog. El sistema monitoriza de forma constante:

1. Intentos de acceso SSH o SFTP fallidos para alertar de posibles ataques de fuerza bruta.
1. Uso de CPU, memoria RAM y almacenamiento en disco de cada servidor.
1. Altas, bajas o modificaciones de privilegios en el árbol del Directorio Activo.
1. **Còpies de seguretat/Backups y RAIDs**
Para proteger la información crítica del negocio y asegurar la persistencia de los repositorios de la base de datos (**Server E**):

* **Redundancia de Almacenamiento (RAID):** Todos los servidores físicos implementan una configuración de discos locales en **RAID 1 (Mirroring)** o **RAID 5 (con paridad)** de tipo *Hot-Swap*. Esto permite que, ante el fallo mecánico de un disco duro, el servidor continúe operando con total normalidad sin pérdida de datos ni interrupción del servicio, permitiendo la sustitución del disco dañado en caliente.
* **Còpies de Seguridad (Backups):** Se ha programado una política de copias automatizada. Se genera una copia completa (*Full Backup*) de forma semanal durante las horas de menor carga y copias incrementales diarias. Estos respaldos se empaquetan, se cifran y se replican externamente en el entorno de la nube (AWS) para garantizar la recuperación ante desastres geográficos.


    1. **Prevención de riesgos laborales**
En cumplimiento de las normativas de salud e higiene en el trabajo, se aplican las siguientes medidas preventivas de obligado cumplimiento dentro de la sala del CPD:

* **Protección acústica:** Debido al ruido continuo generado por las altas revoluciones de los ventiladores de los servidores y los motores de climatización (CRAC), el nivel sonoro de la sala supera habitualmente los 75 dB. Es obligatorio el uso de tapones o auriculares de protección acústica para cualquier operario que deba realizar tareas de mantenimiento prolongadas en el interior.
* **Ergonomía en la Manipulación de Cargas:** Los chasis de los servidores rack de alta densidad presentan un peso elevado. Para su instalación o retirada de los armarios, se exige que la tarea sea realizada por un mínimo de dos operarios o mediante el uso de elevadores mecánicos manuales para prevenir lesiones lumbares.
* **Mitigación del Riesgo Eléctrico:** Todos los bastidores de los racks cuentan con una **conexión física de puesta a tierra** unida a la estructura del edificio para disipar derivaciones eléctricas accidentales. Queda prohibido manipular fuentes de alimentación o realizar conexiones internas sin aislar previamente el equipo de las PDUs activas.


  1. **Implementación del CPD al Núvol AWS y servicios utilizados**
![Imagen Extraída 6](images/image_6.png)

Creamos la VPC

![Imagen Extraída 7](images/image_7.png)



![Imagen Extraída 8](images/image_8.png)

crear subred pública

![Imagen Extraída 9](images/image_9.png)

a bajo crear la subred privada

![Imagen Extraída 10](images/image_10.png)





![Imagen Extraída 11](images/image_11.png)

Crear un gateway hacia internet

![Imagen Extraída 12](images/image_12.png)

Lo vinculamos a la VPC que hemos creado anteriormente

![Imagen Extraída 13](images/image_13.png)

![Imagen Extraída 14](images/image_14.png)

Editamos las rutas añadiendo una gateway a internet (0.0.0.0/0)

![Imagen Extraída 15](images/image_15.png)

![Imagen Extraída 16](images/image_16.png)

creando la primera EC2



![Imagen Extraída 17](images/image_17.png)

creando una llave para poder acceder al server

![Imagen Extraída 18](images/image_18.png)

configurar la red



![Imagen Extraída 19](images/image_19.png)

![Imagen Extraída 20](images/image_20.png)

Dando permisos para poder abrir la llave que esta guardada en /Escriptori/DADES/Miriam y accediendo por ssh sin contraseña mediante la ip pública que se ha seleccionado la EC2 



![Imagen Extraída 21](images/image_21.png)

Hacer un update y un upgrade del sistema y instalar las dependencias que existan



![Imagen Extraída 22](images/image_22.png)

instalar apache2 con sus dependencias.

![Imagen Extraída 23](images/image_23.png)

Comprobar el estado de apache2



![Imagen Extraída 24](images/image_24.png)

se puede acceder a la pagina web con la ip 



![Imagen Extraída 25](images/image_25.png)

instalamos sftp



![Imagen Extraída 26](images/image_26.png)

creamos un usuario para ver si todo funciona en el sftp



![Imagen Extraída 27](images/image_27.png)





![Imagen Extraída 28](images/image_28.png)

![Imagen Extraída 29](images/image_29.png)

le hemos quitado la almohadilla (#)



![Imagen Extraída 30](images/image_30.png)

añadimos esto al final del documento para forzar que el usuario se quede en su carpeta y no pueda acceder a otras carpetas.

![Imagen Extraída 31](images/image_31.png)



![Imagen Extraída 32](images/image_32.png)

instalamos el repositorio oficial de ansible

![Imagen Extraída 33](images/image_33.png)

instalamos ansible

![Imagen Extraída 34](images/image_34.png)



Crear servidor ldap



![Imagen Extraída 35](images/image_35.png)



![Imagen Extraída 36](images/image_36.png)

Ponerle una Primary IP 172.16.10.10  y ponerle una ip privada y que no asigne una ip pública. 

![Imagen Extraída 37](images/image_37.png)

Servidor ldap creado



vamos con el servidor de logs

![Imagen Extraída 38](images/image_38.png)



![Imagen Extraída 39](images/image_39.png)



![Imagen Extraída 40](images/image_40.png)



![Imagen Extraída 41](images/image_41.png)

primero accedemos al servidor web



accedemos aqui al servidor ldap

![Imagen Extraída 42](images/image_42.png)







![Imagen Extraída 43](images/image_43.png)

hacemos lo mismo pero cambiamos la ip para acceder al servidor de logs



![Imagen Extraída 44](images/image_44.png)

creamos el archivo en ~/ansible-infra y pegamos este archivo de aqui



![Imagen Extraída 45](images/image_45.png)



![Imagen Extraída 46](images/image_46.png)



![Imagen Extraída 47](images/image_47.png)

![Imagen Extraída 48](images/image_48.png)

![Imagen Extraída 49](images/image_49.png)

creamos el playbook para instalar mediante ansible el ldap en el servidor-ldap



![Imagen Extraída 50](images/image_50.png)

![Imagen Extraída 51](images/image_51.png)

Ejecutamos el playbook para que se instale todo





![Imagen Extraída 52](images/image_52.png)

 comandos de verificación para saber si se ha hecho bien.





hacemos otro playbook para la instalación del servidor de logs



![Imagen Extraída 53](images/image_53.png)

ejecutamos el playbook



comprobaciones de que el servidor de logs vaya bien

![Imagen Extraída 54](images/image_54.png)







![Imagen Extraída 55](images/image_55.png)

Clonar las llaves autorizadas



![Imagen Extraída 56](images/image_56.png)

Darle la propiedad de los archivos a admin-g7 con los permisos correctos



![Imagen Extraída 57](images/image_57.png)

![Imagen Extraída 58](images/image_58.png)

Instalar los conectores de LDAP (en modo silencioso para que no salten pantallas azules)



![Imagen Extraída 59](images/image_59.png)

Configurar la dirección del servidor LDAP



![Imagen Extraída 60](images/image_60.png)

Decirle al sistema operativo que busque usuarios en el LDAP



![Imagen Extraída 61](images/image_61.png)



![Imagen Extraída 62](images/image_62.png)

hemos accedido con el usuario creado por ldap mediante la ip publica de el servidor web



![Imagen Extraída 63](images/image_63.png)

comprobaciones de si el servidor de logs funciona correctamente



![Imagen Extraída 64](images/image_64.png)

![Imagen Extraída 65](images/image_65.png)























































1. **Implantación de servicios de audio y vídeo**
![Imagen Extraída 66](images/image_66.png)

creamos el servidor de audio video

![Imagen Extraída 67](images/image_67.png)



![Imagen Extraída 68](images/image_68.png)

ponemos donde hosts el servidor de audio porque hemos decidido configurarlo con ansible



![Imagen Extraída 69](images/image_69.png)

![Imagen Extraída 70](images/image_70.png)

![Imagen Extraída 71](images/image_71.png)

![Imagen Extraída 72](images/image_72.png)

![Imagen Extraída 73](images/image_73.png)

![Imagen Extraída 74](images/image_74.png)

![Imagen Extraída 75](images/image_75.png)

![Imagen Extraída 76](images/image_76.png)

![Imagen Extraída 77](images/image_77.png)

![Imagen Extraída 78](images/image_78.png)

![Imagen Extraída 79](images/image_79.png)

configuramos el playbook para el audio video

![Imagen Extraída 80](images/image_80.png)



![Imagen Extraída 81](images/image_81.png)

![Imagen Extraída 82](images/image_82.png)



![Imagen Extraída 83](images/image_83.png)

![Imagen Extraída 84](images/image_84.png)

![Imagen Extraída 85](images/image_85.png)



pasamos a la parte de video

![Imagen Extraída 86](images/image_86.png)

creamos un playbook para la parte de video



![Imagen Extraída 87](images/image_87.png)

![Imagen Extraída 88](images/image_88.png)



![Imagen Extraída 89](images/image_89.png)

![Imagen Extraída 90](images/image_90.png)



![Imagen Extraída 91](images/image_91.png)

![Imagen Extraída 92](images/image_92.png)

1. **Base de datos**


**3.1 Esquema entidad relación (E-R)**



Teniendo en cuenta las necesidades de la empresa, hemos creado un esquema E-R que engloba tanto el modelo de negocio de la empresa, como las necesidades de auditoría y seguridad del sistema.

![Imagen Extraída 93](images/image_93.png)

A continuación se explicará la lógica del esquema parte a parte.



**3.1.1 Core**

![Imagen Extraída 94](images/image_94.png)

El core de la base de datos son los usuarios, ya que al ser un modelo con varios core de negocio, todos se sostienen sobre sus usuarios.

Los usuarios pueden ser de 2 tipos: clientes o trabajadores, y los trabajadores cuentan con rol, departamento, y auditorías asignadas.





**3.1.2 Ventas**

![Imagen Extraída 95](images/image_95.png)

La sección de ventas engloba la los clientes únicamente, ya que las ventas están automatizadas en la web. De esta forma las ventas solo requieren del producto y los usuarios para realizarse sin dependencia de los trabajadores.







**3.1.3 Sesiones**



![Imagen Extraída 96](images/image_96.png)



La sección de sesión cubre la necesidad de la empresa para sus sesiones de formación en streaming. En dicha sección se requiere a un trabajador con el rol de tutor y a los clientes que participan en dicha sesión. Además las sesiones deben tener una formación asignada.









































**3.1.4 Intervenciones**

![Imagen Extraída 97](images/image_97.png)

La sección de intervenciones es la inferior en el esquema, y está orientada al servicio técnico de la empresa. La lógica de dicha sección se basa en el tipo de incidencias que pueden aparecer.En el esquema parece que se genera un bucle, pero realmente es un flujo para pasar de la incidencia a la intervención. Si la incidencia es de tipo externa, es porque un cliente ha llamado a servicio técnico y ha notificado una incidencia, con lo cual en la BD quedará registrada como incidencia externa con el cliente asignado, y pasará a la intervención con el técnico asignado.



Si la incidencia es interna, será algún fallo de hardware o software en el servidor, y pasará inmediatamente a la intervención con su técnico asignado.



![Imagen Extraída 98](images/image_98.png)

![Imagen Extraída 99](images/image_99.png)

![Imagen Extraída 100](images/image_100.png)

hacemos un schema para añadir todo con ansible 



![Imagen Extraída 101](images/image_101.png)

Creamos el playbook



![Imagen Extraída 102](images/image_102.png)



![Imagen Extraída 103](images/image_103.png)

creacion de usuarios con python



![Imagen Extraída 104](images/image_104.png)

creacion de un usuario

![Imagen Extraída 105](images/image_105.png)

El sistema lee correctamente el nombre de 'Alex Jitsi' desde la base de datos a través de Ansible. Sin embargo, al estar integrado el sistema con la autenticación del dominio LDAP, la conexión WebRTC no se completa debido a que se requiere una política de seguridad estricta de login con credenciales del directorio activo, provocando el rechazo de la sala anónima por defecto de Jitsi (Esteu desconnectat).



1. Conectamos todo


![Imagen Extraída 106](images/image_106.png)

![Imagen Extraída 107](images/image_107.png)

![Imagen Extraída 108](images/image_108.png)



![Imagen Extraída 109](images/image_109.png)



![Imagen Extraída 110](images/image_110.png)

![Imagen Extraída 111](images/image_111.png)

![Imagen Extraída 112](images/image_112.png)

![Imagen Extraída 113](images/image_113.png)



playbooks utilitzats en aquest projecte

![Imagen Extraída 114](images/image_114.png)





















Playbooks del servidor multimedia:

![Imagen Extraída 115](images/image_115.png)

![Imagen Extraída 116](images/image_116.png)



![Imagen Extraída 117](images/image_117.png)

![Imagen Extraída 118](images/image_118.png)

![Imagen Extraída 119](images/image_119.png)



Playbooks servidor ldap



![Imagen Extraída 120](images/image_120.png)

![Imagen Extraída 121](images/image_121.png)

![Imagen Extraída 122](images/image_122.png)





Playbooks y otros archivos utilizados para el servidor de base de datos:

![Imagen Extraída 123](images/image_123.png)

![Imagen Extraída 124](images/image_124.png)



![Imagen Extraída 125](images/image_125.png)

![Imagen Extraída 126](images/image_126.png)

![Imagen Extraída 127](images/image_127.png)

![Imagen Extraída 128](images/image_128.png)

![Imagen Extraída 129](images/image_129.png)

![Imagen Extraída 130](images/image_130.png)

![Imagen Extraída 131](images/image_131.png)

![Imagen Extraída 132](images/image_132.png)

![Imagen Extraída 133](images/image_133.png)

![Imagen Extraída 134](images/image_134.png)

![Imagen Extraída 135](images/image_135.png)

![Imagen Extraída 136](images/image_136.png)

![Imagen Extraída 137](images/image_137.png)

![Imagen Extraída 138](images/image_138.png)

![Imagen Extraída 139](images/image_139.png)

