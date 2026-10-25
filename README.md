# Trivial del Lore

Pantalla de preguntas para jugar con el **tablero físico** del Trivial. La ficha cae en un color, tocas esa categoría en la pantalla y sale una pregunta. Si es casilla de quesito, marcas «Es casilla de quesito» y sale una difícil. El marcador de la izquierda lleva los quesitos de cada equipo.

Web publicada: **https://ciaseg.github.io/trivial/**
Enlace directo al creador de preguntas (para mandar a las amigas): **https://ciaseg.github.io/trivial/?crear**

## Cómo crean preguntas las amigas (sin saber nada de Excel)

1. Abren el enlace `?crear` en el móvil y ponen su nombre.
2. Pulsan **+ Nueva pregunta** y rellenan el formulario: categoría, normal o difícil, la pregunta, la respuesta (libre o tipo test), fotos si quieren y a quién no le puede tocar.
3. Cuando acaban, pulsan **Enviar mis preguntas a Lucía** → **Compartir** y te lo mandan por WhatsApp (es un archivo `.zip`).

Sus preguntas se quedan guardadas en su móvil hasta que las envían; pueden volver otro día y seguir.

## Cómo las publica Lucía

En la web, pestaña **Crear preguntas → Zona de Lucía (organizadora)**:

1. **Elegir archivos…** y selecciona los `.zip` que te han mandado. Aparecen en «Recibidas»; puedes editarlas o borrarlas.
2. Si quieres, **Ver y editar las publicadas** para cambiar o quitar preguntas que ya estaban.
3. **Descargar todo para GitHub** → descarga `trivial-para-github.zip`. Descomprímelo dentro de la carpeta del proyecto (la que tiene `index.html`), aceptando sustituir `preguntas.xlsx` y juntando la carpeta `imagenes`.
4. En IntelliJ: **Git → Commit…**, marca los archivos nuevos (también los de `imagenes/`), escribe un mensaje y **Commit and Push**. En 1–2 minutos está publicado.
5. Comprueba que se ve bien y pulsa **Vaciar este dispositivo** para empezar limpio.

> Haz el trabajo de organizadora siempre desde la misma dirección (la web publicada). Lo que se guarda en el navegador de `ciaseg.github.io` no se ve si abres la página desde IntelliJ (`localhost`), y al revés.

## El Excel (`preguntas.xlsx`)

Sigue siendo la base de datos y se puede editar a mano si prefieres:

| Columna | Qué poner |
|---|---|
| Categoría | Las 6 primeras que aparezcan toman los colores azul, rosa, verde, naranja, amarillo y rojo. |
| Dificultad | `Normal` o `Difícil`. Las difíciles salen en las casillas de quesito y en la pregunta final. |
| Persona (no le puede tocar) | Si esa persona está en el equipo que juega, no le sale. Varias, separadas por comas. |
| Pregunta | El texto. |
| Opciones (separadas por ;) | Vacío si es abierta. Tipo test: `Opción A; Opción B; Opción C`. |
| Respuesta | La correcta. Si coincide con una opción, se marca con ✓. |
| Imagen pregunta / Imagen respuesta | Nombre del archivo dentro de la carpeta `imagenes/`. |
| Autora / ID | Los rellena la web. Si añades filas a mano, déjalos vacíos. |

## Probar en local con IntelliJ

Abre `index.html` y pulsa el icono de navegador que sale arriba a la derecha del editor. Con doble clic desde la carpeta el navegador no deja leer el Excel.

## Cómo se juega

1. Pon los equipos y quién está en cada uno.
2. Tira el dado en el tablero físico y mueve la ficha.
3. Toca la categoría del color donde has caído. Si es casilla de quesito, marca antes «Es casilla de quesito».
4. «Ver respuesta» → «Acierto» (tira otra vez y, si era casilla de quesito, se lo lleva) o «Fallo» (pasa el turno).
5. Con todos los quesitos, el equipo elige categoría y se juega la pregunta final (difícil).

> Si el repo es público, cualquiera con el enlace puede ver las respuestas. Que no curioseen antes de la cena 😉
