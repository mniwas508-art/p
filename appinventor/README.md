# Proyek App Inventor — "Cara untuk Bahagia"

File siap import: **`CaraBahagia.aia`**

## Cara import ke App Inventor
1. Download `CaraBahagia.aia` (klik file → tombol **Download raw file**).
2. Buka https://ai2.appinventor.mit.edu → **Projects → Import project (.aia) from my computer** → pilih file tadi.
3. Proyek terbuka lengkap dengan tampilan, gambar, audio, dan blok.
4. **Connect → AI Companion** untuk uji coba, atau **Build → Android App (.apk)**.

## Ganti gambar/suara sendiri (opsional)
Di panel **Media** klik **Upload File…** dan unggah file dengan nama **persis** `bahagia.jpg` atau `motivasi.mp3` → pilih *overwrite*. Tidak perlu mengubah blok.

## Spesifikasi
- **Input**: pengguna mengetuk gambar bertema bahagia pada tampilan warna-warni.
- **Proses**: aplikasi memutar rekaman kata-kata motivasi (Player), mengubah warna latar, dan memperbarui teks status.
- **Output**: rekaman suara motivasi agar selalu bahagia terdengar lewat speaker ponsel.

## Blok
```
when ButtonGambar.Click
  call Player1.Start
  set Screen1.BackgroundColor to [hijau]
  set LabelStatus.Text to "Sedang memutar motivasi... 🎧"

when ButtonStop.Click
  call Player1.Pause
  set Screen1.BackgroundColor to [kuning]
  set LabelStatus.Text to "Dihentikan. Ketuk gambar lagi 😊"

when Player1.Completed
  set Screen1.BackgroundColor to [pink]
  set LabelStatus.Text to "Selesai! Tetap bahagia ya 💖"
```
Folder `CaraBahagia/` adalah isi mentah `.aia` (untuk diedit lewat teks); build ulang dengan `cd CaraBahagia && zip -r ../CaraBahagia.aia assets youngandroidproject src`.
