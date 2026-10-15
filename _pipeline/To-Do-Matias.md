# To-do para Matías — SÓLO acciones que tenés que hacer vos

> **Nunca pegues un token ni una contraseña en `ESTADO.md`**: ese archivo se sube a GitHub. Las
> credenciales van en `_pipeline/.github_token`, que git ignora.

---

**1. GOOGLE YA TE TIENE INDEXADO.** La inspección de URL del 14/10 a la noche dice **«La URL está
en Google»** y **«La página está indexada»**. Rastreo permitido, obtención correcta, indexación
permitida, y la canónica que elige Google es la que declaramos. No hay nada roto.

Lo que Google usó para descubrir el sitio, según la propia inspección, fueron dos páginas de
referencia:

- `https://repository.nottingham.ac.uk/entities/publication/74a864c9-...` — el repositorio de
  Nottingham. Ninguno de los dos lo tenía en la lista y es un enlace muy bueno, porque `ac.uk` es
  un dominio de alta autoridad.
- `https://economicas.uba.ar/iiep/wp-content/uploads/CV_MatiasGolman.pdf` — el CV del IIEP. Queda
  confirmado que ese hipervínculo apunta al sitio nuevo.

**1a. PEDÍ LA INDEXACIÓN DE NUEVO, PORQUE LO QUE TIENE GOOGLE ES VIEJO.** El último rastreo fue a
las 15:23 del 14/10, o sea **antes** de todo el trabajo de esa noche: el castellano completo, el
cambio de «Photography» a «Some pictures», la intro nueva, las fotos. Google tiene una versión
anterior. Volvé a «Inspeccionar URL» → «Solicitar indexación» para:

`/` · `/es/` · `/work/` · `/about/` · `/pictures/`

**1b. EL SITEMAP: reenvialo y listo.** La inspección dice «Error temporal de procesamiento», que es
un problema pasajero del lado de Google, no del archivo. Lo verifiqué desde fuera de tu red:
responde 200, es XML válido, tiene las 31 URLs y el `robots.txt` lo anuncia. Borrá la fila roja y
reenvialo. Si el campo ya muestra el prefijo `https://matiasgolman.github.io/`, escribí sólo
`sitemap.xml`.

**1c. ESTAR INDEXADO NO ES LO MISMO QUE APARECER AL BUSCAR TU NOMBRE.** Son dos cosas distintas.
Estar en el índice es el requisito; rankear por encima de tu ficha de uu.nl y del CV de la UBA
depende de los enlaces entrantes y del tiempo. Ahí el estado real es:

- **uu.nl**: no enlaza todavía. Lo agregás mañana. Es el que más vale de todos.
- **Repositorio de Nottingham**: enlaza (descubierto por la inspección).
- **CV del IIEP, la página y el PDF**: enlazan.
- **ORCID**: enlaza.
- **Google Scholar**: el campo «Homepage» tiene la URL correcta.
- **LinkedIn**: no cuenta, sus enlaces son `nofollow`.

Con uu.nl sumado quedan cinco fuentes buenas. Volvé a buscar tu nombre en una semana.

**2. UU: EL ENLACE AL SITIO** *(lo estás haciendo)*. El texto en inglés y neerlandés te lo dejé
en el chat del 15/10. **Lo importante para Google**: el enlace tiene que ser un enlace de verdad
(`<a href>`), no la URL escrita como texto plano. Si el editor de perfiles de UU tiene un campo
propio de enlaces o «personal website», usá ése; el cuerpo del texto es el plan B. Cuando esté,
avisame y lo doy por cerrado.

**3. COSTA RICA: ¿el informe es público?** *(esperando la respuesta de la OIT)*. El PDF está en
`_pipeline/` y **no** publicado. El trabajo sí está descrito en `/work/`, sin enlace al archivo.

**4. GOATCOUNTER: nada que hacer, salvo mirarlo** una vez por mes. Tu panel es
`https://matiasgolman.goatcounter.com`. Lo único que importa para tu objetivo es **Referrers**: te
dice si alguien llegó desde LinkedIn, desde Scholar o desde una búsqueda. No mires las visitas
totales esperando que suban; lo que buscás es **una** visita de la persona indicada.

**5. EL TEXTO ALTERNATIVO DE LAS FOTOS** *(sólo si te importa la accesibilidad fina)*. Las 259 van
con `alt=""` y una descripción del conjunto en la galería. Describir 259 imágenes una por una no es
algo que se pueda hacer con criterio, y 259 veces «fotografía de paisaje» le estorba a quien usa un
lector de pantalla más de lo que le sirve. Si lo querés resolver, la salida es recortar la
selección a unas pocas decenas y escribirles el texto a mano.

**6. EL ABOUT, CUANDO LO REESCRIBAS.** Está el original verbatim, como pediste. Dos cosas para
tener en cuenta cuando le metas mano: el párrafo de «If I were on the hiring side of the equation»
le habla a alguien que te está por contratar, que es lo único del sitio que dice que estás
buscando (D-03 decía lo contrario); y la versión en castellano de `/es/sobre-mi/` es una traducción
del inglés, así que cuando cambies uno hay que pasar el otro.

*(Al 15/10/2026. Cerrados: la carpeta vieja, el zip de Instagram, las fotos con gente, el nombre
«Things I've built», y los roles por módulo en docencia.)*
