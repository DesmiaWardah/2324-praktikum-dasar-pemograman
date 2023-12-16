## 1. Latar Belakang
Game ini dibuat untuk memenuhi salah satu tugas pada mata kuliah Praktikum Dasar Pemograman sebagai tugas Ulangan Tengah Semester (UTS). Inspirasi saya membuat game ini karena terinspirasi dari keseharian saya sebagai seorang mahasiswa yang sehari-harinya harus mengumpulkan tugas-tugas, semakin banyak tugas yang dikumpulkan maka semakin besar juga nilai yang didapatkan.
## 2. Deksripsi dan alur cerita game
Didalam game ini terdapat satu orang player sebagai mahasiswa yang harus mengumpulkan tugas sebanyak-banyaknya sebelum waktu habis, titik-titik sebanyak 10 buah sebagai tugas yang harus dikumpulkan, tampilan timer yang dimulai dari 0 detik sampai 60 detik, tampilan papan skor yang dimana setiap 1 tugas yang dikumpulkan bernilai 10 berarti jika semua tugas berhasil dikumpulkan bernilai 100. Dan game jika hanya ditampilkan di terminal output maka pada awal game terdapat kalimat "Selamat datang di Game Dikejar Deadline!" dan "Kumpulkan 10 tugas dalam waktu 60 detik." selain itu terdapat juga tampilan sisa waktu dan tugas yang terkumpul, untuk mengumpulkan tugasnya pemain harus mengetikkan kata (hijau, biru, merah, kuning, putih) misal mengetik kata putih maka tugas terkumpul 1 dan sisa waktu akan ditampilkan, jika waktunya habis maka game selesai.
## 3. Branding game
- Nama Game = Dikejar Deadline 
- Tareget pengguna =
  - Game ini bisa dimainkan dari kalangan anak-anak sampai dewasa
- Genre 
## 4. User Story
Sebagai | Saya ingin bisa | Sehingga | Prioritas
---|---|---|---
Pengguna | Menggerakan player | Player bisa bergerak | ⭐⭐⭐⭐⭐
Pengguna | Mengambil objek | Player bisa mengumpulkan objek |  ⭐⭐⭐⭐⭐
Sistem | Set timer | Bisa set timer kapan game dimulai dan berakhir | ⭐⭐⭐⭐
Sistem | Membuat hambatan | Mempersulit player untuk memenangkan game | ⭐⭐
## 5. Desain User Interface
![WhatsApp Image 2023-12-16 at 17 18 06_607d2410](https://github.com/DesmiaWardah/2324-praktikum-dasar-pemograman/assets/144568328/230e64ec-bd73-4153-ba2e-85ce92cc12be)

## 6. Flowchart

## 7. Link Demo game

## 8. Kode Pemograman Game

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






