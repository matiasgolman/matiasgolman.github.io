# To-do para Matías — SÓLO acciones que tenés que hacer vos

> **Nunca pegues un token ni una contraseña en `ESTADO.md`**: ese archivo se sube a GitHub. Las
> credenciales van en `_pipeline/.github_token`, que git ignora. (El token del 14/10 ya lo moví yo;
> no llegó a subirse.)

---

**1. EL TOKEN QUEDÓ DE SÓLO LECTURA** *(1 minuto, y es lo único que me bloquea)*. Lo probé: el token
**autentica bien** como vos y **puede leer** el repo, pero GitHub rechaza el `push` con
`403 Permission denied`. Eso es exactamente lo que pasa cuando en **Repository permissions** quedó
**`Contents: Read-only`** en vez de **`Read and write`**.

*Settings → Developer settings → Personal access tokens → Fine-grained tokens →* abrí el token →
**Repository permissions → Contents → Read and write** → *Update token*. No hace falta generar uno
nuevo ni volver a pegármelo. Avisame y pusheo.

**Mientras tanto hay dos commits míos sin subir** (el crédito a María García-Vega y la serie del GEP,
GoatCounter, el `<h1>` de la portada, y sacar el dashboard de 73 MB del sitemap). Si querés verlos ya:

```
git push origin main
```

**2. ORCID: te falta un clic para los trabajos** *(30 segundos)*. Hice los enlaces (sitio, Scholar,
LinkedIn, uu.nl), la biografía y el puesto de Utrecht — todo público y guardado. **Los trabajos no
los pude subir yo**: el navegador no me deja cargar archivos en tu nombre. Te dejé el archivo listo:

*ORCID → Works → Add → **Import works from a BibTeX file** → elegí
`_pipeline\orcid-works.bib`* → revisá la lista y guardá. Son los **nueve** trabajos (5 publicados,
1 ILO Working Paper, el del GEP con María, y los otros dos working papers).

Ya que estás ahí, dos cosas que yo no hice y te llevan dos minutos:
- **Agregá el doctorado de Nottingham** en *Education and qualifications* (2021–2025, PhD in
  Economics). Es el hueco más visible que queda.
- **Corregí el «to present»** de la Maestría en Economía de la UBA, que figura como si siguiera en
  curso, y el del IIEP-Baires (terminó en 2019).

**3. ¿DÓNDE ESTÁ LA ÚLTIMA VERSIÓN DEL PAPER DE AI?** Dijiste que la agregaste, pero en el repo no
hay ningún PDF nuevo: `golman-ai-personality-traits.pdf` sigue siendo el de enero de 2026. Si la
guardaste en otra carpeta, dejámela en `_pipeline/papers/` y la pongo. *(Los otros dos papers y el CV
sí están al día, y **todos** tienen botón de descarga en `/work/` — sí, la respuesta a tu pregunta
es que siguen descargables.)*

**4. LAS FOTOS** *(sigue pendiente, sin apuro)*. Cuando tengas el zip de Instagram, dejámelo donde
quieras y avisame. La sección está construida y apagada; se enciende el día que haya fotos.

**5. COSTA RICA** *(esperando la respuesta de la OIT)*. El PDF está guardado en `_pipeline/` y **no**
publicado. El trabajo sí está descrito en `/work/`, sin enlace al archivo.

**6. LA MUDANZA DE LA CARPETA — leé esto antes de borrar nada**.

- **No borres nada hasta que estén pusheados los dos commits del punto 1.** Hoy sólo existen en tu
  disco.
- **La ruta que me diste no la puedo ver**: `C:\Users\Golma001\...` es otro usuario de Windows, y
  esta computadora (`matipc`) está logueada como `matia`. O es tu computadora del trabajo, o hace
  falta conectarla con el botón de agregar carpeta. Decime cuál es y la configuro.
- **Sigo sin recomendarte OneDrive para el repo**, y ahora con un número: tu `.git` pesa **1,3 GB**.
  OneDrive lo va a sincronizar archivo por archivo mientras git escribe adentro, que es la receta
  conocida de `.lock` fantasma y objetos corruptos.
- **La forma que resuelve tu problema de espacio de verdad** es no copiar la carpeta, sino clonarla
  superficial en la máquina nueva:
  ```
  git clone --depth 1 https://github.com/matiasgolman/matiasgolman.github.io.git
  ```
  Eso te deja una copia de trabajo de **~100 MB en vez de 1,5 GB**, y podés pushear igual. La
  historia completa queda a salvo en GitHub, que es para lo que existe el remoto.
- **Para el disco externo**, un espejo completo y compacto:
  ```
  git clone --mirror https://github.com/matiasgolman/matiasgolman.github.io.git
  ```
- Después de eso, podés borrar la carpeta vieja sin perder nada.

**7. GOATCOUNTER: qué hacer con él** *(nada, salvo mirarlo)*. Ya está puesto en el sitio y se activa
en el próximo deploy. Tu panel es `https://matiasgolman.goatcounter.com`, con el usuario que creaste.
Lo útil de mirar, una vez por mes y no más:
- **Referrers** — de dónde llega la gente. Es el único número que importa para tu objetivo: te dice
  si alguien llegó desde LinkedIn, desde Scholar o desde una búsqueda.
- **Pages** — qué páginas se leen. Si `/work/` y `/projects/` no se leen nunca, el problema está en
  la portada.
- No mires las visitas totales esperando que suban: un sitio personal con tráfico correcto son
  decenas de visitas al mes, no miles. Lo que buscás es **una** visita de la persona indicada.

*(Al 14/10/2026.)*
