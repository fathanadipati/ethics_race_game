# DOKUMENTASI PROYEK: ETHICS RACE

## 📋 Ringkasan Proyek

**ETHICS RACE** adalah game edukasi interaktif berbasis web yang dirancang untuk mengajarkan etika profesi di bidang Teknologi Informasi (IT) dan Programming. Game ini menggabungkan elemen pembelajaran dengan gamifikasi yang menyenangkan, di mana 8 tim dengan mascot hewan berlomba menjawab pertanyaan etika untuk mencapai garis finish.

---

## 🎯 Tujuan Proyek

1. Menciptakan platform pembelajaran etika IT yang interaktif dan engaging
2. Memudahkan peserta memahami kode etik profesi IT melalui studi kasus praktis
3. Memberikan pengalaman belajar yang kompetitif dan menyenangkan
4. Dapat digunakan untuk presentasi dan pembelajaran di ruang kelas dengan proyektor

---

## ⚙️ Teknologi yang Digunakan

- **Frontend**: HTML5, CSS3, JavaScript ES6+ (Vanilla - tanpa framework)
- **Arsitektur**: Event-driven game state machine
- **Deployment**: Web server (XAMPP/localhost)
- **Browser Compatibility**: Chrome, Firefox, Safari, Edge

---

## 📁 Struktur File

```
ethics game/
├── index.html          # File utama (HTML + CSS + JavaScript inline)
├── DOKUMENTASI.md      # File dokumentasi ini
```

**Catatan**: Semua kode CSS dan JavaScript sudah di-embed langsung dalam `index.html` untuk simplifikasi deployment.

---

## 🎮 Fitur Utama

### 1. **Layar Informasi Awal**
- Menampilkan panduan cara bermain
- Daftar 8 tim dengan emoji dan deskripsi makna setiap tim
- Tombol "Mulai Permainan" untuk memulai

### 2. **Arena Balapan**
- 8 jalur balapan horizontal (satu per tim)
- Garis START (hijau) dan FINISH (merah) dengan label vertikal
- Setiap tim dimulai dari posisi 0% dan harus mencapai 100% (5 kotak)
- Emoji tim bergerak smooth ke kanan seiring menjawab pertanyaan dengan benar

### 3. **Panel Pertanyaan**
- Pertanyaan ditampilkan di tengah dengan font besar (1.35em)
- 4 pilihan jawaban dalam layout grid horizontal
- Setiap pilihan memiliki huruf (A, B, C, D) besar di atas teks jawaban
- Progress bar menunjukkan pertanyaan ke berapa dari 20
- Tombol "Pertanyaan Berikutnya" muncul jika jawaban salah

### 4. **Panel Kontrol Tim**
- 8 tombol dengan emoji tim (tidak ada teks nama)
- Emoji diperbesar signifikan (2.5em) untuk terlihat dari jauh
- Layout grid horizontal (8 kolom)
- Tombol disabled sampai jawaban benar
- Tombol yang diklik akan membuat tim tersebut maju 1 kotak

### 5. **Modal Pemenang**
- Menampilkan header berbeda untuk kondisi berbeda:
  - "🎉 PEMENANG! 🎉" untuk kemenangan normal
  - "⚖️ TIEBREAKER ⚖️" untuk hasil seri
- Menampilkan emoji pemenang (bouncing animation)
- Pesan spesifik sesuai kondisi menang
- Tombol "Mainkan Ulang" untuk memulai game baru

### 6. **Fitur Navigasi**
- Tombol "← Kembali" di layar balapan untuk kembali ke menu
- Reset otomatis game state saat kembali

---

## 📊 Detail Game Mechanics

### **20 Pertanyaan Etika IT**
Pertanyaan mencakup topik:
- Bug reporting & security
- Intellectual property & lisensi software
- Code quality & documentation
- Professional responsibility
- Data privacy & access control
- Honest communication dengan client/boss
- Deadline & scope management
- Team collaboration & code review
- Supply chain security
- AI/ML bias & ethics

