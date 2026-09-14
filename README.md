<!DOCTYPE html>
<html lang="zh-Hant">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>蜂巢進度 · 給團隊</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Figtree:wght@400;600;700;800&family=Noto+Sans+TC:wght@400;500;700&display=swap">

<style>
:root{
  /* surfaces */
  --bg:#121212;
  --s1:#181818;
  --s2:#1f1f1f;
  --s3:#252525;
  --s4:#272727;
  /* text */
  --tx:#ffffff;
  --tx2:#b3b3b3;
  --tx3:#7c7c7c;
  --bright:#fdfdfd;
  /* accent — functional only */
  --green:#1ed760;
  --green-dk:#1db954;
  /* semantic */
  --neg:#f3727f;
  --warn:#ffa42b;
  --info:#539df5;
  --bd:#4d4d4d;
  --bd-lt:#7c7c7c;
  /* elevation */
  --e2:rgba(0,0,0,.3) 0 8px 8px;
  --e3:rgba(0,0,0,.5) 0 8px 24px;

  --f:"Figtree","Noto Sans TC","PingFang TC","Microsoft JhengHei","Helvetica Neue",helvetica,arial,sans-serif;
}
*{box-sizing:border-box}
html{font-size:18px;-webkit-text-size-adjust:100%}
body{
  margin:0;background:var(--bg);color:var(--tx);
  font-family:var(--f);font-weight:400;line-height:1.62;
  -webkit-font-smoothing:antialiased;
}
img{max-width:100%}
.wrap{max-width:1100px;margin:0 auto;padding-inline:22px;padding-block:0 90px}

