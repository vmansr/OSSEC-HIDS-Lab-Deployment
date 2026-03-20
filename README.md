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
