**Study Group I-Smile: EDA to Machine Learning**

**Brief Mini Project Competition**

Laboratorium I-Smile · Program Studi S1 Teknik Komputer, Telkom University

Dirilis pada **Hari 4, Jumat, 9 Oktober 2026**. Seluruh tim menerima brief pada waktu yang sama, sehingga jatah waktu pengerjaan setiap tim sama.

# **1\. Gambaran Umum**

Mini Project adalah penutup Study Group. Setiap kelompok menyelesaikan **satu alur pemodelan secara utuh dan mandiri**, dari data mentah sampai model yang dievaluasi, lalu mempresentasikannya di depan juri.

* Dikerjakan **per kelompok, di luar jam pertemuan**.

* **Dataset dipilih sendiri** oleh kelompok, dengan persetujuan asisten pendamping (bagian 3).

* Jenis masalah boleh **regresi** (menebak angka) atau **klasifikasi** (menebak kategori).

* Yang dinilai adalah **proses dan pemahaman**, bukan skor model tertinggi.

# **2\. Jadwal Penting**

| Waktu | Kegiatan |
| :---- | :---- |
| Jumat, 9 Okt 2026 | Rilis brief Mini Project (Hari 4\) |
| Sabtu, 10 Okt 2026, 08.00 | **Spreadsheet slot hari presentasi dibuka** (siapa cepat dia dapat) |
| Minggu, 11 Okt 2026, 23.59 | **Batas pengisian judul dan link dataset** di spreadsheet Pengajuan Dataset |
| Senin, 12 Okt 2026, 12.00 | Batas keputusan persetujuan dataset dari asisten |
| Senin, 12 Okt 2026, 23.59 | Batas pengajuan dataset pengganti (bila dataset pertama ditolak) |
| Kamis, 15 Okt 2026, 23.59 | **Batas pengumpulan notebook dan slide, berlaku untuk seluruh tim** |
| Sebelum tim tampil | **Wajib mengisi form Post-Test dan Evaluasi** (setiap peserta) |
| Jumat, 16 Okt dan Sabtu, 17 Okt 2026, mulai 17.00 | **Presentasi Mini Project**; setiap tim tampil pada salah satu hari |
| Minggu, 18 Okt 2026 | Pengumuman juara secara online di grup WhatsApp Study Group |

*Batas pengumpulan sama untuk tim yang tampil Jumat maupun Sabtu, agar tidak ada tim yang memperoleh waktu kerja lebih banyak.*

# **3\. Ketentuan Dataset**

## **Syarat dataset**

* **Tabular**: berbentuk baris dan kolom (CSV atau Excel).

* **Sumber publik** yang dapat diakses juri, misalnya Kaggle, UCI Machine Learning Repository, Satu Data Indonesia (data.go.id), atau BPS. Sumber dan tautannya wajib dicantumkan.

* **Target jelas**: satu kolom yang ditebak, dengan jenis masalah regresi atau klasifikasi.

* **Ukuran memadai**: minimal **500 baris** dan **5 kolom fitur**, agar data uji dan cross-validation tetap bermakna.

* **Dilarang memakai dataset Study Group**: California Housing (Dataset A) dan Heart Disease UCI (Dataset B).

* **Contoh project** tersedia di bawah tabel spreadsheet Pengajuan Dataset sebagai gambaran. **Dataset contoh tidak boleh dipakai.**

* **Satu dataset untuk satu kelompok.** Bila dua kelompok mengisi link yang sama, kelompok yang lebih dulu mengisi (dilihat dari riwayat versi spreadsheet) yang berhak memakainya.

## **Prosedur persetujuan (ACC)**

1. Diskusikan judul project dan dataset di grup WhatsApp kelompok.

2. Isi **Judul Project** dan **Link Dataset** di baris kelompokmu pada **spreadsheet Pengajuan Dataset** (tautan tersedia di Pusat Link Study Group) paling lambat **Minggu, 11 Oktober 2026, pukul 23.59**.

