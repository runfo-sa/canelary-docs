---
sidebar_position: 1
slug: /docs/zpl/intro
---

# Introducción

**ZPL (Zebra Programming Language)** es un lenguaje de programación específico diseñado para controlar impresoras térmicas Zebra. Este lenguaje es ampliamente utilizado para la generación de etiquetas, códigos de barras y otros formatos de impresión personalizados en industrias como la logística, manufactura y salud.

---

## Características principales

- **Basado en comandos**: Cada instrucción es un comando que define elementos como texto, gráficos o códigos de barras.
- **Impresión de alta velocidad**: Optimizado para impresoras térmicas, permitiendo una rápida generación de etiquetas.
- **Compatibilidad**: Funciona con diversas impresoras Zebra, desde modelos básicos hasta avanzados.
- **Personalización avanzada**: Permite diseñar etiquetas con texto, imágenes y códigos de barras adaptados a las necesidades específicas de cada aplicación.

---

## Ejemplo básico de una etiqueta

```
^XA
^FO50,50^A0N,50,50^FDHello, ZPL!^FS
^FO50,150^BY2^BCN,100,Y,N,N^FD1234567890^FS
^XZ
```

- **^XA**: Marca el inicio de una nueva etiqueta.
- **^FO50,50**: Define la posición (en puntos) del elemento en la etiqueta.
- **^A0N,50,50**: Establece el tipo y tamaño de la fuente.
- **^FDHello, ZPL!**: Especifica el texto que se imprimirá.
- **^BCN,100,Y,N,N**: Genera un código de barras con el texto proporcionado.
- **^XZ**: Finaliza la etiqueta.

---

## Aplicaciones típicas

- Generación de etiquetas con **códigos de barras** (EAN, UPC, QR, etc.).
- Impresión de **etiquetas de envío** con datos dinámicos.
- Diseño de etiquetas personalizadas para **productos y almacenamiento**.

ZPL es una herramienta poderosa para automatizar procesos de impresión, lo que lo convierte en una solución ideal para entornos industriales y comerciales. Si necesitas personalizar etiquetas para tu empresa, aprender ZPL es un gran punto de partida.
