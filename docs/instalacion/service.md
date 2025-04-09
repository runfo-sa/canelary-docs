---
sidebar_position: 2
slug: /docs/instalacion/service
---

# Instalar Controlador

Enlace de descarga: https://github.com/runfo-sa/visual-ternera-servicio/releases

El servicio para controlar el estado de etiqueta en los puestos está dividido en dos aplicaciones.

Un servidor web API y un servicio de Windows que reporta al servidor su estado de etiquetas cada cierto tiempo.

Por eso el proceso de instalación está dividido en dos partes:

- [Instalar Servidor](#instalar-servidor)
- [Instalar Cliente](#instalar-cliente)

## Instalar Servidor

### Preparar el servidor

Copiar la carpeta **Servidor** a la carpeta que lee el servicio http elegido.
Un servicio http recomendado es [IIS de Microsoft](https://learn.microsoft.com/es-mx/iis/get-started/introduction-to-iis/iis-web-server-overview).
Enlace a como crear un sitio web con IIS: [Crear un Sitio web](https://learn.microsoft.com/es-es/iis/get-started/getting-started-with-iis/create-a-web-site).

Y configurar las claves en **appsettings.json**.

### Preparar la base de datos

1. Para conectar el servidor con la base de datos se debe ejecutar el script **deploy_VSTS.sql**, el cual crea la base de datos y las tablas necesarias para que funcione el servidor.
2. Modificar la cadena de conexión **DefaultConnection** dentro del archivo **appsettings.json** dentro de la carpeta raíz del servidor.
3. Crear un usuario para el servidor dentro de la instancia de SQL Server y asignarle el rol **vsts_server**.

## Instalar Cliente

El servidor ofrece un enlace para descargar el instalador para los clientes, el enlace seria **http://\{hostname\}:\{port\}/instalador?key=\{llave\}**

El instalador es un Powershell script llamado **installer.ps1**, para poder instalarlo debe ser ejecutado como Administrador y el script se encargará de crear e iniciar el servicio.
