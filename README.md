# 🏁 ETHICS RACE 🏁

> **Belajar Etika IT Sambil Berlomba** 🎮
>
> Game edukasi interaktif yang menggabungkan pembelajaran kode etik profesi dengan gamifikasi yang seru dan kompetitif!

---

## ✨ Fitur Utama

| 🎯 | 📊 | 🏆 |
|----|----|-----|
| **20 Pertanyaan Etika IT** | **8 Tim Hewan** | **3 Kondisi Menang** |
| Studi kasus praktis seputar etika profesi IT, security, dan tanggung jawab developer | Setiap tim memiliki emoji unik, warna, dan makna filosofis | Finish race, posisi terjauh, atau rock-paper-scissors tiebreaker |

---

## 🚀 Quick Start

### 1️⃣ **Buka File HTML**
Cukup buka `index.html` di browser Anda:
```bash
# Dengan live server di VS Code
# atau akses langsung via XAMPP
http://localhost/ethics%20game/index.html
```

### 2️⃣ **Mulai Bermain** 
- Klik tombol **"▶️ Mulai Permainan"**
- Jawab pertanyaan etika IT dengan memilih jawaban benar
- Setelah benar, pilih tim mana yang akan maju
- Tim pertama mencapai FINISH adalah **PEMENANG!** 🎉

---

## 🎮 Gameplay

### Arena Balapan
```
🐢 Tim Kura-Kura  ████░░░░░░░░  (Kesabaran & Kehati-hatian)
🐇 Tim Kelinci     ██████░░░░░░  (Kecepatan & Ketangkasan)
🐯 Tim Harimau     ██░░░░░░░░░░  (Kekuatan & Kepemimpinan)
🦁 Tim Singa       ██░░░░░░░░░░  (Keberanian & Keyakinan)
🦊 Tim Rubah       ████░░░░░░░░  (Kecerdikan & Strategi)
🐼 Tim Panda       ██░░░░░░░░░░  (Keseimbangan & Harmoni)
🐮 Tim Sapi        ██░░░░░░░░░░  (Kerja Keras & Dedikasi)
🦅 Tim Elang       ██░░░░░░░░░░  (Visi & Keunggulan)
```

### Mekanisme Permainan
1. **📖 Baca Pertanyaan** - Pertanyaan etika IT dengan 4 pilihan jawaban
2. **✅ Jawab Benar** - Tombol tim menjadi aktif (berwarna)
3. **🎯 Pilih Tim** - Klik tim mana yang menjawab dengan benar
4. **🚀 Tim Maju** - Tim bergerak 1 kotak menuju FINISH
5. **🏆 Menang** - Tim pertama mencapai 100% adalah juara!

---

## 📚 Topik Pertanyaan

Game ini mencakup **20 pertanyaan etika IT** mengenai:

- 🔒 **Security & Data Privacy** - Bug reporting, access control, data breach
- 📄 **Intellectual Property** - Lisensi software, copyright, plagiasi code
- 💼 **Professional Responsibility** - Honest communication, deadline, scope
- 👥 **Team Collaboration** - Code review, documentation, knowledge sharing
- 🎯 **Code Quality** - Testing, refactoring, optimization
- ⚠️ **Risk Management** - Backup, supply chain security, vendor management
- 🤖 **Ethical Tech** - AI bias, discrimination, user welfare

---

## 🎨 Design Highlights

### 🌈 Rainbow Gradient Background
Animasi warna yang bergerak indah (15 detik cycle) dengan 5 warna cerah:
- 🔴 Merah → 🔵 Cyan → 🟡 Kuning → 🟣 Ungu → 🟢 Hijau

### 📱 Responsive & Proyektor-Ready
- ✅ Dioptimasi untuk **desktop, tablet, dan mobile**
- ✅ **Text besar dan bold** untuk proyeksi di kelas
- ✅ **Kontras tinggi** untuk visibility maksimal
- ✅ **Emoji support** di semua browser modern

### ⚡ Smooth Animations
- Team progress bergerak smooth (0.5s transition)
- Winner icon bounce animation
- Modal fade-in & slide-in effects
- Button hover effects dengan scale & shadow

---

## 📁 Struktur File

```
ethics game/
├── 📄 index.html          ← Single file HTML+CSS+JavaScript (43 KB)
├── 📋 DOKUMENTASI.md      ← Dokumentasi lengkap (14 KB)
└── 📖 README.md           ← File ini
```

**💡 Keuntungan Single File:**
- Deployment super mudah (copy 1 file)
- Tidak ada masalah path eksternal
- Sempurna untuk classroom sharing

---

## 🛠️ Customization

### Ubah Pertanyaan
Edit array `questions` di dalam `index.html`:
```javascript
{
    text: "Pertanyaan baru Anda?",
    options: ["Jawaban A", "Jawaban B", "Jawaban C", "Jawaban D"],
    correctAnswer: 0  // Index jawaban benar (0-3)
}
```

### Ubah Tim
Edit array `teams` di dalam `index.html`:
```javascript
{ 
    name: "Nama Tim Baru", 
    icon: "🦁",  // Emoji apa saja
    color: "#FF6B6B",        // Warna tombol
    bgColor: "#FFEBEE"       // Warna latar
}
```

### Ubah Panjang Lintasan
```javascript
const TRACK_LENGTH = 5;  // Ubah ke jumlah kotak yang diinginkan
```

> 📝 **Untuk edit, buka `index.html` dengan text editor (VS Code, Notepad++, dll)**

---

## 💻 Requirements

