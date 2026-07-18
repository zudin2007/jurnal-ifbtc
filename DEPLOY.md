# 🚀 Deploy Jurnal IFBTC ke Vercel

## Quick Start - Deploy ke Vercel (5 Menit)

### Step 1: Buka Vercel
Kunjungi: https://vercel.com/new

### Step 2: Connect GitHub
- Click "Continue with GitHub"
- Authorize Vercel app
- Select repo: **zudin2007/jurnal-ifbtc**

### Step 3: Configure Project
- **Project Name**: jurnal-ifbtc (atau custom)
- **Framework Preset**: Other (untuk static site)
- **Root Directory**: ./
- **Build Command**: (kosongkan)
- **Output Directory**: (kosongkan)

### Step 4: Deploy
Click **"Deploy"** dan tunggu selesai!

### Step 5: Custom Domain (Opsional)
Setelah deploy:
1. Buka dashboard project di Vercel
2. Klik **Settings** → **Domains**
3. Add custom domain (contoh: jurnal.domain.com)
4. Update DNS records sesuai petunjuk

---

## ✨ Fitur Setelah Deploy

✅ **Automatic Deployments**
- Setiap push ke `main` branch → auto-deploy
- Setiap PR → preview URL otomatis

✅ **Instant Rollback**
- Bisa kembali ke versi sebelumnya dalam 1 click

✅ **Global CDN**
- Website jalan cepat di mana saja di dunia
- SSL certificate otomatis

✅ **Analytics**
- Lihat traffic, performance, errors di dashboard

---

## 📊 Project Info

**Files:**
- `dashboard.html` - Main dashboard dengan React compiled
- `watchlist.html` - Watchlist dengan 33 saham (sortable)
- `stock-chart.html` - TradingView chart dengan RSI
- `home.html` - Landing page dengan theme toggle
- `index.html` - Redirect ke home/dashboard
- `vercel.json` - Vercel configuration

**Features:**
- 📈 Portfolio tracking (TH Value In, LKH, ISSI Midcap)
- 📋 Watchlist dengan 33 saham
- 📊 TradingView charts dengan RSI indicator
- 🌓 Dark/Light mode toggle
- 💾 LocalStorage untuk data persistence

---

## 🔧 Manual Deploy (CLI)

Jika lebih suka menggunakan CLI:

```bash
# 1. Install Vercel CLI
npm i -g vercel

# 2. Login
vercel login

# 3. Deploy
cd /home/user/jurnal-ifbtc
vercel

# 4. Follow prompts dan selesai!
```

---

## 📝 Environment Variables (Jika Ada)

Saat ini tidak ada env vars yang diperlukan. Semua data disimpan di:
- Browser localStorage (untuk entries/watchlist)
- GitHub Pages (file statis)

Jika di masa depan perlu API backend:
```bash
# Tambah di Vercel Dashboard → Settings → Environment Variables
REACT_APP_API_URL=https://api.example.com
```

---

## 🎯 Post-Deploy Checklist

Setelah deploy:
- [ ] Buka URL yang diberikan Vercel
- [ ] Test dashboard buka dengan baik
- [ ] Klik beberapa saham untuk verify charts
- [ ] Test watchlist sorting
- [ ] Test dark/light mode toggle
- [ ] Check di mobile/tablet

---

## 🆘 Troubleshooting

**Q: Site shows 404**
A: Vercel tidak detect static site dengan benar. Pastikan vercel.json ada dan benar.

**Q: Charts tidak muncul**
A: TradingView script perlu load dari CDN. Pastikan internet connection baik.

**Q: LocalStorage tidak work**
A: Browser security - only works di https. Vercel provides https automatically.

**Q: Deployment gagal**
A: Check Vercel dashboard logs. Usually ada error di output.

---

## 📚 Resources

- Vercel Docs: https://vercel.com/docs
- Static Site Hosting: https://vercel.com/docs/concepts/edge-functions/streaming/quickstart
- Custom Domains: https://vercel.com/docs/concepts/projects/domains

---

**Happy Deploying! 🎉**
