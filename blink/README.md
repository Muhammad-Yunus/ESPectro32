# Blink menggunakan ESPectro32

ESPEctro32 memiliki LED onborad yang terhubung ke IO15 ESP32. Posisi LED tersebut ada di dekat tombol reset ESPectro32. ESPectro32 akan diprogram dengan menggunakan framework Arduino. Struktur program yang digunakan sama seperti yang terdapat pada Arduino IDE.   

### Alat dan Bahan

  - ESPectro32 
  - Kabel data
  - [PlatformIO] untuk Atom

### Langkah-Langkah:
  1) Pada sidebar Atom Editor, klik icon Home untuk membuka PlatformIO home. 

  2) Klik tombol (+ New Project) Disisi kanan PlatformIO home untuk menambahkan proyek baru.
![N|solid](https://lh5.googleusercontent.com/JNO5VHHm_w0FZNwEDgStMYAOSWa_g-1mvM2QzKdroqIusr_0cOJv7avimos7BWPGAJby62wr2vk80ZZ9WUs-=w1317-h670)

  3) Setelah itu akan muncul Project Wizard untuk menambahkan project baru. Pilih Board, arahkan ke ESPectro32 (DycodeX) dan isian framework dengan Arduino. Setelah itu klik Finish.
![N|solid](https://lh3.googleusercontent.com/2wFt7BXcGz8U9YcVdrt873BUkN5eRlsyl8WzVMrnXpHuBZdLca7GoGUr41Mxq1fIK5rsO3A-a1gvWy17BAjy=w1317-h670)

  4) Project yang berhasil di tambahkan bisa dilihat di sisi bawah PlatformIO home. Klik tanda plus diawalan list project untuk melihat lokasi penyimpanan project yang telah dibuat.
  ![N|solid](https://lh3.googleusercontent.com/m-s_fIjuqWppKf8rix4cIXgkFL9SVJhPf8ihd01OBsgaP8eLDv6C4x4swyZ3P29ChAp18_C6wqzlC3KRFKtB=w1317-h670)
  
 5) Jika pada list project (sisi kiri) Editor Atom project tidak langsung terbuka, kita dapat membukanya secara manual pada menubar. Pilih File > Add Project Folder, arahkan pada folder project sesuai dengan yang terdapat pada langkah 4. Setelah itu pada list Project bisa terlihat project baru yang telah dibuat.
 ![N|solid](https://lh3.googleusercontent.com/hxppQ-OVXsK5DaSohNLawCSLy-rztxTc6szaWQjqFF5w-AddB69-7V6lA6HqcQQSFBuWPAR2O96SLff-w1Qz=w1317-h670)
 
 6) Buka folder src pada project yang dibuat dan double click pada file program main.cpp. Ini akan mengarahkan kita pada tab program utama. 
 ![N|solid](https://lh6.googleusercontent.com/o67p_D8Y5iZyhViVx-Oh-a4856-2r1ZcVVsPhCmXMHgnVqrKC4gAah3X7oS2jdiwkQ7w1JzjlfCFEtz9s4_R=w1317-h670)
 
 7) Masukan program blink berikut dan atur pin nya menjadi pin 15 (ESPectro32 default pin di pin 15).
     ```c++
    #include <Arduino.h>
    #define PIN_LED 15
    
    void setup(){
        pinMode(LED_PIN, OUTPUT);
    }
    void loop(){
        digitalWrite(LED_PIN, HIGH);
        delay(1000);
        digitalWrite(LED_PIN, LOW);
        delay(1000);
    }
    ```
 8) Hubungkan ESPectro32 ke komputer via USB dengan menggunakan kabel USB data.

 9) Setelah itu pada side pannel Atom Editor klik Tombol Build dan dilanjutkan tombol Upload untuk memasukan program yang telah dibuat.
 ![N|Solid](https://lh4.googleusercontent.com/mq_liyk2y1Qhv_n6aJm88pN72rqk1lY0bU6DF_4Mr5tGjh8ObkhY4LGz1Kue_mhQzEXvHwEcYeUCNvsq0VEB=w1317-h670)
10) Led pada ESPectro32 akan mengedip dalam periode 1 detik.

   [PlatformIO]: <http://docs.platformio.org/en/latest/ide/atom.html#installation>

