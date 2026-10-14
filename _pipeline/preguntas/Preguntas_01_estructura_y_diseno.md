# Cuestionario 1 — estructura, contenido y diseño del sitio

> **AL 13/10 YA ESTÁN CONTESTADAS LAS PREGUNTAS 1, 3, 16 y 19** (en el chat). Están anotadas en
> `ESTADO.md > DECISIONES TOMADAS` como D-01 a D-04. **Saltealas**: quedan 18.

**Cómo contestar:** escribí debajo de cada pregunta, donde dice `→`. Sin formato, como te salga, en
castellano o en inglés. **Si una no la sabés o no te importa, dejala en blanco**: cada pregunta
trae mi recomendación, y lo que quede vacío lo decido yo por ahí y lo anoto en
`ESTADO.md > DECISIONES TOMADAS` para que lo puedas revertir después.

**Por qué tantas preguntas.** El sitio que tenés hoy es la plantilla de otra persona: un estudiante
de doctorado en el mercado académico. Esa plantilla trae decisiones metidas adentro (el JMP arriba,
el blog de ejemplo, el CV como PDF suelto) que no son tuyas. Antes de escribir código quiero que
las decisiones sean tuyas, o por lo menos explícitas.

**Un aviso sobre mis recomendaciones:** en cuatro lugares te voy a decir que lo que pediste no es
lo mejor (son las preguntas **10**, **11**, **13** y **19**). Me pediste criterio crítico, así que
ahí está. Vos decidís igual.

---

## BLOQUE A — Posicionamiento: para quién es este sitio

### 1. ¿Quién es el lector que más te importa?
Elegí **dos** y ordenalos. Todo lo demás (qué va arriba, cuánto texto, qué tono) sale de esto.

- (a) Quien recluta en un organismo internacional (OIT, BM, OCDE, BID, CEPAL)
- (b) Quien recluta en un instituto holandés de política (CPB, SCP, SEO, Ecorys, DNB, TNO, WODC)
- (c) Colegas académicos (referees, coautores, seminarios)
- (d) Periodistas y público general
- (e) Clientes potenciales de consultoría
- (f) Estudiantes de Utrecht

→ b, e - Aunque pueden ser tambien colegas academicos y que ya trabajan en institutos, que no necesariamente me vayan a contratar, pero se acordaron de mi y me pueden recomendar para trabajos. Tambien publico en general, estudiantes. En OIT o esos organismos, no busca mi perfil directo alguien de RRHH, posiblemente sea un contacto inicial con alguien que ya conozco. Es distinto.

**Mi recomendación:** (a) y (b) primero, (c) tercero y presente pero no al mando. La diferencia
práctica es grande: un referee quiere el paper y el abstract; alguien de RRHH de la OIT o del CPB
quiere saber en 40 segundos **qué sabés hacer, con qué datos, para quién lo hiciste y si sabés
escribir para un ministro**. Son dos sitios distintos. El que tenés hoy es para (c).

### 2. Si el sitio funcionara perfecto, ¿qué pasaría en los próximos dos años?
Una sola respuesta: ¿que te escriban para una entrevista? ¿que te inviten a consultorías? ¿que te
citen? ¿que te inviten a hablar o a escribir en prensa? ¿que un ex colega te encuentre?

→ Que un Ex colega me encuentre y potencialmente me invite a una consultoria

**Mi recomendación:** definir una. Un sitio que quiere lograr cinco cosas no logra ninguna, porque
la jerarquía visual no se puede repartir en cinco.

### 3. ¿Cuán explícito querés ser con que estás pensando en moverte de trabajo?
Esto es delicado: la web es pública y tus colegas y jefes de Utrecht la pueden leer.

- (a) **Explícito**: una línea tipo «open to roles in policy research and evaluation».
- (b) **Implícito**: el CV al día, el perfil orientado a política, y nada que diga que buscás.
- (c) **Nada**: puramente un sitio de portafolio.

→ por el momento, b) Implicito

