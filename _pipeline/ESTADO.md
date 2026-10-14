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

> **Nunca pegues acá un token, una contraseña ni una clave.** Este archivo se sube a GitHub. Si
> tenés que pasarme una credencial, escribila en `_pipeline/.github_token`, que git ignora.



---

## En una pantalla

**El sitio está reescrito entero y commiteado localmente. Falta pushear** (to-do 1), y en cuanto
pushees se despliega solo. El de al-folio ya no existe en la carpeta.

**Qué hay ahora.** Jekyll propio y mínimo: 9 URLs reales, todas con contenido propio.
`/` (posicionamiento + las dos herramientas + working papers + temas) · `/work/` (working papers,
trabajo de política, publicados) · `/projects/` · `/teaching/` · `/about/` (el statement reescrito
sin el marco de postulación) · `/cv/` (página HTML + PDF) · `/es/` · `/dashboard/` (misma URL de
siempre, ahora con texto y links propios) · `/araucariaspotter/`. `/notes/` existe pero no está en
la navegación ni en el sitemap hasta que haya tres textos. Redirecciones desde las seis URLs viejas.

**Qué desapareció.** Los 31 posts de demo, los 9 proyectos de demo, las 3 noticias, el
`scholar.last_name: [Einstein]`, los veinte plugins de Ruby, purgecss, imagemagick, el workflow de
90 líneas, 14 MB de fotos de Unsplash, y 15 PDFs viejos (nueve JMP y cuatro CV). `assets/` pasó de
194 MB a **89 MB**, y de esos 73 MB son el dashboard.

**Diseño.** Editorial y cálido, como se decidió: **Literata** para leer y **IBM Plex Sans** para
etiquetas y navegación, las dos **autoalojadas** (nada de Google Fonts, nada de GDPR). Papel verde
muy pálido `#f6f8f4`, tinta `#16211b`, acento **verde conífera `#1f5d45`** — el mismo verde de tu
campera en la foto de portada, que es de donde salió. **Modo oscuro: lo hice.** Sigue al sistema
operativo y además hay un botón en la navegación. Tenías razón en que se ve serio; con tokens de
color costaba una hora, así que lo discutí mal la primera vez.

**Lo que decide la portada.** Tu respuesta a la pregunta 2 — *que un ex colega te encuentre y te
invite a una consultoría* — es el norte de todo el sitio. Por eso arriba va una frase que dice qué
hacés, después **las dos cosas que construiste** (que para ese lector prueban más que los papers), y
una línea que dice que estás abierto a consultorías y colaboraciones, sin decir en ningún lado que
estás buscando trabajo.

## COLA DE TRABAJO

*(Abiertos arriba. Un ítem que se cierra se reduce a una línea y el detalle se archiva.)*

### Bloqueado por Matías

- **B1 — Pushear** (to-do 1). Hasta que no pushees, el sitio nuevo vive sólo en tu disco.
- **B2 — El token**, para que pueda desplegar y verificar yo (to-do 1).
- **B3 — ¿El informe de Costa Rica es público?** (to-do 5). Hoy está descrito sin PDF.
- **B4 — Las versiones finales de los tres papers** (to-do 4). Mientras tanto están las que había en
  el repo (`jmp_last_version`, `second_chapter`, `third_chapter`), renombradas.
- **B5 — El paper del GEP**: ¿número de serie y coautoría con María García-Vega? (to-do 6).
- **B6 — ORCID**: decime que sí y lo actualizo (to-do 8).

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

- **S2 — El dashboard, más adelante (proyecto aparte, pedido explícito de Matías).** Se queda como
  está. Cuando lo retomemos: separar datos de presentación (los 73 MB son datos embebidos en el
  HTML, y eso se reduce muchísimo con JSON + carga por demanda, sin perder ni una serie),
  rehacer la interfaz para que acompañe la paleta del sitio, sacar los emojis de los iconos de
  sector, y evaluar sumar países. **Matías tiene el código y las bases.**

- **S4 — Primera nota para `/notes/`.** El texto acordado: las conclusiones del meta-análisis de
  formalización en castellano llano, 600-900 palabras. Material: `golman-formalisation-meta-analysis.pdf`.
  Faltan otras dos para encender la sección.

- **S5 — Links entrantes** (la mitad que falta del arreglo de Google, y la más lenta). Donde Matías
  controla: la ficha de uu.nl, el perfil de Scholar («Homepage»), ORCID, GitHub, LinkedIn, el
  research-portal de Utrecht, y la firma de los papers. Ninguno cuesta dinero.

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

