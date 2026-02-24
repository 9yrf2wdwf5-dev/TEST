<!doctype html>
<html lang="cs">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>GOATA Lab by Dominika Černá</title>
  <meta name="description" content="GOATA instruktorka, trenérka a průvodkyně. Praha i online. Posouzení pohybu, individuální a skupinové tréninky. Přirozený pohyb bez bolesti a bez zranění." />

  <style>
    :root{
      /* khaki + béžová (světlá, vlídná, seriózní) */
      --bg:#fbf5e8;
      --card:rgba(255,255,255,.80);
      --text:#1f2430;
      --muted:#5b6474;
      --line:rgba(31,36,48,.10);

      --accent:#6f8f52;      /* khaki zelená */
      --accent2:#e7d8bf;     /* béžová */
      --shadow:0 10px 30px rgba(31,36,48,.08);
      --radius:18px;
      --max:1100px;
    }

    *{box-sizing:border-box}
    html{scroll-behavior:smooth}
    body{
      margin:0;
      font-family: ui-sans-serif, system-ui, -apple-system, Segoe UI, Roboto, Arial, "Noto Sans", "Liberation Sans", sans-serif;
      color:var(--text);
      line-height:1.65;
      background:
        radial-gradient(900px 520px at 12% 10%, rgba(231,216,191,.55), transparent 62%),
        radial-gradient(900px 520px at 88% 14%, rgba(111,143,82,.18), transparent 60%),
        radial-gradient(900px 520px at 60% 92%, rgba(111,143,82,.10), transparent 60%),
        var(--bg);
    }
    a{color:inherit}

    .wrap{max-width:var(--max); margin:0 auto; padding:26px 18px 84px}

    .topbar{
      display:flex; align-items:center; justify-content:space-between;
      gap:12px;
      position:sticky; top:0;
      padding:14px 0;
      backdrop-filter: blur(8px);
      z-index:10;
    }

    .brand{display:flex; align-items:center; gap:10px; text-decoration:none}
    .logo{
      width:34px; height:34px; border-radius:10px;
      background:linear-gradient(135deg, var(--accent2), rgba(111,143,82,.35));
      border:1px solid var(--line);
      box-shadow:0 6px 16px rgba(31,36,48,.07);
    }
    .brand b{font-weight:850}
    .brand small{display:block; color:var(--muted); margin-top:2px; font-size:12px}

    .nav{display:flex; gap:10px; flex-wrap:wrap; font-size:14px}
    .nav a{
      text-decoration:none;
      padding:8px 10px;
      border-radius:999px;
      border:1px solid transparent;
      color:var(--muted);
    }
    .nav a:hover{border-color:var(--line); background:rgba(255,255,255,.55); color:var(--text)}

    .card{
      background:var(--card);
      border:1px solid var(--line);
      border-radius:var(--radius);
      box-shadow:var(--shadow);
    }

    .hero{
      margin-top:10px;
      display:grid;
      grid-template-columns:1.25fr .75fr;
      gap:18px;
      align-items:stretch;
    }
    @media (max-width:920px){
      .hero{grid-template-columns:1fr}
      .topbar{position:static}
    }

    .hero-left{padding:28px}
    .kicker{
      display:inline-flex; align-items:center; gap:8px;
      font-size:13px; color:var(--muted);
      padding:8px 12px;
      border:1px solid var(--line);
      border-radius:999px;
      background:rgba(255,255,255,.55);
    }
    .dot{
      width:8px; height:8px; border-radius:99px;
      background:var(--accent);
      box-shadow:0 0 0 6px rgba(111,143,82,.16);
    }

    h1{margin:14px 0 10px; font-size:40px; letter-spacing:-.02em; line-height:1.12}
    @media (max-width:520px){h1{font-size:32px}}
    .lead{color:var(--muted); font-size:16px; margin:0 0 18px}

    .cta{display:flex; gap:10px; flex-wrap:wrap; margin-top:18px}
    .btn{
      display:inline-flex; align-items:center; justify-content:center;
      padding:10px 14px;
      border-radius:12px;
      border:1px solid var(--line);
      background:rgba(255,255,255,.65);
      text-decoration:none;
      font-weight:760;
      font-size:14px;
      cursor:pointer;
    }
    .btn.primary{
      border-color:rgba(111,143,82,.35);
      background:linear-gradient(135deg, rgba(231,216,191,.65), rgba(111,143,82,.20));
    }

    .benefits{
      margin-top:14px;
      display:grid;
      grid-template-columns:repeat(2, minmax(0,1fr));
      gap:10px;
    }
    @media (max-width:760px){.benefits{grid-template-columns:1fr}}
    .benefit{
      padding:12px 14px;
      border:1px solid var(--line);
      border-radius:14px;
      background:rgba(255,255,255,.55);
      font-size:14px;
      color:var(--muted);
    }
    .benefit b{color:var(--text)}

    .quote{
      margin:10px 0 0;
      padding-left:12px;
      border-left:3px solid rgba(111,143,82,.60);
      color:var(--muted);
      font-size:14px;
    }

    .meta{display:grid; gap:10px; padding:22px}
    .meta .item{
      padding:14px;
      border:1px solid var(--line);
      border-radius:14px;
      background:rgba(255,255,255,.55);
    }
    .meta h3{
      margin:0 0 4px;
      font-size:13px;
      color:var(--muted);
      font-weight:850;
      letter-spacing:.02em;
      text-transform:uppercase;
    }
    .meta p{margin:0; font-size:14px}

    section{margin-top:18px}
    .section{padding:22px}
    .section h2{margin:0 0 10px; font-size:18px; letter-spacing:-.01em}

    .two{display:grid; grid-template-columns:1fr 1fr; gap:12px; margin-top:12px}
    @media (max-width:920px){.two{grid-template-columns:1fr}}
    .grid3{display:grid; grid-template-columns:repeat(3,1fr); gap:12px; margin-top:12px}
    @media (max-width:920px){.grid3{grid-template-columns:1fr}}

    .feature{
      padding:16px;
      border:1px solid var(--line);
      border-radius:14px;
      background:rgba(255,255,255,.55);
    }
    .feature b{display:block; margin-bottom:6px}
    .feature p{margin:0; color:var(--muted); font-size:14px}

    ul{margin:10px 0 0 18px; color:var(--muted)}
    li{margin:6px 0}

    .price{display:flex; align-items:baseline; justify-content:space-between; gap:14px}
    .price strong{font-size:16px}
    .price span{font-size:13px; color:var(--muted)}

    .contact{display:grid; grid-template-columns:1.2fr .8fr; gap:12px; margin-top:12px}
    @media (max-width:920px){.contact{grid-template-columns:1fr}}
    form{display:grid; gap:10px; margin-top:10px}
    label{font-size:13px; color:var(--muted)}
    input,textarea{
      width:100%;
      padding:11px 12px;
      border-radius:12px;
      border:1px solid var(--line);
      background:rgba(255,255,255,.72);
      font:inherit;
    }
    textarea{min-height:110px; resize:vertical}
    .small{font-size:12px; color:var(--muted)}

    .maplink{display:inline-block; margin-top:10px; font-size:14px; color:var(--muted)}
    .maplink:hover{color:var(--text)}

    footer{
      margin-top:22px;
      padding-top:18px;
      border-top:1px solid var(--line);
      color:var(--muted);
      font-size:13px;
      display:flex; justify-content:space-between; gap:12px; flex-wrap:wrap;
    }
  </style>
