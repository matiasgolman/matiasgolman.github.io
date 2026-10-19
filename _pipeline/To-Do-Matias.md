# To-do para Matías — SÓLO acciones que tenés que hacer vos

> **Nunca pegues un token ni una contraseña en `ESTADO.md`**: ese archivo se sube a GitHub. Las
> credenciales van en `_pipeline/.github_token`, que git ignora.

---

**1. EL SITEMAP: no hay nada roto, y no hay nada que arreglar en el repo.** Lo verifiqué otra vez
el 15/10 desde fuera de tu red: `https://matiasgolman.github.io/sitemap.xml` responde **200**, es
XML válido, lista las **18 páginas** (diez en inglés, ocho en castellano) y el `robots.txt` lo
anuncia. O sea: el archivo está sano.

La fila roja que ves en Search Console es **estado viejo que Google todavía no refrescó**. Cuando
un sitemap falla una vez, la consola deja la fila en rojo hasta que vuelve a leerlo por su cuenta,
y eso tarda entre varios días y un par de semanas. Reenviarlo otra vez no acelera nada y es lo que
ya hiciste.

Lo único que conviene hacer:

- **Dejá una sola fila.** Si hay más de una entrada de `/sitemap.xml`, borrá las repetidas y dejá
  una. Reenviar la misma URL varias veces no ayuda.
- **Mirá la fecha de «Última lectura», no el estado.** Cuando esa fecha pase a ser posterior al
  15/10, el estado se pone en verde solo.
- **Si en dos semanas sigue rojo con una lectura nueva**, ahí sí avisame y lo miro de nuevo.

*(Dato para que no te preocupe: Google ya tiene el sitio indexado y no lo descubrió por el sitemap
sino por el repositorio de Nottingham y el CV del IIEP. El sitemap ayuda, no es imprescindible.)*

---

**2. PEDÍ LA INDEXACIÓN DE LAS DOS PÁGINAS DEL PANEL.** Esta corrida rehízo el panel de
informalidad entero, así que `/dashboard/` y `/es/panel/` cambiaron de arriba abajo. En Search
Console: «Inspeccionar URL» → «Solicitar indexación» para:

`/dashboard/` · `/es/panel/`

Si querés, sumá también `/` y `/es/`, que siguen con el rastreo del 14/10 a las 15:23, anterior al
castellano completo.

---

**3. GOATCOUNTER: nada que hacer, salvo mirarlo cuando tengas ganas.** Tu panel es
`https://matiasgolman.goatcounter.com`. Quedamos en que lo mirás en unos seis meses.

---

**4. LAS FOTOS, CUANDO QUIERAS.** Dijiste que en algún momento vas a sacar las que te gusten
menos. No corre prisa y no depende de mí: borrás el archivo de `assets/img/photos/` y la galería
se reacomoda sola. El texto alternativo **queda como está**, por decisión tuya del 15/10.

---

**5. ARMAR EL PROYECTO DEL PANEL (y antes, correr Costa Rica en Stata).** Todo está en
`Documents\Investigacion\mercado_trabajo_latam\proyectos\mapa_informalidad\_pipeline\COMO_ARMAR_EL_PROYECTO.md`.
El primer paso es correr `codigos_limpieza\Costa_Rica\master_construccion.do` (~20 min), que
confirma el arreglo del error. Desde ahí, lo del panel se pide en ese proyecto y no en este.

---

**6. DOS ENLACES DEL INEC.** En tu nota, 2025T2 tenía el mismo enlace que 2025T1 (descarga 6544)
y 2026T2 el mismo que 2026T1 (7285). Los archivos que bajaste están bien (cada uno es el
trimestre correcto); falta sólo el número de descarga para la próxima vez. Si lo tenés a mano,
dejalo en el `COMENTARIO DE MATIAS`.

---

**7. LOS 31 GB DE `datos\Costa_Rica\_archivo_consultoria_OIT`.** No los comprimí: casi todo se
rehace con el pipeline nuevo, así que lo razonable es **borrarlo**, no guardarlo, cuando Costa
Rica corra en Stata. Qué es qué:
- `stata\trimestres\` (14 GB): los `.sav` del INEC pasados a `.dta`. Repetido: se borra.
- `stata\panel\cross_paneles`, `pool_paneles`, `cross_ocupados`, `*_en.dta`, `*_en.csv`
  (~15 GB): los paneles de la consultoría. Los rehace el pipeline nuevo: se borran.
- **Se guardan**: `base_awe.dta` y `base_education.dta` (los usa el proyecto de trabajador
  adicional), `ECE_datos_tablas.rar`, `panels and codes.zip` (lo entregado) y los `codebook_*.log`.
  `base_econometrica*.dta` (1,9 GB) sólo si querés poder rehacer las regresiones del Producto 3
  sin volver a correr todo.

Decime «borralo» (o qué cambiarías) y lo hace la próxima sesión del panel.
