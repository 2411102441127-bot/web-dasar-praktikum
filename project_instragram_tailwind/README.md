1. Mengapa memilih konfigurasi col-* tertentu untuk tiap breakpoint?
   
  Mobile (≤576px, 1 kolom): layar kecil → konten harus mudah dibaca, feed ditampilkan satu-satu agar tidak terlalu padat.
Tablet (≥768px, 2–3 kolom): layar sedang → memungkinkan menampilkan lebih banyak foto per baris, tapi tetap menjaga ukuran gambar tidak terlalu kecil.
Desktop (≥992px, 4 kolom): layar lebar → foto bisa ditampilkan grid 4 kolom (atau 5–6 kalau rapi) sehingga menyerupai layout Instagram asli.
Konfigurasi ini dipilih agar UX tetap konsisten, konten tetap terbaca jelas, dan layout responsif di berbagai device.

3. Bagaimana memastikan tombol Follow/Edit Profile tetap mudah dijangkau di mobile?
Tombol menggunakan Bootstrap button utilities (btn, btn-primary, w-100 atau d-block).
Pada mobile, tombol diberi lebar penuh (full-width) agar mudah ditekan dengan jari.
Menggunakan Bootstrap responsive utilities (d-sm-inline, d-block, dsb) untuk mengatur posisi tombol agar bergeser sesuai breakpoint.
Pendekatan ini memastikan tombol selalu visible, besar, dan mudah diakses di layar kecil.

4. Jika postingan bertambah jadi 50, apa potensi masalah dan bagaimana solusi gridmu mengatasinya?
Potensi masalah:
Loading halaman lebih berat (butuh load lebih banyak gambar).
Grid bisa jadi terlalu panjang dan butuh scroll berlebihan.
Layout bisa berantakan kalau ukuran gambar tidak konsisten.
