<h1 align="center"><b>TUGAS 4</b></h2>

<h1 align="center"><b>Pemrosesan Citra Digital</b></h2>

<br>

## __Algoritma Patterning, Difhtering, dan Bit Plane Slacing__

### __1. Pseudo Algoritma Patterning__

Misal menggunakan Pola 3x3 :
```java

pola_0 = [
    [0 0 0], 
    [0 0 0], 
    [0 0 0]
    ]; //-----> nilai 0-25

pola_1 = [
    [0 0 0], 
    [0 0 0], 
    [0 0 1]
    ]; //-----> nilai 26-51

pola_2 = [
    [1 0 0], 
    [0 0 0], 
    [0 0 1]
    ]; //-----> nilai 52-77

pola_3 = [
    [1 0 1], 
    [0 0 0], 
    [0 0 1]
    ]; //-----> nilai 78-103

pola_4 = [
    [1 0 1], 
    [0 0 0], 
    [1 0 1]
    ] //-----> nilai 104-129

pola_5 = [
    [1 0 1], 
    [0 0 0], 
    [1 1 1]
    ]; //-----> nilai 130-155

pola_6 = [
    [1 0 1], 
    [1 0 0], 
    [1 1 1]
    ]; //-----> nilai 156-181

pola_7 = [
    [1 0 1], 
    [1 0 1], 
    [1 1 1]
    ]; //-----> nilai 182-207

pola_8 = [
    [1 1 1], 
    [1 0 1], 
    [1 1 1]
    ]; //-----> nilai 208-233

pola_9 = [
    [1 1 1], 
    [1 1 1], 
    [1 1 1]
    ]; //-----> nilai 234-259


A = [
    0     65
    100   222
]

Kemudian Matriks akan di perbesar 3x3 :

Pattern_A = [
    ...  ...  ...  ...  ... ...;
    ...  ...  ...  ...  ... ...;
    ...  ...  ...  ...  ... ...;
    ...  ...  ...  ...  ... ...;
    ...  ...  ...  ...  ... ...;
    ...  ...  ...  ...  ... ...;
]

for x (x = 1 ; 1 ; A.length) //-------> untuk mengakses baris dari 1, dengan update +1 sampai panjang A
    for y (y = 1 ; 1 ; A.length) //-------> untuk mengakses kolom dari 1, dengan update +1 sampai panjang A
        if A[x,y] >= 0 and <=25 ;
            Pattern_A[(x*3)-2 : x*3, (y*3)-2 : y*3,] = pola_0;
            // jika nilai matriks pada posisi A[x,y] >= 0 dan <=25 maka
            // Pattern_A pada posisi[baris (x*3)-2 sampai x*2 , dan kolom (y*3)-2 sampai y*3]
            // akan diisi pola 0
        
        else if A[x,y] >= 26 and <=51 ;
            Pattern_A[(x*3)-2 : x*3, (y*3)-2 : y*3,] = pola_1;
            // jika nilai matriks pada posisi A[x,y] >= 26 dan <=51 maka
            // Pattern_A pada posisi[baris (x*3)-2 sampai x*2 , dan kolom (y*3)-2 sampai y*3]
            // akan diisi pola 1
        
        else if A[x,y] >= 52 and <=77 ;
            Pattern_A[(x*3)-2 : x*3, (y*3)-2 : y*3,] = pola_2;
            // jika nilai matriks pada posisi A[x,y] >= 52 dan <=77 maka
            // Pattern_A pada posisi[baris (x*3)-2 sampai x*2 , dan kolom (y*3)-2 sampai y*3]
            // akan diisi pola 2
        
        else if A[x,y] >= 78 and <=103 ;
            Pattern_A[(x*3)-2 : x*3, (y*3)-2 : y*3,] = pola_3;
            // jika nilai matriks pada posisi A[x,y] >= 78 dan <=103 maka
            // Pattern_A pada posisi[baris (x*3)-2 sampai x*2 , dan kolom (y*3)-2 sampai y*3]
            // akan diisi pola 3
        
        else if A[x,y] >= 104 and <=129 ;
            Pattern_A[(x*3)-2 : x*3, (y*3)-2 : y*3,] = pola_4;
            // jika nilai matriks pada posisi A[x,y] >= 104 dan <=129 maka
            // Pattern_A pada posisi[baris (x*3)-2 sampai x*2 , dan kolom (y*3)-2 sampai y*3]
            // akan diisi pola 4
        
        else if A[x,y] >= 130 and <=155 ;
            Pattern_A[(x*3)-2 : x*3, (y*3)-2 : y*3,] = pola_5;
            // jika nilai matriks pada posisi A[x,y] >= 130 dan <=155 maka
            // Pattern_A pada posisi[baris (x*3)-2 sampai x*2 , dan kolom (y*3)-2 sampai y*3]
            // akan diisi pola 5

        else if A[x,y] >= 156 and <=181 ;
            Pattern_A[(x*3)-2 : x*3, (y*3)-2 : y*3,] = pola_6;
            // jika nilai matriks pada posisi A[x,y] >= 156 dan <=181 maka
            // Pattern_A pada posisi[baris (x*3)-2 sampai x*2 , dan kolom (y*3)-2 sampai y*3]
            // akan diisi pola 6

        else if A[x,y] >= 182 and <=207 ;
            Pattern_A[(x*3)-2 : x*3, (y*3)-2 : y*3,] = pola_7;
            // jika nilai matriks pada posisi A[x,y] >= 182 dan <=207 maka
            // Pattern_A pada posisi[baris (x*3)-2 sampai x*2 , dan kolom (y*3)-2 sampai y*3]
            // akan diisi pola 7

        else if A[x,y] >= 208 and <=233 ;
            Pattern_A[(x*3)-2 : x*3, (y*3)-2 : y*3,] = pola_8;
            // jika nilai matriks pada posisi A[x,y] >= 208 dan <=233 maka
            // Pattern_A pada posisi[baris (x*3)-2 sampai x*2 , dan kolom (y*3)-2 sampai y*3]
            // akan diisi pola 8
        
        else if A[x,y] >= 234 and <=259 ;
            Pattern_A[(x*3)-2 : x*3, (y*3)-2 : y*3,] = pola_9;
            // jika nilai matriks pada posisi A[x,y] >= 156 dan <=181 maka
            // Pattern_A pada posisi[baris (x*3)-2 sampai x*2 , dan kolom (y*3)-2 sampai y*3]
            // akan diisi pola 9
```

