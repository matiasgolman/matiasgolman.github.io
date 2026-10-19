# ESTADO DEL SITIO PERSONAL — leer esto PRIMERO

> **Fuente de verdad del proyecto web.** Toda corrida arranca leyendo, en este orden: el bloque
> `COMENTARIO DE MATIAS`, `En una pantalla`, la `COLA DE TRABAJO`, y `To-Do-Matias.md`.
> Las reglas de higiene de estos archivos están en `LEEME.md` y son parte del trabajo.

**Última actualización:** 2026-10-18 (corrida 6)
**Actualizado por:** Claude
**Fase actual:** Fase 3 — el sitio está vivo y bilingüe, y empezó el trabajo sobre las
herramientas. Esta corrida **rehizo el panel de informalidad de punta a punta**: datos separados
del HTML, interfaz con la tipografía y la paleta del sitio, y el embebido que ya no atrapa el
scroll.

---

## COMENTARIO DE MATIAS

*(vacío — dejame acá lo que quieras que haga la próxima corrida. La corrida lo lee primero, lo
archiva literal en `_archivo/Comentarios_Matias.md` y vuelve a vaciar el bloque.)*

---

## En una pantalla

> **CORRIDA 6 — CERRADA (18/10).** El panel tiene datos nuevos hasta **1T 2026** con la limpieza
> nueva. Los datos los arma `proyectos\mapa_informalidad\mapa_informalidad.do` (Stata) a partir de
> `cross_paneles.dta` y los escribe como CSV en `assets/data/informality/` más `meta.json`; lo
> corre solo `master_construccion.do` al final y, si el contraste con INDEC pasa, hace commit + push
> con `publicar_mapa.ps1`. Dos medidas con selector: **metodología nueva INDEC** (desde 2023T4, reproduce los
> informes: total, sexo, edad, educación y asalariados a ≤0,2 pp en 2023T4–2026T1) y **serie larga**
> (2003–). Decisión de Matías del 18/10: indicadores, sector y mapa con la metodología nueva;
> el análisis interactivo con la serie larga por default y un botón destacado para superponer la
> nueva (punteada, desde 2024); nunca empalmar. Miniatura: el gráfico por grupo de edad. Indicadores trimestrales; resto en promedios anuales de años completos (hasta 2025);
> mapa y sector con nivel o cambio interanual. Corregidas las etiquetas cruzadas de las ramas 11
> (otros servicios) y 12 (servicio doméstico). Miniatura nueva. Para cada trimestre nuevo, Matías
> sólo carga las cifras de INDEC en `validacion\indec_publicado.csv`.

**El panel de informalidad se rehízo entero.** Matías pidió dos cosas: que se vea más profesional
y que el embebido deje de encerrar el scroll. Las dos están hechas, y de paso aparecieron tres
errores que el panel venía publicando sin que nadie los viera.

- **Los números del encabezado estaban mal, y eran fijos.** Los cinco indicadores (total, varones,
  mujeres, jóvenes, adultos) estaban **escritos a mano en el HTML** y nunca se calculaban. Decían
  51,1 % de informalidad total con una variación de ▲ 5,1 %; el cubo de datos dice **46,9 %** y
  **+0,5 pp**. Lo mismo el mapa: tenía las tasas provinciales congeladas de otra versión (Tucumán
  65,4 % cuando el dato es 57,8 %). **Eso era «el mapa desactualizado»**: no era el mapa, era que
  todo lo precalculado venía de una cosecha anterior a los datos del gráfico interactivo. Ahora
  **todo se calcula del mismo cubo en el navegador**, así que el mapa, el ranking por sector y el
  gráfico no pueden volver a contradecirse.
- **Los colores del desglose por sector se repetían.** La paleta tenía ocho colores y el desglose
  por sector tiene doce series: el código hacía `colores[i % 8]`, así que «Actividades primarias» y
  «Transporte» salían del mismo azul, y «Servicios de salud» y «Servicios financieros» del mismo
  naranja. La leyenda era ambigua. **Ése era el «se ve raro» del comentario.**
- **De 73 MB a 58 KB.** El HTML llevaba adentro 377.386 filas en JSON con los nombres de los veinte
  campos repetidos en cada fila y ruido de coma flotante (`30.299999237060547` por `30,3`). Los
  datos se pasaron a **ocho archivos columnares** en `assets/data/informality/`, uno por dimensión
  de desglose, que se cargan sólo cuando hacen falta. **La primera carga pasó de 10,7 MB a 0,17 MB
  comprimidos**, unas setenta veces menos.
- **El scroll ya no se atrapa.** El `iframe` informa su altura a la página por `postMessage` y la
  página lo estira hasta que entra entero, así que se baja con el scroll normal. Decidí **no**
  sacar el panel a una página aparte: embebido se lee como una sección más del sitio, hereda el
  tema claro/oscuro y sigue siendo un archivo portátil que se puede mandar suelto a la OIT. Queda
  además un enlace «abrir en una pestaña aparte».
- **La interfaz usa el sistema del sitio.** Literata y IBM Plex, el verde conífera, el papel
  oscuro, y los filtros **arriba del gráfico en vez de a los costados**: antes el gráfico quedaba
  espachurrado entre dos columnas y el eje de años era una mancha negra de etiquetas superpuestas.
  Fuera los emojis de sector, las sombras, los bordes redondeados y el selector de seis paletas.
