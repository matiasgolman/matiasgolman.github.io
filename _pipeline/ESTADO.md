# ESTADO DEL SITIO PERSONAL — leer esto PRIMERO

> **Fuente de verdad del proyecto web.** Toda corrida arranca leyendo, en este orden: el bloque
> `COMENTARIO DE MATIAS`, `En una pantalla`, la `COLA DE TRABAJO`, y `To-Do-Matias.md`.
> Las reglas de higiene de estos archivos están en `LEEME.md` y son parte del trabajo.

**Última actualización:** 2026-10-13 (corrida 1, reconocimiento)
**Actualizado por:** Claude
**Fase actual:** Fase 0 — **RECONOCIMIENTO Y DECISIONES**. Nada del sitio tocado todavía, salvo
esta carpeta. El sitio vivo sigue siendo la versión de junio 2026 (job market). Esperando las
respuestas del cuestionario `preguntas/Preguntas_01_estructura_y_diseno.md` para abrir la Fase 1.

---

## COMENTARIO DE MATIAS

*(vacío — dejame acá lo que quieras que haga la próxima corrida. La corrida lo lee primero, lo
archiva literal en `_archivo/Comentarios_Matias.md` y vuelve a vaciar el bloque.)*



---

## En una pantalla

**Qué es el sitio hoy.** `matiasgolman.github.io` es el tema **al-folio** (Jekyll), clonado casi
entero, con cinco páginas propias encima: `about`, `teaching`, `policy papers`,
`personal statement`, `other projects`, más `cv` (que es un link directo al PDF) y dos páginas
sueltas (`/dashboard/` y `/araucariaspotter/`). Último deploy: **19 de junio de 2026**.

**El diagnóstico duro: el sitio es, en su mayor parte, la demo del tema.** Del contenido que
Google ve, lo propio es minoría:

| En el sitio hoy | Cantidad | Qué es |
|---|---|---|
| Posts de blog | **31** | **Todos** demo de al-folio (`formatting-and-links`, `tikzjax`, `the_godfather`…) |
| Proyectos | **9** | **Todos** demo (`project 1`, `project 2`… con fotos de Unsplash) |
| Noticias | **3** | **Todas** demo (`announcement_1/2/3`) |
| Páginas propias | 5 + 2 | about, teaching, policy papers, personal statement, other projects |

Además: `scholar.last_name` en `_config.yml` sigue diciendo **`[Einstein]`**; `keywords` son las
del tema (`jekyll, jekyll-theme, academic-website…`); `external_sources` trae el feed de Medium de
al-folio y una nota del blog de Google; la página `repositories` tiene como descripción el texto de
instrucciones del tema. El `about` dice que es **PhD candidate en Nottingham** y que está
**disponible para entrevistas en el job market 2025/26** — ocho meses desactualizado.

**Peso y salud del repo.** 1,5 GB en total: **1,3 GB de `.git`** y **194 MB de `assets/`**, de los
cuales `assets/dashboards/argentina_informality_dashboard.html` es **un solo archivo de 73 MB** y
`assets/pdf/` son 61 MB con **nueve versiones del JMP** (`jmp_june25` … `jmp_last_version`) y
cuatro CV viejos. Las páginas `/dashboard/` y `/araucariaspotter/` declaran `layout: single`, que
**no existe** en al-folio (es de minimal-mistakes): se renderizan sin layout.

**Por qué no aparece en Google.** Porque **no está indexado**: de todo el sitio, Google tiene una
sola página (`/dashboard/`), y es justamente la única que no es plantilla. Verificado en Google el
13/10. Detalle y plan en el ítem **S1** de la cola.

**A dónde va.** El objetivo del sitio cambia: dejar de ser una carpeta de job market académico y
pasar a ser la tarjeta de presentación de un economista laboral que produce evidencia usable para
política pública — el público que importa es quien contrata en OIT / BM / OCDE / CPB / SCP / SEO /
Ecorys y gente que lo googlea 90 segundos antes de una reunión.

---

## COLA DE TRABAJO

*(Abiertos arriba. Un ítem que se cierra se reduce a una línea y el detalle se archiva.)*

### Bloqueado por decisiones de Matías

- **D1 — Cuestionario 1 (estructura y diseño).** 22 preguntas en
  `preguntas/Preguntas_01_estructura_y_diseno.md`. Bloquea todo lo demás.
  Las cuatro de mayor impacto se preguntaron directo en el chat del 13/10: público principal,
  registro visual, cuán explícito ser sobre la búsqueda de trabajo, y stack.

### Abiertos

