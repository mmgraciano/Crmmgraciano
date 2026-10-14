Cumbre es una firma de wealth management con una app de uso jurídico: mandatos, poderes, vencimientos y carteras de clientes. La estética tiene que transmitir lo mismo que un buen estudio: orden, discreción y solidez. Se inspira en el papel de un expediente, la tinta azul pizarra de una firma y el latón de un sello.

## Principios

- **Sobrio antes que vistoso.** Un solo color de marca (`pizarra`) y un acento (`laton`) usado con medida. Nada de degradés, sombras en tarjetas ni ilustraciones.
- **Precisión de documento.** Esquinas casi rectas (`radius-sm`, `radius-md`), filetes de 1px (`line`) en lugar de sombras, cifras en `mono` alineadas.
- **El latón es una firma, no un adorno.** Va en la línea bajo el isotipo, el filete sobre las cifras de una tarjeta, el subrayado de la pestaña activa y el total de una tabla. Nunca como fondo grande.

## Voz y redacción

- Español rioplatense profesional. En la app interna, voseo ("Registrá el mandato"). En documentos y mensajes para clientes, usted ("Le informamos que su mandato vence el 30/06/2027").
- Mayúscula solo al inicio de la oración: "Exportar Excel", no "Exportar EXCEL" ni "Exportar Excel De Clientes".
- Términos del oficio, sin anglicismos de marketing: comitente, mandato, poder, conformidad, tenencia, vencimiento.
- Formato argentino: `USD 1.284.500,00`, `14/10/2026`, `+8,42 %`, `Expte. N° 4.512/2026`.
- Sin emoji, sin signos de exclamación, sin superlativos.

## Color

- Fondo de página `paper`; todo lo que contiene datos va sobre `surface` con borde `line`. `surface-sunken` para encabezados de tabla y totales.
- Texto en `ink`; secundario en `ink-muted`. Ambos pasan 5:1 o más en los dos temas.
- Acción principal en `pizarra` con texto `on-pizarra`. Selección y fila activa en `pizarra-soft`.
- `laton` como texto solo sobre `paper` y `surface`. Sobre `laton-soft` el texto es `laton-ink`.
- Estados: `ok` (conforme, positivo), `warn` (pendiente, por vencer), `lacre` (vencido, rechazado, negativo), cada uno con su `-soft` de fondo. Siempre acompañados de una palabra o un signo (+ / −): el color nunca es la única señal.
- Foco: anillo `focus` de 2px, separado 2px del control.

## Tipografía

- `display` (Libre Caslon Text): títulos y nombres de clientes en tarjetas. Es la letra de los documentos legales clásicos; usala con moderación, un `display` o `title-1` por pantalla.
- `sans` (Public Sans): todo el texto de interfaz en `body`, `small` y `label`. `label` siempre en mayúsculas con su espaciado.
- `mono` (IBM Plex Mono): montos, porcentajes, N° de cuenta, de mandato y de expediente, en `figure` o `reference`, con cifras tabulares.
- Cargar las tres desde Google Fonts:
  `https://fonts.googleapis.com/css2?family=Libre+Caslon+Text:ital,wght@0,400;0,700;1,400&family=Public+Sans:wght@400;500;600;700&family=IBM+Plex+Mono:wght@400;500&display=swap`

## Espacio y forma

- Escala de 4px: `space-1` a `space-12`. Tarjetas con `space-6` de relleno, celdas con `space-3` × `space-4`, secciones separadas por `space-8`.
- `radius-sm` en botones, campos y etiquetas; `radius-md` en tarjetas y tablas; `radius-lg` solo en diálogos.
- `shadow-raised` solo en diálogos y menús flotantes.

## Logo

- El isotipo es una cumbre con un pico secundario sobre una línea de firma en latón (grupo Logos). El nombre se compone en `display` con "Wealth Management" debajo en `label` color `laton` (componente Logo).
- `cumbre-mark-pizarra.svg` sobre fondos claros; `cumbre-mark-claro.svg` sobre `pizarra` o en tema oscuro.

## Íconos

- No hay un set propio todavía. Usá íconos lineales de 1.5px de trazo y esquinas rectas (por ejemplo Lucide), en `ink-muted` o `pizarra`, siempre con texto al lado en acciones.
