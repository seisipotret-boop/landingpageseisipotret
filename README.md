# Panduan Pemeliharaan & Pengelolaan Website Seisi Potret

Dokumen panduan ini disusun khusus untuk membantu pengelola website **Seisi Potret** dalam melakukan pemeliharaan dan pembaruan konten secara mandiri, mulai dari mengganti teks, media (foto/video), harga, hingga menambah item galeri di berbagai komponen dan halaman.

---

## Structure Main Directory

Berikut adalah lokasi folder utama dalam proyek website ini:

```text
├── public/                 <-- Tempat menyimpan aset media publik (Video MP4 & Foto)
│   ├── media/              <-- Tempat menyimpan aset media publik / page tidak rinci (Video MP4 & Foto)
│        ├── galeri/             <-- Tempat menyimpan aset media untuk komponen galeri/portofolio pada beranda
│        ├── layanan/             <-- Tempat menyimpan aset media untuk komponen galeri/portofolio pada semua page layanan
├── src/
│   ├── components/         <-- Seluruh Komponen Website
│   │   ├── BookingProcess.astro      <-- komponen alur kerja jasa dari awal sampai selesai
│   │   ├── CTASection.astro  <-- komponen call to action pada setiap page sebelum footer
│   │   ├── FeaturedPackage.astro   <-- komponen paket hook di beranda 
│   │   ├── FloatingWA.astro   <-- komponen icon wa pada sisi kanan untuk setiap page
│   │   ├── Footer.astro   <-- komponen footer
│   │   ├── Gallery.astro     <-- komponen portofolio pada page beranda
│   │   ├── Hero.astro     <-- komponen hero atau pada awal page paling atas dibawah navbar
│   │   ├── Navbar.astro      <-- komponen navbar atau list menu 
│   │   └── Services.astro    <-- komponen lokasi untuk dipilih
│   │   └── Stats.astro      <-- komponen data statistik seisipotret
│   │   └── Testimonials.astro    <-- komponen testimonial client
│   │   └── Values.astro    <-- komponen values atau visi misi seisi potret
│   └── pages/              <-- Seluruh Halaman Website
│       └── layanan/
│           └── alula.astro  
│           └── jabal-kudai-khandamah.astro
│           └── jabal-uhud.astro
│           └── pelataran-madinah.astro
│           └── pelataran-makkah.astro
│       └── faq.astro
│       └── index.astro     <-- page utama #warning# jangan disentuh!
│       └── kebijakan-privasi.astro
│       └── kontak.astro
│       └── syarat-ketentuan.astro
│       └── tentang.astro
└── README.md
```

## Running System
```
git clone https://github.com/username/nama-repository.git
```
```
npm install
```
```
npm run dev
```

## Clean Step for Editing 
```
1.   cek lokasi komponen yang ingin diubah, berada di file mana pada source code
2.   buka readme.md pada struktur file, cek file mana yang terdapat komponen tersebut
3.   buka source code melalui vscode / code edtitor lain
4.   jika komponen yang ingin di edit berupa teks langsung edit saja
4.1    jika komponen yang ingin diedit berupa gambar/video perhatikan link gambar jika gambar yang ingin dimasukan bersifat online, perhatikan path penyimpanan gambar serta penamaan file gambar
4.2    baru silakan eksekusi code dengan memperhtaikan path dan code agar tetap berjalan dengan baik
5.   Jika komponen bersifat tag seperti lokasi atau yang lain silakan perhatikan point 1 kembali
6.   setelah selesai dan sudah sesuai output nya, lakukan hal dibawah ini
6.1    git add.
6.2    git commit -m "isi message menyesaikan apa yang diedit"
6.3    git push origin main
7.   tunggu hingga automated deployment succees dan silakan cek web terbaru
```

## Notes For Managing System
```
photo format .webp 
photo size 1-2500kb
video format .mp4
video size 1-25000kb
video duration max 2 menit
penamaan file media seperti foto dan video disesuaikan
penggantian isi konten wajib di push ke github dengan commit message yang jelas
```

## Example Name of File for Photo or Video
```
makkah1.wep diletakan di /public/media/layanan/ <-- untuk contoh gambar pada layanan pelataran-makkah pada bagian PREVIEW DESTINASI PELATARAN MEKKAH
herovideo.mp4 diletakan di /public <-- untuk contoh video yang tertera pada hero di page beranda
```