/* ── top bar ─────────────────────────────────────────── */
.top{position:sticky;top:0;z-index:40;background:var(--bg);box-shadow:var(--e2)}
.top-in{max-width:1100px;margin:0 auto;padding:13px 22px;display:flex;align-items:center;gap:14px;flex-wrap:wrap}
.logo{width:32px;height:32px;border-radius:50%;background:var(--green);display:grid;place-items:center;flex:none}
.logo svg{width:18px;height:20px;color:#000}
.top h1{font-size:1rem;font-weight:800;margin:0;line-height:1.2;letter-spacing:-.01em}
.top h1 span{color:var(--tx2);font-weight:400}
.nav{display:flex;gap:6px;margin-left:auto;flex-wrap:wrap}
.nav a{
  font-size:.78rem;font-weight:700;color:var(--tx2);text-decoration:none;
  padding:7px 16px;border-radius:9999px;background:var(--s2);white-space:nowrap;
  transition:background .15s ease-out,color .15s ease-out;
}
.nav a:hover{background:var(--s4);color:var(--tx)}
.nav a:focus-visible{outline:2px solid var(--green);outline-offset:2px}

/* ── hero ────────────────────────────────────────────── */
.hero{padding-block:52px 12px}
.eyebrow{
  font-size:.72rem;font-weight:700;letter-spacing:1.6px;text-transform:uppercase;
  color:var(--green);margin:0 0 16px;
}
.hero h2{
  font-size:clamp(2rem,5.2vw,3.1rem);font-weight:800;line-height:1.1;
  letter-spacing:-.025em;margin:0 0 20px;text-wrap:balance;max-width:17ch;
}
.hero h2 em{font-style:normal;color:var(--neg)}
.lede{font-size:1.06rem;color:var(--tx2);max-width:60ch;margin:0 0 34px}
.lede b{color:var(--tx);font-weight:700}

.kpis{display:grid;grid-template-columns:repeat(auto-fit,minmax(168px,1fr));gap:14px;margin-bottom:46px}
.kpi{background:var(--s1);border-radius:8px;padding:20px 20px 22px;box-shadow:var(--e2)}
.kpi .n{font-size:2.1rem;font-weight:800;letter-spacing:-.03em;line-height:1.08;font-variant-numeric:tabular-nums;display:block}
.kpi .n small{font-size:.55em;font-weight:700;color:var(--tx3);margin-left:3px}
.kpi .k{font-size:.75rem;font-weight:700;letter-spacing:1.2px;text-transform:uppercase;color:var(--tx2);margin-top:7px}
.kpi .note{font-size:.83rem;color:var(--tx3);margin-top:9px;line-height:1.45}
.g{color:var(--green)} .r{color:var(--neg)} .w{color:var(--warn)} .i{color:var(--info)}

/* ── sections ────────────────────────────────────────── */
section{padding-block:50px;scroll-margin-top:74px}
section+section{border-top:1px solid rgba(255,255,255,.07)}
.sh{margin-bottom:28px}
.sh h3{font-size:1.5rem;font-weight:800;letter-spacing:-.015em;margin:0 0 8px}
.sh p{margin:0;color:var(--tx2);font-size:.94rem;max-width:64ch}
h4.sub{font-size:1.1rem;font-weight:700;margin:38px 0 14px;letter-spacing:-.01em}
h4.sub:first-of-type{margin-top:0}
h4.sub .tag{
  display:inline-block;font-size:.68rem;font-weight:700;letter-spacing:1.2px;
  text-transform:uppercase;background:var(--green);color:#000;
  padding:3px 10px;border-radius:9999px;margin-right:10px;vertical-align:3px;
}
.hint{font-size:.9rem;color:var(--tx2);margin:0 0 16px;max-width:66ch}

/* ── deviation ───────────────────────────────────────── */
.dev{background:var(--s1);border-radius:8px;padding:22px 24px;box-shadow:var(--e2)}
.dev-axis{display:grid;grid-template-columns:minmax(130px,190px) 1fr;gap:16px;align-items:center;font-size:.72rem;font-weight:700;letter-spacing:.8px;color:var(--tx3);padding-bottom:8px}
.axis-track{position:relative;height:15px}
.axis-track span{position:absolute;top:0;transform:translateX(-50%);white-space:nowrap}
.dev-row{display:grid;grid-template-columns:minmax(130px,190px) 1fr;gap:16px;align-items:center;padding:9px 0;border-bottom:1px solid rgba(255,255,255,.06)}
.dev-row:last-child{border-bottom:0}
.dev-name{font-size:.92rem;line-height:1.35}
.dev-name b{display:block;font-weight:700}
.dev-name i{font-style:normal;font-size:.76rem;color:var(--tx3);font-variant-numeric:tabular-nums}
.dev-track{position:relative;height:30px;background:var(--s2);border-radius:6px;overflow:hidden}
.dev-zero{position:absolute;top:0;bottom:0;width:1px;background:var(--bd);left:50%}
.dev-bar{position:absolute;top:6px;height:18px;border-radius:9999px}
.dev-bar.pos{background:var(--green)}
.dev-bar.neg{background:var(--neg)}
.dev-bar.zero{background:var(--tx3);width:6px!important;border-radius:9999px}
.dev-val{position:absolute;top:50%;transform:translateY(-50%);font-size:.78rem;font-weight:800;font-variant-numeric:tabular-nums;white-space:nowrap}
.legend{display:flex;gap:22px;flex-wrap:wrap;margin-top:20px;font-size:.78rem;font-weight:600;color:var(--tx3)}
.legend i{display:inline-block;width:11px;height:11px;border-radius:50%;margin-right:7px;vertical-align:-1px}

/* ── weeks ───────────────────────────────────────────── */
.weeks{display:grid;gap:12px}
.week{background:var(--s1);border-radius:8px;padding:20px 22px;display:grid;grid-template-columns:112px 1fr;gap:20px;align-items:start;box-shadow:var(--e2)}
.week-when{font-size:.8rem;color:var(--tx3);line-height:1.5;font-variant-numeric:tabular-nums}
.week-when b{display:block;color:var(--tx);font-size:1rem;font-weight:800;letter-spacing:.5px}
.week-body{display:grid;gap:11px;min-width:0}
.wl{display:grid;grid-template-columns:52px 1fr;gap:12px;font-size:.92rem;align-items:baseline}
.wl>span:first-child{font-size:.7rem;font-weight:700;letter-spacing:1.1px;color:var(--tx3);text-transform:uppercase}
.wl.plan>span:last-child{color:var(--tx2)}
.vd{display:inline-flex;align-items:center;font-size:.74rem;font-weight:700;letter-spacing:.6px;padding:5px 14px;border-radius:9999px;white-space:nowrap}
.v-ok{background:var(--s3);color:var(--tx2)}
.v-g{background:rgba(30,215,96,.16);color:var(--green)}
.v-r{background:rgba(243,114,127,.16);color:var(--neg)}
.v-w{background:rgba(255,164,43,.16);color:var(--warn)}

/* ── people ──────────────────────────────────────────── */
.people{display:grid;grid-template-columns:repeat(auto-fit,minmax(258px,1fr));gap:14px}
.person{background:var(--s1);border-radius:8px;padding:20px 21px;display:flex;flex-direction:column;gap:14px;box-shadow:var(--e2)}
.ptop{display:flex;align-items:center;gap:12px}
.pav{width:44px;height:44px;border-radius:50%;background:var(--s3);display:grid;place-items:center;font-size:1.05rem;font-weight:800;flex:none;color:var(--tx)}
.ptop h4{font-size:1.08rem;font-weight:800;margin:0;letter-spacing:-.01em}
.ptop .sub{font-size:.76rem;color:var(--tx3);font-weight:600}
.pstat{display:flex;gap:20px;font-variant-numeric:tabular-nums}
.pstat div{display:flex;flex-direction:column}
.pstat b{font-size:1.25rem;font-weight:800;line-height:1.2}
.pstat span{font-size:.68rem;font-weight:700;letter-spacing:.9px;color:var(--tx3);text-transform:uppercase}
.plines{display:grid;gap:9px;font-size:.88rem;line-height:1.5}
.plines>div{display:grid;grid-template-columns:46px 1fr;gap:10px}
.plines em{font-style:normal;font-size:.68rem;font-weight:700;letter-spacing:.9px;color:var(--tx3);text-transform:uppercase;padding-top:4px}

/* ── notices ─────────────────────────────────────────── */
.excs{display:grid;grid-template-columns:repeat(auto-fit,minmax(290px,1fr));gap:14px}
.exc{background:var(--s1);border-radius:8px;padding:20px 21px;box-shadow:var(--e2)}
.exc h4{font-size:.78rem;font-weight:700;letter-spacing:1.3px;text-transform:uppercase;margin:0 0 14px;display:flex;align-items:center;gap:9px}
.exc h4 .dot{width:9px;height:9px;border-radius:50%;flex:none}
.exc ul{margin:0;padding:0;list-style:none;display:grid;gap:13px}
.exc li{font-size:.9rem;line-height:1.5}
.exc li b{font-weight:700}
.exc li i{font-style:normal;font-size:.78rem;color:var(--tx3);display:block;margin-top:3px}

/* ── tables ──────────────────────────────────────────── */
.tw{overflow-x:auto;background:var(--s1);border-radius:8px;box-shadow:var(--e2)}
table{border-collapse:collapse;width:100%;font-size:.9rem}
table.wide{min-width:700px}
thead th{
  background:var(--s2);font-size:.7rem;font-weight:700;letter-spacing:1.2px;text-transform:uppercase;
  color:var(--tx2);text-align:left;padding:12px 16px;white-space:nowrap;
}
#logtable thead th{position:sticky;top:0}
tbody td{padding:11px 16px;border-top:1px solid rgba(255,255,255,.06);vertical-align:top;line-height:1.5}
td.d{font-size:.82rem;color:var(--tx3);white-space:nowrap;font-variant-numeric:tabular-nums}
td.p{white-space:nowrap;font-weight:600}
td.next{color:var(--tx2)}
tbody tr.stall td.today{color:var(--warn)}
.hm{font-size:.86rem;font-weight:800}
.hm-y{color:var(--green)} .hm-p{color:var(--warn)} .hm-n{color:var(--neg)}
code{font-family:ui-monospace,SFMono-Regular,Menlo,Consolas,monospace;font-size:.86em;background:var(--s3);padding:2px 7px;border-radius:4px;color:var(--tx)}
.new{display:inline-block;font-size:.6rem;font-weight:800;letter-spacing:.8px;background:var(--green);color:#000;padding:2px 8px;border-radius:9999px;margin-left:8px;vertical-align:2px;text-transform:uppercase}
.badge{display:inline-block;font-size:.72rem;font-weight:700;padding:3px 11px;border-radius:9999px;white-space:nowrap}
.b-blue{background:rgba(83,157,245,.18);color:var(--info)}
.b-yel{background:rgba(255,164,43,.18);color:var(--warn)}
.b-red{background:rgba(243,114,127,.18);color:var(--neg)}
.b-grn{background:rgba(30,215,96,.18);color:var(--green)}
.b-gry{background:var(--s3);color:var(--tx2)}

/* ── do / don't ──────────────────────────────────────── */
.dd2{display:grid;grid-template-columns:repeat(auto-fit,minmax(320px,1fr));gap:14px}
.dd{background:var(--s1);border-radius:8px;overflow:hidden;box-shadow:var(--e2)}
.dd-h{padding:13px 20px;font-size:.76rem;font-weight:700;letter-spacing:1.3px;text-transform:uppercase;display:flex;align-items:center;gap:9px}
.dd.bad .dd-h{background:rgba(243,114,127,.15);color:var(--neg)}
.dd.good .dd-h{background:rgba(30,215,96,.15);color:var(--green)}
.dd ul{margin:0;padding:16px 20px 20px;list-style:none;display:grid;gap:14px}
.dd li{font-size:.92rem;line-height:1.5}
.dd li i{font-style:normal;font-size:.79rem;color:var(--tx3);display:block;margin-top:4px}

/* ── template ────────────────────────────────────────── */
.tmpl{
  background:var(--s2);border-radius:8px;padding:22px 24px;box-shadow:var(--e2);
  font-family:ui-monospace,SFMono-Regular,Menlo,Consolas,monospace;
  font-size:.86rem;line-height:2;white-space:pre-wrap;overflow-x:auto;color:var(--tx2);
}
.tmpl b{color:var(--green);font-weight:700}
.tmpl u{color:var(--tx);text-decoration:none}

.callout{
  background:var(--s2);border-radius:8px;padding:18px 22px;margin-top:18px;
  display:flex;gap:14px;align-items:flex-start;box-shadow:var(--e2);
}
.callout .ic{width:26px;height:26px;border-radius:50%;background:var(--warn);color:#000;display:grid;place-items:center;font-weight:800;font-size:.85rem;flex:none;margin-top:2px}
.callout p{margin:0;font-size:.92rem;color:var(--tx2);line-height:1.55}
.callout p b{color:var(--tx);font-weight:700}

/* ── filters ─────────────────────────────────────────── */
.filters{display:flex;gap:9px;flex-wrap:wrap;margin-bottom:18px;align-items:center}
.chip{
  font-family:inherit;font-size:.8rem;font-weight:700;letter-spacing:.4px;
  padding:9px 20px;border-radius:9999px;border:0;background:var(--s2);color:var(--tx2);
  cursor:pointer;transition:background .15s ease-out,color .15s ease-out,transform .1s ease-out;
}
.chip:hover{background:var(--s4);color:var(--tx)}
.chip:active{transform:scale(.96)}
.chip[aria-pressed="true"]{background:var(--green);color:#000}
.chip:focus-visible{outline:2px solid var(--green);outline-offset:3px}
.cnt{font-size:.8rem;font-weight:600;color:var(--tx3);margin-left:auto;font-variant-numeric:tabular-nums}

.foot{margin-top:46px;padding-top:26px;border-top:1px solid rgba(255,255,255,.07);font-size:.84rem;color:var(--tx3);line-height:1.7}

@media (max-width:760px){ .nav{width:100%;margin-left:0;overflow-x:auto;padding-bottom:2px} }
@media (max-width:640px){
  html{font-size:17px}
  .week{grid-template-columns:1fr;gap:12px}
  .dev-row,.dev-axis{grid-template-columns:1fr;gap:6px}
  .dev{padding:18px 16px}
}
@media (prefers-reduced-motion:reduce){*{transition-duration:1ms!important;animation-duration:1ms!important}}
@media print{
  body{background:#fff;color:#111} .top{position:static;box-shadow:none}
  .chip,.nav{display:none} section{break-inside:avoid}
  .kpi,.week,.person,.exc,.tw,.dd,.dev{box-shadow:none;border:1px solid #ddd}
}
</style>
</head>
<body>

<header class="top">
  <div class="top-in">
    <span class="logo" aria-hidden="true">
      <svg viewBox="0 0 26 30"><path d="M13 1.2 24 7.4v14.4L13 28.8 2 21.8V7.4z" fill="none" stroke="currentColor" stroke-width="2.4"/></svg>
    </span>
    <h1>蜂巢 the Hivebanes <span>· 給團隊</span></h1>
    <nav class="nav">
      <a href="#now">進度</a>
      <a href="#weeks">六週回顧</a>
      <a href="#people">每個人</a>
      <a href="#watch">要注意</a>
      <a href="#howto">日誌怎麼填</a>
      <a href="#log">全紀錄</a>
    </nav>
  </div>
</header>

<div class="wrap">

  <div class="hero">
    <p class="eyebrow">2026/08/03 — 09/11 · 你們自己填的 107 筆日誌</p>
    <h2>角色和分鏡跑在前面，<em>城市和街道慢了七天</em>。</h2>
    <p class="lede">
      這頁是把你們每天在 Notion 填的日誌，跟時程表（方缺版拆解）排的計畫擺在一起看的結果。
      結論很單純：<b>資產線做得很快</b> — 載具提早八個工作日完成、分鏡提前兩天全部收工；
      但<b>場景線卡了一段</b>，城市和街道的設計圖拖到 9/8 才定案，所以 8/31 該開工的城市建模到現在還沒動。
      下一關 10/2 要交「樣片分鏡＋故事／角色正式規劃」，分鏡已經在手上了，缺的是撐得住分鏡的場景。
    </p>

    <div class="kpis">
      <div class="kpi">
        <span class="n i" id="kpi-days">—<small>天</small></span>
        <div class="k">距 10/2 檢查點</div>
        <p class="note">要交：故事／角色正式規劃、樣片分鏡。</p>
      </div>
      <div class="kpi">
        <span class="n g">+8<small>天</small></span>
        <div class="k">跑最快的</div>
        <p class="note">AI 載具建模 8/26–8/27 完成，計畫排 9/7–9/11。</p>
      </div>
      <div class="kpi">
        <span class="n r">−7<small>天</small></span>
        <div class="k">拖最久的</div>
        <p class="note">城市／街道設計圖定案，計畫 8/28、實際 9/8。</p>
      </div>
      <div class="kpi">
        <span class="n">107<small>/110</small></span>
        <div class="k">日誌填報</div>
        <p class="note">29 個工作日、四個人。只有 8/17 婉柔漏一筆，很穩。</p>
      </div>
      <div class="kpi">
        <span class="n w" id="kpi-stall">—</span>
        <div class="k">寫太像的段落</div>
        <p class="note">同一句話連續填 3 天以上，看不出當天推進了多少。</p>
      </div>
    </div>
  </div>

  <!-- 進度 -->
  <section id="now">
    <div class="sh">
      <h3>每條線現在的位置</h3>
      <p>拿時程表上每個節點該完成的日期，比對你們日誌裡實際完成／開工的日期。右邊綠色是提前，左邊粉色是落後，單位是工作日。</p>
    </div>
    <div class="dev">
      <div class="dev-axis">
        <div></div>
        <div class="axis-track">
          <span style="left:6%">慢 8 天</span><span style="left:28%">4 天</span>
          <span style="left:50%">準時</span><span style="left:72%">4 天</span><span style="left:94%">快 8 天</span>
        </div>
      </div>
      <div id="devrows"></div>
    </div>
    <div class="legend">
      <span><i style="background:var(--green)"></i>比計畫快</span>
      <span><i style="background:var(--tx3)"></i>照計畫走</span>
      <span><i style="background:var(--neg)"></i>比計畫慢</span>
      <span style="color:var(--neg)">慢的四項全部是場景／環境</span>
    </div>
  </section>

  <!-- 六週 -->
  <section id="weeks">
    <div class="sh">
      <h3>六週回顧</h3>
      <p>每一週計畫排了什麼、你們實際做了什麼。</p>
    </div>
    <div class="weeks" id="weekwrap"></div>
  </section>

  <!-- 每個人 -->
  <section id="people">
    <div class="sh">
      <h3>每個人的線</h3>
      <p>時程表指派給你的工項，跟日誌裡你實際做的工項。這不是考績，是拿來看誰手上塞太多、誰可以接手。</p>
    </div>
    <div class="people" id="peoplewrap"></div>
  </section>

  <!-- 要注意 -->
  <section id="watch">
    <div class="sh">
      <h3>要注意的三件事</h3>
      <p>做了但表上沒排的、表上排了但還沒開始的、以及看不出推進速度的。</p>
    </div>
    <div class="excs">
      <div class="exc">
        <h4><span class="dot" style="background:var(--warn)"></span>做了，但時程表上沒有</h4>
        <ul>
          <li><b>機械判官／盧西恩建模</b> — 容瀚<i>8/27–8/28、9/4 · 時程表 8–9 月沒有這一欄</i></li>
          <li><b>GPT 風格統一生圖工具</b> — 鈞陽<i>9/2、9/4 兩個工作日 · 工具本身可能很划算，但沒排進表裡就看不見成本</i></li>
          <li><b>Seedance 2.5 動作鏡頭測試</b> — 容瀚<i>9/9 · 應該算在 5+5 的 AI 生成額度裡</i></li>
        </ul>
      </div>
      <div class="exc">
        <h4><span class="dot" style="background:var(--neg)"></span>排了，但還沒開始</h4>
        <ul>
          <li><b>城市建模</b><i>計畫 8/31 起 · 到 9/10 還在設計階段，慢了 8 個工作日</i></li>
          <li><b>諾亞的房間 建模／投影</b><i>計畫 9/3–9/11 · 日誌裡完全沒出現過「房間建模」</i></li>
          <li><b>AI 機器人手臂 拆 UV</b><i>計畫 9/9–9/11 · 婉柔還在畫衣服貼圖</i></li>
        </ul>
      </div>
      <div class="exc">
        <h4><span class="dot" style="background:var(--tx3)"></span>同一句連續填 3 天以上</h4>
        <ul id="stalls"></ul>
      </div>
    </div>
  </section>

  <!-- 日誌怎麼填 -->
  <section id="howto">
    <div class="sh">
      <h3>日誌怎麼填</h3>
      <p>Notion 的「🖍️ 進度日誌」已經加好四個新欄位了。多花大約 20 秒，換來的是大家看得懂彼此的進度、卡住當天就有人知道。</p>
    </div>

    <h4 class="sub"><span class="tag">B</span>新增的四個欄位</h4>
    <p class="hint">綠色標記是新的，已經幫你們開好，打開資料庫就看得到（用「每日填報」這個視圖）。</p>
    <div class="tw">
      <table class="wide">
        <thead><tr><th>欄位</th><th>型別</th><th>怎麼填</th></tr></thead>
        <tbody>
          <tr><td>日期</td><td class="d">日期</td><td class="next">照舊</td></tr>
          <tr><td>人員</td><td class="d">人員</td><td class="next">照舊</td></tr>
          <tr><td>摘要</td><td class="d">標題</td><td class="next">統一寫 <code>MMDD_姓名</code>，例如 <code>0914_江宸欣</code></td></tr>
          <tr><td>工項<span class="new">新</span></td><td class="d">多選下拉</td><td class="next">今天碰到哪幾類就勾哪幾類，<b>可以複選</b>。選項清單見下方 C</td></tr>
          <tr><td>今日進度回報</td><td class="d">文字</td><td class="next">改成寫「今天多做了什麼」，寫法見下方 D。<b>子項（城市／S1／上衣…）就寫在這裡，不另外開欄位</b></td></tr>
          <tr><td>進度完成度<span class="new">新</span></td><td class="d">百分比</td><td class="next">這個子項<b>累計</b>做到幾成，不是今天做了多少。抓大概就好，不用精算</td></tr>
          <tr><td>狀態<span class="new">新</span></td><td class="d">單選下拉</td><td class="next">
            <span class="badge b-blue">進行中</span>
            <span class="badge b-yel">待確認</span>
            <span class="badge b-red">卡住</span>
            <span class="badge b-grn">完成</span>
          </td></tr>
          <tr><td>產出路徑<span class="new">新</span></td><td class="d">文字</td><td class="next"><code>_Dailies\MMDD\</code> 之後的相對路徑，驗收時才找得到檔案</td></tr>
          <tr><td>明日進度安排</td><td class="d">文字</td><td class="next">照舊 — 這欄其實最有價值，寫得出來代表今天真的收斂了</td></tr>
        </tbody>
      </table>
    </div>

    <div class="callout">
      <span class="ic" aria-hidden="true">!</span>
      <p><b>「產出路徑」不取代 Zulip。</b>Notion 這欄只是讓大家在看進度時能順手找到檔案；
      實際的檔案交付<b>還是要照現行流程在 Zulip 回報</b>，兩邊都要填，不能只填一邊。</p>
    </div>

    <div class="callout">
      <span class="ic" aria-hidden="true">!</span>
      <p><b>「卡住」不是扣分，是求救鈕。</b>狀態選「卡住」的日誌會自動出現在資料庫的
      <b>「🚧 卡住」視圖</b>裡。卡住當天就選，不要等到週一例會才講 —
      城市那條線就是因為卡點晚了一週才浮出來。</p>
    </div>

    <h4 class="sub"><span class="tag">C</span>「工項」選什麼</h4>
    <p class="hint">這 14 個選項直接照抄方缺版時程表的欄位群，名稱一字不改 — 名稱一致，日誌才對得上時程表。</p>
    <div class="tw">
      <table class="wide">
        <thead><tr><th>工項</th><th>你今天做的是這些的話就選它</th></tr></thead>
        <tbody>
          <tr><td><span class="badge b-gry">企劃書</span></td><td class="next">標準字&amp;LOGO、海報、企劃書、時程規劃／報告</td></tr>
          <tr><td><span class="badge b-gry">劇本</span></td><td class="next">世界觀、故事大綱、完整故事、分鏡、MB、角色設定、風格設定</td></tr>
          <tr><td><span class="badge b-gry">美術</span></td><td class="next">場景設計（城市／街道／諾亞的房間／競技場）、角色設計（艾可／諾亞服裝／AI）</td></tr>
          <tr><td><span class="badge b-gry">Model+Rig</span></td><td class="next">建模、拆件、綁骨架、綁控制器、權重、表情與口型</td></tr>
          <tr><td><span class="badge b-gry">材質</span></td><td class="next">拆 UV、畫貼圖、Substance Painter</td></tr>
          <tr><td><span class="badge b-gry">動作</span></td><td class="next">若亞的一天、監獄、電梯井／隧道、競技場</td></tr>
          <tr><td><span class="badge b-gry">特效</span></td><td class="next">3D 特效 A／B</td></tr>
          <tr><td><span class="badge b-gry">燈光</span></td><td class="next">城市、諾亞的房間、街道、監獄、競技場</td></tr>
          <tr><td><span class="badge b-gry">算圖</span></td><td class="next">各場景 render</td></tr>
          <tr><td><span class="badge b-gry">2D特效</span></td><td class="next">諾亞科技面板、B／C／D</td></tr>
          <tr><td><span class="badge b-gry">合成</span></td><td class="next">Nuke／AE 合成</td></tr>
          <tr><td><span class="badge b-gry">後製(剪片)</span></td><td class="next">剪接、輸出</td></tr>
          <tr><td><span class="badge b-gry">音樂音效</span></td><td class="next">開頭、各場景音效</td></tr>
          <tr><td><span class="badge b-gry">polish</span></td><td class="next">成片最後調整</td></tr>
        </tbody>
      </table>
    </div>
    <div class="callout">
      <span class="ic" aria-hidden="true">?</span>
      <p><b>學軟體、做工具、聽講座怎麼辦？</b>目前 14 個選項裡沒有對應的格子（Nuke 學習、Seedance 測試、GPT 生圖工具都算）。
      先在「今日進度回報」寫清楚，工項留空；要不要加第 15 項「工具／研發」，等跟 PM 確認。</p>
    </div>

    <h4 class="sub"><span class="tag">D</span>「今日進度回報」怎麼寫</h4>
    <p class="hint">三個東西寫齊就夠了：<b>對象 ＋ 做了什麼 ＋ 還剩什麼</b>。最後那個「還剩什麼」最關鍵 — 有它，隔天才看得出來推進了多少。下面全部是你們自己寫過的句子。</p>
    <div class="dd2">
      <div class="dd bad">
        <div class="dd-h">✗ 看不出進度</div>
        <ul>
          <li>機器人手臂建模<i>8/19–8/25 連續五個工作日一模一樣</i></li>
          <li>若亞服裝建模<i>8/19–8/24 連續四天一模一樣</i></li>
          <li>畫衣服貼圖<i>9/8–9/10 連續三天一模一樣</i></li>
          <li>設計整個城市和街道<i>9/7 · 看不出第幾版、也看不出卡在哪</i></li>
          <li>場景設計 競技場<i>8/24–8/27 · 無法判斷完成度</i></li>
        </ul>
      </div>
      <div class="dd good">
        <div class="dd-h">✓ 一眼看得懂</div>
        <ul>
          <li>手臂建模：肩關節＋上臂完成，剩前臂和手掌<i>完成度 60% · 別人接手看得懂</i></li>
          <li>若亞服裝：上衣完成，褲子開版中，鞋子還沒動<i>三件拆開寫，卡在哪一件很清楚</i></li>
          <li>上衣貼圖：布料底色＋磨損完成，待加繡線和 Logo<i>「待加」就直接變成明天的安排</i></li>
          <li>城市：天際線比例第三版，六邊形元素試打樣，待琬婷確認方向<i>版次＋待辦＋要等誰，卡點直接浮出來</i></li>
          <li>競技場：外觀定稿，內部座席區草圖完成<i>外 100%／內 30%，不會變成一個黑箱</i></li>
        </ul>
      </div>
    </div>
    <div class="callout">
      <span class="ic" aria-hidden="true">★</span>
      <p><b>宸欣的分鏡寫法就是範本。</b>9/3「S7 劇本拆解（分鏡）完、S1 分鏡繪製」、9/7「S3 分鏡完、S6 分鏡完」 —
      對象、做了什麼、還剩什麼三個都有，所以分鏡是四條線裡進度最好判讀的一條。照這個寫就對了。</p>
    </div>

    <h4 class="sub"><span class="tag">E</span>填報範本</h4>
    <p class="hint">複製這段貼進你的日誌頁面，照著填。整套跑下來大概一分鐘。</p>
    <div class="tmpl"><b>摘要</b>　　　　<u>MMDD_你的名字</u>
<b>工項</b>　　　　〔多選，可複選〕
<b>進度完成度</b>　這個子項累計 ___%（不是今天做了多少）
<b>狀態</b>　　　　進行中 / 待確認 / 卡住 / 完成

<b>今日進度回報</b>
　　對象：____________（城市／S1／上衣／機器人手臂…）
　　完成：____________
　　還剩：____________

<b>明日進度安排</b>
　　____________

<b>產出路徑</b>　　_Dailies\MMDD\____________
　　<u>↑ 檔案本身還是要在 Zulip 回報，這欄不能取代</u></div>
  </section>

  <!-- 全紀錄 -->
  <section id="log">
    <div class="sh">
      <h3>全紀錄</h3>
      <p>8/03–9/10 共 107 筆。「兌現」欄是把前一天的「明日安排」跟隔天的「今日回報」對起來看：✓ 有做到、~ 做了一部分、✗ 換做別的。橘色代表跟前一天寫得幾乎一樣。</p>
    </div>
    <div class="filters" id="filters">
      <button class="chip" data-p="" aria-pressed="true">全部</button>
      <button class="chip" data-p="江宸欣" aria-pressed="false">江宸欣</button>
      <button class="chip" data-p="張容瀚" aria-pressed="false">張容瀚</button>
      <button class="chip" data-p="鄭鈞陽" aria-pressed="false">鄭鈞陽</button>
      <button class="chip" data-p="邵婉柔" aria-pressed="false">邵婉柔</button>
      <span class="cnt" id="count"></span>
    </div>
    <div class="tw">
      <table class="wide" id="logtable">
        <thead><tr><th>日期</th><th>人員</th><th>今日進度回報</th><th>明日進度安排</th><th style="text-align:center">兌現</th></tr></thead>
        <tbody id="logbody"></tbody>
      </table>
    </div>
  </section>

  <p class="foot">
    資料：Notion「🖍️ 進度日誌」8/03–9/10 共 107 筆、「時程與檢查點」；Google 試算表《Logic Error 時程表 || 2026 夢想》分頁「方缺版拆解」。9/11 當天日誌尚未填報。<br>
    接下來的關卡：<b style="color:var(--green)">10/02</b> 故事／角色正式規劃＋樣片分鏡 · 10/23 世界觀／角色定案＋樣片 MB＋期中簡報 · 10/30 期中進度報告 · 11/13 樣片 A copy＋字幕 · 11/27 B copy＋期末總驗收 · 12/18 成果發表。
  </p>
</div>

<script>
/* 10/2 倒數 */
(function(){
  var t = new Date(2026,9,2), n = new Date();
  var d = Math.ceil((t - new Date(n.getFullYear(),n.getMonth(),n.getDate()))/86400000);
  document.getElementById("kpi-days").innerHTML = (d>0?d:0) + '<small>天</small>';
})();

var DEV = [
  {line:"Model+Rig · AI 載具", node:"載具建模", plan:"9/07–9/11", act:"8/26–8/27", d:8},
  {line:"Model+Rig · 機器人手臂", node:"綁骨架＋權重", plan:"9/07–9/11", act:"8/31–9/03", d:5},
  {line:"Model+Rig · 未來人服裝", node:"建模起始／綁骨架", plan:"8/24 · 8/31", act:"8/18 · 8/25", d:4},
  {line:"劇本 · 完整故事", node:"10 分鐘劇本完稿", plan:"8/28", act:"8/24", d:4},
  {line:"分鏡", node:"10 分鐘分鏡完成", plan:"9/11", act:"9/09", d:2},
  {line:"時程規劃／報告", node:"協會交期 · 時程規劃", plan:"8/14", act:"8/13", d:1},
  {line:"劇本 · 世界觀", node:"世界觀定案（蜂巢）", plan:"8/06", act:"8/06", d:0},
  {line:"美術 · 角色設計", node:"三視圖／表情圖完成", plan:"8/18", act:"8/18", d:0},
  {line:"材質 · 貼圖", node:"頭皮貼圖／拆 UV 起始", plan:"8/31", act:"8/31", d:0},
  {line:"美術 · 競技場／房間", node:"設計圖定案", plan:"8/28", act:"8/28", d:0},
  {line:"材質 · 機器人手臂", node:"拆 UV 起始", plan:"9/09", act:"還沒開始", d:-2},
  {line:"場景 · 諾亞的房間", node:"建模／投影起始", plan:"9/03", act:"還沒開始", d:-5},
  {line:"美術 · 城市／街道", node:"設計圖定案", plan:"8/28", act:"9/08", d:-7},
  {line:"場景 · 城市建模", node:"建模起始", plan:"8/31", act:"還沒開始", d:-8}
];
var MAX=8;
document.getElementById("devrows").innerHTML = DEV.map(function(r){
  var pct=Math.abs(r.d)/MAX*50, bar, val;
  if(r.d===0){
    bar='<div class="dev-bar zero" style="left:calc(50% - 3px)"></div>';
    val='<span class="dev-val" style="left:calc(50% + 14px);color:var(--tx3)">準時</span>';
  } else if(r.d>0){
    bar='<div class="dev-bar pos" style="left:50%;width:'+pct+'%"></div>';
    val='<span class="dev-val" style="left:calc(50% + '+pct+'% + 10px);color:var(--green)">快 '+r.d+' 天</span>';
  } else {
    bar='<div class="dev-bar neg" style="right:50%;width:'+pct+'%"></div>';
    val='<span class="dev-val" style="right:calc(50% + '+pct+'% + 10px);color:var(--neg)">慢 '+(-r.d)+' 天</span>';
  }
  return '<div class="dev-row"><div class="dev-name"><b>'+r.line+'</b><i>'+r.node+' · 計畫 '+r.plan+' → 實際 '+r.act+'</i></div>'+
    '<div class="dev-track"><div class="dev-zero"></div>'+bar+val+'</div></div>';
}).join("");

var WEEKS=[
 {w:"W1",when:"8/03–8/07",plan:"世界觀重塑發想 → 定案；決定要不要沿用《奧術》《蜘蛛人》《忍者龜》的風格；諾亞／艾可角色發想。",
  act:"8/6 定案為蜂巢，也確立沿用原風格；8/7 起四個人一起進 60 分鐘劇本。",vc:"v-ok",vt:"如期"},
 {w:"W2",when:"8/10–8/14",plan:"第 1–4 集劇情架構與撰寫；8/12 起時程規劃；<b>8/13–8/14 協會交期：四個月輔導規劃與甘特圖</b>；角色草圖 → 設計圖。",
  act:"8/10 二到四集劇情完成；8/11–8/13 時程規劃＋簡報，8/13「動協簡報做完」；8/13–8/14 艾可線稿與三視圖。",vc:"v-g",vt:"交期提前一天達成"},
 {w:"W3",when:"8/17–8/21",plan:"細部時程規劃；10 分鐘劇本討論撰寫；場景設計四項發想 → 討論／圖；三視圖、表情圖、設計稿上色；<b>8/20–8/21 全員講座</b>。",
  act:"8/17 三視圖上底色、8/18 表情圖都如期；8/18 服裝建模提前開工（計畫 8/24）；場景設計 8/19 才第一筆，晚兩天。",vc:"v-w",vt:"前段提前・場景起步晚"},
 {w:"W4",when:"8/24–8/28",plan:"10 分鐘劇本收尾；<b>8/28 場景設計圖定案（城市／街道／房間／競技場）</b>；諾亞五官身形調整；服裝上衣褲子；機器人手臂建模。",
  act:"8/24 劇本完稿（提前 4 天）；8/25 綁骨架、8/26 綁控制器、8/27–8/28 面部權重，整條 Rig 線提前；8/26–8/27 載具建模完成（計畫 9/7）；8/27–8/28 機械判官建模（表上沒排）。競技場 8/28 風格確立，城市只到「細部調整」。",vc:"v-w",vt:"資產超前・城市沒定案"},
 {w:"W5",when:"8/31–9/04",plan:"10 分鐘分鏡開跑；未來人服裝綁骨架權重；城市建模、街道；頭皮貼圖、上衣拆 UV → 畫貼圖；<b>9/03–9/04 協會交期：世界觀故事／角色雛形</b>。",
  act:"8/31 分鏡開工、頭皮貼圖與拆 UV 如期；機器人綁骨架 9/1–9/3 完成（提前 4 天）；協會交期達成。城市那條退回「城市街道設計」，建模沒開工；鈞陽 9/2、9/4 投入自製 GPT 風格生圖工具兩天。",vc:"v-w",vt:"交期達成・城市退回設計"},
 {w:"W6",when:"9/07–9/11",plan:"分鏡收尾到 9/11；機器人手臂綁骨架權重、載具建模；街道、城市投影、房間投影；褲子畫貼圖、手臂拆 UV。",
  act:"9/09 分鏡 S1–S7 全部完成，提前兩天；9/09–9/10 轉進 MB 和 Seedance 動作測試。9/08 城市才「定案增加六邊形元素」並開始競技場建模；房間、街道、手臂拆 UV 都還沒啟動。",vc:"v-r",vt:"分鏡提前・環境全面落後"}
];
document.getElementById("weekwrap").innerHTML = WEEKS.map(function(w){
  return '<div class="week"><div class="week-when"><b>'+w.w+'</b>'+w.when+'</div><div class="week-body">'+
   '<div class="wl plan"><span>計畫</span><span>'+w.plan+'</span></div>'+
   '<div class="wl"><span>實際</span><span>'+w.act+'</span></div>'+
   '<div><span class="vd '+w.vc+'">'+w.vt+'</span></div></div></div>';
}).join("");

var L=[
["08-03","江宸欣","世界觀發想 路人服裝發想","劇情構思 學習 nuke"],
["08-03","張容瀚","世界觀、美術設定發想","美術設定發想、粒子特效學習"],
["08-04","張容瀚","人物對立點構思 角色造型發想","繼續腳本及設定討論"],
["08-05","張容瀚","新世界觀發想 人物美術設定","人物美術設定 劇本改動討論"],
["08-05","江宸欣","人物美術設定","人物美術設定 劇本討論"],
["08-06","鄭鈞陽","討論劇本 概念美術發想","概念美術發想 完善劇本"],
["08-06","張容瀚","劇本討論 美術設定","劇本討論 美術設定"],
["08-06","江宸欣","劇本討論 角色發想","劇本討論 美術設計"],
["08-06","邵婉柔","劇本討論 概念美術發想","概念美術發想 劇本討論"],
["08-07","邵婉柔","60 分鐘劇本討論 撰寫計畫書","完善 60 分鐘劇本 撰寫計畫書"],
["08-07","江宸欣","劇本討論","劇本討論"],
["08-07","鄭鈞陽","完善 60 分鐘劇本","完善整體劇本"],
["08-07","張容瀚","完善世界觀 劇本討論","劇本討論"],
["08-10","鄭鈞陽","劇本第二集解決 三四集概念完成","完善劇本 概念美術"],
["08-10","張容瀚","諾亞角色設計 世界觀討論","美術設計 劇本討論"],
["08-10","邵婉柔","劇本討論三四集 撰寫企畫書","劇本討論第三集轉折劇情 撰寫企畫書"],
["08-10","江宸欣","劇本討論 美術設定","劇本討論"],
["08-11","江宸欣","角色設計","時程安排"],
["08-11","張容瀚","諾亞角色設計","時程規畫表"],
["08-11","邵婉柔","完善企劃書 第三集及第一集","時程規劃＋簡報"],
["08-11","鄭鈞陽","修改故事 BUG 完善世界觀","寫給協會的排程"],
["08-12","江宸欣","角色設計 簡報製作","角色設計"],
["08-12","張容瀚","時程規劃討論 機器人角色微調","諾亞角色調整"],
["08-12","鄭鈞陽","時程表規劃 劇本完善","美術概念設計"],
["08-12","邵婉柔","時程表規劃 劇本結局","細流時程表規劃 美術設定"],
["08-13","張容瀚","艾可線稿 時程規劃","角色設計"],
["08-13","鄭鈞陽","動協簡報做完","概念美術設計"],
["08-13","江宸欣","角色設計 作品規劃討論","判官設計 競技場設計"],
["08-13","邵婉柔","時程規劃 簡報製作","時程細部規劃 美術討論"],
["08-14","邵婉柔","細部流程規劃","細部流程規劃、討論 10 分鐘劇本、場景發想"],
["08-14","鄭鈞陽","概念美術 10 分鐘劇本構想","10 分鐘文字腳本 場景設計發想"],
["08-14","張容瀚","艾可三視圖 未來人服裝","人物表情圖 三視圖"],
["08-14","江宸欣","繪製載具、競技場判官","繪製判官三視圖"],
["08-17","江宸欣","大頭三視圖、角色上色","角色上色"],
["08-17","張容瀚","諾亞三視圖及底色","人物表情圖"],
["08-17","鄭鈞陽","十分鐘劇本構想","十分鐘劇本 概念美術"],
["08-18","邵婉柔","完善細部流程","完成細流、10 分鐘劇本完善"],
["08-18","張容瀚","人物表情圖","機器人手臂建模"],
["08-18","江宸欣","角色上色、衣服建模","服裝建模"],
["08-18","鄭鈞陽","10 分鐘劇本修改","10 分鐘劇本修改"],
["08-19","江宸欣","若亞服裝建模","若亞服裝建模"],
["08-19","鄭鈞陽","10 分鐘劇本修改","10 分鐘劇本修改、聽講座"],
["08-19","邵婉柔","完善細部時程表、競技場設計","競技場設計"],
["08-19","張容瀚","機器人手臂建模","機器人手臂建模"],
["08-20","張容瀚","機器人手臂建模","機器人手臂建模"],
["08-20","鄭鈞陽","寫劇本 聽演講","聽演講"],
["08-20","邵婉柔","場景設計 演講","場景設計 演講"],
["08-20","江宸欣","若亞服裝建模","若亞服裝建模"],
["08-21","邵婉柔","場景設計 聽演講","場景設計"],
["08-21","張容瀚","機器人手臂建模","機器人手臂建模"],
["08-21","江宸欣","若亞服裝建模","若亞服裝建模"],
["08-21","鄭鈞陽","劇本編寫 聽講座","劇本編寫"],
["08-24","邵婉柔","場景設計 競技場","場景設計 競技場"],
["08-24","江宸欣","若亞服裝建模","若亞服裝建模"],
["08-24","鄭鈞陽","10 分鐘劇本寫完","場景設計、概念設計"],
["08-24","張容瀚","機器人手臂建模","機器人手臂建模"],
["08-25","邵婉柔","場景設計 競技場","場景設計 競技場 房間"],
["08-25","鄭鈞陽","場景設計 城市、劇本","場景設計、概念設計"],
["08-25","江宸欣","若亞服裝建模 綁骨架","若亞服裝建模 綁骨架"],
["08-25","張容瀚","機器人手臂建模","車建模"],
["08-26","邵婉柔","場景設計競技場","場景設計競技場、諾亞房間"],
["08-26","張容瀚","車建模","車建模"],
["08-26","江宸欣","綁控制器","綁控制器"],
["08-26","鄭鈞陽","場景設計、概念美術","場景設計城市、調整劇本"],
["08-27","邵婉柔","場景設計 競技場 房間","場景設計 競技場 房間"],
["08-27","鄭鈞陽","場景設計 城市","場景設計 城市"],
["08-27","張容瀚","車完成 機械判官建模","機械判官建模"],
["08-27","江宸欣","面部權重調整","面部權重調整"],
["08-28","江宸欣","面部權重調整","畫分鏡、權重修改"],
["08-28","鄭鈞陽","場景設計城市細部調整","建模投影城市"],
["08-28","邵婉柔","場景設計 競技場風格調整 競技場內部 房間","競技場內部 頭皮貼圖"],
["08-28","張容瀚","機械判官建模","畫分鏡 機械判官建模最後調整"],
["08-31","江宸欣","分鏡繪製","分鏡繪製"],
["08-31","邵婉柔","競技場調整、頭皮貼圖、衣服拆 UV","衣服、褲子拆 UV"],
["08-31","張容瀚","機器人拆件 骨架","機器人綁骨架"],
["08-31","鄭鈞陽","城市街道設計","城市街道建模"],
["09-01","邵婉柔","衣服褲子鞋子拆 UV","鞋子拆 UV、畫貼圖"],
["09-01","張容瀚","綁機器人骨架","綁機器人控制器"],
["09-01","鄭鈞陽","更改城市場景、嘗試建模","更改城市場景、嘗試建模"],
["09-01","江宸欣","分鏡 S1–S3","分鏡 S3–S7"],
["09-02","江宸欣","S3–S7 劇本拆解（分鏡）","S7 劇本拆解（分鏡）完、S1 分鏡繪製"],
["09-02","鄭鈞陽","場景設計城市 用 GPT 製作穩定風格生圖的插件","特休一天"],
["09-02","張容瀚","機器人控制器綁定","機器人手部機關綁定"],
["09-02","邵婉柔","拆好鞋子 UV、學 SP 跟成功匯入檔案","學 SP 跟嘗試畫貼圖"],
["09-03","張容瀚","機器人控制器完成","畫分鏡 諾亞表情綁定"],
["09-03","江宸欣","S7 劇本拆解（分鏡）完、S1 分鏡繪製","S2 分鏡（18 格）"],
["09-03","邵婉柔","畫褲子 UV","畫褲子 UV"],
["09-04","鄭鈞陽","用 ChatGPT 製作了確定風格的網站，把圖丟進去可依設定好的風格匯出","城市、街道設計完、建模"],
["09-04","張容瀚","盧西恩模型及權重調整 控制器綁定","諾亞表情及口型"],
["09-04","江宸欣","S2-0～S3-2 分鏡","S3 分鏡完、動作戲分鏡"],
["09-04","邵婉柔","畫褲子 UV","畫褲子 UV"],
["09-07","張容瀚","處理諾亞權重問題 綁定諾亞及盧西恩手指控制器","控制器綁定完成"],
["09-07","邵婉柔","畫褲子貼圖","畫衣服貼圖"],
["09-07","鄭鈞陽","設計整個城市和街道","設計整個城市和街道"],
["09-07","江宸欣","S3 分鏡完、S6 分鏡完","S7～S7-4 分鏡"],
["09-08","邵婉柔","畫衣服貼圖","畫衣服貼圖"],
["09-08","鄭鈞陽","城市定案增加六邊形元素、競技場建模","競技場建模、生成城市遠景定案圖"],
["09-08","江宸欣","S7-0～S7-3 分鏡","S7 完、S4～S5"],
["09-08","張容瀚","盧西恩及諾亞口形圖 腳色最後調整","S6 動態分鏡"],
["09-09","鄭鈞陽","競技場建模，確認競技場的大結構","建模競技場"],
["09-09","張容瀚","Seedance 2.5 動作鏡頭嘗試","S6 motion board"],
["09-09","江宸欣","S7 完、S4～S5 完","製作 MB S1"],
["09-09","邵婉柔","畫衣服貼圖","畫衣服貼圖"],
["09-10","張容瀚","S6 motion board","S6 motion board"],
["09-10","鄭鈞陽","合理化競技場的建築結構、想怎麼調整分鏡","建模競技場、想怎麼調整分鏡"],
["09-10","邵婉柔","畫衣服貼圖","畫衣服貼圖"],
["09-10","江宸欣","製作 MB S1","修改分鏡 S1、S2、S3"]
];

function norm(s){return (s||"").replace(/[\s、，,。．的了與和及　]/g,"")}
function bg(s){var g={},i;for(i=0;i<s.length-1;i++)g[s.slice(i,i+2)]=1;return g}
function sim(a,b){
  a=norm(a);b=norm(b);if(!a||!b)return 0;
  var A=bg(a),B=bg(b),ka=Object.keys(A),kb=Object.keys(B),n=0,i;
  if(!ka.length||!kb.length)return a===b?1:0;
  for(i=0;i<ka.length;i++)if(B[ka[i]])n++;
  return (2*n)/(ka.length+kb.length);
}

var byP={};
L.forEach(function(r,i){(byP[r[1]]=byP[r[1]]||[]).push(i)});
var hit=new Array(L.length),stalls=[],stallIdx={};
Object.keys(byP).forEach(function(p){
  var ix=byP[p],k,run=1,start=0;
  for(k=1;k<ix.length;k++){
    var pv=L[ix[k-1]],cu=L[ix[k]];
    if(/特休/.test(pv[3]))continue;
    var s=sim(pv[3],cu[2]);
    hit[ix[k]] = s>=0.34?"y":(s>=0.16?"p":"n");
  }
  for(k=1;k<=ix.length;k++){
    var same = k<ix.length && sim(L[ix[k]][2],L[ix[k-1]][2])>=0.75;
    if(same){ if(run===1)start=k-1; run++; stallIdx[ix[k]]=1; }
    else{ if(run>=3) stalls.push({p:p,text:L[ix[start]][2],from:L[ix[start]][0],to:L[ix[start+run-1]][0],n:run}); run=1; }
  }
});
document.getElementById("kpi-stall").textContent = stalls.length;
stalls.sort(function(a,b){return b.n-a.n});
document.getElementById("stalls").innerHTML = stalls.map(function(s){
  return '<li><b>'+s.text+'</b> — '+s.p+'<i>'+s.from.replace("-","/")+' → '+s.to.replace("-","/")+' · 連續 '+s.n+' 個工作日</i></li>';
}).join("");

var PEOPLE=[
 {n:"江宸欣",i:"江",plan:"角色設計圖／上色、AI 判官、未來人服裝 Model+Rig、10 分鐘分鏡",
  act:"整條線都跟著計畫走。8/18 提前開工服裝建模，8/25–8/28 綁骨架權重提前 4 天，8/31 接手分鏡、9/09 全部完成。",
  drift:"沒有。四個人裡唯一全程貼著計畫的，日誌也寫得最清楚 — 大家照他的寫法填就對了。"},
 {n:"張容瀚",i:"張",plan:"諾亞／艾可三視圖、AI 中樞、機器人手臂與載具 Model+Rig、分鏡",
  act:"角色設定如期；手臂建模 8/19–8/25、載具 8/26–8/27（計畫 9/7）、綁骨架 8/31–9/3（計畫 9/7）。9/9 起轉 MB。",
  drift:"機械判官／盧西恩建模（8/27–9/4）時程表上沒有這一欄，要補排進去才算得到工時。"},
 {n:"鄭鈞陽",i:"鄭",plan:"完整故事（10 分鐘劇本）、城市與街道場景設計 → 建模 → 投影",
  act:"劇本 8/24 提前完稿。城市線 8/25 起一直在設計、8/28「細部調整」、9/7 還在「設計整個城市和街道」、9/8 才定案。",
  drift:"手上同時有劇本、城市、街道三條，還加上 9/2、9/4 自製 GPT 生圖工具兩天。城市建模到現在沒開工 — 這條線需要有人接手一塊。"},
 {n:"邵婉柔",i:"邵",plan:"時程規劃／簡報、諾亞房間與競技場場景設計、諾亞／服裝材質貼圖",
  act:"時程規劃 8/13 交件；競技場 8/19–8/28 設計確立；8/31 起轉材質線，拆 UV 與貼圖大致按表推進。",
  drift:"上衣／褲子的順序跟計畫對調（影響不大）；諾亞房間在 8/26–8/28 之後就沒再出現了。"}
];
document.getElementById("peoplewrap").innerHTML = PEOPLE.map(function(p){
  var ix=byP[p.n]||[],days={},sn=0;
  ix.forEach(function(i){days[L[i][0]]=1;if(stallIdx[i])sn++});
  return '<div class="person"><div class="ptop"><span class="pav">'+p.i+'</span>'+
   '<div><h4>'+p.n+'</h4><div class="sub">8/03 – 9/10</div></div></div>'+
   '<div class="pstat">'+
     '<div><b>'+ix.length+'</b><span>日誌</span></div>'+
     '<div><b>'+Object.keys(days).length+'</b><span>回報天數</span></div>'+
     '<div><b class="'+(sn>=4?'w':'')+'">'+sn+'</b><span>重複日</span></div>'+
   '</div><div class="plines">'+
     '<div><em>計畫</em><span>'+p.plan+'</span></div>'+
     '<div><em>實際</em><span>'+p.act+'</span></div>'+
     '<div><em>備註</em><span style="color:var(--tx2)">'+p.drift+'</span></div>'+
   '</div></div>';
}).join("");

var tb=document.getElementById("logbody"),ce=document.getElementById("count"),flt="";
function render(){
  var rows=[];
  L.forEach(function(r,i){ if(!flt||r[1]===flt) rows.push([r,i]); });
  tb.innerHTML = rows.map(function(o){
    var r=o[0],i=o[1],h=hit[i],m;
    if(h==="y")m='<span class="hm hm-y">✓</span>';
    else if(h==="p")m='<span class="hm hm-p">~</span>';
    else if(h==="n")m='<span class="hm hm-n">✗</span>';
    else m='<span class="hm" style="color:var(--tx3)">–</span>';
    return '<tr class="'+(stallIdx[i]?'stall':'')+'"><td class="d">'+r[0].replace("-","/")+'</td>'+
      '<td class="p">'+r[1]+'</td><td class="today">'+r[2]+'</td>'+
      '<td class="next">'+r[3]+'</td><td style="text-align:center">'+m+'</td></tr>';
  }).join("");
  ce.textContent = rows.length + " 筆";
}
document.getElementById("filters").addEventListener("click",function(e){
  var b=e.target.closest(".chip"); if(!b)return;
  flt=b.getAttribute("data-p");
  var cs=document.querySelectorAll("#filters .chip"),i;
  for(i=0;i<cs.length;i++)cs[i].setAttribute("aria-pressed",String(cs[i]===b));
  render();
});
render();
</script>
</body>
</html>
