---
sidebar_position: 4
---

# Configuración

En la carpeta raíz de **Canelary**, se encuentra el archivo Settings.yaml, el cual contiene todos los parámetros configurables del sistema.

**SqlConnection**: Cadena de conexión con la base de datos SQL Server.

**ReportTemplate**: Dirección absoluta a la plantilla utilizada para generar un reporte de cambios.

**Theme**: Tema del editor, posibles modos: Dark, Light.

**Culture**: Región a usar por el programa, para darle formato a las fechas y números.

**Extension**: Extensión de los archivos de etiqueta, esto puede ser una simple extensión o una lista de extensiones.

```
Extension: "zpl"

Extension:
  - "e01"
  - "e02"
  - "zpl"
```

**VirtualDirectories**: Lista de directorios virtuales, con los cuales se genera la jerarquía de etiquetas.

```
VirtualDirectories:
  - Name: "Caja"
    Filter: "CAJA"
  - Name: "Primaria"
    Filter: "PRIMARIA"
```

**Preview**: Servicio responsable de generar una previsualización digital de la etiqueta seleccionada.

**Backend**: Servicio encargado de proporcionar los datos necesarios para completar las variables encontradas en las etiquetas con datos reales.

**Version**: Servicio que administra el sistema de control de versionado a utilizar.

**Modules**: Lista de módulos disponibles en el sistema.

```
Modules:
  - Name: "Editar"
    Icon: FileEdit
  - Name: "Comparar"
    Icon: Compare
  - Name: "Verificar"
    Icon: NotebookCheck
  - Name: "Publicar"
    Icon: Publish
```

:::info
Los valores por defecto se pueden ver desde el repositorio: [Settings.yaml](https://github.com/runfo-sa/canelary/blob/canelary/Main/settings.yaml).
:::
