<!doctype html><html><head><meta charset=utf8><meta name=viewport content="width=device-width,initial-scale=1,viewport-fit=cover"><style>:root{color-scheme:light;box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}html{scroll-padding-top:env(safe-area-inset-top,0px)}body{margin:0;padding:0;font:14px -apple-system,BlinkMacSystemFont,sans-serif;background:#fff;color:#000}img{max-width:100%}[hidden]:not([hidden=until-found i]){display:none!important}</style></head><body>
<title>Thiệp 20/10</title>
<meta name="claude:viewport-fit-sides" content="cover">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Be+Vietnam+Pro:wght@400;500;600&family=Dancing+Script:wght@600;700&family=Lora:ital,wght@0,400;0,500;1,400&display=swap">
<style>
/* Layout: one narrow column. Title, then an envelope; the card slides out of the envelope upward and stays tucked in its mouth. A quiet edit panel sits below. */
:root {
  --bg: #fcf0f1;
  --bg-glow: #f8d6df;
  --ink: #4b1d30;
  --muted: #855566;
  --accent: #b8305c;
  --gold-soft: #e3c78f;
  --paper: #fffaf7;
  --line: #ecc9d3;
  --env-back: #c46f89;
  --env-front: #f0b8c8;
  --env-front-2: #e7a2b6;
  --flap: #f6c8d5;
  --flap-2: #eeb0c3;
  --env-ink: #6b2540;
  --seal: #b8305c;
  --seal-ink: #fff4f6;
  --cta: #b8305c;
  --cta-ink: #fff7f9;
  --shadow: rgba(120, 30, 65, .3);
  --f1: #e48aa5;
  --f2: #f6b9ca;
  --f3: #e2ad55;
  --font-display: 'Dancing Script', 'Segoe Script', cursive;
  --font-body: 'Lora', Georgia, serif;
  --font-ui: 'Be Vietnam Pro', system-ui, -apple-system, 'Segoe UI', sans-serif;
}
@media (prefers-color-scheme: dark) {
  :root:not([data-theme="light"]) {
    --bg: #24101b; --bg-glow: #3b1a2c; --ink: #fde8ee; --muted: #cfa3b2; --accent: #ff86a8;
    --gold-soft: #7a5a2e; --paper: #3a1b2c; --line: #5c2c43;
    --env-back: #4e1d33; --env-front: #8a3d5b; --env-front-2: #74304a; --flap: #a24b6b; --flap-2: #8a3d5b;
    --env-ink: #ffe3ea; --seal: #e0577d; --seal-ink: #ffffff; --cta: #ff86a8; --cta-ink: #3a0f20;
    --shadow: rgba(0, 0, 0, .55); --f1: #e0678c; --f2: #f197b1; --f3: #f0c777;
    color-scheme: dark;
  }
}
:root[data-theme="dark"] {
  --bg: #24101b; --bg-glow: #3b1a2c; --ink: #fde8ee; --muted: #cfa3b2; --accent: #ff86a8;
  --gold-soft: #7a5a2e; --paper: #3a1b2c; --line: #5c2c43;
  --env-back: #4e1d33; --env-front: #8a3d5b; --env-front-2: #74304a; --flap: #a24b6b; --flap-2: #8a3d5b;
  --env-ink: #ffe3ea; --seal: #e0577d; --seal-ink: #ffffff; --cta: #ff86a8; --cta-ink: #3a0f20;
  --shadow: rgba(0, 0, 0, .55); --f1: #e0678c; --f2: #f197b1; --f3: #f0c777;
  color-scheme: dark;
}

* { box-sizing: border-box; }
body {
  background: radial-gradient(900px 520px at 50% -8%, var(--bg-glow), transparent 70%), var(--bg);
  color: var(--ink);
  font-family: var(--font-ui);
  min-height: 100svh;
  padding-block: 22px 56px;
  padding-left: max(16px, env(safe-area-inset-left, 0px));
  padding-right: max(16px, env(safe-area-inset-right, 0px));
}
.page { width: 100%; max-width: 440px; margin: 0 auto; }

.toprow { display: flex; align-items: center; justify-content: space-between; gap: 10px 14px; flex-wrap: wrap; }
.eyebrow { margin: 0; font-size: 11px; font-weight: 500; letter-spacing: .14em; text-transform: uppercase; color: var(--muted); }
h1 {
  font-family: var(--font-display); font-weight: 700;
  font-size: clamp(38px, 11vw, 50px); line-height: 1.05;
  margin: 10px 0 30px; text-wrap: balance;
}
.chip {
  font: 500 12px var(--font-ui); display: inline-flex; align-items: center; gap: 7px;
  padding: 7px 12px; border: 1px solid var(--line); border-radius: 99px;
  background: transparent; color: var(--ink); cursor: pointer;
}
.chip[aria-pressed="true"] { border-color: var(--accent); color: var(--accent); }
button:focus-visible, summary:focus-visible, input:focus-visible, select:focus-visible, textarea:focus-visible, .env:focus-visible {
  outline: 2px solid var(--accent); outline-offset: 3px;
}

/* ---------- stage ---------- */
.stage {
  --w: min(calc(100vw - 40px), 420px);
  --he: calc(var(--w) * .64);
  --ov: calc(var(--he) * .32);
  width: var(--w); margin: 0 auto; position: relative; isolation: isolate;
}
.slot { position: relative; height: 0; transition: height .8s cubic-bezier(.5, 0, .3, 1); }
.stage.open .slot { transition: height 1.1s cubic-bezier(.2, .85, .25, 1) .45s; }

.card {
  position: absolute; left: 4%; width: 92%; bottom: calc(var(--ov) * -1); z-index: 2;
  background: var(--paper); color: var(--ink);
  box-shadow: 0 22px 40px -22px var(--shadow), inset 0 0 0 7px var(--paper), inset 0 0 0 8px var(--gold-soft);
  transform-origin: 50% 100%;
  transform: translateY(calc(var(--he) * .68 - 22px)) scale(.3);
  visibility: hidden;
  transition: transform .8s cubic-bezier(.5, 0, .3, 1), visibility 0s linear .8s;
}
.stage.open .card {
  transform: none; visibility: visible;
  transition: transform 1.1s cubic-bezier(.2, .85, .25, 1) .45s, visibility 0s;
}
.card-inner { padding: 30px 24px calc(var(--ov) + 18px); }
.head { display: flex; justify-content: space-between; align-items: flex-start; gap: 12px; }
.kicker { margin: 4px 0 0; font-size: 10.5px; font-weight: 500; letter-spacing: .16em; text-transform: uppercase; color: var(--muted); line-height: 1.7; max-width: 15ch; }
.blooms { position: relative; width: 108px; height: 66px; flex: none; }
.blooms svg { position: absolute; transform: scale(0) rotate(-50deg); }
.blooms svg:nth-child(1) { width: 50px; height: 50px; left: 0; top: 14px; }
.blooms svg:nth-child(2) { width: 66px; height: 66px; left: 30px; top: 0; }
.blooms svg:nth-child(3) { width: 44px; height: 44px; left: 66px; top: 22px; }
.stage.shown .blooms svg { animation: bloomIn 1s cubic-bezier(.2, 1.2, .4, 1) forwards; }
.stage.shown .blooms svg:nth-child(2) { animation-delay: .15s; }
.stage.shown .blooms svg:nth-child(3) { animation-delay: .3s; }
.card.pop .blooms { animation: pop .8s ease; }
@keyframes bloomIn { to { transform: scale(1) rotate(0); } }
@keyframes pop { 0%, 100% { transform: scale(1); } 40% { transform: scale(1.22) rotate(6deg); } }

.greet {
  font-family: var(--font-display); font-weight: 700; font-size: 36px; line-height: 1.1;
  margin: 18px 0 10px; opacity: 0; transform: translateY(6px);
  transition: opacity .7s, transform .7s; overflow-wrap: anywhere;
}
.stage.shown .greet { opacity: 1; transform: none; }
.msg { font-family: var(--font-body); font-size: 16.5px; line-height: 1.75; margin: 0; white-space: pre-wrap; overflow-wrap: anywhere; }
.ch { opacity: 0; }
.ch.on { opacity: 1; transition: opacity .15s; }
.ch.cur { box-shadow: 2px 0 0 var(--accent); }
.sr { position: absolute; width: 1px; height: 1px; overflow: hidden; clip-path: inset(50%); white-space: nowrap; }
.sign { font-family: var(--font-display); font-weight: 600; font-size: 28px; text-align: right; margin: 10px 0 0; min-height: 1em; opacity: 0; transition: opacity .7s; overflow-wrap: anywhere; }
.sign.on { opacity: 1; }
.surprise { margin-top: 16px; display: flex; flex-direction: column; align-items: center; gap: 12px; }
.cta {
  font: 600 14px var(--font-ui); padding: 13px 24px; border: 0; border-radius: 99px;
  background: var(--cta); color: var(--cta-ink); cursor: pointer;
  opacity: 0; pointer-events: none; transform: translateY(6px);
  transition: opacity .5s, transform .5s, filter .2s;
}
.cta.on { opacity: 1; pointer-events: auto; transform: none; }
.cta.on:hover { filter: brightness(1.08); }
.cta.on:active { transform: scale(.97); }
.ps { font-family: var(--font-body); font-style: italic; font-size: 15px; color: var(--muted); margin: 0; min-height: 1.6em; text-align: center; opacity: 0; transition: opacity .8s .3s; }
.ps.on { opacity: 1; }

/* ---------- envelope ---------- */
.env { position: relative; height: var(--he); cursor: pointer; -webkit-tap-highlight-color: transparent; }
.stage.open .env { cursor: default; }
.env > * { position: absolute; }
.env-back { inset: 0; z-index: 1; background: var(--env-back); box-shadow: 0 22px 34px -18px var(--shadow); }
.env-front {
  inset: 0; z-index: 3;
  background: linear-gradient(165deg, var(--env-front), var(--env-front-2));
  clip-path: polygon(0 0, 50% 50%, 100% 0, 100% 100%, 0 100%);
}
.flap {
  left: 0; right: 0; top: 0; height: calc(var(--he) * .56); z-index: 4;
  transform-origin: 50% 0; transform-style: preserve-3d;
  transform: perspective(900px) rotateX(0deg);
  transition: transform .7s cubic-bezier(.4, 0, .2, 1) .55s, z-index 0s .9s;
}
.stage.open .flap { transform: perspective(900px) rotateX(180deg); z-index: 0; transition: transform .7s cubic-bezier(.4, 0, .2, 1), z-index 0s .35s; }
.ff, .fb { position: absolute; inset: 0; clip-path: polygon(0 0, 100% 0, 50% 100%); backface-visibility: hidden; -webkit-backface-visibility: hidden; }
.ff { background: linear-gradient(180deg, var(--flap), var(--flap-2)); }
.fb { background: var(--env-back); transform: rotateY(180deg); }
.to {
  left: 0; right: 0; bottom: calc(var(--he) * .12); z-index: 3; padding: 0 22%;
  text-align: center; font-family: var(--font-display); font-weight: 700;
  font-size: calc(var(--w) * .062); color: var(--env-ink); white-space: nowrap; overflow: hidden; text-overflow: ellipsis;
}
.stamp {
  right: 6%; bottom: 8%; z-index: 3; width: calc(var(--w) * .1); aspect-ratio: 4 / 5;
  background: var(--paper); outline: 2px dashed var(--env-ink); outline-offset: -4px;
  display: grid; place-items: center; align-content: center; gap: 2px; padding: 4px;
  color: var(--env-ink); font: 600 calc(var(--w) * .026) / 1 var(--font-ui);
}
.stamp svg { width: 62%; height: auto; }
.seal {
  left: 50%; top: calc(var(--he) * .56); z-index: 5; width: calc(var(--w) * .15); aspect-ratio: 1; border-radius: 50%;
  background: var(--seal); color: var(--seal-ink); display: grid; place-items: center;
  font-family: var(--font-display); font-weight: 700; font-size: calc(var(--w) * .046);
  box-shadow: 0 4px 10px var(--shadow), inset 0 0 0 3px rgba(255, 255, 255, .18);
  transform: translate(-50%, -50%); animation: seal 2.8s ease-in-out infinite;
  transition: opacity .3s;
}
.stage.open .seal { opacity: 0; pointer-events: none; }
@keyframes seal { 0%, 100% { transform: translate(-50%, -50%) scale(1); } 50% { transform: translate(-50%, -50%) scale(1.08); } }
.hint { margin: 16px 0 0; text-align: center; font-size: 13px; color: var(--muted); transition: opacity .4s; animation: bob 2.4s ease-in-out infinite; }
.hint.gone { opacity: 0; animation: none; }
@keyframes bob { 0%, 100% { transform: translateY(0); } 50% { transform: translateY(3px); } }

/* ---------- edit panel ---------- */
.tune { margin-top: 36px; border-top: 1px solid var(--line); padding-top: 16px; }
.tune summary { cursor: pointer; font: 500 14px var(--font-ui); display: flex; align-items: center; gap: 10px; list-style: none; }
.tune summary::-webkit-details-marker { display: none; }
.tune summary::before { content: ""; width: 7px; height: 7px; border-right: 2px solid var(--accent); border-bottom: 2px solid var(--accent); transform: rotate(-45deg); transition: transform .2s; }
.tune[open] summary::before { transform: rotate(45deg); }
.tune-body { display: grid; gap: 14px; margin-top: 18px; }
.tune label { display: grid; gap: 6px; font: 500 12px var(--font-ui); letter-spacing: .04em; color: var(--muted); min-width: 0; }
.tune input, .tune select, .tune textarea {
  font: 400 15px/1.5 var(--font-ui); padding: 10px 12px; border: 1px solid var(--line); border-radius: 8px;
  background: var(--paper); color: var(--ink); width: 100%; min-width: 0;
}
.tune textarea { resize: vertical; }
.row { display: flex; gap: 10px; flex-wrap: wrap; }
.btn { font: 600 13px var(--font-ui); padding: 11px 18px; border-radius: 99px; border: 1px solid var(--accent); cursor: pointer; background: var(--cta); color: var(--cta-ink); }
.btn.ghost { background: transparent; color: var(--accent); }
.status { margin: 0; min-height: 1.4em; font-size: 13px; color: var(--accent); }
.note { margin: 0; font-size: 12.5px; line-height: 1.6; color: var(--muted); }
html.view .tune { display: none; }
.linkbox { font-size: 13px !important; }
.foot { margin: 28px 0 0; font-size: 12px; line-height: 1.7; color: var(--muted); }

#fx { position: fixed; inset: 0; width: 100%; height: 100%; pointer-events: none; z-index: 20; }

@media (prefers-reduced-motion: reduce) {
  *, *::before, *::after { transition-duration: .01ms !important; transition-delay: 0s !important; animation-duration: .01ms !important; animation-delay: 0s !important; animation-iteration-count: 1 !important; }
}
</style>

<svg width="0" height="0" style="position:absolute" aria-hidden="true" focusable="false">
  <defs>
    <symbol id="bloom" viewBox="-50 -50 100 100">
      <g style="fill:var(--f1)">
        <ellipse cx="0" cy="-26" rx="15" ry="24"/>
        <ellipse cx="0" cy="-26" rx="15" ry="24" transform="rotate(60)"/>
        <ellipse cx="0" cy="-26" rx="15" ry="24" transform="rotate(120)"/>
        <ellipse cx="0" cy="-26" rx="15" ry="24" transform="rotate(180)"/>
        <ellipse cx="0" cy="-26" rx="15" ry="24" transform="rotate(240)"/>
        <ellipse cx="0" cy="-26" rx="15" ry="24" transform="rotate(300)"/>
      </g>
      <g style="fill:var(--f2)">
        <ellipse cx="0" cy="-15" rx="10" ry="17" transform="rotate(30)"/>
        <ellipse cx="0" cy="-15" rx="10" ry="17" transform="rotate(90)"/>
        <ellipse cx="0" cy="-15" rx="10" ry="17" transform="rotate(150)"/>
        <ellipse cx="0" cy="-15" rx="10" ry="17" transform="rotate(210)"/>
        <ellipse cx="0" cy="-15" rx="10" ry="17" transform="rotate(270)"/>
        <ellipse cx="0" cy="-15" rx="10" ry="17" transform="rotate(330)"/>
      </g>
      <circle r="8" style="fill:var(--f3)"/>
    </symbol>
  </defs>
</svg>

<canvas id="fx" aria-hidden="true"></canvas>

<main class="page">
  <div class="toprow">
    <p class="eyebrow">20 tháng 10 · Ngày Phụ nữ Việt Nam</p>
    <button class="chip" id="musicBtn" type="button" aria-pressed="false">
      <svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true"><path d="M9 18V6l11-2v12"/><circle cx="6.5" cy="18" r="2.5"/><circle cx="17.5" cy="16" r="2.5"/></svg>
      <span id="musicLabel">Bật nhạc</span>
    </button>
  </div>
  <h1>Một lá thư nhỏ gửi bạn</h1>

  <section class="stage" id="stage" aria-label="Thiệp 20/10">
    <div class="slot" id="slot">
      <article class="card" id="card">
        <div class="card-inner">
          <div class="head">
            <p class="kicker">Chúc mừng ngày Phụ nữ Việt Nam</p>
            <div class="blooms" aria-hidden="true">
              <svg viewBox="-50 -50 100 100"><use href="#bloom"/></svg>
              <svg viewBox="-50 -50 100 100"><use href="#bloom"/></svg>
              <svg viewBox="-50 -50 100 100"><use href="#bloom"/></svg>
            </div>
          </div>
          <h2 class="greet" id="greet">Gửi bạn,</h2>
          <div class="msg" id="msg"><span class="sr" id="msgSr"></span><span id="msgVis" aria-hidden="true"></span></div>
          <p class="sign" id="sign"></p>
          <div class="surprise">
            <button class="cta" id="cta" type="button">Bấm vào đây nhé</button>
            <p class="ps" id="ps"></p>
          </div>
        </div>
      </article>
    </div>

    <div class="env" id="env" role="button" tabindex="0" aria-expanded="false" aria-label="Mở phong bì">
      <div class="env-back"></div>
      <div class="flap"><div class="ff"></div><div class="fb"></div></div>
      <div class="env-front"></div>
      <div class="to">Dành cho <span id="toLabel"></span></div>
      <div class="stamp" aria-hidden="true">
        <svg viewBox="-50 -50 100 100"><use href="#bloom"/></svg>
        <span>20·10</span>
      </div>
      <div class="seal" aria-hidden="true">20·10</div>
    </div>
    <p class="hint" id="hint">Chạm vào phong bì để mở</p>
  </section>

  <details class="tune" id="tune">
    <summary>Chỉnh tên và lời chúc</summary>
    <div class="tune-body">
      <label for="who">Gửi cho
        <select id="who">
          <option value="friend">Bạn bè, chị em</option>
          <option value="mom">Mẹ</option>
          <option value="teacher">Cô giáo, giảng viên</option>
          <option value="love">Người yêu</option>
          <option value="work">Đồng nghiệp</option>
        </select>
      </label>
      <label for="to">Tên người nhận
        <input id="to" type="text" autocomplete="off" maxlength="40">
      </label>
      <label for="from">Tên người gửi
        <input id="from" type="text" autocomplete="off" maxlength="40" placeholder="Có thể để trống">
      </label>
      <label for="text">Lời chúc
        <textarea id="text" rows="6" maxlength="600"></textarea>
      </label>
      <div class="row">
        <button class="btn" id="replay" type="button">Xem lại thiệp</button>
        <button class="btn ghost" id="copy" type="button">Sao chép lời chúc</button>
      </div>
      <div class="row">
        <button class="btn" id="makeLink" type="button">Tạo thiệp để gửi</button>
        <button class="btn ghost" id="preview" type="button" hidden>Xem thử như người nhận</button>
      </div>
      <input class="linkbox" id="linkOut" type="text" readonly hidden aria-label="Link thiệp">
      <p class="status" id="status" aria-live="polite"></p>
      <p class="note">Chỉnh xong, bấm “Tạo thiệp để gửi”: bạn sẽ có một đường link chứa sẵn tên và lời chúc của bạn. Người nhận mở link sẽ chỉ thấy phong bì và thiệp, không có phần chỉnh sửa.</p>
    </div>
  </details>

  <p class="foot">20/10 là ngày kỷ niệm thành lập Hội Liên hiệp Phụ nữ Việt Nam, năm 1930.</p>
</main>

<script>
(function () {
  var $ = function (s) { return document.querySelector(s); };
  var reduce = window.matchMedia('(prefers-reduced-motion: reduce)').matches;

  var PRESETS = {
    friend: {
      to: 'bạn thân mến',
      text: 'Chúc bạn một ngày 20/10 thật rực rỡ! Cảm ơn bạn vì luôn là người nghe mình kể chuyện, cười cùng mình và kéo mình dậy mỗi lần mệt. Mong bạn luôn xinh, luôn vui và làm được hết những điều bạn muốn.',
      ps: 'P/S: Cà phê tuần này để mình mời.'
    },
    mom: {
      to: 'mẹ yêu',
      text: 'Mẹ ơi, cảm ơn mẹ đã lặng lẽ lo cho con từng bữa cơm, từng giấc ngủ, từng lần con vấp ngã. Nhân ngày 20/10, con chúc mẹ luôn khỏe mạnh, thật nhiều niềm vui và nụ cười không bao giờ phai. Con thương mẹ nhiều lắm.',
      ps: 'P/S: Mẹ nhớ ăn cơm đúng bữa nhé.'
    },
    teacher: {
      to: 'cô',
      text: 'Em cảm ơn cô đã kiên nhẫn dạy chúng em, không chỉ kiến thức mà cả cách sống tử tế. Nhân ngày 20/10, em kính chúc cô luôn mạnh khỏe, hạnh phúc và giữ mãi ngọn lửa với nghề.',
      ps: 'P/S: Cả lớp thương cô nhiều lắm.'
    },
    love: {
      to: 'người thương',
      text: 'Cảm ơn người đã đến bên mình và làm cho những ngày bình thường trở nên đáng nhớ. Nhân ngày 20/10, chúc người mình thương luôn rạng rỡ, luôn được yêu thương và luôn được là chính mình.',
      ps: 'P/S: Tối nay mình đi ăn món bạn thích nhé.'
    },
    work: {
      to: 'đồng nghiệp quý mến',
      text: 'Nhân ngày 20/10, chúc bạn luôn khỏe, luôn vui và gặp thật nhiều thuận lợi trong công việc lẫn cuộc sống. Cảm ơn bạn vì đã là một đồng nghiệp đáng quý của cả nhóm.',
      ps: 'P/S: Trà sữa chiều nay tính vào phần mình.'
    }
  };

  var stage = $('#stage'), slot = $('#slot'), card = $('#card'), env = $('#env'), hint = $('#hint');
  var greetEl = $('#greet'), msgVis = $('#msgVis'), msgSr = $('#msgSr'), signEl = $('#sign');
  var cta = $('#cta'), psEl = $('#ps'), toLabel = $('#toLabel');
  var who = $('#who'), toIn = $('#to'), fromIn = $('#from'), textIn = $('#text'), statusEl = $('#status');
  var musicBtn = $('#musicBtn'), musicLabel = $('#musicLabel');

  var opened = false, timers = [], typing = null, skip = null, chars = [], musicPref = null;

  function after(ms, fn) { var t = setTimeout(fn, ms); timers.push(t); return t; }
  function clearTimers() {
    timers.forEach(clearTimeout); timers = [];
    if (typing) { clearInterval(typing); typing = null; }
    skip = null;
  }

  /* ---------- falling petals and burst ---------- */
  var fx = (function () {
    var cv = $('#fx'), g = cv.getContext('2d');
    var W = 0, H = 0, petals = [], bits = [], target = reduce ? 0 : 8, rainUntil = 0, last = 0, running = false;
    var COLORS = ['#e0577d', '#ee7f9f', '#f7a6bc', '#ffc7d4', '#e9b765'];
    function size() {
      var dpr = Math.min(window.devicePixelRatio || 1, 2);
      W = window.innerWidth; H = window.innerHeight;
      cv.width = W * dpr; cv.height = H * dpr;
      g.setTransform(dpr, 0, 0, dpr, 0, 0);
    }
    function pick() { return COLORS[(Math.random() * COLORS.length) | 0]; }
    function spawn(initial) {
      petals.push({
        x: Math.random() * W, y: initial ? Math.random() * H : -20, s: 7 + Math.random() * 9,
        vy: 30 + Math.random() * 36, sw: 18 + Math.random() * 30, ph: Math.random() * 6.28, sp: .6 + Math.random(),
        rot: Math.random() * 6.28, vr: (Math.random() - .5) * 1.6, fl: Math.random() * 6.28, vf: 1 + Math.random() * 2,
        c: pick(), a: .55 + Math.random() * .4
      });
    }
    function petal(x, y, s, rot, fl, c, a) {
      g.save(); g.translate(x, y); g.rotate(rot);
      g.scale(.25 + .75 * Math.abs(Math.cos(fl)), 1);
      g.globalAlpha = a; g.fillStyle = c; g.beginPath();
      g.moveTo(0, -s);
      g.bezierCurveTo(s * .95, -s * .55, s * .8, s * .65, 0, s);
      g.bezierCurveTo(-s * .8, s * .65, -s * .95, -s * .55, 0, -s);
      g.fill(); g.restore();
    }
    function frame(t) {
      var dt = Math.min(.05, (t - last) / 1000 || .016); last = t;
      g.clearRect(0, 0, W, H);
      var tgt = rainUntil > performance.now() ? 70 : target;
      if (petals.length < tgt && Math.random() < dt * tgt * .4) spawn(false);
      for (var i = petals.length - 1; i >= 0; i--) {
        var p = petals[i];
        p.y += p.vy * dt; p.ph += p.sp * dt; p.x += Math.sin(p.ph) * p.sw * dt;
        p.rot += p.vr * dt; p.fl += p.vf * dt;
        if (p.y > H + 24 || petals.length > tgt + 12) { petals.splice(i, 1); continue; }
        petal(p.x, p.y, p.s, p.rot, p.fl, p.c, p.a);
      }
      for (var j = bits.length - 1; j >= 0; j--) {
        var b = bits[j];
        b.life -= dt;
        if (b.life <= 0) { bits.splice(j, 1); continue; }
        b.vx *= 1 - 1.1 * dt; b.vy += 430 * dt;
        b.x += b.vx * dt; b.y += b.vy * dt; b.rot += b.vr * dt; b.fl += b.vf * dt;
        var al = Math.min(1, b.life / .7);
        if (b.spark) { g.globalAlpha = al; g.fillStyle = '#f0c777'; g.beginPath(); g.arc(b.x, b.y, 2.4, 0, 6.28); g.fill(); }
        else petal(b.x, b.y, b.s, b.rot, b.fl, b.c, al);
      }
      g.globalAlpha = 1;
      requestAnimationFrame(frame);
    }
    function start() { if (running || reduce) return; running = true; size(); for (var i = 0; i < 6; i++) spawn(true); requestAnimationFrame(frame); }
    window.addEventListener('resize', function () { if (running) size(); });
    return {
      start: start,
      density: function (n) { target = reduce ? 0 : n; },
      rain: function (ms) { rainUntil = performance.now() + ms; },
      burst: function (x, y) {
        if (reduce) return;
        for (var i = 0; i < 64; i++) {
          var a = -Math.PI / 2 + (Math.random() - .5) * Math.PI * 1.25, sp = 220 + Math.random() * 420;
          bits.push({
            x: x, y: y, vx: Math.cos(a) * sp, vy: Math.sin(a) * sp, s: 5 + Math.random() * 8,
            rot: Math.random() * 6.28, vr: (Math.random() - .5) * 6, fl: Math.random() * 6.28, vf: 2 + Math.random() * 4,
            c: pick(), life: 2.2 + Math.random() * 1.2, spark: Math.random() < .25
          });
        }
      }
    };
  })();

  /* ---------- music box (generated in the browser) ---------- */
  var music = (function () {
    var ac = null, master = null, echo = null, playing = false, timer = null, ei = 0, base = 0, t0 = 0;
    var BEAT = 60 / 76;
    var MEL = [[76,1],[79,1],[81,1.5],[79,.5],[76,1],[74,1],[72,2],[74,1],[76,1],[79,1.5],[76,.5],[74,1],[72,1],[69,2],
               [69,1],[72,1],[74,1.5],[76,.5],[79,1],[76,1],[74,2],[76,1],[74,1],[72,1.5],[69,.5],[67,1],[69,1],[72,2]];
    var BASS = [48, 45, 41, 43, 45, 41, 48, 43];
    var EV = [], b = 0, LOOP;
    MEL.forEach(function (n) { EV.push({ b: b, m: n[0], v: .5, l: 1.7 }); b += n[1]; });
    LOOP = b;
    BASS.forEach(function (r, i) {
      var s = i * 4;
      EV.push({ b: s, m: r, v: .45, l: 3 }, { b: s + 1.5, m: r + 12, v: .2, l: 1.6 }, { b: s + 2.5, m: r + 19, v: .18, l: 1.6 });
    });
    EV.sort(function (x, y) { return x.b - y.b; });

    function init() {
      var AC = window.AudioContext || window.webkitAudioContext;
      if (!AC) return false;
      ac = new AC();
      master = ac.createGain(); master.gain.value = 0; master.connect(ac.destination);
      echo = ac.createDelay(1); echo.delayTime.value = .33;
      var fb = ac.createGain(); fb.gain.value = .32;
      var wet = ac.createGain(); wet.gain.value = .35;
      echo.connect(fb); fb.connect(echo); echo.connect(wet); wet.connect(master);
      return true;
    }
    function note(m, t, v, len) {
      var f = 440 * Math.pow(2, (m - 69) / 12);
      var o1 = ac.createOscillator(), o2 = ac.createOscillator(), g = ac.createGain(), g2 = ac.createGain();
      o1.type = 'sine'; o2.type = 'triangle'; o1.frequency.value = f; o2.frequency.value = f * 2; g2.gain.value = .12;
      o1.connect(g); o2.connect(g2); g2.connect(g);
      g.gain.setValueAtTime(.0001, t);
      g.gain.linearRampToValueAtTime(v, t + .012);
      g.gain.exponentialRampToValueAtTime(.0005, t + len);
      g.connect(master); g.connect(echo);
      o1.start(t); o2.start(t); o1.stop(t + len + .05); o2.stop(t + len + .05);
    }
    function pump() {
      var horizon = ac.currentTime + .8;
      while (true) {
        var e = EV[ei], t = t0 + (base + e.b) * BEAT;
        if (t > horizon) break;
        if (t >= ac.currentTime - .05) note(e.m, t, e.v, e.l * BEAT);
        ei++;
        if (ei >= EV.length) { ei = 0; base += LOOP; }
      }
      timer = setTimeout(pump, 200);
    }
    return {
      get on() { return playing; },
      start: function () {
        try {
          if (!ac && !init()) return;
          if (ac.resume) ac.resume();
          if (playing) return;
          playing = true; ei = 0; base = 0; t0 = ac.currentTime + .1;
          master.gain.cancelScheduledValues(ac.currentTime);
          master.gain.setTargetAtTime(.2, ac.currentTime, .3);
          pump();
        } catch (e) { playing = false; }
      },
      stop: function () {
        if (!playing) return;
        playing = false; clearTimeout(timer);
        try { master.gain.setTargetAtTime(0, ac.currentTime, .12); } catch (e) {}
      }
    };
  })();

  function syncMusic() {
    musicBtn.setAttribute('aria-pressed', music.on ? 'true' : 'false');
    musicLabel.textContent = music.on ? 'Tắt nhạc' : 'Bật nhạc';
  }
  musicBtn.addEventListener('click', function () {
    if (music.on) { music.stop(); musicPref = false; } else { music.start(); musicPref = true; }
    syncMusic();
  });

  /* ---------- card content ---------- */
  function buildMsg(text) {
    text = text.normalize('NFC');
    msgSr.textContent = text; msgVis.textContent = '';
    var frag = document.createDocumentFragment();
    Array.from(text).forEach(function (c) {
      if (c === '\n') { frag.appendChild(document.createElement('br')); return; }
      var s = document.createElement('span'); s.className = 'ch'; s.textContent = c; frag.appendChild(s);
    });
    msgVis.appendChild(frag);
    chars = Array.prototype.slice.call(msgVis.querySelectorAll('.ch'));
  }
  function names() {
    var p = PRESETS[who.value];
    var name = toIn.value.trim() || p.to, from = fromIn.value.trim();
    greetEl.textContent = 'Gửi ' + name + ',';
    toLabel.textContent = name;
    signEl.textContent = from ? '— ' + from : '';
    psEl.textContent = p.ps;
  }
  function personalise() {
    names();
    buildMsg(textIn.value.trim() || PRESETS[who.value].text);
  }

  function setSlot() {
    var ov = env.offsetHeight * .32;
    slot.style.height = Math.max(0, card.offsetHeight - ov) + 'px';
  }
  if (window.ResizeObserver) new ResizeObserver(function () { if (opened) setSlot(); }).observe(card);
  window.addEventListener('resize', function () { if (opened) setSlot(); });

  function typeMsg(done) {
    var n = chars.length, i = 0;
    function finish() {
      if (typing) { clearInterval(typing); typing = null; }
      chars.forEach(function (c) { c.classList.remove('cur'); c.classList.add('on'); });
      skip = null; done();
    }
    if (!n || reduce) { finish(); return; }
    skip = finish;
    var step = Math.max(14, Math.min(42, Math.round(8500 / n)));
    typing = setInterval(function () {
      if (i > 0) chars[i - 1].classList.remove('cur');
      chars[i].classList.add('on', 'cur');
      i++;
      if (i >= n) finish();
    }, step);
  }
  msgVis.addEventListener('click', function () { if (skip) skip(); });

  function open() {
    if (opened) return;
    opened = true;
    stage.classList.add('open');
    env.setAttribute('aria-expanded', 'true');
    hint.classList.add('gone');
    setSlot();
    fx.start(); fx.density(26);
    if (musicPref !== false) { music.start(); musicPref = music.on ? true : musicPref; syncMusic(); }
    after(reduce ? 0 : 1250, function () {
      stage.classList.add('shown');
      after(reduce ? 0 : 700, function () {
        typeMsg(function () {
          signEl.classList.add('on');
          after(350, function () { cta.classList.add('on'); });
        });
      });
    });
    after(reduce ? 0 : 1500, function () {
      card.scrollIntoView({ block: 'nearest', behavior: reduce ? 'auto' : 'smooth' });
    });
  }
  env.addEventListener('click', open);
  env.addEventListener('keydown', function (e) {
    if (e.key === 'Enter' || e.key === ' ') { e.preventDefault(); open(); }
  });

  cta.addEventListener('click', function () {
    var r = cta.getBoundingClientRect();
    fx.burst(r.left + r.width / 2, r.top + r.height / 2);
    fx.rain(5000);
    psEl.classList.add('on');
    cta.textContent = 'Thêm hoa nữa';
    card.classList.add('pop');
    setTimeout(function () { card.classList.remove('pop'); }, 900);
  });

  function replay() {
    clearTimers();
    var wasOpen = opened;
    opened = false;
    fx.density(8);
    stage.classList.remove('open', 'shown');
    signEl.classList.remove('on'); cta.classList.remove('on'); psEl.classList.remove('on');
    cta.textContent = 'Bấm vào đây nhé';
    slot.style.height = '0px';
    hint.classList.remove('gone');
    env.setAttribute('aria-expanded', 'false');
    personalise();
    window.scrollTo({ top: 0, behavior: reduce ? 'auto' : 'smooth' });
    after(wasOpen && !reduce ? 1400 : 100, open);
  }
  $('#replay').addEventListener('click', replay);

  /* ---------- edit panel ---------- */
  function onPreset() {
    var p = PRESETS[who.value];
    textIn.value = p.text;
    toIn.placeholder = 'Mặc định: ' + p.to;
    if (!opened) personalise(); else names();
  }
  who.addEventListener('change', onPreset);
  [toIn, fromIn].forEach(function (el) { el.addEventListener('input', names); });
  textIn.addEventListener('input', function () { if (!opened) buildMsg(textIn.value.trim() || PRESETS[who.value].text); });

  $('#copy').addEventListener('click', function () {
    var from = fromIn.value.trim();
    var out = greetEl.textContent + '\n\n' + (textIn.value.trim() || PRESETS[who.value].text) + (from ? '\n\n— ' + from : '');
    var fallback = function () {
      textIn.focus(); textIn.select();
      statusEl.textContent = 'Đã chọn phần lời chúc. Nhấn Ctrl+C (hoặc ⌘+C) để sao chép.';
    };
    try {
      navigator.clipboard.writeText(out).then(function () { statusEl.textContent = 'Đã sao chép lời chúc.'; }, fallback);
    } catch (e) { fallback(); }
  });

  function b64e(by) { var s = ''; for (var i = 0; i < by.length; i++) s += String.fromCharCode(by[i]); return btoa(s).replace(/\+/g, '-').replace(/\//g, '_').replace(/=+$/, ''); }
  function b64d(str) { str = str.replace(/-/g, '+').replace(/_/g, '/'); while (str.length % 4) str += '='; var b = atob(str), u = new Uint8Array(b.length); for (var i = 0; i < b.length; i++) u[i] = b.charCodeAt(i); return u; }
  function pipe(by, S, fmt) { var s = new S(fmt), w = s.writable.getWriter(); w.write(by); w.close(); return new Response(s.readable).arrayBuffer().then(function (b) { return new Uint8Array(b); }); }
  function pack(arr) {
    var raw = new TextEncoder().encode(JSON.stringify(arr));
    if (!window.CompressionStream) return Promise.resolve('p' + b64e(raw));
    return pipe(raw, CompressionStream, 'deflate-raw').then(function (z) { return 'z' + b64e(z); }, function () { return 'p' + b64e(raw); });
  }
  function unpack(code) {
    try {
      var by = b64d(code.slice(1));
      var get = code.charAt(0) === 'z' ? pipe(by, DecompressionStream, 'deflate-raw') : Promise.resolve(by);
      return get.then(function (u) { return JSON.parse(new TextDecoder().decode(u)); }).catch(function () { return null; });
    } catch (e) { return Promise.resolve(null); }
  }
  function linkFor() {
    var w = who.value, m = textIn.value.trim();
    return pack([w, toIn.value.trim(), fromIn.value.trim(), m === PRESETS[w].text ? '' : m]).then(function (code) {
      return location.href.split('#')[0] + '#c=' + code;
    });
  }
  var linkOut = $('#linkOut'), previewBtn = $('#preview');
  $('#makeLink').addEventListener('click', function () {
    linkFor().then(function (url) {
      linkOut.value = url; linkOut.hidden = false; previewBtn.hidden = false;
      var ok = function () { statusEl.textContent = 'Đã tạo và sao chép link thiệp. Gửi link này cho người nhận.'; };
      var no = function () { linkOut.focus(); linkOut.select(); statusEl.textContent = 'Đã tạo link. Hãy sao chép link trong ô bên dưới.'; };
      try { navigator.clipboard.writeText(url).then(ok, no); } catch (e) { no(); }
    });
  });
  previewBtn.addEventListener('click', function () { if (linkOut.value) window.open(linkOut.value, '_blank'); });
  linkOut.addEventListener('focus', function () { linkOut.select(); });

  var hm = /[#&]c=([^&]+)/.exec(location.hash);
  if (hm) document.documentElement.classList.add('view');
  textIn.value = PRESETS.friend.text;
  toIn.placeholder = 'Mặc định: ' + PRESETS.friend.to;
  personalise();
  function applyShared(a) {
    if (!a || !PRESETS[a[0]]) return;
    who.value = a[0];
    toIn.value = String(a[1] || '').slice(0, 40);
    fromIn.value = String(a[2] || '').slice(0, 40);
    textIn.value = String(a[3] || PRESETS[a[0]].text).slice(0, 600);
    personalise();
  }
  if (hm) {
    if (hm[1].charAt(0) === '%') {
      try { var o = JSON.parse(decodeURIComponent(hm[1])); applyShared([o.w, o.t, o.f, o.m]); } catch (e) {}
    } else unpack(hm[1]).then(applyShared);
  }
  syncMusic();
  fx.start();
})();
</script>

</body></html>
