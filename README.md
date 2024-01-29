<table>
  <tr>
    <th colspan="2">DATA MAHASISWA</th>
  </tr>
  <tr>
    <td>Nama</td>
    <td>Muhammad Arifin</td>
  </tr>
  <tr>
    <td>NIM</td>
    <td>312210330</td>
  </tr>
  <tr>
    <td>Kelas</td>
    <td>TI.22.A3</td>
  </tr>
  <tr>
    <td>Mata Kuliah</td>
    <td>Pemrograman Mobile</td>
  </tr>
</table>


Terdapat 7 menu pada aplikasi, diantaranya:
###  1. **Hello** <br>
Ini adalah program yang hanya menampilkan teks pada aplikasi. Disini teksnya adalah "Bagaimana kabar anda hari ini?". <br>

Metode Utama:

-  ```onCreate```: Menginisialisasi dan menetapkan tata letak (layout) dengan menggunakan ```setContentView```.

Fungsi Utama: Menampilkan Layout:

- Kode ini bertujuan untuk menampilkan layout dengan nama ```activity_hello``` ke pengguna.

Catatan:

- Kode ini adalah contoh sederhana dari sebuah aktivitas di Android yang menggunakan layout untuk menampilkan antarmuka pengguna.

- Aktivitas ini tidak memiliki interaksi pengguna tambahan, karena hanya menampilkan layout yang telah ditentukan (```activity_hello```).

- Sangat penting untuk memastikan bahwa file layout yang disebutkan dalam setContentView (```activity_hello```) tersedia dan telah dikonfigurasi sesuai kebutuhan aplikasi.


### 2. **Count** <br>
Count adalah program yang menampilkan perhitungan tambah 1 bisa juga disebut program Toast.

Metode Utama:

- ```onCreate```: Menginisialisasi tata letak (layout) dan komponen-komponen yang diperlukan.
- ```countUp```: Menaikkan nilai hitungan dan menampilkan pada TextView.
- ```showToast```: Menampilkan pesan Toast saat tombol diklik.

Fungsi Utama:

- Inisialisasi:

  - ```onCreate``` digunakan untuk menginisialisasi aktivitas dan menetapkan layout (```activity_count```) serta mendapatkan referensi ke TextView (```show_count```).
  - Penjumlahan dan Tampilan:
  - ```countUp``` digunakan untuk menambah nilai hitungan (currentCount) dan menampilkan pada ```TextView``` (```show_count```).
  - Pesan Toast:
  - ```showToast``` menampilkan pesan Toast dengan pesan yang diambil dari sumber daya string (```R.string.toast_message```).

Catatan:

- ```currentCount``` digunakan untuk menyimpan nilai hitungan saat ini.
- Fungsi ```countUp``` digunakan untuk meningkatkan nilai hitungan dan memperbarui tampilan pada TextView.
- Fungsi ```showToast``` digunakan untuk menampilkan pesan Toast yang berasal dari sumber daya string.

### 3. **Maps** <br>
Maps adalah program yang menampilkan tampilan maps dari aplikasi Google Maps, program ini menerapkan fungsi Implisit. Implisit intent memungkinkan Anda meminta sistem Android untuk menemukan aplikasi yang sesuai untuk menangani tugas tertentu, dalam hal ini menunjukkan lokasi di peta.

- Metode ```onCreate```:
  - Dipanggil saat aktivitas dibuat.
  - Mengatur tata letak tampilan dan menyiapkan data lokasi geografis.
  - Membuat Uri dengan data lokasi latitude dan longitude.
  - Memanggil ```showMap``` untuk menampilkan peta dengan lokasi yang telah ditentukan.

- Metode ```showMap```:
  - Membuat Intent dengan tindakan ```ACTION_VIEW```.
  - Mengatur data intent ke Uri yang mewakili lokasi geografis.
  - Memeriksa keberadaan aplikasi yang dapat menangani intent untuk menampilkan peta.
  - Jika ada aplikasi yang dapat menangani intent, aktivitas baru dimulai untuk menampilkan lokasi pada peta.

- Catatan Tambahan:

  - Intent ```ACTION_VIEW```: Digunakan untuk meminta sistem untuk menampilkan data.
  - ```Uri.parse```: Membuat objek Uri yang mewakili lokasi geografis.