</head>

<body>
  <div class="wrap">
    <div class="topbar">
      <a class="brand" href="#top">
        <span class="logo" aria-hidden="true"></span>
        <div>
          <b>GOATA Lab</b>
          <small>by Dominika Černá</small>
        </div>
      </a>

      <nav class="nav" aria-label="Navigace">
        <a href="#co-je-goata">Co je GOATA</a>
        <a href="#o-mne">O mně</a>
        <a href="#nabidka">Nabídka</a>
        <a href="#cenik">Ceník</a>
        <a href="#misto">Kde</a>
        <a href="#kontakt">Objednat</a>
      </nav>
    </div>

    <main id="top" class="hero">
      <div class="card hero-left">
        <div class="kicker"><span class="dot"></span> observační metodologie • dekomprese • recode</div>

        <h1>GOATA: návrat k přirozenému pohybu bez bolesti a bez zranění</h1>

        <p class="lead">
          Observační metodologie, která pracuje s tělem jako s celkem. Pomáhá vytvářet dekompresi, přepisovat pohybové vzorce
          a budovat mobilitu i sílu zároveň.
        </p>

        <div class="cta">
          <a class="btn primary" href="#kontakt">Objednat konzultaci</a>
          <a class="btn" href="#co-je-goata">Jak GOATA funguje</a>
        </div>

        <div class="benefits">
          <div class="benefit"><b>Dekomprese:</b> víc prostoru v těle, lepší pohyb</div>
          <div class="benefit"><b>Přepis pohybových vzorců:</b> méně kompenzací, více stability</div>
          <div class="benefit"><b>Mobilita + síla:</b> v jednom (celé tělo, ne izolace)</div>
          <div class="benefit"><b>Napříč věkem:</b> pokud jste připraveni být konzistentní</div>
        </div>

        <p class="quote">GOATA je proces. Ne rychlá oprava bez konzistence.</p>
      </div>

      <aside class="card meta" aria-label="Rychlé info">
        <div class="item">
          <h3>Lokalita</h3>
          <p>Praha • online</p>
        </div>
        <div class="item">
          <h3>Studio</h3>
          <p>Patočkova 83<br>Studio Barre Prague</p>
        </div>
        <div class="item">
          <h3>Kontakt</h3>
          <p>
            <a href="mailto:Dominika.c.9@icloud.com">Dominika.c.9@icloud.com</a><br>
            <a href="tel:+420607603554">+420 607 603 554</a>
          </p>
        </div>
      </aside>
    </main>

    <section id="co-je-goata" class="card section">
      <h2>Co je GOATA</h2>

      <div class="two">
        <div>
          <p class="lead" style="margin:0">
            GOATA je observační metodologie pohybu, která vznikla na základě dlouhodobého pozorování lidí a skupin,
            u kterých se přirozeně a opakovaně potvrzuje vysoká odolnost těla, kvalitní pohyb a nízká míra zranění.
            Metoda vychází z principu, že tělo je jeden celek – a proto se i trénink zaměřuje na celek, ne na izolované svaly.
          </p>
          <p class="lead" style="margin:12px 0 0">
            GOATA pracuje s tím, jak se tělo hýbe jako systém: jak nese váhu, jak se umí „poskládat“ do stabilních tvarů,
            jak umí přenášet sílu a jak se dokáže přirozeně regenerovat.
          </p>
        </div>

        <div class="feature">
          <b>Princip: tělo jako celek, tvary jako nástroj</b>
          <p>GOATA „skládá“ tělo do konkrétních tvarů, ve kterých cíleně:</p>
          <ul>
            <li>vytváří dekompresi (prostor v těle),</li>
            <li>napravuje a přepisuje pohybové vzorce,</li>
            <li>rozvíjí zároveň mobilitu i sílu (nikoliv jako oddělené věci).</li>
          </ul>
        </div>
      </div>

      <div class="grid3">
        <div class="feature">
          <b>Z čeho GOATA vychází (4 skupiny pozorování)</b>
          <ul>
            <li>domorodé kmeny v přirozeném prostředí,</li>
            <li>malé děti a jejich přirozený motorický vývoj,</li>
            <li>profesionální sportovci s dlouhou zdravou kariérou,</li>
            <li>aktivní lidé 70+ bez výrazných bolestí a zranění.</li>
          </ul>
        </div>

        <div class="feature">
          <b>Jak může vypadat trénink</b>
          <ul>
            <li><b>Rehabilitačně</b> – snížení nebo odstranění bolesti a návrat k pohybu.</li>
            <li><b>Atleticky</b> – zlepšení výkonu, rychlosti, odolnosti a stability.</li>
            <li><b>Kompensačně</b> – vyrovnání jednostranného sportu nebo sedavého života.</li>
          </ul>
        </div>

        <div class="feature">
          <b>ATA „cílovou čáru“</b>
          <p>
            Když projdete procesem změny zpět k přirozenosti, tělo si dokáže získané kvality udržet díky běžným věcem jako je chůze,
            sezení na zemi a každodenní pohyb.
          </p>
          <p style="margin-top:10px; color:var(--muted); font-size:14px">Neztratíte formu – stanete se jí.</p>
        </div>
      </div>

      <div class="two">
        <div class="feature">
          <b>Proč je důležitá dekomprese a „návrat k přirozenosti“</b>
          <p>
            Moderní životní styl často vede tělo do komprese – zjednodušeně do stavu, kdy uvnitř těla „chybí prostor“.
            Tělo se postupně zkracuje, tuhne, zhoršuje se práce kloubů a mění se způsob přenosu váhy.
          </p>
          <p style="margin-top:10px; color:var(--muted); font-size:14px">
            GOATA se snaží tento vývoj zastavit, ideálně otočit a dostat tělo zpět do stavu, kdy se hýbe efektivně a dlouhodobě udržitelně.
          </p>
        </div>

        <div class="feature">
          <b>Pro koho GOATA je (a pro koho ne)</b>
          <p>
            GOATA může fungovat pro široké spektrum lidí – nezáleží, jestli je Vám 17 nebo 70. Zároveň platí:
            GOATA je pro každého, ale není pro všechny.
          </p>
          <p style="margin-top:10px; color:var(--muted); font-size:14px">
            Nenabízí rychlé opravy bez konzistence. Je to proces a životní styl, který vyžaduje pravidelnost, trpělivost
            a ochotu měnit to, jak se hýbete i mimo trénink.
          </p>
        </div>
      </div>
    </section>

    <section id="o-mne" class="card section">
      <h2>O mně</h2>

      <div class="two">
        <div>
          <p class="lead" style="margin:0">
            Jmenuji se Dominika Černá. Jsem GOATA instruktorka / trenérka / průvodkyně a pomáhám lidem na cestě „recode“ – návratu těla
            k přirozenému pohybu.
          </p>
          <p class="lead" style="margin:12px 0 0">
            Pracuji s lidmi, kteří chtějí žít bez bolesti pohybového aparátu, zlepšit sportovní výkon nebo předcházet zraněním
            (tanec i vrcholové sporty).
          </p>
          <p class="small" style="margin:12px 0 0">
            Až budeš chtít, doplníme sem tvůj příběh, certifikace a fotku.
          </p>
        </div>

        <div class="feature">
          <b>Co můžete očekávat</b>
          <ul>
            <li>pozorování pohybu (včetně slow motion videa),</li>
            <li>přepis stereotypů na odolnější varianty,</li>
            <li>edukaci a plán vlastní praxe,</li>
            <li>GOATA jako životní styl, ne jen „lekci“.</li>
          </ul>
        </div>
      </div>
    </section>

    <section id="nabidka" class="card section">
      <h2>Nabídka</h2>
      <p class="lead" style="margin:0">
        Začínáme úvodním posouzením a postupně přepisujeme pohybové vzorce – tak, aby tělo zvládalo zátěž odolněji.
      </p>

      <div class="grid3">
        <div class="feature">
          <b>Úvodní posouzení pohybu (slow motion video)</b>
          <p>Podíváme se, jak tělo funguje v základních vzorcích pohybu. Naučíte se první cviky a dostanete jasný plán dalšího postupu.</p>
        </div>

        <div class="feature">
          <b>Individuální tréninky</b>
          <p>Přepisování zajetých stereotypů na nové, odolnější. Důraz na detail, techniku a přenos do praxe (běžný den / sport).</p>
        </div>

        <div class="feature">
          <b>Pohybová praxe & edukace</b>
          <p>Nezbytnou součástí je vlastní praxe. Součástí je edukace o globálních zákonech, kterými se GOATA řídí.</p>
        </div>
      </div>
    </section>

    <section id="cenik" class="card section">
      <h2>Ceník</h2>

      <div class="two">
        <div class="feature">
          <div class="price">
            <strong>Individuální lekce</strong>
            <span>60 min (dle domluvy)</span>
          </div>
          <p style="margin:8px 0 0; color:var(--muted)">Cena: <b style="color:var(--text)">1 700 Kč</b></p>
        </div>

        <div class="feature">
          <div class="price">
            <strong>Skupinový trénink</strong>
            <span>lekce ve studiu</span>
          </div>
          <p style="margin:8px 0 0; color:var(--muted)">Cena: <b style="color:var(--text)">450 Kč</b></p>
        </div>
      </div>

      <p class="small" style="margin:12px 0 0">
        Úvodní posouzení pohybu: cenu a délku potvrdím podle domluvy (forma, čas, potřeby).
      </p>
    </section>

    <section id="misto" class="card section">
      <h2>Kde trénujeme</h2>

      <div class="two">
        <div class="feature">
          <b>Praha</b>
          <p>Patočkova 83, Studio Barre Prague</p>
          <a class="maplink" target="_blank" rel="noreferrer"
             href="https://www.google.com/maps/search/?api=1&query=Pato%C4%8Dkova%2083%2C%20Praha%2C%20Studio%20Barre%20Prague">
            Otevřít v Google Maps →
          </a>
        </div>

        <div class="feature">
          <b>Online</b>
          <p>Konzultace, posouzení i trénink mohou proběhnout také online. Řeknu Vám dopředu, co budete potřebovat.</p>
        </div>
      </div>
    </section>

    <section id="kontakt" class="card section">
      <h2>Objednat konzultaci / úvodní posouzení</h2>
      <p class="lead" style="margin:0">
        Vyplňte prosím krátký formulář. Ozvu se Vám s návrhem termínu a dalším postupem.
      </p>

      <div class="contact">
        <div class="feature">
          <b>Registrační formulář</b>

          <!-- ZATÍM DEMO (neodesílá). Až budeš chtít, napojíme zdarma na Formspree. -->
          <form onsubmit="return demoSubmit(event)">
            <div>
              <label for="name">Jméno</label>
              <input id="name" name="jmeno" autocomplete="name" placeholder="Vaše jméno" required />
            </div>

            <div>
              <label for="phone">Telefon</label>
              <input id="phone" name="telefon" inputmode="tel" autocomplete="tel" placeholder="+420…" required />
            </div>

            <div>
              <label for="why">Proč chcete přijít</label>
              <textarea id="why" name="proc_chci_prijit" placeholder="Co chcete zlepšit / vyřešit?" required></textarea>
            </div>

            <div>
              <label for="history">Pohybová minulost</label>
              <textarea id="history" name="pohybova_minulost" placeholder="Sport, tanec, tréninková rutina, práce…"></textarea>
            </div>

            <div>
              <label for="injuries">Zranění nebo operace v minulosti</label>
              <textarea id="injuries" name="zraneni_operace" placeholder="Kdy, co, jak se to projevuje dnes…"></textarea>
            </div>

            <div>
              <label for="pain">Bolesti v současnosti</label>
              <textarea id="pain" name="bolesti_soucasnost" placeholder="Kde bolí, kdy to začíná, co zhoršuje/zlepšuje…"></textarea>
            </div>

            <button class="btn primary" type="submit">Odeslat (zatím demo)</button>
            <div class="small" id="formNote">Formulář je zkušební – nic se nikam neodesílá.</div>
          </form>
        </div>

        <div class="feature">
          <b>Přímý kontakt</b>
          <p style="margin:0; color:var(--muted); font-size:14px">
            E-mail: <a href="mailto:Dominika.c.9@icloud.com">Dominika.c.9@icloud.com</a><br>
            Telefon: <a href="tel:+420607603554">+420 607 603 554</a><br>
            Praha / online
          </p>
          <p class="small" style="margin-top:12px">Až budeš chtít, napojíme formulář na Formspree (zdarma).</p>
        </div>
      </div>
    </section>

    <footer>
      <div>© <span id="y"></span> GOATA Lab by Dominika Černá</div>
      <div><a href="#top" style="text-decoration:none">Nahoru ↑</a></div>
    </footer>
  </div>

  <script>
    document.getElementById("y").textContent = new Date().getFullYear();
    function demoSubmit(e){
      e.preventDefault();
      document.getElementById("formNote").textContent =
        "Děkuji! (Demo) Jakmile napojíme Formspree, formulář se bude odesílat na e-mail.";
      return false;
    }
  </script>
</body>
</html>
