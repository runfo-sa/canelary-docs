---
sidebar_position: 1
slug: /docs/controlador/servicio
---

# Servicio

:::warning
Este servicio esta desarrollado con el software de gestión **PiQuatro** en mente.
:::

El servicio para validar el estado de etiquetas de todos los puestos productivos esta divido en 2 programas:

- [Servidor](./servidor.md), quien se comunica con las maquinas en producción para analizar en qué estado se encuentran.
- [Cliente](./cliente.md), el servicio de Windows que estará funcionando en las máquinas de producción.

Ejemplo:

|    Cliente    | Descripción                | Ultima Conexión     |
| :-----------: | :------------------------- | :------------------ |
| `192.168.X.A` | Archivos Sobrantes         | 202X-04-22 11:24:00 |
| `192.168.X.B` | Okay                       | 202X-04-22 11:49:00 |
| `192.168.X.C` | Desactualizado             | 202X-04-22 11:50:00 |
| `192.168.X.D` | Multiples Instalaciones    | 202X-04-22 11:50:00 |
| `192.168.X.E` | Desactualizado y Sobrantes | 202X-04-22 11:50:00 |
| `192.168.X.F` | Desactualizado             | 202X-04-19 16:26:00 |
| `192.168.X.G` | Archivos Sobrantes         | 202X-04-15 11:36:00 |

## Autenticación

La comunicación entre servidor-cliente es validada mediante un método de autenticación, en donde, el cliente le envía al servidor una llave privada encriptada por su llave pública, y la llave pública. Luego el servidor valida que sean las mismas llaves que el autorizo en su archivo de configuración: **Server/appsettings.json**.

Para el cliente las llaves se pueden configurar desde **C:\ProgramData\Canelary Service\config.toml**.

:::info
Para poder bajar el instalador o el cliente desde el servidor, también se necesita ingresar una clave en la URI de la siguiente forma: **http://\{hostname\}:\{port\}/instalador?key=\{clave\}**
:::