- **S1 — Por qué no aparece en Google. VERIFICADO EN GOOGLE, 13/10.** La intuición de Matías era
  correcta y mi primera lectura estaba equivocada: **el sitio no está indexado**. No es que rankee
  bajo — Google no lo tiene.
  - `site:matiasgolman.github.io` devuelve **UNA sola página de todo el sitio: `/dashboard/`**.
    Ni la home, ni about, ni publications, ni teaching, ni policy papers.
  - Buscar la frase exacta de la home («I am available for interviews in the 2025/26 Job Market»)
    devuelve **«No results found»**. La home no está en el índice.
  - Buscar `"Matias Golman"` (sin tilde) en Google: salen ResearchGate, Facebook, X, Instagram,
    Academia.edu, la página de doctorandos de Richard Upward, el CV alojado en economicas.uba.ar y
    EconStor. **El sitio propio no aparece.** Con tilde salen uu.nl, LinkedIn, Scholar,
    research-portal, ResearchGate, Worktribe, Nottingham. Tampoco.
  - En cambio **otros buscadores sí lo tienen** (aparece en los resultados de búsqueda web de esta
    sesión). O sea: es crawleable, y la decisión de no indexarlo es **de Google**.
  - **Lo técnico está bien y no es el problema:** `robots.txt` permite todo, hay `sitemap.xml` con
    ~50 URLs, hay `canonical`, **no** hay `noindex` ni cabecera `X-Robots-Tag`, y GitHub Pages
    responde 200. Revisado el 13/10.
  - **La hipótesis que explica el patrón, y el dato que la sostiene:** la única página indexada es
    **la única que no es plantilla**. `/dashboard/` tiene contenido propio y en castellano; todo el
    resto del sitio es, para un crawler, la demo de al-folio (31 posts, 9 proyectos, 3 noticias,
    idénticos a miles de sitios) más cinco páginas cortas envueltas en ese mismo molde. Esto es el
    caso de manual de **«Crawled – currently not indexed»**: Google pasó, miró y decidió que no
    valía el lugar en el índice. Lo agravan tres cosas: **cero links entrantes** (LinkedIn pone
    `nofollow`; uu.nl no linkea al sitio; el único link real es el «Homepage» del perfil de
    Scholar), **metadatos de plantilla** (`<title>` «Matías Golman | about», `keywords` de
    al-folio), y **sin Search Console**, así que nunca hubo ni sitemap enviado ni informe.
  - **Esto cambia la prioridad del rediseño.** No vamos a «mejorar el SEO» de un sitio existente:
    vamos a **darle a Google un sitio que valga la pena indexar**, que es exactamente el rediseño
    que Matías pidió por otros motivos. Las dos cosas son el mismo trabajo.
  - **Plan (se ejecuta junto con el rediseño):** (1) borrar las 43 URLs de demo — es la pieza más
    importante y es gratis; (2) contenido propio y sustancial en cada página que quede; (3) título,
    descripción y `keywords` reales, distintos por página; (4) JSON-LD `Person` con `sameAs` a
    Scholar, LinkedIn, ORCID, GitHub, uu.nl; (5) **Search Console**, verificar y mandar el sitemap
    (to-do de Matías, ítem 4) y pedir indexación de la home a mano; (6) links entrantes desde donde
    Matías controla: la ficha de uu.nl, el perfil de Scholar, GitHub, ORCID, LinkedIn, las firmas
    de los papers. Más, si se decide, dominio propio (to-do ítem 7).

- **S2 — Decidir el destino del dashboard de 73 MB.** Hoy es un HTML monolítico dentro del repo.
  Carga lentísimo, infla el repo y Jekyll lo tiene que excluir a mano. Opciones: dejarlo igual,
  partirlo (datos en JSON + página liviana), o moverlo a su propio repo/host. Pregunta 9.

- **S3 — Limpieza del repo (1,3 GB de `.git`).** Decidir si se hace `git gc` agresivo, si se
  depuran los nueve JMP y los CV viejos, o si conviene empezar un repo nuevo y dejar el viejo como
  archivo. Ojo: reescribir historia rompe los links directos a PDFs viejos si alguien los guardó.

### Cerrados

- **R1 — Reconocimiento completo del repo, el sitio desplegado, el CV, el LinkedIn y la lista de
  lugares.** Cerrado 13/10. Resumen en `En una pantalla`.
- **R2 — Pipeline creado** (`_pipeline/`, cuatro archivos + archivo + preguntas), excluido del
  build. Cerrado 13/10.
- **R3 — Backup de la versión vieja.** Cerrado 13/10: tag `v1-academic-jmp-2025` y rama
  `backup/v1-academic-jmp-2025` apuntando a `4462cb1`, más
  `_archivo/snapshot_contenido_v1_20261013.tar.gz` (3,8 MB, todo el contenido y las plantillas sin
  `assets/`). **Falta pushear el tag y la rama** → `To-Do-Matias.md` ítem 1.

---

## DECISIONES TOMADAS

*(Se anotan acá para no rediscutirlas. Cada una con fecha y de quién salió.)*

- *(todavía ninguna — el cuestionario 1 las va a poblar)*
