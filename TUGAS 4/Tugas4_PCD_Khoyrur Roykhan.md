<h1 align="center"><b>TUGAS 4</b></h2>

<h1 align="center"><b>Pemrosesan Citra Digital</b></h2>

<br>

## __Algoritma Patterning, Difhtering, dan Bit Plane Slacing__

### __1. Algoritma Patterning__

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

for x (x = 1 ; 1 ; length.A) //-------> untuk mengakses baris dari 1, dengan update +1 sampai panjang A
    for y (y = 1 ; 1 ; length.A) //-------> untuk mengakses kolom dari 1, dengan update +1 sampai panjang A
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
