# Página de Caishen

Página pública para presentar Caishen y bajar los instaladores. Es una sola página estática (`index.html`), sin fuentes
externas ni librerías, para que cargue rápido con datos móviles.

**Este repo es PÚBLICO.** Aquí solo van la página y los instaladores. El código de Caishen está en el repo
privado y nunca se copia aquí.

## Archivos

- `index.html`: la página.
- `manual.html`: copia de `Distribucion/Caishen-Manual.html` del repo de la app.
- `img/`: ícono, moneda e imagen para compartir (de `Distribucion/Marca`), y las capturas en WebP (`venta`, `venta-oscuro`, `cobro`, `panel-oscuro`, `cierre`), sacadas del emulador de tablet con un negocio de demostración («Cafeteria La Ceiba»).

## Publicar una versión nueva

1. Crear un *release* en GitHub con la etiqueta `vX.Y` y subirle `Instalar-Caishen-X.Y.exe` y `Caishen-X.Y.apk`
   (salen de `Entregas/` en el repo de la app).
2. En `index.html`, cambiar:
   - el título «Descargar Caishen X.Y»;
   - los dos enlaces de descarga (`releases/download/vX.Y/...`);
   - nombre, tamaño y SHA-256 de cada archivo (`sha256sum` sobre cada instalador);
   - la sección Novedades: la versión nueva arriba con la etiqueta «Actual», la anterior pasa a «Versiones anteriores».
3. Si cambió el manual, volver a copiar `manual.html`.

## WhatsApp

El número de contacto va en la variable `WHATSAPP` al final de `index.html` (solo dígitos, con el 53 delante).
Mientras esté vacío, los botones de WhatsApp llevan a la sección de contacto.
