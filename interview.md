## 1.1 Latar Belakang
Game ini dibuat untuk memenuhi salah satu tugas pada mata kuliah Praktikum Dasar Pemograman sebagai tugas Ulangan Tengah Semester (UTS). Inspirasi saya membuat game ini karena terinspirasi dari keseharian saya sebagai seorang mahasiswa yang sehari-harinya harus mengumpulkan tugas-tugas, semakin banyak tugas yang dikumpulkan maka semakin besar juga nilai yang didapatkan.
## 1.2 Deksripsi dan alur cerita game
Didalam game ini terdapat satu orang player sebagai mahasiswa yang harus mengumpulkan tugas sebanyak-banyaknya sebelum waktu habis, titik-titik sebanyak 10 buah sebagai tugas yang harus dikumpulkan, tampilan timer yang dimulai dari 0 detik sampai 60 detik, tampilan papan skor yang dimana setiap 1 tugas yang dikumpulkan bernilai 10 berarti jika semua tugas berhasil dikumpulkan bernilai 100. Dan game jika hanya ditampilkan di terminal output maka pada awal game terdapat kalimat "Selamat datang di Game Dikejar 
Deadline!" dan "Kumpulkan 10 tugas dalam waktu 60 detik." selain itu terdapat juga tampilan sisa waktu dan tugas yang terkumpul, untuk mengumpulkan tugasnya pemain harus mengetikkan kata (hijau, biru, merah, kuning, putih) misal mengetik kata putih maka tugas terkumpul 1 dan sisa waktu akan ditampilkan, jika waktunya habis maka game selesai.
## 1.3 Branding game
- Nama Game = Dikejar Deadline 
- Tareget pengguna =
  - usia 7+
  - Seseorang yang tertarik mensimulasikan kehidupan nyata ke game
  - Seseorang yang suka menetukan strategi
  - Seseorang yang sedang bosan 
- Genre = Simulation (Life Simulation)
## 1.4 User Story
Sebagai | Saya ingin bisa | Sehingga | Prioritas
---|---|---|---
Pengguna | Menggerakan player | Player bisa bergerak | ⭐⭐⭐⭐⭐
Pengguna | Mengambil objek | Player bisa mengumpulkan objek |  ⭐⭐⭐⭐⭐
Pengguna | ganti tema | Player bisa memilih tema yang diinginkannya | ⭐⭐⭐
Pengguna | ganti kostum pemain | Player bisa memilih tema yang diinginkannya | ⭐⭐
Sistem | Set timer | Bisa set timer kapan game dimulai dan berakhir | ⭐⭐⭐⭐
Sistem | Membuat hambatan | Mempersulit player untuk memenangkan game | ⭐⭐
Sistem | Membuat level | game akan semakin menantang |⭐⭐
## 1.5 Desain User Interface
![WhatsApp Image 2023-12-16 at 17 18 06_607d2410](https://github.com/DesmiaWardah/2324-praktikum-dasar-pemograman/assets/144568328/230e64ec-bd73-4153-ba2e-85ce92cc12be)

## 1.6 Flowchart
<img width="329" alt="Screenshot 2023-12-18 145654" src="https://github.com/DesmiaWardah/2324-praktikum-dasar-pemograman/assets/144568328/4b8a439a-f969-46f2-9840-dd111b2dcddc">


## 1.7 Link Demo game
https://youtu.be/MqcoiF-ZPio?si=x7H1ss2d8ZS0bw3n
## 1.8 Kode Pemograman Game

import java.util.Random;
import java.util.Scanner;

public class Game {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        Random random = new Random();

        int score = 0;
        int targetScore = 10;
        int timeLimit = 60;
        long startTime = System.currentTimeMillis();

        System.out.println("Selamat datang di Game Dikejar Deadline!");
        System.out.println("Kumpulkan 10 tugas dalam waktu 60 detik.");

        while (score < targetScore) {
            long currentTime = System.currentTimeMillis();
            int elapsedTime = (int) ((currentTime - startTime) / 1000);

            if (elapsedTime >= timeLimit) {
                System.out.println("Waktu habis! Skor kamu: " + score);
                System.out.println("Game Over!");
                break;
            }

            System.out.println("Waktu tersisa: " + (timeLimit - elapsedTime) + " detik");
            System.out.println("Titik yang terkumpul: " + score);

            // Generate warna secara acak (hijau, biru, merah, kuning, putih)
            String[] warna = {"hijau", "biru", "merah", "kuning", "putih"};
            String titikWarna = warna[random.nextInt(warna.length)];

            System.out.print("Ketik warna titik (hijau, biru, merah, kuning, putih): ");
            String input = scanner.nextLine();

            if (input.equalsIgnoreCase(titikWarna)) {
                score += 10;
                System.out.println("Titik berwarna " + titikWarna + " ditambahkan! Skor saat ini: " + score);
            } else {
                System.out.println("Warna salah! Coba lagi.");
            }
        }

        if (score >= targetScore) {
            System.out.println("Selamat! Kamu berhasil mengumpulkan " + targetScore + " titik dalam waktu 60 detik.");
            System.out.println("Game Winner!");
        }
    }
}

