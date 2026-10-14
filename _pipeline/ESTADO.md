# ESTADO DEL SITIO PERSONAL — leer esto PRIMERO

> **Fuente de verdad del proyecto web.** Toda corrida arranca leyendo, en este orden: el bloque
> `COMENTARIO DE MATIAS`, `En una pantalla`, la `COLA DE TRABAJO`, y `To-Do-Matias.md`.
> Las reglas de higiene de estos archivos están en `LEEME.md` y son parte del trabajo.

**Última actualización:** 2026-10-14 (corrida 4)
**Actualizado por:** Claude
**Fase actual:** Fase 2 — el sitio está vivo y ahora es **bilingüe completo**. Esta corrida sacó
el lenguaje de IA, devolvió el About original, ensanchó el layout, ordenó el repo, encendió
`/photography/` con 246 fotos y tradujo las diez páginas al castellano.

---

## COMENTARIO DE MATIAS

*(vacío — dejame acá lo que quieras que haga la próxima corrida. La corrida lo lee primero, lo
archiva literal en `_archivo/Comentarios_Matias.md` y vuelve a vaciar el bloque.)*

---

## En una pantalla

**Esta corrida atacó los ocho puntos del comentario del 14/10.** El sitio estaba bien armado pero
sonaba a máquina, y ése era el problema de fondo: Matías no se reconocía en su propio sitio.

- **El About es otra vez el personal statement original, literal.** A mitad de la corrida Matías
  pidió el original crudo para trabajarlo él. Se recuperó `_pages/personalstatement.md` del tag
  `v1-academic-jmp-2025` y se pegó **verbatim**, incluidos «I appreciate your interest in my work
  trajectory» y el párrafo de «If I were on the hiring side». Lo único que se tocó son los tres
  `---` que kramdown convertía en em dash. **Queda pendiente de su mano**: el texto todavía le
  habla a un empleador, que es justo lo que el sitio no quiere decir (D-03).
- **Cero em dashes en todo el sitio**, y fuera las estructuras de dos puntos que anticipan. Se
  revisaron las nueve páginas, los dos archivos de datos, el footer y los títulos.
- **Fuera el tono comercial.** No queda ninguna mención a clientes. El standfirst de `/work/` ya no
  dice que la política es «donde fue la mayor parte de mi tiempo» ni a qué apuntaría primero.
- **El titular de la home sale del About:** «I am a labour economist. I work on how to create jobs
  that allow people to have a decent and fulfilling life.» Es su frase del viaje en micro de 21
  horas, no una promesa de valor.
- **Layout más ancho y foto más grande.** El marco pasó de 62rem a 74rem, los márgenes de 2,5rem a
  2rem, y la foto de 10rem a 15rem. El dashboard y Araucaria quedaron lado a lado.
- **`/work/` quedó pareja:** las tres secciones usan la misma jerarquía (título, línea de contexto
  en sans chica, párrafo en serif). Se escribió un párrafo para cada paper publicado, que antes
  quedaban en una línea. **Published subió por encima de Policy**, para que la investigación quede
  junta. Se sumó el paper de tenure premia como *work in progress*.
- **`/teaching/` rehecha con los siete módulos**, ordenada por período lectivo, con descripciones
  sacadas de los manuales de OSIRIS. Integrating Insights quedó afuera.
- **About es el primer ítem del nav**, y «Projects» pasó a llamarse «Things I've built».
- **Segunda tanda, pedida sobre la marcha:** la home quedó ordenada *What I work on → Current work
  → Things I've built*; el **tema oscuro pasó a ser el de fábrica** (el claro sigue a un clic, y la
  elección se recuerda); y en el About cambiaron las dos líneas que pidió.

**El sitio es bilingüe de verdad, no sólo la portada.** Las diez páginas existen en los dos
idiomas y el selector de idioma está **arriba, en la barra de navegación**, separado del menú por
una línea. Cada página conoce a su par (`alt_url` en el front matter), así que el selector lleva a
la página equivalente y no a la portada, y los `hreflang` lo declaran para Google. Los textos de
interfaz viven en `_data/i18n.yml` y los contenidos en `papers_es.yml`, `projects_es.yml` y
`cv_es.yml`. El orden del menú pasó a ser *About · Work · Teaching · CV · Things I've built ·
Photography*: primero lo de trabajo, después lo demás.

**`/photography/` está encendida, con 246 fotos.** El zip de Instagram se pudo abrir recién cuando
Matías lo bajó de OneDrive. De las 379 fotos de publicaciones se clasificaron las tres categorías a
ojo, hoja de contacto por hoja de contacto: **246 de naturaleza** (sin gente, o con él solo y
lejos) van al sitio; **82 con gente** y **51 que no son naturaleza** quedaron en
`personal/_revisar_fotos/`, fuera del repo, para que él las mire. Las del sitio están a 720 px y
calidad 70, que son 25 MB en total y ~100 KB cada una, con `loading="lazy"`.

