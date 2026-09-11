# PoliglotIA

Traduce un PDF y conviértelo en una presentación locutada, en una sola página web.

**App:** https://fborrasumh.github.io/poliglotia/

PoliglotIA lee materiales en PDF con texto, fotos y gráficos, los traduce a las 24 lenguas oficiales de la Unión Europea y a catalán, euskera y gallego, rehace el PDF en cada idioma y genera una presentación locutada que se exporta como vídeo, PowerPoint o paquete para ffmpeg.

## Los cinco pasos

1. **Leer el PDF.** Extrae el texto por bloques respetando las columnas, recorta imágenes y gráficos vectoriales, detecta pies de figura y páginas escaneadas. Con IA ordena el texto, transcribe lo escaneado y clasifica y describe cada figura, extrayendo los datos de los gráficos legibles.
2. **Traducir.** Glosario común, traducción por lotes, comprobaciones automáticas (cifras, longitud, texto sin traducir) y revisión por retrotraducción, obligatoria en irlandés, maltés y euskera. Todo es editable.
3. **Rehacer el PDF.** Formato reorganizado en A4 o fiel al original, con los gráficos redibujados con etiquetas traducidas y la fuente Noto Sans, que cubre las 27 lenguas.
4. **Guion y locución.** Guion maestro editable con las figuras del catálogo, traducción del guion, locución con Azure AI Speech, subtítulos .srt y reproductor.
5. **Vídeo y PowerPoint.** Vídeo MP4 o WebM codificado en el navegador, PowerPoint con texto editable, gráficos nativos, notas y audio, y paquete con imágenes, audio y scripts para montar el MP4 con ffmpeg.

## Requisitos

- Una clave de la API de **OpenAI**. La app lista los modelos de tu cuenta y te deja elegir uno para cada paso.
- Una clave de **Azure AI Speech** para la locución. El plan gratuito (F0) incluye 500.000 caracteres al mes de voz neuronal.
- Un navegador actual. Para codificar el vídeo, Chrome, Edge o Safari de escritorio.

## Privacidad

La app es un único archivo HTML sin servidor propio. Las claves y el trabajo se guardan solo en tu navegador (localStorage e IndexedDB). El contenido del PDF se envía a OpenAI para analizarlo, traducirlo y escribir el guion, y el texto de la narración a Azure para locutarlo, según las condiciones de cada servicio.

## Aviso

Las traducciones y los guiones son automáticos. Revísalos antes de difundirlos, sobre todo en las lenguas con menos recursos. Los PDF generados pueden llevar en el pie la indicación de traducción automática.

## English

PoliglotIA is a single-file web app that reads a PDF with text, photos and charts, translates it into the 24 official EU languages plus Catalan, Basque and Galician, rebuilds the PDF in each language, and turns it into a narrated presentation exported as video, PowerPoint or an ffmpeg package. It requires an OpenAI API key and an Azure AI Speech key; keys and work stay in the browser. Translations are machine-generated and should be reviewed before publication.

## Autor

Fernando Borrás Rocher, Universidad Miguel Hernández de Elche. ORCID: [0000-0002-5519-4573](https://orcid.org/0000-0002-5519-4573)

## Licencia

MIT