- **Con más de ocho series el gráfico se parte en paneles.** Doce sectores o veinticuatro
  provincias en una sola grilla son ilegibles con cualquier paleta. Ahora cada serie tiene su
  panel con la misma escala. Los colores quedaron **atados a la entidad**, no a su posición: si
  sacás una serie, las demás no cambian de color.
- **Plotly pasó a estar alojado en el repo y con versión fija.** Antes era `plotly-latest.min.js`
  desde el CDN, que puede cambiar sin aviso y le filtra la IP del visitante a un tercero. Ahora es
  `plotly-basic-2.35.2` en `assets/js/` (0,36 MB comprimido).
- **El sitemap no tiene nada roto.** Verificado desde fuera: 200, XML válido, las 18 páginas,
  anunciado en `robots.txt`. La fila roja de Search Console es estado viejo que Google todavía no
  refrescó. Está explicado en el To-Do.

**Trampa nueva, que costó una hora:** el paquete `plotly-geo` **no trae el módulo `bar`**, y Plotly
no avisa: acepta `type:"bar"`, lo guarda en `data`, y dibuja una línea igual (`_fullData` dice
`scatter`). Se cambió a `plotly-basic` y **el mapa se dibuja a mano en SVG**, con proyección
Mercator sobre el geojson de provincias, que además bajó de 461 KB a 194 KB. Segunda trampa de la
misma familia: **`Plotly.react` no convierte una traza de `scatter` a `bar`** ni un gráfico plano
en una grilla de paneles; hay que `purge` antes cuando cambia la forma del gráfico.

---

## COLA DE TRABAJO

*(Abiertos arriba. Un ítem que se cierra se reduce a una línea y el detalle se archiva.)*

### Bloqueado por Matías

- **B3 — ¿El informe de Costa Rica es público?** (to-do 2). Hoy está descrito sin PDF.
- **B8 — La carpeta vieja de `Documents\GitHub\...`.** Pedí permiso para borrarla y me lo denegó el
  clasificador de la sesión. Son 30 segundos a mano (to-do 4).

### Abiertos

- **S1 — CERRADO: Google indexó el sitio.** La inspección de URL del 14/10 a la noche devuelve «La
  URL está en Google» y «La página está indexada», con rastreo y canónica correctos. Google lo
  descubrió desde el **repositorio de Nottingham** y desde el **CV del IIEP**, no desde el sitemap.
  Queda sólo pedir la reindexación, porque el último rastreo (15:23) es anterior al castellano, a
  «Some pictures» y a la intro nueva. El sitemap da «Error temporal de procesamiento», que es
  pasajero: el archivo está sano, comprobado desde fuera.
  **Lección para no repetir:** durante la corrida 4 concluí que el sitio no estaba indexado a
  partir de la herramienta de búsqueda de la sesión, que no es Google. La conclusión fue
  equivocada. Search Console es la única fuente válida para esto.
- **S5 — Links entrantes.** Estado al 14/10 de noche: **enlazan** el repositorio de Nottingham
  (lo reveló la inspección de URL), el CV del IIEP y su página, ORCID, y el «Homepage» de Scholar.
  **uu.nl quedó hecho el 15/10**: perfil completado en neerlandés e inglés desde el editor de
  Solis, con el enlace al sitio como `<a href>` real, verificado en las dos versiones públicas. LinkedIn no cuenta, sus
  enlaces son `nofollow`.

- **S11 — CERRADO.** Matías revisó las descartadas y sumó 13 al sitio (quedaron 259). Las carpetas
  de `personal/_revisar_fotos/` se borraron y el zip de Instagram también.
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
- **S13 — Sumar países al panel.** En curso (19/10). Entró Costa Rica (ECE del INEC, 2010T3–2025T3)
  y el panel tiene selector de país y una vista «Comparar». Datos en
  `assets/data/informality/<iso>/` y registro en `paises.json`; un país nuevo no toca el HTML.
  Falta: (1) correr el master de Costa Rica en Stata y comparar con la réplica en Python que hoy
  alimenta el sitio; (2) bajar 2025T4–2026T2 del INEC; (3) push, que espera el OK de Matías;
  (4) miniatura nueva (la actual es sólo Argentina). Próximos países: ver
  `mercado_trabajo_latam\datos\Bases_LATAM_disponibles.md`.
- **S4 — Primera nota para `/notes/`.** Las conclusiones del meta-análisis en castellano llano,
  600-900 palabras. Faltan otras dos para encender la sección.

### Cerrados

- **S2 — El panel de informalidad.** Cerrado 15/10, corrida 5: datos separados del HTML en ocho
  archivos columnares, interfaz con el sistema del sitio, embebido que no atrapa el scroll, y los
  tres errores de datos corregidos. Lo que quedaba de «sumar países» pasó a S13.
- **S6 — Alt text de las fotos.** Cerrado 15/10 por decisión de Matías: las quiere como están.
- **B10 — El perfil de uu.nl.** Cerrado 15/10: Matías apretó «Profieltekst EN naar puur».
- **B11 — Costa Rica.** Fuera de la lista por pedido de Matías el 15/10: avisa él cuando la OIT
  conteste.

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
