# Prediksi dan Klasifikasi Penyakit Tanaman Kentang Menggunakan DenseNet121 🍂

# Deskripsi Proyek
Proyek ini bertujuan untuk mendeteksi dan mengklasifikasikan kondisi tanaman kentang berdasarkan gambar daun, mengidentifikasi apakah tanaman mengalami penyakit early blight, late blight, atau dalam kondisi sehat. Model ini dilatih menggunakan dataset yang terdiri dari 1.722 gambar untuk training, 430 gambar untuk validasi, dan 2.152 gambar untuk pengujian, dengan tiga kategori label utama, yaitu Potato___Early_blight (0), Potato___Late_blight (1), dan Potato___healthy (2).

Model dikembangkan menggunakan arsitektur DenseNet121 sebagai backbone dengan bobot awal dari ImageNet, yang tidak dilatih ulang pada tahap awal untuk mempertahankan fitur-fitur pretrained. Setelah backbone, model dilengkapi dengan beberapa lapisan tambahan, termasuk normalisasi batch, lapisan fully connected dengan aktivasi ReLU, dropout untuk mengurangi overfitting, dan lapisan output dengan tiga neuron menggunakan aktivasi softmax. Model ini dirancang untuk mengoptimalkan kinerja klasifikasi dengan memanfaatkan kombinasi feature extraction dari DenseNet dan lapisan tambahan yang lebih dalam untuk meningkatkan akurasi dalam mendeteksi penyakit pada tanaman kentang.

# Cara Instalasi
Sebelum menjalankan proyek ini, pastikan Anda memiliki Python dan semua dependensi yang diperlukan. Anda dapat menginstalnya dengan menggunakan file requirements.txt yang telah disediakan.
1. Pastikan Python telah terinstal
Proyek ini berjalan dengan Python 3.7 atau versi lebih tinggi. Anda dapat mengecek versi Python dengan perintah berikut:
```
python --version
```
2. Buat virtual environment (Opsional, tetapi disarankan)
Disarankan menggunakan virtual environment agar tidak mengganggu sistem utama. Jalankan perintah berikut untuk membuat dan mengaktifkan environment baru:
```
python -m venv env
source env/bin/activate  # Untuk pengguna macOS/Linux
env\Scripts\activate     # Untuk pengguna Windows
```
3. Instal dependensi proyek
Setelah virtual environment aktif, instal semua dependensi dengan perintah berikut:
```
pip install -r requirements.txt
```
5. Verifikasi Instalasi
Untuk memastikan semua dependensi telah terinstal dengan benar, jalankan:
```
python -c "import tensorflow as tf; print(tf.__version__)"
```

# Hasil

Hasil pelatihan model selama 20 epoch menunjukkan kinerja yang sangat baik dalam mengklasifikasikan kondisi tanaman kentang berdasarkan daun yang terkena penyakit atau dalam kondisi sehat. Pada akhir pelatihan, model mencapai akurasi pelatihan sebesar 99,05% dengan nilai loss 0,0573, yang menunjukkan bahwa model mampu mengenali pola dengan sangat baik pada data latih. 

![Plot Akurasi](https://github.com/adstika20/Image-Classification/blob/main/Plot%20Akurasi.png)

Grafik Loss Curve di sebelah kiri menunjukkan bahwa baik train loss maupun validation loss mengalami penurunan yang konsisten seiring bertambahnya epoch, yang mengindikasikan bahwa model semakin memahami pola dalam data dan mengalami konvergensi yang baik.

Pada grafik Accuracy Curve di sebelah kanan, terlihat bahwa akurasi pelatihan meningkat secara bertahap dari awal hingga akhir pelatihan, sedangkan akurasi validasi tetap tinggi dan stabil di atas 95% sejak awal. Stabilnya akurasi validasi menunjukkan bahwa model tidak mengalami overfitting yang signifikan, karena performa model pada data yang belum pernah dilihat tetap tinggi.

Saat diuji menggunakan dataset pengujian, model tetap menunjukkan performa yang sangat baik dengan test loss sebesar 0,0534 dan test accuracy sebesar 98,70%. Hal ini menunjukkan bahwa model memiliki kemampuan generalisasi yang sangat baik dalam mengenali pola dan fitur penyakit pada daun kentang, sehingga dapat digunakan sebagai alat bantu diagnosis yang andal dalam mendeteksi penyakit tanaman secara otomatis. Akurasi yang tinggi serta gap yang kecil antara train loss dan validation loss menunjukkan bahwa model ini cukup stabil dan dapat digunakan dalam skenario dunia nyata tanpa mengalami penurunan kinerja yang signifikan.

# Rekomendasi Action Items

1. Melakukan augmentasi data yang lebih ekstensif (rotasi, flipping, perubahan pencahayaan, dan noise).
2. Memperluas dataset dengan lebih banyak sampel dari berbagai sumber.
3. Melatih beberapa lapisan atas DenseNet121 agar lebih spesifik dalam mengenali fitur penyakit.
4. Menyesuaikan hyperparameter untuk meningkatkan performa model.
5. Mencoba model lain seperti EfficientNet, ResNet50, berdasarkan akurasi dan efisiensi komputasi.

# Sumber Data 
[Kaggle](https://www.kaggle.com/datasets/hafiznouman786/potato-plant-diseases-data/data)



