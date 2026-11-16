
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>WebsCreatorsSpain | Páginas web y automatizaciones para pymes</title>
  <meta name="description" content="Creamos páginas web a medida de tu negocio y automatizamos tareas para que ganes clientes y tiempo.">
  <link rel="icon" href="data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'><rect width='100' height='100' rx='22' fill='%230B2545'/><path d='M22 30l14 40 14-28 14 28 14-40' stroke='white' stroke-width='9' fill='none' stroke-linecap='round' stroke-linejoin='round'/></svg>">

  <!-- Tipografía: Manrope (sans-serif limpia) -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Manrope:wght@400;500;600;700;800&display=swap" rel="stylesheet">

  <!-- Oculta solo el aviso "no usar en producción" del CDN de Tailwind; el resto de mensajes se mantienen -->
  <script>
    (function () {
      const warn = console.warn;
      console.warn = function (...args) {
        if (typeof args[0] === 'string' && args[0].includes('cdn.tailwindcss.com')) return;
        warn.apply(console, args);
      };
    })();
  </script>

  <!-- Tailwind CSS (CDN). Para producción puedes compilarlo con la CLI de Tailwind -->
  <script src="https://cdn.tailwindcss.com/3.4.17"></script>
  <script>
    /* Paleta: blanco + azul marino. "sky" es un azul claro solo para detalles suaves */
    tailwind.config = {
      theme: {
        extend: {
          fontFamily: { sans: ['Manrope', 'system-ui', 'sans-serif'] },
          colors: {
            navy: { 900: '#0B2545', 700: '#13315C', 600: '#1D4478', 50: '#EEF3FA' },
            sky: { 200: '#C9DAF2' }
          }
        }
      }
    };
  </script>

  <style>
    html { scroll-behavior: smooth; scroll-padding-top: 80px; }
    /* Animación única de carga: el "sitio" del hero se dibuja al entrar */
    @keyframes draw { from { transform: scaleX(0); } to { transform: scaleX(1); } }
    .bar { transform-origin: left; animation: draw .9s ease-out both; }
    .bar:nth-child(2) { animation-delay: .15s; } .bar:nth-child(3) { animation-delay: .3s; }
    .bar:nth-child(4) { animation-delay: .45s; }
    /* FAQ: giro del icono al abrir */
    details[open] .chev { transform: rotate(180deg); }
    details summary::-webkit-details-marker { display: none; }
    @media (prefers-reduced-motion: reduce) {
      html { scroll-behavior: auto; } .bar { animation: none; }
    }
  </style>
</head>

