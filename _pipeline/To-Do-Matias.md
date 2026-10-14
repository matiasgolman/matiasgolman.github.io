# To-do para Matías — SÓLO acciones que tenés que hacer vos

> Este archivo no lleva historia ni confirmaciones: sólo lo que está esperando algo tuyo.
> **Dónde dejarme instrucciones:** el bloque `COMENTARIO DE MATIAS`, arriba de todo en `ESTADO.md`.

---

**1. EL TOKEN DE GITHUB: estabas mirando la lista equivocada** *(2 minutos)*.
En la pantalla de *fine-grained PAT* hay **dos** bloques de permisos y vos viste el de abajo:

- **«Account permissions»** — ahí están `Block another user`, `Codespaces user secrets`,
  `Copilot Chat`, `Gists`, `Git SSH keys`, `Models`… **No es ninguno de esos.**
- **«Repository permissions»** — está *arriba*, y sólo aparece **después** de elegir
  «Only select repositories» → `matiasgolman/matiasgolman.github.io`. Ahí sí está **`Contents`**.

Entonces: *Settings → Developer settings → Personal access tokens → Fine-grained tokens →
Generate new token* → **Resource owner:** tu usuario → **Repository access:** «Only select
repositories» → elegí `matiasgolman.github.io` → en **Repository permissions** poné
**`Contents: Read and write`** (y dejá `Metadata: Read-only`, que se marca solo y es obligatorio).
**Nada más.** Expiración: 90 días está bien.

**Dónde ponerlo:** creá el archivo `_pipeline/.github_token` (una sola línea, el token pelado).
Ya lo agregué al `.gitignore`, así que **no se sube a GitHub**. Avisame cuando esté y a partir de
ahí pusheo yo. Mientras tanto, pusheá vos:

```
git push origin main
git push origin v1-academic-jmp-2025
git push origin backup/v1-academic-jmp-2025
```

> **Lo que el token puede hacer, para que lo sepas:** leer y escribir el contenido de **ese único
> repo**. No puede tocar tus otros repos, ni tu cuenta, ni borrar el repositorio. Si algo te
> incomoda, lo revocás desde la misma pantalla y listo.

**2. VERIFICAR EN GOOGLE SEARCH CONSOLE** *(después del primer push, 1 minuto)*. Ya puse tu código
`4v_RtVj-...` en el sitio. En cuanto pushees y GitHub Pages termine de desplegar (2-3 minutos),
entrá a Search Console y dale **«Verificar»**. Después, en el menú de la izquierda, **«Sitemaps»** →
pegá `https://matiasgolman.github.io/sitemap.xml` → «Enviar».

**3. BING: la vía corta es importar desde Google** *(2 minutos, y conviene hacerlo)*. Bing alimenta
a Copilot y a varios asistentes, así que ya no es secundario.
1. `https://www.bing.com/webmasters` → entrá con Microsoft, Google o Facebook.
2. En «Add your site» elegí **«Import from Google Search Console»** y autorizá. Te trae el sitio,
   la verificación y el sitemap de una, sin tocar código. *(Por eso conviene hacer el punto 2
   primero.)*
3. Si preferís no conectar las cuentas, elegí «Add site manually», copiame la etiqueta
   `<meta name="msvalidate.01" ...>` y la pongo yo.

**4. LAS TRES ÚLTIMAS VERSIONES DE LOS PAPERS** *(dijiste que me las pasabas)*. Dejámelas en
`_pipeline/papers/` con cualquier nombre. Las voy a renombrar a nombres estables
(`golman-ai-personality-traits.pdf`, etc.) para que el link no se rompa nunca más. **Hasta que
estén, las tres páginas de working paper muestran título y abstract pero el botón de PDF no
aparece.**

**5. ¿EL INFORME DE COSTA RICA ES PÚBLICO?** *(bloquea una decisión, y es la única con riesgo real)*
Me lo dejaste en el pipeline y lo puedo publicar, pero **no lo voy a subir hasta que me confirmes**.
Es un entregable a un cliente (OIT) sobre política de un gobierno: si la OIT todavía no lo publicó,
subirlo vos primero puede caer muy mal, por más que no tenga nada confidencial adentro. Tres
opciones: **(a)** la OIT ya lo publicó → me pasás el link y linkeamos al sitio de la OIT, que además
es mejor para Google; **(b)** no está publicado → lo describo en el sitio sin PDF (así quedó ahora);
**(c)** pedís luz verde a tu contraparte en la OIT. **Mi recomendación: (b) hasta tener (a).**

