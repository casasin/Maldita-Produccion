# ¡Chequea, maldito!

### Chequeo de problemas tontos

- "Paths/Correct Path Directions": Mejor haberlo hecho antes, ahora te jodes si se fastidia todo.
- Crear el glifo /nbspace (uni00A0), se hace solo a partir del espacio.
- Crear /softhyphen (u00AD).
- Asegurarse de que todas las letras estén en un grupo de kerning.
- Chequear los glifos con *dotbelow*, que fallan a veces.
- Revisar prosas de Q Ơ Ư Ǿ (o mejor, usar "=|@300" o similar en el espaciado y olvidarse)
- Revisar el kerning de /lcaron, /dcaron, y /tcaron.
- Revisar ligaduras, æ y œ
- Pon un texto de descripción en los *Stylistic Sets*.
- Revisar los componentes anidados. No dejar componentes dentro de otros en los archivos finales. "Scripts/Mekkablue/Components/Component Problem Finder" y hay un plugin "mekkablue/UnnestComponents" en el Plugin Manager.

### Scripts de chequeo de Trazados:

- "Mekkablue/Paths/Path Problem Finder"
- "Mekkablue/Paths/Find Near vertical Misses"
- "Mekkablue/Paths/Rewire Fire"
- "Mekkablue/Paths/New Tab with Small Paths" (entre 600-700 square units. Activar *After Overlap*...)
- "Mekkablue/Paths/Green Blue Manager"

Estos scripts ponen emojis en los nodos con fallo y te dejan la tipo hecha un asco. Para borrar los emojis volver a chequear o: "Mekkablue/Glyphs Names.../Garbage Collection"

### Scripts de chequeo de interpolación:

- "Mekkablue/Interpolation/Find Shapesifting Glyphs"
- "Mekkablue/Interpolation/Travel Tracker"
- "Mekkablue/Interpolation/Kink Finder"
- "Mekkablue/Interpolation/Dekink Master Layers"
- "Mekkablue/Interpolation/New Tab with Dangerous..."

### Chequeo tras deshacer componentes

Es buena idea deshacer componentes en glifos donde los componentes se solapen (/Tbar, /dollar, /cedilla, etc) aunque para Variables dejar los componentes puede hacer todo más facil.

Hacer bonica la unión de /ogoneks, /uhorn y /ohorn si procede.


### Chequeo de problemas con Fontbakery

Se hace en el **Terminal**. Es un programilla de Google para chequear fuentes OpenType. Se puede hacer el check de Adobe, de Google, etc.

- Botón derecho sobre la carpeta que tengamos la fuente / Abrir Terminal en la carpeta.
- `fontbakery check-adobe` (arrastramos el archivo)

Si todo está OK saldrá una magdalena, si no toca pringar. Algunos de estos errores serán de dibujo, de los vertical metrics, de cualquier cosa, vamos.

Unas pocas opciones extra:

- `fontbakery -l FAIL check-adobe archivo` para ver sólo 🔥 FAILs
- `fontbakery check-adobefonts --html test.html nombre_de_archivo.html` para tener los - resultados en html.
- `fontbakery check-adobefonts --github-markdown test.md nombre_de_archivo.md` para tener los resultados en Markdown.
- `fontbakery -h` para ver tooodas las opciones (o `--help`).
- `fontbakery check-adobefonts --help` para ver la ayuda del check de Adobe concretamente.
