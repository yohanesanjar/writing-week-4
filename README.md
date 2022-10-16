# Yohanes Anjar Dewantara - Back End
# writing-week-4

## Asynchronus Javascript 
### Async await
- Apa itu?
  - Merupakan cara lain untuk menangkap objek promise. Fitur ini mempermudah kita dalam menangani proses asynchronous.Async/Await merupakan sebuah syntax khusus yang digunakan untuk menangani Promise agar penulisan code lebih efisien dan rapih.
  - Contoh 
     ```JavaScript 
     const getAllUser = async ()=> {
	 const data = await getUser()
	 console.log(data)
     }
     ```
  - Contoh menjalankan code promise dengan menggunakan async Await 
    ```JavaScript 
    Let nonton = (kondisi) => {
        Return new Promise((resolve, reject) => {
            If (kondisi == “jalan”) {
                Resolve(“nonton terpenuhi”)
            } reject(“batal nonton”)
        })
    }

    Async function asyncNonton() {
        Try {
            Let result = await nonton()
            Console.log(result);
        } catch (error) {
            Console.log(“error”)
        }
    } 
    asyncNonton ()
    ```
- Error Handling 
  - Untuk menghandle error  Async/Await kita dapat menggunakan try catch di dalam function yang kita buat, sehingga jika terjadi error kita dapat menangkap errornya dalam block catch.
  - Contoh
    ```JavaScript 
    const getAllUser = async ()=> {
	    try {
		    const result = await getUser()
		    console.log(result)
	    } catch (error) {
		    console.log(error)
	    }
    }
    ```