### 4. **News** <br>
News adalah program yang menampilkan tampilan seperti Artikel dari sebuah berita. Berita disini adalah tentang **"Ice Cold"**.


Metode Utama:
- ```onCreate```: Menginisialisasi aktivitas dan menetapkan tata letak (layout) yang diberikan oleh ```activity_icecold```.

Fungsi Utama:

- Inisialisasi:
  - ```onCreate``` digunakan untuk menginisialisasi aktivitas dan menetapkan layout (```activity_icecold```) yang berisi tampilan berita.

Tampilan Berita:

- Aktivitas ini bertujuan untuk menampilkan tampilan berita yang diatur dalam layout ```activity_icecold```.

Pembaruan dan Rekomendasi:

- Menambahkan komponen-komponen UI atau fungsionalitas tambahan sesuai kebutuhan aplikasi.
- Menggunakan komponen Android seperti ```TextView```, ```ImageView```, atau ```WebView``` untuk menampilkan konten berita yang lebih dinamis.


### 5. **Alarm** <br>
Alarm adalah program yang menampilkan alarm menggunakan fungsi dari **AlarmManager**. **AlarmManager** adalah komponen sistem Android yang memungkinkan Anda menjadwalkan dan mengeksekusi kode pada waktu tertentu, baik itu dalam waktu segera, satu kali, atau berulang.

Metode Utama:

- ```onCreate```: Menginisialisasi ```TimePicker``` dan ```AlarmManager```.
    
- ```OnToggleClicked```: Mengelola fungsi alarm saat tombol toggle diubah.
    
Fungsi Utama:

- Setting Alarm:
  - Membuat objek Calendar untuk mendapatkan waktu saat ini dalam jam dan menit.
        
  - Menetapkan jam dan menit pada objek Calendar berdasarkan TimePicker.
        
  - Membuat objek Intent untuk memanggil AlarmReceiver saat alarm berbunyi.
        
  - Membuat objek PendingIntent untuk memanggil siaran tertunda saat alarm berbunyi.
        
  - Mengatur waktu alarm menggunakan AlarmManager.setRepeating.
        
  - Jika waktu saat ini lebih besar dari waktu alarm yang diatur, penyesuaian waktu dilakukan untuk alarm keesokan harinya.
        
  - Alarm berbunyi terus-menerus sampai tombol toggle dimatikan.

- Mematikan Alarm:
  - Membatalkan alarm menggunakan AlarmManager.cancel saat tombol toggle dimatikan.

Pesan Log:

- Menampilkan pesan toast "ALARM ON" saat tombol toggle dihidupkan.
- Menampilkan pesan toast "ALARM OFF" saat tombol toggle dimatikan.


### 6. **Fibonacci** <br>
Fibonacci Sequence (Deret angka Fibonacci) adalah deret angka yang diperoleh dengan menjumlahkan dua angka didepannya / sebelumnya:<br>

      1, 1, 2, ... 1 + 2 = 3 ( 1, 1, 2, 3, ... ) 2 + 3 = 5 ( 1, 1, 2, 3, 5, ... ) 3 + 5 = 8 ( 1, 1, 2, 3, 5, 8, ... )

- Mode Perhitungan
Terdapat 2 Mode pada aplikasi fibonacci tersebut yakni:<br>
  - Limited-Mode : harus memasukkan limit/batas terlebih dahulu baru bisa melakukan perhitungan.
  - Unlimited-Mode : tanpa harus memasukkan limit/batas untuk melakukan perhitungan.<br>

- Limit/Batas Perhitungan 
Arti limit/Batas disini adalah User bisa membatasi perhitungan fibonacci dibaris keberapa contoh user menginputkan 12 maka perhitungan fibonacci akan berhenti pada nilai 144 karna nilai 144 adalah baris ke-12 dalam perhitungan fibonacci.<br>

- Perhitungan Naik (Count Up) dan Perhitungan Turun (Count Down)  
Yaitu perhitungan bisa dilakukan naik (Count Up) dan Perhitungan bisa dilakukan menurun (Count Down), maksudnya adalah pada saat user melakukan perhitungan naik smpai nilai 21 daln jika user melakukan perhitungan turun sekali maka akan mundur satu baris, nilainya menjadi 13 karna nilai sebelum 21 adalah 13.<br>

