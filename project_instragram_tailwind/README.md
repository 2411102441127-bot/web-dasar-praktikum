1. Jelaskan keputusan grid-cols/gap di tiap breakpoint — kenapa begitu?

 Mobile (default, grid-cols-1): layar kecil → feed ditampilkan 1 kolom agar gambar besar, mudah dilihat, dan tidak terlalu   padat.
 Tablet (md:grid-cols-2 / md:grid-cols-3): layar sedang → lebih banyak ruang, feed bisa dibagi 2–3 kolom supaya mirip        Instagram asli tapi tetap readable.
 Desktop (lg:grid-cols-4+): layar lebar → memanfaatkan penuh ruang dengan grid 4 kolom atau lebih sehingga user bisa         melihat banyak foto sekaligus.
 Gap (gap-2/gap-4): menjaga jarak antar foto agar tidak menempel, tapi tetap hemat ruang.
 Konfigurasi ini mengikuti prinsip mobile-first + responsive design.

2. Bagaimana kamu memanfaatkan utility responsive Tailwind untuk memecahkan masalah layout yang muncul di mobile?

  Gunakan responsive prefix (sm:, md:, lg:) untuk menyesuaikan grid/flex sesuai device.
  Tombol aksi (Follow/Edit Profile) dibuat full width di mobile (w-full block text-center) agar mudah ditekan, lalu kembali   ke ukuran normal (md:w-auto inline-block) di layar lebih besar.
  Atur ulang urutan elemen dengan order-* dan md:order-* supaya elemen penting muncul duluan di mobile.
  Gunakan ukuran teks yang berbeda (text-sm md:text-base lg:text-lg) agar tetap proporsional di semua layar.
  Pendekatan ini bikin UI mudah dipakai di mobile tanpa mengorbankan pengalaman di desktop.

3. Jelaskan trade-off antara memakai banyak utility classes vs membuat component CSS tersendiri.

 Utility classes (Tailwind murni):
- Cepat dipakai, langsung responsif tanpa nulis CSS tambahan.
- Konsisten dengan design system Tailwind.
- HTML bisa jadi panjang & sulit dibaca.

Component CSS tersendiri (misalnya via @apply / custom class):
- HTML lebih bersih & ringkas, mudah dipelihara.
- Bisa dipakai ulang di banyak tempat.
- Butuh tambahan definisi CSS, sedikit melawan prinsip utility-first Tailwind.
