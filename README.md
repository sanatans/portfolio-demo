<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Sanatan Swain — Portfolio</title>
  <meta name="description" content="Sanatan Swain — Backend & Full-Stack Engineer (Payments, POS, Disputes, Java, Spring Boot)" />
  <style>
    /* ------------------------------------------------------------
       Gamma-style exact clone (1A,2A): dark navy + purple wavy bg,
       alternating full-width colored sections, numbered cards, etc.
       Save as index.html (place Sanatan-Swain.pdf in same folder).
       ------------------------------------------------------------ */

    :root{
      --navy:#07071a;
      --deep:#0c0f1a;
      --muted:#b6c0cf;
      --accent-pink:#b24c86;
      --accent-purple:#8c5bd6;
      --accent-blue:#0b4bc4;
      --card-bg: rgba(255,255,255,0.03);
      --glass: rgba(255,255,255,0.04);
      --white: #f6f8fb;
      --maxw:1200px;
      --radius:14px;
      font-family: "Inter", system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
      color:var(--white);
    }

    *{box-sizing:border-box}
    body{
      margin:0;
      background: radial-gradient(1200px 400px at 10% 20%, rgba(140,91,214,0.12), transparent 8%),
                  radial-gradient(1000px 400px at 90% 80%, rgba(178,76,134,0.10), transparent 8%),
                  linear-gradient(180deg,#060612 0%, #0a0b14 40%, #060613 100%);
      min-height:100vh;
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
      color:var(--white);
      letter-spacing:0.1px;
    }

    a{color:inherit}
    .wrap{max-width:var(--maxw);margin:0 auto;padding:28px 20px}

    /* top tiny header / no nav per PDF but small top bar */
    .topbar{display:flex;justify-content:space-between;align-items:center;margin-bottom:18px}
    .brand{font-weight:800;font-size:20px}
    .top-actions{display:flex;gap:10px;align-items:center}
    .btn{
      background:linear-gradient(90deg,var(--accent-pink),var(--accent-purple));
      color:#fff;padding:8px 12px;border-radius:10px;font-weight:700;text-decoration:none;border:none;cursor:pointer;
      box-shadow:0 8px 22px rgba(140,91,214,0.14);
    }
    .btn.ghost{background:transparent;border:1px solid rgba(255,255,255,0.06);color:var(--white);box-shadow:none}

    /* HERO full width background image style mimic */
    .hero{
      margin:-8px -8px 0 -8px;
      padding:120px 0 90px 0;
      background-image:
        radial-gradient(600px 160px at 10% 20%, rgba(140,91,214,0.08), transparent 20%),
        radial-gradient(700px 180px at 90% 80%, rgba(178,76,134,0.06), transparent 20%),
        linear-gradient(180deg, rgba(5,7,12,0.75), rgba(6,7,14,0.85));
      color:var(--white);
      text-align:center;
    }
    .hero .wrap{display:flex;flex-direction:column;align-items:center;gap:18px}
    .hero h1{font-size:40px;margin:6px 0;font-weight:800}
    .hero .sub{color:var(--muted);max-width:900px;margin:0 auto;font-size:14px}
    .hero .controls{display:flex;gap:12px;margin-top:16px}

    /* PROFESSIONAL PROFILE (Dark gradient block) */
    .section{
      padding:72px 0;
      margin:0 -8px;
    }
    .block--dark{
      background:
        radial-gradient(800px 250px at 12% 18%, rgba(140,91,214,0.04), transparent 15%),
        radial-gradient(900px 300px at 90% 82%, rgba(11,27,86,0.06), transparent 15%),
        linear-gradient(180deg, rgba(6,7,20,0.95), rgba(8,9,20,0.98));
      padding-top:48px;padding-bottom:48px;
    }

    .two-col{display:grid;grid-template-columns:1fr 420px;gap:28px;align-items:start;max-width:var(--maxw);margin:0 auto}
    .profile-cards{display:grid;grid-template-columns:repeat(2,1fr);gap:16px;align-items:start}
    .card{
      background:var(--card-bg);
      border-radius:12px;padding:18px;border:1px solid rgba(255,255,255,0.04);
      box-shadow: 0 8px 30px rgba(2,6,23,0.5);
    }
    .card h4{margin:0 0 8px;font-size:15px}
    .card p{margin:0;color:var(--muted);font-size:13px;line-height:1.5}

    .profile-image{
      display:flex;align-items:center;justify-content:center;
      background:#fff;border-radius:6px;padding:8px;height:420px; /* screenshot shows portrait card */
    }
    .profile-image img{max-width:100%;max-height:100%;display:block}

    /* TECHNICAL EXPERTISE block - maroon */
    .block--maroon{
      background: linear-gradient(180deg,#5b1738 0%, #7a2a57 100%);
      padding-top:42px;padding-bottom:42px;
    }
    .expert-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:20px;color:var(--white);max-width:var(--maxw);margin:0 auto;padding:24px 18px}
    .expert-grid ul{margin:10px 0 0 18px;color:rgba(255,255,255,0.9)}
    .expert-grid h3{margin:0 0 6px}

    /* Education strip (dark with small cards) */
    .edu-strip{padding:36px 0;background:linear-gradient(180deg, rgba(7,7,14,0.98), rgba(7,7,14,0.98));}
    .edu-grid{display:flex;gap:18px;max-width:var(--maxw);margin:0 auto;justify-content:center}
    .edu-card{border:1px solid rgba(255,255,255,0.06);padding:16px;border-radius:10px;width:360px;background:transparent;color:var(--muted)}
    .edu-card .num{display:inline-block;background:rgba(140,91,214,0.18);color:var(--white);padding:8px 12px;border-radius:999px;margin-bottom:8px;font-weight:800}

    /* Experience pink strip EXACT */
    .block--pink{
      background: linear-gradient(180deg, rgba(196,63,144,0.95), rgba(196,63,144,0.95));
      color: #0f1724;
      padding:52px 0;
    }
    .exp-inner{max-width:var(--maxw);margin:0 auto;padding:6px 18px;color:#0f1724}
    .exp-grid{display:grid;grid-template-columns:repeat(2,1fr);gap:18px}
    .exp-feature{display:flex;gap:10px;align-items:flex-start}
    .exp-feature .num{width:34px;height:34px;border-radius:8px;background:rgba(0,0,0,0.06);display:flex;align-items:center;justify-content:center;font-weight:800}

    /* stats (dark) */
    .stats-strip{padding:36px 0;background:linear-gradient(180deg,#050613,#07071a);color:var(--white)}
    .stats-row{display:flex;gap:12px;justify-content:center;max-width:var(--maxw);margin:0 auto}
    .stat{flex:1;min-width:140px;text-align:center;padding:18px}

    .stat strong{display:block;font-size:26px}
    .stat span{display:block;color:var(--muted);font-size:13px;margin-top:6px}

    /* Featured Project block (dark) */
    .project-section{padding:48px 0;background:linear-gradient(180deg,#050613,#080819)}
    .project-inner{max-width:var(--maxw);margin:0 auto;display:grid;grid-template-columns:360px 1fr;gap:28px;align-items:center}
    .project-img{background:#fff;padding:14px;border-radius:8px;height:420px;display:flex;align-items:center;justify-content:center}
    .project-img img{max-width:100%;max-height:100%;display:block}
    .project-cards{display:grid;grid-template-columns:1fr 1fr;gap:12px}

    /* architecture blue block */
    .block--blue{background:linear-gradient(180deg,#0b3a8a,#0b57c4);padding:48px 0}
    .arch-inner{max-width:var(--maxw);margin:0 auto;display:grid;grid-template-columns:1fr 320px;gap:28px;align-items:center;color:#fff}
    .arch-list ul{margin-left:18px;color:rgba(255,255,255,0.95)}

    /* awards strip */
    .awards-strip{padding:36px 0;background:linear-gradient(180deg,#060616,#0a0912)}
    .awards-inner{max-width:var(--maxw);margin:0 auto;display:grid;grid-template-columns:1fr 320px;gap:28px;align-items:start}
    .award-card{background:rgba(178,76,134,0.12);padding:12px;border-radius:10px;border:1px solid rgba(178,76,134,0.18);color:var(--white)}

    /* contact light-blue block */
    .block--lightblue{background:linear-gradient(180deg,#7fb1d0,#86b4d7);padding:40px 0;color:#082030}
    .contact-inner{max-width:var(--maxw);margin:0 auto;display:grid;grid-template-columns:1fr 360px;gap:20px;align-items:start}
    .contact-cards{display:grid;grid-template-columns:repeat(3,1fr);gap:12px}
    .contact-card{background:rgba(255,255,255,0.95);padding:12px;border-radius:8px;color:#082030;text-align:center}

    /* footer */
    footer{padding:28px 0;text-align:center;color:var(--muted)}

    /* responsive */
    @media (max-width:1100px){
      .two-col{grid-template-columns:1fr}
      .project-inner{grid-template-columns:1fr}
      .arch-inner{grid-template-columns:1fr}
      .awards-inner{grid-template-columns:1fr}
      .contact-inner{grid-template-columns:1fr}
      .expert-grid{grid-template-columns:1fr}
      .grid-3{grid-template-columns:1fr}
    }
    @media (max-width:700px){
      .profile-image{height:320px}
      .hero{padding:70px 0}
    }

    /* small decorative helper - centered section titles like Gamma */
    .section-title{font-weight:800;font-size:20px;margin-bottom:12px;text-align:center}
    .centered{display:flex;justify-content:center}
  </style>
</head>
<body>

  <!-- HERO -->
  <section class="hero" aria-label="hero">
    <div class="wrap">
      <div style="max-width:980px">
        <div style="opacity:0.98">
          <h1>Sanatan Swain</h1>
          <p class="sub">Software Engineer | Backend & Full-Stack Development Specialist</p>
          <div style="height:12px"></div>
          <div class="centered">
            <a class="btn" href="mailto:sanatanswain.dev@gmail.com">Get in Touch</a>
            <a class="btn ghost" href="https://www.linkedin.com/in/sanatan-swain-296040241/" target="_blank" style="background:transparent;border:1px solid rgba(255,255,255,0.06);margin-left:12px">View LinkedIn</a>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- PROFESSIONAL PROFILE (dark gradient) -->
  <section class="section block--dark" aria-label="professional profile">
    <div class="two-col">
      <div>
        <div style="max-width:760px;margin:0 auto">
          <h3 class="section-title" style="text-align:left;color:var(--white)">Professional Profile</h3>
          <div class="profile-cards">
            <div class="card">
              <h4>2.10+ YOE Experience</h4>
              <p>Backend and full-stack development with proven expertise in building scalable microservices and cloud deployments.</p>
            </div>
            <div class="card">
              <h4>Cloud & DevOps</h4>
              <p>Hands-on CI/CD implementation, AWS deployments, and high-performance system architecture.</p>
            </div>
            <div class="card" style="grid-column: span 2;">
              <h4>Secure Systems</h4>
              <p>Specializing in secure, high-performance systems with RESTful APIs and enterprise-grade solutions.</p>
            </div>
          </div>
        </div>
      </div>

      <div style="display:flex;align-items:center;justify-content:center">
        <div class="profile-image">
          <!-- replace src with your POS device screenshot if desired -->
          <img src="https://images.unsplash.com/photo-1587825140708-8f6f0b0f4f9a?w=900&q=80" alt="POS image">
        </div>
      </div>
    </div>
  </section>

  <!-- TECHNICAL EXPERTISE (maroon) -->
  <section class="section block--maroon" aria-label="technical expertise">
    <div style="max-width:var(--maxw);margin:0 auto;padding:18px">
      <h3 class="section-title" style="color:#fff">Technical Expertise</h3>
      <div class="expert-grid">
        <div>
          <h3>Core Technologies</h3>
          <ul>
            <li>Java, Spring Boot, Microservices</li>
            <li>RESTful APIs, Spring MVC</li>
            <li>JavaScript, NodeJS, HTML/CSS</li>
            <li>Hibernate, JSP, AJAX</li>
          </ul>
        </div>

        <div>
          <h3>Data & Cloud</h3>
          <ul>
            <li>MySQL, SQL, Oracle databases</li>
            <li>AWS cloud services</li>
            <li>Data structures & algorithms</li>
          </ul>
        </div>

        <div>
          <h3>Dev Tools & Methods</h3>
          <ul>
            <li>Git, JUnit, Postman, Swagger</li>
            <li>Jenkins CI/CD pipelines</li>
            <li>Agile, SDLC, System design</li>
          </ul>
        </div>
      </div>
    </div>
  </section>

  <!-- EDUCATION -->
  <section class="section edu-strip" aria-label="education">
    <div class="edu-grid">
      <div class="edu-card">
        <div class="num">1</div>
        <h4>Master of Computer Applications</h4>
        <div class="small-muted">Kalinga Institute of Industrial Technology (KIIT) — 2021–2023</div>
        <p class="small-muted" style="margin-top:6px">Advanced software engineering, system design, and enterprise application development.</p>
      </div>

      <div class="edu-card">
        <div class="num">2</div>
        <h4>Bachelor of Science in Mathematics</h4>
        <div class="small-muted">Gopabandhu Science College — 2017–2020</div>
        <p class="small-muted" style="margin-top:6px">Strong analytical foundation in mathematical principles and problem-solving.</p>
      </div>
    </div>
  </section>

  <!-- EXPERIENCE (pink block) -->
  <section class="section block--pink" aria-label="experience">
    <div class="exp-inner">
      <h3 style="font-weight:800;margin-bottom:6px">Professional Experience</h3>
      <div class="small-muted" style="margin-bottom:16px">Software Engineer at Financial Software and Systems Pvt. Ltd. — Feb 2023 – Present | Chennai, Tamil Nadu</div>

      <div class="exp-grid">
        <div>
          <div class="exp-feature">
            <div class="num">01</div>
            <div>
              <strong>FSS PoSability Engine Enhancement</strong>
              <p class="small-muted">Enhanced POS transaction engine and migrated Nomad HSM from XOR TDES SMK to AES, implementing HSM commands via APIs.</p>
            </div>
          </div>

          <div class="exp-feature" style="margin-top:14px">
            <div class="num">03</div>
            <div>
              <strong>Merchant Portal & Payment Gateway</strong>
              <p class="small-muted">Engineered POS Merchant Portal for 100+ merchants and secure multi-payment gateway, increasing payment options by 50%.</p>
            </div>
          </div>
        </div>

        <div>
          <div class="exp-feature">
            <div class="num">02</div>
            <div>
              <strong>Banking Solutions Development</strong>
              <p class="small-muted">Developed server-side solutions for ABSA & Nedbank; implemented ISO8583-based changes and webservice modules.</p>
            </div>
          </div>

          <div class="exp-feature" style="margin-top:14px">
            <div class="num">04</div>
            <div>
              <strong>Chargeback Module Development</strong>
              <p class="small-muted">Built Recon Dispute system's Chargeback module from scratch, improving dispute processing accuracy.</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- STATS (dark) -->
  <section class="section stats-strip" aria-label="achievements">
    <div style="max-width:var(--maxw);margin:0 auto;padding:6px 18px">
      <h3 class="section-title" style="color:var(--white)">Key Technical Achievements</h3>
      <div class="stats-row" style="margin-top:18px">
        <div class="stat">
          <strong>100+</strong>
          <span>Merchants Served</span>
        </div>
        <div class="stat">
          <strong>50%</strong>
          <span>Payment Options Increase</span>
        </div>
        <div class="stat">
          <strong>99.9%</strong>
          <span>System Uptime</span>
        </div>
        <div class="stat">
          <strong>&lt;200ms</strong>
          <span>API Response Time</span>
        </div>
      </div>
    </div>
  </section>

  <!-- FEATURED PROJECT (dark) -->
  <section class="section project-section" aria-label="featured project">
    <div class="project-inner">
      <div class="project-img">
        <img src="https://images.unsplash.com/photo-1545239351-1141bd82e8a6?w=900&q=80" alt="SalonEase screenshot">
      </div>

      <div>
        <h3 style="margin:0 0 6px">Featured Project: SalonEase</h3>
        <div class="small-muted">Online Salon Booking Platform</div>

        <div style="margin-top:12px" class="project-cards">
          <div class="card">
            <h4 style="margin:0 0 6px">Full-Stack Development</h4>
            <p class="small-muted">Responsive booking system with role-based auth (JWT, OAuth) and optimized backend APIs.</p>
          </div>
          <div class="card">
            <h4 style="margin:0 0 6px">Real-Time Booking Engine</h4>
            <p class="small-muted">Availability checks preventing double bookings; Stripe & Razorpay integration.</p>
          </div>

          <div class="card" style="grid-column:span 2;">
            <h4 style="margin:0 0 6px">Business Impact</h4>
            <p class="small-muted">Automated reminders reduced no-shows by 40% and admin dashboards improved management.</p>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- ARCHITECTURE BLUE BLOCK -->
  <section class="section block--blue" aria-label="architecture">
    <div class="arch-inner">
      <div class="arch-list">
        <h3 style="margin:0 0 8px">SalonEase Technical Architecture</h3>
        <div class="small-muted">Technology Stack</div>
        <ul style="margin-top:8px;color:#dcecff">
          <li>Backend: RESTful APIs with optimized caching</li>
          <li>Security: JWT & OAuth</li>
          <li>Payments: Stripe & Razorpay</li>
          <li>Deployment: AWS & Vercel</li>
        </ul>

        <div style="height:18px"></div>
        <div class="small-muted">Performance Metrics</div>
        <ul style="margin-top:8px;color:#dcecff">
          <li>99.9% uptime</li>
          <li>Sub-200ms API response times</li>
          <li>40% reduction in no-shows</li>
        </ul>
      </div>

      <div style="display:flex;align-items:center;justify-content:center">
        <div style="background:#fff;padding:18px;border-radius:10px">
          <img src="https://images.unsplash.com/photo-1531297484001-80022131f5a1?w=600&q=80" alt="architecture" style="max-width:220px;display:block">
        </div>
      </div>
    </div>
  </section>

  <!-- AWARDS -->
  <section class="section awards-strip" aria-label="awards">
    <div class="awards-inner">
      <div>
        <h3 class="section-title" style="text-align:left;color:var(--white)">Recognition & Awards</h3>

        <div style="display:grid;gap:12px;max-width:620px">
          <div class="award-card">
            <strong>Team of the Quarter</strong>
            <div class="small-muted" style="margin-top:6px">FSS Q1 & Q3 (2024–2025). Recognized for contributions to security & vulnerability fixes.</div>
          </div>

          <div class="award-card">
            <strong>Client Appreciation Award</strong>
            <div class="small-muted" style="margin-top:6px">For proactive resolution of critical production issues and improving client retention.</div>
          </div>
        </div>
      </div>

      <div style="display:flex;align-items:center;justify-content:center">
        <div style="background:#fff;padding:12px;border-radius:8px">
          <img src="0d94c0a1-2d4d-48d6-99c5-3eddaee9abac.png" 
          alt="Recognition & Awards Trophy" 
          style="max-width:240px;display:block;">
        </div>
      </div>
    </div>
  </section>

  <!-- CONTACT (light blue) -->
  <section class="section block--lightblue" aria-label="contact">
    <div class="contact-inner">
      <div>
        <h3 style="margin:0 0 8px">Let's Connect</h3>
        <p class="small-muted">Open to exciting opportunities in backend development, full-stack engineering, and cloud architecture. Let's build something amazing together!</p>

        <div class="contact-cards" style="margin-top:16px">
          <div class="contact-card">
            <div style="opacity:0.8">Location</div>
            <div style="font-weight:800;margin-top:6px">Chennai, Tamil Nadu, India</div>
          </div>

          <div class="contact-card">
            <div style="opacity:0.8">Email</div>
            <div style="font-weight:800;margin-top:6px">sanatanswain.dev@gmail.com</div>
          </div>

          <div class="contact-card">
            <div style="opacity:0.8">Phone</div>
            <div style="font-weight:800;margin-top:6px">+91 8118022344</div>
          </div>
        </div>

        <div style="margin-top:18px">
          <a class="btn" href="mailto:sanatanswain.dev@gmail.com">Contact Me</a>
          <a style="display:inline-block;margin-left:10px;padding:8px 12px;border-radius:8px;background:#dbeefc;color:#07293b;text-decoration:none;font-weight:700" href="Sanatan-Swain.pdf" download>Download Resume</a>
        </div>
      </div>

      <div>
        <div class="card" style="background:rgba(255,255,255,0.95);color:#082030">
          <form action="mailto:sanatanswain.dev@gmail.com" method="post" enctype="text/plain">
            <input name="name" placeholder="Your name" style="width:100%;padding:10px;border-radius:8px;border:1px solid rgba(0,0,0,0.06);margin-bottom:8px">
            <input name="email" placeholder="Your email" style="width:100%;padding:10px;border-radius:8px;border:1px solid rgba(0,0,0,0.06);margin-bottom:8px">
            <textarea name="message" rows="4" placeholder="Message" style="width:100%;padding:10px;border-radius:8px;border:1px solid rgba(0,0,0,0.06)"></textarea>
            <div style="margin-top:8px;display:flex;gap:8px">
              <button class="btn" type="submit">Send</button>
              <button type="reset" style="padding:10px;border-radius:8px;border:1px solid rgba(0,0,0,0.06);background:#fff;color:#082030">Reset</button>
            </div>
          </form>
        </div>
      </div>
    </div>
  </section>

  <footer class="wrap" aria-label="footer">
    <div style="text-align:center;color:var(--muted)">© <span id="year"></span> Sanatan Swain — Built with focus on payments</div>
  </footer>

  <script>
    document.getElementById('year').textContent = new Date().getFullYear();
    // lazy image replacements or future enhancements can go here
  </script>
</body>
</html>
