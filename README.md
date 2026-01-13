# 🧠 CNN ile FashionMNIST Görüntü Sınıflandırma Projesi

## 📌 Proje Amacı
Bu projenin amacı, **FashionMNIST** veri seti kullanılarak **Evrişimli Sinir Ağları (Convolutional Neural Networks – CNN)** ile görüntü sınıflandırma işlemini gerçekleştirmektir.  
Model, gri seviye (28×28) kıyafet görsellerini kullanarak **10 farklı sınıfı** doğru şekilde tahmin etmeyi hedefler.

Bu çalışma **Sinir Ağları dersi final projesi** kapsamında geliştirilmiş ve **PyTorch** kütüphanesi kullanılarak uygulanmıştır.

---

## 📂 Kullanılan Veri Seti: FashionMNIST

- **Toplam Görsel Sayısı:** 70.000  
  - Eğitim: 60.000  
  - Test: 10.000  
- **Görsel Boyutu:** 28×28  
- **Renk:** Gri seviye  
- **Sınıf Sayısı:** 10  

---

## 🧱 Model Mimarisi (CNN)

Model, iki evrişim katmanı ve iki tam bağlı katmandan oluşan bir CNN mimarisi kullanmaktadır.

**Katman Akışı:**
```
Input (1×28×28)
 → Conv2D + ReLU
 → MaxPooling
 → Conv2D + ReLU
 → MaxPooling
 → Fully Connected
 → Output (10 sınıf)
```

---

## ⚙️ Eğitim Ayarları
- **Optimizer:** Adam  
- **Learning Rate:** 0.001  
- **Batch Size:** 64  
- **Epoch:** 2–3  
- **Loss Function:** CrossEntropyLoss  

---

## 📊 Eğitim Sonuçları

- **Eğitim Doğruluğu:** %94 – %95  
- **Test Doğruluğu:** %91 – %92  

---

## 📈 Eğitim Grafikleri

### 🔹 Loss – Epoch Grafiği
![Loss Curve](loss_curve.png)

### 🔹 Accuracy – Epoch Grafiği
![Accuracy Curve](accuracy_curve.png)

> Bu grafikler modelin öğrenme sürecinde hata ve doğruluk değişimini göstermektedir.

---

## 🔍 Confusion Matrix
Confusion Matrix analizi ile özellikle **Shirt / T-shirt / Pullover** sınıflarında karışıklık olduğu gözlemlenmiştir.

---

## 🧠 Sonuç
Bu projede CNN mimarisinin görüntü sınıflandırma problemlerinde etkili olduğu görülmüş ve akademik düzeyde başarılı sonuçlar elde edilmiştir.

---

## 📁 Proje Yapısı
```
├── data/
├── loss_curve.png
├── accuracy_curve.png
├── cnn_fashionmnist.ipynb
└── README.md
```

---

## 🔗 GitHub Repository
👉 https://github.com/musenna111/cnn-fashionmnist


## 📊 Training Results

### Loss Curve
Model eğitimi boyunca eğitim (train) ve test (validation) kayıp değerlerinin değişimi:

![Loss Curve](loss_curve.png)

---

### Accuracy Curve
Epoch’lara göre eğitim ve test doğruluk (accuracy) değerleri:

![Accuracy Curve](accuracy_curve.png)

