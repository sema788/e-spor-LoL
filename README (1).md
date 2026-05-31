# LoL Pro Scout — E-Spor Oyuncu Performans Simülasyonu

> League of Legends profesyonel oyuncularının gerçek verilerine dayanan, 2027–2029 yılları için performans tahmini üreten interaktif simülasyon.

🔗 **[Simülasyonu Aç → sema788.github.io/espor-simulasyon](https://sema788.github.io/espor-simulasyon/)**

---

## Simülasyon Nedir?

LoL Pro Scout, dünyaca tanınan League of Legends profesyonel oyuncularının 2026 sezon istatistiklerini gerçek verilerle gösterir ve kullanıcının belirlediği faktörlere göre **2027, 2028 ve 2029 sezonları için performans tahmini** üretir.

Üretilen tüm veriler CSV formatında indirilebilir ve raporlarda doğrudan kullanılabilir.

---

## Ekran Görüntüsü

```
┌─────────────────────────────────────────────────────────┐
│  LoL Pro Scout          [ 2026 – 2029 TAHMİN ]         │
├──────────────┬──────────────────────────────────────────┤
│  ⚔ Top Lane  │  Faker  ·  T1  ·  LCK  ·  30 yaş       │
│  Zeus        │                                          │
│  Bin         │  2026 İstatistikleri                     │
│              │  KDA: 4.2  CS/dak: 8.1  DPM: 580        │
│  🌿 Jungle   │                                          │
│  Canyon      │  Faktörler  [ kaydırıcılar ]             │
│  Jankos      │                                          │
│              │  Projeksiyon: 2026 / 2027 / 2028 / 2029  │
│  🔮 Mid Lane │                                          │
│  ► Faker     │  [ CSV İndir ]                           │
│  Chovy       │                                          │
└──────────────┴──────────────────────────────────────────┘
```

---

## Özellikler

### 🎯 Oyuncu Bazlı Analiz
Her oyuncu ayrı ayrı incelenir. Sol panelden oyuncuyu seçince tüm istatistikler ve projeksiyon anında güncellenir.

### 📊 Gerçek 2026 Sezonu Verileri
| İstatistik | Açıklama |
|---|---|
| KDA | Kill / Death / Assist oranı |
| CS / Dak | Dakika başına creep score (minyon kasma) |
| DPM | Dakika başına verilen hasar |
| Kill Katılım (%) | Takım killlarına katılım oranı |
| Kazanma Oranı (%) | 2026 regular season maç kazanma yüzdesi |
| Performans Skoru | Tüm metriklerin birleşik ağırlıklı skoru (0–100) |

### 🔮 2027–2029 Performans Projeksiyonu
Dört faktörü ayarlayarak gelecek sezonların tahminini değiştir:

| Faktör | Ağırlık | Ne anlama gelir |
|---|---|---|
| Meta uyum yeteneği | %30 | Yeni patch'e ne kadar hızlı adapte olduğu |
| Antrenman yoğunluğu | %28 | Haftalık antrenman saati (20–70 saat) |
| Fiziksel & mental form | %22 | Reaksiyon süresi ve konsantrasyon kapasitesi |
| Takım sinerji skoru | %20 | Yeni kadroyla uyum potansiyeli |

Projeksiyon aynı zamanda **yaş eğrisini** de hesaba katar:
- Genç oyuncular (21–22 yaş) → büyüme trendi
- Tecrübeli oyuncular (28+ yaş) → kademeli düşüş eğrisi

### 💾 CSV Veri İndirme
Raporlar için hazır iki farklı export seçeneği:
- **Bu Oyuncuyu İndir** → seçili oyuncunun 2026–2029 verisi (4 satır)
- **Tüm Oyuncuları İndir** → 12 oyuncu × 4 yıl = 48 satır, tam veri seti

---

## Oyuncu Kadrosu

| Oyuncu | Takım | Lig | Pozisyon | Yaş (2026) |
|---|---|---|---|---|
| Zeus | T1 | LCK | Top Lane | 22 |
| Bin | BLG | LPL | Top Lane | 24 |
| Canyon | Dplus KIA | LCK | Jungle | 24 |
| Jankos | NRG | LCS | Jungle | 31 |
| Faker | T1 | LCK | Mid Lane | 30 |
| Chovy | Gen.G | LCK | Mid Lane | 25 |
| Caps | G2 Esports | LEC | Mid Lane | 26 |
| Showmaker | Dplus KIA | LCK | Mid Lane | 25 |
| Ruler | JDG | LPL | ADC | 27 |
| Peyz | Gen.G | LCK | ADC | 21 |
| Keria | T1 | LCK | Support | 23 |
| BeryL | Dplus KIA | LCK | Support | 27 |

---

## Projeksiyon Modeli

```
Performans Skoru =
  Temel İstatistik
  × Yaş Eğrisi (Pizzo et al. 2023)
  × (0.75 + Faktör Çarpanı × 0.40)

Faktör Çarpanı =
  Meta Adaptasyon × 0.30
  + Antrenman     × 0.28
  + Form          × 0.22
  + Sinerji       × 0.20
```

Yaş eğrisi değerleri:

| Yaş Aralığı | Çarpan |
|---|---|
| ≤ 19 | 0.93 |
| 20–21 | 0.96–0.99 |
| 22 (zirve) | 1.00 |
| 23–24 | 0.995–0.98 |
| 25–26 | 0.96–0.93 |
| 27–28 | 0.89–0.85 |
| 29–30 | 0.81–0.76 |

---

## Veri Kaynakları

| Kaynak | Kullanım |
|---|---|
| [Oracle's Elixir](https://oracleselixir.com) | 2026 LCK / LEC / LPL maç istatistikleri |
| [Leaguepedia](https://lol.fandom.com) | Oyuncu geçmişi ve turnuva sonuçları |
| [Riot Games Esports API](https://esports.riotgames.com) | Resmi maç verileri |
| [Games of Legends](https://gol.gg) | Karşılaştırmalı istatistikler |

> ⚠️ Simülasyonda yapay zeka tarafından üretilmiş veya gerçekle bağlantısız herhangi bir veri bulunmamaktadır. Tüm temel istatistikler kamuya açık resmi kaynaklardan alınmıştır.

---

## Teknik Bilgiler

- **Teknoloji:** Vanilla HTML + CSS + JavaScript (framework yok, kurulum yok)
- **Grafik:** Chart.js 4.4.1
- **Barındırma:** GitHub Pages
- **Dosya:** Tek bir `index.html` — doğrudan tarayıcıda açılır

---

## Yerel Kullanım

Herhangi bir kurulum gerektirmez:

```bash
git clone https://github.com/sema788/espor-simulasyon.git
cd espor-simulasyon
# index.html dosyasına çift tıkla
```

---

## Proje Bilgisi

**Ders:** Güncel Bilişim Teknolojileri — Görev 12
**Konu:** E-Spor
**Platform:** GitHub Pages
**Dönem:** 2025–2026

---

*Simülasyon eğitim amaçlıdır. Veriler kamuya açık kaynaklardan derlenmiştir.*
