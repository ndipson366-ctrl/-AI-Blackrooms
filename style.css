/* Backrooms: Level 0 — styles
   Two visual layers on purpose: a VHS camcorder (VT323) laid over a
   blocky Roblox-style game UI (Source Sans 3). */

:root {
  --ink: #0a0803;
  --paper: #f4efc8;
  --rec: #ff3b30;
  --ok: #4ade80;
  --warn: #f87171;
  --font-cam: 'VT323', 'Courier New', monospace;
  --font-ui: 'Source Sans 3', Arial, sans-serif;
  --safe-top: env(safe-area-inset-top, 0px);
  --safe-bottom: env(safe-area-inset-bottom, 0px);
  box-sizing: border-box;
  padding-top: var(--safe-top);
  padding-bottom: var(--safe-bottom);
}

html { height: 100%; scroll-padding-top: var(--safe-top); }

body {
  height: 100%;
  margin: 0;
  overflow: hidden;
  background: var(--ink);
  color: var(--paper);
  font-family: var(--font-cam);
  user-select: none;
}

/* ---------- 3D canvas + camcorder overlays ---------- */

#gl {
  position: fixed;
  inset: 0;
  width: 100%;
  height: 100%;
  filter: sepia(.28) saturate(1.35) contrast(1.12) blur(.5px);
  animation: wobble 6s infinite;
}
@keyframes wobble {
  0%, 93%, 100% { transform: none; }
  95% { transform: translateX(5px) skewX(1deg); }
  97% { transform: translateX(-4px); }
}

.ov { position: fixed; inset: 0; pointer-events: none; }
#scan { background: repeating-linear-gradient(0deg, #0000 0 2px, #0004 2px 3px); }
#vg   { background: radial-gradient(transparent 50%, #000c); }
#nz   { width: 100%; height: 100%; opacity: .11; mix-blend-mode: overlay; image-rendering: pixelated; }
#fx   { background: #fff; opacity: 0; mix-blend-mode: difference; }

#trk {
  top: -20px;
  bottom: auto;
  height: 14px;
  background: #fff2;
  filter: blur(2px);
  animation: tracking 5s linear infinite;
}
@keyframes tracking { to { transform: translateY(110vh); } }

/* ---------- camcorder HUD ---------- */

#hud {
  position: fixed;
  inset: 0;
  pointer-events: none;
  font-size: 28px;
  text-shadow: 2px 0 #f006, -2px 0 #0ff6;
}
#tl, #tr { position: absolute; top: calc(16px + var(--safe-top)); }
#tl { left: 22px; }
#tr { right: 22px; text-align: right; }
#tr b { color: var(--rec); font-weight: 400; animation: blink 1.2s steps(1) infinite; }
@keyframes blink { 50% { opacity: 0; } }

#bl { position: absolute; left: 22px; bottom: calc(18px + var(--safe-bottom)); }
.bar { width: 170px; height: 10px; margin-top: 4px; border: 2px solid var(--paper); }
.bar i { display: block; width: 100%; height: 100%; background: var(--paper); }

#map {
  position: absolute;
  right: 22px;
  bottom: calc(18px + var(--safe-bottom));
  width: 150px;
  height: 150px;
  border: 2px solid var(--paper);
  background: #0007;
}

/* ---------- game UI (chat, players, health, hotbar) ---------- */

.rb {
  position: fixed;
  z-index: 5;
  pointer-events: none;
  font: 700 14px/1.4 var(--font-ui);
  color: #fff;
  text-shadow: 0 1px 2px #000;
}
#chat {
  left: 14px;
  top: calc(100px + var(--safe-top));
  width: 310px;
  max-width: 60vw;
  padding: 6px 8px;
  border-radius: 6px;
  background: #0006;
}
#lb {
  right: 14px;
  top: calc(92px + var(--safe-top));
  width: 180px;
  padding: 6px 10px;
  border-radius: 6px;
  background: #0007;
}
#hb {
  left: 50%;
  bottom: calc(16px + var(--safe-bottom));
  display: flex;
  gap: 6px;
  transform: translateX(-50%);
}
.sl {
  width: 58px;
  height: 58px;
  padding-top: 6px;
  box-sizing: border-box;
  border: 2px solid #fff7;
  border-radius: 8px;
  background: #0008;
  font-size: 12px;
  text-align: center;
}
.sl b { display: block; font-size: 20px; }
#hpw {
  left: 50%;
  bottom: calc(86px + var(--safe-bottom));
  width: 200px;
  height: 14px;
  overflow: hidden;
  transform: translateX(-50%);
  border: 2px solid #fff;
  border-radius: 8px;
  background: #000a;
}
#hpf { width: 100%; height: 100%; background: var(--ok); }

/* ---------- title / game-over panel ---------- */

#msg {
  position: fixed;
  inset: 0;
  z-index: 10;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding: 24px;
  background: #000c;
  font-size: 26px;
  line-height: 1.35;
  text-align: center;
  cursor: pointer;
}
#msg.off { display: none; }
#msg h1 {
  margin: 0;
  font-size: clamp(46px, 10vw, 96px);
  font-weight: 400;
  letter-spacing: .06em;
  text-shadow: 3px 0 #f006, -3px 0 #0ff6;
}
#msg p { max-width: 560px; margin: 12px 0 0; }

.keys {
  display: grid;
  grid-template-columns: auto auto;
  gap: 2px 18px;
  margin: 18px 0 0;
  font-size: 22px;
  text-align: left;
}
.keys dt { color: var(--paper); text-align: right; }
.keys dd { margin: 0; opacity: .75; }
.start { margin-top: 22px; color: var(--rec); animation: blink 1.2s steps(1) infinite; }

/* ---------- accessibility ---------- */

@media (prefers-reduced-motion: reduce) {
  #gl, #trk, #tr b, .start { animation: none; }
}
@media (max-width: 520px) {
  #hud { font-size: 22px; }
  #map { width: 110px; height: 110px; }
  .keys { font-size: 18px; }
}
