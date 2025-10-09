# 🎮 Electro Master - Interactive Electronics Learning Platform

![Electro Master](https://img.shields.io/badge/Version-1.0.0-blue)
![React](https://img.shields.io/badge/React-18.2.0-61dafb)
![Vite](https://img.shields.io/badge/Vite-5.0.8-646cff)
![Firebase](https://img.shields.io/badge/Firebase-10.7.1-orange)

Platform pembelajaran elektronika interaktif yang dirancang untuk mengajarkan konsep-konsep elektronika melalui pengalaman gamifikasi yang menarik.

## ✨ Fitur Utama

### 🎯 6 Modul Pembelajaran Interaktif

1. **Symbol Quest** - Pelajari simbol-simbol komponen elektronika
2. **Circuit Builder** - Bangun rangkaian elektronika virtual
3. **Truth Table** - Latihan tabel kebenaran logika digital
4. **Virtual Lab** - Laboratorium virtual untuk eksperimen
5. **Quiz Battle** - Uji pengetahuan dengan kuis interaktif
6. **Dashboard** - Pantau progress dan pencapaian

### 🎮 Sistem Gamifikasi

- **XP & Level System** - Dapatkan XP dan naik level
- **Achievements** - Buka berbagai pencapaian
- **Streak System** - Pertahankan streak belajar harian
- **Leaderboard** - Bandingkan progress dengan pengguna lain

### 🔐 Fitur Keamanan

- Firebase Authentication
- Protected Routes
- Secure user data storage

## 🚀 Quick Start

### Prerequisites

- Node.js (v16 atau lebih tinggi)
- npm atau yarn
- Firebase account (untuk authentication)

### Instalasi

1. **Clone repository**
   ```bash
   git clone https://github.com/pindoyono/elektronicaGAME.git
   cd elektronicaGAME
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Setup Firebase**
   
   - Buat project di [Firebase Console](https://console.firebase.google.com)
   - Enable Authentication (Email/Password)
   - Copy konfigurasi Firebase Anda

4. **Setup Environment Variables**
   
   Buat file `.env` dari `.env.example`:
   ```bash
   cp .env.example .env
   ```
   
   Edit `.env` dan isi dengan konfigurasi Firebase Anda:
   ```
   VITE_FIREBASE_API_KEY=your-api-key
   VITE_FIREBASE_AUTH_DOMAIN=your-auth-domain
   VITE_FIREBASE_PROJECT_ID=your-project-id
   VITE_FIREBASE_STORAGE_BUCKET=your-storage-bucket
   VITE_FIREBASE_MESSAGING_SENDER_ID=your-sender-id
   VITE_FIREBASE_APP_ID=your-app-id
   ```

5. **Jalankan Development Server**
   ```bash
   npm run dev
   ```

6. **Buka browser**
   ```
   http://localhost:3000
   ```

## 📁 Struktur Project

```
elektronicaGAME/
├── public/              # Static assets
├── src/
│   ├── assets/         # Images, icons
│   ├── components/     # React components
│   │   ├── Login.jsx
│   │   ├── Register.jsx
│   │   └── Navbar.jsx
│   ├── config/         # Configuration files
│   │   └── firebase.js
│   ├── hooks/          # Custom React hooks
│   │   └── useAuth.js
│   ├── pages/          # Page components
│   │   ├── Dashboard.jsx
│   │   ├── SymbolQuest.jsx
│   │   ├── CircuitBuilder.jsx
│   │   ├── TruthTable.jsx
│   │   ├── VirtualLab.jsx
│   │   └── QuizBattle.jsx
│   ├── store/          # Zustand state management
│   │   ├── authStore.js
│   │   └── gameStore.js
│   ├── App.jsx         # Main app component
│   ├── main.jsx        # Entry point
│   └── index.css       # Global styles
├── docs/               # Documentation
├── .env.example        # Environment variables template
├── .gitignore
├── index.html
├── package.json
├── vite.config.js
├── tailwind.config.js
└── README.md
```

## 🛠️ Tech Stack

- **Frontend Framework**: React 18.2
- **Build Tool**: Vite 5.0
- **Styling**: Tailwind CSS 3.3
- **State Management**: Zustand 4.4
- **Authentication**: Firebase Auth 10.7
- **Database**: Firebase Firestore
- **Routing**: React Router DOM 6.20
- **Icons**: Lucide React

## 📚 Modul Pembelajaran

### 1. Symbol Quest
Pelajari dan kenali berbagai simbol komponen elektronika:
- Resistor
- Kapasitor
- Dioda
- LED
- Transistor
- Dan lainnya

**Fitur:**
- 10+ pertanyaan interaktif
- Penjelasan untuk setiap jawaban
- Sistem scoring berbasis waktu

### 2. Circuit Builder
Bangun rangkaian elektronika virtual:
- Rangkaian LED sederhana
- Rangkaian dengan switch
- Rangkaian RC

**Fitur:**
- Drag & drop components
- Real-time circuit validation
- Challenge-based learning

### 3. Truth Table
Latihan tabel kebenaran untuk gerbang logika:
- AND, OR, NOT
- NAND, NOR, XOR

**Fitur:**
- Interactive truth tables
- Instant feedback
- Progressive difficulty

### 4. Virtual Lab
Laboratorium virtual untuk eksperimen:
- Hukum Ohm
- Rangkaian Seri/Paralel
- Perhitungan Daya

**Fitur:**
- Real-time calculations
- Visual circuit simulation
- Measurement displays

### 5. Quiz Battle
Uji pengetahuan dengan kuis interaktif:
- 15+ pertanyaan
- Multiple categories
- Time-based scoring

**Fitur:**
- Timed questions (30s each)
- Time bonus scoring
- Performance statistics

### 6. Dashboard
Pantau progress pembelajaran Anda:
- Total XP dan Level
- Module completion
- Achievements unlocked
- Daily streak

## 🎯 Sistem Gamifikasi

### XP & Leveling
- Dapatkan XP dari setiap aktivitas
- 100 XP = 1 Level
- Level up rewards

### Achievements
- Level milestones
- Streak achievements
- Perfect scores
- Module completion

### Streak System
- Daily login tracking
- 7-day streak badge
- 30-day streak badge
- Streak recovery grace period

## 🚀 Deployment

### Deploy ke Vercel

1. Install Vercel CLI:
   ```bash
   npm i -g vercel
   ```

2. Deploy:
   ```bash
   vercel
   ```

3. Set environment variables di Vercel Dashboard

### Deploy ke Netlify

1. Build project:
   ```bash
   npm run build
   ```

2. Deploy `dist` folder ke Netlify

3. Set environment variables di Netlify Dashboard

### Deploy ke Firebase Hosting

1. Install Firebase CLI:
   ```bash
   npm install -g firebase-tools
   ```

2. Login:
   ```bash
   firebase login
   ```

3. Initialize:
   ```bash
   firebase init hosting
   ```

4. Build & Deploy:
   ```bash
   npm run build
   firebase deploy
   ```

## 📝 Development Tips

### Menambah Pertanyaan Quiz

Edit file `src/pages/QuizBattle.jsx`:

```javascript
const questions = [
  {
    id: 1,
    question: 'Pertanyaan Anda?',
    options: ['A', 'B', 'C', 'D'],
    correct: 0, // index jawaban benar
    category: 'Kategori',
    points: 100
  },
  // tambah pertanyaan lainnya...
]
```

### Menambah Achievement

Edit file `src/store/gameStore.js`:

```javascript
unlockAchievement('achievement_id', 'Achievement Name')
```

### Mengubah Tema Warna

Edit file `tailwind.config.js`:

```javascript
colors: {
  primary: {
    // customize colors
  }
}
```

## 🧪 Testing

### Manual Testing
```bash
npm run dev
```

### Build Testing
```bash
npm run build
npm run preview
```

## 📊 RPP Curriculum Integration

Modul pembelajaran disesuaikan dengan kurikulum:

- **KD 3.1**: Memahami komponen elektronika dasar
- **KD 3.2**: Menganalisis rangkaian elektronika
- **KD 3.3**: Memahami logika digital
- **KD 4.1**: Merancang rangkaian elektronika sederhana

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License.

## 👨‍💻 Author

**Pindoyono**
- GitHub: [@pindoyono](https://github.com/pindoyono)

## 🙏 Acknowledgments

- React Team for the amazing framework
- Vite for blazing fast build tool
- Firebase for backend services
- Tailwind CSS for utility-first CSS
- Lucide for beautiful icons

## 📞 Support

Jika ada pertanyaan atau masalah:
- Open an issue
- Contact: [Your Email]

---

**⚡ Happy Learning! ⚡**