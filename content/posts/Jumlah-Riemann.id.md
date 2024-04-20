---
author: ["Denai"]
title : 'Jumlah Riemann'
date : '2024-04-20'
# description: ""
# summary: ""
tags: ["jumlah riemann", "Integral"]
categories: ["jumlah riemann", "Integral"]
series: ["Integral"]
draft : true
ShowToc : true
TocOpen : false
math : true
ShowBreadCrumbs : true
---
Pada catatan sebelumnya kita telah mengetahui cara mencari estimasi luas daerah dibawah grafik dengan menggunakan jumlah berhingga. Dalam jumlah berhingga saya telah memberikan 2 cara dalam menentukan estimasi luas yakni dengan jumlah atas dan jumlah bawah. Jumlah berhingga tersebut lah yang mendasari Jumlah Riemann ini, ada beberapa perbedaan antara jumlah berhingga dan jumlah Riemann. Yakni : 

1. Jumlah Riemann dapat dikatakan lebih umum jika dibandingkan jumlah berhingga, dimana Jumlah Berhingga hanya untuk menghitung luas daerah diatas sumbu x, $f(x)\geq 0$ ( positif ) sedangkan Jumlah Riemann bisa digunakan untuk menghitung hasil kali luas dibawah sumbu x, $f(x)<0$ ( negatif ) serta menghitung estimasi luas diatas sumbu x.
2. Jumlah Riemann dapat menghitung luas dengan banyak sub-interval limit $n=\infty$, dimana jumlah berhingga hanya menggunakan beberapa bagian saja agar perhitungan tidak terlalu kompleks.
3. Jumlah Berhingga terbatas pada sub-interval yang sama panjang tetapi Jumlah Riemann dapat memiliki panjang sub-interval yang berbeda-beda dimana terdapat suatu sub-interval terbesar yang disebut dengan norma dari partisi $P$ atau dapat ditulis dengan $||P||$.

$||P||$ merupakan partisi atau sub-interval terbesar, dimana jika $P$ diperkecil maka sub-interval lain yang lebih kecil juga ikut mengecil.

$||P||$ berbeda dengan n. Dimana jika kita ingin menggunakan panjang interval yang sama , maka perhitungan semakin akurat ketika kita menggunakan $n$ sebanyak tak-hingga. Sedangkan ketika kita menggunakan panjang interval yang berbeda-beda, kita perlu mengecilkan $||P||$ menuju nol sehingga mencapai tingkat akurasi yang tinggi

Rumus umum :

$S_p = \sum_{k=1}^{n}f(c_k)\cdot \Delta x_k$

Rumus Jumlah Riemann :

- Batas kanan : $S_n = \sum_{k=1}^{n}f(a+k(\frac{b-a}{n}))\cdot (\frac{b-a}{n})$
- Batas kiri : $S_n = \sum_{k=1}^{n}f(a+(k-1)(\frac{b-a}{n}))\cdot (\frac{b-a}{n})$
- Titik tengah : $S_n = \sum_{k=1}^{n}f(a+(k-\frac{1}{2})(\frac{b-a}{n}))\cdot (\frac{b-a}{n})$

Pada rumus diatas, kita bisa memperoleh rumus lain. misalnya kita ingin mencari jumlah riemann untuk titik yang berada pada $\frac{1}{4}$  dari panjang interval ( disebelah kanan $\frac{1}{2}$ dan disebelah kiri 1). Maka kita hanya cukup mengganti nilai $k$  pada rumus menjadi $k-\frac{1}{4}$ begitu pula titik yang lainnya. Silahkan coba sendiri…

<aside>
💡 Remainder !

</aside>

- Variabel $k$  merupakan subinterval ke-$k$ dari seluruh interval.
- Variabel $c_k$ merupakan titik pada subinterval ke-$k$ yang digunakan dalam menghitung hasil kali luas
- $(\frac{b-a}{n})$ merupakan $\Delta x_k$ dimana itu merupakan panjang dari subinterval ke-$k$
- Variabel $P$ merupakan peubah yang merujuk pada partisi

Contoh Soal

1. Tentukan formula untuk Jumlah Riemann dengan membagi interval $[a,b]$ menjadi n sub-interval yang sama panjang dan gunakan titik ujung kanan untuk setiap $c_k$ kemudian ambil limit $n\rightarrow \infty$ untuk menghitung luas daerah dibawah kurvanya.
    1. $f(x)=x+x^2$ pada interval [0,1]
    2. $f(x)=x^2+1$ pada interval [0,3]
    
    Sebelum saya menyelesaikan dua soal diatas, saya perlu memberikan beberapa rumus yang mungkin akan sering kita gunakan.
    
    <aside>
    💡 Jumlah n bilangan bulat pertama : $\sum_{k=1}^{n}k=\frac{n(n+1)}{2}$
    
    </aside>
    
    <aside>
    💡 Jumlah kuadrat n bilangan bulat pertama :  $\sum_{k=1}^{n}k^2=\frac{n(n+1)(2n+1)}{6}$
    
    </aside>
    
    <aside>
    💡 Jumlah kubik n bilangan bulat pertama : $\sum_{k-1}^{n}k^3=(\frac{n(n+1)}{2})^2$
    
    </aside>
    
    Solution !
    
    1. $f(x)=x+x^2$ pada interval $[0,1]$
    
    Untuk mencari jumlah Riemann menggunakan titik tengah kita memerlukan rumus yang telah ada diatas untuk memudahkan kita.
    
    Batas kanan : $S_n = \sum_{k=1}^{n}f(a+k(\frac{b-a}{n}))\cdot (\frac{b-a}{n})$
    
    Yang diketahui dari soal : 
    
    $f(x)=x+x^2$
    
    $[a,b]=[0,1]$ 
    
    $\Delta x_k = \frac{b-a}{n}= \frac{1-0}{n}= \frac{1}{n}$
    