- Fetch
  - Apa itu fetch?
    > Fetch gunakan untuk mengambil data dan menampilkan data ke browser. Berfungsi untuk web dinamis yang datanya selalu berubah. Berikut merupakan ilustrasi mengenai fetch data api.  
  - Mengambil data API menggunakan fetch
    ```JavaScript
    fetch("https://digimon-api.vercel.app/api/digimon")
    .then(result => result.json())
    .then(result => {
        console.log(result)
    })
    ```
  - Menampilkan data API dalam web 
    ```JavaScript 
    listDigimon = document.getElementById("list-digimon")

    let getDataDigimon = async () => {
        let URL = "https://digimon-api.vercel.app/api/digimon"
        let response = await fetch(URL)
        let digimons = await response.json()

        // menampilkan 10 data digimon
        digimons.slice(0, 10).forEach((item, index) => {
            listDigimon.innerHTML += 
            `<div>
                <img src="${item.img}" alt="" width="200">
                <h3>${item.name}</h3>
             </div>`
        })
    }

    getDataDigimon()
    ```
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
1. User membuat repository baru.
   <br>![buat repository](https://user-images.githubusercontent.com/100120189/195994981-cce86eee-6dc2-4273-bea9-125103f189e7.png)
2. melakukan cloning ke local computer/laptop
   <br>![melakukan cloning](https://user-images.githubusercontent.com/100120189/195995098-b9ef2941-a761-4a4e-90a4-f77909e0c3eb.png)
3. User membuat branch baru kemudian masuk ke branch tersebut dengan command `git branch nama_branch` kemudian `git checkout nama_branch`
   <br>![buat branch](https://user-images.githubusercontent.com/100120189/195995682-86a89ed9-661b-4e9b-9644-d9c411836721.png)
4. User melakukan pull branch main ke branch user, dengan command `git pull origin nama_branch_user`
   <br>![melakukan pull ke branch user](https://user-images.githubusercontent.com/100120189/195996160-9a80d42a-af18-4ddf-9e45-9d1eac0488ea.png)
5. User membuat file baru
   <br>![membuat file baru](https://user-images.githubusercontent.com/100120189/195995240-bc5c1f16-e998-4dc6-b823-b924d7b906d5.png)
6. User melakukan push ke branch user, dengan command `git push origin nama_branch_user`. Sebelum melakukan push pastikan sudah melakukan add dan juga commit.
   <br>![Melakukan Push](https://user-images.githubusercontent.com/100120189/195996362-92ed9037-d442-4e37-9307-d0b311f7e470.png)
7. Buka Github, kemudian user melakukan pull request ke branch main.
   <br>![melakukan pull request](https://user-images.githubusercontent.com/100120189/195996473-87c43e32-e047-4c13-859f-196ac8d4bf73.png)
8. Kemudian lakukan merge pull request agar file dari branch user bisa berada di branch main.
   <br>![melakukan merge](https://user-images.githubusercontent.com/100120189/195996559-85075d8c-df9c-4320-b141-0e1479ed9fd0.png)
   <br>![file berhasil ditambahkan ke branch main](https://user-images.githubusercontent.com/100120189/195996593-18c90437-dc12-4ad0-919f-df24b1e75370.png)

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
Kita meisalkan ada user A dan user B, dan user A sebagai ketuanya.
1. User A membuat repository baru, kemudian menambahkan user B untuk collaborator dengan cara pergi ke settings > collaborators > tambahkan teman 
   <br>![Menambahkan teman](https://user-images.githubusercontent.com/100120189/195998279-c3b9044c-f28b-44ed-8cc2-6d0211bff46f.png)
2. User A dan user B membuat branch masing-masing, dengan command `git branch nama_branch`, kemudian masing-masing user pindah ke branch baru yang dibikin dengan command `git checkout nama_branch`
3. User A dan user B melakukan pull masing ke dalam branch masing-masing di local computer/laptop, dengan command `git pull origin main`
4. Misalkan user A ingin menambahkan file, maka user A membuat file terlebih dahulu, kemudian di push di branch user A, dengan command `git push origin nama_branch`
5. User kemudian user A melakukan pull request dan merge ke branch main, dengan cara yang sudah dijelaskan di materi sebelumnya.
6. Jika user B igin menambahkan file, maka user harus melakukan pull request kembali, agar nanti tidak ada error atau kesalahan.
7. Kemudian user B bisa melakukan push ke dalam branch nya.
8. User B kemudian melakukan pull request.
9. User B tidak perlu melakukan merge, dan yang melakukan merge adalah user A karena dia adalah pemimpinnya.
10. Ulangi dari langkah ke-4.

## Responsive Web Design
### Responsive Web Design
    > Memungkinkan website dapat diakses dimanapun (device apapun), tampilannya tetap bagus dan enak dilihat
### Tools untuk membuat website yang responsif
1. Menggunakan viewport
2. Viewport : area website yang dapat diakses oleh user
- Setting viewport : Otomatis keluar saat menggunakan html dengan cara ketikan ! kemudian enter. Atau 
```javascript
<meta name="viewport">
```
2. Menggunakan Max-Width element
- misalnya menjadikan gambar lebih responsif
```javascript
<img scr=" " alt style="max-width:100%" />
```
3. Menggunakan CSS relative unit
-  relative length : em, rem, vw, vh, % (yg sering dipakai)
   - em : mengikuti ukuran huruf dari element dia berada. Nyari font size dengan parent element terdekat. Contoh : container dengan em nya
   - rem : mengikuti ukuran huruf dari root element (ukuran huruf html). Biasanya ukuran default html adalah 16px. Jadi 2rem = 2 x 16px = 32px
   - % : bergantung pada parent element 
   - Vw : relatife 1% dengan lebar viewport.. 50vw = 50% dari lebar viewport
   - Vh : relatife 1% dengan tinggi viewport. 50vh = 50% dari tinggi viewport
4. Menggunakan media query
<br> Membuat beberapa style bergantung pada jenis device
<br> Kata kunci : @media. Contoh :
```javascript
@media (max-width: 500px) {
}
```
<br> Keterangan : Jika ukuran layar dibawah 500px maka style settingan didalam @media yang berlaku

5. Menggunakan Flexbox dan Grid
- Flexbox
<br> Satu arah entah samping(kanan-kiri) atau atas bawah
- Grid
<br> Bisa kearah samping dan atas bawah

## **Bootstrap 5**
- Kapan menggunakan bootstrap?
<br> ketika kita ingin membuat website kita menjadi responsif dengan cara yang simple karena sudah ada templatenya dan tinggal dicopy paste untuk digunakan
- Layout pada bootstrap
1. Breakpoint : sebagai acuan untuk menyesuaikan tampilan dalam berbagai ukuran viewport. Beberapa breakpoint pada bootstrap 5 sm, md, lg, xl, xxl
2. Containers : layout basicnya bootstarp
   - Default Container
     <br> Class container memiliki sifat yang responsive dan fixed-width, yang berarti lebarnya akan berubah pada setiap breakpoint
     ```javascript
     <div class="container">
     <!-- Content here -->
     </div>
     ```
   - Fluid Container
     <br> Class container-fluid memiliki lebar yang sama dengan viewport
     ```javascript
     <div class="container-fluid">
     <!-- Content here -->
     </div>
     ``` 
   - Responsive Container
     ```
     <div class="container-sm">100% wide until small breakpoint</div>
     <div class="container-md">100% wide until medium breakpoint</div>
     <div class="container-lg">100% wide until large breakpoint</div>
     <div class="container-xl">100% wide until extra large breakpoint</div>
     <div class="container-xxl">100% wide until extra extra large breakpoint</div>
     ```
3. Grid : menyediakan 12 kolom system
<br> Grid system membagi lebar halaman menjadi 12 bagian. Sehingga apabila menggunakan class col-8, maka lebarnya akan menjadi 8/12 atau 2/3 dari lebar halaman.
5. Columns
<br> mengatur urutan posisi dan align
- Component pada bootstrap
<br> beberapa component pada bootstrap 5
   - Alerts
   - Breadcrumb
   - Buttons
   - Card
   - Modal
   - Navbar
   - Navs & tabs
   - Pagination
- Content pada bootstrap
   - Reboot
   - Typography
   - Images
   - Tables
   - Figures

##### Info : link bootstrap https://getbootstrap.com/
