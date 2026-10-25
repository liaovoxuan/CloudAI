# CloudAI

CloudAI, platformlar arası bir AI asistanıdır.

> **1.0.1 sürümünün durumu:** Agent modu çok adımlı görevleri destekler ve uygulama paketleri varsayılan olarak ZIP biçimini kullanır. Önceki 1.0.0 paketleri [eski sürümler arşivinde](../Releases/Legacy/v1.0.0/) saklanır. [Agent modu](../docs/AGENT_MODE.md) ve [HarmonyOS sınırlamaları](../docs/HARMONYOS.md) hakkındaki açıklamalara bakın.

> **macOS:** 1.0.1 sürümü Intel ve Apple Silicon için Universal derleme kullanırken arşivlenen 1.0.0 paketi yalnızca Apple Silicon (`arm64`) desteği sunar.

## Özellikler

-   AI sohbeti
-   Çok adımlı görevler için Agent modu
-   Cloud AI API entegrasyonu
-   Çok platformlu masaüstü uygulaması
-   Çok mimarili derlemeler
-   Grafik arayüz
-   Çok dilli destek

## Agent modu

Agent modu bir hedefi adımlara ayırabilir, kullanıcının etkinleştirdiği araçları kullanabilir, izin verilen değişiklikleri yapabilir ve mümkün olduğunda sonucu doğrulayabilir. Kendi başına ek izin sağlamaz ve hassas ya da yıkıcı işlemlerden önce onay istemelidir. [Agent modu kılavuzuna](../docs/AGENT_MODE.md) bakın.

## Desteklenen Platformlar

### Masaüstü

-   Windows x64
-   Windows ARM64
-   macOS Universal (Intel + Apple Silicon) — v1.0.1
-   macOS Apple Silicon — legacy v1.0.0
-   Linux x86_64
-   Linux ARM64

### Diğer Platformlar

-   HarmonyOS
-   OpenHarmony

## Platform ayrıntıları

| Platform | Mimari ve paket durumu | Kurulum ve sınırlamalar |
| --- | --- | --- |
| Windows | 1.0.1 sürümü x64 ve ARM64'ü hedefler ve varsayılan olarak ZIP kullanır. Arşivde eski x64 1.0.0 ZIP bulunur. | Çalıştırmadan önce ZIP'i tamamen çıkarın. |
| Linux | 1.0.1 sürümü x86_64 ve ARM64'ü hedefler ve varsayılan olarak ZIP kullanır. Her iki mimarinin 1.0.0 paketleri arşivlenmiştir. | ZIP; AppImage, DEB, RPM veya TAR.GZ içerebilir. AppImage çalıştırma izni gerektirir; DEB ve RPM paket yöneticisiyle kurulur. |
| macOS | 1.0.1 sürümü Intel ve Apple Silicon için Universal derlemedir ve varsayılan olarak ZIP ile dağıtılır; 1.0.0 yalnızca Apple Silicon (`arm64`) desteği sunar. | Uygulamayı almak için ZIP'i çıkarın. Uygulama imzasızdır ve macOS'te elle izin verilmesi gerekebilir. |
| HarmonyOS | 1.0.1 dağıtımı varsayılan olarak ZIP kullanır; içindeki uyumlu ve imzalı HAP yüklenir. Arşivlenen 1.0.0 HAP dosyaları yalnızca `2in1` için debug derlemeleridir. | Eski HAP dosyaları API `60101024` sürümünü hedefler. Uyumlu sistem ve geçerli imza gerekir. [HarmonyOS notlarına](../docs/HARMONYOS.md) bakın. |
| OpenHarmony | 1.0.1 dağıtımı varsayılan olarak ZIP kullanır; yükleme için içindeki OpenHarmony uyumlu HAP gerekir. | Uyumlu imza ve cihaz testi gerekir. Arşivlenen HarmonyOS 1.0.0 HAP dosyasını OpenHarmony paketi olarak kullanmayın. |

## Kurulum

### Linux

AppImage:

1.  Varsayılan Linux ZIP paketini indirip çıkarın, ardından mimarinize uygun AppImage dosyasını seçin.
2.  Çalıştırma iznini ekleyin:

``` bash
chmod +x CloudAI.AppImage
```

3.  Uygulamayı çalıştırın:

``` bash
./CloudAI.AppImage
```

Deb paketleri şu komutla kurulabilir:

``` bash
sudo apt install ./CloudAI.deb
```

### macOS

macOS sürümü şu anda bir Apple Developer sertifikasıyla imzalanmamıştır.

İlk açılışta kullanıcıların uygulamaya macOS güvenlik ayarlarından elle izin vermesi gerekebilir.

### HarmonyOS

HarmonyOS sürümü resmi HarmonyOS geliştirme araç zinciriyle derlenmiştir.

Geliştirme ve paketleme için DevEco Studio kullanılır. HarmonyOS uygulamaları HAP/App paketleri olarak derlenir ve dağıtımdan önce doğru imzalama yapılandırması gerektirir.

## Lisans

[MIT Lisansı](../LICENSE).

## Açık kaynak proje dosyaları

Lisans, kaynak kodunun kullanılabilirlik durumu, katkı kılavuzu ve proje politikaları için [açık kaynak proje bilgilerine](../docs/OPEN_SOURCE.md) bakın.

CloudAI 1.0.1 kaynak ağacının bir kopyası artık [`Source/CloudAI`](../Source/CloudAI/) altında bulunmaktadır ve masaüstü uygulamasını, Agent ve eklenti desteğini, paketleme kaynaklarını ve HarmonyOS projesini içerir. Ayrı bir OpenHarmony HAP projesi, sürümlerle kaynak arasındaki eşleme, kilitlenmiş bağımlılık sürümleri ve doğrulanmış yeniden üretilebilir paketleme hâlâ mevcut değildir; [açık kaynak durumu incelemesine](../docs/OPEN_SOURCE_STATUS.md) bakın.

## Geliştirici

Liao Boxuan

## Tarih

2026-09-13
