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
