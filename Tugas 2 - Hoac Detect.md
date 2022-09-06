## Deteksi Hoax di Media Sosial Twitter dengan Ekspansi Fitur Menggunakan Glove

### Masalah
<div style="text-align:justify">
<p>Terdapat banyak berita hoax yang saat ini banyak beredar di masyarakat. Bahkan di Indonesia, khusus- nya di media sosial, fenomena hoax tidak jarang terjadi. Hoax bisa membuat orang resah karena informasi yang tidak diketahui kebenarannya. Untuk mengetahui informasi yang disebarluaskan, kita perlu mengklasifikasikannya untuk mengetahui apakah itu hoax atau tidak.
<p>Seiring dengan berkembangnya teknologi, masyarakat beralih ke media sosial sebagai alat komunikasi. Tanpa disadari hoax atau berita palsu juga ikut berkembang di kalangan masyarakat pengguna media sosial. Media sosial merupakan kategori wacana online tempat orang membuat konten dan membagikannya . Jika ada yang menyebarkan berita bohong akan mendapat hukuman selama 6 tahun dan denda sampai dengan Rp.1.000.000.000(satu milyar rupiah). Pada penelitian, menganalisis bahwa Twitter merupakan platform media sosial paling populer dalam penyebaran berita hoax selama 2016-2018.

### Metode
<p>Oleh karena itu dalam penelitian ini, di kembangkan sistem yang mampu mendeteksi informasi hoax di media sosial Twitter dengan menggunakan metode ekspansi fitur Global Vectors for Word Representation (GloVe). Metode ekspansi fitur Glove digunak- an untuk mengurangi adanya ketidakcocokan kosakata pada sebuah tweet pada Twitter. Proses klasifikasi yang digunakan beberapa metode yaitu, Support Vector Machine (SVM), Naive Bayes dan Recurrent Neural Network (RNN).
<ul>
<li>Crawling dan Pelabelan Data
<p>Pada tugas akhir ini menggunakan dataset yang berasal dari hasil crawling Twitter yang berbahasa Indonesia dengan menggunakan Application Programming Integration (API) Key yang telah diberikan oleh Twitter Develo- per. Dalam proses crawling data diambil Tweet dengan kata kunci tertentu dan hastag, data tersebut di simpan dengan format CSV dan di beri label 0 untuk nonhoax dan 1 untuk hoax.
<li>Preprocessing
<p>Preprocessing data merupakan tahapan yang akan di lakukan sebelum data di masukan ke dalam klasifikasi. Proses ini berfungsi untuk menghilangkan kesalahan, kesamaan bentuk kata serta mengurangi banyaknya kata dari data yang sudah ada. Terdapat 5 tahap dalam preprocessing, antara lain:
<ul>
<li>Cleaning
<li>Case Folding
<li>Stopward Removal
<li>Normalisasi Kata
<li>Stemming
<li>Tokenization
</ul>
<li>Ekstraksi Fitur
<p>Fitur ekstraksi merupakan tahapan untuk menscanning ciri yang terdapat dalam teks dokumen. Fitur ekstraksisebagai faktor yang sangat krusial pada pengerjaan dokumen dalam mesin pencari lantaran sangat memilih keber-hasilan proses textittext mining.
<li>Glove
<p>GloVe merupakan word embeddings dari Stanford University untuk memrepresentasikan kata-kata. GloVe ada- lah metode pengajaran tanpa pengawasan untuk representasi kata yang melampaui model lain dalam kesetaraan kata dan identifikasi nama.
<li>Ekspansi Fitur
<p>Selanjutnya melakukan fitur ekspansi, fitur ini dilakukan setelah data tweet diterapkan metode Word Embe- dding, fungsi metode tersebut untuk mengatasi masalah ketidakcocokan pada kosakata, yaitu dengan mengidentifikasikan kata-kata yang telah di dapatkan dari penggunaan metode GloVe
<li>Support Vektor Machine (SVM)
<p>Support Vektor Machine (SVM) cara kerjanya yaitu dengan menemukan fungsi pemisah line yang dapat memi-sahkan dua set dari data antara dua kelas yang berbeda [16]. Metode ini disebut dengan metode learning machine yang memiliki prinsip Sructural Risk Minimazation (SRM) yang bertujuan menemukan hyperplane terbaik untukmemisahkan dua buah dari kelas pada inputan space.
<li>Naïve Bayes 
<p>Metode NaiVe Bayes atau NaiVe Bayes Classifier (NBC) merupakan cara yang biasa dimanfaatkan untuk peng- klasifikasi text pada dokumen. Konsep yang digunakan NBC adalah probabilitas sebagai acuan teorinya. Dalam tulisannya, Han, J. dan Kamber, M. mengatakan: ”Bayesian classffiers memiliki tingkat kecepatan dan accuracyyang unggul ketika diterapkan dalam basedata yang besar” (2001, hlm. 296). Dengan buku tersebut, maka sistem Naive Bayes merupakan sistem yang dipergunakan untuk proses tahapan klasifikasi text dalam eksperimen ini. Ada 2 tahap pada proses yang di lakukan pada klasifikasi text. Yakni proses pertama merupakan training terhadaphimpunan artikel. Sedangkan untuk proses kedua yang dilakukan merupakan tahapan klasifikasi dokumen yang belum diketahui topiknya.
<li>Recurrent Neural Network (RNN) 
<p>RNN merupakan sistem jaringan saraf yang berulang dan menggunakan hidden layer untuk nilai neuron akan diproses untuk data inputan . Proses yang dilakukan untuk Recurrent Neural Network (RNN) akan memanggil secara berkali-kali untuk menjalankan inputan yang masuk, yaitu data linear. Recurrent Neural Network (RNN) juga mempunyai beragam bentuk, salah satu bentuknya yaitu global digunakan standar Multi-Layer Perceptron (MLP) yang ditambah dengan loop tambahan.
</ul>

