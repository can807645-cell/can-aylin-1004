<!doctype html>
<html lang="de">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Can ❤ Aylin — Unsere gemeinsame Seite</title>
  <meta name="description" content="Ein privater Ort nur für uns zwei — Erinnerungen, Fotos, kleine Momente." />

  <!-- nicer font -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Manrope:wght@400;600;700;800&display=swap" rel="stylesheet">

  <style>
    :root{
      --bg0:#090612;
      --bg1:#120a25;

      --card:rgba(255,255,255,.07);
      --card2:rgba(255,255,255,.10);
      --stroke:rgba(255,255,255,.12);
      --stroke2:rgba(255,255,255,.20);

      --text:rgba(255,255,255,.92);
      --muted:rgba(255,255,255,.68);
      --muted2:rgba(255,255,255,.50);

      --pink:#ff4fd8;
      --violet:#9b5cff;
      --cyan:#4dd6ff;
      --good:#61ffb0;
      --warn:#ffd166;
      --bad:#ff6b6b;

      --shadow: 0 18px 60px rgba(0,0,0,.55);
      --shadow2: 0 10px 25px rgba(0,0,0,.35);
      --r:18px;
      --r2:26px;
      --focus: 0 0 0 3px rgba(155,92,255,.35);
    }

    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0;
      color:var(--text);
      font: 600 15px/1.5 "Manrope", ui-sans-serif, system-ui, -apple-system, Segoe UI, Roboto, Arial;
      background:
        radial-gradient(1200px 700px at 10% -10%, rgba(155,92,255,.38), transparent 60%),
        radial-gradient(900px 600px at 90% 5%, rgba(255,79,216,.28), transparent 55%),
        radial-gradient(700px 500px at 60% 110%, rgba(77,214,255,.18), transparent 60%),
        linear-gradient(180deg, var(--bg0), var(--bg1) 55%, #07050f);
      overflow-x:hidden;
    }

    a{color:inherit}

    .wrap{max-width:1100px;margin:0 auto;padding:22px 16px 44px}

    /* top bar */
    .top{
      position:sticky;top:0;z-index:50;
      backdrop-filter: blur(14px);
      background: linear-gradient(180deg, rgba(9,6,18,.78), rgba(9,6,18,.40));
      border-bottom:1px solid rgba(255,255,255,.08);
    }
    .topInner{max-width:1100px;margin:0 auto;padding:14px 16px;display:flex;align-items:center;gap:12px}
    .brand{display:flex;align-items:center;gap:10px;min-width:220px}
    .logo{
      width:38px;height:38px;border-radius:14px;
      background: radial-gradient(circle at 35% 25%, rgba(255,79,216,.95), rgba(155,92,255,.95) 55%, rgba(77,214,255,.45));
      box-shadow: 0 10px 26px rgba(155,92,255,.22), 0 10px 26px rgba(255,79,216,.14);
      border:1px solid rgba(255,255,255,.16);
      flex:0 0 auto;
    }
    .brand h1{margin:0;font-size:14px;letter-spacing:.2px}
    .brand p{margin:0;color:var(--muted);font-size:12px;font-weight:600}

    .nav{
      margin-left:auto;
      display:flex;gap:8px;flex-wrap:wrap;justify-content:flex-end
    }
    .pill{
      border:1px solid var(--stroke);
      background: linear-gradient(180deg, rgba(255,255,255,.10), rgba(255,255,255,.04));
      color:var(--text);
      padding:8px 11px;border-radius:999px;
      cursor:pointer;
      transition: transform .16s ease, border-color .16s ease, background .16s ease;
      user-select:none;
      display:inline-flex;align-items:center;gap:8px;
      font-weight:800;
    }
    .pill:hover{transform: translateY(-1px);border-color:var(--stroke2)}
    .pill:focus{outline:none;box-shadow:var(--focus)}
    .pill .dot{width:7px;height:7px;border-radius:50%;background:var(--pink);box-shadow:0 0 0 4px rgba(255,79,216,.16)}
    .pill.secondary .dot{background:var(--cyan);box-shadow:0 0 0 4px rgba(77,214,255,.14)}
    .pill.warn .dot{background:var(--warn);box-shadow:0 0 0 4px rgba(255,209,102,.14)}
    .pill.lock .dot{background:var(--muted2);box-shadow:0 0 0 4px rgba(255,255,255,.12)}

    /* layout */
    .grid{display:grid;grid-template-columns: 1.1fr .9fr; gap:14px; margin-top:18px}
    @media (max-width: 860px){.grid{grid-template-columns:1fr}}

    .card{
      background: linear-gradient(180deg, rgba(255,255,255,.08), rgba(255,255,255,.05));
      border:1px solid var(--stroke);
      border-radius: var(--r2);
      box-shadow: var(--shadow2);
      overflow:hidden;
      position:relative;
    }
    .card::before{
      content:"";
      position:absolute;inset:-2px;
      background: radial-gradient(520px 180px at 15% 0%, rgba(155,92,255,.18), transparent 60%),
                  radial-gradient(520px 180px at 85% 0%, rgba(255,79,216,.14), transparent 55%);
      pointer-events:none;
      opacity:.95;
    }
    .cardInner{position:relative;padding:16px}
    .titleRow{display:flex;align-items:center;gap:10px;margin-bottom:10px;flex-wrap:wrap}
    .badge{
      font-size:12px;font-weight:800;
      padding:6px 10px;border-radius:999px;
      border:1px solid rgba(255,255,255,.14);
      background: rgba(0,0,0,.20);
      color:var(--muted);
      backdrop-filter: blur(8px);
    }
    .h2{margin:0;font-size:18px;letter-spacing:.2px}
    .small{color:var(--muted);font-size:13px;font-weight:600}
    .hr{height:1px;background:rgba(255,255,255,.10);margin:12px 0}

    .btn{
      border:1px solid var(--stroke);
      background: linear-gradient(180deg, rgba(155,92,255,.28), rgba(155,92,255,.10));
      padding:10px 12px;border-radius:14px;
      color:var(--text);
      cursor:pointer;
      transition: transform .16s ease, border-color .16s ease, filter .16s ease;
      display:inline-flex;align-items:center;gap:8px;
      box-shadow: 0 10px 26px rgba(155,92,255,.14);
      font-weight:900;
    }
    .btn:hover{transform: translateY(-1px);border-color:rgba(155,92,255,.45);filter:saturate(1.05)}
    .btn:focus{outline:none;box-shadow:var(--focus)}
    .btn.gray{
      background: linear-gradient(180deg, rgba(255,255,255,.10), rgba(255,255,255,.06));
      box-shadow:none;
    }
    .btn.good{background: linear-gradient(180deg, rgba(97,255,176,.22), rgba(97,255,176,.08));}
    .btn.bad{background: linear-gradient(180deg, rgba(255,107,107,.20), rgba(255,107,107,.08));}

    .kpis{display:grid;grid-template-columns: repeat(3,1fr); gap:10px; margin-top:10px}
    .kpi{
      padding:12px;border-radius:18px;
      border:1px solid rgba(255,255,255,.12);
      background: rgba(0,0,0,.16);
    }
    .kpi .n{font-size:20px;font-weight:900;letter-spacing:.2px}
    .kpi .l{font-size:12px;color:var(--muted);font-weight:700}

    /* gallery */
    .gallery{display:grid;grid-template-columns: repeat(3, 1fr); gap:10px}
    @media (max-width: 520px){.gallery{grid-template-columns: repeat(2, 1fr)}}

    .thumb{
      position:relative;
      border-radius:18px;
      overflow:hidden;
      border:1px solid rgba(255,255,255,.12);
      background: rgba(0,0,0,.18);
      aspect-ratio: 1/1;
      cursor:pointer;
      transition: transform .16s ease, border-color .16s ease;
    }
    .thumb:hover{transform: translateY(-2px);border-color:rgba(255,255,255,.22)}
    .thumb img{width:100%;height:100%;object-fit:cover;display:block}
    .thumb .ph{
      position:absolute;inset:0;display:grid;place-items:center;
      color:rgba(255,255,255,.60);
      font-size:12px;font-weight:800;
      background: radial-gradient(circle at 30% 20%, rgba(255,79,216,.12), transparent 60%),
                  radial-gradient(circle at 70% 20%, rgba(155,92,255,.12), transparent 60%),
                  rgba(0,0,0,.18);
      text-align:center;
      padding:10px;
    }
    .thumb .cap{
      position:absolute;left:8px;right:8px;bottom:8px;
      padding:6px 8px;border-radius:12px;
      background: rgba(0,0,0,.35);
      border:1px solid rgba(255,255,255,.12);
      font-size:11px;color:rgba(255,255,255,.80);
      white-space:nowrap;overflow:hidden;text-overflow:ellipsis;
      backdrop-filter: blur(8px);
      font-weight:800;
    }

    /* overlay modal */
    .overlay{
      position:fixed;inset:0;z-index:200;
      background: rgba(0,0,0,.62);
      display:none;
      align-items:center;justify-content:center;
      padding:18px;
    }
    .overlay.show{display:flex}

    .modal{
      width:min(980px, 96vw);
      max-height: 88vh;
      overflow:auto;
      border-radius: 26px;
      border:1px solid rgba(255,255,255,.16);
      background:
        radial-gradient(900px 260px at 15% 0%, rgba(155,92,255,.20), transparent 60%),
        radial-gradient(900px 260px at 85% 0%, rgba(255,79,216,.14), transparent 55%),
        rgba(14,10,26,.92);
      box-shadow: var(--shadow);
      transform: translateY(10px) scale(.98);
      opacity: 0;
      transition: transform .18s ease, opacity .18s ease;
      position:relative;
    }
    .overlay.show .modal{transform: translateY(0) scale(1);opacity:1}

    .modalHead{
      position:sticky;top:0;z-index:5;
      padding:14px 14px 10px;
      display:flex;align-items:center;gap:10px;justify-content:space-between;
      border-bottom:1px solid rgba(255,255,255,.10);
      background: linear-gradient(180deg, rgba(14,10,26,.92), rgba(14,10,26,.70));
      backdrop-filter: blur(10px);
    }
    .modalTitle{font-weight:900}
    .close{
      border:1px solid rgba(255,255,255,.16);
      background: rgba(255,255,255,.06);
      padding:8px 10px;border-radius:999px;cursor:pointer;
      font-weight:900;
    }
    .close:hover{border-color:rgba(255,255,255,.26)}
    .modalBody{padding:14px}

    /* lightbox */
    .lightbox{display:grid;gap:10px}
    .lbFrame{
      border-radius:22px;
      border:1px solid rgba(255,255,255,.14);
      background: rgba(0,0,0,.20);
      overflow:hidden;
      min-height: 280px;
      display:grid;place-items:center;
    }
    .lbFrame img{
      max-width:100%;
      max-height:68vh;
      object-fit:contain;
      display:block;
      background: transparent;
    }
    .lbBar{display:flex;align-items:center;gap:10px;flex-wrap:wrap;justify-content:space-between}
    .lbMeta{color:rgba(255,255,255,.80);font-size:12px;font-weight:800}
    .lbControls{display:flex;gap:8px;flex-wrap:wrap}

    /* toast */
    .toast{
      position:fixed;left:50%;bottom:18px;transform:translateX(-50%);
      background: rgba(0,0,0,.74);
      border:1px solid rgba(255,255,255,.16);
      color:rgba(255,255,255,.92);
      padding:10px 12px;border-radius:14px;
      box-shadow: var(--shadow2);
      display:none;
      z-index:250;
      font-weight:900;
    }
    .toast.show{display:block;animation: pop .18s ease}
    @keyframes pop{from{transform:translateX(-50%) translateY(8px);opacity:0}to{transform:translateX(-50%) translateY(0);opacity:1}}

    /* password gate */
    .gate{
      position:fixed;inset:0;z-index:300;
      background:
        radial-gradient(1200px 700px at 10% -10%, rgba(155,92,255,.40), transparent 60%),
        radial-gradient(900px 600px at 90% 5%, rgba(255,79,216,.30), transparent 55%),
        radial-gradient(700px 500px at 60% 110%, rgba(77,214,255,.22), transparent 60%),
        linear-gradient(180deg, var(--bg0), var(--bg1) 55%, #07050f);
      display:flex;align-items:center;justify-content:center;
      padding:16px;
    }
    .gateBox{
      width:min(560px, 96vw);
      border-radius: 30px;
      border:1px solid rgba(255,255,255,.16);
      background: rgba(14,10,26,.84);
      box-shadow: var(--shadow);
      padding:18px;
    }
    .gateBox h2{margin:0 0 6px;font-size:20px;font-weight:900}
    .gateBox p{margin:0;color:var(--muted);font-weight:700}
    .field{margin-top:14px;display:flex;gap:10px}
    .inp{
      flex:1;
      border-radius:14px;
      padding:12px 12px;
      border:1px solid rgba(255,255,255,.14);
      background: rgba(0,0,0,.22);
      color:var(--text);
      outline:none;
      font-weight:800;
    }
    .inp:focus{box-shadow:var(--focus);border-color:rgba(155,92,255,.45)}
    .hint{margin-top:10px;color:rgba(255,255,255,.62);font-size:12px;font-weight:700}
    .tiny{font-size:12px;color:rgba(255,255,255,.55);font-weight:700}
    .sep{height:1px;background:rgba(255,255,255,.12);margin:14px 0}

    .statusLine{
      display:flex;align-items:center;gap:10px;flex-wrap:wrap;
      padding:10px 12px;border-radius:18px;
      border:1px solid rgba(255,255,255,.12);
      background: rgba(0,0,0,.16);
    }
    .statusDot{width:9px;height:9px;border-radius:50%;}
    .statusText{font-size:12px;font-weight:900;color:rgba(255,255,255,.80)}
  </style>
</head>

<body>

  <!-- Passwort-Schutz -->
  <div class="gate" id="gate" aria-hidden="true">
    <div class="gateBox">
      <div style="display:flex;align-items:center;gap:12px">
        <div class="logo" aria-hidden="true"></div>
        <div>
          <h2>Nur für uns zwei ❤</h2>
          <p>Gib das Passwort ein — dann öffnet sich unsere gemeinsame Seite.</p>
        </div>
      </div>

      <div class="field">
        <input class="inp" id="pw" type="password" inputmode="text" placeholder="Passwort…" autocomplete="current-password" />
        <button class="btn good" id="unlockBtn">Öffnen ✨</button>
      </div>

      <div class="hint">
        Tipp: Nutzt etwas, das nur ihr kennt (z. B. ein kleines Codewort). Du kannst es unten in <b>CONFIG.PASSWORD</b> ändern.
      </div>

      <div class="sep"></div>
      <div class="tiny">
        Hinweis: GitHub Pages kann öffentlich sein. Dieser Schutz ist für „privat unter uns“, aber nicht wie Banking-Sicherheit.
      </div>
    </div>
  </div>

  <header class="top">
    <div class="topInner">
      <div class="brand">
        <div class="logo" aria-hidden="true"></div>
        <div>
          <h1>Unsere Seite</h1>
          <p>Erinnerungen, Fotos, kleine Momente — für Can & Aylin</p>
        </div>
      </div>

      <nav class="nav" aria-label="Navigation">
        <button class="pill" data-open="start"><span class="dot"></span>Start</button>
        <button class="pill secondary" data-open="fotos"><span class="dot"></span>Fotos</button>
        <button class="pill" data-open="brief"><span class="dot"></span>Brief</button>
        <button class="pill warn" data-open="surprise"><span class="dot"></span>Überraschung</button>
        <button class="pill secondary" data-open="musik"><span class="dot"></span>Musik</button>
        <button class="pill lock" id="lockBtn"><span class="dot"></span>Sperren</button>
      </nav>
    </div>
  </header>

  <main class="wrap">
    <div class="grid">

      <!-- LEFT -->
      <section class="card">
        <div class="cardInner">
          <div class="titleRow">
            <span class="badge">Can ❤ Aylin</span>
            <span class="badge" id="startBadge">Seit: —</span>
            <span class="badge" id="onlineBadge">—</span>
          </div>

          <h2 class="h2">Unser Datum ✨</h2>
          <p class="small">
            Ein Ort, der sagt: <b>„Wir gehören zusammen.“</b>  
            Nicht laut — sondern ruhig, sicher und echt.
          </p>

          <div class="hr"></div>

          <div style="display:flex;gap:10px;flex-wrap:wrap">
            <button class="btn" id="copyLink">Seite kopieren 🔗</button>
            <button class="btn gray" data-open="brief">Unser Brief 💌</button>
            <button class="btn gray" data-open="fotos">Fotos öffnen 📷</button>
          </div>

          <div class="kpis" aria-label="Zähler">
            <div class="kpi">
              <div class="n" id="daysTogether">—</div>
              <div class="l">Tage zusammen</div>
            </div>
            <div class="kpi">
              <div class="n" id="hoursTogether">—</div>
              <div class="l">Stunden (seitdem)</div>
            </div>
            <div class="kpi">
              <div class="n" id="photosCount">—</div>
              <div class="l">Fotos im Album</div>
            </div>
          </div>

          <div class="hr"></div>

          <div class="small" style="white-space:pre-line">
Aylin,

du bist nicht nur „Liebe“ — du bist mein ruhiger Ort im Chaos.
Wenn du da bist, fühlt sich alles richtiger an.

Ich will, dass du dich jeden Tag sicher fühlst:
Sicher in meiner Stimme.
Sicher in meinen Händen.
Sicher in dem Satz: „Ich bleibe.“

Und falls du mal vergisst, wie besonders du bist:
Ich erinnere dich — sanft, aber immer.

— Wir. Can ❤ Aylin
          </div>

          <div class="hr"></div>

          <div style="display:flex;gap:10px;flex-wrap:wrap">
            <button class="btn" id="copyLetter">Brief kopieren ✨</button>
            <button class="btn gray" data-open="surprise">Überraschung öffnen 🎁</button>
          </div>
        </div>
      </section>

      <!-- RIGHT -->
      <section class="card">
        <div class="cardInner">
          <div class="titleRow">
            <span class="badge">Fotos</span>
            <span class="badge" id="lastSync">Noch nicht geladen</span>
          </div>

          <h2 class="h2">Unsere Fotos 📷</h2>
          <p class="small">
            Lädt automatisch aus eurem Google-Drive-Ordner. Tippe auf ein Bild, um es groß zu öffnen.
          </p>

          <div class="hr"></div>

          <div class="statusLine" id="netLine">
            <span class="statusDot" id="netDot" style="background:var(--warn)"></span>
            <span class="statusText" id="netText">Verbindung wird geprüft…</span>
          </div>

          <div class="hr"></div>

          <div style="display:flex;gap:10px;flex-wrap:wrap;align-items:center">
            <button class="btn good" id="refreshPhotos">Fotos aktualisieren ↻</button>
            <button class="btn gray" id="howUpload">Wie laden wir neue Fotos hoch?</button>
          </div>

          <div class="hr"></div>

          <div class="gallery" id="gallery" aria-label="Galerie"></div>

          <div class="hr"></div>
          <div class="tiny">
            Falls Fotos manchmal „weiß/leer“ sind: Das ist fast immer ein Drive-Freigabeproblem.
            Der Drive-Ordner muss auf <b>„Jeder mit Link kann ansehen“</b> stehen.
          </div>
        </div>
      </section>

    </div>
  </main>

  <!-- Overlay / Modals -->
  <div class="overlay" id="overlay" aria-hidden="true">
    <div class="modal" role="dialog" aria-modal="true" aria-labelledby="modalTitle">
      <div class="modalHead">
        <div class="modalTitle" id="modalTitle">Fenster</div>
        <button class="close" id="closeModal">Schließen ✕</button>
      </div>
      <div class="modalBody" id="modalBody"></div>
    </div>
  </div>

  <!-- Toast -->
  <div class="toast" id="toast">Kopiert ✅</div>

  <script>
    /**********************
     * 1) KONFIGURATION
     **********************/
    const CONFIG = {
      // 🔐 Şifre: burayı değiştir
      PASSWORD: "canaylin1004",

      // 📅 Başlangıç tarihi
      START_DATE: "2025-04-10T00:00:00+02:00",

      // ✅ Apps Script Web-App URL (JSON veriyor)
      SCRIPT_URL: "https://script.google.com/macros/s/AKfycbz89OA07y8Onrq20RsoMGxjfYM7P0QEGL5NFeymsM0QH2PWs8jgle10-rngXybNSPLzcg/exec",

      // kaç foto thumbnail
      MAX_THUMBS: 9,

      // Spotify embed (istersen playlist/track değiştir)
      SPOTIFY_EMBED: "https://open.spotify.com/embed/track/2lR6kgMLGS0zdWvVSdnb7h"
    };

    /**********************
     * 2) HELPERS
     **********************/
    const $ = (q, el=document) => el.querySelector(q);
    const $$ = (q, el=document) => [...el.querySelectorAll(q)];

    function escapeHtml(s){
      return (s||"")
        .replace(/&/g,"&amp;")
        .replace(/</g,"&lt;")
        .replace(/>/g,"&gt;")
        .replace(/"/g,"&quot;")
        .replace(/'/g,"&#039;");
    }

    function toast(msg="Kopiert ✅"){
      const t = $("#toast");
      t.textContent = msg;
      t.classList.add("show");
      clearTimeout(window.__toastT);
      window.__toastT = setTimeout(()=>t.classList.remove("show"), 1400);
    }

    async function copyText(text){
      try{
        await navigator.clipboard.writeText(text);
        toast("Kopiert ✅");
      }catch{
        const ta = document.createElement("textarea");
        ta.value = text;
        document.body.appendChild(ta);
        ta.select();
        document.execCommand("copy");
        ta.remove();
        toast("Kopiert ✅");
      }
    }

    function formatDEDate(d){
      try { return d.toLocaleDateString("de-DE"); } catch { return ""; }
    }

    function clamp(n, a, b){ return Math.max(a, Math.min(b, n)); }

    /**********************
     * 3) PASSWORD GATE
     **********************/
    const gate = $("#gate");
    const pw = $("#pw");
    const unlockBtn = $("#unlockBtn");
    const lockBtn = $("#lockBtn");

    function showGate(){
      gate.style.display = "flex";
      gate.setAttribute("aria-hidden","false");
      setTimeout(()=>pw.focus(), 40);
    }
    function hideGate(){
      gate.style.display = "none";
      gate.setAttribute("aria-hidden","true");
    }
    function isUnlocked(){
      return sessionStorage.getItem("unlocked") === "1";
    }
    function unlock(){
      sessionStorage.setItem("unlocked","1");
      hideGate();
    }
    function lock(){
      sessionStorage.removeItem("unlocked");
      showGate();
    }

    unlockBtn.addEventListener("click", () => {
      if ((pw.value||"").trim() === CONFIG.PASSWORD) {
        unlock();
      } else {
        pw.value = "";
        toast("Falsches Passwort ❌");
        pw.focus();
      }
    });
    pw.addEventListener("keydown", (e) => {
      if(e.key === "Enter") unlockBtn.click();
    });
    lockBtn.addEventListener("click", () => {
      lock();
      toast("Gesperrt 🔒");
    });

    if(!isUnlocked()) showGate(); else hideGate();

    /**********************
     * 4) KPI / ONLINE
     **********************/
    const startDate = new Date(CONFIG.START_DATE);
    $("#startBadge").textContent = "Seit: " + formatDEDate(startDate);

    function setNet(ok, text){
      $("#netDot").style.background = ok ? "var(--good)" : "var(--warn)";
      $("#netText").textContent = text;
    }

    function tick(){
      const now = new Date();
      const diffMs = Math.max(0, now - startDate);
      const days = Math.floor(diffMs / 86400000);
      const hours = Math.floor(diffMs / 3600000);
      $("#daysTogether").textContent = days.toLocaleString("de-DE");
      $("#hoursTogether").textContent = hours.toLocaleString("de-DE");

      const online = navigator.onLine;
      $("#onlineBadge").textContent = online ? "Online" : "Offline";
      $("#onlineBadge").style.borderColor = online ? "rgba(97,255,176,.35)" : "rgba(255,209,102,.35)";
      $("#onlineBadge").style.color = online ? "rgba(97,255,176,.92)" : "rgba(255,209,102,.92)";
    }
    tick();
    setInterval(tick, 1000);

    window.addEventListener("online", ()=>{ setNet(true, "Online — verbinde neu…"); loadPhotos(true); });
    window.addEventListener("offline", ()=> setNet(false, "Offline — warte auf Verbindung…"));

    /**********************
     * 5) OVERLAY MODALS
     **********************/
    const overlay = $("#overlay");
    const modalTitle = $("#modalTitle");
    const modalBody = $("#modalBody");
    const closeModal = $("#closeModal");

    function openModal(title, html){
      modalTitle.textContent = title;
      modalBody.innerHTML = html;
      overlay.classList.add("show");
      overlay.setAttribute("aria-hidden","false");
      setTimeout(()=>closeModal.focus(), 40);
    }
    function close(){
      overlay.classList.remove("show");
      overlay.setAttribute("aria-hidden","true");
      modalBody.innerHTML = "";
      document.onkeydown = null;
    }
    closeModal.addEventListener("click", close);
    overlay.addEventListener("click", (e)=>{ if(e.target === overlay) close(); });
    document.addEventListener("keydown", (e)=>{ if(e.key === "Escape" && overlay.classList.contains("show")) close(); });

    $$(".pill[data-open]").forEach(btn=>{
      btn.addEventListener("click", ()=>{
        const key = btn.getAttribute("data-open");

        if(key === "start"){
          openModal("Start ✨", `
            <div class="small" style="white-space:pre-line">
Willkommen in unserem kleinen Universum.

<b>Drei Dinge, die ich dir nie vergessen lasse:</b>
• Du bist genug — auch an Tagen, an denen du dich klein fühlst.
• Du musst nicht perfekt sein, um geliebt zu werden.
• Ich will dich nicht nur an guten Tagen — ich will dich immer.

<div class="hr"></div>
<button class="btn good" onclick="document.querySelector('[data-open=fotos]').click()">Zu den Fotos ↗</button>
            </div>
          `);
        }

        if(key === "fotos"){
          openModal("Fotos 📷", `
            <div class="small">
              <b>So ladet ihr neue Fotos hoch:</b>
              <ol>
                <li>Öffnet euren Google-Drive-Ordner (den, den das Script liest).</li>
                <li>Ladet dort neue Bilder hoch (JPG/PNG/WebP).</li>
                <li>Öffnet diese Seite neu oder klickt auf <b>„Fotos aktualisieren“</b>.</li>
              </ol>

              <div class="hr"></div>

              <b>Wichtig (damit nichts leer/weiß ist):</b>
              <ul>
                <li>Drive-Ordner: <b>„Jeder mit Link kann ansehen“</b></li>
                <li>Keine „nur ich“-Bilder</li>
              </ul>

              <div class="hr"></div>
              <div style="display:flex;gap:10px;flex-wrap:wrap">
                <button class="btn good" onclick="window.__refreshPhotos && window.__refreshPhotos(true)">Jetzt aktualisieren ↻</button>
                <button class="btn gray" onclick="window.open('${CONFIG.SCRIPT_URL}','_blank')">JSON prüfen ↗</button>
              </div>
            </div>
          `);
        }

        if(key === "brief"){
          const letter = $("#copyLetter").closest(".card").querySelector(".small").textContent.trim();
          openModal("Unser Brief 💌", `
            <div class="small" style="white-space:pre-line">${escapeHtml(letter)}</div>
            <div class="hr"></div>
            <div style="display:flex;gap:10px;flex-wrap:wrap">
              <button class="btn" onclick="copyText(document.querySelector('.modalBody .small').textContent)">Brief kopieren ✨</button>
              <button class="btn gray" onclick="close()">Schließen</button>
            </div>
          `);
        }

        if(key === "surprise"){
          openModal("Überraschung 🎁", `
            <div class="small">
              Wenn du das gerade liest, dann bist du in unserem kleinen Geheim-Ort. ❤<br><br>

              <b>Heute ist dein Reminder:</b>
              <ul>
                <li>Du bist wunderschön — auch ohne perfekten Tag.</li>
                <li>Dein Herz ist selten. Genau deshalb liebe ich dich.</li>
                <li>Du musst nichts beweisen. Du bist mein Lieblingsmensch.</li>
              </ul>

              <div class="hr"></div>

              <div style="display:flex;gap:10px;flex-wrap:wrap">
                <button class="btn good" onclick="toast('Ich liebe dich ❤')">Sag es leise ❤</button>
                <button class="btn" onclick="toast('Du bist mein Zuhause ✨')">Sag es groß ✨</button>
                <button class="btn gray" onclick="document.querySelector('[data-open=musik]').click()">Musik an 🎧</button>
              </div>
            </div>
          `);
        }

        if(key === "musik"){
          openModal("Musik 🎧", `
            <div class="small">
              Mach kurz Musik an — und stell dir vor, wir laufen Hand in Hand irgendwo durch die Stadt.<br><br>
              <div class="hr"></div>
              <iframe style="border-radius:18px;border:1px solid rgba(255,255,255,.16);width:100%;height:152px"
                src="${CONFIG.SPOTIFY_EMBED}"
                allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture"
                loading="lazy"></iframe>
              <div class="hr"></div>
              <div class="tiny">
                Willst du Ayliva/Mero ganz genau? Dann schick mir EIN Spotify Track/Playlist Link,
                ich setze ihn 1:1 hier rein.
              </div>
            </div>
          `);
        }
      });
    });

    /**********************
     * 6) COPY BUTTONS
     **********************/
    $("#copyLink").addEventListener("click", ()=>copyText(location.href));
    $("#copyLetter").addEventListener("click", ()=>{
      const letter = $("#copyLetter").closest(".card").querySelector(".small").textContent;
      copyText(letter);
    });

    /**********************
     * 7) PHOTOS: Robust fetch (timeout + retry) + lightbox
     **********************/
    const gallery = $("#gallery");
    const photosCount = $("#photosCount");
    const lastSync = $("#lastSync");
    const refreshBtn = $("#refreshPhotos");
    const howUpload = $("#howUpload");

    let ITEMS = [];
    let lbIndex = 0;

    function safeName(name){
      return (name||"")
        .replace(/\.[a-z0-9]+$/i,"")
        .replace(/[_-]+/g," ")
        .trim();
    }

    function renderGallery(){
      gallery.innerHTML = "";
      const shown = ITEMS.slice(0, CONFIG.MAX_THUMBS);

      if(shown.length === 0){
        gallery.innerHTML = `
          <div class="thumb" style="grid-column:1/-1;aspect-ratio:auto;min-height:120px;cursor:default">
            <div class="ph">
              Keine Fotos gefunden…<br>
              <span style="font-size:11px;opacity:.78">Oder keine Berechtigung im Drive-Ordner.</span>
            </div>
          </div>`;
        return;
      }

      shown.forEach((it, i)=>{
        const el = document.createElement("div");
        el.className = "thumb";
        el.innerHTML = `
          <div class="ph">Laden…</div>
          <img loading="lazy" alt="${escapeHtml(it.name||'Foto')}" style="display:none" />
          <div class="cap">${escapeHtml(safeName(it.name))}</div>
        `;
        const img = el.querySelector("img");
        const ph = el.querySelector(".ph");

        // cache-bust
        const url = (it.url||"") + (it.url && it.url.includes("?") ? "&" : "?") + "v=" + encodeURIComponent(it.ts||Date.now());
        img.src = url;

        img.onload = () => { ph.style.display="none"; img.style.display="block"; };
        img.onerror = () => {
          ph.innerHTML = "Kann nicht laden.<br><span style='font-size:11px;opacity:.78'>Drive Freigabe prüfen</span>";
        };

        el.addEventListener("click", ()=>openLightbox(i));
        gallery.appendChild(el);
      });
    }

    function openLightbox(index){
      lbIndex = clamp(index, 0, ITEMS.length-1);
      const it = ITEMS[lbIndex];
      const dt = it.ts ? new Date(it.ts) : null;

      openModal("Foto "+(lbIndex+1)+" / "+ITEMS.length+" 📷", `
        <div class="lightbox">
          <div class="lbBar">
            <div class="lbMeta">
              <b>${escapeHtml(it.name||"Foto")}</b>
              ${dt ? " • " + dt.toLocaleString("de-DE") : ""}
            </div>
            <div class="lbControls">
              <button class="btn gray" onclick="window.__lbPrev()">← Zurück</button>
              <button class="btn gray" onclick="window.__lbNext()">Weiter →</button>
              <button class="btn" onclick="window.__lbOpen()">Im neuen Tab öffnen ↗</button>
              <button class="btn" onclick="window.__lbCopy()">Link kopieren 🔗</button>
            </div>
          </div>

          <div class="lbFrame">
            <img id="lbImg" alt="${escapeHtml(it.name||'Foto')}" />
          </div>

          <div class="tiny">Tipp: Pfeiltasten ← → funktionieren auch.</div>
        </div>
      `);

      const img = $("#lbImg", modalBody);
      const url = (it.url||"") + (it.url && it.url.includes("?") ? "&" : "?") + "v=" + encodeURIComponent(it.ts||Date.now());
      img.src = url;

      img.onerror = () => {
        img.replaceWith(Object.assign(document.createElement("div"), {
          style: "padding:18px;color:rgba(255,255,255,.78);text-align:center;font-weight:800",
          innerHTML: "Dieses Bild kann nicht geladen werden.<br><br><span style='color:rgba(255,255,255,.62)'>Meistens fehlt die Drive-Freigabe („Jeder mit Link“).</span>"
        }));
      };

      window.__lbPrev = () => openLightbox((lbIndex-1+ITEMS.length)%ITEMS.length);
      window.__lbNext = () => openLightbox((lbIndex+1)%ITEMS.length);
      window.__lbOpen = () => window.open(it.url, "_blank");
      window.__lbCopy = () => copyText(it.url);

      document.onkeydown = (e) => {
        if(!overlay.classList.contains("show")) return;
        if(e.key === "ArrowLeft") window.__lbPrev();
        if(e.key === "ArrowRight") window.__lbNext();
      };
    }

    // fetch with timeout + retry
    async function fetchWithTimeout(url, ms){
      const ctrl = new AbortController();
      const t = setTimeout(()=>ctrl.abort(), ms);
      try{
        const res = await fetch(url, { cache:"no-store", signal: ctrl.signal });
        return res;
      } finally {
        clearTimeout(t);
      }
    }

    async function loadPhotos(isAuto=false){
      if(!navigator.onLine){
        setNet(false, "Offline — warte auf Verbindung…");
        lastSync.textContent = "Offline";
        return;
      }

      setNet(true, "Online — lade Fotos…");
      lastSync.textContent = "Lade…";

      const maxTries = 5;
      let lastErr = null;

      for(let attempt=1; attempt<=maxTries; attempt++){
        try{
          // anti-cache param (mobil bazen cache yapıyor)
          const url = CONFIG.SCRIPT_URL + (CONFIG.SCRIPT_URL.includes("?") ? "&" : "?") + "t=" + Date.now();

          const res = await fetchWithTimeout(url, 10000); // 10s timeout
          if(!res.ok) throw new Error("HTTP "+res.status);

          const data = await res.json();
          const items = Array.isArray(data.items) ? data.items : [];

          items.sort((a,b)=>(b.ts||0)-(a.ts||0));
          ITEMS = items.filter(x => typeof x?.url === "string" && x.url.includes("drive.google.com"));

          photosCount.textContent = ITEMS.length.toLocaleString("de-DE");
          lastSync.textContent = "Aktualisiert: " + new Date().toLocaleTimeString("de-DE");
          setNet(true, "Online — Fotos geladen ✅");

          renderGallery();
          return;
        }catch(err){
          lastErr = err;
          console.warn("loadPhotos attempt", attempt, err);

          // küçük bekleme (backoff)
          const wait = 400 * attempt * attempt;
          lastSync.textContent = "Fehler… neuer Versuch ("+attempt+"/"+maxTries+")";
          setNet(true, "Online — versuche erneut… ("+attempt+"/"+maxTries+")");

          await new Promise(r=>setTimeout(r, wait));
        }
      }

      console.error(lastErr);
      setNet(true, "Online — aber Fotos konnten nicht geladen werden ❌");
      lastSync.textContent = "Fehler beim Laden";
      toast("Fotos konnten nicht geladen werden ❌");
      renderGallery();
    }

    window.__refreshPhotos = loadPhotos;

    refreshBtn.addEventListener("click", ()=>loadPhotos(false));
    howUpload.addEventListener("click", ()=>document.querySelector('[data-open=fotos]').click());

    // initial load
    loadPhotos(true);

    // auto refresh every 60s (only if online)
    setInterval(()=>loadPhotos(true), 60000);

    /**********************
     * 8) tiny: link copy
     **********************/
    // done
  </script>
</body>
</html>
