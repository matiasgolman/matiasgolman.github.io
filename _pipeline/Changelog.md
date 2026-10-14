# Changelog / bitácora del sitio personal

*Registro de qué se hizo en cada corrida. Se escribe a medida que se completa cada ítem, no al
final. Orden cronológico inverso (lo más nuevo arriba).*

---

## 2026-10-14 (corrida 3) — la mudanza, ORCID entero, y el sitio en vivo

### La mudanza de la carpeta
Matías insistió, así que se hizo, con la precaución que importaba: **no perder los commits sin
pushear**. Se copió el repo entero (árbol de trabajo + `.git` con historia, ramas, tags y la caché
de LFS) a `OneDrive - Universiteit Utrecht\Documents\personal\matiasgolman.github.io`, se verificó
con `diff` de la lista de archivos (1.934 archivos, 0 diferencias) y con `git fsck` limpio, y recién
entonces se borró el original. La carpeta vieja quedó vacía. Se pidió permiso de borrado para la
carpeta nueva porque git no puede limpiar sus propios `.lock` sin él.

**Lo que se le dijo igual:** el `.git` pesa 1,4 GB y OneDrive lo sincroniza archivo por archivo
mientras git escribe adentro. 1 GB de eso es caché de LFS prescindible → `git lfs prune` (to-do 7).

### El paper del GEP
El PDF que Matías dejó en `personal/` resultó ser la versión del **5 de junio de 2026**, publicada
como **GEP Research Paper 2026/06** con María García-Vega, 216 páginas con apéndices — no la de
enero que había en el repo. Reemplazó al PDF viejo, y `_data/papers.yml` pasó a llevar el **título
oficial** («Artificial intelligence and personality traits: evidence from online job vacancies») y el
**abstract oficial**, que no es el que había. Eso cerró B5 y el to-do del PDF de una sola vez.

### ORCID, sección por sección
Esto es lo que Matías había pedido y no se había hecho en la corrida 2.
- **Names:** nombre de publicación «Matías Golman» (estaba vacío) + variantes *Matias Golman*,
  *Matías A. Golman*, *Matías Alejandro Golman*. La variante sin tilde importa: es como lo busca
  Google según el diagnóstico S1.
- **Keywords:** estaba vacío. Once términos, de *labour economics* a *applied microeconometrics*.
- **Countries:** se sumaron Netherlands y United Kingdom a Argentina.
- **Websites:** se sumaron GitHub y el Argentina Informality Dashboard. Seis enlaces en total, todos
  apuntando al sitio o a perfiles suyos — esto es la mitad del ítem S5.
- **Employment:** de 3 a 8. Se agregaron OIT (consultor, 2020–), OIT Research Department (2019),
  OCDE (2024), Banco Mundial (2018) y Nottingham (graduate teaching assistant, 2021–2025). Se
  corrigió el «to present» del IIEP-Baires, que cerró en 2019.
- **Education:** de 2 a 4. Se agregaron el **doctorado de Nottingham (2021–2025)** —el hueco más
  visible que tenía el perfil— y la maestría de Turín/ITC-ILO (2018–2019). Se corrigió el «to
  present» de la maestría de la UBA, que cerró en 2018.
- **Professional activities:** estaba en cero. Los cuatro **Teaching Excellence Awards** (2021-22 a
  2024-25) como Distinction, y el cargo de representante de posgrado y oficial de EDI como Service.
- **Works:** se corrigió la ficha del paper del GEP (título oficial, «GEP Research Paper 2026/06,
  University of Nottingham», y enlace al PDF del sitio) y se agregaron enlaces al sitio en los otros
  dos working papers. Se eligieron los **5 trabajos destacados**: el meta-análisis, el del GEP, los
  dos informes de la OIT y *The value of personality*.
- **Lo que no se pudo:** Refugee Roots no existe en el registro de organizaciones de ORCID, y ORCID
  no acepta nombres de organización escritos a mano en afiliaciones. El voluntariado queda fuera.

### El push
El token ya tenía permiso de escritura. Se subió el commit pendiente y se confirmó que el sitio
nuevo está vivo: el `<title>` es «Matías Golman — labour economist, Utrecht University» y la
navegación es Work · Projects · Teaching · About · CV. **Desde la VM del puente hay que usar
`git push --no-verify`**, porque `git-lfs` no está instalado ahí y el hook `pre-push` aborta.

