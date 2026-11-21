CARA PASANG
1. Buka console.firebase.google.com > Add project > Build > Firestore Database > Create database.
2. Tab Rules, tempel lalu Publish:
   rules_version='2'; service cloud.firestore { match /databases/{d}/documents { match /verifikasi/{id} { allow read, write: if true; } } }
3. Project settings > Your apps > Web (</>) > salin firebaseConfig.
4. Buka index.html, ganti nilai pada baris 'const FB={...}' dengan config Anda.
5. Upload seluruh isi folder ke Netlify (app.netlify.com/drop).
6. Buka alamat Netlify di Chrome HP > menu titik tiga > Instal aplikasi / Add to Home screen.
