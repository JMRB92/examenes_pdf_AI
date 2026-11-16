EXAMEN IA v1.01

1. Abre index.html en el navegador con conexión a Internet, o publícalo en GitHub Pages.
2. Completa identificación, adjunta varios PDF con texto seleccionable, elige preguntas y duración.
3. Gemini genera preguntas en bloques a través de Cloudflare Worker.
4. Realiza el examen y descarga el PDF de resultados.

Worker: https://examen-ia-api.jmramirezb03.workers.dev/generate
Variable ALLOWED_ORIGINS: https://jmrb92.github.io

AVISOS IMPORTANTES:
- El uso gratuito está sujeto a límites de Google Gemini y Cloudflare.
- La generación de 200 preguntas puede tardar bastante o agotar la cuota; la app no inicia exámenes incompletos.
- No incluye OCR de PDF escaneados.
- Las preguntas generadas por IA pueden contener errores y deben ser revisadas en contextos evaluativos.
- Los datos del examen se almacenan localmente en el navegador, sin sincronización.
- El control de cambio de pestaña es orientativo y no impide trampas.
- El Worker público actual no tiene autenticación ni limitación de solicitudes robusta: antes de abrirlo a alumnos, configurar Turnstile o autenticación y rate limiting en Cloudflare.
- La clave API nunca debe introducirse en el HTML público.
- La generación envía el texto de los PDF a Google Gemini, no los datos identificativos del alumno.
- El PDF se genera localmente con jsPDF.
- El código utiliza CDN para pdf.js y jsPDF, por lo que requiere conexión a Internet.
