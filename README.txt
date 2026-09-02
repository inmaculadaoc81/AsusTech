ASUSTECH / EASY-TECH ONE PAGE
Dominio: https://easy-tech.es/
Teléfono caja y botones: +34 918 29 46 56
Diagnóstico: gratuito.
Logo e isotipo: suministrados por el usuario.
Incluye: WhatsApp, recogida, atención telefónica, Google Business, YouTube, Cal.com, formulario SMTP, chatbot n8n, mapa, SEO y sección de datos.
Variables SMTP en Vercel: SMTP_HOST, SMTP_PORT=465, SMTP_SECURE=true, SMTP_USER, SMTP_PASS, CONTACT_EMAIL.
El correo SMTP no aparece visible en la web.
Google Analytics:
G-0T80GRPC03

REVISIÓN (fixes aplicados en esta pasada):
- BUG REAL — sin menú móvil: .links se ocultaba a partir de 900px
  (display:none) sin ningún botón ni menú alternativo, así que la
  navegación desaparecía por completo en móvil. Añadido botón
  .menu-btn + desplegable #mobileMenu con todos los enlaces.
- Google Analytics: no existía. Añadido G-0T80GRPC03.
- Meta tags og:* y robots: no existían. Añadidos.
- Schema.org: faltaban areaServed y sameAs (Maps/YouTube) — añadidos.
- Banner de cookies: no existía. Añadido (Aceptar / Rechazar /
  Política de privacidad → https://kelatos.com/privacy-policy/), con
  diseño apilado a ancho completo en móvil.
- Sección SEO: no existía. Añadida sección "Guía" (id="guia", enlazada
  en el menú de escritorio y móvil) con contenido propio sobre averías
  habituales en equipos Asus (incluida la gama gaming ROG/TUF).
- Borde blanco del botón del chat: faltaba tanto en la regla CSS como
  en el script de reposicionamiento JS. Añadido en ambos sitios.
- .calltop: el texto largo ("Atención Telefónica 24 horas 365 días")
  deformaba la píldora del menú. Acortado a solo el número (mismo
  número, +34 918 29 46 56) y añadido white-space:nowrap como
  salvaguarda. El botón grande .btn.phone del hero conserva su texto
  completo.
- H1 de portada reescrito, corto, directo y totalmente afirmativo (sin
  interrogación ni condicionales), incluye la marca: "Tu Asus no
  funciona. Lo revisamos y te damos soluciones." Tamaño del H1
  aumentado: clamp(38-56px) → clamp(46-74px) en escritorio, 39px →
  48px en móvil.

REVISIÓN ADICIONAL — 3 BUGS REALES (a petición del cliente):
- Logo demasiado grande en móvil: .logo solo tenía height:48px fijo,
  sin límite de ancho ni reducción específica en móvil. Añadido
  max-width:220px en general y, en el breakpoint ≤600px, reducido a
  height:34px;max-width:160px (además de bajar la altura del header
  de 80px a 66px en ese breakpoint).
- El panel #mobileMenu no usaba ningún estilo real (mismo bug
  encontrado en LenovoTech): era un div con solo padding/background
  inline, sin bloques por enlace, así que al abrirlo los enlaces
  aparecían como texto plano separado por "·". Reescrito con la clase
  .mobile-menu estándar de la familia.
- El botón flotante de WhatsApp (.float-wa) mostraba el texto "WA" en
  vez del icono SVG estándar de WhatsApp usado en el resto de la
  familia. Sustituido por el SVG correcto.

REVISIÓN ADICIONAL (checklist unificado de la familia, a petición del cliente):
- H1 repetía la plantilla "no funciona. Lo revisamos..." usada en
  varios repos. Reescrito: "Tu Asus se cuelga o no enciende. Aquí lo
  arreglamos." (10 palabras).
- BUG REAL — texto decorativo ".art:before" ("TUS DATOS", 80px) en la
  sección de protección de datos no tenía reducción de tamaño en
  móvil/tablet, mismo problema visto en MedionTech ("HARDWARE").
  Añadida reducción (60px tablet, 42px móvil).
- BUG REAL — el formulario no tenía ninguna casilla de consentimiento
  de política de privacidad (solo existía el enlace en el banner de
  cookies, no ligado al formulario). Añadida, con enlace a
  https://kelatos.com/privacy-policy/ en azul y subrayado.
- Añadido "Sábados, domingos y días festivos estamos cerrados" debajo
  del horario.
- Añadida franja de aviso de servicio técnico independiente debajo
  del menú (no existía).
- Ninguno de los botones CTA del hero (WhatsApp ni teléfono) tenía
  icono. Añadidos ambos (SVG estándar de la familia).
- Formulario verificado: fetch a /api/contacto coincide con
  api/contacto.js; conexión correcta.

REVISIÓN ADICIONAL (checklist unificado de la familia + nueva regla de menú móvil, a petición del cliente):
- Este repo no había pasado por ninguna de las rondas anteriores del
  checklist de la familia; se aplicaron todos los puntos pendientes
  de una vez.
- BUG REAL — enlace de Cal.com desactualizado. Actualizado a
  https://cal.com/kelatos/30min?embed=true&theme=light&attendeePhoneNumber=%2B34&overlayCalendar=true.
- Verificado: el correo soporte@kelatos.com no aparece visible.
- BUG REAL — el mensaje prellenado de WhatsApp decía "¡Hola Kelatos!".
  Corregido a "¡Hola Asustech!".
- BUG REAL — el menú móvil (#mobileMenu, estilo atributo hidden) no
  tenía ningún listener que lo cerrara al pulsar un enlace. Añadido el
  script estándar de la familia.
- Verificado: sin iconos ni imágenes con proporciones fijas
  incorrectas.
- Verificado: el H1 en móvil ya está en 48px.
- BUG REAL — botones del hero (.btn) con border-radius de 15px y sin
  estado hover. Aumentado a border-radius:999px; añadido
  filter:brightness(.88) en wa/pickup (colores sólidos) y relleno
  sólido con var(--b2) + texto blanco en el botón de teléfono (estilo
  contorno) al pasar el ratón.
- BUG REAL — la franja de aviso de independencia estaba dentro de
  <header>, y el menú móvil desplegable se solapaba con ella al
  abrirse (mismo bug de diseño detectado en AcerTech/KitchenAid).
  Movida fuera de <header>, como hermana justo después de él y antes
  del hero: sigue siendo la misma franja amarilla de ancho completo.
- Verificado: el header (element selector "header{position:sticky;
  top:0}") ya se mantenía fijo/pegado arriba al hacer scroll; no
  requería cambios.
- Verificado: este repo no usa el patrón de franja de insignias bajo
  el H1 (familia Dyson); no aplica la reubicación.