### **8 Tim Peserta**
1. 🐢 Tim Kura-Kura (Hijau - Kesabaran & Kehati-hatian)
2. 🐇 Tim Kelinci (Orange - Kecepatan & Ketangkasan)
3. 🐯 Tim Harimau (Merah - Kekuatan & Kepemimpinan)
4. 🦁 Tim Singa (Beige - Keberanian & Keyakinan)
5. 🦊 Tim Rubah (Pink - Kecerdikan & Strategi)
6. 🐼 Tim Panda (Ungu - Keseimbangan & Harmoni)
7. 🐮 Tim Sapi (Abu-abu - Kerja Keras & Dedikasi)
8. 🦅 Tim Elang (Hijau Muda - Visi & Keunggulan)

### **Mekanisme Permainan**

1. **Menjawab Pertanyaan**
   - User membaca pertanyaan dengan 4 pilihan jawaban
   - Klik salah satu pilihan A, B, C, atau D
   - Visual feedback: hijau untuk benar, merah untuk salah

2. **Jawaban Benar**
   - Tombol pilihan berubah hijau
   - Tombol-tombol tim menjadi aktif (opacity 1, cursor pointer)
   - User harus memilih tim mana yang menjawab dengan benar

3. **Jawaban Salah**
   - Tombol pilihan berubah merah
   - Tombol "Pertanyaan Berikutnya" muncul
   - User bisa lanjut ke pertanyaan berikutnya tanpa ada tim yang maju

4. **Pergerakan Tim**
   - Setelah tim dipilih, emoji tim bergerak 1 kotak (20% dari 5 kotak = dari 0% ke 20%)
   - Transisi smooth selama 0.5 detik
   - Pertanyaan berikutnya dimuat otomatis

5. **Kondisi Menang**
   - **Finish**: Tim pertama mencapai 100% (5 kotak penuh)
   - **Posisi Terjauh**: Jika tidak ada yang finish setelah 20 pertanyaan, tim dengan posisi terjauh menang
   - **Tiebreaker**: Jika ada 2+ tim seri di posisi terjauh, lakukan Rock-Paper-Scissors

---

## 🎨 Design & UI/UX

### **Color Scheme**
- **Header**: Rainbow gradient (merah → cyan → kuning → ungu → hijau) dengan animasi 15 detik
- **Tim Colors**: 8 warna unik untuk setiap tim dengan background pastel
- **Buttons**: Gradient biru ungu untuk tombol aksi utama
- **Tombol Kembali**: Gradient abu-abu

### **Typography**
- **Font Family**: Segoe UI, Tahoma, Geneva, Verdana, sans-serif
- **Pertanyaan**: 1.35em, bold, center-aligned, line-height 1.6
- **Jawaban**: 1.15em, center-aligned, line-height 1.4
- **Huruf Opsi**: 2em, bold, black color

### **Responsive Design**
- Container max-width: 100vw, max-height: 100vh
- Padding adaptif: 8px untuk mobile, lebih besar untuk desktop
- Flex layout untuk responsive pada berbagai ukuran layar
- Teroptimasi untuk proyektor (text besar, kontras tinggi)

### **Animasi**
- **Rainbow Background**: 15 detik cycle
- **Track Movement**: 0.5 detik smooth transition
- **Winner Icon**: Bounce animation
- **Modal**: Fade-in untuk background, slide-in untuk content
- **Button Hover**: Scale 1.1 dengan shadow

---

## 📱 Responsive Breakpoints

- **Tablet (≤768px)**:
  - Header h1 font size: 1.8em
  - Progress bar width: 100%
  - Answer buttons grid: 2 kolom
  - Track cell: 1.4em
  - Modal margin: 20px

---

## 🔧 Variabel Konfigurasi

Semua kode konfigurasi berada di dalam `index.html` di tag `<script>`:

```javascript
const TOTAL_QUESTIONS = 20;  // Jumlah pertanyaan
const TRACK_LENGTH = 5;      // Panjang trek (kotak yang harus ditempuh)
```

