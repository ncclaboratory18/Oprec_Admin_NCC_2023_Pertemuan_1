# Materi 1 - Cloud Computing
## Pengenalan Cloud Computing
Cloud computing merupakan penggunaan sumber daya dan layanan sistem yang dapat diakses melalui internet. Secara sederhana, cloud computing memungkinkan kita menggunakan berbagai fasilitas yang disediakan oleh cloud provider (AWS, Azure, GCP, dst) tanpa perlu memiliki peralatan tersebut secara fisik. Hal ini dikarenakan ketika kita menggunakan layanan cloud, kita menyewa service maupun hardware yang berada pada data center cloud provider lalu mengaksesnya secara remote melalui perangkat yang kita gunakan.
![image](https://user-images.githubusercontent.com/79139753/225175607-a46ae06a-626b-4eeb-ae64-81a482d71fc9.png)

## Model Cloud Computing
Terdapat berbagai jenis model layanan cloud computing yang tersedia secara umum yaitu IaaS, PaaS, dan SaaS:<br>
![image](https://user-images.githubusercontent.com/79139753/225178867-212daad0-de4d-46fc-bc47-210b4d1157f9.png)

### On-premise
Pada on-premise, user bertanggung jawab untuk memanajemen seluruh resource yang ada. Sebagai contohnya adalah ketika membeli PC atau laptop baru yang hanya terdiri dari hardware saja. Maka kita lah yang bertanggung jawab untuk memilih storage yang akan digunakan (SSD, Harddisk), menginstall OS, sampai menginstall aplikasi didalamnya. 
### IaaS (Infrastructure as a Service)
Pada IaaS, user tidak perlu memanajemen infrastruktur (termasuk hardware), karena telah disediakan cloud provider. Contohnya adalah ketika menyewa virtual machine pada cloud provider. Kita tidak perlu membeli hardware sendiri secara fisik, tetapi kita dapat memilih OS yang ingin digunakan maupun aplikasi yang ingin diinstall pada VM tersebut.
### PaaS (Platform as a Service)
Pada PaaS, platform dan infrastruktur telah disediakan oleh cloud provider, sehingga user hanya perlu memanajemen aplikasi/software saja. Contohnya adalah ketika menggunakan layanan web hosting seperti Heroku, kita hanya perlu menspesifikasikan aplikasi apa yang ingin kita gunakan (aplikasi berbasis web) tanpa perlu memikirkan bagaimana aplikasi tersebut dapat dijalankan pada platform milik cloud provider.
### SaaS (Software as a Service)
Pada SaaS, seluruh resource termasuk software telah disediakan oleh cloud provider. Contohnya adalah ketika menggunakan Google Drive, kita dapat menggunakan berbagai aplikasi seperti Google Docs dan Google Form dengan kapasitas storage yang telah disediakan oleh cloud provider.

#### Berikut salah satu contoh analogi model-model tersebut:
![1_JacqOl2kjyTYzv31v0xITw](https://user-images.githubusercontent.com/79139753/225283319-e6ec6eb8-af42-4270-bc76-4f80f999d757.png)

## Cloud computing menggunakan Microsoft Azure
Microsoft Azure merupakan salah satu cloud provider yang dikembangkan oleh Microsoft. Salah satu alasan penggunaan Microsoft Azure adalah dikarenakan Microsoft Azure menyediakan layanan `Azure for Students`, yang memungkinkan pelajar maupun mahasiswa menggunakan resource cloud didalamnya tanpa perlu melakukan registrasi kartu kredit. Untuk melakukan claim `Azure for Students` terdapat beberapa hal yang perlu dipersiapkan:
- Nomor HP (hanya untuk verifikasi)
- Email akademik (bisa menggunakan email ITS)

Berikut adalah langkah claimnya secara lengkap:
1. Akses https://azure.microsoft.com/en-us/free/students/
![Screenshot 2023-03-14 091825](https://user-images.githubusercontent.com/79139753/225182579-2a2bc316-3f91-4c8a-bd51-36f7f6cd94a5.png)
2. Pilih `Start free` lalu sign up menggunakan account bebas (bisa email ITS/email pribadi)
3. Lakukan verifikasi nomor HP, lalu isi data diri sesuai ketentuan termasuk email akademik (tidak perlu sama dengan email account pada poin 2). Kemudian lakukan verifikasi yang akan dikirimkan ke email akademik
![Screenshot 2023-03-14 122025](https://user-images.githubusercontent.com/79139753/225182930-86afc333-fbe4-4ed8-bad6-7cf4c8c443e6.png)
4. Jika sudah selesai, akses https://portal.azure.com/signin/index/ lalu cek pada bagian subscription. Maka subscription `Azure for Students` akan terlihat sudah aktif dan mendapat kredit 100$

### Menyewa Virtual Machine
Salah satu yang dapat dilakukan pada Microsoft Azure adalah melakukan penyewaan Virtual Machine dengan spesifikasi yang diinginkan. Berikut adalah langkah-langkahnya:
1. Klik `Virtual Machines`, lalu pilih `Create` -> `Azure virtual machine` pada bagian kiri atas
![Screenshot 2023-03-14 091939](https://user-images.githubusercontent.com/79139753/225183536-ff0f8874-5af1-4283-9693-79616a0262fd.png)
2. Isi nama VM, region (posisi data center VM), image (OS maupun image lain) yang ingin digunakan pada VM, dan size (CPU, cores)
![Screenshot 2023-03-14 092036](https://user-images.githubusercontent.com/79139753/225183573-0431c21f-f175-453d-91d7-599a55fc98d3.png)
3. Selanjutnya untuk autentikasi dapat menggunakan SSH public key (memerlukan file key ketika ingin mengakses secara remote menggunakan `ssh`) maupun password (lebih mudah karena dapat diakses dari mana saja tetapi lebih rentan), dalam contoh ini akan menggunakan password
![Screenshot 2023-03-14 092252](https://user-images.githubusercontent.com/79139753/225183831-d0222f67-6651-4d4d-abb3-927576febe22.png)
4. Lanjutkan proses review dan create
5. Ketika VM berhasil diinisialisasi, maka VM tersebut akan ditampilkan pada halaman `Virtual Machines`
![Screenshot 2023-03-14 094731](https://user-images.githubusercontent.com/79139753/225184137-8e7567f6-bea1-41a3-914c-fd806bd8961c.png)
![Screenshot 2023-03-14 094743](https://user-images.githubusercontent.com/79139753/225184169-e70acbd6-dc49-4ebd-9ed1-89729e58317b.png)
6. Ketika ingin mengakses VM tersebut, kita dapat menggunakan terminal/command line pada perangkat yang kita miliki lalu gunakan ssh ([secure shell](https://www.biznetgio.com/en/news/apa-itu-ssh-pengertian-fungsi-dan-cara-kerjanya)) dengan command `ssh <username>@<public IP address>` sesuai dengan parameter username dan IP pada VM yang kita miliki
![Screenshot 2023-03-14 121244](https://user-images.githubusercontent.com/79139753/225184391-53b238bc-8542-4f29-8678-bc1beaf5612a.png)
7. VM sudah dapat diakses dan digunakan melalui terminal seperti penggunaan terminal pada umumnya
![Screenshot 2023-03-14 121257](https://user-images.githubusercontent.com/79139753/225184439-cc9ca4bc-61be-4b65-bb9d-29ebe2df8890.png)
