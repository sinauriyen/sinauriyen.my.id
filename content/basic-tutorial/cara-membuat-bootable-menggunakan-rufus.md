---
author: "Faruq 1935"
draft: false
date: 2022-09-25T08:34:15+07:00
description: "Membuat bootable tidak lah sulit cukup menggunakan software rufus di windows cuma membutuhkan waktu beberapa menit, langkah langkah ini ditujukan untuk kalian yang masih
kebingungan membuat bootable, missal untuk keperluan instalasi windows maupun GNU/Linux."
title: "Cara Membuat Bootable Menggunakan Rufus Di windows"
slug: cara-membuat-bootable-menggunakan-rufus
featured_image: "bootable-sy.png"
cascade:
    banner: 

tags:
    - Bootable
    - rufus
    - linux

categories:
    - basic-tutorial

bahasa:
    - Indonesia

topik:


---

### **Pendahuluan**

Membuat bootable tidak lah sulit cukup menggunakan software rufus di windows cuma membutuhkan waktu beberapa menit, langkah langkah ini ditujukan untuk kalian yang masih
kebingungan membuat bootable, missal untuk keperluan instalasi windows maupun GNU/Linux.

> `Pastikan flashdisk kalian kosong atau sudah dibackup sebelum melanjutkan tutorial`

#### **1. Instalasi Rufus**

&nbsp;&nbsp;&nbsp;&nbsp;Langsung saja download rufus di website resmi rufus [link website rufus ](https://rufus.ie/en "link Download")

Secroll ke bawah sampai bagian download, pilih antara rufus biasa dan rufus portable, disini saya pilih yang portable.

&nbsp;&nbsp;&nbsp;&nbsp;
![b](/assets/img/bootable-f/rufus1.png "bootable-rufus")
&nbsp;&nbsp;&nbsp;&nbsp;

#### **2. Membuat Bootable Menggunakan Rufus**

&nbsp;&nbsp;&nbsp;&nbsp;Double klik saja rufus portable yang sudah kalian install tadi, berikut tampilan rufus:

&nbsp;&nbsp;&nbsp;&nbsp;
![b](/assets/img/bootable-f/rufus2.png "bootable-rufus")
&nbsp;&nbsp;&nbsp;&nbsp;

setelah itu kalian tancapkan flashdisk atau bisa mengunakan card reader ke Komputer kalian, bisa dilihat terdeteksi oleh rufus:

&nbsp;&nbsp;&nbsp;&nbsp;
![b](/assets/img/bootable-f/rufus3.png "bootable-rufus")
&nbsp;&nbsp;&nbsp;&nbsp;

Kemudian setelah flashdisk terdeteksi, kalian klik saja di `Boot Selection` **SELECT**, arahkan ke file iso kalian misal disini saya akan membuat bootable linux mint:

&nbsp;&nbsp;&nbsp;&nbsp;
![b](/assets/img/bootable-f/bootable22.png "bootable-rufus")
&nbsp;&nbsp;&nbsp;&nbsp;

Nah dibagian `Partion Scheme` sesuaikan dengan partion scheme storage kalian kebetulan saya menggunakan `MBR` disini, untuk `Target System` pilih `BIOS or UEFI`

&nbsp;&nbsp;&nbsp;&nbsp;
![b](/assets/img/bootable-f/bootable3.png "bootable-rufus")
&nbsp;&nbsp;&nbsp;&nbsp;

**`TIPS:`**

> Cara mengetahui `Partion Scheme` kita mbr atau gpt kalian bisa pergi ke `Disk Management`,
cari saja di setting atau pencarian windows ketikan `disk management`

&nbsp;&nbsp;&nbsp;&nbsp;
![b](/assets/img/bootable-f/mbr.png "bootable-rufus")
&nbsp;&nbsp;&nbsp;&nbsp;

> Setelah di `Disk Management`, klik `Disk 0` kemudian klik kanan pilih `Properties`

&nbsp;&nbsp;&nbsp;&nbsp;
![b](/assets/img/bootable-f/mbr1.png "bootable-rufus")
&nbsp;&nbsp;&nbsp;&nbsp;

> di `Properties` menuju `Volumes`, tertera di `Partition Style`

&nbsp;&nbsp;&nbsp;&nbsp;
![b](/assets/img/bootable-f/mbr4.png "bootable-rufus")
&nbsp;&nbsp;&nbsp;&nbsp;

Lanjut kalian bisa beri nama di `Volume label`,
oke semua sudah selesai tinggal klik **`START`**

&nbsp;&nbsp;&nbsp;&nbsp;
![b](/assets/img/bootable-f/bootable7.png "bootable-rufus")
&nbsp;&nbsp;&nbsp;&nbsp;

> Ingat ya flashdisk kalian akan di format ulang jadi pastikan isi didalam flashdisk sudah dibackup ya

&nbsp;&nbsp;&nbsp;&nbsp;
![b](/assets/img/bootable-f/bootable4.png "bootable-rufus")
&nbsp;&nbsp;&nbsp;&nbsp;

&nbsp;&nbsp;&nbsp;&nbsp;
![b](/assets/img/bootable-f/bootable5.png "bootable-rufus")
&nbsp;&nbsp;&nbsp;&nbsp;

**Tunggu sampai proses selesai:**

&nbsp;&nbsp;&nbsp;&nbsp;
![b](/assets/img/bootable-f/bootable77.png "bootable-rufus")
&nbsp;&nbsp;&nbsp;&nbsp;

**Setelah selesai tinggal klik close**

&nbsp;&nbsp;&nbsp;&nbsp;
![b](/assets/img/bootable-f/bootable8.png "bootable-rufus")
&nbsp;&nbsp;&nbsp;&nbsp;


Sudah deh kalian bisa melakukan installasi Windows maupun GNU/Linux,
untuk cara instalasi sistem operasi akan saya tulis ditutorial selanjutnya.

Jika ada pertanyaan tulis saja dikolom komentar ya.