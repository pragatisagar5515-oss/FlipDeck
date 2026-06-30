<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>FlipDeck — Draw. Flip. Animate.</title>
<style>
  :root{
    --bg-deep:#14161b;
    --bg-panel:#1c1f26;
    --bg-panel-2:#23272f;
    --paper:#f4efe2;
    --paper-line:#d8cfb6;
    --ink:#2a2620;
    --amber:#ffb238;
    --amber-dim:#caa15a;
    --red:#ff5d5d;
    --text:#ece8df;
    --text-dim:#9b9f8;
    --text-dim2:#8b8e96;
    --radius:10px;
    --display: Futura, "Century Gothic", "Trebuchet MS", sans-serif;
    --body: "Trebuchet MS", "Segoe UI", sans-serif;
    --mono: "Courier New", ui-monospace, monospace;
  }
  *{box-sizing:border-box;}
  html{scroll-behavior:smooth;}
  body{
    margin:0;
    background:var(--bg-deep);
    color:var(--text);
    font-family:var(--body);
    -webkit-font-smoothing:antialiased;
  }
  @media (prefers-reduced-motion: reduce){
    *{animation-duration:0.001s !important; transition-duration:0.001s !important;}
  }

  /* ---------- sprocket strip background flourish ---------- */
  .sprockets{
    position:fixed; top:0; left:0; width:18px; height:100%;
    background-image: radial-gradient(circle, var(--bg-panel-2) 3px, transparent 3.5px);
    background-size: 18px 28px;
    background-position: 4px 10px;
    opacity:.5;
    z-index:0;
  }
  .sprockets.right{ left:auto; right:0; }

  /* ---------- NAV ---------- */
  nav{
    position:sticky; top:0; z-index:50;
    display:flex; align-items:center; justify-content:space-between;
    padding:18px 36px;
    background:rgba(20,22,27,.88);
    backdrop-filter:blur(6px);
    border-bottom:1px solid #2a2d35;
  }
  .logo{
    font-family:var(--display);
    font-size:22px; letter-spacing:.5px; font-weight:700;
    color:var(--text); display:flex; align-items:center; gap:10px;
  }
  .logo .corner{
    width:20px;height:20px;background:var(--amber);
    clip-path: polygon(0 0, 100% 0, 0 100%);
    display:inline-block;
    animation: flipcorner 2.6s ease-in-out infinite;
  }
  @keyframes flipcorner{
    0%,100%{ transform: rotate(0deg); }
    50%{ transform: rotate(-18deg) scaleX(.85); }
  }
  nav .links{ display:flex; gap:30px; font-size:14px; color:var(--text-dim2); }
  nav .links a{ color:var(--text-dim2); text-decoration:none; }
  nav .links a:hover{ color:var(--amber); }
  nav .cta{
    background:var(--amber); color:#1a1300; border:none;
    padding:10px 20px; border-radius:999px; font-weight:700; font-size:14px;
    cursor:pointer; font-family:var(--body);
  }
  nav .cta:hover{ background:#ffc35e; }

  /* ---------- HERO ---------- */
  header.hero{
    position:relative;
    padding:90px 36px 70px;
    display:grid; grid-template-columns:1.1fr .9fr; gap:40px;
    align-items:center;
    max-width:1280px; margin:0 auto;
    overflow:hidden;
  }
  .eyebrow{
    font-family:var(--mono); font-size:12px; letter-spacing:2px; text-transform:uppercase;
    color:var(--amber); margin-bottom:18px; display:flex; align-items:center; gap:8px;
  }
  .eyebrow .dot{ width:7px;height:7px;border-radius:50%;background:var(--red); animation:pulse 1.4s infinite; }
  @keyframes pulse{ 0%,100%{opacity:1} 50%{opacity:.25} }
  h1.title{
    font-family:var(--display);
    font-size:clamp(40px, 5.4vw, 72px);
    line-height:1.02;
    margin:0 0 22px;
    font-weight:700;
    letter-spacing:-0.5px;
  }
  h1.title em{
    font-style:normal; color:var(--amber);
    position:relative;
  }
  .hero p.lead{
    font-size:18px; line-height:1.6; color:#c8c4b8; max-width:480px; margin:0 0 30px;
  }
  .hero-ctas{ display:flex; gap:14px; }
  .btn-primary{
    background:var(--amber); color:#1a1300; border:none; padding:15px 28px;
    border-radius:999px; font-weight:700; font-size:15px; cursor:pointer;
    font-family:var(--body);
    box-shadow:0 8px 24px -8px rgba(255,178,56,.6);
  }
  .btn-primary:hover{ background:#ffc35e; transform:translateY(-1px); }
  .btn-ghost{
    background:transparent; color:var(--text); border:1px solid #3a3e47; padding:15px 24px;
    border-radius:999px; font-weight:600; font-size:15px; cursor:pointer; font-family:var(--body);
  }
  .btn-ghost:hover{ border-color:var(--amber); color:var(--amber); }

  /* flipbook signature animation */
  .flipbook-rig{
    position:relative; height:380px; display:flex; align-items:center; justify-content:center;
    perspective:1200px;
  }
  .flip-stack{ position:relative; width:230px; height:300px; }
  .flip-page{
    position:absolute; top:0; left:0; width:230px; height:300px;
    background:var(--paper);
    border-radius:6px;
    box-shadow:0 18px 40px -12px rgba(0,0,0,.6);
    transform-origin:left center;
    border:1px solid var(--paper-line);
  }
  .flip-page svg{ width:100%; height:100%; }
  .flip-page:nth-child(1){ transform: rotate(-3deg) translate(-6px,4px); z-index:1; }
  .flip-page:nth-child(2){ transform: rotate(2deg) translate(4px,-2px); z-index:2; }
  .flip-page:nth-child(3){ z-index:3; animation: pageflip 3.2s ease-in-out infinite; }
  @keyframes pageflip{
    0%, 18%{ transform: rotateY(0deg); }
    50%, 68%{ transform: rotateY(-150deg); }
    100%{ transform: rotateY(0deg); }
  }

  /* ---------- SECTION HEADERS ---------- */
  .section{ max-width:1280px; margin:0 auto; padding:70px 36px; position:relative; }
  .section-head{ margin-bottom:42px; max-width:620px; }
  .section-head .eyebrow{ margin-bottom:10px; }
  .section-head h2{
    font-family:var(--display); font-size:clamp(28px,3.2vw,40px); margin:0 0 12px; font-weight:700;
  }
  .section-head p{ color:#a9a59a; font-size:16px; line-height:1.6; margin:0; }

  /* ---------- FEATURE FILMSTRIP ---------- */
  .filmstrip{
    display:flex; gap:0; overflow-x:auto; padding:18px 0;
    border-top:2px dashed #343844; border-bottom:2px dashed #343844;
  }
  .frame-card{
    flex:0 0 240px;
    background:var(--bg-panel);
    border-right:1px dashed #343844;
    padding:26px 22px;
    position:relative;
  }
  .frame-card:last-child{ border-right:none; }
  .frame-card .num{
    font-family:var(--mono); font-size:11px; color:var(--amber-dim); letter-spacing:1px;
  }
  .frame-card .icon{ font-size:28px; margin:14px 0 12px; }
  .frame-card h3{ font-family:var(--display); font-size:17px; margin:0 0 8px; }
  .frame-card p{ font-size:13.5px; color:#9b988c; line-height:1.55; margin:0; }

  /* ---------- APP SECTION (the real tool) ---------- */
  #studio{
    background:var(--bg-panel);
    border-top:1px solid #2a2d35;
    border-bottom:1px solid #2a2d35;
  }
  .studio-inner{ max-width:1280px; margin:0 auto; padding:60px 36px 80px; }
  .studio-grid{
    display:grid; grid-template-columns:230px 1fr 260px; gap:24px; margin-top:30px;
    align-items:start;
  }
  .panel{
    background:var(--bg-panel-2); border:1px solid #2e323b; border-radius:var(--radius);
    padding:18px;
  }
  .panel h4{
    font-family:var(--mono); font-size:11px; letter-spacing:1.5px; text-transform:uppercase;
    color:var(--text-dim2); margin:0 0 14px;
  }
  .tool-row{ display:flex; flex-wrap:wrap; gap:8px; margin-bottom:18px; }
  .tool-btn{
    width:44px; height:44px; border-radius:8px; border:1px solid #353a44; background:#1a1d23;
    color:var(--text); cursor:pointer; font-size:18px; display:flex; align-items:center; justify-content:center;
  }
  .tool-btn.active{ background:var(--amber); color:#1a1300; border-color:var(--amber); }
  .tool-btn:hover{ border-color:var(--amber); }
  label.mini{ font-size:12px; color:var(--text-dim2); display:block; margin:10px 0 6px; }
  input[type=range]{ width:100%; accent-color:var(--amber); }
  input[type=color]{
    width:100%; height:38px; border-radius:8px; border:1px solid #353a44; background:#1a1d23; cursor:pointer; padding:2px;
  }
  .swatches{ display:flex; flex-wrap:wrap; gap:6px; margin-top:8px; }
  .swatch{ width:22px; height:22px; border-radius:50%; cursor:pointer; border:2px solid #1a1d23; }
  .swatch:hover{ border-color:var(--amber); }

  .canvas-wrap{
    background:#10121600; display:flex; flex-direction:column; align-items:center; gap:16px;
  }
  .canvas-frame{
    background:repeating-conic-gradient(#2c2f37 0% 25%, #23262d 0% 50%) 0 0/20px 20px;
    padding:14px; border-radius:var(--radius); border:1px solid #2e323b;
  }
  #drawCanvas{
    background:var(--paper);
    border-radius:4px;
    cursor:crosshair;
    touch-action:none;
    display:block;
  }
  .playback-bar{
    display:flex; align-items:center; gap:14px; background:var(--bg-panel-2);
    border:1px solid #2e323b; border-radius:999px; padding:10px 18px; width:100%;
    justify-content:center;
  }
  .pb-btn{
    background:none; border:none; color:var(--text); font-size:18px; cursor:pointer;
    width:36px; height:36px; border-radius:50%; display:flex; align-items:center; justify-content:center;
  }
  .pb-btn:hover{ background:#2e323b; }
  .pb-btn.play{ background:var(--amber); color:#1a1300; }
  .pb-btn.play:hover{ background:#ffc35e; }
  .fps-readout{ font-family:var(--mono); font-size:12px; color:var(--text-dim2); min-width:70px; text-align:center;}

  .frames-panel{ display:flex; flex-direction:column; height:100%; }
  .frames-list{
    display:flex; flex-direction:column; gap:8px; max-height:520px; overflow-y:auto; padding-right:4px;
  }
  .frame-thumb{
    position:relative; border:2px solid #353a44; border-radius:8px; overflow:hidden; cursor:pointer;
    background:var(--paper); aspect-ratio:4/3;
  }
  .frame-thumb.active{ border-color:var(--amber); }
  .frame-thumb canvas{ width:100%; height:100%; display:block; }
  .frame-thumb .tag{
    position:absolute; bottom:2px; left:4px; font-family:var(--mono); font-size:10px;
    background:rgba(0,0,0,.55); color:#fff; padding:1px 5px; border-radius:3px;
  }
  .frame-thumb .del{
    position:absolute; top:2px; right:2px; background:rgba(0,0,0,.55); color:#fff; border:none;
    width:18px; height:18px; border-radius:4px; font-size:11px; cursor:pointer; line-height:1;
  }
  .frame-thumb .del:hover{ background:var(--red); }
  .add-frame-btn{
    margin-top:10px; background:var(--amber); color:#1a1300; border:none; border-radius:8px;
    padding:12px; font-weight:700; cursor:pointer; font-family:var(--body); font-size:13px;
  }
  .add-frame-btn:hover{ background:#ffc35e; }
  .toggle-row{ display:flex; align-items:center; justify-content:space-between; margin-top:14px; font-size:13px; color:var(--text-dim2); }
  .toggle-row input{ accent-color:var(--amber); }

  /* ---------- FOOTER ---------- */
  footer{
    padding:50px 36px; text-align:center; color:#6b6e76; font-size:13px;
    border-top:1px solid #2a2d35;
  }
  footer .corner{
    width:14px;height:14px;background:var(--amber);
    clip-path: polygon(0 0, 100% 0, 0 100%);
    display:inline-block; margin-right:6px; vertical-align:middle;
  }

  @media (max-width:980px){
    header.hero{ grid-template-columns:1fr; }
    .studio-grid{ grid-template-columns:1fr; }
    .frames-list{ flex-direction:row; overflow-x:auto; max-height:none; }
    .frame-thumb{ min-width:120px; }
    nav .links{ display:none; }
  }
</style>
</head>
<body>

<div class="sprockets"></div>
<div class="sprockets right"></div>

<nav>
  <div class="logo"><span class="corner"></span>FlipDeck</div>
  <div class="links">
    <a href="#how">How it works</a>
    <a href="#studio">Studio</a>
    <a href="#tips">Tips</a>
  </div>
  <button class="cta" onclick="document.getElementById('studio').scrollIntoView()">Open Studio</button>
</nav>

<header class="hero">
  <div>
    <div class="eyebrow"><span class="dot"></span> FRAME 1 OF INFINITY</div>
    <h1 class="title">Draw a line.<br>Flip a page.<br>Make it <em>move</em>.</h1>
    <p class="lead">FlipDeck is a frame-by-frame animation studio that runs right in your browser. Sketch a frame, duplicate it, nudge it, and watch your drawings come to life — no install, no signup, just a blank page and a pencil.</p>
    <div class="hero-ctas">
      <button class="btn-primary" onclick="document.getElementById('studio').scrollIntoView()">Start animating →</button>
      <button class="btn-ghost" onclick="document.getElementById('how').scrollIntoView()">See how it works</button>
    </div>
  </div>
  <div class="flipbook-rig">
    <div class="flip-stack">
      <div class="flip-page"></div>
      <div class="flip-page"></div>
      <div class="flip-page">
        <svg viewBox="0 0 230 300"><circle cx="115" cy="150" r="46" fill="none" stroke="#2a2620" stroke-width="6"/><line x1="115" y1="150" x2="115" y2="112" stroke="#2a2620" stroke-width="6" stroke-linecap="round"/><line x1="115" y1="150" x2="146" y2="160" stroke="#2a2620" stroke-width="6" stroke-linecap="round"/></svg>
      </div>
    </div>
  </div>
</header>

<section class="section" id="how">
  <div class="section-head">
    <div class="eyebrow">THE PROCESS</div>
    <h2>Animation, broken into frames you can actually hold</h2>
    <p>Every animation is just a flipbook in disguise. FlipDeck keeps that idea front and center — your timeline is a literal stack of drawings, not a confusing graph of keyframes.</p>
  </div>
  <div class="filmstrip">
    <div class="frame-card">
      <div class="num">FRAME 01</div>
      <div class="icon">✏️</div>
      <h3>Sketch</h3>
      <p>Pick a brush, pick a color, and draw straight onto the paper canvas. Pressure-free, distraction-free.</p>
    </div>
    <div class="frame-card">
      <div class="num">FRAME 02</div>
      <div class="icon">📑</div>
      <h3>Duplicate</h3>
      <p>Copy the current frame so your next drawing starts from where the last one left off.</p>
    </div>
    <div class="frame-card">
      <div class="num">FRAME 03</div>
      <div class="icon">🫥</div>
      <h3>Onion skin</h3>
      <p>See a ghost of the previous frame underneath so every new line lands exactly where it should.</p>
    </div>
    <div class="frame-card">
      <div class="num">FRAME 04</div>
      <div class="icon">▶️</div>
      <h3>Play it back</h3>
      <p>Hit play and watch your stack of still drawings turn into motion, frame by frame, at your chosen speed.</p>
    </div>
  </div>
</section>

<section id="studio">
  <div class="studio-inner">
    <div class="section-head">
      <div class="eyebrow">THE STUDIO</div>
      <h2>Your desk. Your pencil. Your flipbook.</h2>
      <p>This is a fully working animation tool — draw, add frames, and press play below.</p>
    </div>

    <div class="studio-grid">
      <!-- LEFT: TOOLS -->
      <div class="panel">
        <h4>Brush</h4>
        <div class="tool-row">
          <button class="tool-btn active" id="toolPencil" title="Pencil">✏️</button>
          <button class="tool-btn" id="toolEraser" title="Eraser">🧽</button>
          <button class="tool-btn" id="toolFill" title="Clear frame">🗑️</button>
        </div>
        <label class="mini">Size: <span id="sizeVal">5</span>px</label>
        <input type="range" id="sizeRange" min="1" max="40" value="5">
        <label class="mini">Color</label>
        <input type="color" id="colorPicker" value="#2a2620">
        <div class="swatches" id="swatches"></div>

        <h4 style="margin-top:22px;">Onion skin</h4>
        <div class="toggle-row">
          <span>Show previous frame</span>
          <input type="checkbox" id="onionToggle" checked>
        </div>
      </div>

      <!-- CENTER: CANVAS -->
      <div class="canvas-wrap">
        <div class="canvas-frame">
          <canvas id="drawCanvas" width="640" height="480"></canvas>
        </div>
        <div class="playback-bar">
          <button class="pb-btn" id="prevFrame" title="Previous frame">⏮</button>
          <button class="pb-btn play" id="playBtn" title="Play">▶</button>
          <button class="pb-btn" id="nextFrame" title="Next frame">⏭</button>
          <span class="fps-readout" id="fpsReadout">8 fps</span>
          <input type="range" id="fpsRange" min="1" max="24" value="8" style="width:100px;">
        </div>
      </div>

      <!-- RIGHT: FRAMES -->
      <div class="panel frames-panel">
        <h4>Timeline (<span id="frameCount">1</span> frames)</h4>
        <div class="frames-list" id="framesList"></div>
        <button class="add-frame-btn" id="addFrameBtn">+ Duplicate &amp; add frame</button>
        <button class="add-frame-btn" id="addBlankBtn" style="background:#2e323b;color:var(--text);margin-top:8px;">+ Add blank frame</button>
      </div>
    </div>
  </div>
</section>

<section class="section" id="tips">
  <div class="section-head">
    <div class="eyebrow">TIPS FROM THE DESK</div>
    <h2>Small habits that make animation feel like magic</h2>
  </div>
  <div class="filmstrip">
    <div class="frame-card">
      <div class="num">TIP</div>
      <div class="icon">🐌</div>
      <h3>Slow it down</h3>
      <p>Lower the fps while you're working so you can actually see what each frame contributes.</p>
    </div>
    <div class="frame-card">
      <div class="num">TIP</div>
      <div class="icon">👻</div>
      <h3>Trust the ghost</h3>
      <p>Onion skin isn't cheating — every animator alive leans on the frame before it.</p>
    </div>
    <div class="frame-card">
      <div class="num">TIP</div>
      <div class="icon">🔁</div>
      <h3>Loop short, loop often</h3>
      <p>Four good frames looped beat forty rushed ones. Start small and let the loop breathe.</p>
    </div>
  </div>
</section>

<footer>
  <span class="corner"></span>FlipDeck — a flipbook for people who'd rather draw than configure.
</footer>

<script>
(function(){
  const canvas = document.getElementById('drawCanvas');
  const ctx = canvas.getContext('2d');
  const W = canvas.width, H = canvas.height;

  let frames = [];      // array of ImageData-producing dataURLs
  let current = 0;
  let tool = 'pencil';
  let brushSize = 5;
  let brushColor = '#2a2620';
  let onion = true;
  let drawing = false;
  let lastX=0, lastY=0;
  let playing = false;
  let playTimer = null;
  let fps = 8;

  const offscreen = document.createElement('canvas');
  offscreen.width = W; offscreen.height = H;
  const octx = offscreen.getContext('2d');

  function blankPaper(c){
    c.fillStyle = '#f4efe2';
    c.fillRect(0,0,W,H);
  }

  function newBlankFrameData(){
    blankPaper(octx);
    return offscreen.toDataURL();
  }

  function init(){
    frames.push(newBlankFrameData());
    renderCurrentToCanvas();
    renderThumbnails();
    bindSwatches();
    bindEvents();
  }

  function loadDataURLToCtx(dataURL, targetCtx, cb){
    const img = new Image();
    img.onload = function(){
      targetCtx.clearRect(0,0,W,H);
      targetCtx.drawImage(img,0,0,W,H);
      if(cb) cb();
    };
    img.src = dataURL;
  }

  function renderCurrentToCanvas(){
    ctx.clearRect(0,0,W,H);
    blankPaper(ctx);
    if(onion && current > 0){
      const prevImg = new Image();
      prevImg.onload = function(){
        ctx.globalAlpha = 0.28;
        ctx.drawImage(prevImg,0,0,W,H);
        ctx.globalAlpha = 1;
        drawCurrentOnTop();
      };
      prevImg.src = frames[current-1];
    } else {
      drawCurrentOnTop();
    }
  }

  function drawCurrentOnTop(){
    const img = new Image();
    img.onload = function(){
      ctx.drawImage(img,0,0,W,H);
    };
    img.src = frames[current];
  }

  function saveCurrentFrame(){
    frames[current] = canvas.toDataURL();
  }

  function renderThumbnails(){
    const list = document.getElementById('framesList');
    list.innerHTML = '';
    frames.forEach((data, i) => {
      const thumb = document.createElement('div');
      thumb.className = 'frame-thumb' + (i === current ? ' active' : '');
      const tCanvas = document.createElement('canvas');
      tCanvas.width = 160; tCanvas.height = 120;
      const tctx = tCanvas.getContext('2d');
      const img = new Image();
      img.onload = () => tctx.drawImage(img,0,0,160,120);
      img.src = data;
      thumb.appendChild(tCanvas);
      const tag = document.createElement('span');
      tag.className = 'tag';
      tag.textContent = (i+1);
      thumb.appendChild(tag);
      if(frames.length > 1){
        const del = document.createElement('button');
        del.className = 'del';
        del.textContent = '✕';
        del.onclick = (e) => { e.stopPropagation(); deleteFrame(i); };
        thumb.appendChild(del);
      }
      thumb.onclick = () => { goToFrame(i); };
      list.appendChild(thumb);
    });
    document.getElementById('frameCount').textContent = frames.length;
  }

  function goToFrame(i){
    saveCurrentFrame();
    current = i;
    renderCurrentToCanvas();
    renderThumbnails();
  }

  function deleteFrame(i){
    if(frames.length <= 1) return;
    frames.splice(i,1);
    if(current >= frames.length) current = frames.length - 1;
    renderCurrentToCanvas();
    renderThumbnails();
  }

  function addDuplicateFrame(){
    saveCurrentFrame();
    frames.splice(current+1, 0, frames[current]);
    current = current + 1;
    renderCurrentToCanvas();
    renderThumbnails();
  }

  function addBlankFrame(){
    saveCurrentFrame();
    frames.splice(current+1, 0, newBlankFrameData());
    current = current + 1;
    renderCurrentToCanvas();
    renderThumbnails();
  }

  function clearCurrentFrame(){
    blankPaper(ctx);
    saveCurrentFrame();
    renderThumbnails();
  }

  function getPos(e){
    const rect = canvas.getBoundingClientRect();
    const clientX = e.touches ? e.touches[0].clientX : e.clientX;
    const clientY = e.touches ? e.touches[0].clientY : e.clientY;
    return {
      x: (clientX - rect.left) * (W / rect.width),
      y: (clientY - rect.top) * (H / rect.height)
    };
  }

  function startDraw(e){
    e.preventDefault();
    drawing = true;
    const p = getPos(e);
    lastX = p.x; lastY = p.y;
    ctx.beginPath();
    ctx.arc(p.x, p.y, brushSize/2, 0, Math.PI*2);
    ctx.fillStyle = tool === 'eraser' ? '#f4efe2' : brushColor;
    ctx.fill();
  }
  function moveDraw(e){
    if(!drawing) return;
    e.preventDefault();
    const p = getPos(e);
    ctx.strokeStyle = tool === 'eraser' ? '#f4efe2' : brushColor;
    ctx.lineWidth = brushSize;
    ctx.lineCap = 'round';
    ctx.lineJoin = 'round';
    ctx.beginPath();
    ctx.moveTo(lastX, lastY);
    ctx.lineTo(p.x, p.y);
    ctx.stroke();
    lastX = p.x; lastY = p.y;
  }
  function endDraw(){
    if(!drawing) return;
    drawing = false;
    saveCurrentFrame();
    renderThumbnails();
  }

  function bindSwatches(){
    const colors = ['#2a2620','#ffffff','#ff5d5d','#ffb238','#4caf78','#3e7fff','#9b59ff','#ff7ab8'];
    const wrap = document.getElementById('swatches');
    colors.forEach(c => {
      const sw = document.createElement('div');
      sw.className = 'swatch';
      sw.style.background = c;
      sw.onclick = () => {
        brushColor = c;
        document.getElementById('colorPicker').value = c;
        setTool('pencil');
      };
      wrap.appendChild(sw);
    });
  }

  function setTool(t){
    tool = t;
    document.getElementById('toolPencil').classList.toggle('active', t==='pencil');
    document.getElementById('toolEraser').classList.toggle('active', t==='eraser');
  }

  function togglePlay(){
    playing = !playing;
    const btn = document.getElementById('playBtn');
    if(playing){
      btn.textContent = '⏸';
      saveCurrentFrame();
      playTimer = setInterval(() => {
        current = (current + 1) % frames.length;
        renderThumbnails();
        // during playback, skip onion skin for clean preview
        const wasOnion = onion;
        onion = false;
        renderCurrentToCanvas();
        onion = wasOnion;
      }, 1000 / fps);
    } else {
      btn.textContent = '▶';
      clearInterval(playTimer);
      renderCurrentToCanvas();
    }
  }

  function bindEvents(){
    canvas.addEventListener('mousedown', startDraw);
    canvas.addEventListener('mousemove', moveDraw);
    window.addEventListener('mouseup', endDraw);
    canvas.addEventListener('touchstart', startDraw, {passive:false});
    canvas.addEventListener('touchmove', moveDraw, {passive:false});
    canvas.addEventListener('touchend', endDraw);

    document.getElementById('toolPencil').onclick = () => setTool('pencil');
    document.getElementById('toolEraser').onclick = () => setTool('eraser');
    document.getElementById('toolFill').onclick = clearCurrentFrame;

    document.getElementById('sizeRange').oninput = (e) => {
      brushSize = parseInt(e.target.value);
      document.getElementById('sizeVal').textContent = brushSize;
    };
    document.getElementById('colorPicker').oninput = (e) => {
      brushColor = e.target.value;
      setTool('pencil');
    };
    document.getElementById('onionToggle').onchange = (e) => {
      onion = e.target.checked;
      renderCurrentToCanvas();
    };

    document.getElementById('addFrameBtn').onclick = addDuplicateFrame;
    document.getElementById('addBlankBtn').onclick = addBlankFrame;

    document.getElementById('prevFrame').onclick = () => {
      if(playing) togglePlay();
      if(current > 0) goToFrame(current - 1);
    };
    document.getElementById('nextFrame').onclick = () => {
      if(playing) togglePlay();
      if(current < frames.length - 1) goToFrame(current + 1);
      else addDuplicateFrame();
    };
    document.getElementById('playBtn').onclick = togglePlay;

    document.getElementById('fpsRange').oninput = (e) => {
      fps = parseInt(e.target.value);
      document.getElementById('fpsReadout').textContent = fps + ' fps';
      if(playing){ clearInterval(playTimer); togglePlay(); togglePlay(); }
    };
  }

  init();
})();
</script>

</body>
</html>
