Komponen Arsitektur, terdapat tingkatan dari yang paling terlihat sampai proses yang berada dibelakang layar, dimulai dari UI Controller (activity/fragment), kemudian dibawahnya ada livedata, yaitu class penyimpan data yang yang dapat diamati. Selalu menaham/menyimpan cache versi terbaru data, dan ada view model yang merupakan penghubung antara repositori dan UI, dibawah mereka terdapat Repositori yang dimana class uang digunakan untuk mengelola beberapa sumber data, dibawah repositori terdapat room database dimana segala yang berhubungan dengan database berada disini

DAO = Dao harus berupa antarmuka atau class abstrak, Anotasi @Dao mengidentifikasikannya sebagai class DAO untuk Room, fun getAlphabetizedWords(): List<Word>: Metode untuk mendapatkan semua kata dan menghasilkan List Words.
  
Perubahan Database = Untuk mengamati perubahan data, Anda akan menggunakan Flow dari kotlinx-coroutines. Gunakan nilai hasil dari jenis Flow dalam deskripsi metode, dan Room akan menghasilkan semua kode yang diperlukan untuk memperbarui Flow saat database diupdate., Di WordDao, ubah tanda tangan metode getAlphabetizedWords() sehingga List<Word> yang ditampilkan digabungkan dengan Flow.
  
Repositori = Class repositori memisahkan akses ke beberapa sumber data. Repositori bukan bagian dari library. Repositori mengelola kueri dan memungkinkan Anda menggunakan beberapa backend. 
  
Flow = Flow menghasilkan nilai satu per satu (bukan sekaligus) yang dapat menghasilkan nilai dari operasi asinkron seperti permintaan jaringan, panggilan database, atau kode asinkron lainnya.
lazy = penggunakan delegasi properti Kotlin: by lazy.
