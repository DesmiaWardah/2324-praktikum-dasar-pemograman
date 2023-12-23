## 1. Jelaskan penggunaan array, looping, condition, dan class pada game yang dibuat
- konsep array digunakan untuk menyimpan daftar warna titik dalam array warna[], memungkinkan pemilihan warna secara acak dengan bantuan kelas Random.
- Looping digunakan dalam perulangan while untuk terus menjalankan permainan selama skor belum mencapai target atau waktu masih cukup, seperti while (score < targetScore).
- Conditions digunakan untuk mengontrol alur permainan dan memeriksa kesesuaian input pemain. Seperti pada saat memeriksa sisa waktu pada game digunakan conditions if (elapsedTime >= timeLimit) dengan tipe data boolean untuk memeriksa apakah waktu sudah habis atau belum. Selain itu, pada game ini juga digunakan coditions if (input.equalsIgnoreCase(titikWarna)) untuk memeriksa apakah input pemain sama dengan warna titik yang dihasilkan secara acak. if (input.equalsIgnoreCase(titikWarna)) untuk mengembalikan nilai boolean true atau false tergantung kesesuaian kedua nilai.  if (score >= targetScore) untuk memeriksa apakah score yang didapat nilainya sama dengan nilai target score. Dengan adanya penggunaan conditions ini, permainan dapat berjalan dengan benar dan memberikan respon yang sesuai kepada pemain berdasarkan input dan kondisi yang diberikan.
- Dalam game ini, konsep class pada bahasa pemrograman Java digunakan dengan membuat sebuah kelas bernama Game. Kelas ini menyediakan sebuah metode statis main yang merupakan titik awal eksekusi program. Beberapa variabel seperti score, targetScore, timeLimit, dan startTime diatur sebagai atribut kelas. Selain itu, objek-objek dari kelas Scanner dan Random juga dibuat di dalam kelas untuk digunakan dalam metode main. Semua logika permainan, termasuk input dari pemain, pengolahan waktu, dan penanganan perulangan, terletak di dalam metode main. Dengan menggunakan kelas, Anda dapat mengorganisasi kode dengan lebih baik, memisahkan tanggung jawab dan meningkatkan keterbacaan serta pemeliharaan kode.
## 2. Jelaskan proses pengembangan algoritma yang dilakukan pada game yang dibuat
## 3. Jelaskan bagaimana game yang dibuat dapat didistribusikan dan digunakan oleh pengguna
- Merancang dan membuat game
Buat game Anda menggunakan platform pengembangan yang sesuai seperti Unity, Unreal Engine, atau engine lainnya.
Pastikan game Anda memenuhi persyaratan teknis dan hukum platform yang dituju.
- Pengembangan game
  Kembangkan game dari algoritma yang sudah dibuat agar lebih menarik peminat
- Pemilihan platfrom
  Menentukan platform distribusi yang akan digunakan, seperti PC (Steam, Epic Games Store), konsol (PlayStation, Xbox, Nintendo), atau perangkat seluler (Google Play Store, Apple App Store).
- Pendaftaran dan persetujuan
  Untuk platform tertentu, perlu mendaftar sebagai pengembang dan mendapatkan persetujuan sebelum dapat mendistribusikan game. Persyaratan ini bervariasi tergantung pada platform.
- Penilaian dan sertifikasi
  Beberapa platform memerlukan penilaian dan sertifikasi untuk memastikan bahwa game yang dibuat memenuhi standar kualitas dan keamanan. Ini melibatkan peninjauan dari pihak platform.
- Penyandian dan kompilasi
  Sesuaikan game Anda agar dapat dijalankan pada platform yang dituju. Ini mungkin melibatkan proses penyandian (jika game Anda menggunakan bahasa seperti C++) dan kompilasi ulang untuk platform spesifik.
- Distribusi digital
  Jika Anda memilih distribusi digital, siapkan game Anda untuk diunggah ke platform distribusi digital (seperti Steam, Google Play Store, dll.).
Ikuti petunjuk yang diberikan oleh platform untuk mengunggah game dan memasarkan produk Anda.
- Penjualan atau distribusi gratis
  Tentukan apakah game Anda akan dijual atau didistribusikan secara gratis. Atur harga, jika diperlukan, dan tentukan metode pembayaran atau monetisasi (misalnya, pembelian dalam aplikasi, mikrotransaksi).
- Peluncuran dan pemasaran
  Siapkan kampanye pemasaran untuk meningkatkan visibilitas game Anda. Gunakan media sosial, situs web, dan alat pemasaran lainnya untuk mempromosikan game Anda sebelum dan setelah peluncuran.
- Pemeliharaan dan pembaruan
  Setelah peluncuran, terus perbarui dan perbaiki bug pada game. Perhatikan umpan balik dari pengguna dan berikan pembaruan secara teratur untuk meningkatkan pengalaman pengguna.
- Dukungan Pengguna
  Siapkan sistem dukungan pengguna untuk menanggapi pertanyaan, masalah, atau umpan balik dari pengguna.
- Analisis dan pemantauan
  Gunakan alat analisis untuk memantau kinerja game Anda, memahami perilaku pengguna, dan membuat perbaikan berdasarkan data yang diperoleh.
