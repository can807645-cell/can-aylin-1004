<!doctype html>
<html lang="de">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Can ❤️ Aylin — Unsere gemeinsame Seite</title>
  <meta name="description" content="Ein privater Ort nur für uns zwei — Erinnerungen, Fotos, kleine Momente." />
  <style>
    :root{
      --bg0:#07070b;
      --bg1:#0b0b13;
      --card:rgba(255,255,255,.06);
      --stroke:rgba(255,255,255,.12);
      --text:rgba(255,255,255,.92);
      --muted:rgba(255,255,255,.68);
      --muted2:rgba(255,255,255,.52);
      --pink:#ff4da6;
      --violet:#8a5cff;
      --cyan:#4dd7ff;
      --good:#61ffa0;
      --bad:#ff6b6b;
      --shadow: 0 20px 60px rgba(0,0,0,.55);
      --shadow2: 0 10px 30px rgba(0,0,0,.45);
      --r: 22px;
      --max: 1100px;
      --font: ui-sans-serif, system-ui, -apple-system, Segoe UI, Roboto, Helvetica, Arial, "Apple Color Emoji","Segoe UI Emoji";
      --mono: ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, "Liberation Mono", "Courier New", monospace;
    }
    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0;
      font-family:var(--font);
      color:var(--text);
      background: radial-gradient(1000px 600px at 20% 10%, rgba(138,92,255,.18), transparent 60%),
                  radial-gradient(900px 600px at 80% 20%, rgba(255,77,166,.16), transparent 55%),
                  radial-gradient(800px 600px at 60% 80%, rgba(77,215,255,.14), transparent 55%),
                  linear-gradient(180deg, var(--bg0), var(--bg1));
      overflow-x:hidden;
    }
    .noise{
      position:fixed; inset:0; pointer-events:none;
      background-image:url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='200' height='200'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='.8' numOctaves='3' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='200' height='200' filter='url(%23n)' opacity='.12'/%3E%3C/svg%3E");
      mix-blend-mode:overlay; opacity:.4;
    }
    .glow{
      position:fixed; inset:-200px; pointer-events:none;
      background:
        radial-gradient(900px 500px at 15% 25%, rgba(255,77,166,.10), transparent 60%),
        radial-gradient(900px 600px at 85% 35%, rgba(138,92,255,.10), transparent 60%),
        radial-gradient(800px 600px at 60% 85%, rgba(77,215,255,.08), transparent 60%);
      filter: blur(30px); opacity:.9;
    }
    header{
      position:sticky; top:0; z-index:50;
      backdrop-filter: blur(12px);
      background: linear-gradient(180deg, rgba(7,7,11,.72), rgba(7,7,11,.38));
      border-bottom:1px solid rgba(255,255,255,.06);
    }
    .wrap{max-width:var(--max); margin:0 auto; padding:18px 18px}
    .row{display:flex; align-items:center; justify-content:space-between; gap:14px}
    .brand{display:flex; align-items:center; gap:12px; user-select:none;}
    .logo{
      width:38px; height:38px; border-radius:14px;
      background: radial-gradient(circle at 30% 30%, rgba(255,77,166,.9), rgba(138,92,255,.9));
      box-shadow: 0 12px 30px rgba(255,77,166,.16);
      position:relative;
    }
    .logo:after{
      content:""; position:absolute; inset:2px; border-radius:12px;
      background: radial-gradient(circle at 70% 30%, rgba(77,215,255,.85), transparent 55%);
      opacity:.9;
    }
    .brand h1{font-size:14px; margin:0; letter-spacing:.2px}
    .brand p{margin:0; font-size:12px; color:var(--muted)}
    nav{display:flex; gap:10px; flex-wrap:wrap; justify-content:flex-end}
    .chip{
      padding:9px 12px;
      border:1px solid rgba(255,255,255,.10);
      background: rgba(255,255,255,.04);
      border-radius:999px;
      font-size:12px;
      color:rgba(255,255,255,.86);
      cursor:pointer;
      transition: transform .15s ease, background .15s ease, border-color .15s ease;
    }
    .chip:hover{transform: translateY(-1px); background: rgba(255,255,255,.06); border-color: rgba(255,255,255,.16)}
    .chip.primary{
      background: linear-gradient(90deg, rgba(255,77,166,.22), rgba(138,92,255,.18));
      border-color: rgba(255,77,166,.22);
    }
    main{padding:26px 0 80px}
    .hero{padding:22px 0 8px;}
    .heroGrid{display:grid; grid-template-columns: 1.05fr .95fr; gap:18px; align-items:stretch;}
    @media (max-width: 920px){ .heroGrid{grid-template-columns: 1fr;} nav{justify-content:flex-start} }
    .card{
      background: var(--card);
      border:1px solid rgba(255,255,255,.10);
      border-radius: var(--r);
      box-shadow: var(--shadow2);
      overflow:hidden;
      position:relative;
    }
    .card.pad{padding:18px}
    .cardHeader{display:flex; gap:10px; align-items:flex-start; justify-content:space-between;}
    .kicker{display:flex; gap:8px; align-items:center; flex-wrap:wrap;}
    .pill{
      font-size:11px; padding:6px 10px; border-radius:999px;
      border:1px solid rgba(255,255,255,.12);
      background: rgba(255,255,255,.04);
      color: rgba(255,255,255,.82);
    }
    .pill.good{border-color: rgba(97,255,160,.30); background: rgba(97,255,160,.08)}
    .pill.bad{border-color: rgba(255,107,107,.28); background: rgba(255,107,107,.08)}
    .grad{
      background: linear-gradient(90deg, var(--pink), var(--violet), var(--cyan));
      -webkit-background-clip:text; background-clip:text; color:transparent;
    }
    .title{font-size:32px; line-height:1.12; margin:10px 0 8px; letter-spacing:.2px;}
    .sub{margin:0; color:var(--muted); font-size:14px; line-height:1.55; max-width:52ch;}
    .actions{margin-top:14px; display:flex; gap:10px; flex-wrap:wrap;}
    .btn{
      border:none; cursor:pointer;
      padding:11px 14px; border-radius: 14px;
      font-size:13px; color: rgba(255,255,255,.92);
      background: rgba(255,255,255,.06);
      border:1px solid rgba(255,255,255,.12);
      transition: transform .15s ease, background .15s ease, border-color .15s ease;
    }
    .btn:hover{transform: translateY(-1px); background: rgba(255,255,255,.08); border-color: rgba(255,255,255,.18)}
    .btn.big{
      padding:12px 16px;
      background: linear-gradient(90deg, rgba(255,77,166,.24), rgba(138,92,255,.20));
      border-color: rgba(255,77,166,.24);
    }
    .btn.ghost{background: transparent;}
    .statGrid{display:grid; grid-template-columns: repeat(3, 1fr); gap:10px; margin-top:14px;}
    @media (max-width: 520px){ .statGrid{grid-template-columns: 1fr} }
    .stat{
      padding:14px; border-radius: 18px;
      border:1px solid rgba(255,255,255,.10);
      background: rgba(0,0,0,.16);
    }
    .stat .n{font-size:18px; font-weight:700; letter-spacing:.2px}
    .stat .l{font-size:12px; color:var(--muted); margin-top:4px}
    .rightPanel{padding:0; display:flex; flex-direction:column; min-height: 320px;}
    .photoTop{padding:16px 16px 0; display:flex; align-items:center; justify-content:space-between; gap:10px;}
    .photoTop h3{margin:0; font-size:14px; letter-spacing:.2px; color: rgba(255,255,255,.88);}
    .photoTop .meta{font-size:12px; color:var(--muted)}
    .grid{padding:14px 16px 16px; display:grid; grid-template-columns: repeat(2, 1fr); gap:10px; flex:1;}
    .thumb{
      border-radius: 18px;
      border:1px solid rgba(255,255,255,.10);
      background: linear-gradient(180deg, rgba(255,255,255,.06), rgba(0,0,0,.14));
      overflow:hidden; position:relative; cursor:pointer; min-height: 150px;
    }
    .thumb img{width:100%; height:100%; object-fit:cover; display:block; filter:saturate(1.08) contrast(1.04); transform: scale(1.02); transition: transform .25s ease, opacity .25s ease; opacity:.95;}
    .thumb:hover img{transform: scale(1.06); opacity:1}
    .thumb .cap{
      position:absolute; left:10px; right:10px; bottom:10px;
      font-size:11px; color: rgba(255,255,255,.86);
      text-shadow: 0 6px 24px rgba(0,0,0,.65);
      display:flex; justify-content:space-between; gap:10px; align-items:center;
    }
    .cap .dot{width:8px; height:8px; border-radius:999px; background: linear-gradient(90deg, var(--pink), var(--violet)); box-shadow: 0 10px 20px rgba(255,77,166,.15); flex:0 0 auto;}
    section{margin-top:18px}
    .two{display:grid; grid-template-columns: 1fr 1fr; gap:18px; align-items:stretch;}
    @media (max-width: 920px){ .two{grid-template-columns: 1fr} }
    .secTitle{font-size:14px; margin:0 0 10px; color: rgba(255,255,255,.88); letter-spacing:.2px; display:flex; align-items:center; gap:10px;}
    .secTitle .spark{width:10px; height:10px; border-radius:999px; background: linear-gradient(90deg, var(--cyan), var(--violet)); box-shadow: 0 10px 20px rgba(77,215,255,.12);}
    .letter{line-height:1.75; color: rgba(255,255,255,.86); font-size:14px; margin:0; white-space: pre-line;}
    .smallNote{margin-top:12px; color: var(--muted); font-size:12px; display:flex; gap:10px; flex-wrap:wrap; align-items:center;}
    .divider{height:1px; background: rgba(255,255,255,.10); margin:14px 0;}

    /* Lightbox */
    .lightbox{position:fixed; inset:0; background: rgba(0,0,0,.68); display:none; align-items:center; justify-content:center; z-index:2000; padding:18px; backdrop-filter: blur(10px);}
    .lightbox.on{display:flex}
    .lbCard{width:min(980px, 96vw); background: rgba(20,20,30,.72); border:1px solid rgba(255,255,255,.12); border-radius: 26px; box-shadow: var(--shadow); overflow:hidden; position:relative;}
    .lbTop{display:flex; align-items:center; justify-content:space-between; gap:10px; padding:12px 14px; border-bottom:1px solid rgba(255,255,255,.10); background: rgba(255,255,255,.04);}
    .lbTop .t{display:flex; gap:10px; align-items:center; min-width:0;}
    .lbTop .t strong{font-size:13px; overflow:hidden; text-overflow:ellipsis; white-space:nowrap;}
    .lbTop .t span{color:var(--muted); font-size:12px; white-space:nowrap;}
    .lbTop .x{border:none; background: rgba(255,255,255,.08); border:1px solid rgba(255,255,255,.12); color: rgba(255,255,255,.92); padding:8px 10px; border-radius: 12px; cursor:pointer;}
    .lbImgWrap{background: rgba(0,0,0,.24); display:flex; align-items:center; justify-content:center; min-height: 56vh;}
    .lbImgWrap img{width:100%; height:auto; max-height: 80vh; object-fit:contain; display:block;}
    .lbBottom{display:flex; gap:10px; justify-content:space-between; align-items:center; padding:12px 14px; border-top:1px solid rgba(255,255,255,.10); background: rgba(255,255,255,.03); flex-wrap:wrap;}
    .lbBottom .hint{color: var(--muted); font-size:12px;}
    .navBtn{border:none; cursor:pointer; padding:10px 12px; border-radius: 14px; background: rgba(255,255,255,.06); border:1px solid rgba(255,255,255,.12); color: rgba(255,255,255,.92);}

    /* Password overlay */
    .lock{position:fixed; inset:0; display:flex; align-items:center; justify-content:center; z-index:3000; padding:18px; background: rgba(0,0,0,.62); backdrop-filter: blur(14px);}
    .lock.off{display:none}
    .lockCard{width:min(560px, 96vw); border-radius: 28px; background: linear-gradient(180deg, rgba(255,255,255,.08), rgba(255,255,255,.04)); border:1px solid rgba(255,255,255,.12); box-shadow: var(--shadow); padding:18px; position:relative; overflow:hidden;}
    .lockCard:before{content:""; position:absolute; inset:-100px; background: radial-gradient(280px 240px at 20% 20%, rgba(255,77,166,.20), transparent 65%), radial-gradient(280px 240px at 80% 25%, rgba(138,92,255,.18), transparent 65%), radial-gradient(280px 240px at 55% 80%, rgba(77,215,255,.14), transparent 65%); filter: blur(18px); opacity:.95; pointer-events:none;}
    .lockInner{position:relative}
    .lockTitle{font-size:26px; margin:10px 0 6px; letter-spacing:.2px; line-height:1.15;}
    .lockSub{margin:0 0 14px; color: var(--muted); line-height:1.6; font-size:14px;}
    .pwRow{display:flex; gap:10px; flex-wrap:wrap; align-items:center; margin-top:6px;}
    .pwRow input{flex:1 1 260px; padding:12px 14px; border-radius:999px; border:1px solid rgba(255,255,255,.18); background: rgba(0,0,0,.18); color: rgba(255,255,255,.92); outline:none; font-size:14px;}
    .pwRow input::placeholder{color: rgba(255,255,255,.45)}
    .pwErr{display:none; color: rgba(255,120,180,.95); font-size:12px; margin-top:10px}
    .pwErr.on{display:block}
    .lockHint{margin-top:12px; color: var(--muted2); font-size:12px; line-height:1.55;}

    /* Toast */
    .toast{position: fixed; left:50%; bottom:18px; transform: translateX(-50%); background: rgba(20,20,30,.86); border:1px solid rgba(255,255,255,.12); border-radius: 999px; padding:10px 14px; color: rgba(255,255,255,.88); font-size:12px; box-shadow: var(--shadow2); display:none; z-index:4000; max-width:min(680px, 92vw); text-align:center;}
    .toast.on{display:block}

    /* Floating hearts */
    .heart{position:fixed; left:0; top:0; pointer-events:none; z-index:3500; font-size:16px; filter: drop-shadow(0 10px 20px rgba(255,77,166,.18)); will-change: transform, opacity; opacity:0;}

    footer{margin-top:26px; padding:16px 0 0; color: var(--muted2); font-size:12px; text-align:center;}
    .mini{font-family:var(--mono); font-size:11px; color: rgba(255,255,255,.60);}
  </style>
