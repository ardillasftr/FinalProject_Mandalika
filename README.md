# FinalProject_Mandalika

Pada Stage 1 memiliki kesimpulan:
1. Apa saja attributes dan target output dari dataset
yang dipilih?
Attributes: Complain, Satisfaction Score, Cashback
Amount, Day Since Last Order, dan Tenure
Target : Churn
2. Untuk setiap feature yang disiapkan, apakah
sudah dicek distribusinya terhadap variabel target?
Complain : Tipe data boelean
SatisfactionScore : Normal
CashbackAmount : Positive skewed
DaySinceLastOrder : Positive skewed
Tenure : Positive skewed
3. Apakah sudah menemukan beberapa insight
• Dilihat dari feature Tenure, pengguna baru yaitu
pengguna yang memiliki Tenure < 1 minggu lebih
beresiko untuk churn.
• Nilai rata-rata satisfaction score tergolong biasa saja
(3,06 out of 5) sehingga perlu adanya peningkatan
layanan agar customer tetap berlangganan.
• Nilai rata- rata complain tergolong besar (0.28 out of 1)
sehingga perlu adanya evaluasi layanan agar customer
tetap berlangganan.
• Berdasarkan PreferredorderCat untuk kategori Laptop
& Accessory memiliki complain yang lebih banyak
dibandingkan kategori yang lain, sehingga beresiko
untuk churn.
• Mayoritas customer churn berdasarkan gender dan
marital status ialah laki-laki single sehingga perlu
adanya spesial service untuk customer laki-laki yang
masih single.

Pada saat Stage 2 memiliki kesimpulan:
Dataset telah dilakukan pre-processing sehingga menghasilkan 4 bagian dataset yang siap digunakan untuk modeling, yaitu Xtrain (4.899 baris), Ytrain (4.899 baris), Xtest (1.687 baris), dan Ytest (1.687 baris).


Feature yang masih digunakan ialah Tenure, CityTier, WarehouseToHome, Gender, NumberOfDeviceRegistered, PreferedOrderCat_Fashion, PreferedOrderCat_Grocery, PreferedOrderCat_Laptop & Accessory, PreferedOrderCat_Mobile Phone, PreferedOrderCat_Others, SatisfactionScore, MaritalStatus, Complain, DaySinceLastOrder, CashbackAmount CashbackAmount_std', OtherRevenue.


Feature extraction ialah OtherRevenue.

Pada Stage 3 memiliki kesimpulan: 
Penggunaan hyperparameter tuning pada model evaluation tidak cukup berpengaruh serta cenderung menurunkan metric model evaluation.

Penurunanan metric model evaluation menggunakan hyperparameter tuning sehingga model evaluation yang dipilih tanpa hyperparameter tuning. Adapun model evaluation yang dipilih ialah XGBOOST.

Tipe data bersifat non-linear sehingga model yang dapat digunakan ialah Decision Tree, K-Nearest Neighbors, XGBOOST. Penggunaan model XGBOOST disebabkan nilai evaluation recallnya tertinggi dan memiliki false negatif kecil dibandingkan dengan model non-linear lainnya.