- Reset
Yaitu semua nilai terkait Fibonacci diatur kembali ke nilai awal, dan tampilan diperbarui.<br>

### Tampilan UI
    Saya mempunyai 3 button dan 1 edit text :
    - edit text untuk user dapat menginput memberikan maksimal angka fibonacci
    - button max untuk membatasi angka maksimal yg sudah di input pada edit text
    - button count untuk menambah angka fibonacci untuk mencapai nilai maksimalnya
    - button back untuk mereset angka fibonacci dan inputan max menjadi 0

Penjelasan Menampilkan Angka Fibonacci

    Membuat Objek Toast:
    Toast adalah suatu fitur di Android yang digunakan untuk menampilkan Angka Fibonacci ditengah layar.
    Toast.makeText(this, R.string.toast_message, Toast.LENGTH_SHORT); membuat pesan dengan durasi singkat. 
    Pesan yang ditampilkan diambil dari resource string yang diidentifikasi oleh R.string.toast_message.

    Menampilkan Toast:
        toast.show(); digunakan untuk menampilkan Toast yang telah dibuat sebelumnya.

    Mengatur Teks pada Elemen Tampilan:
        showHitung.setText(Integer.toString(1)); Menampilkan Angka Fibonacci menjadi "1" pada saat awal.
        Integer.toString(1) digunakan untuk mengonversi angka 1 menjadi string, karena setText membutuhkan parameter berupa string.

Penjelasan ButtonMax

    Mengambil Teks dari Elemen Tampilan:
    inputCount.getText().toString(); mengambil teks dari EditText yang telah di input user dan menyimpannya dalam bentuk string.

    Memeriksa String Tidak Kosong:
        if (!maxCountString.isEmpty()) memeriksa apakah EditText tidak kosong. Jika tidak kosong, maka melanjutkan ke langkah berikutnya.

    Mengonversi String ke Integer:
        int newMaxCount = Integer.parseInt(maxCountString); mengonversi string yg telah di input di EditText menjadi integer (bilangan bulat).

    Memeriksa Nilai Integer Baru:
        if (newMaxCount >= 0) memeriksa apakah nilai integer baru tidak kurang dari 0.

    Mengatur Nilai Maksimum (maxCount):
        maxCount = newMaxCount; jika semua kondisi terpenuhi, nilai maksimum (maxCount) diatur menjadi nilai integer baru (newMaxCount).

Penjelasan ButtonBack

    fib1 dan fib2 diatur ke 1
        fib1 dan fib2 membuat bilangan yg sudah ditambah menjadi 1.

    maxCount diatur ke 0.
       batas maksimum Angka Fibonacci menjadi 0.

    maxCountSet diatur ke false.
       batas maksimum angka Fibonacci menjadi false atau belum dimasukkan
       
    Teks pada elemen inputCount dikosongkan.
        Mengosongkan EditText atau inputan maksimal untuk angka Fibonacci

    Teks pada elemen showHitung diatur menjadi "0".
       Menampilkan Angka Fibonacci menjadi 0

Penjelasan ButtonCount

    Mengambil Nilai Input:
        maxCountString mengambil nilai input dari EditText yang telah di input.

    Memeriksa Input Tidak Kosong:
        Memeriksa apakah EditTExt tidak kosong.

    Mengonversi Input menjadi Integer:
        Mengonversi nilai Inputan maksimalnya menjadi integer.

    Menghitung Fibonacci Berikutnya:
        Menghitung nilai Fibonacci berikutnya (nextFib).

    Memeriksa Kondisi:
        Melakukan beberapa pengecekan kondisi terkait nilai maxCount, fib1, dan nextFib.

    Memperbarui Nilai dan Menampilkan:
        Memperbarui nilai fib1 dan fib2 tergantung pada kondisi.
        Menampilkan nilai terbaru pada elemen tampilan showHitung.


- Tampilan Baris Fibonacii  
Yaitu menampilkan baris berapa dalam perhitungan fibonacci saat ini.


### 7. **Chat** <br>
Chat adalah program yang terdapat 2 fungsi yaitu mengirim pesan dan membalas pesan tetapi ini hanya implementasi dari program **Two Activity**.

