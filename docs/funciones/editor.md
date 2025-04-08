---
sidebar_position: 2
---

# Editor

El propósito de este módulo es editar y previsualizar el diseño de las etiquetas.

<div className="text--center">
    <img src="/img/editor.png" />
</div>

## Árbol

Este árbol de archivos realiza una separación lógica entre distintos tipos de etiqueta.
En este ejemplo separa las etiquetas de caja de las primarias, y toda etiqueta que no entre en ningún criterio va a parar a la sección 'Otros'.

:::info
Para poder configurar el criterio del árbol ver [Configuración](../category/configuración/).
:::

<div className="text--center">
    <img src="/img/arbol.png" />
</div>

## Editor

Permite editar las etiquetas abiertas con el [árbol](#árbol) o independientemente de el desde _Archivos -> Abrir_.
Cuenta con soporte para abrir múltiples archivos en simultaneo, _syntax highlighting_ para el lenguaje **ZPL**, reporte de problemas en el código (**linter**), cambiar la resolución, reporte de variables faltantes y [metadata](#metadata).

### Linter

El editor ofrece la posibilidad de resaltar (subrayando en amarillo) los posibles problemas encontrados en el código de una etiqueta.

:::info
Es función del módulo de previsualización analizar y reportar al editor que problemas se encontraron.
Por defecto, **Canelary** incluye el módulo [Labelary](./labelary.md).
:::

:::tip
Esta función se puede desactivar desde _Herramientas -> Habilitar Linter_.
:::

### Metadata

El editor ofrece la posibilidad de cambiar el comportamiento de la previsualización generada mediante el uso de metadata.
Esta metadata se escribe como comentarios _(^FX \<...metadata...\>)_ en el archivo de etiqueta como en el siguiente ejemplo:

```
^FX Start Metadata#Labelary
^FX Languages:
^FX   - LanguageType: Chinese
^FX     Letter: 1
^FX ProductId: 1660
^FX End Metadata

```

La sintaxis ésta definida por una línea de inicio y una de fin, en la primer línea se especifica para que modulo de previsualización es compatible, y a continuación se definen los atributos incluidos dentro del módulo, utilizando el formato de serialización: **YAML**.

```
Start Metadata#<PreviewEngine>
    <PreviewEngine.Property>
    <PreviewEngine.Property>
    ...
End Metadata
```

### Cambiar resolución

Incluye la funcionalidad de convertir el código ZPL de una resolución a otra. Generando un nuevo archivo con la nomenclatura: **\<Nombre del Archivo\>\_\<Nueva resolución\>.\<Extensión\>**

<div className="text--center">
    <img src="/img/resolucion.png" />
</div>

### Reporte de variables faltantes

Al generar una previsualización el módulo de previsualización le pedirá al módulo backend que complete las variables encontradas en la etiqueta con los datos correspondientes. Si por algún motivo el módulo backend no pudiera completar alguna de esas variables, aparecerá un cuadro sobre el archivo indicando cuales son.

<div className="text--center">
    <img src="/img/editor_errores.png" />
</div>

:::tip
Esta función se puede desactivar desde _Herramientas -> Mostrar Errores_.
:::

## Preview

El editor ofrece la posibilidad de previsualizar el resultado final de la etiqueta, permite rotar, alejar-acercar la imagen, cambiar tamaño y dpi, renderizar archivos con múltiples etiquetas e imprimir.

:::tip
También permite generar la previsualización cada vez que se guarda el archivo desde _Herramientas -> Vista previa al guardar_.
:::
