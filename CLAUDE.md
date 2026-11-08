# CLAUDE.md

Repositorio de conocimiento y herramientas del usuario (habla español rioplatense; responder en español).

## ⏸️ Estado actual (8/11/2026): EN PAUSA
El producto todavía puede cambiar (el alambrado eléctrico no es definitivo). Hasta que Santino diga lo contrario:
no crear logos, contenido, webs, campañas ni otros entregables. Solo responder consultas y ayudar con la
configuración. Cuando se defina el producto, actualizar `.agents/product-marketing.md` y el plan antes de producir.

## Proyecto principal: empresa de alambrado eléctrico rural
- El usuario y su papá importan de China hilo electroplástico, soga eléctrica, varillas y aisladores
  para vender en Argentina. Claude arma marca, WhatsApp, Instagram, web, contenido y publicidad.
- `plan/plan-maestro.md`: plan por fases con checklist. Actualizarlo a medida que se avanza.
- `.agents/product-marketing.md`: contexto del negocio que leen todas las skills de marketing.
  Completar los campos [PENDIENTE] cuando el usuario dé los datos.
- Skills de marketing instaladas (coreyhaines31/marketingskills): ads, ad-creative, social, video,
  copywriting, copy-editing, image, marketing-plan, marketing-ideas, marketing-psychology, offers,
  pricing, product-marketing, customer-research, competitors, content-strategy, emails, cold-email,
  prospecting, sales-enablement, launch, seo-audit, site-architecture, schema, cro, analytics.
  Además, de anthropics/skills: frontend-design y canvas-design.
- Conectores en uso: Canva, Shopify, vidIQ (publica Reels en IG), Gmail, Drive, Calendar.

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

## Oficina virtual (`.claude/agents/`)
Claude actúa como gerente y delega en 7 agentes: marketing, redes, diseno-web, publicidad, ventas,
atencion-cliente e importaciones (ver `oficina/README.md`). Para pedidos que tocan varias áreas,
repartir el trabajo entre los agentes y presentar el resultado unificado. Nada se publica, se envía
ni se paga sin aprobación de Marco o Santino.
