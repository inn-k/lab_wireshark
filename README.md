# 🛡️ LAB: Análisis forense de red | Detección de ARP spoofing

![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![Networking](https://img.shields.io/badge/Networking-008CFF?style=for-the-badge&logo=cisco&logoColor=white)
![Security](https://img.shields.io/badge/Blue_Team-101345?style=for-the-badge&logo=hackthebox&logoColor=white)
![Wireshark](https://img.shields.io/badge/Wireshark-1679A7?style=for-the-badge&logo=wireshark&logoColor=white)
![SOC](https://img.shields.io/badge/SOC-171434?style=for-the-badge)
![Ubuntu](https://img.shields.io/badge/Ubuntu-e95420?style=for-the-badge&logo=ubuntu&logoColor=white)
![Proxmox](https://img.shields.io/badge/Proxmox-e57000?style=for-the-badge&logo=proxmox&logoColor=white)

---

## 🌟 Descripción

Análisis forense que documenta la detección e investigación de un ataque de **ARP Spoofing** e **IP Spoofing** dentro de un entorno controlado.  
Se emplearon filtros especializados de Wireshark para identificar al atacante, validar patrones anómalos y correlacionar eventos.

---

## 📁 Hallazgos

**Identificación del atacante** \
• MAC Address: `bc:24:11:52:16:9a`  
• Sistema operativo: Linux  
• Host: `ProxmoxServe`

**Técnicas de análisis** \
Filtros clave utilizados en Wireshark:
- `arp.duplicate-address-detected`
- `arp.opcode == 1` / `arp.opcode == 2`
- `eth.addr == <MAC>`
- `ip.ttl == 64`

**Evidencias del ataque** \
• Asociación de múltiples IP a una misma MAC (envenenamiento ARP).  
• Suplantación de IP pública: **8.8.8.8**.  
• TTL característico de sistemas Linux (64).

---

## 🎯 Objetivos

• Detectar intento de envenenamiento ARP mediante técnicas de monitoreo pasivo.  
• Identificar atributos del atacante a partir del tráfico capturado.  
• Utilizar evidencia técnica concreta para sustentar la conclusión forense.  

---

## 📬 Contacto

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/ingrid-k)  
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:ingridkaufmannok@gmail.com)
