# Panel WM Micaela Graciano

Panel para registrar tu base de cuentas, en un solo archivo (`index.html`).

## Cómo abrirlo

- **Recomendado:** https://claude.ai/artifact/MRNV6HsmrXEA3EfA43gzYs (abrilo en una pestaña del navegador y guardalo en favoritos).
  Las cuentas se guardan en una base de datos de tu cuenta de Claude y las ves desde la compu o el celular.
- **Archivo suelto:** descargá `index.html` y abrilo con doble clic. En ese modo los datos quedan solo en ese navegador.

## Cómo funciona

- **WM3** muestra todas las cuentas. Las demás pestañas (Tareas pendientes y, dentro de Tenencia total, SGR, Prospects, FAL y Notas Estructuradas)
  muestran solo las cuentas asignadas a cada una. Una cuenta puede estar en varias pestañas.
- **Tareas pendientes:** con **+ Nueva tarea** anotás una tarea, con un cliente y una fecha si querés. Cada tarea tiene un
  estado (**Sin hacer**, **Pendiente** o **Hecha ✓**): tocá el estado para pasar al siguiente. Las vencidas se marcan en rojo
  y las hechas quedan guardadas abajo, en **Hechas**. Cada cliente tiene una sola tarea abierta: si se agrega otra para el mismo cliente
  (a mano, desde Tomar ganancia o desde la IA) se suma a la que ya tenía. Arriba hay un buscador (por texto, cliente o estado; en Tomar ganancia,
  por cliente, N° de cuenta o activo). En WM3 y las demás pestañas de cuentas, debajo de cada cliente se ven sus tareas abiertas;
  al tocarlas se abre Mis tareas filtrado por ese cliente. A la derecha de cada tarea, "Aprobado por el cliente": ✓ verde, ✗ roja
  o punto amarillo (pendiente); con **Ordenar** se agrupan por color (amarillas, verdes, rojas o sin marcar primero); cada grupo (amarillas, verdes, rojas y sin marcar) tiene **Eliminar todo** (pide confirmación). Marcar la aprobación (cualquiera de las tres) o hacer la tarea actualiza
  "Última vez contactado" del cliente a hoy;
  tocar el marcado lo desmarca. Se guardan en la base del panel (colección `tareas`).
- **Coach:** pestaña con el resumen semanal de jueves a miércoles (por defecto la semana que contiene a ayer, así el miércoles ya se
  puede adelantar y el jueves está la semana cerrada; ◀ ▶ para ver otras). Cuenta reuniones (Reuniones), clientes con los que habló
  (reuniones, tareas hechas, tareas marcadas en verde/amarillo/rojo esa semana —campo `aprobEl`— y cada fecha de "Última vez contactado", que ahora queda en un historial `contactos` de la cuenta),
  licitaciones y la facturación del mes (sin tareas: es el resumen comercial). Cada reunión muestra su resumen (las notas de la
  reunión), que se puede escribir ahí mismo y entra en el texto para el coach. Tiene notas por semana (`coach/{jueves}`) y **Copiar resumen** para WhatsApp.
- **Licitaciones:** pestaña propia. **+ Nueva licitación** crea una y deja escribir el título ahí mismo (ej: S29E7); en **Más datos**
  van cierre, moneda, comisión % por defecto, notas y copiar los comitentes de otra. En cada una se anotan comitentes con monto y comisión %; la comisión estimada y los totales se
  calculan solos, cada comitente tiene estado (a confirmar, confirmó, orden cargada, adjudicada, no entró) y notas, y se baja en Excel.
  Abajo, **Preguntale a la IA** responde con tenencias (con la moneda de cada activo), rendimientos y licitaciones, y puede proponer
  comitentes para sumar a una licitación (ella confirma). Colección `licitaciones`.
- **Tomar ganancia (+10%):** segunda solapa de Tareas pendientes. Con **Importar rendimientos** se sube el Excel de rendimientos
  por posición (Comitente, Ticker, Pppc Mep, Precio Actual Mep) y lista, por cliente, los activos 10% o más arriba del precio de
  compra en USD MEP (el % se puede cambiar). **+ Tarea** crea la tarea en Mis tareas y el tilde verde marca al cliente como hecho:
  baja a "Hechos" (y si tenía la tarea abierta, la cierra; al revés, marcar como hecha la tarea "Tomar ganancia…" en Mis tareas
  también pasa al cliente a Hechos). La etiqueta de la tarea queda en el cliente: "Tarea creada · pendiente" mientras está abierta y
  "Tarea hecha ✓" cuando se hace; arriba se cuentan las tareas armadas, hechas, pendientes y los clientes sin tarea. **⬇ Imagen** (general, por grupo o en cada cliente) baja una imagen
  "Wealth Management" con el desglose activo por activo (suba % y ganancia USD). Se guarda en `ganancias/hechas` y se mantiene con informes nuevos. Las subas de 300% o más se marcan para revisar
  el precio de compra y no se suman. Se guarda en la base del panel (documento `ganancias/actual`).
