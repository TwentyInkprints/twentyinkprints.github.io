# Twenty Inkprints Banjarmasin

Website percetakan digital **Twenty Inkprints** di Banjarmasin, Kalimantan Selatan. Pengunjung bisa melihat produk, menghitung perkiraan biaya cetak, lalu memesan lewat WhatsApp.

**Situs:** https://twentyinkprints.github.io/

## Produk

- Stiker Chromo, Vinyl Waterproof, dan Transparan (per lembar A3+)
- Kartu Nama (per box, isi 100)
- Thank You Card / Hangtag (per pak, isi 100)
- Jasa desain layout sederhana

## Fitur

- **Kalkulator harga:** pilih produk, jumlah, laminasi (Glossy atau Doff), dan kecepatan (Reguler atau Express). Total langsung dihitung.
- **Pesan WhatsApp otomatis:** rincian pesanan dari kalkulator terkirim sebagai pesan siap kirim ke admin.
- **Pembayaran QRIS:** kode QRIS bisa diperbesar agar mudah dipindai.
- **Daftar produk ringkas:** tiap produk bisa dibuka untuk melihat penjelasannya.
- **Menu hamburger** di HP, FAQ, dan tombol WhatsApp melayang.
- **Tetap berguna tanpa JavaScript:** daftar harga acuan, QRIS, dan tombol WhatsApp tetap tampil.
- **Responsif:** diuji dari layar 320 px sampai 1440 px.

## Struktur

Seluruh situs ada dalam satu file:

```
index.html   # HTML, CSS, dan JavaScript dalam satu file
README.md
```

Tidak ada proses build dan tidak ada library tambahan. Satu-satunya sumber dari luar adalah font Google (Plus Jakarta Sans), dan halaman tetap terbaca jika font gagal dimuat.

## Mengubah isi

Semua pengaturan ada di bagian `<script>` paling bawah `index.html`.

| Yang ingin diubah | Di mana |
|---|---|
| Harga, nama, deskripsi, minimal pesan, harga laminasi | Array `P` |
| Nomor WhatsApp | Konstanta `WA` (format `62...`, tanpa `+` atau `0`) |
| Tambahan biaya Express | Opsi `cExp` di bagian kalkulator |
| Tulisan FAQ dan cara pesan | Bagian `<section id="faq">` dan `<section id="cara-pesan">` |

Nomor WhatsApp juga tertulis di beberapa tautan `wa.me` dan di footer. Cari `6281959001170` lalu ganti semuanya.

**Mengganti QRIS:** simpan gambar QRIS baru (misalnya `qris.jpg`) di folder yang sama, lalu ubah atribut `src` pada `<img id="qImg">` menjadi `src="qris.jpg"`. Gambar di kotak perbesar ikut berubah otomatis. Ubah juga nama merchant dan NMID di bawah gambar.

## Memasang di GitHub Pages

1. Repository harus bernama `twentyinkprints.github.io` dan berstatus **Public**.
2. Pastikan file halaman bernama `index.html` di folder utama.
3. Buka **Settings → Pages**, pilih *Deploy from a branch*, branch `main`, folder `/ (root)`.
4. Tunggu 1–2 menit. Kalau tampilan belum berubah, buka ulang dengan menambahkan `?v=2` di akhir alamat untuk melewati cache.

## Catatan

- Harga di kalkulator adalah **perkiraan**. Harga akhir dikonfirmasi admin lewat WhatsApp setelah file desain dicek.
- Repository ini publik, jadi hindari menaruh data internal seperti harga modal atau catatan pelanggan di dalamnya.

## Kontak

- WhatsApp: 0819-5900-1170
- Instagram: [@twenty.inkprints](https://instagram.com/twenty.inkprints)
- Lokasi: Banjarmasin, Kalimantan Selatan