3. Link yang sudah dipakai kelompok lain otomatis ditandai merah; segera ganti dataset bila barismu ditandai.

4. Asisten memeriksa kelayakan dataset dan mengisi kolom **Status** (Disetujui atau Ditolak, beserta alasannya) paling lambat **Senin, 12 Oktober 2026, pukul 12.00**.

5. Bila ditolak, ganti link di baris yang sama paling lambat **Senin, 12 Oktober 2026, pukul 23.59**.

6. **Project dengan dataset yang belum disetujui tidak dapat dipresentasikan.**

Daftar periksa yang dipakai asisten:

| Pemeriksaan | Pertanyaan |
| :---- | :---- |
| Target | Apakah ada satu kolom target yang jelas, dan jenis masalahnya regresi atau klasifikasi? |
| Ukuran | Minimal 500 baris dan 5 kolom fitur? |
| Sumber | Tautan dapat dibuka dan sumber datanya jelas? |
| Larangan | Bukan California Housing atau Heart Disease UCI, dan belum dipakai kelompok lain? |
| Kebocoran target | Tidak ada kolom fitur yang sebenarnya adalah jawaban (misalnya kolom turunan dari target)? |

# **4\. Ketentuan Pengerjaan**

Notebook wajib memuat seluruh tahapan berikut, sesuai materi Hari 1–4.

| Tahap | Yang wajib ada |
| :---- | :---- |
| EDA | Ringkasan data (info, describe), distribusi target, minimal **3 visualisasi** yang masing-masing disertai temuan |
| Data cleaning | Pemeriksaan missing value, duplikat, outlier, dan encoding kolom kategorik; **setiap keputusan disertai alasan** |
| Split data | train\_test\_split dengan test\_size=0.2 dan random\_state=42; klasifikasi memakai stratify=y |
| Model standar | **Regresi: wajib LinearRegression. Klasifikasi: wajib KNeighborsClassifier dengan scaling.** Model ini menjadi pembanding |
| Model lain | Opsional dan bebas (Decision Tree, Random Forest, XGBoost, LightGBM, MLP, dan lainnya). Bila dipakai, dibandingkan dengan model standar memakai aturan yang sama |
| Evaluasi | Regresi: **MAE, RMSE, R²**. Klasifikasi: **accuracy, precision, recall, confusion matrix**. Skor data latih dan data uji ditampilkan berdampingan |
| Pemilihan model | Perbandingan dan tuning memakai **cross-validation 5 lipatan** pada data latih. Data uji dipakai **satu kali** untuk model terpilih |
| Interpretasi | Arti metrik dalam bahasa awam, alasan memilih model, dan keterbatasan hasil |

**Tidak ada skor minimal.** Model dengan skor sedang tetapi prosesnya benar dan alasannya kuat dinilai lebih tinggi daripada skor tinggi tanpa penjelasan.

# **5\. Yang Dikumpulkan**

| Berkas | Ketentuan |
| :---- | :---- |
| Notebook | Format .ipynb dari Google Colab. **Runtime → Run all berjalan tanpa error.** Setiap tahap diberi judul dan penjelasan markdown. Dataset dimuat **dari tautan di dalam notebook** (Kaggle, UCI, atau Google Drive dengan akses Anyone with the link), sehingga juri dapat menjalankannya |
| Slide | Format **PDF**, maksimal **15 slide**, mengikuti kerangka wajib di bagian 6 |
| Penamaan berkas | Kelompok XX \- Judul Project (contoh: Kelompok 03 \- Prediksi Harga Mobil Bekas) |
| Cara pengumpulan | Satu anggota mengisi **form Pengumpulan Tugas Akhir** (tautan di Pusat Link Study Group): pilih nomor kelompok, lalu **upload 2 file terpisah**, yaitu slide (PDF) dan notebook (.ipynb). Link Colab boleh ditambahkan sebagai cadangan. Pengisian form **wajib login akun Google**, dan form ditutup tepat pukul 23.59 |

