# 🌐 Proyecto Coworking - Diseño y Segmentación de Redes

## 📄 Descripción del Proyecto

Este repositorio contiene la documentación y los archivos de simulación correspondientes a la **Actividad 1** del proyecto, cuyo objetivo es diseñar una infraestructura de red segura, escalable y de alto rendimiento para **The LED Coworking** (Madrid, Calle López de Hoyos).

El diseño se enfoca en la segmentación del tráfico mediante **VLANs** para aislar a los usuarios administrativos de los hosts generales y optimizar el rendimiento de servicios como VoIP y Wi-Fi de alta velocidad.

## 👥 Miembros del Equipo

| Nombre | Apellido |
| :--- | :--- |
| Fabio | Rieker |
| Luis | Lázaro |
| Guillermo | Gutiérrez |

***

## ⚙️ Requerimientos y Diseño

El proyecto aborda el diseño de dos redes con capacidades muy diferentes, utilizando el direccionamiento IP privado `192.168.x.x` como base:

| Requisito | Cantidad de Hosts | Direccionamiento Base | Método de Segmentación |
| :--- | :--- | :--- | :--- |
| **Red Administrativa (Red 1)** | 50 hosts | `192.168.1.0/26` | Router-on-a-Stick y VLANs básicas. |
| **Red de Usuarios (Red 2)** | 500 hosts | `192.168.2.0/23` | Diseño Jerárquico con **Switch Capa 3** y 5 VLANs. |

### Segmentación Lógica (VLANs)

Para la Red 2 (500 hosts), se implementó la siguiente estructura de VLANs:

* **VLAN 10:** Usuarios (Puestos de trabajo).
* **VLAN 20:** Administración (Personal del Coworking).
* **VLAN 30:** VoIP (Tráfico de voz con QoS).
* **VLAN 40:** Invitados (Aislamiento de la red principal).
* **VLAN 99:** Gestión (Administración remota del hardware).

***

## 📁 Estructura del Repositorio

| Archivo/Carpeta | Contenido |
| :--- | :--- |
| `README.md` | Este documento de introducción. |
| `Red1_50hosts.pkt` | Simulación de la Red 1 en Packet Tracer (Router-on-a-Stick). |
| `Red2_500hosts.pkt` | Simulación de la Red 2 en Packet Tracer (Switch Capa 3/Inter-VLAN Routing). |
| `GrupoX_Actividad1_FabioRieker.pdf` | **Documento de Entrega Final (PDF).** |

***

## 🛠️ Herramientas Utilizadas

* **Cisco Packet Tracer (PT):** Software utilizado para el diseño, simulación y prueba de la conectividad de las redes.
* **Git / GitHub:** Plataforma utilizada para el control de versiones y la entrega del proyecto.

***

## 🔗 Enlace al Documento de Entrega

El desarrollo teórico, los cálculos de *subnetting* y el análisis de resultados se encuentran detallados en el documento PDF de la entrega. El repositorio es la prueba de la simulación práctica.
