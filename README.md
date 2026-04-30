Muhammad Rafi Sugianto / 2406357135

1. Game Polishing

Pada tutorial ini, saya melakukan beberapa perubahan untuk meningkatkan game feel, yaitu:
- Menambahkan sistem acceleration dan deceleration pada pergerakan player menggunakan fungsi `lerp()`
- Menambahkan particle effect saat player berlari menggunakan node `GPUParticles2D`

Setelah menambahkan acceleration dan deceleration, pergerakan karakter terasa lebih halus dan tidak kaku seperti sebelumnya. Player tidak langsung mencapai kecepatan maksimum, melainkan mengalami percepatan secara bertahap dari yg awalnya pelan. Hal ini membuat kontrol terasa lebih natural dan realistis.

Selanjutnya, penambahan particle saat berlari memberikan feedback visual yang jelas kepada pemain ketika karakter sudah mencapai kecepatan maksimum. Dengan adanya partikel ini, pemain dapat dengan mudah memahami state dari karakter tanpa perlu melihat nilai velocity secara langsung.

Menurut saya, kedua perubahan ini meningkatkan game feelnya karena:

- Memberikan feedback visual terhadap aksi player
- Membuat pergerakan terasa lebih responsif dan smooth
- Meningkatkan kepuasan saat bermain


2. Game Balancing

Pada kondisi awal, spawn rate enemy terlalu cepat sehingga pemain hampir tidak memiliki kesempatan untuk melewati rintangan. Hal ini membuat game terasa terlalu sulit dan cenderung tidak fair.

Selanjutnya, saya mencoba beberapa nilai spawn rate:

- 5 detik: terlalu mudah, pemain dapat melewati rintangan tanpa kesulitan
- 3 detik: mulai menantang tetapi masih sangat mudah
- 1,5 detik: cukup sulit dan menantang (setidaknya bagi saya), namun masih bisa diselesaikan

Saya memilih spawn rate sebesar 1,5 detik karena menurut saya nilai ini memberikan keseimbangan yang baik antara tantangan dan kemungkinan untuk menyelesaikan level. Dengan begitu, pemain tetap harus fokus dan timing dengan baik, level juga menjadi tidak terlalu mudah, tetapi juga tidak membuat frustrasi. Hal inilah yg akan memberikan pengalaman flow, di mana pemain merasa tertantang namun tetap bisa berkembang


3. Proses Pengerjaan

Langkah-langkah yang saya lakukan:
1. Mengubah variabel `speed` menjadi float dan menambahkan konstanta acceleration dan deceleration
2. Mengimplementasikan `lerp()` untuk pergerakan horizontal player
3. Menambahkan node `GPUParticles2D` sebagai child dari player
4. Mengatur konfigurasi partikel (texture, gravity, velocity, emission shape)
5. Menambahkan logika untuk menampilkan partikel hanya saat player mencapai kecepatan maksimum
6. Melakukan eksperimen terhadap nilai spawn rate untuk mendapatkan balancing yang tepat


4. Referensi
- Materi Tutorial Game Development