Presentasi memakai **satu laptop panitia** dengan berkas yang sudah dikumpulkan. **Berkas tidak dapat diubah setelah batas pengumpulan.**

# **6\. Kerangka Slide Wajib**

Urutan bagian berikut wajib diikuti agar juri dapat membandingkan seluruh tim dengan adil. Isi, jumlah slide per bagian, dan desain bebas.

| No | Bagian | Isi minimal |
| :---- | :---- | :---- |
| 1 | Judul | Judul project, nomor kelompok, nama dan NIM anggota |
| 2 | Masalah | Pertanyaan yang ingin dijawab, kolom target, jenis masalah, dan siapa yang memakai hasilnya |
| 3 | Dataset | Sumber dan tautan, jumlah baris dan kolom, arti kolom-kolom penting |
| 4 | EDA | Temuan utama beserta visualisasi pendukung |
| 5 | Data cleaning | Tabel masalah → tindakan → alasan |
| 6 | Pemodelan | Cara split, preprocessing per model, model standar, dan model lain (bila ada) |
| 7 | Evaluasi | Tabel perbandingan model: skor cross-validation, skor latih vs uji, metrik wajib |
| 8 | Pemilihan model | Model terpilih dan alasannya, hasil satu kali di data uji |
| 9 | Kesimpulan | Jawaban atas pertanyaan di bagian 2 dan keterbatasan hasil |
| 10 | Pembagian tugas | **Wajib.** Kontribusi setiap anggota, dikonfirmasi oleh asisten pendamping |

# **7\. Presentasi**

## **Pemilihan hari**

* Hari tampil dipilih **per kelompok** melalui spreadsheet slot dengan sistem **siapa cepat dia dapat**. Spreadsheet dibuka **Sabtu, 10 Oktober 2026, pukul 08.00**; tautannya dibagikan di grup WhatsApp.

* Setiap hari dibatasi **maksimal 6 tim**. Bila slot satu hari penuh, tim memilih hari lainnya.

* Spreadsheet dikunci setelah batas waktu. Anggota tidak dapat pindah hari secara perorangan.

## **Alokasi waktu per tim (20 menit)**

| Tahap | Durasi |
| :---- | :---- |
| Persiapan (membuka berkas di laptop panitia) | 5 menit |
| Presentasi | **10 menit** |
| Tanya jawab juri | 5 menit |

* Timekeeper menunjukkan kartu waktu **5 menit, 1 menit, dan selesai**. Presentasi dihentikan saat waktu habis.

* **Seluruh anggota wajib berbicara** saat presentasi.

* Bila ada anggota yang tidak hadir, kelompok tetap presentasi dan tetap berhak menjadi juara.

## **Rundown per hari presentasi**

| Waktu | Kegiatan |
| :---- | :---- |
| 17.00–17.05 | Pembukaan |
| 17.05–17.45 | Tim 1–2 |
| 17.45–18.30 | Istirahat maghrib |
| 18.30–19.50 | Tim 3–6 |
| 19.50–20.00 | Penutup |

# **8\. Penilaian**

Penilaian dilakukan oleh **tiga juri dari tim riset I-Smile** yang tidak mendampingi kelompok mana pun. Komposisi juri sama pada kedua hari. Setiap kriteria dinilai pada **skala 1–5**, nilai akhir adalah **rata-rata tiga juri**, dan skor diisi langsung setiap tim selesai tampil. **Keputusan juri bersifat final.**

