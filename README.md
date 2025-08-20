<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Elle Stone Craft — Where Stone Meets Art.</title>
  <meta name="description" content="Premium 2D & 3D CNC carved stone panels for luxury interiors and architecture. Custom design, precision manufacturing, finishing and installation." />
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@600;700&family=Poppins:wght@300;400;500;600&display=swap" rel="stylesheet">
  <style>
    :root{
      --bg:#0f0f10;--ink:#eceaea;--muted:#b7b5b2;--line:#2a2a2a;--gold:#d6b36a;--card:#161616;--stone:#c9c4b8
    }
    *{box-sizing:border-box}
    html,body{margin:0;background:var(--bg);color:var(--ink);font-family:Poppins,system-ui,-apple-system,Segoe UI,Roboto,Helvetica,Arial,sans-serif;scroll-behavior:smooth}
    a{color:inherit;text-decoration:none}
    img{max-width:100%;display:block}
    .container{max-width:1180px;margin:auto;padding:0 20px}
    .btn{display:inline-flex;align-items:center;gap:.6rem;background:linear-gradient(135deg,var(--gold),#b8923f);color:#111;font-weight:600;padding:.9rem 1.15rem;border-radius:12px;border:none;cursor:pointer;transition:transform .15s ease, box-shadow .15s ease}
    .btn:hover{transform:translateY(-2px);box-shadow:0 10px 30px rgba(214,179,106,.25)}
    .btn.outline{background:transparent;color:var(--ink);border:1px solid var(--line)}

    /* Header */
    header{position:sticky;top:0;z-index:40;background:rgba(15,15,15,.7);backdrop-filter:saturate(130%) blur(8px);border-bottom:1px solid var(--line)}
    .nav{display:flex;align-items:center;justify-content:space-between;padding:14px 0}
    .brand{display:flex;align-items:center;gap:.7rem}
    .monogram{width:40px;height:40px;border-radius:10px;background:linear-gradient(145deg,#b8ab8a,#8e8265);display:grid;place-items:center;box-shadow:inset 0 1px 0 #fff2}
    .monogram svg{width:20px;height:20px}
    .brand b{font-family:"Playfair Display",serif;letter-spacing:.06em}
    nav a{padding:8px 10px;border-radius:8px}
    nav a:hover{background:#ffffff08}

    /* Hero */
    .hero{position:relative;isolation:isolate}
    .hero .bg{position:absolute;inset:0;background:url('https://images.unsplash.com/photo-1617854818583-09e7f077a163?q=80&w=1600&auto=format&fit=crop') center/cover no-repeat;filter:grayscale(100%) brightness(.55) contrast(1.05)}
    .hero .overlay{position:absolute;inset:0;background:radial-gradient(70% 60% at 60% 40%, #0000, #0008 60%, #000e)}
    .hero .content{padding:92px 0 70px}
    .kicker{color:var(--muted);text-transform:uppercase;letter-spacing:.22em;font-size:.78rem}
    h1{font-family:"Playfair Display",serif;font-size:clamp(2rem,5vw,3.6rem);line-height:1.05;margin:.5rem 0 1rem}
    .sub{color:#ddd;max-width:780px}
    .cta{display:flex;gap:12px;flex-wrap:wrap;margin-top:20px}
    .badges{display:grid;grid-template-columns:repeat(3,1fr);gap:10px;margin-top:26px}
    .badge{border:1px solid var(--line);background:rgba(255,255,255,.02);padding:10px 12px;border-radius:12px;text-align:center;font-weight:500}

    /* Sections */
    section{padding:70px 0;border-top:1px solid var(--line)}
    h2{font-family:"Playfair Display",serif;font-size:clamp(1.6rem,3.3vw,2.2rem);margin:0 0 12px}
    .muted{color:var(--muted)}

    /* Gallery */
    .grid{display:grid;gap:14px}
    .grid.cols-3{grid-template-columns:repeat(3,1fr)}
    .grid.cols-4{grid-template-columns:repeat(4,1fr)}
    .card{position:relative;overflow:hidden;border-radius:16px;background:var(--card);border:1px solid var(--line)}
    .card .cap{position:absolute;inset:auto 0 0 0;padding:12px 14px;background:linear-gradient(180deg,transparent,rgba(0,0,0,.55));font-weight:500}

    /* Capabilities / Steps */
    .steps{display:grid;grid-template-columns:repeat(4,1fr);gap:12px}
    .step{background:var(--card);border:1px solid var(--line);padding:18px;border-radius:14px}
    .step b{display:block;margin-bottom:6px}

    /* Quote band */
    .band{background:linear-gradient(135deg,#1b1b1b,#101010);border:1px solid var(--line);padding:26px;border-radius:18px;display:flex;flex-wrap:wrap;align-items:center;justify-content:space-between;gap:14px}

    /* Contact */
    .contact{display:grid;grid-template-columns:1.1fr .9fr;gap:18px}
    form{background:var(--card);border:1px solid var(--line);padding:18px;border-radius:14px}
    label{display:block;font-size:.9rem;margin:.2rem 0}
    input,textarea,select{width:100%;background:#0b0b0b;border:1px solid #2b2b2b;color:var(--ink);padding:12px;border-radius:10px;outline:none}
    textarea{min-height:120px;resize:vertical}
    .small{font-size:.86rem;color:var(--muted)}

    /* FAQ */
    details{background:var(--card);border:1px solid var(--line);padding:14px;border-radius:12px}
    details+details{margin-top:10px}
    summary{cursor:pointer;font-weight:600}

    /* Lightbox */
    .lightbox{position:fixed;inset:0;background:#000d;display:none;place-items:center;z-index:60}
    .lightbox.open{display:grid}
    .lightbox img{max-width:92vw;max-height:86vh;border-radius:12px}

    /* Floating WhatsApp */
    .fab{position:fixed;right:18px;bottom:18px;z-index:55}
    .fab a{display:inline-flex;align-items:center;gap:.5rem;background:#25D366;color:#051;box-shadow:0 10px 20px #0006;padding:.9rem 1rem;border-radius:999px;font-weight:600}

    footer{border-top:1px solid var(--line);padding:26px 0;color:var(--muted)}

    /* Responsive */
    @media (max-width: 1024px){.grid.cols-4{grid-template-columns:repeat(3,1fr)}}
    @media (max-width: 920px){
      .badges{grid-template-columns:1fr 1fr}
      .grid.cols-3{grid-template-columns:1fr 1fr}
      .steps{grid-template-columns:1fr 1fr}
      .contact{grid-template-columns:1fr}
    }
    @media (max-width: 560px){
      .grid.cols-3,.grid.cols-4{grid-template-columns:1fr}
      .steps{grid-template-columns:1fr}
    }
  </style>
</head>
<body>
  <header>
    <div class="container nav">
      <a class="brand" href="#top">
        <span class="monogram" aria-hidden="true">
          <svg viewBox="0 0 24 24" fill="none" stroke="#101010" stroke-width="1.6"><path d="M5 18V6h6a5 5 0 010 10H5Z" fill="#e9dec5"/><path d="M13 6h6v12" stroke="#c3b28b"/></svg>
        </span>
        <b>Elle Stone Craft</b>
      </a>
      <nav style="display:flex;gap:14px;align-items:center">
        <a href="#work" class="small">Portfolio</a>
        <a href="#services" class="small">Capabilities</a>
        <a href="#materials" class="small">Materials</a>
        <a href="#process" class="small">Process</a>
        <a href="#testimonials" class="small">Clients</a>
        <a href="#faq" class="small">FAQ</a>
        <a href="#contact" class="btn">Get a Quote</a>
      </nav>
    </div>
  </header>

  <main id="top">
    <!-- Hero -->
    <section class="hero">
      <div class="bg" aria-hidden="true"></div>
      <div class="overlay"></div>
      <div class="container content">
        <span class="kicker">2D & 3D CNC CARVED STONE PANELS</span>
        <h1>Where <span style="color:var(--gold)">Stone</span> Meets Art.</h1>
        <p class="sub">We craft precision CNC‑carved stone surfaces for luxury interiors & architecture — floral compositions, geometric lattices, temple & heritage work, and back‑lit feature walls.</p>
        <div class="cta">
          <a class="btn" href="#contact">WhatsApp Quote</a>
          <a class="btn outline" href="#work">View Portfolio</a>
        </div>
        <div class="badges">
          <div class="badge">Custom CAD & Design</div>
          <div class="badge">High‑Precision CNC</div>
          <div class="badge">Finish & Installation</div>
        </div>
      </div>
    </section>

    <!-- Portfolio / Work -->
    <section id="work">
      <div class="container">
        <h2>Signature Work</h2>
        <p class="muted">Replace the placeholders with your project photos. Click to view large.</p>
        <div class="grid cols-4" style="margin-top:14px">
          <figure class="card"><img src="https://images.unsplash.com/photo-1615529170410-9ead9a91f61e?q=80&w=1200&auto=format&fit=crop" alt="3D carved floral panel" loading="lazy" data-large="https://images.unsplash.com/photo-1615529170410-9ead9a91f61e?q=80&w=1800&auto=format&fit=crop"/><figcaption class="cap">3D floral feature wall</figcaption></figure>
          <figure class="card"><img src="https://images.unsplash.com/photo-1523474253046-8cd2748b5fd2?q=80&w=1200&auto=format&fit=crop" alt="Geometric CNC surface" loading="lazy" data-large="https://images.unsplash.com/photo-1523474253046-8cd2748b5fd2?q=80&w=1800&auto=format&fit=crop"/><figcaption class="cap">Geometric carved surface</figcaption></figure>
          <figure class="card"><img src="https://images.unsplash.com/photo-1582582494700-68f5f9a6383c?q=80&w=1200&auto=format&fit=crop" alt="Backlit stone wall" loading="lazy" data-large="https://images.unsplash.com/photo-1582582494700-68f5f9a6383c?q=80&w=1800&auto=format&fit=crop"/><figcaption class="cap">Back‑lit statement wall</figcaption></figure>
          <figure class="card"><img src="https://images.unsplash.com/photo-1519710884001-0e3d3d93d46f?q=80&w=1200&auto=format&fit=crop" alt="Temple carving" loading="lazy" data-large="https://images.unsplash.com/photo-1519710884001-0e3d3d93d46f?q=80&w=1800&auto=format&fit=crop"/><figcaption class="cap">Heritage inspired carving</figcaption></figure>
          <figure class="card"><img src="https://images.unsplash.com/photo-1519710164239-da123dc03ef4?q=80&w=1200&auto=format&fit=crop" alt="Contemporary panel" loading="lazy" data-large="https://images.unsplash.com/photo-1519710164239-da123dc03ef4?q=80&w=1800&auto=format&fit=crop"/><figcaption class="cap">Contemporary panel</figcaption></figure>
          <figure class="card"><img src="https://images.unsplash.com/photo-1501183638710-841dd1904471?q=80&w=1200&auto=format&fit=crop" alt="Craft detail" loading="lazy" data-large="https://images.unsplash.com/photo-1501183638710-841dd1904471?q=80&w=1800&auto=format&fit=crop"/><figcaption class="cap">Detail & texture</figcaption></figure>
          <figure class="card"><img src="https://images.unsplash.com/photo-1564497340540-2b1b6fe1a7f2?q=80&w=1200&auto=format&fit=crop" alt="Workshop" loading="lazy" data-large="https://images.unsplash.com/photo-1564497340540-2b1b6fe1a7f2?q=80&w=1800&auto=format&fit=crop"/><figcaption class="cap">Workshop & QC</figcaption></figure>
          <figure class="card"><img src="https://images.unsplash.com/photo-1582719478250-c89cae4dc85b?q=80&w=1200&auto=format&fit=crop" alt="Installation" loading="lazy" data-large="https://images.unsplash.com/photo-1582719478250-c89cae4dc85b?q=80&w=1800&auto=format&fit=crop"/><figcaption class="cap">Installation on site</figcaption></figure>
        </div>
      </div>
    </section>

    <!-- Capabilities -->
    <section id="services">
      <div class="container">
        <h2>Capabilities</h2>
        <div class="grid cols-3" style="margin-top:10px">
          <div class="step"><b>Custom Design & CAD</b><span class="small">Bespoke patterns, CAD/CAM tool‑paths and material guidance for marble, sandstone, limestone & more.</span></div>
          <div class="step"><b>2D & 3D CNC Carving</b><span class="small">High‑precision machining with depth control for intricate florals, geometry and murals.</span></div>
          <div class="step"><b>Finishing & Installation</b><span class="small">Hand finishing, back‑lighting integration, onsite fitment and quality assurance.</span></div>
        </div>

        <h3 style="margin:28px 0 10px">Process</h3>
        <div id="process" class="steps">
          <div class="step"><b>01 — Brief</b><span class="small">Share sizes, reference style and material.</span></div>
          <div class="step"><b>02 — Design</b><span class="small">We prepare artwork & approvals.</span></div>
          <div class="step"><b>03 — Manufacture</b><span class="small">CNC carving + hand finishing.</span></div>
          <div class="step"><b>04 — Install</b><span class="small">Delivery & fitment with care.</span></div>
        </div>

        <div class="band" style="margin-top:22px">
          <div>
            <b style="font-family:'Playfair Display',serif;font-size:1.2rem">Have a wall in mind?</b>
            <div class="small">Send sizes & a photo on WhatsApp for a quick estimate.</div>
          </div>
          <div style="display:flex;gap:10px">
            <a class="btn" href="https://wa.me/918000000000?text=Hi%20Elle%20Stone%20Craft%2C%20please%20quote%20for%20a%20custom%20carved%20panel." target="_blank" rel="noopener">WhatsApp Now</a>
            <a class="btn outline" href="#contact">Send Enquiry</a>
          </div>
        </div>
      </div>
    </section>

    <!-- Materials -->
    <section id="materials">
      <div class="container">
        <h2>Materials</h2>
        <p class="muted">Recommended stones for carving and back‑lighting.</p>
        <div class="grid cols-4" style="margin-top:12px">
          <figure class="card"><img src="https://images.unsplash.com/photo-1582582494700-68f5f9a6383c?q=80&w=1200&auto=format&fit=crop" alt="Italian marble"/><figcaption class="cap">Italian / Indian Marble</figcaption></figure>
          <figure class="card"><img src="https://images.unsplash.com/photo-1534088568595-a066f410bcda?q=80&w=1200&auto=format&fit=crop" alt="Sandstone"/><figcaption class="cap">Sandstone</figcaption></figure>
          <figure class="card"><img src="https://images.unsplash.com/photo-1523419409543-8c4b6b8a76df?q=80&w=1200&auto=format&fit=crop" alt="Limestone"/><figcaption class="cap">Limestone</figcaption></figure>
          <figure class="card"><img src="https://images.unsplash.com/photo-1596079890731-6b6f0efa4699?q=80&w=1200&auto=format&fit=crop" alt="Onyx backlit"/><figcaption class="cap">Onyx (Back‑lit)</figcaption></figure>
        </div>
      </div>
    </section>

    <!-- Testimonials / Clients -->
    <section id="testimonials">
      <div class="container">
        <h2>Trusted by Designers & Builders</h2>
        <div class="grid cols-3" style="margin-top:12px">
          <div class="step"><b>Studio A (Mumbai)</b><span class="small">“Flawless execution on a 22‑ft feature wall — superb detailing and timelines.”</span></div>
          <div class="step"><b>Interior Lab (Delhi)</b><span class="small">“Back‑lit panels were engineered perfectly for even light diffusion.”</span></div>
          <div class="step"><b>Heritage Homes (Jaipur)</b><span class="small">“Temple carvings with museum‑grade finish. Highly recommended.”</span></div>
        </div>
      </div>
    </section>

    <!-- FAQ -->
    <section id="faq">
      <div class="container">
        <h2>FAQ</h2>
        <details open>
          <summary>How do I get a quote?</summary>
          <p class="small">Share wall size (H×W), stone preference and a reference image. We reply with concepts, timeline and estimate.</p>
        </details>
        <details>
          <summary>Do you handle installation?</summary>
          <p class="small">Yes, pan‑India installation is available. Export shipping on request.</p>
        </details>
        <details>
          <summary>What file formats do you accept?</summary>
          <p class="small">JPEG/PNG for references, DWG/AI/SVG for vector/CAD when available. We can also design from scratch.</p>
        </details>
      </div>
    </section>

    <!-- Contact / Quote -->
    <section id="contact">
      <div class="container">
        <h2>Request a Quote</h2>
        <p class="muted">Send your sizes and notes. The form opens WhatsApp with a pre‑filled message so you can attach photos easily.</p>
        <div class="contact" style="margin-top:10px">
          <form onsubmit="return sendQuote(event)">
            <label>Name</label>
            <input required name="name" placeholder="Your name" />
            <label>Phone / WhatsApp</label>
            <input required name="phone" placeholder="+91 …" />
            <label>Email</label>
            <input name="email" type="email" placeholder="you@example.com" />
            <label>Project Type</label>
            <select name="type">
              <option>3D Carved Feature Wall</option>
              <option>2D Decorative Panel</option>
              <option>Temple / Heritage Style</option>
              <option>Back‑lit Panel</option>
              <option>Other / Not sure</option>
            </select>
            <label>Wall Size & Notes</label>
            <textarea name="notes" placeholder="Height × Width (in feet), stone preference, timeline…"></textarea>

            <div style="display:flex;gap:10px;align-items:center;margin-top:10px">
              <button class="btn" type="submit">Send on WhatsApp</button>
              <a class="btn outline" target="_blank" rel="noopener" href="mailto:hello@ellestonecraft.com?subject=Quote%20Request%20-%20Elle%20Stone%20Craft">Email Instead</a>
            </div>
            <p class="small" style="margin-top:8px">Call: <a href="tel:+918000000000">+91 80000 00000</a></p>
          </form>
          <div>
            <div class="card" style="padding:18px">
              <h3 style="margin:0 0 10px;font-family:'Playfair Display',serif">Quick Area Estimator</h3>
              <div class="small">Enter wall size to estimate panel area.</div>
              <div style="display:grid;grid-template-columns:1fr 1fr;gap:10px;margin-top:10px">
                <input id="ht" placeholder="Height (ft)" inputmode="decimal">
                <input id="wd" placeholder="Width (ft)" inputmode="decimal">
              </div>
              <div class="small" style="margin-top:10px">Area: <b id="area">0</b> sq.ft</div>
              <div class="small" style="margin-top:8px">Indicative price (editable): ₹ <input id="rate" value="1800" style="width:90px"> / sq.ft → <b id="amt">₹0</b></div>
            </div>
            <div class="card" style="margin-top:12px;padding:18px">
              <h3 style="margin:0 0 10px;font-family:'Playfair Display',serif">Showroom / Factory</h3>
              <p class="small">Plot 12, Industrial Area, Jaipur, Rajasthan • Mon–Sat, 10am–7pm</p>
              <div style="display:flex;gap:10px;margin-top:8px">
                <a class="btn outline" href="#" target="_blank" rel="noopener">View on Google Maps</a>
                <a class="btn outline" href="https://instagram.com/ellestonecraft" target="_blank" rel="noopener">Instagram</a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </main>

  <div class="fab"><a href="https://wa.me/918000000000?text=Hi%20Elle%20Stone%20Craft%2C%20I%27d%20like%20a%20quote." target="_blank" rel="noopener">WhatsApp Quote</a></div>

  <footer>
    <div class="container" style="display:flex;justify-content:space-between;gap:10px;flex-wrap:wrap">
      <span class="small">© <span id="year"></span> Elle Stone Craft. All rights reserved.</span>
      <span class="small">Tagline: <i>Where Stone Meets Art.</i></span>
    </div>
  </footer>

  <!-- Lightbox -->
  <div id="lb" class="lightbox" onclick="this.classList.remove('open')"><img alt="preview"/></div>

  <script>
    // dynamic year
    document.getElementById('year').textContent = new Date().getFullYear();

    // simple form -> open WhatsApp with prefilled message
    function sendQuote(e){
      e.preventDefault();
      const f = e.target;
      const msg = encodeURIComponent(
        `Enquiry from website:%0AName: ${f.name.value}%0APhone: ${f.phone.value}%0AEmail: ${f.email.value || '-'}%0AType: ${f.type.value}%0ASize/Notes: ${f.notes.value}`
      );
      window.open(`https://wa.me/918000000000?text=${msg}`,'_blank');
      return false;
    }

    // gallery lightbox
    const lb = document.getElementById('lb');
    document.querySelectorAll('#work img').forEach(img=>{
      img.style.cursor='zoom-in';
      img.addEventListener('click',()=>{
        lb.querySelector('img').src = img.dataset.large || img.src;
        lb.classList.add('open');
      });
    });

    // area calculator
    const ht = document.getElementById('ht');
    const wd = document.getElementById('wd');
    const rate = document.getElementById('rate');
    const area = document.getElementById('area');
    const amt = document.getElementById('amt');
    [ht,wd,rate].forEach(el=> el.addEventListener('input', calc));
    function calc(){
      const h = parseFloat(ht.value)||0, w = parseFloat(wd.value)||0, r=parseFloat(rate.value)||0;
      const a = +(h*w).toFixed(2); area.textContent = a;
      const v = Math.round(a*r).toLocaleString('en-IN'); amt.textContent = '₹'+v;
    }

    // fade-in on scroll
    const io = new IntersectionObserver((entries)=>{
      entries.forEach(e=>{ if(e.isIntersecting){ e.target.style.opacity=1; e.target.style.transform='translateY(0)'; } });
    },{threshold:.15});
    document.querySelectorAll('section .container').forEach(el=>{ el.style.opacity=.001; el.style.transform='translateY(14px)'; io.observe(el); });
  </script>

  <!-- SEO Schema -->
  <script type="application/ld+json">
  {
    "@context": "https://schema.org",
    "@type": "LocalBusiness",
    "name": "Elle Stone Craft",
    "description": "2D & 3D CNC carved stone panels for luxury interiors and architecture.",
    "url": "https://ellestonecraft.example",
    "telephone": "+91-80000-00000",
    "address": {"@type":"PostalAddress","streetAddress":"Plot 12, Industrial Area","addressLocality":"Jaipur","addressRegion":"Rajasthan","addressCountry":"IN"},
    "sameAs": ["https://instagram.com/ellestonecraft"],
    "slogan": "Where Stone Meets Art.",
    "image": "https://images.unsplash.com/photo-1615529170410-9ead9a91f61e?q=80&w=1200&auto=format&fit=crop"
  }
  </script>
</body>
</html>
