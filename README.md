# Prediksi-KinerjaSiswa

# Domain Proyek 
Kinerja Siswa adalah adalah konsep yang mengacu pada seberapa baik atau seberapa buruk siswa mencapai tujuan belajar mereka dalam konteks pendidikan. Ini bisa mencakup berbagai aspek, termasuk nilai atau prestasi akademi siswa .
Dalam Hal kinerja siswa ini sangat bergantung pada factor seperti factor pendidikan,factor lingkungan,Kesehatan dan Gizi dan sebagainya.Salah satu factor yang menarik untuk ditelusuri lebih lanjut adalah factor kinerja siswa dalam ujian.Oleh karena itu,dengan mempertimbangkan  factor-factor tersebut,yang juga tersedia pada dataset,maka dapat diestimasi kinerja siswa tersebut dengan melihat seberapa besar hail dalam mereka melakukan ujian tersebut.
Dalam membuat model regresi ada banyak cara algoritma yang bisa dipilih,salah satunya dengan algoritma yang paling umum digunakan adalah regresi.dengan menggunakan regresi dan memasukkan factor-factor dari hasil ujian yang dituju dan diharapkan dapat memprediksi hasil ujian mereka.

# Business Understanding
Pengembangan Model ii memiliki potensi dampak atau manfaat salah satunya alat bantu dalam kulitas pengajaran oleh siswa. Contoh potensi manfaat dari hasil yang akurat adalah membantu siswa dalam memahami materi yang diajarkan sehingga siswa dapat lebih mudah buat menangkapnya.

# Problem Statements
. Berdasarkan eksplorasi dataset dengan memahami faktor-faktor apa yang berkontribusi terhadap kinerja siswa dalam ujian matematika, membaca, dan menulis
. berdasarkan dataset yang mencakup variabel gender, ras/etnis, tingkat pendidikan orang tua, status makan siang, kursus persiapan ujian, serta skor ujian matematika, baca, dan tulis.

# Goals 
1.	Mengidentifikasi hubungan antara variabel gender, ras/etnis, tingkat pendidikan orang tua, status makan siang, kursus persiapan ujian dengan skor ujian matematika, baca, dan tulis.
2.	Menganalisis perbedaan kinerja antara siswa berdasarkan faktor-faktor yang disebutkan di atas.
3.	Membangun model prediktif untuk memprediksi skor ujian matematika, baca, dan tulis berdasarkan variabel-variabel yang ada.
4.	Memberikan rekomendasi kepada pihak pendidikan atau pemangku kepentingan lainnya berdasarkan temuan dari analisis ini untuk meningkatkan kinerja siswa, terutama bagi kelompok yang mungkin berisiko rendah

# Solution Statements
1.	Menganalisis korelasi antara variabel-variabel seperti gender, ras/etnis, tingkat pendidikan orang tua, status makan siang, dan kursus persiapan ujian dengan skor ujian matematika, baca, dan tulis untuk memahami faktor-faktor yang paling berpengaruh terhadap kinerja siswa.
2.	Menggunakan teknik visualisasi data seperti diagram batang, diagram lingkaran, dan matriks korelasi untuk memperjelas hubungan antara variabel-variabel tersebut dan skor ujian.
3.	Membagi dataset menjadi kelompok-kelompok berdasarkan variabel kategoris seperti gender, ras/etnis, dan tingkat pendidikan orang tua, dan kemudian melakukan analisis statistik perbandingan antara kelompok-kelompok ini untuk mengidentifikasi perbedaan signifikan dalam kinerja.
4.	Membangun model regresi linier atau model klasifikasi seperti regresi logistik atau pohon keputusan untuk memprediksi skor ujian berdasarkan variabel-variabel prediktif yang relevan.
5.	Melakukan evaluasi model menggunakan metrik seperti akurasi, RMSE (Root Mean Squared Error), atau R-squared untuk memeriksa seberapa baik model dapat memprediksi skor ujian siswa.
6.	Menyusun rekomendasi berdasarkan temuan analisis untuk membantu pendidik dan pemangku kepentingan lainnya dalam merancang intervensi yang tepat untuk meningkatkan kinerja siswa, seperti program bantuan belajar tambahan atau dukungan pendidikan khusus.
Data Undertanding
Data yang digunakan dalam pembuatan model merupakan data sekunder.Data diambil dari kaggle dengan nama dataset yaitu For Beginners: Students Performance.
URL : 
https://www.kaggle.com/code/melikedilekci/for-beginners-students-performance/input
Berikut merupakan detail dari dataset yang digunakan untuk pembuatan model :
. Dataset berupa CSV
. Dataset Terdiri dari 1001 records dengan 8 buah fitur yang diukur.
. Dataset terdiri dari 5 data kategori dan 3 data numeric.
Variabel-variabel pada dataset adalah sebagai berikut :
1.	Gender (Jenis Kelamin): Mencatat jenis kelamin siswa (misalnya, laki-laki atau perempuan).
2.	Race/Ethnicity (Ras/Etnis): Menunjukkan ras atau etnis siswa, mungkin direpresentasikan dalam bentuk kategori seperti A, B, C, D, E atau dengan nama kelompok etnis tertentu.
3.	Parental Level of Education (Tingkat Pendidikan Orang Tua): Mengidentifikasi tingkat pendidikan tertinggi orang tua atau wali siswa (misalnya, sekolah menengah atau lebih tinggi, sarjana, dll.).
4.	Lunch (Makan Siang): Menandai status makan siang siswa (misalnya, apakah siswa menerima makan siang gratis atau berbayar).
5.	Test Preparation Course (Kursus Persiapan Ujian): Menunjukkan apakah siswa mengikuti kursus persiapan ujian sebelum ujian (mungkin dalam bentuk "completed" atau "none").
6.	Math Score (Skor Matematika): Menyimpan skor ujian matematika siswa.
7.	Reading Score (Skor Membaca): Mencatat skor ujian membaca siswa.
8.	Writing Score (Skor Menulis): Merupakan skor ujian menulis siswa.
   
