Firebase içinde iki farklı gerçek zamanlı veritabanı vardır: **Cloud Firestore** ve **Firebase Realtime Database**. İkisi de gerçek zamanlı veri senkronizasyonu sağlar ama yapı, ölçeklenebilirlik ve sorgulama özellikleri farklıdır.

Aşağıda en önemli farkları sade şekilde:

|Özellik|Cloud Firestore|Realtime Database|
|---|---|---|
|Veri Yapısı|**Collection → Document** (NoSQL, daha düzenli)|**Tek büyük JSON tree**|
|Sorgular|Gelişmiş query (where, orderBy, limit vs.)|Çok sınırlı query|
|Ölçeklenebilirlik|Çok daha iyi, büyük projeler için|Küçük–orta projeler için|
|Offline Support|Güçlü|Var ama daha basit|
|Fiyatlandırma|Read / Write / Delete bazlı|Bandwidth + connection bazlı|
|Bölgesel dağıtım|Multi-region destekler|Tek region|
|Performans|Büyük datasetlerde daha stabil|Küçük realtime datada hızlı|
### Basit veri yapısı örneği

**Realtime Database:**

```
{  
  "users": {  
    "user1": {  
      "name": "Ali",  
      "age": 25  
    }  
  }  
}
```

**Firestore:**

```
users (collection)  
   └── user1 (document)  
        ├── name: "Ali"  
        └── age: 25
```

### Hangi durumda hangisi kullanılır?

**Realtime Database iyi olur:**

- Basit chat uygulaması
    
- Küçük realtime data
    
- Küçük projeler
    

**Firestore daha iyi olur:**

- Büyük ölçekli uygulamalar
    
- Karmaşık sorgular
    
- Production seviyesinde modern uygulamalar
    

### Günümüzde hangisi daha çok kullanılıyor?

Çoğu yeni projede **Cloud Firestore** tercih ediliyor çünkü:

- daha ölçeklenebilir
    
- query sistemi güçlü
    
- daha modern mimari


## Kullanımı

Firebase consola  girdikten sonra solda **Databases & Storage** adımından NoSQL seçeneğinden
- Firestore
- Realtime Database

seçilir.

