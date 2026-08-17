<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Kalkulator Ayam</title>
<style>
  * { box-sizing: border-box; }
  body {
    margin: 0;
    font-family: -apple-system, Segoe UI, Roboto, sans-serif;
    background: #f7f3e9;
    color: #2b2620;
    display: flex;
    justify-content: center;
    padding: 40px 16px;
  }
  .wrap { width: 100%; max-width: 420px; }
  h1 { font-size: 26px; margin: 0 0 4px; }
  .sub { color: #8a7f6c; font-size: 13px; margin-bottom: 20px; }
  .card {
    background: #fff;
    border: 1px solid #e4ddd0;
    border-radius: 16px;
    margin-bottom: 16px;
    overflow: hidden;
  }
  .card h2 {
    font-size: 13px;
    text-transform: uppercase;
    letter-spacing: .05em;
    padding: 18px 20px 4px;
    margin: 0;
  }
  .row {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 14px 20px;
    border-bottom: 1px solid #eee6d8;
  }
  .row:last-of-type { border-bottom: none; }
  .row .label b { display: block; }
  .row .label span { font-size: 12px; color: #8a7f6c; font-family: monospace; }
  .stepper { display: flex; align-items: center; gap: 10px; }
  .stepper button {
    width: 30px; height: 30px; border-radius: 50%;
    border: 1px solid #d8cfbc; background: #fff;
    font-size: 16px; cursor: pointer; line-height: 1;
  }
  .stepper button.plus { background: #3f6b4a; color: #fff; border: none; }
  .stepper input {
    width: 48px; text-align: center; font-family: monospace;
    font-size: 16px; font-weight: bold; border: none; background: transparent;
  }
  .total-bar {
    display: flex; justify-content: space-between; align-items: center;
    background: #2b2620; color: #fff; padding: 14px 20px;
  }
  .total-bar .num { font-family: monospace; font-size: 22px; font-weight: bold; }
  .stok-input {
    width: 70px; text-align: center; font-family: monospace;
    font-size: 16px; font-weight: bold; padding: 6px;
    border: 1px solid #d8cfbc; border-radius: 8px;
  }
  .status {
    margin: 0 20px 18px; padding: 12px 16px; border-radius: 10px;
    display: flex; justify-content: space-between; align-items: center;
    font-weight: 600; font-size: 14px;
  }
  .footnote { text-align: center; font-size: 11px; color: #a89d87; font-family: monospace; margin-top: 8px; }
</style>
</head>
<body>
<div class="wrap">
  <h1>Kalkulator Ayam</h1>
  <div class="sub">Hitung pemakaian harian & cocokkan dengan stok.</div>

  <!-- Kartu Pemakaian -->
  <div class="card">
    <h2>Pemakaian Hari Ini</h2>

    <div class="row">
      <div class="label"><b>Ekor Utuh</b><span>1 ekor</span></div>
      <div class="stepper">
        <button onclick="ubah('utuh', -1)">−</button>
        <input id="utuh" type="number" value="0" min="0" onchange="hitung()">
        <button class="plus" onclick="ubah('utuh', 1)">+</button>
      </div>
    </div>

    <div class="row">
      <div class="label"><b>Setengah</b><span>1/2 ekor</span></div>
      <div class="stepper">
        <button onclick="ubah('setengah', -1)">−</button>
        <input id="setengah" type="number" value="0" min="0" onchange="hitung()">
        <button class="plus" onclick="ubah('setengah', 1)">+</button>
      </div>
    </div>

    <div class="row">
      <div class="label"><b>Seperempat</b><span>1/4 ekor</span></div>
      <div class="stepper">
        <button onclick="ubah('seperempat', -1)">−</button>
        <input id="seperempat" type="number" value="0" min="0" onchange="hitung()">
        <button class="plus" onclick="ubah('seperempat', 1)">+</button>
      </div>
    </div>

    <div class="total-bar">
      <span>Total Pemakaian</span>
      <span class="num" id="totalPakai">0 ekor</span>
    </div>
  </div>

  <!-- Kartu Pembanding Stok -->
  <div class="card">
    <h2>Pembanding Stok Aktual</h2>

    <div class="row">
      <div class="label"><b>Stok Aktual</b><span>hasil hitung fisik (ekor)</span></div>
      <input id="stok" class="stok-input" type="number" value="0" min="0" step="0.25" onchange="hitung()">
    </div>

    <div class="row">
      <div class="label">Total pemakaian</div>
      <span id="cekPakai" style="font-family:monospace">0 ekor</span>
    </div>
    <div class="row">
      <div class="label">Stok aktual</div>
      <span id="cekStok" style="font-family:monospace">0 ekor</span>
    </div>

    <div class="status" id="statusBox">
      <span id="statusLabel">Pas / cocok</span>
      <span id="statusNum">0 ekor</span>
    </div>
  </div>

  <div class="footnote">selisih + = sisa · selisih − = kurang</div>
</div>

<script>
  function ubah(id, delta) {
    const el = document.getElementById(id);
    el.value = Math.max(0, Number(el.value) + delta);
    hitung();
  }

  function fmt(n) {
    const r = Math.round(n * 100) / 100;
    return Number.isInteger(r) ? r.toString() : r.toFixed(2).replace(/0+$/, '').replace(/\.$/, '');
  }

  function hitung() {
    const utuh = Number(document.getElementById('utuh').value) || 0;
    const setengah = Number(document.getElementById('setengah').value) || 0;
    const seperempat = Number(document.getElementById('seperempat').value) || 0;
    const stok = Number(document.getElementById('stok').value) || 0;

    const totalPakai = utuh * 1 + setengah * 0.5 + seperempat * 0.25;
    const selisih = stok - totalPakai;

    document.getElementById('totalPakai').textContent = fmt(totalPakai) + ' ekor';
    document.getElementById('cekPakai').textContent = fmt(totalPakai) + ' ekor';
    document.getElementById('cekStok').textContent = fmt(stok) + ' ekor';

    const box = document.getElementById('statusBox');
    const label = document.getElementById('statusLabel');
    const num = document.getElementById('statusNum');

    let bg = '#e9f2ea', color = '#3f6b4a', txt = 'Pas / cocok';
    if (selisih > 0.001) { bg = '#f7eed8'; color = '#a3781f'; txt = 'Sisa stok'; }
    if (selisih < -0.001) { bg = '#f8e6e0'; color = '#a8402f'; txt = 'Kurang / lebih pakai'; }

    box.style.background = bg;
    label.style.color = color;
    num.style.color = color;
    label.textContent = txt;
    num.textContent = (selisih > 0 ? '+' : '') + fmt(selisih) + ' ekor';
  }

  hitung();
</script>
</body>
</html>
