---
sidebar_position: 7
slug: /docs/funciones/labelary
---

# Preview: Labelary

En **Canelary** un módulo preview es aquel que en base al código fuente en ZPL genera una previsualización de la etiqueta.

La preview por defecto de **Canelary** es, [Labelary](https://labelary.com/viewer.html).

:::tip
El módulo preview utilizado puede cambiarse dentro de **Settings.yaml**.
:::

El comportamiento del módulo preview puede ser alterado por etiqueta utilizando un bloque de código como metadata, ver [Editor - Metadata](./editor.md#metadata).

**Labelary** incluye 2 tipos de parámetros dentro de su metadata.

1. Una lista de lenguajes, indicando de que tipo son y que letra remplazarían en el comando ^A. Con esto se podría renderizar una preview que soporte caracteres especiales.
   La lista de lenguajes disponibles es:
   - Chinese
   - Japanese
   - Korean
   - Cyrillic
   - Greek
   - Arabic
2. La id del producto, con esto se generará una preview en la cual se reemplazarían todas las variables con los datos del producto procedentes del módulo backend.

Ejemplo:

```
^FX Start Metadata#Labelary
^FX Languages:
^FX   - LanguageType: Chinese
^FX     Letter: 1
^FX ProductId: 1660
^FX End Metadata
```
