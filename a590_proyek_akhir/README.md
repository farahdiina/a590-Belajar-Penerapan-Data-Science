# Proyek Akhir: Menyelesaikan Permasalahan Perusahaan Edutech

## Business Understanding
Jaya Jaya Institut adalah sebuah institusi pendidikan tinggi yang telah berdiri sejak tahun 2000 dan dikenal dengan reputasi lulusannya yang sangat baik. Sebagai lembaga pendidikan, tujuan utama mereka adalah mencetak lulusan yang kompeten dan siap bersaing di dunia kerja. Namun, salah satu tantangan besar yang dihadapi adalah tingginya tingkat dropout mahasiswa, yang dapat berdampak negatif pada citra institusi, akreditasi, serta kepercayaan masyarakat terhadap kualitas pendidikannya. Tingkat dropout yang tinggi bisa disebabkan oleh berbagai faktor, seperti kesulitan akademik, masalah ekonomi, kurangnya motivasi, atau kendala pribadi lainnya. Jika tidak diatasi dengan baik, kondisi ini dapat menurunkan daya saing institusi dan menghambat pencapaian target akademik serta operasional. Oleh karena itu, Jaya Jaya Institut ingin menerapkan pendekatan berbasis data untuk mengidentifikasi mahasiswa yang berisiko tinggi mengalami dropout. Dengan adanya model prediksi berbasis machine learning, institusi dapat mendeteksi mahasiswa yang berpotensi mengalami dropout sejak dini dan memberikan intervensi yang lebih tepat, seperti bimbingan akademik tambahan, konseling, atau bantuan keuangan. Selain itu, institusi juga menginginkan dashboard interaktif yang memungkinkan pemantauan performa mahasiswa secara visual dan lebih mudah dipahami oleh pihak manajemen. Melalui analisis ini, diharapkan tingkat dropout dapat ditekan, sehingga Jaya Jaya Institut dapat mempertahankan reputasinya sebagai lembaga pendidikan yang berkualitas serta meningkatkan keberhasilan mahasiswanya. 

### Permasalahan Bisnis
Di banyak institusi pendidikan tinggi, tingkat dropout mahasiswa menjadi tantangan yang signifikan, memengaruhi stabilitas akademik dan reputasi lembaga. Jaya Jaya Institut juga menghadapi masalah serupa, dengan jumlah mahasiswa yang tidak menyelesaikan studinya mengalami peningkatan dalam beberapa tahun terakhir. Dengan menganalisis data yang dikumpulkan sejak pendaftaran hingga evaluasi akademik pada semester awal, kita dapat membangun model prediktif untuk mengidentifikasi mahasiswa yang berisiko mengalami dropout. Penting untuk memahami faktor-faktor yang berkontribusi terhadap keputusan ini, termasuk latar belakang akademik, kondisi ekonomi, dan tingkat kehadiran mahasiswa. Jika masalah ini tidak ditangani dengan baik, dampaknya bisa mencakup rendahnya angka kelulusan, meningkatnya beban administrasi akibat mahasiswa yang keluar di tengah jalan, serta persepsi negatif terhadap institusi. Oleh karena itu, model prediksi yang akurat dapat membantu Jaya Jaya Institut dalam menerapkan strategi intervensi yang lebih efektif, seperti bimbingan akademik dan dukungan finansial, guna meningkatkan tingkat retensi mahasiswa dan menciptakan lingkungan belajar yang lebih kondusif.

### Cakupan Proyek
1. Pengumpulan dan Pemahaman Data
   - Dataset sudah tersedia dalam file data.csv.
   - Memahami struktur dan karakteristik data, termasuk tipe variabel, jumlah data, serta nilai yang hilang atau tidak valid.
2. Eksplorasi Data (Exploratory Data Analysis - EDA)
   - Melakukan analisis awal untuk mengidentifikasi pola, tren, dan distribusi data.
   - Visualisasi data menggunakan seaborn, matplotlib, dan plotly untuk memahami hubungan antar variabel serta mendeteksi anomali atau outlier.
3. Pembersihan dan Persiapan Data
   - Menangani nilai yang hilang dengan SimpleImputer menggunakan strategi yang sesuai.
   - Menghapus duplikasi data untuk memastikan keakuratan analisis.
   - Menggunakan Label Encoding untuk variabel kategorikal dan StandardScaler untuk menormalisasi data numerik.
4. Penanganan Ketidakseimbangan Data
   - Menggunakan teknik SMOTETomek untuk menangani ketidakseimbangan kelas dan meningkatkan kualitas model prediksi.
5. Seleksi Fitur
   - Menggunakan SelectFromModel dengan RandomForestClassifier untuk memilih fitur yang paling berpengaruh terhadap prediksi.
   - Menghapus fitur yang tidak memiliki kontribusi signifikan dalam meningkatkan akurasi model.
6. Pengembangan Model Prediksi
   - Membagi dataset menjadi data latih (train) dan data uji (validation) dengan train_test_split.
   - Menggunakan teknik Pipeline dan ColumnTransformer untuk preprocessing sebelum model dijalankan.
   - Membangun dan melatih model prediksi dengan algoritma Random Forest, Gradient Boosting, AdaBoost, SVM, dan SGDClassifier.
   - Menggunakan VotingClassifier untuk membangun model ensemble guna meningkatkan akurasi prediksi.
   - Menyimpan model terbaik dalam format .pkl menggunakan pickle.
