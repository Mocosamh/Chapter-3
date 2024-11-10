# Chapter-3: Computer Vision and Natural Language Processing<br>
03_Tim 5_1<br>
    *Tujuan*: Menerapkan dan membandingkan metode peningkatan gambar (image enhancement) untuk mencerahkan foto dengan warna gelap, lalu menambahkannya ke *portfolio* peserta.<br>
        **Deskripsi Tugas**:<br>
        - Meniru pendekatan teknologi kamera terbaru yang diterapkan oleh Apple (Deep Fusion dan Photonic Engine) dan Samsung (Adaptive Tetra-squared Pixel Sensor) dalam menangani gambar minim cahaya.
        - Menerapkan operasi *Max Pooling* untuk meningkatkan kecerahan gambar dan membandingkan hasilnya dengan metode *Contrast Limited Adaptive Histogram Equation* (CLAHE), yang mampu mencerahkan gambar dengan lebih baik di kondisi cahaya rendah.<br>
        **Langkah-Langkah Tugas**:<br>
        1. **Konversi Warna dan Thresholding**:
        - Mengonversi gambar dari BGR ke RGB, BGR ke grayscale, dan grayscale ke binary.
        - Membuat histogram gambar asli dan grayscale untuk analisis distribusi piksel.
        2. **Penggunaan Pooling**:
        - Menggunakan operasi **Max Pooling** dan **CLAHE** untuk melihat perbandingan hasil.
        - Mengulang fungsi *block_reduce()* dengan fungsi np.min (Min Pooling) dan np.mean (Average Pooling) untuk memahami perbedaan antara metode pooling.
        3. **Pertanyaan Teoritis**:
        - Menjawab pertanyaan tentang keunggulan Max Pooling di PyTorch dibandingkan Scikit-image, perbedaan Min Pooling dan Average Pooling, serta keunggulan CLAHE dibanding Max Pooling untuk gambar bernuansa gelap.<br>
    *Checklist Tugas*: Peserta perlu menyelesaikan beberapa #TODO, seperti konversi warna, pemanggilan metode pooling, penerapan CLAHE, dan menyimpan gambar yang disempurnakan.<br>

03_Tim 5_2<br>
    *Tujuan*: Menerapkan *Transfer Learning* menggunakan beberapa model *pre-trained CNN* dari PyTorch untuk mengklasifikasikan digit tulisan tangan (0-9), dan mengevaluasi efek pembekuan (freezing) beberapa bagian dari *neural network*.<br>
        **Deskripsi Tugas**:<br>
        Sebuah fasilitas robot di Kalimantan Timur meminta peserta untuk mengembangkan model Computer Vision agar robot dapat mengenali angka tulisan tangan. Karena tenggat waktu yang ketat, peserta diminta menggunakan *Transfer Learning* dengan model *pre-trained* (DenseNet, ResNet18, dan ViT) untuk efisiensi.<br>
        **Langkah Tugas**:<br>
        1. **Pemodelan dengan DenseNet**:
        - Mengubah layer pertama dan terakhir dari DenseNet agar sesuai dengan data MNIST (input 1 channel dan output 10 kelas).
        - Menentukan *hyperparameter* dan melatih model sepenuhnya.
        2. **Freezing Layer**:
        - Melatih ulang model DenseNet setelah membekukan beberapa bagian layer, yaitu *denseblock1* untuk satu model dan *denseblock1* serta *denseblock2* untuk model lainnya.
        - Menganalisis performa model sebelum dan sesudah pembekuan layer.
        3. **Bonus**:
        - Mereplikasi langkah-langkah ini menggunakan model *ResNet18* dan *Vision Transformer (ViT)* sebagai perbandingan.<br>
    *Checklist*: Peserta perlu menyelesaikan beberapa #TODO, seperti mengubah layer input/output, menentukan *batch size*, *learning rate*, *loss function*, memanggil model sesuai parameter, dan menjawab beberapa pertanyaan.<br>
    *Pertanyaan Teoritis*:<br>
    - Mengapa *Transfer Learning* dengan layer yang dibekukan memiliki akurasi akhir yang lebih rendah?
    - Mengapa semakin banyak layer yang dibekukan, akurasi model di awal iterasi semakin rendah dan waktu pelatihan semakin cepat?<br>

03_Tim 5_3<br>
        **Langkah Tugas**:<br>
        1. **Memanggil Model YOLOv5**: 
      - Menggunakan YOLOv5 dari *ultralytics* untuk mendeteksi objek dalam video YouTube yang ditentukan.
      2. **Checklist Tugas**:
    - Peserta perlu melengkapi beberapa #TODO, termasuk memanggil model YOLOv5, mengisi parameter dengan URL video YouTube yang relevan, dan menjawab pertanyaan teoritis terkait konsep deteksi objek.
        3. **Pertanyaan Teoritis**:
     - Menjelaskan perbedaan antara "image classification" dan "object detection".
    - Menentukan video mana yang memiliki akurasi deteksi terburuk oleh YOLOv5 dan menjelaskan alasannya.<br>

03_Tim 3_4<br>
        *Langkah-langkah yang harus dilakukan*:<br>
        1. *Aktifkan GPU* untuk pelatihan model.
        2. *Impor dan preprocess data training* untuk tweet tentang bencana.
        3. Tentukan *fitur (X)* dan *label (Y** untuk klasifikasi.
        4. *Pecah dataset* menjadi 80% untuk training dan 20% untuk validasi.
        5. Tentukan *batch size*, *jumlah epoch*, dan *learning rate*.
        6. Buat *DataLoader* untuk training, validasi, dan testing.
        7. Jika akurasi kurang dari 80%, lakukan penyesuaian *hyperparameters*.<br>