# Trivial del Lore

Pantalla de preguntas para jugar con el **tablero físico** del Trivial. La ficha cae en un color, tocas esa categoría en la pantalla y sale una pregunta. Si es casilla de quesito, marcas «Es casilla de quesito» y sale una difícil. El marcador de la izquierda lleva los quesitos de cada equipo.

Web publicada: **https://ciaseg.github.io/trivial/**
Enlace directo al creador de preguntas (para mandar a las amigas): **https://ciaseg.github.io/trivial/?crear**

## Cómo crean preguntas las amigas

1. Abren el enlace `?crear` en el móvil y ponen su nombre.
2. **+ Nueva pregunta**, rellenan el formulario y **Guardar**.
3. Pueden **Editar** o **Borrar** sus preguntas cuando quieran, también las que ya están publicadas.
4. Pulsan **📤 Enviar a Lucía**, eligen WhatsApp y te llega un **.zip** con sus cambios (nuevas, editadas y borradas, con fotos).

## Cómo lo publica Lucía

1. Guarda el `.zip` de WhatsApp en el ordenador.
2. Clic derecho → **Extraer todo…** → en «Destino» pon la carpeta del proyecto (`...\Downloads\trivial\trivial`, **borrando el nombre del zip que Windows añade al final**). Se crean/llenan las carpetas `envios` e `imagenes`.
3. En IntelliJ: **Git → Commit…**, marca lo nuevo de `envios/` e `imagenes/` y **Commit and Push**. En 1–2 minutos está en la web.

Cada envío es un archivo aparte dentro de `envios/` (con fecha y nombre), así que nunca se pisan entre amigas. La web los aplica en orden encima de `preguntas.xlsx`.

Tú también puedes crear, editar o borrar **cualquier** pregunta desde la web (pon «Lucía» como nombre): tus cambios salen en un zip igual, con el botón **📦 Descargar zip para GitHub**.

> La web lee la lista de envíos desde GitHub (`CiaSeg/trivial`, rama `master`). Si cambias el nombre del repo o de la rama, cambia `REPO` y `BRANCH` al principio del script de `index.html`.

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

Los Excel de `envios/` tienen además una columna **Acción** (`Nueva`, `Editar` o `Borrar`).

## Probar en local con IntelliJ

Abre `index.html` y pulsa el icono de navegador que sale arriba a la derecha del editor. Con doble clic desde la carpeta el navegador no deja leer el Excel.

## Cómo se juega

1. Pon los equipos y quién está en cada uno.
2. Tira el dado en el tablero físico y mueve la ficha.
3. Toca la categoría del color donde has caído. Si es casilla de quesito, marca antes «Es casilla de quesito».
4. «Ver respuesta» → «Acierto» (tira otra vez y, si era casilla de quesito, se lo lleva) o «Fallo» (pasa el turno).
5. Con todos los quesitos, el equipo elige categoría y se juega la pregunta final (difícil).

> Si el repo es público, cualquiera con el enlace puede ver las respuestas. Que no curioseen antes de la cena 😉