**Mi recomendación:** (b). Con un sitio bien posicionado, quien recluta no necesita que le avises
que estás disponible: te escribe igual. Y (a) tiene un costo asimétrico — no te suma nada con
quien te quiere contratar, y te puede costar algo con quien hoy te paga el sueldo. Para señalar
disponibilidad sin cartel, está LinkedIn, que tiene un ajuste privado («Open to work», visible sólo
para reclutadores) hecho exactamente para esto.

### 4. ¿Dominio propio, o seguimos en `matiasgolman.github.io`?
Después de los links entrantes, es la palanca más grande de Google a mediano plazo.

- (a) Comprar `matiasgolman.com` (~12 €/año)
- (b) Comprar `matiasgolman.nl` (señal local holandesa, útil si el objetivo es (b) de la pregunta 1)
- (c) Quedarnos en `matiasgolman.github.io` (gratis)

→ Por el momento, matiasgolman.github.io. No estoy pensando en cambiar de trabajo en al menos un año. Quiero usar esta experiencia como modelo de prueba, ir llenandola de contenido, como excusa para escribir notas y subirlas, refinarlo, y mas adelante ver si tiene sentido tener un matiasgolman.com

**Mi recomendación:** (a), y lo antes posible. Razones: tu nombre queda en la URL; dejás de
depender de que GitHub siga regalando el subdominio; si algún día te mudás de Jekyll a otra cosa,
los links que juntaste siguen sirviendo. **La contra honesta:** una mudanza de dominio cuesta unas
semanas de ranking mientras Google reprocesa los redirects — por eso, si lo vamos a hacer, hay que
hacerlo **ahora**, antes de empezar a juntar links, no en un año. Lo tenés que comprar vos (yo no
puedo pagar nada); después configuro el `CNAME` y los DNS.

### 5. ¿Una versión en castellano?
Tu trabajo con OIT, CEPAL, Argentina y Costa Rica es en castellano, y buena parte de la gente que
te podría contratar para eso lee en castellano.

- (a) Sólo inglés
- (b) Inglés + una página «Español» con el perfil y los trabajos en castellano
- (c) Sitio bilingüe completo (cada página en los dos idiomas)

→ Ahora no esta en ambos? hagamosla b entonces.

**Mi recomendación:** (b). (c) duplica para siempre el trabajo de mantenimiento y, en un sitio
personal, casi nadie lee las dos versiones. (b) te da lo que importa (que alguien de la OIT en
Lima o del Ministerio de Trabajo de Costa Rica te lea en su idioma y encuentre tus informes) con
una sola página extra.

### 6. En una frase y sin jerga: ¿qué hacés?
Escribila vos, como se la dirías a alguien en un ascensor que no es economista. Me va a servir
para el `<title>`, la metadescripción, el JSON-LD y el primer párrafo de la home — los cuatro
lugares donde Google y una persona apurada deciden quién sos.

→ Soy un Economista Laboral, experto en temas de informalidad, habilidades laborales y desarrollo economico. Tengo un rol docente activo, una fuerte capacidad de lectura critica y manejo de bases de datos y progracion.


Me gusta tu version, aunque lo haria un poquito mas generico; soy un experto en economia laboral. Tengo la capacidad y el conocimiento para trabajar en temas que no son exactamente los que ya trabaje (informalidad, habilidades, desempleo), sino que puedo trabajar multiples temas (desigualdad, pobreza, migracion, salario minimo, educacion, politica industrial, instituciones). Tengo una rapida capacidad de adaptacion y aprendizaje.

**Mi versión, para que la corrijas:** «Economista laboral. Mido cómo funciona el empleo informal,
qué políticas lo reducen y qué habilidades piden las empresas — y convierto esos datos en evidencia
que se pueda usar para decidir.»

---

## BLOQUE B — Contenido: qué entra, qué sale, qué falta

### 7. Los tres working papers: ¿cuáles pueden ser públicos y cómo se llaman ahora?
Hoy el sitio tiene: el JMP (*AI adoption on Personality Traits demand*), *The Value of Personality*
y el meta-análisis de formalización. **Todos están marcados como de 2026 y sin estado.** Para cada
uno: ¿PDF público, o sólo título y abstract? ¿Está enviado a alguna revista, en R&R, publicado?
¿Alguno tiene restricciones de coautores (Escudero, López-Mourelo)?