- **Cartera completa:** igual que Tomar ganancia (que no incluye a los clientes Lang; acá sí están) pero con todos los activos de cada cliente (sin filtro de suba, tipo ni monto),
  con rendimiento % y resultado USD de cada uno. Cada cliente tiene su **⬇ Imagen** (Wealth Management) y arriba están el Excel y la imagen general.
- **Reuniones:** solapa de Tareas pendientes con las reuniones de la semana (lunes a domingo) agrupadas por día, más las próximas y
  las anteriores. **+ Nueva reunión** agenda una (cliente, día, hora y tema); a la derecha, el tilde verde la marca como hecha, y
  debajo de cada una hay un cuadro de notas que se guarda solo. Una reunión cargada con fecha pasada queda como hecha
  (en Reuniones anteriores); las reuniones hechas actualizan el último contacto del cliente. Colección `reuniones`.
- **Clientes Lang:** en Mis tareas y en Tomar ganancia, los clientes que se llevan en conjunto con Lang (Victorel, Lang Esteban,
  Lang Carlos, Tassisto, Barchiesi, D Amico, Morassi Luciano, Haidar, Bengoechea, Olle, Morassi Alejandro, Sorichetti y Laffitte) aparecen arriba en un grupo desplegable "Clientes Lang" (`config.grupos`).
