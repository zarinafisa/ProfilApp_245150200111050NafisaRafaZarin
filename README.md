Nama  Nafisa Rafa Zarin
NIM   245150200111050
Kelas TIF - D

Penjelasan Singkat Kode

Seluruh tampilan aplikasi ada di file MainActivity.kt.

1. MainActivity memanggil fungsi ProfileScreen() di dalam setContent agar tampilan profil muncul saat aplikasi dibuka.
2. ProfileScreen() adalah fungsi Composable utama. Di dalamnya ada Column luar yang membuat semua komponen rata tengah secara horizontal dan vertikal, diberi padding, dan bisa digulir dengan verticalScroll agar tidak terpotong saat landscape.
3. Column dalam membentuk bagian profil dengan warna latar biru muda dan padding.
4. Image menampilkan foto profil dari res/drawable dengan ukuran 120 dp, dibentuk lingkaran dengan clip(CircleShape) dan ContentScale.Crop.
5. Text menampilkan nama lengkap, NIM, dan deskripsi singkat, sedangkan Spacer memberi jarak antar komponen.
6. FollowButton() adalah tombol interaktif yang menyimpan state isFollowed dengan remember { mutableStateOf(false) }. Saat ditekan, nilainya dibalik sehingga teks tombol berganti antara Follow dan Unfollow.

Analisis Keuntungan Compose Dibandingkan XML Layout

1. Kode lebih ringkas. UI ditulis langsung dalam Kotlin tanpa file XML terpisah, findViewById, atau ViewBinding, sehingga boilerplate berkurang.
2. UI deklaratif. Programmer cukup menyatakan tampilan yang diinginkan, dan tampilan otomatis berubah mengikuti state (recomposition), tidak perlu mengubah properti view secara manual.
3. Mudah dipelihara dan dipakai ulang. Komponen berupa fungsi Composable yang modular, dan logika serta tampilan berada di satu tempat sehingga risiko ketidaksinkronan UI dan data lebih kecil.
4. Produktivitas lebih tinggi. Fitur Preview dan Modifier yang bisa dirangkai mempercepat pembuatan dan penyesuaian tampilan.
