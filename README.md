
<style>
@import url('https://fonts.googleapis.com/css2?family=Baloo+2:wght@400;700;800&family=Nunito:wght@600;700;800&display=swap');
*{box-sizing:border-box;margin:0;padding:0;user-select:none;}
.wrap{border-radius:24px;padding:22px 16px;font-family:'Nunito',sans-serif;display:flex;flex-direction:column;align-items:center;gap:16px;background:var(--color-background-secondary);}
.game-title{font-family:'Baloo 2',cursive;font-size:26px;font-weight:800;background:linear-gradient(135deg,#f97316,#ec4899,#8b5cf6);-webkit-background-clip:text;-webkit-text-fill-color:transparent;background-clip:text;text-align:center;}
.sub{font-size:12px;color:var(--color-text-secondary);font-weight:700;text-align:center;}

/* LANG BAR */
.lang-bar{display:flex;gap:6px;flex-wrap:wrap;justify-content:center;}
.lang-btn{font-family:'Nunito',sans-serif;font-size:11px;font-weight:800;padding:5px 11px;border-radius:50px;border:2px solid transparent;cursor:pointer;transition:all .18s;background:var(--color-background-primary);color:var(--color-text-secondary);}
.lang-btn:hover{transform:scale(1.07);}
.lang-btn.active{color:white;}
.lang-btn[data-lang="pt"].active{background:linear-gradient(135deg,#22c55e,#16a34a);}
.lang-btn[data-lang="en"].active{background:linear-gradient(135deg,#3b82f6,#1d4ed8);}
.lang-btn[data-lang="es"].active{background:linear-gradient(135deg,#f59e0b,#d97706);}
.lang-btn[data-lang="fr"].active{background:linear-gradient(135deg,#ec4899,#be185d);}
.lang-btn[data-lang="de"].active{background:linear-gradient(135deg,#6b7280,#374151);}
.lang-btn[data-lang="it"].active{background:linear-gradient(135deg,#ef4444,#b91c1c);}

/* LEVEL BAR */
.level-section{width:100%;max-width:520px;}
.level-header{display:flex;align-items:center;justify-content:space-between;margin-bottom:8px;}
.level-title{font-family:'Baloo 2',cursive;font-size:14px;font-weight:800;color:var(--color-text-primary);}
.level-badge{font-family:'Baloo 2',cursive;font-size:13px;font-weight:800;padding:3px 12px;border-radius:20px;color:white;}
.stars-display{font-size:14px;letter-spacing:1px;}
.level-bar-track{width:100%;height:10px;background:var(--color-background-primary);border-radius:10px;overflow:hidden;border:1.5px solid var(--color-border-secondary);}
.level-bar-fill{height:100%;border-radius:10px;transition:width .5s cubic-bezier(.34,1.2,.64,1);}
.level-dots{display:flex;gap:4px;margin-top:8px;justify-content:center;}
.lvl-dot{width:26px;height:26px;border-radius:50%;border:2.5px solid var(--color-border-secondary);background:var(--color-background-primary);font-family:'Baloo 2',cursive;font-size:11px;font-weight:800;display:flex;align-items:center;justify-content:center;cursor:pointer;transition:all .18s;color:var(--color-text-secondary);}
.lvl-dot:hover{transform:scale(1.15);}
.lvl-dot.done{color:white;border-color:transparent;}
.lvl-dot.active{color:white;border-color:transparent;transform:scale(1.2);box-shadow:0 0 0 3px rgba(0,0,0,.15);}
.lvl-dot.locked{opacity:.4;cursor:default;}

/* WORD STAGE */
.word-stage{width:100%;max-width:520px;border-radius:20px;padding:20px 14px;text-align:center;min-height:138px;display:flex;flex-direction:column;align-items:center;justify-content:center;gap:7px;position:relative;overflow:hidden;border:3px solid transparent;background:var(--color-background-primary);}
.lang-pt .word-stage{background:linear-gradient(white,white) padding-box,linear-gradient(135deg,#4ade80,#22c55e) border-box;}
.lang-en .word-stage{background:linear-gradient(white,white) padding-box,linear-gradient(135deg,#60a5fa,#3b82f6) border-box;}
.lang-es .word-stage{background:linear-gradient(white,white) padding-box,linear-gradient(135deg,#fbbf24,#f59e0b) border-box;}
.lang-fr .word-stage{background:linear-gradient(white,white) padding-box,linear-gradient(135deg,#f472b6,#ec4899) border-box;}
.lang-de .word-stage{background:linear-gradient(white,white) padding-box,linear-gradient(135deg,#9ca3af,#4b5563) border-box;}
.lang-it .word-stage{background:linear-gradient(white,white) padding-box,linear-gradient(135deg,#f87171,#dc2626) border-box;}
.big-word{font-family:'Baloo 2',cursive;font-size:48px;font-weight:800;letter-spacing:4px;text-transform:uppercase;animation:pop .4s cubic-bezier(.34,1.56,.64,1) both;}
.lang-pt .big-word{color:#15803d;}.lang-en .big-word{color:#1d4ed8;}.lang-es .big-word{color:#b45309;}
.lang-fr .big-word{color:#be185d;}.lang-de .big-word{color:#1f2937;}.lang-it .big-word{color:#991b1b;}
@keyframes pop{from{transform:scale(.4) rotate(-5deg);opacity:0}to{transform:scale(1) rotate(0);opacity:1}}
.cat-badge{font-size:11px;font-weight:800;padding:3px 11px;border-radius:20px;letter-spacing:.5px;text-transform:uppercase;}
.lang-pt .cat-badge{background:#dcfce7;color:#166534;}.lang-en .cat-badge{background:#dbeafe;color:#1e40af;}
.lang-es .cat-badge{background:#fef3c7;color:#92400e;}.lang-fr .cat-badge{background:#fce7f3;color:#9d174d;}
.lang-de .cat-badge{background:#f3f4f6;color:#1f2937;}.lang-it .cat-badge{background:#fee2e2;color:#991b1b;}
.hint{font-size:13px;color:var(--color-text-secondary);font-weight:700;}
.idle{font-size:15px;color:var(--color-text-tertiary);font-weight:700;}
.lvl-pill-stage{font-size:11px;font-weight:800;padding:2px 10px;border-radius:20px;color:white;}

/* ACTIONS */
.actions{display:flex;gap:9px;flex-wrap:wrap;justify-content:center;}
.btn-draw{font-family:'Baloo 2',cursive;font-size:15px;font-weight:800;padding:11px 26px;border-radius:50px;border:none;color:white;cursor:pointer;transition:transform .1s,box-shadow .1s;}
.lang-pt .btn-draw{background:#22c55e;box-shadow:0 4px 0 #15803d;}
.lang-en .btn-draw{background:#3b82f6;box-shadow:0 4px 0 #1d4ed8;}
.lang-es .btn-draw{background:#f59e0b;box-shadow:0 4px 0 #b45309;}
.lang-fr .btn-draw{background:#ec4899;box-shadow:0 4px 0 #be185d;}
.lang-de .btn-draw{background:#4b5563;box-shadow:0 4px 0 #1f2937;}
.lang-it .btn-draw{background:#ef4444;box-shadow:0 4px 0 #b91c1c;}
.btn-draw:hover{transform:translateY(-2px);}.btn-draw:active{transform:translateY(2px);}
.btn-speak{font-family:'Baloo 2',cursive;font-size:15px;font-weight:800;padding:11px 18px;border-radius:50px;border:2.5px solid;background:var(--color-background-primary);cursor:pointer;transition:all .15s;}
.lang-pt .btn-speak{border-color:#22c55e;color:#15803d;}.lang-en .btn-speak{border-color:#3b82f6;color:#1d4ed8;}
.lang-es .btn-speak{border-color:#f59e0b;color:#92400e;}.lang-fr .btn-speak{border-color:#ec4899;color:#be185d;}
.lang-de .btn-speak{border-color:#4b5563;color:#1f2937;}.lang-it .btn-speak{border-color:#ef4444;color:#991b1b;}
.btn-speak:disabled{opacity:.35;cursor:default;}

/* DROP */
.section-label{font-size:11px;font-weight:800;color:var(--color-text-secondary);text-transform:uppercase;letter-spacing:1px;align-self:flex-start;max-width:520px;width:100%;}
.drop-zone{width:100%;max-width:520px;min-height:64px;background:var(--color-background-primary);border-radius:14px;border:2.5px dashed var(--color-border-secondary);display:flex;flex-wrap:wrap;gap:7px;padding:9px 11px;align-items:center;transition:all .2s;position:relative;}
.drop-zone.drag-over{border-color:#3b82f6;background:#eff6ff;}
.drop-zone.correct-zone{border-color:#10b981;background:#d1fae5;border-style:solid;}
.drop-zone.wrong-zone{border-color:#ef4444;background:#fee2e2;border-style:solid;}
.drop-placeholder{font-size:13px;color:var(--color-text-tertiary);font-weight:700;position:absolute;left:50%;transform:translateX(-50%);pointer-events:none;white-space:nowrap;}
.tiles-pool{width:100%;max-width:520px;min-height:60px;display:flex;flex-wrap:wrap;gap:7px;padding:4px 0;align-items:center;justify-content:center;}

/* TILES */
.tile-wrap{position:relative;display:inline-flex;flex-direction:column;align-items:center;margin-top:28px;}
.arrow-label{position:absolute;top:-28px;left:50%;transform:translateX(-50%);display:flex;flex-direction:column;align-items:center;opacity:0;pointer-events:none;transition:opacity .2s;}
.arrow-label.visible{opacity:1;}
.arrow-txt{font-family:'Baloo 2',cursive;font-size:11px;font-weight:800;color:#dc2626;background:#fee2e2;border:1.5px solid #fca5a5;border-radius:6px;padding:2px 7px;white-space:nowrap;}
.arrow-tri{width:0;height:0;border-left:5px solid transparent;border-right:5px solid transparent;border-top:6px solid #fca5a5;margin-top:-1px;}
.tile{display:inline-flex;align-items:center;justify-content:center;border-radius:11px;border:2.5px solid;font-family:'Baloo 2',cursive;font-weight:800;cursor:grab;transition:transform .15s,border-color .15s;text-transform:uppercase;animation:tile-in .3s ease both;}
@keyframes tile-in{from{transform:scale(0) rotate(10deg);opacity:0}to{transform:scale(1) rotate(0);opacity:1}}
.tile:hover{transform:scale(1.12);}.tile.dragging{opacity:.35;transform:scale(.88);}
.tile.speaking,.tile.highlighted{transform:scale(1.2);}
.tile.correct-tile{border-color:#10b981!important;background:#d1fae5!important;color:#065f46!important;}
.tile.wrong-tile{border-color:#ef4444!important;background:#fee2e2!important;color:#991b1b!important;animation:shake .4s ease;}
@keyframes shake{0%,100%{transform:translateX(0)}20%{transform:translateX(-6px)}40%{transform:translateX(6px)}60%{transform:translateX(-4px)}80%{transform:translateX(4px)}}
.tile.c0{background:#fef3c7;border-color:#fbbf24;color:#92400e;}.tile.c1{background:#dbeafe;border-color:#60a5fa;color:#1e40af;}
.tile.c2{background:#fce7f3;border-color:#f472b6;color:#9d174d;}.tile.c3{background:#dcfce7;border-color:#4ade80;color:#166534;}
.tile.c4{background:#ede9fe;border-color:#a78bfa;color:#4c1d95;}.tile.c5{background:#ffedd5;border-color:#fb923c;color:#9a3412;}
.tile.c6{background:#cffafe;border-color:#22d3ee;color:#164e63;}.tile.c7{background:#fef9c3;border-color:#facc15;color:#713f12;}
.tile.c0:hover,.tile.c0.speaking,.tile.c0.highlighted{background:#fde68a;border-color:#f59e0b;}
.tile.c1:hover,.tile.c1.speaking,.tile.c1.highlighted{background:#bfdbfe;border-color:#3b82f6;}
.tile.c2:hover,.tile.c2.speaking,.tile.c2.highlighted{background:#fbcfe8;border-color:#ec4899;}
.tile.c3:hover,.tile.c3.speaking,.tile.c3.highlighted{background:#bbf7d0;border-color:#22c55e;}
.tile.c4:hover,.tile.c4.speaking,.tile.c4.highlighted{background:#ddd6fe;border-color:#7c3aed;}
.tile.c5:hover,.tile.c5.speaking,.tile.c5.highlighted{background:#fed7aa;border-color:#ea580c;}
.tile.c6:hover,.tile.c6.speaking,.tile.c6.highlighted{background:#a5f3fc;border-color:#06b6d4;}
.tile.c7:hover,.tile.c7.speaking,.tile.c7.highlighted{background:#fef08a;border-color:#eab308;}

/* FEEDBACK */
.feedback-box{width:100%;max-width:520px;border-radius:14px;padding:12px 15px;font-family:'Baloo 2',cursive;font-size:15px;font-weight:600;line-height:1.5;display:none;}
.feedback-box.win{background:linear-gradient(135deg,#d1fae5,#a7f3d0);color:#065f46;border:2px solid #6ee7b7;display:block;}
.feedback-box.lose{background:linear-gradient(135deg,#fee2e2,#fecaca);color:#991b1b;border:2px solid #fca5a5;display:block;}
.fb-title{font-size:17px;font-weight:800;margin-bottom:4px;}
.err-list{list-style:none;padding:0;margin:5px 0 0;display:flex;flex-direction:column;gap:4px;}
.err-list li{font-size:13px;display:flex;align-items:center;gap:5px;cursor:pointer;padding:4px 8px;border-radius:8px;transition:background .15s;font-weight:700;}
.err-list li:hover{background:#fecaca;}
.err-pill{display:inline-block;padding:2px 8px;border-radius:7px;font-weight:800;font-size:13px;background:#fecaca;color:#991b1b;border:1.5px solid #fca5a5;}
.ok-pill{display:inline-block;padding:2px 8px;border-radius:7px;font-weight:800;font-size:13px;background:#d1fae5;color:#065f46;border:1.5px solid #6ee7b7;}
.level-up-banner{display:none;width:100%;max-width:520px;background:linear-gradient(135deg,#fef3c7,#fde68a);border:2px solid #fbbf24;border-radius:14px;padding:12px 16px;text-align:center;font-family:'Baloo 2',cursive;font-size:18px;font-weight:800;color:#92400e;animation:pop .5s cubic-bezier(.34,1.56,.64,1) both;}

.confetti-wrap{position:absolute;top:0;left:0;right:0;bottom:0;pointer-events:none;border-radius:20px;overflow:hidden;z-index:10;}
.dot{position:absolute;border-radius:50%;animation:fall 1.3s ease-out both;}
@keyframes fall{from{transform:translateY(-20px) rotate(0);opacity:1}to{transform:translateY(200px) rotate(400deg);opacity:0}}
.check-btn{font-family:'Baloo 2',cursive;font-size:15px;font-weight:800;padding:10px 26px;border-radius:50px;border:none;color:white;cursor:pointer;transition:all .15s;}
.check-btn:disabled{opacity:.3;cursor:default;}
.lang-pt .check-btn{background:#22c55e;}.lang-en .check-btn{background:#3b82f6;}
.lang-es .check-btn{background:#f59e0b;}.lang-fr .check-btn{background:#ec4899;}
.lang-de .check-btn{background:#4b5563;}.lang-it .check-btn{background:#ef4444;}
.game-inner{width:100%;display:flex;flex-direction:column;align-items:center;gap:16px;}
</style>

<div class="wrap" id="mainWrap">
  <div><div class="game-title">✏️ Hora de Soletrar!</div><div class="sub" id="subTxt">Arraste as letras na ordem certa</div></div>

  <div class="lang-bar">
    <button class="lang-btn active" data-lang="pt" onclick="setLang('pt')">🇧🇷 Português</button>
    <button class="lang-btn" data-lang="en" onclick="setLang('en')">🇺🇸 English</button>
    <button class="lang-btn" data-lang="es" onclick="setLang('es')">🇪🇸 Español</button>
    <button class="lang-btn" data-lang="fr" onclick="setLang('fr')">🇫🇷 Français</button>
    <button class="lang-btn" data-lang="de" onclick="setLang('de')">🇩🇪 Deutsch</button>
    <button class="lang-btn" data-lang="it" onclick="setLang('it')">🇮🇹 Italiano</button>
  </div>

  <div class="level-section" id="levelSection">
    <div class="level-header">
      <div class="level-title" id="levelTitle">📊 Nível 1 — Iniciante</div>
      <div>
        <span class="stars-display" id="starsDisplay">⭐☆☆</span>
      </div>
    </div>
    <div class="level-bar-track"><div class="level-bar-fill" id="levelBarFill" style="width:0%"></div></div>
    <div style="display:flex;justify-content:space-between;margin-top:4px;">
      <span style="font-size:11px;font-weight:700;color:var(--color-text-secondary)" id="xpLabel">0 / 3 acertos</span>
      <span style="font-size:11px;font-weight:700;color:var(--color-text-secondary)" id="nextLvlLabel">Próximo: Nível 2</span>
    </div>
    <div class="level-dots" id="levelDots"></div>
  </div>

  <div class="game-inner lang-pt" id="gameInner">
    <div class="word-stage lang-pt" id="wordStage">
      <div class="confetti-wrap" id="confetti"></div>
      <div class="idle" id="idleMsg">Clique em Sortear! 🎲</div>
      <div class="big-word" id="bigWord" style="display:none"></div>
      <div class="cat-badge" id="catBadge" style="display:none"></div>
      <div class="hint" id="hint" style="display:none"></div>
    </div>
    <div class="actions">
      <button class="btn-draw" id="btnDraw" onclick="drawWord()">🎲 Sortear</button>
      <button class="btn-speak" id="btnSpeak" onclick="speakWord()" disabled>🔊 Ouvir</button>
    </div>
    <div class="section-label" id="dropLabel" style="display:none"></div>
    <div class="drop-zone" id="dropZone" style="display:none"><span class="drop-placeholder" id="dropPlaceholder"></span></div>
    <div class="tiles-pool" id="tilesPool" style="display:none"></div>
    <button class="check-btn" id="checkBtn" onclick="checkAnswer()" disabled style="display:none"></button>
    <div class="level-up-banner" id="levelUpBanner"></div>
    <div class="feedback-box" id="feedbackBox"><div class="fb-title" id="fbTitle"></div><div id="fbBody"></div></div>
  </div>
</div>

<script>
// ─── LEVEL CONFIG ───────────────────────────────────────────────
const LEVELS=[
  {n:1,label:{pt:'Iniciante',en:'Beginner',es:'Principiante',fr:'Débutant',de:'Anfänger',it:'Principiante'},color:'#22c55e',xpNeeded:3},
  {n:2,label:{pt:'Fácil',en:'Easy',es:'Fácil',fr:'Facile',de:'Einfach',it:'Facile'},color:'#84cc16',xpNeeded:3},
  {n:3,label:{pt:'Básico',en:'Basic',es:'Básico',fr:'Basique',de:'Grundlegend',it:'Base'},color:'#a3e635',xpNeeded:4},
  {n:4,label:{pt:'Intermediário',en:'Intermediate',es:'Intermedio',fr:'Intermédiaire',de:'Mittel',it:'Intermedio'},color:'#eab308',xpNeeded:4},
  {n:5,label:{pt:'Avançado',en:'Advanced',es:'Avanzado',fr:'Avancé',de:'Fortgeschritten',it:'Avanzato'},color:'#f97316',xpNeeded:4},
  {n:6,label:{pt:'Difícil',en:'Hard',es:'Difícil',fr:'Difficile',de:'Schwer',it:'Difficile'},color:'#ef4444',xpNeeded:4},
  {n:7,label:{pt:'Expert',en:'Expert',es:'Experto',fr:'Expert',de:'Experte',it:'Esperto'},color:'#e11d48',xpNeeded:5},
  {n:8,label:{pt:'Mestre',en:'Master',es:'Maestro',fr:'Maître',de:'Meister',it:'Maestro'},color:'#9333ea',xpNeeded:5},
  {n:9,label:{pt:'Especialista',en:'Specialist',es:'Especialista',fr:'Spécialiste',de:'Spezialist',it:'Specialista'},color:'#7c3aed',xpNeeded:5},
  {n:10,label:{pt:'Lendário',en:'Legendary',es:'Legendario',fr:'Légendaire',de:'Legendär',it:'Leggendario'},color:'#4f46e5',xpNeeded:999},
];

// ─── WORDS: each entry has level 1-10 ───────────────────────────
const WORDS_DB={
  pt:[
    // Nível 1-2: 3-4 letras simples
    {w:'BOI',cat:'Animal',d:'Animal de fazenda 🐂',l:1},{w:'PAI',cat:'Família',d:'Nosso papai 👨',l:1},
    {w:'MÃE',cat:'Família',d:'Nossa mamãe 👩',l:1},{w:'SOL',cat:'Natureza',d:'Brilha no céu ☀️',l:1},
    {w:'LUA',cat:'Natureza',d:'Aparece à noite 🌙',l:1},{w:'MAR',cat:'Natureza',d:'Água salgada 🌊',l:1},
    {w:'CÃO',cat:'Animal',d:'Faz au au 🐶',l:1},{w:'OVO',cat:'Comida',d:'Galinha bota 🥚',l:1},
    {w:'PÉ',cat:'Corpo',d:'Fica no fim da perna 🦶',l:1},{w:'MÃO',cat:'Corpo',d:'Tem cinco dedos ✋',l:1},
    {w:'GATO',cat:'Animal',d:'Faz miau 🐱',l:2},{w:'PATO',cat:'Animal',d:'Nada na lagoa 🦆',l:2},
    {w:'BOLA',cat:'Brinquedo',d:'Se rola e quica ⚽',l:2},{w:'CASA',cat:'Lugar',d:'Onde moramos 🏠',l:2},
    {w:'SAPO',cat:'Animal',d:'Pula e croá 🐸',l:2},{w:'FADA',cat:'Fantasia',d:'Tem varinha mágica 🧚',l:2},
    // Nível 3-4: 5 letras
    {w:'CABRA',cat:'Animal',d:'Dá leite na fazenda 🐐',l:3},{w:'COELHO',cat:'Animal',d:'Tem orelhas grandes 🐰',l:3},
    {w:'FLOR',cat:'Natureza',d:'Tem pétalas coloridas 🌸',l:3},{w:'LIVRO',cat:'Objeto',d:'Tem páginas para ler 📚',l:3},
    {w:'CHUVA',cat:'Natureza',d:'Cai do céu 🌧️',l:3},{w:'NUVEM',cat:'Natureza',d:'Flutua no céu ☁️',l:3},
    {w:'PORTA',cat:'Objeto',d:'Abrimos para entrar 🚪',l:3},{w:'PEIXE',cat:'Animal',d:'Vive na água 🐟',l:3},
    {w:'AVIÃO',cat:'Veículo',d:'Voa no céu ✈️',l:4},{w:'CARRO',cat:'Veículo',d:'Tem quatro rodas 🚗',l:4},
    {w:'ESCOLA',cat:'Lugar',d:'Onde aprendemos 🏫',l:4},{w:'GIRAFA',cat:'Animal',d:'Pescoço longo 🦒',l:4},
    {w:'TIGRE',cat:'Animal',d:'Tem listras 🐯',l:4},{w:'RINOCERONTE',cat:'Animal',d:'Tem chifre 🦏',l:4},
    // Nível 5-6: 6-7 letras
    {w:'BORBOLETA',cat:'Animal',d:'Tem asas coloridas 🦋',l:5},{w:'ELEFANTE',cat:'Animal',d:'Tem tromba 🐘',l:5},
    {w:'FUTEBOL',cat:'Esporte',d:'Jogo com bola nos pés ⚽',l:5},{w:'JANELA',cat:'Objeto',d:'Deixa entrar luz 🪟',l:5},
    {w:'TARTARUGA',cat:'Animal',d:'Anda devagar 🐢',l:5},{w:'CASTELO',cat:'Lugar',d:'Onde moram reis 🏰',l:5},
    {w:'CAVALO',cat:'Animal',d:'Galopeia no campo 🐴',l:6},{w:'PÁSSARO',cat:'Animal',d:'Tem asas e voa 🐦',l:6},
    {w:'FLORESTA',cat:'Natureza',d:'Cheia de árvores 🌲',l:6},{w:'PLANETA',cat:'Natureza',d:'A Terra é um planeta 🌍',l:6},
    {w:'FAMÍLIA',cat:'Pessoas',d:'Papai mamãe e filhos 👨‍👩‍👧',l:6},{w:'ROBÔTICO',cat:'Tecnologia',d:'Parecido com robô 🤖',l:6},
    // Nível 7-8: palavras longas
    {w:'HIPOPÓTAMO',cat:'Animal',d:'Vive no rio 🦛',l:7},{w:'CROCODILO',cat:'Animal',d:'Tem dentes grandes 🐊',l:7},
    {w:'BRINQUEDO',cat:'Objeto',d:'Crianças adoram jogar 🧸',l:7},{w:'COMPUTADOR',cat:'Tecnologia',d:'Máquina inteligente 💻',l:7},
    {w:'UNIVERSIDADE',cat:'Lugar',d:'Faculdade para adultos 🎓',l:8},{w:'PERSONALIDADE',cat:'Conceito',d:'Jeito de ser 💫',l:8},
    {w:'FOTOSSÍNTESE',cat:'Ciência',d:'Plantas fazem com o sol 🌿',l:8},{w:'BIBLIOTECÁRIA',cat:'Profissão',d:'Cuida dos livros 📖',l:8},
    // Nível 9-10: altamente complexas
    {w:'RESPONSABILIDADE',cat:'Conceito',d:'Ser responsável pelas coisas 🏆',l:9},{w:'INTERDISCIPLINAR',cat:'Educação',d:'Várias disciplinas juntas 📚',l:9},
    {w:'DESENVOLVIMENTO',cat:'Conceito',d:'Processo de crescer 🌱',l:9},{w:'SUSTENTABILIDADE',cat:'Natureza',d:'Cuidar do planeta 🌎',l:9},
    {w:'ANTICONSTITUCIONAL',cat:'Direito',d:'Contra a Constituição ⚖️',l:10},{w:'INCONSTITUCIONALÍSSIMO',cat:'Direito',d:'A palavra mais longa do Brasil 🇧🇷',l:10},
    {w:'DESCONSTITUCIONALIZAR',cat:'Direito',d:'Retirar caráter constitucional ⚖️',l:10},{w:'INTERNACIONALIZAÇÃO',cat:'Negócios',d:'Expandir para outros países 🌍',l:10},
  ],
  en:[
    {w:'CAT',cat:'Animal',d:'Says meow 🐱',l:1},{w:'DOG',cat:'Animal',d:'Says woof 🐶',l:1},
    {w:'SUN',cat:'Nature',d:'Shines in the sky ☀️',l:1},{w:'BIG',cat:'Adjective',d:'Not small 📏',l:1},
    {w:'RED',cat:'Color',d:'Color of fire 🔴',l:1},{w:'BED',cat:'Object',d:'We sleep on it 🛏️',l:1},
    {w:'BALL',cat:'Toy',d:'Round and bouncy ⚽',l:2},{w:'FISH',cat:'Animal',d:'Lives in water 🐟',l:2},
    {w:'MOON',cat:'Nature',d:'Comes out at night 🌙',l:2},{w:'CAKE',cat:'Food',d:'Sweet and delicious 🎂',l:2},
    {w:'FROG',cat:'Animal',d:'Jumps and croaks 🐸',l:3},{w:'STAR',cat:'Nature',d:'Twinkles at night ⭐',l:3},
    {w:'TREE',cat:'Nature',d:'Has branches 🌳',l:3},{w:'BEAR',cat:'Animal',d:'Big and fluffy 🐻',l:3},
    {w:'HORSE',cat:'Animal',d:'Gallops fast 🐴',l:4},{w:'CLOUD',cat:'Nature',d:'Floats in the sky ☁️',l:4},
    {w:'FLOWER',cat:'Nature',d:'Has petals 🌸',l:4},{w:'RABBIT',cat:'Animal',d:'Has long ears 🐰',l:4},
    {w:'BUTTER',cat:'Food',d:'Goes on bread 🧈',l:5},{w:'CASTLE',cat:'Place',d:'Where kings live 🏰',l:5},
    {w:'JUNGLE',cat:'Nature',d:'Dense tropical forest 🌴',l:5},{w:'PLANET',cat:'Nature',d:'Earth is one 🌍',l:5},
    {w:'LIBRARY',cat:'Place',d:'Full of books 📚',l:6},{w:'PENGUIN',cat:'Animal',d:'Black and white bird 🐧',l:6},
    {w:'DOLPHIN',cat:'Animal',d:'Swims and jumps 🐬',l:6},{w:'VOLCANO',cat:'Nature',d:'Erupts with lava 🌋',l:6},
    {w:'ELEPHANT',cat:'Animal',d:'Has a trunk 🐘',l:7},{w:'BUTTERFLY',cat:'Animal',d:'Has colorful wings 🦋',l:7},
    {w:'CHOCOLATE',cat:'Food',d:'Sweet brown treat 🍫',l:7},{w:'TELESCOPE',cat:'Object',d:'See stars up close 🔭',l:7},
    {w:'SUBMARINE',cat:'Vehicle',d:'Goes underwater 🤿',l:8},{w:'DINOSAUR',cat:'Animal',d:'Ancient creature 🦕',l:8},
    {w:'CATERPILLAR',cat:'Animal',d:'Becomes a butterfly 🐛',l:8},{w:'MATHEMATICS',cat:'Science',d:'Numbers and equations ➕',l:8},
    {w:'COMMUNICATION',cat:'Concept',d:'Sharing information 💬',l:9},{w:'EXTRAORDINARY',cat:'Adjective',d:'Beyond ordinary ✨',l:9},
    {w:'RESPONSIBILITY',cat:'Concept',d:'Being accountable 🏆',l:9},{w:'ACCOMPLISHMENT',cat:'Concept',d:'Achieving something great 🎯',l:9},
    {w:'ELECTROENCEPHALOGRAM',cat:'Science',d:'Brain activity record 🧠',l:10},{w:'UNCHARACTERISTICALLY',cat:'Grammar',d:'Not typical behavior 📖',l:10},
    {w:'COUNTERINTELLIGENCE',cat:'Concept',d:'Spying on spies 🕵️',l:10},{w:'INTERNATIONALIZATION',cat:'Business',d:'Going global 🌍',l:10},
  ],
  es:[
    {w:'SOL',cat:'Naturaleza',d:'Brilla en el cielo ☀️',l:1},{w:'PAZ',cat:'Concepto',d:'Tranquilidad 🕊️',l:1},
    {w:'LUZ',cat:'Física',d:'Ilumina todo 💡',l:1},{w:'MAR',cat:'Naturaleza',d:'Agua salada 🌊',l:1},
    {w:'GATO',cat:'Animal',d:'Dice miau 🐱',l:2},{w:'PATO',cat:'Animal',d:'Nada en el lago 🦆',l:2},
    {w:'LUNA',cat:'Naturaleza',d:'Sale de noche 🌙',l:2},{w:'SAPO',cat:'Animal',d:'Salta y croa 🐸',l:2},
    {w:'FLOR',cat:'Naturaleza',d:'Tiene pétalos 🌸',l:3},{w:'LIBRO',cat:'Objeto',d:'Tiene páginas 📚',l:3},
    {w:'ÁRBOL',cat:'Naturaleza',d:'Tiene ramas 🌳',l:3},{w:'NUBE',cat:'Naturaleza',d:'Flota en el cielo ☁️',l:3},
    {w:'CABALLO',cat:'Animal',d:'Galopa rápido 🐴',l:4},{w:'PELOTA',cat:'Juguete',d:'Redonda y rebota ⚽',l:4},
    {w:'ESTRELLA',cat:'Naturaleza',d:'Brilla de noche ⭐',l:4},{w:'COLEGIO',cat:'Lugar',d:'Donde aprendemos 🏫',l:4},
    {w:'MARIPOSA',cat:'Animal',d:'Tiene alas coloridas 🦋',l:5},{w:'ELEFANTE',cat:'Animal',d:'Tiene trompa 🐘',l:5},
    {w:'TORTUGA',cat:'Animal',d:'Camina despacio 🐢',l:5},{w:'CASTILLO',cat:'Lugar',d:'Donde viven reyes 🏰',l:5},
    {w:'COCODRILO',cat:'Animal',d:'Tiene dientes grandes 🐊',l:6},{w:'DELFÍN',cat:'Animal',d:'Nada y salta 🐬',l:6},
    {w:'PLANETA',cat:'Naturaleza',d:'La Tierra es uno 🌍',l:6},{w:'FAMILIA',cat:'Personas',d:'Papá mamá e hijos 👨‍👩‍👧',l:6},
    {w:'HIPOPÓTAMO',cat:'Animal',d:'Vive en el río 🦛',l:7},{w:'TELESCOPIO',cat:'Objeto',d:'Para ver las estrellas 🔭',l:7},
    {w:'BIBLIOTECA',cat:'Lugar',d:'Llena de libros 📚',l:7},{w:'CHOCOLATITO',cat:'Comida',d:'Dulce y delicioso 🍫',l:7},
    {w:'DINOSAURIO',cat:'Animal',d:'Criatura antigua 🦕',l:8},{w:'MATEMÁTICAS',cat:'Ciencia',d:'Números y ecuaciones ➕',l:8},
    {w:'COMUNICACIÓN',cat:'Concepto',d:'Compartir información 💬',l:8},{w:'EXTRAORDINARIO',cat:'Adjetivo',d:'Fuera de lo común ✨',l:8},
    {w:'RESPONSABILIDAD',cat:'Concepto',d:'Ser responsable 🏆',l:9},{w:'INTERDISCIPLINARIO',cat:'Educación',d:'Varias disciplinas juntas 📚',l:9},
    {w:'SOSTENIBILIDAD',cat:'Naturaleza',d:'Cuidar el planeta 🌎',l:9},{w:'INTERNACIONALIZACIÓN',cat:'Negocios',d:'Expandir a otros países 🌍',l:9},
    {w:'ANTICONSTITUCIONAL',cat:'Derecho',d:'Contra la Constitución ⚖️',l:10},{w:'ELECTROENCEFALOGRAMA',cat:'Ciencia',d:'Registro de la actividad cerebral 🧠',l:10},
    {w:'DESCENTRALIZACIÓN',cat:'Política',d:'Distribuir el poder 🏛️',l:10},{w:'INCONSTITUCIONALIDAD',cat:'Derecho',d:'Ser contra la ley máxima ⚖️',l:10},
  ],
  fr:[
    {w:'SOL',cat:'Nature',d:'On marche dessus 🌍',l:1},{w:'AIR',cat:'Nature',d:'On respire ça 💨',l:1},
    {w:'FEU',cat:'Nature',d:'Chaud et orange 🔥',l:1},{w:'EAU',cat:'Nature',d:'On la boit 💧',l:1},
    {w:'CHAT',cat:'Animal',d:'Dit miaou 🐱',l:2},{w:'BALLE',cat:'Jouet',d:'Ronde et rebondit ⚽',l:2},
    {w:'LUNE',cat:'Nature',d:'Apparaît la nuit 🌙',l:2},{w:'PLUIE',cat:'Nature',d:'Tombe du ciel 🌧️',l:2},
    {w:'FLEUR',cat:'Nature',d:'A des pétales 🌸',l:3},{w:'ARBRE',cat:'Nature',d:'A des branches 🌳',l:3},
    {w:'NUAGE',cat:'Nature',d:'Flotte dans le ciel ☁️',l:3},{w:'LIVRE',cat:'Objet',d:'A des pages 📚',l:3},
    {w:'CHEVAL',cat:'Animal',d:'Galope vite 🐴',l:4},{w:'ÉTOILE',cat:'Nature',d:'Brille la nuit ⭐',l:4},
    {w:'GRENOUILLE',cat:'Animal',d:'Saute et coasse 🐸',l:4},{w:'VOITURE',cat:'Véhicule',d:'A quatre roues 🚗',l:4},
    {w:'PAPILLON',cat:'Animal',d:'A des ailes colorées 🦋',l:5},{w:'ÉLÉPHANT',cat:'Animal',d:'A une trompe 🐘',l:5},
    {w:'TORTUE',cat:'Animal',d:'Marche lentement 🐢',l:5},{w:'CHÂTEAU',cat:'Lieu',d:'Où habitent les rois 🏰',l:5},
    {w:'CROCODILE',cat:'Animal',d:'A de grandes dents 🐊',l:6},{w:'DAUPHIN',cat:'Animal',d:'Nage et saute 🐬',l:6},
    {w:'PLANÈTE',cat:'Nature',d:'La Terre en est une 🌍',l:6},{w:'FAMILLE',cat:'Personnes',d:'Papa maman enfants 👨‍👩‍👧',l:6},
    {w:'HIPPOPOTAME',cat:'Animal',d:'Vit dans la rivière 🦛',l:7},{w:'TÉLESCOPE',cat:'Objet',d:'Pour voir les étoiles 🔭',l:7},
    {w:'BIBLIOTHÈQUE',cat:'Lieu',d:'Pleine de livres 📚',l:7},{w:'CHOCOLATERIE',cat:'Commerce',d:'Fait du chocolat 🍫',l:7},
    {w:'DINOSAURE',cat:'Animal',d:'Créature ancienne 🦕',l:8},{w:'MATHÉMATIQUES',cat:'Science',d:'Chiffres et équations ➕',l:8},
    {w:'EXTRAORDINAIRE',cat:'Adjectif',d:'Au-delà de l\'ordinaire ✨',l:8},{w:'COMMUNICATION',cat:'Concept',d:'Partager information 💬',l:8},
    {w:'RESPONSABILITÉ',cat:'Concept',d:'Être responsable 🏆',l:9},{w:'INTERDISCIPLINAIRE',cat:'Éducation',d:'Plusieurs disciplines 📚',l:9},
    {w:'DÉVELOPPEMENT',cat:'Concept',d:'Processus de croissance 🌱',l:9},{w:'INTERNATIONALISATION',cat:'Affaires',d:'Aller à l\'international 🌍',l:9},
    {w:'ANTICONSTITUTIONNEL',cat:'Droit',d:'Contre la Constitution ⚖️',l:10},{w:'ÉLECTROENCÉPHALOGRAMME',cat:'Science',d:'Enregistrement cérébral 🧠',l:10},
    {w:'INCONSTITUTIONNELLEMENT',cat:'Droit',d:'De manière inconstitutionnelle ⚖️',l:10},{w:'DÉCENTRALISATION',cat:'Politique',d:'Distribuer le pouvoir 🏛️',l:10},
  ],
  de:[
    {w:'SOL',cat:'Natur',d:'Gibt Wärme ☀️',l:1},{w:'EIS',cat:'Natur',d:'Gefrorenes Wasser 🧊',l:1},
    {w:'OHR',cat:'Körper',d:'Damit hören wir 👂',l:1},{w:'AUGE',cat:'Körper',d:'Damit sehen wir 👁️',l:1},
    {w:'HUND',cat:'Tier',d:'Sagt wau 🐶',l:2},{w:'BALL',cat:'Spielzeug',d:'Rund und springt ⚽',l:2},
    {w:'MOND',cat:'Natur',d:'Kommt nachts raus 🌙',l:2},{w:'FISCH',cat:'Tier',d:'Lebt im Wasser 🐟',l:2},
    {w:'BLUME',cat:'Natur',d:'Hat Blütenblätter 🌸',l:3},{w:'BAUM',cat:'Natur',d:'Hat Äste 🌳',l:3},
    {w:'REGEN',cat:'Natur',d:'Fällt vom Himmel 🌧️',l:3},{w:'BUCH',cat:'Objekt',d:'Hat Seiten 📚',l:3},
    {w:'PFERD',cat:'Tier',d:'Galoppiert schnell 🐴',l:4},{w:'STERN',cat:'Natur',d:'Leuchtet nachts ⭐',l:4},
    {w:'FROSCH',cat:'Tier',d:'Springt und quakt 🐸',l:4},{w:'SCHULE',cat:'Ort',d:'Wo wir lernen 🏫',l:4},
    {w:'SCHMETTERLING',cat:'Tier',d:'Hat bunte Flügel 🦋',l:5},{w:'ELEFANT',cat:'Tier',d:'Hat einen Rüssel 🐘',l:5},
    {w:'SCHILDKRÖTE',cat:'Tier',d:'Geht langsam 🐢',l:5},{w:'SCHLOSS',cat:'Ort',d:'Wo Könige wohnen 🏰',l:5},
    {w:'KROKODIL',cat:'Tier',d:'Hat große Zähne 🐊',l:6},{w:'DELFIN',cat:'Tier',d:'Schwimmt und springt 🐬',l:6},
    {w:'PLANET',cat:'Natur',d:'Die Erde ist einer 🌍',l:6},{w:'FAMILIE',cat:'Personen',d:'Papa Mama Kinder 👨‍👩‍👧',l:6},
    {w:'NILPFERD',cat:'Tier',d:'Lebt im Fluss 🦛',l:7},{w:'TELESKOP',cat:'Objekt',d:'Um Sterne zu sehen 🔭',l:7},
    {w:'BIBLIOTHEK',cat:'Ort',d:'Voller Bücher 📚',l:7},{w:'SCHOKOLADE',cat:'Essen',d:'Süß und lecker 🍫',l:7},
    {w:'DINOSAURIER',cat:'Tier',d:'Urzeitliches Wesen 🦕',l:8},{w:'MATHEMATIK',cat:'Wissenschaft',d:'Zahlen und Gleichungen ➕',l:8},
    {w:'KOMMUNIKATION',cat:'Konzept',d:'Informationen teilen 💬',l:8},{w:'AUSSERGEWÖHNLICH',cat:'Adjektiv',d:'Über das Gewöhnliche hinaus ✨',l:8},
    {w:'VERANTWORTUNG',cat:'Konzept',d:'Verantwortlich sein 🏆',l:9},{w:'NACHHALTIGKEITSZIELE',cat:'Natur',d:'Ziele für Nachhaltigkeit 🌱',l:9},
    {w:'INTERNATIONALISIERUNG',cat:'Wirtschaft',d:'Global werden 🌍',l:9},{w:'GESCHWINDIGKEITSBEGRENZUNG',cat:'Verkehr',d:'Tempolimit 🚗',l:9},
    {w:'RINDFLEISCHETIKETTIERUNGSÜBERWACHUNGSAUFGABENÜBERTRAGUNGSGESETZ',cat:'Recht',d:'Längster Wort Deutschlands ⚖️',l:10},{w:'DONAUDAMPFSCHIFFFAHRTSGESELLSCHAFT',cat:'Geschichte',d:'Historische Schifffahrtsgesellschaft 🚢',l:10},
    {w:'KRAFTFAHRZEUGHAFTPFLICHTVERSICHERUNG',cat:'Recht',d:'KFZ-Versicherung 🚗',l:10},{w:'ARBEITSUNFÄHIGKEITSBESCHEINIGUNG',cat:'Medizin',d:'Krankenschein 🏥',l:10},
  ],
  it:[
    {w:'SOL',cat:'Natura',d:'Riscalda la Terra ☀️',l:1},{w:'MAR',cat:'Natura',d:'Acqua salata 🌊',l:1},
    {w:'OCA',cat:'Animale',d:'Uccello di fattoria 🦢',l:1},{w:'APE',cat:'Animale',d:'Produce miele 🐝',l:1},
    {w:'GATTO',cat:'Animale',d:'Fa miao 🐱',l:2},{w:'CANE',cat:'Animale',d:'Fa bau 🐶',l:2},
    {w:'LUNA',cat:'Natura',d:'Appare di notte 🌙',l:2},{w:'PALLA',cat:'Giocattolo',d:'Rotonda e rimbalza ⚽',l:2},
    {w:'FIORE',cat:'Natura',d:'Ha petali 🌸',l:3},{w:'ALBERO',cat:'Natura',d:'Ha rami 🌳',l:3},
    {w:'PIOGGIA',cat:'Natura',d:'Cade dal cielo 🌧️',l:3},{w:'LIBRO',cat:'Oggetto',d:'Ha pagine 📚',l:3},
    {w:'CAVALLO',cat:'Animale',d:'Galoppa veloce 🐴',l:4},{w:'STELLA',cat:'Natura',d:'Brilla di notte ⭐',l:4},
    {w:'RANA',cat:'Animale',d:'Salta e gracida 🐸',l:4},{w:'SCUOLA',cat:'Luogo',d:'Dove impariamo 🏫',l:4},
    {w:'FARFALLA',cat:'Animale',d:'Ha ali colorate 🦋',l:5},{w:'ELEFANTE',cat:'Animale',d:'Ha la proboscide 🐘',l:5},
    {w:'TARTARUGA',cat:'Animale',d:'Cammina lentamente 🐢',l:5},{w:'CASTELLO',cat:'Luogo',d:'Dove vivono i re 🏰',l:5},
    {w:'COCCODRILLO',cat:'Animale',d:'Ha denti grandi 🐊',l:6},{w:'DELFINO',cat:'Animale',d:'Nuota e salta 🐬',l:6},
    {w:'PIANETA',cat:'Natura',d:'La Terra è un pianeta 🌍',l:6},{w:'FAMIGLIA',cat:'Persone',d:'Papà mamma figli 👨‍👩‍👧',l:6},
    {w:'IPPOPOTAMO',cat:'Animale',d:'Vive nel fiume 🦛',l:7},{w:'TELESCOPIO',cat:'Oggetto',d:'Per vedere le stelle 🔭',l:7},
    {w:'BIBLIOTECA',cat:'Luogo',d:'Piena di libri 📚',l:7},{w:'CIOCCOLATO',cat:'Cibo',d:'Dolce e delizioso 🍫',l:7},
    {w:'DINOSAURO',cat:'Animale',d:'Creatura antica 🦕',l:8},{w:'MATEMATICA',cat:'Scienza',d:'Numeri e equazioni ➕',l:8},
    {w:'COMUNICAZIONE',cat:'Concetto',d:'Condividere informazioni 💬',l:8},{w:'STRAORDINARIO',cat:'Aggettivo',d:'Fuori dal comune ✨',l:8},
    {w:'RESPONSABILITÀ',cat:'Concetto',d:'Essere responsabile 🏆',l:9},{w:'INTERDISCIPLINARE',cat:'Istruzione',d:'Varie discipline insieme 📚',l:9},
    {w:'SOSTENIBILITÀ',cat:'Natura',d:'Prendersi cura del pianeta 🌎',l:9},{w:'INTERNAZIONALIZZAZIONE',cat:'Affari',d:'Espandersi globalmente 🌍',l:9},
    {w:'ANTICOSTITUZIONALE',cat:'Diritto',d:'Contro la Costituzione ⚖️',l:10},{w:'ELETTROENCEFALOGRAMMA',cat:'Scienza',d:'Registrazione cerebrale 🧠',l:10},
    {w:'INCOSTITUZIONALMENTE',cat:'Diritto',d:'In modo incostituzionale ⚖️',l:10},{w:'PRECIPITEVOLISSIMEVOLMENTE',cat:'Poesia',d:'La parola più lunga italiana 🇮🇹',l:10},
  ],
};

const LANG_CFG={
  pt:{code:'pt-BR',draw:'🎲 Sortear',hear:'🔊 Ouvir',sub:'Arraste as letras na ordem certa',arrange:'Organize as letras aqui ⬇️',placeholder:'Arraste as letras aqui...',verify:'✅ Verificar',start:'Clique em Sortear! 🎲',win:'🎉 Perfeito! Você acertou!',winBody:'Todas as letras estão no lugar certo!',lose:'❌ Quase! Olha onde errou:',pos:['1ª','2ª','3ª','4ª','5ª','6ª','7ª','8ª','9ª','10ª','11ª','12ª','13ª','14ª','15ª'],got:'colocou',shouldBe:'mas deveria ser',placed:'deveria ser',congrats:'Parabéns! Você acertou!',levelUp:'🎉 Subiu para o Nível',errSpeak:(g,e)=>`Aqui é ${g}, mas deveria ser ${e}`},
  en:{code:'en-US',draw:'🎲 Draw',hear:'🔊 Listen',sub:'Drag the letters in the right order',arrange:'Arrange the letters here ⬇️',placeholder:'Drag the letters here...',verify:'✅ Check',start:'Click Draw! 🎲',win:'🎉 Perfect! You got it!',winBody:'All letters are in the right place!',lose:'❌ Almost! See where you went wrong:',pos:['1st','2nd','3rd','4th','5th','6th','7th','8th','9th','10th','11th','12th','13th','14th','15th'],got:'you put',shouldBe:'but should be',placed:'should be',congrats:'Congratulations! You got it right!',levelUp:'🎉 Level Up! Now Level',errSpeak:(g,e)=>`Here is ${g}, but it should be ${e}`},
  es:{code:'es-ES',draw:'🎲 Sortear',hear:'🔊 Escuchar',sub:'Arrastra las letras en orden',arrange:'Ordena las letras aquí ⬇️',placeholder:'Arrastra las letras aquí...',verify:'✅ Verificar',start:'¡Haz clic en Sortear! 🎲',win:'🎉 ¡Perfecto! ¡Lo lograste!',winBody:'¡Todas las letras están en el lugar correcto!',lose:'❌ ¡Casi! Mira dónde te equivocaste:',pos:['1ª','2ª','3ª','4ª','5ª','6ª','7ª','8ª','9ª','10ª','11ª','12ª','13ª','14ª','15ª'],got:'pusiste',shouldBe:'pero debería ser',placed:'debería ser',congrats:'¡Felicidades! ¡Lo lograste!',levelUp:'🎉 ¡Subiste al Nivel',errSpeak:(g,e)=>`Aquí es ${g}, pero debería ser ${e}`},
  fr:{code:'fr-FR',draw:'🎲 Tirer',hear:'🔊 Écouter',sub:"Glisse les lettres dans le bon ordre",arrange:'Organise les lettres ici ⬇️',placeholder:'Glisse les lettres ici...',verify:'✅ Vérifier',start:'Clique sur Tirer ! 🎲',win:'🎉 Parfait ! Tu as réussi !',winBody:'Toutes les lettres sont au bon endroit !',lose:'❌ Presque ! Regarde tes erreurs :',pos:['1ère','2ème','3ème','4ème','5ème','6ème','7ème','8ème','9ème','10ème','11ème','12ème','13ème','14ème','15ème'],got:'tu as mis',shouldBe:'mais devrait être',placed:'devrait être',congrats:'Félicitations ! Tu as réussi !',levelUp:'🎉 Niveau supérieur ! Niveau',errSpeak:(g,e)=>`Ici c'est ${g}, mais ça devrait être ${e}`},
  de:{code:'de-DE',draw:'🎲 Ziehen',hear:'🔊 Hören',sub:'Ziehe die Buchstaben in die richtige Reihenfolge',arrange:'Ordne die Buchstaben hier ⬇️',placeholder:'Buchstaben hierher ziehen...',verify:'✅ Prüfen',start:'Klick auf Ziehen! 🎲',win:'🎉 Perfekt! Du hast es geschafft!',winBody:'Alle Buchstaben sind an der richtigen Stelle!',lose:'❌ Fast! Schau wo du Fehler gemacht hast:',pos:['1.','2.','3.','4.','5.','6.','7.','8.','9.','10.','11.','12.','13.','14.','15.'],got:'du hast',shouldBe:'aber es sollte sein',placed:'sollte sein',congrats:'Herzlichen Glückwunsch!',levelUp:'🎉 Level erreicht! Level',errSpeak:(g,e)=>`Hier ist ${g}, aber es sollte ${e} sein`},
  it:{code:'it-IT',draw:'🎲 Estrarre',hear:'🔊 Ascolta',sub:"Trascina le lettere nell'ordine giusto",arrange:'Organizza le lettere qui ⬇️',placeholder:'Trascina le lettere qui...',verify:'✅ Verifica',start:'Clicca su Estrarre! 🎲',win:'🎉 Perfetto! Ce l\'hai fatta!',winBody:'Tutte le lettere sono al posto giusto!',lose:'❌ Quasi! Guarda dove hai sbagliato:',pos:['1ª','2ª','3ª','4ª','5ª','6ª','7ª','8ª','9ª','10ª','11ª','12ª','13ª','14ª','15ª'],got:'hai messo',shouldBe:'ma dovrebbe essere',placed:'dovrebbe essere',congrats:'Congratulazioni! Hai indovinato!',levelUp:'🎉 Livello superiore! Livello',errSpeak:(g,e)=>`Qui c'è ${g}, ma dovrebbe essere ${e}`},
};

const COLORS=['c0','c1','c2','c3','c4','c5','c6','c7'];
let currentLang='pt', currentLevel=1, xp=0, current=null, dragSrc=null, errorTimer=null;

// ─── LEVEL UI ────────────────────────────────────────────────────
function getLevelColor(n){return LEVELS[n-1].color;}
function getLevelLabel(n,lang){return LEVELS[n-1].label[lang]||LEVELS[n-1].label.en;}

function renderLevelUI(){
  const lv=LEVELS[currentLevel-1];
  const cfg=LANG_CFG[currentLang];
  const color=getLevelColor(currentLevel);
  const label=getLevelLabel(currentLevel,currentLang);
  const xpNeeded=lv.xpNeeded;

  document.getElementById('levelTitle').textContent=`📊 ${cfg.code==='pt-BR'?'Nível':cfg.code==='en-US'?'Level':cfg.code==='es-ES'?'Nivel':cfg.code==='fr-FR'?'Niveau':cfg.code==='de-DE'?'Level':'Livello'} ${currentLevel} — ${label}`;

  // stars
  const stars=currentLevel<=3?'⭐☆☆☆☆':currentLevel<=5?'⭐⭐☆☆☆':currentLevel<=7?'⭐⭐⭐☆☆':currentLevel<=9?'⭐⭐⭐⭐☆':'⭐⭐⭐⭐⭐';
  document.getElementById('starsDisplay').textContent=stars;

  const pct=currentLevel===10?100:Math.min(100,Math.round((xp/xpNeeded)*100));
  const fill=document.getElementById('levelBarFill');
  fill.style.width=pct+'%';
  fill.style.background=`linear-gradient(90deg,${color},${color}cc)`;

  const xpLbl=document.getElementById('xpLabel');
  const nextLbl=document.getElementById('nextLvlLabel');
  const acertos=cfg.code==='pt-BR'?'acertos':cfg.code==='en-US'?'correct':cfg.code==='es-ES'?'correctas':cfg.code==='fr-FR'?'correct':cfg.code==='de-DE'?'richtig':'corrette';
  xpLbl.textContent=`${xp} / ${xpNeeded===999?'∞':xpNeeded} ${acertos}`;

  if(currentLevel<10){
    const nextLabel=getLevelLabel(currentLevel+1,currentLang);
    const nextWord=cfg.code==='pt-BR'?'Próximo':cfg.code==='en-US'?'Next':cfg.code==='es-ES'?'Siguiente':cfg.code==='fr-FR'?'Suivant':cfg.code==='de-DE'?'Nächstes':'Prossimo';
    const lvWord=cfg.code==='pt-BR'?'Nível':cfg.code==='en-US'?'Level':cfg.code==='es-ES'?'Nivel':cfg.code==='fr-FR'?'Niveau':cfg.code==='de-DE'?'Level':'Livello';
    nextLbl.textContent=`${nextWord}: ${lvWord} ${currentLevel+1}`;
  } else {
    nextLbl.textContent='🏆 Nível Máximo!';
  }

  // dots
  const dotsEl=document.getElementById('levelDots');
  dotsEl.innerHTML='';
  for(let i=1;i<=10;i++){
    const dot=document.createElement('div');
    dot.className='lvl-dot'+(i<currentLevel?' done':i===currentLevel?' active':i>currentLevel+1?' locked':'');
    dot.textContent=i;
    const c=getLevelColor(i);
    if(i<=currentLevel){dot.style.background=c;dot.style.borderColor=c;dot.style.color='white';}
    dot.addEventListener('click',()=>{
      if(i>currentLevel+1) return;
      currentLevel=i; xp=0; renderLevelUI();
    });
    dotsEl.appendChild(dot);
  }
}

// ─── LANG ────────────────────────────────────────────────────────
function setLang(lang){
  currentLang=lang; currentLevel=1; xp=0;
  document.querySelectorAll('.lang-btn').forEach(b=>b.classList.toggle('active',b.getAttribute('data-lang')===lang));
  document.getElementById('gameInner').className='game-inner lang-'+lang;
  document.getElementById('wordStage').className='word-stage lang-'+lang;
  const d=LANG_CFG[lang];
  document.getElementById('subTxt').textContent=d.sub;
  document.getElementById('btnDraw').textContent=d.draw;
  document.getElementById('btnSpeak').textContent=d.hear;
  document.getElementById('idleMsg').textContent=d.start;
  document.getElementById('idleMsg').style.display='block';
  document.getElementById('bigWord').style.display='none';
  document.getElementById('catBadge').style.display='none';
  document.getElementById('hint').style.display='none';
  document.getElementById('dropZone').style.display='none';
  document.getElementById('dropZone').className='drop-zone';
  document.getElementById('dropLabel').style.display='none';
  document.getElementById('tilesPool').style.display='none';
  document.getElementById('tilesPool').innerHTML='';
  document.getElementById('checkBtn').style.display='none';
  document.getElementById('feedbackBox').className='feedback-box';
  document.getElementById('levelUpBanner').style.display='none';
  document.getElementById('dropPlaceholder').textContent=d.placeholder;
  document.getElementById('btnSpeak').disabled=true;
  document.getElementById('confetti').innerHTML='';
  current=null; renderLevelUI();
}

function drawWord(){
  const d=LANG_CFG[currentLang];
  const pool=WORDS_DB[currentLang].filter(w=>w.l===currentLevel);
  const fallback=WORDS_DB[currentLang].filter(w=>w.l<=currentLevel);
  const src=pool.length>0?pool:fallback;
  const item=src[Math.floor(Math.random()*src.length)];
  current=item; clearAllHighlights();
  document.getElementById('idleMsg').style.display='none';
  const bw=document.getElementById('bigWord');
  bw.textContent=item.w; bw.style.display='block';
  bw.style.animation='none'; void bw.offsetWidth; bw.style.animation='';

  // adjust font size for long words
  const len=item.w.length;
  bw.style.fontSize=len<=5?'50px':len<=8?'38px':len<=12?'28px':len<=16?'22px':'16px';
  bw.style.letterSpacing=len<=8?'4px':len<=12?'2px':'1px';

  document.getElementById('catBadge').textContent=item.cat;
  document.getElementById('catBadge').style.display='inline-block';
  document.getElementById('hint').textContent=item.d;
  document.getElementById('hint').style.display='block';
  document.getElementById('confetti').innerHTML='';
  document.getElementById('btnSpeak').disabled=false;
  document.getElementById('feedbackBox').className='feedback-box';
  document.getElementById('levelUpBanner').style.display='none';
  const dz=document.getElementById('dropZone');
  dz.style.display='flex'; dz.className='drop-zone';
  document.getElementById('dropLabel').textContent=d.arrange;
  document.getElementById('dropLabel').style.display='block';
  document.getElementById('dropPlaceholder').textContent=d.placeholder;
  document.getElementById('dropPlaceholder').style.display='block';
  buildTiles(item.w);
  document.getElementById('checkBtn').textContent=d.verify;
  document.getElementById('checkBtn').style.display='inline-flex';
  document.getElementById('checkBtn').disabled=true;
  setTimeout(()=>speakWord(),500);
}

function buildTiles(word){
  const pool=document.getElementById('tilesPool');
  pool.innerHTML=''; pool.style.display='flex';
  Array.from(document.getElementById('dropZone').querySelectorAll('.tile-wrap')).forEach(t=>t.remove());
  const letters=[...word].sort(()=>Math.random()-.5);
  letters.forEach((l,i)=>pool.appendChild(createTileWrap(l,i,COLORS[i%COLORS.length],word.length)));
}

function getTileSize(wordLen){
  if(wordLen<=5) return {w:46,h:50,fs:22};
  if(wordLen<=8) return {w:40,h:44,fs:19};
  if(wordLen<=12) return {w:34,h:38,fs:16};
  if(wordLen<=16) return {w:28,h:32,fs:13};
  return {w:24,h:28,fs:11};
}

function createTileWrap(letter,delay,colorClass,wordLen){
  const sz=getTileSize(wordLen);
  const wrap=document.createElement('div'); wrap.className='tile-wrap';
  const arrow=document.createElement('div'); arrow.className='arrow-label';
  const atxt=document.createElement('div'); atxt.className='arrow-txt'; atxt.textContent='';
  const atri=document.createElement('div'); atri.className='arrow-tri';
  arrow.appendChild(atxt); arrow.appendChild(atri); wrap.appendChild(arrow);
  const t=document.createElement('div');
  t.className='tile '+colorClass; t.draggable=true;
  t.style.animationDelay=(delay*0.06)+'s';
  t.style.width=sz.w+'px'; t.style.height=sz.h+'px'; t.style.fontSize=sz.fs+'px';
  t.setAttribute('data-letter',letter); t.setAttribute('data-color',colorClass);
  t.textContent=letter;
  t.addEventListener('dragstart',e=>{dragSrc=wrap;t.classList.add('dragging');e.dataTransfer.effectAllowed='move';e.dataTransfer.setData('text/plain',letter);speakLetter(letter,t);});
  t.addEventListener('dragend',()=>{t.classList.remove('dragging');dragSrc=null;updateCheckBtn();});
  t.addEventListener('click',()=>{
    const dz=document.getElementById('dropZone'),pl=document.getElementById('tilesPool');
    speakLetter(letter,t);
    if(wrap.parentNode===pl){t.classList.add('in-drop');dz.appendChild(wrap);updateDropPlaceholder();}
    else{t.classList.remove('in-drop','correct-tile','wrong-tile');pl.appendChild(wrap);updateDropPlaceholder();}
    updateCheckBtn();
  });
  wrap.addEventListener('dragover',e=>{
    if(dragSrc&&dragSrc!==wrap&&wrap.parentNode===document.getElementById('dropZone')){
      e.preventDefault();
      const dz=document.getElementById('dropZone'),all=[...dz.querySelectorAll('.tile-wrap')];
      const ti=all.indexOf(wrap),si=all.indexOf(dragSrc);
      if(si<ti)dz.insertBefore(dragSrc,wrap.nextSibling);else dz.insertBefore(dragSrc,wrap);
    }
  });
  wrap.appendChild(t); return wrap;
}

const dz=document.getElementById('dropZone');
dz.addEventListener('dragover',e=>{e.preventDefault();dz.classList.add('drag-over');});
dz.addEventListener('dragleave',()=>dz.classList.remove('drag-over'));
dz.addEventListener('drop',e=>{
  e.preventDefault();dz.classList.remove('drag-over');
  if(dragSrc&&dragSrc.parentNode!==dz){dragSrc.querySelector('.tile').classList.add('in-drop');dz.appendChild(dragSrc);updateDropPlaceholder();updateCheckBtn();}
});

function updateDropPlaceholder(){
  document.getElementById('dropPlaceholder').style.display=document.getElementById('dropZone').querySelectorAll('.tile-wrap').length===0?'block':'none';
}
function updateCheckBtn(){
  const count=document.getElementById('dropZone').querySelectorAll('.tile-wrap').length;
  document.getElementById('checkBtn').disabled=!current||count!==[...current.w].length;
}
function clearAllHighlights(){
  document.querySelectorAll('.tile').forEach(t=>t.classList.remove('highlighted','wrong-tile','correct-tile'));
  document.querySelectorAll('.arrow-label').forEach(a=>a.classList.remove('visible'));
  if(errorTimer)clearTimeout(errorTimer);
}
function highlightErrors(errors,tileWraps){
  let i=0;clearAllHighlights();
  function next(){
    if(i>0){const pw=tileWraps[errors[i-1].pos];if(pw){pw.querySelector('.tile').classList.remove('highlighted');pw.querySelector('.arrow-label').classList.remove('visible');}}
    if(i>=errors.length)return;
    const err=errors[i],w=tileWraps[err.pos];
    if(w){const tile=w.querySelector('.tile'),arrow=w.querySelector('.arrow-label');tile.classList.add('highlighted');arrow.querySelector('.arrow-txt').textContent=LANG_CFG[currentLang].placed+' '+err.exp;arrow.classList.add('visible');w.scrollIntoView({behavior:'smooth',block:'nearest'});}
    const norm=s=>s.normalize('NFD').replace(/[\u0300-\u036f]/g,'');
    const u=new SpeechSynthesisUtterance(LANG_CFG[currentLang].errSpeak(norm(err.got),norm(err.exp)));
    u.lang=LANG_CFG[currentLang].code;u.rate=0.82;u.pitch=1.1;
    u.onend=()=>{i++;errorTimer=setTimeout(next,300);};
    window.speechSynthesis.cancel();window.speechSynthesis.speak(u);
  }
  next();
}

function checkAnswer(){
  if(!current)return;clearAllHighlights();
  const dz=document.getElementById('dropZone');
  const tileWraps=[...dz.querySelectorAll('.tile-wrap')];
  const correct=[...current.w],d=LANG_CFG[currentLang];
  const fb=document.getElementById('feedbackBox');
  let errors=[];
  tileWraps.forEach((w,i)=>{
    const tile=w.querySelector('.tile'),got=tile.getAttribute('data-letter'),exp=correct[i];
    tile.classList.remove('correct-tile','wrong-tile','in-drop');
    if(got===exp)tile.classList.add('correct-tile');
    else{tile.classList.add('wrong-tile');errors.push({pos:i,got,exp});}
  });
  if(errors.length===0){
    fb.className='feedback-box win';
    document.getElementById('fbTitle').textContent=d.win;
    document.getElementById('fbBody').textContent=d.winBody;
    dz.className='drop-zone correct-zone';
    launchConfetti(); speak(d.congrats);
    // XP gain
    xp++;
    const lv=LEVELS[currentLevel-1];
    if(xp>=lv.xpNeeded&&currentLevel<10){
      currentLevel++; xp=0;
      const banner=document.getElementById('levelUpBanner');
      const lvWord=d.code==='pt-BR'?'Nível':d.code==='en-US'?'Level':d.code==='es-ES'?'Nivel':d.code==='fr-FR'?'Niveau':d.code==='de-DE'?'Level':'Livello';
      banner.textContent=`🎉 ${lvWord} ${currentLevel} — ${getLevelLabel(currentLevel,currentLang)}! 🚀`;
      banner.style.background=`linear-gradient(135deg,${getLevelColor(currentLevel)}33,${getLevelColor(currentLevel)}66)`;
      banner.style.borderColor=getLevelColor(currentLevel);
      banner.style.display='block';
      setTimeout(()=>{banner.style.animation='none';void banner.offsetWidth;banner.style.animation='';},50);
    }
    renderLevelUI();
  } else {
    fb.className='feedback-box lose';
    document.getElementById('fbTitle').textContent=d.lose;
    dz.className='drop-zone wrong-zone';
    const ul=document.createElement('ul');ul.className='err-list';
    errors.forEach(err=>{
      const li=document.createElement('li');
      const ord=d.pos[err.pos]||`${err.pos+1}`;
      li.innerHTML=`${ord} — ${d.got} <span class="err-pill">${err.got}</span> ${d.shouldBe} <span class="ok-pill">${err.exp}</span>`;
      li.addEventListener('click',()=>highlightErrors([err],[...document.getElementById('dropZone').querySelectorAll('.tile-wrap')]));
      ul.appendChild(li);
    });
    document.getElementById('fbBody').innerHTML='';document.getElementById('fbBody').appendChild(ul);
    setTimeout(()=>highlightErrors(errors,[...dz.querySelectorAll('.tile-wrap')]),400);
    setTimeout(()=>{tileWraps.forEach(w=>{const t=w.querySelector('.tile');t.classList.remove('correct-tile','wrong-tile','highlighted');w.querySelector('.arrow-label').classList.remove('visible');});dz.className='drop-zone';},errors.length*3800+2000);
  }
}

function speakLetter(letter,tile){
  if(!window.speechSynthesis)return;
  window.speechSynthesis.cancel();
  if(tile){tile.classList.add('speaking');setTimeout(()=>tile.classList.remove('speaking'),600);}
  const norm=letter.normalize('NFD').replace(/[\u0300-\u036f]/g,'');
  const u=new SpeechSynthesisUtterance(norm.toLowerCase());
  u.lang=LANG_CFG[currentLang].code;u.rate=0.75;u.pitch=1.2;
  window.speechSynthesis.speak(u);
}
function speakWord(){if(!current)return;speak(current.w.toLowerCase());}
function speak(text){
  if(!window.speechSynthesis)return;
  window.speechSynthesis.cancel();
  const u=new SpeechSynthesisUtterance(text);
  u.lang=LANG_CFG[currentLang].code;u.rate=0.85;u.pitch=1.1;
  window.speechSynthesis.speak(u);
}
function launchConfetti(){
  const wrap=document.getElementById('confetti');wrap.innerHTML='';
  const colors=['#f97316','#3b82f6','#10b981','#ef4444','#8b5cf6','#ec4899','#fbbf24','#22c55e','#06b6d4'];
  for(let i=0;i<40;i++){
    const d=document.createElement('div');d.className='dot';
    d.style.left=(Math.random()*100)+'%';d.style.top=(Math.random()*20)+'%';
    d.style.background=colors[Math.floor(Math.random()*colors.length)];
    d.style.animationDelay=(Math.random()*.8)+'s';d.style.animationDuration=(1+Math.random()*.8)+'s';
    const sz=(5+Math.random()*7)+'px';d.style.width=sz;d.style.height=sz;
    wrap.appendChild(d);
  }
}

// init
renderLevelUI();
</script>
