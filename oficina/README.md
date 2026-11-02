# La oficina virtual

Siete agentes de Claude Code, cada uno con su área. Están definidos en `.claude/agents/`.

| Agente | Puesto | Qué le pedís |
|---|---|---|
| `marketing` | Jefe de Marketing | Estrategia, marca, precios, ofertas, lanzamiento |
| `redes` | Community Manager | Calendario de Instagram y Facebook, posts, guiones de Reels |
| `diseno-web` | Diseñador y Desarrollador Web | Logo, flyers, catálogo, página web, tienda, SEO |
| `publicidad` | Media Buyer | Campañas en Meta y Google, anuncios, presupuesto |
| `ventas` | Jefe de Ventas | Mayoristas, prospectos, mails, cotizaciones |
| `atencion-cliente` | Atención al Cliente | WhatsApp, preguntas frecuentes, agente de IA de WhatsApp |
| `importaciones` | Comercio Exterior | Proveedores en China, costos, márgenes, aduana |

**Claude (esta conversación) es el gerente:** recibe tu pedido, lo reparte entre los agentes que correspondan, revisa
lo que entregan y te presenta el resultado.

## Cómo se usa
Le hablás normal a Claude, por ejemplo:
- "Que el equipo arme el lanzamiento de la marca", y participan marketing, diseño-web, redes y publicidad.
- "Pedile a ventas una lista de 30 agronomías de la provincia de Buenos Aires y el mail de presentación."
- "Que importaciones compare estos 3 proveedores" (y les pasás los links).

Cada agente lee primero `.agents/product-marketing.md`, que es la ficha del negocio. Cuanto más completa esté, mejor
trabajan todos.

## Reglas de la oficina
- Nada sale al público (posts, mails, anuncios) sin que Marco o Santino lo aprueben.
- No se gasta plata (anuncios, dominios, compras) sin aprobación explícita.
- Ningún agente inventa datos: lo que falta queda marcado como [PENDIENTE].
- Los temas legales, aduaneros e impositivos se validan con un profesional.

## ¿Y la oficina con personajes pixelados?
Lo que viste en videos es una capa visual opcional: programas que muestran a cada agente como un muñequito trabajando
en una oficina, por ejemplo [Claude-Office](https://github.com/W17ant/Claude-Office) o
[pixel-agents](https://github.com/rolandal/pixel-agents-standalone). Solo dibujan lo que hacen los agentes; el
trabajo real lo hacen los agentes de esta carpeta. Funcionan corriendo Claude Code en una computadora, no desde el
celular. Cuando tengan una PC con Claude Code, se puede instalar.
