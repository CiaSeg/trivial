# Trivial del Lore

Pantalla de preguntas para jugar con el **tablero físico** del Trivial. La ficha cae en un color, tocas esa categoría en la pantalla y sale una pregunta. Si es casilla de quesito, activas «Pregunta de quesito» y sale una difícil.

Las preguntas viven en **`preguntas.xlsx`**. Para cambiarlas solo hay que editar el Excel y subirlo a GitHub.

## Columnas del Excel (hoja «Preguntas»)

| Columna | Qué poner |
|---|---|
| Categoría | Nombre de la categoría. Las 6 primeras que aparezcan toman los colores azul, rosa, verde, naranja, amarillo y rojo, en ese orden. |
| Dificultad | `Normal` o `Difícil`. Las difíciles salen en las casillas de quesito. |
| Persona (no le puede tocar) | Si esa persona está en el equipo que juega, la pregunta no le sale. Varias, separadas por comas. |
| Pregunta | El texto. |
| Opciones (separadas por ;) | Vacío si es abierta. Si es tipo test: `Opción A; Opción B; Opción C`. |
| Respuesta | La correcta. Si coincide con una opción, se marca en verde. |

## Trabajar desde IntelliJ

1. **File → New → Project from Version Control…** y pega `https://github.com/CiaSeg/trivial.git`.
2. Copia en esa carpeta los archivos de este proyecto (`index.html`, `preguntas.xlsx`, `README.md`, `.gitignore`).
3. Para probar: abre `index.html` y pulsa el icono de navegador que aparece arriba a la derecha del editor. IntelliJ lo sirve con su servidor local y así el Excel se lee bien. (Si lo abres con doble clic desde la carpeta, el navegador no deja leer el Excel; la página te ofrece elegirlo a mano.)
4. Para publicar cambios: **Git → Commit…** (Ctrl+K / Cmd+K), marca los archivos, escribe un mensaje y pulsa **Commit and Push**.

## Publicarlo para tus amigas (GitHub Pages, una sola vez)

1. En GitHub, entra en el repo → **Settings → Pages**.
2. En *Build and deployment*, Source: **Deploy from a branch**, Branch: **main**, carpeta **/(root)** → Save.
3. En un par de minutos estará en **https://ciaseg.github.io/trivial/**.

Cada vez que hagas push con un Excel nuevo, la web se actualiza sola (tarda uno o dos minutos). En la partida, el botón «Recargar Excel» trae la última versión sin recargar la página.

> Ojo: si el repo es público, cualquiera con el enlace puede ver las preguntas y respuestas. Que no lo abran antes de la cena 😉

## Cómo se juega

1. Pon los equipos y quién está en cada uno (los nombres como en la columna «Persona»).
2. Tira el dado en el tablero físico y mueve la ficha.
3. Toca en pantalla la categoría del color donde has caído. Si es casilla de quesito, activa antes «Pregunta de quesito».
4. «Ver respuesta» → «Acierto · sigue» o «Fallo · pasa turno».

La web recuerda qué preguntas ya han salido (en ese navegador) para no repetirlas. «Equipos → Olvidar preguntas ya usadas» lo reinicia.
