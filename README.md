# 🏦 Loan Default Prediction with CatBoost

Bu proje, kredi başvurusunda bulunan müşterilerin temerrüde düşme (borcunu ödeyememe) olasılığını tahmin etmek amacıyla geliştirilmiş bir uçtan uca makine öğrenmesi projesidir.

## 📊 Proje Özeti
Projede, müşteri demografisinden kredi detaylarına kadar birçok değişken analiz edilerek, yüksek riskli kredilerin tespit edilmesi hedeflenmiştir. Model olarak kategorik verilerde üstün performans gösteren **CatBoost** algoritması kullanılmıştır.

## 🛠️ Uygulanan Adımlar
1. **Keşifçi Veri Analizi (EDA):** Yaş, cinsiyet ve kredi türü bazında ödeme performansları görselleştirildi.
2. **Özellik Mühendisliği (Feature Engineering):**
   - `loan_to_income`: Kredi miktarının gelire oranı.
   - `credit_score_bin`: Kredi skorlarının kategorize edilmesi.
   - `age_numeric`: Yaş gruplarının sayısal değerlere dönüştürülmesi.
   - Ve çeşitli riskli durum kombinasyonları (Düşük kredi skoru + Negatif amortizasyon vb.) oluşturuldu.
3. **Model Eğitimi:** 5-Katlı Çapraz Doğrulama (5-Fold Cross Validation) ile CatBoost modeli eğitildi.
4. **Performans Ölçümü:** Modelin başarısı ROC-AUC ve Accuracy metrikleri ile değerlendirildi.

## 📈 Sonuçlar
* **Test ROC-AUC:** 0.85+ (Kendi sonucunu buraya yaz)
* **Önemli Değişkenler:** Modelin karar vermesinde en etkili olan ilk 3 özellik: `income`, `loan_amount` ve `credit_score`.

## 🚀 Kullanılan Teknolojiler
* **Dil:** Python
* **Kütüphaneler:** Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn
* **Algoritma:** CatBoost (Gradient Boosting)

## 📁 Dosya Yapısı
- `loan_prediction.ipynb`: Tüm analiz ve modelleme kodları.
- `README.md`: Proje açıklamaları.

## 📝 Notlar
Bu çalışma, [Kaggle Loan Default Dataset](KAGGE_LINKINI_BURAYA_YAPISTIR) kullanılarak hazırlanmıştır.