## 2. konsep variable, data type dan operator pada bahasa pemrograman digunakan dalam pembuatan game ini
game ini memanfaatkan variabel-variabel seperti score, targetScore, timeLimit, startTime, elapsedTime untuk mengatur logika permainan dan waktu. Input dari pemain dibaca menggunakan objek Scanner, dan pemain diminta untuk memasukkan warna titik yang sesuai dengan warna yang dihasilkan secara acak.
## 3. konsep boolean dan conditions pada bahasa pemrograman digunakan dalam pembuatan game ini
Dalam pembuatan game ini, konsep boolean dan conditions digunakan untuk mengontrol alur permainan dan memeriksa kesesuaian input pemain. Seperti pada saat memeriksa sisa waktu pada game digunakan conditions `if (elapsedTime >= timeLimit)` dengan tipe data boolean untuk memeriksa apakah waktu sudah habis atau belum. Selain itu, pada game ini juga digunakan coditions 
`if (input.equalsIgnoreCase(titikWarna))` untuk memeriksa apakah input pemain sama dengan warna titik yang dihasilkan secara acak. `if (input.equalsIgnoreCase(titikWarna))` untuk mengembalikan nilai boolean true atau false tergantung kesesuaian kedua nilai. `  if (score >= targetScore) ` untuk memeriksa apakah score yang didapat nilainya sama dengan nilai target score. Dengan adanya penggunaan conditions ini, permainan dapat berjalan dengan benar dan memberikan respon yang sesuai kepada pemain berdasarkan input dan kondisi yang diberikan.
## 4. konsep looping dan array pada bahasa pemrograman digunakan dalam pembuatan game ini
Pada game ini, konsep looping digunakan dalam perulangan while untuk terus menjalankan permainan selama skor belum mencapai target atau waktu masih cukup, seperti `while (score < targetScore)`. Sedangkan array digunakan untuk menyimpan daftar warna titik dalam array warna[], memungkinkan pemilihan warna secara acak dengan bantuan kelas Random.
## 5. konsep method pada bahasa pemrograman digunakan dalam pembuatan game ini
Dalam game ini, konsep method pada bahasa pemrograman Java tidak digunakan secara eksplisit. Semua logika permainan dan interaksi dengan pemain terletak di dalam metode main. Namun, meskipun tidak ada metode terpisah, Anda masih dapat mengorganisasi kode lebih lanjut dengan membuat metode-metode kecil untuk tugas-tugas tertentu.
Contoh penggunaan metode bisa melibatkan pemisahan fungsionalitas seperti inisialisasi permainan, input dari pemain, logika permainan, dan output pesan. Hal ini dapat meningkatkan keterbacaan dan pemeliharaan kode.
## 6. konsep class pada bahasa pemrograman digunakan dalam pembuatan game ini 
Dalam game ini, konsep class pada bahasa pemrograman Java digunakan dengan membuat sebuah kelas bernama Game. Kelas ini menyediakan sebuah metode statis main yang merupakan titik awal eksekusi program. Beberapa variabel seperti score, targetScore, timeLimit, dan startTime diatur sebagai atribut kelas.
Selain itu, objek-objek dari kelas Scanner dan Random juga dibuat di dalam kelas untuk digunakan dalam metode main. Semua logika permainan, termasuk input dari pemain, pengolahan waktu, dan penanganan perulangan, terletak di dalam metode main.
Dengan menggunakan kelas, Anda dapat mengorganisasi kode dengan lebih baik, memisahkan tanggung jawab dan meningkatkan keterbacaan serta pemeliharaan kode.
## 7. algoritma
- user menekan tombol start pada halaman awal
- game dimulai
- kumpulkan tugas-tugas sebelum waktu habis
- jika tugas terkumpul maka game menang
- jika tugas tidak terkumpul maka game over

