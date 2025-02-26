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

Hasil pelatihan model selama 20 epoch menunjukkan kinerja yang sangat baik dalam mengklasifikasikan kondisi tanaman kentang berdasarkan daun yang terkena penyakit atau dalam kondisi sehat. Pada akhir pelatihan, model mencapai akurasi pelatihan sebesar 99,05% dengan nilai loss 0,0573, yang menandakan bahwa model mampu mengenali pola dengan sangat baik pada data latih. Selain itu, akurasi validasi yang tinggi dan stabil menunjukkan bahwa model memiliki generalisasi yang baik terhadap data baru, sehingga dapat diandalkan untuk mendeteksi penyakit tanaman kentang secara akurat.

![Plot Akurasi](https://github.com/adstika20/Image-Classification/blob/main/download.png)

Berdasarkan plot kurva loss dan akurasi dari model prediksi dan klasifikasi penyakit tanaman kentang menggunakan DenseNet121 sebagai feature extractor, diperoleh beberapa temuan penting. Kurva loss menunjukkan bahwa baik train loss maupun validation loss mengalami penurunan signifikan sejak awal pelatihan dan mencapai titik yang stabil di sekitar nilai rendah. Hal ini menunjukkan bahwa model belajar secara efektif dan tidak mengalami overfitting yang serius.

Kurva akurasi menunjukkan peningkatan yang konsisten, di mana train accuracy terus meningkat hingga mendekati 100%, sedangkan validation accuracy juga tinggi dan stabil, bahkan sejak epoch awal. Dengan hasil evaluasi pada test set yang menunjukkan test accuracy sebesar 98.98% dan test loss sebesar 0.0292, dapat disimpulkan bahwa model ini memiliki performa yang sangat baik dalam mengklasifikasikan penyakit tanaman kentang.

Arsitektur model yang menggunakan DenseNet121 sebagai feature extractor dan menambahkan lapisan tambahan seperti Conv2D, Batch Normalization, dan Dropout, membantu dalam meningkatkan generalisasi model terhadap data yang belum pernah dilihat. Dengan hasil ini, model ini siap digunakan dalam sistem deteksi penyakit tanaman kentang berbasis deep learning.

# Rekomendasi Action Items

1. Melakukan augmentasi data yang lebih ekstensif (rotasi, flipping, perubahan pencahayaan, dan noise).
2. Memperluas dataset dengan lebih banyak sampel dari berbagai sumber.
3. Melatih beberapa lapisan atas DenseNet121 agar lebih spesifik dalam mengenali fitur penyakit.
4. Menyesuaikan hyperparameter untuk meningkatkan performa model.
5. Mencoba model lain seperti EfficientNet, ResNet50, berdasarkan akurasi dan efisiensi komputasi.

# Sumber Data 
[Kaggle](https://www.kaggle.com/datasets/hafiznouman786/potato-plant-diseases-data/data)



