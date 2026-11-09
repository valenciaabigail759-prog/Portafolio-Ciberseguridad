# 🌐 Práctica 01: Topología Básica de Red LAN en Cisco Packet Tracer

## 🎯 1. El Problema / Objetivo
Configurar y validar la conectividad en una Red de Área Local (LAN) simple mediante la asignación estática de direcciones IPv4, máscara de subred predeterminada y puerta de enlace, interconectando 3 dispositivos finales a través de un Switch de capa 2.

---

## 🛠️ 2. Herramientas y Entorno
* **Simulador:** Cisco Packet Tracer[cite: 18].
* **Dispositivos:** 
  * 1x Switch Cisco Catalyst 2960-24TT[cite: 17].
  * 3x Equipos de cómputo finales (PC0, PC1, PC2)[cite: 17].
* **Protocolos:** Ethernet, IPv4, ICMP, ARP[cite: 20].

---

## 📊 3. Esquema de Direccionamiento IP

| Dispositivo | Dirección IP | Máscara de Subred | Gateway Preddeterminado |
| :--- | :--- | :--- | :--- |
| **PC0** | `192.168.1.10` | `255.255.255.0` | `192.168.1.1`[cite: 17] |
| **PC1** | `192.168.1.11` | `255.255.255.0` | `192.168.1.1`[cite: 17] |
| **PC2** | `192.168.1.12` | `255.255.255.0` | `192.168.1.1`[cite: 17] |

---

## ⚙️ 4. Pasos Realizados
1. **Ensamblado de Topología:** Se colocaron tres estaciones de trabajo (PCs) y se conectaron mediante cables directos Ethernet (*Copper Straight-Through*) a los puertos FastEthernet del Switch 2960[cite: 17].
2. **Configuración de IP Estática:** Se ingresó a la interfaz de red de cada PC en Packet Tracer y se configuró manualmente su dirección IP dentro del segmento `192.168.1.0/24`[cite: 17].
3. **Prueba de Conectividad (ICMP):** Se ejecutó el comando `ping` desde el Command Prompt de **PC0** hacia **PC1** y **PC2** para verificar la comunicación fluida entre nodos.

---

## 📸 5. Evidencia Visual
![Topologia Basica LAN](captura-topologia.png)
> *Figura 1: Topología lógica finalizada mostrando las IPs asignadas y la señal verde de enlace activo en los puertos del Switch.*

---

## 💡 6. Conclusión y Análisis de Redes
* **Dominio de Difusión (Broadcast Domain):** Todos los equipos pertenecen al mismo segmento `/24`, lo que les permite comunicarse directamente sin necesidad de pasar por un Router.
* **Resolución ARP:** Al realizar el primer ping, los equipos utilizan el protocolo ARP para asociar las direcciones IP fijas con las direcciones MAC físicas de las tarjetas de red de las PCs[cite: 20].
* **Relevancia para Ciberseguridad:** Entender la visibilidad directa entre hosts de una misma subred es el primer paso para comprender ataques de man-in-the-middle (ARP Spoofing) y la importancia de implementar segmentación mediante VLANs[cite: 18].
