<h1 align="center"><b>TUGAS 7</b></h2>

<h1 align="center"><b>Pemrosesan Citra Digital</b></h2>

### __KELOMPOK 10 :__
- Khoyrur Roykhan
- Delphia Aryana
- Naila Hasanah
<hr>
<br>

### __LOW-PASS FILTERING & HIGH-PASS FILTERING__

<br>

### __1. Low-Pass Filtering__

<p align="justify">&ensp;&ensp;&ensp;&ensp;Low-pass filtering adalah proses filter yang melewatkan komponen citra dengan nilai intensitas yang rendah dan meredam komponen citra dengan nilai intensitas yang tinggi. Low pass filter akan menyebabkan citra menjadi lebih halus dan lebih blur.</p>

Aturan kernel untuk low-pass filter adalah:
1. Semua koefisien kernel harus positif
2. Jumlah semua koefisien kernel harus sama dengan 1

Contoh kernel  yang dapat digunakan pada low-pass filtering adalah

<p align="center"><img width="700" src="img/kernel low pass.jpg"></p>

Low-pass filtering menggunakan kernel (iii) disebut juga neighborhood averaging. 

Contoh perintah untuk melakukan low-pass filtering adalah:

<p align="center"><img width="700" src="img/kode.png"></p>

Hasil :

- Citra Asli
<p align="center"><img width="500" src="img/figure1.png"></p>

- Citra Menggunakan Kernel 1
<p align="center"><img width="500" src="img/figure2.png"></p>

- Citra Menggunakan Kernel 2
<p align="center"><img width="500" src="img/figure3.png"></p>

- Citra Menggunakan Kernel 3
<p align="center"><img width="500" src="img/figure4.png"></p>