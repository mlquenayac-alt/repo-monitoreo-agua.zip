# Monitoreo de calidad de agua (ECA)

Aplicación web de un solo archivo (`index.html`, sin dependencias ni servidor) para:

- Registrar muestras: código, punto, día, hora, coordenadas UTM (Este, Norte, zona), pH, conductividad eléctrica, temperatura, SST, SDT, sólidos totales, turbidez y reactivos (observación).
- Estadística descriptiva: n, media, DE, CV, mínimo, mediana y máximo.
- Estadística inferencial: ANOVA de una vía entre puntos de muestreo, correlación de Pearson con valor p y prueba t de una muestra frente al límite ECA.
- Comparar cada muestra con el ECA de la categoría elegida (límites editables).
- Generar el informe imprimible o en PDF: encargado de monitoreo, marco legal, muestras, resultados, reactivos, estadística, interpretación, conclusiones y firmas.

## Publicar en GitHub

1. Crea un repositorio en https://github.com/new (por ejemplo `monitoreo-agua`).
2. Sube `index.html` y este `README.md`.
3. En **Settings → Pages**, elige la rama `main` y la carpeta `/ (root)`.
4. Tu app quedará en `https://TU-USUARIO.github.io/monitoreo-agua/`.

## Notas

- Los datos se guardan en el navegador (localStorage). Usa **Exportar JSON** para respaldarlos e **Importar JSON** para recuperarlos en otro equipo.
- Los límites ECA vienen precargados desde el D.S. N.° 004-2017-MINAM, pero son editables. Verifícalos contra el texto oficial vigente (incluidas sus modificatorias) antes de emitir un informe.
- La temperatura del ECA se define como Δ3 °C respecto a la línea base; la app no la evalúa automáticamente.
- Si dejas vacío «Sólidos totales» y completas SST y SDT, la app los suma.
