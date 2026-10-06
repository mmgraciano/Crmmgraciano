# CRM Clientes

CRM simple para registrar tu base de clientes, en un solo archivo (`index.html`). No necesita servidor ni instalación.

## Cómo usarlo

- **Opción rápida:** descargá `index.html` y abrilo con doble clic en Chrome, Edge o Firefox.
- **Online:** activá GitHub Pages en este repo (Settings → Pages → rama principal) y entrá desde cualquier dispositivo.

> Los datos se guardan en el navegador donde lo uses (localStorage). Usá **Exportar Excel** seguido como respaldo,
> y para pasar tus datos a otra computadora: exportás en una e importás en la otra.

## Funciones

- **Pestañas:** Todos, Clientes activos, Prospectos, Inactivos y ★ Para operar.
- **Mover entre pestañas:** cambiá el estado desde la lista desplegable de cada fila, o tocá la ★ para marcar que le tenés que operar.
- **Buscar** por nombre (o empresa) en la barra de arriba.
- **Ordenar** tocando el título de cualquier columna (otro toque invierte el orden).
- **Alta manual** con "+ Nuevo cliente", y editar o borrar desde cada fila.
- **Próximo contacto:** si la fecha ya pasó, aparece en rojo.

## Cargar desde Excel

1. Tocá **Descargar plantilla** y completala (una fila por cliente). También sirve tu propio Excel o CSV:
   solo necesita una columna `Nombre`; se reconocen además `Empresa`, `Teléfono`, `Email`/`Correo`, `Estado`,
   `Para operar` (Sí/No o X), `Qué operar`, `Próximo contacto` y `Notas`.
2. Tocá **Importar Excel** y elegí el archivo.

En `Estado`, cualquier valor que contenga "prospecto" o "inactivo" va a esa pestaña; el resto queda como cliente activo.
Si un cliente ya existe (mismo email, o mismo nombre y teléfono) se actualiza en vez de duplicarse.

**Exportar Excel** descarga la pestaña en la que estás, con el orden actual.
