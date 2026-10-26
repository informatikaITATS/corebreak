# COREBREAK — Ekspedisi Sistem Biner

Game simulasi RPG HTML5 + Three.js berdasarkan materi **Sistem Biner, Satuan Data, dan Prosesor** dari PPT.

## Menjalankan lewat Apache (XAMPP/WAMP)

1. Ekstrak isi paket ini ke folder baru, misalnya `C:\xampp\htdocs\corebreak\`.
2. Pastikan `index.html`, `game.js`, `style.css`, dan folder `assets` berada langsung di dalam folder `corebreak`.
3. Jalankan Apache, lalu buka `http://localhost/corebreak/`.
4. Jika pernah membuka versi lama, tekan **Ctrl+F5** untuk memuat ulang file tanpa cache.

Three.js dan model karakter 3D dimuat dari CDN, sehingga koneksi internet diperlukan untuk scene dan karakter 3D. Daftar misi dan soal ditampilkan segera dan tetap dapat dimainkan dari panel misi saat CDN lambat/gagal; scene 3D akan muncul jika CDN berhasil dimuat.

## Menjalankan tanpa Apache

Buka PowerShell di folder game, lalu jalankan:

    python -m http.server 8000

Kemudian kunjungi `http://localhost:8000`. Jangan membuka `index.html` langsung sebagai `file://`, karena browser membatasi ES module.

## Cara bermain

- Gerakkan karakter 3D dengan **W A S D** atau tombol panah.
- Dekati simpul bercahaya, lalu tekan **E** untuk membuka soal.
- Klik simpul atau pilih nama misi di panel untuk berjalan ke tujuan; semua misi terbuka sejak awal.
- Setiap jawaban benar memberi Bit Coin. Buka **Toko baju** untuk membeli atau memakai seragam; warna pakaian karakter ikut berubah.
- Ada 20 soal. Jawaban yang benar diganti soal lain dalam topik yang sama; setelah seluruh bank soal dipakai, soal berputar kembali.
- Tiap soal menampilkan hint. XP, jawaban unik, Bit Coin, dan kostum tersimpan otomatis di browser.

## Bank 20 soal

Bank mencakup konversi biner-desimal; jumlah kombinasi bit; bit/byte; GB dan GiB; alur data digital; sinyal analog-digital; satuan waktu; frekuensi dan periode clock; ukuran word; CISC/RISC; serta faktor kinerja prosesor. Formatnya bervariasi: hitung angka, sakelar bit, pilihan, menyusun alur, mencocokkan, dan memilih faktor diagnosis.

## Aset karakter

Model animasi [RobotExpressive dari three.js](https://threejs.org/examples/webgl_animation_skinning_morph.html), karya Tomás Laulhé dengan modifikasi Don McCurdy, berlisensi CC0 1.0 menurut [README model resminya](https://github.com/mrdoob/three.js/blob/dev/examples/models/gltf/RobotExpressive/README.md?plain=1). Jika aset gagal dimuat, game menampilkan karakter prosedural sebagai cadangan.