**2026-10-13, respondidas por Matías en el chat (preguntas 1, 16, 3 y 19 del cuestionario):**

- **D-01 · Público.** Los dos primeros son **organismos internacionales** (OIT, BM, OCDE, BID,
  CEPAL) **e institutos holandeses de política** (CPB, SCP, SEO, Ecorys, DNB, TNO). Lo académico
  queda presente pero **no manda**. Consecuencia directa: la home no abre con papers, abre con
  posicionamiento y con productos; los dos proyectos (dashboard y Araucaria) suben; el JMP deja de
  llamarse JMP.
- **D-02 · Registro visual.** **Editorial + cálido**: serif de lectura, columna angosta, mucho
  aire, un verde profundo sacado de sus propias fotos de montaña, proyectos como tarjetas con
  imagen. Nada de azul institucional, nada de modo oscuro automático, tipografías autoalojadas.
- **D-03 · Búsqueda de trabajo: implícita.** El sitio **no** dice que está buscando. CV al día,
  perfil orientado a política, y la señal de disponibilidad va por el ajuste privado de LinkedIn.
  Nada de «open to opportunities» en la web.
- **D-04 · Stack: Jekyll propio y mínimo**, en el mismo repo y en GitHub Pages. Se borra la demo de
  al-folio entera, se escriben ~5 layouts a medida, sin plugins salvo `jekyll-sitemap` y
  `jekyll-feed`. Esto además es la mitad del arreglo de Google (ítem S1).

**2026-10-14, del cuestionario contestado (preguntas 2 y 4-22):**

- **D-05 · El objetivo del sitio, en una sola frase:** que un ex colega lo encuentre y lo invite a
  una consultoría. Es el criterio con el que se resuelve cualquier duda de jerarquía.
- **D-06 · Matiz sobre el público:** en los organismos internacionales el primer contacto no es
  RRHH, es alguien que ya lo conoce. El sitio no tiene que convencer a un desconocido desde cero:
  tiene que **recordarle a alguien que ya lo conoce qué sabe hacer**, y ser fácil de reenviar.
- **D-07 · Dominio:** se queda en `matiasgolman.github.io` por ahora. Revisar cuando el sitio tenga
  contenido propio acumulado y notas publicadas.
- **D-08 · Idiomas:** inglés + una página `/es/`. No bilingüe completo.
- **D-09 · Posicionamiento:** economista laboral con **amplitud explícita** — el sitio dice que el
  método viaja a desigualdad, pobreza, migración, salario mínimo, educación, política industrial.
- **D-10 · Papers:** fuera la etiqueta «job market paper». Los tres son working papers.
- **D-11 · PDFs:** una sola versión estable de cada uno, con nombre que no cambia nunca más
  (`golman-ai-personality-traits.pdf`, etc.). Las 15 versiones viejas, borradas.
- **D-12 · Dashboard:** se queda como está (es la versión final, 73 MB). Mejorarlo —interfaz, datos,
  más países— es un proyecto aparte, **no en esta conversación**. Anotado como ítem S2.
- **D-13 · Araucaria:** URL buena `https://araucaria-spotter.vercel.app/`. *(La página vieja
  apuntaba a `araucaria-spotter-eyna.vercel.app`, que quedó obsoleta.)*
- **D-14 · Fotos:** sección propia, pero **apagada** hasta que haya fotos. No «fotógrafo»: viaje y
  naturaleza. Instagram público queda linkeado en el pie.
- **D-15 · Notas:** se llama «Notes», existe, y **no se linkea hasta que haya tres textos**.
  Primer texto acordado: las conclusiones del meta-análisis en castellano llano.
- **D-16 · Nada que ocultar**, pero el CV público pasa a ser el nuevo (sin teléfono, dirección
  Utrecht).
- **D-17 · «Personal statement» → «About»**, conservando casi todo el texto y sacando el marco de
  postulación. Se agregó la línea de apertura a proyectos.
- **D-18 · Docencia:** Utrecht arriba, Nottingham condensado, premios conservados.
- **D-19 · CV:** página HTML + botón de descarga del PDF.
- **D-20 · Foto:** la actual, chica, al costado del titular.
- **D-21 · Modo oscuro: SÍ** (sigue al sistema + botón). Matías tenía razón; la objeción original
  era de costo de mantenimiento y con tokens de color ese costo no existe.
- **D-22 · Analítica:** GoatCounter, sólo si es gratis. Pendiente de que Matías cree la cuenta.
- **D-23 · Ritmo:** aprobar antes de publicar durante el rediseño, con preview. Después, autónomo.
