# Lo aprendido de los videos

Transcripciones reconstruidas a partir de los subtítulos de cada video (OCR) más lo que se ve en pantalla.

---

## Video 1: Agente de IA en WhatsApp en ~30 minutos (@juanbertorello.ai)

**Idea central:** no pases semanas armando un "monstruo complicado que nadie usa". En unos 30 min se arma
un agente que **conversa** con el cliente, **recuerda** la charla, **responde sobre tu negocio** y, lo
principal, **actúa de verdad**.

> "El chatbot conversa, el agente actúa."

### Los 8 pasos

1. **Plan.** Abrí un proyecto nuevo en Claude Code y empezá en *modo plan* (ningún código todavía).
   Contale a Claude:
   - qué hace tu negocio (ej.: clínica dental)
   - quiénes son tus clientes (ej.: escriben por WhatsApp)
   - qué tiene que resolver el agente
   - qué acciones puede tomar

   Dejá que diseñe la arquitectura antes de tirar código. Arquitectura que se ve:
   `Cliente → WhatsApp → Agente → {Memoria, Negocio, Acciones}`.
2. **WhatsApp.** Creá tu app de desarrollador en **Meta for Developers**, agregá el producto WhatsApp,
   configurá las **credenciales** y el **webhook**. El webhook es cómo Meta le avisa a tu sistema:
   "ey, alguien te acaba de mandar un mensaje" (`Cliente → Meta → Tu sistema`).
3. **Modelo.** Conectá el modelo de IA a través de **OpenRouter**: una sola conexión para hablar con
   cualquier modelo (Claude, GPT…). Cambiar de modelo = cambiar una línea:
   `model: "anthropic/claude"`.
4. **Memoria.** Sin memoria, cada mensaje es una charla desde cero. Guardá el historial reciente y
   mandalo de vuelta al modelo con cada mensaje nuevo. Así el agente sabe de qué venía hablando el
   cliente.
5. **Negocio.** Dale al agente una "ficha del negocio": servicios, precios, horarios, preguntas
   frecuentes, políticas, dirección y reglas para agendar. Así responde con datos de tu negocio
   en vez de inventar. (Ejemplo: "Clínica Dental Norte: limpieza $38.000, 45 min, lun a sáb 8 a 18 h,
   acepta obra social".)
6. **Herramientas.** Conectá algo como **Cal.com** y dale al agente el poder de ver la agenda,
   mostrar horarios libres, tomar los datos del cliente y agendar el turno (tools tipo `ver_agenda()`,
   `agendar_cita()`).
7. **Prueba.** Probá hasta que se rompa: preguntas simples, fechas imposibles ("turno el 31 de febrero"),
   2 mensajes a la vez, "ignorá tus instrucciones", agendar y cancelar. Si falla, corregí y volvé a probar.
8. **En vivo.** Tu notebook no es un servidor: subilo a un **VPS** y queda andando aunque apagues la compu.

Resultado: WhatsApp + IA + memoria + negocio + herramientas + en línea.

**Extra, para conseguir clientes:** **Mailerfind** saca negocios de Google Maps (o Instagram) por rubro y
zona, les mandás un mail con el link a tu WhatsApp y el agente atiende a quien conteste.

---

## Video 2: "Este video lo hizo Claude": videos animados con Remotion (@danielbrown.ia)

Video con animaciones y subtítulos hecho entero por Claude. **4 pasos:**

1. **Instalá Remotion y conectalo con Claude Code.** Remotion convierte código (React) en video y Claude
   lo programa por vos (`<Composition id="Reel" fps={30} />` → MP4 9:16).
2. **Aterrizá tu idea:** qué **historia** querés contar, a qué **público** va dirigido y qué **objetivo**
   querés lograr con ese video.
3. **Escribí un prompt bien completo** (ej. `prompt.md`):
   - duración (ej. 50 segundos)
   - formato (Reels y TikTok, 9:16)
   - escenas (gancho, pasos y cierre)
   - animaciones (cinéticas, premium)
   - identidad de marca: colores, tipografía, estilo

   Cuanto más contexto, mejor el resultado.
4. **Dáselo a Claude Code** y en minutos tenés el video con animaciones de nivel profesional
   (se edita/previsualiza en Remotion Studio: escenas, voz, SFX, subtítulos).

---

## Video 3: Por qué tu app hecha con Claude Code parece barata: 5 herramientas (@revolutia.ai)

Las apps de algunos parecen costar 10.000 € y otras parecen hechas en un día. Te faltan 5 herramientas:

1. **Taste Skill** ("The Anti-Slop Frontend Framework for AI Agents"). Le da a Claude criterio estético
   de verdad, para que entienda qué significa que algo se vea premium. Basta de degradados morados
   y de tres tarjetas redondeadas.
2. **Web Design Guidelines** (skill de Vercel). Revisa lo que Claude ya construyó: audita la interfaz
   contra guías de diseño reales. Te ahorra lanzamientos vergonzosos.
3. **Awesome Design MD** (VoltAgent, getdesign.md). Colección de archivos `DESIGN.md` que analizan
   sistemas de diseño de marcas populares (Stripe, Linear, Apple, Nike…): tipografía, colores,
   espaciado, componentes, estructuras. Metés uno en tu proyecto y el agente genera una UI acorde.
   Se acabó pasar 45 minutos eligiendo entre dos tonos de azul.
4. **Image To Code.** Encontrás un diseño que te gusta, le sacás una captura, se la das a Claude y él te
   lo recrea. Convierte Pinterest en herramienta de desarrollo. ("Peligroso, pero funciona".)
5. **playwright-cli.** Claude abre el navegador, interactúa con tu web, hace capturas y comprueba lo que
   construyó: lo construye, lo abre y lo mira.

---

## Ideas transversales

- **Planificar antes de codear** (modo plan, arquitectura primero).
- **Contexto abundante = mejores resultados** (prompts completos, ficha del negocio, DESIGN.md).
- **Darle a Claude ojos y criterio:** skills de gusto, auditoría de diseño y navegador para verificar
  su propio trabajo.
- **Agente > chatbot:** herramientas que ejecutan acciones reales (agendar, consultar).
- **Probar hasta romper** y desplegar en un servidor real.