→ Si, sacar la etiqueta de JMP y dejar todo como working paper, luego te paso las ultimas versiones

**Mi recomendación:** sacar la etiqueta «job market paper» de los tres. Fuera del mercado académico
no significa nada, y en el mercado de política suena a que todavía estás buscando el primer
trabajo. Pasan a ser «working papers», con el estado al lado si lo tiene.

### 8. Los nueve PDFs del JMP en `assets/pdf/`
Hay `jmp_june25`, `jmp_aug25`, `jmp_sep25`, `jmp_oct25`, `jmp_nov25`, `jmp_dec25`, `jmp_jan26`,
`jmp_last_version`, más cuatro CVs viejos. ¿Los borro, o alguno lo mandaste por mail y querés que
el link siga vivo?

→ Borra las versiones viejas, dejar solo una version estable.

**Mi recomendación:** dejar una sola versión de cada paper, con el nombre estable
(`golman_2026_personality_ai.pdf`), y archivar el resto fuera del repo. Pero **no borrar nada hasta
que me confirmes**: si pusiste `jmp_oct25.pdf` en una postulación, ese link tiene que seguir
funcionando.

### 9. Los dos proyectos propios: ¿en qué estado están?
- **Dashboard de informalidad argentina**: hoy es un HTML de **73 MB** dentro del repo. ¿Existe la
  fuente (script, datos) de la que se genera? ¿Es la versión final? ¿La OIT lo publicó en algún
  lado (si sí, mejor linkear al sitio de la OIT y además tenerlo acá)?
- **App Araucaria**: ¿cuál es la URL que funciona? ¿Dónde vive el código? ¿Cuánta gente la usa?

→ El dashbord esta estable, tengo el codigo y las bases que lo genera, todo esta accesible. Lo quiero actualizar y mejorar la interfaz y algunas cuestiones de los datos, quizas agregar neuvos paises. Tu me vas a ayudar mas adelante. pero no en esta conversacion. La OIT no lo publico. El dashbord es pesado porque son muchisimos datos, es lo mas reducido que pude lograr!

La app de la araucaria esta en proceso de ser publicada por Google Play, el codigo vive en esta computadora, por ahora solo la usan 10 personas al mes. Es una app de telefono, pero peudes acceder por aca https://araucaria-spotter.vercel.app/ 

**Mi recomendación:** estos dos proyectos son, para el público que te importa, **más persuasivos
que los tres papers**. Un dashboard que un gobierno usa y una app que mapea árboles prueban tres
cosas que un paper no prueba: que terminás cosas, que las hacés usables por otros, y que sabés
construir, no sólo estimar. Van arriba en la home, con una imagen cada uno. Pero 73 MB de HTML
tardan como 40 segundos en una conexión mala y mucha gente se va antes: hay que partirlo.

### 10. Las fotos de naturaleza
Me pediste que traiga las fotos de tu Instagram. **Te lo voy a discutir.**

Lo técnico: la API de Instagram sólo sirve con cuenta de empresa o creador, el token caduca cada 60
días (se renueva a mano) y los widgets de terceros o se rompen o te meten rastreadores de terceros
en el sitio. Pero el argumento de fondo es otro: en Instagram están **todas** tus fotos; en el
sitio tienen que estar **las doce mejores**. Una galería curada con tus archivos carga rápido, la
puede leer Google (una foto embebida de Instagram es invisible para el buscador) y la controlás vos.

- (a) Galería curada con archivos que me pasás (**mi recomendación**), con un link a tu Instagram
- (b) Insistir con el feed automático de Instagram
- (c) Las dos: galería curada + link al perfil

→

**Y una pregunta de fondo:** ¿las fotos van como **sección propia** («Photography»), como una
**página personal** donde conviven la foto y la biografía larga, o integradas al diseño (por
ejemplo, una foto tuya de paisaje de fondo en la portada)? Mi recomendación es sección propia, en
la navegación pero al final, y **nunca** mezcladas con el trabajo: a quien te está evaluando
profesionalmente, las fotos le suman como señal de persona completa, pero sólo si están ordenadas.

