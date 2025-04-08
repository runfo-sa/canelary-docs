---
sidebar_position: 4
---

# Verificador

El propósito de este módulo es asegurarnos que los datos utilizados en las etiquetas estén cargados correctamente.

<div className="text--center">
    <img src="/img/verificador.png" />
</div>

Cada etiqueta tiene asignada N cantidad de productos, cada uno de esos productos deben tener correctamente cargadas las variables que la etiqueta vaya a utilizar. En caso de encontrarse algún problema se resaltaran con naranja las variables por producto que están mal cargadas, y con rojo las variables que todavía no fueron parametrizadas.

Ahora, como definimos que variables deben ser observadas para cada etiqueta? Para eso **Canelary** incluye un sistema de reglas. Estas reglas incluyen los atributos a considerar y que valores podrían contener. Una regla se puede aplicar a una o varias etiquetas.

:::info
Estos atributos son proporcionados por el módulo de backend seleccionado.
:::

## Como crear una regla

Para poder crear una regla tenemos que ir al menú _Reglas -> Crear Regla_.
En esta ventana indicamos el nombre, etiqueta, descripción (opcional) y que atributos se deben analizar.

<div className="text--center">
    <img src="/img/crear_regla.png" />
</div>

Para cada atributo hay que especificar la variable a analizar, y en caso de que el valor deba respetar alguna norma se puede definir un **valor fijo** que puede ser una constante o una cadena regex.

En caso de ue se quiera aplicar esta regla a otra etiqueta, abajo de la lista de productos se encuentra la siguiente barra, donde podemos ver que regla está actualmente aplicada para esta etiqueta. Podemos cambiar (o remover) la regla aplicada haciendo click en el librito a la derecha.

<div className="text--center">
    <img src="/img/cambiar_regla.png" />
</div>

:::tip
Para poder modificar una regla se debe acceder al menú _Reglas -> Modificar Regla_.
Seleccionamos la regla a modificar y ahí podemos cambiar los atributos o la descripción.
:::

## Generar Muestra

Para los productos de una etiqueta que estén libres de errores, **Canelary** te permite generar una muestra de esos productos.
Para eso basta con seleccionar esa opción, marcar los productos a imprimir y seleccionar la impresora deseada.

<div className="text--center">
    <img src="/img/muestra.png" />
</div>

## Generar Reporte

:::warning
TODO!
:::
