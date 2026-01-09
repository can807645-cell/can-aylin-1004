<!doctype html>
<html lang="de">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Can ❤ Aylin — Unser Ort</title>
  <meta name="description" content="Ein privater Ort für Can & Aylin: Fotos, Erinnerungen, Liebe." />

  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Manrope:wght@400;600;700;800&display=swap" rel="stylesheet">

  <style>
    :root{
      --bg0:#080611;
      --bg1:#140a2b;
      --bg2:#2a0f3a;

      --glass: rgba(255,255,255,.08);
      --glass2: rgba(255,255,255,.12);
      --stroke: rgba(255,255,255,.14);
      --stroke2: rgba(255,255,255,.22);

      --text: rgba(255,255,255,.92);
      --muted: rgba(255,255,255,.72);
      --muted2: rgba(255,255,255,.55);

      --pink:#ff4fd8;
      --vio:#9b5cff;
      --cyan:#4dd6ff;
      --good:#61ffb0;
      --warn:#ffd166;
      --bad:#ff6b6b;

      --shadow: 0 18px 60px rgba(0,0,0,.55);
      --shadow2: 0 10px 26px rgba(0,0,0,.38);
      --r:18px;
      --r2:26px;
      --focus: 0 0 0 3px rgba(155,92,255,.35);
    }

    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0;
      font-family: "Manrope", system-ui, -apple-system, Segoe UI, Roboto, Arial;
      color:var(--text);
      background:
        radial-gradient(1200px 700px at 10% -10%, rgba(155,92,255,.35), transparent 60%),
        radial-gradient(900px 600px at 90% 5%, rgba(255,79,216,.28), transparent 55%),
        radial-gradient(700px 500px at 60% 110%, rgba(77,214,255,.18), transparent 60%),
        linear-gradient(180deg, var(--bg0), var(--bg1) 55%, var(--bg2));
      overflow-x:hidden;
    }

    .wrap{max-width:1100px;margin:0 auto;padding:18px 14px 44px; position:relative; z-index:2}
    .top{
      position:sticky; top:10px; z-index:50;
      border:1px solid rgba(255,255,255,.10);
      background: linear-gradient(180deg, rgba(8,6,16,.72), rgba(8,6,16,.38));
      backdrop-filter: blur(14px);
      border-radius: 22px;
      box-shadow: var(--shadow2);
    }
    .topInner{display:flex;align-items:center;gap:12px;padding:12px 14px}
    .brand{display:flex;align-items:center;gap:10px;min-width:220px}
    .logo{
      width:40px;height:40px;border-radius:14px;
      background: radial-gradient(circle at 35% 25%, rgba(255,79,216,.95), rgba(155,92,255,.95) 55%, rgba(77,214,255,.45));
      border:1px solid rgba(255,255,255,.16);
      box-shadow: 0 12px 26px rgba(155,92,255,.18);
      flex:0 0 auto;
    }
    .brand h1{margin:0;font-size:14px;letter-spacing:.2px}
    .brand p{margin:2px 0 0;color:var(--muted2);font-size:12px}

    .nav{margin-left:auto;display:flex;gap:8px;flex-wrap:wrap;justify-content:flex-end}
    .pill{
      border:1px solid rgba(255,255,255,.14);
      background: rgba(255,255,255,.06);
      color:var(--text);
      padding:8px 11px;border-radius:999px;
      cursor:pointer;
      transition: transform .16s ease, border-color .16s ease, background .16s ease;
      user-select:none;
      display:inline-flex;align-items:center;gap:8px;
      font-weight:800;
    }
    .pill:hover{transform: translateY(-1px);border-color:rgba(255,255,255,.22); background: rgba(255,255,255,.09)}
    .pill:focus{outline:none;box-shadow:var(--focus)}
    .pill .dot{width:7px;height:7px;border-radius:50%;background:var(--pink);box-shadow:0 0 0 4px rgba(255,79,216,.16)}
    .pill.secondary .dot{background:var(--cyan);box-shadow:0 0 0 4px rgba(77,214,255,.14)}
    .pill.warn .dot{background:var(--warn);box-shadow:0 0 0 4px rgba(255,209,102,.14)}
    .pill.lock .dot{background:var(--muted2);box-shadow:0 0 0 4px rgba(255,255,255,.12)}

    .grid{display:grid;grid-template-columns: 1.1fr .9fr; gap:14px; margin-top:14px}
    @media (max-width: 860px){.grid{grid-template-columns:1fr}.brand{min-width:auto}}

    .card{
      border:1px solid rgba(255,255,255,.12);
      background: linear-gradient(180deg, rgba(255,255,255,.09), rgba(255,255,255,.05));
      border-radius: 26px;
      box-shadow: var(--shadow2);
      overflow:hidden;
      position:relative;
    }
    .card::before{
      content:"";
      position:absolute;inset:-2px;
      background:
        radial-gradient(520px 180px at 15% 0%, rgba(155,92,255,.16), transparent 60%),
        radial-gradient(520px 180px at 85% 0%, rgba(255,79,216,.12), transparent 55%);
      pointer-events:none;
      opacity:.95;
    }
    .inner{position:relative;padding:16px}

    .titleRow{display:flex;align-items:center;gap:10px;flex-wrap:wrap;justify-content:space-between}
    .badge{
      font-size:12px;font-weight:800;
      padding:6px 10px;border-radius:999px;
      border:1px solid rgba(255,255,255,.14);
      background: rgba(0,0,0,.18);
      color: rgba(255,255,255,.80);
      backdrop-filter: blur(10px);
    }
    .h2{margin:10px 0 0;font-size:18px;letter-spacing:.2px}
    .small{color:var(--muted);font-size:13px;font-weight:600;line-height:1.6}
    .hr{height:1px;background:rgba(255,255,255,.10);margin:12px 0}

    .btnRow{display:flex;gap:10px;flex-wrap:wrap}
    .btn{
      border:1px solid rgba(255,255,255,.14);
      background: rgba(255,255,255,.06);
      padding:10px 12px;border-radius:14px;
      color:var(--text);
      cursor:pointer;
      transition: transform .16s ease, border-color .16s ease, background .16s ease;
      display:inline-flex;align-items:center;gap:8px;
      font-weight:900;
    }
    .btn:hover{transform: translateY(-1px);border-color:rgba(255,255,255,.22);background:rgba(255,255,255,.09)}
    .btn.good{border-color: rgba(97,255,176,.28); background: rgba(97,255,176,.10)}
    .btn.hot{border-color: rgba(255,79,216,.28); background: rgba(255,79,216,.10)}
    .btn:focus{outline:none;box-shadow:var(--focus)}

    .kpis{display:grid;grid-template-columns: repeat(3,1fr); gap:10px; margin-top:12px}
    .kpi{
      padding:12px;border-radius:18px;
      border:1px solid rgba(255,255,255,.12);
      background: rgba(0,0,0,.14);
    }
    .kpi .n{font-size:20px;font-weight:900;letter-spacing:.2px}
    .kpi .l{font-size:12px;color:var(--muted2);font-weight:800}

    /* Gallery */
    .gallery{display:grid;grid-template-columns: repeat(3, 1fr); gap:10px; margin-top:10px}
    @media (max-width:520px){.gallery{grid-template-columns: repeat(2, 1fr)}}
    .thumb{
      border-radius:18px;
      overflow:hidden;
      border:1px solid rgba(255,255,255,.12);
      background: rgba(0,0,0,.16);
      aspect-ratio: 1/1;
      position:relative;
      cursor:pointer;
      transition: transform .16s ease, border-color .16s ease;
    }
    .thumb:hover{transform: translateY(-2px);border-color:rgba(255,255,255,.22)}
    .thumb img{width:100%;height:100%;object-fit:cover;display:block}
    .thumb .ph{
      position:absolute;inset:0;display:grid;place-items:center;
      color:rgba(255,255,255,.65);
      font-size:12px;font-weight:900;
      text-align:center;
      padding:10px;
      background:
        radial-gradient(circle at 30% 20%, rgba(255,79,216,.12), transparent 60%),
        radial-gradient(circle at 70% 20%, rgba(155,92,255,.12), transparent 60%),
        rgba(0,0,0,.14);
    }
    .thumb .cap{
      position:absolute;left:8px;right:8px;bottom:8px;
      padding:6px 8px;border-radius:12px;
      background: rgba(0,0,0,.35);
      border:1px solid rgba(255,255,255,.12);
      font-size:11px;color:rgba(255,255,255,.82);
      white-space:nowrap;overflow:hidden;text-overflow:ellipsis;
      backdrop-filter: blur(8px);
      font-weight:900;
    }

    /* Modal (büyüyen sayfa + karartı) */
    .overlay{
      position:fixed;inset:0;z-index:200;
      background: rgba(0,0,0,.62);
      display:none;align-items:center;justify-content:center;
      padding:16px;
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

    /* Lightbox */
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
    }
    .lbBar{display:flex;align-items:center;gap:10px;flex-wrap:wrap;justify-content:space-between;margin-bottom:10px}
    .lbMeta{color:rgba(255,255,255,.82);font-size:12px;font-weight:900}
    .lbControls{display:flex;gap:8px;flex-wrap:wrap}

    /* Password gate */
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
    .gateBox p{margin:0;color:var(--muted);font-weight:700;line-height:1.55}
    .field{margin-top:14px;display:flex;gap:10px;flex-wrap:wrap}
    .inp{
      flex:1; min-width:200px;
      border-radius:14px;
      padding:12px 12px;
      border:1px solid rgba(255,255,255,.14);
      background: rgba(0,0,0,.22);
      color:var(--text);
      outline:none;
      font-weight:900;
    }
    .inp:focus{box-shadow:var(--focus);border-color:rgba(155,92,255,.45)}
    .hint{margin-top:10px;color:rgba(255,255,255,.62);font-size:12px;font-weight:700}
    .toast{
      position:fixed;left:50%;bottom:18px;transform:translateX(-50%);
      background: rgba(0,0,0,.74);
      border:1px solid rgba(255,255,255,.16);
      color:rgba(255,255,255,.92);
      padding:10px 12px;border-radius:14px;
      box-shadow: var(--shadow2);
      display:none;
      z-index:350;
      font-weight:900;
    }
    .toast.show{display:block;animation: pop .18s ease}
    @keyframes pop{from{transform:translateX(-50%) translateY(8px);opacity:0}to{transform:translateX(-50%) translateY(0);opacity:1}}
  </style>
