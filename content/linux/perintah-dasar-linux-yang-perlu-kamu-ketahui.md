---
author: "Faruq 1935"
draft: false
date: 2022-10-05T07:29:23Z
description: ""
title: "Perintah Dasar Linux Yang Perlu Di Ketahui Pemula"
slug: perintah-dasar-linux-yang-perlu-kamu-ketahui
featured_image: "Linux-sinauriyen.png"
cascade:
    banner: 
tags:
    - cli
    - linux

categories:
    - linux

bahasa:
    - Indonesia 

topik:


---
### **Pendahuluan**

Oke kali ini saya akan membagikan perintah-perintah dasar linux beserta fungsinya, oke langsung saja di simak.

&nbsp;&nbsp;&nbsp;&nbsp;
#### **A. Navigasi**
&nbsp;&nbsp;&nbsp;&nbsp;

##### 1. **pwd**

* Berfungsi untuk memberitahu letak direktori kita saat ini.

##### 2. **ls dan ls -la**

* `ls` (list directory content)Melihat isi direktori, misal `$ ls /home` | digunakan untuk melihat isi dari direktori **home**, `ls -la` untuk melihat isi dari direktori secara menditail mulai dari hak akses , pemilik file dan ukuran.

##### 3. **cd**

* `cd` (cange direktori) untuk pindah direktori, misal `$ cd /bin` untuk masuk ke direktori **bin**, `cd ..` untuk naik ke folder diatasnya.

##### 4. **cp**

* Untuk menyalin suatu file, misal `cp Downloads/sinauriyen.docx Documents/` brarti dokumen sinauriyen.docx yang ada di folder Downloads akan di salin ke folder Music.

##### 5. **mv**

* Untuk memindahkan suatu file, misal `mv Downloads/sinauriyen.txt Documents/` dokumen sinauriyen.txt dari folder Download akan di pindahkan ke folder `Documents`.

##### 6. **mkdir**

* `mkdir` (make direktori) membuat folder baru, misal `mkdir Documents/belajar-linux` maka folder belajar-linux akan dibuatkan di folder `Dokuments`.

##### 7. **rm**

* `rm` (remove) ya sesuai namanya berfungsi unutk menghapus folder, misal `rm -r Documents/belajar-linux` maka folder `belajar-linux` akan dihapus.

##### 8. **shortcut Ctrl+C**

* Mempunyai fungsi untuk membatalkan perintah/aksi.

##### 9. **shortcut Ctrl+l**

* Mempunyai fungsi untuk mengkosongkan layar sama dengan perintah `clear`.

##### 10. **shortcut Ctrl+W**

* Mempunyai fungsi untuk menghapus satu kata belakang ketika mengetikan perintah 

##### 11. **tombol panah atas dan bawah**

* tombol atas memiliki fungsi untuk menampilkan history perintah yang sudah kamu ketikan sebelumnya, begitu juga dengan tombol bawah 

&nbsp;&nbsp;&nbsp;&nbsp;
#### **B. Redirection**
&nbsp;&nbsp;&nbsp;&nbsp;

##### 1. **cat**

* `cat` (concatenate) untuk menggabungkan file. Perintah tersebut dapat membaca dan menyatukan file, menulis. konten ke output standar.

##### 2. **cat > sinauriyen.txt**

* untuk menciptakan dokument misal `cat > sinauriyen.txt` maka akan terbuatkan dokumen sinauriyen.txt

##### 3. **echo**

* untuk mencetak string yang akan ditampilkan sebagai output standar, misal `echo "hallo pembaca"` maka akan tampil diterminal tulisan **hallo pembaca**

&nbsp;&nbsp;&nbsp;&nbsp;
#### **C. Editing**
&nbsp;&nbsp;&nbsp;&nbsp;

##### 1. **nano**

* `nano` adalah text editor default terminal linux, misal `nano test.txt` kalian bisa memgisi apa saja seperti halnya notepad di windows, nah unutk keluarnya sekaligus save, ketik shortcut `ctrl+o` kemudian tekan enter dan `ctrl+x` untuk keluar

##### 2. **echo “belajar” > test.txt**

* ini untuk replace isi file dengan tulisan belajar.

##### 3. **echo “baris baru” >> test.txt**
* ini append(menambah) isi dari test.txt