| No | Kriteria | Bobot | Skor 1 | Skor 3 | Skor 5 |
| :---- | :---- | :---- | :---- | :---- | :---- |
| 1 | Pemahaman masalah | 15% | Tujuan dan target tidak jelas | Target dan jenis masalah jelas | Pertanyaan spesifik, pengguna hasil jelas, metrik dipilih sesuai konteks |
| 2 | Proses dan metode | 25% | Tahapan tidak lengkap, tanpa alasan | EDA, cleaning, split, dan model standar lengkap | Setiap keputusan disertai alasan dari data; cross-validation dipakai dengan benar |
| 3 | Hasil model dan interpretasi metrik | 20% | Model error atau metrik tidak dilaporkan | Metrik wajib dilaporkan dan dibandingkan dengan model standar | Arti metrik dijelaskan dalam konteks; latih vs uji diperiksa; keterbatasan disampaikan |
| 4 | Penyampaian dan penguasaan materi | 20% | Membaca slide, melebihi waktu | Runtut dan sesuai waktu | Runtut, mudah dipahami orang awam, visual mendukung |
| 5 | Tanya jawab | 10% | Tidak dapat menjawab | Sebagian besar dijawab dengan benar | Jawaban tepat beserta alasan, termasuk pertanyaan tentang kode |
| 6 | Kekompakan dan pembagian tugas | 10% | Hanya sebagian anggota berbicara; pembagian tugas tidak ada | Seluruh anggota berbicara; pembagian tugas tercantum | Seluruh anggota berbicara dan menjawab; pembagian tugas seimbang |

* **Kriteria 3 tidak menilai skor tertinggi.** Yang dinilai adalah model berjalan utuh, metrik dilaporkan, dan tim mampu menjelaskan arti angkanya.

* **Kriteria 6 dinilai dari hal yang terlihat**: seluruh anggota berbicara, dan pembagian tugas tercantum pada slide serta masuk akal.

# **9\. Hadiah dan Pengumuman**

| Peringkat | Hadiah |
| :---- | :---- |
| Juara 1 | Rp250.000 \+ sertifikat juara |
| Juara 2 | Rp200.000 \+ sertifikat juara |
| Juara 3 | Rp150.000 \+ sertifikat juara |
| Juara 4 | Rp100.000 \+ sertifikat juara |

Juara diumumkan secara online di grup WhatsApp Study Group pada **Minggu, 18 Oktober 2026**, agar tim yang tampil Jumat tidak dirugikan.

# **10\. Sertifikat, Kehadiran, dan Deposit**

* **Sertifikat Mini Project** diberikan kepada peserta yang hadir presentasi pada hari kelompoknya, **atau** izin sah dan terbukti berkontribusi pada project.

* Izin sah disampaikan paling lambat **12 jam sebelum** presentasi kepada Abil (0853-5378-5203).

* Kontribusi dibuktikan melalui **slide pembagian tugas** yang dikonfirmasi asisten pendamping.

* Setiap peserta **wajib mengisi form Post-Test dan Evaluasi sebelum kelompoknya tampil**. Pengisian form ini menjadi syarat pengembalian deposit.

* Deposit dikembalikan kepada peserta yang memperoleh **Sertifikat Study Group dan Sertifikat Mini Project** serta telah mengisi form Post-Test dan Evaluasi, sesuai Ketentuan Peserta.

# **11\. Integritas dan Konsultasi**

* Kode boleh merujuk sumber lain (dokumentasi, notebook publik) dengan **mencantumkan sumbernya** di notebook.

* Alat bantu AI boleh dipakai, tetapi **tim wajib memahami seluruh isi notebook**. Juri dapat menanyakan bagian kode mana pun.

* Konsultasi dilakukan melalui **asisten pendamping kelompok**. Asisten membantu memahami konsep dan menelusuri error, tetapi **tidak mengerjakan dan tidak memberikan kode jadi**.

# **12\. Kontak**

| Keperluan | Kontak |
| :---- | :---- |
| Status dataset | Spreadsheet Pengajuan Dataset |
| Konsultasi teknis | Asisten pendamping kelompok |
| Pertanyaan umum dan izin | Abil — 0853-5378-5203 |
| Deposit dan keuangan | Cheyza — 0812-8594-9092 |

