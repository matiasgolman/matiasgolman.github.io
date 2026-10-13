# To-do para Matías — SÓLO acciones que tenés que hacer vos

> Este archivo no lleva historia ni confirmaciones: sólo lo que está esperando algo tuyo. Todo lo
> demás va a `ESTADO.md` (dónde estamos) o al `Changelog.md` (qué pasó).
> **Dónde dejarme instrucciones:** el bloque `COMENTARIO DE MATIAS`, arriba de todo en `ESTADO.md`.

---

**1. CONTESTAR EL CUESTIONARIO** *(y es lo primero: bloquea todo el resto)*.
`preguntas/Preguntas_01_estructura_y_diseno.md`, 22 preguntas. Escribí debajo de cada una, en
castellano o inglés, sin formato. Las que no sepas, dejalas en blanco y pongo yo mi recomendación.
Cuatro ya te las pregunté en el chat del 13/10 (público, registro visual, visibilidad de la
búsqueda, stack); si las contestaste ahí, salteá la 1, la 13, la 3 y la 19.

**2. PUSHEAR EL BACKUP A GITHUB** *(dos comandos, 10 segundos)*. Hice el tag y la rama localmente,
pero **la VM del puente no tiene tus credenciales de GitHub**, así que no puedo pushear yo. Desde
tu terminal, en la carpeta del repo:

```
git push origin v1-academic-jmp-2025
git push origin backup/v1-academic-jmp-2025
```

Con eso la versión de job market queda guardada también en el servidor, no sólo en tu disco.

**3. DECIDIR SI ME DAS PERMISO DE PUSH** *(o si pusheás vos cada vez)*. Hoy puedo leer el repo pero
no escribir en GitHub. Dos caminos:
- **(a) Pusheás vos.** Yo dejo todo commiteado localmente y te aviso; vos corrés `git push`. Cero
  riesgo, un paso manual por deploy.
- **(b) Me das un token.** Un *fine-grained PAT* de GitHub, con acceso **sólo a este repositorio** y
  permiso de `Contents: read and write`, guardado en un archivo que el repo ignora. Con eso puedo
  desplegar sola la web y verificar que el deploy salió bien. Es tu llamada: un token, aunque esté
  limitado a un repo, es una credencial que queda escrita en tu disco.
**Mi recomendación: (a) mientras rediseñamos** (vas a querer mirar antes de publicar cada cambio
grande) **y (b) más adelante**, si el sitio pasa a tener un blog que se actualiza seguido.

**4. CREAR LA PROPIEDAD EN GOOGLE SEARCH CONSOLE** *(5 minutos, gratis, y es la pieza que falta)*.
Esto no lo puedo hacer yo: necesita tu cuenta de Google. Pasos:
1. Entrá a `https://search.google.com/search-console` con tu cuenta.
2. «Añadir propiedad» → **Prefijo de URL** → `https://matiasgolman.github.io/`.
3. Elegí el método **«Etiqueta HTML»** y copiame el código que te da (es un
   `<meta name="google-site-verification" content="...">`). Pegalo en el `COMENTARIO DE MATIAS`.
4. Yo lo pongo en `_config.yml`, desplegamos, y vos le das «Verificar».
5. Después mando el sitemap y ya tenemos informe de cobertura: qué páginas indexó, cuáles no, y por
   qué. Hoy estamos adivinando; con esto dejamos de adivinar.

*(Si querés, lo mismo con Bing Webmaster Tools. Bing alimenta a ChatGPT y a Copilot, así que
cada vez importa más, pero es secundario.)*

**5. MANDARME LAS FOTOS DE NATURALEZA** *(las que quieras que estén en el sitio)*.
**No puedo bajarlas de tu Instagram**: la API de Instagram exige cuenta de empresa y un token que
caduca cada 60 días, y los widgets de terceros se rompen o te meten rastreadores. Y hay un motivo
mejor para no hacerlo: una galería con tus archivos carga más rápido, Google la puede leer, y vos
elegís qué se ve. Dejame los archivos originales en una carpeta (por ejemplo
`C:\Users\matia\Pictures\web_fotos\`) y avisame; yo las optimizo (WebP, varios tamaños), armo la
galería y les pongo texto alternativo. **Ideal: 12 a 20 fotos**, de las que más te gusten, con el
lugar y el año si te acordás. Menos de 10 se ve flaco; más de 30, nadie las mira.

**6. DATOS Y ARCHIVOS QUE ME FALTAN** *(los que puedas; los que no, los marco como pendientes)*:
- **Foto tuya** para la home, si no te gusta la actual (`assets/img/matias_profile.jpeg`). Horizontal
  o cuadrada, cara visible, luz natural. Si tenés una en contexto de trabajo (dando clase, en un
  panel), mejor todavía: dice más que un retrato.
- **La app Araucaria**: ¿cuál es la URL que funciona hoy, y dónde vive el código?
- **El dashboard de informalidad**: ¿el HTML de 73 MB es la versión final, o hay una fuente (script,
  datos) de la que se genera? Si hay fuente, mandámela: cambia el plan del ítem S2.
- **ORCID**, si tenés. Si no, armalo (`https://orcid.org/register`, 2 minutos): es gratis, y es uno
  de los pocos perfiles que Google asocia fuerte con un nombre de investigador.
- **El informe de Costa Rica** y cualquier producto de OIT/OCDE/BM que ya sea público y no esté en
  `assets/pdf/` — o el link, si está publicado en el sitio del organismo (mejor linkear que alojar).
- **¿Hay algo que NO quieras que esté en el sitio?** (temas, opiniones, datos personales, ubicación
  exacta, familia). Es la pregunta 12 del cuestionario, pero la repito acá porque es la única del
  cuestionario cuya respuesta equivocada es difícil de deshacer.

**7. DECIDIR EL DOMINIO** *(pregunta 4 del cuestionario; la separo porque cuesta plata y tiempo)*.
`matiasgolman.github.io` funciona, pero un dominio propio (`matiasgolman.com`, `.nl`, `.eco`…)
cuesta ~10-15 €/año y es, después de los links entrantes, lo que más te va a mover en Google a
mediano plazo: es tu nombre en la URL y la señal no se la queda GitHub. **Si decís que sí, lo
compro yo no puedo** — tenés que comprarlo vos (Namecheap, Gandi, TransIP si lo querés holandés).
Después yo configuro el `CNAME` y los DNS. **Importante: si lo hacemos, hay que hacerlo ANTES de
empezar a juntar links entrantes**, no después, para no mudar el sitio dos veces.
