# 🏀 Larrobeltz Saskibaloi Taldea — Web Oficial

Bienvenido/a al repositorio oficial de la página web de **Larrobeltz Saskibaloi Taldea**, el club de baloncesto de Alonsotegi (Bizkaia). Este proyecto es una web estática, moderna, *responsive* y bilingüe (Castellano / Euskera) diseñada para dar a conocer la historia, los valores, los equipos, los horarios y la información del club.

---

## 🌟 Características Principales

* **Design & UX:** Estilo oscuro (*Dark Mode*) deportivo, limpio e impactante.
* **100% Responsive:** Adaptado para móviles, tablets y ordenadores.
* **Bilingüe (ES / EU):** Selector de idioma estático superior para cambiar al instante entre castellano y euskera.
* **Estructura Completa:**
  * **Inicio / Hero:** Presentación del club y llamados a la acción.
  * **Valores:** Identidad, compromiso social y deportivo.
  * **Historia:** Reseña histórica desde la fundación del club en 2009.
  * **Equipos y Cuerpo Técnico:** Información sobre las categorías (Eskola, Premini, Infantil A, Infantil B, Junior).
  * **Horarios:** Cuadrante completo de entrenamientos.
  * **Cuotas:** Información sobre las matrículas para la temporada.
  * **Contacto y Mapa:** Formulario de contacto y ubicación interactiva del Frontón Municipal de Alonsotegi.

---

## 🛠️ Tecnologías Utilizadas

* **HTML5** semántico.
* **Tailwind CSS** (vía CDN) para un diseño moderno y ágil.
* **JavaScript Vanilla** para la gestión bilingüe y la interactividad.
* **GitHub Pages** para el alojamiento web estático.

---

## 💡 CÓMO ACTUALIZAR LA WEB CADA TEMPORADA

Solo hay que editar el fichero "temporada.json" (con el Bloc de notas, VS Code, etc.).
No hace falta tocar index.html. Guarda el fichero, súbelo al hosting y recarga la web.

## FORMA FÁCIL: EL EDITOR VISUAL (editor.html)

Abre editor.html en el navegador (misma carpeta que index.html), edita los datos en formularios y pulsa
"Descargar temporada.json". Después sube ese fichero a la carpeta "data" del servidor sustituyendo el anterior.
Si la página no carga el JSON sola (por abrirla con doble clic), usa "Abrir fichero…" y elige temporada.json.
Lo que sigue explica cómo editar el JSON a mano, por si prefieres hacerlo así.

## QUÉ CONTIENE
temporada   -> texto "2026 / 2027" que sale en el subtítulo de Cuotas.
equipos     -> sección Equipos (nombre, categoría, entrenadores, descripción, objetivos).
horarios    -> sección Horarios. También genera el horario que aparece en la ficha de cada equipo.
cuotas      -> tarjetas de precios y el descuento familiar.
documentos  -> tarjetas de descarga (el fichero va en la carpeta "docs").

## TEXTOS EN CASTELLANO Y EUSKERA

Cuando un texto cambia según el idioma se escribe así:   { "es": "Hola", "eu": "Kaixo" }
Si el texto es igual en los dos idiomas (o solo existe en castellano) basta con escribirlo normal:  "Hola"

## TAREAS FRECUENTES

Cambiar un precio ...... busca "precio" dentro de "cuotas" y cambia el valor, p. ej. "75 €".
Cambiar un horario ..... en "horarios", cambia la hora del día. Para quitar un día, borra esa línea
                         (si el día no aparece, la tabla muestra "—").
Añadir un equipo ....... 1) copia un bloque completo de "equipos" y cámbiale el "id" (sin espacios ni tildes,
                         p. ej. "mini") y el resto de datos; 2) añade su línea en "horarios" con el mismo "id"
                         en el campo "equipo".
Quitar un equipo ....... borra su bloque en "equipos" y su línea en "horarios".
Añadir un documento .... sube el fichero a la carpeta "docs", copia un bloque de "documentos" y cambia
                         título, descripción y "archivo" (p. ej. "docs/nuevo.pdf").
Cambiar de temporada ... actualiza "temporada" y revisa precios, horarios y entrenadores.

## REGLAS DEL FORMATO JSON (para que no se rompa)

- Los textos van siempre entre comillas dobles "así".
- Entre un elemento y el siguiente va una coma, pero NO después del último.
- No borres llaves { } ni corchetes [ ].
- Antes de subirlo, pega el contenido en https://jsonlint.com para comprobar que es válido.
- Si algo falla, la web muestra "No se ha podido cargar esta información" en la sección afectada.
