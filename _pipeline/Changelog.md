# Changelog / bitácora del sitio personal

*Registro de qué se hizo en cada corrida. Se escribe a medida que se completa cada ítem, no al
final. Orden cronológico inverso (lo más nuevo arriba).*

---

## 2026-10-13 (corrida 1) — reconocimiento, backup y pipeline

**Primera corrida del proyecto web.** No se tocó nada del sitio: sólo se leyó, se hizo backup y se
armó esta carpeta. El sitio vivo sigue siendo el de junio 2026.

### Lo que se leyó
- **El repo completo** (`matiasgolman.github.io`, rama `main`, último commit `4462cb1` del
  19/6/2026, árbol limpio y al día con `origin/main`): `_config.yml` entero, las siete páginas de
  `_pages/`, `_bibliography/papers.bib` (3 entradas: JMP, *Value of Personality*, meta-análisis de
  formalización), `_data/socials.yml`, los 9 `_projects/`, los 31 `_posts/`, `_layouts/`, el
  workflow `deploy.yml`, y el inventario de `assets/`.
- **El sitio desplegado**: cabeceras HTTP, `robots.txt`, `sitemap.xml`, y el `<head>` de la home.
- **CV (oct 2026), perfil de LinkedIn y `list_of_places.xlsx`** (83 filas: portales holandeses,
  agregadores y organismos internacionales, con la columna de requisito de neerlandés).

### Hallazgos que cambian el plan
1. **El sitio es, en su mayoría, la demo de al-folio.** 31 posts, 9 proyectos y 3 noticias son todos
   del tema. `scholar.last_name: [Einstein]`. Detalle en `ESTADO.md`.
2. **El `about` está ocho meses desactualizado**: dice «PhD candidate en Nottingham, disponible para
   entrevistas en el job market 2025/26». Es lo primero que lee cualquiera que entre hoy.
3. **El sitio NO está indexado en Google — verificado en Google el mismo día.** Mi primera lectura
   (basada en que el sitio aparecía en los resultados de otro buscador) era equivocada y quedó
   corregida: `site:matiasgolman.github.io` devuelve **una sola página, `/dashboard/`**, y la frase
   exacta de la home da **«No results found»**. Buscando su nombre con y sin tilde salen uu.nl,
   LinkedIn, Scholar, ResearchGate, Facebook, X, Instagram y hasta su CV alojado en
   economicas.uba.ar — el sitio propio, no. Lo técnico está bien (robots, sitemap, canonical, sin
   `noindex`), así que es una decisión de calidad de Google: «Crawled – currently not indexed».
   El dato que lo explica: **la única página indexada es la única que no es plantilla de al-folio**.
   Detalle y plan de seis pasos en el ítem **S1** de `ESTADO.md`.

4. **El repo pesa 1,5 GB**: 1,3 GB de `.git`, 73 MB en un solo HTML (el dashboard), 61 MB de PDFs
   con nueve versiones del JMP. Ítems **S2** y **S3**.
5. **`/dashboard/` y `/araucariaspotter/` declaran `layout: single`, que no existe en al-folio.**
   Se renderizan sin layout (sin navbar, sin estilos del sitio).

### Backup de la versión vieja (ítem R3)
- Tag **`v1-academic-jmp-2025`** y rama **`backup/v1-academic-jmp-2025`**, los dos en `4462cb1`.
- **`_pipeline/_archivo/snapshot_contenido_v1_20261013.tar.gz`** (3,8 MB): todo el contenido y las
  plantillas, sin `assets/` ni `.git`. Sirve para leer o recuperar un texto sin clonar 1,5 GB.
- **No se pudo pushear**: la VM del puente no tiene credenciales de GitHub (`git push` falla con
  «could not read Username», y no hay `gh` instalado). Queda en el to-do de Matías, ítem 2.

### Pipeline creado (ítem R2)
`_pipeline/` con `LEEME.md`, `ESTADO.md`, `To-Do-Matias.md`, `Changelog.md`,
`_archivo/Comentarios_Matias.md` y `preguntas/`. Mismas convenciones que el pipeline de `tenure`.
Añadido a `exclude:` en `_config.yml` para que Jekyll no lo publique.

### Cuestionario 1
`preguntas/Preguntas_01_estructura_y_diseno.md`, 22 preguntas en cuatro bloques (posicionamiento,
contenido, diseño, técnico). Las cuatro de mayor impacto se preguntaron además en el chat.

**Ítems cerrados:** R1, R2, R3 (con el push pendiente).
**Próximo:** D1 (las respuestas de Matías) → Fase 1, arquitectura de contenido.