| Kebutuhan | Spesifikasi |
|-----------|-------------|
| **Browser** | Chrome, Firefox, Safari, Edge (modern) |
| **JavaScript** | ES6+ support |
| **Server** | XAMPP, local server, atau buka langsung (file://) |
| **OS** | Windows, macOS, Linux |

---

## 🚀 Setup di XAMPP

### Step 1: Copy Folder
```bash
# Copy folder 'ethics game' ke:
C:\xampp\htdocs\
```

### Step 2: Start Apache
```bash
# Buka XAMPP Control Panel
# Klik "Start" pada Apache
```

### Step 3: Buka di Browser
```
http://localhost/ethics%20game/index.html
```

### Step 4: Enjoy! 🎉

---

## 🎯 Use Cases

### 👨‍🏫 Untuk Guru/Dosen
- ✅ Material pembelajaran interaktif untuk kelas IT
- ✅ Engagement tinggi dengan gamification
- ✅ Cocok untuk presentasi di kelas dengan proyektor
- ✅ Bisa digunakan untuk ice-breaker atau review

### 👨‍💻 Untuk Developer
- ✅ Portfolio project yang impressive
- ✅ Contoh implementasi game mechanics dengan vanilla JS
- ✅ Belajar state management, event handling, DOM manipulation
- ✅ Responsive design patterns

### 🏢 Untuk Training Perusahaan
- ✅ Training etika IT untuk karyawan baru
- ✅ Team building activity yang edukatif
- ✅ Kompetisi antar departemen/tim
- ✅ Fun learning environment

---

## 🐛 Troubleshooting

| ❌ Masalah | ✅ Solusi |
|-----------|----------|
| Halaman kosong | Clear cache (Ctrl+Shift+Del) → F5 |
| Tombol tidak responsif | Pastikan JS enabled di browser |
| Text terlalu kecil | Zoom browser 150-200% atau F11 (fullscreen) |
| Emoji tidak muncul | Update browser ke versi terbaru |
| File tidak loading | Gunakan live server / XAMPP (bukan file://) |

---

## 📊 Game Statistics

- 🎮 **20 Pertanyaan** etika IT yang challenging
- 👥 **8 Tim** dengan personality unik
- 🏁 **5 Kotak** per lintasan (customizable)
- ⏱️ **No Time Limit** - jawab dengan santai!
- 🎨 **Rainbow Design** - visual yang menarik

---

## 🎓 Pembelajaran

Game ini mengajarkan:

| Konsep | Deskripsi |
|--------|-----------|
| **Security First** | Melaporkan bug & vulnerability dengan proper channel |
| **Integrity** | Tidak plagiarisme code, respect IP |
| **Honesty** | Komunikasi jujur dengan client/boss tentang progress |
| **Quality** | Testing, documentation, code review penting |
| **Responsibility** | Setiap decision affects users dan team |

---

## 🌟 Highlights

### ✨ User Experience
- 🎯 **Intuitive** - Interface jelas, easy to understand
- ⚡ **Responsive** - Smooth animations & transitions
- 🎨 **Beautiful** - Modern design dengan gradient & colors
- ♿ **Accessible** - Large text, high contrast, emoji support

### 🏗️ Code Quality
- 📝 **Well Documented** - Comments di setiap function
- 🧹 **Clean Code** - Organized, readable, maintainable
- 🎯 **Modular** - Separated concerns (data, logic, UI)
- 🚀 **Optimized** - No external dependencies

---

## 📄 Lisensi

MIT License - Bebas gunakan & modifikasi untuk keperluan apapun! 📜

---

## 🤝 Contributing

Punya ide untuk improve game ini? Silakan:
1. **Fork** repository
2. **Edit** index.html atau DOKUMENTASI.md
3. **Test** perubahan Anda
4. **Submit Pull Request**

Kontribusi dipersilahkan! Baik itu:
- ➕ Pertanyaan etika IT baru
- 🎨 Design improvements
- 🐛 Bug fixes
- 📚 Documentation improvements

---

## 📞 Support

Ada pertanyaan atau bug? 

1. Check **DOKUMENTASI.md** untuk detailed guide
2. Open **browser console** (F12) untuk error messages
3. Review **inline comments** dalam index.html

---

## 🎉 Credits

| Role | Contribution |
|------|--------------|
| **Konsep** | Ethics education through gamification |
| **Development** | Vanilla HTML5, CSS3, JavaScript ES6+ |
| **Design** | Modern UI/UX dengan focus accessibility |
| **Testing** | Classroom ready & proyektor optimized |

---

## 🔄 Version History

| Versi | Tanggal | Highlights |
|-------|---------|-----------|
| **1.0** | 18 Dec 2025 | 🎉 Initial Release - Single File Version |

---

## 🎯 Roadmap (Future Ideas)

- 🔊 Sound effects & background music
- ⏱️ Timer challenge mode
- 📊 Leaderboard & score tracking
- 🌍 Multiplayer online support
- 🎓 Multiple difficulty levels
- 🏆 Achievement badges system
- 🌐 i18n (Internationalization)

---

<div align="center">

### Made with ❤️ for Ethical Tech Education

**Selamat bermain dan belajar! 🚀**

⭐ Jika suka, berikan star! ⭐

---

![ETHICS RACE](https://img.shields.io/badge/ETHICS-RACE-rainbow)
![HTML5](https://img.shields.io/badge/HTML5-E34C26?logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)
![License MIT](https://img.shields.io/badge/License-MIT-blue)

</div>
