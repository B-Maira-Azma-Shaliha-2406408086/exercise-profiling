# Test Plan Screenshot

## all-students endpoint
### before optimization
![all-students.png](all-students.png)

### after optimization
![all-students-opt.png](all-students-opt.png)

## all-student-name endpoint
### before optimization
![all-student-name.png](all-student-name.png)

### after optimization
![all-student-name-opt.png](all-student-name-opt.png)

## highest-gpa endpoint
### before optimization
![highest-gpa.png](highest-gpa.png)

## after optimization
![highest-gpa-opt.png](highest-gpa-opt.png)

# Run JMeter via command line
I use 1 test plan for 3 endpoints so I just run it once.
![run-jmeter-cmd.png](run-jmeter-cmd.png)

Here's the result.
![testresults1.png](testresults1.png)

# Reflection
1. What is the difference between the approach of performance testing with JMeter and profiling with IntelliJ Profiler in the context of optimizing application performance?  
   JMeter itu buat ngetes performa dari luar secara keseluruhan (seperti simulasi banyak orang akses aplikasi barengan), sedangkan Profiler itu buat "bedah" kode dari dalam untuk cari baris mana yang bikin lambat atau boros memori.


2. How does the profiling process help you in identifying and understanding the weak points in your application?  
   Proses ini membantu karena dia mencatat semua yang dilakukan kode saat aplikasi jalan. Hasilnya kasih lihat kita data nyata, jadi kita bisa tahu persis fungsi mana yang paling banyak makan waktu tanpa perlu tebak-tebakan lagi.


3. Do you think IntelliJ Profiler is effective in assisting you to analyze and identify bottlenecks in your application code?  
   Sangat efektif karena dia punya tampilan visual (grafik) yang gampang dibaca. Kita bisa langsung lihat "leher botol" atau bagian yang menghambat aliran kode kita, jadi kita tahu bagian mana yang harus segera diperbaiki.


4. What are the main challenges you face when conducting performance testing and profiling, and how do you overcome these challenges?  
   Tantangan terbesarnya adalah hasil tes yang kadang nggak stabil karena pengaruh laptop atau sistem yang belum "panas". Solusinya, aplikasi harus dijalankan dulu beberapa kali (pemanasan) dan tutup aplikasi berat lain biar datanya lebih akurat.


5. What are the main benefits you gain from using IntelliJ Profiler for profiling your application code?  
   Manfaat paling berasa adalah fiturnya sudah jadi satu di tempat kita ngetik kode (IDE), jadi nggak perlu ribet pindah aplikasi. Selain itu, fiturnya lengkap buat bandingin performa sebelum dan sesudah kode diubah.


6. How do you handle situations where the results from profiling with IntelliJ Profiler are not entirely consistent with findings from performance testing using JMeter?  
   Kalau hasil JMeter dan Profiler beda, kita harus cek ulang lingkungannya. Biasanya ini terjadi karena perbedaan beban kerja. Solusinya adalah fokus dulu ke data Profiler untuk benerin kode yang jelas-jelas lambat, baru tes ulang lagi pakai JMeter buat mastiin performa luarnya juga naik.


7. What strategies do you implement in optimizing application code after analyzing results from performance testing and profiling? How do you ensure the changes you make do not affect the application's functionality?  
   Strateginya adalah fokus benerin bagian yang paling lambat dulu (berdasarkan data tadi), misalnya ganti cara gabung teks atau hapus jeda yang nggak penting. Biar fungsinya nggak rusak, kita harus jalankan unit testing atau tes fungsi setelah optimasi buat mastiin aplikasi masih jalan dengan benar seperti semula.****