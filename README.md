# SMS Latency Analyzer - Web App

Web app untuk menganalisis latensi SMS log

## Cara Pakai

### Local

1. Double-click `index.html` atau
2. Buka di browser: `file:///path/to/index.html`

### Local Server

```bash
# Python
python3 -m http.server 8000

# Node.js
npx serve

# Lalu buka http://localhost:8000
```

### Deploy ke Vercel

```bash
cd web-analyzer
vercel deploy
```

### Deploy ke Cloudflare Pages

```bash
cd web-analyzer
npx wrangler pages deploy
```

Atau drag & drop folder ini ke Cloudflare Pages dashboard

## Fitur

- 📝 Paste log SMS
- 🔍 Generate report latensi
- 📋 Copy report hasil
- 📅 Tanggal lengkap di output
- 🎨 Dark mode background hitam
- 📱 Responsive design
- ⚡ Client-side processing (JavaScript)

## Format Log

Format yang didukung:
```
[2026-02-13 07:44:32.394.528] trx_id=A001260213074416728936250 | STEP=finished
[2026-02-13 07:43:33.954.874] trx_id=A001260213074333679936250 | STEP=job_started
```

## Output Report

```
📌 SMS Timing Report
Durasi proses log (2026-02-13 07:43:33 - 2026-02-13 07:44:32) : ±58.4 detik

Detail per Transaksi:
1. A001260213074333679936250
   Start: 2026-02-13 07:43:33 → End: 2026-02-13 07:43:49
   Latensi: ±15.2 detik

Ringkasan Statistik:
Total transaksi : 2
Rata-rata       : ±15.3 detik
...
```
