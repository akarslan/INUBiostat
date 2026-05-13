<img width="1209" height="309" alt="Logo" src="https://github.com/user-attachments/assets/d7428310-328a-45b7-8d39-25a0b9f0b28f" />

**INUBiostat**, klinik ve sağlık bilimleri araştırmacıları için geliştirilmiş kapsamlı bir biyoistatistik ve makine öğrenmesi yazılımıdır. Kod yazmaya gerek kalmadan parametrik testlerden sağkalım analizlerine, faktör analizinden makine öğrenmesi modellerine kadar geniş bir analiz yelpazesi sunar.

---

## Özellikler

### Parametrik Testler
- Tek Örneklem, Bağımsız Örneklem ve Eşleştirilmiş t-Testi
- Tek Yönlü ANOVA, RM ANOVA, ANCOVA, MANOVA
- Bootstrap t-Testleri (Tek Örneklem, Eşleştirilmiş, Bağımsız)

### Parametrik Olmayan Testler
- İşaret Testi, Wilcoxon İşaretli Sıralar Testi
- Mann-Whitney U, Brunner-Munzel Testi
- Kruskal-Wallis H, Friedman Testi
- Ki-Kare Bağımsızlık Testi
- PERMANOVA & ANOSIM

### Korelasyon & Regresyon
- Pearson, Spearman, Kısmi Korelasyon
- Nominal İlişki Ölçütleri (Phi, Cramer's V, Contingency C)
- Nokta Biserial, Eta Katsayısı, Somer's d
- Doğrusal, Lojistik, Polinom, Robust Regresyon
- Hiyerarşik Doğrusal & Lojistik Regresyon

### Tanı Testleri
- 2×2 Tablo Analizi (Duyarlılık, Seçicilik, PPD, NPD)
- ROC Eğrisi & AUC, ROC Karşılaştırması (DeLong)
- Cohen's Kappa & Weighted Kappa
- McNemar Testi, ICC, Risk Analizi (RR, OR, RD)

### Sağkalım Analizi
- Kaplan-Meier (log-rank testi, çoklu grup karşılaştırma)
- Nelson-Aalen Kümülatif Tehlike Tahmini
- Cox Orantılı Tehlike Regresyonu

### Çok Değişkenli Analizler
- Açıklayıcı Faktör Analizi (AFA) — KMO, Bartlett, Scree plot
- Doğrulayıcı Faktör Analizi (DFA) — CFI, TLI, RMSEA ve daha fazlası
- Diskriminant Analizi — LDA, QDA, FDA, RDA
- Güvenilirlik Analizi — Cronbach α, McDonald ω, madde analizi

### Makine Öğrenmesi
- **Sınıflandırma:** Karar Ağacı, Random Forest, Gradient Boosting, AdaBoost, SVM, KNN, Naive Bayes
- **Regresyon:** Karar Ağacı, Random Forest, Gradient Boosting, AdaBoost, SVR, KNN, Ridge, Lasso, ElasticNet
- **Kümeleme:** K-Means, Hiyerarşik (Ward), DBSCAN
- **SHAP Açıklanabilirlik:** Global önem, beeswarm, waterfall grafikleri; Permütasyon önemi
- ML Görev Seçici — bağımlı değişken tipine göre otomatik öneri

### Veri İşleme
- CSV, Excel ve SPSS dosyası yükleme
- Değişken tipi belirleme (nominal / ordinal / sürekli)
- Değişken hesaplama ve dönüştürme
- Kayıp değer doldurma (MICE, Random Forest, KNN ve daha fazlası)
- Aykırı değer tespiti
- Hızlı Özet Tablo (Table 1) — etki büyüklükleri dahil

### Çıktı & Raporlama
- Tüm analizler için HTML dışa aktarma
- Analiz geçmişi paneli
- Bağlamsal yardım — her analiz için GitHub Wiki sayfası

---

## Kurulum

### Gereksinimler

- Python 3.11 veya üzeri
- pip

### Kurulum Adımları

```bash
# Depoyu klonlayın
git clone https://github.com/akarslan/INUBiostat.git
cd INUBiostat

# Sanal ortam oluşturun (önerilir)
conda create -n inubiostat python=3.12
conda activate inubiostat

# Bağımlılıkları yükleyin
pip install -r requirements.txt

# Uygulamayı başlatın
python run.py
```

Uygulama başladıktan sonra tarayıcınızda `http://127.0.0.1:8050` adresini açın.

---

## Kullanılan Teknolojiler

| Katman | Teknoloji |
|---|---|
| Arayüz | Dash, Dash Bootstrap Components |
| API | FastAPI, Uvicorn |
| İstatistik | SciPy, Statsmodels, Pingouin |
| Makine Öğrenmesi | scikit-learn, SHAP |
| Faktör Analizi | factor_analyzer, semopy |
| Sağkalım | lifelines |
| Veri | pandas, NumPy |
| Görselleştirme | Matplotlib |

---

## Proje Yapısı

```
INUBiostat/
├── run.py                      # Uygulama başlatıcı
├── requirements.txt
├── frontend/
│   ├── app.py                  # Dash arayüzü
│   └── assets/
│       └── logo_b64.txt        # Logo
└── backend/
    ├── api.py                  # FastAPI ana giriş
    ├── models.py               # Pydantic request modelleri
    ├── utils.py                # Ortak yardımcı fonksiyonlar
    └── routers/                # Analiz modülleri
        ├── ttest.py
        ├── anova.py
        ├── regression.py
        ├── survival.py
        ├── ml.py
        ├── explain.py
        └── ...                 # 17 modül
```

---

## Katkı & Lisans

Bu yazılım İnönü Üniversitesi Tıp Fakültesi Biyoistatistik ve Tıp Bilişimi AD bünyesinde geliştirilmektedir.

Geliştiriciler: **Doç. Dr. Ahmet Kadir Arslan, Arş. Gör. Furkan Hazar, Prof. Dr. Cemil Çolak**