- Variabel Kelas:
  - ```LOG_TAG```: Variabel konstan yang digunakan untuk tag log.
  - ```EXTRA_MESSAGE```: Variabel konstan yang berfungsi sebagai kunci untuk menyimpan pesan ekstra dalam Intent.
  - ```TEXT_REQUEST```: Konstanta yang menentukan kode permintaan untuk startActivityForResult.
  - ```mMessageEditText```: EditText untuk memasukkan pesan.
  - ```mReplyHeadTextView```: TextView untuk menampilkan header balasan.
  - ```mReplyTextView```: TextView untuk menampilkan balasan.

- Metode ```onCreate```:
  - Menginisialisasi tampilan dan variabel kelas.

- Metode ```launchSecondActivity```:
  - Dipanggil ketika tombol di ```MainActivityOne``` diklik.
  - Membuat Intent untuk memulai ```SecondActivity``` dengan membawa pesan dari ```mMessageEditText```.
  - Memulai aktivitas kedua dengan ```startActivityForResult``` untuk mendapatkan hasil balasan.

- Metode ```onActivityResult```:
  - Dipanggil ketika aktivitas kedua selesai.
  - Memeriksa apakah permintaan adalah ```TEXT_REQUEST``` dan hasilnya adalah ```RESULT_OK```.
  - Menampilkan header balasan dan menetapkan teks balasan ke ```mReplyTextView```.
    

### 8. **Movie** <br>
Movie adalah program yang dibuat untuk mengimplementasikan fungsi **Fragment** dalam program movie yang saya buat ini terdapat beberapa Fragment dan fitur, diantaranya:<br>
**Menu-Buttom**<br>

Komponen Utama

- TabLayout (```tabLayout```):
  - Digunakan untuk menampilkan tab yang mewakili setiap fragment.
  - Didefinisikan dalam layout dengan ID ```tablayout```.

- ViewPager (```viewPager```):
  - Digunakan untuk menampilkan dan mengelola fragment.
  - Didefinisikan dalam layout dengan ID ```viewpager```.

- VPAdapter (```vpAdapter```):
  - Kelas yang mengg extends ```FragmentPagerAdapter```.
  - Digunakan untuk menghubungkan ```ViewPager``` dengan fragment dan menangani navigasi antar fragment.

- Fragment1, Fragment2, dan Fragment3:
  - Fragmen yang masing-masing mewakili kategori Eyeliner, Lipcream, Eyebrow.

- **Home**<br>
    adalah fragment yang menampilkan tampilan utama yang berisikan poster-poster dari sebuah film.

**Menu-Sidebar**
- **Home**<br>
    adalah fragment yang menampilkan tampilan utama yang berisikan poster-poster dari sebuah film.

- **Settings**<br>
    adalah fragment yang berisikan pengaturan sistem apliksi dan pengaktifan fitur dan lain sebagainya.
  Komponen Utama

- TabLayout (```tabLayout```):
  - Digunakan untuk menampilkan tab yang mewakili setiap fragment.
  - Didefinisikan dalam layout dengan ID ```tablayout```.

- ViewPager (```viewPager```):
  - Digunakan untuk menampilkan dan mengelola fragment.
  - Didefinisikan dalam layout dengan ID ```viewpager```.

- VPAdapter (```vpAdapter```):
  - Kelas yang mengg extends ```FragmentPagerAdapter```.
  - Digunakan untuk menghubungkan ```ViewPager``` dengan fragment dan menangani navigasi antar fragment.

- Fragment1, Fragment2, dan Fragment3:
  - Fragmen yang masing-masing mewakili kategori Eyeliner, Lipcream, Eyebrow.

- **Home**<br>
    adalah fragment yang menampilkan tampilan utama yang berisikan poster-poster dari sebuah film.

https://github.com/marifinnnnn/UAS-pemrograman-mobile/assets/115518274/43b2cc3a-6f53-4c43-9fe8-74dc72ce80ee



**Menu-Sidebar**
- **Home**<br>
    adalah fragment yang menampilkan tampilan utama yang berisikan poster-poster dari sebuah film.

- **Settings**<br>
    adalah fragment yang berisikan pengaturan sistem apliksi dan pengaktifan fitur dan lain sebagainya.


  