→ link a Instagram: https://www.instagram.com/gol.mat/ . No se como ver la version de fotos. Solo me gusta subir fotos de naturaleza cuando viajo, cuando exploro. suelo tener mi instagram abierto porque no solo no tengo nada que esconder, sino que creo que suma si un desconocido ve mis fotos y ve que soy aventurero, que disfruto la naturaleza. No se como mostrar eso, si en una seccion propia o solo un link a instagram o. Quizas como seccion propia, pero tampoco quiero ser "fotografo", no lo soy, solo me gusta viajar y documentar la naturaleza que veo.

### 11. El blog
Me dijiste que en el futuro querés notas, reflexiones, borradores de piezas de prensa. **Te lo voy
a discutir también:** un blog con cero posts, o con tres de hace dos años, resta. Es lo primero que
mira alguien que quiere saber si escribís seguido, y un blog abandonado dice que no.

Entonces: **¿cuáles son las primeras tres cosas que escribirías?** Título aproximado y de qué va.
Si no te salen tres, decímelo y armamos la sección sin publicarla (lista para encender el día que
tengas el primer texto).

→ Tengo muchos datos descargados sobre cosas de bariloche (te puedo dar acceso si queres), que van desde informacion geografica, educacional, de hospedajes de booking y demanda, y en algun momento me gustaria tener reflexiones etc. Quizas me gustaria crear la seccion, y a medida que la vaya llenando, la "abrimos" al publico. Te parece? es tu recomendacion. Notes me parece bien de nombre. OK con lo de "qué funciona para formalizar empleo en América Latina, según 150 evaluaciones". Ve las conclusiones de mi paper sobre meta analisis.

**Mi recomendación:** armarla pero **no linkearla** hasta que haya tres textos. Y que no se llame
«Blog»: que se llame **«Notes»** o **«Writing»**, que no promete frecuencia. Lo que sí publicaría
ya: dos o tres notas cortas (600-900 palabras) explicando en castellano llano un resultado tuyo —
por ejemplo «qué funciona para formalizar empleo en América Latina, según 150 evaluaciones». Ese
tipo de texto es exactamente lo que hace que alguien del CPB o de la OIT se acuerde de tu nombre,
y de paso es lo que Google puede indexar (un PDF rankea mucho peor que una página).

### 12. ¿Qué NO querés que esté en el sitio?
Temas, opiniones (políticas, Argentina), datos personales, ubicación exacta, familia, religión,
fotos de otras personas, tu teléfono. **Es la única pregunta cuya respuesta equivocada es difícil
de deshacer** (una vez que Google lo indexa, queda en el caché un tiempo).

→ I have saved a new CV withouth the phone, and change the Adress to Utrecht (which is where the university is). I think having the address is fine, becouse people may not know if I am still in Utrecht, in Nottingham in ARgentina.

**Nota:** hoy el CV que está público en el sitio tiene **tu teléfono** y **la ciudad donde vivís
(Zeist)**. Eso es decisión tuya, pero decímelo explícitamente. Lo normal en un CV público es dejar
el mail y el país, y dar el teléfono sólo cuando te lo piden.

### 13. ¿Qué hacemos con la página «personal statement»?
Es el mejor texto del sitio: está bien escrito, es personal y es raro de encontrar. Pero está
escrito **para un comité de selección académico** («If I were on the hiring side of the
equation…»), y eso se nota.

- (a) Reescribirla como **«About me»**, en primera persona, sin el marco de postulación (**mi
  recomendación**)
- (b) Dejarla como está
- (c) Partirla: dos párrafos en la home, el texto largo en su propia página

→Reescribirla como About me. Sin el hiring, pero mantieniendo la gran mayoria del texto y la parte personal. Solo recorta/modifica la parte del hiring. O quizas poner algo con que estoy abierto a sumarme a proyectos de investigacion, politica o coordinacion?

### 14. Docencia
Hoy la página lista siete puestos de asistente en Nottingham y cuatro premios. Para un público de
política, una lista larga de asistencias de doctorado se lee como «junior».

