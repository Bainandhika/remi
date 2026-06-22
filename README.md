# 🃏 Custom Remi Game (1v3 AI)

Sebuah *Single-Page Application* (SPA) berbasis web game kartu remi kustom yang dimainkan secara *client-side* (sepenuhnya di browser). Pengguna akan ditantang untuk bertanding melawan 3 Bot Komputer (AI) cerdas dalam mengumpulkan skor hingga mencapai **1000 poin**. 

Game ini mengadaptasi aturan remi tradisional yang dimodifikasi dengan mekanik modern yang kompetitif, taktis, dan penuh dengan tensi tinggi.

---

## 🚀 Fitur Unggulan & Mekanik Kustom

* **100% Serverless & Client-Side:** Seluruh logic permainan, pembagian kartu, kocok deck, hingga kecerdasan Bot berjalan langsung di browser pengguna tanpa ketergantungan server eksternal.
* **Joker Dinamis:** Di setiap awal ronde, satu kartu akan dibuka secara acak dari meja. Peringkat dari kartu tersebut otomatis berubah menjadi kartu *Wildcard* (Joker) untuk sisa ronde berjalan.
* **Early Punishment (-50 Poin):** Putaran pertama yang brutal! Jika pemain membuang kartu dengan peringkat kembar dengan pemain lain atau sama dengan kartu Joker dinamis, penalti -50 poin langsung diberikan.
* **Deep Discard Pile Pickup (Mekanik Serok):** Pemain diizinkan mengambil kartu dari urutan tengah/bawah tumpukan buangan asalkan mengangkut seluruh kartu di atasnya, dengan syarat sisa kartu di tangan setelah menggelar kartu jadi maksimal 7 kartu.
* **Mekanik "Salip-Sembelih" (Reset 0):** Fitur pengubah keadaan! Jika total skor Anda berada di atas 100 poin dan berhasil disalip (dilewati) oleh pemain lain di akhir ronde, skor Anda akan otomatis ambles kembali ke **0 poin**.
* **Rule-Based AI Bot:** Tiga bot komputer dengan algoritma logika yang mampu menganalisis kegunaan tumpukan buangan, kalkulasi batas kartu di tangan, serta memilih kartu sampah dengan nilai minus terbesar untuk dibuang.
* **Persistent Leaderboard:** Menggunakan *LocalStorage* untuk menyimpan histori skor, sehingga sesi permainan multi-ronde Anda tetap aman meskipun halaman web di-*refresh*.

---

## 🛠️ Tech Stack

* **Frontend Framework:** Vue.js 3 (Composition API)
* **State Management:** Pinia (Mengelola *state* kartu, antrean giliran, validasi kartu jadi, dan kalkulasi skor)
* **Styling & UI:** Tailwind CSS & Animasi CSS transisi kartu
* **Storage:** LocalStorage Web API
* **Deployment:** Vercel / GitHub Pages

---

## 🎮 Cara Menang
1. Buat kombinasi kartu **Seri** (Run: berurutan, kembang sama) atau **Tris** (Set: kembar, kembang beda) minimal 3 kartu.
2. Ingat! Kartu Tris baru dianggap sah dan bernilai positif jika Anda **sudah memiliki minimal 1 kombinasi kartu Seri**. Jika tidak, Tris Anda akan hangus terbakar (menjadi poin minus).
3. Lakukan **Closed Card** (Tutup Kartu) untuk mendapatkan bonus instan **+250 poin**.
4. Jadilah pemain pertama yang menembus total **1000 poin** untuk memenangkan seluruh permainan!
