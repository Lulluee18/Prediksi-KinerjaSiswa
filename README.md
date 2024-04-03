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
					
![image](https://github.com/Lulluee18/Prediksi-KinerjaSiswa/assets/165852408/1748cd89-aaa6-42f5-af9e-09acbe1d0b2d)



					
			                	            Gambar 1b. Analisis Univariant (Data Numerik)
Berdasarkan gambar 1a,dapat dilihat bahwa ada 5 distribusi data kategori yaitu : untuk ‘ gender’memiliki perbandingan jumlah yang beda tipis atau perbandingan yang rendah dimana untuk male berjumlah 517 dengan persentase hampir 99%  sedangkan pada data female hanya 483,untuk ‘race_ethnicity’ pada distribusi data ini memiliki 5 group yang dimana perbandingan kelima grub ini memiliki nilai yang berbeda-beda,telah terlihat bahwa group a memiliki distribusi data yang rendah sedangka distribusi data yang tinggi terdapat pada group e,selanjutnya untuk ‘education’ distribusi data ini memiliki 5 yaitu some college,associate’s degree,high school,some high school,bachelor’s degree dan master’s degree pada some college memiliki distribusi data yang tinggi sedangkan distribusi data yang rendah jatuh di master’s degree,untuk’lunch terbagi menjadi dua itu standard dan free/reduced pada distribusi ini persebaran yang jauh lebih drastic pada standard dimana nilainya 65,2% jauh lebih tinggi dengan distribusi data 652 sedangkan pada free/reduced setegah persen dari distribusi data standard,untuk ‘test_preparation_course’ini sama seperti lunch yang dimana memiliki 2 distribusi data yaitu none dan completed telah terlihat persebaran distribusi data yang jauh lebih tinggi yaitu none.Pada Gambar 1b, untuk data numeric memiliki karakteristik,yaitu :
. Koordinat reading score mayoritas berada pada 149 derajat 150 derajat dan koodinat writing score mayoritas pada 150 derajat 120 derajat.
. Median dari kinerja siswa terdistribusi pada rentang 100-150 dan 150-200
![image](https://github.com/Lulluee18/Prediksi-KinerjaSiswa/assets/165852408/59238ecc-8b73-4aa1-a2f5-fddde114c145) ![image](https://github.com/Lulluee18/Prediksi-KinerjaSiswa/assets/165852408/eb161748-729b-4b85-b736-dd87ba782b5a) ![image](https://github.com/Lulluee18/Prediksi-KinerjaSiswa/assets/165852408/82f796df-6c9b-4b66-9c1c-0055ab9eab4e) ![image](https://github.com/Lulluee18/Prediksi-KinerjaSiswa/assets/165852408/c679973e-f9c4-417b-add2-6ae83e3f0cf6) ![image](https://github.com/Lulluee18/Prediksi-KinerjaSiswa/assets/165852408/94cf8074-6159-4763-944d-3c3b8a2a7a77) 
											Gambar 2a. Analisis Multivariant (Data Kategorik)
		   
							![image](https://github.com/Lulluee18/Prediksi-KinerjaSiswa/assets/165852408/ba370ab2-4c9f-4063-92a3-41a9917151dc)

       											Gambar 2b. Analisis Multivariat (Data Numeric) 
		  					![image](https://github.com/Lulluee18/Prediksi-KinerjaSiswa/assets/165852408/78f0ce37-813b-4010-b66f-09327ea755a2)
	 										Gambar 2c. Analisis Multivariant (Correlation Matrix)
Dengan mengamati Gambar 2a rata-rata 'writing score' relatif terhadap fitur kategori di atas, diperoleh insight sebagai berikut:Pada fitur 'writing score', rata-rata 'test preparation course' cenderung bervariasi. Rentangnya berada antara 70 hingga 70. Nilai 'writing score' tertinggi berada pada nilai 'parental level of education' yaitu 'master's degree' dan nilai 'writing score' terendah berada pada nilai 'parental level of education' yaitu 'some high school'. Sehingga, fitur 'parental level of education' memiliki pengaruh yang signifikan terhadap rata-rata 'writing score'. Kesimpulan akhir, fitur kategori memiliki pengaruh terhadap 'writing score'. b. Data Numerik Pada Gambar 2b. Fungsi pairplot dari library seaborn menunjukkan relasi pasangan dalam dataset. Dari grafik, terlihat plot relasi masing-masing fitur numerik pada dataset. Pada pola sebaran data grafik pairplot sebelumnya, terlihat bahwa 'median_income' memiliki korelasi dengan fitur 'median_house_value'. Sedangkan kedua fitur lainnya terlihat memiliki korelasi yang lemah karena sebarannya tidak membentuk pola
Koefisien korelasi berkisar antara -1 dan +1. Ia mengukur kekuatan hubungan antara dua variabel serta arahnya (positif atau negatif). Mengenai kekuatan hubungan antar variabel, semakin dekat nilainya ke 1 atau -1, korelasinya semakin kuat. Sedangkan, semakin dekat nilainya ke 0, korelasinya semakin lemah

Pada Gambar 2c Jika diamati, fitur 'reading score' memiliki skor korelasi yang cukup besar (0.95) dengan fitur target 'writing score'. Artinya, fitur 'writing score' berkorelasi cukup tinggi dengan keempat fitur tersebut. Sementara itu, fitur lainnya memiliki korelasi negatif sehingga, fitur tersebut dapat di-drop.

# Data Preparation
Pada proses Data Preparation dilakukan kegiatan seperti Data Gathering, Data Assessing, dan Data Cleaning. Pada proses Data Gathering, data diimpor sedemikian rupa agar bisa dibaca dengan baik menggunakan dataframe Pandas. Untuk proses Data Assessing, berikut adalah beberapa pengecekan yang dilakukan:

Duplicate data (data yang serupa dengan data lainnya)
Missing value (data atau informasi yang "hilang" atau tidak tersedia)
Outlier (data yang menyimpang dari rata-rata sekumpulan data yang ada)
Pada proses Data Cleaning, secara garis besar, terdapat tiga metode yang dapat digunakan antara lain seperti berikut:

Dropping (metode yang dilakukan dengan cara menghapus sejumlah baris data)
Imputation (metode yang dilakukan dengan cara mengganti nilai yang "hilang" atau tidak tersedia dengan nilai tertentu yang bisa berupa median atau mean dari data)
Interpolation (metode menghasilkan titik-titik data baru dalam suatu jangkauan dari suatu data)
Pada kasus proyek ini tidak ditemukan data duplikat. Pada proyek ini ditemukan Missing Value. Adapaun metode yang digunakan untuk mengatasi hal ini adalah dengan menerapkan imputation dimana data yang missing diganti dengan nilai mean. Untuk outlier sendiri dilakukan metode dropping menggunakan metode IQR. IQR sendiri didapatkan dengan cara mengurangi Q3 dengan Q1 sebagaimana rumusan berikut.


dimana Q1 adalah kuartil pertama dan Q3 adalah kuartil ketiga.

Dengan menggunakan metode IQR, dapat ditentukan outlier melalui suatu nilai batas yang ditentukan. Setelah menggunakan metode IQR dimana dataset yang sebelumnya berjumlah 1000 menjadi 994.

Semua proses ini diperlukan dalam rangka membuat model yang baik.

Untuk mereduksi jumlah fitur dilakukan proses PCA. Teknik reduksi ini adalah prosedur yang mengurangi jumlah fitur dengan tetap mempertahankan informasi pada data. PCA ini adalah teknik untuk mereduksi dimensi, mengekstraksi fitur, dan mentransformasi data dari “n-dimensional space” ke dalam sistem berkoordinat baru dengan dimensi m, di mana m lebih kecil dari
# Modeling
Seperti yang dijelaskan di awal, model yang dipilih adalah model regresi karena merupakan salah satu algoritma yang paling umum digunakan dalam pembuatan model prediksi. Dalam bentuk yang sederhana, regresi terdiri dari intersep dan slope yang dituliskan dalam rumusan berikut
y=a+bX
dimana:
•	y adalah variabel kriterium (variabel terikat yang digunakan untuk memprediksi)
•	a adalah intersep (variabel konstan yang memiliki arti sebagai titik perpotongan suatu garis dengan sumbu Y),
•	b adalah slope (nilai koefisien yang menyatakan ukuran kemiringan suatu garis), dan
•	X adalah variabel prediktor (variabel yang digunakan untuk memprediksi atau menjelaskan variabel lain dalam suatu model)
Secara umum, regresi ini itu sendiri digunakan untuk meramalkan pengaruh variabel prediktor terhadap variabel kriterium atau membuktikan ada atau tidaknya hubungan fungsional antara variabel bebas (X) dengan variabel terikat (y).
Namun begitu terdapat kelebihan dan kekurangan dari model regresi, yaitu:

Kelebihan regresi:

•	Kemudahan untuk digunakan
•	Kekuatan Prediktor dalam mengidentifikasi sekuat apa pengaruh yang diberikan oleh variabel prediktor (variabel independen) terhadap variabel lainnya (variabel dependen).
•	Dapat memprediksi nilai/tren di masa yang mendatang

Kelemahan dari model regresi adalah karena hasil ramalan dari analisis regresi merupakan nilai estimasi sehingga kemungkinan untuk tidak sesuai dengan data aktual tetaplah ada.
Pada proyek yang dikerjakan, algoritma regresi yang coba dibandingkan adalah regresi linear, regresi ridge, random forest regressor, dan random forest regressor dengan hyperparamter tuning. Regresi linear adalah teknik analisis data yang memprediksi nilai data yang tidak diketahui dengan menggunakan nilai data lain yang terkait dan diketahui dimana secara matematis dimodelkan sebagai persamaan linier, regresi ridge merupakan metode estimasi koefisien regresi yang diperoleh melalui penambahan konstanta bias c, dan random forest adalah suatu algoritma yang digunakan pada klasifikasi data dalam jumlah yang besar dimana teknik klasifikasi random forest dilakukan melalui penggabungan pohon dengan melakukan training pada sampel data yang dimiliki.
Untuk meningkatkan model, dilakukan hyperparamter tuning. Adapun paramater yang di-tuning antara lain n_estimators', 'max_depth', 'min_samples_split', dan 'min_samples_leaf. Untuk memudahkan proses tuning digunakan GridSearchCV. GridSearchCV itu sendiri merupakan bagian dari modul scikit-learn yang dapat digunakan untuk mendapatkan nilai hyperparameter secara otomatis. Grid Search adalah metode yang digunakan untuk mencari parameter yang paling tepat untuk meningkatkan performa model dengan mencoba seluruh kombinasi hyperparameter yang diberikan.
Berikut adalah nilai parameter tuning
params = {'n_estimators' : [50,80,100],
          'max_depth' : [3,5,10],
           'min_samples_split':[2,3,4],
            'min_samples_leaf': [2,3,4]}
Berdasarkan hasil pengujian, terpilih grid.best_params_ yaitu
{'max_depth': 10,
 'min_samples_leaf': 4,
 'min_samples_split': 2,
 'n_estimators': 100}
Parameter dengan nilai inilah yang kemudian dibuat sebagai model.

# Evaluation
Adapun metrik yang sebagai alat ukur perfoma model yang dibuat antara lain
 MSE • MAE • R2.
Berikut merupakan rumus dari masing-masing metrik yang digunakan:
![image](https://github.com/Lulluee18/Prediksi-KinerjaSiswa/assets/165852408/14df2150-6b4c-4035-9b94-2f01aadfe6e7)
yi mewakili nilai yang diamati, ŷi mewakili nilai prediksi, n adalah jumlah titik data, Var(y) mewakili varians dari nilai yang diamati.
Berikut merupakan penjelasan kegunaan dari masing-masing metrik yang digunakan:
•	MAE menghitung rata-rata dari selisih absolut antara nilai prediksi dan nilai aktual. Semakin kecil nilai MAE, semakin baik kualitas model tersebut.
•	MSE menghitung rata-rata dari selisih kuadrat antara nilai prediksi dan nilai aktual. Semakin kecil nilai MSE, semakin baik kualitas model tersebut.
•	R2 digunakan untuk menilai seberapa besar pengaruh variabel independen tertentu terhadap variabel dependen

				![image](https://github.com/Lulluee18/Prediksi-KinerjaSiswa/assets/165852408/49647b25-d87b-48dd-9498-59c8d2223482)

# Referensi 
[1] https://journals.sagepub.com/doi/abs/10.3102/00346543057003293
[2] https://r.search.yahoo.com/_ylt=Awr4.mwIiA1mk44E4zJXNyoA;_ylu=Y29sbwNncTEEcG9zAzEEdnRpZAMEc2VjA3Ny/RV=2/RE=1713372424/RO=10/RU=https%3a%2f%2fwww.ncbi.nlm.nih.gov%2fpmc%2farticles%2fPMC8654637%2f/RK=2/RS=5_zHvOqERG1F94wgMCsg6i5Wf8U-
[3] https://r.search.yahoo.com/_ylt=Awr4.mwIiA1mk44E5jJXNyoA;_ylu=Y29sbwNncTEEcG9zAzMEdnRpZAMEc2VjA3Ny/RV=2/RE=1713372424/RO=10/RU=https%3a%2f%2fjurnal.uns.ac.id%2fenglishedu%2farticle%2fviewFile%2f35816%2f23419/RK=2/RS=5ARBFtsssNkUbfMira4AhhawPh4-









