Bagian terakhir dari materi one-way ANOVA adalah pengerjaan quiz sebagai bagian dari proses pemahaman materi tersebut. Pada quiz ini, anda akan menggunakan dataset tentang masa pakai ban mobil — data tersebut disimpan dalam format csv pada folder `data_input` dengan nama file `tyre.csv`.

Untuk menyelesaikan quiz ini, anda perlu menerapkan metode one-way ANOVA untuk menguji dan membandingkan masa pakai empat merek ban dengan mengikuti langkah-langkah berikut:

# 1 Data Exploration

Sebelum melakukan one-way ANOVA, kita harus melakukan eksplorasi data terlebih dahulu. Untuk itu anda perlu mengimport dan memahami secara umum data yang digunakan (`tyre.csv`) dengan menggunakan fungsi `read.csv()` dan `glimpse()`.

```
# your code here
```
Berdasarkan output yang diperoleh di atas, data masa pakai ban mobil terdiri dari 60 ban mobil dari 4 merek berbeda (Apollo, Bridgestone, CEAT and Falken). Masing-masing ban mobil tersebut diukur masa pakainya dalam mileage run in ’000 miles.

- `Brands`: Merek ban mobil (Apollo, Bridgestone, CEAT and Falken).
- `Miliage`: Masa pakai ban mobil dalam mileage run in ’000 miles.

1. Berdasarkan eksplorasi di atas, apa respon (y) yang diukur?
  - [v] masa pakai ban mobil
  - [ ] ukuran ban mobil
  - [ ] merek ban mobil
  - [ ] harga ban mobil
2. Apa prediktor/perlakuan (x) yang diterapkan?
  - [ ] masa pakai ban mobil
  - [ ] ukuran ban mobil
  - [v] merek ban mobil
  - [ ] harga ban mobil
3. Sebutkan kategori pada prediktor/perlakuan (x) yang diterapkan?
  - [ ] Apollo, Bridgestone, CEAT and Dunlop
  - [ ] Achilles, Bridgestone, CEAT and Falken
  - [ ] Apollo, Bridgestone, Corsa and Falken
  - [v] Apollo, Bridgestone, CEAT and Falken
4. Tentukan null hypothesis (H0) untuk permasalahan di atas?
  - [ ] merek ban mobil berpengaruh terhadap masa pakai ban mobil
  - [v] semua merek ban mobil memiliki masa pakai yang sama
  - [ ] terdapat minimal 1 merek ban mobil yang memiliki masa pakai yang berbeda
  - [ ] terdapat perbedaan yang signifikan antara berbagai merek ban mobil yang diterapkan terhadap masa pakai ban mobil
5. Tentukan alternative hypothesis (H1) untuk permasalahan di atas?
  - [ ] merek ban mobil tidak berpengaruh terhadap masa pakai ban mobil
  - [ ] semua merek ban mobil memiliki masa pakai yang sama
  - [v] terdapat minimal 1 merek ban mobil yang memiliki masa pakai yang berbeda
  - [ ] terdapat minimal 2 merek ban mobil yang memiliki masa pakai yang berbeda

# 2 Compute One-Way ANOVA

Sebagai seorang bisnis manajer, anda memiliki tanggung jawab untuk menguji dan membandingkan masa pakai 4 merek ban mobil (Apollo, Bridgestone, CEAT and Falken). Untuk setiap merek ban mobil diberikan sampel 15 ban mobil. Berdasarkan data tersebut anda harus bisa mengambil keputusan mengenai 4 merek ban mobil tersebut. Anda bisa mencoba melakukan one-way ANOVA menggunakan fungsi `aov()`dan melihat output dari hasil one-way ANOVA menggunakan fungsi `summary()`.

```
# your code here
```
6. Berdasarkan hasil one-way ANOVA di atas, apa yang dapat disimpulkan oleh bisnis manajer?
  - [v] terdapat minimal 1 merek ban mobil yang memiliki masa pakai yang berbeda
  - [ ] terdapat minimal 2 merek ban mobil yang memiliki masa pakai yang berbeda
  - [ ] merek ban mobil tidak berpengaruh terhadap masa pakai ban mobil
  - [ ] semua merek ban mobil memiliki masa pakai yang sama
  
# 3 Pairwise Mean Comparison

Pada one-way ANOVA manajer bisnis hanya mengetahui bahwa setiap merek ban mobil memiliki masa pakai yang berbeda. Namun, ia tidak mengetahui ban mobil dengan merek apa yang memiliki masa pakai paling lama. Anda bisa melakukan tes lanjutan (Tukey's HSD test) untuk mengetahui hal tersebut dengan menggunakan fungsi `TukeyHSD()`.

```
# your code here
```
7. Berdasarkan hasil tes lanjutan di atas, merek ban mobil apa yang memiliki masa pakai paling lama?
  - [ ] Apollo
  - [ ] Bridgestone
  - [ ] CEAT
  - [v] Falken

# 3 Anova Assumptions

8. Supaya keputusan yang diperoleh di atas tidak bias dan presisi. Hasil one-way ANOVA harus memenuhi asumsi?
  - [ ] homogeneity of Variance dan non - autocorrelation
  - [v] homogeneity of variance dan normality residuals
  - [ ] normality residuals dan non - multicolinearity
  - [ ] normality residuals dan white noise

Anda bisa melakukan pengecekkan kedua asumsi tersebut dengan fungsi `leveneTest()` dari package `car` dan fungsi `shapiro.test()`.

9. Pelanggaran asumsi apa yang terjadi?
  - [v] tidak ada
  - [ ] homogeneity of variance
  - [ ] normality residuals
  - [ ] keduanya



