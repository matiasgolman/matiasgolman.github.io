# ESTADO DEL SITIO PERSONAL — leer esto PRIMERO

> **Fuente de verdad del proyecto web.** Toda corrida arranca leyendo, en este orden: el bloque
> `COMENTARIO DE MATIAS`, `En una pantalla`, la `COLA DE TRABAJO`, y `To-Do-Matias.md`.
> Las reglas de higiene de estos archivos están en `LEEME.md` y son parte del trabajo.

**Última actualización:** 2026-10-14 (corrida 3)
**Actualizado por:** Claude
**Fase actual:** Fase 2 — **EL SITIO NUEVO ESTÁ VIVO Y PUSHEADO.** Queda la difusión: Search
Console, links entrantes y las notas. El repo vive ahora en OneDrive.

---

## COMENTARIO DE MATIAS

*(vacío — dejame acá lo que quieras que haga la próxima corrida. La corrida lo lee primero, lo
archiva literal en `_archivo/Comentarios_Matias.md` y vuelve a vaciar el bloque.)*

> **Nunca pegues acá un token, una contraseña ni una clave.** Este archivo se sube a GitHub. Si
> tenés que pasarme una credencial, escribila en `_pipeline/.github_token`, que git ignora.

---

## En una pantalla

**El sitio nuevo está vivo y todo está pusheado.** `matiasgolman.github.io` ya sirve la versión
reescrita: el titular es la frase de posicionamiento, la navegación es Work · Projects · Teaching ·
About · CV, y no queda nada del marco de job market. El token quedó con permiso de escritura y el
push funciona desde acá (con `--no-verify`, porque el hook de Git LFS no corre en la VM del puente).

**La carpeta se mudó a OneDrive.** El repo entero vive ahora en
`C:\Users\matia\OneDrive - Universiteit Utrecht\Documents\personal\matiasgolman.github.io`:
1,4 GB, copia idéntica archivo por archivo, `git fsck` limpio, ramas y tags intactos. La carpeta
vieja de `Documents\GitHub\...` quedó vacía y la podés borrar a mano. **Cuidado conocido:** el
`.git` pesa 1,4 GB (1 GB es caché de Git LFS) y OneDrive lo sincroniza archivo por archivo mientras
git escribe adentro. Si algún día aparece un `.lock` fantasma o un objeto corrupto, la salida es
`git lfs prune` y, si hace falta, clonar de nuevo desde GitHub.

**El paper con María es el de la serie GEP.** El PDF que dejaste en `personal/` es la versión del
5 de junio de 2026, **GEP Research Paper 2026/06** (216 páginas con apéndices). Reemplazó al de
enero en el sitio, y la ficha de `/work/` ahora lleva el título y el abstract oficiales. Eso cierra
de una vez el pendiente del PDF y la pregunta del número de serie.

**ORCID quedó completo, sección por sección.** Nombre de publicación «Matías Golman» más tres
variantes · 11 keywords (estaba vacío) · tres países · seis enlaces, con GitHub y el dashboard ·
**8 empleos** (se sumaron OIT consultor, OIT Research Department, OCDE, Banco Mundial y Nottingham;
se cerró el «to present» del IIEP) · **4 titulaciones** (se sumaron el doctorado de Nottingham y la
maestría de Turín; se cerró el «to present» de la maestría de la UBA) · **5 actividades
profesionales** (los cuatro Teaching Excellence Awards y el cargo de representante de posgrado y
EDI) · los nueve trabajos, con el del GEP corregido y enlaces a los PDFs del sitio · **5 trabajos
destacados**. El dashboard **no se borró nunca**: sigue en `/dashboard/`, con sus 71 MB; lo único
que se hizo fue sacarlo del sitemap, porque un HTML de 73 MB en el sitemap perjudica el rastreo.

## COLA DE TRABAJO

*(Abiertos arriba. Un ítem que se cierra se reduce a una línea y el detalle se archiva.)*

### Bloqueado por Matías

- **B3 — ¿El informe de Costa Rica es público?** (to-do 2). Hoy está descrito sin PDF.
- **B4 — Las versiones finales del segundo y el tercer paper** (to-do 3). El del GEP ya está al día.

### Abiertos

- **S1 — Google todavía no indexa el sitio.** El diagnóstico de la corrida 1 sigue en pie, pero la
  causa principal —que el sitio era la demo de al-folio— ya no existe: hay contenido propio en las
  nueve URLs. Falta la otra mitad: **Search Console** (verificar y mandar el sitemap, pedir
  indexación de la home a mano) y los **links entrantes** (S5). Bing ya lo tiene.
- **S5 — Links entrantes.** **ORCID ya está hecho** y apunta al sitio, a Scholar, a LinkedIn, a
  uu.nl, a GitHub y al dashboard. Faltan: la ficha de uu.nl, el «Homepage» del perfil de Scholar,
  el research-portal de Utrecht y la firma de los papers.
- **S6 — Las fotos.** El zip de Instagram (1,4 GB) ya está en `personal/`. La sección está
  construida y apagada; se enciende cuando se elijan las fotos. Siguiente paso: abrir el zip,
  elegir diez o doce de viaje y naturaleza, y reducirlas.
- **S2 — El dashboard, más adelante (proyecto aparte).** Se queda como está. Cuando se retome:
  separar datos de presentación (los 71 MB son datos embebidos en el HTML), rehacer la interfaz con
  la paleta del sitio, sacar los emojis de los iconos de sector, y evaluar sumar países.
- **S4 — Primera nota para `/notes/`.** Las conclusiones del meta-análisis en castellano llano,
  600-900 palabras. Faltan otras dos para encender la sección.
- **S3 — Limpieza del repo.** El `.git` pesa 1,4 GB y **1 GB es caché de Git LFS** de versiones
  viejas de los JSON del dashboard, que también están en GitHub. `git lfs prune` lo baja a ~400 MB
  sin perder nada. Es la forma barata de resolver el problema de espacio que motivó la mudanza.
- **S7 — Líneas CRLF en `.github/` y en el dashboard.** `git status` marca siete archivos como
  modificados y el diff es sólo fin de línea. Es anterior a la mudanza y es inofensivo, pero si se
  commitea por error mete un diff de 73 MB. No tocar sin decidir qué hacer con `.gitattributes`.

### Cerrados

- **B1/B2 — Pushear y el token.** Cerrado 14/10: el token quedó con permiso de escritura y el sitio
  nuevo está desplegado. Desde la VM del puente hay que usar `git push --no-verify`.
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
