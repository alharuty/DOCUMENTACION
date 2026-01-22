# SCRIPT PARA SUPABASE


### DESCARGAR TABLA COMPLETA EN FORMATO .CSV DESDE SUPABSE (hatsa 1M datos)

- **Paso 1:** Instalar psql
  ```
  brew instal libpq
  ```
  
- **Paso 2:** Exportar a la DSN de supabase
  ```
  export SUPABASE_PG_DSN="postgresql://postgres.tu_clave....../postgres?sslmode=require"
  ```
- **Paso 3:** Conectarse a la DSN de supabase
  ```
  psql "$SUPABASE_PG_DSN"
  ```
Se abrirá una pestaña en el terminal conel formato postgres=>

- **Paso 4:** Descargar la tabla que queramos
  ```
  \copy public.tu_tabla TO 'tu_tabla.csv' CSV HEADER;
  ```


  ### DESCARGAR TABLA COMPLETA EN FORMATO .CSV DESDE SUPABASE (más de 1M datos)

- **Paso 1:** Guarda este archivo llamándolo export_tu_tabla.sh
- **Paso 2:** Define tu SUPABASE_PD_DSN en la línea 5
```
#!/usr/bin/env bash
set -euo pipefail

# definimos la conexión a la base de datos
: "${SUPABASE_PG_DSN:?Falta SUPABASE_PG_DSN. Ej: export SUPABASE_PG_DSN='AQUÍ VA TU DSN'}"

DSN="$SUPABASE_PG_DSN"

# Ajusta estos 3 valores a tu caso
TABLE="public.tu_tabla"
COL="id"
CHUNK=5000000   # 5M por archivo (ajusta a 1000000 si prefieres 1M)

# (Opcional) carpeta de salida
OUT_DIR="."
mkdir -p "$OUT_DIR"

echo "Obteniendo MAX($COL)…"
MAX="$(psql "$DSN" -Atc "SELECT max($COL) FROM $TABLE;")"

if [[ -z "${MAX}" || "${MAX}" == "NULL" ]]; then
  echo "No se pudo obtener MAX($COL) (¿tabla vacía o columna incorrecta?)"
  exit 1
fi

echo "MAX($COL) = $MAX"

START=1
while [ "$START" -le "$MAX" ]; do
  END=$((START + CHUNK))

  OUT_FILE="$(printf "%s_%010d_%010d.csv.gz" "$(echo "$TABLE" | sed 's/.*\.//')" "$START" "$((END-1))")"
  OUT_PATH="$OUT_DIR/$OUT_FILE"

  echo "Exportando filas [$START, $END) → $OUT_PATH"

  psql "$DSN" \
    -c "\copy (
      SELECT *
      FROM $TABLE
      WHERE $COL >= $START AND $COL < $END
      ORDER BY $COL
    ) TO STDOUT CSV HEADER" \
    | gzip > "$OUT_PATH"

  START=$END
done

echo "✅ Export terminado en: $OUT_DIR"
```
- **Paso 3:** Corre el executable
```
./export_tu_tabla.sh
```
