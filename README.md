 <!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8"><meta name="viewport" content="width=device-width,initial-scale=1">
<title>MODS STYLE - Adquirir Productos</title>
<style>
body{margin:0;background:#050505;color:#fff;font-family:Arial;overflow-x:hidden}
canvas{position:fixed;top:0;left:0;z-index:-1}
.wrap{max-width:460px;margin:auto;padding:15px;position:relative;z-index:1}
.head{border:1.5px solid #D4AF37;border-radius:20px;padding:12px 20px;display:flex;justify-content:space-between;align-items:center;background:rgba(0,0,0,0.7);box-shadow:0 0 20px rgba(212,175,55,.3)}
h2{color:#E8C874;text-align:center;font-size:32px;margin:25px 0 5px}
.pchoose{text-align:center;color:#aaa;font-size:14px;margin-bottom:20px}
.cards{display:flex;gap:12px}
.card{flex:1;border:2px solid #D4AF37;border-radius:18px;padding:18px;background:rgba(15,15,15,0.9);box-shadow:0 0 15px rgba(212,175,55,.2);cursor:pointer;transition:.3s}
.card.active{border-color:#F3BA2F;box-shadow:0 0 25px #F3BA2F;transform:scale(1.03)}
.price{font-size:28px;color:#E8C874;font-weight:bold}
.feat{font-size:12px;margin:6px 0;color:#ccc}
.btnsel{background:linear-gradient(#F9E8A0,#D4AF37);border:none;padding:10px;border-radius:20px;width:100%;font-weight:bold;margin-top:12px;cursor:pointer}
.paygrid{display:flex;gap:10px;justify-content:space-between;margin:20px 0;flex-wrap:wrap}
.paybtn{width:18%;border:1.5px solid #D4AF37;border-radius:14px;padding:10px 2px;text-align:center;background:rgba(20,20,20,.8);text-decoration:none;color:#fff;font-size:11px}
.paybtn img{width:32px;display:block;margin:0 auto 5px}
.qrbox{border:2px solid #F3BA2F;border-radius:16px;padding:15px;text-align:center;background:rgba(0,0,0,.6)}
.addr{color:#F3BA2F;background:#222;padding:10px;border-radius:8px;word-break:break-all;font-size:13px;margin:10px 0}
.upload{border:2px dashed #D4AF37;border-radius:16px;padding:22px;text-align:center;background:rgba(212,175,55,.05);margin-top:20px}
</style>
</head>
<body>
<canvas id="bg"></canvas>
<div class="wrap">
<div class="head"><span style="color:#D4AF37;font-weight:bold;letter-spacing:3px">◆ MODS STYLE</span><span>🔍 👤 🛒</span></div>

<h2>Adquirir Productos</h2>
<p class="pchoose">Elige tu plataforma y tu precio. Cada producto incluye instalación, soporte 24/7 y actualizaciones. Selecciona Android o iOS para ver el precio final.</p>

<div class="cards">
<div class="card active" id="android" onclick="sel('android')">
<div>🤖 <b>Android</b></div>
<div class="price">$9.99 / mes</div>
<div class="feat">✓ Acceso completo</div>
<div class="feat">✓ Actualizaciones automáticas</div>
<div class="feat">✓ Soporte 24/7</div>
<button class="btnsel">Seleccionar</button>
</div>
<div class="card" id="ios" onclick="sel('ios')">
<div>🍎 <b>iOS</b></div>
<div class="price">$12.99 / mes</div>
<div class="feat">✓ Integración iCloud</div>
<div class="feat">✓ Rendimiento optimizado</div>
<div class="feat">✓ Soporte prioritario</div>
<button class="btnsel" style="background:transparent;border:1.5px solid #D4AF37;color:#D4AF37">Seleccionar</button>
</div>
</div>

<h3 style="text-align:center;color:#D4AF37;margin-top:25px">Método de Pago</h3>
<div class="paygrid">
<a class="paybtn" href="https://t.me/moodsstylee" target="_blank"><img src="https://cdn-icons-png.flaticon.com/512/2111/2111646.png">Telegram</a>
<a class="paybtn" href="https://discord.gg/HkhsjqpY3" target="_blank"><img src="https://cdn-icons-png.flaticon.com/512/5968/5968756.png">Discord</a>
<a class="paybtn" href="https://www.paypal.me/roberto1985702" target="_blank"><img src="https://cdn-icons-png.flaticon.com/512/174/174861.png">PayPal</a>
<a class="paybtn" href="#qr"><img src="https://cdn-icons-png.flaticon.com/512/6001/6001368.png">Binance</a>
<a class="paybtn" href="#qr"><img src="https://cryptologos.cc/logos/tron-trx-logo.png?v=026" style="background:#fff;border-radius:50%;padding:2px">TRX</a>
</div>

<div class="qrbox" id="qr">
<h4 style="margin:0;color:#F3BA2F">Binance — TRX TRC20 Deposit</h4>
<p style="font-size:11px;color:#888">Red: Tron (TRC20)</p>
<div class="addr">TB1335NgAykxyiY1au5jmjn8tDdLnikFxu</div>
<img src="qr.jpg" style="width:190px;background:#fff;padding:8px;border-radius:12px" onerror="this.src='https://api.qrserver.com/v1/create-qr-code/?size=200x200&data=TB1335NgAykxyiY1au5jmjn8tDdLnikFxu'">
<p style="font-size:10px;color:#666">Enviar solo TRX en red TRC20</p>
</div>

<div class="upload">
<div style="font-size:30px">☁️</div>
<b style="color:#E8C874">Arrastra o súbelo aquí</b>
<p style="font-size:12px;color:#aaa">Formatos:.zip,.apk,.ipa — Máx. 100MB</p>
<input type="file" id="f" style="display:none">
<label for="f" style="background:linear-gradient(#F9E8A0,#D4AF37);color:#000;padding:12px 22px;border-radius:25px;font-weight:bold;cursor:pointer">⬆️ Subir archivo</label>
<p id="fn" style="color:#D4AF37;font-size:13px"></p>
</div>

<p style="text-align:center;font-size:10px;color:#555;margin-top:20px">MODS STYLE • Compra segura • Transacción encriptada</p>
</div>

<script>
function sel(p){document.querySelectorAll('.card').forEach(c=>c.classList.remove('active'));document.getElementById(p).classList.add('active');}
const c=document.getElementById('bg'),x=c.getContext('2d');let w,h,a=[];
function R(){w=c.width=innerWidth;h=c.height=innerHeight}R();onresize=R;
for(let i=0;i<90;i++)a.push({x:Math.random()*w,y:Math.random()*h,r:Math.random()*2.5+0.5,s:Math.random()*1.2+0.3});
(function L(){x.clearRect(0,0,w,h);x.fillStyle='#D4AF37';a.forEach(o=>{o.y-=o.s;if(o.y<0)o.y=h;x.beginPath();x.arc(o.x,o.y,o.r,0,7);x.fill()});requestAnimationFrame(L)})();
document.getElementById('f').onchange=e=>{let f=e.target.files[0];if(f)document.getElementById('fn').textContent='✅ '+f.name}
</script>
</body>
</html>