</head>

<body>
  <div class="glow"></div>
  <div class="noise"></div>

  <!-- 🔐 PASSWORT-SPERRE -->
  <div class="lock" id="lock">
    <div class="lockCard">
      <div class="lockInner">
        <div class="kicker">
          <span class="pill">Can ❤️ Aylin</span>
          <span class="pill">Privat</span>
          <span class="pill good">Nur wir zwei</span>
        </div>

        <h2 class="lockTitle"><span class="grad">Unsere gemeinsame Seite</span></h2>
        <p class="lockSub">
          Ein kleiner Ort nur für uns — mit Fotos, Erinnerungen und Momenten, die wir nie vergessen wollen. 💞
        </p>

        <div class="pwRow">
          <input id="pw" type="password" autocomplete="off" placeholder="Passwort eingeben…" />
          <button class="btn big" id="pwBtn">Öffnen 🔐</button>
          <button class="btn ghost" id="pwHintBtn">Tipp ✨</button>
        </div>

        <div class="pwErr" id="pwErr">Falsches Passwort… bitte nochmal 🥺</div>
        <div class="lockHint" id="pwHint" style="display:none;">
          Tipp: Das Passwort ist etwas, das nur wir wissen. 🤍
        </div>
      </div>
    </div>
  </div>

  <header>
    <div class="wrap">
      <div class="row">
        <div class="brand">
          <div class="logo" aria-hidden="true"></div>
          <div>
            <h1 id="brandTitle">Unsere Seite</h1>
            <p id="brandSub">Ein Zuhause für unsere Momente</p>
          </div>
        </div>

        <nav>
          <button class="chip primary" id="goHero">Start</button>
          <button class="chip" id="goGallery">Fotos</button>
          <button class="chip" id="goLetter">Brief</button>
          <button class="chip" id="goSurprise">Überraschung</button>
          <button class="chip" id="lockAgain">Sperren</button>
        </nav>
      </div>
    </div>
  </header>

  <main class="wrap">
    <section class="hero" id="hero">
      <div class="heroGrid">
        <div class="card pad">
          <div class="cardHeader">
            <div class="kicker">
              <span class="pill" id="pillNames">Can ❤️ Aylin</span>
              <span class="pill" id="pillSince">Seit: 10.04.2025</span>
              <span class="pill good" id="pillMode">Gemeinsam</span>
            </div>
            <span class="pill" title="Status" id="statusPill">Online</span>
          </div>

          <h2 class="title"><span class="grad">Unsere Geschichte</span> ✨</h2>
          <p class="sub">
            Ein privater Ort nur für uns — Erinnerungen, Fotos und kleine Momente.
            Für immer <span class="grad">wir</span>. 🤍
          </p>

          <div class="actions">
            <button class="btn big" id="btnHearts">Herzen schicken 💘</button>
            <button class="btn" id="btnCopyLink">Seite kopieren 🔗</button>
            <button class="btn" id="btnReload">Fotos aktualisieren ↻</button>
          </div>

          <div class="statGrid">
            <div class="stat">
              <div class="n" id="daysCount">–</div>
              <div class="l">Tage zusammen</div>
            </div>
            <div class="stat">
              <div class="n" id="hoursCount">–</div>
              <div class="l">Stunden voller „Wir“</div>
            </div>
            <div class="stat">
              <div class="n" id="picsCount">–</div>
              <div class="l">Fotos in unserer Galerie</div>
            </div>
          </div>

          <div class="divider"></div>
          <div class="smallNote">
            <span class="pill">💡 Mini-Regel: Wenn wir streiten, wählen wir immer wieder „uns“.</span>
            <span class="pill">🫶 Vertrauen. Ruhe. Liebe.</span>
          </div>
        </div>

        <div class="card rightPanel" id="gallery">
          <div class="photoTop">
            <div>
              <h3>Unsere Fotos</h3>
              <div class="meta" id="galleryMeta">Wird geladen…</div>
            </div>
            <button class="btn" id="btnOpenGallery">Öffnen ▸</button>
          </div>
          <div class="grid" id="thumbGrid"></div>
        </div>
      </div>
    </section>

    <section class="two">
      <div class="card pad" id="letter">
        <div class="secTitle"><span class="spark"></span> Unser Brief</div>
        <div class="kicker" style="margin-bottom:10px;">
          <span class="pill" id="dearLine">Can ❤️ Aylin</span>
          <span class="pill">Nur wir</span>
          <span class="pill good">Für immer</span>
        </div>

        <p class="letter" id="letterText">