- **Preguntale a la IA:** tercera solapa de Tareas pendientes. Se le pregunta en lenguaje natural (por ejemplo "¿qué clientes
  tienen QQQ, SPY o NVDA y por qué rotarlos?") y responde Claude con los datos del panel: tenencias, rendimientos desde la compra,
  research del día, facturación por mes, clientes y tareas. Usa la cuenta de Claude de quien pregunta (capacidad `sample`); la
  conversación queda solo en ese navegador. Si se le pide ("poné como tarea…"), propone tareas por cliente que se crean en
  Mis tareas al tocar **Crear tareas**. Con 📎 (o pegando o arrastrando) se le pueden pasar prints e imágenes, PDF, Excel, CSV o
  texto: las imágenes van a Claude como imágenes y el resto se lee en el navegador y va como texto.
- **Asignar pestañas:** tocá **+ pestaña** debajo del nombre de la cuenta, o marcalas al editarla.
- **Agregar, renombrar o quitar pestañas:** botón **+** al final de las pestañas. Ahí también se cambian los días de la alarma.
- **Alarma:** se pone en rojo cuando pasaron más de 21 días desde el último contacto (o si no hay fecha).
  Tocá la alarma para marcar que la contactaste hoy. El recuadro **para contactar** filtra solo esas cuentas.
- **Edición en la tabla:** la fecha de último contacto y la acción/comentarios se editan directo en la fila.
- **Buscar** por nombre o por N° de cuenta. **Ordenar** tocando el título de cada columna.
- **×** en WM3 elimina la cuenta; en otra pestaña solo la quita de esa pestaña.
- **Eliminar sin cuenta** borra los registros que no tienen N° de cuenta (en la pestaña que estás viendo).

## Tenencias detalladas

Dentro de **Tenencia total** (submenú) está **Tenencias detalladas**, que muestra el detalle por especie de tus clientes. Tocá **Importar tenencias** estando en Tenencias detalladas y elegí el Excel
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
En el Resumen, **Por precio** y **Por movimientos** se despliegan con la flechita (▾) y muestran qué comitentes explican esa
variación y con qué activos (compró / ingresó, vendió / retiró, posición nueva o cerrada), con buscador.
Los mismos filtros están en **Tenencias detalladas**. El submenú de Tenencia total tiene: Resumen, Tenencias detalladas, En 0, Menos de 10.000 USD, SGR, Prospects, FAL y Notas Estructuradas (estas cuatro se siguen asignando con **+ pestaña** y se renombran o quitan desde **+**).

En **Ajustes de tenencia** se elige qué columna es la valuación, la moneda, la cantidad y la especie, y se carga el
**tipo de cambio** para pasar a USD las posiciones en pesos. Si importás dos veces el mismo día, la segunda corrige a la primera.

## Facturación

La pestaña **Facturación** muestra lo que factura cada cliente por categoría (ACDI, OPERACIONES, FUTUROS…).

- Al tocar **Importar facturación** se elige qué período cubre el archivo (por ejemplo "Septiembre completo" u "Octubre a la fecha").
- **Separada por mes:** si el Excel trae una columna de fecha o mes, se guarda un período por cada mes automáticamente.
- **Meta de facturación** (USD 10.000 por mes y objetivo de USD 60.000 de julio a diciembre, ambos editables): lo facturado contra el objetivo y cuánto hace falta por mes en lo que queda, el promedio por mes, el mes anterior y el mes en curso.
  **Para copiar este mes** lista los comitentes que más facturaron el mes anterior, con el acumulado hasta llegar a la meta,
  lo que facturó cada uno este mes y cuánto le falta para repetir. Abajo, **Facturan este mes y el mes anterior no** marca a los
  comitentes nuevos del mes y desglosa el total del mes (lista + otros del mes anterior + nuevos).
  Cada período queda guardado; si subís otra vez el mismo período, se reemplaza.
- Arriba se elige el **período** y con cuál **comparar** (por defecto, el anterior). Si los períodos tienen distinto largo,
  se comparan por ritmo mensual.
- En el mes en curso se ve cuánto llevás facturado contra el mes anterior y la **proyección al cierre**.
- **Top 10 clientes por facturación** con barras y el peso de cada uno sobre el total.
- Los clientes del archivo que no están en WM3 se pueden agregar con un clic.

## Research

La pestaña **Research** muestra alertas de compra, venta, activos para sumar y eventos a vigilar, cada una con la explicación,
los riesgos, las fuentes y la exposición actual de la cartera (USD, % y clientes). Una tarea programada en la nube
("Research Panel WM", días hábiles 8:59 hora de Argentina) busca noticias oficiales y de mercado, las cruza con las tenencias
y escribe el research del día en la base del panel; avisa por celular y mail. Es un insumo de análisis, no una orden de operar.

La subpestaña **Vencimientos del mes** lista, a partir de las tenencias, lo que vence en el mes elegido (o en los próximos
90 días, o lo pendiente de pago): letras, bonos, ONs, e-cheqs, pagarés, futuros y opciones, agrupado por fecha, con el total
en USD y el detalle por cliente. La fecha sale del código o la descripción de cada especie. No incluye rentas ni amortizaciones parciales.

La subpestaña **Cartera nueva** propone qué comprar para armar una cartera desde cero según el perfil (conservador, moderado
o agresivo) y el monto a invertir: instrumentos concretos agrupados por tipo, % y USD de cada uno, por qué, y si ya está
en la cartera de otros clientes. La actualiza el research diario y se puede exportar a Excel.
El perfil **moderado** sigue siempre la regla de Micaela: 80% en obligaciones negociables de emisores con calificación
AAA local y 20% en CEDEARs o acciones argentinas, según el momento. Las acciones se eligen por consenso de analistas
(recomendación, precio objetivo promedio y potencial de suba), sin índices en máximos, y se muestran las candidatas descartadas con el motivo.

## Pestañas automáticas (dentro de Tenencia total)

- **En 0:** clientes de WM3 sin tenencia (o con saldo negativo) en el último informe.
- **Menos de 10.000 USD:** clientes con tenencia mayor a 0 y menor al umbral (se cambia en Ajustes de tenencia).

## Importar desde Excel

El archivo necesita una columna `Nombre` o `N° de cuenta` (o una columna tipo `12915 - APELLIDO NOMBRE`, como el reporte del broker). También reconoce `Última vez contactado`, `Acción / comentarios`,
`Teléfono`, `Email`, `Notas` y `Pestañas` (por ejemplo `SGR, FAL`; si una pestaña no existe, se crea).

- Si importás estando en una pestaña (por ejemplo SGR), las cuentas importadas también quedan en esa pestaña.
- Si una cuenta ya existe (mismo N° de cuenta) se actualiza en vez de duplicarse.
- **Exportar Excel** descarga la pestaña que estás viendo; ese archivo sirve como plantilla para volver a importar.
