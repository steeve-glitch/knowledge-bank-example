# Tu Biblioteca de Conocimiento Personal
### Guía de uso — Claude Desktop / Claude Code

---

## ¿Qué es esto?

Una biblioteca de investigación personal que crece contigo. Cada artículo que lees, cada conferencia a la que asistes, cada capítulo que anotas — lo agregas aquí, y Claude lo lee, lo resume, lo conecta con todo lo demás que tienes guardado, y te ayuda a encontrar las ideas dentro.

Piénsalo como una Wikipedia que construyes tú mismo, sobre los temas que *a ti* te interesan.

---

## Lo que necesitas

- **Claude Desktop** o **Claude Code** instalado en tu computador
- La carpeta de esta biblioteca (te la compartieron por GitHub o en un pendrive)
- **Obsidian** *(opcional pero recomendado)* — una app gratuita para navegar tu biblioteca visualmente, seguir los vínculos entre páginas y ver un mapa de cómo todo se conecta. Descárgala en [obsidian.md](https://obsidian.md). Ábrela apuntando a esta misma carpeta.

---

## Primera vez — configuración

1. Descarga o clona esta carpeta en tu computador
2. Abre **Claude Desktop** o **Claude Code**
3. Apunta Claude a esta carpeta como tu directorio de trabajo
4. Claude leerá automáticamente las instrucciones — no necesitas decirle nada

Eso es todo. Claude sabe qué hacer desde el primer momento.

---

## Cómo agregar una fuente

Hay tres formas:

### Opción A — Pegar texto directamente
Copia el texto de un artículo, una transcripción o tus propias notas. Luego escribe:

> *"Ingresa esto: [pegar el texto]"*

### Opción B — Subir un PDF
Guarda el archivo en la carpeta `raw/` dentro de tu biblioteca. Luego escribe:

> *"Ingresa raw/nombre-del-archivo.pdf"*

### Opción C — Dar un enlace
> *"Ingresa este artículo: https://..."*

---

Claude hará todo lo siguiente solo:
- Te dirá los 3 a 5 puntos más importantes
- Te preguntará si hay algo específico que quieras destacar
- Escribirá una página de resumen
- Creará páginas para los arquitectos, edificios e ideas mencionados
- Actualizará el catálogo de tu biblioteca

---

## Cómo hacer preguntas

Simplemente pregunta con tus propias palabras. Ejemplos:

- *"¿Qué dijo Zaha Hadid sobre la relación entre software y forma?"*
- *"Compara el brutalismo y el diseño paramétrico"*
- *"Resume todo lo que sé sobre Tadao Ando"*
- *"¿Qué materiales aparecen con más frecuencia en los proyectos que he estudiado?"*
- *"Estoy escribiendo sobre sostenibilidad — ¿qué hay relevante en mi biblioteca?"*

Claude responderá usando solo lo que está en tu biblioteca, citando sus fuentes.

---

## Cómo navegar tu biblioteca

Si tienes Obsidian instalado:

1. Abre Obsidian → **Abrir carpeta como vault** → selecciona esta carpeta
2. Haz clic en cualquier página de la carpeta `wiki/` para abrirla
3. Haz clic en cualquier `[[término vinculado]]` para ir a esa página
4. Abre la **Vista de grafo** (ícono en la barra lateral) para ver visualmente cómo todo se conecta

También puedes leer los archivos directamente — son texto plano, legibles en cualquier editor.

---

## Cómo revisar la salud de tu biblioteca

De vez en cuando escribe:

> *"lint"* o *"revisión de salud"*

Claude escaneará todas tus páginas y te dirá:
- Páginas huérfanas (a las que nada apunta)
- Personas o conceptos mencionados en el texto pero sin vínculo
- Contradicciones entre fuentes
- Vacíos que vale la pena llenar — preguntas que tu biblioteca todavía no puede responder

---

## Consejos para arquitectos

**Buenas fuentes para agregar:**
- Artículos de revistas (Dezeen, Architectural Review, ARQ, entrevistas de El Croquis)
- Capítulos de libros o ensayos (Venturi, Koolhaas, Frampton, Zumthor)
- Transcripciones de conferencias o tus notas de clases
- Bases de concursos o programas de proyectos que hayas estudiado
- Tus propias notas de visitas a obras *(ver ejemplo abajo)*
- Críticas o reseñas de edificios

**Un hábito que marca la diferencia:**
Después de cualquier conferencia, charla o visita a obra — aunque sean solo 5 minutos de notas — agrégalas como fuente. La biblioteca se compone: una nota es nada, cincuenta notas es un activo de investigación.

**Ejemplo de nota de visita a obra:**

> *"Ingresa esto: Visité el Therme Vals de Peter Zumthor hoy. Lo más llamativo fue la forma en que la luz entra por las grietas entre los bloques de gneis — crea una sensación de tiempo geológico, como si el edificio hubiera emergido de la roca. El agua y la piedra son el mismo material en distinto estado. La circulación es confusa a propósito: no hay un recorrido claro, te pierdes. Zumthor llama a esto 'arquitectura silenciosa'. Temperatura del agua: tibia en el interior, fría en la piscina exterior."*

---

## El ejemplo incluido

La carpeta `wiki/` ya contiene un ejemplo completo — un perfil de **Zaha Hadid** ya ingresado. Te muestra:

- `wiki/sources/` — cómo se ve una página de fuente
- `wiki/entities/` — cómo se ve una página de persona o firma
- `wiki/concepts/` — cómo se ve una página de concepto

Lee estos archivos antes de empezar a agregar tu propio contenido para entender el formato.

---

## Referencia rápida

| Qué quieres hacer | Qué escribirle a Claude |
|-------------------|------------------------|
| Agregar una fuente | *"Ingresa esto: [texto / URL / nombre de archivo]"* |
| Hacer una pregunta | Simplemente pregunta |
| Ver un resumen de una persona o edificio | *"¿Qué sé sobre [nombre]?"* |
| Comparar dos cosas | *"Compara [X] e [Y]"* |
| Encontrar conexiones | *"¿Qué conecta [X] e [Y] en mi biblioteca?"* |
| Revisar la salud de la biblioteca | *"lint"* |
| Guardar una buena respuesta | *"Guarda esto como página de síntesis"* |
