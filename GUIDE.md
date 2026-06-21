# ⚡ Compressly — Complete Beginner Guide
## Step-by-Step: Setup → Hosting → AdSense

---

## 📁 FOLDER STRUCTURE (aapka project)

```
compressly/
├── src/
│   ├── layouts/
│   │   └── Base.astro          ← Nav, Footer, SEO tags (sab pages yahan se aate hain)
│   ├── pages/
│   │   ├── index.astro         ← Homepage (Image Compressor)
│   │   ├── pdf-compress.astro  ← PDF Compressor page
│   │   ├── about.astro         ← About page
│   │   └── privacy.astro       ← Privacy Policy
│   └── styles/
│       └── global.css          ← Saara design/styling
├── public/
│   ├── favicon.svg             ← Website icon
│   ├── robots.txt              ← Google ke liye
│   └── sitemap.xml             ← Google indexing ke liye
├── astro.config.mjs            ← Astro settings
└── package.json                ← Dependencies
```

---

## 🛠️ STEP 1 — Computer Setup

### 1.1 Node.js install karo
👉 https://nodejs.org/en/download pe jao
- "LTS" version download karo (v20+)
- Install karo (Next, Next, Finish)
- Verify: terminal/cmd mein type karo: `node --version`
- Should show: `v20.x.x`

### 1.2 VS Code install karo (code editor)
👉 https://code.visualstudio.com/

---

## 📦 STEP 2 — Project Setup

### 2.1 Project folder banao
```bash
# Terminal/Command Prompt mein:
mkdir compressly
cd compressly
```

### 2.2 Saari files copy karo
Ye saari files jo maine banai hain unhe copy karo apne `compressly/` folder mein
(same folder structure maintain karna)

### 2.3 Dependencies install karo
```bash
npm install
```

### 2.4 Local pe chalao (test karo)
```bash
npm run dev
```
Browser mein open karo: http://localhost:4321

🎉 Agar website dikhti hai — aap ready hain!

---

## 🌐 STEP 3 — GitHub pe upload karo

### 3.1 GitHub account banao
👉 https://github.com/signup

### 3.2 New Repository banao
- GitHub pe click karo "New repository"
- Name: `compressly`
- Public rakhna
- Click "Create repository"

### 3.3 Git install karo (agar nahi hai)
👉 https://git-scm.com/downloads

### 3.4 Code upload karo
```bash
# Apne compressly folder mein ye commands chalao:
git init
git add .
git commit -m "Initial commit - Compressly"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/compressly.git
git push -u origin main
```
(YOUR_USERNAME = apna GitHub username)

---

## 🚀 STEP 4 — Vercel pe Deploy (FREE hosting)

### 4.1 Vercel account banao
👉 https://vercel.com/signup
- "Continue with GitHub" se login karo

### 4.2 Project import karo
1. Vercel dashboard pe "Add New Project" click karo
2. Apna `compressly` GitHub repo select karo
3. Framework: **Astro** (auto-detect hoga)
4. Click **Deploy**

### 4.3 Wait karo (1-2 minutes)
✅ Done! Aapki website live hai!
URL milega: `https://compressly-xyz.vercel.app`

### 4.4 Custom domain lagao (optional, baad mein)
- Vercel → Settings → Domains
- Apna domain add karo (GoDaddy/Namecheap se kharido)

---

## 🔄 STEP 5 — Future mein changes kaise karein

Jab bhi code change karo:
```bash
git add .
git commit -m "Changes kya kiye likho yahan"
git push
```
Vercel automatically deploy karega! ✨

---

## 💰 STEP 6 — Google AdSense lagao

### 6.1 AdSense ke liye apply karo
👉 https://adsense.google.com/start/
- Apna Gmail se sign up karo
- Website URL dalo: `https://compressly.vercel.app`
- Apply karo

⚠️ **Note:** AdSense approval ke liye website pe kuch content hona chahiye.
Approval mein 1-2 weeks lag sakte hain.

### 6.2 AdSense code milne ke baad

`src/layouts/Base.astro` file mein `<head>` tag ke andar add karo:
```html
<script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-XXXXXXXXXXXXXXXX" crossorigin="anonymous"></script>
```
(XXXXXXXXXXXXXXXX = apna Publisher ID)

### 6.3 Ad units activate karo

`src/pages/index.astro` mein ye section dhundo:
```html
<!-- Uncomment after AdSense approval: -->
```
Uske neeche ke code ko uncomment karo (<!-- --> hatao) aur apna `data-ad-client` aur `data-ad-slot` dalo.

---

## 🔍 STEP 7 — Google Search Console (SEO)

### 7.1 Setup karo
👉 https://search.google.com/search-console/
- "Add Property" → apna domain
- Verify karo (Vercel se HTML file method use karo)

### 7.2 Sitemap submit karo
- Search Console → Sitemaps
- Add: `https://compressly.vercel.app/sitemap.xml`

### 7.3 Wait karo
Google 1-4 weeks mein index karega.

---

## 📈 STEP 8 — Traffic badhane ke tips

1. **Title tags optimize karo** — keywords jaise "free image compressor", "compress JPG online"
2. **Speed** — Aapki site already fast hai (browser-based = no server lag)
3. **Social share** — Reddit r/webdev, Twitter, LinkedIn pe share karo
4. **Backlinks** — Doosri websites pe comment/contribute karo aur apni site ka link lagao

---

## 🐛 Common Problems & Solutions

| Problem | Solution |
|---------|----------|
| `npm install` error | Node.js version check karo: `node --version` (chahiye v18+) |
| `npm run dev` port busy | `npm run dev -- --port 4322` try karo |
| Vercel build fail | `npm run build` locally pehle test karo |
| PDF compress kaam nahi kar raha | Internet connection check karo (PDF.js CDN se load hota hai) |
| AdSense approved nahi | Privacy page add karo, thoda aur content likho, 2-4 weeks wait karo |

---

## 📞 Quick Commands Reference

```bash
npm run dev      # Local development server start
npm run build    # Production build test
git add .        # Saari changes stage karo
git commit -m "" # Commit with message
git push         # Vercel pe deploy
```

---

## ✅ Checklist

- [ ] Node.js installed
- [ ] Project folder setup
- [ ] `npm install` done
- [ ] Local test (npm run dev) ✓
- [ ] GitHub repo banaya
- [ ] Code pushed to GitHub
- [ ] Vercel pe deployed
- [ ] Live URL test kiya
- [ ] Google Search Console setup
- [ ] Sitemap submit kiya
- [ ] AdSense ke liye apply kiya
- [ ] AdSense code add kiya (after approval)

---

Made with ❤️ | Compressly