</head>

<body>

  <!-- Passwort -->
  <div class="gate" id="gate">
    <div class="gateBox">
      <div style="display:flex;align-items:center;gap:12px">
        <div class="logo"></div>
        <div>
          <h2>Nur für uns zwei ❤</h2>
          <p>Dieser Ort gehört uns. Für Erinnerungen, Fotos und das Gefühl: <b>„Wir.“</b></p>
        </div>
      </div>

      <div class="field">
        <input class="inp" id="pw" type="password" placeholder="Passwort…" autocomplete="current-password" />
        <button class="btn good" id="unlockBtn">Öffnen ✨</button>
      </div>

      <div class="hint">
        Tipp: Passwort steht im Code bei <b>SITE_PASSWORD</b>.
      </div>
    </div>
  </div>

  <div class="wrap">

    <header class="top">
      <div class="topInner">
        <div class="brand">
          <div class="logo"></div>
          <div>
            <h1>Can ❤ Aylin</h1>
            <p>Unser gemeinsamer Ort — nur wir.</p>
          </div>
        </div>

        <nav class="nav">
          <button class="pill" data-open="start"><span class="dot"></span>Start</button>
          <button class="pill secondary" data-open="fotos"><span class="dot"></span>Fotos</button>
          <button class="pill" data-open="brief"><span class="dot"></span>Brief</button>
          <button class="pill warn" data-open="surprise"><span class="dot"></span>Überraschung</button>
          <button class="pill secondary" data-open="musik"><span class="dot"></span>Musik</button>
          <button class="pill lock" id="lockBtn"><span class="dot"></span>Sperren</button>
        </nav>
      </div>
    </header>

    <main class="grid">

      <section class="card">
        <div class="inner">
          <div class="titleRow">
            <div style="display:flex;gap:8px;flex-wrap:wrap">
              <span class="badge">Can ❤ Aylin</span>
              <span class="badge" id="sinceBadge">Seit: 10.04.2025</span>
              <span class="badge" id="netBadge">Online</span>
            </div>
            <div class="btnRow">
              <button class="btn" id="copyLink">Link kopieren 🔗</button>
              <button class="btn hot" data-open="brief">Herz öffnen 💌</button>
            </div>
          </div>

          <h2 class="h2">Für dich, Aylin ✨</h2>
          <p class="small">
            Du bist nicht nur „Liebe“ — du bist mein Ruhepunkt.  
            Du bist die Person, bei der sich mein Kopf leiser anfühlt und mein Herz sicherer.  
            Und egal wie der Tag war: <b>Du bist genug. Mehr als genug.</b>
          </p>

          <div class="hr"></div>

          <div class="kpis">
            <div class="kpi"><div class="n" id="daysTogether">—</div><div class="l">Tage zusammen</div></div>
            <div class="kpi"><div class="n" id="hoursTogether">—</div><div class="l">Stunden „wir“</div></div>
            <div class="kpi"><div class="n" id="photosCount">—</div><div class="l">Fotos im Album</div></div>
          </div>

          <div class="hr"></div>

          <p class="small">
            Ich will, dass du dich jeden Tag gut fühlst — nicht weil alles perfekt ist,  
            sondern weil du jemanden hast, der dich hält, wenn es schwer wird.  
            <b>Ich bin da. Immer.</b>
          </p>
        </div>
      </section>

      <section class="card">
        <div class="inner">
          <div class="titleRow">
            <div style="display:flex;gap:8px;flex-wrap:wrap">
              <span class="badge">Fotos</span>
              <span class="badge" id="lastSync">Noch nicht geladen</span>
            </div>
            <button class="btn good" id="refreshPhotos">Aktualisieren ↻</button>
          </div>

          <h2 class="h2">Unsere Erinnerungen 📷</h2>
          <p class="small">
            Tippe auf ein Foto, um es groß zu öffnen.  
            (Wenn mal eins nicht lädt: Drive-Freigabe „Jeder mit Link“ ist Pflicht.)
          </p>

          <div class="gallery" id="gallery"></div>

          <div class="hr"></div>
          <p class="small" style="color:var(--muted2)">
            Upload-Weg: Foto in euren Google-Drive-Ordner hochladen → hier „Aktualisieren“ drücken.
          </p>
        </div>
      </section>

    </main>
  </div>

  <!-- Modal -->
  <div class="overlay" id="overlay" aria-hidden="true">
    <div class="modal" role="dialog" aria-modal="true">
      <div class="modalHead">
        <div class="modalTitle" id="modalTitle">Fenster</div>
        <button class="close" id="closeModal">Schließen ✕</button>
      </div>
      <div class="modalBody" id="modalBody"></div>
    </div>
  </div>

  <div class="toast" id="toast">Ok ✅</div>

  <script>
    /**********************
     * KONFIG (nur hier anfassen)
     **********************/
    const SITE_PASSWORD = "canaylin"; // ← istediğin şifreyi yaz
    const START_DATE = "2025-04-10T00:00:00+02:00";

    // senin Apps Script /exec linkin:
    const SCRIPT_URL = "https://script.google.com/macros/s/AKfycbz89OA07y8Onrq20RsoMGxjfYM7P0QEGL5NFeymsM0QH2PWs8jgle10-rngXybNSPLzcg/exec";

    const MAX_THUMBS = 9;

    /**********************
     * Helpers
     **********************/
    const $ = (q, el=document)=>el.querySelector(q);
    const $$ = (q, el=document)=>[...el.querySelectorAll(q)];
    const clamp = (n,a,b)=>Math.max(a,Math.min(b,n));

    function toast(msg){
      const t = $("#toast");
      t.textContent = msg;
      t.classList.add("show");
      clearTimeout(window.__tt);
      window.__tt = setTimeout(()=>t.classList.remove("show"), 1400);
    }

    async function copyText(txt){
      try{
        await navigator.clipboard.writeText(txt);
        toast("Kopiert ✅");
      }catch{
        toast("Kopieren nicht möglich");
      }
    }

    function escapeHtml(s){
      return (s||"")
        .replace(/&/g,"&amp;").replace(/</g,"&lt;").replace(/>/g,"&gt;")
        .replace(/"/g,"&quot;").replace(/'/g,"&#039;");
    }

    /**********************
     * Passwort
     **********************/
    const gate = $("#gate");
    $("#unlockBtn").addEventListener("click", ()=>{
      const v = ($("#pw").value||"").trim();
      if(v === SITE_PASSWORD){
        sessionStorage.setItem("unlocked","1");
        gate.style.display="none";
        toast("Willkommen ❤");
      }else{
        $("#pw").value = "";
        toast("Falsches Passwort ❌");
        $("#pw").focus();
      }
    });
    $("#pw").addEventListener("keydown", (e)=>{ if(e.key==="Enter") $("#unlockBtn").click(); });

    $("#lockBtn").addEventListener("click", ()=>{
      sessionStorage.removeItem("unlocked");
      gate.style.display="flex";
      toast("Gesperrt 🔒");
    });

    if(sessionStorage.getItem("unlocked")==="1") gate.style.display="none";

    /**********************
     * Sayaç
     **********************/
    const startDate = new Date(START_DATE);
    $("#sinceBadge").textContent = "Seit: " + startDate.toLocaleDateString("de-DE");

    function tick(){
      const now = new Date();
      const diff = Math.max(0, now - startDate);
      $("#daysTogether").textContent = Math.floor(diff/86400000).toLocaleString("de-DE");
      $("#hoursTogether").textContent = Math.floor(diff/3600000).toLocaleString("de-DE");

      const online = navigator.onLine;
      $("#netBadge").textContent = online ? "Online" : "Offline";
      $("#netBadge").style.borderColor = online ? "rgba(97,255,176,.30)" : "rgba(255,209,102,.30)";
    }
    tick();
    setInterval(tick, 1000);

    /**********************
     * Modal (büyüyen sayfa)
     **********************/
    const overlay = $("#overlay");
    const modalTitle = $("#modalTitle");
    const modalBody = $("#modalBody");

    function openModal(title, html){
      modalTitle.textContent = title;
      modalBody.innerHTML = html;
      overlay.classList.add("show");
      overlay.setAttribute("aria-hidden","false");
      setTimeout(()=>$("#closeModal").focus(), 50);
    }
    function closeModal(){
      overlay.classList.remove("show");
      overlay.setAttribute("aria-hidden","true");
      modalBody.innerHTML = "";
      document.onkeydown = null;
    }
    $("#closeModal").addEventListener("click", closeModal);
    overlay.addEventListener("click", (e)=>{ if(e.target === overlay) closeModal(); });
    document.addEventListener("keydown", (e)=>{ if(e.key==="Escape" && overlay.classList.contains("show")) closeModal(); });

    const PAGES = {
      start: ()=>`
        <div class="small" style="white-space:pre-line">
Willkommen in unserem Ort — nur für uns.

Aylin, du bist nicht „irgendwer“.
Du bist die Person, die aus einem normalen Tag etwas macht, das sich nach Zuhause anfühlt.

Wenn du zweifelst:
• Du bist wunderschön.
• Du bist wertvoll.
• Du bist geliebt — ohne Bedingungen.

<div class="hr"></div>
<button class="btn good" onclick="document.querySelector('[data-open=fotos]').click()">Zu den Fotos ↗</button>
        </div>
      `,
      brief: ()=>{
        const text = `Aylin,

ich liebe nicht nur dein Lächeln.
Ich liebe die Art, wie du fühlst.
Wie du echt bist.
Wie du auch dann weitermachst, wenn es schwer ist.

Du musst bei mir nichts beweisen.
Du bist genug — schon lange.
Und wenn du mal vergisst, wie besonders du bist:
Ich erinnere dich. Immer.

Ich will, dass du dich bei mir sicher fühlst:
Sicher in meiner Stimme,
sicher in meinen Händen,
sicher in dem Satz: „Ich bleibe.“

— Wir. Can ❤ Aylin`;
        return `
          <div class="small" style="white-space:pre-line">${escapeHtml(text)}</div>
          <div class="hr"></div>
          <button class="btn" onclick="navigator.clipboard.writeText(${JSON.stringify(text)}).then(()=>toast('Kopiert ✅')).catch(()=>toast('Nicht möglich'))">Brief kopieren ✨</button>
        `;
      },
      surprise: ()=>`
        <div class="small">
          <b>Überraschung für dich, Aylin:</b><br><br>
          Wenn du das gerade liest, dann sollst du nur eins wissen:
          <b>Du bist mein Lieblingsmensch.</b><br><br>

          <ul>
            <li>Du bist schön — auch ohne perfekten Tag.</li>
            <li>Du bist stark — auch wenn du müde bist.</li>
            <li>Du bist Liebe — und du verdienst Liebe.</li>
          </ul>

          <div class="hr"></div>
          <div class="btnRow">
            <button class="btn good" onclick="toast('Ich liebe dich ❤')">Sag es leise ❤</button>
            <button class="btn hot" onclick="toast('Du bist mein Zuhause ✨')">Sag es groß ✨</button>
          </div>
        </div>
      `,
      musik: ()=>`
        <div class="small">
          Wegen Copyright packen wir keine Songs direkt rein.
          Aber wir machen’s sauber & perfekt über Spotify.<br><br>

          <div class="btnRow">
            <a class="btn" target="_blank" rel="noopener" href="https://open.spotify.com/search/AYLIVA">Spotify: AYLIVA</a>
            <a class="btn" target="_blank" rel="noopener" href="https://open.spotify.com/search/MERO">Spotify: MERO</a>
          </div>

          <div class="hr"></div>

          <b>Optional:</b> Wenn du einen Spotify <b>Playlist-Link</b> hast, füge ihn unten ein.
          Dann wird er als Embed angezeigt.<br><br>

          <input class="inp" id="pl" placeholder="z.B. https://open.spotify.com/playlist/..." />
          <div class="btnRow" style="margin-top:10px">
            <button class="btn good" onclick="window.__setPlaylist()">Playlist anzeigen 🎧</button>
          </div>

          <div id="plBox" style="margin-top:12px"></div>
        </div>
      `,
      fotos: ()=>`
        <div class="small">
          <b>So ladet ihr neue Fotos hoch:</b>
          <ol>
            <li>Foto in euren Google-Drive-Ordner hochladen</li>
            <li>Ordner muss sein: <b>„Jeder mit Link kann ansehen“</b></li>
            <li>Zurück und „Aktualisieren“ drücken</li>
          </ol>

          <div class="hr"></div>
          <div class="btnRow">
            <button class="btn good" onclick="window.__refreshPhotos(true)">Jetzt aktualisieren ↻</button>
            <button class="btn" onclick="window.open(${JSON.stringify(SCRIPT_URL)}, '_blank')">JSON prüfen ↗</button>
          </div>
        </div>
      `
    };

    $$("[data-open]").forEach(btn=>{
      btn.addEventListener("click", ()=>{
        const key = btn.getAttribute("data-open");
        openModal(btn.textContent.trim(), PAGES[key] ? PAGES[key]() : "<div class='small'>Fehlt.</div>");
      });
    });

    /**********************
     * Spotify embed helper
     **********************/
    window.__setPlaylist = ()=>{
      const link = ($("#pl")?.value||"").trim();
      const box = $("#plBox");
      if(!box) return;

      // Accept playlist/track/album; build embed
      const m = link.match(/open\.spotify\.com\/(playlist|track|album)\/([a-zA-Z0-9]+)/);
      if(!m){
        box.innerHTML = `<div class="small" style="color:rgba(255,255,255,.75)">Bitte einen echten Spotify Link einfügen.</div>`;
        return;
      }
      const type = m[1], id = m[2];
      box.innerHTML = `
        <iframe style="border-radius:18px;border:1px solid rgba(255,255,255,.16);width:100%;height:${type==='track'?'152':'380'}px"
          src="https://open.spotify.com/embed/${type}/${id}"
          allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture"
          loading="lazy"></iframe>
      `;
    };

    /**********************
     * Foto sistemi: JSON + retry + Drive alternatifleri
     **********************/
    const gallery = $("#gallery");
    let ITEMS = [];

    function altUrls(url){
      const out = [];
      try{
        out.push(url);
        const m = String(url||"").match(/id=([a-zA-Z0-9_-]+)/);
        if(m){
          const id = m[1];
          out.push(`https://drive.google.com/uc?export=download&id=${id}`);
          out.push(`https://drive.google.com/thumbnail?id=${id}&sz=w2000`);
          out.push(`https://lh3.googleusercontent.com/d/${id}`);
        }
      }catch(e){}
      return out.filter(Boolean);
    }

    function safeName(name){
      return (name||"").replace(/\.[a-z0-9]+$/i,"").replace(/[_-]+/g," ").trim();
    }

    async function fetchWithTimeout(url, ms){
      const ctrl = new AbortController();
      const t = setTimeout(()=>ctrl.abort(), ms);
      try{
        return await fetch(url, { cache:"no-store", signal: ctrl.signal });
      } finally {
        clearTimeout(t);
      }
    }

    function renderGallery(){
      gallery.innerHTML = "";
      const shown = ITEMS.slice(0, MAX_THUMBS);

      $("#photosCount").textContent = ITEMS.length.toLocaleString("de-DE");

      if(shown.length === 0){
        gallery.innerHTML = `
          <div class="thumb" style="grid-column:1/-1;aspect-ratio:auto;min-height:120px;cursor:default">
            <div class="ph">Keine Fotos gefunden…<br><span style="font-size:11px;opacity:.8">Oder Drive-Freigabe fehlt.</span></div>
          </div>`;
        return;
      }

      shown.forEach((it, i)=>{
        const el = document.createElement("div");
        el.className = "thumb";
        el.innerHTML = `
          <div class="ph">Laden…</div>
          <img style="display:none" alt="${escapeHtml(it.name||'Foto')}" />
          <div class="cap">${escapeHtml(safeName(it.name))}</div>
        `;
        const img = el.querySelector("img");
        const ph = el.querySelector(".ph");

        const tries = altUrls(it.url);
        let k = 0;

        const tryNext = ()=>{
          if(k >= tries.length){
            ph.innerHTML = "Kann nicht laden.<br><span style='font-size:11px;opacity:.78'>Drive Freigabe prüfen</span>";
            return;
          }
          const u = tries[k++] + (tries[k-1].includes("?") ? "&" : "?") + "v=" + encodeURIComponent(it.ts||Date.now());
          img.src = u;
        };

        img.onload = ()=>{ ph.style.display="none"; img.style.display="block"; };
        img.onerror = ()=>tryNext();
        tryNext();

        el.addEventListener("click", ()=>openLightbox(i));
        gallery.appendChild(el);
      });
    }

    function openLightbox(index){
      const i = clamp(index, 0, ITEMS.length-1);
      const it = ITEMS[i];
      const tries = altUrls(it.url);

      openModal(`Foto ${i+1} / ${ITEMS.length} 📷`, `
        <div class="lbBar">
          <div class="lbMeta"><b>${escapeHtml(it.name||"Foto")}</b></div>
          <div class="lbControls">
            <button class="btn" onclick="window.__lbNav(-1)">←</button>
            <button class="btn" onclick="window.__lbNav(1)">→</button>
            <button class="btn good" onclick="window.open(${JSON.stringify(it.url)}, '_blank')">Neu öffnen ↗</button>
            <button class="btn" onclick="navigator.clipboard.writeText(${JSON.stringify(it.url)}).then(()=>toast('Kopiert ✅')).catch(()=>toast('Nicht möglich'))">Link kopieren 🔗</button>
          </div>
        </div>
        <div class="lbFrame"><img id="lbImg" alt="Foto"/></div>
      `);

      const img = $("#lbImg", modalBody);
      let k = 0;
      const tryNext = ()=>{
        if(k >= tries.length){
          img.replaceWith(Object.assign(document.createElement("div"), {
            style:"padding:18px;text-align:center;color:rgba(255,255,255,.78);font-weight:900",
            innerHTML:"Bild kann nicht geladen werden.<br><br><span style='opacity:.8'>Meistens fehlt: Drive „Jeder mit Link“</span>"
          }));
          return;
        }
        const u = tries[k++] + (tries[k-1].includes("?") ? "&" : "?") + "v=" + encodeURIComponent(it.ts||Date.now());
        img.src = u;
      };
      img.onerror = ()=>tryNext();
      tryNext();

      window.__lbNav = (dir)=>{
        const ni = (i + dir + ITEMS.length) % ITEMS.length;
        openLightbox(ni);
      };

      document.onkeydown = (e)=>{
        if(!overlay.classList.contains("show")) return;
        if(e.key==="ArrowLeft") window.__lbNav(-1);
        if(e.key==="ArrowRight") window.__lbNav(1);
      };
    }

    async function loadPhotos(forceToast=false){
      $("#lastSync").textContent = "Lade…";
      if(!navigator.onLine){
        $("#lastSync").textContent = "Offline";
        return;
      }

      const maxTries = 5;
      let lastErr = null;

      for(let a=1; a<=maxTries; a++){
        try{
          const url = SCRIPT_URL + (SCRIPT_URL.includes("?") ? "&" : "?") + "t=" + Date.now();
          const res = await fetchWithTimeout(url, 10000);
          if(!res.ok) throw new Error("HTTP " + res.status);
          const data = await res.json();
          const items = Array.isArray(data.items) ? data.items : [];
          items.sort((x,y)=>(y.ts||0)-(x.ts||0));
          ITEMS = items.filter(x => x && typeof x.url === "string" && x.url.includes("drive.google.com"));
          renderGallery();
          $("#lastSync").textContent = "Aktualisiert: " + new Date().toLocaleTimeString("de-DE");
          if(forceToast) toast("Fotos aktualisiert ✅");
          return;
        }catch(e){
          lastErr = e;
          $("#lastSync").textContent = `Fehler… Versuch ${a}/${maxTries}`;
          await new Promise(r=>setTimeout(r, 350*a*a));
        }
      }

      console.error(lastErr);
      $("#lastSync").textContent = "Fehler beim Laden";
      renderGallery();
      if(forceToast) toast("Fotos konnten nicht geladen werden ❌");
    }

    window.__refreshPhotos = loadPhotos;
    $("#refreshPhotos").addEventListener("click", ()=>loadPhotos(true));
    loadPhotos(false);

    // Copy link
    $("#copyLink").addEventListener("click", ()=>copyText(location.href));

  </script>
</body>
</html>
