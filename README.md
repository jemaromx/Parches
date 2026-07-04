# Parches — Suite de Diseño Estructural

Repositorio público de actualizaciones. El launcher de la suite consulta
`latest.json` al iniciar; si `version` es mayor que la instalada, ofrece
descargar y aplicar el parche indicado en `download_url`.

## Publicar un parche

1. Crear el .zip con la estructura:
   ```
   manifest.json          ← {"version","date","notes","files":[...]}
   modulo/archivo.py      ← archivos corregidos, con su ruta relativa
   ```
2. Subir el .zip a este repositorio (o como Release) y copiar su URL raw.
3. Actualizar `latest.json`: `version`, `date`, `notes`, `download_url`.
4. Commit y push. Los usuarios verán el aviso al abrir la suite.
