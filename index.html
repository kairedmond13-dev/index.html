<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>GeoBrain</title>
<link href="https://fonts.googleapis.com/css2?family=Space+Mono:ital,wght@0,400;0,700;1,400&family=Nunito:wght@400;600;700;800;900&display=swap" rel="stylesheet"/>
<link rel="stylesheet" href="https://unpkg.com/leaflet@1.9.4/dist/leaflet.css"/>
<script src="https://unpkg.com/leaflet@1.9.4/dist/leaflet.js"></script>
<script src="https://unpkg.com/peerjs@1.5.2/dist/peerjs.min.js"></script>
<style>
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0}
:root{
  --bg:#f4f6f0;--green:#639922;--gl:#e8f0d8;--gm:#c8dda0;
  --red:#ff4b2b;--blk:#1a1a1a;--wht:#ffffff;
  --sh:8px 8px 0 #1a1a1a;--shsm:4px 4px 0 #1a1a1a;
  --bd:3px solid #1a1a1a;--r:14px;
}
html,body{height:100%;overflow:hidden}
body{font-family:'Nunito',sans-serif;background:var(--bg);display:flex;flex-direction:column;height:100vh}

/* MODE SELECT */
#mode-screen{position:fixed;inset:0;background:var(--bg);z-index:9000;display:flex;flex-direction:column;align-items:center;justify-content:center;padding:20px}
#mode-screen.hidden{display:none}
.ms-logo{font-family:'Space Mono',monospace;font-size:44px;font-weight:700;color:var(--blk);letter-spacing:-2px;margin-bottom:2px}
.ms-logo span{color:var(--green)}
.ms-tag{font-size:12px;color:#888;margin-bottom:32px;font-weight:700;letter-spacing:2px;text-transform:uppercase}
.ms-grid{display:grid;grid-template-columns:1fr 1fr;gap:14px;width:100%;max-width:480px}
.ms-card{background:var(--wht);border:var(--bd);border-radius:var(--r);padding:22px 16px;cursor:pointer;box-shadow:var(--sh);transition:all 0.12s;text-align:center;position:relative;overflow:hidden}
.ms-card:hover{transform:translate(-3px,-3px);box-shadow:11px 11px 0 var(--blk)}
.ms-card:active{transform:translate(4px,4px);box-shadow:2px 2px 0 var(--blk)}
.ms-icon{font-size:36px;margin-bottom:8px;display:block}
.ms-label{font-family:'Space Mono',monospace;font-size:13px;font-weight:700;color:var(--blk);margin-bottom:3px}
.ms-desc{font-size:11px;color:#888;font-weight:600;line-height:1.4}
.ms-card.green{background:var(--green)}.ms-card.green .ms-label,.ms-card.green .ms-desc{color:var(--wht)}
.ms-badge{position:absolute;top:8px;right:8px;background:var(--red);color:var(--wht);font-family:'Space Mono',monospace;font-size:8px;font-weight:700;padding:2px 5px;border-radius:3px;border:1.5px solid var(--blk)}

/* MODALS */
.modal{position:fixed;inset:0;background:rgba(0,0,0,0.6);z-index:9500;display:none;align-items:center;justify-content:center;backdrop-filter:blur(4px)}
.modal.open{display:flex}
.modal-card{background:var(--wht);border:var(--bd);border-radius:20px;box-shadow:var(--sh);padding:28px;max-width:360px;width:90%}
.modal-title{font-family:'Space Mono',monospace;font-size:17px;font-weight:700;margin-bottom:16px;color:var(--blk)}
.tabs{display:flex;gap:8px;margin-bottom:18px}
.tab{flex:1;padding:9px;border:2px solid var(--blk);border-radius:9px;font-family:'Space Mono',monospace;font-size:11px;font-weight:700;cursor:pointer;background:var(--bg);transition:all 0.1s}
.tab.on{background:var(--blk);color:var(--wht)}
.tsec{display:none}.tsec.on{display:block}
.m-input{width:100%;padding:11px 14px;border:2px solid var(--blk);border-radius:9px;font-family:'Space Mono',monospace;font-size:20px;font-weight:700;background:var(--bg);color:var(--blk);outline:none;margin-bottom:12px;text-align:center;letter-spacing:4px}
.m-input.sm{font-size:14px;letter-spacing:0;font-family:'Nunito',sans-serif}
.m-btn{width:100%;padding:13px;border:var(--bd);border-radius:9px;font-family:'Space Mono',monospace;font-size:13px;font-weight:700;cursor:pointer;box-shadow:var(--shsm);transition:all 0.1s;margin-bottom:8px}
.m-btn:active{transform:translate(3px,3px);box-shadow:1px 1px 0 var(--blk)}
.m-btn.pri{background:var(--green);color:var(--wht)}.m-btn.sec{background:var(--bg);color:var(--blk)}
#code-box{background:var(--gl);border:2px solid var(--blk);border-radius:9px;padding:14px;text-align:center;margin-bottom:12px}
#code-box .code{font-family:'Space Mono',monospace;font-size:32px;font-weight:700;letter-spacing:8px;color:var(--green)}
#code-box .sub{font-size:11px;color:#888;margin-top:3px;font-weight:600}
.m-status{font-size:11px;color:#888;text-align:center;font-weight:600;min-height:16px;margin-bottom:8px}
.pnp-row{display:flex;gap:8px;margin-bottom:12px}

/* HEADER */
#header{background:var(--wht);border-bottom:var(--bd);padding:10px 16px;display:flex;align-items:center;justify-content:space-between;gap:10px;flex-shrink:0;z-index:1000;position:relative}
#logo{font-family:'Space Mono',monospace;font-size:20px;font-weight:700;color:var(--blk);letter-spacing:-1px;cursor:pointer}
#logo span{color:var(--green)}
#hearts{display:flex;gap:4px;align-items:center}
.heart{font-size:18px;transition:transform 0.3s,opacity 0.3s}
.heart.lost{opacity:0.2;transform:scale(0.7)}
#hdr-mid{text-align:center}
#round-text{font-family:'Space Mono',monospace;font-size:11px;color:var(--blk)}
#mode-badge{font-family:'Space Mono',monospace;font-size:9px;font-weight:700;padding:2px 7px;border-radius:4px;border:1.5px solid var(--blk);background:var(--blk);color:var(--wht);margin-top:2px;display:inline-block}
#score-disp{font-family:'Space Mono',monospace;font-size:12px;font-weight:700;background:var(--green);color:var(--wht);padding:4px 10px;border:2px solid var(--blk);border-radius:6px;box-shadow:3px 3px 0 var(--blk);white-space:nowrap}

/* MAIN */
#main{display:flex;flex:1;overflow:hidden;position:relative}
#map{flex:1;height:100%;z-index:1}
.leaflet-container{background:#e8eef4}

/* CLUE CARD */
#clue-card{position:absolute;top:12px;left:50%;transform:translateX(-50%);background:var(--wht);border:var(--bd);border-radius:var(--r);box-shadow:var(--sh);padding:12px 16px;min-width:270px;max-width:400px;z-index:500;animation:sld 0.4s cubic-bezier(0.34,1.56,0.64,1)}
@keyframes sld{from{transform:translateX(-50%) translateY(-20px);opacity:0}to{transform:translateX(-50%) translateY(0);opacity:1}}
#clue-hdr{display:flex;align-items:center;justify-content:space-between;margin-bottom:8px}
#clue-lbl{font-family:'Space Mono',monospace;font-size:9px;font-weight:700;letter-spacing:2px;text-transform:uppercase;color:var(--green);background:var(--gl);padding:3px 8px;border-radius:4px;border:1.5px solid var(--gm)}
#clue-n{font-family:'Space Mono',monospace;font-size:10px;color:#888}
#clue-txt{font-size:13px;font-weight:700;color:var(--blk);line-height:1.5}
#hint-btn{margin-top:10px;width:100%;padding:7px;background:var(--gl);border:2px solid var(--blk);border-radius:8px;font-family:'Nunito',sans-serif;font-size:12px;font-weight:700;cursor:pointer;box-shadow:3px 3px 0 var(--blk);transition:all 0.1s;color:var(--blk)}
#hint-btn:hover{background:var(--gm)}
#hint-btn:active{transform:translate(2px,2px);box-shadow:1px 1px 0 var(--blk)}
#hint-btn:disabled{opacity:0.4;cursor:not-allowed;transform:none;box-shadow:3px 3px 0 var(--blk)}

/* TURN BANNER */
#turn-banner{position:absolute;top:12px;left:12px;background:var(--blk);color:var(--wht);border:var(--bd);border-radius:var(--r);padding:10px 14px;z-index:500;font-family:'Space Mono',monospace;font-size:11px;font-weight:700;box-shadow:var(--shsm);display:none}
#turn-banner.on{display:block}
#turn-name{font-size:15px;color:var(--green)}

/* ONLINE BAR */
#online-bar{position:absolute;left:12px;top:12px;background:var(--wht);border:var(--bd);border-radius:10px;padding:8px 12px;z-index:500;box-shadow:var(--shsm);display:none}
#online-bar.on{display:block}
.ob-lbl{font-family:'Space Mono',monospace;font-size:8px;letter-spacing:2px;text-transform:uppercase;color:#888;margin-bottom:3px}
.ob-peer{font-size:12px;font-weight:800;color:var(--blk);display:flex;align-items:center;gap:6px}
.ob-dot{width:8px;height:8px;border-radius:50%;background:var(--green);display:inline-block;animation:pulse 1.5s infinite}
@keyframes pulse{0%,100%{opacity:1}50%{opacity:0.3}}

/* SEARCH */
#search-panel{position:absolute;bottom:12px;left:50%;transform:translateX(-50%);width:90%;max-width:480px;z-index:500}
#search-wrap{background:var(--wht);border:var(--bd);border-radius:var(--r);box-shadow:var(--sh);padding:12px}
#search-row{display:flex;gap:8px}
#guess-input{flex:1;height:46px;padding:0 14px;border:2px solid var(--blk);border-radius:10px;font-family:'Nunito',sans-serif;font-size:15px;font-weight:700;background:var(--bg);color:var(--blk);outline:none;transition:all 0.15s}
#guess-input:focus{background:var(--wht);box-shadow:0 0 0 3px rgba(99,153,34,0.2);border-color:var(--green)}
#guess-input.shake{animation:shk 0.4s}
@keyframes shk{0%,100%{transform:translateX(0)}20%{transform:translateX(-8px)}40%{transform:translateX(8px)}60%{transform:translateX(-6px)}80%{transform:translateX(6px)}}
#guess-btn{height:46px;padding:0 18px;background:var(--green);color:var(--wht);border:2px solid var(--blk);border-radius:10px;font-family:'Space Mono',monospace;font-size:13px;font-weight:700;cursor:pointer;box-shadow:var(--shsm);transition:all 0.1s;white-space:nowrap}
#guess-btn:hover{background:#527a1a}
#guess-btn:active{transform:translate(3px,3px);box-shadow:1px 1px 0 var(--blk)}
#ac-list{position:absolute;bottom:100%;left:0;right:0;background:var(--wht);border:var(--bd);border-radius:var(--r);box-shadow:var(--sh);max-height:200px;overflow-y:auto;margin-bottom:8px;display:none;z-index:600}
#ac-list.open{display:block}
.ac-item{padding:10px 14px;cursor:pointer;font-size:14px;font-weight:600;display:flex;align-items:center;gap:8px;border-bottom:1px solid #eee;transition:background 0.1s}
.ac-item:last-child{border-bottom:none}
.ac-item:hover,.ac-item.sel{background:var(--gl)}
.ac-item .m{color:var(--green);font-weight:800}

/* HISTORY */
#hist-tray{position:absolute;right:12px;top:12px;bottom:70px;width:195px;z-index:400;display:flex;flex-direction:column;overflow:hidden}
#hist-lbl{font-family:'Space Mono',monospace;font-size:9px;letter-spacing:2px;text-transform:uppercase;color:#888;margin-bottom:6px}
#hist-list{display:flex;flex-direction:column;gap:6px;overflow-y:auto;flex:1;scrollbar-width:thin}
.hi{background:var(--wht);border:2px solid var(--blk);border-radius:10px;padding:8px 10px;display:flex;align-items:center;gap:8px;box-shadow:3px 3px 0 var(--blk);animation:pop 0.3s cubic-bezier(0.34,1.56,0.64,1)}
@keyframes pop{from{transform:scale(0.8) translateX(20px);opacity:0}to{transform:scale(1) translateX(0);opacity:1}}
.hi-flag{font-size:18px;line-height:1}
.hi-info{flex:1;min-width:0}
.hi-name{font-size:11px;font-weight:800;color:var(--blk);white-space:nowrap;overflow:hidden;text-overflow:ellipsis}
.hi-who{font-size:9px;color:#aaa;font-weight:700}
.hi-dist{font-family:'Space Mono',monospace;font-size:10px;font-weight:700}
.hi-dist.f{color:var(--red)}.hi-dist.c{color:var(--green)}.hi-dist.m{color:#f59e0b}

/* AI BADGE */
#ai-badge{position:absolute;left:12px;bottom:70px;background:var(--blk);color:var(--wht);border:2px solid var(--blk);border-radius:10px;padding:8px 12px;font-family:'Space Mono',monospace;font-size:10px;font-weight:700;z-index:400;box-shadow:var(--shsm);display:none}
#ai-badge.on{display:block}

/* HANDOFF */
#handoff{position:fixed;inset:0;background:var(--blk);z-index:8000;display:none;flex-direction:column;align-items:center;justify-content:center;gap:20px}
#handoff.open{display:flex}
#ho-emoji{font-size:70px}
#ho-title{font-family:'Space Mono',monospace;font-size:24px;font-weight:700;color:var(--wht);text-align:center}
#ho-sub{font-size:14px;color:#aaa;text-align:center;font-weight:600}
#ho-btn{padding:16px 40px;background:var(--green);color:var(--wht);border:var(--bd);border-radius:14px;font-family:'Space Mono',monospace;font-size:16px;font-weight:700;cursor:pointer;box-shadow:var(--sh);transition:all 0.1s}
#ho-btn:active{transform:translate(4px,4px);box-shadow:2px 2px 0 var(--blk)}

/* RESULT */
#result{position:fixed;inset:0;background:rgba(0,0,0,0.6);z-index:2000;display:none;align-items:center;justify-content:center;backdrop-filter:blur(4px)}
#result.open{display:flex}
#rc{background:var(--wht);border:var(--bd);border-radius:20px;box-shadow:var(--sh);padding:26px 30px;max-width:420px;width:90%;text-align:center;animation:pop 0.4s cubic-bezier(0.34,1.56,0.64,1)}
#r-flag{font-size:58px;margin-bottom:10px}
#r-title{font-family:'Space Mono',monospace;font-size:20px;font-weight:700;color:var(--blk);margin-bottom:4px}
#r-sub{font-size:13px;color:#666;margin-bottom:12px}
#r-dist{font-family:'Space Mono',monospace;font-size:26px;font-weight:700;margin-bottom:14px}
#r-dist.win{color:var(--green)}#r-dist.loss{color:var(--red)}
#r-scores{display:flex;gap:10px;justify-content:center;margin-bottom:18px;flex-wrap:wrap}
.rsb{flex:1;min-width:80px;background:var(--bg);border:2px solid var(--blk);border-radius:10px;padding:10px 8px;text-align:center}
.rsb-n{font-size:10px;font-weight:800;color:#888;margin-bottom:4px}
.rsb-v{font-family:'Space Mono',monospace;font-size:20px;font-weight:700;color:var(--blk)}
#r-next{width:100%;padding:14px;background:var(--green);color:var(--wht);border:var(--bd);border-radius:12px;font-family:'Space Mono',monospace;font-size:14px;font-weight:700;cursor:pointer;box-shadow:var(--shsm);transition:all 0.1s}
#r-next:active{transform:translate(3px,3px);box-shadow:1px 1px 0 var(--blk)}

/* GAME OVER */
#gameover{position:fixed;inset:0;background:rgba(0,0,0,0.75);z-index:3000;display:none;align-items:center;justify-content:center;backdrop-filter:blur(6px)}
#gameover.open{display:flex}
#gc{background:var(--wht);border:var(--bd);border-radius:20px;box-shadow:12px 12px 0 var(--blk);padding:30px;max-width:440px;width:90%;text-align:center}
#go-emo{font-size:58px;margin-bottom:10px}
#go-ttl{font-family:'Space Mono',monospace;font-size:26px;font-weight:700;color:var(--blk);margin-bottom:16px}
#go-scores{display:flex;gap:12px;justify-content:center;margin-bottom:14px;flex-wrap:wrap}
.gsb{background:var(--bg);border:var(--bd);border-radius:12px;padding:14px 20px;min-width:110px;box-shadow:var(--shsm)}
.gsb.win{background:var(--green);border-color:var(--blk)}
.gsb.win .gsb-n,.gsb.win .gsb-v{color:var(--wht)}
.gsb-n{font-size:11px;font-weight:800;color:#666;margin-bottom:4px}
.gsb-v{font-family:'Space Mono',monospace;font-size:30px;font-weight:700;color:var(--blk)}
.gsb-l{font-size:10px;color:#888;font-weight:700}
#go-win{font-size:16px;font-weight:800;color:var(--blk);margin-bottom:20px}
#go-btn{width:100%;padding:15px;background:var(--blk);color:var(--wht);border:var(--bd);border-radius:12px;font-family:'Space Mono',monospace;font-size:15px;font-weight:700;cursor:pointer;box-shadow:var(--shsm);transition:all 0.1s}
#go-btn:active{transform:translate(3px,3px);box-shadow:1px 1px 0 var(--blk)}

@media(max-width:600px){#hist-tray{display:none}#clue-card{min-width:230px;max-width:calc(100vw - 24px)}#search-panel{width:95%}#logo{font-size:16px}.ms-grid{grid-template-columns:1fr}.ms-logo{font-size:34px}}
</style>
</head>
<body>

<!-- ═══ MODE SELECT ═══ -->
<div id="mode-screen">
  <div class="ms-logo">Geo<span>Brain</span></div>
  <div class="ms-tag">🌍 Choose Your Mode</div>
  <div class="ms-grid">
    <div class="ms-card green" onclick="startMode('solo')">
      <span class="ms-icon">🎯</span>
      <div class="ms-label">SOLO</div>
      <div class="ms-desc">You vs the world.<br/>Chase your high score.</div>
    </div>
    <div class="ms-card" onclick="startMode('ai')">
      <span class="ms-icon">🤖</span>
      <div class="ms-label">VS AI</div>
      <div class="ms-desc">Face a smart AI<br/>that learns each round.</div>
    </div>
    <div class="ms-card" onclick="openPnP()">
      <span class="ms-icon">🤝</span>
      <div class="ms-label">PASS & PLAY</div>
      <div class="ms-desc">2 players, 1 device.<br/>Take turns guessing.</div>
    </div>
    <div class="ms-card" onclick="openOnline()">
      <div class="ms-badge">LIVE</div>
      <span class="ms-icon">🌐</span>
      <div class="ms-label">ONLINE</div>
      <div class="ms-desc">Challenge a friend<br/>with a room code.</div>
    </div>
  </div>
</div>

<!-- ═══ ONLINE MODAL ═══ -->
<div id="online-modal" class="modal">
  <div class="modal-card">
    <div class="modal-title">🌐 Online Multiplayer</div>
    <div class="tabs">
      <button class="tab on" onclick="omTab('host',this)">HOST</button>
      <button class="tab" onclick="omTab('join',this)">JOIN</button>
    </div>
    <div id="t-host" class="tsec on">
      <div id="code-box"><div class="code" id="om-code">····</div><div class="sub">Share this code with a friend</div></div>
      <div id="om-stat" class="m-status">Generating code...</div>
    </div>
    <div id="t-join" class="tsec">
      <input id="om-join-inp" class="m-input" type="text" maxlength="4" placeholder="CODE" oninput="this.value=this.value.toUpperCase()"/>
      <button class="m-btn pri" onclick="joinOnline()">JOIN ROOM →</button>
      <div id="om-join-stat" class="m-status"></div>
    </div>
    <button class="m-btn sec" onclick="closeOnline()">← Back</button>
  </div>
</div>

<!-- ═══ PASS & PLAY MODAL ═══ -->
<div id="pnp-modal" class="modal">
  <div class="modal-card">
    <div class="modal-title">🤝 Pass & Play Setup</div>
    <p style="font-size:13px;color:#666;margin-bottom:14px;font-weight:600">Enter names for both players:</p>
    <div class="pnp-row">
      <input id="pnp-p1" class="m-input sm" type="text" placeholder="Player 1" value="Player 1"/>
      <input id="pnp-p2" class="m-input sm" type="text" placeholder="Player 2" value="Player 2"/>
    </div>
    <button class="m-btn pri" onclick="startPnP()">START GAME →</button>
    <button class="m-btn sec" onclick="closePnP()">← Back</button>
  </div>
</div>

<!-- ═══ HEADER ═══ -->
<div id="header">
  <div id="logo" onclick="goHome()">Geo<span>Brain</span></div>
  <div id="hdr-mid">
    <div id="round-text">ROUND 1/10</div>
    <span id="mode-badge">SOLO</span>
  </div>
  <div id="hearts">
    <span class="heart" id="h1">❤️</span><span class="heart" id="h2">❤️</span>
    <span class="heart" id="h3">❤️</span><span class="heart" id="h4">❤️</span>
    <span class="heart" id="h5">❤️</span>
  </div>
  <div id="score-disp">0 PTS</div>
</div>

<!-- ═══ GAME ═══ -->
<div id="main">
  <div id="map"></div>

  <div id="clue-card">
    <div id="clue-hdr">
      <span id="clue-lbl">CLUE 1 — REGION</span>
      <span id="clue-n">1/4</span>
    </div>
    <div id="clue-txt">Loading...</div>
    <button id="hint-btn">🔍 Reveal Next Clue (–50 pts)</button>
  </div>

  <div id="turn-banner">
    <div style="font-size:9px;letter-spacing:2px;text-transform:uppercase;color:#aaa;margin-bottom:2px">NOW GUESSING</div>
    <div id="turn-name">Player 1</div>
  </div>

  <div id="online-bar">
    <div class="ob-lbl">Opponent</div>
    <div class="ob-peer"><span class="ob-dot"></span><span id="ob-name">Friend</span></div>
  </div>

  <div id="hist-tray">
    <div id="hist-lbl">Guesses This Round</div>
    <div id="hist-list"></div>
  </div>

  <div id="ai-badge">🤖 AI IS THINKING...</div>

  <div id="search-panel">
    <div id="search-wrap">
      <div style="position:relative">
        <div id="ac-list"></div>
        <div id="search-row">
          <input id="guess-input" type="text" placeholder="Type a country name..." autocomplete="off" spellcheck="false"/>
          <button id="guess-btn">GUESS →</button>
        </div>
      </div>
    </div>
  </div>
</div>

<!-- HANDOFF -->
<div id="handoff">
  <div id="ho-emoji">📱</div>
  <div id="ho-title">Pass the device!</div>
  <div id="ho-sub"></div>
  <button id="ho-btn">I'M READY →</button>
</div>

<!-- RESULT -->
<div id="result">
  <div id="rc">
    <div id="r-flag"></div>
    <div id="r-title"></div>
    <div id="r-sub"></div>
    <div id="r-dist"></div>
    <div id="r-scores"></div>
    <button id="r-next">NEXT ROUND →</button>
  </div>
</div>

<!-- GAME OVER -->
<div id="gameover">
  <div id="gc">
    <div id="go-emo">🧠</div>
    <div id="go-ttl">GAME OVER</div>
    <d
