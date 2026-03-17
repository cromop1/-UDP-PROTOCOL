
<p align="center">
  <img src="https://i.imgur.com/jaVUqG3.png" width="100%" alt="banner principal ">
</p>
<p align="center">
  <img src="https://i.imgur.com/RVGaecC.png" width="100%" alt="Banner Proyecto Integrador 2025">
</p>

<p align="center">
  <!-- UDP principal - color azul clásico de protocolos de red -->
  <img src="https://img.shields.io/badge/UDP-User%20Datagram%20Protocol-007ACC?style=for-the-badge&logo=udacity&logoColor=white" />
  
  <!-- Variante simple y limpia -->
  <img src="https://img.shields.io/badge/Protocol-UDP-00A3E0?style=for-the-badge&logo=fastly&logoColor=white" />
  
  <!-- Con logo de red genérico (usando cloudflare como proxy de red) -->
  <img src="https://img.shields.io/badge/UDP-Transport-1E90FF?style=for-the-badge&logo=cloudflare&logoColor=white" />
  
  <!-- TCP para comparación -->
  <img src="https://img.shields.io/badge/TCP-Transmission%20Control%20Protocol-006400?style=for-the-badge&logo=tcp&logoColor=white" />
  
  <!-- IP (capa inferior) -->
  <img src="https://img.shields.io/badge/IP-Internet%20Protocol-8A2BE2?style=for-the-badge&logo=ipfs&logoColor=white" />
  
  <!-- DNS (usa UDP comúnmente) -->
  <img src="https://img.shields.io/badge/DNS-Domain%20Name%20System-FFD700?style=for-the-badge&logo=googlechrome&logoColor=black" />
  
  <!-- QUIC (moderno, sobre UDP) -->
  <img src="https://img.shields.io/badge/QUIC-Quick%20UDP%20Internet%20Connections-4285F4?style=for-the-badge&logo=google&logoColor=white" />
  
  <!-- Networking general -->
  <img src="https://img.shields.io/badge/Networking-TCP%2FIP%20%26%20UDP-FF4500?style=for-the-badge&logo=nginx&logoColor=white" />
  
  <!-- Capa de Transporte -->
  <img src="https://img.shields.io/badge/Transport%20Layer-UDP%20%2F%20TCP-32CD32?style=for-the-badge&logo=apache&logoColor=white" />
  
  <!-- Wireshark (herramienta para ver UDP) -->
  <img src="https://img.shields.io/badge/Wireshark-UDP%20Analysis-1679A7?style=for-the-badge&logo=wireshark&logoColor=white" />
</p>
<p align="center">
  <img src="https://i.imgur.com/RVGaecC.png" width="100%" alt="Banner Proyecto Integrador 2025">
</p>


# Protocolo UDP 

## 1. Introducción: ¿Por qué necesitamos protocolos en redes?

En el mundo actual, **todo dispositivo conectado** (PC, móvil, servidor, consola, smart TV) intercambia datos constantemente:

- Abrir una web → HTTP/HTTPS  
- Enviar un mensaje de voz o video → Apps de mensajería  
- Videollamada → Zoom, Teams, Discord  
- Jugar online → Fortnite, Valorant, FIFA  

Para que esta comunicación funcione entre dispositivos de **diferentes marcas y sistemas operativos**, se necesitan **reglas universales**: los **protocolos de red**.

**Analogía simple**:  
Un protocolo es como un **idioma común**. Si todos hablan el mismo idioma, la conversación fluye sin problemas. Si cada uno usa un idioma diferente → imposible entenderse.

Sin protocolos → Internet no funcionaría como lo conocemos.


<p align="center">
  <img src="https://i.imgur.com/zDTIHyR.png" width="100%" alt="Banner Proyecto Integrador 2025">
</p>

## 2. ¿Qué es exactamente un protocolo?

Conjunto estandarizado de reglas que definen:

- Cómo **iniciar** la comunicación  
- Cómo **formatear** y **encapsular** los datos  
- Cómo **detectar** errores (o decidir no hacerlo)  
- Cómo **finalizar** la comunicación  

**Ejemplos clave**:
- TCP y UDP → Capa de transporte  
- IP → Capa de red  
- HTTP/HTTPS, DNS → Capa de aplicación  

<p align="center">
  <img src="https://i.imgur.com/zDTIHyR.png" width="100%" alt="Banner Proyecto Integrador 2025">
</p>

## 3. Protocolos vs. Atributos (clave para comparar)

| Concepto     | Definición                                      | Ejemplos                              |
|--------------|-------------------------------------------------|---------------------------------------|
| **Protocolo** | Conjunto completo de reglas                     | TCP, UDP, QUIC, HTTP, DNS             |
| **Atributo**  | Característica o propiedad del protocolo        | Velocidad, confiabilidad, latencia, consumo de recursos |

**Ejemplo práctico**:  
- Un protocolo puede priorizar **velocidad** (UDP)  
- Otro prioriza **confiabilidad total** (TCP)




