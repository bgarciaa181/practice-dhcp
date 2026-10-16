Práctica DHCP

Configuración de un servidor DHCP (isc-dhcp-server) en Debian mediante Vagrant.
Datos de la red

    Servidor (srv): IP fija 192.168.57.10

    Rango dinámico: 192.168.57.20 - 192.168.57.50 (cliente c1)

    Reserva estática: 192.168.57.111 para printer según su MAC

    Opciones: Dominio yourname.test, DNS 10.0.0.2 y 4.4.4.4

Archivos

    Vagrantfile: Creación de las 3 máquinas virtuales (srv, c1, printer).

    dhcpd.conf: Configuración del servicio DHCP.

    doc/: Documentación de las pruebas realizadas.

Probar la red

En las máquinas cliente (c1 y printer):

sudo dhclient -r eth1
sudo dhclient -v eth1
