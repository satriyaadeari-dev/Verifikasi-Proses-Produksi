CARA PASANG
1. Buka console.firebase.google.com > Add project > Build > Firestore Database > Create database.
2. Tab Rules, tempel lalu Publish:
   rules_version='2'; service cloud.firestore { match /databases/{d}/documents { match /verifikasi/{id} { allow read, write: if true; } } }
3. Project settings > Your apps > Web (</>) > salin firebaseConfig.
4. Buka index.html, ganti nilai pada baris 'const FB={...}' dengan config Anda.
5. Upload seluruh isi folder ke Netlify (app.netlify.com/drop).
6. Buka alamat Netlify di Chrome HP > menu titik tiga > Instal aplikasi / Add to Home screen.

UPDATE v17: tambah pilihan "Laporan" (Verifikasi Proses, OS & IPQC, Premium). Upload ulang seluruh isi folder ke Netlify, lalu tutup dan buka lagi aplikasi di HP agar versi baru terpasang.

UPDATE v18: tabel lebih ringkas, OS & IPQC 5 kolom Visual, Premium 1 kolom Qty Reject, unduh Excel 3 sheet, dashboard per laporan + Perbandingan, judul baru.

UPDATE v19: dashboard Perbandingan dihapus; OS (berat, Avg, Std Dev) dan IPQC (visual) dipisah; Premium 3 defect terbanyak per lokasi.

UPDATE v20: UH/UB di OS & IPQC, Premium 60 baris, laporan Durasi Ambri/Sap (input, dashboard, Excel 4 sheet), dashboard IPQC (UH, UB, Visual), pilihan jumlah NBK/ID di Premium, penyimpanan lebih ringan.

UPDATE v21: dashboard OS (standar berat, % Lower/Standar/Upper), IPQC (UH/UB kategori, Sd UH/Sd UB, pemisah Diameter dan Visual), Premium 3 defect per Lokasi/ID, Durasi 'ID', tab dan filter tanggal lebih ringkas.

UPDATE v23: IPQC: Visual di atas, Diameter di bawah; tabel % UH/UB 1 desimal tanpa geser; Visual dihitung per rokok defect/tanpa defect.

UPDATE v24: data dimuat 31 hari terakhir (hemat baca Firebase); periode lebih lama dimuat saat dipilih; 'Semua' meminta konfirmasi. Indeks field tanggal harus tetap aktif.

UPDATE v25: hemat baca (tanpa listener realtime, data dimuat sesuai periode, batas baca per perangkat), mode admin (ketuk judul 5x), Premium: Baris diganti MPP.