<p align="center">
  <img src="https://i.imgur.com/zDTIHyR.png" width="100%" alt="Banner Proyecto Integrador 2025">
</p>

## 4. Capa de Transporte en el modelo TCP/IP

La capa de transporte se encarga de:

- Dividir datos en paquetes o datagramas  
- Enviarlos al puerto correcto del dispositivo destino  
- (En algunos casos) asegurar entrega y orden  

**Protocolos principales**:
- **TCP** (Transmission Control Protocol)  
- **UDP** (User Datagram Protocol)  
- **QUIC** (Quick UDP Internet Connections) → moderno, basado en UDP  








<p align="center">
  <img src="https://i.imgur.com/zDTIHyR.png" width="100%" alt="Banner Proyecto Integrador 2025">
</p>

## 5. Comparación técnica: TCP vs UDP vs QUIC

| Característica              | TCP                          | UDP                          | QUIC (sobre UDP)             |
|-----------------------------|------------------------------|------------------------------|------------------------------|
| Orientado a conexión        | Sí (3-way handshake)         | No                           | Sí (pero más rápido)         |
| Confiabilidad (entrega)     | Alta (ACK + retransmisión)   | Ninguna                      | Alta                         |
| Orden de paquetes           | Garantizado                  | No garantizado               | Garantizado                  |
| Control de congestión       | Sí                           | No                           | Sí (mejorado)                |
| Latencia                    | Media-Alta                   | Muy baja                     | Baja                         |
| Velocidad                   | Media                        | Muy alta                     | Alta                         |
| Overhead (tamaño cabecera)  | 20–60 bytes                  | 8 bytes                      | Variable (eficiente)         |
| Uso principal               | Web, email, descargas        | Juegos, streaming, DNS, VoIP | HTTP/3 (web moderna)         |








<p align="center">
  <img src="https://i.imgur.com/zDTIHyR.png" width="100%" alt="Banner Proyecto Integrador 2025">
</p>

## 6. Protocolo UDP en detalle

**UDP = User Datagram Protocol**  
Protocolo de transporte **sin conexión** y **no confiable** (best-effort delivery).

**Cabecera UDP** (solo **8 bytes** – extremadamente ligera):

| Campo              | Tamaño    | Descripción                                      |
|--------------------|-----------|--------------------------------------------------|
| Puerto origen      | 16 bits   | Puerto de la aplicación que envía                |
| Puerto destino     | 16 bits   | Puerto de la aplicación que recibe               |
| Longitud           | 16 bits   | Tamaño total (cabecera + datos)                  |
| Checksum           | 16 bits   | Verificación opcional de integridad              |

**Proceso de envío (muy sencillo)**:

1. La aplicación genera los datos  
2. UDP los encapsula en **datagramas**  
3. Los envía directamente a la IP:puerto destino  
4. No espera confirmación ni reenvía nada  
5. El receptor entrega los datagramas a la aplicación (si llegan)  

→ **Mínimo procesamiento** → **máxima velocidad** y **latencia mínima**


<p align="center">
  <img src="https://i.imgur.com/zDTIHyR.png" width="100%" alt="Banner Proyecto Integrador 2025">
</p>



## 7. Usos reales de UDP (donde destaca)

UDP es ideal cuando la **velocidad y la baja latencia** son prioritarias:

- **Videojuegos online** (Fortnite, Call of Duty, Valorant): posición de jugadores, movimientos, disparos → la info se actualiza constantemente, perder algún paquete no rompe la experiencia  
- **Streaming de video y audio en vivo** (Twitch, YouTube Live): fluidez del video > perfección absoluta  
- **DNS** (consultas de nombres de dominio → puerto 53/UDP): respuestas ultrarrápidas  
- **VoIP y llamadas** (WhatsApp, Discord, Zoom audio): voz en tiempo real sin retrasos notables  
- **DHCP** (asignación automática de IP al conectar a la red)  
- **Protocolos de descubrimiento** (mDNS para Bonjour/Apple, SSDP para dispositivos UPnP)






<p align="center">
  <img src="https://i.imgur.com/zDTIHyR.png" width="100%" alt="Banner Proyecto Integrador 2025">
</p>


## 8. Ventajas y desventajas técnicas de UDP

**Ventajas**  
- Velocidad de transmisión muy alta  
- Latencia extremadamente baja  
- Bajo consumo de CPU y ancho de banda  
- Simplicidad → cabecera pequeña y procesamiento mínimo  
- Perfecto para aplicaciones en tiempo real  

**Desventajas**  
- No garantiza que los paquetes lleguen  
- No garantiza el orden de llegada  
- La aplicación debe manejar pérdidas o desorden (si es necesario)  

<p align="center">
  <img src="https://i.imgur.com/zDTIHyR.png" width="100%" alt="Banner Proyecto Integrador 2025">
</p>

# RESUMEN RAPIDO MODELO OSI :

<p align="center">
  <img src="https://i.imgur.com/9bKCuNx.png" width="100%" alt="Banner Proyecto Integrador 2025">
</p>
