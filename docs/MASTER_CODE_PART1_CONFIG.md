# 📦 MASTER CODE - PART 1: KONFIGURASI & SETUP
## Electro Master - Complete Configuration Files
**Created:** 2025-10-08 07:21:02 UTC  
**Developer:** pindoyono  
**Part:** 1 of 5  

---

## 📋 ISI PART 1 (5 FILES)

1. ✅ tailwind.config.js
2. ✅ postcss.config.js
3. ✅ .gitignore
4. ✅ .env.example
5. ✅ index.html

---

## 🔧 FILE 1: tailwind.config.js

**Path:** `tailwind.config.js` (di root folder)

**Cara membuat:**
1. Buka https://github.com/pindoyono/elektronicaGAME
2. Klik "Add file" → "Create new file"
3. Nama file: `tailwind.config.js`
4. Copy-paste kode di bawah ini:

```javascript
/** @type {import('tailwindcss').Config} */
export default {
  content: [
    "./index.html",
    "./src/**/*.{js,ts,jsx,tsx}",
  ],
  theme: {
    extend: {
      colors: {
        primary: {
          50: '#f0f4ff',
          100: '#e0e7ff',
          200: '#c7d2fe',
          300: '#a5b4fc',
          400: '#818cf8',
          500: '#667eea',
          600: '#5568d3',
          700: '#4c51bf',
          800: '#434190',
          900: '#3730a3',
        },
        secondary: {
          500: '#764ba2',
        },
        success: '#28a745',
        warning: '#ffc107',
        danger: '#dc3545',
        info: '#17a2b8',
      },
      fontFamily: {
        sans: ['Inter', 'system-ui', 'sans-serif'],
        mono: ['Fira Code', 'monospace'],
      },
      animation: {
        'pulse-slow': 'pulse 3s cubic-bezier(0.4, 0, 0.6, 1) infinite',
        'bounce-slow': 'bounce 2s infinite',
        'wiggle': 'wiggle 1s ease-in-out infinite',
        'slide-up': 'slideUp 0.3s ease-out',
        'slide-down': 'slideDown 0.3s ease-out',
      },
      keyframes: {
        wiggle: {
          '0%, 100%': { transform: 'rotate(-3deg)' },
          '50%': { transform: 'rotate(3deg)' },
        },
        slideUp: {
          '0%': { transform: 'translateY(100%)', opacity: 0 },
          '100%': { transform: 'translateY(0)', opacity: 1 },
        },
        slideDown: {
          '0%': { transform: 'translateY(-100%)', opacity: 0 },
          '100%': { transform: 'translateY(0)', opacity: 1 },
        },
      },
    },
  },
  plugins: [],
}
```

5. Klik "Commit changes"
6. ✅ Checklist: File tailwind.config.js sudah dibuat

---

## 🔧 FILE 2: postcss.config.js

**Path:** `postcss.config.js` (di root folder)

```javascript
export default {
  plugins: {
    tailwindcss: {},
    autoprefixer: {},
  },
};
```

✅ Checklist setelah dibuat

---

## 🔧 FILE 3: .gitignore

**Path:** `.gitignore` (di root folder)

```gitignore
# Dependencies
node_modules/
.pnp
.pnp.js

# Testing
coverage/

# Production
dist/
build/

# Misc
.DS_Store
.env
.env.local
.env.development.local
.env.test.local
.env.production.local

# Logs
npm-debug.log*
yarn-debug.log*
yarn-error.log*
pnpm-debug.log*

# Editor
.vscode/
.idea/
*.swp
*.swo
*~

# Firebase
.firebase/
.firebaserc
firebase-debug.log
firestore-debug.log

# Vite
.vite/
vite.config.js.timestamp-*
```

✅ Checklist setelah dibuat

---

## 🔧 FILE 4: .env.example

**Path:** `.env.example` (di root folder)

```env
# Firebase Configuration
# Copy file ini ke .env dan isi dengan Firebase config Anda

VITE_FIREBASE_API_KEY=your_api_key_here
VITE_FIREBASE_AUTH_DOMAIN=your_project.firebaseapp.com
VITE_FIREBASE_PROJECT_ID=your_project_id
VITE_FIREBASE_STORAGE_BUCKET=your_project.appspot.com
VITE_FIREBASE_MESSAGING_SENDER_ID=your_sender_id
VITE_FIREBASE_APP_ID=your_app_id
VITE_FIREBASE_MEASUREMENT_ID=your_measurement_id
```

✅ Checklist setelah dibuat

---

## 🔧 FILE 5: index.html

**Path:** `index.html` (di root folder)

```html
<!DOCTYPE html>
<html lang="id">
  <head>
    <meta charset="UTF-8" />
    <link rel="icon" type="image/svg+xml" href="/icons/logo.svg" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta name="description" content="Interactive Learning Platform for Electronics Education - Electro Master" />
    <meta name="keywords" content="electronics, education, SMK, gamification, learning platform" />
    <meta name="author" content="pindoyono" />
    
    <meta property="og:title" content="Electro Master - Interactive Electronics Learning" />
    <meta property="og:description" content="Platform pembelajaran interaktif untuk Elektronika Dasar SMK dengan gamifikasi" />
    <meta property="og:type" content="website" />
    
    <title>⚡ Electro Master - Learn Electronics Interactively</title>
  </head>
  <body>
    <div id="root"></div>
    <script type="module" src="/src/index.jsx"></script>
  </body>
</html>
```

✅ Checklist setelah dibuat

---

## ✅ CHECKLIST LENGKAP PART 1

Centang setelah file berhasil dibuat:

- [ ] tailwind.config.js
- [ ] postcss.config.js
- [ ] .gitignore
- [ ] .env.example
- [ ] index.html

**Progress Part 1:** 0/5 files

---

## ➡️ NEXT: PART 2

Setelah semua file Part 1 selesai, lanjut ke:
**PART 2: Core Application** (App.jsx, index.jsx, globals.css, Header, Sidebar)

---

**END OF PART 1**
