# Autovermietung-Probe-2
M3 comp Gand Car Rent 
<!doctype html>
<html lang="de">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Grand Car Rent — Rostock & Warnemünde | Autovermietung</title>
  <meta name="description" content="Grand Car Rent — Autovermietung in Rostock und Warnemünde. Große Auswahl an Fahrzeugen, fairen Preisen und persönlichem Service." />
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&display=swap" rel="stylesheet">
  <style>
    :root {
      --max-width: 1100px;
      --accent: #0b74da;
      --muted: #6b7280;
      --bg: #f7f8fa;
      --card: #ffffff;
      --radius: 10px;
      --gap: 1.25rem;
      font-family: 'Inter', system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
      color-scheme: light;
    }
    * { box-sizing: border-box; }
    html,body { height: 100%; margin:0; background:var(--bg); color:#111827; }
    .container { max-width:var(--max-width); margin:0 auto; padding:1.5rem; }
    .site-header { background:white; box-shadow:0 2px 6px rgba(10,10,10,0.04); position:sticky; top:0; z-index:50; }
    .header-inner { display:flex; align-items:center; justify-content:space-between; gap:1rem; }
    .brand { font-weight:700; color:var(--accent); text-decoration:none; font-size:1.2rem; }
    .main-nav { display:flex; gap:0.75rem; align-items:center; }
    .main-nav a { text-decoration:none; color:var(--muted); padding:0.35rem 0.45rem; }
    .btn { border:1px solid transparent; padding:0.6rem 0.9rem; border-radius:8px; cursor:pointer; background:transparent; font-weight:600; }
    .btn.primary { background:var(--accent); color:white; border-color:var(--accent); }
    .btn.outline { border-color:#d1d5db; color:#111827; background:white; }
    .menu-toggle { display:none; background:transparent; border:0; font-size:1.25rem; }
    .hero { padding:3rem 0; }
    .hero-inner { display:flex; gap:2rem; align-items:center; }
    .hero-copy { flex:1; }
    .hero-copy h1 { font-size:2rem; margin:0 0 0.5rem 0; }
    .hero-copy p { color:var(--muted); margin:0 0 1rem 0; }
    .hero-image img { width:100%; max-width:540px; border-radius:12px; box-shadow:0 6px 30px rgba(16,24,40,0.06); }
    .features { display:flex; gap:1rem; margin-top:1rem; }
    .feature { background:var(--card); padding:1rem; border-radius:10px; flex:1; box-shadow:0 2px 8px rgba(16,24,40,0.04); }
    .fleet { padding:2rem 0; }
    .fleet-grid { display:grid; grid-template-columns:repeat(3,1fr); gap:1rem; margin-top:1rem; }
    .fleet-card { background:var(--card); border-radius:10px; overflow:hidden; box-shadow:0 6px 20px rgba(16,24,40,0.04); display:flex; flex-direction:column; }
    .fleet-card img { width:100%; height:220px; object-fit:cover; }
    .fleet-body { padding:0.9rem; display:flex; gap:0.5rem; flex-direction:column; }
    .fleet-meta { display:flex; justify-content:space-between; align-items:center; margin-top:0.5rem; }
    .price { font-weight:700; color:var(--accent); }
    .about, .contact { padding:2rem 0; }
    .contact-grid { display:grid; grid-template-columns:1fr 320px; gap:1.25rem; align-items:start; }
    .contact-form input, .contact-form textarea, .booking-form input, .booking-form select {
      width:100%; padding:0.6rem; border:1px solid #e6e7eb; border-radius:8px; margin-bottom:0.6rem;
    }
    .small { color:var(--muted); font-size:0.9rem; margin-top:0.6rem; }
    .site-footer { padding:1rem 0; background:white; margin-top:2rem; }
    .footer-inner { display:flex; gap:1rem; justify-content:space-between; align-items:center; }
    .modal { position:fixed; inset:0; display:grid; place-items:center; z-index:100; }
    .modal-panel { background:white; width:100%; max-width:720px; border-radius:12px; padding:1.25rem; box-shadow:0 12px 40px rgba(2,6,23,0.3); transform:translateY(0); }
    .modal-close { float:right; background:transparent; border:0; font-size:1.1rem; cursor:pointer; }
    .overlay { position:fixed; inset:0; background:rgba(2,6,23,0.45); z-index:90; }
    .booking-actions { display:flex; gap:0.6rem; margin-top:0.6rem; }
    @media (max-width: 900px) {
      .hero-inner { flex-direction:column-reverse; text-align:center; }
      .fleet-grid { grid-template-columns:repeat(2,1fr); }
      .contact-grid { grid-template-columns:1fr; }
    }
    @media (max-width: 600px) {
      .fleet-grid { grid-template-columns:1fr; }
      .main-nav a { display:none; }
      .menu-toggle { display:block; }
      .header-inner { gap:0.5rem; }
    }
  </style>
</head>
<body>
  <header class="site-header">
    <div class="container header-inner">
      <a class="brand" href="#">Grand Car Rent</a>
      <nav class="main-nav" aria-label="Hauptnavigation">
        <a href="#home">Home</a>
        <a href="#fleet">Flotte</a>
        <a href="#about">Über uns</a>
        <a href="#contact">Kontakt</a>
        <button id="bookNowBtn" class="btn primary">Jetzt buchen</button>
      </nav>
      <button class="menu-toggle" aria-label="Menü" aria-expanded="false">☰</button>
    </div>
  </header>

  <main>
    <section id="home" class="hero">
      <div class="container hero-inner">
        <div class="hero-copy">
          <h1>Grand Car Rent — Autovermietung in Rostock & Warnemünde</h1>
          <p>Top-gepflegte Fahrzeuge, persönliche Betreuung vor Ort in Mecklenburg‑Vorpommern. Kurz- und Langzeitmieten, Firmenkonditionen und Urlaubsangebote.</p>
          <div class="hero-cta">
            <button id="heroBook" class="btn primary">Fahrzeug buchen</button>
            <a href="#fleet" class="btn outline">Zur Flotte</a>
          </div>
        </div>
        <div class="hero-image" aria-hidden="true">
          <img src="https://via.placeholder.com/800x480?text=Grand+Car+Rent+Rostock" alt="Grand Car Rent in Rostock">
        </div>
      </div>
    </section>

    <section class="features container">
      <div class="feature">
        <h3>Standort</h3>
        <p>Stationen in Rostock und Warnemünde – Abholung am Hafen oder Bahnhof möglich.</p>
      </div>
      <div class="feature">
        <h3>Faire Preise</h3>
        <p>Keine versteckten Gebühren. Transparente Tages‑ und Wochenpreise.</p>
      </div>
      <div class="feature">
        <h3>Persönlicher Service</h3>
        <p>Lokales Team in MV für schnellen Support und flexible Abwicklung.</p>
      </div>
    </section>

    <section id="fleet" class="fleet container">
      <h2>Unsere Flotte</h2>
      <p class="lead">Vom City-Flitzer bis zur sportlichen Performance — hier einige Highlights unserer aktuellen Fahrzeuge.</p>
      <div id="fleetGrid" class="fleet-grid" aria-live="polite"></div>
    </section>

    <section id="about" class="about container">
      <h2>Über Grand Car Rent</h2>
      <p>Grand Car Rent ist deine lokale Autovermietung in Rostock und Warnemünde. Wir kombinieren moderne Fahrzeuge mit persönlichem Service — ideal für Urlauber, Geschäftsreisende und Einheimische.</p>
      <ul>
        <li>Abholung in Rostock Hauptbahnhof, Warnemünde Hafen oder nach Vereinbarung</li>
        <li>Flexible Mietzeiten: stunden-, tages- oder monatsweise</li>
        <li>Optionale Versicherungen und Zusatzpakete</li>
      </ul>
    </section>

    <section id="contact" class="contact container">
      <h2>Kontakt & Öffnungszeiten</h2>
      <div class="contact-grid">
        <form id="contactForm" class="contact-form" novalidate>
          <label for="name">Name</label>
          <input id="name" name="name" required placeholder="Vor- und Nachname">

          <label for="email">E-Mail</label>
          <input id="email" type="email" name="email" required placeholder="name@beispiel.de">

          <label for="message">Nachricht</label>
          <textarea id="message" name="message" rows="5" required placeholder="Wie können wir helfen?"></textarea>

          <button type="submit" class="btn primary">Nachricht senden</button>
        </form>

        <div class="contact-info">
          <h3>Standorte</h3>
          <p>Rostock & Warnemünde<br>Mecklenburg‑Vorpommern, Deutschland</p>

          <h3>Öffnungszeiten</h3>
          <p>Mo–Fr: 08:00–18:00<br>Sa: 09:00–13:00</p>

          <h3>Telefon</h3>
          <p><a href="tel:+493811234567">+49 381 1234567</a> (Demo)</p>

          <h3>E‑Mail</h3>
          <p><a href="mailto:info@grandcarrent.de">info@grandcarrent.de</a></p>
        </div>
      </div>
    </section>
  </main>

  <footer class="site-footer">
    <div class="container footer-inner">
      <p>© <span id="year"></span> Grand Car Rent — Rostock & Warnemünde. Alle Rechte vorbehalten.</p>
      <nav class="footer-nav" aria-label="Footer Navigation">
        <a href="#privacy">Datenschutz</a>
        <a href="#terms">AGB</a>
      </nav>
    </div>
  </footer>

  <!-- Booking Modal -->
  <div id="bookingModal" class="modal" role="dialog" aria-hidden="true" style="display:none;">
    <div class="modal-panel" role="document">
      <button class="modal-close" aria-label="Schließen">✕</button>
      <h2 id="bookingTitle">Fahrzeug buchen</h2>
      <form id="bookingForm" class="booking-form" novalidate>
        <label for="carSelect">Fahrzeug</label>
        <select id="carSelect" name="car" required></select>

        <label for="pickupDate">Abholung</label>
        <input id="pickupDate" name="pickupDate" type="date" required>

        <label for="returnDate">Rückgabe</label>
        <input id="returnDate" name="returnDate" type="date" required>

        <label for="driverAge">Alter des Fahrers</label>
        <input id="driverAge" name="driverAge" type="number" min="18" max="120" required placeholder="z. B. 30">

        <label for="extras">Extras</label>
        <div class="checkboxes">
          <label><input type="checkbox" name="extras" value="gps"> GPS</label>
          <label><input type="checkbox" name="extras" value="child"> Kindersitz</label>
          <label><input type="checkbox" name="extras" value="roof"> Dachträger</label>
        </div>

        <div class="booking-actions">
          <button type="submit" class="btn primary">Anfrage senden</button>
          <button type="button" class="btn outline modal-cancel">Abbrechen</button>
        </div>
        <p class="small">Hinweis: Diese Demo sendet keine echten Buchungen. Ersetze die Formularaktion durch deine Server-API.</p>
      </form>
    </div>
  </div>
  <div id="overlay" class="overlay" hidden style="display:none;"></div>

  <script>
    document.addEventListener('DOMContentLoaded', () => {
      document.getElementById('year').textContent = new Date().getFullYear();

      // Flottendaten (angepasst mit BMW M3 Competition)
      const cars = [
        {
          id: 'bmw-m3c',
          name: 'BMW M3 Competition',
          type: 'Performance / Sport',
          seats: 5,
          pricePerDay: 349,
          img: 'https://via.placeholder.com/1200x700?text=BMW+M3+Competition',
          specs: `3,0‑Liter‑Sechszylinder‑Reihenmotor mit TwinPower Turbo‑Technologie, Leistung: 375 kW (510 PS), maximales Drehmoment: 650 Nm. Beschleunigung 0–100 km/h: 3,9 s (Hinterradantriebsversion). Elektronisch abgeregelte Höchstgeschwindigkeit: 250 km/h. 8‑Gang Steptronic Automatik mit Drivelogic.`
        },
        { id:'c1', name:'VW Golf', type:'Economy', seats:5, pricePerDay:49, img:'https://via.placeholder.com/800x480?text=VW+Golf' },
        { id:'c2', name:'Toyota RAV4', type:'SUV', seats:5, pricePerDay:69, img:'https://via.placeholder.com/800x480?text=Toyota+RAV4' }
      ];

      const fleetGrid = document.getElementById('fleetGrid');
      const carSelect = document.getElementById('carSelect');

      function formatCurrency(n){
        return new Intl.NumberFormat('de-DE',{style:'currency',currency:'EUR',maximumFractionDigits:0}).format(n);
      }

      function renderFleet(){
        fleetGrid.innerHTML = '';
        cars.forEach(car => {
          const card = document.createElement('article');
          card.className = 'fleet-card';
          card.innerHTML = `\n            <img src="${car.img}" alt="${car.name}">\n            <div class="fleet-body">\n              <div>\n                <strong>${car.name}</strong>\n                <div class="muted">${car.type} • ${car.seats} Sitze</div>\n              </div>\n              <div class="fleet-meta">\n                <div class="price">${formatCurrency(car.pricePerDay)}/Tag</div>\n                <div>\n                  <button class="btn outline btn-details" data-id="${car.id}">Details</button>\n                  <button class="btn primary btn-book" data-id="${car.id}">Buchen</button>\n                </div>\n              </div>\n            </div>\n          `;
          fleetGrid.appendChild(card);
        });
      }

      function populateSelect(){
        carSelect.innerHTML = '<option value="">-- Fahrzeug wählen --</option>';
        cars.forEach(car => {
          const opt = document.createElement('option');
          opt.value = car.id;
          opt.textContent = `${car.name} — ${formatCurrency(car.pricePerDay)}/Tag`;
          carSelect.appendChild(opt);
        });
      }

      renderFleet();
      populateSelect();

      // Modal-Steuerung
      const modal = document.getElementById('bookingModal');
      const overlay = document.getElementById('overlay');
      const openBtns = document.querySelectorAll('#bookNowBtn, #heroBook, .btn-book');
      const closeBtns = document.querySelectorAll('.modal-close, .modal-cancel');

      function openModal(prefillCarId){
        modal.setAttribute('aria-hidden','false');
        overlay.hidden = false; overlay.style.display = 'block'; modal.style.display = 'grid';
        if(prefillCarId) carSelect.value = prefillCarId;
      }
      function closeModal(){
        modal.setAttribute('aria-hidden','true');
        overlay.hidden = true; overlay.style.display = 'none'; modal.style.display = 'none';
      }

      openBtns.forEach(btn => btn.addEventListener('click', (e)=>{
        const id = e.currentTarget.dataset && e.currentTarget.dataset.id;
        openModal(id || null);
      }));
      closeBtns.forEach(b => b.addEventListener('click', closeModal));
      overlay.addEventListener('click', closeModal);

      // Details-Button: zeigt Modal mit Specs
      document.addEventListener('click', (e) => {
        if(e.target.matches('.btn-details')){
          const id = e.target.dataset.id;
          const car = cars.find(c => c.id === id);
          if(car){
            // einfache Detailanzeige
            const detailText = `${car.name}\nTyp: ${car.type}\nSitze: ${car.seats}\nPreis: ${formatCurrency(car.pricePerDay)}/Tag\n\n${car.specs || ''}`;
            alert(detailText);
          }
        }
        if(e.target.matches('.btn-book')){
          openModal(e.target.dataset.id);
        }
      });

      // Kontaktformular (Demo)
      const contactForm = document.getElementById('contactForm');
      contactForm.addEventListener('submit', (e) =>{
        e.preventDefault();
        if(!contactForm.checkValidity()){
          alert('Bitte fülle alle Pflichtfelder korrekt aus.');
          return;
        }
        alert('Danke! Ihre Nachricht wurde (Demo) empfangen.');
        contactForm.reset();
      });

      // Buchungsformular
      const bookingForm = document.getElementById('bookingForm');
      bookingForm.addEventListener('submit', (e)=>{
        e.preventDefault();
        if(!bookingForm.checkValidity()){
          alert('Bitte fülle alle Pflichtfelder korrekt aus.');
          return;
        }
        const data = new FormData(bookingForm);
        const payload = {
          carId: data.get('car'),
          pickupDate: data.get('pickupDate'),
          returnDate: data.get('returnDate'),
          driverAge: data.get('driverAge'),
          extras: data.getAll('extras')
        };
        if(new Date(payload.returnDate) < new Date(payload.pickupDate)){
          alert('Rückgabedatum darf nicht vor Abholdatum liegen.');
          return;
        }
        if(parseInt(payload.driverAge,10) < 18){
          alert('Fahrer muss mindestens 18 Jahre alt sein.');
          return;
        }
        const car = cars.find(c => c.id === payload.carId);
        const days = Math.ceil((new Date(payload.returnDate) - new Date(payload.pickupDate)) / (1000*60*60*24)) || 1;
        const base = (car ? car.pricePerDay : 0) * days;
        alert(`Buchungsanfrage:\nFahrzeug: ${car ? car.name : '—'}\nZeitraum: ${payload.pickupDate} → ${payload.returnDate} (${days} Tage)\nBasispreis: ${formatCurrency(base)}\nExtras: ${payload.extras.join(', ') || 'keine'}\n\n(Demo) Wir senden diese Anfrage an das Backend.`);
        bookingForm.reset();
        closeModal();
      });

      // Mobile menu toggle
      const menuToggle = document.querySelector('.menu-toggle');
      const mainNav = document.querySelector('.main-nav');
      menuToggle?.addEventListener('click', ()=>{
        const expanded = menuToggle.getAttribute('aria-expanded') === 'true';
        menuToggle.setAttribute('aria-expanded', (!expanded).toString());
        if(!expanded) mainNav.style.display = 'flex'; else mainNav.style.display = '';
      });

    });
  </script>
</body>
</html>
