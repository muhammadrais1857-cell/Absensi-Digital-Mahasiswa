# Absensi Digital Mahasiswa

Aplikasi absensi mahasiswa berbasis web, satu file HTML, tanpa server dan tanpa instalasi. Bisa dibuka langsung di browser atau di-hosting gratis lewat GitHub Pages.

## Fitur

- Kelola beberapa kelas sekaligus (tambah, ganti nama, hapus)
- Tambah/hapus mahasiswa (nama + NIM opsional)
- Tambah pertemuan (sesi) baru dengan satu klik
- Klik sel untuk mengubah status: **H** Hadir, **S** Sakit, **I** Izin, **A** Alpa
- Rekap otomatis jumlah H/S/I/A per mahasiswa
- Ekspor data ke CSV (bisa dibuka di Excel/Google Sheets)
- Data tersimpan otomatis di browser (localStorage) — tidak hilang saat direfresh

## Cara pakai cepat (tanpa GitHub)

Cukup buka `index.html` langsung di browser (dobel klik filenya). Semua data tersimpan di browser perangkat tersebut.

## Cara menjalankan di GitHub Pages

1. Buat repository baru di GitHub, misalnya `absensi-digital`.
2. Upload file `index.html` ini ke repository tersebut (lewat "Add file" → "Upload files", atau via `git push`).
3. Buka menu **Settings** → **Pages** pada repository.
4. Pada bagian **Build and deployment**, pilih **Source: Deploy from a branch**, lalu pilih branch `main` dan folder `/ (root)`. Klik **Save**.
5. Tunggu 1–2 menit, lalu buka URL yang muncul, biasanya:
   ```
   https://<username-github-kamu>.github.io/absensi-digital/
   ```
6. Selesai — aplikasi sudah bisa diakses dan digunakan siapa saja yang membuka link tersebut.

### Lewat terminal (opsional)

```bash
git init
git add index.html README.md
git commit -m "Absensi digital mahasiswa"
git branch -M main
git remote add origin https://github.com/<username-kamu>/absensi-digital.git
git push -u origin main
```

Lalu aktifkan GitHub Pages seperti langkah 3–5 di atas.

## Catatan penting

- Data absensi tersimpan **per browser/perangkat**, bukan di server bersama. Artinya jika dibuka dari HP dosen dan laptop asisten, datanya akan berbeda (tidak otomatis sinkron).
- Untuk mencegah kehilangan data, gunakan tombol **Ekspor CSV** secara berkala sebagai cadangan.
- Cocok untuk penggunaan satu operator (misalnya dosen/asisten mencatat absensi di satu perangkat setiap pertemuan).
