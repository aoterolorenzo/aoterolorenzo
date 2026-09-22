# RianxoSenCabos

- **Dates:** 2006 → 2015
- **Role:** Responsable de redes y sistemas, voluntario
- **Stack:** OpenWRT, FreeRADIUS, MySQL, PHP, Debian, Postfix, Dovecot

![Members portal](../img/portal.png)

Una asociación sin ánimo de lucro de redes inalámbricas que llevó internet a zonas rurales sin infraestructura pública. Llegó a ser una red de área metropolitana de más de 100 km², dando servicio de ISP a más de 50 socios con un 97% de disponibilidad durante nueve años.

Diseñé y construí la mayor parte de su software y sus servidores:

- Un OpenWRT personalizado en los puntos de acceso con un portal cautivo Coova, respaldado por FreeRADIUS sobre MySQL.
- Un portal de socios con inicio de sesión único para todos los servicios, además de pagos automáticos con PayPal.
- Un panel de administración que leía los puntos de acceso cada minuto (señal, ruido, dispositivos conectados, ancho de banda) y nos permitía gestionar a cada socio.
- Una red social autoalojada (Diaspora), servidor de correo con webmail, 50 GB de almacenamiento en la nube por socio (ownCloud) y un servidor de streaming.
- Un servidor Debian con RAID 10 y tres redes, y un servidor de backup en una segunda ubicación con su propia conexión.

![Access point status](../img/estadoaps2.png)
