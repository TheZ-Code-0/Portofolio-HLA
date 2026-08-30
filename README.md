# Situs PT Hikma Langgeng Abadi

Situs statis satu halaman. Tidak butuh server, database, atau proses build —
cukup file HTML, aset gambar, dan katalog PDF.

## Isi

```
index.html              seluruh halaman (HTML, CSS, dan JS jadi satu berkas)
assets/img/             foto dan logo
assets/pdf/             company profile dan tujuh katalog produk
CNAME                   domain khusus (dibuat saat mengaktifkan GitHub Pages)
```

## Menjalankan di komputer sendiri

Buka `index.html` langsung di browser. Untuk menghindari masalah pada peta,
jalankan lewat server lokal:

```bash
python3 -m http.server 8000
# lalu buka http://localhost:8000
```

## Menerbitkan lewat GitHub Pages

1. Buat repositori baru di GitHub, lalu push isi folder ini.
2. Buka **Settings → Pages**.
3. Bagian *Source* pilih **Deploy from a branch**, branch `main`, folder `/ (root)`.
4. Simpan. Beberapa menit kemudian situs terbit di
   `https://<nama-akun>.github.io/<nama-repo>/`.

### Memakai domain sendiri

1. Di **Settings → Pages → Custom domain**, isi `www.hikmalanggengabadi.com`
   lalu simpan. GitHub akan membuat berkas `CNAME` di repositori.
2. Di panel DNS penyedia domain, arahkan:
   - `www` → CNAME ke `<nama-akun>.github.io`
   - domain tanpa `www` → empat A record ke alamat GitHub Pages
     (lihat dokumentasi GitHub, alamatnya bisa berubah)
3. Setelah DNS menyebar, centang **Enforce HTTPS**.

## Memperbarui katalog

Katalog dipanggil memakai nama berkas tetap. Cukup timpa berkas lama di
`assets/pdf/` dengan nama yang sama, tidak perlu mengubah `index.html`.

| Berkas | Isi |
|---|---|
| `company-profile-hla.pdf` | Profil perusahaan |
| `katalog-sika-hla.pdf` | Waterproofing, perekat keramik, mortar dinding |
| `katalog-shera-hla.pdf` | Papan silikat RB SHERA |
| `katalog-aplus-hla.pdf` | Sistem plafon dan gypsum |
| `katalog-mattaka-hla.pdf` | Atap uPVC |
| `katalog-turbinku-hla.pdf` | Turbin ventilator |
| `katalog-hikma-fold-hla.pdf` | Folding container |
| `katalog-toilet-cubicle-hla.pdf` | Sistem partisi toilet |

## Catatan

- Gambar disimpan dalam format WebP agar halaman ringan (total aset gambar
  sekitar 280 KB).
- Tahun pada footer mengikuti tanggal, tidak perlu diubah tiap Januari.
- Formulir konsultasi mengarahkan pesan ke WhatsApp; tidak ada data yang
  tersimpan di server. Bila butuh arsip masuknya pesan, tambahkan layanan
  penampung formulir.
