# Yohanes Anjar Dewantara - Back End
# writing-week-4


## Git dan GitHub


### Git dan Github
    > Git dan GitHub adalah salah satu tool yang wajib digunakan dalam proyek pengembangan software. Git dan juga GitHub adalah Pengontrol versi bertugas mencatat setiap perubahan pada file proyek yang dikerjakan oleh banyak orang maupun sendiri. Git dan GitHub juga git digunakan untuk kolaborasi. Oleh karena itu Git dan Github sangat penting untuk Programmer.
    
### Perbedaan antara Git dan Github
- Git
  > Git merupakan software berbasis Version Control System (VCS) yang bertugas untuk mencatat perubahan seluruh file atau repository suatu project.
- GitHub
  > GitHub merupakan layanan cloud yang berguna untuk menyimpan dan mengelola sebuah project yang dinamakan repository (repo git). Cara kerja pada GitHub harus terkoneksi pada internet sehingga tidak perlu meng-install sebuah software ke dalam perangkat keras.
<br>Berikut Perbedaan Git dan GitHub
- Git :
<br>1. Meng-install software di penyimpanan lokal
<br>2. Dikelola oleh The Linux Foundation
<br>3. Berfokus pada version control dan code sharing
<br>4. Akses secara offline
<br>5. Tidak menggunakan fitur user management
<br>6. Menyediakan desktop interface bernama “Git GUI”
<br>7. Open sourced licensed
- GitHub :
<br>1. Host melalui layanan cloud
<br>2. Diakuisisi oleh Microsoft pada 2018
<br>3. Berfokus pada source code hosting terpusat
<br>4. Akses secara online
<br>5. Menggunakan user management
<br>6. Menggunakan nama desktop interface “GitHub Desktop”
<br>7. Pilihan bagi pengguna gratis dan pengguna berbayar

### Membuat Repository Git
1. Buat folder di laptop/komputer
<br>![buat folder](https://user-images.githubusercontent.com/100120189/192084875-5267d4a7-fc2b-4b17-92e0-54d5e06489c4.png)
2. masuk ke folder tersebut, kemudian klik kanan pilih "Git Bash Here"
<br>![membuka git bash](https://user-images.githubusercontent.com/100120189/192084918-d1540374-b086-4236-8467-d248cc6a0ee2.png)
3. ketikan git init. Sekarang folder yang dibuat tadi sudahh menjadi repository
<br>![git init](https://user-images.githubusercontent.com/100120189/192085032-3023b79a-d206-4800-9695-90c4c8a66f6d.png)

### Melakukan commit pada Git
1. Buat satu atau dua file
<br>![membuat file](https://user-images.githubusercontent.com/100120189/192085394-c691958c-aa18-4b08-9861-712cc4082247.png)
2. Ketikkan "git add ." untuk melacak perubahan
<br>![git add .](https://user-images.githubusercontent.com/100120189/192085341-a09f7304-74bc-4a38-bc2f-77f46191ea5f.png)
3. Kemudian baru ketikkan "git commit -m "(pesan perubahan)" untuk melakukan commit
<br>![melakukan commit](https://user-images.githubusercontent.com/100120189/192085457-0023f22a-85f2-4f71-93b5-2163fb484d81.png)

### Merge pada Git


### Mempublish aplikasi ke Github
1. Membuat repository di github
<br>![membuat repository](https://user-images.githubusercontent.com/100120189/192085907-f5c21a69-fdc9-4a51-a6ef-721a59416370.png)
2. Ketikkan "git remote add origin https://github.com/(username)/(repository yang dibuat).git" Untuk me-remote ke github
<br>![git remote add command](https://user-images.githubusercontent.com/100120189/192086110-fbcea64f-b151-49ca-b35f-3231485e802b.png)
3. Ketikkan "git push -u origin (branch yang dipakai)"
<br>![git push command](https://user-images.githubusercontent.com/100120189/192086193-9d2c28d5-c54c-4866-af6b-e48d3876e2e6.png)
4. Seleseai. File sudah ada di Github
<br>![mengecek file](https://user-images.githubusercontent.com/100120189/192086262-f192b2f9-b6bc-4159-a3be-e9e97108b79d.png)

### Melakukan cloning Github ke local
1. buka repository yang ikin di cloning, kemudian klik code dan salin kode tersebut
<br>![image](https://user-images.githubusercontent.com/100120189/192086298-04dfd51e-67d1-443f-b773-1b381f00a095.png)
2. Tentukan penyimpanan lokal, kemudian klik kanan dan pilih "Git Bash Here"
<br>![menentukan penyimpanan lokal](https://user-images.githubusercontent.com/100120189/192086520-89471820-f852-4a42-a5e2-1a019a4b807c.png)
3. Ketikkan "git clone (link yang tadi dicopy)"
<br>![git clone command](https://user-images.githubusercontent.com/100120189/192086665-a0e07fd9-9101-4a13-9f2c-f9d6322fa504.png)
4. File yang ada di GitHub sudah selasai di cloning ke local
<br>![cek file](https://user-images.githubusercontent.com/100120189/192086750-587dcadb-f217-44c6-8e50-3d69a939c724.png)

### Github Kolaborasi