### Mengubah Pertanyaan
Edit array `questions` di dalam `<script>` di `index.html`. Format:
```javascript
{
    text: "Pertanyaan di sini?",
    options: [
        "Pilihan A",
        "Pilihan B",
        "Pilihan C",
        "Pilihan D"
    ],
    correctAnswer: 0  // Index jawaban benar (0-3)
}
```

### Mengubah Tim
Edit array `teams` di dalam `<script>` di `index.html`. Format:
```javascript
{ 
    name: "Nama Tim", 
    icon: "🐢", 
    color: "#warna", 
    bgColor: "#warna-background" 
}
```

### Mengubah Panjang Trek
Ubah nilai `TRACK_LENGTH` di dalam `<script>` di `index.html` (default: 5)

---

## 📄 Struktur File Detail

### File: `index.html`

File ini mengandung:
1. **HTML Structure** - Kerangka halaman dengan:
   - Layar info awal
   - Panel pertanyaan
   - Arena balapan
   - Panel kontrol tim
   - Modal pemenang

2. **CSS Styling** - Di dalam tag `<style>`:
   - Layout responsive
   - Color scheme dan animasi
   - Styling untuk semua komponen UI
   - Media queries untuk berbagai ukuran layar

3. **JavaScript Logic** - Di dalam tag `<script>`:
   - Data pertanyaan (20 soal etika IT)
   - Data tim (8 tim dengan emoji)
   - Fungsi game mechanics
   - Event handlers
   - State management

**Total size**: Single file HTML dengan embedded CSS dan JavaScript

---

## 🔍 Navigasi Kode di index.html

| Bagian | Lokasi | Fungsi |
|--------|--------|--------|
| **Structure** | `<body>` - `</body>` | Kerangka halaman utama |
| **CSS** | `<style>` di `<head>` | Styling semua elemen |
| **Game Data** | `<script>` - `const questions = [...]` | 20 pertanyaan etika |
| **Game Data** | `<script>` - `const teams = [...]` | 8 tim peserta |
| **Utility Functions** | `<script>` - `shuffleArray()`, `prepareQuestion()` | Fungsi helper |
| **Game State** | `<script>` - `let gameState = {...}` | Status game saat ini |
| **Init Functions** | `<script>` - `startGame()`, `initGame()` | Inisialisasi game |
| **Render Functions** | `<script>` - `renderTrack()`, `renderAnswerButtons()` | Menggambar UI |
| **Game Mechanics** | `<script>` - `handleAnswerOption()`, `handleTeamAnswer()` | Logika game |
| **Win Condition** | `<script>` - `determineWinnerByPosition()`, `endGame()` | Penentuan pemenang |

---

## 📈 Game Flow Diagram
│   Daftar Tim)       │
└──────────┬──────────┘
           │
    ┌──────┴──────────────────┐
    │                         │
    ▼                         │
┌──────────────┐              │
│ Klik Mulai   │              │
│ Permainan    │              │
└──────┬───────┘              │
       │                      │
       ▼                      │
┌──────────────────────┐      │
│ Tampilkan Pertanyaan │      │
│ + 4 Pilihan Jawaban  │      │
└──────────┬───────────┘      │
           │                  │
    ┌──────┴───────┐          │
    │              │          │
    ▼              ▼          │
┌────────┐  ┌──────────┐      │
│ Jawab  │  │ Jawab    │      │
│ Benar  │  │ Salah    │      │
└───┬────┘  └──┬───────┘      │
    │         │               │
    ▼         ▼               │
┌─────────┐ ┌──────────────┐  │
│ Pilih   │ │ Next Question│  │
│ Tim     │ │ Button       │  │
└────┬────┘ └──────┬───────┘  │
     │             │          │
     ▼             │          │
┌──────────┐       │          │
│ Tim Maju │       │          │
│ 1 Kotak  │       │          │
└────┬─────┘       │          │
     │             │          │
     ├─────────────┘          │
     │                        │
     ▼                        │
┌──────────────┐              │
│ Cek Kondisi  │              │
│ Menang?      │              │
└────┬─────────┘              │
     │                        │
  ┌──┼──┬─────────────┐       │
  │  │  │             │       │
  ▼  ▼  ▼             │       │
