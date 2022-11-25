---
author: "Faruq 1935"
draft: false
date: 2022-11-14T10:13:48+07:00
description: ""
title: "langkah-langkah cara install linux mint untuk pemula"
slug: cara-install-linux-mint
featured_image: "herolinuxmint.png"
cascade:
    banner: 


tags:
    - linux
 
categories:
    - linux
bahasa:
    -

topik:
    -

---

Hallo semua kali ini saya akan membagikan cara install linux mint untuk kalian yang ingin pindah atau ingin menggunakan linux dari windows.
Untuk cara installasi tidaklah sulit karena menggunakan GUI, oke langsung saja kita mulai.


#### **1. Pendahuluan**
&nbsp;&nbsp;&nbsp;&nbsp;Pertama kalian perlu membuat Bootable ISO Linux mint 21 ya saya tidak akan jabarkan di sini karena saya sudah membuat tutorialnya: [Cara Membuat Bootable Menggunakan Rufus Di windows](https://sinauriyen.my.id/basic-tutorial/cara-membuat-bootable-menggunakan-rufus/ "tutorial-bootable")

Kalian langsung bisa tancapkan flashidsk bootable linux mint 21 kalian ke PC/laptop,
kemudian kalian bisa masuk ke bios (Boot Menu) dan pilih flashidsk bootable untuk caranya kalian bisa search di google masing-masing merek PC/laptop kalian.

#### **2. Cara install linux mint 21 di komputer**
&nbsp;&nbsp;&nbsp;&nbsp;Di grub linux mint kalian pilih yang paling atas

![b](/assets/img/install-linux-mint/grub-efi.png "linuxmint")
&nbsp;&nbsp;&nbsp;&nbsp;

Setelah kalian masuk ke dekstop live usb linux, langsung doubel-klik saja di icon menu **`Install linux mint`** bergambar kaset.

![b](/assets/img/install-linux-mint/mint-1.png "linuxmint")
&nbsp;&nbsp;&nbsp;&nbsp;

#### A. Kemudian kalian bisa memilih bahasa.
&nbsp;&nbsp;&nbsp;&nbsp;

![b](/assets/img/install-linux-mint/mint-1edit.png "linuxmint")
&nbsp;&nbsp;&nbsp;&nbsp;

#### B. Di pilihan **`Keyboard Layout`**
&nbsp;&nbsp;&nbsp;&nbsp;
"`Chose your keyboard layout`" pilih sesuai keyboard layout kamu, atau kalian bisa otomatis mendeteksi keyboard layout dengan klik **`Detect Keyboard Layout`** kalian bisa test keyboard kalian sudah terdeteksi atau belum dengan mengetikan sesuatu di kolom yang saya tandai dengan kotak merah.

![b](/assets/img/install-linux-mint/mint-2.png "linuxmint")
&nbsp;&nbsp;&nbsp;&nbsp;

#### C. Kalian checklist saja di **`Install multi media codecs`**
&nbsp;&nbsp;&nbsp;&nbsp;

![b](/assets/img/install-linux-mint/mint-3.png "linuxmint")
&nbsp;&nbsp;&nbsp;&nbsp;

`=======================================================================`
`=======================================================================`


#### D. Instalation Type checklist **`Erse disk and install linux mint`**
&nbsp;&nbsp;&nbsp;&nbsp;Ini akan otomatis dibuatkan partisi oleh linux mint tapi ingat satu storage kalian akan di isi dengan OS linux mint ini karena **`semua data dapat hilang pada hard drive`**, harus kosog dari data-data penting.

![b](/assets/img/install-linux-mint/mint-4.png "linuxmint")
&nbsp;&nbsp;&nbsp;&nbsp;

![b](/assets/img/install-linux-mint/mint-5.png "linuxmint")
&nbsp;&nbsp;&nbsp;&nbsp;

#### E. Jika kalian ingin membuat partisi sendiri checklist **`Something Else`**
&nbsp;&nbsp;&nbsp;&nbsp;

![b](/assets/img/install-linux-mint/mint-alternatif1.png "linuxmint")
&nbsp;&nbsp;&nbsp;&nbsp;

* Pilih penyimpanan yang ingin kalian pakai
* Pilih partisi yang kosong 
* Pilih new partition table untuk membuat partisi linux mint yang baru
 
![b](/assets/img/install-linux-mint/mintpartisi.png "linuxmint")
&nbsp;&nbsp;&nbsp;&nbsp;

* Pilih continue

![b](/assets/img/install-linux-mint/mintpartisi1.png "linuxmint")
&nbsp;&nbsp;&nbsp;&nbsp;

* Untuk membuat partisi baru pilih tombol tambah/ples

![b](/assets/img/install-linux-mint/mintpartisi2.png "linuxmint")
&nbsp;&nbsp;&nbsp;&nbsp;

Di sini saya akan membuat partisi
* `swap area` menambah RAM virtual, cukup 2048MB
* `root` kemudian partisi root ini penting karena sistem linux akan di letakan disini untuk ukuran sesuaikan dengan penyimpanan kalian
* `home` sebenarnya ini tidak terlalu di wajibkan karena kalian bisa membuat partisi root saja
* `boot` jika UEFI kalian perlu membuat partisi /boot/efi cukup 250MB, kalu kalian masih BIOS tidak diperlukan


![b](/assets/img/install-linux-mint/mintpartisi3.png "linuxmint")
&nbsp;&nbsp;&nbsp;&nbsp;

> ext4 direkomendasikan. Ini adalah sistem file Linux yang paling populer.

![b](/assets/img/install-linux-mint/root.png "linuxmint")
&nbsp;&nbsp;&nbsp;&nbsp;

![b](/assets/img/install-linux-mint/home.png "linuxmint")
&nbsp;&nbsp;&nbsp;&nbsp;

![b](/assets/img/install-linux-mint/partisiselesai.png "linuxmint")
&nbsp;&nbsp;&nbsp;&nbsp;

`=======================================================================`
`=======================================================================`

#### F. Memilih Zona Waktu
&nbsp;&nbsp;&nbsp;&nbsp; Kalian bisa klik pulau yang ada di peta sesuai tempat kalian tinggal
atau kalian bisa ketikan saja di kolom pencarian

![b](/assets/img/install-linux-mint/zonawaktu.png "linuxmint")
&nbsp;&nbsp;&nbsp;&nbsp;

#### G. Siapa Kamu ?
&nbsp;&nbsp;&nbsp;&nbsp;Isi saja dengan **Nama** kalian, untuk **Password** pastikan mudah diingat

![b](/assets/img/install-linux-mint/form.png "linuxmint")
&nbsp;&nbsp;&nbsp;&nbsp;

#### H. Tunggu sampai selesai proses instalasi Linux Mint
&nbsp;&nbsp;&nbsp;&nbsp;

![b](/assets/img/install-linux-mint/selesailm.png "linuxmint")
&nbsp;&nbsp;&nbsp;&nbsp;

**Proses instalasi linux mint selesai kalian bisa klik restart now, sebelum itu cabut bootable usb**

![b](/assets/img/install-linux-mint/lmfinish.png "linuxmint")
&nbsp;&nbsp;&nbsp;&nbsp;

![b](/assets/img/install-linux-mint/bootloder.png "linuxmint")
&nbsp;&nbsp;&nbsp;&nbsp;

Tampilan linux mint cinnamon 21 menjalankan terminal `neofetch`

![b](/assets/img/install-linux-mint/nef.png "linuxmint")
&nbsp;&nbsp;&nbsp;&nbsp;
