**Firebase Functions** (resmi adıyla **Cloud Functions for Firebase**), uygulamanın arka planında çalışan **sunucusuz (serverless) backend kodlarıdır**. Yani sen ayrı bir sunucu kurmadan, belirli olaylar gerçekleştiğinde çalışan kodlar yazabilirsin.

Basitçe:  
➡️ **Bir olay olur → Firebase otomatik olarak senin fonksiyonunu çalıştırır.**

Genellikle **JavaScript / TypeScript** ile yazılır ve **Google Cloud** üzerinde çalışır.

---

# Firebase Functions Ne Amaçla Kullanılır? 🚀

## 1️⃣ Otomatik işlemler yapmak

Firebase içinde bir olay gerçekleştiğinde otomatik kod çalıştırabilirsin.

Örnek:

- Yeni kullanıcı kayıt olunca → Hoşgeldin maili gönder
    
- Veritabanına veri eklenince → başka bir veri oluştur
    
- Fotoğraf yüklenince → otomatik küçük resim üret
    

Örnek olaylar:

- **Firebase Authentication** → kullanıcı oluşturuldu
    
- **Cloud Firestore** → veri eklendi / güncellendi
    
- **Firebase Storage** → dosya yüklendi
    

---

## 2️⃣ Backend API oluşturmak

Mobil veya web uygulaman için **API endpoint** yazabilirsin.

Örneğin:

https://.../api/getUserData

Böylece:

- ödeme işlemleri
    
- özel veri işlemleri
    
- güvenli işlemler
    

backend tarafında yapılır.

---

## 3️⃣ Güvenli işlemler yapmak 🔐

Bazı işlemler **client tarafında yapılmamalıdır**.

Örnek:

- ödeme alma
    
- admin işlemleri
    
- gizli API anahtarları kullanma
    

Bunları **Firebase Functions** içinde saklayabilirsin.

---

## 4️⃣ Zamanlanmış görevler (cron jobs)

Belirli zamanlarda çalışan işlemler yazabilirsin.

Örnek:

- Her gün saat 00:00 → verileri temizle
    
- Her saat → rapor üret
    

---

## 5️⃣ Üçüncü parti servislerle entegrasyon

Örneğin:

- **Stripe** → ödeme
    
- **Twilio** → SMS
    
- **SendGrid** → email
    

---

# Basit Bir Firebase Function Örneği

const functions = require("firebase-functions");  
  
exports.helloWorld = functions.https.onRequest((req, res) => {  
  res.send("Merhaba Firebase!");  
});

Bu bir **HTTP API endpoint** oluşturur.

---

# Firestore Trigger Örneği

Firestore'a veri eklenince çalışan fonksiyon:

exports.newUser = functions.firestore  
  .document("users/{userId}")  
  .onCreate((snap, context) => {  
    const userData = snap.data();  
    console.log("Yeni kullanıcı:", userData);  
  });

---

# Firebase Functions Avantajları 👍

✔ Sunucu kurmana gerek yok  
✔ Otomatik ölçeklenir  
✔ Firebase servisleriyle entegre  
✔ Event tabanlı çalışır  
✔ Backend yazmadan backend gibi kullanabilirsin

---

💡 **Kısaca:**  
Firebase Functions = **Uygulamanın backend mantığını server kurmadan yazmanı sağlar.**

---

İstersen sana ayrıca şunları da anlatabilirim:

- Firebase Functions **gerçek bir projede nasıl kullanılır**
    
- **Frontend → Firebase Functions → Database** mimarisi
    
- **En çok kullanılan 10 Firebase Function senaryosu**
    
- Firebase Functions vs **Node.js backend farkı**
    

İstersen onları da detaylı anlatabilirim.