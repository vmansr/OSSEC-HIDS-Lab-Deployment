# OSSEC-HIDS-Lab-Deployment
Laboratorio de despliegue y configuración de OSSEC HIDS en entorno virtual (Ubuntu Server &amp; Desktop
# Laboratorio de Implementación OSSEC HIDS

## 📌 Descripción
Este proyecto documenta la instalación y configuración de un sistema de detección de intrusos (HIDS) utilizando **OSSEC 3.7.0**. El laboratorio consta de una arquitectura Cliente-Servidor desplegada sobre máquinas virtuales.

## 🛠️ Tecnologías utilizadas
* **Hypervisor:** VirtualBox
* **Manager:** Ubuntu Server 24.04 LTS
* **Agent:** Ubuntu Desktop 24.04 LTS
* **Lenguaje:** Bash / C (Compilación desde código fuente)

## 🚀 Desafíos Superados (Resolución de Dependencias)
Durante la compilación, se resolvieron manualmente las siguientes dependencias críticas:
* `libpcre2-dev`: Para el motor de expresiones regulares.
* `libssl-dev`: Para el cifrado de comunicaciones.
* `libsystemd-dev`: Para la integración con los servicios del sistema.

## 🛡️ Pruebas de Seguridad
Se realizó un ataque de fuerza bruta simulado (`su - root`), logrando una detección exitosa en el Manager con una regla de **Nivel 5**.


"La implementación de este laboratorio no solo demuestra la capacidad de desplegar herramientas Open Source de seguridad, sino que sienta las bases para el estudio de la seguridad proactiva. El dominio de OSSEC permite transitar desde la simple gestión de logs hacia el monitoreo de integridad y la respuesta automatizada ante incidentes, competencias críticas en la protección de activos digitales modernos."

# 🛡️ OSSEC HIDS: Implementación de Laboratorio de Seguridad Híbrido

## 🏫 Contexto Académico
Este proyecto forma parte de mi formación como estudiante de **Ingeniería Informática en la UNIR**. El objetivo principal fue diseñar, configurar e implementar un sistema de detección de intrusos basado en host (HIDS) para monitorear activos digitales en un entorno empresarial y legal.

## 📁 Descripción del Proyecto
Implementación de un entorno de seguridad utilizando **OSSEC** para centralizar la vigilancia de tres nodos distintos, logrando la detección de ataques de fuerza bruta y el monitoreo de integridad de archivos críticos.

### 🏗️ Arquitectura del Laboratorio
| Componente | Sistema Operativo | Función | IP Estática |
| :--- | :--- | :--- | :--- |
| **Manager** | Ubuntu Server | Cerebro y recolector de logs | `192.168.1.15` |
| **Agente 001** | Ubuntu Desktop | Nodo de operaciones (Víctima) | `192.168.1.X` |
| **Agente 004** | Windows 10 | Estación de trabajo (VMA Abogados) | `192.168.1.X` |

---

## 🛠️ Desafíos Técnicos Superados (Troubleshooting)

### 1. Error 1067 en Windows (Servicio OSSEC)
Uno de los mayores retos fue el fallo del servicio en Windows. Se diagnosticó que el archivo `client.keys` y el `ossec.conf` presentaban errores de permisos y codificación.
* **Solución:** Se implementó una **carpeta compartida en VirtualBox** para transferir las llaves de identidad de forma íntegra, evitando errores de transcripción manual.

### 2. Configuración de Red (Adaptador Puente)
Para garantizar la visibilidad entre el Manager y los Agentes, se configuraron las interfaces de red en modo **Bridge**, permitiendo que cada máquina virtual obtuviera una IP dentro de la subred local.

---

## 🚀 Laboratorios Ejecutados

### Lab 1: Detección de Fuerza Bruta
Se simularon múltiples intentos de acceso fallidos. OSSEC detectó el patrón de ataque y generó alertas de nivel alto en el `alerts.log` del Manager.

### Lab 2: Monitoreo de Integridad (FIM)
Se configuró el agente de Windows para vigilar la carpeta `C:\VMA_Documentos`. 
* **Resultado:** Cualquier modificación, creación o eliminación de documentos legales disparó una alerta de integridad, demostrando la capacidad de OSSEC para proteger evidencia digital.

---

## ⚖️ Aplicación Profesional
Como CEO de **VMA Abogados Asociados**, este proyecto me permite unir la ingeniería con el derecho, garantizando que la información de nuestros clientes esté protegida bajo estándares técnicos internacionales.

---

## 📚 Tecnologías Utilizadas
* **OSSEC HIDS** (Manager & Agents)
* **VirtualBox** (Virtualización)
* **Ubuntu Server / Desktop**
* **Windows 10 Pro**
* **Networking & Firewall (UFW)**

---
**Víctor Manuel Sánchez Ramírez** *Estudiante de Ingeniería Informática - UNIR* *CEO & Legal Director en VMA Abogados Asociados S.A.S.*
