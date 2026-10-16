# Regalo-navide-o-
REGALOS NAVIDEÑOS RD — Página de ayuda y solidaridad en República Dominicana.
<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>REGALOS NAVIDEÑOS RD 🎄</title>
<style>
*{box-sizing:border-box}
body{margin:0;font-family:Arial,sans-serif;background:#f3f7f1;color:#26352b}
header{background:linear-gradient(135deg,#064b2d,#11834a);color:white;text-align:center;padding:30px 15px}
header h1{font-size:clamp(25px,6vw,38px);margin:10px 0}
header p{line-height:1.6}
nav{background:#b51f32;text-align:center;padding:14px 5px}
nav a{color:white;text-decoration:none;font-weight:bold;margin:8px}
.hero{text-align:center;padding:35px 18px;background:#e4f3e4}
.hero h2{color:#075b36;font-size:28px}
section{padding:30px 16px;max-width:950px;margin:auto}
h2{text-align:center;color:#087642}
.btn{display:inline-block;background:#b51f32;color:white;padding:13px 20px;border:0;border-radius:9px;text-decoration:none;font-weight:bold;cursor:pointer}
.notice{background:#fff2d4;padding:15px;border-radius:10px;line-height:1.6}
.wheel-area{text-align:center;background:white;padding:22px 12px;border-radius:18px;box-shadow:0 4px 18px #0001}
.wheel-wrap{position:relative;width:min(310px,85vw);margin:25px auto}
#arrow{position:absolute;z-index:2;top:-13px;left:calc(50% - 15px);width:0;height:0;border-left:15px solid transparent;border-right:15px solid transparent;border-top:30px solid #b51f32}
canvas{width:100%;height:auto;border-radius:50%;display:block}
#spin{margin:12px auto;font-size:17px}
#result{font-size:20px;font-weight:bold;color:#087642;min-height:30px;margin:15px 0}
.cards{display:grid;grid-template-columns:repeat(auto-fit,minmax(210px,1fr));gap:16px}
.card{background:white;padding:20px;border-radius:13px;text-align:center;box-shadow:0 3px 12px #0001}
.emoji{font-size:42px}
.card h3{color:#b51f32}
footer{background:#064b2d;color:white;text-align:center;padding:25px 15px;line-height:1.8}
small{line-height:1.6}
</style>
</head>
<body>
<header>
<div style="font-size:42px">🎄 🎁 🇩🇴</div>
<h1>REGALOS NAVIDEÑOS RD</h1>
<p>Compartiendo alegría, esperanza y solidaridad esta Navidad.</p>
</header>

<nav>
<a href="#inicio">Inicio</a>
<a href="#ruleta">Ruleta</a>
<a href="#premios">Premios</a>
<a href="#contacto">Contacto</a>
</nav>

<div class="hero" id="inicio">
<h2>✨ ¡La magia de la Navidad! ✨</h2>
<p>Descubre nuestra ruleta navideña de entretenimiento y conoce los premios de demostración.</p>
<a class="btn" href="#ruleta">🎡 Jugar a la ruleta</a>
</div>

<section id="ruleta">
<h2>🎡 Ruleta navideña</h2>
<div class="wheel-area">
<p>¡Pulsa el botón y descubre un premio de demostración!</p>
<p><strong>Modo de prueba:</strong> los resultados son ficticios y no representan premios reales.</p>
<div class="wheel-wrap">
<div id="arrow"></div>
<canvas id="wheel" width="600" height="600"></canvas>
</div>
<button class="btn" id="spin">🎁 GIRAR RULETA</button>
<div id="result" aria-live="polite">¡Mucha diversión!</div>
<p id="explain" class="notice" style="display:none"></p>
</div>
</section>

<section id="premios">
<h2>🎁 Premios ilustrativos</h2>
<div class="cards">
<div class="card"><div class="emoji">💵</div><h3>RD$10,000</h3><p>Premio monetario ficticio para la demostración.</p></div>
<div class="card"><div class="emoji">🏍️</div><h3>Un motor</h3><p>Premio ilustrativo, no disponible para reclamar.</p></div>
<div class="card"><div class="emoji">🧺</div><h3>Una lavadora</h3><p>Premio ilustrativo de la ruleta.</p></div>
<div class="card"><div class="emoji">📺</div><h3>Smart TV</h3><p>Premio ilustrativo de la ruleta.</p></div>
<div class="card"><div class="emoji">📱</div><h3>Teléfono</h3><p>Premio ilustrativo de la ruleta.</p></div>
<div class="card"><div class="emoji">🎄</div><h3>Regalo sorpresa</h3><p>Una opción adicional de entretenimiento.</p></div>
</div>
</section>

<section>
<h2>❤️ Nuestra misión solidaria</h2>
<div class="notice">
<p>Queremos promover la ayuda comunitaria, el respeto a las personas mayores y la solidaridad con las familias dominicanas.</p>
<p>Esta página es un proyecto independiente. No afirmamos tener patrocinio de bancos, instituciones públicas ni empresas sin autorización.</p>
</div>
</section>

<section id="contacto">
<h2>📞 Contacto</h2>
<div class="card">
<p>Para información sobre el proyecto:</p>
<p><strong>Teléfono: 849 398 9042</strong></p>
<p>Este contacto es informativo; no implica que existan premios reales disponibles.</p>
<a class="btn" href="https://wa.me/18493989042">Consultar por WhatsApp</a>
</div>
</section>

<footer>
<div style="font-size:32px">🎄 🎁 🇩🇴</div>
<strong>REGALOS NAVIDEÑOS RD</strong>
<p>La solidaridad ilumina la Navidad.</p>
<small>Ruleta de demostración. Los premios mostrados son ficticios y no se pueden reclamar.</small>
</footer>

<script>
const prizes=[
"RD$10,000 (ficticio)",
"Un motor (ficticio)",
"Una lavadora (ficticia)",
"Smart TV (ficticio)",
"Teléfono (ficticio)",
"Regalo sorpresa (ficticio)"
];
const colors=["#c62839","#087642","#e5b93f","#2864a6","#853f91","#e77727"];
const canvas=document.getElementById("wheel");
const ctx=canvas.getContext("2d");
const cx=300,cy=300,r=280;
let rotation=0,busy=false;

function drawWheel(){
 ctx.clearRect(0,0,600,600);
 const arc=2*Math.PI/prizes.length;
 prizes.forEach((prize,i)=>{
   const start=rotation+i*arc-Math.PI/2;
   const end=start+arc;
   ctx.beginPath();
   ctx.moveTo(cx,cy);
   ctx.arc(cx,cy,r,start,end);
   ctx.closePath();
   ctx.fillStyle=colors[i];
   ctx.fill();
   ctx.strokeStyle="#fff";
   ctx.lineWidth=4;
   ctx.stroke();
   ctx.save();
   ctx.translate(cx,cy);
   ctx.rotate(start+arc/2);
   ctx.textAlign="right";
   ctx.fillStyle="#fff";
   ctx.font="bold 22px Arial";
   ctx.fillText(prize, r-17, 8, 210);
   ctx.restore();
 });
 ctx.beginPath();
 ctx.arc(cx,cy,43,0,Math.PI*2);
 ctx.fillStyle="#fff";
 ctx.fill();
 ctx.strokeStyle="#e5b93f";
 ctx.lineWidth=7;
 ctx.stroke();
 ctx.fillStyle="#075b36";
 ctx.textAlign="center";
 ctx.font="bold 22px Arial";
 ctx.fillText("RD",cx,cy+8);
}
drawWheel();

document.getElementById("spin").addEventListener("click",()=>{
 if(busy)return;
 busy=true;
 document.getElementById("spin").disabled=true;
 document.getElementById("result").textContent="La ruleta está girando…";
 document.getElementById("explain").style.display="none";
 const start=rotation;
 const extra=(5+Math.random()*4)*2*Math.PI;
 const duration=3500;
 const began=performance.now();
 function animate(now){
   const t=Math.min((now-began)/duration,1);
   const eased=1-Math.pow(1-t,4);
   rotation=start+extra*eased;
   drawWheel();
   if(t<1){requestAnimationFrame(animate);return;}
   busy=false;
   document.getElementById("spin").disabled=false;
   const index=Math.floor(Math.random()*prizes.length);
   document.getElementById("result").textContent="Resultado de demostración: "+prizes[index];
   const explain=document.getElementById("explain");
   explain.textContent="Este resultado es únicamente una simulación de entretenimiento. No has ganado un premio real y no existe una recompensa que reclamar. No envíes dinero ni datos bancarios para participar.";
   explain.style.display="block";
 }
 requestAnimationFrame(animate);
});
</script>
</body>
</html>
