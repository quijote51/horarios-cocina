[e.html](https://github.com/user-attachments/files/34425500/e.html)
# Horarios de cocina.
[index.html](https://github.com/user-attachments/files/34425504/index.html)<!doctype html>
<html lang="es"><head><meta charset="utf-8"><meta name="viewport" content="width=device-width,initial-scale=1,viewport-fit=cover">
<meta name="robots" content="noindex"><meta name="theme-color" content="#0f6e56">
<title>Horarios de Cocina</title>
<link rel="preconnect" href="https://fonts.googleapis.com"><link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Bricolage+Grotesque:wght@600;700&family=Instrument+Sans:wght@400;500;600&display=swap" rel="stylesheet">
<style>
:root{--bg:#f5f6f2;--surface:#fff;--fg:#17231f;--muted:#5d6b65;--line:#dfe4dd;--accent:#0f6e56;--accent-fg:#fff;
--work-bg:#e1f5ee;--work-fg:#085041;--jefe-bg:#e6f1fb;--jefe-fg:#0c447c;--libre-bg:#faeeda;--libre-fg:#633806;--vac-bg:#fcebeb;--vac-fg:#791f1f;--baja-bg:#fbeaf0;--baja-fg:#72243e;--extra-bg:#eeedfe;--extra-fg:#3c3489;
--ok-bg:#e1f5ee;--ok-fg:#085041;--warn-bg:#faeeda;--warn-fg:#633806;--bad-bg:#fcebeb;--bad-fg:#791f1f;--good:#5dcaa5;--attn:#ef9f27;--crit:#e24b4a;
--font-body:'Instrument Sans',system-ui,-apple-system,'Segoe UI',sans-serif;--font-display:'Bricolage Grotesque','Instrument Sans',system-ui,sans-serif}
@media(prefers-color-scheme:dark){:root{--bg:#101714;--surface:#17211d;--fg:#e8efe9;--muted:#9aa8a1;--line:#2a3832;--accent:#3ec59d;--accent-fg:#06231b;
--work-bg:#123a30;--work-fg:#9be7cf;--jefe-bg:#10304f;--jefe-fg:#9fcdf5;--libre-bg:#44300f;--libre-fg:#f3c985;--vac-bg:#471c1c;--vac-fg:#f4aaaa;--baja-bg:#47202f;--baja-fg:#f2b0c6;--extra-bg:#2b2860;--extra-fg:#c3bff6;
--ok-bg:#123a30;--ok-fg:#9be7cf;--warn-bg:#44300f;--warn-fg:#f3c985;--bad-bg:#471c1c;--bad-fg:#f4aaaa;color-scheme:dark}}
*{box-sizing:border-box}
body{margin:0;background:var(--bg);color:var(--fg);font:14px/1.45 var(--font-body);padding:max(16px,env(safe-area-inset-top)) max(16px,env(safe-area-inset-right)) 40px max(16px,env(safe-area-inset-left))}
.wrap{max-width:1100px;margin:0 auto;display:flex;flex-direction:column;gap:14px}
header{display:flex;flex-wrap:wrap;align-items:flex-end;justify-content:space-between;gap:8px 16px}
h1{font-family:var(--font-display);font-size:1.6rem;line-height:1.1;margin:0}
.sub{color:var(--muted);font-size:.85rem;margin-top:2px}
.reloj{font-variant-numeric:tabular-nums;text-align:right;font-size:.85rem;color:var(--muted)}
.reloj b{display:block;font-family:var(--font-display);font-size:1.5rem;color:var(--fg);line-height:1}
nav{display:flex;gap:4px;overflow-x:auto;border-bottom:1px solid var(--line)}
nav button{flex:none;background:none;border:0;border-bottom:2px solid transparent;color:var(--muted);font:500 .92rem var(--font-body);padding:10px 12px;cursor:pointer;min-height:44px}
nav button[aria-selected="true"]{color:var(--accent);border-bottom-color:var(--accent)}
button:focus-visible,input:focus-visible,select:focus-visible,textarea:focus-visible{outline:2px solid var(--accent);outline-offset:2px}
.bar{display:flex;flex-wrap:wrap;align-items:center;gap:8px}.bar .grow{flex:1}
.btn{font:500 .88rem var(--font-body);background:var(--surface);color:var(--fg);border:1px solid var(--line);border-radius:8px;padding:8px 12px;min-height:40px;cursor:pointer}
.btn:hover{border-color:var(--accent)}.btn.pri{background:var(--accent);color:var(--accent-fg);border-color:var(--accent)}.btn.sm{min-height:32px;padding:4px 9px;font-size:.8rem}
.semana{font-family:var(--font-display);font-weight:600;font-size:1.05rem;min-width:11ch;text-align:center}
.aviso{padding:10px 12px;border-radius:8px;font-size:.88rem}.aviso.warn{background:var(--warn-bg);color:var(--warn-fg)}.aviso.bad{background:var(--bad-bg);color:var(--bad-fg)}.aviso.ok{background:var(--ok-bg);color:var(--ok-fg)}
.aviso ul{margin:4px 0 0;padding-left:1.1rem}
.tabla{overflow-x:auto;border:1px solid var(--line);border-radius:10px;background:var(--surface)}
table{border-collapse:separate;border-spacing:0;width:100%;min-width:760px;font-size:.82rem}
th,td{padding:5px 6px;border-bottom:1px solid var(--line);text-align:center;vertical-align:middle}
thead th{font-weight:600;color:var(--muted);font-size:.76rem;background:var(--surface)}thead th.hoy{color:var(--accent)}
th.nom,td.nom{text-align:left;position:sticky;left:0;background:var(--surface);z-index:1;min-width:104px;border-right:1px solid var(--line)}
td.nom b{display:block;font-weight:600}td.nom small{color:var(--muted);font-size:.72rem}
tr.grp td{background:var(--bg);color:var(--muted);font-size:.7rem;font-weight:600;text-transform:uppercase;letter-spacing:.07em;text-align:left;padding:4px 8px}
.cel{display:flex;flex-direction:column;gap:2px;width:100%;min-height:34px;border:0;border-radius:6px;padding:4px 3px;font:500 .74rem var(--font-body);cursor:pointer;align-items:center;justify-content:center;font-variant-numeric:tabular-nums}
.cel.trab{background:var(--work-bg);color:var(--work-fg)}.cel.jefe{background:var(--jefe-bg);color:var(--jefe-fg)}.cel.libre{background:var(--libre-bg);color:var(--libre-fg)}.cel.vac{background:var(--vac-bg);color:var(--vac-fg)}.cel.baja{background:var(--baja-bg);color:var(--baja-fg)}.cel.extra{background:var(--extra-bg);color:var(--extra-fg)}
.cel.vacio{background:transparent;color:var(--muted);border:1px dashed var(--line)}.cel.sel{outline:2px solid var(--accent)}
td.h{font-variant-numeric:tabular-nums;font-weight:600;min-width:52px}td.h.alta{color:var(--bad-fg)}tr.cob td{font-weight:600;border-bottom:0}
.cobp{display:inline-block;min-width:28px;padding:2px 8px;border-radius:99px}.cobp.ok{background:var(--ok-bg);color:var(--ok-fg)}.cobp.warn{background:var(--warn-bg);color:var(--warn-fg)}.cobp.bad{background:var(--bad-bg);color:var(--bad-fg)}
.editor{background:var(--surface);border:1px solid var(--accent);border-radius:10px;padding:12px;display:flex;flex-direction:column;gap:10px}.editor h3{margin:0;font-size:.95rem}
.chips{display:flex;flex-wrap:wrap;gap:6px}
textarea,input,select{font:inherit;color:var(--fg);background:var(--bg);border:1px solid var(--line);border-radius:8px;padding:8px 10px;min-height:40px;width:100%}
.card{background:var(--surface);border:1px solid var(--line);border-radius:10px;padding:12px 14px}.card h3{margin:0 0 8px;font-family:var(--font-display);font-size:1rem}
.cols{display:grid;grid-template-columns:repeat(auto-fit,minmax(260px,1fr));gap:12px}
.fila{display:flex;align-items:center;justify-content:space-between;gap:10px;padding:8px 0;border-bottom:1px solid var(--line)}.fila:last-child{border-bottom:0}.fila>*{min-width:0}.fila small{color:var(--muted)}
.pill{display:inline-block;padding:2px 9px;border-radius:99px;font-size:.75rem;font-weight:600}
.pill.trab{background:var(--work-bg);color:var(--work-fg)}.pill.libre{background:var(--libre-bg);color:var(--libre-fg)}.pill.vac{background:var(--vac-bg);color:var(--vac-fg)}.pill.baja{background:var(--baja-bg);color:var(--baja-fg)}.pill.extra{background:var(--extra-bg);color:var(--extra-fg)}
.vacio-txt{color:var(--muted);padding:14px 0}
.form{display:grid;grid-template-columns:repeat(auto-fit,minmax(150px,1fr));gap:8px;align-items:end}.form label{display:flex;flex-direction:column;gap:3px;font-size:.78rem;color:var(--muted)}
.dias7{display:grid;grid-template-columns:repeat(auto-fit,minmax(84px,1fr));gap:6px;margin:8px 0}.dias7 label{font-size:.72rem}
.saldo{height:8px;border-radius:99px;background:var(--line);overflow:hidden;margin-top:4px}.saldo i{display:block;height:100%}
.meses{display:grid;grid-template-columns:repeat(12,1fr);gap:2px;margin-top:6px}.meses span{height:14px;border-radius:3px;background:var(--line)}
.meses .v{background:var(--vac-fg)}.meses .i{background:var(--jefe-fg)}.meses .x{background:var(--attn)}.meses .m{background:var(--baja-fg)}
.leyenda{display:flex;gap:10px;flex-wrap:wrap;font-size:.76rem;color:var(--muted)}
.nota-tipo{font-size:.72rem;font-weight:600;text-transform:uppercase;letter-spacing:.06em}.aviso-guardado{font-size:.78rem;color:var(--muted)}
.arow{display:flex;border-bottom:1px solid var(--line)}
.anom{position:sticky;left:0;z-index:2;flex:none;width:116px;background:var(--surface);border-right:1px solid var(--line);padding:4px 8px;display:flex;flex-direction:column;justify-content:center;font-size:.82rem}.anom small{color:var(--muted);font-size:.7rem}
.atrk{position:relative;height:36px;flex:none}.atrk.ah{height:24px}
.atrk.ah span{position:absolute;top:0;height:100%;display:flex;align-items:center;padding-left:4px;font-size:.7rem;font-weight:600;color:var(--muted);text-transform:uppercase;border-left:1px solid var(--line)}
.bar2{position:absolute;top:7px;height:22px;border-radius:5px;color:#fff;font-size:.66rem;font-weight:600;display:flex;align-items:center;justify-content:center;white-space:nowrap;overflow:hidden;box-shadow:inset 0 -2px 0 rgba(0,0,0,.18)}
.bar2.bv{background:#e5383b}.bar2.bi{background:#1d6fe0}.bar2.bx{background:#ffb000;color:#1f1400}.bar2.bm{background:#d6336c;opacity:.6}
.bar2.cv{border-radius:3px}.cv.ok{background:#0ca678}.cv.warn{background:#ffb000;color:#1f1400}.cv.bad{background:#e03131}
.lst{margin:0;padding-left:1.1rem;font-size:.85rem;display:flex;flex-direction:column;gap:6px}.opt .cel{cursor:default}
.login{max-width:340px;margin:12vh auto 0;display:flex;flex-direction:column;gap:10px}
.est{font-size:.76rem;color:var(--muted)}.est.err{color:var(--bad-fg)}
@media(max-width:520px){h1{font-size:1.35rem}}
.pt{display:none;font:700 1.2rem var(--font-display);margin:0 0 6px}
@media print{@page{size:landscape;margin:10mm}body{background:#fff;color:#000;padding:0}nav,header .reloj,.bar,.editor,.aviso,.est,.sub a{display:none!important}.tabla{overflow:visible;border:0}table{min-width:0}.pt{display:block!important}}
</style></head><body>
<div class="wrap" id="raiz"></div>
<script>
const SB='https://gxkxslkdqgwovgxcuzkr.supabase.co',AK='sb_publishable_xAUprOgWQi0HhYms69zUhA_yiTwDYPK';
const DIAS=['Lun','Mar','Mié','Jue','Vie','Sáb','Dom'],DIAS_LARGO=['lunes','martes','miércoles','jueves','viernes','sábado','domingo'];
const MESES=['ene','feb','mar','abr','may','jun','jul','ago','sep','oct','nov','dic'];
const GRUPOS=['Jefatura','Cocineros','Segunda cocina','Ayudantes','Fregantinas'];
const ROLES=['Jefe de cocina','Cocinero','Segunda cocina','Ayudante','Fregantina'];
const MIN_COB=3,MAX_H=40,VAC_ANUAL=30;
let EMP=[];
const nomDe=id=>(EMP.find(x=>x.id===id)||{}).n;

/* ---------- nube (Supabase) ---------- */
let SES=null,HOTEL=null,estado='',pend=0,cadena=Promise.resolve();
try{SES=JSON.parse(localStorage.getItem('hz-ses')||'null')}catch(e){}
async function auth(body,tipo){
  const r=await fetch(SB+'/auth/v1/token?grant_type='+tipo,{method:'POST',headers:{apikey:AK,'Content-Type':'application/json'},body:JSON.stringify(body)});
  const j=await r.json();if(!r.ok||!j.access_token)throw new Error(j.error_description||j.msg||'Error de acceso');
  SES={at:j.access_token,rt:j.refresh_token};localStorage.setItem('hz-ses',JSON.stringify(SES));return j}
async function api(path,o={},reint=true){
  const h={apikey:AK,'Content-Type':'application/json',...(SES?{Authorization:'Bearer '+SES.at}:{}),...(o.h||{})};
  const r=await fetch(SB+'/rest/v1/'+path,{method:o.m||'GET',headers:h,body:o.b?JSON.stringify(o.b):undefined});
  if((r.status===401||r.status===403&&false)&&reint&&SES){try{await auth({refresh_token:SES.rt},'refresh_token');return api(path,o,false)}catch(e){SES=null;localStorage.removeItem('hz-ses');throw new Error('sesión')}}
  if(!r.ok)throw new Error(await r.text());
  const t=await r.text();return t?JSON.parse(t):null}
async function todo(path){let o=0,out=[];for(;;){const a=await api(path+'&limit=1000&offset='+o);out=out.concat(a);if(a.length<1000)return out;o+=1000}}
function marca(t,err){estado=t;const e=document.getElementById('est');if(e){e.textContent=t;e.className='est'+(err?' err':'')}}

/* ---------- estado ---------- */
const LK='hz-local-v2';
let S={datos:{},extras:{},practicas:{},vac:[],notas:[],peticiones:[]};
try{const g=JSON.parse(localStorage.getItem(LK)||'null');if(g){S.extras=g.extras||{};S.practicas=g.practicas||{};S.notas=g.notas||[]}}catch(e){}
const sucias=new Set();let vacSucia=false,ajSucio=false;
function guardarLocal(){try{localStorage.setItem(LK,JSON.stringify({extras:S.extras,practicas:S.practicas,notas:S.notas}))}catch(e){}}
function guardar(){sincronizar()}
function guardarAj(){guardarLocal();ajSucio=true;sincronizar()}
function sincronizar(){
  cadena=cadena.then(async()=>{
    const ks=[...sucias];sucias.clear();const vs=vacSucia;vacSucia=false;const as=ajSucio;ajSucio=false;
    if(!ks.length&&!vs&&!as)return;marca('Guardando…');
    try{
      for(const k of ks){
        const fin=iso(sumar(new Date(k+'T00:00'),6));
        await api(`hz_turnos?fecha=gte.${k}&fecha=lte.${fin}`,{m:'DELETE'});
        const rows=[];EMP.forEach(e=>{((S.datos[k]||{})[e.n]||[]).forEach((t,d)=>{if(t)rows.push({hotel_id:HOTEL,empleado_id:e.id,fecha:iso(sumar(new Date(k+'T00:00'),d)),codigo:t})})});
        if(rows.length)await api('hz_turnos',{m:'POST',b:rows,h:{Prefer:'return=minimal'}})}
      if(vs){await api('hz_vacaciones?id=not.is.null',{m:'DELETE'});
        const rows=S.vac.map(v=>({hotel_id:HOTEL,empleado_id:(EMP.find(e=>e.n===v.e)||{}).id,desde:v.i,hasta:v.f,tipo:v.t,nota:v.n||null})).filter(r=>r.empleado_id);
        if(rows.length)await api('hz_vacaciones',{m:'POST',b:rows,h:{Prefer:'return=minimal'}})}
      if(as)await api('hz_ajustes?on_conflict=hotel_id,clave',{m:'POST',b:[['notas',S.notas],['extras',S.extras],['practicas',S.practicas]].map(([c,v])=>({hotel_id:HOTEL,clave:c,valor:v,actualizado:new Date().toISOString()})),h:{Prefer:'resolution=merge-duplicates,return=minimal'}});
      marca('Guardado en la nube')}
    catch(e){ks.forEach(k=>sucias.add(k));vacSucia=vacSucia||vs;ajSucio=ajSucio||as;marca('No se pudo guardar: '+String(e.message).slice(0,80),1)}})}
async function cargarNube(){
  marca('Cargando…');
  HOTEL=await api('rpc/mi_hotel',{m:'POST',b:{}});
  const em=await api('hz_empleados?select=id,nombre,grupo,token,tel&activo=eq.true&order=orden,nombre');
  EMP=em.map(e=>({id:e.id,n:e.nombre,g:e.grupo,rol:ROLES[e.grupo]||'',token:e.token,tel:e.tel||''}));
  const id2n={};EMP.forEach(e=>id2n[e.id]=e.n);
  const tu=await todo(`hz_turnos?select=empleado_id,fecha,codigo&fecha=gte.${new Date().getFullYear()-1}-01-01&order=fecha`);
  S.datos={};tu.forEach(t=>{const n=id2n[t.empleado_id];if(!n)return;const f=new Date(t.fecha+'T00:00'),k=iso(lunes(f)),d=(f.getDay()+6)%7;
    const o=S.datos[k]||(S.datos[k]={});(o[n]||(o[n]=['','','','','','','']))[d]=t.codigo});
  const va=await api('hz_vacaciones?select=*&order=desde');
  S.vac=va.map(v=>({e:id2n[v.empleado_id],t:v.tipo,i:v.desde,f:v.hasta,n:v.nota||''})).filter(v=>v.e);
  S.peticiones=await api('hz_peticiones?select=*&order=creado.desc&limit=60');
  const aj=await api('hz_ajustes?select=clave,valor'),ajm={};aj.forEach(a=>ajm[a.clave]=a.valor);
  if(ajm.notas){S.notas=ajm.notas;S.extras=ajm.extras||{};S.practicas=ajm.practicas||{}}
  else if(S.notas.length||Object.keys(S.extras).length||Object.keys(S.practicas).length){ajSucio=true;sincronizar()}
  marca('Guardado en la nube')}

/* ---------- utilidades ---------- */
const $=s=>document.querySelector(s);
const esc=s=>String(s??'').replace(/[&<>"']/g,c=>({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;'}[c]));
function iso(d){return d.getFullYear()+'-'+String(d.getMonth()+1).padStart(2,'0')+'-'+String(d.getDate()).padStart(2,'0')}
function lunes(d){const x=new Date(d.getFullYear(),d.getMonth(),d.getDate());x.setDate(x.getDate()-((x.getDay()+6)%7));return x}
function sumar(d,n){const x=new Date(d);x.setDate(x.getDate()+n);return x}
function corto(d){return d.getDate()+' '+MESES[d.getMonth()]}
function parseHM(x){const[h,m]=x.trim().replace('.',':').split(':').map(Number);return h+(m||0)/60}
function tramos(t){if(!t)return[];const u=t.toUpperCase();if(['LIBRE','VACACIONES','BAJA'].some(k=>u.includes(k)))return[];
  const r=[];t.split('\n').forEach(seg=>{const p=seg.trim().split(/[-aA]/);if(p.length<2)return;const i=parseHM(p[0]);let f=parseHM(p[1]);if(isNaN(i)||isNaN(f))return;if(f<=i)f+=24;r.push([i,f])});return r}
function horas(t){return tramos(t).reduce((s,[i,f])=>s+f-i,0)}
function tipoTurno(t){if(!t)return'vacio';const u=t.toUpperCase();if(u.includes('LIBRE'))return'libre';if(u.includes('VACACIONES'))return'vac';if(u.includes('BAJA'))return'baja';return'trab'}
function trabaja(t){return tramos(t).length>0}
function datosSemana(k){return S.datos[k]||(S.datos[k]={})}
function filaEmp(k,n){const d=datosSemana(k);return d[n]||(d[n]=['','','','','','',''])}
function semanaVacia(k){const d=S.datos[k];return!d||!Object.values(d).some(a=>a.some(x=>x))}
function fmtH(h){return(Math.round(h*10)/10).toString().replace('.',',')}

/* ---------- motor optimizador ---------- */
/* ===== MOTOR OPTIMIZADOR (se pega tal cual en la app) ===== */
const SH={D:{t:'06:30-14:30',s:6.5,e:14.5},M:{t:'08:00-16:00',s:8,e:16},E:{t:'12:00-20:00',s:12,e:20},T:{t:'14:30-22:30',s:14.5,e:22.5},N:{t:'16:00-00:00',s:16,e:24},P:{t:'12:00-16:00\n20:00-00:00',s:12,e:24,p:1}};
const MIDI=['M','E','P'], NOCHE=['N','P'];
const NECESITA={mediodia:2,noche:2};
const PREF={'Rubén':'M','Darío':'NPT','Fabián':'MNPD','Álvaro':'NPT','John':'D','David':'D','Ana':'NPET','Jimena':'NPE'};
const COSTE_D=[40,8,20,0,0]; /* por grupo: jefe, cocinero, segunda, ayudante (fregantina no puede) */
const OPCIONES=[
 {id:'A',nombre:'Reparto parejo',desc:'Reparte por igual partidos, fines de semana y desayunos de cobertura.',w:{part:2,pref:.5,bal:4,chg:1}},
 {id:'B',nombre:'Menos partidos',desc:'Reduce al mínimo los turnos partidos.',w:{part:10,pref:.5,bal:.5,chg:1}},
 {id:'C',nombre:'Turnos habituales',desc:'Cada uno en el turno que suele hacer.',w:{part:2,pref:5,bal:.5,chg:1}}];
const AYUDA_DESAYUNO=['John','David'];
function permitidos(e){const g=e.g;
  if(g===4||(g===3&&!AYUDA_DESAYUNO.includes(e.n)))return['M','E','T','N','P'];
  if(g===0)return['M','E','N','P','D'];
  return['M','E','T','N','P','D']}
function rng(seed){let a=seed>>>0;return()=>{a|=0;a=a+0x6D2B79F5|0;let t=Math.imul(a^a>>>15,1|a);t=t+Math.imul(t^t>>>7,61|t)^t;return((t^t>>>14)>>>0)/4294967296}}

/* ctx: {emp:[{n,g}], fijo:[[null|'V'|'B' x7] por empleado], prev:[null|codigo]} */
function evaluar(ctx,G,w,msgs){
  const {emp,fijo,prev}=ctx,H=100,n=emp.length;let c=0;const M=m=>{if(msgs)msgs.push(m)};
  const DN=['lunes','martes','miércoles','jueves','viernes','sábado','domingo'];
  const part=new Array(n).fill(0),fin=new Array(n).fill(0),dCook=[];
  for(let i=0;i<n;i++){
    const g=G[i],f=fijo[i],nf=f.filter(Boolean).length;
    let libres=0,ids=[];g.forEach((x,d)=>{if(x==='L'){libres++;ids.push(d)}});
    const obj=Math.max(0,2-nf);
    if(libres!==obj){c+=H*Math.abs(libres-obj);M(`${emp[i].n}: ${libres} días libres (debe tener ${obj})`)}
    else if(nf===0&&libres===2&&ids[1]-ids[0]!==1){c+=H;M(`${emp[i].n}: los 2 libres no son seguidos`)}
    let last=null;
    for(let d=0;d<7;d++){const x=g[d];if(x==='L'||x==='V'||x==='B'){last=null;continue}
      const s=SH[x];
      if(s.p){c+=w.part;part[i]++}
      if(d>=5)fin[i]++;
      const pf=PREF[emp[i].n];if(pf&&!pf.includes(x))c+=w.pref;
      if(x==='D')c+=COSTE_D[emp[i].g];
      if(AYUDA_DESAYUNO.includes(emp[i].n)&&x!=='D')c+=3;
      if(last&&last!==x)c+=w.chg;
      last=x;
      const pe=d===0?prev[i]:(SH[g[d-1]]?SH[g[d-1]].e:null);
      if(pe!=null){const desc=s.s+24-pe;if(desc<12-1e-9){c+=H;M(`${emp[i].n}: solo ${Math.round(desc*10)/10} h de descanso antes del ${DN[d]}`)}}
    }
  }
  for(let d=0;d<7;d++){
    let nd=0,mid=0,noc=0,midK=0,nocK=0,libres=0,tr=0;
    for(let i=0;i<n;i++){const x=G[i][d];if(x==='L')libres++;
      if(SH[x]){tr++;if(x==='D')nd++;if(MIDI.includes(x)){mid++;if(emp[i].g<=2)midK++}if(NOCHE.includes(x)){noc++;if(emp[i].g<=2)nocK++}}}
    const D=DN[d];
    if(nd===0){c+=H;M(`${D}: nadie hace el desayuno`)}else if(nd>1)c+=15*(nd-1);
    if(mid<NECESITA.mediodia){c+=H*(NECESITA.mediodia-mid);M(`${D}: mediodía con ${mid} (mínimo ${NECESITA.mediodia})`)}
    if(noc<NECESITA.noche){c+=H*(NECESITA.noche-noc);M(`${D}: noche con ${noc} (mínimo ${NECESITA.noche})`)}
    if(!midK){c+=H;M(`${D}: sin cocinero a mediodía`)}
    if(!nocK){c+=H;M(`${D}: sin cocinero por la noche`)}
    if(tr<3){c+=H;M(`${D}: solo ${tr} personas`)}
    if(d>=5&&libres>1){c+=H*(libres-1);M(`${D}: ${libres} personas libres (máximo 1)`)}
  }
  /* equilibrio: varianza de partidos, fines de semana y desayunos de cocineros */
  const vari=a=>{if(a.length<2)return 0;const m=a.reduce((s,x)=>s+x,0)/a.length;return a.reduce((s,x)=>s+(x-m)*(x-m),0)/a.length};
  const act=[];for(let i=0;i<n;i++)if(emp[i].g!==4&&fijo[i].filter(Boolean).length<3)act.push(i);
  c+=w.bal*(vari(act.map(i=>part[i]))+vari(act.map(i=>fin[i])));
  const ck=[];for(let i=0;i<n;i++)if(emp[i].g===1)ck.push(G[i].filter(x=>x==='D').length);
  c+=w.bal*vari(ck);
  return c}

function resolver(ctx,w,seed,iter){
  const R=rng(seed),{emp,fijo}=ctx,n=emp.length,perm=emp.map(permitidos);
  const G=emp.map((e,i)=>{const nf=fijo[i].filter(Boolean).length,obj=Math.max(0,2-nf);
    const f=fijo[i].slice();const libres=[];
    if(obj===2){const s=Math.floor(R()*6);libres.push(s,s+1)}else if(obj===1)libres.push(Math.floor(R()*7));
    return f.map((x,d)=>{if(x)return x;if(libres.includes(d))return'L';
      const pf=(PREF[e.n]||'').split('').filter(k=>perm[i].includes(k));const pool=pf.length?pf:perm[i].filter(k=>k!=='D');return pool[Math.floor(R()*pool.length)]})});
  const libre=(i,d)=>!fijo[i][d];
  let cur=evaluar(ctx,G,w),best=cur,bestG=G.map(r=>r.slice());
  const T0=25,T1=.15;
  for(let it=0;it<iter;it++){
    const T=T0*Math.pow(T1/T0,it/iter),r=R();let undo;
    if(r<.55){const i=Math.floor(R()*n),d=Math.floor(R()*7);if(!libre(i,d))continue;
      const op=perm[i].concat(['L']),v=op[Math.floor(R()*op.length)],o=G[i][d];if(v===o)continue;G[i][d]=v;undo=()=>{G[i][d]=o}}
    else if(r<.8){const d=Math.floor(R()*7),i=Math.floor(R()*n),j=Math.floor(R()*n);if(i===j||!libre(i,d)||!libre(j,d))continue;
      const a=G[i][d],b=G[j][d];if(a===b)continue;if(b!=='L'&&!perm[i].includes(b))continue;if(a!=='L'&&!perm[j].includes(a))continue;
      G[i][d]=b;G[j][d]=a;undo=()=>{G[i][d]=a;G[j][d]=b}}
    else{const i=Math.floor(R()*n),d=Math.floor(R()*7),e2=Math.floor(R()*7);if(d===e2||!libre(i,d)||!libre(i,e2))continue;
      const a=G[i][d],b=G[i][e2];if(a===b)continue;G[i][d]=b;G[i][e2]=a;undo=()=>{G[i][d]=a;G[i][e2]=b}}
    const nw=evaluar(ctx,G,w);
    if(nw<=cur||R()<Math.exp((cur-nw)/T)){cur=nw;if(cur<best){best=cur;bestG=G.map(r=>r.slice())}}else undo();
  }
  return{G:bestG,coste:best}}

function optimizar(ctx,semilla){
  return OPCIONES.map((o,k)=>{let mejor=null;
    for(let r=0;r<3;r++){const s=resolver(ctx,o.w,semilla*101+k*7+r,14000);if(!mejor||s.coste<mejor.coste)mejor=s}
    const msgs=[];evaluar(ctx,mejor.G,o.w,msgs);
    return{...o,G:mejor.G,coste:mejor.coste,avisos:msgs}})}
function resumen(ctx,G){const {emp}=ctx;let partidos=0,cobertura=[];const DN=['lun','mar','mié','jue','vie','sáb','dom'];
  const horas=emp.map((e,i)=>G[i].filter(x=>SH[x]).length*8);
  G.forEach((g,i)=>g.forEach((x,d)=>{if(x==='P')partidos++;if(x==='D'&&!AYUDA_DESAYUNO.includes(emp[i].n))cobertura.push(`${DN[d]}: ${emp[i].n}`)}));
  return{partidos,cobertura,horas}}



/* ---------- interfaz ---------- */
let tab='plantilla',semana=lunes(new Date()),edit=null,anioVac=new Date().getFullYear();
const TABS=[['plantilla','Plantilla'],['ahora','Ahora'],['extras','Extras'],['practicas','Prácticas'],['vacaciones','Vacaciones'],['anual','Año completo'],['opt','Optimizador'],['equipo','Equipo'],['notas','Notas']];
function reloj(){const n=new Date(),h=document.getElementById('hora');if(!h)return;h.textContent=String(n.getHours()).padStart(2,'0')+':'+String(n.getMinutes()).padStart(2,'0');
  document.getElementById('fecha').textContent=DIAS_LARGO[(n.getDay()+6)%7]+' '+n.getDate()+' '+MESES[n.getMonth()]}
setInterval(()=>{reloj();if(tab==='ahora'&&EMP.length)pintar()},30000);
function esqueleto(){$('#raiz').innerHTML=`<header><div><h1>Horarios de Cocina</h1><div class="sub">Seda Club Hotel · Granada · <span id="est" class="est">${esc(estado)}</span> · <a href="#" data-a="salir" style="color:inherit">Salir</a></div></div><div class="reloj"><b id="hora">--:--</b><span id="fecha"></span></div></header><nav role="tablist" id="tabs"></nav><main id="vista"></main>`;reloj()}
function login(m){$('#raiz').innerHTML=`<form class="login card" id="f-login"><h1>Horarios de Cocina</h1><div class="sub">Entra con tu cuenta de jefe</div><input id="lm" type="email" placeholder="Correo" autocomplete="username" required><input id="lp" type="password" placeholder="Contraseña" autocomplete="current-password" required><button class="btn pri" type="submit">Entrar</button><div class="est err">${esc(m||'')}</div></form>`}
function pintar(){if(!document.getElementById('vista'))esqueleto();
  $('#tabs').innerHTML=TABS.map(([k,n])=>`<button role="tab" aria-selected="${k===tab}" data-t="${k}">${n}${k==='equipo'&&S.peticiones.filter(p=>p.estado==='pendiente').length?' ('+S.peticiones.filter(p=>p.estado==='pendiente').length+')':''}</button>`).join('');
  const f={plantilla:vPlantilla,ahora:vAhora,extras:()=>vPersonas('extras'),practicas:()=>vPersonas('practicas'),vacaciones:vVacaciones,anual:vAnual,opt:vOpt,equipo:vEquipo,notas:vNotas}[tab];$('#vista').innerHTML=f()}

function avisosSemana(k){const av=[],d=S.datos[k];if(!d)return av;
  EMP.forEach(e=>{const a=d[e.n];if(!a)return;const h=a.reduce((s,t)=>s+horas(t),0);if(h>MAX_H)av.push(`${e.n} suma ${fmtH(h)} h (máximo ${MAX_H} h)`);
    for(let i=0;i<6;i++){const t1=tramos(a[i]),t2=tramos(a[i+1]);if(!t1.length||!t2.length)continue;const fin=Math.max(...t1.map(x=>x[1])),ini=Math.min(...t2.map(x=>x[0]))+24,desc=ini-fin;
      if(desc<12)av.push(`${e.n}: solo ${fmtH(desc)} h de descanso entre ${DIAS_LARGO[i]} y ${DIAS_LARGO[i+1]}`)}});
  for(let i=0;i<7;i++){const c=cobertura(k,i);if(c<MIN_COB)av.push(`${DIAS_LARGO[i][0].toUpperCase()+DIAS_LARGO[i].slice(1)}: ${c} persona${c===1?'':'s'} (mínimo ${MIN_COB})`)}
  [5,6].forEach(i=>{const l=EMP.filter(e=>tipoTurno((d[e.n]||[])[i])==='libre').length;if(l>1)av.push(`${DIAS_LARGO[i][0].toUpperCase()+DIAS_LARGO[i].slice(1)}: ${l} personas libres (máximo 1)`)});return av}
function cobertura(k,i){const d=S.datos[k]||{};let n=EMP.filter(e=>trabaja((d[e.n]||[])[i])).length;(S.extras[k]||[]).forEach(p=>{if(trabaja(p.t[i]))n++});return n}

function vPlantilla(){
  const k=iso(semana),fin=sumar(semana,6),hoyIso=iso(new Date()),vacia=semanaVacia(k);
  const prev=Object.keys(S.datos).filter(x=>x<k&&!semanaVacia(x)).sort().pop();
  let h=`<div class="pt">Horario de cocina · ${corto(semana)} – ${corto(fin)}</div><div class="bar"><button class="btn" data-a="ant" aria-label="Semana anterior">←</button><div class="semana">${corto(semana)} – ${corto(fin)}</div><button class="btn" data-a="sig" aria-label="Semana siguiente">→</button><button class="btn" data-a="hoy">Esta semana</button><button class="btn" data-a="imprimir">Imprimir / PDF</button><span class="grow"></span>${vacia&&prev?`<button class="btn pri" data-a="copiar" data-p="${prev}">Copiar semana del ${corto(new Date(prev+'T00:00'))}</button>`:''}</div>`;
  if(vacia)h+=`<div class="aviso warn">Esta semana no tiene turnos. Toca una celda para escribirlos${prev?' o copia la última semana con datos':''}.</div>`;
  else{const av=avisosSemana(k);h+=av.length?`<div class="aviso warn"><b>${av.length} aviso${av.length===1?'':'s'} en esta semana</b><ul>${av.map(x=>`<li>${esc(x)}</li>`).join('')}</ul></div>`:`<div class="aviso ok">Sin avisos: cobertura, descansos y horas dentro de las reglas.</div>`}
  h+=`<div class="tabla"><table><thead><tr><th class="nom">Equipo</th>${DIAS.map((n,i)=>`<th class="${iso(sumar(semana,i))===hoyIso?'hoy':''}">${n}<br>${sumar(semana,i).getDate()}</th>`).join('')}<th>h/sem</th></tr></thead><tbody>`;
  GRUPOS.forEach((g,gi)=>{h+=`<tr class="grp"><td colspan="9">${g}</td></tr>`;
    EMP.filter(e=>e.g===gi).forEach(e=>{const a=filaEmp(k,e.n),tot=a.reduce((s,t)=>s+horas(t),0);
      h+=`<tr><td class="nom"><b>${esc(e.n)}</b><small>${e.rol}</small></td>${a.map((t,i)=>{let c=tipoTurno(t);if(c==='trab'&&e.g===0)c='jefe';
        const sel=edit&&edit.k===k&&edit.e===e.n&&edit.i===i?' sel':'';
        return`<td><button class="cel ${c}${sel}" data-e="${esc(e.n)}" data-i="${i}" aria-label="${esc(e.n)}, ${DIAS_LARGO[i]}">${c==='vacio'?'+':t.split('\n').map(s=>`<span>${esc(s)}</span>`).join('')}</button></td>`}).join('')}<td class="h ${tot>MAX_H?'alta':''}">${tot?fmtH(tot):'–'}</td></tr>`})});
  h+=`<tr class="cob"><td class="nom">Cobertura</td>${[0,1,2,3,4,5,6].map(i=>{const c=cobertura(k,i);return`<td><span class="cobp ${vacia?'':c>=MIN_COB?'ok':c===2?'warn':'bad'}">${vacia?'–':c}</span></td>`}).join('')}<td></td></tr></tbody></table></div>`;
  if(edit&&edit.k===k){const t=filaEmp(k,edit.e)[edit.i];
    h+=`<div class="editor"><h3>${esc(edit.e)} · ${DIAS_LARGO[edit.i]} ${sumar(semana,edit.i).getDate()} ${MESES[sumar(semana,edit.i).getMonth()]}</h3>
    <label for="turno-txt" class="aviso-guardado">Turno (un bloque por línea; el partido son dos líneas)</label><textarea id="turno-txt" rows="2" placeholder="08:00-16:00">${esc(t)}</textarea>
    <div class="chips">${[['Libre','LIBRE'],['Vacaciones','VACACIONES'],['Baja','BAJA MATERNAL'],['06:30-14:30','06:30-14:30'],['08:00-16:00','08:00-16:00'],['12:00-20:00','12:00-20:00'],['14:30-22:30','14:30-22:30'],['16:00-00:00','16:00-00:00'],['Partido','12:00-16:00\n20:00-00:00']].map(([n,v])=>`<button class="btn sm" data-q="${esc(v)}">${n}</button>`).join('')}</div>
    <div class="bar"><button class="btn pri" data-a="gturno">Guardar</button><button class="btn" data-a="cturno">Cancelar</button><button class="btn" data-a="bturno">Borrar celda</button></div></div>`}
  return h}

function vAhora(){
  const n=new Date(),k=iso(lunes(n)),di=(n.getDay()+6)%7,hr=n.getHours()+n.getMinutes()/60,d=S.datos[k];
  if(semanaVacia(k))return`<div class="card"><h3>Sin turnos esta semana</h3><div class="vacio-txt">Carga los turnos de la semana en Plantilla.</div><button class="btn pri" data-a="irplantilla">Ir a Plantilla</button></div>`;
  const en=[],pronto=[],fuera=[],todos=EMP.map(e=>({n:e.n,rol:e.rol,t:(d[e.n]||[])[di]||''}));
  (S.extras[k]||[]).forEach(p=>todos.push({n:p.n,rol:'Extra · '+p.rol,t:p.t[di]||''}));
  todos.forEach(p=>{let est='fuera';for(const[i,f]of tramos(p.t)){let h2=hr;if(f>24&&hr<i-12)h2=hr+24;if(h2>=i&&h2<f){est='en';break}if(i>h2&&i-h2<2)est='pronto'}(est==='en'?en:est==='pronto'?pronto:fuera).push(p)});
  const lista=(a,v)=>a.length?a.map(p=>`<div class="fila"><span><b>${esc(p.n)}</b><br><small>${esc(p.rol)}</small></span><span class="pill ${tipoTurno(p.t)==='trab'?'trab':tipoTurno(p.t)}">${esc(p.t.replace('\n',' · ')||'—')}</span></div>`).join(''):`<div class="vacio-txt">${v}</div>`;
  return`<div class="cols"><div class="card"><h3>En turno ahora (${en.length})</h3>${lista(en,'Nadie en este momento.')}</div><div class="card"><h3>Entran en menos de 2 h (${pronto.length})</h3>${lista(pronto,'Nadie entra pronto.')}</div><div class="card"><h3>Fuera hoy (${fuera.length})</h3>${lista(fuera,'Todos están en turno.')}</div></div>`}

function vPersonas(tipo){
  const k=iso(semana),lista=S[tipo][k]||[],fin=sumar(semana,6),extra=tipo==='extras';
  let h=`<div class="bar"><button class="btn" data-a="ant">←</button><div class="semana">${corto(semana)} – ${corto(fin)}</div><button class="btn" data-a="sig">→</button><button class="btn" data-a="hoy">Esta semana</button></div>`;
  h+=`<div class="card"><h3>${extra?'Personal extra':'Alumnos en prácticas'} de la semana</h3>`;
  h+=lista.length?lista.map((p,ix)=>`<div class="fila" style="align-items:flex-start;flex-wrap:wrap"><span><b>${esc(p.n)}</b><br><small>${esc(p.rol)}</small></span><span style="display:flex;gap:4px;flex-wrap:wrap">${p.t.map((t,i)=>`<span class="pill ${t?'extra':'libre'}">${DIAS[i]} ${esc((t||'—').replace('\n',' · '))}</span>`).join('')}</span><button class="btn sm" data-del="${ix}">Quitar</button></div>`).join(''):`<div class="vacio-txt">Nadie apuntado esta semana.</div>`;
  h+=`</div><form class="card" id="f-pers" data-tipo="${tipo}"><h3>Añadir ${extra?'extra':'alumno'}</h3><div class="form"><label>Nombre<input id="pn" required></label><label>${extra?'Puesto':'Centro educativo'}<input id="pr" required></label></div><div class="dias7">${DIAS.map((n,i)=>`<label>${n}<input id="pt${i}" placeholder="08:00-16:00"></label>`).join('')}</div><button class="btn pri" type="submit">Añadir</button></form><div class="aviso-guardado">Extras y prácticas se guardan en la nube.</div>`;
  return h}

function diasEn(i,f,y){const a=new Date(Math.max(new Date(i+'T00:00'),new Date(y+'-01-01T00:00'))),b=new Date(Math.min(new Date(f+'T00:00'),new Date(y+'-12-31T00:00')));return b<a?0:Math.round((b-a)/864e5)+1}
function vVacaciones(){
  const y=anioVac;
  let h=`<div class="bar"><button class="btn" data-a="aant">←</button><div class="semana">${y}</div><button class="btn" data-a="asig">→</button><span class="grow"></span><button class="btn pri" data-a="irannual">Ver año completo</button></div>
  <div class="leyenda"><span>■ <span style="color:var(--vac-fg)">verano</span></span><span>■ <span style="color:var(--jefe-fg)">invierno</span></span><span>■ <span style="color:var(--attn)">extra</span></span><span>■ <span style="color:var(--baja-fg)">baja</span></span></div><div class="cols">`;
  EMP.forEach(e=>{const ps=S.vac.filter(v=>v.e===e.n&&v.i.slice(0,4)<=y&&v.f.slice(0,4)>=y);
    const usados=ps.filter(v=>v.t!=='maternal').reduce((s,v)=>s+diasEn(v.i,v.f,y),0),res=VAC_ANUAL-usados,col=res>10?'var(--good)':res>=5?'var(--attn)':'var(--crit)';
    const meses=Array.from({length:12},(_,m)=>{const ini=new Date(y,m,1),fi=new Date(y,m+1,0);const p=ps.find(v=>new Date(v.i+'T00:00')<=fi&&new Date(v.f+'T00:00')>=ini);return`<span class="${p?({verano:'v',invierno:'i',extra:'x',maternal:'m'}[p.t]):''}" title="${MESES[m]}"></span>`}).join('');
    const mat=ps.some(v=>v.t==='maternal');
    h+=`<div class="card"><div class="fila" style="border:0;padding:0"><b>${esc(e.n)}</b><small>${mat&&!usados?'Baja':`${res} de ${VAC_ANUAL} días`}</small></div>${mat&&!usados?'':`<div class="saldo"><i style="width:${Math.max(0,Math.min(100,usados/VAC_ANUAL*100))}%;background:${col}"></i></div>`}<div class="meses">${meses}</div>
    ${ps.map(v=>`<div class="fila"><span><small>${esc(v.t)} · ${corto(new Date(v.i+'T00:00'))} – ${corto(new Date(v.f+'T00:00'))}</small>${v.n?`<br><small>${esc(v.n)}</small>`:''}</span><span style="display:flex;gap:6px;align-items:center"><small>${diasEn(v.i,v.f,y)} d</small><button class="btn sm" data-vdel="${S.vac.indexOf(v)}">Quitar</button></span></div>`).join('')}</div>`});
  h+=`</div><form class="card" id="f-vac"><h3>Añadir periodo</h3><div class="form"><label>Empleado<select id="ve">${EMP.map(e=>`<option>${esc(e.n)}</option>`).join('')}</select></label><label>Tipo<select id="vt"><option value="verano">verano</option><option value="invierno">invierno</option><option value="extra">extra</option><option value="maternal">maternal</option></select></label><label>Desde<input type="date" id="vi" required></label><label>Hasta<input type="date" id="vf" required></label><label>Nota<input id="vn"></label></div><br><button class="btn pri" type="submit">Añadir</button></form>`;
  return h}

function vAnual(){
  const y=anioVac,ini=new Date(y,0,1),nd=Math.round((new Date(y+1,0,1)-ini)/864e5),W=5,NW=116;
  const idx=s=>Math.round((new Date(s+'T00:00')-ini)/864e5),cl=v=>Math.max(0,Math.min(nd-1,v));
  const ps=S.vac.filter(v=>v.i.slice(0,4)<=y&&v.f.slice(0,4)>=y);
  const away=Array.from({length:nd},()=>[]),mat=new Array(nd).fill(0);
  ps.forEach(v=>{for(let d=cl(idx(v.i));d<=cl(idx(v.f));d++){if(v.t==='maternal')mat[d]++;else if(!away[d].includes(v.e))away[d].push(v.e)}});
  const disp=d=>EMP.length-mat[d]-away[d].length,grp=n=>EMP.find(e=>e.n===n).g,dd=d=>sumar(ini,d);
  const runs=f=>{const r=[];let s=0;for(let d=1;d<=nd;d++){if(d===nd||f(d)!==f(s)){r.push([s,d-1]);s=d}}return r};
  const dias=(a,b)=>b-a+1,rango=(a,b)=>corto(dd(a))+' – '+corto(dd(b));
  const lin=[];for(let m=1;m<12;m++)lin.push(`linear-gradient(var(--line),var(--line)) ${Math.round((new Date(y,m,1)-ini)/864e5)*W}px 0/1px 100% no-repeat`);
  const t0=new Date(),hoyD=t0.getFullYear()===y?Math.round((new Date(y,t0.getMonth(),t0.getDate())-ini)/864e5):-1;
  if(hoyD>=0)lin.push(`linear-gradient(var(--accent),var(--accent)) ${hoyD*W}px 0/2px 100% no-repeat`);
  const bg=lin.join(','),wpx=nd*W;
  const mh=Array.from({length:12},(_,m)=>{const a=Math.round((new Date(y,m,1)-ini)/864e5),b=Math.round((new Date(y,m+1,1)-ini)/864e5);return`<span style="left:${a*W}px;width:${(b-a)*W}px">${MESES[m]}</span>`}).join('');
  const filas=EMP.map(e=>{const mine=ps.filter(v=>v.e===e.n),usados=mine.filter(v=>v.t!=='maternal').reduce((s,v)=>s+diasEn(v.i,v.f,y),0);
    const barras=mine.map(v=>{const a=cl(idx(v.i)),b=cl(idx(v.f)),w=(b-a+1)*W,c={verano:'bv',invierno:'bi',extra:'bx',maternal:'bm'}[v.t]||'bx',r=corto(new Date(v.i+'T00:00'))+' – '+corto(new Date(v.f+'T00:00'));
      return`<div class="bar2 ${c}" style="left:${a*W}px;width:${w}px" title="${esc(e.n+' · '+v.t+' · '+r)}">${w>=70?esc(r):''}</div>`}).join('');
    return`<div class="arow"><div class="anom"><b>${esc(e.n)}</b><small>${mine.some(v=>v.t==='maternal')&&!usados?'baja':usados+' / '+VAC_ANUAL+' d'}</small></div><div class="atrk" style="width:${wpx}px;background:${bg}">${barras}</div></div>`}).join('');
  const segs=runs(d=>away[d].join('|'));
  const cov=segs.filter(([a])=>away[a].length).map(([a,b])=>{const dp=disp(a),c=dp<5?'bad':dp===5?'warn':'ok',w=dias(a,b)*W;return`<div class="bar2 cv ${c}" style="left:${a*W}px;width:${w}px" title="${esc(away[a].join(', ')+' · '+rango(a,b))}">${w>=14?away[a].length:''}</div>`}).join('');
  const sol=segs.filter(([a])=>away[a].length>=2),huecos=runs(d=>away[d].length?1:0).filter(([a,b])=>!away[a].length&&dias(a,b)>=7);
  const li=sol.map(([a,b])=>{const nm=away[a],mismo=nm.some((n,i)=>nm.findIndex(m=>grp(m)===grp(n))!==i);return`<li><b>${rango(a,b)}</b> (${dias(a,b)} d): ${nm.map(esc).join(' + ')} · quedan ${disp(a)}${mismo?' · <b>mismo puesto</b>':''}</li>`}).join('');
  const hu=huecos.map(([a,b])=>`<li><b>${rango(a,b)}</b> (${dias(a,b)} d)</li>`).join('');
  if(hoyD>=0)setTimeout(()=>{const t=document.getElementById('ano-sc');if(t)t.scrollLeft=Math.max(0,hoyD*W-80)},0);
  return`<div class="bar"><button class="btn" data-a="aant">←</button><div class="semana">${y}</div><button class="btn" data-a="asig">→</button><span class="grow"></span><button class="btn" data-a="irvac">Añadir o editar periodos</button></div>
  <div class="leyenda"><span><span style="color:#e5383b">■</span> verano</span><span><span style="color:#1d6fe0">■</span> invierno</span><span><span style="color:#ffb000">■</span> extra</span><span><span style="color:#d6336c">■</span> baja</span><span>| Ausentes: <span style="color:#0ca678">■</span> quedan 6+ · <span style="color:#ffb000">■</span> 5 · <span style="color:#e03131">■</span> menos de 5</span></div>
  <div class="tabla" id="ano-sc"><div style="width:${NW+wpx}px"><div class="arow"><div class="anom"></div><div class="atrk ah" style="width:${wpx}px">${mh}</div></div>${filas}<div class="arow"><div class="anom"><b>Ausentes</b><small>por día</small></div><div class="atrk" style="width:${wpx}px;background:${bg}">${cov}</div></div></div></div>
  <div class="cols"><div class="card"><h3>Se pisan (${sol.length})</h3>${li?`<ul class="lst">${li}</ul>`:'<div class="vacio-txt">Nadie coincide de vacaciones este año.</div>'}</div><div class="card"><h3>Huecos sin vacaciones</h3>${hu?`<ul class="lst">${hu}</ul>`:'<div class="vacio-txt">No quedan huecos de 7 días o más.</div>'}</div></div>`}

let OPT={k:null,opts:null,ctx:null,seed:0,busy:false};
const COD_TXT=c=>c==='L'?'LIBRE':c==='V'?'VACACIONES':c==='B'?'BAJA MATERNAL':SH[c].t;
function ctxOpt(){const k=iso(semana),pk=iso(sumar(semana,-7));
  const fijo=EMP.map(e=>Array.from({length:7},(_,d)=>{const f=iso(sumar(semana,d)),p=S.vac.find(v=>v.e===e.n&&v.i<=f&&v.f>=f);if(p)return p.t==='maternal'?'B':'V';
    const u=(((S.datos[k]||{})[e.n]||[])[d]||'').toUpperCase();return u.includes('BAJA')?'B':u.includes('VACACIONES')?'V':null}));
  const prev=EMP.map(e=>{const t=((S.datos[pk]||{})[e.n]||[])[6]||'',tr=tramos(t);return tr.length?Math.max(...tr.map(x=>x[1])):null});
  return{emp:EMP.map(e=>({n:e.n,g:e.g})),fijo,prev}}
function vOpt(){
  const k=iso(semana),fin=sumar(semana,6),lista=OPT.k===k&&OPT.opts?OPT.opts:null,vacia=semanaVacia(k);
  let h=`<div class="bar"><button class="btn" data-a="ant">←</button><div class="semana">${corto(semana)} – ${corto(fin)}</div><button class="btn" data-a="sig">→</button><button class="btn" data-a="hoy">Esta semana</button><span class="grow"></span><button class="btn pri" data-a="optgen" ${OPT.busy?'disabled':''}>${OPT.busy?'Calculando…':lista?'Otras opciones':'Generar opciones'}</button></div>`;
  h+=`<details class="card"><summary>Reglas que aplica</summary><ul class="lst" style="margin-top:8px"><li>2 días libres seguidos por persona; máximo 1 libre el sábado y 1 el domingo.</li><li>12 h de descanso entre turnos y máximo 40 h.</li><li>Mediodía y noche: mínimo ${NECESITA.mediodia} personas, una de ellas cocinero.</li><li>Desayuno: John o David; si falta uno, lo cubre un cocinero (rotando), luego la segunda y por último el jefe.</li><li>Respeta las vacaciones y bajas cargadas.</li></ul></details>`;
  if(!lista){h+=`<div class="card"><h3>${OPT.busy?'Calculando propuestas…':'Sin propuestas todavía'}</h3><div class="vacio-txt">${vacia?'':'Esta semana ya tiene turnos: si aplicas una propuesta, los reemplaza. '}Pulsa Generar opciones para ver 3 alternativas. No cambia nada hasta que apliques una.</div></div>`;return h}
  lista.forEach((o,ix)=>{const r=resumen(OPT.ctx,o.G);
    h+=`<div class="card opt"><div class="bar"><h3 style="margin:0">${o.id} · ${o.nombre}</h3><span class="grow"></span><span class="cobp ${o.avisos.length?'bad':'ok'}">${o.avisos.length?o.avisos.length+' avisos':'Sin avisos'}</span><span class="cobp ok">${r.partidos} partidos</span></div><div class="sub">${o.desc}</div>
    <div class="tabla" style="margin:8px 0"><table><thead><tr><th class="nom">Equipo</th>${DIAS.map((n,i)=>`<th>${n}<br>${sumar(semana,i).getDate()}</th>`).join('')}</tr></thead><tbody>${EMP.map((e,i)=>`<tr><td class="nom"><b>${esc(e.n)}</b></td>${o.G[i].map(c=>{const t=COD_TXT(c);let cl=tipoTurno(t);if(cl==='trab'&&e.g===0)cl='jefe';return`<td><div class="cel ${cl}">${t.split('\n').map(s=>`<span>${esc(s)}</span>`).join('')}</div></td>`}).join('')}</tr>`).join('')}</tbody></table></div>
    <div class="sub">${r.cobertura.length?'Desayuno cubierto por cocineros: '+r.cobertura.join(' · '):'Desayunos: solo John y David.'}</div>${o.avisos.length?`<div class="aviso warn"><ul>${o.avisos.map(x=>`<li>${esc(x)}</li>`).join('')}</ul></div>`:''}
    <div class="bar" style="margin-top:8px"><button class="btn pri" data-a="optaplicar" data-o="${ix}">${vacia?'Aplicar a la semana':'Reemplazar turnos de la semana'}</button></div></div>`});
  return h}

function turnoDe(n,f){const d=new Date(f+'T00:00'),k=iso(lunes(d));return((S.datos[k]||{})[n]||[])[(d.getDay()+6)%7]||'sin turno'}
function textoSemana(e){const a=(S.datos[iso(semana)]||{})[e.n]||[];
  return `Hola ${e.n}, tu horario del ${corto(semana)} al ${corto(sumar(semana,6))}:\n`+DIAS.map((d,i)=>`${d} ${sumar(semana,i).getDate()}: ${(a[i]||'sin turno').replace(/\n/g,' y ')}`).join('\n')+`\nVer tu turno y pedir cambios: ${location.origin}/e.html?t=${e.token}`}
function waUrl(e){let t=(e.tel||'').replace(/\D/g,'');if(t.length===9)t='34'+t;return'https://wa.me/'+t+'?text='+encodeURIComponent(textoSemana(e))}
function vEquipo(){
  const base=location.origin+'/e.html?t=',pen=S.peticiones.filter(p=>p.estado==='pendiente');
  const fd=s=>s?corto(new Date(s+'T00:00')):'';
  const fila=p=>{const n=nomDe(p.empleado_id)||'?',cn=nomDe(p.con_empleado_id);let t;
    if(p.tipo==='intercambio'&&cn&&p.desde)t=`<b>${esc(n)}</b> quiere cambiar su turno del ${fd(p.desde)} con <b>${esc(cn)}</b><br><small>${esc(n)}: ${esc(turnoDe(n,p.desde).replace(/\n/g,' y '))} ⇄ ${esc(cn)}: ${esc(turnoDe(cn,p.desde).replace(/\n/g,' y '))}</small>`;
    else t=`<b>${esc(n)}</b> · ${esc(p.tipo)} · ${fd(p.desde)}${p.hasta&&p.hasta!==p.desde?' – '+fd(p.hasta):''}`;
    return`<div class="fila" style="align-items:flex-start;flex-wrap:wrap"><span>${t}${p.nota?`<br><small>${esc(p.nota)}</small>`:''}</span><span style="display:flex;gap:6px"><button class="btn sm pri" data-pet="aprobada" data-id="${p.id}">Aprobar</button><button class="btn sm" data-pet="rechazada" data-id="${p.id}">Rechazar</button></span></div>`};
  let h=`<div class="card"><h3>Peticiones pendientes (${pen.length})</h3>${pen.length?pen.map(fila).join(''):'<div class="vacio-txt">Nada pendiente.</div>'}</div>`;
  h+=`<div class="card"><h3>Equipo: enlaces y WhatsApp</h3><div class="sub">Semana que se envía: <b>${corto(semana)} – ${corto(sumar(semana,6))}</b> (cámbiala en Plantilla). Apunta el móvil de cada uno para mandarle su semana ya escrita.</div>${EMP.map(e=>`<div class="fila" style="flex-wrap:wrap"><span><b>${esc(e.n)}</b><br><small>${e.rol}</small></span><span style="display:flex;gap:6px;flex-wrap:wrap;align-items:center"><input data-tel="${e.id}" value="${esc(e.tel)}" placeholder="Móvil" inputmode="tel" style="width:120px;min-height:32px"><button class="btn sm" data-copy="${base}${e.token}">Copiar enlace</button>${e.tel?`<a class="btn sm pri" style="text-decoration:none" target="_blank" rel="noopener" href="${waUrl(e)}">Enviar semana</a>`:''}</span></div>`).join('')}</div>`;
  return h}

function vNotas(){
  const lista=[...S.notas].map((n,i)=>({...n,i})).sort((a,b)=>a.f.localeCompare(b.f)),col={evento:'--work-fg',aviso:'--bad-fg',info:'--jefe-fg'};
  return`<div class="card"><h3>Eventos y avisos</h3>${lista.length?lista.map(n=>`<div class="fila"><span><span class="nota-tipo" style="color:var(${col[n.t]||'--muted'})">${esc(n.t)}</span> · <small>${corto(new Date(n.f+'T00:00'))}</small><br>${esc(n.x)}</span><button class="btn sm" data-ndel="${n.i}">Quitar</button></div>`).join(''):'<div class="vacio-txt">No hay notas.</div>'}</div>
  <form class="card" id="f-nota"><h3>Añadir nota</h3><div class="form"><label>Fecha<input type="date" id="nf" required value="${iso(new Date())}"></label><label>Tipo<select id="nt"><option value="evento">evento</option><option value="aviso">aviso</option><option value="info">info</option></select></label></div><br><label style="display:flex;flex-direction:column;gap:3px;font-size:.78rem;color:var(--muted)">Texto<textarea id="nx" rows="2" required></textarea></label><br><button class="btn pri" type="submit">Añadir</button></form><div class="aviso-guardado">Los avisos, eventos e info de las próximas 3 semanas los ve cada empleado en su móvil.</div>`}

/* ---------- eventos ---------- */
document.addEventListener('click',async e=>{
  const T=e.target.closest('button[data-t]');if(T){tab=T.dataset.t;edit=null;pintar();return}
  const c=e.target.closest('.cel');
  if(c&&c.dataset.e){edit={k:iso(semana),e:c.dataset.e,i:+c.dataset.i};pintar();const t=$('#turno-txt');if(t)t.focus();return}
  const q=e.target.closest('[data-q]');if(q){$('#turno-txt').value=q.dataset.q;return}
  const cp=e.target.closest('[data-copy]');if(cp){try{await navigator.clipboard.writeText(cp.dataset.copy);cp.textContent='¡Copiado!'}catch(x){prompt('Copia el enlace:',cp.dataset.copy)}return}
  const pt=e.target.closest('[data-pet]');if(pt){const p=S.peticiones.find(x=>x.id===pt.dataset.id);
    try{await api('hz_peticiones?id=eq.'+p.id,{m:'PATCH',b:{estado:pt.dataset.pet},h:{Prefer:'return=minimal'}});p.estado=pt.dataset.pet;
      if(pt.dataset.pet==='aprobada'&&p.tipo==='vacaciones'&&p.desde){const n=nomDe(p.empleado_id);if(n){S.vac.push({e:n,t:'extra',i:p.desde,f:p.hasta||p.desde,n:p.nota||'Petición'});vacSucia=true;guardar()}}
      if(pt.dataset.pet==='aprobada'&&p.tipo==='intercambio'&&p.desde){const a=nomDe(p.empleado_id),b=nomDe(p.con_empleado_id);if(a&&b){const f=new Date(p.desde+'T00:00'),k=iso(lunes(f)),d=(f.getDay()+6)%7,fa=filaEmp(k,a),fb=filaEmp(k,b);[fa[d],fb[d]]=[fb[d],fa[d]];sucias.add(k);guardar();const av=avisosSemana(k).length;setTimeout(()=>marca(av?'Cambio hecho: revisa '+av+' aviso(s) de esa semana':'Cambio hecho y guardado'),1500)}}}
    catch(x){marca('Error: '+String(x.message).slice(0,60),1)}pintar();return}
  const a=e.target.closest('[data-a]')?.dataset.a;
  if(a==='salir'){e.preventDefault();SES=null;localStorage.removeItem('hz-ses');EMP=[];login();return}
  if(a==='ant'){semana=sumar(semana,-7);edit=null;pintar()}
  else if(a==='sig'){semana=sumar(semana,7);edit=null;pintar()}
  else if(a==='hoy'){semana=lunes(new Date());edit=null;pintar()}
  else if(a==='imprimir'){window.print()}
  else if(a==='aant'){anioVac--;pintar()}else if(a==='asig'){anioVac++;pintar()}
  else if(a==='irplantilla'){tab='plantilla';pintar()}else if(a==='irannual'){tab='anual';pintar()}else if(a==='irvac'){tab='vacaciones';pintar()}
  else if(a==='optgen'){OPT.busy=true;pintar();setTimeout(()=>{const c=ctxOpt(),k=iso(semana);OPT.seed=(OPT.k===k&&OPT.opts)?OPT.seed+1:1;OPT.k=k;OPT.ctx=c;OPT.opts=optimizar(c,OPT.seed);OPT.busy=false;pintar()},40)}
  else if(a==='optaplicar'){const o=OPT.opts[+e.target.closest('[data-o]').dataset.o],k=iso(semana);S.datos[k]={};EMP.forEach((m,i)=>{S.datos[k][m.n]=o.G[i].map(COD_TXT)});sucias.add(k);guardar();OPT.opts=null;tab='plantilla';edit=null;pintar()}
  else if(a==='copiar'){const p=e.target.closest('[data-p]').dataset.p,k=iso(semana);S.datos[k]={};EMP.forEach(m=>{S.datos[k][m.n]=[...filaEmp(p,m.n)]});sucias.add(k);guardar();pintar()}
  else if(a==='gturno'){filaEmp(edit.k,edit.e)[edit.i]=$('#turno-txt').value.trim();sucias.add(edit.k);guardar();edit=null;pintar()}
  else if(a==='bturno'){filaEmp(edit.k,edit.e)[edit.i]='';sucias.add(edit.k);guardar();edit=null;pintar()}
  else if(a==='cturno'){edit=null;pintar()}
  const d=e.target.closest('[data-del]');if(d){S[tab][iso(semana)].splice(+d.dataset.del,1);guardarAj();pintar()}
  const v=e.target.closest('[data-vdel]');if(v){S.vac.splice(+v.dataset.vdel,1);vacSucia=true;guardar();pintar()}
  const n=e.target.closest('[data-ndel]');if(n){S.notas.splice(+n.dataset.ndel,1);guardarAj();pintar()}
});
document.addEventListener('change',async e=>{const t=e.target.closest('[data-tel]');if(!t)return;const em=EMP.find(x=>x.id===t.dataset.tel);em.tel=t.value.trim();try{await api('hz_empleados?id=eq.'+em.id,{m:'PATCH',b:{tel:em.tel||null},h:{Prefer:'return=minimal'}});pintar()}catch(x){marca('Error: '+String(x.message).slice(0,60),1)}});
document.addEventListener('submit',async e=>{
  e.preventDefault();const f=e.target.id;
  if(f==='f-login'){try{await auth({email:$('#lm').value.trim(),password:$('#lp').value},'password');await arrancar()}catch(x){login(x.message)}}
  else if(f==='f-pers'){const tipo=e.target.dataset.tipo,k=iso(semana);(S[tipo][k]=S[tipo][k]||[]).push({n:$('#pn').value.trim(),rol:$('#pr').value.trim(),t:DIAS.map((_,i)=>$('#pt'+i).value.trim())});guardarAj();pintar()}
  else if(f==='f-vac'){if($('#vf').value<$('#vi').value)return;S.vac.push({e:$('#ve').value,t:$('#vt').value,i:$('#vi').value,f:$('#vf').value,n:$('#vn').value.trim()});vacSucia=true;guardar();pintar()}
  else if(f==='f-nota'){S.notas.push({f:$('#nf').value,t:$('#nt').value,x:$('#nx').value.trim()});guardarAj();pintar()}
});
async function arrancar(){
  $('#raiz').innerHTML='<div class="sub">Cargando…</div>';
  try{await cargarNube();esqueleto();pintar()}
  catch(x){if(!SES)login(x.message==='sesión'?'La sesión caducó, entra otra vez.':x.message);else $('#raiz').innerHTML=`<div class="card"><h3>No se pudo cargar</h3><div class="vacio-txt">${esc(String(x.message).slice(0,160))}</div><button class="btn pri" onclick="arrancar()">Reintentar</button></div>`}}
document.addEventListener('visibilitychange',()=>{if(!document.hidden&&SES&&EMP.length&&!sucias.size&&!vacSucia&&!ajSucio&&!edit)cargarNube().then(pintar).catch(()=>{})});
if(SES)arrancar();else login();
</script></body></html>
