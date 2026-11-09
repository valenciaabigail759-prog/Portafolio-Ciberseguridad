# 🐉 Laboratorio 01: Escaneo de Red con Nmap (Kali Linux)

## 📌 1. Objetivo del Laboratorio
Identificar puertos abiertos y servicios activos en un segmento de red local mediante escaneos con Nmap en Kali Linux.

---

## 🛠️ 2. Herramientas Utilizadas
* **Sistema Operativo:** Kali Linux (Máquina Virtual)
* **Herramientas:** Nmap, Terminal de Linux

---

## ⚙️ 3. Comandos Ejecutados y Procedimiento
1. Escaneo rápido de detección de host:
   `nmap -sn 192.168.1.0/24`
2. Escaneo de puertos y detección de versiones:
   `nmap -sV -sC 192.168.1.15`

---

## 📸 4. Evidencia Visual
*(Arrastra y suelta aquí tu captura de pantalla de la terminal de Kali Linux)*

---
> **Conclusión:** Se identificaron exitosamente los puertos web HTTP (80) y SSH (22) abiertos en el objetivo.
