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

## 🔍 Confusion Matrix Analizi

Model performansının sınıf bazında incelenmesi amacıyla Confusion Matrix oluşturulmuştur.

Çoğu sınıf için doğru sınıflandırma oranı yüksektir.

Hatalı tahminler genellikle görsel olarak birbirine benzeyen sınıflar (ör. Shirt – T-shirt/top) arasında gerçekleşmiştir.

Bu durum, veri setinin doğası gereği beklenen bir sonuçtur.

---

📊 Eğitim Grafikleri ve Başarı Metriklerinin Detaylı Analizi

Bu çalışmada Fashion-MNIST veri seti üzerinde geliştirilen Evrişimsel Sinir Ağı (CNN) modeli, eğitim ve test süreçleri boyunca çeşitli performans metrikleri kullanılarak değerlendirilmiştir.
Modelin öğrenme süreci hem sayısal değerler hem de grafiksel gösterimler ile analiz edilmiştir.

Kayıp (Loss) Analizi

Loss vs Epoch grafiğinde, modelin her epoch sonunda hesaplanan eğitim (train) kaybı ve test (validation) kaybı değerleri gösterilmektedir.

Eğitim kaybının epoch’lar ilerledikçe istikrarlı bir şekilde azaldığı gözlemlenmiştir.

Test kaybı da benzer bir eğilim sergileyerek eğitim kaybına paralel şekilde düşmüştür.

Eğitim ve test kayıpları arasında aşırı bir fark oluşmaması, modelin overfitting yapmadığını göstermektedir.

Bu sonuçlar, modelin veriyi başarılı bir şekilde öğrendiğini ve genelleme kabiliyetinin yüksek olduğunu göstermektedir.
Doğruluk (Accuracy) Analizi

Accuracy vs Epoch grafiği, modelin sınıflandırma başarımını değerlendirmek amacıyla kullanılmıştır.

Eğitim doğruluğu epoch’lar boyunca artış göstermiş ve yüksek bir değere ulaşmıştır.

Test doğruluğu da eğitim doğruluğuna yakın seyretmiş ve modelin genel veri üzerinde tutarlı sonuçlar verdiği gözlemlenmiştir.

Eğitim ve test doğrulukları arasındaki farkın düşük olması, modelin ezberleme yerine öğrenme gerçekleştirdiğini göstermektedir.
## 🧠 Sonuç
Elde edilen grafikler ve başarı metrikleri incelendiğinde:
Modelin istikrarlı şekilde öğrendiği
Aşırı öğrenme (overfitting) göstermediği
Test verisi üzerinde yüksek doğrulukla sonuç verdiği sonucuna ulaşılmıştır.

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

