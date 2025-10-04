# 🛡️ Análisis Forense de Red: Detección de ARP Spoofing

![Wireshark](https://img.shields.io/badge/Wireshark-2A0?style=for-the-badge&logo=wireshark&logoColor=white)
![Forensics](https://img.shields.io/badge/Network-Forensics-blue?style=for-the-badge)
![SOC](https://img.shields.io/badge/SOC-Analyst-red?style=for-the-badge)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![Proxmox](https://img.shields.io/badge/Proxmox-E57000?style=for-the-badge&logo=proxmox&logoColor=white)

## 📄 Descripción

El documento presenta un análisis forense de tráfico de red donde se identifica y documenta un ataque de **ARP Spoofing** y **IP Spoofing**.

## 🔍 Hallazgos Principales

### 🎯 Identificación del Atacante
- **MAC Address del atacante**: `bc:24:11:52:16:9a`
- **Sistema Operativo**: Linux
- **Host identificado**: ProxmoxServe

### 🔧 Técnicas de Análisis
- **Filtros Wireshark utilizados**:
  - `arp.duplicate-address-detected` - Para detectar IPs duplicadas
  - `arp.opcode == 1` - Solicitudes ARP
  - `arp.opcode == 2` - Respuestas ARP  
  - `eth.addr == MAC` - Filtrado por dirección MAC específica
  - `ip.ttl == 64` - Identificación de TTL característico de Linux

### ⚠️ Evidencia de Ataque
- **ARP Spoofing**: Múltiples IPs asociadas a la misma MAC
- **IP Spoofing**: Suplantación de IP pública (8.8.8.8)
- **TTL Analysis**: Valor de 64 confirmando sistema Linux/Unix

## 🎯 Objetivos del Análisis

- Demostrar técnicas de detección de ataques de envenenamiento ARP
- Identificar atributos clave del atacante (MAC, SO, método de ataque)
- Utilizar evidencia concreta y filtros de Wireshark para sustentar las conclusiones

## 📌 Conclusión

Se confirma un intento de **ARP Spoofing** mediante la duplicación de direcciones IP y el uso de **IP Spoofing**, donde el atacante utilizó una máquina Linux (posiblemente una máquina virtual Proxmox) para suplantar identidades en la red.

---

## 👩‍💻 Autora

**Ingrid K.**  

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/ingrid-k)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:ingridkaufmannok@gmail.com)
