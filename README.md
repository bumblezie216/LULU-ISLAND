<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Lulu Island</title>
<link href="https://fonts.googleapis.com/css2?family=Pacifico&family=Nunito:wght@400;700;800&display=swap" rel="stylesheet">
<style>
:root{--bg:#fff1dc;--glow:#ffb06a;--ink:#2a0f3d;--card:#ffffff;--pink:#e8236f;--teal:#0a7f86;--muted:#6d4b7c;--line:#f0d3b4;
box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}
@media (prefers-color-scheme:dark){:root:not([data-theme="light"]){--bg:#1b0a2b;--glow:#7a1f5c;--ink:#ffe9d2;--card:#2c1244;--pink:#ff5c9b;--teal:#3fd0c9;--muted:#c9a8d6;--line:#4a2766}}
:root[data-theme="dark"]{--bg:#1b0a2b;--glow:#7a1f5c;--ink:#ffe9d2;--card:#2c1244;--pink:#ff5c9b;--teal:#3fd0c9;--muted:#c9a8d6;--line:#4a2766}
*{box-sizing:border-box}
body{margin:0;min-height:100vh;background:radial-gradient(ellipse at 50% -10%,var(--glow),transparent 60%),var(--bg);color:var(--ink);font-family:'Nunito',system-ui,sans-serif;font-size:17px;line-height:1.45}
.wrap{max-width:520px;margin:0 auto;padding:22px 18px 40px}
h1{font-family:'Pacifico',cursive;font-weight:400;font-size:clamp(2.6rem,12vw,3.6rem);margin:8px 0 4px;color:var(--pink);text-shadow:0 0 18px color-mix(in srgb,var(--pink) 45%,transparent);line-height:1.1}
h2{font-family:'Pacifico',cursive;font-weight:400;font-size:1.7rem;margin:6px 0 10px;color:var(--pink)}
.tag{margin:0 0 18px;color:var(--muted)}
.hint{font-size:.9rem;color:var(--muted);margin:6px 0 14px}
textarea{width:100%;font:inherit;padding:12px;border-radius:14px;border:2px solid var(--line);background:var(--card);color:var(--ink);resize:vertical}
textarea:focus-visible,button:focus-visible{outline:3px solid var(--teal);outline-offset:2px}
.btn{display:block;width:100%;font:inherit;font-weight:800;padding:14px;border:0;border-radius:999px;background:var(--pink);color:#fff;cursor:pointer;margin-top:10px}
.btn.alt{background:var(--teal);color:#fff}
.pick{display:grid;grid-template-columns:1fr 1fr;gap:10px}
.pick button{font:inherit;font-weight:800;padding:14px 8px;border-radius:16px;border:2px solid var(--line);background:var(--card);color:var(--ink);cursor:pointer}
.pick button:active{border-color:var(--pink);transform:scale(.97)}
.couple{display:flex;justify-content:space-between;align-items:center;gap:10px;background:var(--card);border:2px solid var(--line);border-radius:16px;padding:12px 14px;margin:8px 0}
.couple.you{border-color:var(--pink)}
.couple.danger{border-color:#d62828;background:color-mix(in srgb,#d62828 12%,var(--card))}
.couple b{font-weight:800}
.num{font-weight:800;color:var(--teal);white-space:nowrap}
.arena{position:relative;height:300px;border-radius:20px;background:var(--card);border:2px dashed var(--line);overflow:hidden;touch-action:manipulation}
.heart{position:absolute;width:60px;height:60px;border:0;background:none;font-size:42px;cursor:pointer;padding:0;line-height:1}
.hud{display:flex;justify-content:space-between;font-weight:800;margin-bottom:8px}
.err{color:#d62828;font-weight:700;min-height:1.4em}
.big{font-size:3.4rem;text-align:center;margin:12px 0}
.msg{background:var(--card);border-radius:16px;padding:14px;border-left:6px solid var(--pink);margin:10px 0}
.intro{text-align:center}
.intro h1{animation:drop 1s cubic-bezier(.2,1.4,.4,1) backwards}
@keyframes drop{from{opacity:0;transform:translateY(-30px) scale(.8)}}
.scene{display:block;width:100%;max-width:400px;margin:0 auto;border-radius:24px;overflow:hidden}
.sub{margin:14px 0 0;animation:fade 1s 1.2s backwards}
.go{animation:fade 1s 2.4s backwards}
@keyframes fade{from{opacity:0;transform:translateY(8px)}}
.sway{transform-box:fill-box;transform-origin:50% 100%;animation:sway 4s ease-in-out infinite alternate}
@keyframes sway{from{transform:rotate(-3deg)}to{transform:rotate(3deg)}}
.sun{transform-box:fill-box;transform-origin:center;animation:pulse 3s ease-in-out infinite alternate}
@keyframes pulse{to{transform:scale(1.06)}}
.wave{animation:wave 5s linear infinite}
.w2{animation-duration:3.5s;animation-direction:reverse}
@keyframes wave{to{transform:translateX(-60px)}}
.tilt{transform-box:view-box;transform-origin:180px 330px;animation:tilt 5s ease-in-out infinite alternate}
@keyframes tilt{from{transform:rotate(-3deg)}to{transform:rotate(4deg)}}
.blink{transform-box:fill-box;transform-origin:center;animation:blink 4s infinite}
@keyframes blink{0%,92%,100%{transform:scaleY(1)}95%{transform:scaleY(.08)}}
.wink{transform-box:fill-box;transform-origin:center;animation:wink 6s infinite}
@keyframes wink{0%,28%,42%,100%{transform:scaleY(1)}32%,38%{transform:scaleY(.06)}}
.winkline{opacity:0;animation:winkl 6s infinite}
@keyframes winkl{0%,29%,41%,100%{opacity:0}32%,38%{opacity:1}}
.brow{animation:brow 6s infinite}
@keyframes brow{0%,28%,42%,100%{transform:translateY(0)}32%,38%{transform:translateY(-4px)}}
.smile{animation:smilem 6s infinite}
@keyframes smilem{0%,52%,72%,100%{opacity:1}56%,68%{opacity:0}}
.kiss{opacity:0;animation:kissm 6s infinite}
@keyframes kissm{0%,52%,72%,100%{opacity:0}56%,68%{opacity:1}}
.fly{opacity:0;transform-box:fill-box;transform-origin:center;animation:fly 6s infinite}
@keyframes fly{0%,56%{opacity:0;transform:translate(0,0) scale(.4)}60%{opacity:1}82%,100%{opacity:0;transform:translate(90px,-80px) scale(1.2)}}
.bubble{transform-box:fill-box;transform-origin:20% 100%;animation:pop .6s 1.6s cubic-bezier(.2,1.6,.4,1) backwards}
@keyframes pop{from{transform:scale(0);opacity:0}}
@media (prefers-reduced-motion:reduce){.intro *{animation:none!important}}
#stage{position:fixed;inset:0;z-index:50;background:#12041f;overflow:hidden}
#sc,.sc{position:absolute;inset:0}
.sc{display:flex;flex-direction:column;align-items:center;justify-content:center;text-align:center;color:#fff;overflow:hidden}
.flash{position:absolute;inset:0;background:#fff;z-index:5;pointer-events:none;animation:fl .45s ease-out forwards}
@keyframes fl{from{opacity:.6}to{opacity:0}}
.bug{position:absolute;top:calc(env(safe-area-inset-top,0px) + 12px);left:14px;z-index:9;background:#d62828;color:#fff;font-weight:800;font-size:13px;padding:3px 9px;border-radius:6px}
.skip{position:absolute;top:calc(env(safe-area-inset-top,0px) + 10px);right:12px;z-index:9;font:inherit;font-weight:800;font-size:14px;color:#fff;background:rgba(0,0,0,.45);border:1px solid rgba(255,255,255,.5);border-radius:999px;padding:6px 14px;cursor:pointer}
.s1{background:linear-gradient(#12041f,#5b2a86 50%,#ff5c9b)}
.sunr{position:absolute;left:50%;bottom:30%;width:200px;height:200px;margin-left:-100px;border-radius:50%;background:#ffd27a;box-shadow:0 0 90px #ffb06a;animation:rise 3s ease-out both}
@keyframes rise{from{transform:translateY(240px)}}
.sea{position:absolute;left:0;right:0;bottom:0;height:32%;background:linear-gradient(#14b8b0,#0a5f86)}
.pl{position:absolute;bottom:26%;font-size:110px;line-height:1}
.cap{position:absolute;top:18%;margin:0;font-family:'Pacifico',cursive;font-size:2rem;animation:fade 1.2s .5s backwards}
.s2{background:linear-gradient(#5b2a86 50%,#0a5f86 50%)}
.zoom{width:100%;max-width:560px;animation:zoomin 6s ease-out both}
@keyframes zoomin{from{transform:scale(1.5)}}
.lt{position:absolute;left:0;bottom:10%;background:#fff;color:#2a0f3d;padding:8px 20px 8px 14px;border-radius:0 40px 40px 0;font-weight:800;font-size:1.3rem;border-left:8px solid #ff3d81;animation:slidein .5s 1s backwards}
@keyframes slidein{from{transform:translateX(-110%)}}
.ph{width:min(68vw,300px);aspect-ratio:1;border-radius:50%;background:rgba(255,255,255,.22);border:6px solid #fff;display:grid;place-items:center;font-size:min(30vw,130px);animation:bnc .55s cubic-bezier(.2,1.6,.4,1) backwards}
@keyframes bnc{from{transform:scale(0) rotate(-40deg)}}
.ph span{animation:pulse .5s ease-in-out infinite alternate}
.nm{font-family:'Pacifico',cursive;font-size:clamp(2.2rem,11vw,3.4rem);margin:22px 0 8px;text-shadow:0 4px 0 rgba(0,0,0,.25);animation:drop .5s .15s backwards}
.sb{font-weight:800;background:rgba(0,0,0,.35);padding:6px 14px;border-radius:999px;font-size:1rem;animation:fade .5s .35s backwards}
.hr{position:absolute;bottom:-40px;font-size:28px;animation:up 1.7s linear infinite}
@keyframes up{to{transform:translateY(-110vh) rotate(20deg)}}
.sl{font-size:clamp(2.6rem,15vw,4.5rem);font-weight:800;line-height:1.1;padding:0 16px;text-shadow:0 5px 0 rgba(0,0,0,.25);animation:slam .35s cubic-bezier(.2,1.8,.4,1) backwards}
@keyframes slam{from{transform:scale(3);opacity:0}}
.logo{font-family:'Pacifico',cursive;font-size:clamp(3.4rem,18vw,6rem);color:#ff5c9b;text-shadow:0 0 12px #ff5c9b,0 0 40px #ff3d81;animation:zl .8s cubic-bezier(.2,1.6,.4,1) backwards,glow 1.2s ease-in-out infinite alternate}
@keyframes zl{from{transform:scale(0);opacity:0}}
@keyframes glow{to{text-shadow:0 0 6px #ff5c9b,0 0 70px #ff3d81}}
.tg{font-weight:800;font-size:1.2rem;margin:6px 0 24px;animation:fade 1s .9s backwards}
.ent{width:min(80vw,320px);animation:fade 1s 2.6s backwards}
.bh{position:absolute;left:50%;top:45%;font-size:30px;animation:burst 1.6s ease-out backwards}
@keyframes burst{from{transform:translate(0,0) scale(.2);opacity:1}to{transform:translate(var(--x),var(--y)) scale(1.3);opacity:0}}
@media (prefers-reduced-motion:reduce){.flash{display:none}}
.k{display:inline-block;animation:kin .6s cubic-bezier(.2,1.6,.4,1) backwards}
@keyframes kin{from{transform:translateY(16px) scale(.7);opacity:0}}
@keyframes shk{25%{transform:translate(3px,-3px)}50%{transform:translate(-3px,3px)}75%{transform:translate(3px,3px)}}
.rumble .sl{animation:slam .35s cubic-bezier(.2,1.8,.4,1) backwards,shk .1s .4s linear infinite}
.vig{position:absolute;inset:0;box-shadow:inset 0 0 120px 30px rgba(0,0,0,.75);pointer-events:none;z-index:3}
.scan{position:absolute;inset:0;background:repeating-linear-gradient(transparent 0 3px,rgba(0,0,0,.2) 3px 4px);pointer-events:none;z-index:4}
.cap2{top:27%;color:#ffd27a}
.ph.fc{overflow:hidden;align-items:end}
.ph.two{width:min(88vw,400px);aspect-ratio:auto;border-radius:30px;display:flex;overflow:hidden}
.fz{flex:1;min-width:0}
.av2{display:block;width:100%;height:auto}
.clip{background:linear-gradient(160deg,#2b0a2e,#8a0f3a)}
.pair{display:flex;gap:6px;width:min(92vw,420px);animation:push 2.4s ease-in both}
@keyframes push{from{transform:scale(1)}to{transform:scale(1.15)}}
.pair .fz{background:rgba(255,255,255,.12);border-radius:20px;overflow:hidden}
.sp{background:#fff;color:#2a0f3d;border-radius:18px;padding:10px 16px;font-weight:800;font-size:1.2rem;margin:16px 14px 0;max-width:92%;animation:pop .4s .5s backwards}
.nx{position:absolute;top:calc(env(safe-area-inset-top,0px) + 46px);width:100%;text-align:center;font-weight:800;font-size:1.05rem;letter-spacing:.08em;color:#ff7a9a}
.ph2{background:#fff;color:#2a0f3d;border-radius:26px;padding:18px 22px;max-width:80vw;font-weight:800;font-size:1.4rem;animation:buzz .15s infinite}
@keyframes buzz{25%{transform:rotate(-3deg)}75%{transform:rotate(3deg)}}
@media (prefers-reduced-motion:reduce){.rumble .sl,.pair,.ph2{animation:none}}
.s2 .bubble{display:none}
.lsay{position:absolute;top:calc(env(safe-area-inset-top,0px) + 48px);left:12px;right:12px;display:flex;justify-content:center;z-index:6}
.sp2{background:#fff;color:#2a0f3d;border-radius:22px;padding:12px 18px;font-weight:800;font-size:1.25rem;box-shadow:0 8px 0 rgba(0,0,0,.2);animation:pop .4s backwards}
.lq{position:absolute;bottom:calc(env(safe-area-inset-bottom,0px) + 28px);left:14px;right:14px;background:rgba(255,255,255,.92);color:#2a0f3d;border-radius:20px;padding:10px 14px;font-weight:800;font-size:1.05rem;animation:pop .4s .8s backwards}
.cap3{top:36%;color:#ff7a9a}
.lightn{position:absolute;inset:0;background:#fff;opacity:0;z-index:6;pointer-events:none;animation:ltn 2s infinite}
@keyframes ltn{0%,6%,100%{opacity:0}2%{opacity:.35}}
@keyframes redp{from{box-shadow:inset 0 0 120px 30px rgba(120,0,20,.6)}to{box-shadow:inset 0 0 170px 60px rgba(230,0,50,.75)}}
.rumble .vig,.clip .vig{animation:redp .9s ease-in-out infinite alternate}
@media (prefers-reduced-motion:reduce){.lightn{display:none}}
.s1 .sunr{animation-duration:7s}
.s2 .zoom{animation-duration:13s}
.dl{position:relative;opacity:.55;transform:scale(.94)}
.dl.on{opacity:1;transform:scale(1.04);animation:talk .35s ease-in-out infinite alternate}
@keyframes talk{to{transform:translateY(-6px) scale(1.06)}}
.rx{position:absolute;top:6px;right:8px;font-size:34px;animation:pop .4s .2s backwards}
.dp{animation-duration:2.6s}
@media (prefers-reduced-motion:reduce){.dl.on{animation:none}}
.caps{position:absolute;top:10%;left:0;right:0;display:flex;flex-direction:column;gap:16px;align-items:center;text-align:center;padding:0 14px}
.cl{margin:0;font-family:'Pacifico',cursive;font-size:clamp(1.5rem,7vw,2.2rem)}
.pk{color:#ff7a9a}
.m .ph{width:min(52vw,220px)}
.pair.rw{animation:none;width:min(94vw,440px)}
.rw .fz{flex:1}
.tw{transform-box:fill-box;transform-origin:center;animation:tw 1.8s ease-in-out infinite alternate}
@keyframes tw{from{opacity:.2;transform:scale(.5)}to{opacity:1;transform:scale(1)}}
.av2{transform-origin:50% 100%;animation:bob 3.4s ease-in-out infinite alternate}
@keyframes bob{to{transform:translateY(-3px) rotate(1.2deg)}}
@media (prefers-reduced-motion:reduce){.av2{animation:none}}
</style>
</head>
<body>
<main class="wrap" id="app"></main>
<script>
var $=function(s){return document.querySelector(s)};
var esc=function(s){return String(s).replace(/[&<>"']/g,function(c){return{'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;'}[c]})};
var rnd=function(n){return Math.floor(Math.random()*n)};
var shuffle=function(a){a=a.slice();for(var i=a.length-1;i>0;i--){var j=rnd(i+1),t=a[i];a[i]=a[j];a[j]=t}return a};
var S={},timer=null;
function show(h){$('#app').innerHTML=h;window.scrollTo(0,0)}
var DEF="Lola\nBree\nRie\nLulu\nPuddy\nFaye\nTalisa\nKim\nDamien\nFefe";
var BONDS=[['Lola','Bree','real'],['Puddy','Faye','talking']];
function bond(a,b){for(var i=0;i<BONDS.length;i++){var x=BONDS[i];if((x[0]===a&&x[1]===b)||(x[0]===b&&x[1]===a))return x[2]}return null}
function lab(a,b){var t=bond(a,b);return t==='real'?' 💍':t==='talking'?' 💬':''}
function pickYou(){
  var b=S.alive.map(function(n,i){return '<button onclick="setYou('+i+')">'+esc(n)+'</button>'}).join('');
  show('<h2>Who are you?</h2><p class="tag">Pick the islander you want to play as.</p><div class="pick">'+b+'</div>');
}
function setYou(i){S.you=S.alive[i];pickPartner()}

function home(){
  show('<h1>Lulu Island</h1><p class="tag">Couple up, win the challenges, and don\'t get dumped from the island.</p>'+
  '<textarea id="names" rows="9" aria-label="Islanders">'+DEF+'</textarea>'+
  '<p class="hint">One name per line. Use an even number, 4 to 12. 💍 is a real couple and 💬 is talking.</p>'+
  '<div class="err" id="err"></div><button class="btn" onclick="begin()">Enter the villa</button>');
}
function begin(){
  var seen={},names=$('#names').value.split('\n').map(function(s){return s.trim()}).filter(function(s){if(!s||seen[s.toLowerCase()])return false;seen[s.toLowerCase()]=1;return true});
  if(names.length<4||names.length>12||names.length%2){$('#err').textContent='You have '+names.length+' islanders. Use an even number from 4 to 12.';return}
  S={alive:names,round:1};
  pickYou();
}
function pickPartner(){
  S.others=S.alive.filter(function(n){return n!==S.you});
  var b=S.others.map(function(n,i){return '<button onclick="couple('+i+')">'+esc(n)+'</button>'}).join('');
  show('<h2>Round '+S.round+': Coupling up</h2><p class="tag">'+S.alive.length+' islanders are left. Who do you want to couple up with?</p><div class="pick">'+b+'</div>');
}
function couple(i){
  var p=S.others[i],pool=S.alive.filter(function(n){return n!==S.you&&n!==p}),drama='';
  BONDS.forEach(function(b){var a=b.indexOf(S.you)>=0,c=b.indexOf(p)>=0;if(a!==c&&S.alive.indexOf(b[0])>=0&&S.alive.indexOf(b[1])>=0)drama+='<div class="msg"><b>Drama!</b> '+esc(S.you)+' just split up '+esc(b[0])+' &amp; '+esc(b[1])+'.</div>'});
  S.couples=[[S.you,p]];
  BONDS.forEach(function(b){if(pool.indexOf(b[0])>=0&&pool.indexOf(b[1])>=0){S.couples.push([b[0],b[1]]);pool=pool.filter(function(n){return n!==b[0]&&n!==b[1]})}});
  pool=shuffle(pool);
  for(var j=0;j<pool.length;j+=2)S.couples.push([pool[j],pool[j+1]]);
  S.chem=S.couples.map(function(c){var t=bond(c[0],c[1]);return t==='real'?100:t==='talking'?90:40+rnd(60)});
  var h=S.couples.map(function(c,k){return '<div class="couple'+(k?'':' you')+'"><span><b>'+esc(c[0])+'</b> &amp; <b>'+esc(c[1])+'</b>'+lab(c[0],c[1])+'</span><span class="num">'+S.chem[k]+'% match</span></div>'}).join('');
  show('<h2>The couples</h2><p class="tag">Match percentage gives each couple a small boost in the challenge.</p>'+drama+h+'<button class="btn" onclick="challenge()">Start the challenge</button>');
}
function challenge(){
  var taps=0,left=80;
  show('<h2>Heart Catch</h2><p class="tag">Tap the hearts for '+esc(S.couples[0][0])+' &amp; '+esc(S.couples[0][1])+'. You have 8 seconds.</p>'+
  '<div class="hud"><span>Hearts: <span id="t">0</span></span><span>Time: <span id="l">8.0</span>s</span></div><div class="arena" id="ar"><button class="heart" id="h" aria-label="Heart">💖</button></div>');
  var h=$('#h');
  function move(){h.style.left=rnd(240)/2.4+'%';h.style.top=rnd(240)/2.4+'%'}
  move();
  h.onclick=function(){taps++;$('#t').textContent=taps;move()};
  clearInterval(timer);
  timer=setInterval(function(){left--;$('#l').textContent=(left/10).toFixed(1);if(left<=0){clearInterval(timer);finish(taps)}},100);
}
function finish(taps){
  S.res=S.couples.map(function(c,k){
    var bonus=Math.round(S.chem[k]/10),pts=k===0?taps:8+S.round*2+rnd(14);
    return{c:c,k:k,pts:pts,total:pts+bonus,key:pts+bonus+Math.random()*.5};
  }).sort(function(a,b){return b.key-a.key});
  var h=S.res.map(function(r,i){var last=i===S.res.length-1;
    return '<div class="couple'+(r.k===0?' you':'')+(last?' danger':'')+'"><span><b>'+esc(r.c[0])+'</b> &amp; <b>'+esc(r.c[1])+'</b>'+(last?'<br><small>In the danger zone</small>':'')+'</span><span class="num">'+r.total+' pts</span></div>'}).join('');
  show('<h2>Challenge results</h2><p class="tag">You caught '+taps+' hearts. The lowest couple is at risk.</p>'+h+'<button class="btn" onclick="elim()">Read the text message</button>');
}
function elim(){
  var lo=S.res[S.res.length-1],gone=lo.c;
  var msg='<div class="big">💌</div><div class="msg"><b>I got a text!</b><br>'+esc(gone[0])+' and '+esc(gone[1])+', you have been dumped from the island.</div>';
  if(lo.k===0){
    show('<h2>Dumped!</h2>'+msg+'<p class="tag">You and '+esc(gone[1])+' made it to round '+S.round+'.</p><button class="btn" onclick="home()">Play again</button>');return}
  S.alive=S.alive.filter(function(n){return gone.indexOf(n)<0});
  S.round++;
  if(S.alive.length<=2){
    show('<h2>Final</h2>'+msg+'<button class="btn alt" onclick="win()">Meet the winners</button>');
  }else{
    show('<h2>Round '+(S.round-1)+' over</h2>'+msg+'<button class="btn" onclick="pickPartner()">Next round</button>');
  }
}
function win(){
  var p=S.alive.filter(function(n){return n!==S.you})[0];
  show('<h1>Winners!</h1><div class="big">👑🏝️👑</div><p class="tag" style="text-align:center;font-size:1.2rem"><b>'+esc(S.you)+'</b> &amp; <b>'+esc(p)+'</b> win Lulu Island!</p><button class="btn" onclick="home()">Play again</button>');
}
function lulu(){
  var palm="<g id='palm'><g class='sway'><path d='M50 440Q38 340 72 250' stroke='#2d1442' stroke-width='9' fill='none' stroke-linecap='round'/><g fill='#1c7a62'>"+[-35,10,60,160,205].map(function(a){return "<ellipse cx='108' cy='250' rx='36' ry='9' transform='rotate("+a+" 72 250)'/>"}).join("")+"</g></g></g>";
  var W="q15-14 30 0"+new Array(18).join("t30 0");
  var eye=function(x,c){return "<g class='"+c+"'><ellipse cx='"+x+"' cy='258' rx='17' ry='20' fill='#fff'/><circle cx='"+x+"' cy='260' r='13' fill='url(#ir)'/><circle cx='"+x+"' cy='260' r='6' fill='#0f2f1d'/><circle cx='"+(x-5)+"' cy='253' r='4.5' fill='#fff'/><circle cx='"+(x+4)+"' cy='266' r='2' fill='#fff'/></g>"};
  var hearts=["💖","💋","💗"].map(function(e,i){return "<text class='fly' style='animation-delay:"+(i*.3)+"s' x='"+(174+i*5)+"' y='304' font-size='20'>"+e+"</text>"}).join("");
  var petals=[0,72,144,216,288].map(function(a){return "<ellipse cy='-9' rx='6.5' ry='10' fill='#ff5c9b' transform='rotate("+a+")'/>"}).join("");
  var brow="fill='none' stroke='#4a2414' stroke-width='3' stroke-linecap='round'";
  return "<svg class='scene' viewBox='0 0 360 520' role='img' aria-label='Lulu winks and blows a kiss on the island'>"+
  "<defs><linearGradient id='sk' x1='0' y1='0' x2='0' y2='1'><stop offset='0' stop-color='#5b2a86'/><stop offset='.55' stop-color='#ff5c9b'/><stop offset='1' stop-color='#ffb06a'/></linearGradient>"+
  "<linearGradient id='se' x1='0' y1='0' x2='0' y2='1'><stop offset='0' stop-color='#14b8b0'/><stop offset='1' stop-color='#0a5f86'/></linearGradient>"+
  "<radialGradient id='ir' cx='.4' cy='.35' r='.8'><stop offset='0' stop-color='#7ae8a8'/><stop offset='.6' stop-color='#25a862'/><stop offset='1' stop-color='#136b3c'/></radialGradient>"+palm+"</defs>"+
  "<rect width='360' height='520' fill='url(#sk)'/>"+
  "<circle cx='180' cy='340' r='140' fill='#ffd27a' opacity='.2'/><circle class='sun' cx='180' cy='340' r='105' fill='#ffd27a' opacity='.85'/>"+
  "<use href='#palm'/><use href='#palm' transform='translate(360 0) scale(-1 1)'/>"+
  "<path class='wave' d='M-60 405"+W+"L480 520L-60 520Z' fill='#14b8b0' opacity='.7'/>"+
  "<path class='wave w2' d='M-60 440"+W+"L480 520L-60 520Z' fill='url(#se)'/>"+
  "<g class='tilt'><path d='M180 168C100 168 92 270 100 340C104 395 90 420 112 442L248 442C270 420 256 395 260 340C268 270 260 168 180 168Z' fill='#5a2f1b'/></g>"+
  "<rect x='167' y='298' width='26' height='52' rx='10' fill='#f3c9b8'/><path d='M118 520Q118 382 160 346L200 346Q242 382 242 520Z' fill='#ffe3d6'/>"+
  "<path d='M120 440Q180 414 240 440L242 520L118 520Z' fill='#ff4d94'/><path d='M158 352Q180 372 202 352' stroke='#ffcc4d' stroke-width='2.5' fill='none'/><circle cx='180' cy='366' r='4' fill='#ffcc4d'/>"+
  "<path d='M106 300C98 360 100 412 118 442C134 420 138 360 134 318Z' fill='#6b3a22'/><path d='M254 300C262 360 260 412 242 442C226 420 222 360 226 318Z' fill='#6b3a22'/>"+
  "<g class='tilt'><ellipse cx='180' cy='250' rx='60' ry='64' fill='#ffe3d6'/>"+
  "<circle cx='140' cy='284' r='10' fill='#ff8fab' opacity='.45'/><circle cx='220' cy='284' r='10' fill='#ff8fab' opacity='.45'/>"+
  eye(153,"blink")+eye(207,"wink")+
  "<path d='M134 252Q152 233 171 249M189 249Q208 233 226 252' stroke='#3a1d12' stroke-width='3.5' fill='none' stroke-linecap='round'/>"+
  "<path class='winkline' d='M189 257Q207 271 225 257' stroke='#3a1d12' stroke-width='3.5' fill='none' stroke-linecap='round'/>"+
  "<path d='M138 232Q153 224 168 231' "+brow+"/><path class='brow' d='M192 231Q207 224 222 232' "+brow+"/>"+
  "<path d='M180 276q-3 6 2 7' stroke='#e0a58f' stroke-width='2' fill='none' stroke-linecap='round'/>"+
  "<g class='smile'><path d='M169 290Q180 305 191 290Q180 297 169 290Z' fill='#ff5c8a' stroke='#d6336c' stroke-width='2.5' stroke-linejoin='round'/></g>"+
  "<g class='kiss'><ellipse cx='180' cy='294' rx='7' ry='6' fill='#e0245e'/><circle cx='178' cy='292' r='1.8' fill='#fff' opacity='.8'/></g>"+
  "<path d='M116 244C114 178 150 166 182 166C214 166 248 178 244 244C230 212 212 196 190 192C168 208 140 212 116 244Z' fill='#6b3a22'/><path d='M150 190Q180 176 212 192' stroke='#8a4f2e' stroke-width='3' fill='none' opacity='.7'/>"+
  "<g transform='translate(234 204)'>"+petals+"<circle r='4' fill='#ffcc4d'/></g>"+
  "<circle cx='124' cy='292' r='5' fill='none' stroke='#ffcc4d' stroke-width='2.5'/><circle cx='236' cy='292' r='5' fill='none' stroke='#ffcc4d' stroke-width='2.5'/></g>"+
  hearts+
  "<g class='bubble'><rect x='198' y='64' width='150' height='58' rx='18' fill='#fff'/><path d='M222 120L214 142L244 120Z' fill='#fff'/><text x='212' y='88' font-size='14' font-weight='800' font-family='Nunito,sans-serif' fill='#2a0f3d'>Hey you… 😉</text><text x='212' y='108' font-size='13' font-weight='800' font-family='Nunito,sans-serif' fill='#2a0f3d'>ready to couple up?</text></g></svg>";
}
function intro(){
  show("<div class='intro'><h1>Lulu Island</h1>"+lulu()+"<p class='tag sub'>Short episodes from the villa. Sound on, babes. 💕</p><button class='btn go' onclick='play5()'>▶ Watch Episode 1 (sound on!)</button><button class='btn alt' onclick='play6()'>▶ Watch Episode 2 (sound on!)</button><button class='btn alt' onclick='play7()'>▶ Watch Episode 3 (sound on!)</button></div>");
}
var AC=null,M=null,NB=null,TL=[];
function at(ms,f){TL.push(setTimeout(f,ms))}
function sc(h){$('#sc').innerHTML="<div class='flash'></div>"+h}
function mtof(m){return 440*Math.pow(2,(m-69)/12)}
function tone(t,f,d,ty,v,lp){var o=AC.createOscillator(),g=AC.createGain(),l=AC.createBiquadFilter();o.type=ty;o.frequency.value=f;l.type='lowpass';l.frequency.value=lp;g.gain.setValueAtTime(.0001,t);g.gain.linearRampToValueAtTime(v,t+.01);g.gain.exponentialRampToValueAtTime(.001,t+d);o.connect(l);l.connect(g);g.connect(M);o.start(t);o.stop(t+d+.05)}
function nz(t,d,v,hp){var s=AC.createBufferSource(),f=AC.createBiquadFilter(),g=AC.createGain();s.buffer=NB;f.type='highpass';f.frequency.value=hp;g.gain.setValueAtTime(v,t);g.gain.exponentialRampToValueAtTime(.001,t+d);s.connect(f);f.connect(g);g.connect(M);s.start(t);s.stop(t+d)}
function kick(t){var o=AC.createOscillator(),g=AC.createGain();o.frequency.setValueAtTime(150,t);o.frequency.exponentialRampToValueAtTime(45,t+.12);g.gain.setValueAtTime(.9,t);g.gain.exponentialRampToValueAtTime(.001,t+.22);o.connect(g);g.connect(M);o.start(t);o.stop(t+.25)}
function music(t0){
  var B=.5,CH=[[60,64,67],[55,59,62],[57,60,64],[53,57,60]],RT=[48,43,45,41];
  for(var bar=0;bar<48;bar++){var c=CH[bar%4],r=RT[bar%4],T=bar>=20&&bar<=27;if(bar<4&&bar%2===0)c.forEach(function(n){tone(t0+bar*2,mtof(n-12),4,'sine',.12,900)});
    for(var b=0;b<4;b++){var t=t0+(bar*4+b)*B;
      if(T){if(b===0||b===2){kick(t);kick(t+.2);if(b===0)tone(t,mtof(r-12),1.8,'sine',.5,300)}}else if(bar>=4){kick(t);nz(t+B/2,.05,.12,7000)}
      if(!T&&bar>=6&&!(bar>=28&&bar<=41)&&(b===1||b===3))nz(t,.12,.35,1200);
      if(!T&&bar>=2){tone(t,mtof(r),.4,'sawtooth',.26,420);tone(t+B/2,mtof(r+(b%2?7:0)),.2,'sawtooth',.2,420)}
    }
    if(!T)[0,1.5].forEach(function(x){c.forEach(function(n){tone(t0+(bar*4+x)*B,mtof(n),.35,'square',.05,2500)})});
    if(bar>=6&&!T&&!(bar>=28&&bar<=41))for(var k=0;k<8;k++)tone(t0+(bar*4+k/2)*B,mtof(c[k%3]+12+(k%4===3?12:0)),.22,'sawtooth',.05,3000);
  }
  var s=AC.createBufferSource(),f=AC.createBiquadFilter(),g=AC.createGain();s.buffer=NB;s.loop=true;f.type='highpass';f.frequency.setValueAtTime(400,t0+86.5);f.frequency.exponentialRampToValueAtTime(7000,t0+90.5);g.gain.setValueAtTime(.001,t0+86.5);g.gain.linearRampToValueAtTime(.3,t0+90.5);g.gain.setValueAtTime(0,t0+90.55);s.connect(f);f.connect(g);g.connect(M);s.start(t0+86.5);s.stop(t0+90.6);
  nz(t0+90.5,1.6,.5,3000);kick(t0+90.5);
  M.gain.setValueAtTime(.8,t0+95.3);M.gain.linearRampToValueAtTime(.05,t0+96.5);
}
var CARDS=[["Rene","😎","#ff9a3c","#ff3d81","Single and ready to mingle"],["Talisa","💃","#14b8b0","#5b2a86","Single and ready to mingle"],["Kim","🌸","#ff5c9b","#ffb06a","Single and ready to mingle"],["Damien","🕶️","#3a7bd5","#8e2de2","Single and ready to mingle"],["Fefe","🦋","#8e2de2","#ff5c9b","Single and ready to mingle"],["Lola & Bree","💍","#ff3d81","#ff9a3c","Already a couple. For now…"],["Puddy & Faye","💬","#14b8b0","#ffcc4d","It's complicated. They're talking."]];
function card(i){var c=CARDS[i],h=[10,30,50,70,88].map(function(l,j){return "<span class='hr' style='left:"+l+"%;animation-delay:"+(j*.3)+"s'>💗</span>"}).join("");
  sc("<div class='sc' style='background:linear-gradient(160deg,"+c[2]+","+c[3]+")'><div class='ph'><span>"+c[1]+"</span></div><div class='nm'>"+c[0]+"</div><div class='sb'>"+c[4]+"</div>"+h+"</div>")}
function slam(t,e,bg){sc("<div class='sc' style='background:"+bg+"'><div class='sl'>"+e+"<br>"+t+"</div></div>")}
function logo(){var b="";for(var i=0;i<12;i++){var a=i*Math.PI/6;b+="<span class='bh' style='--x:"+Math.round(Math.cos(a)*150)+"px;--y:"+Math.round(Math.sin(a)*150)+"px;animation-delay:"+(i%3)*.05+"s'>"+(i%2?"💖":"✨")+"</span>"}
  sc("<div class='sc' style='background:radial-gradient(circle at 50% 45%,#5b1a6e,#12041f 70%)'>"+b+"<div class='logo'>Lulu Island</div><p class='tg'>Love. Drama. Paradise.</p><button class='btn ent' onclick='skip()'>Enter the villa</button></div>")}
function play(){
  var st=document.createElement('div');st.id='stage';st.innerHTML="<div id='sc'></div><div class='bug'>● LIVE</div><button class='skip' onclick='skip()'>Skip ▸</button>";document.body.appendChild(st);
  var t0=0;
  try{AC=new (window.AudioContext||window.webkitAudioContext)();if(AC.state==='suspended')AC.resume();M=AC.createGain();M.gain.value=.8;M.connect(AC.destination);NB=AC.createBuffer(1,AC.sampleRate*2,AC.sampleRate);var d=NB.getChannelData(0);for(var i=0;i<d.length;i++)d[i]=Math.random()*2-1;t0=AC.currentTime+.15;music(t0)}catch(e){AC=null}
  at(150,function(){sc("<div class='sc s1'><div class='sunr'></div><div class='pl sway' style='left:4%'>🌴</div><div class='pl sway' style='right:4%'>🌴</div><div class='sea'></div><p class='cap'>Somewhere in paradise…</p></div>")});
  at(3150,function(){sc("<div class='sc s2'><div class='zoom'>"+lulu()+"</div><div class='lt'>Lulu 💚 your host</div></div>")});
  for(var i=0;i<7;i++)(function(i){at(9150+i*1700,function(){card(i)})})(i);
  at(21150,function(){slam("Couple up","💘","#e8236f")});
  at(22850,function(){slam("Win the challenges","🏆","#0a7f86")});
  at(24550,function(){slam("Don't get dumped","💌","#d96a0c")});
  at(26150,logo);
}
function skip(){TL.forEach(clearTimeout);TL=[];try{speechSynthesis.cancel()}catch(e){}var a=AC;if(a){try{M.gain.cancelScheduledValues(0);M.gain.setTargetAtTime(0,a.currentTime,.08);setTimeout(function(){a.close()},500)}catch(e){}}AC=null;var s=$('#stage');if(s)s.remove();intro()}
var CAST={Damien:{skin:"#f1c9a5",hair:"#17120f",style:"long",top:"#3a7bd5"},Talisa:{skin:"#e8b890",hair:"#d6402a",style:"bob",top:"#14b8b0"},Kim:{skin:"#f1c9a5",hair:"#1a1512",style:"wolf",top:"#8e2de2"},Puddy:{skin:"#7a4a2e",hair:"#3b2214",style:"mid",top:"#ff9a3c"},Faye:{skin:"#f6d9bd",hair:"#17120f",style:"mid",top:"#ff5c9b"},Rie:{skin:"#b9774a",hair:"#5a3418",style:"pony",top:"#14b8b0"},Lola:{skin:"#fde6d8",hair:"#f0cf6a",eye:"#a27a2b",style:"long",top:"#ff3d81"},Bree:{skin:"#d9a577",hair:"#14100d",style:"long",top:"#0a7f86"},Lulu:{skin:"#ffe3d6",hair:"#5a2f1b",eye:"#25a862",style:"long",top:"#ff4d94"}};
function face(n){var o=CAST[n],s=o.skin,h=o.hair,e=o.eye||"#4a2a12",k=o.style;
  var B={long:"M100 18C44 18 36 100 42 150C44 188 36 205 52 216L148 216C164 205 156 188 158 150C164 100 156 18 100 18Z",mid:"M100 18C46 18 40 96 44 135C46 160 40 172 54 180L146 180C160 172 154 160 156 135C160 96 154 18 100 18Z",bob:"M100 20C48 20 42 80 46 118C50 134 62 138 66 130L134 130C138 138 150 134 154 118C158 80 152 20 100 20Z",wolf:"M100 18C50 18 38 70 46 112L38 134L58 126L62 142L76 128L100 136L124 128L138 142L142 126L162 134L154 112C162 70 150 18 100 18Z",pony:"M100 22C52 22 44 80 50 120L150 120C156 80 148 22 100 22Z"}[k];
  var tail=k==="pony"?"<path d='M142 52C196 56 200 140 176 180C170 150 170 112 140 96Z' fill='"+h+"'/><circle cx='146' cy='62' r='6' fill='#ff5c9b'/>":"";
  var ey=function(x){return "<g class='blink'><ellipse cx='"+x+"' cy='116' rx='11' ry='13' fill='#fff'/><circle cx='"+x+"' cy='118' r='8.5' fill='"+e+"'/><circle cx='"+x+"' cy='118' r='4' fill='#1d1208'/><circle cx='"+(x-3)+"' cy='113' r='3' fill='#fff'/></g>"};
  return "<svg viewBox='0 0 200 220' class='av2'><path d='"+B+"' fill='"+h+"'/>"+tail+"<path d='M40 220C40 172 70 158 100 158C130 158 160 172 160 220Z' fill='"+o.top+"'/><rect x='88' y='140' width='24' height='26' rx='8' fill='"+s+"'/><ellipse cx='100' cy='110' rx='46' ry='50' fill='"+s+"'/><circle cx='64' cy='136' r='9' fill='#ff7a9a' opacity='.4'/><circle cx='136' cy='136' r='9' fill='#ff7a9a' opacity='.4'/>"+ey(80)+ey(120)+"<path d='M66 112Q80 98 94 110M106 110Q120 98 134 112' stroke='#2a160c' stroke-width='3' fill='none' stroke-linecap='round'/><path d='M92 142Q100 151 108 142' stroke='#c2415f' stroke-width='3' fill='none' stroke-linecap='round'/><path d='M54 104C52 50 80 34 102 34C126 34 150 50 146 104C136 78 122 66 104 62C84 76 68 82 54 104Z' fill='"+h+"'/></svg>"}
function kin(t,d,sp){var o="",i=0;t.split(" ").forEach(function(w){o+="<span style='display:inline-block;white-space:nowrap'>";w.split("").forEach(function(ch){o+="<span class='k' style='animation-delay:"+((d||0)+i*(sp||.04))+"s'>"+ch+"</span>";i++});o+="</span> "});return o}
var CARDS2=[{n:"Rie",f:["Rie"],a:"#ff9a3c",b:"#ff3d81",s:"Calm on the outside. Plotting on the inside."},{n:"Talisa",f:["Talisa"],a:"#14b8b0",b:"#5b2a86",s:"She sees everything. She says nothing."},{n:"Kim",f:["Kim"],a:"#8e2de2",b:"#ff5c9b",s:"Here to win. Heart optional."},{n:"Damien",f:["Damien"],a:"#3a7bd5",b:"#8e2de2",s:"Heartbreaker. Allegedly."},{n:"Fefe",f:[],a:"#ff5c9b",b:"#5b2a86",s:"One secret could burn the villa down."},{n:"Lola & Bree",f:["Lola","Bree"],a:"#ff3d81",b:"#ff9a3c",s:"Together for real… until someone gets between them."},{n:"Puddy & Faye",f:["Puddy","Faye"],a:"#14b8b0",b:"#ffcc4d",s:"Just talking. Or are they?"}];
var CLIPS=[{f:["Bree","Lola"],s:"Bree",q:"Who were you with last night?"},{f:["Puddy","Faye"],s:"Puddy",q:"We're just talking… right?"},{f:["Kim","Damien"],s:"Kim",q:"I know what you did."},{f:["Talisa","Rie"],s:"Talisa",q:"Don't tell Lulu."},{f:["Lulu"],s:"Lulu",q:"Somebody's getting dumped tonight 😉"}];
function card2(i){var c=CARDS2[i],h=[10,30,50,70,88].map(function(l,j){return "<span class='hr' style='left:"+l+"%;animation-delay:"+(j*.3)+"s'>💗</span>"}).join("");
  var fz=function(x){return "<div class='fz'>"+face(x)+"</div>"};
  var av=c.f.length===2?"<div class='ph two'>"+fz(c.f[0])+fz(c.f[1])+"</div>":c.f.length?"<div class='ph fc'>"+face(c.f[0])+"</div>":"<div class='ph'><span>🦋</span></div>";
  sc("<div class='sc' style='background:linear-gradient(160deg,"+c.a+","+c.b+")'><div class='vig'></div>"+av+"<div class='nm'>"+kin(c.n,.15)+"</div><div class='sb'>"+c.s+"</div><div class='lq'>💚 Lulu: "+kin(c.l||"",.9)+"</div>"+h+"</div>")}
function slam2(t,bg){sc("<div class='sc rumble' style='background:"+bg+"'><div class='vig'></div><div class='sl'>"+kin(t,0)+"</div></div>")}
function txt(){sc("<div class='sc' style='background:#12041f'><div class='vig'></div><div class='ph2'>📱 I got a text!<br><small>Islanders, one couple will be dumped tonight…</small></div></div>")}
function clip(i){var c=CLIPS[i],p=c.f.map(function(x){return "<div class='fz'>"+face(x)+"</div>"}).join("");
  sc("<div class='sc clip'><div class='scan'></div><div class='vig'></div><div class='nx'>NEXT ON LULU ISLAND</div><div class='pair' style='"+(c.f.length<2?"width:min(60vw,240px)":"")+"'>"+p+"</div><div class='sp'><b>"+c.s+":</b> "+kin(c.q,.5)+"</div></div>")}
function play2(){
  var st=document.createElement('div');st.id='stage';st.innerHTML="<div id='sc'></div><div class='bug'>● LIVE</div><button class='skip' onclick='skip()'>Skip ▸</button>";document.body.appendChild(st);
  try{AC=new (window.AudioContext||window.webkitAudioContext)();if(AC.state==='suspended')AC.resume();M=AC.createGain();M.gain.value=.8;M.connect(AC.destination);NB=AC.createBuffer(1,AC.sampleRate*2,AC.sampleRate);var d=NB.getChannelData(0);for(var i=0;i<d.length;i++)d[i]=Math.random()*2-1;music(AC.currentTime+.15)}catch(e){AC=null}
  at(150,function(){sc("<div class='sc s1'><div class='sunr'></div><div class='pl sway' style='left:4%'>🌴</div><div class='pl sway' style='right:4%'>🌴</div><div class='sea'></div><p class='cap'>"+kin("Somewhere in paradise…",.3)+"</p><p class='cap cap2'>"+kin("…where secrets are buried.",2.2)+"</p></div>")});
  at(4650,function(){sc("<div class='sc s2'><div class='zoom'>"+lulu()+"</div><div class='lt'>Lulu 💚 your host</div></div>")});
  for(var i=0;i<7;i++)(function(i){at(10650+i*1750,function(){card2(i)})})(i);
  at(22950,function(){slam2("Secrets…","#3a0a1f")});at(24150,function(){slam2("Lies…","#12041f")});at(25350,function(){slam2("Temptation…","#7a0f3a")});at(26550,txt);
  for(var j=0;j<5;j++)(function(j){at(28150+j*2400,function(){clip(j)})})(j);
  at(40150,logo);
}
CAST.Fefe={skin:"#f1cfa8",hair:"#100c0a",style:"long",top:"#ffcc4d"};
CARDS2[4].f=["Fefe"];
var LQ=["Sweet like mango… but watch out 🥭","Quiet girls always have the best tea ☕","She's here to win, babes 🏆","Cute and dangerous. My favorite 😏","Mystery girl. I LOVE a secret 🤫","Aww… real love. Let's see how long it lasts 💔","Just talking? Girl, please 🙄"];
CARDS2.forEach(function(c,i){c.l=LQ[i]});
CLIPS.splice(4,0,{f:["Fefe","Lola"],s:"Fefe",q:"It wasn't me… I swear."});
function speak(t){try{var u=new SpeechSynthesisUtterance(t.replace(/[^\w\s.,!?'~]/g,''));u.pitch=1.7;u.rate=1.05;speechSynthesis.cancel();speechSynthesis.speak(u)}catch(e){}}
function say(t){var e=$('#ls');if(e)e.innerHTML="<div class='sp2'>"+kin(t,0)+"</div>";speak(t)}
function play3(){
  play2();TL.forEach(clearTimeout);TL=[];
  at(150,function(){sc("<div class='sc s1'><div class='sunr'></div><div class='pl sway' style='left:4%'>🌴</div><div class='pl sway' style='right:4%'>🌴</div><div class='sea'></div><p class='cap'>"+kin("Somewhere in paradise…",.3)+"</p><p class='cap cap2'>"+kin("…where secrets are buried.",2.2)+"</p><p class='cap cap3'>"+kin("…and one of you is going home.",4.2)+"</p></div>")});
  at(6150,function(){sc("<div class='sc s2'><div class='zoom'>"+lulu()+"</div><div class='lt'>Lulu 💚 your host</div><div class='lsay' id='ls'></div></div>")});
  [["Hiii babes~ welcome to Lulu Island! 💕",6300],["I'm Lulu, your host… and I know ALL the secrets 😉",9500],["Grab your popcorn, cuties. It's about to get messy! 🍿",12700],["Now meet the islanders… 🌴",15300]].forEach(function(x){at(x[1],function(){say(x[0])})});
  for(var i=0;i<7;i++)(function(i){at(17150+i*2000,function(){card2(i)})})(i);
  at(31150,function(){slam2("Secrets…","#3a0a1f")});at(32350,function(){slam2("Lies…","#12041f")});at(33550,function(){slam2("Betrayal…","#7a0f3a")});at(34750,function(){slam2("Temptation…","#3a0a1f")});
  at(35950,function(){sc("<div class='sc' style='background:radial-gradient(circle,#3a0a3f,#0b0212 75%)'><div class='lightn'></div><div class='vig'></div><div class='ph fc'>"+face("Lulu")+"</div><div class='sp'>"+kin("Ooooh… somebody's about to get their heart broken 💔",.2)+"</div></div>");speak("Ooh, somebody's about to get their heart broken")});
  at(38150,txt);
  for(var j=0;j<6;j++)(function(j){at(40150+j*2400,function(){clip(j)})})(j);
  at(52300,function(){speak("Somebody's getting dumped tonight")});
  at(54650,logo);
}
var DLG=[{f:["Bree","Lola"],bg:"linear-gradient(160deg,#2b0a2e,#8a0f3a)",l:[["Bree","Who were you with last night?","😳"],["Lola","Nobody! Why are you doing this?","💔"],["Bree","I saw you, Lola…","😢"]]},
{f:["Puddy","Faye"],bg:"linear-gradient(160deg,#0b1a3a,#5b2a86)",l:[["Puddy","So… are we official, or are we just talking?","👀"],["Faye","Define official 👀","😏"],["Puddy","Faye.","😤"]]},
{f:["Kim","Damien"],bg:"linear-gradient(160deg,#1a0a2e,#6b1030)",l:[["Kim","I know what you did.","😶"],["Damien","Kim… don't.","😰"],["Kim","Everyone's about to find out.","😈"]]},
{f:["Talisa","Rie","Fefe"],bg:"linear-gradient(160deg,#0a1f2e,#3a0a3f)",l:[["Talisa","Don't tell Lulu.","🤫"],["Rie","Tell her WHAT?","😳"],["Fefe","…It's already too late.","😱"]]}];
function dlg(i,k){var d=DLG[i],ln=d.l[k];
  var p=d.f.map(function(x){var on=x===ln[0];return "<div class='fz dl"+(on?" on":"")+"'>"+face(x)+(on?"":"<span class='rx'>"+ln[2]+"</span>")+"</div>"}).join("");
  sc("<div class='sc clip' style='background:"+d.bg+"'><div class='scan'></div><div class='vig'></div><div class='nx'>NEXT ON LULU ISLAND</div><div class='pair dp'>"+p+"</div><div class='sp'><b>"+ln[0]+":</b> "+kin(ln[1],.2,.05)+"</div></div>")}
function play4(){
  play2();TL.forEach(clearTimeout);TL=[];
  at(150,function(){sc("<div class='sc s1'><div class='sunr'></div><div class='pl sway' style='left:4%'>🌴</div><div class='pl sway' style='right:4%'>🌴</div><div class='sea'></div><p class='cap'>"+kin("Somewhere in paradise…",.8,.09)+"</p><p class='cap cap2'>"+kin("…where secrets are buried.",3.8,.09)+"</p><p class='cap cap3'>"+kin("…and one of you is going home.",6.6,.07)+"</p></div>")});
  at(9350,function(){sc("<div class='sc s2'><div class='zoom'>"+lulu()+"</div><div class='lt'>Lulu 💚 your host</div><div class='lsay' id='ls'></div></div>")});
  [["Hiii babes~ welcome to Lulu Island! 💕",9500],["I'm Lulu, your host… and I know ALL the secrets 😉",13000],["Grab your popcorn, cuties. It's about to get messy! 🍿",16600],["Now meet the islanders… 🌴",20200]].forEach(function(x){at(x[1],function(){say(x[0])})});
  for(var i=0;i<7;i++)(function(i){at(23150+i*2600,function(){card2(i)})})(i);
  at(41350,function(){slam2("Secrets…","#3a0a1f")});at(43050,function(){slam2("Lies…","#12041f")});at(44750,function(){slam2("Betrayal…","#7a0f3a")});at(46450,function(){slam2("Temptation…","#3a0a1f")});
  at(48150,function(){sc("<div class='sc' style='background:radial-gradient(circle,#3a0a3f,#0b0212 75%)'><div class='lightn'></div><div class='vig'></div><div class='ph fc'>"+face("Lulu")+"</div><div class='sp'>"+kin("Ooooh… somebody's about to get their heart broken 💔",.2,.07)+"</div></div>");speak("Ooh, somebody's about to get their heart broken")});
  at(52650,txt);
  DLG.forEach(function(d,i){d.l.forEach(function(l,k){at(55650+i*7200+k*2400,function(){dlg(i,k)})})});
  at(84450,function(){sc("<div class='sc' style='background:radial-gradient(circle,#5b1a6e,#12041f 75%)'><div class='vig'></div><div class='ph fc'>"+face("Lulu")+"</div><div class='sp'>"+kin("Somebody's getting dumped tonight… 😉",.2,.06)+"</div></div>");speak("Somebody's getting dumped tonight")});
  at(87500,function(){sc("<div class='sc' style='background:radial-gradient(circle,#5b1a6e,#12041f 75%)'><div class='vig'></div><div class='ph fc'>"+face("Lulu")+"</div><div class='sp'>"+kin("Stay tuned, cuties… 💋",.2,.06)+"</div></div>");speak("Stay tuned, cuties")});
  at(90650,logo);
}
CAST.Soomy={skin:"#d9a877",hair:"#5a3418",style:"long",top:"#5b8def"};
function spk(t,p){try{var u=new SpeechSynthesisUtterance(t.replace(/[^\w\s.,!?'~]/g,''));u.pitch=p||1.5;u.rate=1.05;speechSynthesis.cancel();speechSynthesis.speak(u)}catch(e){}}
function talk(f,bg,lb,ln){var p=f.map(function(x){var on=x===ln[0];return "<div class='fz dl"+(on?" on":"")+"'>"+face(x)+(on||!ln[2]?"":"<span class='rx'>"+ln[2]+"</span>")+"</div>"}).join("");
  sc("<div class='sc clip' style='background:"+bg+"'><div class='vig'></div><div class='nx'>"+lb+"</div><div class='pair dp'>"+p+"</div><div class='sp'><b>"+ln[0]+":</b> "+kin(ln[1],.15,.04)+"</div></div>");if(ln[3])spk(ln[1],ln[3])}
function meet(n,tag,line,a,b){sc("<div class='sc m' style='background:linear-gradient(160deg,"+a+","+b+")'><div class='vig'></div><div class='nx'>MEET THE ISLANDERS</div><div class='ph fc'>"+face(n)+"</div><div class='nm'>"+kin(n,.2,.08)+"</div><div class='sb'>"+tag+"</div><div class='sp'>"+kin(line,.9,.04)+"</div></div>")}
function ttl(sub,btn){var b="";for(var i=0;i<12;i++){var a=i*Math.PI/6;b+="<span class='bh' style='--x:"+Math.round(Math.cos(a)*150)+"px;--y:"+Math.round(Math.sin(a)*150)+"px'>"+(i%2?"💖":"✨")+"</span>"}
  sc("<div class='sc' style='background:radial-gradient(circle at 50% 45%,#5b1a6e,#12041f 70%)'>"+b+"<div class='logo'>Lulu Island</div><p class='tg'>Hosted by Lola &amp; Bree 💍</p><p class='tg'>"+kin(sub,1.2,.06)+"</p>"+(btn?"<button class='btn ent' onclick='skip()'>Back to episodes</button>":"")+"</div>")}
function mus(t0){
  var B=.5,CH=[[60,64,67],[55,59,62],[57,60,64],[53,57,60]],RT=[48,43,45,41];
  for(var bar=0;bar<60;bar++){var s=bar*2,c=CH[bar%4],r=RT[bar%4],calm=s<8||s>=116,lull=s>=8&&s<16,beat=(s>=16&&s<72)||(s>=82&&s<116),heart=s>=72&&s<82,lead=(s>=24&&s<72)||(s>=96&&s<116);
    if(calm&&bar%2===0)c.forEach(function(n){tone(t0+s,mtof(n-12),4,'sine',.1,900)});
    for(var b=0;b<4;b++){var t=t0+s+b*B;
      if(lull&&b===0)tone(t,mtof(r),1.6,'sine',.25,500);
      if(heart&&(b===0||b===2)){kick(t);kick(t+.2);if(b===0)tone(t,mtof(r-12),1.8,'sine',.5,300)}
      if(beat){kick(t);nz(t+B/2,.05,.12,7000);if(b%2)nz(t,.12,.3,1200);tone(t,mtof(r),.4,'sawtooth',.24,420);tone(t+B/2,mtof(r+(b%2?7:0)),.2,'sawtooth',.18,420)}}
    if(beat)[0,1.5].forEach(function(x){c.forEach(function(n){tone(t0+s+x*B,mtof(n),.35,'square',.05,2500)})});
    if(lead)for(var k=0;k<8;k++)tone(t0+s+k*.25,mtof(c[k%3]+12+(k%4===3?12:0)),.22,'sawtooth',.05,3000);
  }
  [72,76,79,84].forEach(function(n,i){tone(t0+72+i*.3,mtof(n+12),.9,'triangle',.12,5000)});
  nz(t0+16,1.6,.5,3000);kick(t0+16);
  var sr=AC.createBufferSource(),f=AC.createBiquadFilter(),g=AC.createGain();sr.buffer=NB;sr.loop=true;f.type='highpass';f.frequency.setValueAtTime(400,t0+111.6);f.frequency.exponentialRampToValueAtTime(7000,t0+115.6);g.gain.setValueAtTime(.001,t0+111.6);g.gain.linearRampToValueAtTime(.3,t0+115.6);g.gain.setValueAtTime(0,t0+115.65);sr.connect(f);f.connect(g);g.connect(M);sr.start(t0+111.6);sr.stop(t0+115.7);
  nz(t0+115.6,1.6,.5,3000);kick(t0+115.6);
  M.gain.setValueAtTime(.8,t0+119.3);M.gain.linearRampToValueAtTime(.05,t0+120.5);
}
var INTRO=[["Rie","Calm on the outside. Plotting on the inside.","Hi! I'm Rie. I come in peace… mostly. 🌺","#ff9a3c","#ff3d81"],["Talisa","She sees everything. She says nothing.","I'm Talisa. I'm just here to observe. 👀","#14b8b0","#5b2a86"],["Kim","Here to win. Heart optional.","Kim. I'm not here to make friends. Okay, maybe one.","#8e2de2","#ff5c9b"],["Damien","Heartbreaker. Allegedly.","Hey, I'm Damien. Don't fall for me… okay, you can.","#3a7bd5","#8e2de2"],["Fefe","One secret could burn the villa down.","I'm Fefe. I have a secret. Ask me later 🤫","#ff5c9b","#5b2a86"],["Soomy","Quiet. Mysterious. Watching.","I'm Soomy. I'm just here to see what happens.","#0a7f86","#3a0a3f"]];
function play5(){
  var st=document.createElement('div');st.id='stage';st.innerHTML="<div id='sc'></div><div class='bug'>● EPISODE 1</div><button class='skip' onclick='skip()'>Skip ▸</button>";document.body.appendChild(st);
  try{AC=new (window.AudioContext||window.webkitAudioContext)();if(AC.state==='suspended')AC.resume();M=AC.createGain();M.gain.value=.8;M.connect(AC.destination);NB=AC.createBuffer(1,AC.sampleRate*2,AC.sampleRate);var d=NB.getChannelData(0);for(var i=0;i<d.length;i++)d[i]=Math.random()*2-1;mus(AC.currentTime+.15)}catch(e){AC=null}
  var S=function(s,f){at(Math.round(s*1000)+150,f)},HB="linear-gradient(#ffb06a,#ff5c9b 55%,#14b8b0 55%)",RB="linear-gradient(160deg,#2b0a2e,#8a0f3a)",PB="linear-gradient(160deg,#0b1a3a,#5b2a86)",H=["Lola","Bree"];
  var seq=function(t0,f,bg,lb,L,dt){L.forEach(function(l,k){S(t0+k*dt,function(){talk(f,bg,lb,l)})})};
  S(0,function(){sc("<div class='sc s1'><div class='sunr'></div><div class='pl sway' style='left:4%'>🌴</div><div class='pl sway' style='right:4%'>🌴</div><div class='sea'></div><div class='caps'><p class='cl'>"+kin("Nine islanders.",.6,.07)+"</p><p class='cl'>"+kin("One villa.",2.4,.07)+"</p><p class='cl pk'>"+kin("One girl everyone wants.",4.2,.06)+"</p></div></div>")});
  seq(7,H,HB,"YOUR HOSTS",[["Lola","Welcome to Lulu Island! 🌴","😍",1.35],["Bree","I'm Bree. And this is my love, Lola 💍","🥰",1.1],["Lola","We'll be your hosts…","😉",1.35],["Bree","Drama? Oh, there will be drama.","😈",1.1]],2.25);
  S(16,function(){ttl("Episode 1 · The Arrival");spk("Lulu Island. With your hosts, Lola and Bree.",1.2)});
  INTRO.slice(0,5).forEach(function(x,i){S(24+i*6,function(){meet(x[0],x[1],x[2],x[3],x[4])})});
  seq(54,["Puddy","Faye"],PB,"MEET THE ISLANDERS",[["Puddy","Hi everyone, I'm Puddy. And this is Faye.","😊"],["Faye","We're… talking. Don't make it weird.","😏"],["Puddy","It's not weird!","😳"]],2.4);
  S(61.2,function(){var x=INTRO[5];meet(x[0],x[1],x[2],x[3],x[4])});
  seq(67.2,H,HB,"YOUR HOSTS",[["Lola","But wait… there's one more islander.","😮",1.35],["Bree","The one everyone has been waiting for…","😏",1.1]],2.4);
  S(72,function(){sc("<div class='sc s2'><div class='zoom'>"+lulu()+"</div><div class='lt'>Lulu 💚 islander</div><div class='lsay' id='ls'></div></div>")});
  [["Hiii everyone~ I'm Lulu! 💕",72.3],["I hope you all brought your A-game 😉",75.6],["Let's have some fun, cuties… 💋",78.9]].forEach(function(x){S(x[1],function(){say(x[0])})});
  seq(82,["Rie","Talisa","Kim","Damien","Fefe"],RB,"THE ISLANDERS REACT",[["Damien","…Okay. Wow.","😳"],["Kim","Hi?? Hello?? Who is that??","😳"],["Rie","She's SO pretty 😍","😍"],["Talisa","Everybody's staring…","👀"],["Fefe","This is going to be a long night.","😬"]],2.4);
  seq(94,["Puddy","Faye"],PB,"MEANWHILE…",[["Puddy","Anyway, as I was saying…","🙂"],["Faye","Mm-hm. Go on.","😊"]],2.4);
  seq(98.8,H,HB,"YOUR HOSTS",[["Lola","Nine islanders. One night.","😏",1.35],["Bree","And everyone wants Lulu.","😍",1.1],["Lola","Well… almost everyone 👀","😂",1.35]],2.4);
  seq(106,H,HB,"YOUR HOSTS",[["Bree","Next time… Lulu picks up the phone.","😱",1.1],["Lola","And one choice changes everything.","😮",1.35]],2.4);
  S(110.8,function(){slam2("Phone calls…","#12041f")});S(112.4,function(){slam2("Secrets…","#7a0f3a")});S(114,function(){slam2("One choice.","#3a0a1f")});
  S(115.6,function(){ttl("Episode 2 · The Phone Calls",1)});
}
function mus2(t0){
  var B=.5,CH=[[57,60,64],[53,57,60],[60,64,67],[55,59,62]],RT=[45,41,48,43];
  for(var bar=0;bar<61;bar++){var s=bar*2,c=CH[bar%4],r=RT[bar%4],calm=s<8||s>=118||(s>=84&&s<98),lull=(s>=8&&s<16)||(s>=84&&s<98),beat=(s>=16&&s<72)||(s>=98&&s<118),heart=s>=72&&s<84,lead=(s>=24&&s<72)||(s>=104&&s<118);
    if(calm&&bar%2===0)c.forEach(function(n){tone(t0+s,mtof(n-12),4,'sine',.1,900)});
    for(var b=0;b<4;b++){var t=t0+s+b*B;
      if(lull&&b===0)tone(t,mtof(r),1.6,'sine',.25,500);
      if(heart&&(b===0||b===2)){kick(t);kick(t+.2);if(b===0)tone(t,mtof(r-12),1.8,'sine',.5,300)}
      if(beat){kick(t);nz(t+B/2,.05,.12,7000);if(b%2)nz(t,.12,.3,1200);tone(t,mtof(r),.4,'sawtooth',.24,420);tone(t+B/2,mtof(r+(b%2?7:0)),.2,'sawtooth',.18,420)}}
    if(beat)[0,1.5].forEach(function(x){c.forEach(function(n){tone(t0+s+x*B,mtof(n),.35,'square',.05,2500)})});
    if(lead)for(var k=0;k<8;k++)tone(t0+s+k*.25,mtof(c[k%3]+12+(k%4===3?12:0)),.22,'sawtooth',.05,3000);
  }
  [72,76,79,84].forEach(function(n,i){tone(t0+83.1+i*.3,mtof(n+12),1.2,'triangle',.12,5000)});
  nz(t0+16,1.6,.5,3000);kick(t0+16);
  var sr=AC.createBufferSource(),f=AC.createBiquadFilter(),g=AC.createGain();sr.buffer=NB;sr.loop=true;f.type='highpass';f.frequency.setValueAtTime(400,t0+114);f.frequency.exponentialRampToValueAtTime(7000,t0+118);g.gain.setValueAtTime(.001,t0+114);g.gain.linearRampToValueAtTime(.3,t0+118);g.gain.setValueAtTime(0,t0+118.05);sr.connect(f);f.connect(g);g.connect(M);sr.start(t0+114);sr.stop(t0+118.1);
  nz(t0+118,1.6,.5,3000);kick(t0+118);
  M.gain.setValueAtTime(.8,t0+121);M.gain.linearRampToValueAtTime(.05,t0+122.2);
}
var CALLS=[["Rie","Hiii Rie~ it's Lulu! 💕 Tell me something about you.","😳","I make a really good mango smoothie. 🥭 Want one?","😊"],["Talisa","Talisa… you've been so quiet. Spill it, babe.","😶","I'm just observing. But I notice you. 👀","😏"],["Kim","Kim! Are you here to win my heart? 💘","😎","I'm here to win. The heart is a bonus.","😏"],["Damien","Damien, I heard you're a heartbreaker 😏","😳","Only if you ask nicely. 😉","😍"],["Fefe","Fefe… I heard you have a secret. 🤫","😳","Maybe. Come and find out.","😏"],["Puddy","Puddy! Wanna chat? 💕","🙂","Hey Lulu! Can I call you back? I'm kind of in the middle of something.","😬"],["Faye","Faye~ wanna get to know each other?","🙂","Aww, thanks, but I'm good. Puddy's waiting for me. 😊","😅"],["Soomy","Soomy… I've been waiting to call you. 💗","😶","…Took you long enough.","😏"]];
function dec(i){var N=["Rie","Talisa","Kim","Damien","Fefe","Puddy","Faye","Soomy"];
  var row=N.map(function(x,j){return "<div class='fz dl"+(j===i?" on":"")+"'>"+face(x)+"</div>"}).join("");
  sc("<div class='sc m' style='background:radial-gradient(circle,#4a0f5a,#0b0212 75%)'><div class='vig'></div><div class='nx'>LULU DECIDES…</div><div class='ph fc'>"+face("Lulu")+"</div><div class='pair rw' style='margin-top:14px'>"+row+"</div><div class='sp'>"+(i<7?kin("Hmm… "+N[i]+"? 🤔",0,.05):kin("It's Soomy. 💘",0,.06))+"</div></div>")}
function play6(){
  var st=document.createElement('div');st.id='stage';st.innerHTML="<div id='sc'></div><div class='bug'>● EPISODE 2</div><button class='skip' onclick='skip()'>Skip ▸</button>";document.body.appendChild(st);
  try{AC=new (window.AudioContext||window.webkitAudioContext)();if(AC.state==='suspended')AC.resume();M=AC.createGain();M.gain.value=.8;M.connect(AC.destination);NB=AC.createBuffer(1,AC.sampleRate*2,AC.sampleRate);var d=NB.getChannelData(0);for(var i=0;i<d.length;i++)d[i]=Math.random()*2-1;mus2(AC.currentTime+.15)}catch(e){AC=null}
  var S=function(s,f){at(Math.round(s*1000)+150,f)},HB="linear-gradient(#ffb06a,#ff5c9b 55%,#14b8b0 55%)",PH="linear-gradient(160deg,#0b1a3a,#3a0a5f)",NT="linear-gradient(#0b1a3a,#1b0a2b)",MB="linear-gradient(#ffd27a,#ff9a6a 60%,#ff5c9b)",PB="linear-gradient(160deg,#0b1a3a,#5b2a86)",H=["Lola","Bree"];
  var seq=function(t0,f,bg,lb,L,dt){L.forEach(function(l,k){S(t0+k*dt,function(){talk(f,bg,lb,l)})})};
  S(0,function(){sc("<div class='sc' style='background:linear-gradient(#05010d,#2a0f4d 60%,#5b2a86)'><div style='position:absolute;left:50%;bottom:36%;width:150px;height:150px;margin-left:-75px;border-radius:50%;background:#fff3cf;box-shadow:0 0 70px #cbb6ff'></div><div class='pl sway' style='left:4%'>🌴</div><div class='pl sway' style='right:4%'>🌴</div><div class='sea'></div><div class='caps'><p class='cl'>"+kin("Night one.",.6,.07)+"</p><p class='cl'>"+kin("One phone.",2.4,.07)+"</p><p class='cl pk'>"+kin("Eight chances.",4.2,.06)+"</p></div></div>")});
  seq(7,H,HB,"YOUR HOSTS",[["Lola","Night one on Lulu Island! 🌙","😍",1.35],["Bree","Tonight, Lulu gets a phone. 📱","😮",1.1],["Lola","She'll call every single islander.","😉",1.35],["Bree","Everyone gets a chance. But she can only pick one.","😈",1.1]],2.25);
  S(16,function(){ttl("Episode 2 · The Phone Calls");spk("Lulu Island. Episode two.",1.2)});
  CALLS.forEach(function(c,i){seq(24+i*6,["Lulu",c[0]],PH,"📞 LULU CALLS "+c[0].toUpperCase(),[["Lulu",c[1],c[2],1.7],[c[0],c[3],c[4]]],3)});
  seq(72,H,HB,"YOUR HOSTS",[["Lola","Eight calls. Eight chances.","😮",1.35],["Bree","Now… who does Lulu choose? 👀","😱",1.1]],2.4);
  for(var i=0;i<7;i++)(function(i){S(76.8+i*.9,function(){dec(i)})})(i);
  S(83.1,function(){dec(7);spk("It's Soomy.",1.7)});
  seq(84,["Soomy","Lulu"],NT,"MIDNIGHT 🌙",[["Soomy","You came…","😍"],["Lulu","I couldn't stop thinking about you. 💗","😳",1.7],["Soomy","So… are we telling anyone?","😏"],["Lulu","Shhh. Nobody can know. Our little secret. 🤫","😉",1.7]],2.4);
  S(93.6,function(){sc("<div class='sc' style='background:#000'><div class='caps' style='top:34%'><p class='cl'>"+kin("A door closes…",.4,.07)+"</p><p class='cl'>"+kin("…and the lights go out. 🌙",2.2,.05)+"</p></div></div>")});
  seq(98,["Rie","Kim","Damien","Lulu","Soomy"],MB,"THE NEXT MORNING ☀️",[["Rie","Okay, who did Lulu pick?? I need to know!","😍"],["Kim","I heard footsteps last night…","🤨"],["Damien","Lulu? Anything to share?","😏"],["Lulu","A lady never tells~ 😉","😍",1.7],["Soomy","…I'm just here for breakfast.","😶"]],2.4);
  seq(110,["Puddy","Faye"],PB,"MEANWHILE…",[["Puddy","Wait… did something happen last night?","🙂"],["Faye","Honestly? I slept great.","😴"]],2.4);
  S(114.8,function(){slam2("Nobody knows…","#12041f")});S(116.4,function(){slam2("…except two.","#7a0f3a")});
  S(118,function(){ttl("Episode 3 · Lulu's Court",1)});
}
var oldFace=face;
function mix(h,t,k){var a=parseInt(h.slice(1),16),b=parseInt(t.slice(1),16),f=function(q){var u=(a>>q)&255,v=(b>>q)&255;return Math.round(u+(v-u)*k)};return "rgb("+f(16)+","+f(8)+","+f(0)+")"}
function st(x,y,k,d){return "<g transform='translate("+x+" "+y+") scale("+k+")'><path class='tw' style='animation-delay:"+d+"s' d='M0-8L2-2L8 0L2 2L0 8L-2 2L-8 0L-2-2Z' fill='#fff6c8'/></g>"}
var GL={Lola:{fl:"#7fb3ff",fr:1},Bree:{fl:"#ff8fb0",fr:1,tat:1},Lulu:{fl:"#ff5c9b",fr:1},Damien:{fl:"#ff9ccf",fr:1,ch:1},Rie:{fl:"#ffd166"},Talisa:{fl:"#ff7a59"},Kim:{fl:"#c084fc"},Puddy:{fl:"#ffb347"},Faye:{fl:"#ff9ccf"},Fefe:{fl:"#ffcc4d",fr:1},Soomy:{fl:"#7fd1ff",fr:1}};
face=function(n){var o=CAST[n],g=GL[n]||{fl:"#ff5c9b"},s=oldFace(n),sk=o.skin,sh=mix(sk,"#8a3a2a",.22),hi=mix(o.hair,"#ffffff",.35),eye=o.eye||"#4a2a12",L={long:200,mid:172,bob:130,wolf:134,pony:122}[o.style],x="",i,pt="";
  s=s.replace("<path d='M40 220C40 172 70 158 100 158C130 158 160 172 160 220Z' fill='"+o.top+"'/>","<path d='M40 220C40 172 70 158 100 158C130 158 160 172 160 220Z' fill='"+sk+"'/><path d='M60 220L68 186Q84 178 100 194Q116 178 132 186L140 220Z' fill='"+o.top+"'/><path d='M68 186Q84 178 100 194Q116 178 132 186' fill='none' stroke='"+mix(o.top,"#000000",.2)+"' stroke-width='2.5'/>");
  [80,120].forEach(function(e){s=s.replace("<circle cx='"+e+"' cy='118' r='4' fill='#1d1208'/>","<circle cx='"+e+"' cy='118' r='8.5' fill='none' stroke='#000' stroke-opacity='.25' stroke-width='1.4'/><circle cx='"+e+"' cy='123' r='4' fill='"+mix(eye,"#ffffff",.55)+"' opacity='.5'/><circle cx='"+e+"' cy='118' r='4' fill='#1d1208'/><circle cx='"+(e+4)+"' cy='123' r='1.6' fill='#fff'/>")});
  x+="<path d='M138 84C150 112 142 140 112 154C136 140 144 114 138 84Z' fill='"+sh+"' opacity='.4'/><path d='M90 146Q100 164 110 146Z' fill='"+sh+"' opacity='.6'/>";
  x+="<path d='M62 54C52 90 60 "+(L-70)+" 50 "+L+"M138 54C148 90 140 "+(L-70)+" 150 "+L+"' stroke='"+hi+"' stroke-width='4' fill='none' stroke-linecap='round' opacity='.5'/><path d='M72 52Q98 38 132 46' stroke='"+hi+"' stroke-width='4' fill='none' stroke-linecap='round' opacity='.6'/><path d='M66 112L60 108M134 112L140 108' stroke='#2a160c' stroke-width='3' stroke-linecap='round'/>";
  if(g.fr)[[66,132],[74,140],[82,134],[118,134],[126,140],[134,132],[98,130],[104,130]].forEach(function(q){x+="<circle cx='"+q[0]+"' cy='"+q[1]+"' r='1.4' fill='#d9926f' opacity='.7'/>"});
  x+="<path d='M92 142Q100 152 108 142Q100 146 92 142Z' fill='#e64b78'/><path d='M97 146Q100 148 103 146' stroke='#ffd9e3' stroke-width='1.6' fill='none' stroke-linecap='round'/>";
  for(i=0;i<360;i+=72)pt+="<ellipse cy='-7' rx='5' ry='8' fill='"+g.fl+"' transform='rotate("+i+")'/>";
  x+="<g transform='translate("+(o.style==="pony"?58:142)+" 48)'>"+pt+"<circle r='3.5' fill='#ffcc4d'/></g><circle cx='57' cy='142' r='4' fill='none' stroke='#ffcc4d' stroke-width='2.2'/><circle cx='143' cy='142' r='4' fill='none' stroke='#ffcc4d' stroke-width='2.2'/>";
  if(g.ch)x+="<path d='M86 150Q100 162 114 150' stroke='#ff9ccf' stroke-width='5' fill='none' stroke-linecap='round'/><circle cx='100' cy='159' r='3.5' fill='#ffcc4d'/><path d='M100 162Q96 176 108 190' stroke='#ffcc4d' stroke-width='1.5' fill='none'/>";
  if(g.tat)x+="<path d='M48 200C54 190 64 192 66 200S58 212 52 206M58 214Q64 208 70 214' stroke='#3b2a2a' stroke-width='1.8' fill='none' opacity='.6'/>";
  x+=st(28,44,1,0)+st(176,96,.8,.6)+st(24,130,.7,1.1);
  return s.replace("</svg>",x+"</svg>")};
function musG(t0,fl,r0,r1,end){
  var B=.5,CH=[[57,60,64],[53,57,60],[60,64,67],[55,59,62]],RT=[45,41,48,43];
  for(var bar=0;bar<end/2;bar++){var s=bar*2,c=CH[bar%4],r=RT[bar%4],F=fl(s);
    if(F.calm&&bar%2===0)c.forEach(function(n){tone(t0+s,mtof(n-12),4,'sine',.1,900)});
    for(var b=0;b<4;b++){var t=t0+s+b*B;
      if(F.lull&&b===0)tone(t,mtof(r),1.6,'sine',.25,500);
      if(F.heart&&(b===0||b===2)){kick(t);kick(t+.2);if(b===0)tone(t,mtof(r-12),1.8,'sine',.5,300)}
      if(F.beat){kick(t);nz(t+B/2,.05,.12,7000);if(b%2)nz(t,.12,.3,1200);tone(t,mtof(r),.4,'sawtooth',.24,420);tone(t+B/2,mtof(r+(b%2?7:0)),.2,'sawtooth',.18,420)}}
    if(F.beat)[0,1.5].forEach(function(x){c.forEach(function(n){tone(t0+s+x*B,mtof(n),.35,'square',.05,2500)})});
    if(F.lead)for(var k=0;k<8;k++)tone(t0+s+k*.25,mtof(c[k%3]+12+(k%4===3?12:0)),.22,'sawtooth',.05,3000);
  }
  nz(t0+16,1.6,.5,3000);kick(t0+16);
  var sr=AC.createBufferSource(),f=AC.createBiquadFilter(),g=AC.createGain();sr.buffer=NB;sr.loop=true;f.type='highpass';f.frequency.setValueAtTime(400,t0+r0);f.frequency.exponentialRampToValueAtTime(7000,t0+r1);g.gain.setValueAtTime(.001,t0+r0);g.gain.linearRampToValueAtTime(.3,t0+r1);g.gain.setValueAtTime(0,t0+r1+.05);sr.connect(f);f.connect(g);g.connect(M);sr.start(t0+r0);sr.stop(t0+r1+.1);
  nz(t0+r1,1.6,.5,3000);kick(t0+r1);
  M.gain.setValueAtTime(.8,t0+end-1.2);M.gain.linearRampToValueAtTime(.05,t0+end+.2);
}
function role(n,tag,line,a,b){sc("<div class='sc m' style='background:linear-gradient(160deg,"+a+","+b+")'><div class='vig'></div><div class='nx'>CHOOSE YOUR ROLE</div><div class='ph fc'>"+face(n)+"</div><div class='nm'>"+kin(n,.2,.08)+"</div><div class='sb'>"+tag+"</div><div class='sp'>"+kin(line,.7,.035)+"</div></div>")}
var ROLES=[["Rie","🎀 Obsessed bestie","I've known her five minutes. We're soulmates.","#ff9a3c","#ff3d81"],["Talisa","🕵️ Secret hater","Hater? Me? …Maybe.","#14b8b0","#5b2a86"],["Kim","👑 Fake queen","Queen of what? Of winning.","#8e2de2","#ff5c9b"],["Damien","💋 Jealous ex-bestie","We're not talking about it.","#3a7bd5","#8e2de2"],["Fefe","🤡 Desperate fan","I'd do anything. ANYTHING.","#ff5c9b","#5b2a86"],["Puddy","🤡 Desperate fan","Faye picked this for me.","#ffb347","#ff5c9b"],["Faye","💕 Loyal bodyguard","I'm protecting Puddy. Obviously.","#14b8b0","#ffcc4d"],["Soomy","💕 Loyal bodyguard","I'll guard her with my life.","#0a7f86","#3a0a3f"]];
var PITCH=[["Rie","I'd carry Lulu's bags, her drinks… her whole life. 🎀","😍","Aww, Rie. You're my emotional support mango. 🥭","😳"],["Talisa","Obsessed? She's fine. I guess. 🙄","🤨","Girl, you're staring at me right now. 😏","😳"],["Kim","I'm not obsessed. I'm here for the crown. 👑","😎","Bold. I like bold. Don't touch the crown though. 😘","😏"],["Damien","I was her bestie first. FIRST. 💋","😤","Damien, it's been five minutes, babe. 😂","😅"],["Fefe","I would do ANYTHING for Lulu. Ask me! 🤡","🥺","Aww, hold my drink? 💅","😍"],["Soomy","I'm obsessed. Quietly. Very quietly. 😶","😶","Soomy… behave. 😉","😳"]];
function play7(){
  var st2=document.createElement('div');st2.id='stage';st2.innerHTML="<div id='sc'></div><div class='bug'>● EPISODE 3</div><button class='skip' onclick='skip()'>Skip ▸</button>";document.body.appendChild(st2);
  try{AC=new (window.AudioContext||window.webkitAudioContext)();if(AC.state==='suspended')AC.resume();M=AC.createGain();M.gain.value=.8;M.connect(AC.destination);NB=AC.createBuffer(1,AC.sampleRate*2,AC.sampleRate);var d=NB.getChannelData(0);for(var i=0;i<d.length;i++)d[i]=Math.random()*2-1;musG(AC.currentTime+.15,function(s){return{calm:s<8||s>=114,lull:s>=8&&s<16,beat:(s>=16&&s<94)||(s>=108&&s<114),heart:s>=94&&s<108,lead:s>=24&&s<94}},109.4,113.4,120)}catch(e){AC=null}
  var S=function(s,f){at(Math.round(s*1000)+150,f)},HB="linear-gradient(#ffb06a,#ff5c9b 55%,#14b8b0 55%)",PH="linear-gradient(160deg,#2b0a2e,#7a0f5a)",PB="linear-gradient(160deg,#0b1a3a,#5b2a86)",RB="linear-gradient(160deg,#2b0a2e,#8a0f3a)",H=["Lola","Bree"];
  var seq=function(t0,f,bg,lb,L,dt){L.forEach(function(l,k){S(t0+k*dt,function(){talk(f,bg,lb,l)})})};
  S(0,function(){sc("<div class='sc' style='background:linear-gradient(#12041f,#5b2a86 55%,#ff9a6a)'><div class='pl sway' style='left:4%'>🌴</div><div class='pl sway' style='right:4%'>🌴</div><div class='sea'></div><div class='caps'><p class='cl'>"+kin("Last time on Lulu Island…",.5,.06)+"</p><p class='cl'>"+kin("Lulu made her choice.",2.8,.07)+"</p><p class='cl pk'>"+kin("Nobody knows… except two.",4.8,.06)+"</p></div></div>")});
  seq(8,H,HB,"YOUR HOSTS",[["Lola","Good morning, islanders! ☀️","😍",1.35],["Bree","I hope you all slept well…","😏",1.1],["Lola","Because today is a challenge.","😮",1.35],["Bree","Welcome to Lulu's Court. 👑","😈",1.1]],2);
  S(16,function(){ttl("Episode 3 · Lulu's Court");spk("Lulu Island. Episode three.",1.2)});
  seq(24,H,HB,"LULU'S COURT 👑",[["Lola","Lulu is the queen of this island. 👑","😍",1.35],["Bree","Everyone picks a role.","🤩",1.1],["Lola","Bestie. Fan. Rival. Hater. Bodyguard.","👀",1.35],["Bree","Choose wisely. Everyone is replaceable. 💀","😱",1.1]],2.4);
  ROLES.forEach(function(x,i){S(33.6+i*2.4,function(){role(x[0],x[1],x[2],x[3],x[4])})});
  seq(52.8,H,HB,"FIRST CHALLENGE",[["Bree","First challenge: why are you obsessed with Lulu?","😳",1.1],["Lola","You have sixty seconds. No boring answers.","😬",1.35],["Bree","The audience votes for the most iconic.","🤩",1.1]],2.4);
  PITCH.forEach(function(p,i){seq(60+i*4.8,[p[0],"Lulu"],PH,"PITCH TO THE QUEEN 👑",[[p[0],p[1],p[2]],["Lulu",p[3],p[4],1.7]],2.4)});
  seq(88.8,["Puddy","Faye"],PB,"PITCH TO THE QUEEN 👑",[["Puddy","Honestly? We're only here for each other. 😊","🙂"],["Faye","Lulu who? 😌","😏"]],2.4);
  seq(93.6,H,HB,"PLOT TWIST 💀",[["Lola","Time's up! Votes are in… but first!","😮",1.35],["Bree","A plot twist. 💀","😱",1.1],["Lola","Someone has been running a fake Lulu fan account.","😳",1.35]],2.4);
  seq(100.8,["Rie","Talisa","Kim","Damien","Fefe"],RB,"THE ISLANDERS REACT",[["Kim","WHAT. Who would do that?!","😱"],["Talisa","…Not me. Obviously. 👀","🤨"]],2.4);
  seq(105.6,["Lulu","Soomy"],PH,"THE QUEEN SPEAKS 👑",[["Lulu","Ooh, messy. I love it. 😏","😶",1.7]],2.4);
  S(108,function(){slam2("Who is the fake fan?","#12041f")});S(109.8,function(){slam2("Who gets replaced?","#7a0f3a")});S(111.6,function(){slam2("Next time…","#3a0a1f")});
  S(113.4,function(){ttl("Episode 4 · The Fake Fan",1)});
}
intro();
</script>
</body>
</html>
