Cumbre es una firma de wealth management con una app de uso jurídico: mandatos, poderes, vencimientos y carteras de clientes. La identidad nace de una idea: la cumbre se dibuja como la línea de un gráfico de mercado. Una línea fina, con tramos planos y saltos, que forma una cordillera; un punto de latón marca siempre el pico más alto. El mercado sube y baja; el patrimonio sigue un plan.

## Principios

- **Pocos colores, usados con convicción.** `celeste` (el cielo), `pizarra` (la montaña) y `paper` (el neutro). Ningún otro fondo.
- **El punto de latón es la firma.** `laton` va solo en el punto de la cumbre y en el único dato destacado de una pantalla. Si aparece en todos lados, deja de significar algo.
- **La cordillera vuelve.** Cada pieza repite el motivo: portada, separadores entre secciones, fondos tenues, pie. Cada vez con otra forma, siempre con el mismo trazo fino.
- **Precisión de documento.** Esquinas casi rectas, filetes de 1px en `ink` en lugar de sombras, cifras alineadas.

## Voz y redacción

- Español rioplatense profesional. En la app interna, voseo ("Registrá el mandato"). En la web, documentos y mensajes para clientes, usted ("Le informamos que su mandato vence el 30/06/2027").
- Mayúscula solo al inicio de la oración.
- Términos del oficio: comitente, mandato, poder, conformidad, tenencia, vencimiento.
- Formato argentino: `USD 1.284.500,00`, `14/10/2026`, `+8,42 %`, `Expte. N° 4.512/2026`.
- Sin emoji, sin signos de exclamación, sin superlativos.

## Color

- **Web y piezas de marca:** se alternan secciones `celeste`, `paper` y `pizarra`. Sobre `celeste` el texto es `ink` y el secundario `ink-soft` (nunca `ink-muted`). Sobre `pizarra`, `on-pizarra` y `on-pizarra-muted`, con filetes `pizarra-line`.
- **App:** fondo `paper`, datos sobre `surface` con filete `line`, `surface-sunken` para encabezados de tabla. Acción principal en `pizarra` con texto `on-pizarra`.
- **Latón:** el punto de la cumbre (`laton` sobre claro, `laton-on-dark` sobre pizarra) y un solo dato destacado por pantalla. En la app, además, la etiqueta Firmado (`laton-soft` con `laton-ink`).
- **Estados de la app:** `ok`, `warn`, `lacre`, cada uno con su `-soft`. Siempre con una palabra o un signo (+ / −) al lado.
- Foco: anillo `focus` de 2px, separado 2px del control.

## Tipografía

- **El nombre** se compone mezclando dos letras: "Cumbre" en `sans` 700 muy apretada (`brand-name`) y "Wealth Management" en `display` 300.
- `display` (Newsreader, peso 300): títulos de sección, párrafos de entrada, citas y cifras grandes. Nunca por debajo de 24px: a tamaño chico la serifa fina se ve débil.
- `sans` (Hanken Grotesk): todo el texto de interfaz y lectura (`body`, `small`, `label`, `title-2`) y las listas grandes (`headline`).
- `mono` (IBM Plex Mono): solo datos. Montos, N° de cuenta, de mandato y de expediente, numeración de pasos.
- Cargar las tres desde Google Fonts:
  `https://fonts.googleapis.com/css2?family=Hanken+Grotesk:wght@400;500;600;700&family=Newsreader:ital,opsz,wght@0,6..72,300;0,6..72,400;1,6..72,300&family=IBM+Plex+Mono:wght@400;500&display=swap`

## La cordillera

- Una línea escalonada: tramos planos alternados con subidas y bajadas, como una cotización. Trazo de 1 a 1.6px, uniones redondeadas.
- La forma general tiene un pico dominante cerca del centro y picos menores a los lados. El punto de latón va exactamente en el máximo.
- **Portada:** cordillera de líneas apiladas. La primera (el horizonte) en `ink`, y debajo relleno `pizarra` con líneas `celeste` cada vez más visibles hacia adelante, sobre un cielo `celeste`. Línea punteada de latón que sube desde el pico.
- **Separadores:** una sola línea en `ink` de 70px de alto entre secciones claras.
- **Fondos:** líneas `celeste` al 7–17 % de opacidad sobre `pizarra`.
- Siempre con la leyenda "Relieve ilustrativo, no representa una cartera real" cuando pueda confundirse con un gráfico de rendimiento.
- **Movimiento:** una sola animación en toda la pieza. La línea del horizonte se dibuja de izquierda a derecha en 2.2 s y el punto de latón aparece al final. Con `prefers-reduced-motion`, sin animación.

## Espacio y forma

- Escala de 4px: `space-1` a `space-12`. Las secciones de la web alternan `space-section` (112px) y 72px para que el ritmo no sea monótono.
- `radius-sm` en botones, campos y etiquetas; `radius-md` en tarjetas y tablas de la app; `radius-lg` solo en diálogos.
- `shadow-raised` solo en diálogos y menús flotantes.

## Fotografía

- Personas y lugares reales (el equipo, la oficina, Buenos Aires), tratados en duotono `pizarra` y `celeste` para que entren en la paleta. Nunca fotos de stock de apretones de manos ni gráficos de bolsa.

## Logo

- El isotipo es la cordillera mínima con el punto de latón (grupo Logos): `cumbre-isotipo-tinta.svg` sobre `paper` y `celeste`; `cumbre-isotipo-blanco.svg` sobre `pizarra`.
- El nombre completo se compone con tipografía (componente Logo). Tamaño mínimo del isotipo: 24px de ancho.

## Íconos

- No hay un set propio todavía. Usá íconos lineales de 1.5px de trazo (por ejemplo Lucide), en `ink` o `pizarra`, siempre con texto al lado en acciones.
