<h1 align="center"><b>TUGAS 5</b></h2>

<h1 align="center"><b>Pemrosesan Citra Digital</b></h2>

<br>

## __Bit Plane Slacing dan Steganography__

### __1. Bit Plane Slacing__
- Penjelasan

<p align="justify">&ensp;&ensp;&ensp;&ensp;Secara digital sebuah gambar merupakan representasi dari sejumlah pixel. Pixel ini dapat diekspresikan lebih lanjut dalam bentuk bit. Bit-plane slicing merupakan metode yang digunakan untuk melihat konstribusi atau pengaruh tiap bit penyusun citra. Untuk citra 8 bit, pada dasarnya tiap intensitas yang nilainya dalam format decimal, bisa dipecah menjadi bit-bit dalam format biner. Misalnya, sebuah pixel dengan intensitas 245 (decimal) bila dijadikan biner adalah 11110101.</p>

<p align="center"><img width="800" src="img/bit8.png"></p>

Misalkan diberikan citra grayscale berukuran 2x2 dengan nilai matriks sebagai berikut : 

<p align="center"><img width="200" src="img/1.png"></p>

jika nilai di intensitas pixel diubah kedalam biner akan menghasilkan :

<p align="center"><img width="300" src="img/2.png"></p>

<p align="justify">&ensp;&ensp;&ensp;&ensp;Kemudian secara berurutan mengambil bit-bit untuk setiap intensitas dan dimasukan kedalam matriks baru. sehingga nanti akan mendapatkan 8 buah matriks baru yang berisi bit-bit urutan yang sama.</p>

<p align="center"><img width="600" src="img/3.png"></p>

<p align="justify">&ensp;&ensp;&ensp;&ensp;Tiap Matriks tersebut merupakan tiap slice dari sebuah gambar A. Tiap slice ini sudah menjadi citra biner dengan sendirinya. Tiap slice akan memberikan informasi dan menunjukan kontribusi dalam penyusun sebuah citra. A1 merupakan layer paling bawah dari gambar A (least significant), A8 merupakan layer paling atas dari gambar A (most significant).</p>