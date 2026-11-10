Laboratorio 01 Configuración de Red LAN y Direccionamiento IP Estático

Objetivo de la Práctica: Diseñar, implementar y validar la conectividad lógica de una Red de Área Local (LAN) simple mediante la asignación estática de direcciones IPv4 y máscaras de subred, asegurando la comunicación entre múltiples dispositivos finales a través de un Switch de capa 2.

Entorno y Herramientas
Simulador: Cisco Packet Tracer.
Dispositivos de Red:
1. Switch Cisco Catalyst 2960-24TT[cite: 17].
2. 3x Estaciones de trabajo (PC0, PC1, PC2)[cite: 17].
---
Esquema de Direccionamiento IP

| Dispositivo | Dirección IP | Máscara de Subred | Gateway Predeterminado |
| :--- | :--- | :--- | :--- |
| **PC0** | `192.168.1.10` | `255.255.255.0` | `192.168.1.1` |
| **PC1** | `192.168.1.11` | `255.255.255.0` | `192.168.1.1` |
| **PC2** | `192.168.1.12` | `255.255.255.0` | `192.168.1.1` |

---

Pasos de Implementación
1. **Despliegue de Topología:** Colocación de los equipos de cómputo y el Switch central, interconectándolos mediante cables de tipo par trenzado directo (*Copper Straight-Through*).
2. **Configuración de Interfaces:** Asignación manual de las direcciones IP estáticas y la máscara de subred en la configuración de escritorio de cada PC (`Desktop > IP Configuration`)[cite: 17].
3. **Validación de Conectividad (Pruebas ICMP):** Ejecución del comando `ping` desde el símbolo del sistema (*Command Prompt*) de la PC0 hacia el resto de los nodos para verificar el éxito de la transmisión de paquetes.

---

## 📸 5. Evidencia Visual
![Topologia LAN Estatica](captura-topologia.png)
> *Figura 1: Topología lógica operando correctamente con los enlaces activos (indicadores en verde) y las direcciones IP visibles.*

---

## 💡 6. Conclusión y Análisis Técnico
* **Dominio de Difusión:** Al encontrarse todos los equipos dentro del mismo segmento de red (`192.168.1.0/24`), las tramas viajan de manera directa a través del Switch de Capa 2 sin requerir un enrutador (Router).
* **Fundamento de Ciberseguridad:** Comprender cómo interactúan los hosts en una misma LAN mediante solicitudes ARP y pings es el punto de partida fundamental para identificar flujos de red legítimos y detectar posibles anomalías o ataques de suplantación en entornos corporativos[cite: 18, 20].