### Hasil Pembahasan
<p>Data tweet yang telah didapatkan dari hasil crawling berjumlah 26.948 tweet berbahasa Indonesia yang memu-at data yang berhubungan dengan bahasan hoax di Indonesia, namun data tweet yang digunakan berjumlah 10.000. Kemudian data tersebut akan dijadikan sebagai data train dan data test. Data ini terdiri dari beberapa keyword ber-beda yang berkaitan dengan hastag, #VaksinUntukKita, #IndonesiaMaju, #NKRI, #Mudik, #Paspampres, #Wakilbupatisangihe, #Gajijakarta. Dengan jumlah penyebarannya data yang telah diberi label hoax dan non-hoax Kemudian, terdapat data pelengkap pembuatan kamus kata menggunakan data yang diambil dari beberapa media berita seperti CNN Indonesia, Sindonews, Kompas, Tempo, Detik.com, Liputan6, dan Republika sebanyak 142.544 data. Digunakan korpus Indonews untuk kombinasi percobaan pada penelitian ini mencari hasil terbaik. Komposisi data IndoNews yang digunakan untuk pembuatan kamus similarity dengan word embedding Terdapat 3 corpus GloVe yang akan dibangun, diantaranya adalah corpus GloVe dengan menggunakan dataset Tweet saja, corpus GloVe dengan menggunakan dataset IndoNews saja dan corpus GloVe yang menggunakan dataset gabungan dari keduanya.

### Kesimpulan
<p>telah dibangun deteksi hoax menggunakan ekspansi fitur metode GloVe dengan metode klasifikasi Naive Bayes, Recurrent Neural Network (RNN), Support Vector Machine (SVM). Ekspansi Fitur GloVe digunakan pada sistem pendeteksi hoax ini bertujuan untuk mengurangi ketidakcocokan kosakata pada kalimat tweet. Ekspansi fitur dilakukan dengan menggunakan 3 korpus GloVe (Tweet, IndoNews, dan Tweet + IndoNews)dan juga 3 variasi ekspansi fitur (Top 1, Top 5, Top 10) untuk mencari model terbaik. Pada hasil penelitian menunjukan bahwa metode ekspansi fitur GloVe berhasil meningkatkan akurasi nilai pada sistem yang telah di bangun.