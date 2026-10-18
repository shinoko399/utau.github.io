---
permalink: /
title: "Academic Pages is a ready-to-fork GitHub Pages template for academic personal websites"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

<!DOCTYPE html>
<html lang="zh-CN">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1">
<title>無生物UTAU音源合成器 · 辅音修复版</title>
<style>
*{box-sizing:border-box;margin:0;padding:0}
body{font-family:-apple-system,"Segoe UI",system-ui,"Hiragino Sans",sans-serif;background:#0d0d12;color:#e0e0e0;min-height:100vh;padding:36px 20px;line-height:1.5}
.container{max-width:920px;margin:0 auto}
h1{font-size:1.45rem;margin-bottom:6px;color:#fff;letter-spacing:-.01em}
.subtitle{color:#888;font-size:.85rem;margin-bottom:24px}
.card{background:#16161f;border:1px solid #282835;border-radius:12px;padding:22px;margin-bottom:16px}
.card h2{font-size:1rem;margin-bottom:14px;color:#9d9dff;font-weight:600}
.drop-zone{border:2px dashed #383850;border-radius:10px;padding:28px 18px;text-align:center;cursor:pointer;transition:all .18s ease}
.drop-zone:hover,.drop-zone.dragover{border-color:#6060ff;background:#1a1a2c}
.drop-zone .icon{font-size:2rem;margin-bottom:6px;opacity:.8}
.drop-zone p{color:#888;font-size:.84rem}
.file-list{margin-top:14px}
.file-item{display:flex;align-items:center;gap:10px;padding:9px 12px;background:#101018;border-radius:8px;margin-bottom:6px;font-size:.82rem;border:1px solid #202028}
.file-item .name{flex:1;overflow:hidden;text-overflow:ellipsis;white-space:nowrap}
.file-item .status{color:#5fb85f;font-size:.75rem;font-family:ui-monospace,monospace}
.file-item .del{background:none;border:none;color:#e05555;cursor:pointer;font-size:1.1rem;padding:0 4px}
.file-item .del:hover{color:#ff7777}
.stats{display:grid;grid-template-columns:repeat(3,1fr);gap:10px;margin-top:12px}
.stat{background:#101018;padding:10px 12px;border-radius:8px;border:1px solid #202028}
.stat .k{font-size:.7rem;color:#666;text-transform:uppercase;letter-spacing:.04em}
.stat .v{font-size:1.02rem;color:#9d9dff;font-family:ui-monospace,monospace;margin-top:2px}
.setting-row{display:flex;align-items:center;gap:12px;padding:10px 0;border-bottom:1px solid #202028}
.setting-row:last-child{border-bottom:none}
.setting-row label{flex:1;font-size:.87rem;color:#ccc}
.setting-row input[type=checkbox]{width:17px;height:17px;accent-color:#6060ff;cursor:pointer}
.action-btn{width:100%;padding:13px;border-radius:10px;border:none;background:linear-gradient(135deg,#5050dd,#8040cc);color:#fff;font-size:.97rem;font-weight:500;cursor:pointer;transition:all .18s;margin-top:16px}
.action-btn:disabled{opacity:.35;cursor:not-allowed}
.action-btn:hover:not(:disabled){opacity:.92;transform:translateY(-1px)}
.progress-bar{height:5px;background:#202030;border-radius:3px;margin-top:14px;overflow:hidden}
.progress-fill{height:100%;background:linear-gradient(90deg,#5050dd,#8040cc);width:0%;transition:width .25s ease;border-radius:3px}
.log{margin-top:12px;font-size:.72rem;color:#888;max-height:240px;overflow-y:auto;font-family:ui-monospace,"SF Mono",Menlo,monospace;line-height:1.5;padding-right:6px}
.log::-webkit-scrollbar{width:6px}
.log::-webkit-scrollbar-thumb{background:#303040;border-radius:3px}
.log div{padding:1px 0}
.log .ok{color:#5fb85f}
.log .warn{color:#e0aa50}
.log .err{color:#e05555}
.log .diag{color:#6a9eff}
.download-btn{display:none;width:100%;padding:13px;border-radius:10px;border:2px solid #40c060;background:transparent;color:#40c060;font-size:.97rem;font-weight:500;cursor:pointer;margin-top:12px;transition:all .18s}
.download-btn:hover{background:#40c060;color:#000}
.preview-header{display:flex;align-items:center;gap:10px;padding:10px 12px;background:#101018;border:1px solid #202028;border-radius:8px;margin-bottom:14px}
.preview-header .btn{padding:7px 14px;border-radius:6px;border:1px solid #303040;background:#0a0a10;color:#ccc;font-size:.8rem;cursor:pointer;transition:all .15s;font-family:inherit}
.preview-header .btn:hover{border-color:#6060ff;color:#fff}
.preview-header .btn.primary{border-color:#5050dd;color:#a0a0ff}
.preview-header .btn.primary:hover{background:#282860;color:#fff}
.now-playing{margin-left:auto;font-size:.82rem;color:#5fb85f;font-family:ui-monospace,monospace}
.phoneme-grid{display:flex;flex-direction:column;gap:6px;max-height:520px;overflow-y:auto;padding-right:8px}
.phoneme-grid::-webkit-scrollbar{width:6px}
.phoneme-grid::-webkit-scrollbar-thumb{background:#303040;border-radius:3px}
.phoneme-row{display:flex;align-items:flex-start;gap:10px}
.phoneme-row-label{font-size:.72rem;color:#666;width:72px;flex-shrink:0;padding-top:8px;font-family:ui-monospace,monospace}
.phoneme-row-items{display:flex;flex-wrap:wrap;gap:4px;flex:1}
.phoneme-btn{min-width:46px;padding:6px 10px;background:#101018;border:1px solid #202028;border-radius:6px;color:#ccc;font-size:.86rem;cursor:pointer;transition:all .15s;font-family:inherit;user-select:none}
.phoneme-btn:hover{border-color:#6060ff;background:#1a1a2c;color:#fff}
.phoneme-btn:active{transform:scale(.95)}
.phoneme-btn.playing{border-color:#40c060;background:#0e2a0e;color:#40c060;box-shadow:0 0 0 2px rgba(64,192,96,.2)}
.tip{font-size:.75rem;color:#666;margin-top:10px}
</style>
</head>
<body>
<div class="container">
  <h1>🎛️ 無生物UTAU音源合成器 · 辅音修复版</h1>
  <p class="subtitle">辅音独立分段合成 · 无过渡段混淆 · 平假名文件名 · Shift-JIS</p>

  <div class="card">
    <h2>① 上传采样</h2>
    <div class="drop-zone" id="dropZone">
      <div class="icon">📁</div>
      <p>拖拽音频到此处，或点击选择</p>
      <p style="margin-top:6px;font-size:.76rem;color:#555">文件名支持罗马字（ka.wav）或平假名（か.wav）；否则自动切片</p>
      <input type="file" id="fileInput" accept="audio/*" multiple hidden>
    </div>
    <div class="file-list" id="fileList"></div>
    <div class="stats" id="stats" style="display:none">
      <div class="stat"><div class="k">文件</div><div class="v" id="statFiles">0</div></div>
      <div class="stat"><div class="k">音素</div><div class="v" id="statSamples">0</div></div>
      <div class="stat"><div class="k">时长</div><div class="v" id="statDur">0s</div></div>
    </div>
  </div>

  <div class="card">
    <h2>② 合成设置</h2>
    <div class="setting-row">
      <label>自动补齐缺失元音</label>
      <input type="checkbox" id="autoVowel" checked>
    </div>
    <div class="setting-row">
      <label>自动合成缺失 CV 音节</label>
      <input type="checkbox" id="autoCV" checked>
    </div>
    <div class="setting-row">
      <label>共振峰锐化（+1.5dB）</label>
      <input type="checkbox" id="sharpenFormant" checked>
    </div>
    <div class="setting-row">
      <label>辅音前置静默段（持阻）</label>
      <input type="checkbox" id="silenceBurst" checked>
    </div>
    <div class="setting-row">
      <label>元音时长上限 500ms</label>
      <input type="checkbox" id="trimVowel" checked>
    </div>
    <div class="setting-row">
      <label>去除 DC + 80Hz 高通</label>
      <input type="checkbox" id="cleanup" checked>
    </div>
    <div class="setting-row">
      <label>oto.ini 使用 Shift-JIS 编码</label>
      <input type="checkbox" id="useSjis" checked>
    </div>
    <div style="font-size:.75rem;color:#666;padding-top:10px">
      ※ 辅音独立合成，不做过渡段；元音和辅音分别归一化
    </div>
  </div>

  <div class="card">
    <h2>③ 合成并导出</h2>
    <button class="action-btn" id="generateBtn" disabled>开始合成</button>
    <div class="progress-bar"><div class="progress-fill" id="progressFill"></div></div>
    <div class="log" id="log"></div>
    <button class="download-btn" id="downloadBtn">⬇ 下载音源包 (ZIP)</button>
  </div>

  <div class="card" id="previewCard" style="display:none">
    <h2>④ 试听</h2>
    <div class="preview-header">
      <button class="btn primary" id="previewAllBtn">▶ 播放全部</button>
      <button class="btn" id="stopPreviewBtn">■ 停止</button>
      <span class="now-playing" id="nowPlaying"></span>
    </div>
    <div class="phoneme-grid" id="phonemeGrid"></div>
    <p class="tip">提示：单击任一音素试听，再次点击"播放全部"可顺序试听</p>
  </div>
</div>

<script>
"use strict";

// ============================================================
// 常量
// ============================================================
const TWO_PI = Math.PI * 2;
const SR = 44100;
const EPS = 1e-10;
const LPC_ORDER = 20;
const DEFAULT_F0 = 130;
const VOWEL_MAX_MS = 500;
const VOWEL_PEAK = 0.72;
const XFADE_MS = 3;

const VOWEL_FORMANTS = {
  a: [{ f: 800, bw: 90 }, { f: 1200, bw: 110 }, { f: 2800, bw: 160 }],
  i: [{ f: 300, bw: 70 }, { f: 2300, bw: 120 }, { f: 3000, bw: 170 }],
  u: [{ f: 350, bw: 80 }, { f: 1300, bw: 110 }, { f: 2200, bw: 150 }],
  e: [{ f: 500, bw: 80 }, { f: 1800, bw: 110 }, { f: 2600, bw: 150 }],
  o: [{ f: 500, bw: 80 }, { f: 900, bw: 100 }, { f: 2400, bw: 150 }],
};

const HIGH_FORMANTS = [
  { f: 3500, bw: 220 },
  { f: 4500, bw: 280 },
  { f: 5800, bw: 350 },
];

const PHONEMES = [
  { kana:'あ', romaji:'a', cons:'', vowel:'a' },
  { kana:'い', romaji:'i', cons:'', vowel:'i' },
  { kana:'う', romaji:'u', cons:'', vowel:'u' },
  { kana:'え', romaji:'e', cons:'', vowel:'e' },
  { kana:'お', romaji:'o', cons:'', vowel:'o' },
  { kana:'か', romaji:'ka', cons:'k', vowel:'a' },
  { kana:'き', romaji:'ki', cons:'k', vowel:'i' },
  { kana:'く', romaji:'ku', cons:'k', vowel:'u' },
  { kana:'け', romaji:'ke', cons:'k', vowel:'e' },
  { kana:'こ', romaji:'ko', cons:'k', vowel:'o' },
  { kana:'が', romaji:'ga', cons:'g', vowel:'a' },
  { kana:'ぎ', romaji:'gi', cons:'g', vowel:'i' },
  { kana:'ぐ', romaji:'gu', cons:'g', vowel:'u' },
  { kana:'げ', romaji:'ge', cons:'g', vowel:'e' },
  { kana:'ご', romaji:'go', cons:'g', vowel:'o' },
  { kana:'さ', romaji:'sa', cons:'s', vowel:'a' },
  { kana:'し', romaji:'shi', cons:'sh', vowel:'i' },
  { kana:'す', romaji:'su', cons:'s', vowel:'u' },
  { kana:'せ', romaji:'se', cons:'s', vowel:'e' },
  { kana:'そ', romaji:'so', cons:'s', vowel:'o' },
  { kana:'ざ', romaji:'za', cons:'z', vowel:'a' },
  { kana:'じ', romaji:'ji', cons:'j', vowel:'i' },
  { kana:'ず', romaji:'zu', cons:'z', vowel:'u' },
  { kana:'ぜ', romaji:'ze', cons:'z', vowel:'e' },
  { kana:'ぞ', romaji:'zo', cons:'z', vowel:'o' },
  { kana:'た', romaji:'ta', cons:'t', vowel:'a' },
  { kana:'ち', romaji:'chi', cons:'ch', vowel:'i' },
  { kana:'つ', romaji:'tsu', cons:'ts', vowel:'u' },
  { kana:'て', romaji:'te', cons:'t', vowel:'e' },
  { kana:'と', romaji:'to', cons:'t', vowel:'o' },
  { kana:'だ', romaji:'da', cons:'d', vowel:'a' },
  { kana:'ぢ', romaji:'di', cons:'j', vowel:'i' },
  { kana:'づ', romaji:'du', cons:'z', vowel:'u' },
  { kana:'で', romaji:'de', cons:'d', vowel:'e' },
  { kana:'ど', romaji:'do', cons:'d', vowel:'o' },
  { kana:'な', romaji:'na', cons:'n', vowel:'a' },
  { kana:'に', romaji:'ni', cons:'n', vowel:'i' },
  { kana:'ぬ', romaji:'nu', cons:'n', vowel:'u' },
  { kana:'ね', romaji:'ne', cons:'n', vowel:'e' },
  { kana:'の', romaji:'no', cons:'n', vowel:'o' },
  { kana:'は', romaji:'ha', cons:'h', vowel:'a' },
  { kana:'ひ', romaji:'hi', cons:'h', vowel:'i' },
  { kana:'ふ', romaji:'fu', cons:'f', vowel:'u' },
  { kana:'へ', romaji:'he', cons:'h', vowel:'e' },
  { kana:'ほ', romaji:'ho', cons:'h', vowel:'o' },
  { kana:'ば', romaji:'ba', cons:'b', vowel:'a' },
  { kana:'び', romaji:'bi', cons:'b', vowel:'i' },
  { kana:'ぶ', romaji:'bu', cons:'b', vowel:'u' },
  { kana:'べ', romaji:'be', cons:'b', vowel:'e' },
  { kana:'ぼ', romaji:'bo', cons:'b', vowel:'o' },
  { kana:'ぱ', romaji:'pa', cons:'p', vowel:'a' },
  { kana:'ぴ', romaji:'pi', cons:'p', vowel:'i' },
  { kana:'ぷ', romaji:'pu', cons:'p', vowel:'u' },
  { kana:'ぺ', romaji:'pe', cons:'p', vowel:'e' },
  { kana:'ぽ', romaji:'po', cons:'p', vowel:'o' },
  { kana:'ま', romaji:'ma', cons:'m', vowel:'a' },
  { kana:'み', romaji:'mi', cons:'m', vowel:'i' },
  { kana:'む', romaji:'mu', cons:'m', vowel:'u' },
  { kana:'め', romaji:'me', cons:'m', vowel:'e' },
  { kana:'も', romaji:'mo', cons:'m', vowel:'o' },
  { kana:'や', romaji:'ya', cons:'y', vowel:'a' },
  { kana:'ゆ', romaji:'yu', cons:'y', vowel:'u' },
  { kana:'よ', romaji:'yo', cons:'y', vowel:'o' },
  { kana:'ら', romaji:'ra', cons:'r', vowel:'a' },
  { kana:'り', romaji:'ri', cons:'r', vowel:'i' },
  { kana:'る', romaji:'ru', cons:'r', vowel:'u' },
  { kana:'れ', romaji:'re', cons:'r', vowel:'e' },
  { kana:'ろ', romaji:'ro', cons:'r', vowel:'o' },
  { kana:'わ', romaji:'wa', cons:'w', vowel:'a' },
  { kana:'を', romaji:'wo', cons:'w', vowel:'o' },
  { kana:'ん', romaji:'n', cons:'', vowel:null, special:'n' },
  { kana:'きゃ', romaji:'kya', cons:'ky', vowel:'a' },
  { kana:'きゅ', romaji:'kyu', cons:'ky', vowel:'u' },
  { kana:'きょ', romaji:'kyo', cons:'ky', vowel:'o' },
  { kana:'ぎゃ', romaji:'gya', cons:'gy', vowel:'a' },
  { kana:'ぎゅ', romaji:'gyu', cons:'gy', vowel:'u' },
  { kana:'ぎょ', romaji:'gyo', cons:'gy', vowel:'o' },
  { kana:'しゃ', romaji:'sha', cons:'sh', vowel:'a' },
  { kana:'しゅ', romaji:'shu', cons:'sh', vowel:'u' },
  { kana:'しょ', romaji:'sho', cons:'sh', vowel:'o' },
  { kana:'じゃ', romaji:'ja', cons:'j', vowel:'a' },
  { kana:'じゅ', romaji:'ju', cons:'j', vowel:'u' },
  { kana:'じょ', romaji:'jo', cons:'j', vowel:'o' },
  { kana:'ちゃ', romaji:'cha', cons:'ch', vowel:'a' },
  { kana:'ちゅ', romaji:'chu', cons:'ch', vowel:'u' },
  { kana:'ちょ', romaji:'cho', cons:'ch', vowel:'o' },
  { kana:'にゃ', romaji:'nya', cons:'ny', vowel:'a' },
  { kana:'にゅ', romaji:'nyu', cons:'ny', vowel:'u' },
  { kana:'にょ', romaji:'nyo', cons:'ny', vowel:'o' },
  { kana:'ひゃ', romaji:'hya', cons:'hy', vowel:'a' },
  { kana:'ひゅ', romaji:'hyu', cons:'hy', vowel:'u' },
  { kana:'ひょ', romaji:'hyo', cons:'hy', vowel:'o' },
  { kana:'びゃ', romaji:'bya', cons:'by', vowel:'a' },
  { kana:'びゅ', romaji:'byu', cons:'by', vowel:'u' },
  { kana:'びょ', romaji:'byo', cons:'by', vowel:'o' },
  { kana:'ぴゃ', romaji:'pya', cons:'py', vowel:'a' },
  { kana:'ぴゅ', romaji:'pyu', cons:'py', vowel:'u' },
  { kana:'ぴょ', romaji:'pyo', cons:'py', vowel:'o' },
  { kana:'みゃ', romaji:'mya', cons:'my', vowel:'a' },
  { kana:'みゅ', romaji:'myu', cons:'my', vowel:'u' },
  { kana:'みょ', romaji:'myo', cons:'my', vowel:'o' },
  { kana:'りゃ', romaji:'rya', cons:'ry', vowel:'a' },
  { kana:'りゅ', romaji:'ryu', cons:'ry', vowel:'u' },
  { kana:'りょ', romaji:'ryo', cons:'ry', vowel:'o' },
];

const KANA_INDEX = {};
const ROMAJI_INDEX = {};
for (const p of PHONEMES) {
  KANA_INDEX[p.kana] = p;
  ROMAJI_INDEX[p.romaji] = p;
}

const VOWEL_LIST = ['a', 'i', 'u', 'e', 'o'];

const PHONEME_ROWS = [
  { name: 'あ行', keys: ['a','i','u','e','o'] },
  { name: 'か行', keys: ['ka','ki','ku','ke','ko'] },
  { name: 'が行', keys: ['ga','gi','gu','ge','go'] },
  { name: 'さ行', keys: ['sa','shi','su','se','so'] },
  { name: 'ざ行', keys: ['za','ji','zu','ze','zo'] },
  { name: 'た行', keys: ['ta','chi','tsu','te','to'] },
  { name: 'だ行', keys: ['da','di','du','de','do'] },
  { name: 'な行', keys: ['na','ni','nu','ne','no'] },
  { name: 'は行', keys: ['ha','hi','fu','he','ho'] },
  { name: 'ば行', keys: ['ba','bi','bu','be','bo'] },
  { name: 'ぱ行', keys: ['pa','pi','pu','pe','po'] },
  { name: 'ま行', keys: ['ma','mi','mu','me','mo'] },
  { name: 'や行', keys: ['ya','yu','yo'] },
  { name: 'ら行', keys: ['ra','ri','ru','re','ro'] },
  { name: 'わ行', keys: ['wa','wo'] },
  { name: 'ん',    keys: ['n'] },
  { name: '拗・き', keys: ['kya','kyu','kyo'] },
  { name: '拗・ぎ', keys: ['gya','gyu','gyo'] },
  { name: '拗・し', keys: ['sha','shu','sho'] },
  { name: '拗・じ', keys: ['ja','ju','jo'] },
  { name: '拗・ち', keys: ['cha','chu','cho'] },
  { name: '拗・に', keys: ['nya','nyu','nyo'] },
  { name: '拗・ひ', keys: ['hya','hyu','hyo'] },
  { name: '拗・び', keys: ['bya','byu','byo'] },
  { name: '拗・ぴ', keys: ['pya','pyu','pyo'] },
  { name: '拗・み', keys: ['mya','myu','myo'] },
  { name: '拗・り', keys: ['rya','ryu','ryo'] },
];

// ============================================================
// Shift-JIS
// ============================================================
let SJIS_AVAILABLE = false;
async function loadShiftJisLib() {
  if (window.Encoding) { SJIS_AVAILABLE = true; return true; }
  try {
    await new Promise((resolve, reject) => {
      const s = document.createElement('script');
      s.src = 'https://cdnjs.cloudflare.com/ajax/libs/encoding-japanese/2.0.0/encoding.min.js';
      s.onload = resolve;
      s.onerror = () => reject(new Error('load failed'));
      document.head.appendChild(s);
    });
    SJIS_AVAILABLE = !!(window.Encoding && window.Encoding.convert);
    return SJIS_AVAILABLE;
  } catch (e) { SJIS_AVAILABLE = false; return false; }
}

function textToBlob(text, useSjis) {
  if (useSjis && SJIS_AVAILABLE && window.Encoding) {
    try {
      const u = window.Encoding.stringToCode(text);
      const sj = window.Encoding.convert(u, { to: 'SJIS', from: 'UNICODE', fallback: '?' });
      return new Blob([new Uint8Array(sj)], { type: 'text/plain' });
    } catch (e) { console.warn('SJIS failed'); }
  }
  return new Blob([text], { type: 'text/plain;charset=utf-8' });
}

// ============================================================
// 基础工具
// ============================================================
function toMono(ab) {
  const nCh = ab.numberOfChannels, len = ab.length;
  if (nCh === 1) return new Float32Array(ab.getChannelData(0));
  const out = new Float32Array(len);
  for (let c = 0; c < nCh; c++) {
    const d = ab.getChannelData(c);
    for (let i = 0; i < len; i++) out[i] += d[i];
  }
  for (let i = 0; i < len; i++) out[i] /= nCh;
  return out;
}

function resampleLinear(input, srIn, srOut) {
  if (srIn === srOut) return new Float32Array(input);
  const ratio = srOut / srIn;
  const outLen = Math.floor(input.length * ratio);
  const out = new Float32Array(outLen);
  const last = input.length - 1;
  for (let i = 0; i < outLen; i++) {
    const s = i / ratio;
    const i0 = Math.floor(s);
    const i1 = i0 + 1 > last ? last : i0 + 1;
    const t = s - i0;
    out[i] = input[i0] * (1 - t) + input[i1] * t;
  }
  return out;
}

function removeDC(sig) {
  const n = sig.length;
  if (n === 0) return new Float32Array(0);
  let s = 0;
  for (let i = 0; i < n; i++) s += sig[i];
  const m = s / n;
  const out = new Float32Array(n);
  for (let i = 0; i < n; i++) out[i] = sig[i] - m;
  return out;
}

function highpass(sig, sr, fc) {
  const n = sig.length;
  const out = new Float32Array(n);
  const w0 = TWO_PI * fc / sr;
  const c = Math.cos(w0), s = Math.sin(w0);
  const alpha = s / Math.SQRT2;
  const a0 = 1 + alpha;
  const b0 = (1 + c) / 2 / a0;
  const b1 = -(1 + c) / a0;
  const b2 = (1 + c) / 2 / a0;
  const a1 = -2 * c / a0;
  const a2 = (1 - alpha) / a0;
  let x1 = 0, x2 = 0, y1 = 0, y2 = 0;
  for (let i = 0; i < n; i++) {
    const x0 = sig[i];
    const y0 = b0 * x0 + b1 * x1 + b2 * x2 - a1 * y1 - a2 * y2;
    out[i] = y0;
    x2 = x1; x1 = x0; y2 = y1; y1 = y0;
  }
  return out;
}

function normalizePeak(sig, target) {
  const n = sig.length;
  if (n === 0) return sig;
  let p = 0;
  for (let i = 0; i < n; i++) { const a = Math.abs(sig[i]); if (a > p) p = a; }
  if (p < 1e-9) return sig;
  const g = (target || 0.89) / p;
  const out = new Float32Array(n);
  for (let i = 0; i < n; i++) out[i] = sig[i] * g;
  return out;
}

function getPeak(sig) {
  let p = 0;
  for (let i = 0; i < sig.length; i++) { const a = Math.abs(sig[i]); if (a > p) p = a; }
  return p;
}

function trimToMax(sig, sr, maxMs) {
  const maxLen = Math.floor(sr * maxMs / 1000);
  if (sig.length <= maxLen) return sig;
  const start = Math.floor((sig.length - maxLen) / 2);
  const out = new Float32Array(maxLen);
  for (let i = 0; i < maxLen; i++) out[i] = sig[start + i];
  return out;
}

function applyFadeInOut(sig, sr, fadeMs) {
  const n = sig.length;
  const fade = Math.min(Math.floor(sr * fadeMs / 1000), Math.floor(n / 2));
  if (fade <= 0) return sig;
  const out = new Float32Array(sig);
  for (let i = 0; i < fade; i++) {
    const g = i / fade;
    out[i] *= g;
    out[n - 1 - i] *= g;
  }
  return out;
}

function hannWindow(N) {
  const w = new Float32Array(N);
  for (let i = 0; i < N; i++) w[i] = 0.5 * (1 - Math.cos(TWO_PI * i / (N - 1)));
  return w;
}

// ============================================================
// LPC
// ============================================================
function preEmphasis(sig, alpha) {
  alpha = alpha === undefined ? 0.97 : alpha;
  const n = sig.length;
  const out = new Float32Array(n);
  if (n === 0) return out;
  out[0] = sig[0];
  for (let i = 1; i < n; i++) out[i] = sig[i] - alpha * sig[i-1];
  return out;
}

function deEmphasis(sig, alpha) {
  alpha = alpha === undefined ? 0.97 : alpha;
  const n = sig.length;
  const out = new Float32Array(n);
  if (n === 0) return out;
  let prev = 0;
  for (let i = 0; i < n; i++) {
    let v = sig[i] + alpha * prev;
    if (!isFinite(v)) v = 0;
    out[i] = v;
    prev = v;
  }
  return out;
}

function autocorrelation(sig, order) {
  const n = sig.length;
  const r = new Float64Array(order + 1);
  for (let k = 0; k <= order; k++) {
    let s = 0;
    for (let i = k; i < n; i++) s += sig[i] * sig[i-k];
    r[k] = s;
  }
  return r;
}

function levinsonDurbin(r, order) {
  const a = new Float64Array(order + 1);
  let E = r[0];
  if (E < EPS) return { a, error: 0 };
  for (let i = 1; i <= order; i++) {
    let num = r[i];
    for (let j = 1; j < i; j++) num += a[j] * r[i-j];
    const k = -num / E;
    if (Math.abs(k) >= 1) { a[i] = 0; break; }
    const ac = new Float64Array(a);
    a[i] = k;
    for (let j = 1; j < i; j++) a[j] = ac[j] + k * ac[i-j];
    E *= (1 - k * k);
    if (E < EPS) break;
  }
  return { a, error: E };
}

function lpcAnalyzeSegment(seg, sr, order) {
  const n = seg.length;
  if (n < order * 4) return new Float64Array(order + 1);
  const pre = preEmphasis(seg, 0.97);
  const win = hannWindow(n);
  for (let i = 0; i < n; i++) pre[i] *= win[i];
  const r = autocorrelation(pre, order);
  const { a } = levinsonDurbin(r, order);
  return a;
}

function formantToLPC(formants, sr, order) {
  let poly = new Float64Array([1]);
  for (const { f, bw } of formants) {
    const r = Math.exp(-Math.PI * bw / sr);
    const theta = TWO_PI * f / sr;
    const a1 = -2 * r * Math.cos(theta);
    const a2 = r * r;
    const np = new Float64Array(poly.length + 2);
    for (let i = 0; i < poly.length; i++) {
      np[i] += poly[i];
      np[i+1] += poly[i] * a1;
      np[i+2] += poly[i] * a2;
    }
    poly = np;
  }
  const a = new Float64Array(order + 1);
  a[0] = 1;
  for (let i = 1; i < Math.min(poly.length, order + 1); i++) a[i] = poly[i];
  return a;
}

function buildVowelLPC(vowel, sr, sharpen) {
  let formants = VOWEL_FORMANTS[vowel].map(f => ({ f: f.f, bw: f.bw }));
  if (sharpen) for (const f of formants) f.bw *= 0.8;
  for (const hf of HIGH_FORMANTS) formants.push({ f: hf.f, bw: hf.bw });
  return formantToLPC(formants, sr, LPC_ORDER);
}

function lpcSynthesize(excitation, a) {
  const p = a.length - 1;
  const n = excitation.length;
  const out = new Float32Array(n);
  for (let i = 0; i < n; i++) {
    let s = excitation[i];
    for (let k = 1; k <= p; k++) {
      if (i - k >= 0) s -= a[k] * out[i - k];
    }
    if (!isFinite(s)) s = 0;
    out[i] = s;
  }
  return out;
}

function vowelTransformLPC(input, sr, srcV, dstV, sharpen) {
  if (srcV === dstV) return new Float32Array(input);
  const frameSize = Math.floor(sr * 0.04);
  const hop = Math.max(64, Math.floor(sr * 0.005));
  const order = LPC_ORDER;
  const halfFrame = Math.floor(frameSize / 2);
  const numFrames = Math.ceil(input.length / hop) + 2;
  const frameCoeffs = [];
  let prevA = new Float64Array(order + 1);
  for (let f = 0; f < numFrames; f++) {
    const center = f * hop;
    const s0 = Math.max(0, center - halfFrame);
    const s1 = Math.min(input.length, s0 + frameSize);
    const segLen = s1 - s0;
    if (segLen < order * 4) { frameCoeffs.push(prevA); continue; }
    const seg = new Float32Array(segLen);
    for (let i = 0; i < segLen; i++) seg[i] = input[s0 + i];
    const a = lpcAnalyzeSegment(seg, sr, order);
    let valid = true;
    for (let k = 0; k <= order; k++) if (!isFinite(a[k]) || Math.abs(a[k]) > 20) { valid = false; break; }
    const coeff = valid ? a : prevA;
    frameCoeffs.push(coeff);
    prevA = coeff;
  }
  const pre = preEmphasis(input, 0.97);
  const excitation = new Float32Array(input.length);
  for (let i = 0; i < input.length; i++) {
    const fp = i / hop;
    const f0 = Math.min(Math.floor(fp), frameCoeffs.length - 1);
    const f1 = Math.min(f0 + 1, frameCoeffs.length - 1);
    const t = fp - f0;
    const a0 = frameCoeffs[f0], a1 = frameCoeffs[f1];
    let e = pre[i];
    const kmax = Math.min(order, i);
    for (let k = 1; k <= kmax; k++) {
      const ak = a0[k] * (1 - t) + a1[k] * t;
      e += ak * pre[i - k];
    }
    if (!isFinite(e)) e = 0;
    if (Math.abs(e) > 50) e = Math.sign(e) * 50;
    excitation[i] = e;
  }
  const aDst = buildVowelLPC(dstV, sr, sharpen);
  const synth = lpcSynthesize(excitation, aDst);
  let maxAbs = 0;
  for (let i = 0; i < synth.length; i++) { const a = Math.abs(synth[i]); if (isFinite(a) && a > maxAbs) maxAbs = a; }
  if (!isFinite(maxAbs) || maxAbs > 1e4) return new Float32Array(input);
  const result = deEmphasis(synth, 0.97);
  for (let i = 0; i < result.length; i++) if (!isFinite(result[i])) result[i] = 0;
  return result;
}

// ============================================================
// 激励源生成
// ============================================================
function generateNoise(len, seed) {
  const out = new Float32Array(len);
  let s = (seed | 0) || 12345;
  if (s === 0) s = 12345;
  for (let i = 0; i < len; i++) {
    s = (Math.imul(s, 1103515245) + 12345) & 0x7fffffff;
    out[i] = (s / 0x3fffffff) - 1;
  }
  return out;
}

function generatePulseTrain(len, sr, f0) {
  const out = new Float32Array(len);
  if (!f0 || f0 <= 0) f0 = DEFAULT_F0;
  const basePeriod = sr / f0;
  if (basePeriod <= 0 || !isFinite(basePeriod)) return out;
  let pos = 0;
  while (pos < len) {
    const periodJitter = 1 + (Math.random() - 0.5) * 0.04;
    const ampShimmer = 1 + (Math.random() - 0.5) * 0.12;
    const period = basePeriod * periodJitter;
    const periodSamples = Math.max(2, Math.round(period));
    for (let i = 0; i < periodSamples && pos + i < len; i++) {
      const phase = i / periodSamples;
      let v;
      if (phase < 0.4) {
        const t1 = phase / 0.4;
        v = Math.tanh(t1 * 4) * Math.tanh((1 - t1) * 4) * 0.85;
      } else {
        v = -Math.exp(-(phase - 0.4) * 6) * 0.30;
      }
      out[pos + i] = v * ampShimmer;
    }
    pos += periodSamples;
  }
  return out;
}

// ============================================================
// 谐振器（二阶 IIR，峰值归一化）
// ============================================================
function resonatorCoeffsPeak(freq, bw, sr) {
  const r = Math.exp(-Math.PI * bw / sr);
  const theta = TWO_PI * freq / sr;
  const a1 = -2 * r * Math.cos(theta);
  const a2 = r * r;
  const dRe = 1 + a1 * Math.cos(theta) + a2 * Math.cos(2 * theta);
  const dIm = -a1 * Math.sin(theta) - a2 * Math.sin(2 * theta);
  const dMag = Math.sqrt(dRe * dRe + dIm * dIm) + 1e-10;
  return { b0: dMag, a1, a2 };
}

function applyResonators(input, resonators, sr) {
  const n = input.length;
  const numRes = resonators.length;
  const out = new Float32Array(n);
  const coeffs = resonators.map(([f, bw]) => resonatorCoeffsPeak(f, bw, sr));
  const y1 = new Float32Array(numRes);
  const y2 = new Float32Array(numRes);
  for (let i = 0; i < n; i++) {
    const x = input[i];
    let sum = 0;
    for (let r = 0; r < numRes; r++) {
      const c = coeffs[r];
      const y0 = c.b0 * x - c.a1 * y1[r] - c.a2 * y2[r];
      if (!isFinite(y0)) { y2[r] = 0; y1[r] = 0; continue; }
      y2[r] = y1[r];
      y1[r] = y0;
      sum += y0;
    }
    out[i] = sum / numRes;
  }
  return out;
}

// ============================================================
// 辅音定义（分类型设计）
// ============================================================
// 两种结构：
//   plosive 型：silenceMs + burstMs + aspMs（burst 和 asp 各用一套谐振器）
//   steady 型：silenceMs + mainMs（单段稳态）
//
// peak：目标峰值（辅音在拼接前归一化到这个值）
//   - 爆破音 0.60-0.65（短促，能量集中）
//   - 擦音 0.50-0.55（高频，不需要太响）
//   - 鼻音 0.72（和元音接近）
//   - 浊音 0.60-0.65

const CONS_DEFS = {
  // ===== 清爆破音 =====
  k: {
    type: 'plosive',
    silenceMs: 18, burstMs: 8, aspMs: 25,
    burstReson: [[2000, 500], [3500, 800]],
    aspReson: [[1800, 600]],
    voiced: false, noiseAmt: 1.0, peak: 0.62,
  },
  p: {
    type: 'plosive',
    silenceMs: 18, burstMs: 6, aspMs: 22,
    burstReson: [[1000, 400], [1800, 700]],
    aspReson: [[1200, 500]],
    voiced: false, noiseAmt: 0.95, peak: 0.58,
  },
  t: {
    type: 'plosive',
    silenceMs: 18, burstMs: 7, aspMs: 25,
    burstReson: [[3500, 700], [5000, 1000]],
    aspReson: [[3000, 800]],
    voiced: false, noiseAmt: 1.0, peak: 0.62,
  },
  // ===== 浊爆破音 =====
  g: {
    type: 'plosive',
    silenceMs: 15, burstMs: 8, aspMs: 30,
    burstReson: [[1800, 600], [2800, 800]],
    aspReson: [[1800, 600]],
    voiced: true, noiseAmt: 0.35, peak: 0.60,
  },
  b: {
    type: 'plosive',
    silenceMs: 15, burstMs: 8, aspMs: 30,
    burstReson: [[700, 400], [1200, 700]],
    aspReson: [[900, 500]],
    voiced: true, noiseAmt: 0.35, peak: 0.60,
  },
  d: {
    type: 'plosive',
    silenceMs: 15, burstMs: 8, aspMs: 30,
    burstReson: [[2800, 700], [3800, 900]],
    aspReson: [[2500, 700]],
    voiced: true, noiseAmt: 0.35, peak: 0.60,
  },
  // ===== 清塞擦音（burst + 摩擦）=====
  ch: {
    type: 'plosive',
    silenceMs: 12, burstMs: 5, aspMs: 65,
    burstReson: [[3500, 800]],
    aspReson: [[3500, 900], [5000, 1400], [2500, 800]],
    voiced: false, noiseAmt: 1.0, peak: 0.50,
  },
  ts: {
    type: 'plosive',
    silenceMs: 12, burstMs: 5, aspMs: 65,
    burstReson: [[4500, 800]],
    aspReson: [[5500, 1000], [4200, 1200]],
    voiced: false, noiseAmt: 1.0, peak: 0.50,
  },
  j: {
    type: 'plosive',
    silenceMs: 10, burstMs: 5, aspMs: 60,
    burstReson: [[3500, 800]],
    aspReson: [[3500, 900], [5000, 1400]],
    voiced: true, noiseAmt: 0.5, peak: 0.55,
  },
  // ===== 清擦音 =====
  s: { type: 'steady', silenceMs: 0, mainMs: 100, reson: [[6500, 1000], [4200, 1300], [8000, 1500]], voiced: false, noiseAmt: 1.0, peak: 0.50 },
  sh: { type: 'steady', silenceMs: 0, mainMs: 95, reson: [[3500, 1000], [5000, 1500], [2500, 900]], voiced: false, noiseAmt: 1.0, peak: 0.50 },
  h: { type: 'steady', silenceMs: 0, mainMs: 75, reson: [[1500, 900], [2500, 1300]], voiced: false, noiseAmt: 1.0, peak: 0.55 },
  f: { type: 'steady', silenceMs: 0, mainMs: 80, reson: [[5000, 1800], [7000, 2200]], voiced: false, noiseAmt: 0.95, peak: 0.55 },
  // ===== 浊擦音 =====
  z: { type: 'steady', silenceMs: 0, mainMs: 85, reson: [[5500, 1100], [4000, 1300]], voiced: true, noiseAmt: 0.6, peak: 0.55 },
  // ===== 鼻音 =====
  m: { type: 'steady', silenceMs: 0, mainMs: 75, reson: [[300, 150], [1100, 300]], voiced: true, noiseAmt: 0.05, peak: 0.72 },
  n: { type: 'steady', silenceMs: 0, mainMs: 75, reson: [[300, 150], [1600, 350]], voiced: true, noiseAmt: 0.05, peak: 0.72 },
  // ===== 流音 / 半元音 =====
  r: { type: 'steady', silenceMs: 0, mainMs: 55, reson: [[500, 120], [1300, 200]], voiced: true, noiseAmt: 0.05, peak: 0.68 },
  y: { type: 'steady', silenceMs: 0, mainMs: 55, reson: [[300, 100], [2200, 250]], voiced: true, noiseAmt: 0.05, peak: 0.68 },
  w: { type: 'steady', silenceMs: 0, mainMs: 55, reson: [[350, 100], [800, 200]], voiced: true, noiseAmt: 0.05, peak: 0.68 },
};

const CONS_Y_EXTEND = { ky: 'k', gy: 'g', ny: 'n', hy: 'h', by: 'b', py: 'p', my: 'm', ry: 'r' };

function getConsDef(consType, useSilence) {
  let def;
  if (CONS_DEFS[consType]) {
    def = JSON.parse(JSON.stringify(CONS_DEFS[consType]));
  } else if (CONS_Y_EXTEND[consType] && CONS_DEFS[CONS_Y_EXTEND[consType]]) {
    def = JSON.parse(JSON.stringify(CONS_DEFS[CONS_Y_EXTEND[consType]]));
    // 拗音加长 30%
    if (def.type === 'plosive') {
      def.aspMs = Math.round(def.aspMs * 1.3);
      def.burstMs = Math.round(def.burstMs * 1.15);
    } else {
      def.mainMs = Math.round(def.mainMs * 1.3);
    }
  } else {
    def = JSON.parse(JSON.stringify(CONS_DEFS.h));
  }
  if (!useSilence) def.silenceMs = 0;
  return def;
}

// ============================================================
// 包络（末尾保持能量，不衰减到 0）
// ============================================================
const ENV_POINTS = {
  burst: [[0, 0], [0.12, 1.0], [0.35, 0.55], [0.7, 0.38], [1.0, 0.28]],  // 冲击后保持 28%
  fric: [[0, 0], [0.05, 0.85], [0.15, 0.96], [0.6, 0.94], [0.85, 0.88], [1.0, 0.62]],  // 末尾保持 62%
  nasal: [[0, 0], [0.1, 0.88], [0.5, 0.95], [0.9, 0.92], [1.0, 0.75]],  // 末尾保持 75%
  tap: [[0, 0], [0.25, 0.9], [0.55, 0.7], [0.8, 0.6], [1.0, 0.55]],
};

function computeEnvelope(envType, t) {
  const pts = ENV_POINTS[envType] || ENV_POINTS.nasal;
  if (t <= pts[0][0]) return pts[0][1];
  if (t >= pts[pts.length-1][0]) return pts[pts.length-1][1];
  for (let i = 0; i < pts.length - 1; i++) {
    const t0 = pts[i][0], v0 = pts[i][1], t1 = pts[i+1][0], v1 = pts[i+1][1];
    if (t >= t0 && t <= t1) return v0 + (v1 - v0) * (t - t0) / (t1 - t0);
  }
  return 1;
}

// ============================================================
// 辅音合成（无过渡段，纯辅音）
// ============================================================
/**
 * 返回 { signal, consLen }
 * signal 只包含辅音（silence + burst + asp/main）
 * 完全不含"过渡到元音"的部分
 */
function synthConsonantPure(consType, sr, baseF0, useSilence) {
  const def = getConsDef(consType, useSilence);
  if (!baseF0 || baseF0 <= 0) baseF0 = DEFAULT_F0;

  const silenceLen = Math.floor(sr * (def.silenceMs || 0) / 1000);
  const seedBase = 12345 + consType.charCodeAt(0) * 999 + consType.length * 77;

  let totalLen, out;

  if (def.type === 'plosive') {
    // ===== 爆破/塞擦：silence + burst + asp =====
    const burstLen = Math.max(16, Math.floor(sr * def.burstMs / 1000));
    const aspLen = Math.max(32, Math.floor(sr * def.aspMs / 1000));
    totalLen = silenceLen + burstLen + aspLen;
    out = new Float32Array(totalLen);

    const noise = generateNoise(totalLen, seedBase);
    const pulse = def.voiced ? generatePulseTrain(totalLen, sr, baseF0) : null;

    // ---- burst 段 ----
    const burstIn = new Float32Array(burstLen);
    for (let i = 0; i < burstLen; i++) {
      const idx = silenceLen + i;
      burstIn[i] = noise[idx] * def.noiseAmt;
      if (pulse) burstIn[i] += pulse[idx] * (1 - def.noiseAmt) * 0.6;
    }
    const burstFilt = applyResonators(burstIn, def.burstReson, sr);
    for (let i = 0; i < burstLen; i++) {
      const t = i / burstLen;
      out[silenceLen + i] = burstFilt[i] * computeEnvelope('burst', t);
    }

    // ---- aspiration 段 ----
    const aspIn = new Float32Array(aspLen);
    for (let i = 0; i < aspLen; i++) {
      const idx = silenceLen + burstLen + i;
      aspIn[i] = noise[idx] * def.noiseAmt;
      if (pulse) aspIn[i] += pulse[idx] * (1 - def.noiseAmt) * 0.8;
    }
    const aspFilt = applyResonators(aspIn, def.aspReson, sr);
    for (let i = 0; i < aspLen; i++) {
      const t = i / aspLen;
      // asp 段：起始 0.55 → 末尾 0.35（不衰减到 0）
      const env = 0.55 - 0.20 * t;
      out[silenceLen + burstLen + i] = aspFilt[i] * env;
    }
  } else {
    // ===== 稳态：silence + main =====
    const mainLen = Math.max(64, Math.floor(sr * def.mainMs / 1000));
    totalLen = silenceLen + mainLen;
    out = new Float32Array(totalLen);

    const noise = generateNoise(totalLen, seedBase);
    const pulse = def.voiced ? generatePulseTrain(totalLen, sr, baseF0) : null;

    const src = new Float32Array(mainLen);
    for (let i = 0; i < mainLen; i++) {
      const idx = silenceLen + i;
      if (def.voiced) {
        src[i] = pulse[idx] * (1 - def.noiseAmt) + noise[idx] * def.noiseAmt * 0.7;
      } else {
        src[i] = noise[idx] * def.noiseAmt;
      }
    }

    const filtered = applyResonators(src, def.reson, sr);
    for (let i = 0; i < mainLen; i++) {
      const t = i / mainLen;
      out[silenceLen + i] = filtered[i] * computeEnvelope('fric', t);
    }
  }

  // ---- 归一化到 def.peak（只算有声部分，静默段保持 0）----
  let peak = 0;
  for (let i = silenceLen; i < totalLen; i++) {
    const a = Math.abs(out[i]);
    if (a > peak) peak = a;
  }
  if (peak < 1e-8) {
    // fallback：填噪声
    for (let i = silenceLen; i < totalLen; i++) {
      out[i] = (Math.random() * 2 - 1) * 0.2;
    }
    peak = 0.2;
  }
  const scale = def.peak / peak;
  for (let i = silenceLen; i < totalLen; i++) out[i] *= scale;

  return { signal: out, consLen: totalLen };
}

// ============================================================
// 拼接
// ============================================================
function concatCrossfade(a, b, sr, crossMs) {
  if (a.length === 0) return new Float32Array(b);
  if (b.length === 0) return new Float32Array(a);

  const fadeN = Math.min(
    Math.floor(sr * (crossMs || 3) / 1000),
    Math.floor(a.length / 4),
    Math.floor(b.length / 4)
  );

  if (fadeN < 4) {
    const out = new Float32Array(a.length + b.length);
    out.set(a, 0);
    out.set(b, a.length);
    return out;
  }

  const out = new Float32Array(a.length + b.length - fadeN);
  out.set(a.subarray(0, a.length - fadeN), 0);
  for (let i = 0; i < fadeN; i++) {
    const t = i / fadeN;
    const ga = Math.cos(t * Math.PI / 2);
    const gb = Math.sin(t * Math.PI / 2);
    out[a.length - fadeN + i] = a[a.length - fadeN + i] * ga + b[i] * gb;
  }
  out.set(b.subarray(fadeN), a.length);
  return out;
}

// ============================================================
// 静音切片
// ============================================================
function detectSegments(signal, sr, opts) {
  opts = opts || {};
  const silenceThresh = opts.silenceThresh || 0.015;
  const minSilenceMs = opts.minSilenceMs || 120;
  const minSegmentMs = opts.minSegmentMs || 60;
  const frameSize = Math.floor(sr * 0.025);
  const hop = Math.floor(frameSize / 2);
  const nFrames = Math.max(1, Math.floor((signal.length - frameSize) / hop) + 1);
  const energies = new Float32Array(nFrames);
  for (let i = 0; i < nFrames; i++) {
    let sum = 0;
    const s = i * hop;
    for (let j = 0; j < frameSize; j++) { const v = signal[s+j]||0; sum += v*v; }
    energies[i] = Math.sqrt(sum / frameSize);
  }
  const sorted = Array.from(energies).sort((a, b) => a - b);
  const p10 = sorted[Math.floor(nFrames * 0.1)] || 0;
  const p90 = sorted[Math.floor(nFrames * 0.9)] || 0.1;
  const threshold = Math.max(silenceThresh, p10 * 2 + (p90 - p10) * 0.04);
  const isSilent = new Uint8Array(nFrames);
  for (let i = 0; i < nFrames; i++) isSilent[i] = energies[i] < threshold ? 1 : 0;
  const minSilFrames = Math.floor(minSilenceMs * sr / 1000 / hop);
  const minSegFrames = Math.floor(minSegmentMs * sr / 1000 / hop);
  const segments = [];
  let i = 0;
  while (i < nFrames && isSilent[i]) i++;
  if (i >= nFrames) return [];
  let segStart = i;
  while (i < nFrames) {
    if (isSilent[i]) {
      let j = i;
      while (j < nFrames && isSilent[j]) j++;
      if (j - i >= minSilFrames) {
        if (i - segStart >= minSegFrames) segments.push({
          start: Math.max(0, segStart * hop - frameSize),
          end: Math.min(signal.length, i * hop),
        });
        segStart = j;
      }
      i = j;
    } else i++;
  }
  if (nFrames - segStart >= minSegFrames) segments.push({
    start: Math.max(0, segStart * hop - frameSize),
    end: signal.length,
  });
  return segments;
}

function splitCVBoundary(signal, sr) {
  const frameSize = Math.floor(sr * 0.005);
  const nFrames = Math.floor(signal.length / frameSize);
  if (nFrames < 4) return 0;
  const env = new Float32Array(nFrames);
  for (let i = 0; i < nFrames; i++) {
    let sum = 0;
    const s = i * frameSize;
    for (let j = 0; j < frameSize; j++) { const v = signal[s+j]||0; sum += v*v; }
    env[i] = Math.sqrt(sum / frameSize);
  }
  let peakIdx = 0, peakVal = 0;
  for (let i = 0; i < nFrames; i++) if (env[i] > peakVal) { peakVal = env[i]; peakIdx = i; }
  if (peakVal < 1e-6) return 0;
  let splitIdx = peakIdx;
  for (let i = peakIdx; i >= 0; i--) if (env[i] < peakVal * 0.55) { splitIdx = i; break; }
  return splitIdx * frameSize;
}

function detectPitchAutocorr(signal, sr, fmin, fmax) {
  fmin = fmin || 60; fmax = fmax || 800;
  const minLag = Math.floor(sr / fmax), maxLag = Math.floor(sr / fmin);
  const start = Math.floor(signal.length * 0.25);
  const len = Math.min(Math.floor(sr * 0.1), Math.floor(signal.length * 0.5));
  if (len < maxLag * 2) return 0;
  const buf = signal.subarray(start, start + len);
  let bestLag = 0, bestNCC = 0;
  for (let lag = minLag; lag <= maxLag; lag++) {
    let num = 0, den1 = 0, den2 = 0;
    for (let i = 0; i < len - lag; i++) {
      const a = buf[i], b = buf[i + lag];
      num += a * b; den1 += a * a; den2 += b * b;
    }
    const ncc = num / (Math.sqrt(den1 * den2) + EPS);
    if (ncc > bestNCC) { bestNCC = ncc; bestLag = lag; }
  }
  if (bestNCC < 0.3 || bestLag === 0) return 0;
  return sr / bestLag;
}

// ============================================================
// WAV
// ============================================================
function floatToWavBlob(samples, sr) {
  const numCh = 1, len = samples.length, bps = 2;
  const blockAlign = numCh * bps, dataSize = len * blockAlign;
  const buffer = new ArrayBuffer(44 + dataSize);
  const view = new DataView(buffer);
  function ws(off, s) { for (let i = 0; i < s.length; i++) view.setUint8(off + i, s.charCodeAt(i)); }
  ws(0, 'RIFF'); view.setUint32(4, 36 + dataSize, true); ws(8, 'WAVE'); ws(12, 'fmt ');
  view.setUint32(16, 16, true); view.setUint16(20, 1, true); view.setUint16(22, numCh, true);
  view.setUint32(24, sr, true); view.setUint32(28, sr * blockAlign, true);
  view.setUint16(32, blockAlign, true); view.setUint16(34, 16, true);
  ws(36, 'data'); view.setUint32(40, dataSize, true);
  let off = 44;
  for (let i = 0; i < len; i++) {
    let s = samples[i];
    if (!isFinite(s)) s = 0;
    if (s > 1) s = 1; else if (s < -1) s = -1;
    view.setInt16(off, s < 0 ? s * 0x8000 : s * 0x7FFF, true);
    off += 2;
  }
  return new Blob([buffer], { type: 'audio/wav' });
}

// ============================================================
// 工具
// ============================================================
function nearestVowel(target, available) {
  if (available.includes(target)) return target;
  const tgt = VOWEL_FORMANTS[target];
  if (!tgt) return available[0];
  let best = available[0], bestD = Infinity;
  for (const v of available) {
    const f = VOWEL_FORMANTS[v];
    if (!f) continue;
    const d = Math.abs(f[0].f - tgt[0].f) + Math.abs(f[1].f - tgt[1].f) + Math.abs(f[2].f - tgt[2].f);
    if (d < bestD) { bestD = d; best = v; }
  }
  return best;
}

function guessPhonemeFromFilename(name) {
  let base = name.replace(/\.[^.]+$/, '').trim();
  if (KANA_INDEX[base]) return KANA_INDEX[base];
  const lower = base.toLowerCase().replace(/[\s_\-]+/g, '');
  if (ROMAJI_INDEX[lower]) return ROMAJI_INDEX[lower];
  const noNum = lower.replace(/\d+$/, '');
  if (ROMAJI_INDEX[noNum]) return ROMAJI_INDEX[noNum];
  const kanaNoNum = base.replace(/\d+$/, '');
  if (KANA_INDEX[kanaNoNum]) return KANA_INDEX[kanaNoNum];
  return null;
}

// ============================================================
// 状态
// ============================================================
const state = { files: [], samples: {}, processed: {} };
const $ = (id) => document.getElementById(id);

const $dropZone = $('dropZone'), $fileInput = $('fileInput'), $fileList = $('fileList');
const $stats = $('stats'), $generateBtn = $('generateBtn'), $progressFill = $('progressFill');
const $log = $('log'), $downloadBtn = $('downloadBtn'), $previewCard = $('previewCard');
const $phonemeGrid = $('phonemeGrid'), $nowPlaying = $('nowPlaying');
const $previewAllBtn = $('previewAllBtn'), $stopPreviewBtn = $('stopPreviewBtn');

function log(msg, cls) {
  const d = document.createElement('div');
  if (cls) d.className = cls;
  d.textContent = '› ' + msg;
  $log.appendChild(d);
  $log.scrollTop = $log.scrollHeight;
}
function setProgress(p) { $progressFill.style.width = Math.min(100, Math.max(0, p)) + '%'; }

function updateStats() {
  if (state.files.length === 0) { $stats.style.display = 'none'; return; }
  $stats.style.display = 'grid';
  $('statFiles').textContent = state.files.length;
  $('statSamples').textContent = Object.keys(state.samples).length;
  let dur = 0;
  for (const f of state.files) dur += f.buffer.duration;
  $('statDur').textContent = dur.toFixed(1) + 's';
}

$dropZone.addEventListener('click', () => $fileInput.click());
$dropZone.addEventListener('dragover', (e) => { e.preventDefault(); $dropZone.classList.add('dragover'); });
$dropZone.addEventListener('dragleave', () => $dropZone.classList.remove('dragover'));
$dropZone.addEventListener('drop', (e) => { e.preventDefault(); $dropZone.classList.remove('dragover'); handleFiles(e.dataTransfer.files); });
$fileInput.addEventListener('change', () => handleFiles($fileInput.files));

async function handleFiles(fileList) {
  const ctx = new (window.AudioContext || window.webkitAudioContext)();
  let decoded = 0;
  for (const f of fileList) {
    if (!f.type.startsWith('audio/') && !f.name.match(/\.(wav|mp3|ogg|m4a|flac|aiff?)$/i)) continue;
    try {
      const ab = await f.arrayBuffer();
      const buf = await ctx.decodeAudioData(ab);
      state.files.push({ name: f.name, buffer: buf });
      decoded++;
    } catch (e) { log(`无法解码: ${f.name}`, 'warn'); }
  }
  await ctx.close();
  renderFileList(); updateStats(); updateGenerateBtn();
  if (decoded > 0) log(`已加载 ${decoded} 个文件`, 'ok');
}

function renderFileList() {
  $fileList.innerHTML = '';
  state.files.forEach((f, i) => {
    const div = document.createElement('div');
    div.className = 'file-item';
    div.innerHTML = `<span>🎵</span><span class="name"></span><span class="status">${f.buffer.duration.toFixed(2)}s · ${f.buffer.sampleRate}Hz</span><button class="del" data-i="${i}">×</button>`;
    div.querySelector('.name').textContent = f.name;
    div.querySelector('.del').addEventListener('click', () => removeFile(i));
    $fileList.appendChild(div);
  });
}

function removeFile(i) {
  state.files.splice(i, 1);
  renderFileList(); updateStats(); updateGenerateBtn();
}

function updateGenerateBtn() { $generateBtn.disabled = state.files.length === 0; }

// ============================================================
// 素材库
// ============================================================
async function buildLibrary(targetSR, trimVowel) {
  const samples = {};
  for (const f of state.files) {
    const mono = toMono(f.buffer);
    const rs = resampleLinear(mono, f.buffer.sampleRate, targetSR);
    const dcRemoved = removeDC(rs);
    const phoneme = guessPhonemeFromFilename(f.name);
    if (phoneme) {
      let sig = dcRemoved;
      if (trimVowel && phoneme.vowel && !phoneme.cons) sig = trimToMax(sig, targetSR, VOWEL_MAX_MS);
      samples[phoneme.romaji] = { signal: sig, source: f.name, phoneme };
      log(`识别: ${f.name} → ${phoneme.kana} (${phoneme.romaji})`);
    } else {
      const segments = detectSegments(dcRemoved, targetSR);
      log(`${f.name}: 检测到 ${segments.length} 段`);
      for (let i = 0; i < segments.length && i < PHONEMES.length; i++) {
        const s = segments[i], p = PHONEMES[i];
        let seg = new Float32Array(s.end - s.start);
        for (let j = 0; j < seg.length; j++) seg[j] = dcRemoved[s.start + j] || 0;
        seg = removeDC(seg);
        if (trimVowel && p.vowel && !p.cons) seg = trimToMax(seg, targetSR, VOWEL_MAX_MS);
        samples[p.romaji] = { signal: seg, source: `${f.name}[${i + 1}]`, phoneme: p };
      }
    }
  }
  return samples;
}

function extractConsonantBank(samples, sr) {
  const bank = {};
  for (const key of Object.keys(samples)) {
    const entry = samples[key];
    const p = entry.phoneme || ROMAJI_INDEX[key];
    if (!p || !p.cons || !p.vowel) continue;
    if (bank[p.cons]) continue;
    const s = entry.signal;
    if (s.length < sr * 0.05) continue;
    const splitSample = splitCVBoundary(s, sr);
    if (splitSample > sr * 0.01) {
      const cons = new Float32Array(splitSample);
      cons.set(s.subarray(0, splitSample));
      bank[p.cons] = cons;
    }
  }
  return bank;
}

// ============================================================
// 试听
// ============================================================
const preview = { ctx: null, currentSource: null, currentKey: null, queue: [], playing: false };

function ensurePreviewCtx() {
  if (!preview.ctx || preview.ctx.state === 'closed') preview.ctx = new (window.AudioContext || window.webkitAudioContext)();
  if (preview.ctx.state === 'suspended') preview.ctx.resume();
  return preview.ctx;
}

function stopPreview() {
  preview.queue = []; preview.playing = false;
  if (preview.currentSource) { try { preview.currentSource.stop(); } catch (e) {} preview.currentSource = null; }
  if (preview.currentKey) {
    const btn = document.querySelector(`.phoneme-btn[data-key="${preview.currentKey}"]`);
    if (btn) btn.classList.remove('playing');
    preview.currentKey = null;
  }
  $nowPlaying.textContent = '';
}

function playPhoneme(key, onEnded) {
  const entry = state.processed[key];
  if (!entry || entry.signal.length === 0) { if (onEnded) onEnded(); return; }
  const ctx = ensurePreviewCtx();
  const buffer = ctx.createBuffer(1, entry.signal.length, SR);
  buffer.copyToChannel(entry.signal, 0);
  const source = ctx.createBufferSource();
  source.buffer = buffer; source.connect(ctx.destination);
  if (preview.currentSource) { try { preview.currentSource.stop(); } catch (e) {} }
  if (preview.currentKey) {
    const btn = document.querySelector(`.phoneme-btn[data-key="${preview.currentKey}"]`);
    if (btn) btn.classList.remove('playing');
  }
  const btn = document.querySelector(`.phoneme-btn[data-key="${key}"]`);
  if (btn) btn.classList.add('playing');
  const p = ROMAJI_INDEX[key];
  $nowPlaying.textContent = '正在播放: ' + (p ? p.kana : key);
  preview.currentSource = source; preview.currentKey = key;
  source.onended = () => {
    if (preview.currentSource === source) {
      preview.currentSource = null;
      if (preview.currentKey) {
        const b = document.querySelector(`.phoneme-btn[data-key="${preview.currentKey}"]`);
        if (b) b.classList.remove('playing');
        preview.currentKey = null;
      }
      $nowPlaying.textContent = '';
    }
    if (onEnded) onEnded();
  };
  source.start();
}

function previewSingle(key) { stopPreview(); playPhoneme(key); }
function previewAll() {
  stopPreview();
  preview.queue = PHONEMES.map(p => p.romaji).filter(k => state.processed[k]);
  preview.playing = true;
  playNextInQueue();
}
function playNextInQueue() {
  if (!preview.playing || preview.queue.length === 0) { preview.playing = false; return; }
  const key = preview.queue.shift();
  playPhoneme(key, () => setTimeout(playNextInQueue, 120));
}

function buildPreviewGrid() {
  $phonemeGrid.innerHTML = '';
  for (const row of PHONEME_ROWS) {
    const keys = row.keys.filter(k => state.processed[k]);
    if (keys.length === 0) continue;
    const rowDiv = document.createElement('div');
    rowDiv.className = 'phoneme-row';
    const label = document.createElement('div');
    label.className = 'phoneme-row-label'; label.textContent = row.name;
    rowDiv.appendChild(label);
    const items = document.createElement('div');
    items.className = 'phoneme-row-items';
    for (const key of keys) {
      const p = ROMAJI_INDEX[key];
      const btn = document.createElement('button');
      btn.className = 'phoneme-btn';
      btn.dataset.key = key;
      btn.textContent = p ? p.kana : key;
      btn.addEventListener('click', () => previewSingle(key));
      items.appendChild(btn);
    }
    rowDiv.appendChild(items);
    $phonemeGrid.appendChild(rowDiv);
  }
}

$previewAllBtn.addEventListener('click', previewAll);
$stopPreviewBtn.addEventListener('click', stopPreview);

// ============================================================
// 主流程
// ============================================================
$generateBtn.addEventListener('click', async () => {
  $generateBtn.disabled = true;
  $downloadBtn.style.display = 'none';
  $previewCard.style.display = 'none';
  stopPreview();
  $log.innerHTML = '';
  setProgress(0);

  const autoVowel = $('autoVowel').checked;
  const autoCV = $('autoCV').checked;
  const sharpenFormant = $('sharpenFormant').checked;
  const useSilence = $('silenceBurst').checked;
  const trimVowel = $('trimVowel').checked;
  const doCleanup = $('cleanup').checked;
  const useSjis = $('useSjis').checked;

  try {
    if (useSjis) {
      log('加载 Shift-JIS 编码库...');
      const ok = await loadShiftJisLib();
      if (ok) log('Shift-JIS 库加载成功', 'ok');
      else log('Shift-JIS 库加载失败，降级 UTF-8', 'warn');
    }

    log('构建素材库...');
    state.samples = await buildLibrary(SR, trimVowel);
    updateStats();
    setProgress(8);

    const srcKeys = Object.keys(state.samples);
    if (srcKeys.length === 0) { log('错误: 素材库为空', 'err'); $generateBtn.disabled = false; return; }
    log(`素材库: ${srcKeys.length} 项`, 'ok');

    // 检测基频
    log('检测源基频...');
    let baseF0 = 0;
    const f0s = [];
    for (const v of VOWEL_LIST) {
      if (state.samples[v]) {
        const hz = detectPitchAutocorr(state.samples[v].signal, SR, 80, 600);
        if (hz > 0) f0s.push(hz);
      }
    }
    if (f0s.length > 0) {
      f0s.sort((a, b) => a - b);
      baseF0 = f0s[Math.floor(f0s.length / 2)];
      log(`基频 ≈ ${baseF0.toFixed(1)} Hz`);
    } else {
      baseF0 = DEFAULT_F0;
      log(`无法检测基频，使用 ${DEFAULT_F0} Hz`, 'warn');
    }
    setProgress(18);

    // 元音（含 LPC 补齐）
    const fullBank = {};
    const availableVowels = VOWEL_LIST.filter(v => state.samples[v]);

    if (autoVowel) {
      if (availableVowels.length === 0) { log('错误: 无元音素材', 'err'); $generateBtn.disabled = false; return; }
      for (const v of VOWEL_LIST) {
        if (state.samples[v]) {
          fullBank[v] = { signal: state.samples[v].signal, meta: { consLen: 0 } };
          continue;
        }
        const srcV = nearestVowel(v, availableVowels);
        log(`LPC 变换元音: ${srcV} → ${v}`);
        const transformed = vowelTransformLPC(state.samples[srcV].signal, SR, srcV, v, sharpenFormant);
        fullBank[v] = { signal: transformed, meta: { consLen: 0, morphed: `${srcV}→${v}` } };
      }
    } else {
      for (const v of VOWEL_LIST) if (state.samples[v]) {
        fullBank[v] = { signal: state.samples[v].signal, meta: { consLen: 0 } };
      }
    }

    // 已上传的其他音素
    for (const key of srcKeys) {
      if (fullBank[key]) continue;
      const p = state.samples[key].phoneme;
      if (!p) continue;
      if (!p.cons && p.vowel && VOWEL_LIST.includes(p.vowel) && p.romaji === p.vowel) continue;
      if (p.cons) {
        const splitSample = splitCVBoundary(state.samples[key].signal, SR);
        const hasCons = splitSample > SR * 0.01;
        fullBank[key] = {
          signal: state.samples[key].signal,
          meta: { consLen: hasCons ? splitSample : 0 },
        };
      } else {
        fullBank[key] = { signal: state.samples[key].signal, meta: { consLen: 0 } };
      }
    }
    setProgress(35);
    log(`元音/已上传: ${Object.keys(fullBank).length} 项`);

    // 元音归一化（这是修复"辅音被吃"的关键之一）
    log('元音归一化...');
    for (const v of VOWEL_LIST) {
      if (fullBank[v]) {
        fullBank[v].signal = normalizePeak(fullBank[v].signal, VOWEL_PEAK);
      }
    }

    // 辅音库
    log('提取辅音素材...');
    const consBank = extractConsonantBank(state.samples, SR);
    log(`从采样提取 ${Object.keys(consBank).length} 个辅音`);
    setProgress(45);

    // 合成缺失 CV
    if (autoCV) {
      log('合成缺失 CV 音节...');
      let synthesized = 0;
      const diagSamples = [];

      for (const p of PHONEMES) {
        if (fullBank[p.romaji]) continue;
        if (p.special === 'n') {
          const aBuf = fullBank['a'] || fullBank['u'] || fullBank['i'];
          if (aBuf) fullBank.n = { signal: new Float32Array(aBuf.signal), meta: { consLen: 0, nSubstitute: true } };
          continue;
        }
        if (!p.vowel) continue;
        const vowelEntry = fullBank[p.vowel];
        if (!vowelEntry) continue;

        if (p.cons) {
          let consSignal, consLen, isReal = false;

          if (consBank[p.cons]) {
            // 用真实提取的辅音
            consSignal = normalizePeak(consBank[p.cons], 0.6);
            consLen = consSignal.length;
            isReal = true;
          } else {
            // 合成辅音
            const result = synthConsonantPure(p.cons, SR, baseF0, useSilence);
            consSignal = result.signal;
            consLen = result.consLen;
            synthesized++;
          }

          if (consLen === 0) {
            fullBank[p.romaji] = { signal: new Float32Array(vowelEntry.signal), meta: { consLen: 0, fallback: true } };
            continue;
          }

          if (diagSamples.length < 6) {
            const peak = getPeak(consSignal);
            diagSamples.push(`${p.kana}[${p.cons}] 辅音 ${(consLen/SR*1000).toFixed(0)}ms, 峰值 ${peak.toFixed(2)}`);
          }

          // 3ms 拼接
          const combined = concatCrossfade(consSignal, vowelEntry.signal, SR, XFADE_MS);
          fullBank[p.romaji] = {
            signal: combined,
            meta: { consLen: consLen, consReal: isReal },
          };
        } else {
          fullBank[p.romaji] = { signal: new Float32Array(vowelEntry.signal), meta: { consLen: 0, vowelCopy: true } };
        }
      }
      log(`合成辅音音节 ${synthesized} 个`);
      if (diagSamples.length > 0) { log('诊断样本:', 'diag'); for (const s of diagSamples) log('  ' + s, 'diag'); }
    }
    setProgress(78);
    log(`音节库: ${Object.keys(fullBank).length} 项`);

    // 后处理：只做清理和防 clip，不强制归一化
    log('后处理...');
    const processed = {};
    let cnt = 0;
    const total = Object.keys(fullBank).length;
    for (const key of Object.keys(fullBank)) {
      const entry = fullBank[key];
      let sig = new Float32Array(entry.signal);
      if (doCleanup) { sig = removeDC(sig); sig = highpass(sig, SR, 80); }
      // 只在两端极短淡入淡出
      const n = sig.length;
      const fade = Math.min(Math.floor(SR * 0.002), Math.floor(n / 4));
      for (let i = 0; i < fade; i++) {
        const g = i / fade;
        sig[i] *= g;
        sig[n - 1 - i] *= g;
      }
      // 保护性归一化：只有峰值 > 0.95 才缩放
      const peak = getPeak(sig);
      if (peak > 0.95) {
        const g = 0.95 / peak;
        for (let i = 0; i < sig.length; i++) sig[i] *= g;
      }
      processed[key] = { signal: sig, meta: entry.meta };
      cnt++;
      setProgress(78 + (cnt / total) * 15);
    }
    state.processed = processed;
    setProgress(95);

    // oto.ini + WAV
    log('生成 oto.ini...');
    const otoLines = [], wavFiles = [];
    for (const p of PHONEMES) {
      const entry = processed[p.romaji];
      if (!entry) continue;
      const alias = p.kana, fileName = `${p.kana}.wav`;
      const totalMs = entry.signal.length / SR * 1000;
      let offsetMs, consMs, preMs, overlapMs, cutoffMs;
      if (entry.meta.consLen > 0) {
        consMs = entry.meta.consLen / SR * 1000;
        preMs = consMs + 5;
        overlapMs = Math.min(consMs * 0.4, 40);
        offsetMs = 0;
        cutoffMs = -(totalMs - preMs - 40);
        if (cutoffMs > -40) cutoffMs = -40;
      } else {
        offsetMs = 0; consMs = 0; preMs = 25; overlapMs = 15;
        cutoffMs = -(totalMs - preMs - 25);
        if (cutoffMs > -25) cutoffMs = -25;
      }
      otoLines.push(`${fileName}=${alias},${Math.round(offsetMs)},${Math.round(consMs)},${Math.round(cutoffMs)},${Math.round(preMs)},${Math.round(overlapMs)}`);
      const blob = floatToWavBlob(entry.signal, SR);
      wavFiles.push({ name: fileName, blob });
    }
    wavFiles.push({ name: 'oto.ini', blob: textToBlob(otoLines.join('\r\n') + '\r\n', useSjis) });

    const charTxt = [`name=無名音源`, `image=`, `author=`, `voice=無生物音源`, `web=`, `sample=`].join('\r\n') + '\r\n';
    wavFiles.push({ name: 'character.txt', blob: textToBlob(charTxt, useSjis) });
    const yamlTxt = [`name: 無名音源`, `singerType: utau`, `voice: 無生物音源`].join('\n') + '\n';
    wavFiles.push({ name: 'character.yaml', blob: new Blob([yamlTxt], { type: 'text/plain;charset=utf-8' }) });

    setProgress(97);

    log('打包 ZIP...');
    if (!window.JSZip) {
      await new Promise((resolve, reject) => {
        const s = document.createElement('script');
        s.src = 'https://cdnjs.cloudflare.com/ajax/libs/jszip/3.10.1/jszip.min.js';
        s.onload = resolve; s.onerror = () => reject(new Error('JSZip 加载失败'));
        document.head.appendChild(s);
      });
    }
    const zip = new JSZip();
    for (const wf of wavFiles) zip.file(wf.name, wf.blob);
    const zipBlob = await zip.generateAsync({ type: 'blob', compression: 'DEFLATE', compressionOptions: { level: 6 } });

    const url = URL.createObjectURL(zipBlob);
    $downloadBtn.style.display = 'block';
    $downloadBtn.onclick = () => {
      const a = document.createElement('a');
      a.href = url;
      a.download = 'utau_voicebank.zip';
      a.click();
    };

    log(`✅ 完成: ${wavFiles.length} 个文件`, 'ok');
    log(`音源包大小: ${(zipBlob.size / 1024).toFixed(1)} KB`);
    setProgress(100);

    buildPreviewGrid();
    $previewCard.style.display = 'block';
    log('试听已就绪', 'ok');
    $previewCard.scrollIntoView({ behavior: 'smooth', block: 'start' });
  } catch (err) {
    log(`❌ 错误: ${err.message}`, 'err');
    console.error(err);
  }

  $generateBtn.disabled = false;
});

loadShiftJisLib().then(ok => {
  if (ok) console.log('[UTAU] Shift-JIS 库已加载');
  else console.warn('[UTAU] Shift-JIS 库不可用');
});

updateGenerateBtn();
updateStats();
</script>
</body>
</html>
