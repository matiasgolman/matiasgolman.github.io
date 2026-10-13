# Pipeline del sitio personal — cómo funciona

Cuatro archivos, igual que en el proyecto `tenure`. Toda corrida (mía, agendada o no) arranca
leyendo en este orden:

1. **`ESTADO.md`** → el bloque `COMENTARIO DE MATIAS` (arriba de todo), `En una pantalla`, y la
   `COLA DE TRABAJO`. Es la fuente de verdad: dónde estamos, qué sigue, qué se decidió.
2. **`To-Do-Matias.md`** → sólo lo que está esperando una acción tuya (subir algo, decidir algo,
   crear una cuenta, pushear). Nada de historia ni de confirmaciones.
3. **`Changelog.md`** → qué pasó, en orden cronológico inverso. Se escribe a medida que se cierra
   cada ítem, no al final.
4. **`preguntas/`** → los cuestionarios largos. Los contestás ahí mismo, escribiendo debajo de cada
   pregunta, o en el `COMENTARIO DE MATIAS` si preferís.

**Dónde me dejás instrucciones:** el bloque `COMENTARIO DE MATIAS`, arriba de todo en `ESTADO.md`.
Yo lo leo primero, lo archivo literal en `_archivo/Comentarios_Matias.md` con fecha, y vuelvo a
vaciar el bloque. Podés escribir en castellano o en inglés, sin formato, como te salga.

**Higiene (es parte del trabajo, no un extra):**
- `To-Do-Matias.md` lleva SÓLO acciones tuyas. Un ítem resuelto se va del archivo ese mismo día.
- `ESTADO.md` no acumula historia: lo que pasó va al `Changelog.md`. `En una pantalla` se reescribe
  entero en cada corrida y no pasa de ~40 líneas.
- Un ítem de la cola que se cierra se reduce a una línea; el detalle se archiva en `_archivo/`.
- La corrida que deja estos archivos más largos que como los encontró, sin haber abierto trabajo
  nuevo, no terminó.

**Esta carpeta no se publica.** Está excluida del build de Jekyll (`exclude:` en `_config.yml`), así
que nada de acá aparece en el sitio. Sí se versiona en git, para tener historia.
