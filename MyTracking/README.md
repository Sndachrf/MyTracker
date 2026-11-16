# MyTracker

Prototype WebApp statis untuk merencanakan sesi, mengimpor workbook `.xlsx`, memisahkan sheet pendukung, dan mencatat progres.

Font Inter dan ikon instalasi disertakan di folder `assets`. Manifest Web App mengatur ikon, nama aplikasi, serta warna latar instalasi `#211f1f`.

## Menjalankan di komputer

Di PowerShell, buka folder project lalu jalankan:

```powershell
python -m http.server 4173 --bind 0.0.0.0
```

Buka `http://localhost:4173` di browser.

## Membuka dari smartphone di jaringan Wi-Fi yang sama

Cari alamat IPv4 komputer, lalu buka `http://ALAMAT-IP-KOMPUTER:4173` di browser smartphone. Firewall Windows mungkin meminta izin jaringan privat.

File Excel dibaca di browser dan tidak dikirim ke server. Plan tersimpan di `localStorage` browser pada perangkat yang mengimpor. Nilai rumus Excel memakai hasil hitung terakhir yang disimpan di workbook; hitung ulang dan simpan file di Excel sebelum impor jika rumusnya baru berubah.

## Batas versi ini

- Mendukung `.xlsx`, belum mendukung `.xls`.
- Pengingat disimpan sebagai preferensi lokal; notifikasi terjadwal belum dikirim.
- Progress dihitung ulang dari sesi yang tersimpan; setiap workbook dan sheet pendukung dipetakan menurut jenis plan.
