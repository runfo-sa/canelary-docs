---
sidebar_position: 9
slug: /docs/funciones/database
---

# Versión: Database

En **Canelary** un módulo de versionado es aquel que gestiona el cómo se almacenan y controlan los archivos de etiqueta y sus diferentes versiones.

**Canelary** incluye una segunda opción de versionado además de [Git](./git.md), la cual utiliza **SQL Server** para realizar el almacenamiento y versionado.

:::tip
El módulo de versionado utilizado puede cambiarse dentro de **Settings.yaml**.
:::

Este módulo incluye su propio archivo de configuración **Version.Database.Settings.yaml**, ubicado también dentro de la carpeta **Modulos**, el cual incluye los siguientes parámetros:

- **SqlConnection**: Cadena de conexión a la base de datos.
- **Schema**: Esquema a utilizar dentro de la base de datos.

Al editar cualquier archivo se genera una nueva versión del mismo, pero para definir cuál sería la versión a utilizar en producción se debe definir desde el módulo [Publicar](./publish.md).
