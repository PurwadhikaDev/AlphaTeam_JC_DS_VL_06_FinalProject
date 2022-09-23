## Final Project - Brazilian E-Commerce by Olist
#### By: Oktafransdy Taryaka & Safira Kemala Dewi (Alpha Team)
<hr>

<!-- ABOUT THE PROJECT -->
### BUSINESS PROBLEM UNDERSTANDING

**Context**

Olist adalah *marketplace* yang beroperasi sebagai perusahaan teknologi perangkat lunak SaaS (Software as a Service) di segmen *E-Commerce* sejak 2015 dan wilayah operasinya berpusat di Sao Paulo, Brazil. Perusahaan ini telah menghubungkan berbagai usaha mikro di Brazil dan menawarkan solusi kepada para pelaku usaha untuk meningkatkan penjualan mereka melalui platform online. 

Sebagai perusahaan <i>Fulfillment Center</i> yang akan melebarkan sayap ke pasar negara Brazil, data historis transaksi yang terdapat pada platform <i>E-Commerce</i> Brazil Olist ini menjadi sangat berharga. Perusahaan ini bergerak sebagai penyedia jasa logistik pihak ketiga, yang menyediakan pergudangan untuk pengelolaan stok produk dengan sistem terintegrasi, sehingga dapat memenuhi pesanan pelanggan dengan tepat waktu dan membebaskan perusahaan <i>E-Commerce</i> dalam mengelola prosesnya. 

Berikut gambaran secara umum Brazilian E-Commerce by Olist.

![Overview](https://github.com/PurwadhikaDev/AlphaTeam_JC_DS_VL_06_FinalProject/blob/4f661ae398a79c8acde147a9ff0d072056df9a83/Brazilian%20E-Commerce%20Milestones.png?raw=True)

**Problem Statement**

Bagi perusahaan <i>Fulfillment Center</i> yang akan melayani para pelaku usaha di platform <i>E-Commerce</i>, penting bagi perusahaan untuk dapat memprediksi perkembangan pasar di masa yang akan datang, sehingga manajemen dapat mengambil keputusan kapan saat yang tepat untuk melakukan ekspansi gudang dan penambahan karyawan.

Dari data yang dimiliki sekarang ini juga dapat dilakukan analisa untuk mendapatkan insight yang menjadi masukan bagi manajemen untuk melakukan optimalisasi pada proses operasional. 

**Goals**

Berdasarkan masalah diatas, Machine Learning Project ini bertujuan untuk memprediksi penjualan produk, baik secara *Expected Revenue*, *Quantity Produk*, dan *Volume Total* dari produk *Health and Beauty* pada platform <i>E-Commerce</i> di masa yang akan datang, dengan harapan prediksi yang dihasilkan dapat dimanfaatkan untuk pengambilan keputusan manajemen di perusahaan. 

**Analytic Approach**

Jadi, yang akan kita lakukan adalah menganalisis data Brazilian E-Commerce untuk menemukan pola yang tersembunyi dari fitur-fitur yang ada, menganalisis tren dan pertumbuhan penjualan produk, dan menjelaskan korelasi antar fitur.

Kemudian dari Data Brazilian E-Commerce tadi, kita akan bangun sebuah model *Timeseries Forecasting* untuk memprediksi penjualan produk baik dari segi Revenue, Quantity, maupun Volume barang yang terjual untuk menjadi alat bantu bagi pengambilan keputusan oleh manajemen.


**Metric Evaluation**

Evaluasi Metric yang digunakan adalah MAPE, dimana MAPE menggambarkan selisih rata-rata dari nilai Forecast dengan nilai sesungguhnya yang dinotasikan dalam bentuk persentase. MAPE juga merupakan metrics yang paling banyak digunakan karena kemudahan interpretasinya dibandingkan metric lain.


### **Conclusion & Recommendation**

**Conclusion**

* Untuk model prediksi Expected Revenue, digunakan feature engineering Binning data bulanan dimana model menghasilkan MAPE 12.4%, setelah dilakukan Hyperparameter Tuning didapati performa model meningkat dengan MAPE menjadi 11.5%. Nilai MAPE 11,5% menjadikan model ini dapat dikategorikan ke dalam *'good forecasting'* (Lewis, 1982).

* Untuk model prediksi Quantity Sales, digunakan feature engineering Binning data mingguan & Log Transform dimana model menghasilkan MAPE 21.3%, setelah dilakukan Hyperparameter Tuning didapati ada sedikit peningkatan performa model dengan MAPE menjadi 21.1%. Nilai MAPE 21.1% menjadikan model ini dapat dikategorikan ke dalam *'reasonable forecasting'* (Lewis, 1982).

* Untuk model prediksi Volume, digunakan feature engineering Binning Mingguan & Log Transform dimana model menghasilkan MAPE 32%, setelah dilakukan Hyperparamter Tuning didapati ada sedikit peningkatan performa model dengan MAPE menjadi 31.7%. Nilai MAPE 31.7% menjadikan model ini dapat dikategorikan ke dalam *'reasonable forecasting'* (Lewis, 1982).


**Recommendation**

* Expected Revenue untuk bulan September 2018 adalah R$46,760 Dengan asumsi Item Management Fee 5%, maka expected income dari perusahaan adalah R$2,338.

* Expected Volume untuk bulan September 2018 adalah 3,554 liter. Disarankan untuk melakukan replenishment barang setiap minggu agar tidak perlu menyediakan kapasitas gudang 3,600 liter, untuk angka tertinggi expected volume ada pada 739 Liter pada minggu terakhir pada bulan September 2018.

* Replenishment dapat dilakukan pada Weekend (Sabtu/Minggu) karena dari data exploration, terlihat bahwa trend pesanan barang paling rendah di hari Sabtu/Minggu.

* Apabila memungkinkan, tambahkan informasi produk seperti Brand, Jenis Produk, Nama Produk pada data untuk memungkinkan forecast spesifik terhadap item-item tersebut.

* Apabila memungkinkan, dapatkan informasi stock per item di gudang, untuk memungkinkan hasil forecast Sales Quantity digunakan untuk menjadi masukan rekomendasi kapan harus dilakukan replenishment suatu item.

* Tambahkan data historis untuk meningkatkan performa model yang di training.
