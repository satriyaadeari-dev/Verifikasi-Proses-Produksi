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
