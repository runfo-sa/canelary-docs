---
sidebar_position: 3
slug: /docs/controlador/cliente
---

# Cliente

:::warning
La primera vez que se ejecuta el servicio realizara un análisis para encontrar **PiQuatro**, en caso de no encontrarlo o encontrar múltiples, el cliente enviara el reporte al servidor y finalizara.
:::

El servicio de cliente realiza tres tipos de análisis diarios:

1.  Envía al servidor una lista de etiquetas encontradas en PiQuatro, indicando nombre y hash. Esto se realiza cada N minutos, donde N es un valor configurable, por defecto '180' minutos.
2.  Reporta al servidor si se encontró más de una, o ninguna, instalación de PiQuatro en el sistema. Para mejorar el rendimiento de este análisis, solamente se realiza la búsqueda en una unidad de disco configurable, por defecto en 'C:'. Este análisis se realiza a una cierta hora del día, también configurable.
3.  Consulta al servidor si hay alguna actualización del cliente pendiente, en caso de haberla el mismo servicio realizara la actualización. Esta consulta también se realiza a una cierta hora del día configurable.

:::info
El archivo de configuración se encuentra en la unidad principal **C:\ProgramData\Canelary Service\config.toml**.
:::

Junto al archivo de configuración se encuentra la carpeta '**Logs**', todo error que encuentre el servicio será reportado ahí, separado en un archivo por día, subdividido por hora.
