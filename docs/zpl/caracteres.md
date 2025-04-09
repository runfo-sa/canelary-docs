---
sidebar_position: 5
slug: /docs/zpl/caracteres
---

# Caracteres especiales

El comando `^CI` (Change International Font/Encoding) se utiliza en ZPL para especificar la tabla de codificación de caracteres que debe usar la impresora. Esto es particularmente útil al trabajar con **caracteres especiales**, símbolos o idiomas que requieren un conjunto de caracteres específico, como los acentos en español, caracteres chinos o símbolos de otros alfabetos.

---

## Sintaxis

```
^CIn
```

- `n`: Identificador del conjunto de caracteres a utilizar.

---

## Tablas de codificación más comunes

| Valor (`n`) | Codificación        | Descripción                              |
| :---------: | :------------------ | :--------------------------------------- |
|     `0`     | US-ASCII            | Conjunto básico de caracteres en inglés. |
|     `1`     | ISO 8859-1          | Europa Occidental, incluyendo español.   |
|     `2`     | Code Page 850 (DOS) | Europa Occidental ampliada.              |
|     `3`     | UTF-8               | Unicode, soporta múltiples idiomas.      |
|    `10`     | ASCII               | Caracteres Españoles.                    |
|    `13`     | Windows-1252        | Europa Occidental (Windows).             |
|    `28`     | UTF-16              | Unicode (compatibilidad adicional).      |
