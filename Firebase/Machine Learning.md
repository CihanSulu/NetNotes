**Firebase ML** (Firebase Machine Learning), mobil uygulamalara **yapay zeka / makine öğrenmesi özellikleri eklemeyi kolaylaştıran** bir Firebase servisidir. Özellikle Android ve iOS uygulamalarında **cihaz üzerinde (on-device)** veya **bulut üzerinden** çalışan ML modellerini kullanmanı sağlar.

Basitçe:  
📱 **Uygulamana görüntü tanıma, metin okuma, obje algılama gibi AI özellikleri eklemek için kullanılır.**

---

# Firebase ML Ne Amaçla Kullanılır? 🤖

## 1️⃣ Metin Tanıma (Text Recognition)

Bir fotoğraf içindeki yazıları okuyabilir.

Örnek kullanım:

- fatura okuma
    
- kartvizit okuma
    
- belge tarama
    
- plaka okuma
    

Bu özellik aslında **Google ML Kit** teknolojisini kullanır.

---

## 2️⃣ Görüntü Etiketleme (Image Labeling)

Bir fotoğrafın içinde ne olduğunu algılar.

Örnek:

📷 Fotoğraf → sonuç

- "cat"
    
- "animal"
    
- "pet"
    

---

## 3️⃣ Nesne Algılama (Object Detection)

Fotoğraftaki nesneleri tespit eder.

Örnek:

- insan
    
- araba
    
- telefon
    
- masa
    

---

## 4️⃣ Barkod / QR Kod Okuma

Kameradan:

- QR kod
    
- barkod
    
- ürün kodu
    

okuyabilirsin.

Örneğin:

- market uygulamaları
    
- bilet uygulamaları
    

---

## 5️⃣ Yüz Algılama (Face Detection)

Bir fotoğrafta:

- yüz var mı
    
- kaç yüz var
    
- yüz konumu
    

tespit edilir.

---

# Özel Model Kullanma (Custom Model) 🧠

Firebase ML sadece hazır modeller değil, **kendi eğittiğin modelleri de kullanmana izin verir.**

Örneğin:

Modeli şu platformlarda eğitirsin:

- **TensorFlow**
    
- **TensorFlow Lite**
    

Sonra Firebase'e yükleyip uygulamada kullanırsın.

Örnek:

- bitki tanıma uygulaması
    
- hastalık teşhis modeli
    
- ürün tanıma sistemi
    

---

# Firebase ML Nasıl Çalışır?

2 farklı çalışma yöntemi vardır:

### 1️⃣ On-device ML (Cihaz üzerinde)

Model telefon içinde çalışır.

Avantajları:

- internet gerekmez
    
- hızlıdır
    
- gizlilik sağlar
    

---

### 2️⃣ Cloud ML (Bulut)

Model **Google Cloud sunucularında çalışır.

Avantajları:

- daha güçlü modeller
    
- daha yüksek doğruluk
    

---

# Basit Kullanım Örneği (Text Recognition)

Android örneği:
```
val recognizer = TextRecognition.getClient()  
  
val image = InputImage.fromBitmap(bitmap, 0)  
  
recognizer.process(image)  
    .addOnSuccessListener { visionText ->  
        val text = visionText.text  
        println(text)  
    }

```
---

# Firebase ML Ne Tür Uygulamalarda Kullanılır?

📱 Yaygın örnekler:

- belge tarama uygulamaları
    
- çeviri uygulamaları
    
- alışveriş uygulamaları
    
- güvenlik uygulamaları
    
- fotoğraf analiz uygulamaları
    
- AR uygulamaları
    

---

# Önemli Not ⚠️

Firebase ML servisi zamanla **büyük ölçüde**  
👉 **Google ML Kit**'e taşınmıştır.

Yani yeni projelerde genelde:

**Firebase ML yerine ML Kit kullanılır.**

---

✅ **Özet:**

Firebase ML =  
Mobil uygulamalara **AI özellikleri eklemek için kullanılan Firebase servisi**.

Örnek özellikler:

- metin okuma
    
- yüz algılama
    
- obje tanıma
    
- barkod okuma
    
- özel ML modeli kullanma