**El repo bajó de 1,4 GB a 375 MB.** `git lfs` no está instalado en la VM del puente, así que en vez
de `git lfs prune` se borró `.git/lfs/objects` a mano: eran 1.022 MB de versiones viejas de los JSON
del dashboard, que ya no existen en el árbol de trabajo (ningún archivo usa LFS hoy) y que están en
GitHub igual. También se borraron los restos de al-folio en `.github/` (plantillas de issues,
`release.yml`, `stale.yml`, que apuntaban al repo de otra gente) y el `.gitattributes` nuevo frena
el churn de CRLF que amenazaba con meter un diff de 73 MB.

**El código de Search Console estaba desde el principio.** `4v_RtVj-MRC238cDUQl3VPdihKXF3uZXfXrp2WzUf_k`,
ya puesto en `_config.yml` y servido en el `<head>`. No hace falta pedirlo de nuevo: sólo entrar y
darle «Verificar».

## COLA DE TRABAJO

*(Abiertos arriba. Un ítem que se cierra se reduce a una línea y el detalle se archiva.)*

### Bloqueado por Matías

- **B3 — ¿El informe de Costa Rica es público?** (to-do 2). Hoy está descrito sin PDF.
- **B8 — La carpeta vieja de `Documents\GitHub\...`.** Pedí permiso para borrarla y me lo denegó el
  clasificador de la sesión. Son 30 segundos a mano (to-do 4).

### Abiertos

- **S1 — Google todavía no indexa el sitio.** La etiqueta de verificación **ya está servida en el
  `<head>`**. Falta que Matías entre a Search Console y le dé «Verificar»; después yo mando el
  sitemap y pido la indexación de la home. Bing ya lo tiene.
- **S5 — Links entrantes.** ORCID está hecho. Faltan: la ficha de uu.nl, el «Homepage» del perfil de
  Scholar, el research-portal de Utrecht y la firma de los papers.
- **S6 — Alt text de las 246 fotos.** Hoy van con `alt=""` y una descripción del conjunto en el
  `aria-label` de la galería, porque no hay forma de describir 246 imágenes una por una en una
  corrida. Si le importa la accesibilidad fina, hay que escribirlos a mano o recortar la selección.
- **S11 — Las 82 fotos con gente.** Están en `personal/_revisar_fotos/con-gente/`. Él dijo que iba
  a mirar si hay alguna que sí quiere. Cuando la haya, se agrega al manifiesto y listo.
- **S8 — ¿«Things I've built» es el nombre bueno?** Es la decisión que tomé esta corrida sobre la
  duda del punto 6. Descarté «Data projects» porque Araucaria no es un proyecto de datos en el
  sentido en que lo es el dashboard, y porque suena a categoría de portfolio. Si no le cierra, el
  cambio es una línea en `_includes/header.html` y otra en `projects.md`.
- **S12 — El About en castellano es una traducción, no un original.** Matías escribió el personal
  statement en inglés y lo va a reescribir él. Cuando lo haga, hay que volver a traducir
  `es/sobre-mi.md`, que hoy sigue al inglés párrafo por párrafo.
- **S10 — El About le habla a un empleador.** Es la versión original, tal como la pidió, y la va a
  trabajar él. Mientras tanto el sitio tiene un texto que dice «If I were on the hiring side of the
  equation», lo que choca con D-03 (la búsqueda es implícita). No tocarlo sin que él avise.
- **S9 — Roles de docencia.** Matías dijo que da clase y tutoriales «en muchos» pero no cuál en
  cuál. La página hoy lo dice en general, en el standfirst. Si quiere el rol por módulo, hay que
  preguntárselo.
- **S2 — El dashboard, más adelante (proyecto aparte).** Se queda como está. Cuando se retome:
  separar datos de presentación (los 71 MB son datos embebidos en el HTML), rehacer la interfaz con
  la paleta del sitio, sacar los emojis de los iconos de sector, y evaluar sumar países.
- **S4 — Primera nota para `/notes/`.** Las conclusiones del meta-análisis en castellano llano,
  600-900 palabras. Faltan otras dos para encender la sección.

### Cerrados

- **B7 — El zip de Instagram.** Cerrado 14/10: Matías lo bajó y se procesaron las 379 fotos.
- **S3 — Limpieza del repo.** Cerrado 14/10: 1,4 GB → 375 MB, borrando la caché muerta de Git LFS.
- **S7 — Líneas CRLF.** Cerrado 14/10: `.gitattributes` nuevo y restos de al-folio eliminados.
- **B4 — Versiones finales de los papers.** Cerrado 14/10: Matías confirmó que las tres son finales.
- **B9 — Los siete manuales de curso.** Cerrado 14/10: contestó cuáles dicta y en qué período.
- **B1/B2 — Pushear y el token.** Cerrado 14/10. Desde la VM del puente hay que usar
  `git push --no-verify`.
- **B5 — El paper del GEP.** Cerrado 14/10: GEP Research Paper 2026/06, con María García-Vega.
- **B6 — ORCID.** Cerrado 14/10: perfil completo, sección por sección.
- **La mudanza de la carpeta.** Cerrada 14/10: el repo vive en OneDrive, verificado con `git fsck`.
- **R1 — Reconocimiento** y **R2 — Pipeline creado.** Cerrados 13/10.
- **R3 — Backup de la versión vieja.** Cerrado 13/10: tag `v1-academic-jmp-2025`, rama
  `backup/v1-academic-jmp-2025` y `_archivo/snapshot_contenido_v1_20261013.tar.gz`.

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
