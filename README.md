# bikeshare_paris_sevilla — Disponibilidad de bicicletas compartidas (París y Sevilla)

Archivo histórico de la **disponibilidad de bicicletas en sistemas de
bicicleta pública** de París y Sevilla, capturado en formato CityBikes.

## Origen

- **Fuente:** API agregadora **CityBikes** (citybikes.cy), que normaliza la
  ocupación de redes de bicicleta compartida de todo el mundo.
- Redes incluidas:
  - **París** (Vélib') — 75 estaciones (directorio `Paris_11045`).
  - **Sevilla** (Sevici) — 73 estaciones (directorio `Seville_178`).

## Periodo

- **2014–2015**.

## Estructura del repositorio

- Una serie temporal **por estación** en formato CSV.
- 149 ficheros (75 estaciones de París + 73 de Sevilla + metadatos).

## Formato y campos

Cabecera CSV: `# timestamp,status,avbikes,avstamps,totstamps`

| Columna      | Significado                                                  |
|--------------|-------------------------------------------------------------|
| `timestamp`  | Marca de tiempo de la lectura (epoch UNIX, segundos).       |
| `status`     | Estado de la estación (operativa / fuera de servicio).      |
| `avbikes`    | Bicicletas disponibles.                                     |
| `avstamps`   | Anclajes (bornetas) libres disponibles.                     |
| `totstamps`  | Anclajes totales de la estación.                            |