**6. EL PAPER DEL GEP** *(30 segundos)*. Google muestra un *GEP discussion paper 26/06* de Nottingham,
«Artificial Intelligence and Personality Traits», **firmado por vos y María García-Vega**. No lo
pude abrir para confirmarlo. ¿Es la versión publicada de tu primer capítulo? ¿Va con coautora? Si
sí, es una ficha citable y linkeable — vale la pena ponerla en el sitio con su número de serie.

**7. LAS FOTOS: así se bajan de Instagram** *(5 minutos de trabajo tuyo, el resto lo hace Meta)*.
Dijiste que no sabías cómo. No hace falta ir trip por trip: **Instagram te las da todas juntas**.
En la app: *Perfil → ☰ → Tu actividad → Descargar tu información → Descargar o transferir
información → Parte de tu información → **Contenido** → Publicaciones → Descargar en el dispositivo
→ Formato **JPEG** / Calidad **Alta** → Crear archivos*. Te llega un mail con un `.zip` en unas
horas. Me pasás el zip o la carpeta y yo elijo una preselección, la optimizo y te la muestro para
que la apruebes. **No hace falta que lo hagas ahora**: la sección de fotos queda construida y
apagada hasta que aparezcan.

**8. ORCID: decime que sí y lo actualizo yo** *(necesito que estés logueado)*. Tu ORCID
(`0000-0001-6557-963X`) está sin tocar desde 2018 y hoy ya está enlazado desde el sitio nuevo.
**Sí, lo puedo actualizar por el navegador** con los datos del CV: empleos, educación, los cinco
trabajos publicados y los tres working papers. Lo que necesito de vos:
- Que inicies sesión en ORCID vos mismo, en el navegador que usemos. **Yo no voy a escribir tu
  contraseña** — no manejo credenciales, es una regla que no rompo ni con permiso.
- Que me digas «dale» acá o en el chat. Después te muestro el perfil terminado antes de guardar los
  cambios grandes.

**9. ANALÍTICA GRATUITA** *(opcional, 3 minutos)*. Dijiste «si es gratis, sí». **GoatCounter** es
gratis para uso personal, no usa cookies y no necesita cartel de consentimiento:
`https://www.goatcounter.com/signup`, elegí un código de sitio (por ejemplo `matiasgolman`) y
pasame ese código. Son dos líneas en el sitio. *(Plausible es más lindo pero cuesta ~9 €/mes; no lo
vale para este tamaño de sitio.)*

**10. LA MUDANZA DE LA CARPETA — leé esto antes de mover nada** *(importante, y una advertencia)*.
Buenas noticias primero: **la carpeta NO está dentro de otro repo de git**. Chequeé los tres niveles
de arriba y no hay ningún `.git`, así que está sólo *visualmente* mal ubicada. Nada está roto y
mover la carpeta **no rompe nada**: el remoto, las ramas y los tags viven adentro de `.git`, y
viajan con ella. Tres cosas, en orden de importancia:

- **No la pongas adentro de OneDrive.** Es la advertencia principal. OneDrive sincroniza archivo por
  archivo mientras git escribe decenas de archivos chicos a la vez dentro de `.git`; el resultado
  conocido son `.lock` fantasma, objetos a medio escribir y repos corruptos. Con 1,3 GB de `.git`,
  además, le vas a dar a OneDrive un trabajo enorme para nada. **El backup de un repo de git es
  GitHub**, para eso existe el remoto. Ponelo en una carpeta local común, por ejemplo
  `C:\Users\matia\GitHub\matiasgolman.github.io`.
- **Cómo mudarlo, en la computadora nueva:** no copies la carpeta. Clonala de cero, que es más
  limpio y te deja un repo sano:
  ```
  cd C:\Users\<vos>\GitHub
  git clone https://github.com/matiasgolman/matiasgolman.github.io.git
  ```
  Eso ya queda enlazado a GitHub y podés pushear desde ahí sin configurar nada. **Hacelo después de
  pushear lo que hay acá** (punto 1), si no perdés los commits que todavía no subiste.
- **El disco externo:** copiá la carpeta entera con `.git` adentro, o mejor, hacé
  `git clone --mirror https://github.com/matiasgolman/matiasgolman.github.io.git` en el disco: queda
  un espejo completo, con todas las ramas y tags, en una fracción del espacio.
- Cuando la carpeta nueva exista, **dame acceso a ella** (el botón de agregar carpeta en la app de
  escritorio) y seguimos ahí sin perder nada.

*(Al 14/10/2026.)*
