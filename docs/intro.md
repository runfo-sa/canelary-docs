---
sidebar_position: 1
---

# Introdución
#### Canelary es una herramienta para la creación, edición y validación de etiquetas para el lenguaje de programación de Zebra, ZPL.

## Funciones

### Controlador de puestos
Canelary ofrece un sistema para controlar el estado de etiquetas en todos los puesto de producción. Para ello cuenta con un servicio instalable en los puestos y una Web API para reportar el estado de los puestos.

### Modificación de etiquetas
Canelary permite la creación y edición de etiquetas, incluye un editor con soporte para editar múltiples etiquetas en simultaneo, crear una imagen que muestre el resultado preliminar de la etiqueta, soporte para imprimir las etiquetas y un arbol logico de archivos para un acceso más rápido al área de trabajo.

### Comparación de etiquetas
Canelary permite realizar una comparación entre el código o imagen de dos etiquetas distintas, o distintas versiones de la misma.

### Verificador de productos
Canelary ofrece un sistema de reglas para validar que las variables utilizadas en una etiqueta estén bien parametrizadas para una familia de productos. Ofrece un sistema de reporte de errores, en caso de que los parámetros no estén en orden.

### Generar Muestra
Si la familia de productos se encuentra bien parametrizada, Canelary ofrece la posibilidad de generar una muestra de etiquetas. Imprimiendo una copia por cada producto seleccionado, completando las variables con los datos únicos del producto.

### Generar Registro
Junto con la generación de una muestra, se pude además especificar la creación de un documento especificando los cambios realizados a la etiqueta.

### Integración con Git
Además, Canelary permite integrar tus etiquetas con Git. Ofreciendo la posibilidad de sincronizar varios puestos con un repositorio global.

### Sistema de archivos virtuales
Con Canelary se puede abstraer la forma en la que se almacenan el codigo de las etiquetas, desde un simple archivo de texto hasta integrado en una base de datos.