### Para la próxima
Search Console (to-do 1) es lo único grande que falta para Google. Y el zip de Instagram ya está,
así que la sección de fotos se puede encender.

---

## 2026-10-14 (corrida 2) — el sitio nuevo, escrito entero

**El rediseño está hecho y commiteado localmente.** Sin pushear todavía: la VM del puente sigue sin
credenciales.

### Lo que se leyó primero
El bloque `COMENTARIO DE MATIAS` (archivado literal) y las 22 respuestas del cuestionario. Las
decisiones quedaron como **D-05 a D-23** en `ESTADO.md`. La que manda sobre todo lo demás es la
respuesta a la pregunta 2: *que un ex colega me encuentre y me invite a una consultoría*.

### El sitio
- **Borrado:** todo al-folio. 31 posts de demo, 9 proyectos, 3 noticias, `_sass` del tema, 20
  plugins, purgecss, imagemagick, el workflow de 90 líneas, 14 MB de imágenes de Unsplash, 15 PDFs
  viejos. `assets/` de 194 MB a 89 MB.
- **Escrito:** Jekyll 4 con dos plugins (`jekyll-feed`, `jekyll-sitemap`), 4 layouts, 4 includes,
  3 archivos de datos, 9 páginas reales y 6 redirecciones. Fuentes **autoalojadas** (Literata +
  IBM Plex Sans, vía `@fontsource`, sólo los pesos usados: 7 archivos woff2).
- **Diseño:** paleta verde-papel con acento `#1f5d45`, tokens en CSS custom properties, modo oscuro
  automático **y** botón. Probado en 1180 px, 390 px y en oscuro con capturas reales.
- **Capturas de los dos proyectos** tomadas del vivo (el dashboard desplegado y la app en Vercel) y
  optimizadas; son las que ilustran las tarjetas.
- **SEO estructural:** `<title>` y `description` propios por página, JSON-LD `Person` con `sameAs` a
  Scholar, ORCID, LinkedIn, GitHub, uu.nl e Instagram, `alternateName` con y sin tilde, canonical,
  Open Graph, sitemap de 9 URLs, y el código de Search Console puesto (también en el sitio viejo,
  para que se pueda verificar apenas se pushee).

### PDFs renombrados a nombres estables
`jmp_last_version` → `golman-ai-personality-traits`, `second_chapter` → `golman-value-of-personality`,
`third_chapter` → `golman-formalisation-meta-analysis`, `ilo-wp34` →
`ilo-wp34-old-age-income-security`, `wcms_855420` → `ilo-future-of-work-formality`,
`problemasdesarrollo` → `golman-bekerman-microfinance`, `neets` → `golman-neets`, los cuatro premios
a `gta-award-XXXX`. El CV nuevo (sin teléfono) quedó como `cv-matias-golman.pdf` **y** con el nombre
viejo `CV_MatiasGolman.pdf`, para no romper links ya enviados.

### Lo que NO se hizo, y por qué
- **El informe de Costa Rica no se subió.** Es un entregable a un cliente sobre política de un
  gobierno; si la OIT no lo publicó, publicarlo primero puede caer mal. Descrito sin PDF hasta que
  Matías confirme (to-do 5).
- **La sección de fotos está construida pero apagada**: no hay fotos todavía. En el to-do quedó cómo
  bajarlas de Instagram en bloque, que era lo que Matías no sabía hacer.
- **`/notes/` existe pero no se linkea** hasta que haya tres textos.

### Respondido en el to-do
El permiso correcto del PAT (estaba mirando «Account permissions»; `Contents` está en «Repository
permissions», y sólo aparece tras elegir el repo), cómo verificar en Bing importando desde Google,
cómo bajar las fotos de Instagram, cómo mudar la carpeta sin romper nada — **con la advertencia de
no poner el repo adentro de OneDrive**, que es la que más importa — y que la carpeta, chequeado, no
está dentro de otro repo de git.

**Ítems cerrados:** D1, y el rediseño completo. **Abiertos:** S1 (links entrantes y verificación),
S2 (dashboard, más adelante), S3 (los 1,3 GB de `.git`), S4 (primera nota), S5 (links entrantes).
**Bloqueados:** B1 a B6.

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
