# denki1
<!DOCTYPE html>

<html lang="ja">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>第一種電気工事士 学科試験 完全攻略</title>
<link href="https://fonts.googleapis.com/css2?family=Noto+Sans+JP:wght@400;500;700&family=BIZ+UDGothic:wght@400;700&display=swap" rel="stylesheet">
<style>
:root {
  --bg: #0f1117;
  --bg2: #1a1d27;
  --bg3: #22263a;
  --card: #1e2235;
  --border: #2e3450;
  --accent: #4f8ef7;
  --accent2: #38d9a9;
  --accent3: #ffa94d;
  --accent4: #f06595;
  --text: #e8ecf4;
  --text2: #8892b0;
  --text3: #cdd6f4;
  --red: #ff6b6b;
  --yellow: #ffd43b;
  --green: #51cf66;
}
* { box-sizing: border-box; margin: 0; padding: 0; }
body {
  font-family: 'Noto Sans JP', 'BIZ UDGothic', sans-serif;
  background: var(--bg);
  color: var(--text);
  min-height: 100vh;
  font-size: 14px;
  line-height: 1.6;
}
/* Header */
.app-header {
  background: linear-gradient(135deg, #1a1d27 0%, #0f1117 100%);
  border-bottom: 1px solid var(--border);
  padding: 16px 20px;
  position: sticky;
  top: 0;
  z-index: 100;
  display: flex;
  align-items: center;
  gap: 12px;
}
.app-header .logo {
  width: 36px; height: 36px;
  background: var(--accent);
  border-radius: 8px;
  display: flex; align-items: center; justify-content: center;
  font-size: 18px; flex-shrink: 0;
}
.app-header h1 { font-size: 15px; font-weight: 700; color: var(--text); }
.app-header p { font-size: 11px; color: var(--text2); }
.progress-bar {
  margin-left: auto;
  background: var(--bg3);
  border-radius: 99px;
  height: 6px;
  width: 80px;
  overflow: hidden;
  flex-shrink: 0;
}
.progress-fill {
  height: 100%;
  background: linear-gradient(90deg, var(--accent), var(--accent2));
  border-radius: 99px;
  transition: width 0.3s;
  width: 0%;
}

/* Layout */
.layout { display: flex; height: calc(100vh - 69px); }

/* Sidebar */
.sidebar {
width: 220px;
background: var(–bg2);
border-right: 1px solid var(–border);
overflow-y: auto;
flex-shrink: 0;
padding: 12px 0;
}
.sidebar-section { padding: 8px 16px 4px; font-size: 10px; color: var(–text2); text-transform: uppercase; letter-spacing: 0.1em; font-weight: 700; }
.nav-item {
display: flex; align-items: center; gap: 10px;
padding: 9px 16px;
cursor: pointer;
color: var(–text2);
font-size: 12px;
border-left: 3px solid transparent;
transition: all 0.15s;
user-select: none;
}
.nav-item:hover { background: var(–bg3); color: var(–text); }
.nav-item.active { background: rgba(79,142,247,0.1); color: var(–accent); border-left-color: var(–accent); }
.nav-item .icon { width: 20px; text-align: center; font-size: 14px; flex-shrink: 0; }
.nav-item .check { margin-left: auto; font-size: 11px; color: var(–accent2); }

/* Main content */
.main { flex: 1; overflow-y: auto; padding: 24px; }
.section { display: none; }
.section.active { display: block; }
.section-header { margin-bottom: 20px; }
.section-header h2 { font-size: 20px; font-weight: 700; color: var(–text); margin-bottom: 4px; }
.section-header p { font-size: 12px; color: var(–text2); }

/* Cards */
.card {
background: var(–card);
border: 1px solid var(–border);
border-radius: 12px;
padding: 16px 20px;
margin-bottom: 16px;
}
.card-title {
font-size: 13px; font-weight: 700; color: var(–text);
margin-bottom: 12px; display: flex; align-items: center; gap: 8px; flex-wrap: wrap;
}
.tag {
font-size: 10px; padding: 2px 8px; border-radius: 99px; font-weight: 700;
}
.tag-blue { background: rgba(79,142,247,0.2); color: #7ec8ff; }
.tag-green { background: rgba(56,217,169,0.2); color: #63e6be; }
.tag-orange { background: rgba(255,169,77,0.2); color: #ffd08a; }
.tag-red { background: rgba(240,101,149,0.2); color: #f9a8d4; }
.tag-gray { background: rgba(136,146,176,0.2); color: #a8b2cc; }

/* Formula box */
.formula {
background: rgba(79,142,247,0.1);
border: 1px solid rgba(79,142,247,0.3);
border-radius: 8px;
padding: 10px 16px;
font-size: 14px;
font-weight: 700;
text-align: center;
color: #7ec8ff;
margin: 8px 0;
font-family: ‘BIZ UDGothic’, monospace;
}

/* Tip/Warn boxes */
.tip {
background: rgba(56,217,169,0.08);
border-left: 3px solid var(–accent2);
border-radius: 0 8px 8px 0;
padding: 10px 14px;
font-size: 12px;
color: #63e6be;
margin-top: 10px;
line-height: 1.6;
}
.warn {
background: rgba(255,169,77,0.08);
border-left: 3px solid var(–accent3);
border-radius: 0 8px 8px 0;
padding: 10px 14px;
font-size: 12px;
color: #ffd08a;
margin-top: 10px;
line-height: 1.6;
}
.danger {
background: rgba(255,107,107,0.08);
border-left: 3px solid var(–red);
border-radius: 0 8px 8px 0;
padding: 10px 14px;
font-size: 12px;
color: #ff8787;
margin-top: 10px;
line-height: 1.6;
}

/* Grid */
.g2 { display: grid; grid-template-columns: 1fr 1fr; gap: 10px; }
.g3 { display: grid; grid-template-columns: 1fr 1fr 1fr; gap: 10px; }
.g4 { display: grid; grid-template-columns: repeat(4, 1fr); gap: 10px; }
.term {
background: var(–bg3);
border-radius: 8px;
padding: 12px;
}
.term-name { font-size: 12px; font-weight: 700; color: var(–text3); margin-bottom: 4px; }
.term-desc { font-size: 11px; color: var(–text2); line-height: 1.55; }

/* Table */
.tw { overflow-x: auto; }
table { width: 100%; border-collapse: collapse; font-size: 12px; }
th {
background: var(–bg3);
text-align: left; padding: 8px 10px;
color: var(–text2); font-weight: 700;
border-bottom: 1px solid var(–border);
font-size: 11px;
}
td {
padding: 8px 10px;
border-bottom: 1px solid var(–border);
color: var(–text);
line-height: 1.5;
}
tr:last-child td { border-bottom: none; }
tr:hover td { background: rgba(255,255,255,0.02); }

/* List */
.pl { list-style: none; }
.pl li {
font-size: 12px; color: var(–text);
padding: 5px 0; border-bottom: 1px solid var(–border);
display: flex; gap: 8px; line-height: 1.6;
}
.pl li:last-child { border-bottom: none; }
.pl li::before { content: “▸”; color: var(–accent); flex-shrink: 0; }

/* Stats */
.stats { display: grid; grid-template-columns: repeat(4,1fr); gap: 10px; margin-bottom: 20px; }
.stat {
background: var(–card);
border: 1px solid var(–border);
border-radius: 10px;
padding: 14px;
text-align: center;
}
.stat-label { font-size: 11px; color: var(–text2); margin-bottom: 4px; }
.stat-value { font-size: 22px; font-weight: 700; color: var(–accent); }

/* Symbols grid */
.sym { display: grid; grid-template-columns: repeat(auto-fill, minmax(150px,1fr)); gap: 8px; }
.sy {
background: var(–bg3);
border-radius: 8px;
padding: 10px 12px;
display: flex; align-items: center; gap: 10px;
}
.si { font-size: 18px; width: 32px; text-align: center; flex-shrink: 0; color: var(–accent); }
.sn2 { font-size: 12px; font-weight: 700; color: var(–text3); }
.sd { font-size: 10px; color: var(–text2); }

/* Number table highlight */
.num-highlight { color: var(–accent3); font-weight: 700; }

/* Mobile */
@media (max-width: 640px) {
.sidebar { display: none; }
.sidebar.open { display: block; position: fixed; top: 69px; left: 0; bottom: 0; z-index: 200; width: 240px; }
.g2, .g3, .g4 { grid-template-columns: 1fr; }
.stats { grid-template-columns: repeat(2,1fr); }
.menu-btn { display: flex !important; }
.main { padding: 16px; }
}
.menu-btn {
display: none;
align-items: center; justify-content: center;
width: 36px; height: 36px;
background: var(–bg3); border: 1px solid var(–border);
border-radius: 8px; cursor: pointer; font-size: 18px;
margin-right: 4px;
}
.overlay {
display: none;
position: fixed; inset: 0;
background: rgba(0,0,0,0.6);
z-index: 150;
}
.overlay.open { display: block; }
</style>

</head>
<body>

<header class="app-header">
  <div class="menu-btn" id="menuBtn" onclick="toggleMenu()">☰</div>
  <div class="logo">⚡</div>
  <div>
    <h1>第一種電気工事士</h1>
    <p>学科試験 完全攻略テキスト</p>
  </div>
  <div class="progress-bar"><div class="progress-fill" id="progressFill"></div></div>
</header>

<div class="overlay" id="overlay" onclick="closeMenu()"></div>

<div class="layout">
  <nav class="sidebar" id="sidebar">
    <div class="sidebar-section">メインメニュー</div>
    <div class="nav-item active" onclick="show('s0',this)"><span class="icon">📋</span>試験概要・攻略法</div>
    <div class="sidebar-section">電気理論</div>
    <div class="nav-item" onclick="show('s1',this)"><span class="icon">⚡</span>電気理論①基礎</div>
    <div class="nav-item" onclick="show('s2',this)"><span class="icon">〜</span>電気理論②交流・三相</div>
    <div class="nav-item" onclick="show('s3',this)"><span class="icon">🔢</span>電気計算の応用</div>
    <div class="sidebar-section">機器・設備</div>
    <div class="nav-item" onclick="show('s4',this)"><span class="icon">🔌</span>電気機器・測定器</div>
    <div class="nav-item" onclick="show('s5',this)"><span class="icon">🏭</span>電力系統・高圧受電</div>
    <div class="sidebar-section">施工・図記号</div>
    <div class="nav-item" onclick="show('s6',this)"><span class="icon">🔧</span>電気工事の施工方法</div>
    <div class="nav-item" onclick="show('s7',this)"><span class="icon">📐</span>配線図記号</div>
    <div class="sidebar-section">検査・法規</div>
    <div class="nav-item" onclick="show('s8',this)"><span class="icon">🔍</span>検査・測定</div>
    <div class="nav-item" onclick="show('s9',this)"><span class="icon">📜</span>法規①工事士法</div>
    <div class="nav-item" onclick="show('s10',this)"><span class="icon">🔒</span>法規②接地・安全</div>
    <div class="sidebar-section">その他</div>
    <div class="nav-item" onclick="show('s11',this)"><span class="icon">💡</span>照明・熱・電池</div>
    <div class="nav-item" onclick="show('s12',this)"><span class="icon">📊</span>重要数値まとめ</div>
  </nav>

  <main class="main">

```
<!-- 試験概要 -->
<section class="section active" id="s0">
  <div class="section-header">
    <h2>📋 試験概要と攻略法</h2>
    <p>まずここから確認しよう</p>
  </div>
  <div class="stats">
    <div class="stat"><div class="stat-label">問題数</div><div class="stat-value">50問</div></div>
    <div class="stat"><div class="stat-label">試験時間</div><div class="stat-value">160分</div></div>
    <div class="stat"><div class="stat-label">合格ライン</div><div class="stat-value" style="color:var(--accent2)">60点</div></div>
    <div class="stat"><div class="stat-label">出題形式</div><div class="stat-value" style="font-size:16px;color:var(--accent3)">四択式</div></div>
  </div>
  <div class="card">
    <div class="card-title"><span class="tag tag-blue">出題科目と目安</span></div>
    <div class="tw"><table>
      <tr><th>科目</th><th>問題数目安</th><th>重要度</th></tr>
      <tr><td>電気に関する基礎理論</td><td>約10問</td><td style="color:var(--accent3)">★★★</td></tr>
      <tr><td>配電理論・配線設計</td><td>約10問</td><td style="color:var(--accent3)">★★★</td></tr>
      <tr><td>電気機器・蓄電池・配線器具</td><td>約10問</td><td style="color:var(--accent3)">★★★</td></tr>
      <tr><td>電気工事の施工方法</td><td>約5問</td><td style="color:var(--text2)">★★☆</td></tr>
      <tr><td>自家用電気工作物の検査</td><td>約5問</td><td style="color:var(--text2)">★★☆</td></tr>
      <tr><td>電気工事の種類・内容</td><td>約3問</td><td style="color:var(--text2)">★☆☆</td></tr>
      <tr><td>法令</td><td>約7問</td><td style="color:var(--accent3)">★★★</td></tr>
    </table></div>
  </div>
  <div class="card">
    <div class="card-title"><span class="tag tag-green">攻略のポイント</span></div>
    <ul class="pl">
      <li>まずオームの法則を完全マスター。計算問題の土台になる</li>
      <li>法規・接地工事の数値は丸暗記（A種10Ω／D種100Ω等）</li>
      <li>配線図記号は毎年出題。全記号を書いて覚える</li>
      <li>過去5年分の問題を繰り返すだけで合格ラインに届く</li>
      <li>計算が苦手なら法規・施工・記号で満点を狙う戦略も有効</li>
      <li>1問あたり約3分。時間配分を意識した練習をしておく</li>
    </ul>
    <div class="tip">50問中30問正解でOK。全問解けなくても合格できる。得意分野を確実に得点することが鍵！</div>
  </div>
</section>

<!-- 電気理論① -->
<section class="section" id="s1">
  <div class="section-header"><h2>⚡ 電気理論①｜基礎</h2><p>オームの法則から始めよう</p></div>
  <div class="card">
    <div class="card-title"><span class="tag tag-blue">必須</span>オームの法則</div>
    <div class="formula">V = I × R　（電圧 = 電流 × 抵抗）</div>
    <div class="g2" style="margin-top:10px">
      <div class="term"><div class="term-name">電流を求める</div><div class="term-desc" style="font-size:14px;color:var(--accent);font-weight:700">I = V ÷ R</div></div>
      <div class="term"><div class="term-name">抵抗を求める</div><div class="term-desc" style="font-size:14px;color:var(--accent);font-weight:700">R = V ÷ I</div></div>
    </div>
    <div class="tip">▲三角形で覚える：V を上、I と R を下に書く。求めたい文字を指で隠すと式がわかる！</div>
  </div>
  <div class="card">
    <div class="card-title"><span class="tag tag-blue">必須</span>電力・電力量・熱量</div>
    <div class="formula">P = V×I = I²R = V²/R　（単位：W ワット）</div>
    <div class="formula">W = P × t　（電力量、単位：Wh ワット時）</div>
    <div class="formula">Q = 0.24 × P × t　（熱量、単位：cal カロリー）</div>
    <ul class="pl" style="margin-top:10px">
      <li>1kWh = 1000Wh。電気料金の単位</li>
      <li>1cal = 4.186J（ジュール）。約4.2Jで計算してOK</li>
      <li>1kWh = 860kcal（電力量→熱量換算）</li>
    </ul>
  </div>
  <div class="card">
    <div class="card-title"><span class="tag tag-orange">重要</span>直列・並列回路</div>
    <div class="g2">
      <div>
        <div class="term-name" style="margin-bottom:8px;color:var(--accent)">直列回路</div>
        <ul class="pl">
          <li>合成抵抗 R = R₁+R₂（足し算）</li>
          <li>電流はどこも同じ（I共通）</li>
          <li>電圧は抵抗に比例して分配</li>
        </ul>
      </div>
      <div>
        <div class="term-name" style="margin-bottom:8px;color:var(--accent2)">並列回路</div>
        <ul class="pl">
          <li>1/R = 1/R₁+1/R₂（逆数の和）</li>
          <li>電圧はどこも同じ（V共通）</li>
          <li>2つなら R=R₁×R₂÷(R₁+R₂)</li>
        </ul>
      </div>
    </div>
    <div class="tip">2つの抵抗が並列のとき：合成抵抗 = 積 ÷ 和（「積和の公式」）</div>
  </div>
  <div class="card">
    <div class="card-title"><span class="tag tag-green">基礎</span>電線の抵抗</div>
    <div class="formula">R = ρ × L / A　（抵抗率 × 長さ ÷ 断面積）</div>
    <ul class="pl">
      <li>長さが2倍 → 抵抗2倍　断面積が2倍 → 抵抗½</li>
      <li>銅の抵抗率：約1.72×10⁻⁸Ω·m</li>
      <li>温度が上がると金属の抵抗は増加する</li>
    </ul>
  </div>
</section>

<!-- 電気理論② -->
<section class="section" id="s2">
  <div class="section-header"><h2>〜 電気理論②｜交流・三相</h2><p>交流・三相の基礎をマスター</p></div>
  <div class="card">
    <div class="card-title"><span class="tag tag-blue">重要</span>交流の基礎用語</div>
    <div class="g2">
      <div class="term"><div class="term-name">周波数（Hz：ヘルツ）</div><div class="term-desc">1秒間の交流サイクル数。東日本50Hz・西日本60Hz</div></div>
      <div class="term"><div class="term-name">実効値</div><div class="term-desc">交流を直流換算した値。家庭用100Vはこれ。最大値×(1/√2)≒0.707倍</div></div>
      <div class="term"><div class="term-name">最大値（波高値）</div><div class="term-desc">実効値×√2（≒1.414倍）。100Vの場合、最大約141V</div></div>
      <div class="term"><div class="term-name">力率（cosθ）</div><div class="term-desc">有効電力÷皮相電力。1に近いほど効率が良い状態</div></div>
    </div>
  </div>
  <div class="card">
    <div class="card-title"><span class="tag tag-blue">重要</span>インピーダンスとリアクタンス</div>
    <div class="formula">Z = √(R² + X²)　インピーダンス（Ω）</div>
    <div class="formula">XL = 2πfL　コイルのリアクタンス（Ω）</div>
    <div class="formula">XC = 1/(2πfC)　コンデンサのリアクタンス（Ω）</div>
    <div class="g2" style="margin-top:10px">
      <div class="term"><div class="term-name">コイル（L）の性質</div><div class="term-desc">電流が電圧より90°遅れる。周波数が高いほどXL大</div></div>
      <div class="term"><div class="term-name">コンデンサ（C）の性質</div><div class="term-desc">電流が電圧より90°進む。周波数が高いほどXC小</div></div>
    </div>
  </div>
  <div class="card">
    <div class="card-title"><span class="tag tag-blue">重要</span>電力の3種類</div>
    <div class="formula">有効電力 P = V×I×cosθ　（W ワット）</div>
    <div class="formula">無効電力 Q = V×I×sinθ　（var バール）</div>
    <div class="formula">皮相電力 S = V×I　（VA ボルトアンペア）</div>
    <ul class="pl" style="margin-top:10px">
      <li>コンデンサを並列接続することで力率を改善できる</li>
      <li>低力率では同じ有効電力でも電流が多く流れ電線が熱くなる</li>
    </ul>
  </div>
  <div class="card">
    <div class="card-title"><span class="tag tag-orange">重要</span>三相交流・Y△結線</div>
    <div class="tw"><table>
      <tr><th></th><th>スター（Y）結線</th><th>デルタ（△）結線</th></tr>
      <tr><td>線間電圧と相電圧</td><td>線間電圧 = 相電圧×√3</td><td>線間電圧 = 相電圧（同じ）</td></tr>
      <tr><td>線電流と相電流</td><td>線電流 = 相電流（同じ）</td><td>線電流 = 相電流×√3</td></tr>
      <tr><td>中性線</td><td>あり（4線式可能）</td><td>なし</td></tr>
    </table></div>
    <div class="formula">三相電力 P = √3 × V × I × cosθ</div>
    <div class="tip">√3 ≈ 1.732 を使う。6600VをY結線に換算→6600÷√3≈3810V</div>
  </div>
</section>

<!-- 電気計算 -->
<section class="section" id="s3">
  <div class="section-header"><h2>🔢 電気計算の応用</h2><p>頻出の計算問題をまとめて攻略</p></div>
  <div class="card">
    <div class="card-title"><span class="tag tag-blue">頻出</span>電圧降下の計算</div>
    <div class="formula">単相2線式：e = 2 × I × R（往復分）</div>
    <div class="formula">三相3線式：e = √3 × I × R</div>
    <ul class="pl">
      <li>電線を太くする・短くすれば電圧降下を減らせる</li>
      <li>低圧配線の電圧降下は最遠端まで原則5%以内（内線規程）</li>
    </ul>
    <div class="warn">例題：単相100V回路、電線抵抗0.1Ω、電流10Aのとき<br>e = 2×10×0.1 = 2V　→ 受電端電圧 = 100−2 = <strong>98V</strong></div>
  </div>
  <div class="card">
    <div class="card-title"><span class="tag tag-blue">頻出</span>変圧器の計算</div>
    <div class="formula">V₁/V₂ = N₁/N₂ = I₂/I₁</div>
    <ul class="pl">
      <li>電圧比 = 巻数比。電流比は逆（電圧が上がれば電流は下がる）</li>
      <li>効率 η = 出力/(出力+損失) × 100%</li>
    </ul>
    <div class="warn">例題：6600V→200V変圧器の巻数比 = 6600:200 = <strong>33:1</strong></div>
  </div>
  <div class="card">
    <div class="card-title"><span class="tag tag-orange">重要</span>電動機の回転速度</div>
    <div class="formula">同期速度 Ns = 120 × f / P　（rpm）</div>
    <ul class="pl">
      <li>f：周波数（Hz）、P：極数</li>
      <li>滑り s = (同期速度−実速度)÷同期速度。通常2〜5%</li>
      <li>三相誘導電動機の逆転：3線のうち2線を入れ替える</li>
    </ul>
  </div>
  <div class="card">
    <div class="card-title"><span class="tag tag-orange">重要</span>力率改善のコンデンサ容量</div>
    <div class="formula">Q_C = P × (tanθ₁ − tanθ₂)　（kvar）</div>
    <ul class="pl">
      <li>P：有効電力（kW）、θ₁：改善前の角度、θ₂：改善後の角度</li>
      <li>コンデンサは並列接続で力率改善効果あり</li>
    </ul>
  </div>
</section>

<!-- 電気機器 -->
<section class="section" id="s4">
  <div class="section-header"><h2>🔌 電気機器・測定器</h2><p>機器の名称と特徴を覚えよう</p></div>
  <div class="card">
    <div class="card-title"><span class="tag tag-blue">重要</span>変圧器の種類</div>
    <div class="tw"><table>
      <tr><th>種類</th><th>特徴・用途</th></tr>
      <tr><td>油入変圧器</td><td>絶縁・冷却に絶縁油。大容量。定期的な油の点検が必要</td></tr>
      <tr><td>モールド変圧器</td><td>エポキシ樹脂でモールド。難燃性。屋内・地下設備向き</td></tr>
      <tr><td>計器用変圧器（VT）</td><td>高電圧→110Vに変換して計器・継電器へ</td></tr>
      <tr><td>変流器（CT）</td><td>大電流→5Aに変換して計器・継電器へ</td></tr>
    </table></div>
    <div class="danger">⚠️ CTの2次側を開放したまま1次側に電流を流すと危険な高電圧が発生！測定しないときは必ず短絡（ショート）しておく。</div>
  </div>
  <div class="card">
    <div class="card-title"><span class="tag tag-blue">重要</span>遮断器・開閉器の種類</div>
    <div class="tw"><table>
      <tr><th>名称</th><th>略称</th><th>特徴</th></tr>
      <tr><td>配線用遮断器</td><td>MCCB</td><td>過電流・短絡から回路を保護。最も一般的</td></tr>
      <tr><td>漏電遮断器</td><td>ELCB</td><td>漏電検出して遮断。感電防止に必須</td></tr>
      <tr><td>真空遮断器</td><td>VCB</td><td>高圧用。真空中でアーク消弧。保守が容易</td></tr>
      <tr><td>ガス遮断器</td><td>GCB</td><td>SF₆ガスで消弧。超高圧用</td></tr>
      <tr><td>断路器</td><td>DS</td><td>負荷電流を切れない。停電時専用</td></tr>
      <tr><td>電磁接触器</td><td>MC</td><td>電磁力でON/OFF。自動制御に使用</td></tr>
      <tr><td>高圧負荷開閉器</td><td>LBS</td><td>高圧の開閉。短絡遮断はできない</td></tr>
    </table></div>
  </div>
  <div class="card">
    <div class="card-title"><span class="tag tag-orange">重要</span>電動機（モーター）の種類</div>
    <div class="tw"><table>
      <tr><th>種類</th><th>特徴</th><th>用途</th></tr>
      <tr><td>三相誘導電動機</td><td>最も普及。堅牢・安価。スリップあり</td><td>工場・ポンプ・送風機</td></tr>
      <tr><td>同期電動機</td><td>回転数が周波数に同期</td><td>精密機器・大型設備</td></tr>
      <tr><td>直流電動機</td><td>速度制御容易。ブラシが必要</td><td>クレーン・圧延機</td></tr>
    </table></div>
  </div>
  <div class="card">
    <div class="card-title"><span class="tag tag-green">覚える</span>測定器一覧</div>
    <div class="tw"><table>
      <tr><th>測定器</th><th>接続</th><th>注意点</th></tr>
      <tr><td>電圧計</td><td>並列</td><td>内部抵抗は大きく</td></tr>
      <tr><td>電流計</td><td>直列</td><td>内部抵抗は小さく</td></tr>
      <tr><td>絶縁抵抗計（メガー）</td><td>対地・相互間</td><td>停電して測定。500V/1000Vメガー使用</td></tr>
      <tr><td>接地抵抗計</td><td>補助接地極2本使用</td><td>A〜D種の確認に使用</td></tr>
      <tr><td>クランプメーター</td><td>電線を挟む</td><td>活線測定可能。非接触</td></tr>
      <tr><td>検電器</td><td>充電部に接触</td><td>停電確認作業に必須</td></tr>
    </table></div>
  </div>
</section>

<!-- 電力系統 -->
<section class="section" id="s5">
  <div class="section-header"><h2>🏭 電力系統・高圧受電設備</h2><p>高圧受電の流れと機器を理解しよう</p></div>
  <div class="card">
    <div class="card-title"><span class="tag tag-blue">重要</span>電圧の区分</div>
    <div class="tw"><table>
      <tr><th>区分</th><th>交流</th><th>直流</th></tr>
      <tr><td style="color:var(--accent2)">低圧</td><td>600V以下</td><td>750V以下</td></tr>
      <tr><td style="color:var(--accent3)">高圧</td><td>600V超〜7,000V以下</td><td>750V超〜7,000V以下</td></tr>
      <tr><td style="color:var(--red)">特別高圧</td><td colspan="2">7,000Vを超えるもの</td></tr>
    </table></div>
    <div class="tip">一般の高圧配電は6,600V。家庭への供給は100V/200V。</div>
  </div>
  <div class="card">
    <div class="card-title"><span class="tag tag-blue">重要</span>高圧受電設備の主要機器</div>
    <div class="warn" style="margin-bottom:12px">機器の順番：PAS → LA → MOF → DS → VCB → 主母線 → 変圧器</div>
    <div class="tw"><table>
      <tr><th>機器名</th><th>略称</th><th>役割</th></tr>
      <tr><td>高圧気中負荷開閉器</td><td style="color:var(--accent)">PAS</td><td>引込口の開閉。SOG付きは地絡時自動遮断</td></tr>
      <tr><td>避雷器</td><td style="color:var(--accent)">LA</td><td>雷サージから機器を保護</td></tr>
      <tr><td>計器用変成器</td><td style="color:var(--accent)">MOF</td><td>VT+CTが一体。電力量計測用</td></tr>
      <tr><td>断路器</td><td style="color:var(--accent)">DS</td><td>停電時に主回路を開放</td></tr>
      <tr><td>真空遮断器</td><td style="color:var(--accent)">VCB</td><td>主遮断装置。事故電流を遮断</td></tr>
      <tr><td>過電流継電器</td><td style="color:var(--accent)">OCR</td><td>過電流を検出しVCBをトリップ</td></tr>
      <tr><td>地絡方向継電器</td><td style="color:var(--accent)">DGR</td><td>構内地絡のみを選択的に検出</td></tr>
      <tr><td>電力用コンデンサ</td><td style="color:var(--accent)">SC</td><td>力率改善。直列リアクトル（SR）と併用</td></tr>
    </table></div>
  </div>
  <div class="card">
    <div class="card-title"><span class="tag tag-orange">基礎</span>主なケーブルの種類</div>
    <div class="tw"><table>
      <tr><th>記号</th><th>名称（略）</th><th>用途</th></tr>
      <tr><td style="color:var(--accent3)">CV</td><td>架橋ポリエチレン絶縁ビニルシースケーブル</td><td>最も一般的な電力ケーブル</td></tr>
      <tr><td style="color:var(--accent3)">VVF</td><td>600Vビニルケーブル 平型</td><td>家庭の屋内配線の主流</td></tr>
      <tr><td style="color:var(--accent3)">IV</td><td>600Vビニル絶縁電線</td><td>管内配線の基本</td></tr>
      <tr><td style="color:var(--accent3)">OC</td><td>屋外用架橋ポリエチレン絶縁電線</td><td>高圧架空電線</td></tr>
      <tr><td style="color:var(--accent3)">MI</td><td>無機絶縁ケーブル</td><td>耐火・耐熱が必要な場所</td></tr>
    </table></div>
  </div>
</section>

<!-- 施工方法 -->
<section class="section" id="s6">
  <div class="section-header"><h2>🔧 電気工事の施工方法</h2><p>施工の種類・数値・禁止事項を覚えよう</p></div>
  <div class="card">
    <div class="card-title"><span class="tag tag-blue">重要</span>配線工事の種類</div>
    <div class="tw"><table>
      <tr><th>工事の種類</th><th>特徴・使用場所</th></tr>
      <tr><td>金属管配線（厚鋼・薄鋼）</td><td>機械的保護が必要な場所。支持間隔2m以下</td></tr>
      <tr><td>合成樹脂管配線（PF管）</td><td>軽量・耐食性・自消性あり。支持間隔1.5m以下</td></tr>
      <tr><td>合成樹脂管配線（CD管）</td><td>オレンジ色。自消性なし。コンクリート埋設専用</td></tr>
      <tr><td>金属ダクト配線</td><td>多数の電線をまとめて収める。工場・ビルの幹線</td></tr>
      <tr><td>バスダクト配線</td><td>大電流用の裸導体ダクト。変電室〜分電盤間</td></tr>
      <tr><td>ケーブルラック配線</td><td>梯子状の支持物にケーブルを乗せる</td></tr>
    </table></div>
  </div>
  <div class="card">
    <div class="card-title"><span class="tag tag-orange">数値</span>施工の重要数値</div>
    <div class="tw"><table>
      <tr><th>項目</th><th>数値</th></tr>
      <tr><td>金属管の支持間隔</td><td class="num-highlight">2m以下ごと</td></tr>
      <tr><td>合成樹脂管の支持間隔</td><td class="num-highlight">1.5m以下ごと</td></tr>
      <tr><td>埋設ケーブルの深さ（重量物圧迫あり）</td><td class="num-highlight">1.2m以上</td></tr>
      <tr><td>埋設ケーブルの深さ（管路式・通行なし）</td><td class="num-highlight">0.6m以上</td></tr>
      <tr><td>電線の接続後の引張強度</td><td class="num-highlight">元の80%以上保持</td></tr>
      <tr><td>低圧幹線の電圧降下（推奨値）</td><td class="num-highlight">幹線+分岐で2〜5%以内</td></tr>
    </table></div>
  </div>
  <div class="card">
    <div class="card-title"><span class="tag tag-red">禁止事項</span>施工の注意点</div>
    <ul class="pl">
      <li>電線の接続はテープ巻きだけでは不可。差込コネクタ・リングスリーブを使用</li>
      <li>CD管は自消性がないためコンクリート埋設以外には使用不可</li>
      <li>金属管内での電線の接続は禁止（ボックス内で接続すること）</li>
      <li>断路器（DS）は負荷電流が流れている状態での開閉禁止</li>
      <li>CTの2次側を開放したまま1次側に電流を流してはならない</li>
    </ul>
  </div>
</section>

<!-- 配線図記号 -->
<section class="section" id="s7">
  <div class="section-header"><h2>📐 配線図記号</h2><p>毎年必ず出題！全記号を覚えよう</p></div>
  <div class="card">
    <div class="card-title"><span class="tag tag-blue">スイッチ類</span></div>
    <div class="sym">
      <div class="sy"><div class="si">●</div><div><div class="sn2">単極スイッチ</div><div class="sd">最も一般的な片切</div></div></div>
      <div class="sy"><div class="si">●₂</div><div><div class="sn2">2極スイッチ</div><div class="sd">2回路同時開閉</div></div></div>
      <div class="sy"><div class="si">3●</div><div><div class="sn2">3路スイッチ</div><div class="sd">2か所から点滅。階段など</div></div></div>
      <div class="sy"><div class="si">4●</div><div><div class="sn2">4路スイッチ</div><div class="sd">3か所以上から点滅</div></div></div>
      <div class="sy"><div class="si">●T</div><div><div class="sn2">タイムスイッチ</div><div class="sd">時刻で自動点滅</div></div></div>
      <div class="sy"><div class="si">●A</div><div><div class="sn2">自動点滅器</div><div class="sd">明暗で自動ON/OFF</div></div></div>
      <div class="sy"><div class="si">●L</div><div><div class="sn2">ランプ付スイッチ</div><div class="sd">位置確認用ランプ内蔵</div></div></div>
      <div class="sy"><div class="si">●P</div><div><div class="sn2">プルスイッチ</div><div class="sd">引き紐で点滅</div></div></div>
    </div>
    <div class="tip">3路は2か所、4路は3か所以上から点滅できる。3路を2個＋4路を必要数組み合わせる。</div>
  </div>
  <div class="card">
    <div class="card-title"><span class="tag tag-orange">コンセント類</span></div>
    <div class="sym">
      <div class="sy"><div class="si">⊕</div><div><div class="sn2">一般コンセント</div><div class="sd">2P 15A 125V</div></div></div>
      <div class="sy"><div class="si">⊕₂₀</div><div><div class="sn2">20Aコンセント</div><div class="sd">IH・エアコン等</div></div></div>
      <div class="sy"><div class="si">⊕ET</div><div><div class="sn2">接地端子付き</div><div class="sd">漏電対策・E付き</div></div></div>
      <div class="sy"><div class="si">⊕EL</div><div><div class="sn2">漏電保護用</div><div class="sd">漏電遮断器内蔵</div></div></div>
      <div class="sy"><div class="si">⊕WP</div><div><div class="sn2">防雨型</div><div class="sd">屋外・水のかかる場所</div></div></div>
      <div class="sy"><div class="si">⊕LK</div><div><div class="sn2">引掛形</div><div class="sd">ロック機構付き</div></div></div>
    </div>
  </div>
  <div class="card">
    <div class="card-title"><span class="tag tag-green">照明・機器</span></div>
    <div class="sym">
      <div class="sy"><div class="si">⊙</div><div><div class="sn2">引掛シーリング</div><div class="sd">天井付け照明器具用</div></div></div>
      <div class="sy"><div class="si">◎</div><div><div class="sn2">天井直付照明</div><div class="sd">シーリングライト</div></div></div>
      <div class="sy"><div class="si">□</div><div><div class="sn2">分電盤</div><div class="sd">ブレーカーが入った箱</div></div></div>
      <div class="sy"><div class="si">♦</div><div><div class="sn2">ジョイントボックス</div><div class="sd">電線の接続・分岐用</div></div></div>
      <div class="sy"><div class="si">□T</div><div><div class="sn2">変圧器</div><div class="sd">電圧変換機器</div></div></div>
      <div class="sy"><div class="si">E⊙</div><div><div class="sn2">埋込照明</div><div class="sd">ダウンライト等</div></div></div>
    </div>
  </div>
  <div class="card">
    <div class="card-title"><span class="tag tag-gray">線の種類</span></div>
    <div class="tw"><table>
      <tr><th>表記</th><th>意味</th></tr>
      <tr><td>実線（太）</td><td>電源線・幹線</td></tr>
      <tr><td>実線（細）</td><td>一般配線</td></tr>
      <tr><td>破線</td><td>隠蔽配線（天井・壁内）</td></tr>
      <tr><td>一点鎖線</td><td>地中配線</td></tr>
    </table></div>
  </div>
</section>

<!-- 検査・測定 -->
<section class="section" id="s8">
  <div class="section-header"><h2>🔍 検査・測定</h2><p>竣工検査・定期点検の手順と基準値</p></div>
  <div class="card">
    <div class="card-title"><span class="tag tag-blue">重要</span>絶縁抵抗の基準値</div>
    <div class="tw"><table>
      <tr><th>回路の種類</th><th>最低絶縁抵抗値</th></tr>
      <tr><td>300V以下の対地電圧</td><td class="num-highlight">0.1MΩ以上</td></tr>
      <tr><td>300V超600V以下の回路</td><td class="num-highlight">0.2MΩ以上</td></tr>
      <tr><td>高圧回路（6,600V）</td><td class="num-highlight">6MΩ以上（目安）</td></tr>
    </table></div>
    <div class="tip">低圧回路→500Vメガー、高圧回路→1000V/2000Vメガーを使用</div>
  </div>
  <div class="card">
    <div class="card-title"><span class="tag tag-blue">重要</span>絶縁耐力試験</div>
    <div class="tw"><table>
      <tr><th>電路の種類</th><th>試験電圧</th><th>印加時間</th></tr>
      <tr><td>最大使用電圧7,000V以下</td><td class="num-highlight">×1.5倍（最低500V）</td><td class="num-highlight">10分間</td></tr>
      <tr><td>7,000V超〜60,000V以下</td><td class="num-highlight">×1.25倍</td><td class="num-highlight">10分間</td></tr>
      <tr><td>60,000V超</td><td class="num-highlight">×1.1倍</td><td class="num-highlight">10分間</td></tr>
    </table></div>
  </div>
  <div class="card">
    <div class="card-title"><span class="tag tag-orange">点検</span>定期点検の種類</div>
    <div class="tw"><table>
      <tr><th>種類</th><th>停電</th><th>主な内容</th></tr>
      <tr><td style="color:var(--red)">年次点検</td><td>要（停電）</td><td>絶縁抵抗・絶縁耐力・接地抵抗・継電器試験</td></tr>
      <tr><td style="color:var(--accent2)">月次点検</td><td>不要（活線）</td><td>外観・電流・電圧・温度・異音・臭気の確認</td></tr>
      <tr><td style="color:var(--accent3)">竣工検査</td><td>要</td><td>外観→接地→絶縁→耐力→継電器→負荷試験の順</td></tr>
    </table></div>
  </div>
  <div class="card">
    <div class="card-title"><span class="tag tag-green">保護継電器</span></div>
    <div class="tw"><table>
      <tr><th>名称</th><th>略称</th><th>動作条件</th></tr>
      <tr><td>過電流継電器</td><td style="color:var(--accent)">OCR</td><td>設定値以上の電流が流れたとき</td></tr>
      <tr><td>地絡方向継電器</td><td style="color:var(--accent)">DGR</td><td>地絡の方向を検出。構内地絡のみに動作</td></tr>
      <tr><td>不足電圧継電器</td><td style="color:var(--accent)">UVR</td><td>電圧が設定値以下に下がったとき</td></tr>
      <tr><td>過電圧継電器</td><td style="color:var(--accent)">OVR</td><td>電圧が設定値以上になったとき</td></tr>
    </table></div>
  </div>
</section>

<!-- 法規① -->
<section class="section" id="s9">
  <div class="section-header"><h2>📜 法規①｜電気工事士法・電気事業法</h2><p>法規は暗記勝負！確実に点を取ろう</p></div>
  <div class="card">
    <div class="card-title"><span class="tag tag-red">法規</span>電気工事士の種類と作業範囲</div>
    <div class="tw"><table>
      <tr><th>資格</th><th>作業できる範囲</th></tr>
      <tr><td style="color:var(--accent3)">第一種電気工事士</td><td>自家用（500kW未満）＋一般用のすべての工事</td></tr>
      <tr><td style="color:var(--accent2)">第二種電気工事士</td><td>一般用電気工作物の工事のみ</td></tr>
      <tr><td>認定電気工事従事者</td><td>自家用のうち600V以下の低圧部分</td></tr>
      <tr><td>特種電気工事資格者（ネオン）</td><td>ネオン工事</td></tr>
      <tr><td>特種電気工事資格者（非常用発電）</td><td>非常用予備発電装置の工事</td></tr>
    </table></div>
    <div class="tip">第一種電気工事士は免状取得後、<strong>5年ごと</strong>に定期講習の受講義務がある（免状自体の更新は不要）</div>
  </div>
  <div class="card">
    <div class="card-title"><span class="tag tag-red">法規</span>電気工作物の区分</div>
    <div class="tw"><table>
      <tr><th>区分</th><th>対象</th><th>主な義務</th></tr>
      <tr><td>一般用電気工作物</td><td>低圧受電の家庭・小規模工場等</td><td>電気工事士が工事。電力会社が調査</td></tr>
      <tr><td>自家用（小規模）</td><td>高圧受電で最大電力500kW未満</td><td>電気主任技術者（外部委託可）・保安規程届出</td></tr>
      <tr><td>自家用（大規模）</td><td>最大電力500kW以上または特別高圧受電</td><td>電気主任技術者の選任義務（外部委託不可）</td></tr>
    </table></div>
  </div>
  <div class="card">
    <div class="card-title"><span class="tag tag-red">法規</span>電気主任技術者の種類</div>
    <div class="tw"><table>
      <tr><th>種別</th><th>保安監督できる電圧</th></tr>
      <tr><td>第一種電気主任技術者</td><td>すべての電気工作物</td></tr>
      <tr><td>第二種電気主任技術者</td><td>170,000V未満</td></tr>
      <tr><td>第三種電気主任技術者</td><td>50,000V未満</td></tr>
    </table></div>
  </div>
  <div class="card">
    <div class="card-title"><span class="tag tag-red">法規</span>届出・報告義務</div>
    <ul class="pl">
      <li>保安規程の届出：自家用電気工作物の設置・変更前に届出</li>
      <li>主任技術者の選任届：選任・解任の際に遅滞なく届出</li>
      <li>工事計画の届出：特定の工事は着工30日前までに届出</li>
      <li>事故報告：感電死傷・電気火災・波及事故は速やかに報告</li>
    </ul>
  </div>
</section>

<!-- 法規② -->
<section class="section" id="s10">
  <div class="section-header"><h2>🔒 法規②｜接地工事・安全基準</h2><p>接地の種類と数値は絶対暗記！</p></div>
  <div class="card">
    <div class="card-title"><span class="tag tag-blue">最重要</span>接地工事の種類（必ず覚える！）</div>
    <div class="tw"><table>
      <tr><th>種別</th><th>接地抵抗</th><th>最小電線径</th><th>主な使用箇所</th></tr>
      <tr><td style="color:var(--red)">A種接地</td><td class="num-highlight">10Ω以下</td><td>2.6mm以上</td><td>高圧・特別高圧機器の外箱・フレーム</td></tr>
      <tr><td style="color:var(--accent3)">B種接地</td><td class="num-highlight">変圧器容量等による</td><td>4mm²以上</td><td>高低圧結合変圧器の低圧側中性点</td></tr>
      <tr><td style="color:var(--accent2)">C種接地</td><td class="num-highlight">10Ω以下</td><td>1.6mm以上</td><td>300Vを超える低圧機器の外箱</td></tr>
      <tr><td style="color:var(--accent)">D種接地</td><td class="num-highlight">100Ω以下</td><td>1.6mm以上</td><td>300V以下の低圧機器の外箱</td></tr>
    </table></div>
    <div class="tip">暗記法：<strong>A種・C種は10Ω以下（厳しい）、D種は100Ω以下（緩い）</strong></div>
    <div class="warn">特例：漏電遮断器（0.1秒以内）設置でD種は500Ω以下に緩和可能</div>
  </div>
  <div class="card">
    <div class="card-title"><span class="tag tag-blue">重要</span>B種接地抵抗の計算</div>
    <div class="formula">R_B = 150 / I_g（Ω）</div>
    <ul class="pl">
      <li>I_g：高圧側の1線地絡電流（A）</li>
      <li>地絡継電器がある場合：R_B = 600 / I_g</li>
    </ul>
  </div>
  <div class="card">
    <div class="card-title"><span class="tag tag-orange">安全</span>停電作業の手順と安全基準</div>
    <ul class="pl">
      <li>停電確認（検電器で無電圧確認）→ 放電 → 短絡接地 の順で行う</li>
      <li>作業中は「作業中通電禁止」の表示と施錠が必須</li>
      <li>高所作業：6.75m以上はフルハーネス型墜落制止用器具を着用</li>
      <li>絶縁用保護具（手袋・靴・ヘルメット）は使用前に耐圧試験済品を確認</li>
    </ul>
  </div>
  <div class="card">
    <div class="card-title"><span class="tag tag-orange">施工基準</span>電気設備技術基準の重要数値</div>
    <div class="tw"><table>
      <tr><th>項目</th><th>基準値</th></tr>
      <tr><td>架空電線の道路横断最低高さ</td><td class="num-highlight">6m以上</td></tr>
      <tr><td>架空電線路（道路以外）の最低高さ</td><td class="num-highlight">5m以上</td></tr>
      <tr><td>供給電圧の許容変動（低圧）</td><td class="num-highlight">101±6V または 202±20V</td></tr>
      <tr><td>漏電遮断器の感度電流（人体保護）</td><td class="num-highlight">30mA以下・0.1秒以内</td></tr>
    </table></div>
  </div>
</section>

<!-- 照明・熱・電池 -->
<section class="section" id="s11">
  <div class="section-header"><h2>💡 照明・熱の計算・蓄電池</h2><p>照明・熱・電池の基礎知識</p></div>
  <div class="card">
    <div class="card-title"><span class="tag tag-blue">重要</span>照明の基礎用語</div>
    <div class="g2">
      <div class="term"><div class="term-name">光束（lm：ルーメン）</div><div class="term-desc">光源から出る光の全量</div></div>
      <div class="term"><div class="term-name">照度（lx：ルクス）</div><div class="term-desc">ある面の明るさ。E = lm/m²</div></div>
      <div class="term"><div class="term-name">光度（cd：カンデラ）</div><div class="term-desc">特定方向への光の強さ</div></div>
      <div class="term"><div class="term-name">演色性（Ra）</div><div class="term-desc">自然光との色再現性。Ra100が最高</div></div>
    </div>
    <div class="formula">照度 E = F×N×U×M / A　（lx）</div>
    <div class="tip">F：1灯の光束(lm)、N：灯数、U：照明率、M：保守率、A：床面積(m²)</div>
  </div>
  <div class="card">
    <div class="card-title"><span class="tag tag-orange">重要</span>照明器具の種類と特徴</div>
    <div class="tw"><table>
      <tr><th>種類</th><th>特徴</th><th>用途</th></tr>
      <tr><td>LED</td><td>長寿命・省エネ・小型</td><td>現在の主流。ほぼ全用途</td></tr>
      <tr><td>高圧ナトリウム灯</td><td>最も効率が高い。演色性低い（黄色）</td><td>道路・トンネル</td></tr>
      <tr><td>メタルハライド灯</td><td>高輝度・演色性良い</td><td>スタジアム・展示場</td></tr>
      <tr><td>高圧水銀灯</td><td>高輝度。始動時間が長い</td><td>工場・スポーツ施設</td></tr>
      <tr><td>白熱電球</td><td>演色性最高（Ra100）。効率が低い</td><td>装飾・特殊用途</td></tr>
    </table></div>
  </div>
  <div class="card">
    <div class="card-title"><span class="tag tag-green">計算</span>熱の計算</div>
    <div class="formula">Q = P × t × 0.24　（cal）</div>
    <div class="formula">Q = P × t　（J）</div>
    <ul class="pl">
      <li>1cal = 4.186J（約4.2Jで計算してOK）</li>
      <li>1kWh = 860kcal（電力量→熱量換算）</li>
    </ul>
  </div>
  <div class="card">
    <div class="card-title"><span class="tag tag-blue">重要</span>蓄電池の種類</div>
    <div class="tw"><table>
      <tr><th>種類</th><th>起電力/セル</th><th>特徴</th><th>用途</th></tr>
      <tr><td>鉛蓄電池</td><td class="num-highlight">約2V</td><td>安価・大容量。重い</td><td>UPS・自動車</td></tr>
      <tr><td>ニッケルカドミウム</td><td class="num-highlight">約1.2V</td><td>長寿命・耐過放電</td><td>非常用電源</td></tr>
      <tr><td>リチウムイオン</td><td class="num-highlight">約3.6V</td><td>高エネルギー密度・軽量</td><td>スマホ・電動車</td></tr>
      <tr><td>ニッケル水素</td><td class="num-highlight">約1.2V</td><td>カドミウムなし。自己放電大</td><td>ハイブリッド車</td></tr>
    </table></div>
  </div>
  <div class="card">
    <div class="card-title"><span class="tag tag-green">太陽光</span>太陽光発電の基礎</div>
    <ul class="pl">
      <li>太陽電池（PVモジュール）は直流発電→パワーコンディショナ（PCS）で交流に変換</li>
      <li>系統連系：商用電源と連系。逆潮流（売電）が可能</li>
      <li>自立運転：停電時に商用電源から切り離して単独で発電・使用するモード</li>
      <li>FIT（固定価格買取制度）：再生可能エネルギーを一定価格で買い取る制度</li>
    </ul>
  </div>
</section>

<!-- 重要数値まとめ -->
<section class="section" id="s12">
  <div class="section-header"><h2>📊 重要数値 総まとめ</h2><p>試験直前にここだけ確認！</p></div>
  <div class="card">
    <div class="card-title"><span class="tag tag-blue">試験に出る重要数値一覧</span></div>
    <div class="tw"><table>
      <tr><th>項目</th><th>数値</th></tr>
      <tr><td>低圧の上限（交流）</td><td class="num-highlight">600V</td></tr>
      <tr><td>高圧の上限</td><td class="num-highlight">7,000V</td></tr>
      <tr><td>A種・C種接地抵抗</td><td class="num-highlight">10Ω以下</td></tr>
      <tr><td>D種接地抵抗</td><td class="num-highlight">100Ω以下</td></tr>
      <tr><td>漏電遮断器の感度電流</td><td class="num-highlight">30mA以下</td></tr>
      <tr><td>漏電遮断器の動作時間</td><td class="num-highlight">0.1秒以内</td></tr>
      <tr><td>絶縁耐力試験の印加時間</td><td class="num-highlight">10分間</td></tr>
      <tr><td>絶縁耐力試験電圧倍率（7000V以下）</td><td class="num-highlight">×1.5倍</td></tr>
      <tr><td>低圧回路の絶縁抵抗（300V以下）</td><td class="num-highlight">0.1MΩ以上</td></tr>
      <tr><td>CTの2次側定格電流</td><td class="num-highlight">5A</td></tr>
      <tr><td>VTの2次側定格電圧</td><td class="num-highlight">110V</td></tr>
      <tr><td>第一種電気工事士の定期講習</td><td class="num-highlight">5年ごと</td></tr>
      <tr><td>東日本／西日本の周波数</td><td class="num-highlight">50Hz／60Hz</td></tr>
      <tr><td>架空電線の道路横断最低高さ</td><td class="num-highlight">6m以上</td></tr>
      <tr><td>金属管の支持間隔</td><td class="num-highlight">2m以下</td></tr>
      <tr><td>合成樹脂管の支持間隔</td><td class="num-highlight">1.5m以下</td></tr>
      <tr><td>埋設ケーブルの最小深さ（重量物あり）</td><td class="num-highlight">1.2m以上</td></tr>
      <tr><td>1kWh = ?kcal</td><td class="num-highlight">860kcal</td></tr>
      <tr><td>1cal = ?J</td><td class="num-highlight">4.186J（≒4.2J）</td></tr>
      <tr><td>鉛蓄電池の起電力（1セル）</td><td class="num-highlight">約2V</td></tr>
    </table></div>
  </div>
  <div class="card">
    <div class="card-title"><span class="tag tag-orange">よく出る重要用語</span></div>
    <div class="g2">
      <div class="term"><div class="term-name">SOG機能</div><div class="term-desc">地絡保護・自動開放機能。地絡を検出したPASが自動的に開放する</div></div>
      <div class="term"><div class="term-name">ZCT（零相変流器）</div><div class="term-desc">地絡電流を検出する変流器。DGR・ELCBと組み合わせる</div></div>
      <div class="term"><div class="term-name">波及事故</div><div class="term-desc">自家用電気工作物の事故が配電系統に広がり他の需要家も停電する事故</div></div>
      <div class="term"><div class="term-name">フェランチ現象</div><div class="term-desc">軽負荷時に長い送電線の受電端電圧が送電端より高くなる現象</div></div>
      <div class="term"><div class="term-name">ヒステリシス損</div><div class="term-desc">交流磁界により磁性体内で発生する損失。珪素鋼板で低減する</div></div>
      <div class="term"><div class="term-name">渦電流損</div><div class="term-desc">磁性体内に誘起される渦電流による損失。積層鉄心で低減する</div></div>
      <div class="term"><div class="term-name">表皮効果</div><div class="term-desc">高周波電流が導体表面付近に集中する現象。周波数が高いほど顕著</div></div>
      <div class="term"><div class="term-name">UPS（無停電電源装置）</div><div class="term-desc">停電時に蓄電池からコンピュータ等へ安定電力を供給する装置</div></div>
    </div>
  </div>
</section>
```

  </main>
</div>

<script>
const visited = new Set(['s0']);
function updateProgress(){
  const total = 13;
  document.getElementById('progressFill').style.width = (visited.size/total*100)+'%';
}
function show(id, el){
  document.querySelectorAll('.section').forEach(s=>s.classList.remove('active'));
  document.querySelectorAll('.nav-item').forEach(n=>n.classList.remove('active'));
  document.getElementById(id).classList.add('active');
  if(el) el.classList.add('active');
  visited.add(id);
  updateProgress();
  document.querySelector('.main').scrollTop=0;
  closeMenu();
}
function toggleMenu(){
  document.getElementById('sidebar').classList.toggle('open');
  document.getElementById('overlay').classList.toggle('open');
}
function closeMenu(){
  document.getElementById('sidebar').classList.remove('open');
  document.getElementById('overlay').classList.remove('open');
}
updateProgress();
</script>

</body>
</html>
