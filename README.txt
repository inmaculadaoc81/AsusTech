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
