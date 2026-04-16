<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Actividad 2 — Simulador Dinámico del Banco Central</title>

<style>
:root {
  --primary:#1e3a5f;
  --accent:#c0392b;
  --success:#27ae60;
  --warning:#f39c12;
  --info:#2980b9;
  --bg:#f4f6f9;
  --card:#ffffff;
  --border:#dce3ea;
  --text:#2c3e50;
  --muted:#7f8c8d;
}

body{
  font-family:'Segoe UI',system-ui;
  background:var(--bg);
  margin:0;
  padding:20px;
}

.container{max-width:1000px;margin:auto;}

header{
  background:var(--primary);
  color:white;
  padding:28px;
  border-radius:12px;
  margin-bottom:20px;
}

.intro{
  background:white;
  padding:20px;
  border-radius:10px;
  margin-bottom:20px;
  border-left:4px solid var(--accent);
}

.grid{
  display:grid;
  grid-template-columns:1fr;
  gap:20px;
}

.panel{
  background:white;
  padding:20px;
  border-radius:10px;
  border:1px solid var(--border);
}

.state-row{
  display:flex;
  justify-content:space-between;
  padding:10px 0;
  border-bottom:1px dashed #eaeef3;
}

.state-value.high{color:var(--accent);}
.state-value.low{color:var(--info);}
.state-value.ok{color:var(--success);}

.decision-panel{
  background:#fff8e1;
  border:2px solid var(--warning);
  padding:20px;
  border-radius:10px;
  margin:20px 0;
}

button.primary{
  background:var(--primary);
  color:white;
  padding:10px 20px;
  border:none;
  border-radius:8px;
  cursor:pointer;
}

.chart-container, .log{
  background:white;
  padding:20px;
  border-radius:10px;
  border:1px solid var(--border);
  margin-bottom:20px;
}

.final-panel{
  display:none;
  background:#1e3a5f;
  color:white;
  padding:20px;
  border-radius:10px;
}

.final-panel.show{display:block;}
</style>
</head>

<body>

<div class="container">

<header>
<h1>🏛️ Simulador Dinámico del Banco Central</h1>
<p>Eres el Gobernador. Tomas decisiones de tasa y observas la economía.</p>
</header>

<div class="intro">
<p><strong>Contexto:</strong> Banco central de Andina. Meta inflación 3%, r* = 2%.</p>
<p>Cada trimestre decides la tasa de interés observando inflación y brecha.</p>
</div>

<div class="grid">
<div class="panel">
<h3>Estado actual — Trimestre <span id="quarter">1</span>/8</h3>

<div class="state-row">
<span>Inflación</span>
<span id="pi-now"></span>
</div>

<div class="state-row">
<span>Brecha producto</span>
<span id="gap-now"></span>
</div>

<div class="state-row">
<span>Tasa previa</span>
<span id="prev-rate"></span>
</div>

<div id="context-note"></div>
</div>
</div>

<div class="decision-panel">
<h3>Tu decisión</h3>
<input type="number" id="rate-input" placeholder="5.50">
<button class="primary" id="submit-rate">Fijar tasa</button>
</div>

<div class="chart-container">
<h3>Trayectoria</h3>
<svg id="chart" viewBox="0 0 800 300"></svg>
</div>

<div class="log">
<h3>Bitácora</h3>
<div id="log-entries"></div>
</div>

<div class="final-panel" id="final-panel">
<h2>Resultados</h2>
<p id="final-text"></p>
</div>

</div>

<script>
const PI_TARGET=3;
const R_STAR=2;
const TOTAL=8;

let state={
q:0,
pi:4.5,
gap:2,
prev:null,
history:[]
};

function taylor(pi,gap){
return R_STAR+pi+0.5*(pi-PI_TARGET)+0.5*gap;
}

function evolve(rate){
let newGap=0.7*state.gap-0.4*(rate-5);
let newPi=0.6*state.pi+0.4*PI_TARGET+0.3*newGap;
return {pi:newPi,gap:newGap};
}

function updateUI(){
document.getElementById("quarter").textContent=state.q+1;
document.getElementById("pi-now").textContent=state.pi.toFixed(2)+"%";
document.getElementById("gap-now").textContent=state.gap.toFixed(2)+"%";
document.getElementById("prev-rate").textContent=state.prev?state.prev+"%":"—";
}

function log(text){
let div=document.createElement("div");
div.textContent=text;
document.getElementById("log-entries").prepend(div);
}

function submit(){
let val=parseFloat(document.getElementById("rate-input").value);
if(isNaN(val))return;

let t=taylor(state.pi,state.gap);

let next=evolve(val);

log("T"+(state.q+1)+" | Tu tasa:"+val+" | Taylor:"+t.toFixed(2));

state.history.push(val);

state.pi=next.pi;
state.gap=next.gap;
state.prev=val;
state.q++;

if(state.q>=TOTAL){
finish();
return;
}

updateUI();
}

function finish(){
document.getElementById("final-panel").classList.add("show");
document.getElementById("final-text").textContent="Simulación completada.";
}

document.getElementById("submit-rate").onclick=submit;

updateUI();
</script>

</body>
</html>
