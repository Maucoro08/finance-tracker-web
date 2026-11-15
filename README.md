# Finance Tracker Web

Visor web de registros financieros exportados desde la app **Finance PM**.
Todo corre en tu navegador: no hay servidor, no hay cuentas y tus datos no se envían a ningún lado.

🔗 **Abrir la app:** https://maucoro08.github.io/finance-tracker-web/

> Este repositorio contiene únicamente el build final (`index.html`, un solo archivo).
> El código fuente se mantiene en otro lugar.

## ¿Qué datos necesita?

Un **archivo de respaldo de Finance PM**, con extensión `.json` o `.data`.

| Dato | Detalle |
|---|---|
| Origen | Exportación / copia de seguridad de la app **Finance PM** |
| Formatos aceptados | `.json` (legible) y `.data` (compacto). Ambos son JSON por dentro |
| Colecciones que usa | `transactions`, `categories`, `accounts`, `arrears`, `arrear_transaction_relations` |
| Resto del archivo | Se conserva intacto al exportar, aunque la app no lo muestre |

El archivo **no se incluye en este repositorio** ni se descarga desde ningún servidor. Debes aportarlo tú.

### Cómo obtenerlo

1. En Finance PM, abre la opción de **respaldo / exportar datos**.
2. Guarda el archivo en tu dispositivo (por ejemplo `financePM_YYYYMMDD_HHMMSS.json`).
3. Pásalo a tu computador si hace falta.

## Cómo usarlo

1. Abre la página.
2. Abre el menú de datos (icono de base de datos, arriba a la derecha) y elige **⬆ Importar datos**. También puedes usar el botón de la pantalla inicial.
3. Selecciona tu archivo `.json` o `.data`.
4. Explora las pestañas:

| Pestaña | Para qué sirve |
|---|---|
| **Dashboard** | KPIs, balance neto y tasa de ahorro, ingresos/gastos por categoría, evolución de cuentas e inversiones |
| **Deudas** | Consulta de deudas y préstamos |
| **Transacciones** | Tabla paginada con filtros y ordenamiento |
| **Categorías** | Árbol de categorías con conteo de transacciones |
| **Tools** | Reasignar transacciones entre categorías y editar en lote |

5. Si modificas algo en **Tools**, usa **⬇ Exportar datos** para descargar el archivo actualizado.
   Conserva el formato original (`.json` o `.data`).

## Menú de datos

El botón con el icono de base de datos muestra la fecha del último guardado y despliega:

| Opción | Qué hace |
|---|---|
| 💾 Guardar ahora | Guarda el estado actual en el navegador |
| ⬆ Importar datos | Carga un archivo de respaldo (reemplaza lo que haya en pantalla) |
| ⬇ Exportar datos | Descarga el estado actual como archivo |
| 🗑 Eliminar datos | Borra los datos guardados en el navegador y en memoria (pide confirmación) |

## Salir

El botón **⏻ Salir** cierra la sesión dentro de la app y muestra una pantalla de despedida. Puedes volver con **Volver a entrar**.
El engranaje ⚙ define qué pasa al salir:

| Opción | Efecto |
|---|---|
| 💾 Guardar automáticamente | Guarda al pulsar Salir y también al cerrar o recargar la pestaña. **Viene activada por defecto** |
| 🗑 Preguntar para borrar | Al pulsar Salir pregunta si quieres borrar los datos guardados |

Pulsa una opción activa para desactivarla. Con ambas desactivadas, Salir no hace nada con tus datos.
La pregunta de borrado solo aparece con el botón Salir, no al cerrar la pestaña.

## Privacidad

- Tu archivo se lee **localmente** con el navegador. No se sube a ningún servidor.
- Al importar, la app guarda una copia en el **almacenamiento local (`localStorage`)** de tu navegador.
  Esa copia queda solo en tu equipo.
- Los cambios hechos en **Tools** viven en memoria hasta que los guardes (💾), los exportes o salgas con guardado automático activo.

### Cómo borrar tus datos

1. Abre el **menú de datos** (icono de base de datos, arriba a la derecha).
2. Pulsa **🗑 Eliminar datos** y confirma.

Esto borra los datos guardados en el navegador y los que están en pantalla. No se puede deshacer.
Si usas **⏻ Salir**, la opción **Preguntar para borrar** te ofrece el mismo borrado (**Borrar y salir**).

Se conservan solo tus preferencias de salida (`finance_tracker_prefs`). Si quieres quitarlas también, limpia los datos del sitio desde la configuración del navegador.

> En un equipo compartido, elimina tus datos al terminar.

## Limitaciones

- Los montos se muestran en **pesos colombianos (COP)**.
- Las cuentas en otra moneda se marcan y no se suman al total.
- Las modificaciones solo existen en esta app y en el archivo que exportes. No cambian nada en Finance PM.

## Actualizaciones

Este repositorio se sobrescribe con cada publicación (un único commit con el `index.html` más reciente).
