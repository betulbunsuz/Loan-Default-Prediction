# 🏦 Loan Default Prediction with CatBoost

Bu proje, kredi başvurusunda bulunan müşterilerin temerrüde düşme (borcunu ödeyememe) olasılığını tahmin etmek amacıyla geliştirilmiş bir uçtan uca makine öğrenmesi projesidir.

<img width="1800" height="1200" alt="image" src="https://github.com/user-attachments/assets/ff068879-3aff-49cf-a40a-a9b3f7f123d6" />

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

<img width="1189" height="690" alt="image" src="https://github.com/user-attachments/assets/20b65d78-8eba-45fe-bfb0-06edee5b1635" />
<img width="1189" height="690" alt="image" src="https://github.com/user-attachments/assets/9ac1de86-30b9-4270-8931-b5916e5ff046" />
<img width="989" height="490" alt="image" src="https://github.com/user-attachments/assets/227af9df-7a44-40cb-985a-f4becebac4be" />
<img width="1204" height="989" alt="image" src="https://github.com/user-attachments/assets/d75f26bd-2e33-45c6-b3dc-5a12cf6cad88" />

## 📈 Sonuçlar
* **Test ROC-AUC:** 0.85+ (Kendi sonucunu buraya yaz)
* **Önemli Değişkenler:** Modelin karar vermesinde en etkili olan ilk 3 özellik: `income`, `loan_amount` ve `credit_score`.
* 
<img width="710" height="435" alt="image" src="https://github.com/user-attachments/assets/415a6f28-5da1-40f0-8511-5f1e4fa96082" />
<img width="582" height="490" alt="image" src="https://github.com/user-attachments/assets/31c52c60-81c4-4b3b-b241-9c04a0632435" />

## 🚀 Kullanılan Teknolojiler
* **Dil:** Python
* **Kütüphaneler:** Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn
* **Algoritma:** CatBoost (Gradient Boosting)

## 📁 Dosya Yapısı
- `loan_prediction.ipynb`: Tüm analiz ve modelleme kodları.
- `README.md`: Proje açıklamaları.

## 📝 Notlar
Bu çalışma, [Kaggle Loan Default Dataset](KAGGE_LINKINI_BURAYA_YAPISTIR) kullanılarak hazırlanmıştır.
