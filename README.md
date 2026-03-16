# Sirven — Portfolio

## Stack
- Astro 4 (static output)
- Vercel (hosting)
- CSS custom (no Tailwind, no framework)

## Local dev
```bash
npm install
npm run dev
```

## Deploy sur Vercel

### 1. Push sur GitHub
```bash
git init
git add .
git commit -m "init"
git remote add origin https://github.com/TON_USERNAME/sirven-site.git
git push -u origin main
```

### 2. Vercel
- Va sur vercel.com → New Project
- Importe le repo GitHub
- Framework : Astro (auto-détecté)
- Deploy

### 3. Domaine custom
- Dans Vercel → Settings → Domains
- Ajoute ton domaine (ex: sirven.dev)
- Pointe les DNS chez ton registrar vers Vercel

## À brancher
- `/contact` : remplace `https://calendar.google.com` par ton vrai lien Google Cal
- Décommente le `fetch()` dans `submitForm()` avec ton URL webhook n8n

## Structure
```
src/
  components/
    Nav.astro         — Navigation + toggle FR/EN
  layouts/
    Base.astro        — Layout global (cursor, grain, footer, reveal)
  pages/
    index.astro       — Page principale (hero, services, works, CTA)
    contact.astro     — Form multi-étapes (5 steps, budget conditionnel, upload)
  styles/
    global.css        — Variables, grain, cursor, reveal, container
```
