# Bank Marketing Champaign
## Bussiness Understanding
### Context 
Bank bukanlah satu-satunya bisnis yang menggunakan kampanye pemasaran. Kampanye pemasaran adalah proses di mana sebuah bisnis atau organisasi mengiklankan produknya kepada klien saat ini dan di masa depan. Dalam dataset ini, sebuah bank mempromosikan agar kliennya menyetor dana ke dalam akun mereka, baik mereka merupakan pelanggan saat ini atau calon pelanggan yang telah memiliki akun dengan bank tersebut.

Pendapatan yang dihasilkan selama kampanye, baik jangka pendek maupun jangka panjang, serta seberapa banyak biaya akuisisi klien yang berhasil dikurangi oleh kampanye itu sendiri digunakan untuk menentukan seberapa efektif kampanye pemasaran tersebut.

Untuk melakukan upaya pemasaran ini, bank akan menelepon pelanggannya melalui telepon rumah dan telepon seluler mereka.

Berikut adalah data dari hasil kampanye pemasaran bank yang dilakukan melalui panggilan telepon langsung untuk menaruh deposit berjangka. Untuk klien yang setuju untuk menaruh deposit, variabel target akan diisi dengan 'yes', jika tidak 'no'

Target: 
* 0 : Tidak menaruh deposit 
* 1 : Menaruh deposit
* ### Problem Statement 
Isu utama dari dataset ini adalah menentukan bagaimana meningkatkan efektivitas kampanye pemasaran, target market, dan dengan demikian, meningkatkan pendapatan yang dihasilkan dari produk, dalam contoh ini, setoran.

Karena kesuksesan kampanye pemasaran ini tergantung pada keputusan klien untuk melakukan setoran di bank, sangat penting untuk terlebih dahulu memahami faktor-faktor kunci yang mempengaruhi keputusan ini, serta memprediksi konsumen mana yang akan melakukan setoran sehingga kita dapat fokus pada kampanye pemasaran untuk pelanggan tersebut.
### Goals 
Oleh karena itu, untuk menentukan apakah seorang calon pelanggan akan melakukan setoran selama kampanye pemasaran atau tidak, bank memerlukan sebuah alat. Sifat dataset, seperti informasi pelanggan dan dampak kampanye pemasaran pada setoran klien, sangat penting dalam hal ini.

Sebagai hasilnya, dengan menggunakan model machine learning, kita dapat memprediksi kecenderungan seorang calon pelanggan untuk melakukan setoran berdasarkan kampanye pemasaran dan juga mengevaluasi efek fitur pada keputusan konsumen. Setiap faktor ini berpotensi untuk meningkatkan pendapatan bank melalui peningkatan setoran, dan prediksi setoran pelanggan dapat membantu bank menentukan pelanggan mana yang harus diprioritaskan.
## Analytic Approach

Tugas yang akan dilakukan adalah melakukan analisis data untuk mengidentifikasi pola yang membedakan kandidat nasabah yang akan menempatkan deposit dan yang tidak. Selanjutnya, langkah berikutnya adalah membangun sebuah model klasifikasi untuk membantu bank dalam memprediksi probabilitas bahwa seorang calon nasabah akan atau tidak akan menempatkan deposit.
## Metric Evaluation 
Type 1 error : False Positive  
Konsekuensi: membuang waktu dan biaya kampanye untuk nasabah yang tidak berpotensial menaruh deposit

Type 2 error : False Negative  
Konsekuensi: kehilangan kandidat nasabah potensial

Dalam rangka untuk mengurangi biaya kampanye bank tanpa mengurangi jumlah nasabah potensial yang diinginkan oleh bank, model akan dibuat seoptimal mungkin. Tujuannya adalah untuk memprediksi kelas positif sebanyak mungkin dengan meminimalkan jumlah prediksi false positive. Oleh karena itu, F1 Score akan digunakan sebagai metrik utama.

## Data Understanding 
* Terdapat ketidakseimbangan pada dataset.
* Sebagian besar fitur pada dataset bersifat kategorikal, baik nominal maupun ordinal, dengan beberapa fitur memiliki kardinalitas yang tinggi.
* Setiap baris pada dataset merepresentasikan informasi kandidat nasabah yang pernah melakukan deposit di masa lalu.
* **Conclusion:**

Berdasarkan hasil classification report model, dapat disimpulkan bahwa bila seandainya menggunakan model ini untuk memfilter/menyaring list kandidat nasabah, maka model ini dapat mengurangi 69% kandidat nasabah tidak potensial untuk tidak di approach melalui kampanye, dan model dapat memprediksi dengan benar 74% kandidat nasabah yang tertarik, dengan skor False Positive mencapai 25%. 
Tanpa model, perusahaan akan melakukan kampanye terhadap 1563 kandidat nasabah yang mana tidak semuanya adalah kandidat nasabah potensial untuk menaruh deposit. Sedangkan dengan model, perusahaan dapat mengerucutkan target kampanye menjadi hanya 652 kandidat nasabah potensial saja, yang mana ini akan meningkatkan efisiensi bagi bank baik dari segi finansial maupun waktu.

maka dari itu, kesimpulannya adalah penggunaan model dapat menjawab bussiness problem bank.

**Recommendation:**

Beberapa poin yang bisa dilakukan untuk membuat model menjadi lebih baik adalah:
* menambah fitur yang memiliki pengaruh kuat terhadap target, misal: status perkawinan, pendapatan, dll
* melakukan improvisasi pada model seperti melakukan hyperparameter tuning kembali, atau membuat model dengan algoritma yang lain