Das hier ist unsere kleine Welt.
Ein Platz, an dem unsere Momente leben: ein Lächeln, ein Blick, eine Umarmung.
Wir sind nicht perfekt – aber wir sind echt.
Und egal was passiert: Wir wählen immer wieder „uns“.

Danke, dass du da bist.
Danke, dass wir zusammen wachsen.
Heute, morgen und jedes Mal, wenn wir uns ansehen und still wissen: Das ist Liebe.
        </p>

        <div class="divider"></div>

        <div class="smallNote">
          <span>— <strong id="signLine">Wir</strong></span>
          <span class="mini" id="signatureMini">♡ Can & Aylin ♡</span>
        </div>
      </div>

      <div class="card pad" id="surprise">
        <div class="secTitle"><span class="spark"></span> Überraschung</div>

        <p class="sub" style="max-width:none">
          Drück den Button, wenn du ein kleines „Wow“ willst. 😄
          (Ja… das ist unsere <span class="grad">gemeinsame</span> Seite.)
        </p>

        <div class="actions">
          <button class="btn big" id="btnSurprise">Überrasch mich ✨</button>
          <button class="btn" id="btnSweet">Süße Nachricht 💌</button>
        </div>

        <div class="divider"></div>

        <div class="card pad" style="background:rgba(0,0,0,.16); border-radius:18px;">
          <div class="kicker" style="margin-bottom:10px;">
            <span class="pill">Unsere kleine Liste</span>
            <span class="pill good">„Wir“-Versprechen</span>
          </div>
          <ul style="margin:0; padding-left:18px; color:rgba(255,255,255,.86); line-height:1.7; font-size:14px;">
            <li>Wir reden ruhig — auch wenn’s schwer ist.</li>
            <li>Wir sind ein Team, nicht Gegner.</li>
            <li>Wir vertrauen — und wir schützen das Vertrauen.</li>
            <li>Wir bauen uns ein Leben, das sich nach Zuhause anfühlt.</li>
          </ul>
        </div>

        <div class="smallNote" style="margin-top:14px;">
          <span class="pill">🔒 Privat</span>
          <span class="pill">✨ Nur wir kennen das Passwort</span>
        </div>
      </div>
    </section>

    <footer>
      <div>Made for <span class="grad" id="footerNames">Can ❤️ Aylin</span> · <span id="footerYear"></span></div>
      <div class="mini" id="footerMini">Wenn Liebe ein Ort wäre, wäre es: „Wir“.</div>
    </footer>
  </main>

  <div class="lightbox" id="lightbox" aria-hidden="true">
    <div class="lbCard">
      <div class="lbTop">
        <div class="t">
          <strong id="lbTitle">Foto</strong>
          <span id="lbMeta">–</span>
        </div>
        <button class="x" id="lbClose">Schließen ✕</button>
      </div>

      <div class="lbImgWrap">
        <img id="lbImg" alt="Foto" />
      </div>

      <div class="lbBottom">
        <div style="display:flex; gap:10px; align-items:center; flex-wrap:wrap;">
          <button class="navBtn" id="lbPrev">←</button>
          <button class="navBtn" id="lbNext">→</button>
          <button class="navBtn" id="lbOpen">Öffnen ↗</button>
          <button class="navBtn" id="lbCopy">Kopieren 🔗</button>
        </div>
        <div class="hint">Tipp: Pfeiltasten ← → funktionieren auch.</div>
      </div>
    </div>
  </div>

  <div class="toast" id="toast">–</div>

  <script>
    // ✅ FIXE EINSTELLUNGEN (fertig für dich)
    const COUPLE_A = "Can";
    const COUPLE_B = "Aylin";
    const SINCE_DATE = "2025-04-10T00:00:00";
    const SITE_PASSWORD = "1904";
    const PHOTOS_JSON_URL = "https://script.google.com/macros/s/AKfycbz89OA07y8Onrq20RsoMGxjfYM7P0QEGL5NFeymsM0QH2PWs8jgle10-rngXybNSPLzcg/exec";

    const $ = (q, el=document) => el.querySelector(q);

    const lockEl = $("#lock");
    const pw = $("#pw");
    const pwBtn = $("#pwBtn");
    const pwErr = $("#pwErr");
    const pwHintBtn = $("#pwHintBtn");
    const pwHint = $("#pwHint");

    const pillNames = $("#pillNames");
    const footerNames = $("#footerNames");
    const pillSince = $("#pillSince");

    const daysCount = $("#daysCount");
    const hoursCount = $("#hoursCount");
    const picsCount = $("#picsCount");
    const galleryMeta = $("#galleryMeta");
    const thumbGrid = $("#thumbGrid");

    const toast = $("#toast");
    const statusPill = $("#statusPill");

    const lightbox = $("#lightbox");
    const lbImg = $("#lbImg");
    const lbTitle = $("#lbTitle");
    const lbMeta = $("#lbMeta");
    const lbClose = $("#lbClose");
    const lbPrev = $("#lbPrev");
    const lbNext = $("#lbNext");
    const lbOpen = $("#lbOpen");
    const lbCopy = $("#lbCopy");

    $("#goHero").addEventListener("click", () => scrollToId("hero"));
    $("#goGallery").addEventListener("click", () => scrollToId("gallery"));
    $("#goLetter").addEventListener("click", () => scrollToId("letter"));
    $("#goSurprise").addEventListener("click", () => scrollToId("surprise"));
    $("#lockAgain").addEventListener("click", lockAgain);

    $("#btnHearts").addEventListener("click", () => burstHearts(14));
    $("#btnCopyLink").addEventListener("click", () => copyText(location.href, "Seitenlink kopiert ✅"));
    $("#btnReload").addEventListener("click", () => loadPhotos(true));
    $("#btnOpenGallery").addEventListener("click", () => scrollToId("gallery"));

    $("#btnSurprise").addEventListener("click", surprise);
    $("#btnSweet").addEventListener("click", sweetMsg);

    const names = `${COUPLE_A} ❤️ ${COUPLE_B}`;
    pillNames.textContent = names;
    footerNames.textContent = names;
    $("#footerYear").textContent = new Date().getFullYear();
    pillSince.textContent = `Seit: ${formatGermanDate(SINCE_DATE)}`;
    $("#dearLine").textContent = names;
    $("#signatureMini").textContent = `♡ ${COUPLE_A} & ${COUPLE_B} ♡`;

    setInterval(() => {
      const online = navigator.onLine;
      statusPill.textContent = online ? "Online" : "Offline";
      statusPill.className = "pill " + (online ? "good" : "bad");
    }, 900);

    // PASSWORT
    if (localStorage.getItem("unlocked") === "1") lockEl.classList.add("off");

    function unlock() {
      const val = (pw.value || "").trim();
      if (val === SITE_PASSWORD) {
        localStorage.setItem("unlocked", "1");
        lockEl.classList.add("off");
        pwErr.classList.remove("on");
        toastMsg("Willkommen, ihr zwei 💞");
        burstHearts(10);
      } else {
        pwErr.classList.add("on");
        burstHearts(3);
      }
    }
    pwBtn.addEventListener("click", unlock);
    pw.addEventListener("keydown", (e) => e.key === "Enter" && unlock());
    pwHintBtn.addEventListener("click", () => {
      pwHint.style.display = (pwHint.style.display === "none") ? "block" : "none";
    });

    function lockAgain(){
      localStorage.removeItem("unlocked");
      lockEl.classList.remove("off");
      pw.value = "";
      pw.focus();
      toastMsg("Seite gesperrt 🔒");
    }

    // COUNTER
    const since = new Date(SINCE_DATE);
    function updateCounter(){
      const now = new Date();
      const ms = now - since;
      const days = Math.floor(ms / (1000*60*60*24));
      const hours = Math.floor(ms / (1000*60*60));
      daysCount.textContent = isFinite(days) ? days.toLocaleString("de-DE") : "–";
      hoursCount.textContent = isFinite(hours) ? hours.toLocaleString("de-DE") : "–";
    }
    updateCounter();
    setInterval(updateCounter, 1000);

    // PHOTOS
    let items = [];
    let currentIndex = 0;

    async function loadPhotos(force=false){
      galleryMeta.textContent = force ? "Aktualisiere…" : "Wird geladen…";
      try{
        const res = await fetch(PHOTOS_JSON_URL, { cache: force ? "no-store" : "default" });
        if(!res.ok) throw new Error("HTTP " + res.status);
        const data = await res.json();
        items = (data.items || [])
          .filter(x => x && typeof x.url === "string" && x.url.startsWith("http"))
          .sort((a,b) => (b.ts||0) - (a.ts||0));

        picsCount.textContent = items.length.toLocaleString("de-DE");
        galleryMeta.textContent = items.length ? `${items.length} Foto(s) · Tippen zum Öffnen` : "Noch keine Fotos im Ordner…";
        renderThumbs();
        if(force) toastMsg("Fotos aktualisiert ✅");
      }catch(err){
        console.error(err);
        galleryMeta.textContent = "Fehler beim Laden. Prüfe Apps Script / Ordnerzugriff.";
        toastMsg("Fotos konnten nicht geladen werden ❌");
      }
    }

    function renderThumbs(){
      thumbGrid.innerHTML = "";
      const show = items.slice(0, 4);

      if(!show.length){
        for(let i=0;i<4;i++){
          const d = document.createElement("div");
          d.className = "thumb";
          d.innerHTML = `<div class="cap"><span style="display:flex;gap:8px;align-items:center;"><span class="dot"></span>Warte auf Fotos…</span><span>♡</span></div>`;
          thumbGrid.appendChild(d);
        }
        return;
      }

      show.forEach((it, idx) => {
        const d = document.createElement("div");
        d.className = "thumb";
        const name = safeText(it.name || "Foto");
        const date = it.ts ? new Date(it.ts).toLocaleString("de-DE") : "";
        d.innerHTML = `
          <img loading="lazy" referrerpolicy="no-referrer" src="${it.url}" alt="${name}">
          <div class="cap">
            <span style="display:flex;gap:8px;align-items:center;min-width:0;">
              <span class="dot"></span>
              <span style="overflow:hidden;text-overflow:ellipsis;white-space:nowrap;max-width:140px;">${name}</span>
            </span>
            <span style="color:rgba(255,255,255,.72)">${date ? "🕒" : "♡"}</span>
          </div>
        `;
        d.addEventListener("click", () => openLightbox(idx));
        thumbGrid.appendChild(d);
      });

      for(let i=show.length; i<4; i++){
        const d = document.createElement("div");
        d.className = "thumb";
        d.innerHTML = `<div class="cap"><span style="display:flex;gap:8px;align-items:center;"><span class="dot"></span>Mehr Fotos folgen…</span><span>✨</span></div>`;
        thumbGrid.appendChild(d);
      }
    }

    // LIGHTBOX
    function openLightbox(index){
      if(!items.length) return;
      currentIndex = clamp(index, 0, items.length-1);
      renderLightbox();
      lightbox.classList.add("on");
      lightbox.setAttribute("aria-hidden","false");
    }
    function closeLightbox(){
      lightbox.classList.remove("on");
      lightbox.setAttribute("aria-hidden","true");
    }
    function renderLightbox(){
      const it = items[currentIndex];
      lbImg.src = it.url;
      lbTitle.textContent = it.name ? it.name : `Foto ${currentIndex+1}`;
      lbMeta.textContent = `${currentIndex+1} / ${items.length}` + (it.ts ? ` · ${new Date(it.ts).toLocaleString("de-DE")}` : "");
      lbOpen.onclick = () => window.open(it.url, "_blank");
      lbCopy.onclick = () => copyText(it.url, "Foto-Link kopiert ✅");
    }

    lbClose.addEventListener("click", closeLightbox);
    lightbox.addEventListener("click", (e) => { if(e.target === lightbox) closeLightbox(); });
    lbPrev.addEventListener("click", () => { currentIndex = (currentIndex - 1 + items.length) % items.length; renderLightbox(); });
    lbNext.addEventListener("click", () => { currentIndex = (currentIndex + 1) % items.length; renderLightbox(); });

    window.addEventListener("keydown", (e) => {
      if(!lightbox.classList.contains("on")) return;
      if(e.key === "Escape") closeLightbox();
      if(e.key === "ArrowLeft") lbPrev.click();
      if(e.key === "ArrowRight") lbNext.click();
    });

    // SURPRISE
    const surprises = [
      "Wenn Liebe ein Ort wäre… dann wären wir Zuhause. 🏡🤍",
      "Wir sind nicht perfekt — aber wir sind echt. Und das ist selten. ✨",
      "Heute, morgen, immer wieder: Wir. 💞",
      "Mit dir wird die Welt leiser — und mein Herz ruhiger. 🫶",
      "Egal wie laut alles ist: Wir bleiben unser sicherer Ort. 🔒🤍"
    ];
    function surprise(){
      toastMsg(surprises[Math.floor(Math.random()*surprises.length)]);
      burstHearts(16);
    }
    function sweetMsg(){
      toastMsg("Nur wir zwei. Ohne Publikum. Ohne Lärm. Einfach wir. 💗");
      burstHearts(12);
    }

    // HEARTS
    function burstHearts(n=10){
      const emojis = ["💖","💘","💗","💞","❤️","✨","🌙"];
      for(let i=0;i<n;i++){
        const el = document.createElement("div");
        el.className = "heart";
        el.textContent = emojis[Math.floor(Math.random()*emojis.length)];
        document.body.appendChild(el);

        const x = Math.random() * window.innerWidth;
        const y = window.innerHeight - 20;
        const dx = (Math.random()*2-1) * 120;
        const dy = 260 + Math.random()*220;
        const rot = (Math.random()*2-1) * 40;
        const scale = .9 + Math.random()*1.2;
        const dur = 1200 + Math.random()*900;
        const delay = Math.random()*220;

        el.style.left = x + "px";
        el.style.top = y + "px";

        requestAnimationFrame(() => {
          el.style.transition = `transform ${dur}ms cubic-bezier(.2,.9,.2,1) ${delay}ms, opacity ${dur}ms ease ${delay}ms`;
          el.style.opacity = "1";
          el.style.transform = `translate(${dx}px, -${dy}px) rotate(${rot}deg) scale(${scale})`;
        });

        setTimeout(() => { el.style.opacity = "0"; }, dur*0.75);
        setTimeout(() => el.remove(), dur + delay + 200);
      }
    }

    // HELPERS
    function scrollToId(id){
      const el = document.getElementById(id);
      if(!el) return;
      el.scrollIntoView({ behavior:"smooth", block:"start" });
    }
    function toastMsg(text){
      toast.textContent = text;
      toast.classList.add("on");
      clearTimeout(toast._t);
      toast._t = setTimeout(() => toast.classList.remove("on"), 2800);
    }
    async function copyText(text, okMsg="Kopiert ✅"){
      try{
        await navigator.clipboard.writeText(text);
        toastMsg(okMsg);
      }catch{
        const ta = document.createElement("textarea");
        ta.value = text;
        document.body.appendChild(ta);
        ta.select();
        document.execCommand("copy");
        ta.remove();
        toastMsg(okMsg);
      }
    }
    function clamp(v,min,max){ return Math.max(min, Math.min(max, v)); }
    function safeText(s){ return String(s).replace(/[<>&"]/g, c => ({'<':'&lt;','>':'&gt;','&':'&amp;','"':'&quot;'}[c])); }
    function formatGermanDate(iso){
      const d = new Date(iso);
      if(!isFinite(d)) return "–";
      return d.toLocaleDateString("de-DE", { day:"2-digit", month:"2-digit", year:"numeric" });
    }

    // NAV
    document.getElementById("goHero").addEventListener("click", () => scrollToId("hero"));
    document.getElementById("goGallery").addEventListener("click", () => scrollToId("gallery"));
    document.getElementById("goLetter").addEventListener("click", () => scrollToId("letter"));
    document.getElementById("goSurprise").addEventListener("click", () => scrollToId("surprise"));

    // START
    loadPhotos(false);
    toastMsg("Bereit. Nur wir zwei. 🔒💞");
  </script>
</body>
</html>