- (a) Página de docencia con lo de Utrecht arriba (lecturer, dos cursos, supervisión) y Nottingham
  condensado en dos líneas + los premios (**mi recomendación**)
- (b) Dejar la lista completa
- (c) Sacar la página y que la docencia viva sólo dentro del CV

→ a) tu recomendacion. Son muchos los cursos que estoy enseniando en Utrecht, no se si condensarlos o mostrarlos todos.

### 15. ¿CV como PDF suelto, o también una página HTML?
Hoy el ítem «cv» del menú es un link directo al PDF. Google lee los PDFs, pero mucho peor que una
página; y un PDF no se puede actualizar sin romper el link.

- (a) Página HTML de CV + botón «descargar PDF» (**mi recomendación**: es la página que más te va a
  ayudar a aparecer cuando alguien busca «Matias Golman labour economist»)
- (b) Sólo el PDF, como ahora

→ OK, pagina HTML de CV. No se como generar eso.

---

## BLOQUE C — Diseño: cómo se ve

### 16. Registro visual
Cuatro direcciones posibles. No es sólo gusto: cada una le habla a un lector distinto.

- (a) **Institucional sobrio.** Mucho blanco, una tipografía sans discreta, un solo color de acento
  frío, datos y tablas limpias. Se parece a un CPB o una OCDE. Dice: «soy de confianza, trabajo con
  rigor». Riesgo: parecerse a todos.
- (b) **Editorial.** Una serif buena para leer, columna angosta, mucho aire, los textos como
  protagonistas. Se parece a una revista o a un Substack cuidado. Dice: «escribo y pienso». Es el
  que mejor aguanta un blog y una galería de fotos juntos.
- (c) **Mínimo cálido.** Neutros tibios, un verde o un terracota apagado, bordes suaves, una foto de
  paisaje tuya como única imagen grande. Dice: «persona, no institución».
- (d) **Técnico / de datos.** Oscuro o gris, algún detalle monoespaciado, gráficos como decoración
  funcional. Dice: «hago esto con código». Riesgo: frío, y envejece rápido.

→ Si, me quedo con tu recomendacion.

**Mi recomendación:** **(b) con el calor de (c)**: serif para leer, una paleta neutra con un acento
verde profundo sacado de tus propias fotos, y los proyectos como tarjetas con imagen. Es el único
registro que sostiene las tres cosas que querés en un mismo sitio (trabajo serio, escritura, fotos)
sin que ninguna parezca fuera de lugar. (a) te haría una copia del sitio de tu futuro empleador,
que es un error sutil pero real: no te distingue.

### 17. ¿Foto tuya en la portada?
- (a) Grande, arriba, al lado del primer párrafo
- (b) Chica, de perfil, al costado (como ahora)
- (c) Sin foto

→ b. La foto que esta ahora me gusta, es al aire libre, y sino tengo una foto mas formal, con camisa, sonriendo, pero en un espacio cerrado. Pero es retrato de estudio, no tengo fotos lindas dando clase / panel / presentando.

**Mi recomendación:** (a) o (b), nunca (c). Un sitio personal sin cara se lee como un CV, y el 80%
de la gente que lo abra ya sabe tu nombre y quiere ponerle cara. Si tenés una foto trabajando
(dando clase, en un panel, presentando), mejor que un retrato de estudio.

### 18. Colores y tipografías: ¿hay algo que te guste o que odies?
Un color que uses siempre, uno que no quieras ver, alguna web que te guste cómo se ve (pasame el
link, es la información más útil que me podés dar acá).

→ Me gusta el verde. Me gusta asociarme al verde. OK con tus descartes. Seguro que el modo oscuro automatico no va? me da la impresion de seriedad, de algo gourmet.

**Dos cosas que yo descartaría de entrada:** el azul institucional de la OIT o de la ONU (parece
que te hacés pasar por el organismo) y el modo oscuro automático, que hoy el sitio tiene prendido
y que en un sitio de cinco páginas duplica el trabajo de diseño para que lo use muy poca gente.
Las tipografías las voy a **autoalojar** en vez de llamarlas a Google Fonts, que además de ser más
rápido te evita el problema de GDPR de mandar la IP de tus visitantes europeos a Google.