Substitusi nilai yang kita ketahui dari soal kedalam rumus batas kanan,

$S_n = \sum_{k=1}^{n}f(0+k(\frac{1-0}{n}))\cdot (\frac{1-0}{n})$

$\ \ \ \ \  \Leftrightarrow \sum_{k=1}^{n}f(\frac{k}{n})\cdot (\frac{1}{n})$

$\ \ \ \ \  \Leftrightarrow \sum_{k=1}^{n}(\frac{k}{n}+(\frac{k}{n})^2)\cdot (\frac{1}{n})$

$\ \ \ \ \  \Leftrightarrow \sum_{k=1}^{n}(\frac{k}{n}+\frac{k^2}{n^2})\cdot (\frac{1}{n})$

$\ \ \ \ \  \Leftrightarrow \sum_{k=1}^{n}\frac{k}{n^2}+\frac{k^2}{n^3}$

$\ \ \ \ \  \Leftrightarrow \sum_{k=1}^{n}\frac{k}{n^2}+\sum_{k=1}^{n}\frac{k^2}{n^3}$

$\ \ \ \ \  \Leftrightarrow \frac{1}{n^2}\sum_{k=1}^{n}k+\frac{1}{n^3}\sum_{k=1}^{n}k^2$

$\ \ \ \ \  \Leftrightarrow \frac{1}{n^2}\frac{n(n+1)}{2}+\frac{1}{n^3}\frac{n(n+1)(2n+1)}{6}$

$\ \ \ \ \  \Leftrightarrow \frac{1}{n^2}(\frac{n^2+n}{2})+\frac{1}{n^3}(\frac{2n^3+3n^2+n}{6})$

$\ \ \ \ \  \Leftrightarrow \frac{n^2+n}{2n^2}+\frac{2n^3+3n^2+n}{6n^3}$

$\ \ \ \ \  \Leftrightarrow \lim_{n\rightarrow \infty} \frac{n^2+n}{2n^2}+\frac{2n^3+3n^2+n}{6n^3}$

$\ \ \ \ \  \Leftrightarrow \lim_{n\rightarrow \infty} \frac{n^2+n}{2n^2}+\lim_{n\rightarrow \infty}\frac{2n^3+3n^2+n}{6n^3}$

$\ \ \ \ \  = \frac{1}{2}+\frac{2}{6}=\frac{5}{6}\approx 0.833...$

Substitusi $\frac{k}{n}$ kedalam fungsi $f(x)=x+x^2$

$\therefore$  jumlah Riemann dari $f(x)=x+x^2$ pada interval $[0,1]$ adalah $\approx 0.833...$

b. $f(x)=x^2+1$ pada interval $[0,3]$

Untuk mencari jumlah Riemann menggunakan titik tengah kita memerlukan rumus yang telah ada diatas untuk memudahkan kita.

Batas kanan : $S_n = \sum_{k=1}^{n}f(a+k(\frac{b-a}{n}))\cdot (\frac{b-a}{n})$

Yang diketahui dari soal : 

$f(x)=x^2+1$

$[a,b]=[0,3]$ 

$\Delta x_k = \frac{b-a}{n}= \frac{3-0}{n}= \frac{3}{n}$

Substitusi nilai yang kita ketahui dari soal kedalam rumus batas kanan,

$S_n = \sum_{k=1}^{n}f(0+k(\frac{3-0}{n}))\cdot (\frac{3-0}{n})$

$\ \ \ \ \  \Leftrightarrow \sum_{k=1}^{n}f(\frac{3k}{n})\cdot (\frac{3}{n})$

$\ \ \ \ \  \Leftrightarrow \sum_{k=1}^{n}((\frac{3k}{n})^2+1)\cdot (\frac{3}{n})$

$\ \ \ \ \  \Leftrightarrow \sum_{k=1}^{n}(\frac{9k^2}{n^2}+1)\cdot (\frac{3}{n})$

$\ \ \ \ \  \Leftrightarrow \sum_{k=1}^{n}(\frac{9k^2+n^2}{n^2})\cdot (\frac{3}{n})$

$\ \ \ \ \  \Leftrightarrow \sum_{k=1}^{n}\frac{27k^2+3n^2}{n^3}$

$\ \ \ \ \  \Leftrightarrow \sum_{k=1}^{n}\frac{27k^2}{n^3}+\sum_{k=1}^{n}\frac{3n^2}{n^3}$

$\ \ \ \ \  \Leftrightarrow \frac{27}{n^3}\sum_{k=1}^{n}k^2+\frac{1}{n^3}\sum_{k=1}^{n}3n^2$

$\ \ \ \ \  \Leftrightarrow \frac{27}{n^3}\frac{n(n+1)(2n+1)}{6}+\frac{1}{n^3}\cdot n \cdot 3n^2$

$\ \ \ \ \  \Leftrightarrow \frac{27}{n^3}(\frac{2n^3+3n^2+n}{6})+3$

$\ \ \ \ \  \Leftrightarrow \frac{54n^3+81n^2+27n}{6n^3}+3$

$\ \ \ \ \  \Leftrightarrow \lim_{n\rightarrow \infty} \frac{54n^3+81n^2+27n}{6n^3}+3$

$\ \ \ \ \  = \frac{54}{6}+3=9+3=12$

Substitusi $\frac{k}{n}$ kedalam fungsi $f(x)=x^2+1$

$\therefore$  jumlah Riemann dari $f(x)x^2+1$ pada interval $[0,3]$ adalah $12$