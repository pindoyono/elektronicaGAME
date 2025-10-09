# 🚀 Panduan Deployment Electro Master

## 📋 Persiapan

Sebelum deploy, pastikan:
- ✅ Semua fitur sudah ditest
- ✅ Environment variables sudah disiapkan
- ✅ Firebase project sudah dibuat
- ✅ Build berhasil tanpa error

## 🔥 Deploy ke Firebase Hosting

### 1. Install Firebase CLI

```bash
npm install -g firebase-tools
```

### 2. Login ke Firebase

```bash
firebase login
```

### 3. Initialize Firebase

```bash
firebase init hosting
```

Pilih:
- Use existing project
- Public directory: `dist`
- Configure as SPA: `Yes`
- Set up automatic builds: `No`

### 4. Build Project

```bash
npm run build
```

### 5. Deploy

```bash
firebase deploy --only hosting
```

### 6. Set Environment Variables

Gunakan Firebase Functions config atau hard-code di build (tidak recommended untuk production).

---

## ▲ Deploy ke Vercel

### 1. Install Vercel CLI

```bash
npm i -g vercel
```

### 2. Deploy

```bash
vercel
```

### 3. Set Environment Variables

Di Vercel Dashboard:
1. Go to Project Settings
2. Environment Variables
3. Add semua variable dari `.env`

### 4. Redeploy (jika perlu)

```bash
vercel --prod
```

---

## 🌐 Deploy ke Netlify

### Method 1: Netlify CLI

```bash
# Install Netlify CLI
npm install -g netlify-cli

# Build
npm run build

# Deploy
netlify deploy --prod
```

### Method 2: Git Integration

1. Push ke GitHub
2. Connect repo di Netlify
3. Set build command: `npm run build`
4. Set publish directory: `dist`
5. Add environment variables
6. Deploy!

---

## 🔐 Environment Variables

Pastikan set semua variable ini di platform deployment:

```
VITE_FIREBASE_API_KEY=
VITE_FIREBASE_AUTH_DOMAIN=
VITE_FIREBASE_PROJECT_ID=
VITE_FIREBASE_STORAGE_BUCKET=
VITE_FIREBASE_MESSAGING_SENDER_ID=
VITE_FIREBASE_APP_ID=
```

---

## ✅ Post-Deployment Checklist

- [ ] Website accessible
- [ ] Login/Register works
- [ ] All modules load correctly
- [ ] XP system working
- [ ] Achievements unlock
- [ ] Responsive on mobile
- [ ] No console errors
- [ ] Firebase connection stable

---

## 🐛 Troubleshooting

### Build Error

```bash
rm -rf node_modules package-lock.json
npm install
npm run build
```

### Firebase Error

Check Firebase config di `.env` dan `src/config/firebase.js`

### Routing Error (404)

Pastikan `_redirects` atau rewrite rules sudah benar.

---

## 📊 Monitoring

### Firebase Analytics

```javascript
// src/config/firebase.js
import { getAnalytics } from 'firebase/analytics'
export const analytics = getAnalytics(app)
```

### Performance Monitoring

```bash
firebase deploy --only hosting,analytics
```

---

**Happy Deploying! 🚀**