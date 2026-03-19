# Infraestructura para Control de Enjambres Robóticos con ROS2 y MOCAP4ROS2

Este repositorio forma parte del proyecto de graduación **“Implementación de infraestructura para el control de enjambres robóticos con ROS2 y captura de movimiento dentro del ecosistema Robotat”**, desarrollado en la **Universidad del Valle de Guatemala**.

El objetivo del proyecto es establecer una infraestructura distribuida basada en **ROS2**, integrando el paquete **MOCAP4ROS2** con el sistema de captura de movimiento **OptiTrack**, y empleando **CrazySwarm2** y **MQTT** para la coordinación y comunicación entre agentes robóticos.

---

## Arquitectura general

<p align="center">
  <img width="900" alt="Infraestructura Robotat ROS2" src="https://github.com/user-attachments/assets/a7b8895a-c5bb-45e9-bc59-fdf6f8b8cc8e" />
</p>

1. **Captura de movimiento:** Sistema OptiTrack administrado por Motive.  
2. **Transmisión de datos:** Mediante los protocolos **NatNet** y **MQTT**.  
3. **Procesamiento:** En un servidor **ROS2** con el paquete **MOCAP4ROS2** dentro de un contenedor Docker.  
4. **Validación experimental:** Con múltiples robots **Pololu 3pi+** sincronizados en tiempo real.

---

## Espacio de trabajo actual

Actualmente, este repositorio incluye el entorno de **comunicación MQTT**, encargado del intercambio de mensajes entre el sistema de captura de movimiento y el servidor ROS2.  
Los demás componentes —imágenes Docker, nodos ROS2 y documentación técnica— se encuentran disponibles en el siguiente enlace:

🔗 **[Repositorio general del proyecto (Google Drive)](https://drive.google.com/drive/folders/1ajJXgjBkqGwcT6tUxGNX3f0VVaDPKLEW?usp=sharing)**
Video Resumen: https://youtu.be/ge7PwUTfvk8

---

##  Tecnologías principales

- **ROS2 Humble**
- **MOCAP4ROS2**
- **CrazySwarm2**
- **Docker**
- **OptiTrack + Motive**
- **MQTT (Eclipse Mosquitto)**

---

##  Comandos Docker básicos

```bash
# Verificar imágenes disponibles
docker images

# Cargar imagen .tar exportada
sudo docker load -i crazyflie_ros2_humble.tar

# Ejecutar el contenedor
sudo docker run -it crazyflie-ros2:humble

# Reconstruir imagen si hay cambios
sudo docker build -t crazyflie-ros2:humble .
