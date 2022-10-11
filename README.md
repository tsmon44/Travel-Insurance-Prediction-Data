# EDA dan Supervised Machine Learning pada Travel Insurance Prediction Data

## Exploratory Data Analysis (EDA)

  Exploratory Data Analysis (EDA) atau analisis data eksploratif merupakan metode eksplorasi data untuk membuat gambaran keseluruhan 
(summary) data sehingga mudah untuk dipahami. 
EDA digunakan untuk :
1. Mengidentifikasi pola suatu data
2. Menemukan sebuah penyimpangan 
3. Menguji hipotesis 
4. Memeriksa asumsi melalui visualisasi data

  Dengan melakukan EDA, pengguna akan sangat terbantu dalam mendeteksi kesalahan dari awal, mengecek kualitas data yang dilanjutkan dengan proses cleansing dan processing, dapat mengidentifikasi outlier, mengetahui hubungan antar data, serta mendapatkan insight data. Proses EDA ini sangat bermanfaat dalam proses analisis statistik.  .
  
## Supervised Machine Learning

  Supervised Learning adalah machine learning model yang membutuhkan data target. Model-model di Supervised Learning membutuhkan data training berupa input data dan target data yang diinginkan. Supervised Learning menggunakan data training untuk membuat machine learning model dan model ini akan digunakan untuk diuji pada data test. 
  Random Forest merupakan salah satu jenis algoritma machine learning supervised learning. Random Forest adalah kombinasi masing-masing tree dari decision tree yang kemudian digabungkan menjadi satu model, digunakan untuk pengklasifikasian data set dalam jumlah besar. Ada beberapa macam sampling methods pada Random forest, yaitu model Random Forest biasa, model Random Forest dengan Undersampling, model Random Forest dengan Oversampling, dan model Random Forest combining Undersampling Oversampling.

## Travel Insurance Prediction Data

  Sebuah perusahaan tour & travels yang menawarkan paket asuransi perjalanan kepada pelanggannya. Perusahaan perlu mengetahui pelanggan mana yang akan tertarik untuk membelinya berdasarkan databasenya. Asuransi ditawarkan kepada beberapa pelanggan pada tahun 2019 dan data yang diberikan telah disarikan dari kinerja/penjualan paket selama periode itu. Data diberikan untuk hampir 2000 pelanggan sebelumnya.

Dataset dapat didownload di https://www.kaggle.com/datasets/tejashvi14/travel-insurance-prediction-data?datasetId=1457162&searchQuery=acc

## EDA Conclusion

1. Data tidak mengandung masalah besar. Hanya ada beberapa nilai baris duplikat yang telah ditangani
2. Secara keseluruhan, nilai minimum dan maksimum masuk akal untuk setiap kolom
3. ChronicDiseases dan TravelInsurance adalah kolom boolean/biner karena nilainya 0 atau 1, tidak perlu disimpulkan simetrinya. Karena ini dapat menjadi variabel target untuk pemodelan, nanti akan diperiksa balance-level
4. Mean ~ 50% (Median) pada kolom Age, AnnualIncome, dan FamilyMembers, menunjukan symmetrical distribution
5. Dari boxplot tidak ada outlier
6. The true continuous numeric features: AnnualIncome agak symmetric (tidak perlu transform ke approximate normal distribution)
7. Pada target variable, ChronicDiseases dan TravelInsurance = 0 lebih sering muncul pada dataset. Tetapi, the imbalance condition tidak parah (masih OK)

## Insight yang diperoleh dari Travel Insurance Prediction Data melalui exploratory data analysis:

1. Pelanggan Private Sector/Self Employed dan Government Sector lebih banyak yang tidak membeli travel insurance
2. Pelanggan graduate dari perguruan tinggi lebih banyak yang tidak membeli travel insurance, begitu juga dengan pelanggan yang tidak graduate
3. Pelanggan yang tidak memiliki Chronic Diseases lebih banyak yang tidak membeli travel insurance, begitu juga dengan pelanggan yang memiliki Chronic Diseases
4. Pelanggan yang tidak pernah membeli plane tickets tidak membeli travel insurance daripada yang membeli travel insurance, tetapi pelanggan yang pernah membeli plane tickets hampir 50:50 membeli dan tidak membeli travel insurance
5. Pelanggan yang tidak pernah traveled abroad tidak membeli travel insurance. Sebaliknya, pelanggan yang pernah traveled abroad membeli travel insurance
6. Private Sector/Self Employed merupakan pelanggan yang paling banyak memiliki pendapatan tahunan
7. Usia 28 paling rentan terkena penyakit kronis

## Supervised Machine Learning Conclusion

1. Model dengan konfigurasi yang memiliki nilai precision terbaik adalah Model Random Forest Biasa saja
2. Model dengan konfigurasi yang memiliki nilai recall terbaik adalah Model Random Forest dengan Undersampling
3. Model dengan konfigurasi yang memiliki nilai F1-Score terbaik adalah Model Random Forest Biasa saja atau Model Random Forest dengan Oversampling dan Undersampling dengan koefisien oversampling = 0.6 dan koefisien undersampling = 0.7
