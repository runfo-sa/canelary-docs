---
sidebar_position: 2
slug: /docs/zpl/comandos
---

# Comandos principales

ZPL se basa en comandos simples y estructurados para crear etiquetas personalizadas. A continuación, te presento una lista de los comandos más utilizados y su función principal:

---

## `^XA` y `^XZ`

- `^XA`: Inicia una nueva etiqueta.
- `^XZ`: Finaliza y envía la etiqueta a imprimir.

---

## `^FO` (Field Origin)

- Establece la posición del elemento utilizando la esquina superior izquierda como referencia.
- **Sintaxis**: `^FOx,y`
  - `x`: Coordenada horizontal.
  - `y`: Coordenada vertical.

---

## `^FT` (Field Typeset)

- Posiciona un elemento utilizando la línea base como referencia, ideal para texto.
- **Sintaxis**: `^FTx,y`
  - `x`: Coordenada horizontal.
  - `y`: Coordenada vertical.

---

## `^A` (Font Specification)

- Define el tipo, orientación y tamaño de la fuente para el texto.
- **Sintaxis**: `^Afo,h,w`
  - `f`: Tipo de fuente.
  - `o`: Orientación (e.g., `N` para normal, `R` para rotada).
  - `h`: Altura.
  - `w`: Ancho.

---

## `^FD` (Field Data)

- Contiene el texto o datos a imprimir, como el contenido de códigos de barras o texto.
- **Sintaxis**: `^FDtexto_a_imprimir^FS`

---

## `^FS` (Field Separator)

- Marca el final del elemento actual (obligatorio después de los comandos `^FD` y `^GB`, opcional para los demas).

---

## `^BY` (Bar Code Field Default)

- Establece el grosor de las barras y el espacio entre ellas en un código de barras.
- **Sintaxis**: `^BYw,r,h`
  - `w`: Ancho de la barra más delgada.
  - `r`: Relación entre barras gruesas y delgadas.
  - `h`: Altura del código de barras.

---

## `^BC` (Bar Code Code 128)

- Genera un código de barras en formato Code 128.
- **Sintaxis**: `^BCo,h,f,g,e`
  - `o`: Orientación.
  - `h`: Altura.
  - `f`: Imprime texto debajo (`Y`/`N`).

---

## `^BQN` (Bar Code QR Code)

- Crea un código QR.
- **Sintaxis**: `^BQN,e,s`
  - `e`: Nivel de corrección de errores (`H`, `Q`, `M`, `L`).
  - `s`: Tamaño del módulo.

---

## `^GB` (Graphic Box)

- Dibuja un rectángulo relleno o con bordes.
- **Sintaxis**: `^GBw,h,t,c,r`
  - `w`: Ancho.
  - `h`: Altura.
  - `t`: Grosor del borde.
  - `c`: Color (`B` para negro, `W` para blanco).
  - `r`: Radio de las esquinas (opcional).

---

Para mas comandos ver [ZPL Programming Guide](https://www.zebra.com/content/dam/support-dam/en/documentation/unrestricted/guide/software/zpl-zbi2-pg-en.pdf).
