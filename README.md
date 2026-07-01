<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Nique Systems — AI Assistants, Automation, Website + AI</title>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700;800&display=swap" rel="stylesheet" />
  <style>
    :root{--bg:#0b0e13;--surface:#121825;--text:#e6e9ef;--muted:#a9b1bc;--primary:#6ee7ff;--primary-2:#8b5cf6;--accent:#22d3ee;--ring:rgba(110,231,255,.35);--grid:rgba(255,255,255,.035);--card:rgba(255,255,255,.04);--glass:rgba(110,231,255,.08);--radius:14px;--shadow:0 10px 30px rgba(0,0,0,.45), inset 0 1px 0 rgba(255,255,255,.03);--space:clamp(56px,8vw,96px);--container:1200px}
    *{box-sizing:border-box}
    html,body{margin:0;background:#0b0e13;color:var(--text);font-family:Inter,system-ui,-apple-system,Segoe UI,Roboto,"Helvetica Neue",Arial,sans-serif;line-height:1.6}
    a{color:var(--primary);text-decoration:none}
    .container{max-width:var(--container);margin:0 auto;padding:0 20px}
    body::before{content:"";position:fixed;inset:0;z-index:-2;background:radial-gradient(800px 500px at 80% -10%, rgba(139,92,246,.25), transparent 60%),radial-gradient(700px 400px at -10% 10%, rgba(34,211,238,.18), transparent 60%),linear-gradient(#0b0e13,#0b0e13)}
    body::after{content:"";position:fixed;inset:0;z-index:-3;background-image:linear-gradient(#0b0e13,#0b0e13),radial-gradient(circle at 25px 25px, var(--grid) 2px, transparent 2px);background-size:100% 100%,40px 40px;background-attachment:fixed}
    .nav{position:sticky;top:0;z-index:50;backdrop-filter:saturate(140%) blur(10px);background:linear-gradient(180deg, rgba(10,14,20,.85), rgba(10,14,20,.45));border-bottom:1px solid rgba(255,255,255,.06)}
    .nav-inner{display:flex;align-items:center;justify-content:space-between;height:64px}
    .brand{display:flex;align-items:center;gap:12px;font-weight:800}
    .mark{width:28px;height:28px;border-radius:8px;background:conic-gradient(from 180deg, var(--primary), var(--primary-2), var(--accent), var(--primary));box-shadow:0 0 22px rgba(110,231,255,.45), inset 0 0 10px rgba(255,255,255,.2)}
    .nav-actions{display:flex;gap:10px}
    .btn{display:inline-flex;align-items:center;justify-content:center;gap:8px;padding:12px 16px;border-radius:10px;border:1px solid rgba(255,255,255,.08);color:var(--text);background:linear-gradient(180deg, rgba(255,255,255,.03), rgba(255,255,255,.01));box-shadow:var(--shadow);cursor:pointer;transition:all .2s}
    .btn:hover{transform:translateY(-1px);border-color:rgba(110,231,255,.35)}
    .btn-primary{background:linear-gradient(180deg, rgba(34,211,238,.35), rgba(139,92,246,.28));color:#071018;font-weight:700;border:1px solid rgba(110,231,255,.55)}
    .hero{padding:calc(var(--space) + 24px) 0 var(--space)}
    .hero-grid{display:grid;grid-template-columns:1.15fr .85fr;gap:40px;align-items:center}
    .badge{display:inline-flex;gap:8px;padding:6px 10px;border-radius:999px;background:linear-gradient(180deg, rgba(110,231,255,.12), rgba(139,92,246,.1));border:1px solid rgba(110,231,255,.3);font-size:12px;color:#b9f9ff}
    .h1{font-size:clamp(36px,6vw,64px);line-height:1.05;margin:10px 0 14px;font-weight:800;letter-spacing:-.02em;background:linear-gradient(180deg,#ffffff,#b6f7ff 65%,#90a0ff);-webkit-background-clip:text;color:transparent}
    .sub{color:var(--muted);font-size:clamp(16px,2.5vw,18px);max-width:52ch}
    .hero-cta{display:flex;gap:12px;flex-wrap:wrap;margin-top:24px}
    .hero-media{position:relative;border-radius:clamp(14px,2vw,20px);overflow:hidden;background:radial-gradient(120% 120% at 80% 10%, rgba(110,231,255,.18), rgba(139,92,246,.14) 40%, transparent 70%), var(--surface);border:1px solid rgba(255,255,255,.06);box-shadow:var(--shadow);min-height:340px}
    .hero-media::after{content:"";position:absolute;inset:-1px;background:radial-gradient(400px 200px at 20% 0%, rgba(110,231,255,.35), transparent 60%),radial-gradient(400px 200px at 100% 60%, rgba(139,92,246,.3), transparent 60%);mix-blend-mode:screen}
    .ai-caption{position:absolute;left:16px;bottom:16px;font-size:12px;color:#cdefff;opacity:.8;background:rgba(7,16,24,.45);padding:6px 10px;border-radius:999px;border:1px solid rgba(110,231,255,.35)}
    .section{padding:var(--space) 0}
    .section h2{font-size:clamp(26px,3.8vw,36px);margin:0 0 10px}
    .section p.lead{color:var(--muted);margin:0 0 28px}
    .features{display:grid;grid-template-columns:repeat(3,1fr);gap:18px}
    .card{background:linear-gradient(180deg,var(--card),rgba(255,255,255,.02));border:1px solid rgba(255,255,255,.07);border-radius:var(--radius);padding:18px 18px 22px;box-shadow:var(--shadow)}
    .icon{width:40px;height:40px;border-radius:10px;display:grid;place-items:center;margin-bottom:12px;background:linear-gradient(180deg,var(--glass),rgba(255,255,255,.03));border:1px solid rgba(110,231,255,.35);color:#bdf4ff;font-weight:800}
    .selector{display:grid;grid-template-columns:repeat(3,1fr);gap:18px}
    .select-card{position:relative;padding:22px;border-radius:var(--radius);overflow:hidden;background:linear-gradient(180deg, rgba(139,92,246,.08), rgba(34,211,238,.06));border:1px solid rgba(110,231,255,.28);box-shadow:var(--shadow);transition:transform .18s,border-color .18s}
    .select-card:hover{transform:translateY(-2px);border-color:rgba(110,231,255,.6)}
    .select-card h3{margin:0 0 6px;font-size:18px}
    .select-card p{margin:0 0 12px;color:var(--muted)}
    .select-actions{display:flex;gap:10px;flex-wrap:wrap}
    .tag{font-size:12px;padding:4px 8px;border-radius:999px;border:1px solid rgba(255,255,255,.1);color:#d9d9ff;background:rgba(139,92,246,.16)}
    .select-card .btn{padding:10px 12px}
    .contact-grid{display:grid;grid-template-columns:1.1fr .9fr;gap:22px}
    form{display:grid;gap:12px}
    .field{display:grid;gap:6px}
    label{font-size:13px;color:#c7d2df}
    input,textarea,select{width:100%;padding:12px;border-radius:10px;border:1px solid rgba(255,255,255,.08);background:linear-gradient(180deg, rgba(255,255,255,.02), rgba(255,255,255,.01));color:var(--text);outline:none;transition:border .2s, box-shadow .2s}
    input:focus,textarea:focus,select:focus{border-color:var(--accent);box-shadow:0 0 0 6px var(--ring)}
    textarea{min-height:120px;resize:vertical}
    .help{font-size:12px;color:var(--muted)}
    .inline{display:flex;gap:10px;flex-wrap:wrap}
    footer{padding:28px 0 56px;color:var(--muted);border-top:1px solid rgba(255,255,255,.06);background:linear-gradient(180deg, rgba(255,255,255,.02), rgba(255,255,255,.0))}
    .foot{display:flex;align-items:center;justify-content:space-between;gap:12px;flex-wrap:wrap}
    @media (max-width:1024px){.hero-grid{grid-template-columns:1fr;gap:22px}.features,.selector{grid-template-columns:1fr 1fr}.contact-grid{grid-template-columns:1fr}}
    @media (max-width:640px){.features,.selector{grid-template-columns:1fr}.hero-cta .btn{flex:1}}
  </style>
</head>
<body>
  <div id="root"></div>

  <script>
    // Config
    const bookingUrl = '#'; // replace with your Calendly/Cal.com link
    const heroImageUrl = 'https://files.use.ai/files/chat%2Ffiles%2F5cca7295-f215-42b3-a5ff-fe2ca1b08848-agentic-image-1782925129666-0.png';

    // Build page via JS (Option B)
    const app = 
      <header class="nav">
        <div class="container nav-inner">
          <div class="brand"><div class="mark" aria-hidden="true"></div><span>Nique Systems</span></div>
          <div class="nav-actions">
            <a href="#services" class="btn">Explore Services</a>
            <a href="#contact" class="btn btn-primary">Book Consultation</a>
          </div>
        </div>
      </header>

      <main id="app">
        <section class="hero">
          <div class="container hero-grid">
            <div>
              <div class="badge">AI • Automation • Integration</div>
              <h1 class="h1">Nique Systems</h1>
              <p class="sub">Deploy production-ready AI assistants, automate workflows, and integrate AI across your website and stack — fast, secure, and measurable.</p>
              <div class="hero-cta">
                <a href="#services" class="btn btn-primary">Explore Services</a>
                <a href="#contact" class="btn">Book Consultation</a>
              </div>
            </div>
            <div class="hero-media" id="heroMedia" aria-label="High-tech AI visual">
              <div class="ai-caption">Concept: Humanlike AI — dark hi‑tech</div>
            </div>
          </div>
        </section>

        <section id="services" class="section">
          <div class="container">
            <h2>What We Do</h2>
            <p class="lead">Focused offerings that move the needle from day one.</p>
            <div class="features">
              <div class="card"><div class="icon">A</div><h3>AI Assistants</h3><p>Custom GPT-style agents for support, sales, and internal ops with guardrails, analytics, and continuous improvement.</p></div>
              <div class="card"><div class="icon">⚙︎</div><h3>Automation</h3><p>Orchestrate across your stack to eliminate manual work — from lead routing to fulfillment and reporting.</p></div>
              <div class="card"><div class="icon">⌂</div><h3>Website + AI Integration</h3><p>Embed AI into your site: smart search, guided flows, dynamic content, and secure data connectors.</p></div>
            </div>
          </div>
        </section>

        <section class="section">
          <div class="container">
            <h2>Choose Your Path</h2>
            <p class="lead">Pick the option that best matches where you are today.</p>
            <div class="selector">
              <div class="select-card">
                <span class="tag">Fastest</span>
                <h3>I know what I need</h3>
                <p>Great — tell us the scope and we’ll get you a proposal within 24–48 hours.</p>
                <div class="select-actions">
                  <a href="#contact" class="btn btn-primary">Start my brief</a>
                  <a href="#contact" class="btn">Ask a question</a>
                </div>
              </div>
              <div class="select-card">
                <span class="tag">Guided</span>
                <h3>I need help choosing</h3>
                <p>We’ll map your goals to the right assistant, automations, and integrations.</p>
                <div class="select-actions">
                  <a href="#contact" class="btn btn-primary">Free discovery call</a>
                  <a href="#services" class="btn">See capabilities</a>
                </div>
              </div>
              <div class="select-card">
                <span class="tag">Premium</span>
                <h3>I want AI strategy (paid)</h3>
                <p>A structured strategy sprint: roadmap, KPIs, architecture, and phased delivery plan.</p>
                <div class="select-actions">
                  <a href="#contact" class="btn btn-primary">Book strategy session</a>
                  <a href="#contact" class="btn">Request outline</a>
                </div>
              </div>
            </div>
          </div>
        </section>

        <section id="contact" class="section">
          <div class="container">
            <h2>Contact / Booking</h2>
            <p class="lead">Tell us a bit about your goals. We’ll reply quickly with next steps.</p>
            <div class="contact-grid">
              <form id="contactForm">
                <div class="field"><label for="name">Name</label><input id="name" name="name" placeholder="Your name" required /></div>
                <div class="field"><label for="email">Email</label><input id="email" type="email" name="email" placeholder="you@company.com" required /></div>
                <div class="field"><label for="path">Which path?</label>
                  <select id="path" name="path">
                    <option>I know what I need</option>
                    <option>I need help choosing</option>
                    <option>I want AI strategy (paid)</option>
                  </select>
                </div>
                <div class="inline">
                  <div class="field" style="flex:1 1 220px"><label for="company">Company</label><input id="company" name="company" placeholder="Company or project" /></div>
                  <div class="field" style="flex:1 1 180px"><label for="budget">Rough budget</label>
                    <select id="budget" name="budget">
                      <option>Undecided</option><option>Starter</option><option>Growth</option><option>Scale</option>
                    </select>
                    <div class="help">Optional — helps us tailor options.</div>
                  </div>
                </div>
                <div class="field"><label for="message">Goals / scope</label><textarea id="message" name="message" placeholder="Briefly describe what you want to build…"></textarea></div>
                <div class="inline">
                  <button class="btn btn-primary" type="submit">Send message</button>
                  <a class="btn" id="bookingLink" href="#booking">Book consultation</a>
                </div>
                <div id="formNote" class="help"></div>
              </form>
              <div class="card">
                <h3>Fast scheduling</h3>
                <p>Pick a time that works for you. We’ll meet on video and map the next steps.</p>
                <div style="height:16px"></div>
                <a id="booking" class="btn btn-primary" href="#">Open booking</a>
                <div style="height:10px"></div>
                <p class="help">Link this to your Calendly/Cal.com once ready.</p>
                <div style="height:18px"></div>
                <h3>What to expect</h3>
                <ul style="margin:8px 0 0 18px; color:var(--muted)">
                  <li>10–20 min to understand goals</li>
                  <li>Feasibility and suggested approach</li>
                  <li>Clear next steps and timeline</li>
                </ul>
              </div>
            </div>
          </div>
        </section>
      </main>

      <footer>
        <div class="container foot">
          <div>© <span id="y"></span> Nique Systems</div>
          <div class="inline">
            <a href="#services">Services</a><span style="opacity:.3">•</span>
            <a href="#contact">Contact</a><span style="opacity:.3">•</span>
            <a href="#">Privacy</a>
          </div>
        </div>
      </footer>
    ;

    // Inject into DOM
    document.getElementById('root').innerHTML = app;

    // Wire interactions
    document.querySelectorAll('a[href^="#"]').forEach(a=>{
      a.addEventListener('click', e=>{
        const id=a.getAttribute('href');
        if(id==="#"||!document.querySelector(id)) return;
        e.preventDefault();
        document.querySelector(id).scrollIntoView({behavior:'smooth', block:'start'});
      });
    });

    // Year
    document.getElementById('y').textContent = new Date().getFullYear();

    // Form (stub)
    const form = document.getElementById('contactForm');
    const formNote = document.getElementById('formNote');
    form.addEventListener('submit', async (e)=>{
      e.preventDefault();
      const data = Object.fromEntries(new FormData(form).entries());
      // await fetch('/api/contact', { method:'POST', headers:{'Content-Type':'application/json'}, body: JSON.stringify(data) });
      formNote.textContent = 'Thanks — captured locally. Connect your endpoint to send.';
      form.reset();
    });

    // Booking links
    document.getElementById('booking').setAttribute('href', bookingUrl);
    document.getElementById('bookingLink').setAttribute('href', bookingUrl);

    // Apply hero image
    const media = document.getElementById('heroMedia');
    media.style.background = \url('\${heroImageUrl}') center / cover no-repeat, radial-gradient(120% 120% at 80% 10%, rgba(110,231,255,.18), rgba(139,92,246,.14) 40%, transparent 70%), #121825\;
    media.style.border = '1px solid rgba(255,255,255,.06)';
    media.style.borderRadius = '18px';
    media.style.minHeight = '340px';
  </script>
</body>
</html>
