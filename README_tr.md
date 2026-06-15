<div align="center">
  <p>
    <a href="README.md">🇬🇧 English</a> | <a href="README_tr.md">🇹🇷 Türkçe</a>
  </p>
  <h1>KristalBASIC</h1>
  <p><strong>C dilinin performansını, BASIC sözdiziminin kolaylığıyla birleştiren modern programlama dili.</strong></p>

  [![License: Freeware](https://img.shields.io/badge/License-Freeware-blue.svg)](#license)
  [![Platform: Windows](https://img.shields.io/badge/Platform-Windows%20x64-lightgrey.svg)](#)
  [![VS Code Extension](https://img.shields.io/badge/VS%20Code-Extension%20Available-blue)](#)
</div>

---

## 🌟 Nedir?

**KristalBASIC**, arka planda güçlü **GCC (MinGW-w64)** motorunu kullanarak yazdığınız kodları doğrudan yerel Windows uygulamalarına (`.exe`) derleyen bağımsız bir programlama dilidir. 

Öğrenmesi zor olan C/C++ dilleriyle uğraşmadan, okuması ve yazması son derece kolay olan BASIC sözdizimini (syntax) kullanarak yüksek performanslı masaüstü yazılımları ve 3D oyunlar geliştirebilirsiniz.

## ✨ Öne Çıkan Özellikler

*   🚀 **C Seviyesinde Performans:** Kodlarınız yorumlanmaz (interpreted), doğrudan makine koduna (native) derlenir.
*   🎮 **Dahili 3D Oyun Motoru Altyapısı:** Dünyaca ünlü [Raylib](https://www.raylib.com/) kütüphanesi derleyiciye gömülüdür. Ekstra kurulum yapmadan anında 2D/3D grafik, fizik, ses ve girdi (input) işlemlerini yönetebilirsiniz.
*   📦 **Bağımlılık Yok:** Oluşturduğunuz `.exe` dosyaları başka hiçbir DLL veya çalışma zamanı (runtime) kütüphanesine ihtiyaç duymadan her Windows bilgisayarda çalışır.
*   🛠️ **VS Code Entegrasyonu:** Resmi VSIX eklentisi sayesinde Visual Studio Code üzerinde otomatik tamamlama (IntelliSense) ve sözdizimi renklendirmesi (syntax highlighting) desteği sunar.

## 📥 Kurulum

1.  **[Releases](../../releases)** sekmesine gidin ve en güncel `KristalBASIC_Setup.exe` dosyasını indirin.
2.  Setup dosyasını çalıştırarak derleyiciyi bilgisayarınıza kurun.
3.  Yine Releases bölümünde bulunan `kristalbasic-vscode.vsix` dosyasını indirin.
4.  VS Code'u açın, **Extensions** sekmesine gidin, sağ üstteki `...` menüsünden **"Install from VSIX..."** seçeneğine tıklayın ve eklentiyi kurun.

## 💻 Sözdizimi (Syntax) ve Örnek Kod

KristalBASIC Nesne Yönelimli Programlamayı (OOP) ve statik tiplemeyi destekler. İşte repository'deki **Kristal Vadisi 3D** oyunundan bir kesit:

```basic
# --- Toplanabilir Kristal Sınıfı ---
CLASS Kristal {
    DECIMAL x
    DECIMAL y
    DECIMAL z
    DECIMAL yaricap
    INT deger
    STRING tur
    BOOL toplandi

    # Hafif bir "yüzme" animasyonu için yükseklik salınımı
    FUNC VOID Guncelle(DECIMAL zaman) {
        THIS.y = THIS.y + SIN(zaman * 2.0 + THIS.x) * 0.01
    }
}

# --- Düşman Yapay Zeka (AI) Durum Makinesi ---
CLASS Dusman {
    DECIMAL x
    DECIMAL y
    DECIMAL z
    INT durum

    FUNC VOID Guncelle(DECIMAL oyuncuX, DECIMAL oyuncuZ) {
        DECIMAL dx = oyuncuX - THIS.x
        DECIMAL dz = oyuncuZ - THIS.z
        DECIMAL mesafe = SQRT(dx * dx + dz * dz)

        IF (mesafe < 18.0) {
            THIS.durum = DusmanDurumu.TAKIP
        } ELSE {
            THIS.durum = DusmanDurumu.DEVRIYE
        }
    }
}
```

## 🎮 Örnek 3D Oyun

KristalBASIC'in yeteneklerini göstermek amacıyla hazırlanan **Örnek 3D Oyunu** incelemek için, yayınlanan dosyalar arasındaki oyun klasörüne veya kılavuzlara göz atabilirsiniz. Bu sayede 3D modellerin nasıl yüklendiğini, kamera kontrollerini ve çarpışma (collision) testlerini uygulamalı olarak görebilirsiniz.

## 📄 Lisans (Freeware)

*   **Derleyici ve Araçlar:** KristalBASIC derleyicisi kapalı kaynaklı ve tamamen **Ücretsiz Yazılımdır (Freeware)**. 
*   **Sizin Uygulamalarınız:** KristalBASIC kullanarak geliştirdiğiniz tüm uygulamalar, oyunlar ve programlar **%100 SİZE AİTTİR**. Yazdığınız uygulamaları açık kaynaklı dağıtabilir veya ticari bir ürün olarak satabilirsiniz. Projeleriniz GCC veya Raylib lisanslarından (GPL kısıtlamalarından) etkilenmez.
*   **Örnek Kodlar:** Sunulan tüm örnek kaynak kodlar **MIT Lisansı** altındadır, dilediğiniz gibi kendi projelerinizde kullanabilirsiniz.

Daha fazla detay için deponun ana dizinindeki lisans metnine göz atabilirsiniz.

---
<div align="center">
  <b>Kristalsoft</b> tarafından Türkiye'de sevgiyle geliştirildi. 🇹🇷
</div>
