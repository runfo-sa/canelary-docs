---
sidebar_position: 3
---

# Comparador

El propósito de este módulo es mostrar las diferencias entre dos etiquetas, o dos versiones de la misma.

<div className="text--center">
    <img src="/img/comparador.png" />
</div>

Al iniciar nos pedirá que indiquemos las dos etiquetas a comparar y sus versiones.

<div className="text--center">
    <img src="/img/comparador_select.png" />
</div>

:::info
El tipo de versión es especificado por el módulo de versionado seleccionado.
Por defecto **Canelary** incluye un módulo de versionado integrando Git y otro como base de datos.
:::

**Canelary** realiza dos tipos de comparaciones, código e imágenes.
En el primer caso se hace una comparación línea por línea entre el código de ambas etiquetas y se muestran las modificaciones resaltándolas con colores.
Verde para líneas agregadas, rojo para líneas removidas y amarillo para líneas modificadas.

En el segundo caso se generan una previsualización de ambas etiquetas, y una muestra en el centro con solo el código diferente entre ambas etiquetas.

<div className="text--center">
    <img src="/img/comparador_imagen.png" />
</div>
