# 🌺 Interactive Spider Lily — Versi Web 🌸

Bunga 3D yang **tumbuh dan mekar mengikuti gerakan tanganmu** lewat webcam ✋✨
Dibuat dengan Three.js + MediaPipe, versi kode dari karya TouchDesigner aslinya.

Ada dua pilihan bunga:
- 🌺 `index.html` → Spider Lily merah
- 🌸 `index-lily.html` → Lily pink

---

## 🚀 Cara Menjalankan

```bash
cd spiderlily-web
npx http-server -p 8642
```

Lalu buka di browser 🌐:
- Spider Lily → http://127.0.0.1:8642
- Lily pink → http://127.0.0.1:8642/index-lily.html

Jangan lupa klik **Allow** saat diminta izin kamera 📷

> 💡 Harus dibuka lewat `localhost` / `127.0.0.1`, bukan klik dua kali file-nya, supaya kamera bisa jalan.
> Punya Python? Bisa juga pakai `python -m http.server 8642` 🐍

---

## 🖐️ Cara Main

| Tangan | Gerakan | Hasil |
|---|---|---|
| 🤚 Kiri | Renggangkan jempol & telunjuk | 🌱 Tanaman tumbuh |
| ✋ Kanan | Renggangkan jempol & telunjuk | 🌸 Bunga mekar |

- Webcam muncul di pojok kanan bawah dengan titik putih di ujung jarimu 👀
- Tangan ketuker kiri-kanan? Ubah `swapHands` jadi `true` 🔄
- Mau bunganya mekar gantian? Naikkan `bloomStagger` mendekati `1` 🎀

---

## ⌨️ Tombol

| Tombol | Fungsi |
|---|---|
| `D` | 🤖 Ganti mode otomatis ↔ mode tangan |
| `1` / `2` / `3` | 🌷 Kunci di kuncup / setengah / mekar penuh |
| `0` | 🔁 Lanjutkan animasi otomatis |
| `H` | 🙈 Sembunyikan / tampilkan info |
| Drag / scroll | 🎥 Putar & zoom kamera |

---

## 🎨 Kustomisasi

Semua pengaturan ada di objek **`PARAMS`** di bagian atas file HTML: bentuk tanaman, jumlah kelopak, warna, efek glow, sampai posisi kamera 🖌️

Bisa juga diubah langsung dari Console browser (`F12`) 🧪

```js
PARAMS.glow.strength = 1.6   // langsung berubah ✨
PARAMS.stamens.count = 12    // perlu refresh 🔃
```

---

## 🐛 Kalau Ada Masalah

| Pesan | Solusi |
|---|---|
| 🚫 `NotAllowedError` | Izinkan kamera di browser & di Settings Windows → Camera |
| 📵 `NotReadableError` | Tutup aplikasi lain yang pakai kamera (Zoom, Discord, dll) |
| 🖤 Layar hitam | Cek internet, library diambil dari CDN |
| 📂 Muncul "Index of /" | Server dijalankan di folder yang salah, masuk ke `spiderlily-web` dulu |

Selamat bermain dan semoga bunganya mekar indah! 🌸💖🐝
