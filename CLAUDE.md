# CLAUDE.md

Repositorio de conocimiento y herramientas del usuario (habla español rioplatense; responder en español).

## Conocimiento aprendido
- `conocimiento/videos-aprendidos.md`: resumen detallado de los videos que el usuario compartió
  (agente de WhatsApp con IA, videos con Remotion, 5 herramientas de diseño). Leerlo cuando la tarea
  toque esos temas.

## Skills instaladas (`.claude/skills/`)
- `taste-skill` (Leonxlnx/taste-skill): dirección de arte anti-"slop" para landing pages y pantallas
  de apps. Usar al diseñar o pulir cualquier frontend.
- `web-design-guidelines` (vercel-labs/agent-skills): auditar UI contra las Web Interface Guidelines.
- `remotion-best-practices` (remotion-dev/skills): router de todas las skills de Remotion para crear
  videos con código.
- `playwright-cli` (microsoft/playwright-cli): controlar el navegador para revisar visualmente lo que
  se construye (`npm install -g @playwright/cli@latest`).

## Referencias de diseño
- `design-references/awesome-design-md/<marca>/DESIGN.md`: 84 sistemas de diseño de marcas
  (VoltAgent/awesome-design-md). Copiar el que corresponda al proyecto para guiar la UI.
- Image To Code: no hace falta herramienta extra; Claude recrea diseños a partir de capturas.

## Forma de trabajar (lecciones de los videos)
1. Planificar primero (arquitectura antes de código).
2. Pedir/armar contexto completo: objetivo, público, marca, datos del negocio.
3. Diseño: elegir dirección con taste-skill o un DESIGN.md → construir → abrir con playwright y mirar
   capturas → auditar con web-design-guidelines → corregir.
4. Agentes: memoria + datos del negocio + herramientas reales; probar casos raros; desplegar en VPS.
