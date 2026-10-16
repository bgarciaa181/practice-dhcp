# Práctica DHCP

Configuración de un servidor DHCP (`isc-dhcp-server`) en Debian mediante Vagrant[cite: 6, 7].

## Datos de la red

* **Servidor (`srv`):** IP fija `192.168.57.10`[cite: 6, 10]
* **Rango dinámico:** `192.168.57.20` - `192.168.57.50` (cliente `c1`)[cite: 10, 11]
* **Reserva estática:** `192.168.57.111` para `printer` según su MAC[cite: 13]
* **Opciones:** Dominio `yourname.test`, DNS `10.0.0.2` y `4.4.4.4`[cite: 10]

## Archivos

* `Vagrantfile`: Creación de las 3 máquinas virtuales (`srv`, `c1`, `printer`)[cite: 9, 13].
* `dhcpd.conf`: Configuración del servicio DHCP[cite: 10, 13].
* `doc/`: Documentación de las pruebas realizadas[cite: 12].

## Probar la red

En las máquinas cliente (`c1` y `printer`):

```bash
sudo dhclient -r eth1
sudo dhclient -v eth1
