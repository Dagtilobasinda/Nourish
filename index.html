<!doctype html>
<html lang="en"><head><meta charset="UTF-8"><meta name="viewport" content="width=device-width,initial-scale=1,viewport-fit=cover">
<title>Nourish</title>
<style>
:root{--bg:#F7F5F0;--ink:#2A2B28;--sage:#7D8F69;--sage-d:#5E6F4D;--soft:#E6EBDD;--line:#E4E0D6}
*{box-sizing:border-box}body{margin:0;background:var(--bg);color:var(--ink);font:15px/1.5 system-ui,sans-serif;padding-bottom:84px}
h1,h2{font-family:Georgia,serif;font-weight:600;margin:0 0 6px}h2{font-size:20px}
main{max-width:640px;margin:0 auto;padding:20px 16px;display:grid;gap:14px}
.card{background:#fff;border:1px solid var(--line);border-radius:16px;padding:18px}
input,select,textarea{width:100%;padding:10px 12px;border:1px solid var(--line);border-radius:12px;font:inherit;background:#fff;margin-top:6px}
button{font:inherit;cursor:pointer}.btn{background:var(--sage);color:#fff;border:0;border-radius:12px;padding:10px 16px}
.btn:hover{background:var(--sage-d)}.ghost{background:none;border:0;color:#777;font-size:13px}
.muted{color:#777;font-size:13px}.err{color:#a33;font-size:13px}.row{display:flex;justify-content:space-between;align-items:center;gap:8px;padding:4px 0}
.grid{display:grid;grid-template-columns:1fr 1fr;gap:8px}.bar{height:8px;background:var(--soft);border-radius:8px;margin-top:4px}.bar i{display:block;height:8px;background:var(--sage);border-radius:8px}
nav{position:fixed;bottom:0;left:0;right:0;background:#fff;border-top:1px solid var(--line);display:flex;justify-content:space-between;overflow-x:auto;padding:8px 4px calc(8px + env(safe-area-inset-bottom))}
nav button{white-space:nowrap;background:none;border:0;padding:8px 10px;border-radius:12px;color:#777;font-size:13px}nav .on{background:var(--soft);color:var(--sage-d)}
.chips{display:flex;gap:8px;flex-wrap:wrap}.chip{background:#fff;border:1px solid var(--line);border-radius:20px;padding:6px 12px;font-size:13px}.chip.on{background:var(--soft);border-color:var(--sage)}
.rc{cursor:pointer}ul,ol{margin:6px 0;padding-left:20px}
</style></head>
<body><div id="app"></div>
<script>
const MEALS=['Breakfast','Morning Snack','Lunch','Afternoon Snack','Dinner','Post-Workout']
const $=id=>document.getElementById(id)
const esc=s=>String(s).replace(/[&<>"']/g,c=>({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;'}[c]))
const uid=()=>Date.now().toString(36)+Math.random().toString(36).slice(2,7)
const todayStr=()=>{const d=new Date();return d.getFullYear()+'-'+String(d.getMonth()+1).padStart(2,'0')+'-'+String(d.getDate()).padStart(2,'0')}

// name, meal categories, minutes, kcal, protein, carbs, fat (per 1 serving, ESTIMATES), ingredients, steps
const R=[
['Tomato Sauce Pasta',['Lunch','Dinner'],15,563,22,83,18,['100 g dry pasta','150 g tomato sauce','10 g olive oil','20 g Parmesan','Garlic','Basil','Salt and pepper'],['Boil the pasta in salted water until al dente, about 9–10 minutes.','Warm the olive oil in a pan and cook sliced garlic for 30 seconds.','Add the tomato sauce and simmer for 5 minutes.','Toss in the drained pasta with a splash of pasta water.','Top with Parmesan, basil, salt and pepper.']],
['Eggs with Tomatoes and Bread',['Breakfast'],15,715,37,57,37,['3 eggs','150 g tomatoes','10 g olive oil','100 g bread','30 g cheese (optional)'],['Dice the tomatoes.','Heat the oil and cook the tomatoes for 4–5 minutes until soft.','Crack in the eggs, stir gently and cook to your liking.','Add the cheese in the last minute.','Serve with the bread.']],
['Chickpea Rice Bowl',['Lunch','Dinner'],10,575,23,80,18,['150 g cooked rice','100 g cooked chickpeas','100 g Greek yogurt','10 g olive oil','Cucumber','Tomatoes','Lemon','Spices'],['Warm the chickpeas with the olive oil and spices for 3 minutes.','Put the rice in a bowl and add the chickpeas.','Add chopped cucumber and tomatoes.','Top with the yogurt and a squeeze of lemon.']],
['Banana Oatmeal',['Breakfast'],10,696,30,96,23,['80 g oats','200 ml whole milk','1 banana','100 g Greek yogurt','Cinnamon','10 g peanut butter'],['Simmer the oats in the milk for 5 minutes, stirring.','Mash half the banana into the oats.','Pour into a bowl and add the yogurt and peanut butter.','Slice the rest of the banana on top and sprinkle cinnamon.']],
['Tuna and Chickpea Salad',['Lunch','Dinner'],10,433,42,35,14,['120 g tuna','100 g cooked chickpeas','Tomatoes','Cucumber','10 g olive oil','Lemon','Parsley'],['Drain the tuna and chickpeas.','Chop the tomatoes, cucumber and parsley.','Combine everything in a bowl.','Dress with olive oil and lemon juice, then season.']],
['Peanut Butter Banana Overnight Oats',['Breakfast'],5,755,33,98,28,['80 g oats','200 ml whole milk','100 g Greek yogurt','1 banana','20 g peanut butter','Cinnamon'],['Mix the oats, milk, yogurt, peanut butter and cinnamon in a jar.','Stir in half the mashed banana.','Refrigerate overnight.','Top with sliced banana in the morning.']],
['Avocado Cheese Egg Toast',['Breakfast'],12,659,37,38,40,['3 eggs','2 slices of bread','Half an avocado','30 g Parmesan','A little olive oil'],['Toast the bread.','Fry or scramble the eggs in a little olive oil.','Mash the avocado onto the toast.','Add the eggs and grate the Parmesan on top.']],
['Creamy Chicken Pesto Pasta',['Lunch','Dinner'],25,1003,63,82,46,['100 g dry pasta','120 g chicken breast','30 g pesto','30 g Parmesan','50 ml cream','Cherry tomatoes'],['Boil the pasta until al dente.','Slice the chicken and cook in a pan for 6–7 minutes until done.','Add halved cherry tomatoes for 2 minutes.','Stir in the pesto and cream and warm through.','Toss with the pasta and top with Parmesan.']],
['Mediterranean Tuna Rice Bowl',['Lunch','Dinner'],10,748,48,84,25,['150 g cooked rice','120 g tuna','100 g cooked chickpeas','Half an avocado','10 g olive oil','Lemon','Tomatoes','Cucumber'],['Put the rice in a bowl.','Add the tuna, chickpeas, sliced avocado, tomatoes and cucumber.','Drizzle with olive oil and lemon juice, then season.']],
['Beef Tomato Parmesan Pasta',['Lunch','Dinner'],25,793,49,83,30,['100 g dry penne','120 g lean ground beef','150 g tomato sauce','30 g Parmesan','10 g olive oil','Garlic','Basil'],['Boil the penne until al dente.','Brown the beef in the olive oil with garlic, about 6 minutes.','Add the tomato sauce and simmer for 8 minutes.','Toss with the penne, top with Parmesan and basil.']],
['Mass Gain Smoothie',['Morning Snack','Afternoon Snack','Post-Workout'],5,662,31,76,29,['300 ml whole milk','1 banana','40 g oats','20 g peanut butter','100 g Greek yogurt'],['Add everything to a blender.','Blend until smooth and drink right away.']],
['Greek Yogurt Power Bowl',['Breakfast','Afternoon Snack'],5,585,26,58,29,['200 g Greek yogurt','40 g granola','20 g walnuts','10 g honey','Strawberries or banana'],['Spoon the yogurt into a bowl.','Top with granola, walnuts and fruit.','Finish with the honey.']]
].map(r=>({id:'r'+r[0].length+r[3],name:r[0],cats:r[1],min:r[2],cal:r[3],p:r[4],c:r[5],f:r[6],ing:r[7],steps:r[8]}))

const DEF={recipes:[],favs:[],goals:{calories:2400,protein_g:100,carbs_g:300,fat_g:80,water_ml:2500,target_kg:70},entries:[],water:[],weights:[{id:uid(),date:todayStr(),kg:54.6,note:'Starting weight'}]}
let D;try{D=JSON.parse(localStorage.getItem('nourish_v1'))}catch(e){}
D=Object.assign({},DEF,D||{});D.goals=Object.assign({},DEF.goals,D.goals)
const save=()=>{try{localStorage.setItem('nourish_v1',JSON.stringify(D))}catch(e){alert('Could not save data in this browser.')}}
let S={range:'7',cm:todayStr().slice(0,7),edit:null,img:'',tab:'home',date:todayStr(),view:null,filter:'All',msg:''}

const E=()=>D.entries.filter(e=>e.date===S.date),W=()=>D.water.filter(w=>w.date===S.date)
const sum=k=>Math.round(E().reduce((a,e)=>a+Number(e[k]),0)),wt=()=>W().reduce((a,w)=>a+w.ml,0)
const bar=(l,v,m,u)=>`<div style="margin-bottom:10px"><div class="row"><span>${l}</span><span class="muted">${v} / ${m} ${u}</span></div><div class="bar"><i style="width:${m?Math.min(100,v/m*100):0}%"></i></div></div>`

function donut(P=sum('p'),C=sum('c'),F=sum('f')){const p=P*4,c=C*4,f=F*9,t=p+c+f,cols=['#7D8F69','#C9B99A','#A9B4C2'],v=[p,c,f],n=['Protein','Carbs','Fat'];let off=0,a=''
 if(t)v.forEach((x,i)=>{const l=x/t*251.2;a+=`<circle r="40" cx="50" cy="50" fill="none" stroke="${cols[i]}" stroke-width="14" stroke-dasharray="${l} ${251.2-l}" stroke-dashoffset="${-off}" transform="rotate(-90 50 50)"/>`;off+=l})
 else a='<circle r="40" cx="50" cy="50" fill="none" stroke="#E6EBDD" stroke-width="14"/>'
 return `<div class="card row" style="gap:20px"><svg width="120" height="120" viewBox="0 0 100 100">${a}</svg><div>${n.map((x,i)=>`<div><span style="color:${cols[i]}">●</span> ${x} ${t?Math.round(v[i]/t*100):0}% of calories</div>`).join('')}</div></div>`}

function home(){const g=D.goals,c=sum('calories'),p=sum('p'),left=g.calories-c,w=D.weights.slice().sort((a,b)=>a.date<b.date?-1:1),cur=w.length?w[w.length-1].kg:null
 return `<div class="card"><div class="muted">Calories today</div><h1>${c} <span class="muted">/ ${g.calories} kcal</span></h1><div>${Math.round(c/g.calories*100)}% of your target · ${left>=0?left+' kcal remaining':(-left)+' kcal above target'}</div></div>
 <div class="card">${bar('Protein',p,g.protein_g,'g')}${bar('Carbohydrates',sum('c'),g.carbs_g,'g')}${bar('Fat',sum('f'),g.fat_g,'g')}${bar('Water',wt(),g.water_ml,'ml')}</div>${donut()}
 ${c>0&&p<g.protein_g?`<div class="muted">You need about ${g.protein_g-p} g more protein to reach your target.</div>`:''}
 ${cur?`<div class="card">${bar('Weight',cur,g.target_kg,'kg')}<div class="muted">${(g.target_kg-cur).toFixed(1)} kg remaining to your target.</div></div>`:''}`}

function diary(){const rows=MEALS.map(m=>{const it=E().filter(e=>e.meal===m);return it.length?`<div class="card"><b>${m}</b>${it.map(e=>`<div class="row"><span>${esc(e.name)} × ${e.s}</span><span class="muted">${Math.round(e.calories)} kcal · ${Math.round(e.p)} g protein <button class="ghost" onclick="delE('${e.id}')">Remove</button></span></div>`).join('')}</div>`:''}).join('')
 return `<input type="date" value="${S.date}" onchange="if(this.value){S.date=this.value;render()}" style="max-width:190px">
 <div class="card"><b>Quick add</b><input id="n" placeholder="Food name"><select id="m">${MEALS.map(m=>`<option>${m}</option>`).join('')}</select>
 <div class="grid"><input id="s" type="number" min="0" step="0.25" value="1" placeholder="Servings"><input id="c" type="number" min="0" placeholder="Calories per serving"><input id="p" type="number" min="0" placeholder="Protein (g)"><input id="cb" type="number" min="0" placeholder="Carbs (g)"><input id="f" type="number" min="0" placeholder="Fat (g)"></div>
 <p id="e" class="err"></p><button class="btn" onclick="quick()">Add to diary</button></div>
 ${rows||'<div class="muted">Nothing logged for this day yet. Use quick add, or open a recipe and add it to your diary.</div>'}`}

function recipes(){
 if(S.edit)return recForm()
 if(S.view){const r=ALL().find(x=>x.id===S.view);if(!r){S.view=null;return recipes()}
  const fav=D.favs.includes(r.id)
  return `<button class="ghost" onclick="S.view=null;render()">‹ Back to recipes</button><div class="card">${r.img?`<img src="${r.img}" style="width:100%;border-radius:12px;margin-bottom:10px">`:''}<h2>${esc(r.name)}</h2>${r.desc?`<div>${esc(r.desc)}</div>`:''}
  <div class="muted">${r.cats.join(' / ')} · ${r.min} min · per serving${r.custom?'':' (estimates)'}</div>
  <p><b>${r.cal} kcal</b> · ${r.p} g protein · ${r.c} g carbs · ${r.f} g fat</p>
  <b>Ingredients (1 serving)</b><ul>${r.ing.map(i=>`<li>${esc(i)}</li>`).join('')}</ul><b>Steps</b><ol>${r.steps.map(i=>`<li>${esc(i)}</li>`).join('')}</ol>
  <div class="chips"><button class="chip" onclick="favR('${r.id}')">${fav?'★ Favorite':'☆ Favorite'}</button><button class="chip" onclick="dupR('${r.id}')">Duplicate</button>${r.custom?`<button class="chip" onclick="editR('${r.id}')">Edit</button><button class="chip" onclick="delR('${r.id}')">Delete</button>`:''}</div></div>
  <div class="card"><b>Add to diary</b><input type="date" id="rd" value="${S.date}"><select id="rm">${MEALS.map(m=>`<option ${r.cats.includes(m)?'selected':''}>${m}</option>`).join('')}</select>
  <input id="rs" type="number" min="0" step="0.25" value="1" placeholder="Servings"><p></p><button class="btn" onclick="addR('${r.id}')">Add to diary</button></div>`}
 const fl=['All','Favorites','Breakfast','Lunch','Dinner','Snack','High protein','Under 20 min'],ok=r=>S.filter=='All'||(S.filter=='Favorites'?D.favs.includes(r.id):S.filter=='Snack'?r.cats.some(c=>/Snack|Post/.test(c)):S.filter=='High protein'?r.p>=35:S.filter=='Under 20 min'?r.min<20:r.cats.includes(S.filter))
 return `<button class="btn" onclick="newR()">+ New recipe</button><div class="chips">${fl.map(f=>`<button class="chip ${S.filter==f?'on':''}" onclick="S.filter='${f}';render()">${f}</button>`).join('')}</div>
 ${ALL().filter(ok).map(r=>`<div class="card rc row" onclick="S.view='${r.id}';render()" style="gap:12px">${r.img?`<img src="${r.img}" style="width:64px;height:64px;object-fit:cover;border-radius:12px">`:''}<div style="flex:1"><b>${D.favs.includes(r.id)?'★ ':''}${esc(r.name)}</b><div class="muted">${r.cats.join(' / ')} · ${r.min} min</div><div>${r.cal} kcal · ${r.p} g protein ${r.custom?'':'<span class="muted">(estimate)</span>'}</div></div></div>`).join('')||'<div class="muted">No recipes match this filter.</div>'}`}

function water(){return `<div class="card">${bar('Water',wt(),D.goals.water_ml,'ml')}</div><div class="chips">${[150,250,500].map(n=>`<button class="btn" onclick="addW(${n})">+${n} ml</button>`).join('')}</div>
 <div class="grid"><input id="w" type="number" min="1" placeholder="Custom ml"><button class="btn" onclick="addW(Number($('w').value))">Add</button></div>
 <div class="card">${W().length?W().map(w=>`<div class="row">${w.ml} ml<button class="ghost" onclick="delW('${w.id}')">Remove</button></div>`).join(''):'<span class="muted">No water logged for this day.</span>'}</div>`}

function weight(){const w=D.weights.slice().sort((a,b)=>a.date<b.date?1:-1)
 return `<div class="card"><b>Add weight</b><input type="date" id="wd" value="${S.date}"><input id="wk" type="number" step="0.1" min="0" placeholder="Weight (kg)"><input id="wn" placeholder="Note (optional)"><p id="we" class="err"></p><button class="btn" onclick="addWt()">Save weight</button></div>
 <div class="card"><b>History</b>${w.length?w.map(x=>`<div class="row"><span>${x.date} · <b>${x.kg} kg</b> <span class="muted">${esc(x.note||'')}</span></span><button class="ghost" onclick="delWt('${x.id}')">Remove</button></div>`).join(''):'<div class="muted">No weights yet.</div>'}</div>`}

function settings(){const g=D.goals,f=[['calories','Calories (kcal)'],['protein_g','Protein (g)'],['carbs_g','Carbohydrates (g)'],['fat_g','Fat (g)'],['water_ml','Water (ml)'],['target_kg','Target weight (kg)']]
 return `<div class="card"><b>Daily targets</b>${f.map(([k,l])=>`<label class="muted">${l}<input id="g_${k}" type="number" min="0" step="any" value="${g[k]}"></label>`).join('')}<p class="muted">${esc(S.msg)}</p><button class="btn" onclick="saveG()">Save targets</button></div>
 <div class="card"><b>Backup</b><p class="muted">Your data is stored only in this browser. Download a backup now and then.</p><div class="chips"><button class="btn" onclick="backup()">Download backup</button><button class="btn" onclick="csv()">Export CSV</button></div>
 <p></p><input type="file" accept=".json" onchange="restore(this.files[0])"></div>`}

function render(){const t=new Date(S.date+'T00:00').toLocaleDateString('en',{weekday:'long',month:'long',day:'numeric'})
 const tabs=[['home','Today'],['diary','Diary'],['recipes','Recipes'],['water','Water'],['weight','Weight'],['stats','Stats'],['cal','Calendar'],['settings','Settings']]
 $('app').innerHTML=`<main><h1>${t}</h1>${({home,diary,recipes,water,weight,stats,cal:calendar,settings}[S.tab])()}</main><nav>${tabs.map(([i,l])=>`<button class="${S.tab==i?'on':''}" onclick="S.tab='${i}';S.view=null;S.edit=null;render()">${l}</button>`).join('')}</nav>`}

function quick(){const s=Number($('s').value),c=$('c').value,n=$('n').value.trim()
 if(!n||!(s>0)||c===''||Number(c)<0){$('e').textContent='Add a name, calories, and a serving amount above 0.';return}
 D.entries.push({id:uid(),date:S.date,meal:$('m').value,name:n,s,calories:c*s,p:($('p').value||0)*s,c:($('cb').value||0)*s,f:($('f').value||0)*s});save();render()}
function addR(id){const r=ALL().find(x=>x.id===id),s=Number($('rs').value),d=$('rd').value;if(!(s>0)||!d)return alert('Choose a date and servings above 0.')
 D.entries.push({id:uid(),date:d,meal:$('rm').value,name:r.name,s,calories:r.cal*s,p:r.p*s,c:r.c*s,f:r.f*s});save();S.date=d;S.tab='diary';S.view=null;render()}
const delE=id=>{D.entries=D.entries.filter(e=>e.id!=id);save();render()}
const addW=n=>{if(!(n>0))return;D.water.push({id:uid(),date:S.date,ml:Math.round(n)});save();render()}
const delW=id=>{D.water=D.water.filter(w=>w.id!=id);save();render()}
function addWt(){const k=Number($('wk').value),d=$('wd').value;if(!(k>0)||!d){$('we').textContent='Enter a date and a weight above 0.';return}
 D.weights.push({id:uid(),date:d,kg:k,note:$('wn').value.trim()});save();render()}
const delWt=id=>{D.weights=D.weights.filter(w=>w.id!=id);save();render()}
function saveG(){Object.keys(D.goals).forEach(k=>{const v=Number($('g_'+k).value);if(v>0)D.goals[k]=v});save();S.msg='Saved';render()}
function backup(){const a=document.createElement('a');a.href=URL.createObjectURL(new Blob([JSON.stringify(D)],{type:'application/json'}));a.download='nourish-backup.json';a.click()}
function restore(f){if(!f)return;const r=new FileReader();r.onload=()=>{try{const x=JSON.parse(r.result);if(!x.goals||!x.entries)throw 0;D=Object.assign({},DEF,x);save();render();alert('Backup restored.')}catch(e){alert('This is not a valid backup file.')}};r.readAsText(f)}
const ALL=()=>R.concat(D.recipes)
const pad=n=>String(n).padStart(2,'0')
const addDays=(d,n)=>{const x=new Date(d+'T00:00');x.setDate(x.getDate()+n);return x.getFullYear()+'-'+pad(x.getMonth()+1)+'-'+pad(x.getDate())}
function recForm(){const n=S.edit=='new',r=n?{cats:['Lunch'],min:10,cal:'',p:'',c:'',f:'',ing:[],steps:[]}:ALL().find(x=>x.id==S.edit)
 return `<button class="ghost" onclick="S.edit=null;render()">‹ Cancel</button><div class="card"><h2>${n?'New recipe':'Edit recipe'}</h2>
 <input id="rn" placeholder="Recipe name" value="${esc(r.name||'')}"><input id="rdsc" placeholder="Short description" value="${esc(r.desc||'')}">
 <select id="rcat">${MEALS.map(m=>`<option ${r.cats[0]==m?'selected':''}>${m}</option>`).join('')}</select>
 <div class="grid"><input id="rmin" type="number" min="0" placeholder="Minutes" value="${r.min}"><input id="rk" type="number" min="0" placeholder="Calories per serving" value="${r.cal}"><input id="rpp" type="number" min="0" placeholder="Protein (g)" value="${r.p}"><input id="rcc" type="number" min="0" placeholder="Carbs (g)" value="${r.c}"><input id="rff" type="number" min="0" placeholder="Fat (g)" value="${r.f}"></div>
 <textarea id="ri" rows="4" placeholder="Ingredients, one per line (e.g. 100 g oats)">${esc(r.ing.join('\n'))}</textarea><textarea id="rst" rows="4" placeholder="Steps, one per line">${esc(r.steps.join('\n'))}</textarea>
 <p class="muted">Photo (optional)</p><input type="file" accept="image/*" onchange="pickImg(this.files[0])"><img id="pv" src="${S.img}" style="max-width:100%;border-radius:12px;margin-top:8px;${S.img?'':'display:none'}">
 <p id="re" class="err"></p><button class="btn" onclick="saveR()">Save recipe</button></div>`}
function newR(){S.edit='new';S.img='';render()}
function editR(id){S.edit=id;S.img=ALL().find(x=>x.id==id).img||'';render()}
function pickImg(f){if(!f)return;const fr=new FileReader();fr.onload=()=>{const im=new Image();im.onload=()=>{const k=Math.min(1,520/Math.max(im.width,im.height)),c=document.createElement('canvas');c.width=im.width*k;c.height=im.height*k;c.getContext('2d').drawImage(im,0,0,c.width,c.height);S.img=c.toDataURL('image/jpeg',.7);const v=$('pv');v.src=S.img;v.style.display='block'};im.src=fr.result};fr.readAsDataURL(f)}
function saveR(){const n=$('rn').value.trim(),k=$('rk').value,lines=x=>$(x).value.split('\n').map(a=>a.trim()).filter(Boolean)
 if(!n||k===''||Number(k)<0){$('re').textContent='Add a recipe name and calories per serving.';return}
 const o={name:n,desc:$('rdsc').value.trim(),cats:[$('rcat').value],min:Number($('rmin').value)||0,cal:Number(k),p:Number($('rpp').value)||0,c:Number($('rcc').value)||0,f:Number($('rff').value)||0,ing:lines('ri'),steps:lines('rst'),img:S.img,custom:true}
 if(S.edit=='new'){o.id=uid();D.recipes.push(o)}else{o.id=S.edit;D.recipes=D.recipes.map(x=>x.id==S.edit?o:x)}
 save();S.view=o.id;S.edit=null;render()}
function dupR(id){const r=ALL().find(x=>x.id==id),o=Object.assign({},r,{id:uid(),name:r.name+' (copy)',custom:true});D.recipes.push(o);save();S.view=o.id;render()}
function delR(id){if(!confirm('Delete this recipe? Diary entries stay.'))return;D.recipes=D.recipes.filter(x=>x.id!=id);D.favs=D.favs.filter(x=>x!=id);save();S.view=null;render()}
function favR(id){D.favs=D.favs.includes(id)?D.favs.filter(x=>x!=id):D.favs.concat(id);save();render()}
function dayT(d){const e=D.entries.filter(x=>x.date==d),sm=k=>e.reduce((a,x)=>a+Number(x[k]),0);return{n:e.length,cal:sm('calories'),p:sm('p'),c:sm('c'),f:sm('f'),w:D.water.filter(x=>x.date==d).reduce((a,x)=>a+x.ml,0)}}
function chart(v,l,t,col){const W=320,H=110,m=Math.max(t||0,...v,1),bw=W/v.length,ty=H-(t||0)/m*H
 return `<svg viewBox="0 0 ${W} ${H+16}" width="100%"><line x1="0" x2="${W}" y1="${ty}" y2="${ty}" stroke="#C9B99A" stroke-dasharray="4"/>${v.map((x,i)=>`<rect x="${i*bw+bw*.15}" y="${H-x/m*H}" width="${bw*.7}" height="${x/m*H}" rx="2" fill="${col}"/>`).join('')}<text x="0" y="${H+13}" font-size="9" fill="#777">${l[0]}</text><text x="${W}" y="${H+13}" font-size="9" fill="#777" text-anchor="end">${l[l.length-1]}</text></svg>`}
function stats(){const b=todayStr();let a=b,e=b
 if(S.range=='7')a=addDays(b,-6);else if(S.range=='30')a=addDays(b,-29);else if(S.range=='c'){a=S.from||addDays(b,-6);e=S.to||b}
 const ds=[];for(let d=a;d<=e&&ds.length<366;d=addDays(d,1))ds.push(d)
 const T=ds.map(dayT),lg=T.filter(t=>t.n>0),L=lg.length,g=D.goals,avg=k=>L?Math.round(lg.reduce((x,t)=>x+t[k],0)/L):0,tot=k=>lg.reduce((x,t)=>x+t[k],0)
 const hit=lg.filter(t=>t.cal>=g.calories).length,wl=T.filter(t=>t.w>0),lab=ds.map(d=>d.slice(5))
 const opts=[['1','Today'],['7','Last 7 days'],['30','Last 30 days'],['c','Custom']]
 return `<div class="chips">${opts.map(([k,l])=>`<button class="chip ${S.range==k?'on':''}" onclick="S.range='${k}';render()">${l}</button>`).join('')}</div>
 ${S.range=='c'?`<div class="grid"><input type="date" value="${a}" onchange="S.from=this.value;render()"><input type="date" value="${e}" onchange="S.to=this.value;render()"></div>`:''}
 ${L?`<div class="card"><b>Calories vs target</b><div class="muted">Dashed line = ${g.calories} kcal target</div>${chart(T.map(t=>Math.round(t.cal)),lab,g.calories,'#7D8F69')}</div>
 <div class="card"><b>Protein</b><div class="muted">Dashed line = ${g.protein_g} g target</div>${chart(T.map(t=>Math.round(t.p)),lab,g.protein_g,'#A9B4C2')}</div>
 <div class="card"><b>Water</b><div class="muted">Dashed line = ${g.water_ml} ml target</div>${chart(T.map(t=>t.w),lab,g.water_ml,'#9DB7C4')}</div>
 <div class="card"><b>Macro split of calories</b></div>${donut(tot('p'),tot('c'),tot('f'))}
 <div class="card"><b>Insights</b><ul><li>You logged food on ${L} of ${ds.length} day${ds.length>1?'s':''}.</li><li>Average on logged days: ${avg('cal')} kcal and ${avg('p')} g protein.</li><li>You reached your calorie target on ${hit} of those days.</li>${wl.length?`<li>Average water on days with water logged: ${Math.round(wl.reduce((x,t)=>x+t.w,0)/wl.length)} ml.</li>`:''}</ul><div class="muted">Based only on days you recorded.</div></div>`
 :'<div class="card muted">No food logged in this period yet. Add meals in the Diary tab and your charts will appear here.</div>'}`}
function calendar(){const [y,m]=S.cm.split('-').map(Number),off=(new Date(y,m-1,1).getDay()+6)%7,nd=new Date(y,m,0).getDate(),g=D.goals
 let c='';for(let i=0;i<off;i++)c+='<div></div>'
 for(let i=1;i<=nd;i++){const d=S.cm+'-'+pad(i),t=dayT(d);c+=`<div onclick="goDay('${d}')" style="border:1px solid ${d==todayStr()?'var(--sage)':'var(--line)'};border-radius:10px;padding:4px;min-height:60px;font-size:11px;cursor:pointer;background:#fff"><b>${i}</b>${t.n?`<div>${Math.round(t.cal)} kcal${t.cal>=g.calories?' ✓':''}</div><div class="muted">${Math.round(t.p)} g P</div>`:''}${t.w?`<div class="muted">${t.w} ml</div>`:''}</div>`}
 return `<div class="row"><button class="chip" onclick="shiftM(-1)">‹</button><b>${new Date(y,m-1,1).toLocaleDateString('en',{month:'long',year:'numeric'})}</b><button class="chip" onclick="shiftM(1)">›</button></div>
 <div style="display:grid;grid-template-columns:repeat(7,1fr);gap:4px"><div class="muted">Mon</div><div class="muted">Tue</div><div class="muted">Wed</div><div class="muted">Thu</div><div class="muted">Fri</div><div class="muted">Sat</div><div class="muted">Sun</div>${c}</div>
 <div class="muted">✓ = calorie target reached. Tap a day to open its diary.</div>`}
function shiftM(n){const [y,m]=S.cm.split('-').map(Number),d=new Date(y,m-1+n,1);S.cm=d.getFullYear()+'-'+pad(d.getMonth()+1);render()}
function goDay(d){S.date=d;S.tab='diary';render()}
function csv(){const rows=[['date','meal','food','servings','kcal','protein_g','carbs_g','fat_g']].concat(D.entries.slice().sort((a,b)=>a.date<b.date?-1:1).map(e=>[e.date,e.meal,e.name,e.s,Math.round(e.calories),Math.round(e.p),Math.round(e.c),Math.round(e.f)]))
 const t=rows.map(r=>r.map(x=>'"'+String(x).replace(/"/g,'""')+'"').join(',')).join('\n'),a=document.createElement('a');a.href=URL.createObjectURL(new Blob([t],{type:'text/csv'}));a.download='nourish-diary.csv';a.click()}

render()
</script></body></html>
