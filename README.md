## Tutorial 10
Nama: Syifa Kaffa Billah

NPM: 2206816430

Kelas: C

### Result of Execution<br>
![img1.png](img%2Fimg1.png)

Output di atas menunjukkan bahwa "hey hey" di-print sebelum "howdy!" dan "done!" karena pada kode program, fungsi `main` 
menjalankan perintah print "hey hey" terlebih dahulu yang dilanjutkan dengan menjalankan dua perintah print yang ada 
pada antrean queue di executor.

### Multiple Spawn<br>
![multiple_spawn.png](img%2Fmultiple_spawn.png)
### Tanpa menggunakan kode: `drop(spawner);`<br>
![without_drop.png](img%2Fwithout_drop.png)
### Kembali menggunakan kode: drop(spawner);`<br>
![put_drop_again.png](img%2Fput_drop_again.png)

Dari hasil percobaan tersebut, dapat dilihat bawha saat menjalankan multiple spawn, semua task yang di-spawn akan 
dieksekusi secara bersamaan. Dalam kode program, ada sebuah timer yang menunda pencetakan semua string "done" selama 
2 detik. Oleh karena itu, program akan mencetak semua string "howdy" terlebih dahulu sebelum melanjutkan dengan mencetak 
semua string "done". Jika statement `drop(spawner)` dihapus, program akan tetap berjalan seperti biasanya, namun tidak 
akan selesai karena fungsi `drop(spawner)` itu sendiri adalah untuk memberi tahu program bahwa tidak akan ada lagi task 
yang ditambahkan ke executor. Dengan demikian, jika `drop(spawner)` dihapus, program akan terus menunggu kedatangan task 
baru.