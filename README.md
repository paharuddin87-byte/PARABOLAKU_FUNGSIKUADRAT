<!DOCTYPE html>
<html lang="id"><head><meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>ParabolaKu – Grafik Fungsi Kuadrat</title>
<style>
:root{--n:#16294d;--m:#7a1f2e;--b:#eceef2;--t:#1c2333;box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}
*{box-sizing:inherit}body{margin:0;background:var(--b);color:var(--t);font:16px/1.65 system-ui,sans-serif}
h1,h2,h3{font-family:Georgia,serif;color:var(--n);margin:.2em 0 .5em}
header{background:var(--n);color:#fff;padding:14px 18px;border-bottom:4px solid var(--m)}
header b{font:700 22px Georgia,serif}header small{display:block;opacity:.8}
nav{display:flex;gap:6px;overflow-x:auto;background:#fff;padding:8px;position:sticky;top:0;z-index:5;box-shadow:0 2px 6px #0002}
button{font:inherit;cursor:pointer;border:0;border-radius:10px;padding:10px 16px;background:var(--n);color:#fff}
button.m{background:var(--m)}nav button{background:transparent;color:var(--n);white-space:nowrap}nav button.on{background:var(--n);color:#fff}
main{max-width:860px;margin:auto;padding:12px}.pg{display:none}.pg.on{display:block}
.c{background:#fff;border-radius:14px;padding:16px;margin:12px 0;box-shadow:0 2px 10px #16294d1a;border-top:4px solid var(--m)}
.tb{overflow-x:auto}table{border-collapse:collapse;width:100%}td,th{border:1px solid #ccd;padding:8px;text-align:left}th{background:var(--n);color:#fff}
canvas{width:100%;display:block;border:1px solid #dde;border-radius:10px}
.o{display:block;width:100%;text-align:left;margin:8px 0;background:#fff;color:var(--t);border:2px solid #c9cedb}
.o.ok{background:#e3f4e6;border-color:#2e7d32}.o.no{background:#fbe4e4;border-color:var(--m)}
input[type=range]{width:100%;accent-color:var(--m)}input[type=number],input[type=text]{width:90px;font:inherit;padding:8px;border:2px solid #c9cedb;border-radius:8px}
.f{font:italic 20px Georgia,serif;color:var(--m);text-align:center}.hid{display:none!important}
.sp{position:fixed;inset:0;background:linear-gradient(160deg,var(--n),#0b1730 70%);color:#fff;display:flex;flex-direction:column;align-items:center;justify-content:center;text-align:center;z-index:9;padding:20px}
.sp{--img:url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 800 600'%3E%3Crect width='800' height='600' fill='%230b1730'/%3E%3Cpath d='M0 300H800M400 0V600M0 150H800M0 450H800M200 0V600M600 0V600' stroke='%23ffffff18'/%3E%3Cpath d='M100 0Q400 900 700 0' fill='none' stroke='%23c9566a88' stroke-width='6'/%3E%3Cpath d='M100 600Q400 -300 700 600' fill='none' stroke='%23e0b25255' stroke-width='4'/%3E%3C/svg%3E");background:linear-gradient(160deg,#16294de6,#7a1f2ecc),var(--img) center/cover;transition:opacity .5s}
.sp h1{color:#fff;font-size:44px;margin:.1em;text-shadow:0 3px 12px #0008}.sp svg{width:220px;max-width:70%}.sp svg path:first-child{stroke-dasharray:500;stroke-dashoffset:500;animation:dr 2s forwards}@keyframes dr{to{stroke-dashoffset:0}}
.ld{width:min(280px,80%);height:10px;background:#ffffff33;border-radius:9px;overflow:hidden;margin:18px auto 6px}.ld i{display:block;height:100%;width:0;background:linear-gradient(90deg,#e0b252,#f5d98a);border-radius:9px;transition:width .2s}
.go{font-size:20px;padding:14px 44px;margin-top:14px;background:linear-gradient(135deg,#e0b252,#f5d98a);color:#16294d;font-weight:700;box-shadow:0 6px 18px #0006}.go:active{transform:scale(.96)}
</style></head><body>
<div class="sp" id="sp"><svg viewBox="0 0 220 130"><path d="M20 10 Q110 250 200 10" fill="none" stroke="#c9566a" stroke-width="5"/><path d="M10 100H210M110 5V125" stroke="#ffffff88" stroke-width="2"/><circle cx="110" cy="72" r="6" fill="#fff"/></svg>
<h1>📈 ParabolaKu</h1><p>Grafik Fungsi Kuadrat · Matematika Fase E (Kelas X)</p><div class="ld"><i id="ldb"></i></div><small id="ldt">Memuat… 0%</small><button class="go hid" id="sb0" onclick="mulaiApp()">Mulai ▶</button></div>
<header><b>📈 ParabolaKu</b><small>Web Interaktif Grafik Fungsi Kuadrat</small></header>
<nav id="nv"></nav>
<main>
<section class="pg" id="p0"><div class="c"><h2>Selamat Datang!</h2>
<p><b>Masalah:</b> banyak murid hanya menghafal rumus titik puncak dan sumbu simetri, sehingga sulit memahami mengapa grafik berubah ketika koefisien a, b, c berubah, dan sulit menggambar sketsa grafik fungsi kuadrat.</p></div>
<div class="c"><h3>Tujuan Pembelajaran</h3><ol><li>Menjelaskan pengaruh koefisien a, b, c dan diskriminan terhadap grafik fungsi kuadrat.</li><li>Menentukan titik potong sumbu, sumbu simetri, dan titik puncak.</li><li>Menggambar sketsa grafik secara runtut.</li><li>Menyelesaikan masalah kontekstual nilai maksimum/minimum.</li></ol></div>
<div class="c"><h3>Alur Belajar</h3><ol><li><b>Konsep</b> – pahami rumus dan unsur parabola</li><li><b>Eksplorasi</b> – ubah a, b, c dan amati grafiknya</li><li><b>Langkah Melukis</b> – gambar sketsa secara runtut</li><li><b>Latihan</b> – soal acak 3 tingkat</li><li><b>Masalah Nyata</b> – lintasan bola dan nilai maksimum</li><li><b>Kuis Akhir</b> – 10 soal acak, target skor ≥ 75</li></ol><button class="m" onclick="go(1)">Mulai belajar →</button></div></section>

<section class="pg" id="p1"><div class="c"><h2>Konsep Dasar</h2><p>Fungsi kuadrat berbentuk</p><p class="f">f(x) = ax² + bx + c, dengan a ≠ 0</p><p>Grafiknya berupa kurva simetris yang disebut <b>parabola</b>.</p>
<div class="tb"><table><tr><th>Unsur</th><th>Rumus / Ketentuan</th></tr>
<tr><td>Arah bukaan</td><td>a &gt; 0 terbuka ke atas (ada nilai minimum); a &lt; 0 terbuka ke bawah (ada nilai maksimum)</td></tr>
<tr><td>Diskriminan</td><td>D = b² − 4ac</td></tr>
<tr><td>Titik potong sumbu y</td><td>(0, c)</td></tr>
<tr><td>Titik potong sumbu x</td><td>x = (−b ± √D) / (2a), ada jika D ≥ 0</td></tr>
<tr><td>Sumbu simetri</td><td>x = −b / (2a)</td></tr>
<tr><td>Titik puncak</td><td>( −b/(2a) , −D/(4a) )</td></tr>
<tr><td>Nilai ekstrem</td><td>y = −D/(4a)</td></tr></table></div></div>
<div class="c"><h3>Pengaruh a, b, c, dan D</h3><ul>
<li><b>a</b>: tanda a menentukan arah bukaan; makin besar |a| grafik makin sempit, makin kecil |a| makin lebar.</li>
<li><b>b</b>: bersama a menentukan sumbu simetri x = −b/(2a). Jika a dan b bertanda sama, sumbu simetri di kiri sumbu y; jika berbeda tanda, di kanan; jika b = 0, sumbu simetri adalah sumbu y.</li>
<li><b>c</b>: titik potong sumbu y, yaitu (0, c). Mengubah c menggeser grafik naik atau turun.</li>
<li><b>D &gt; 0</b>: memotong sumbu x di dua titik. <b>D = 0</b>: menyinggung sumbu x di satu titik (puncak berada di sumbu x). <b>D &lt; 0</b>: tidak memotong sumbu x (a &gt; 0: seluruh grafik di atas sumbu x; a &lt; 0: di bawah sumbu x).</li></ul></div>
<div class="c"><h3>Contoh</h3><p>f(x) = x² − 4x + 3 → a = 1, b = −4, c = 3. D = 16 − 12 = 4. Titik potong y: (0, 3). Titik potong x: (4 ± 2)/2 → x = 1 dan x = 3. Sumbu simetri x = 4/2 = 2. Puncak: (2, −D/4a) = (2, −1).</p><button class="m" onclick="go(2)">Lanjut ke Eksplorasi →</button></div></section>

<section class="pg" id="p2"><div class="c"><h2>Eksplorasi Grafik</h2><p class="f" id="fx"></p><canvas id="ce"></canvas>
<p>a = <b id="va"></b><input type="range" id="sa" min="-3" max="3" step="0.5" value="1"></p>
<p>b = <b id="vb"></b><input type="range" id="sb" min="-8" max="8" step="0.5" value="-4"></p>
<p>c = <b id="vc"></b><input type="range" id="sc" min="-8" max="8" step="0.5" value="3"></p>
<div class="tb"><table id="tu"></table></div></div>
<div class="c"><h3>🎯 Tantangan</h3><p id="chq"></p><p id="chf"></p><button class="m" onclick="ci=(ci+1)%CH.length;ex()">Tantangan lain</button></div></section>

<section class="pg" id="p3"><div class="c"><h2>Langkah Melukis Grafik</h2><p>Masukkan koefisien fungsi f(x) = ax² + bx + c lalu ikuti enam langkahnya.</p>
a <input type="number" id="ia" value="1"> b <input type="number" id="ib" value="-4"> c <input type="number" id="ic" value="3">
<p><button class="m" onclick="mulai()">Mulai</button> <button onclick="nxt()">Langkah berikutnya</button> <button onclick="acak()">Contoh acak</button></p><p id="msg"></p><canvas id="cl"></canvas><div id="stl"></div></div></section>

<section class="pg" id="p4"><div class="c"><h2>Latihan Bertingkat</h2><p>Pilih tingkat kesulitan. Soal dibangkitkan secara acak dan jawabannya dihitung otomatis dari rumus.</p><div id="lvb"></div><p id="lsc"></p></div><div class="c" id="lq"></div><button id="ln" class="m hid" onclick="lat()">Soal berikutnya →</button></section>

<section class="pg" id="p5"><div class="c"><h2>Masalah Nyata: Lintasan Bola</h2><p>Tinggi bola yang ditendang ke atas: <b>h(t) = −5t² + vt</b> (h dalam meter, t dalam detik, v kecepatan awal m/s).</p>
<p>v = <b id="vv"></b> m/s<input type="range" id="v" min="10" max="50" step="5" value="20"></p><canvas id="cm"></canvas><p id="mi"></p></div>
<div class="c"><h3>Soal Kontekstual</h3><p id="pq"></p><input type="text" id="ai" inputmode="decimal"> <button onclick="cek()">Periksa</button> <button class="m" onclick="np()">Soal baru</button><p id="pf"></p></div></section>

<section class="pg" id="p6"><div class="c"><h2>Kuis Akhir</h2><p>10 soal acak dari bank 30 soal. Target: skor ≥ 75.</p><p id="kp"></p><div id="kq"></div></div></section>

<section class="pg" id="p7"><div class="c"><h2>Pengembang</h2><p><b>Paharuddin, S.Pd</b><br>SMA Negeri 22 Bone<br>Mata Pelajaran Matematika · Fase E (Kelas X)<br>Karya: ParabolaKu v1.0 – Aplikasi Website<br>Periode pengembangan: 1–10 November 2026</p>
<p>Seluruh rumus bersumber dari materi fungsi kuadrat Kurikulum Merdeka Fase E. Soal dibangkitkan program dan kunci jawaban dihitung langsung dari rumus, sehingga jawaban dan pembahasan selalu konsisten.</p></div></section>
</main>
<script>
/*L*/
const $=s=>document.querySelector(s),fm=n=>{n=Math.round(n*100)/100;if(!n)n=0;return String(n).replace('-','−').replace('.',',')};
const rng=a=>()=>{a|=0;a=a+0x6D2B79F5|0;let t=Math.imul(a^a>>>15,1|a);t=t+Math.imul(t^t>>>7,61|t)^t;return((t^t>>>14)>>>0)/4294967296};
const ri=(r,l,h)=>l+Math.floor(r()*(h-l+1)),pick=(r,A)=>A[Math.floor(r()*A.length)],nz=(r,l,h)=>{let x;do x=ri(r,l,h);while(!x);return x};
const xm=p=>p<0?'x + '+fm(-p):'x − '+fm(p),sg=n=>n<0?'− '+fm(-n):'+ '+fm(n),P=(x,y)=>`(${fm(x)}, ${fm(y)})`;
function fx(a,b,c){let s='';const t=(k,v)=>{if(!k)return;const ab=Math.abs(k);s+=(s?(k<0?' − ':' + '):(k<0?'−':''))+((v&&ab==1)?'':fm(ab))+v};t(a,'x²');t(b,'x');t(c,'');return 'f(x) = '+s}
function un(a,b,c){let D=b*b-4*a*c;if(Math.abs(D)<1e-9)D=0;const r=D>0?[(-b-Math.sqrt(D))/(2*a),(-b+Math.sqrt(D))/(2*a)].sort((p,q)=>p-q):D==0?[-b/(2*a)]:[];return{D,xs:-b/(2*a),yp:c-b*b/(4*a),rt:r}}
function mk(r,q,ok,wr,e){const o=[ok,...[...new Set(wr)].filter(x=>x!==ok).slice(0,3)];for(let i=o.length-1;i>0;i--){const j=Math.floor(r()*(i+1));[o[i],o[j]]=[o[j],o[i]]}return{q,o,a:o.indexOf(ok),e}}
const T={
1:r=>{const a=pick(r,[1,2,3,-1,-2]),k=nz(r,-4,4),b=-2*a*k,c=ri(r,-6,6);return mk(r,`Sumbu simetri grafik ${fx(a,b,c)} adalah ...`,'x = '+fm(k),[-k,2*k,k+1,k-1,k+2].map(v=>'x = '+fm(v)),`x = −b/(2a) = −(${fm(b)})/(2·(${fm(a)})) = ${fm(k)}.`)},
2:r=>{const a=pick(r,[1,2,3,-1,-2]),k=nz(r,-3,3),m=nz(r,-8,8),b=-2*a*k,c=a*k*k+m;return mk(r,`Titik puncak grafik ${fx(a,b,c)} adalah ...`,P(k,m),[P(-k,m),P(k,-m),P(-k,-m),P(m,k),P(k,c)],`x = −b/(2a) = ${fm(k)}; y = f(${fm(k)}) = ${fm(a*k*k+b*k+c)}. Puncak ${P(k,m)}.`)},
3:r=>{const a=nz(r,-3,3),b=nz(r,-6,6),c=nz(r,-9,9);return mk(r,`Grafik ${fx(a,b,c)} memotong sumbu y di titik ...`,P(0,c),[P(c,0),P(-c,0),P(0,-c),P(0,b)],`Substitusi x = 0: f(0) = c = ${fm(c)}, titik ${P(0,c)}.`)},
4:r=>{const a=nz(r,-3,3),b=ri(r,-6,6),c=nz(r,-6,6),D=b*b-4*a*c;return mk(r,`Diskriminan dari ${fx(a,b,c)} adalah ...`,'D = '+fm(D),[b*b+4*a*c,4*a*c-b*b,b*b-2*a*c,D+4,D-4].map(v=>'D = '+fm(v)),`D = b² − 4ac = (${fm(b)})² − 4(${fm(a)})(${fm(c)}) = ${fm(D)}.`)},
5:(r,s)=>{const cs=s%3,a=pick(r,[1,2,-1]),p=ri(r,-4,4);let q=ri(r,-4,4);while(q==p)q=ri(r,-4,4);let b,c;if(cs==2){b=-a*(p+q);c=a*p*q}else if(cs==1){b=-2*a*p;c=a*p*p}else{const m=(a>0?1:-1)*ri(r,1,5);b=-2*a*p;c=a*p*p+m}const D=b*b-4*a*c,L=['Tidak ada titik','Satu titik','Dua titik','Tiga titik'],ok=L[D>0?2:D==0?1:0];return mk(r,`Grafik ${fx(a,b,c)} memotong sumbu x di ...`,ok,L,`D = (${fm(b)})² − 4(${fm(a)})(${fm(c)}) = ${fm(D)}. ${D>0?'D > 0 → dua titik potong.':D==0?'D = 0 → menyinggung sumbu x (satu titik).':'D < 0 → tidak memotong sumbu x.'}`)},
6:r=>{const a=pick(r,[1,2,3,-1,-2]),k=ri(r,-3,3),m=nz(r,-8,8),b=-2*a*k,c=a*k*k+m,y=-(b*b-4*a*c)/(4*a),mn=a>0,L=['Minimum = '+fm(y),'Maksimum = '+fm(y),'Minimum = '+fm(-y),'Maksimum = '+fm(-y)];return mk(r,`Nilai ekstrem dari ${fx(a,b,c)} adalah ...`,mn?L[0]:L[1],L,`a = ${fm(a)} ${mn?'> 0 → ada nilai minimum':'< 0 → ada nilai maksimum'}. Nilai ekstrem y = −D/(4a) = ${fm(y)}.`)},
7:r=>{const a=pick(r,[1,2,-1]);let p,q;do{p=nz(r,-5,5);q=nz(r,-5,5)}while(p==q||p+q==0);const b=-a*(p+q),c=a*p*q,f=(u,v)=>'x = '+fm(Math.min(u,v))+' dan x = '+fm(Math.max(u,v));return mk(r,`Titik potong sumbu x dari ${fx(a,b,c)} adalah ...`,f(p,q),[f(-p,-q),f(p,-q),f(-p,q)],`f(x) = ${fm(a)}(${xm(p)})(${xm(q)}) = 0 → x = ${fm(p)} atau x = ${fm(q)}. (Cek: jumlah akar = −b/a = ${fm(p+q)}, hasil kali = c/a = ${fm(p*q)}.)`)},
8:r=>{const a=nz(r,-4,4),b=ri(r,-5,5),c=ri(r,-5,5),L=['Terbuka ke atas, memiliki nilai minimum','Terbuka ke atas, memiliki nilai maksimum','Terbuka ke bawah, memiliki nilai maksimum','Terbuka ke bawah, memiliki nilai minimum'];return mk(r,`Pernyataan yang benar tentang grafik ${fx(a,b,c)} adalah ...`,a>0?L[0]:L[2],L,`a = ${fm(a)} ${a>0?'> 0 → terbuka ke atas dan memiliki nilai minimum':'< 0 → terbuka ke bawah dan memiliki nilai maksimum'}.`)},
9:(r,s)=>{const v=pick(r,[10,20,30,40]),t=s%2;return t?mk(r,`Bola ditendang ke atas dengan tinggi h(t) = −5t² + ${v}t (h dalam meter, t dalam detik). Tinggi maksimum bola adalah ...`,fm(v*v/20)+' m',[v*v/10,v*v/40,v*v/5,v*v].map(x=>fm(x)+' m'),`t = −b/(2a) = ${fm(v/10)} s. h = −5(${fm(v/10)})² + ${v}(${fm(v/10)}) = ${fm(v*v/20)} m.`):mk(r,`Bola ditendang ke atas dengan tinggi h(t) = −5t² + ${v}t (h dalam meter, t dalam detik). Bola mencapai tinggi maksimum pada t = ...`,fm(v/10)+' detik',[v/5,v/20,v,v/10+1].map(x=>fm(x)+' detik'),`t = −b/(2a) = −${v}/(2·(−5)) = ${fm(v/10)} detik.`)},
10:r=>{const h=ri(r,-3,3),k=ri(r,-5,5),a=pick(r,[-3,-2,-1,1,2,3]),d=pick(r,[1,2,-1,-2]),x0=h+d,y0=k+a*d*d;return mk(r,`Fungsi y = a(x − p)² + q memiliki titik puncak ${P(h,k)} dan melalui titik ${P(x0,y0)}. Nilai a adalah ...`,fm(a),[-a,2*a,a+1,a-1].map(x=>fm(x)),`Puncak ${P(h,k)} → y = a(${xm(h)})² ${sg(k)}. Substitusi ${P(x0,y0)}: ${fm(y0)} = a(${fm(d)})² ${sg(k)} → a = ${fm(y0-k)}/${d*d} = ${fm(a)}.`)}};
const gen=(t,s)=>{const q=T[t](rng(s*7+t*1000+1),s);q.t=t;return q};
/*E*/
function draw(cv,a,b,c,o={}){const w=cv.parentElement.clientWidth||340,dp=devicePixelRatio||1,h=Math.min(400,w*.8);cv.style.height=h+'px';cv.width=w*dp;cv.height=h*dp;const g=cv.getContext('2d');g.scale(dp,dp);
const st=o.s??6,u=un(a,b,c),X=[0,u.xs,...u.rt],Y=[0,c,u.yp];let [x0,x1,y0,y1]=o.fix||[Math.min(...X),Math.max(...X),Math.min(...Y),Math.max(...Y)];
if(!o.fix){let p=Math.max(2,(x1-x0)*.25);x0-=p;x1+=p;if(x1-x0<8){const m=(x0+x1)/2;x0=m-4;x1=m+4}p=Math.max(2,(y1-y0)*.25);y0-=p;y1+=p;if(y1-y0<6){const m=(y0+y1)/2;y0=m-3;y1=m+3}}
const sx=x=>(x-x0)/(x1-x0)*w,sy=y=>h-(y-y0)/(y1-y0)*h,nice=r=>{const k=r/8,p=10**Math.floor(Math.log10(k)),f=k/p;return(f<1.5?1:f<3.5?2:f<7.5?5:10)*p};
g.fillStyle='#fff';g.fillRect(0,0,w,h);g.font='11px system-ui';g.lineWidth=1;const gx=nice(x1-x0),gy=nice(y1-y0);
for(let x=Math.ceil(x0/gx)*gx;x<=x1;x+=gx){g.strokeStyle='#e1e4ea';g.beginPath();g.moveTo(sx(x),0);g.lineTo(sx(x),h);g.stroke();if(Math.abs(x)>1e-9){g.fillStyle='#667';g.fillText(fm(x),sx(x)+2,Math.min(h-3,Math.max(11,sy(0)+12)))}}
for(let y=Math.ceil(y0/gy)*gy;y<=y1;y+=gy){g.strokeStyle='#e1e4ea';g.beginPath();g.moveTo(0,sy(y));g.lineTo(w,sy(y));g.stroke();if(Math.abs(y)>1e-9){g.fillStyle='#667';g.fillText(fm(y),Math.min(w-30,Math.max(2,sx(0)+3)),sy(y)-2)}}
g.strokeStyle='#16294d';g.lineWidth=1.6;g.beginPath();g.moveTo(0,sy(0));g.lineTo(w,sy(0));g.moveTo(sx(0),0);g.lineTo(sx(0),h);g.stroke();
if(st>=4){g.setLineDash([6,5]);g.strokeStyle='#16294d99';g.beginPath();g.moveTo(sx(u.xs),0);g.lineTo(sx(u.xs),h);g.stroke();g.setLineDash([])}
if(st>=6){g.strokeStyle='#7a1f2e';g.lineWidth=3;g.beginPath();for(let i=0;i<=w;i+=2){const x=x0+i/w*(x1-x0),y=a*x*x+b*x+c;i?g.lineTo(i,sy(y)):g.moveTo(i,sy(y))}g.stroke()}
const seen=new Set,pt=(x,y,t)=>{const k=fm(x)+','+fm(y);if(seen.has(k))return;seen.add(k);g.fillStyle='#7a1f2e';g.beginPath();g.arc(sx(x),sy(y),5,0,7);g.fill();g.font='bold 12px system-ui';g.fillStyle='#16294d';const tw=g.measureText(t).width;let tx=sx(x)+8;if(tx+tw>w)tx=sx(x)-tw-8;g.fillText(t,tx,sy(y)-8)};
if(st>=2)pt(0,c,P(0,c));if(st>=3)u.rt.forEach(x=>pt(x,0,P(x,0)));if(st>=5)pt(u.xs,u.yp,'P'+P(u.xs,u.yp))}
const NM=['Beranda','Konsep','Eksplorasi','Langkah Melukis','Latihan','Masalah Nyata','Kuis Akhir','Pengembang'];let cur=0;
nv.innerHTML=NM.map((n,i)=>`<button onclick="go(${i})">${n}</button>`).join('');
function go(i){cur=i;document.querySelectorAll('.pg').forEach((p,j)=>p.classList.toggle('on',j==i));nv.querySelectorAll('button').forEach((b,j)=>b.classList.toggle('on',j==i));scrollTo(0,0);({2:ex,3:melr,4:lat,5:mn,6:()=>kq.length||kstart()})[i]?.()}
onresize=()=>({2:ex,3:melr,5:mn})[cur]?.();
const CH=[['Buat parabola terbuka ke atas yang tidak memotong sumbu x.',(a,b,c,u)=>a>0&&u.D<0],['Buat parabola dengan sumbu simetri x = 2.',(a,b,c,u)=>Math.abs(u.xs-2)<1e-9],['Buat parabola yang menyinggung sumbu x (D = 0).',(a,b,c,u)=>u.D==0],['Buat parabola terbuka ke bawah yang memotong sumbu y di (0, −3).',(a,b,c)=>a<0&&c==-3],['Buat parabola dengan titik puncak di kuadran I (x > 0 dan y > 0).',(a,b,c,u)=>u.xs>0&&u.yp>0]];let ci=0,pa=1;
function ex(){let a=+sa.value,b=+sb.value,c=+sc.value;if(a==0)a=+(sa.value=pa<0?.5:-.5);pa=a;va.textContent=fm(a);vb.textContent=fm(b);vc.textContent=fm(c);const u=un(a,b,c);fx_=fx(a,b,c);$('#fx').textContent=fx_;draw(ce,a,b,c,{fix:[-10,10,-12,12]});
tu.innerHTML=`<tr><th>Unsur</th><th>Nilai</th></tr><tr><td>Arah bukaan</td><td>${a>0?'Ke atas (minimum)':'Ke bawah (maksimum)'}</td></tr><tr><td>Diskriminan D</td><td>${fm(u.D)} → ${u.D>0?'dua titik potong sumbu x':u.D==0?'menyinggung sumbu x':'tidak memotong sumbu x'}</td></tr><tr><td>Sumbu simetri</td><td>x = ${fm(u.xs)}</td></tr><tr><td>Titik puncak</td><td>${P(u.xs,u.yp)}</td></tr><tr><td>Titik potong sumbu y</td><td>${P(0,c)}</td></tr><tr><td>Titik potong sumbu x</td><td>${u.rt.map(x=>P(x,0)).join(' dan ')||'tidak ada'}</td></tr>`;
chq.textContent=CH[ci][0];chf.textContent=CH[ci][1](a,b,c,u)?'✅ Tantangan terpenuhi!':'Belum terpenuhi, coba geser slider lagi.'}
var fx_;sa.oninput=sb.oninput=sc.oninput=ex;
let stp=0,A=1,B=-4,C=3;
function sm(a,b,c){const u=un(a,b,c),D=u.D;return[`Arah bukaan: a = ${fm(a)} ${a>0?'> 0 → parabola terbuka ke atas (memiliki titik minimum).':'< 0 → parabola terbuka ke bawah (memiliki titik maksimum).'}`,`Titik potong sumbu y: substitusi x = 0, f(0) = c = ${fm(c)}. Titik ${P(0,c)}.`,`Diskriminan: D = b² − 4ac = (${fm(b)})² − 4(${fm(a)})(${fm(c)}) = ${fm(D)}. `+(D>0?`D > 0, ada dua titik potong sumbu x: x = (−b ± √D)/(2a) → ${P(u.rt[0],0)} dan ${P(u.rt[1],0)}.`:D==0?`D = 0, grafik menyinggung sumbu x di ${P(u.rt[0],0)}.`:'D < 0, grafik tidak memotong sumbu x.'),`Sumbu simetri: x = −b/(2a) = −(${fm(b)})/(2·(${fm(a)})) = ${fm(u.xs)}.`,`Titik puncak: x = ${fm(u.xs)}, y = −D/(4a) = ${fm(u.yp)}. Puncak P${P(u.xs,u.yp)}.`,`Hubungkan titik-titik dengan kurva mulus yang simetris terhadap sumbu x = ${fm(u.xs)}. Sketsa selesai!`]}
function melr(){const S=sm(A,B,C);draw(cl,A,B,C,{s:stp});stl.innerHTML='<p class="f">'+fx(A,B,C)+'</p>'+S.slice(0,stp).map((t,i)=>`<div class="c" style="margin:6px 0;border-top-color:${i==stp-1?'#7a1f2e':'#2e7d32'}">${i<stp-1?'✅':'👉'} <b>Langkah ${i+1}.</b> ${t}</div>`).join('')}
function mulai(){const a=+ia.value,b=+ib.value,c=+ic.value;if(!a||isNaN(a)||isNaN(b)||isNaN(c)){msg.textContent='Isi a, b, c dengan angka dan a tidak boleh 0.';return}msg.textContent='';A=a;B=b;C=c;stp=1;melr()}
function nxt(){if(!stp)return mulai();if(stp<6)stp++;melr()}
function acak(){ia.value=pick(Math.random,[1,2,-1,-2]);ib.value=ri(Math.random,-6,6);ic.value=ri(Math.random,-6,6);mulai()}
function qc(el,q,cb){el.innerHTML=`<p><b>${q.q}</b></p>`+q.o.map((x,i)=>`<button class="o" data-i="${i}">${'ABCD'[i]}. ${x}</button>`).join('')+'<div class="fb"></div>';let d=0;el.querySelectorAll('.o').forEach(b=>b.onclick=()=>{if(d)return;d=1;const i=+b.dataset.i;el.querySelectorAll('.o')[q.a].classList.add('ok');if(i!=q.a)b.classList.add('no');el.querySelector('.fb').innerHTML=`<p>${i==q.a?'✅ Benar!':'❌ Belum tepat.'} <i>Pembahasan:</i> ${q.e}</p>`;cb(i==q.a)})}
const LV={Dasar:[1,3,4,8],Menengah:[2,5,6,7],Tantangan:[9,10]};let lv='Dasar',ls=0,lb=0;
function lat(){lvb.innerHTML=Object.keys(LV).map(k=>`<button class="${k==lv?'m':''}" onclick="lv='${k}';ls=lb=0;lat()">${k}</button>`).join(' ');lsc.textContent=`Benar ${lb} dari ${ls} soal`;ln.classList.add('hid');qc(lq,gen(pick(Math.random,LV[lv]),Math.random()*1e6|0),ok=>{ls++;lb+=ok;lsc.textContent=`Benar ${lb} dari ${ls} soal`;ln.classList.remove('hid')})}
function mn(){const x=+v.value;vv.textContent=x;draw(cm,-5,x,0);mi.innerHTML=`Tinggi maksimum dicapai saat t = −b/(2a) = ${x}/10 = <b>${fm(x/10)} s</b>, yaitu h = <b>${fm(x*x/20)} m</b>.<br>Bola kembali ke tanah saat t = <b>${fm(x/5)} s</b>.`;if(!pb)np()}
v.oninput=mn;let pb;
function np(){const V=pick(Math.random,[20,30,40,50]),K=pick(Math.random,[40,60,80]),H=`Bola ditendang ke atas dengan tinggi h(t) = −5t² + ${V}t (h dalam meter, t dalam detik). `;pb=pick(Math.random,[{q:H+'Berapa tinggi maksimum bola (meter)?',a:V*V/20,s:`t = ${fm(V/10)} s → h = −5(${fm(V/10)})² + ${V}(${fm(V/10)}) = ${fm(V*V/20)} m.`},{q:H+'Setelah berapa detik bola kembali ke tanah?',a:V/5,s:`h = 0 → t(−5t + ${V}) = 0 → t = ${fm(V/5)} detik.`},{q:`Pagar persegi panjang dibuat dari kawat sepanjang ${K} m. Berapa luas maksimum yang dapat dipagari (m²)?`,a:K*K/16,s:`Lebar x, panjang ${K/2} − x. L = −x² + ${K/2}x, maksimum saat x = ${K/4}, L = ${fm(K*K/16)} m².`}]);pq.textContent=pb.q;ai.value='';pf.textContent=''}
function cek(){const u=parseFloat(ai.value.replace(',','.'));pf.innerHTML=isNaN(u)?'Masukkan angka.':Math.abs(u-pb.a)<.01?'✅ Benar! '+pb.s:'❌ Belum tepat. Penyelesaian: '+pb.s}
let kq=[],ki=0,ks=0;
function kstart(){const all=[];for(let t=1;t<=10;t++)for(let s=1;s<=3;s++)all.push(gen(t,s));for(let i=all.length-1;i>0;i--){const j=Math.floor(Math.random()*(i+1));[all[i],all[j]]=[all[j],all[i]]}kq=all.slice(0,10);ki=ks=0;kshow()}
function kshow(){const el=$('#kq');if(ki>=10){const sk=ks*10;el.innerHTML=`<h2>Skor: ${sk}</h2><p>${ks} dari 10 soal benar. ${sk>=75?'🎉 Tuntas! Skor ≥ 75.':'Belum tuntas (target ≥ 75). Ulangi menu Konsep, Eksplorasi, Langkah Melukis, dan Latihan, lalu coba lagi.'}</p><button class="m" onclick="kstart()">Ulangi kuis</button>`;kp.textContent='Selesai';return}
kp.textContent=`Soal ${ki+1} dari 10`;qc(el,kq[ki],ok=>{ks+=ok;el.insertAdjacentHTML('beforeend',`<button onclick="ki++;kshow()">${ki==9?'Lihat skor':'Lanjut →'}</button>`)})}
function bunyi(){try{const ac=new(window.AudioContext||window.webkitAudioContext)(),o=ac.createOscillator(),g=ac.createGain(),t=ac.currentTime;o.type='sine';o.frequency.setValueAtTime(523,t);o.frequency.setValueAtTime(784,t+.1);g.gain.setValueAtTime(.25,t);g.gain.exponentialRampToValueAtTime(.001,t+.35);o.connect(g);g.connect(ac.destination);o.start();o.stop(t+.35)}catch(e){}}
function mulaiApp(){bunyi();sp.style.opacity=0;setTimeout(()=>sp.classList.add('hid'),500)}
let pr=0;const iv=setInterval(()=>{pr=Math.min(100,pr+Math.random()*12+4);ldb.style.width=pr+'%';ldt.textContent=pr<100?'Memuat… '+Math.round(pr)+'%':'Siap!';if(pr>=100){clearInterval(iv);sb0.classList.remove('hid')}},200);
go(0);
</script></body></html>
