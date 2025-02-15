# Proyek Akhir: Menyelesaikan Permasalahan Perusahaan Edutech

## Business Understanding

Jaya Jaya Maju merupakan perusahaan multinasional yang telah beroperasi sejak tahun 2000. Dengan lebih dari 1000 karyawan yang tersebar di seluruh penjuru negeri, perusahaan ini telah berkembang menjadi salah satu entitas bisnis yang cukup besar di industrinya. Meskipun memiliki skala bisnis yang luas, Jaya Jaya Maju menghadapi tantangan dalam pengelolaan sumber daya manusia. Salah satu permasalahan utama yang dihadapi adalah tingginya attrition rate, yaitu rasio jumlah karyawan yang keluar dibandingkan dengan total jumlah karyawan keseluruhan. Saat ini, angka tersebut telah mencapai lebih dari 10%, yang berpotensi menghambat produktivitas, meningkatkan biaya rekrutmen, serta mengganggu stabilitas tenaga kerja perusahaan. Untuk mengatasi permasalahan ini, departemen HR berinisiatif untuk menganalisis faktor-faktor yang berkontribusi terhadap tingginya attrition rate. Dengan memahami faktor penyebab, perusahaan dapat merancang strategi yang lebih efektif dalam mempertahankan karyawan. 

### Permasalahan Bisnis

1. Berapa jumlah total karyawan dan berapa persentase tingkat attrition di perusahaan?
2. Departemen mana yang memiliki tingkat attrition tertinggi?
3. Jabatan apa yang paling sering mengalami attrition?
4. Apa saja faktor utama yang memiliki korelasi tinggi dengan attrition?

### Cakupan Proyek

**Cakupan Proyek**

1. Pengumpulan dan Pemahaman Data:
- Dataset diperoleh dari file CSV dan dimuat menggunakan pandas.
- Memeriksa nilai yang hilang dalam dataset dan menangani nilai yang hilang pada kolom Attrition
- Menghapus kolom yang tidak relevan seperti EmployeeCount, StandardHours, Over18.

2. Eksplorasi Data (Exploratory Data Analysis - EDA):
- Melakukan eksplorasi awal untuk mengidentifikasi pola dan tren dalam dataset.
- Visualisasi distribusi variabel numerik menggunakan histogram.
- Analisis distribusi variabel kategorikal dengan countplot.
- Menampilkan hubungan antara variabel kategorikal dan Attrition.
- Menggunakan pairplot untuk mengeksplorasi hubungan antara variabel numerik dan Attrition.
- Menghitung korelasi antara variabel menggunakan heatmap.
- Mengurutkan 10 Faktor Terkorelasi dengan Attrition untuk melihat faktor apa yang paling berpengaruh.

3. Pembersihan dan Persiapan Data:
- Menggunakan Label Encoding untuk mengonversi data kategorikal menjadi numerik.
- Menggunakan StandardScaler untuk normalisasi variabel numerik.
- Menggunakan SMOTE untuk menangani ketidakseimbangan data.
- Membagi dataset menjadi training dan testing set dengan train_test_split.

4. Pengembangan Model untuk Memprediksi Employee Attrition:
   Melatih dan menguji berbagai model machine learning:
  - Random Forest dengan GridSearchCV untuk optimasi hyperparameter.
  - Gradient Boosting dengan learning rate dan max depth yang ditentukan.
  - Support Vector Machine (SVM) dengan probability=True.
  - Neural Network (MLPClassifier) dengan hidden layers (64,32).
  - Voting Classifier untuk menggabungkan hasil model terbaik.

5. Evaluasi Model dan Seleksi Model Terbaik:
- Menggunakan metrik evaluasi seperti Accuracy Score, AUC-ROC Score, Confusion Matrix, dan Classification Report.
- Menentukan model terbaik berdasarkan kombinasi Accuracy dan AUC-ROC Score.
- Model terbaik disimpan menggunakan joblib.

6. Visualisasi Hasil dan Dashboard:
- Merancang dan membangun dashboard interaktif menggunakan Google Looker Studio.

Dengan cakupan proyek yang telah dijelaskan di atas, diharapkan hasil analisis ini dapat memberikan wawasan mendalam bagi Jaya Jaya Maju dalam mengurangi tingkat attrition dan meningkatkan strategi manajemen karyawan secara efektif.


### Persiapan

Sumber data: dataset yang digunakan https://github.com/dicodingacademy/dicoding_dataset/tree/main/employee

Setup environment:

- Menggunakan bahasa pemrograman Python dengan pustaka utama:
  - pandas untuk manipulasi data.
  - matplotlib & seaborn untuk visualisasi data.
  - scikit-learn untuk preprocessing dan machine learning.
  - imblearn untuk menangani ketidakseimbangan data dengan SMOTE.
  - xgboost untuk model Gradient Boosting.
  - joblib untuk menyimpan model terbaik.
- Menggunakan Google Looker Studio untuk dashboard visualisasi hasil analisis.

## Business Dashboard

Dashboard ini menyajikan berbagai metrik penting untuk menganalisis tingkat attrition di perusahaan Jaya Jaya Maju. Berikut adalah hubungan data yang divisualisasikan dan penjelasannya:

