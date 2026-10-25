# CloudAI

CloudAI adalah asisten AI lintas platform.

> **Status versi 1.0.1:** Mode Agent mendukung tugas bertahap dan paket aplikasi menggunakan ZIP sebagai format bawaan. Paket 1.0.0 sebelumnya disimpan dalam [arsip versi lama](../Releases/Legacy/v1.0.0/). Lihat [mode Agent](../docs/AGENT_MODE.md) dan [batasan HarmonyOS](../docs/HARMONYOS.md).

> **macOS:** Versi 1.0.1 menggunakan build Universal untuk Intel dan Apple Silicon, sedangkan paket 1.0.0 yang diarsipkan hanya mendukung Apple Silicon (`arm64`).

## Fitur

-   Percakapan AI
-   Mode Agent untuk tugas bertahap
-   Integrasi API Cloud AI
-   Aplikasi desktop lintas platform
-   Build multi-arsitektur
-   Antarmuka grafis
-   Dukungan banyak bahasa

## Mode Agent

Mode Agent dapat membagi tujuan menjadi beberapa langkah, menggunakan alat yang diaktifkan pengguna, membuat perubahan yang telah diizinkan, dan memverifikasi hasil jika memungkinkan. Mode ini tidak memberikan izin tambahan dan harus meminta konfirmasi sebelum melakukan tindakan sensitif atau destruktif. Lihat [panduan mode Agent](../docs/AGENT_MODE.md).

## Platform yang Didukung

### Desktop

-   Windows x64
-   Windows ARM64
-   macOS Universal (Intel + Apple Silicon) — v1.0.1
-   macOS Apple Silicon — legacy v1.0.0
-   Linux x86_64
-   Linux ARM64

### Platform Lain

-   HarmonyOS
-   OpenHarmony

## Detail Platform

| Platform | Arsitektur dan status paket | Instalasi dan batasan |
| --- | --- | --- |
| Windows | Versi 1.0.1 menargetkan x64 dan ARM64 serta menggunakan ZIP secara bawaan. Arsip menyimpan ZIP x64 lama versi 1.0.0. | Ekstrak ZIP sepenuhnya sebelum menjalankan aplikasi. |
| Linux | Versi 1.0.1 menargetkan x86_64 dan ARM64 serta menggunakan ZIP secara bawaan. Paket 1.0.0 untuk kedua arsitektur telah diarsipkan. | ZIP dapat berisi AppImage, DEB, RPM, atau TAR.GZ. AppImage memerlukan izin eksekusi; DEB dan RPM dipasang melalui pengelola paket. |
| macOS | Versi 1.0.1 menggunakan build Universal untuk Intel dan Apple Silicon serta didistribusikan sebagai ZIP secara bawaan; 1.0.0 hanya mendukung Apple Silicon (`arm64`). | Ekstrak ZIP untuk memperoleh aplikasi. Aplikasi belum ditandatangani dan mungkin perlu diizinkan secara manual di macOS. |
| HarmonyOS | Distribusi 1.0.1 menggunakan ZIP secara bawaan; instalasi memakai HAP kompatibel dan bertanda tangan di dalamnya. HAP 1.0.0 yang diarsipkan adalah build debug khusus `2in1`. | HAP lama menargetkan API `60101024`. Diperlukan sistem kompatibel dan tanda tangan valid. Lihat [catatan HarmonyOS](../docs/HARMONYOS.md). |
| OpenHarmony | Distribusi 1.0.1 menggunakan ZIP secara bawaan; instalasi memerlukan HAP yang kompatibel dengan OpenHarmony di dalamnya. | Diperlukan tanda tangan kompatibel dan pengujian perangkat. Jangan gunakan HAP HarmonyOS 1.0.0 yang diarsipkan sebagai paket OpenHarmony. |

## Instalasi

### Linux

AppImage:

1.  Unduh dan ekstrak paket ZIP Linux bawaan, lalu pilih AppImage yang sesuai dengan arsitektur Anda.
2.  Tambahkan izin eksekusi:

``` bash
chmod +x CloudAI.AppImage
```

3.  Jalankan aplikasi:

``` bash
./CloudAI.AppImage
```

Paket .deb dapat diinstal dengan:

``` bash
sudo apt install ./CloudAI.deb
```

### macOS

Versi macOS saat ini tidak ditandatangani dengan sertifikat Apple Developer.

Saat pertama kali dibuka, pengguna mungkin perlu mengizinkan aplikasi secara manual di pengaturan Keamanan macOS.

### HarmonyOS

Versi HarmonyOS dibuat dengan toolchain pengembangan resmi HarmonyOS.

Pengembangan dan pengemasan menggunakan DevEco Studio. Aplikasi HarmonyOS dibuat sebagai paket HAP/App dan memerlukan konfigurasi penandatanganan yang tepat sebelum didistribusikan.

## Lisensi

[Lisensi MIT](../LICENSE).

## Berkas proyek sumber terbuka

Lihat [informasi proyek sumber terbuka](../docs/OPEN_SOURCE.md) untuk lisensi, status ketersediaan kode sumber, panduan kontribusi, dan kebijakan proyek.

Salinan pohon sumber CloudAI 1.0.1 kini tersedia di [`Source/CloudAI`](../Source/CloudAI/) dan mencakup aplikasi desktop, dukungan Agent dan plugin, sumber daya pemaketan, serta proyek HarmonyOS. Proyek HAP OpenHarmony yang terpisah, pemetaan rilis ke sumber, versi dependensi yang dikunci, dan pemaketan yang dapat direproduksi serta telah diverifikasi masih belum tersedia; lihat [tinjauan status sumber terbuka](../docs/OPEN_SOURCE_STATUS.md).

## Pengembang

Liao Boxuan

## Tanggal

2026-09-13
