# Final Project
## Kelompok Mandalika

# Deskripsi
Sebuah perusahaan e-commerce mengalami peningkatan jumlah pelanggan yang berhenti berlangganan dalam satu bulan terakhir. Perusahaan tentu saja ingin menjaga pelanggan agar tetap berlangganan dan meminta tim data scientist untuk memprediksi potensi pelanggan yang akan berhenti berlangganan (churn) dengan mengharapkan revenue yang optimal.

# Tujuan
Mencegah pelanggan untuk berhenti berlangganan (churn) dengan meningkatkan satisfaction score dan menurunkan jumlah komplain sehingga dapat mencegah kehilangan revenue.

# Ringkasan
## Pada Stage 1 memiliki kesimpulan:
<ol> 
  <li>Apa saja attributes dan target output dari dataset
yang dipilih?
Attributes: Complain, Satisfaction Score, Cashback
Amount, Day Since Last Order, dan Tenure
Target : Churn</li>
  <li>Untuk setiap feature yang disiapkan, apakah
sudah dicek distribusinya terhadap variabel target?
Complain : Tipe data boelean
SatisfactionScore : Normal
CashbackAmount : Positive skewed
DaySinceLastOrder : Positive skewed
Tenure : Positive skewed </li>
  <li> Apakah sudah menemukan beberapa insight?
    <ul>
      <li>Dilihat dari feature Tenure, pengguna baru yaitu pengguna yang memiliki Tenure < 1 minggu lebih beresiko untuk churn.</li>
      <li>Nilai rata-rata satisfaction score tergolong biasa saja (3,06 out of 5) sehingga perlu adanya peningkatan layanan agar customer tetap berlangganan.</li>
      <li>Nilai rata- rata complain tergolong besar (0.28 out of 1) sehingga perlu adanya evaluasi layanan agar customer tetap berlangganan.</li>
      <li>Berdasarkan PreferredorderCat untuk kategori Laptop & Accessory memiliki complain yang lebih banyak dibandingkan kategori yang lain, sehingga beresiko   untuk churn.</li>
      <li>Mayoritas customer churn berdasarkan gender dan
marital status ialah laki-laki single sehingga perlu
adanya spesial service untuk customer laki-laki yang
masih single.</li>
      </ul>
    </ol>
    
## Pada Stage 2 memiliki kesimpulan:
<ol>
  <li>Dataset telah dilakukan pre-processing sehingga menghasilkan 4 bagian dataset yang siap digunakan untuk modeling, yaitu Xtrain (4.899 baris), Ytrain (4.899 baris), Xtest (1.687 baris), dan Ytest (1.687 baris).</li>
  <li>Feature yang masih digunakan ialah Tenure, CityTier, WarehouseToHome, Gender, NumberOfDeviceRegistered, PreferedOrderCat_Fashion, PreferedOrderCat_Grocery, PreferedOrderCat_Laptop & Accessory, PreferedOrderCat_Mobile Phone, PreferedOrderCat_Others, SatisfactionScore, MaritalStatus, Complain, DaySinceLastOrder, CashbackAmount CashbackAmount_std', OtherRevenue.</li>
  <li>Feature extraction ialah OtherRevenue.
    </ol>

## Pada Stage 3 memiliki kesimpulan: 
  <ol>
    <li>Penggunaan hyperparameter tuning pada model evaluation tidak cukup berpengaruh serta cenderung menurunkan metric model evaluation.</li>
    <li>Penurunanan metric model evaluation menggunakan hyperparameter tuning sehingga model evaluation yang dipilih tanpa hyperparameter tuning. Adapun model evaluation yang dipilih ialah XGBOOST.</li>
    <li>Tipe data bersifat non-linear sehingga model yang dapat digunakan ialah Decision Tree, K-Nearest Neighbors, XGBOOST. Penggunaan model XGBOOST disebabkan nilai evaluation recallnya tertinggi dan memiliki false negatif kecil dibandingkan dengan model non-linear lainnya.