┌──┐ │ ┌──┐           │       │
## 🚀 Cara Menjalankan

### Persyaratan:
- Web server (XAMPP, Wampserver, atau server lokal)
- Browser modern (Chrome, Firefox, Safari, Edge)

### Langkah:
1. Copy folder `ethics game` ke folder `htdocs` di XAMPP
2. Jalankan XAMPP (Start Apache)
3. Buka browser dan akses `http://localhost/ethics%20game/index.html`
4. Klik "▶️ Mulai Permainan" untuk memulai

---

## 🐛 Troubleshooting

| Masalah | Solusi |
|---------|--------|
| Browser menampilkan halaman kosong | Clear browser cache (Ctrl+Shift+Delete), refresh (F5) |
| Tombol tidak responsif | Pastikan JavaScript enabled di browser settings |
| Text terlalu kecil saat diproyeksikan | Zoom browser ke 150-200% atau gunakan fullscreen mode (F11) |
| Emoji tidak muncul | Update browser ke versi terbaru yang support emoji |
| Game tidak bisa dimulai | Periksa console (F12) untuk error messages |

---

## 📝 Catatan Pengembangan

### Versi Saat Ini: 1.0

### Feature yang Sudah Diimplementasikan:
- ✅ Layar informasi dengan panduan bermain
- ✅ 8 tim dengan emoji dan warna unik
- ✅ 20 pertanyaan etika IT dalam format studi kasus singkat
- ✅ 4 pilihan jawaban dengan layout grid horizontal
- ✅ Visual feedback untuk jawaban benar/salah
- ✅ Track balapan dengan pergerakan smooth
- ✅ 3 kondisi menang (finish, posisi terjauh, tiebreaker)
- ✅ Rock-Paper-Scissors untuk tiebreaker
- ✅ Modal pemenang dengan animasi
- ✅ Tombol kembali ke menu
- ✅ Responsive design untuk berbagai ukuran layar
- ✅ Dioptimasi untuk proyektor (text besar, kontras tinggi)

### Future Enhancement Ideas:
- 🔄 Leaderboard/Score tracking
- 🔊 Sound effects dan background music
- ⏱️ Timer untuk menjawab pertanyaan
- 🎓 Multiple difficulty levels
- 📊 Statistics dan analytics
- 🌐 Multiplayer online
- 🏆 Achievement badges
- 🎨 Theme customization

---

## 👥 Tim Pengembang

**Project Owner**: User (Requestor)
**Developer**: GitHub Copilot (AI Assistant)
**Technology Stack**: Vanilla HTML5, CSS3, JavaScript ES6+

---

## 📄 Lisensi

Proyek ini dibuat untuk tujuan edukasi. Silakan gunakan dan modifikasi sesuai kebutuhan.

---

## 📞 Support & Contact

Untuk pertanyaan atau masalah teknis, periksa:
1. Browser console (F12) untuk error messages
2. File dokumentasi ini untuk troubleshooting
3. Inline comments dalam `index.html` untuk penjelasan logika

---

**Dokumen terakhir diperbarui**: 18 Desember 2025

**Status Proyek**: ✅ Selesai & Berfungsi Optimal (Single File Version)

---

## 📋 Checklist Fitur

- [x] Game structure dengan 8 tim
- [x] Race track dengan START dan FINISH
- [x] 20 pertanyaan etika IT
- [x] Multiple choice answer system
- [x] Answer validation dengan visual feedback
- [x] Team progression mechanics
- [x] Winner determination (semua 3 skenario)
- [x] Rock-Paper-Scissors tiebreaker
- [x] Responsive layout
- [x] Answer randomization
- [x] Back to menu button
- [x] Dynamic modal headers
- [x] Optimized untuk proyektor
- [x] Clean & intuitive UI/UX
- [x] CSS & JavaScript embedded dalam index.html
- [x] Simplifikasi file struktur (single file deployment)
- [x] Dynamic modal headers
- [x] Optimized untuk proyektor
- [x] Clean & intuitive UI/UX