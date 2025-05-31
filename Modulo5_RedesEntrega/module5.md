# Módulo 5 - Redes y entrega de contenido
Texto

---

## 📌 Temas

- Conceptos básicos de las redes
- Amzon VPC
- Redes de VPC
- Seguridad de VPC
- Route S3
- CloudFront

---

## Sección 1: **Conceptos básicos de las redes**
### **🔌 ¿Qué es una red?**
Una red informática conecta dos o más máquinas (clientes) para compartir recursos.
- Las redes pueden dividirse lógicamente en subredes.
- Requieren dispositivos de red como enrutadores o switches para permitir la comunicación entre clientes.

### **🌐 Dirección IP**
Cada dispositivo en una red tiene una dirección IP única (formato decimal).
- Se compone de 4 números separados por puntos (IPv4).
- Cada número puede ir de 0 a 255 (representa 8 bits → 1 byte).
- Ejemplo: 192.0.2.0 equivale en binario a:
  - 11000000 . 00000000 . 00000010 . 00000000

### **📏 IPv4 vs IPv6**
- IPv4: 32 bits → formato clásico, limitado en cantidad.
- IPv6: 128 bits → diseñado para una mayor cantidad de dispositivos.
  - Ejemplo IPv6: 2600:1f18:22ba:8c00:ba86:a05e:a5ba:00F
  - Compuesto por 8 grupos de 4 caracteres hexadecimales (16 bits cada uno).
  - Soporta ≈ 340 undecillones de direcciones únicas.

### **📶 CIDR – Enrutamiento sin clases**
CIDR (Classless Inter-Domain Routing) permite definir la porción de red y de host en una dirección IP:
- Sintaxis: Dirección IP / número de bits de red
- Ejemplo: 192.0.2.0/24 → los primeros 24 bits son de red, los otros 8 bits son para hosts.
  - Permite 2⁸ = 256 direcciones.
- Si fuese 192.0.2.0/16, se podrían usar 2¹⁶ = 65,536 direcciones (más flexibilidad).

### **🧱 Modelo OSI (Interconexión de Sistemas Abiertos)**
Modelo conceptual con 7 capas que explica cómo viajan los datos en la red:

| Capa         | Nº | Función Principal                     | Protocolos / Direcciones |
| ------------ | -- | ------------------------------------- | ------------------------ |
| Aplicación   | 7  | Acceso a aplicaciones de red          | HTTP/S, FTP, DHCP        |
| Presentación | 6  | Formato y cifrado de datos            | ASCII, ICA               |
| Sesión       | 5  | Manejo de sesiones entre aplicaciones | NetBIOS, RPC             |
| Transporte   | 4  | Entrega confiable entre host          | TCP, UDP                 |
| Red          | 3  | Enrutamiento y direcciones IP         | IP                       |
| Enlace       | 2  | Transferencia en redes LAN            | MAC                      |
| Física       | 1  | Transmisión de bits físicos           | Señales, cables          |

- Enrutadores operan en capa 3 (Red).
- Switches y hubs operan en capa 2 (Enlace de datos)
- AWS también usa este modelo para crear redes virtuales (como las VPC).

---

## Sección 2: **Amzon VPC**
### **🌐 ¿Qué es Amazon VPC?**
Amazon VPC (Virtual Private Cloud) te permite aprovisionar una red privada virtual en la nube de AWS.
- Es una sección aislada lógicamente, donde puedes lanzar recursos como EC2.
- Puedes definir rango IP, subredes, reglas de seguridad, tablas de enrutamiento.

### **🧱 Componentes clave de una VPC**
- Direcciones IP privadas: cada VPC necesita un bloque de direcciones IPv4 (CIDR).
- Subredes: divisiones lógicas dentro de la VPC, pueden ser:
  - Públicas: con acceso a Internet.
  - Privadas: sin acceso a Internet.
- Seguridad: mediante grupos de seguridad (SG) y listas de control de acceso (ACL).
- Tablas de enrutamiento: definen hacia dónde va el tráfico.

### **📍 Dirección IP y Subredes**
- Un bloque CIDR define el rango IP de tu VPC. Ejemplo: 10.0.0.0/16 → 65,536 IPs.
- Subredes más pequeñas como 10.0.0.0/24 → 256 IPs, de las cuales:
  - Solo 251 IPs están disponibles (5 reservadas por AWS).

### **🚦 Tipos de IP públicas**
- IPv4 pública:
  - Se asigna manualmente o de forma automática.
- IP elástica (EIP):
- Se asocia a tu cuenta de AWS.
- Puede reasignarse.
- Tiene costos adicionales si no se utiliza.

### **🔌 Interfaz de red elástica (ENI)**
- Es una tarjeta de red virtual que puedes conectar/desconectar de una instancia.
- Cada ENI tiene:
  - Una IP principal.
  - Una dirección MAC.
  - Se puede mover entre instancias.

### **🛣️ Tablas de enrutamiento**
- Son conjuntos de reglas (rutas) que indican hacia dónde debe ir el tráfico.
- Cada subred debe estar asociada a una tabla de rutas.
- Hay una tabla predeterminada para cada VPC con una ruta local (10.0.0.0/16 → local).

---

## Sección 3: **Redes de VPC**


---

## Sección 4: **Seguridad de VPC**

---

## Sección 5: **Route S3**

---

## Sección 6: **CloudFront**
