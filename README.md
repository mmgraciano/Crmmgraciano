# Panel WM Micaela Graciano

Panel para registrar tu base de cuentas, en un solo archivo (`index.html`).

## Cómo abrirlo

- **Recomendado:** https://claude.ai/artifact/MRNV6HsmrXEA3EfA43gzYs (abrilo en una pestaña del navegador y guardalo en favoritos).
  Las cuentas se guardan en una base de datos de tu cuenta de Claude y las ves desde la compu o el celular.
- **Archivo suelto:** descargá `index.html` y abrilo con doble clic. En ese modo los datos quedan solo en ese navegador.

## Cómo funciona

- **WM3** muestra todas las cuentas. Las demás pestañas (SGR, Prospects, Tareas pendientes, FAL, Notas Estructuradas, FWD)
  muestran solo las cuentas asignadas a cada una. Una cuenta puede estar en varias pestañas.
- **Asignar pestañas:** tocá **+ pestaña** debajo del nombre de la cuenta, o marcalas al editarla.
- **Agregar, renombrar o quitar pestañas:** botón **+** al final de las pestañas. Ahí también se cambian los días de la alarma.
- **Alarma:** se pone en rojo cuando pasaron más de 21 días desde el último contacto (o si no hay fecha).
  Tocá la alarma para marcar que la contactaste hoy. El recuadro **para contactar** filtra solo esas cuentas.
- **Edición en la tabla:** la fecha de último contacto y la acción/comentarios se editan directo en la fila.
- **Buscar** por nombre o por N° de cuenta. **Ordenar** tocando el título de cada columna.
- **×** en WM3 elimina la cuenta; en otra pestaña solo la quita de esa pestaña.
- **Eliminar sin cuenta** borra los registros que no tienen N° de cuenta (en la pestaña que estás viendo).

## Tenencias

La pestaña **Tenencias** muestra el detalle por especie de tus clientes. Tocá **Importar tenencias** estando en Tenencias y elegí el Excel
(el reporte del broker con `descripcion_comitente_completa`, `valoracion_mep`, etc. se lee tal cual).

- Necesita una columna con el N° de cuenta (`N° de cuenta`, `Cuenta`, `Comitente`…). Puede haber filas de título arriba.
- El resto de las columnas (especie, cantidad, precio, valuación, moneda…) se muestran tal como vienen en el archivo.
- Si la cuenta aparece solo en la primera fila de cada cliente, se completa en las filas siguientes. Las filas de "Total" se ignoran.
- El nombre sale del archivo, o si no hay columna de nombre, de la cuenta cargada en WM3.
- Cada importación **reemplaza** las tenencias anteriores (te pide confirmación).

## Tenencia total

La pestaña **Tenencia total** muestra el total en USD del último informe de tenencias y, desde el segundo informe:

- cuánto subió o bajó contra el informe anterior, en USD y en %;
- cuánto de esa variación viene **por precio** (mercado y tipo de cambio) y cuánto **por movimientos**
  (ingresos, retiros, compras y ventas). Para separarlo, el Excel necesita una columna de cantidad;
- tablas **por cliente** y **por especie**, ordenadas por impacto;
- un gráfico con la evolución del total y el historial de informes.

Arriba hay dos filtros: **Tipo de activo** (Obligaciones Negociables, Fondos, CEDEARS…) y **Activo** (AL30, GD30…).
Al elegir uno se actualizan el total, el % sobre tu tenencia, el gráfico, la variación y la lista de clientes que lo tienen.
El panel **Composición por tipo de activo** muestra cuánto pesa cada tipo; tocá una fila para filtrar.
Los mismos filtros están en la pestaña **Tenencias**.

En **Ajustes de tenencia** se elige qué columna es la valuación, la moneda, la cantidad y la especie, y se carga el
**tipo de cambio** para pasar a USD las posiciones en pesos. Si importás dos veces el mismo día, la segunda corrige a la primera.

## Ingresos

La pestaña **Ingresos** muestra lo que generó cada cliente por categoría (por ejemplo ACDI, OPERACIONES, FUTUROS) y el total en USD.
Tocá **Importar ingresos** estando en esa pestaña. Los clientes del archivo que no están en WM3 se pueden agregar con un clic.

## Pestañas automáticas

- **En 0:** clientes de WM3 sin tenencia (o con saldo negativo) en el último informe.
- **Menos de 10.000 USD:** clientes con tenencia mayor a 0 y menor al umbral (se cambia en Ajustes de tenencia).

## Importar desde Excel

El archivo necesita una columna `Nombre` o `N° de cuenta` (o una columna tipo `12915 - APELLIDO NOMBRE`, como el reporte del broker). También reconoce `Última vez contactado`, `Acción / comentarios`,
`Teléfono`, `Email`, `Notas` y `Pestañas` (por ejemplo `SGR, FAL`; si una pestaña no existe, se crea).

- Si importás estando en una pestaña (por ejemplo SGR), las cuentas importadas también quedan en esa pestaña.
- Si una cuenta ya existe (mismo N° de cuenta) se actualiza en vez de duplicarse.
- **Exportar Excel** descarga la pestaña que estás viendo; ese archivo sirve como plantilla para volver a importar.
