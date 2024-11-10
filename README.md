# Chapter-3: Computer Vision and Natural Language Processing<br>
03_Tim 5_1<br>
    *Tujuan*: Menerapkan dan membandingkan metode peningkatan gambar (image enhancement) untuk mencerahkan foto dengan warna gelap, lalu menambahkannya ke *portfolio* peserta.<br>
        **Deskripsi Tugas**:<br> 
        - Meniru pendekatan teknologi kamera terbaru yang diterapkan oleh Apple (Deep Fusion dan Photonic Engine) dan Samsung (Adaptive Tetra-squared Pixel Sensor) dalam menangani gambar minim cahaya.<br>
        - Menerapkan operasi *Max Pooling* untuk meningkatkan kecerahan gambar dan membandingkan hasilnya dengan metode *Contrast Limited Adaptive Histogram Equation* (CLAHE), yang mampu mencerahkan gambar dengan lebih baik di kondisi cahaya rendah.<br>
        **Langkah-Langkah Tugas**:<br>
        1. **Konversi Warna dan Thresholding**:<br>
        - Mengonversi gambar dari BGR ke RGB, BGR ke grayscale, dan grayscale ke binary.<br>
        - Membuat histogram gambar asli dan grayscale untuk analisis distribusi piksel.<br>
        2. **Penggunaan Pooling**:<br>
        - Menggunakan operasi **Max Pooling** dan **CLAHE** untuk melihat perbandingan hasil.<br>
        - Mengulang fungsi *block_reduce()* dengan fungsi np.min (Min Pooling) dan np.mean (Average Pooling) untuk memahami perbedaan antara metode pooling.<br>
        3. **Pertanyaan Teoritis**:<br>
        - Menjawab pertanyaan tentang keunggulan Max Pooling di PyTorch dibandingkan Scikit-image, perbedaan Min Pooling dan Average Pooling, serta keunggulan CLAHE dibanding Max Pooling untuk gambar bernuansa gelap.<br>
    *Checklist Tugas*: Peserta perlu menyelesaikan beberapa #TODO, seperti konversi warna, pemanggilan metode pooling, penerapan CLAHE, dan menyimpan gambar yang disempurnakan.<br>

03_Tim 5_2<br>
    *Tujuan*: Menerapkan *Transfer Learning* menggunakan beberapa model *pre-trained CNN* dari PyTorch untuk mengklasifikasikan digit tulisan tangan (0-9), dan mengevaluasi efek pembekuan (freezing) beberapa bagian dari *neural network*.<br>
        **Deskripsi Tugas**:<br>
        Sebuah fasilitas robot di Kalimantan Timur meminta peserta untuk mengembangkan model Computer Vision agar robot dapat mengenali angka tulisan tangan. Karena tenggat waktu yang ketat, peserta diminta menggunakan *Transfer Learning* dengan model *pre-trained* (DenseNet, ResNet18, dan ViT) untuk efisiensi.<br>
        **Langkah Tugas**:<br>
        1. **Pemodelan dengan DenseNet**:<br>
        - Mengubah layer pertama dan terakhir dari DenseNet agar sesuai dengan data MNIST (input 1 channel dan output 10 kelas).<br>
        - Menentukan *hyperparameter* dan melatih model sepenuhnya.<br>
        2. **Freezing Layer**:<br>
        - Melatih ulang model DenseNet setelah membekukan beberapa bagian layer, yaitu *denseblock1* untuk satu model dan *denseblock1* serta *denseblock2* untuk model lainnya.<br>
        - Menganalisis performa model sebelum dan sesudah pembekuan layer.<br>
        3. **Bonus**:<br>
        - Mereplikasi langkah-langkah ini menggunakan model *ResNet18* dan *Vision Transformer (ViT)* sebagai perbandingan.<br>
    *Checklist*: Peserta perlu menyelesaikan beberapa #TODO, seperti mengubah layer input/output, menentukan *batch size*, *learning rate*, *loss function*, memanggil model sesuai parameter, dan menjawab beberapa pertanyaan.<br>
    *Pertanyaan Teoritis*:<br>
    - Mengapa *Transfer Learning* dengan layer yang dibekukan memiliki akurasi akhir yang lebih rendah?<br>
    - Mengapa semakin banyak layer yang dibekukan, akurasi model di awal iterasi semakin rendah dan waktu pelatihan semakin cepat?<br>

03_Tim 5_3<br>
        **Langkah Tugas**:<br>
        1. **Memanggil Model YOLOv5**: <br>
      - Menggunakan YOLOv5 dari *ultralytics* untuk mendeteksi objek dalam video YouTube yang ditentukan.<br>
      2. **Checklist Tugas**:<br>
    - Peserta perlu melengkapi beberapa #TODO, termasuk memanggil model YOLOv5, mengisi parameter dengan URL video YouTube yang relevan, dan menjawab pertanyaan teoritis terkait konsep deteksi objek.<br>
        3. **Pertanyaan Teoritis**:<br>
     - Menjelaskan perbedaan antara "image classification" dan "object detection".<br>
    - Menentukan video mana yang memiliki akurasi deteksi terburuk oleh YOLOv5 dan menjelaskan alasannya.<br>

03_Tim 3_4<br>
        *Langkah-langkah yang harus dilakukan*:<br>
        1. *Aktifkan GPU* untuk pelatihan model.<br>
        2. *Impor dan preprocess data training* untuk tweet tentang bencana.<br>
        3. Tentukan *fitur (X)* dan *label (Y** untuk klasifikasi.<br>
        4. *Pecah dataset* menjadi 80% untuk training dan 20% untuk validasi.<br>
        5. Tentukan *batch size*, *jumlah epoch*, dan *learning rate*.<br>
        6. Buat *DataLoader* untuk training, validasi, dan testing.<br>
        7. Jika akurasi kurang dari 80%, lakukan penyesuaian *hyperparameters*.<br>
