# Plan maestro: empresa de alambrado eléctrico rural

Importación desde China de hilo electroplástico, soga eléctrica, varillas y aisladores, con venta en Argentina.
Este plan ordena todo lo que vamos a armar juntos (vos, tu papá y Claude).

---

## Fase 0: bases del negocio (antes de mostrar nada)

### 0.1 Importación (checklist para validar con un profesional)
- [ ] Inscribirse como importador ante ARCA (ex AFIP) o trabajar con un importador que ya esté habilitado.
- [ ] Conseguir un **despachante de aduana**: define la posición arancelaria de cada producto, los derechos, la tasa de
      estadística, el IVA y las percepciones, y si hace falta alguna certificación o licencia.
- [ ] Consultar si los productos eléctricos necesitan **certificación de seguridad eléctrica**. Lo más probable es que
      el hilo, la soga, las varillas y los aisladores no la necesiten, pero los **energizadores (boyeros)** casi seguro
      que sí.
- [ ] Pedir **muestras** a 2 o 3 proveedores (Alibaba o Made-in-China) y probarlas en el campo: resistencia, conducción
      y rayos UV.
- [ ] Calcular el **costo puesto en depósito** por unidad (FOB + flete + seguro + impuestos + despachante + flete
      interno). Con ese número se fijan los precios.
- [ ] Definir el modelo de venta: minorista al productor, mayorista a agronomías o ambos.

> Claude puede armar la planilla de costos de importación (skill `xlsx`), comparar proveedores y redactar los mensajes
> en inglés para negociar con los fabricantes chinos.

### 0.2 Marca
- [ ] Nombre. Claude propone opciones y verificamos que el dominio `.com.ar` y el usuario de Instagram estén libres
      (con el conector de Shopify se pueden chequear dominios).
- [ ] Logo, colores y tipografía. Se diseñan con Canva (conectado) y la skill `canvas-design`.
- [ ] Voz de marca y propuesta de valor. Se completan en `.agents/product-marketing.md` con la skill `product-marketing`.
- [ ] Fichas técnicas de cada producto (PDF) para revendedores, con la skill `pdf` o `sales-enablement`.

---

## Fase 1: canales

### 1.1 WhatsApp Business: canal principal de venta
**Etapa A (ya):** WhatsApp Business App gratis en un celular dedicado, con catálogo, respuestas rápidas, mensaje de
bienvenida y etiquetas (consulta, presupuesto, vendido). Claude escribe todos los textos.

**Etapa B: agente de IA** (como en el video 1):
1. Plan y arquitectura en Claude Code.
2. App en **Meta for Developers** con WhatsApp Cloud API, credenciales y webhook.
3. Modelo de IA vía OpenRouter o la API de Claude.
4. Memoria de la conversación.
5. "Ficha del negocio": productos, medidas, precios, envíos, cómo armar un cerco, preguntas frecuentes.
6. Herramientas: cotizar un pedido (metros de hilo, cantidad de varillas y aisladores según los metros de cerco),
   anotar el pedido en una planilla de Google y avisarles a ustedes.
7. Pruebas con casos raros.
8. Deploy en un VPS.

> Alternativa sin código: el conector **MyChatBot** (agente de ventas de IA con canales de Instagram y otros).

### 1.2 Instagram y Facebook
- [ ] Crear la cuenta de **Instagram profesional** y la **página de Facebook**, vincularlas en Meta Business Suite y
      conectar WhatsApp.
- [ ] Bio, destacadas (Productos, Cómo se arma, Envíos, Clientes) y links.
- [ ] Calendario de contenido mensual con la skill `social`. Pilares:
  1. **Producto en el campo** (Reels de instalación, potreros armados).
  2. **Educación** ("cuántas varillas necesito por hectárea", "hilo vs. soga", errores comunes del eléctrico).
  3. **Confianza** (llegada del contenedor, depósito, padre e hijo, clientes reales).
  4. **Oferta** (combos de kit potrero, precios por bulto, envíos).
- [ ] Publicación: vidIQ (conectado) publica Reels en Instagram. Para programar todo (posts, carruseles, historias,
      Facebook) conviene el conector **Metricool**.
