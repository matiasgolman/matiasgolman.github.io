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

**2. LAS 82 FOTOS CON GENTE, POR SI QUERÉS RESCATAR ALGUNA** *(cuando tengas un rato)*. Están en
`personal\_revisar_fotos\con-gente\`, en su tamaño original y fuera del repo. Son las que quedaron
afuera por la regla que me diste: más de una persona, o vos de cerca. Al lado, en `otras\`, hay 51
que descarté por no ser naturaleza (ciudades, comida, documentos). Marcame los números que querés y
los agrego.

**2b. EL ZIP DE INSTAGRAM YA NO HACE FALTA** *(1,4 GB que podés borrar)*. Ya extraje todo lo que
necesitaba. Si lo querés conservar, bien; si no, se puede ir.

**3. BORRAR LA CARPETA VIEJA** *(30 segundos)*. `C:\Users\matia\Documents\GitHub\skills_vacancies\
Skills identification - Coding resources\matiasgolman.github.io` está **vacía**. Pedí permiso para
borrarla y la sesión me lo denegó, así que te toca. Ojo: borrá **sólo esa subcarpeta**, no
`skills_vacancies`, que es otro proyecto tuyo con cosas adentro.

**4. EL ABOUT ES EL ORIGINAL, TAL CUAL LO PEDISTE** *(cuando quieras)*. Está verbatim, con
«I appreciate your interest in my work trajectory» y el párrafo de «If I were on the hiring side of
the equation». Lo único que toqué son los tres `---` que se convertían en em dash.
**Lo que te dejo para pensar cuando lo trabajes:** ese párrafo le habla a alguien que te está por
contratar, y en D-03 decidimos que el sitio no dice que estás buscando. Hoy es la única parte del
sitio que lo dice. No lo toco hasta que me avises.

**5. ¿«Things I've built» te cierra?** Era tu duda del punto 6. Descarté «Data projects» porque
Araucaria no es un proyecto de datos en el sentido en que lo es el dashboard, y porque suena a
categoría de portfolio más que a algo tuyo. Si preferís otra cosa, es una línea en
`_includes/header.html` y otra en `projects.md`.

**6. ¿QUERÉS EL ROL POR MÓDULO EN `/teaching/`?** Me dijiste que das clase y tutoriales «en muchos»
pero no cuál en cuál. Hoy la página lo dice en general, arriba. Si me pasás el detalle, lo pongo
módulo por módulo.

**7. COSTA RICA: ¿el informe es público?** *(esperando la respuesta de la OIT)*. El PDF está en
`_pipeline/` y **no** publicado. El trabajo sí está descrito en `/work/`, sin enlace al archivo.

**8. GOATCOUNTER: nada que hacer, salvo mirarlo** una vez por mes. Tu panel es
`https://matiasgolman.goatcounter.com`. Lo único que importa para tu objetivo es **Referrers**: te
dice si alguien llegó desde LinkedIn, desde Scholar o desde una búsqueda. No mires las visitas
totales esperando que suban; lo que buscás es **una** visita de la persona indicada.

**9. UN HUECO QUE TE DEJO ANOTADO: el texto alternativo de las fotos.** Las 246 van con `alt=""` y
una descripción del conjunto en la galería. Describir 246 imágenes una por una no es algo que pueda
hacer de taquito, y 246 veces «fotografía de paisaje» le molesta más que le sirve a quien usa un
lector de pantalla. Si querés accesibilidad fina, la salida es recortar la selección a unas pocas
decenas y escribirles el texto a mano. Decime si te interesa.

*(Al 14/10/2026. Se cerraron: las versiones finales de los papers, los siete manuales de curso, la
decisión sobre el `.git` de 1,4 GB, y la selección de fotos.)*