### 19. El stack: ¿seguimos con al-folio?
Esta es la decisión técnica grande, y acá también te voy a discutir una premisa. al-folio es un
tema muy bueno **para lo que fue hecho**: un sitio académico con muchas publicaciones, citas,
badges de Altmetric, notebooks de Jupyter y matemática. Vos usás casi nada de eso, y a cambio
cargás con 1,5 GB de repo, 31 posts de demo, nueve proyectos de demo, veinte plugins de Ruby y un
workflow de GitHub Actions de 90 líneas que se puede romper en cualquier actualización.

- (a) **Limpiar al-folio donde está**: borrar la demo, arreglar el config, reescribir el contenido,
  restilar. Rápido (días), menor riesgo, y te queda la maquinaria que no usás.
- (b) **Jekyll propio y mínimo en el mismo repo**: cinco layouts escritos a medida, sin plugins
  salvo sitemap y feed, control total del HTML y del CSS. Más trabajo al principio (una semana),
  mucho menos mantenimiento después, y el sitio deja de parecerse a los otros mil al-folio.
  **Mi recomendación.**
- (c) **Dejar al-folio casi como está** y sólo cambiar los textos.

→ OK con tu recomendacion (b).

**Por qué (b):** lo que querés hacer —portada con posicionamiento, tarjetas de proyecto, galería de
fotos, notas, una página de CV en HTML, datos estructurados bien hechos— es más fácil de escribir
de cero que de arrancarle a al-folio. Y el beneficio de SEO es directo: hoy el 85% de tus URLs son
plantilla duplicada; en (b) el 100% del sitio es tuyo. Seguimos en Jekyll y en GitHub Pages (no te
cambio de tecnología, no tenés que aprender nada nuevo).

### 20. ¿Cuántas páginas querés mantener?
Cada página es una promesa de mantenimiento.

- (a) **Cinco**: Home, Research & policy work, Projects, Writing, About (+ CV y fotos dentro)
- (b) **Siete u ocho**: lo de arriba separando CV, Teaching y Photography
- (c) **Una sola página larga** con todo y anclas

→ vamos con la opcion (a)

**Mi recomendación:** (a) al lanzar, con Photography y Writing como sexta y séptima cuando haya
material. (c) se ve moderno pero rankea peor (una sola URL compite por todo) y envejece mal.

---

## BLOQUE D — Operación

### 21. ¿Analítica?
¿Querés saber cuánta gente entra, de dónde y a qué páginas?

- (a) Nada
- (b) Algo liviano y respetuoso de la privacidad (GoatCounter gratis, o Plausible ~9 €/mes): sin
  cookies, sin banner de consentimiento, y no le regalás los datos de tus visitantes a Google
  (**mi recomendación**)
- (c) Google Analytics

→ Si es gratuita, si. Sino, no. 

**Nota:** Google **Search Console** (el del to-do, ítem 4) es otra cosa y hay que tenerlo igual:
no mide visitas, te dice qué ve Google de tu sitio. Eso no es opcional si queremos resolver el
problema de las búsquedas.

### 22. Ritmo y autonomía
¿Cómo querés trabajar esto?

- (a) Yo avanzo entre tus mensajes y vos revisás cuando podés (como el pipeline de `tenure`)
- (b) Querés aprobar cada cambio antes de que se publique
- (c) Una corrida agendada (por ejemplo, semanal) que avanza la cola sola y te deja el resumen

→ Si, hagamos tu recomendacion. incluido el preview.

**Mi recomendación:** (b) **para el rediseño** (vas a querer ver la portada antes de que exista en
internet) y (a) o (c) después, para el mantenimiento. Y una cosa concreta: puedo armar una **rama
de preview** para que veas el sitio nuevo entero, con su URL, sin tocar el que está publicado. Así
el cambio no es un salto al vacío.

---

*Fin del cuestionario. Cuando lo tengas, avisame por el `COMENTARIO DE MATIAS` de `ESTADO.md` o
directo por chat. Con las respuestas armo la arquitectura de contenido (qué página dice qué, en qué
orden) y te la paso para aprobar antes de escribir una línea de código.*
