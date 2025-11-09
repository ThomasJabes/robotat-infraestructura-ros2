# Infraestructura para Control de Enjambres Robóticos con ROS2 y MOCAP4ROS2

Este repositorio forma parte del proyecto de graduación **“Implementación de infraestructura para el control de enjambres robóticos con ROS2 y captura de movimiento dentro del ecosistema Robotat”**, desarrollado en la Universidad del Valle de Guatemala.

El objetivo del proyecto es establecer una infraestructura distribuida basada en **ROS2**, integrando el paquete **MOCAP4ROS2** con el sistema de captura de movimiento **OptiTrack**, y empleando **CrazySwarm2** y **MQTT** para la coordinación y comunicación entre agentes robóticos.

---

## Arquitectura general
<p align="center">
  <img width="900" alt="Infraestructura Robotat ROS2" src="https://github.com/user-attachments/assets/a7b8895a-c5bb-45e9-bc59-fdf6f8b8cc8e" />
</p>

1. **Captura de movimiento:** sistema OptiTrack administrado por Motive.  
2. **Transmisión de datos:** mediante los protocolos **NatNet** y **MQTT**.  
3. **Procesamiento:** en un servidor **ROS2** con el paquete **MOCAP4ROS2** dentro de un contenedor Docker.  
4. **Validación experimental:** con múltiples robots **Pololu 3pi+** sincronizados en tiempo real.

---

## Espacio de trabajo actual

Por el momento, el repositorio contiene el **entorno MQTT**, donde se gestiona la comunicación entre el sistema de captura y el servidor ROS2.  
Los demás componentes (imágenes Docker, nodos ROS2 y documentación completa) estarán disponibles próximamente.

---

## Tecnologías principales

- **ROS2 Humble**
- **MOCAP4ROS2**
- **CrazySwarm2**
- **Docker**
- **OptiTrack + Motive**
- **MQTT (mosquitto)**

---

## 📬 Contacto

> Proyecto desarrollado por **Thomas Solís**  
> Ingeniería Mecatrónica — Universidad del Valle de Guatemala  
> Año 2025

---

> **Nota:** la documentación completa y archivos complementarios estarán disponibles en el repositorio de OneDrive asociado al proyecto.

