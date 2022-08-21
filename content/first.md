---
author: "M Faruq Syarifudin"
draft: true
date: 2022-01-25T21:36:21+07:00
description: "Ini adalah deskripsi artikel"
title: "Cara Menggunakan Markdown"
slug: markdown
featured_image: "dhcp.png"
cascade:
    banner: logo.png
tags:
    - front-end

categories:
    - jaringan 

---

# Satu
## Dua
### Tiga
#### Empat
##### Limo
###### Enem

**Kandel**
*mireng*
~~kecoret~~

**Elaina X Debian**

<!-- ini untuk mengatur besar kecilnya gambar dengan memberi width-->
{{< figure class="mb-3 text-center" width="150px" src="/assets/img/smk.png" >}}
<!-- ini untuk mengatur besar kecilnya gambar dengan memberi width-->

![ini gambar debian x elaina](/assets/img/debian.png)

<!-- ![ini gambar elaina]() -->

[link ke sinaundisik](https://sinaudhisik.netlify.app/ "Pergi ke sinaundisik.my.id")

https://sinaudhisik.netlify.app/

* Satu
* Dua
* Tiga
* Empat
* Lima

1. siji
2. Loro
3. Telu
4. Papat
5. Limo

- item 1
- item 2
- item 3

Perintah `apt-get install` adalah perintah untuk menginstall paket di Debian.

```javascript
    console.log("HELLO WORLD !");
```

{{< bootstrap-table "table table table-striped table-hover border-success" >}}
| Animal  | Sounds |
|---------|--------|
| Cat     | Meow   |
| Dog     | Woof   |
| Cricket | Chirp  |
{{< /bootstrap-table >}}

> Barang Kelihatan Pasti Bisa Di Kerjakan

**Tugas hari ini:**

- [x] Install Dan Konfigurasi Web Server Apache Di Debian 11
- [ ] Belajar Menginstall Linux Debian 11
- [ ] Belajar Bahasa Pemrograman PHP
- [x] Membuat Website Portofolio Dengan Framework Bootstrap 5

            <div class="container p-3 mb-3">
                <div class="row">
                    <h3 class="fw-bold"># Rekomendasi Artikel</h3>
                </div>
                <div class="row">
                    <div class="card shadow-sm">
                        <div class="card-body">
                            <div class="overflow-auto">
                                <div class="row">
                                   
                                  <div class="col-4">
                                    <div class="card ml-1">
                                        <a href="">
                                            <img src="" class="card-img-top" alt="sinauriyen">
                                        <a>
                                        <div class="card-body">
                                          <p class="card-text"></p>
                                        </div>
                                      </div>
                                  </div>
                         
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>


<!-- ini untuk mengatur besar kecilnya gambar dengan memberi width-->
{{< figure class="mb-3 text-center" width="150px" src="/assets/img/owner.jpg" >}}
<!-- ini untuk mengatur besar kecilnya gambar dengan memberi width-->
### batas
  <div class="container p-3 mb-3">
                <div class="row">
                    <h3 class="fw-bold"># Rekomendasi Artikel</h3>
                </div>
                <div class="row">
                    <div class="card shadow-sm" style="border-radius: 8px;">
                        <div class="card-body">
                            <div class="overflow-auto">
                                <div class="row">
                                    <div class="col-4">
                                        <div class="card">
                                            <div class="card-body">
                                                
                                            </div>
                                        </div>
                                    </div>
                                    {{ range first 3 ( where ( where .Site.Pages.ByDate.Reverse ".Params.tags" "intersect" .Params.tags ) "Permalink" "!=" .Permalink ) }}
                                  <div class="col-4">
                                    <div class="card">
                                        <div class="card-body">
                                            {{/*  <ul>
                                             
                                                  <li class="relatedPost">
                                                    <a href="{{ .RelPermalink }}">{{ .Title | markdownify }}</a><br />
                                                    {{ .Description | markdownify }}
                                                  </li>
                                                
                                              </ul>  */}}
                                              <a href=" {{ .Permalink }} ">
                                                <img src="/img/{{ .Params.featured_image }}" alt="sinauriyen" class="card-img-top img-index">
                                            </a>
                                            <div class="card-body">
                                                    <h6 class="card-title h6 font-weight-bold mb-1">
                                                      <a href=" {{ .Permalink }} " style="text-decoration: none; color: black;">
                                                        {{ .Title }}
                                                      </a>
                                                    </h6>
                                                    <div class="text-secondary small">
                                                      {{ or .Params.description .Summary }}
                                                    </div>         
                                            </div>
                                        </div>
                                    </div>
                                </div>
                                {{ end }}
                            </div>
                        </div>
                    </div>
                </div>