- Jumlah karyawan, tingkat attrition, jumlah departemen, dan pendapatan bulanan rata-rata disajikan dalam score card untuk memberikan gambaran umum tentang kondisi tenaga kerja di perusahaan.
- Hubungan antara departemen dan jumlah karyawan yang mengundurkan diri menunjukkan bahwa beberapa departemen memiliki tingkat attrition yang lebih tinggi dibandingkan yang lain, yang dapat membantu dalam mengidentifikasi area dengan turnover tertinggi.
- Hubungan antara job role dan jumlah karyawan yang keluar membantu dalam memahami peran pekerjaan mana yang lebih rentan terhadap pengunduran diri.
- Hubungan antara lama bekerja di perusahaan dan tingkat attrition memperlihatkan tren kapan karyawan paling sering mengundurkan diri, apakah di tahun-tahun awal bekerja atau setelah bekerja dalam waktu lama.
- Hubungan antara tingkat pendidikan dan pendapatan bulanan memberikan wawasan apakah tingkat pendidikan memengaruhi gaji karyawan serta bagaimana distribusinya dalam perusahaan.
- Hubungan antara gender dan tingkat attrition membantu dalam menganalisis apakah terdapat perbedaan tingkat pengunduran diri antara karyawan laki-laki dan perempuan.
- Hubungan antara status pernikahan dan tingkat attrition memperlihatkan bagaimana status pernikahan dapat berpengaruh terhadap keputusan karyawan untuk tetap bekerja atau mengundurkan diri.
- Hubungan antara berbagai faktor dengan tingkat attrition menunjukkan faktor-faktor yang paling berkorelasi dengan keputusan karyawan untuk keluar dari perusahaan, seperti peran pekerjaan, jam lembur, perjalanan bisnis, dan status pernikahan.

Dashboard ini memberikan wawasan yang mendalam bagi manajer HR untuk memahami faktor-faktor yang memengaruhi attrition dan membantu dalam merancang strategi yang tepat untuk meningkatkan retensi karyawan.

<img width="571" alt="image" src="https://github.com/user-attachments/assets/1736b7c7-f0b2-42b6-8cab-5c3627e6d308" />


## Conclusion

Berdasarkan hasil analisis, jumlah total karyawan di Perusahaan Jaya Jaya Maju adalah 1.058, dengan persentase tingkat attrition sebesar 16,92%. Departemen yang memiliki tingkat attrition tertinggi adalah Sales, diikuti oleh departemen Research & Development. Dari segi jabatan, Human Resources dan Sales Executive adalah posisi yang paling sering mengalami attrition, menunjukkan kemungkinan adanya tekanan kerja atau kurangnya kepuasan kerja di jabatan tersebut. Faktor utama yang memiliki korelasi tinggi dengan attrition adalah OverTime, Business Travel, Job Role, dan Marital Status. Karyawan yang sering bekerja lembur dan memiliki jadwal perjalanan dinas yang tinggi cenderung lebih rentan terhadap attrition. Hasil model machine learning menunjukkan bahwa Random Forest dan Gradient Boosting memberikan akurasi dan stabilitas terbaik dalam memprediksi attrition, sehingga dapat digunakan untuk membantu perusahaan mengidentifikasi karyawan yang berisiko keluar serta merancang strategi retensi yang lebih efektif.

### Rekomendasi Action Items

1. Meningkatkan Retensi Karyawan di Departemen Sales
   Perusahaan perlu melakukan evaluasi mendalam terhadap lingkungan kerja di departemen Sales, seperti beban kerja, kompensasi, dan peluang pengembangan karier. Program insentif berbasis performa dan pelatihan khusus dapat membantu mengurangi tingkat attrition di departemen ini.

2. Mengurangi Dampak OverTime dan Business Travel terhadap Attrition
   Mengingat OverTime dan Business Travel memiliki korelasi tinggi dengan attrition, perusahaan dapat mempertimbangkan kebijakan work-life balance yang lebih baik, seperti fleksibilitas jam kerja, sistem kerja hybrid, dan insentif tambahan bagi karyawan yang sering bepergian untuk pekerjaan.

3. Meningkatkan Kepuasan Kerja pada Jabatan dengan Attrition Tinggi
   Posisi Human Resources dan Sales Executive memiliki tingkat attrition tinggi. Perusahaan dapat melakukan survei kepuasan kerja secara berkala dan menawarkan jalur pengembangan karier yang lebih jelas untuk meningkatkan retensi di jabatan tersebut.

4. Optimalisasi Kebijakan Marital Status dan Gender Data menunjukkan adanya perbedaan attrition berdasarkan marital status dan gender. Perusahaan dapat mengkaji lebih lanjut bagaimana faktor keseimbangan kerja-kehidupan dapat ditingkatkan bagi karyawan dengan kondisi tertentu, seperti fleksibilitas bagi orang tua atau tunjangan tambahan untuk kelompok rentan.

Dengan menerapkan action items ini, Jaya Jaya Maju dapat meningkatkan kepuasan kerja karyawan, mengurangi tingkat attrition, dan menciptakan strategi retensi yang lebih efektif.
