---
sidebar_position: 2
slug: /docs/controlador/servidor
---

# Servidor

Una vez iniciado el servidor, se puede consultar las APIs disponibles mediante el enlace **http://\{hostname\}:\{port\}/swagger**.

El servidor escucha y responde a las peticiones realizada por los clientes mediante una comunicación de tipo API REST. Todo reporte de estado que es recibido por un cliente es publicado en la base de datos, en la tabla **[service].[EstadoCliente]** y es detallado en un archivo log.

:::info
Estos archivos logs se encuentran en la unidad principal **C:\ProgramData\Canelary Server**, separados en una carpeta por cliente, un archivo por día, subdivido por hora.
:::

:::info
Cualquier error interno que encuentre el servidor, es reportado en el Visor de Eventos de Windows.
:::

:::note
El servidor está limitado a solamente recibir 100 peticiones cada 10 minutos.
:::
