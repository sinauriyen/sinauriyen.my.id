---
author: "Faruq 1935"
draft: false
date: 2022-07-25T10:21:06+07:00
description: "Hallo, kali ini saya ingin membagikan bagaimana cara menginstall debian 11 bullseye cli di virtualbox, tutorial ini akan manejelaskan langkah-langkah mulai dari nol"
title: "Cara Install Debian 11 CLI Bullseye Di Virtualbox"
slug: cara-install-debian-11-bullseye
featured_image: "thumbnail-debian11.svg"
cascade:
    banner: 
tags:

    - server
    - linux
    - virtualbox
    - administrasi-sistem-jaringan

categories:
    - administrasi-sistem-jaringan

bahasa:
    - Indonesia

topik:
    -

---

#### **1. Menginstall  iso Debian 11 Bullseye** 

&nbsp;&nbsp;&nbsp;&nbsp;Hallo, kali ini saya ingin membagikan bagaimana cara menginstall debian 11 bullseye cli di virtualbox, tutorial ini akan manejelaskan langkah-langkah mulai dari nol.

Pertama kalian bisa download fiel iso debian 11 bulseye [di website debian ](https://www.debian.org/CD/http-ftp/ "link Download")

&nbsp;&nbsp;&nbsp;&nbsp;
![b](/assets/img/cara-install-debian11/idebian.png "debianinstall")
&nbsp;&nbsp;&nbsp;&nbsp;

kalian bisa pilih amd64 yang artinya arsitektur set instruksi prosesor kalian x64/64bit jika arsitektur set intruksi processor kalian x86/32bit bisa pilih i386 disini saya pilih yang 64bit.

#### **2. Konfigurasi di mesin virtual**

&nbsp;&nbsp;&nbsp;&nbsp;Saya anggap kalian sudah menginstall virtualbox jika belom bisa install [di website virtualbox ](https://www.virtualbox.org/wiki/Downloads "link Download")

Buka virtualbox, kemudian pilih tools **New** untuk membuat mesin virtual baru.

&nbsp;&nbsp;&nbsp;&nbsp;
![b](/assets/img/cara-install-debian11/v1.png "debianinstall")
&nbsp;&nbsp;&nbsp;&nbsp;

* Kalian bisa isi kolom **Name** dengan nama yang kalian sukai
* kemudian kolom **Machine Folder** letak si mesin virtual tersebut biarkan saja.
* kolom **Type** pilih linux 
* yang terakhir pilih Debian (64bit).

&nbsp;&nbsp;&nbsp;&nbsp;
![b](/assets/img/cara-install-debian11/v2.png "debianinstall")
&nbsp;&nbsp;&nbsp;&nbsp;

* Set RAM sesuai kebutuhan dan spek komputer kalian

&nbsp;&nbsp;&nbsp;&nbsp;
![b](/assets/img/cara-install-debian11/v3.png "debianinstall")
&nbsp;&nbsp;&nbsp;&nbsp;

* Ikuti saja langkah langkah ini

&nbsp;&nbsp;&nbsp;&nbsp;
![b](/assets/img/cara-install-debian11/v4.png "debianinstall")
&nbsp;&nbsp;&nbsp;&nbsp;

&nbsp;&nbsp;&nbsp;&nbsp;
![b](/assets/img/cara-install-debian11/v5.png "debianinstall")
&nbsp;&nbsp;&nbsp;&nbsp;

&nbsp;&nbsp;&nbsp;&nbsp;
![b](/assets/img/cara-install-debian11/v6.png "debianinstall")
&nbsp;&nbsp;&nbsp;&nbsp;

* Sesuaikan ukuran penyimpanan sesuai kebutuhan kalian 

&nbsp;&nbsp;&nbsp;&nbsp;
![b](/assets/img/cara-install-debian11/v7.png "debianinstall")
&nbsp;&nbsp;&nbsp;&nbsp;

#### **3. Proses instalasi Debian 11 Bullseye**

&nbsp;&nbsp;&nbsp;&nbsp;
* Pilih tools **Settings berlogo gerigi** ![b](/assets/img/cara-install-debian11/setting.png "debianinstall")
* pilih menu **Storage** >> pilih logo kaset **Empty** >> pilih logo kaset yang bertuliskan `empty` >> pilih **Choose a disk file...** arahkan ke file iso Debian 11 Bullseye yang sudah kalian install tadi

&nbsp;&nbsp;&nbsp;&nbsp;
![b](/assets/img/cara-install-debian11/disk.png "debianinstall")
&nbsp;&nbsp;&nbsp;&nbsp;

* kemudian kita ke menu **Network** set adapter network menjadi **Bridged Adapter**.

&nbsp;&nbsp;&nbsp;&nbsp;
![b](/assets/img/cara-install-debian11/network-adapter.png "debianinstall")
&nbsp;&nbsp;&nbsp;&nbsp;

* Setelah selesai pilih Ok, **Start** ![b](/assets/img/cara-install-debian11/start.png "debianinstall")
  
##### **Disini kita pilih menu install karena kita akan menginstall mode CLI**

&nbsp;&nbsp;&nbsp;&nbsp;
![b](/assets/img/cara-install-debian11/install-debian1.png "debianinstall")
&nbsp;&nbsp;&nbsp;&nbsp;

Di pilihan  **[! !] Select a language**
* pilih bahasa English, untuk bahasa sistem

Di pilihan **[! !] Select your location**
* pilih **other >> Asia >> Indonesia**

Di pilihan **[!] Configure locales**
* pilih **United States**

Di pilihan **[! !] Configure the keyboard**
* pilih **American English**

Di **[!] Configure the network**
* isikan **Hostname** dengan Nama kalian

&nbsp;&nbsp;&nbsp;&nbsp;
![b](/assets/img/cara-install-debian11/install-debian3.png "debianinstall")
&nbsp;&nbsp;&nbsp;&nbsp;

Di pilihan **[!] Configure the network**
* kosongi saja di **Domain name** tekan enter

Nah di **[! !] Set up users and passwords** 
* bagian **Root pasword** kalian bisa isi dengan password yang kalian inginkan
semisal **123** 

&nbsp;&nbsp;&nbsp;&nbsp;
![b](/assets/img/cara-install-debian11/pw-install.png "debianinstall")
&nbsp;&nbsp;&nbsp;&nbsp;

* kemudian isikan kembali root pasword tadi

Untuk **Full name for new user** / nama user biasa kalian bisa isikan dengan nama kalian atau sesuka hati.

&nbsp;&nbsp;&nbsp;&nbsp;
![b](/assets/img/cara-install-debian11/install-debian4.png "debianinstall")
&nbsp;&nbsp;&nbsp;&nbsp;

* Isikan kembali untuk **Username for your account** dengan nama sesuka kalian

**Isikan password untuk user baru pastikan password mudah diingat ya**

&nbsp;&nbsp;&nbsp;&nbsp;
![b](/assets/img/cara-install-debian11/install-debian5.png "debianinstall")
&nbsp;&nbsp;&nbsp;&nbsp;

* Isikan kembali password

**Pilih zona waktu ditempat kalian**

&nbsp;&nbsp;&nbsp;&nbsp;
![b](/assets/img/cara-install-debian11/install-debian6.png "debianinstall")
&nbsp;&nbsp;&nbsp;&nbsp;

#### **Untuk partisi disk pilih Guided - use entire disk**

&nbsp;&nbsp;&nbsp;&nbsp;
![b](/assets/img/cara-install-debian11/install-debian-guided.png "debianinstall")
&nbsp;&nbsp;&nbsp;&nbsp;

* karena disini kita pakai virtualbox kita tinggal enter saja
* pilih **All files in one operration** maka akan dibuatkan secara otomatis oleh debian 

&nbsp;&nbsp;&nbsp;&nbsp;
![b](/assets/img/cara-install-debian11/install-debian7.png "debianinstall")
&nbsp;&nbsp;&nbsp;&nbsp;

* tinggal pilih **Finish partitioning and write chages to disk**
* **write change to disk pilih** `Yes` 

&nbsp;&nbsp;&nbsp;&nbsp;
![b](/assets/img/cara-install-debian11/install-debian8.png "debianinstall")
&nbsp;&nbsp;&nbsp;&nbsp;

* pada pilihan **Scan extra installation media?** pilih  `No`

&nbsp;&nbsp;&nbsp;&nbsp;
![b](/assets/img/cara-install-debian11/install-debian9.png "debianinstall")
&nbsp;&nbsp;&nbsp;&nbsp;

* pada pilihan **Continue without a network miror** pilih `No`

* di pilihan **Participate in the pacakge user survey?** pilih `No`

&nbsp;&nbsp;&nbsp;&nbsp;
![b](/assets/img/cara-install-debian11/install-debian11.png "debianinstall")
&nbsp;&nbsp;&nbsp;&nbsp;

* pilih **Choose software to install** checklist hanya di bagian `standard system utilities`

&nbsp;&nbsp;&nbsp;&nbsp;
![b](/assets/img/cara-install-debian11/install-debian12.png "debianinstall")
&nbsp;&nbsp;&nbsp;&nbsp;

> cara menghapus tanda pagar (unchecklist) dengan `spasi`

##### Untuk penginstallan **GRUB boot loader to your primaty drive?** pilih `Yes`

&nbsp;&nbsp;&nbsp;&nbsp;
![b](/assets/img/cara-install-debian11/install-debian13.png "debianinstall")
&nbsp;&nbsp;&nbsp;&nbsp;

* kemudian taruh GRUB boot loader di `/dev/sda/partisi-kalian` karena kita pakai virtualbox pilih seperti di gambar

&nbsp;&nbsp;&nbsp;&nbsp;
![b](/assets/img/cara-install-debian11/install-debian14.png "debianinstall")
&nbsp;&nbsp;&nbsp;&nbsp;

##### Stelah itu tunggu penginstallan GRUB boot loader

* setelah selesai penginstallan pilih **Continue**

&nbsp;&nbsp;&nbsp;&nbsp;
![b](/assets/img/cara-install-debian11/install-debian15.png "debianinstall")
&nbsp;&nbsp;&nbsp;&nbsp;

> Kemudian otomatis mesin virtual akan restart, terus dibagian GRUB boot loader nanti tingal enter

##### Kalian bisa login dengan user root langsung
* `Username:root` 
* `Password: 123` password sesuai yang kalian masukan tadi untuk user root

&nbsp;&nbsp;&nbsp;&nbsp;
![b](/assets/img/cara-install-debian11/login-debian.png "debianinstall")
&nbsp;&nbsp;&nbsp;&nbsp;

##### Tampilan Debian 11 Bullseye CLI 

&nbsp;&nbsp;&nbsp;&nbsp;
![b](/assets/img/cara-install-debian11/hasil-ids.png "debianinstall")
&nbsp;&nbsp;&nbsp;&nbsp;

Ya begitu cata install Debian 11 di virtualbox cara ini sama dengan versi Debian sebelumya Debian 8, Debian 9, dan Debian 10.

Jika ada yang ingin ditanyakan bisa tulis dikolom komentar.