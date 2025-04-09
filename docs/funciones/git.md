---
sidebar_position: 8
slug: /docs/funciones/git
---

# Versión: Git

En **Canelary** un módulo de versionado es aquel que gestiona el cómo se almacenan y controlan los archivos de etiqueta y sus diferentes versiones.

El versionado por defecto de **Canelary** es, [Git](https://git-scm.com/).

:::tip
El módulo de versionado utilizado puede cambiarse dentro de **Settings.yaml**.
:::

Este módulo incluye su propio archivo de configuración **Version.Git.Settings.yaml**, ubicado también dentro de la carpeta **Modulos**, el cual incluye los siguientes parámetros:

- **EtiquetasDir**: Indica en que carpeta se van a gestionar las etiquetas.
- **GitRepo**: Indica la URL del repositorio central a utilizar.

Para poder diferenciar entre versiones este módulo aprovecha de la funcionalidad de [tags en Git](https://git-scm.com/book/es/v2/Fundamentos-de-Git-Etiquetado).
Por lo cual al querer publicar los cambios con el módulo [Publicar](./publish.md), Git generara un nuevo tag.

:::tip
La nomenclatura de los tags queda a elección del usuario, pero recomendamos usar una nomenclatura como: **año.mes.dia-numerador**.
Ejemplo: **2025.04.09-03**
:::
