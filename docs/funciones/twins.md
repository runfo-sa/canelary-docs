---
sidebar_position: 6
---

# Backend: Twins

En **Canelary** un módulo backend es aquel que provee los productos utilizados por etiqueta, y sus parámetros.

El backend por defecto de **Canelary** es [Twins Informática - PiQuatro](https://twins.com.ar/).

:::tip
El módulo backend utilizado puede cambiarse dentro de **Settings.yaml**.
:::

En el caso de Twins, todos sus datos son obtenidos a través de SQL Server.

La lista de productos utilizado por etiqueta se obtienen mediante un Store Procedure llamado **[Twins].[ListarProductos] (@Etiqueta nvarchar)**.

Las variables disponibles y que datos obtienen cada variable se almacenan en la tabla **[Twins].[Variables]**. Que contiene dos columnas principales, el _nombre_ de la variable y la _query_ que se debe ejecutar para obtener su valor. El resultado de esa _query_ debe ser un valor escalar con el mismo nombre que la variable, ejemplo.

```
INSERT INTO [Twins].[Variables]
VALUES
(
    'Mercaderias.sCodSenasa',
    'SELECT B.sCodSenasa as [Mercaderias.sCodSenasa] FROM cte1 as A LEFT JOIN TwinsDBQuatro053.configuracion.MercaderiasFrigo as B WITH(NOLOCK) ON A.Id = B.Mercaderia_Id'
)
```