<body class="font-sans text-slate-700 bg-white antialiased">

  <!-- ========== CABECERA / NAVEGACIÓN ========== -->
  <header class="sticky top-0 z-50 bg-white/90 backdrop-blur border-b border-slate-200">
    <nav class="max-w-6xl mx-auto flex items-center justify-between px-5 h-16" aria-label="Principal">
      <a href="#inicio" class="flex items-center gap-2 font-extrabold text-xl text-navy-900">
        <svg width="28" height="28" viewBox="0 0 100 100" aria-hidden="true"><rect width="100" height="100" rx="22" fill="#0B2545"/><path d="M22 30l14 40 14-28 14 28 14-40" stroke="#fff" stroke-width="9" fill="none" stroke-linecap="round" stroke-linejoin="round"/></svg>
        WebsCreatorsSpain
      </a>
      <!-- Enlaces de escritorio -->
      <ul class="hidden md:flex items-center gap-8 text-sm font-semibold">
        <li><a class="hover:text-navy-900" href="#nosotros">Nosotros</a></li>
        <li><a class="hover:text-navy-900" href="#servicios">Servicios</a></li>
        <li><a class="hover:text-navy-900" href="#testimonios">Opiniones</a></li>
        <li><a class="hover:text-navy-900" href="#faq">Preguntas</a></li>
        <li><a href="#contacto" class="bg-navy-900 text-white px-4 py-2 rounded-lg hover:bg-navy-700">Pide presupuesto</a></li>
      </ul>
      <!-- Botón menú móvil -->
      <button id="menu-btn" class="md:hidden p-2 rounded-lg text-navy-900 focus:outline-none focus-visible:ring-2 focus-visible:ring-navy-600" aria-label="Abrir menú" aria-expanded="false" aria-controls="menu-movil">
        <svg width="24" height="24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round"><path d="M4 7h16M4 12h16M4 17h16"/></svg>
      </button>
    </nav>
    <!-- Menú móvil -->
    <div id="menu-movil" class="hidden md:hidden border-t border-slate-200 bg-white px-5 py-4">
      <ul class="flex flex-col gap-3 font-semibold">
        <li><a class="block py-1" href="#nosotros">Nosotros</a></li>
        <li><a class="block py-1" href="#servicios">Servicios</a></li>
        <li><a class="block py-1" href="#testimonios">Opiniones</a></li>
        <li><a class="block py-1" href="#faq">Preguntas</a></li>
        <li><a href="#contacto" class="block text-center bg-navy-900 text-white px-4 py-3 rounded-lg">Pide presupuesto</a></li>
      </ul>
    </div>
  </header>

  <main>
    <!-- ========== 1. HERO ========== -->
    <section id="inicio" class="bg-navy-50">
      <div class="max-w-6xl mx-auto px-5 py-16 md:py-24 grid md:grid-cols-2 gap-12 items-center">
        <div>
          <h1 class="text-4xl md:text-5xl font-extrabold text-navy-900 leading-tight">
            Tu negocio merece una web que trabaje por ti
          </h1>
          <p class="mt-5 text-lg max-w-md">
            Diseñamos páginas web a medida de tu pyme y automatizamos las tareas repetitivas, para que te encuentren más clientes y tú pierdas menos tiempo.
          </p>
          <div class="mt-8 flex flex-col sm:flex-row gap-3">
            <!-- CTA principal -->
            <a href="#contacto" class="bg-navy-900 text-white font-bold px-6 py-3.5 rounded-lg text-center hover:bg-navy-700 focus:outline-none focus-visible:ring-2 focus-visible:ring-offset-2 focus-visible:ring-navy-600">Solicita tu presupuesto gratis</a>
            <a href="#servicios" class="border-2 border-navy-900 text-navy-900 font-bold px-6 py-3 rounded-lg text-center hover:bg-white">Ver servicios</a>
          </div>
        </div>

        <!-- Elemento visual: maqueta de una web construida con CSS (sin imágenes externas) -->
        <div class="relative" aria-hidden="true">
          <div class="bg-white rounded-xl shadow-xl border border-sky-200 overflow-hidden">
            <div class="flex items-center gap-1.5 px-4 py-3 bg-navy-900">
              <span class="w-2.5 h-2.5 rounded-full bg-white/40"></span><span class="w-2.5 h-2.5 rounded-full bg-white/40"></span><span class="w-2.5 h-2.5 rounded-full bg-white/40"></span>
              <span class="ml-3 flex-1 h-5 rounded bg-white/15 text-[11px] text-white/80 px-2 leading-5">tunegocio.es</span>
            </div>
            <div class="p-5 space-y-3">
              <div class="bar h-5 w-2/3 rounded bg-navy-900"></div>
              <div class="bar h-3 w-full rounded bg-sky-200"></div>
              <div class="bar h-3 w-5/6 rounded bg-sky-200"></div>
              <div class="bar h-9 w-32 rounded-lg bg-navy-600"></div>
              <div class="grid grid-cols-3 gap-3 pt-3">
                <div class="h-16 rounded-lg bg-navy-50"></div><div class="h-16 rounded-lg bg-navy-50"></div><div class="h-16 rounded-lg bg-navy-50"></div>
              </div>
            </div>
          </div>
          <!-- Tarjeta flotante: automatización -->
          <div class="absolute -bottom-5 -left-3 sm:-left-6 bg-white rounded-lg shadow-lg border border-sky-200 px-4 py-3 flex items-center gap-3">
            <span class="w-9 h-9 rounded-full bg-navy-900 text-white flex items-center justify-center">
              <svg width="18" height="18" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M3 9l4 4 8-8"/></svg>
            </span>
            <span class="text-sm font-bold text-navy-900 leading-tight">Nuevo cliente<br><span class="font-medium text-slate-500">respondido al instante</span></span>
          </div>
        </div>
      </div>
    </section>

    <!-- ========== 2. SOBRE NOSOTROS ========== -->
    <section id="nosotros" class="py-20">
      <div class="max-w-6xl mx-auto px-5 grid md:grid-cols-2 gap-12 items-center">
        <div>
          <h2 class="text-3xl font-extrabold text-navy-900">Somos el equipo digital de tu negocio local</h2>
          <p class="mt-5">En WebNova trabajamos solo con pequeñas y medianas empresas. Entendemos que no necesitas una web genérica: necesitas una que explique bien lo que haces, inspire confianza y te traiga llamadas, reservas o pedidos.</p>
          <p class="mt-4">Hablamos sin tecnicismos, damos plazos claros y nos quedamos contigo después de publicar la web.</p>
        </div>
        <!-- Valores -->
        <ul class="grid sm:grid-cols-2 gap-4">
          <li class="p-5 rounded-xl bg-navy-50"><h3 class="font-bold text-navy-900">A tu medida</h3><p class="mt-1 text-sm">Cada web parte de tu negocio, no de una plantilla.</p></li>
          <li class="p-5 rounded-xl bg-navy-50"><h3 class="font-bold text-navy-900">Precio claro</h3><p class="mt-1 text-sm">Presupuesto cerrado antes de empezar.</p></li>
          <li class="p-5 rounded-xl bg-navy-50"><h3 class="font-bold text-navy-900">Trato directo</h3><p class="mt-1 text-sm">Hablas siempre con la persona que hace tu proyecto.</p></li>
          <li class="p-5 rounded-xl bg-navy-50"><h3 class="font-bold text-navy-900">Soporte continuo</h3><p class="mt-1 text-sm">Cambios, dudas y mejoras cuando lo necesites.</p></li>
        </ul>
      </div>
    </section>

    <!-- ========== 3. SERVICIOS ========== -->
    <section id="servicios" class="py-20 bg-navy-900 text-white">
      <div class="max-w-6xl mx-auto px-5">
        <h2 class="text-3xl font-extrabold max-w-xl">Lo que hacemos para que tu negocio crezca</h2>
        <div class="mt-10 grid md:grid-cols-3 gap-6">
          <article class="rounded-xl bg-white text-slate-700 p-6">
            <svg class="text-navy-900" width="32" height="32" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true"><rect x="3" y="5" width="26" height="18" rx="2"/><path d="M11 28h10M16 23v5"/></svg>
            <h3 class="mt-4 text-xl font-bold text-navy-900">Páginas web a medida</h3>
            <p class="mt-2 text-sm">Webs rápidas, claras y adaptadas a móvil, con tu imagen y tus textos. Pensadas para que te encuentren en Google.</p>
          </article>
          <article class="rounded-xl bg-white text-slate-700 p-6">
            <svg class="text-navy-900" width="32" height="32" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true"><path d="M16 4v6M16 22v6M4 16h6M22 16h6M8 8l4 4M20 20l4 4M24 8l-4 4M12 20l-4 4"/></svg>
            <h3 class="mt-4 text-xl font-bold text-navy-900">Automatizaciones</h3>
            <p class="mt-2 text-sm">Respuestas automáticas, avisos de nuevos contactos, facturas y recordatorios a clientes sin tareas manuales.</p>
          </article>
          <article class="rounded-xl bg-white text-slate-700 p-6">
            <svg class="text-navy-900" width="32" height="32" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true"><path d="M5 26V14M13 26V8M21 26V17M29 26V4"/></svg>
            <h3 class="mt-4 text-xl font-bold text-navy-900">Mantenimiento y mejora</h3>
            <p class="mt-2 text-sm">Actualizaciones, copias de seguridad y ajustes continuos para que tu web siga funcionando y atrayendo clientes.</p>
          </article>
        </div>
        <a href="#contacto" class="inline-block mt-10 bg-white text-navy-900 font-bold px-6 py-3 rounded-lg hover:bg-navy-50">Cuéntanos qué necesitas</a>
      </div>
    </section>

    <!-- ========== 4. TESTIMONIOS ========== -->
    <!-- NOTA: son ejemplos ficticios. Sustitúyelos por opiniones reales de tus clientes. -->
    <section id="testimonios" class="py-20">
      <div class="max-w-6xl mx-auto px-5">
        <h2 class="text-3xl font-extrabold text-navy-900">Lo que dicen otros negocios como el tuyo</h2>
        <div class="mt-10 grid md:grid-cols-3 gap-6">
          <figure class="p-6 rounded-xl border border-slate-200">
            <blockquote>“Desde que tenemos la web nueva recibimos reservas a diario. Antes todo era por teléfono.”</blockquote>
            <figcaption class="mt-5 flex items-center gap-3">
              <span class="w-10 h-10 rounded-full bg-navy-900 text-white font-bold flex items-center justify-center">LM</span>
              <span class="text-sm"><strong class="block text-navy-900">Laura M.</strong>Restaurante familiar</span>
            </figcaption>
          </figure>
          <figure class="p-6 rounded-xl border border-slate-200">
            <blockquote>“Automatizaron los avisos de citas y ahora casi nadie falla. Ganamos horas cada semana.”</blockquote>
            <figcaption class="mt-5 flex items-center gap-3">
              <span class="w-10 h-10 rounded-full bg-navy-900 text-white font-bold flex items-center justify-center">CR</span>
              <span class="text-sm"><strong class="block text-navy-900">Carlos R.</strong>Clínica de fisioterapia</span>
            </figcaption>
          </figure>
          <figure class="p-6 rounded-xl border border-slate-200">
            <blockquote>“Nos explicaron todo con calma y entregaron en el plazo acordado. Totalmente recomendables.”</blockquote>
            <figcaption class="mt-5 flex items-center gap-3">
              <span class="w-10 h-10 rounded-full bg-navy-900 text-white font-bold flex items-center justify-center">AS</span>
              <span class="text-sm"><strong class="block text-navy-900">Ana S.</strong>Tienda de decoración</span>
            </figcaption>
          </figure>
        </div>
      </div>
    </section>

    <!-- ========== 5. FAQ ========== -->
    <section id="faq" class="py-20 bg-navy-50">
      <div class="max-w-3xl mx-auto px-5">
        <h2 class="text-3xl font-extrabold text-navy-900">Preguntas frecuentes</h2>
        <div class="mt-8 space-y-3">
          <details class="group bg-white rounded-xl border border-sky-200 p-5">
            <summary class="flex justify-between items-center gap-4 cursor-pointer font-bold text-navy-900">¿Cuánto tarda en estar lista mi web?
              <svg class="chev shrink-0 transition-transform" width="20" height="20" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" aria-hidden="true"><path d="M4 7l6 6 6-6"/></svg></summary>
            <p class="mt-3 text-sm">Una web corporativa estándar suele estar lista entre 2 y 4 semanas, según el contenido y las funciones que necesites. Te damos una fecha concreta en el presupuesto.</p>
          </details>
          <details class="group bg-white rounded-xl border border-sky-200 p-5">
            <summary class="flex justify-between items-center gap-4 cursor-pointer font-bold text-navy-900">¿Qué es una automatización y para qué me sirve?
              <svg class="chev shrink-0 transition-transform" width="20" height="20" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" aria-hidden="true"><path d="M4 7l6 6 6-6"/></svg></summary>
            <p class="mt-3 text-sm">Es una tarea que se hace sola: por ejemplo, enviar un correo de confirmación cuando alguien te escribe o avisarte por mensaje de cada nuevo pedido. Ahorras tiempo y no pierdes oportunidades.</p>
          </details>
          <details class="group bg-white rounded-xl border border-sky-200 p-5">
            <summary class="flex justify-between items-center gap-4 cursor-pointer font-bold text-navy-900">¿Podré modificar mi web yo mismo?
              <svg class="chev shrink-0 transition-transform" width="20" height="20" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" aria-hidden="true"><path d="M4 7l6 6 6-6"/></svg></summary>
            <p class="mt-3 text-sm">Sí, si lo prefieres. Podemos dejarte un panel sencillo para cambiar textos y fotos, o encargarnos nosotros de los cambios con un plan de mantenimiento.</p>
          </details>
          <details class="group bg-white rounded-xl border border-sky-200 p-5">
            <summary class="flex justify-between items-center gap-4 cursor-pointer font-bold text-navy-900">¿Cuánto cuesta?
              <svg class="chev shrink-0 transition-transform" width="20" height="20" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" aria-hidden="true"><path d="M4 7l6 6 6-6"/></svg></summary>
            <p class="mt-3 text-sm">Depende de lo que necesites. Cuéntanos tu caso en el formulario y te enviamos un presupuesto cerrado, sin compromiso y sin costes ocultos.</p>
          </details>
        </div>
      </div>
    </section>

    <!-- ========== 6. CONTACTO ========== -->
    <section id="contacto" class="py-20">
      <div class="max-w-6xl mx-auto px-5 grid md:grid-cols-2 gap-12">
        <div>
          <h2 class="text-3xl font-extrabold text-navy-900">Hablemos de tu proyecto</h2>
          <p class="mt-5 max-w-md">Rellena el formulario y te respondemos en menos de 24 horas laborables con una propuesta a tu medida.</p>
          <!-- Sustituye estos datos por los reales -->
          <ul class="mt-8 space-y-2 text-sm">
            <li><strong class="text-navy-900">Correo:</strong> <a class="underline" href="mailto:webscreatorspain@gmail.com">webscreatorspain@gmail.com</a></li>
            <li><strong class="text-navy-900">Teléfono:</strong> <a class="underline" href="tel:+34640742530">640 74 25 30</a></li>
            <li><strong class="text-navy-900">Horario:</strong> lunes a viernes, 9:00 a 18:00</li>
          </ul>
        </div>

        <form id="form-contacto" class="space-y-4" novalidate>
          <div>
            <label for="nombre" class="block text-sm font-bold text-navy-900 mb-1">Nombre</label>
            <input id="nombre" name="nombre" type="text" required autocomplete="name" class="w-full rounded-lg border border-slate-300 px-4 py-3 focus:outline-none focus:ring-2 focus:ring-navy-600">
          </div>
          <div>
            <label for="email" class="block text-sm font-bold text-navy-900 mb-1">Correo electrónico</label>
            <input id="email" name="email" type="email" required autocomplete="email" class="w-full rounded-lg border border-slate-300 px-4 py-3 focus:outline-none focus:ring-2 focus:ring-navy-600">
          </div>
          <div>
            <label for="interes" class="block text-sm font-bold text-navy-900 mb-1">¿Qué necesitas?</label>
            <select id="interes" name="interes" class="w-full rounded-lg border border-slate-300 px-4 py-3 bg-white focus:outline-none focus:ring-2 focus:ring-navy-600">
              <option>Una página web nueva</option>
              <option>Automatizar tareas</option>
              <option>Mejorar mi web actual</option>
              <option>Otra consulta</option>
            </select>
          </div>
          <div>
            <label for="mensaje" class="block text-sm font-bold text-navy-900 mb-1">Mensaje</label>
            <textarea id="mensaje" name="mensaje" rows="4" required class="w-full rounded-lg border border-slate-300 px-4 py-3 focus:outline-none focus:ring-2 focus:ring-navy-600"></textarea>
          </div>
          <!-- Mensaje de estado (errores o éxito) -->
          <p id="form-estado" class="text-sm font-semibold" role="status" aria-live="polite"></p>
          <button type="submit" class="w-full bg-navy-900 text-white font-bold px-6 py-3.5 rounded-lg hover:bg-navy-700 focus:outline-none focus-visible:ring-2 focus-visible:ring-offset-2 focus-visible:ring-navy-600">Enviar mensaje</button>
        </form>
      </div>
    </section>
  </main>

  <!-- ========== FOOTER ========== -->
  <footer class="bg-navy-900 text-sky-200">
    <div class="max-w-6xl mx-auto px-5 py-10 flex flex-col md:flex-row justify-between gap-6 text-sm">
      <div>
        <p class="font-extrabold text-white text-lg">WebsCreatorsSpain</p>
        <p class="mt-1 max-w-xs">Páginas web y automatizaciones para pymes locales.</p>
      </div>
      <ul class="flex flex-wrap gap-x-6 gap-y-2">
        <li><a class="hover:text-white" href="#nosotros">Nosotros</a></li>
        <li><a class="hover:text-white" href="#servicios">Servicios</a></li>
        <li><a class="hover:text-white" href="#faq">Preguntas</a></li>
        <li><a class="hover:text-white" href="#contacto">Contacto</a></li>
      </ul>
    </div>
    <div class="border-t border-white/10 py-4 text-center text-xs">© <span id="anio">2026</span> WebsCreatorsSpain. Todos los derechos reservados.</div>
  </footer>

  <!-- ========== JAVASCRIPT ========== -->
  <script>
    // Año automático en el footer
    document.getElementById('anio').textContent = new Date().getFullYear();

    // Menú móvil: abrir/cerrar y cerrar al pulsar un enlace
    const btn = document.getElementById('menu-btn');
    const menu = document.getElementById('menu-movil');
    function toggleMenu(open) {
      menu.classList.toggle('hidden', !open);
      btn.setAttribute('aria-expanded', String(open));
    }
    btn.addEventListener('click', () => toggleMenu(menu.classList.contains('hidden')));
    menu.querySelectorAll('a').forEach(a => a.addEventListener('click', () => toggleMenu(false)));

    // Formulario: validación en el navegador.
    // IMPORTANTE: para recibir los mensajes, conecta el envío a un servicio
    // (Formspree, Formsubmit, tu backend…). Ejemplo en el comentario de fetch.
    const form = document.getElementById('form-contacto');
    const estado = document.getElementById('form-estado');
    form.addEventListener('submit', (e) => {
      e.preventDefault();
      const { nombre, email, mensaje } = form.elements;
      const emailOk = /^[^\s@]+@[^\s@]+\.[^\s@]+$/.test(email.value.trim());

      if (!nombre.value.trim() || !emailOk || !mensaje.value.trim()) {
        estado.className = 'text-sm font-semibold text-red-700';
        estado.textContent = 'Revisa el formulario: completa tu nombre, un correo válido y tu mensaje.';
        return;
      }

      /* Ejemplo de envío real con Formspree (sustituye TU_ID):
         fetch('https://formspree.io/f/TU_ID', {
           method: 'POST', body: new FormData(form), headers: { Accept: 'application/json' }
         }).then(...) */

      estado.className = 'text-sm font-semibold text-navy-700';
      estado.textContent = 'Mensaje enviado. Te responderemos en menos de 24 horas laborables.';
      form.reset();
    });
  </script>
</body>
</html>
