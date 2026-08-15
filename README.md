# Afet Durumlarında UDP Tabanlı Yerel Haberleşme Prototipi

[![TÜBİTAK](https://img.shields.io/badge/TÜBİTAK-2209--A%20Destekli-blue.svg)](https://tubitak.gov.tr/)
[![Platform](https://img.shields.io/badge/Platform-Android%20(Wi--Fi%20Direct%20%2F%20Aware)-brightgreen.svg)]()
[![Protocol](https://img.shields.io/badge/Protocol-UDP%20%2F%20Mesh-orange.svg)]()
[![Status](https://img.shields.io/badge/Status-Ar--Ge%20%2F%20Prototip-yellow.svg)]()

> **TÜBİTAK 2209-A Üniversite Öğrencileri Araştırma Projeleri Destekleme Programı** kapsamında desteklenen Ar-Ge projesidir.

---

## 📌 İçindekiler
- [Proje Özeti](#-proje-özeti)
- [Giriş ve Motivasyon](#-giriş-ve-motivasyon)
- [Temel Özellikler ve Kapsam](#-temel-özellikler-ve-kapsam)
- [Yöntem ve Çalışma Aşamaları](#-yöntem-ve-çalışma-aşamaları)
- [Teknoloji Yığını](#-teknoloji-yığını)
- [Proje Ekibi ve Danışman](#-proje-ekibi-ve-danışman)
- [Destekleyen Kurumlar & Teşekkür](#-destekleyen-kurumlar--teşekkür)

---

## 📖 Proje Özeti

Bu proje, afet bölgelerinde internet, baz istasyonu veya herhangi bir merkezi altyapı bulunmadığında dahi çalışabilen, **düşük maliyetli**, **enerji verimli** ve kullanıcıların mevcut akıllı telefonlarını kullanan bir **yerel ad-hoc/mesh haberleşme prototipi** geliştirmeyi amaçlamaktadır.

---

## 🎯 Giriş ve Motivasyon

Türkiye, jeolojik konumu ve sismik hareketliliği nedeniyle sık sık büyük depremlerle karşılaşan bir ülkedir. Afet anlarında hücresel şebekelerin ve internet altyapısının fiziksel hasar veya aşırı yoğunluk sebebiyle çökmesi;
- Arama-kurtarma koordinasyonunun aksamasına,
- İlk müdahale ekipleri ile afetzedeler arasındaki iletişimin tamamen kopmasına yol açmaktadır.

**Projenin Temel Amacı:**  
Merkezi bir altyapı gerektirmeksizin mevcut akıllı telefonlar arasında cihazdan cihaza (D2D) bağlantı kurarak, internetsiz koşullarda çalışan yerel bir UDP mesh iletişim prototipi geliştirmektir. Ağ üzerindeki paket teslimat güvenilirliğini artırmak için **hafif İleri Hata Düzeltme (FEC)** ve **hop-by-hop yeniden iletim (retransmission)** mekanizmaları entegre edilmektedir.

---

## 🔍 Temel Özellikler ve Kapsam

- **Altyapısız / İnternetsiz Çalışma:** İnternet, hücresel veri veya baz istasyonuna bağımlılık olmaksızın iletişim.
- **Düşük Enerji Tüketimi:** Sahada batarya süresini korumak adına optimize edilmiş hafif UDP veri transferi.
- **Hata Dayanıklılığı:** Paket kayıplarını tolere eden hafif FEC algoritmaları.
- **Doğrulanabilir MVP Kapsamı:** Saha uygulanabilirliği önceliğiyle mahalle/kampüs ölçeğinde **3–5 cihazlı test kümeleri** üzerinde doğrulanacak gerçekçi deney ortamı.

---

## 🛠 Yöntem ve Çalışma Aşamaları

Proje üç temel mühendislik ve araştırma fazından oluşmaktadır:

┌────────────────────────────────┐    ┌─────────────────────────────────┐    ┌───────────────────────────────────┐
│ 1. Mobil Uygulama Geliştirme   │───>│ 2. Saha & Performans Testleri   │───>│ 3. Veri Analizi & Optimizasyon    │
│ • Wi-Fi Direct / Wi-Fi Aware   │    │ • Kampüs / Mahalle ölçeği test  │    │ • Hata düzeltme (FEC) optimizasyonu│
│ • UDP Soket Programlama         │    │ • Gecikme (Latency) analizi     │    │ • Hop-by-hop mekanizma doğrulama  │
│ • D2D Mesh Mimarisi Entegrasyon │    │ • Paket kaybı (Loss) ölçümü     │    │ • Güvenilirlik raporlaması        │
└────────────────────────────────┘    └─────────────────────────────────┘    └───────────────────────────────────┘


1. **Mobil Uygulama Geliştirme:** Android platformu üzerinde *Wi-Fi Direct* ve *Wi-Fi Aware* (NAN) teknolojileri kullanılarak UDP soket tabanlı veri alışveriş mekanizmasının geliştirilmesi.
2. **Saha Testleri ve Performans Ölçümleri:** Kampüs ve yerel mahalle ölçeğinde gerçekleştirilen testlerle uçtan uca gecikme (*latency*), paket teslim oranı (*PDR*) ve paket kaybı (*packet loss*) metriklerinin çıkarılması.
3. **Veri Analizi ve Değerlendirme:** Elde edilen saha verileriyle hafif hata düzeltme (*FEC*) ve paket iletim algoritmalarının performansının optimize edilmesi.

---

## 💻 Teknoloji Yığını

| Alan | Kullanılan Teknolojiler / Protokoller |
| :--- | :--- |
| **Platform** | Android OS |
| **Bağlantı & Protokol** | UDP (User Datagram Protocol), Wi-Fi Direct (P2P), Wi-Fi Aware (NAN) |
| **Ağ Topolojisi** | Ad-Hoc / D2D Mesh Ağı |
| **Güvenilirlik & Hata Denetimi** | Forward Error Correction (FEC), Hop-by-Hop Retransmission |

---

## 👥 Proje Ekibi ve Danışman

**Yalova Üniversitesi — Mühendislik Fakültesi**  
*Elektrik-Elektronik Mühendisliği Bölümü*

* **Proje Yürütücüsü:** Ali SABOURI
* **Akademik Danışman:** Dr. Öğr. Üyesi Abdullah BALCI

### Proje Ekibi / Araştırmacılar
  Zelal MUŞTU - Özde ÖZGEN - Sinem ŞAHİN - Elisa KAYİŞ

---

## 🤝 Destekleyen Kurumlar & Teşekkür

Bu çalışma, **TÜBİTAK 2209-A - Üniversite Öğrencileri Araştırma Projeleri Destekleme Programı** kapsamında desteklenmektedir. Ekibimizin azmına teşekkür ediyorum.
