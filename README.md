# 🛡️ Análisis Forense de Red: Detección de ARP Spoofing

![Wireshark](https://img.shields.io/badge/Wireshark-205C85?style=for-the-badge&logo=wireshark&logoColor=white)
![Forensics](https://img.shields.io/badge/Network_Forensics-3C3C3C?style=for-the-badge&logo=linux&logoColor=white)
![SOC](https://img.shields.io/badge/SOC-Analyst-B80000?style=for-the-badge)
![Linux](https://img.shields.io/badge/Linux-34A853?style=for-the-badge&logo=linux&logoColor=black)
![Proxmox](https://img.shields.io/badge/Proxmox-E57000?style=for-the-badge&logo=proxmox&logoColor=white)

Análisis forense de tráfico de red orientado a la detección de actividades sospechosas, utilizando técnicas de inspección ARP e indicadores clave para identificar un ataque activo.

---

## 📄 Descripción

Este análisis forense documenta la detección e investigación de un ataque de **ARP Spoofing** e **IP Spoofing** dentro de un entorno controlado.  
Se emplearon filtros especializados de Wireshark para identificar al atacante, validar patrones anómalos y correlacionar eventos.

---

## 🔍 Hallazgos Principales

### 🎯 Identificación del atacante
• **MAC Address:** `bc:24:11:52:16:9a`  
• **Sistema operativo:** Linux  
• **Host:** `ProxmoxServe`

### 🔧 Técnicas de análisis
Filtros clave utilizados en Wireshark:
- `arp.duplicate-address-detected`
- `arp.opcode == 1` / `arp.opcode == 2`
- `eth.addr == <MAC>`
- `ip.ttl == 64`

### ⚠️ Evidencias del ataque
• Asociación de múltiples IP a una misma MAC (envenenamiento ARP)  
• Suplantación de IP pública: **8.8.8.8**  
• TTL característico de sistemas Linux (64)

---

## 🎯 Objetivos del Análisis

• Detectar intento de envenenamiento ARP mediante técnicas de monitoreo pasivo  
• Identificar atributos del atacante a partir del tráfico capturado  
• Utilizar evidencia técnica concreta para sustentar la conclusión forense  

---

## 📌 Conclusión

El análisis confirma un caso de **ARP Spoofing** apoyado por **IP Spoofing**, donde el atacante utilizó un sistema Linux virtualizado en Proxmox para manipular la resolución de direcciones en la red.

---

## 📬 Contacto

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/ingrid-k)  
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:ingridkaufmannok@gmail.com)