7. Evaluasi Model
   - Menggunakan metrik evaluasi seperti accuracy, precision, recall, f1-score, dan confusion matrix.
   - Melakukan cross-validation untuk mengukur stabilitas model.
8. Pembuatan Dashboard Interaktif
   - Merancang dan membangun dashboard interaktif menggunakan Google Looker Studio.
   - Menggunakan data hasil preprocessing untuk menampilkan insight terkait faktor-faktor yang mempengaruhi dropout mahasiswa.
     
Dengan cakupan proyek ini, diharapkan dapat memberikan solusi berbasis data bagi Jaya Jaya Institut dalam mengidentifikasi dan mengurangi angka dropout, serta menciptakan lingkungan akademik yang lebih mendukung keberhasilan mahasiswa.

### Persiapan

Sumber data: (https://github.com/dicodingacademy/dicoding_dataset/blob/main/students_performance/data.csv)

Setup Environment - Anaconda
```
conda create --name main-ds python=3.9  
conda activate main-ds  
pip install -r requirements.txt  
```
Setup Environment - Shell/Terminal
```
mkdir proyek_analisis_data  
cd proyek_analisis_data  
pipenv install  
pipenv shell  
pip install -r requirements.txt 
```
## Business Dashboard
Dashboard ini dirancang untuk menganalisis performa mahasiswa dan faktor-faktor yang mempengaruhi kelulusan serta dropout. Dua indikator utama yang ditampilkan adalah jumlah mahasiswa (4.424) dan tingkat kelulusan (49,93%). Beberapa visualisasi utama dalam dashboard ini meliputi hubungan antara pendidikan sebelumnya dengan status mahasiswa (lulus, dropout, atau masih terdaftar), serta pengaruh biaya kuliah terhadap dropout, yang menunjukkan bahwa 24,7% mahasiswa mengalami dropout. Selain itu, ada analisis kehadiran di semester awal, yang membantu memahami keterlibatan akademik sebagai faktor keberhasilan. Dashboard ini juga mengevaluasi pengaruh beasiswa terhadap status mahasiswa dan hubungan antara jumlah mata kuliah yang diambil dengan nilai penerimaan. Dengan wawasan ini, institusi dapat merancang strategi untuk meningkatkan kelulusan dan mengurangi dropout.
Dashboard dapat diakses pada link ini : https://lookerstudio.google.com/reporting/39a8d8b5-e939-4393-8ea9-265bac9e0ccd


## Menjalankan Sistem Machine Learning
Jelaskan cara menjalankan protoype sistem machine learning yang telah dibuat. Selain itu, sertakan juga link untuk mengakses prototype tersebut.
- Instalasi Dependensi
```
pip install -r requirements.txt
pip install streamlit pandas joblib plotly scikit-learn
streamlit run app.py
```

## Conclusion
Melalui proyek ini, kami berhasil membangun model prediksi dropout mahasiswa berdasarkan data akademik, demografis, dan sosial-ekonomi. Dengan memanfaatkan teknik machine learning, seperti Random Forest, Gradient Boosting, SVM, dan ensemble modeling, model yang dikembangkan mampu mengidentifikasi faktor-faktor utama yang berkontribusi terhadap kemungkinan mahasiswa tidak menyelesaikan studi mereka. Hasil analisis menunjukkan bahwa faktor kehadiran di semester awal, latar belakang pendidikan, biaya kuliah, dan penerimaan beasiswa memiliki pengaruh signifikan terhadap status mahasiswa, apakah mereka akan lulus, tetap terdaftar, atau dropout. Dengan adanya model, institusi dapat mengambil tindakan preventif lebih awal, seperti memberikan bimbingan akademik, dukungan finansial, atau strategi pembelajaran yang lebih adaptif, guna meningkatkan retensi mahasiswa dan memperbaiki tingkat kelulusan. Implementasi dashboard interaktif juga memungkinkan pemantauan data secara real-time, sehingga pengambilan keputusan menjadi lebih cepat dan berbasis data.

Secara keseluruhan, proyek ini tidak hanya membantu dalam mengurangi angka dropout, tetapi juga berkontribusi pada peningkatan kualitas pendidikan dan reputasi institusi dalam jangka panjang.

### Rekomendasi Action Items
1. Mengembangkan Sistem Prediksi dan Pemantauan Mahasiswa
  Menggunakan model prediktif untuk mengidentifikasi mahasiswa yang berisiko dropout berdasarkan faktor akademik, kehadiran, dan kondisi ekonomi, sehingga intervensi dapat dilakukan lebih cepat.

2. Meningkatkan Program Bimbingan Akademik dan Dukungan Finansial
  Menyediakan bimbingan akademik secara rutin dan memperluas akses ke beasiswa atau bantuan keuangan bagi mahasiswa yang membutuhkan, guna mengurangi hambatan akademik dan ekonomi yang berkontribusi terhadap dropout.

3. Mengoptimalkan Metode Pembelajaran dan Keterlibatan Mahasiswa
  Menerapkan metode pembelajaran yang lebih fleksibel, seperti kelas hybrid atau e-learning, serta mendorong keterlibatan mahasiswa dalam organisasi dan kegiatan kampus untuk meningkatkan rasa memiliki dan motivasi belajar.
