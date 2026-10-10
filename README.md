# Belajar Embed di Golang

## Daftar Materi
- Pengenalan Embed Package
- Embed File ke String
- Embed File ke []Byte
- Embed Multiple Files
- Path Matcher
- Hasil Embed di Compile

---

## Ringkasan Materi

### Pengenalan Embed Package
Package `embed` di Golang dipakai buat menyertakan file statis langsung ke dalam binary saat compile. Cocok buat nyimpen konfigurasi, template, atau asset tanpa perlu file eksternal.

### Embed File ke String
File bisa di-embed ke variabel bertipe `string`. Biasanya dipakai buat teks atau konfigurasi kecil.

### Embed File ke []Byte
File bisa di-embed ke variabel bertipe `[]byte`. Berguna buat file biner atau data non-teks.

### Embed Multiple Files
Dengan directive `//go:embed`, kita bisa embed banyak file sekaligus ke dalam variabel `embed.FS`.

### Path Matcher
`//go:embed` mendukung pola path matcher (misalnya `*.txt` atau folder) buat embed banyak file sesuai pola.

### Hasil Embed di Compile
Semua file yang di-embed akan langsung masuk ke binary hasil compile. Jadi aplikasi bisa jalan tanpa bergantung pada file eksternal.

---

## Catatan
- `embed` hanya bisa dipakai di variabel global.  
- Cocok buat aplikasi yang butuh **self-contained binary**.  
- Pastikan file yang di-embed tidak terlalu besar supaya ukuran binary tetap manageable.
