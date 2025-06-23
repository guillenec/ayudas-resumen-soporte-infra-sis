# Resumen Unidad 3

## 🧠 **1. ¿Qué es una red de computadoras?**

📚 *Fuente: M08-Conceptos\_Redes-1.pdf*

* Es un conjunto de dispositivos conectados entre sí para **compartir información y recursos**.
* Evolucionó desde los grandes computadores centralizados a redes distribuidas modernas (como Internet).
* Tipos de redes por alcance:

  * **LAN**: Red de área local.
  * **MAN**: Área metropolitana.
  * **WAN**: Área amplia (como Internet).

---

## 🌐 **2. Internet y Protocolos**

📚 *Fuente: Unidad-03.01-Red Internet.pdf* y M07

* **Internet**: Red global de redes interconectadas.
* **Protocolo**: Conjunto de reglas que determinan cómo se comunican los dispositivos.

  * Ej: HTTP, TCP, IP, DNS, FTP.

---

## 📶 **3. Capas del modelo OSI vs. TCP/IP**

📚 *Fuente: M09-Capas\_de\_red-1.pdf*

* **Modelo OSI** tiene 7 capas (de física a aplicación).
* **Modelo TCP/IP** tiene 4:

  * Aplicación
  * Transporte (TCP/UDP)
  * Internet (IP)
  * Enlace de datos / física

**Comparación rápida:**

| OSI             | TCP/IP           |
| --------------- | ---------------- |
| Aplicación      | Aplicación       |
| Presentación    |                  |
| Sesión          |                  |
| Transporte      | Transporte (TCP) |
| Red             | Internet (IP)    |
| Enlace de datos | Enlace de datos  |
| Física          | Física           |

---

## 🔄 **4. Tipos de comunicación**

📚 *Fuente: Unidad-03.01-Red Internet.pdf*

* **Cliente-Servidor**: Un cliente pide, un servidor responde.
* **P2P (peer-to-peer)**: Todos los nodos pueden actuar como clientes y servidores.

---

## 🚛 **5. Conmutación: cómo viajan los datos**

📚 *Fuente: M08-Conceptos\_Redes-1.pdf y Unidad-03.01-Red Internet.pdf*

* **Circuitos**: Reservan camino (como una llamada telefónica).
* **Paquetes**: Se dividen en partes, se enrutan dinámicamente. Más eficiente, aunque puede haber congestión.

---

### 🧱 **6. Capas clave: transporte, red y aplicación**

📚 *Fuente: M09 y M10*

### Capa de Transporte (TCP/UDP)

* **TCP**: Orientado a conexión, fiable (usa en web, email, etc.).
* **UDP**: No orientado a conexión, rápido pero sin garantía (usa en juegos online, streaming, DNS).

### Capa de Red (IP)

* IP = dirección lógica para ubicar un host.
* **IPv4** (ej: 192.168.1.1) y **IPv6** (más direcciones, para IoT).

### Capa de Aplicación

* Servicios como HTTP, FTP, SMTP, DNS, etc.
* Arquitecturas: cliente-servidor y P2P.
* Protocolos específicos:

  * **HTTP/HTTPS** para web.
  * **SMTP/IMAP/POP** para email.
  * **DNS** para resolver nombres.
  * **SSH/Telnet** para acceso remoto.

---

## 🔍 **7. Práctica de red (TP tuyo)**

📚 *Fuente: TP\_5-Redes-Neculqueo\_Guillermo\_Agustin.pdf*

* Usaste `ssh`, `hostname`, `ifconfig`, `netstat -rn` y `/etc/resolv.conf`.
* Analizaste IP privada/pública, máscara, MAC.
* Calculaste red usando `ipcalc`.
* Entendiste cómo funcionan router (usa IP), switch (usa MAC), y hub (no toma decisiones).
