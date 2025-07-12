# Pools & Sensors System - Node-RED Flow

Este proyecto implementa un sistema básico para gestionar dispositivos y piscinas en una aplicación relacionada con acuicultura, usando Node-RED.

## ¿Qué hace?

- Genera datos simulados para diferentes sensores (oxígeno, temperatura, pH, conductividad, turbidez, salinidad).
- Ofrece endpoints HTTP para:
  - Listar todos los dispositivos disponibles (`/available-devices`).
  - Obtener detalles de un dispositivo específico (`/device-detail?name=...`).
  - Listar las piscinas disponibles (`/available-pools`).
  - Obtener detalles de una piscina con sus sensores asociados (`/pool-detail?poolId=...`).
  - Obtener sensores asociados a una piscina específica (`/pool-devices?poolId=...`).

## Cómo usar

1. Importa este flujo en tu instancia de Node-RED (por defecto en el puerto 7400).
2. Ejecuta el flujo para que los datos simulados se generen automáticamente.
3. Accede a los endpoints mediante HTTP GET para consultar dispositivos y piscinas.

## Endpoints disponibles

- `GET /available-devices`  
  Lista todos los dispositivos (sensores y futuros dispositivos).

- `GET /device-detail?name=<device_name>`  
  Obtiene detalle de un dispositivo por su nombre.

- `GET /available-pools`  
  Lista todas las piscinas disponibles.

- `GET /pool-detail?poolId=<pool_uuid>`  
  Detalle de una piscina y sus dispositivos.

- `GET /pool-devices?poolId=<pool_uuid>`  
  Lista los dispositivos asociados a una piscina específica.
