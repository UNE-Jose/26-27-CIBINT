# A01 · Del dato a la Inteligencia

## 1.0 Entendiendo el ejercicio

Hubo una reciente brecha de seguridad en hugging face y nuestra organizacion quiere analizar el impacto sobre la empresa y que pasos hay que hacer para salvaguardarnos.

### 1.1 Posibles acciones:

| | Opción |
|---|---|
| **O1** | Seguir descargando con normalidad |
| **O2** | Congelar las descargas automatizadas |
| **O3** | Rotar las credenciales de la plataforma |
| **O4** | Verificar la integridad de los artefactos ya descargados |
| **O5** | Revisar qué credenciales propias están publicadas fuera de la empresa |
| **O6** | Avisar a los clientes del servicio |
| **O7** | Mantener la observación y fijar un punto de revisión |
Con posibilidad de añadir nuevas opciones nuevas fuera de las proporcionadas.

### 1.2 Material proporcionado:

| Archivo | Contenido |
|---|---|
| [cronologia-inicial.csv](datos/cronologia-inicial.csv) | `C01`–`C14`. Hechos públicos **hasta el 20 de julio**, cuando te llega la petición |
| [cronologia-posterior.csv](datos/cronologia-posterior.csv) | `C15`–`C25`. Hechos públicos **publicados después** |
| [superficies-plataforma.csv](datos/superficies-plataforma.csv) | `S01`–`S10`. Qué partes tiene la plataforma, quién gestiona cada una y qué filas de la cronología inicial la mencionan |
| [fuentes.csv](datos/fuentes.csv) | `F01`–`F12`. Las fuentes de donde sale cada hecho |
**Campos de las cronologías**

| Campo | Qué contiene |
|---|---|
| `id` | Identificador del hecho, `C01`–`C25` |
| `fecha` | Fecha de publicación o de ocurrencia declarada |
| `actor` | Quién lo afirma o de quién trata |
| `tipo` | `declaracion_oficial`, `cobertura`, `antecedente` o `cronologia` |
| `contenido` | El hecho, sin interpretación añadida |
| `fuente_ref` | Enlaza con `fuentes.csv` |
| `corroboracion` | `una_parte` si lo afirma solo una de las organizaciones implicadas · `prensa` si lo publica un medio sin aportar verificación propia · `dos_partes` si lo afirman las dos |

**Campos de las superficies**

| Campo | Qué contiene |
|---|---|
| `superficie_id` | Identificador, `S01`–`S10` |
| `elemento` | Parte de la plataforma |
| `descripcion` | Qué es |
| `gestionada_por` | `plataforma`, `usuario` o `compartida`: quién decide sobre ella |
| `mencion_en_cronologia_inicial` | Filas `C…` que hablan de esa parte |
Con posibilidad de aumentar material si se encuentra publicamente en internet.

NO USAR CRONLOGIA POSTERIOR HASTA PASO 5.