Untuk memahami data lebih lanjut, dilakukan Analisis Univariat dan Analisis Multivariat, serta Visualisasi Data
Analisis Univariat merupakan bentuk analisis data yang hanya merepresentasikan informasi yang terdapat pada satu variabel. Jenis visualisasi ini umumnya digunakan untuk memberikan gambaran terkait distribusi sebuah variabel dalam suatu dataset. Sedangkan, Analisis Multivariat tmerupakan jenis analisis data yang terdapat dalam lebih dari dua variabel. Jenis visualisasi ini digunakan untuk merepresentasikan hubungan dan pola yang terdapat dalam multidimensional data.
Selain melalui analisis, dilakukan juga Visualisasi Data. Memvisualisasikan data memberikan wawasan mendalam tentang perilaku berbagai fitur-fitur yang tersedia dalam dataset. Teknik visualisasi yang digunakan pada pembuatan model proyek ini adalah dengan menggunakan catplot yang digunakan untuk memplot distribusi data pada data kategori, pairplot yang digunakan untuk melakukan hubungan antar fitur dalam dataset, dan heatmap yang menampilkan korelasi antar fitur yang ada dalam dataset dalam bentuk matriks.
Berikut adalah hasil Exploratory Data Analysis (EDA), dimana Gambar 1 merupakan EDA Analisis Univariat dan Gambar 2 merupakan EDA Analisis Multivariat.

![image](https://github.com/Lulluee18/Prediksi-KinerjaSiswa/assets/165852408/d0051b9a-c333-4f73-a3a7-d1a7b7cc927b) ![image](https://github.com/Lulluee18/Prediksi-KinerjaSiswa/assets/165852408/d7e51c8e-d473-461c-8042-f22bac3c7448) ![image](https://github.com/Lulluee18/Prediksi-KinerjaSiswa/assets/165852408/08c54a14-63e7-4ebd-9e2c-69a33f2f5453) ![image](https://github.com/Lulluee18/Prediksi-KinerjaSiswa/assets/165852408/e38e9ee2-948e-4a25-b546-25cd2e88652e) ![image](https://github.com/Lulluee18/Prediksi-KinerjaSiswa/assets/165852408/8bf49c9f-d2a4-488a-986c-5557e0ec6ef0)





                                          






 	                                           Gambar 1a . Analisis Univariant (Data Kategori)
			



			             Gambar 1b. Analisis Univariant (Data Numerik)
Berdasarkan gambar 1a,dapat dilihat bahwa ada 5 distribusi data kategori yaitu : untuk ‘ gender’memiliki perbandingan jumlah yang beda tipis atau perbandingan yang rendah dimana untuk male berjumlah 517 dengan persentase hampir 99%  sedangkan pada data female hanya 483,untuk ‘race_ethnicity’ pada distribusi data ini memiliki 5 group yang dimana perbandingan kelima grub ini memiliki nilai yang berbeda-beda,telah terlihat bahwa group a memiliki distribusi data yang rendah sedangka distribusi data yang tinggi terdapat pada group e,selanjutnya untuk ‘education’ distribusi data ini memiliki 5 yaitu some college,associate’s degree,high school,some high school,bachelor’s degree dan master’s degree pada some college memiliki distribusi data yang tinggi sedangkan distribusi data yang rendah jatuh di master’s degree,untuk’lunch terbagi menjadi dua itu standard dan free/reduced pada distribusi ini persebaran yang jauh lebih drastic pada standard dimana nilainya 65,2% jauh lebih tinggi dengan distribusi data 652 sedangkan pada free/reduced setegah persen dari distribusi data standard,untuk ‘test_preparation_course’ini sama seperti lunch yang dimana memiliki 2 distribusi data yaitu none dan completed telah terlihat persebaran distribusi data yang jauh lebih tinggi yaitu none.Pada Gambar 1b, untuk data numeric memiliki karakteristik,yaitu :