- [ ] Grupos de Facebook rurales y ganaderos de la zona (ahí está el público).

### 1.3 Página web
Dos caminos:
- **Shopify (conectado):** tienda con carrito y cobro (Mercado Pago). Es lo más rápido para vender online.
- **Web propia** (HTML/Next.js con `taste-skill` y `frontend-design`): catálogo con botón "Pedir por WhatsApp" y una
  calculadora de materiales. Barata de mantener.

Páginas mínimas: Inicio, Productos (una por cada uno), Calculadora de cerco, Cómo armar un cerco eléctrico, Envíos,
Mayoristas/Revendedores, Contacto. SEO local con las skills `seo-audit`, `schema` y `site-architecture`.

### 1.4 Mercado Libre (recomendado evaluarlo)
En Argentina gran parte de la búsqueda de "hilo electroplástico" o "varillas para boyero" pasa por Mercado Libre.
Publicar ahí da ventas desde el día uno mientras crecen los canales propios.

---

## Fase 2: contenido y publicidad

### Videos
- **Remotion** (`remotion-best-practices`): videos animados con la marca, como "Cómo armar un potrero en 30 min",
  comparativas o promociones, con el método del video 2 (idea → prompt completo → Claude Code).
- **Videos reales del campo** grabados con el celular. Claude escribe los guiones con gancho, pasos y cierre (skills
  `social` y `video`) y, con vidIQ, genera subtítulos, clips y música.
- Canva para editar placas, flyers y carruseles.

### Publicidad (Meta Ads)
- Skills `ads` y `ad-creative`: estrategia, públicos (productores ganaderos por zona, intereses en ganadería) y
  variantes de anuncios.
- El objetivo inicial son **mensajes a WhatsApp** (campañas "Click to WhatsApp"), con presupuesto chico, testeando
  creativos.
- Conector sugerido: **Adspirer** (Meta Ads desde Claude: crear campañas en pausa, ver métricas).

### Ventas B2B a revendedores
- Lista de agronomías, forrajerías y veterinarias rurales por zona (skill `prospecting`; Mailerfind, del video 1, saca
  negocios de Google Maps).
- Mail y WhatsApp de presentación con catálogo mayorista (skills `cold-email` y `sales-enablement`), con Gmail
  (conectado) para borradores y envíos.

---

## Fase 3: operación
- Planilla de stock, pedidos y clientes en Google Drive (conectado).
- Agenda de entregas y llamados en Google Calendar (conectado).
- Métricas mensuales: consultas por WhatsApp, ventas por canal, costo por mensaje de los anuncios (skill `analytics`).

---

## Herramientas instaladas y conectadas

| Para qué | Herramienta | Estado |
|---|---|---|
| Diseños, flyers, posts | Canva | Conectado |
| Tienda online y dominios | Shopify | Conectado |
| Publicar Reels, subtítulos, clips, guiones | vidIQ | Conectado |
| Mails a revendedores | Gmail | Conectado |
| Planillas y archivos | Google Drive | Conectado |
| Agenda | Google Calendar | Conectado |
| Videos animados con código | Skill Remotion | Instalada |
| Web con diseño profesional | taste-skill, frontend-design, web-design-guidelines, playwright-cli | Instaladas |
| Marketing, redes, anuncios, copy, SEO, ventas | 26 skills de marketing (`.claude/skills/`) | Instaladas |
| Programar posts en IG/FB | Metricool | **Sugerido: conectar** |
| Meta Ads (Facebook e Instagram) | Adspirer | **Sugerido: conectar** |
| Agente de ventas IA sin código | MyChatBot | **Opcional** |
| WhatsApp con IA a medida | Meta Cloud API + agente propio | **A construir (fase 1.1 B)** |

## Lo que necesitamos de ustedes
1. Nombre tentativo (o pedimos opciones).
2. Zona base y hasta dónde envían.
3. Si venden al por menor, al por mayor o ambos.
4. Fotos y especificaciones de los productos (o los links de los proveedores).
5. Un número de celular para el WhatsApp del negocio.