### ____2. Pseudo Algoritma Dithering____

Misal Batasnya adalah :
```java
D = [
    [0 128],
    [192 64]
    ]
 
kemudian misal matriksnya :

A = [
    [0 123 32 160], 
    [192 64 224 96], 
    [48 176 16 144], 
    [240 112 208 80]
    ]

for  all x & y do
      if f(x,y) > m(x,y) then
            g(x,y) = white
      else 
            g(x,y) = black
      end if
End for

    [0 123  | 32 160] 
    [192 64 | 224 96] 
    -----------------
    [48 176 | 16 144] 
    [240 112| 208 80]

//setiap blok dari matriks tersebut akan di bandingkan dengan batas D yang telah di tentukan
//jika batas lebih besar dari matriknya, maka akan menjadi warna putih (1)
//jika lebih kecil maka akan menjadi warna hitam (0)
```

### __3. Pseudo Algoritma Bit Plane Slacing__
```java
A = [
    100 245; 
    80 65
    ]

untuk mengubah matriks tersebut menjadi biner, dapat menggunakan fungsi bitget pada octave

for x = 1:2
    for y = 1:2
        printf(bitget(A(x,y),8:-1:1));
        //untuk mengubah nilai dari A posisi (x,y) menjadi biner
        //dan menampilkannya dari element ke 8 sampai 1,
        //karena jika tidak dibalik nilai biner tersebut akan berbeda
        printf(" ");
        endfor
    printf("\n");
    endfor
```
Hasil :
<p align="center"><img width="250" src="img/hasil bit.png"></p>

```java
for x = 1:2
    for y = 1:2
        print(bitget(A(x,y),1)); //-----------> untuk menampilkan layer 1 saja
        //jika ingin menampilkan layer lainnya, tinggal ganti angka 1 dengan angka layer yang diinginkan
        printf(" ");
        endfor
    printf("\n");
 endfor
```

Hasil :

<p align="center"><img width="100" src="img/hasil bit layer.png"></p>


### __4. Pseudo Algorimta Histogram-Equalized__

Misal :
```java
Gray_level  = [0  1 2 3 4  5 6 7]
               ^  ^ ^ ^ ^  ^ ^ ^
               |  | | | |  | | |
No_of_pixel = [10 8 9 2 14 1 5 2]

sum_0 = No_of_pixel[0]
sum_1 = sum_0+No_of_pixel[1]
sum_2 = sum_1+No_of_pixel[2]
sum_3 = sum_2+No_of_pixel[3]
sum_4 = sum_3+No_of_pixel[4]
sum_5 = sum_4+No_of_pixel[5]
sum_6 = sum_5+No_of_pixel[6]
sum_7 = sum_6+No_of_pixel[7]


run_sum = [sum_0 sum_1 sum_2 sum_3 sum_4 sum_5 sum_6 sum_7]
//jadi  = [10 18 27 29 43 44 49 51]

normalized = [sum_0/sum7, sum_1/sum7, sum_2/sum7, sum_3/sum7, sum_4/sum7, sum_5/sum7, sum_6/sum7, sum_7/sum7]
// jadi    = [10/51 18/51 27/51 29/51 43/51 44/51 51/51]

multiply_7 = []

for (int x = 0 ; x < Gray_level.length ; x++)
    multiply_7[x] = normalized[x]*(Gray_level.length-1) //--------> (Gray_level.length-1) = 8-1 = 7
    //Hasilnya dibulatkan.

// multiply_7 menjadi [1  2 4 4 6  6 7 7]
                       ^  ^ ^ ^ ^  ^ ^ ^
                       |  | | | |  | | |
// No_of_pixel   =    [10 8 9 2 14 1 5 2]

Histogram-equalized Image =
Gray-level 0 = 0           
Gray-level 1 = 10
Gray-level 2 = 8
Gray-level 3 = 0
Gray-level 4 = 9 + 2 = 11
Gray-level 5 = 0
Gray-level 6 = 14 + 1 = 15
Gray-level 7 = 5 + 1 = 7

//jika nilai gray-level tidak ada di dalam multiply_7 maka akan diisi dengan nilai 0
//jika nilai gray-level di dalam multipy_7 lebih dari 1,
//maka No_of_pixel di indeks yang sama dengan gray_level akan dijumlahkan