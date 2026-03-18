# 🚀 Tugas Besar: Sistem Manajemen Lead dan Funnel Marketing

> **Dosen Pengampu:** Muhammad Shiddiq Azis, S.T., MBA

---

## 📊 Perancangan Sistem (DFD)

### DFD Level 0
![WhatsApp Image 2026-03-18 at 20 39 34](https://github.com/user-attachments/assets/2ccd32dd-adb8-48b0-8d74-cffcbb6d1462)
Deskripsi DFD Level 0 : 
Data Flow Diagram Level 0  pada sistem manajemen lead & funnel digital marketing ini menggambarkan gambaran besar interaksi antara sistem dengan tiga entitas luar, yaitu Sumber Lead, Marketing, dan Sales.
Sumber Lead merupakan entitas yang menjadi titik awal masuknya data calon pelanggan ke dalam sistem. Data tersebut dapat berasal dari berbagai kanal seperti form online, iklan digital (Ads), maupun integrasi API. Setelah data diterima, sistem akan mengembalikan notifikasi follow-up sebagai tanda bahwa data lead telah berhasil masuk dan siap diproses lebih lanjut.
Entitas Marketing memiliki peran yang paling luas dalam sistem ini. Sebagai pengelola utama, Marketing dapat melakukan registrasi akun, login, membuat kampanye pemasaran, melakukan request generate link, menginput lead secara manual, mengelola data lead, serta mendistribusikan lead kepada tim Sales. Sebagai timbal balik, sistem menyediakan akses kepada Marketing berupa data lead secara lengkap, riwayat aktivitas, dashboard ringkas, serta berbagai laporan yang dapat dijadikan dasar pengambilan keputusan pemasaran.
Entitas Sales berperan sebagai eksekutor di lapangan yang bertanggung jawab menindaklanjuti setiap lead yang telah di-assign oleh Marketing. Sales dapat melakukan login, mencatat aktivitas per lead, memperbarui status lead dalam pipeline funnel, serta melaporkan hasil follow-up ke dalam sistem. Sebagai respons, sistem memberikan Sales akses terhadap data lead yang ditugaskan, notifikasi setiap kali ada lead baru, riwayat aktivitas lead, dan dashboard ringkas untuk memantau progres harian mereka.
*Diagram Konteks yang menunjukkan aliran data global.*

### DFD Level 1
![WhatsApp Image 2026-03-18 at 20 38 18](https://github.com/user-attachments/assets/2e5f40af-35ff-474d-8b31-3bd86d2642ee)

1.0 Registrasi dan Autentikasi
Proses ini mengelola akses pengguna melalui registrasi dan login. Admin melakukan registrasi dan otomatis mendapatkan role sebagai admin, kemudian data divalidasi dan disimpan dalam Database User. Admin juga dapat membuat link registrasi untuk sales yang disimpan dalam Database Link Registrasi.
Sales melakukan registrasi melalui link tersebut, dan datanya akan di validasi terhadap Database Link Registrasi dan Database User sebelum disimpan. Setelah terdaftar, admin dan sales dapat melakukan login, dan setiap aktivitas login akan dicatat dalam Database Log Login untuk keperluan monitoring oleh admin.
2.0 Pengelolaan Distribusi Lead
Proses ini berfungsi untuk menerima input data lead secara manual ataupun otomatis yang kemudian dikelola dan didistribusikan kepada sales. Sistem mengambil data dari Data Lead dan Data User untuk menentukan pembagian lead.
Hasil distribusi akan disimpan dalam Database Assignment, yang dapat diakses dan dikelola oleh admin, termasuk untuk melakukan penyesuaian pembagian lead. Sementara itu, sales hanya dapat melihat data lead yang telah di-assign kepadanya.
3.0 Update Tagging dan Segmentasi Lead
Proses ini bertanggung jawab untuk mengkategorikan dan memperbarui status lead sesuai dengan tahapan pipeline funnel.
Admin memiliki akses penuh untuk mengubah status dan tagging seluruh lead, sedangkan sales hanya dapat memperbarui status dan tagging pada lead yang menjadi tanggung jawabnya. Setiap perubahan yang dilakukan akan disimpan dalam Database Leads.
4.0 Analisis dan Dashboard 
Dalam proses ini, sistem menghasilkan dua jenis dashboard, yaitu dashboard detail lead dan dashboard ringkas.
Dashboard detail lead:  menampilkan informasi lengkap mengenai lead, seperti nama, sales yang bertanggung jawab, tagging, dan status, dengan menggunakan data dari Database Lead dan Database Assignment. Dashboard ini dapat diakses secara penuh oleh admin dan secara terbatas oleh sales.
dashboard ringkas:  menyajikan informasi penting seperti conversion rate dan cost per lead yang dihasilkan dari analisis data pada Database Lead dan Database Campaign. Dashboard ini dapat diakses oleh seluruh pengguna.
---

## 🎨 Mockup Antarmuka
Rancangan UI aplikasi yang berfokus pada pengalaman pengguna.

| Login Page | Dashboard | Core Feature |
| :---: | :---: | :---: |
| <img width="630" height="379" alt="Screenshot 2026-03-18 132933" src="https://github.com/user-attachments/assets/bae66b70-9e92-4d60-8301-c62964399ffc" />  | <img width="667" height="562" alt="Screenshot 2026-03-18 133118" src="https://github.com/user-attachments/assets/9e00967f-a7d8-4eed-b7f7-8ec55ee8c992" />  | <img width="813" height="439" alt="Screenshot 2026-03-18 133314" src="https://github.com/user-attachments/assets/11d3e4a2-d5ae-4322-9d3b-fb5c5853419d" />
 |

---

## 🛠️ Stack Teknologi
- **Frontend:** HTML
- **Backend:** phyton
- **Database:**  MySQL

---

## 📂 Cara Instalasi
1. `git clone [url-repo]`
2. `npm install` (atau sesuaikan dengan environment)
3. `npm run dev`
