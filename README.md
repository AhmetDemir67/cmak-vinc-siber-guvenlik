# CMAK Gezer Köprülü Vinç — Siber Güvenlik & Emniyet Çalışması

**Ders:** Yazılım Mühendisliği Güncel Konular
**Hazırlayan:** Ahmet Demir · Fırat Üniversitesi, Yazılım Mühendisliği
**Makine:** CMAK (Çakmak Vinç) Gezer Köprülü Vinç — SAMİB üyesi
**Yöntem:** INSPECCO × Kriptarium "Safety 4.0 Bootcamp" laboratuvar föyleri

---

## 📌 Konu

Endüstriyel bir makinenin (gezer köprülü vinç) **siber güvenlik** açısından incelenmesi:
makinenin varlıkları, emniyet fonksiyonları, siber zafiyetleri, bu zafiyetlerin
**fiziksel (insana zarar) sonuçları**, saldırı altında emniyetli kalıp kalmadığı ve
bir SWOT analizi. Çalışma tamamen **savunma / uyum (compliance)** odaklıdır.

> Merkez fikir: Bu vinçte doğru tasarımda her siber saldırının sonucu **"güvenli durma"**
> (safe state) olmalıdır — asla kontrolsüz hareket değil. Yeni AB Makine Tüzüğü'nün
> (2023/1230) 1.1.9 maddesi ve CRA (2024/2847) tam olarak bunu bekler.

---

## 📁 İçerik

| Dosya | Açıklama |
|------|----------|
| `CMAK_Lab1_Safety_Architecture.pdf` | **Lab 1** — Safety Architecture / Safety Function Map |
| `CMAK_Lab2_IEC62443_Zone_Conduit.pdf` | **Lab 2** — IEC 62443 Zone / Conduit + güvenli uzak erişim kararı |
| `CMAK_Lab3_Threat_Risk_Matrix.pdf` | **Lab 3** — Tehdit senaryoları + Risk Matrisi (L × S × E) |
| `CMAK_Lab4_Secure_Remote_Access.pdf` | **Lab 4** — Secure Remote Access + functional safety köprüsü |
| `CMAK_Lab5_SBOM_CVE_Patch.pdf` | **Lab 5** — SBOM / CVE / Patch karar akışı (Vulnerability Decision) |
| `CMAK_Lab6_CRA_Incident_Simulation.pdf` | **Lab 6** — CRA Olay Müdahale Simülasyonu (24s / 72s / 14 gün) |
| `CMAK_Lab7_AI_Safety_Challenge.pdf` | **Lab 7** — AI Safety Challenge (AI Fail-Safe Decision) |
| `CMAK_SWOT_Analizi.pdf` | Siber güvenlik odaklı **SWOT** analizi |
| `CMAK_SMART_Analizi.pdf` | SWOT bulgularını somut, ölçülebilir, tarihli hedeflere çeviren **SMART** analizi |

> Laboratuvar föyleri, dersin orijinal föy şablonu **birebir korunarak** doldurulmuştur;
> yalnızca örnek makine adı CMAK Gezer Köprülü Vinç olarak değiştirilmiş ve cevaplar
> föyün üzerine (mavi "→" ile) yazılmıştır.

---

## 🔑 Özet bulgular

**Siberden bağımsız, korunan katman:** yaylı fail-safe fren, kablolu E-stop,
elektromekanik aşırı yük koruması (CMAK'ta standart), elektromekanik limit şalterleri.

**Siber saldırıya açık katman:** telsiz (433 MHz) kumanda, uzak izleme modülü,
invertör parametreleri, HoistSense+ yazılım yük ölçümü, hesap/ağ yönetimi.

**En kritik senaryo (S1):** şifresiz telsiz kumandada komut tekrarı (replay) →
operatör yokken yük kalkar → personele çarpar/ezer. Skor **18 (Kritik)**.

---

## 📐 Referanslar

- **Standartlar:** EN ISO 12100 · EN ISO 13849-1 · IEC 62061 · IEC 62443 · EN 15011 · EN 14492-2 · EN 60204-32
- **Mevzuat:** (AB) 2023/1230 Makine Tüzüğü · (AB) 2024/2847 CRA (Cyber Resilience Act)
- **Araştırma:** Trend Micro (2019), telsiz kumanda replay saldırıları

---

## ⚠️ Sorumluluk reddi

Bu çalışma bir **eğitim çıktısıdır**; resmî denetim, uygunluk değerlendirmesi veya
belgelendirme değildir ve CE/mevzuat uygunluğunu garanti etmez. Belirtilen zafiyetler,
bu tip vinçlerde bilinen/olası sınıf-düzeyi varsayımlardır; CMAK ürününde test edilip
doğrulanmış açıklar değildir ve üreticiyle teyit edilmelidir.
