<!DOCTYPE html>
<html lang="ja">
<head>
<meta charset="UTF-8"><meta name="viewport" content="width=device-width,initial-scale=1.0">
<title>お楽しみ抽選会</title>
<style>
body{font-family:sans-serif;margin:0;background:#fff9f0;display:flex;justify-content:center;align-items:center;min-height:100vh;text-align:center}
.box{background:#fff;padding:30px 20px;border-radius:20px;box-shadow:0 10px 25px rgba(0,0,0,.1);width:360px;max-width:90%;position:relative}
.congrats{font-size:22px;font-weight:bold;color:#e67e22;margin-bottom:10px;animation:pop .5s ease}
.rank{font-size:38px;font-weight:bold;color:#ff4757;margin:10px 0;animation:pop .6s ease}
.prize{font-size:28px;font-weight:bold;color:#2f3542;margin-bottom:20px;background:#fff3cd;padding:12px;border-radius:10px}
.timer{color:#747d8c;font-size:13px;background:#f1f2f6;padding:10px;border-radius:8px}
@keyframes pop{0%{transform:scale(.5);opacity:0}100%{transform:scale(1);opacity:1}}
.set-btn{position:absolute;top:12px;right:15px;background:none;border:none;color:#bdc3c7;cursor:pointer;text-decoration:underline;font-size:13px}
.modal{display:none;position:fixed;inset:0;background:rgba(0,0,0,.6);justify-content:center;align-items:center;z-index:10}
.m-body{background:#fff;padding:20px;border-radius:15px;width:300px;text-align:left}
.row{display:flex;justify-content:space-between;margin:8px 0}
input{width:60px;text-align:right}
button{cursor:pointer;border:none;border-radius:5px;padding:8px 12px;color:#fff}
</style>
</head>
<body>
<div class="box">
  <button class="set-btn" onclick="openSet()">設定</button>
  
  <div id="s2">
    <div class="congrats">🎉 おめでとうございます！ 🎉</div>
    <div id="r-rank" class="rank"></div>
    <div id="r-prize" class="prize"></div>
    <p style="font-size:14px;color:#555;margin-bottom:15px">スタッフにこの画面を見せてください！</p>
    <div id="r-time" class="timer"></div>
  </div>

  <div id="s1" style="display:none;padding:30px 0">
    <h2 style="color:#2f3542">抽選終了</h2>
    <p style="color:#747d8c;font-size:14px">ご参加ありがとうございました！<br>次の方はQRコードを再度読み込んでください。</p>
  </div>
</div>

<div id="modal" class="modal"><div class="m-body">
  <h3>⚙️ 出現確率 (合計100%)</h3>
  <div class="row"><span>一等 (カレー/柿の種):</span><div><input type="number" id="p1" oninput="calc()">%</div></div>
  <div class="row"><span>二等 (なしのしずく):</span><div><input type="number" id="p2" oninput="calc()">%</div></div>
  <div class="row"><span>三等 (うまい棒):</span><div><input type="number" id="p3" oninput="calc()">%</div></div>
  <div id="tot" style="text-align:right;font-weight:bold">合計: 100%</div>
  <h3>📊 出た数カウント</h3>
  <div class="row"><span>明和町カレー:</span><b id="c1">0</b></div>
  <div class="row"><span>柿の種:</span><b id="c2">0</b></div>
  <div class="row"><span>なしのしずく:</span><b id="c3">0</b></div>
  <div class="row"><span>うまい棒:</span><b id="c4">0</b></div>
  <button style="background:#ff4757;width:100%;margin-top:8px" onclick="rst()">カウントを0にリセット</button>
  <div style="display:flex;gap:10px;margin-top:15px">
    <button style="background:#747d8c" onclick="document.getElementById('modal').style.display='none'">閉じる</button>
    <button style="background:#2ed573;flex:1" onclick="save()">確率を保存</button>
  </div>
</div></div>

<script>
let p=JSON.parse(localStorage.getItem('lp'))||{p1:20,p2:30,p3:50},c=JSON.parse(localStorage.getItem('lc'))||{c1:0,c2:0,c3:0,c4:0},t1,t2;
function calc(){let s=(+p1.value||0)+(+p2.value||0)+(+p3.value||0);tot.innerText=`合計: ${s}%`;tot.style.color=s===100?'#2ed573':'#ff4757'}
function openSet(){if(prompt('パスワード(4桁)')==='0000'){p1.value=p.p1;p2.value=p.p2;p3.value=p.p3;calc();c1.innerText=c.c1;c2.innerText=c.c2;c3.innerText=c.c3;c4.innerText=c.c4;modal.style.display='flex'}}
function save(){let s=(+p1.value||0)+(+p2.value||0)+(+p3.value||0);if(s!==100)return alert('合計を100%にしてください');p={p1:+p1.value,p2:+p2.value,p3:+p3.value};localStorage.setItem('lp',JSON.stringify(p));alert('保存しました');modal.style.display='none'}
function rst(){if(confirm('リセットしますか？')){c={c1:0,c2:0,c3:0,c4:0};localStorage.setItem('lc',JSON.stringify(c));c1.innerText=c2.innerText=c3.innerText=c4.innerText=0}}
window.onload=()=>{
  let r=Math.random()*100,rk,pz;
  if(r<p.p1){rk='一等';if(Math.random()<.5){pz='明和町カレー';c.c1++}else{pz='柿の種';c.c2++}}
  else if(r<p.p1+p.p2){rk='二等';pz='なしのしずく';c.c3++}
  else{rk='三等';pz='うまい棒';c.c4++}
  localStorage.setItem('lc',JSON.stringify(c));
  document.getElementById('r-rank').innerText=rk;document.getElementById('r-prize').innerText=pz;
  let sec=10;document.getElementById('r-time').innerText=`あと ${sec} 秒で画面が閉じます`;
  clearInterval(t1);t1=setInterval(()=>{if(--sec>0)document.getElementById('r-time').innerText=`あと ${sec} 秒で画面が閉じます`;else clearInterval(t1)},1000);
  clearTimeout(t2);t2=setTimeout(()=>{s2.style.display='none';s1.style.display='block'},10000);
};
</script>
</body>
</html>
