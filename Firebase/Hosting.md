Firebase içindeki **hosting**, web sitelerini veya web uygulamalarını internet üzerinden yayınlamak için kullanılan bir servistir. Temelde **frontend dosyalarını (HTML, CSS, JS, React, Angular, Vue vb.) hızlı ve güvenli şekilde yayınlamanı sağlar.**

Firebase Hosting'in arkasında global CDN vardır, bu yüzden site dünyanın farklı noktalarından **çok hızlı yüklenir**.
# Firebase Hosting nedir? 🚀

Firebase Hosting şu amaçlarla kullanılır:

- Statik web siteleri yayınlamak
    
- SPA uygulamaları yayınlamak (React, Vue, Angular)
    
- API'ye proxy yapmak
    
- SSL ile güvenli hosting
    
- CDN ile hızlı dağıtım
    
- CI/CD ile otomatik deploy
    

Örnek kullanım:

- React sitesi
    
- Landing page
    
- Portfolio sitesi
    
- Admin panel
    
- Web app
    

Deploy genelde şöyle yapılır:

`firebase deploy`

# Firebase panelindeki iki hosting türü

Senin gördüğün iki şey:

- **App Hosting**
    
- **Hosting**
    

Bunlar yeni Firebase sürümünde farklı amaçlara hizmet ediyor.

# 1️⃣ Hosting (klasik Firebase Hosting)

Bu **eski ve en yaygın kullanılan hosting türü.**

Genelde şu projeler için kullanılır:

- React
    
- Vue
    
- Angular
    
- statik site
    
- SPA
    

Deploy mantığı:

local project  
   ↓  
firebase deploy  
   ↓  
Firebase CDN  
   ↓  
internet

Özellikler:

- statik dosya hosting
    
- CDN
    
- ücretsiz SSL
    
- custom domain
    
- redirect & rewrite
    
- backend'e proxy
    

Örnek:

myproject.web.app  
myproject.firebaseapp.com

---

# 2️⃣ App Hosting (yeni sistem)

Firebase App Hosting **2024'te gelen yeni bir sistemdir.**

Amaç:

**Modern fullstack frameworkleri direkt deploy etmek**

Özellikle:

- Next.js
    
- Nuxt.js
    
- Angular SSR
    

gibi frameworkleri **build + server + hosting birlikte çalıştırmak**.

Yani sadece statik hosting değil.

---

### App Hosting nasıl çalışır

Normal hosting:

React build → CDN

App Hosting:

Next.js  
   ↓  
Server Rendering  
   ↓  
Edge / Server  
   ↓  
User

Yani:

- SSR
    
- Server actions
    
- backend logic
    
- dynamic rendering
    

destekler.

---

# Basit fark tablosu

|Özellik|Hosting|App Hosting|
|---|---|---|
|Statik site|✅|✅|
|React SPA|✅|✅|
|Next.js SSR|❌|✅|
|Backend logic|❌|✅|
|Server side rendering|❌|✅|
|En yaygın kullanım|✅|yeni|

---

# Hangi durumda hangisini kullanmalısın?

### Hosting kullan

Eğer:

- React
    
- Vue
    
- Angular SPA
    
- statik site
    
- landing page
    

yapıyorsan.

---

### App Hosting kullan

Eğer:

- Next.js
    
- SSR
    
- fullstack web app
    
- edge rendering
    

yapıyorsan.

---

# Küçük ama önemli bilgi 💡

App Hosting aslında arka planda şu servisleri kullanır:

- Google Cloud Run
    
- Cloud Build
    
- Firebase Hosting CDN
    

Yani **daha kompleks ama güçlü bir sistemdir.**

## Projeyi Canlıya Alma
https://firebase.google.com/docs/hosting?hl=tr

#### 1) Firebase CLI kurulumu
Önce bilgisayara **Firebase CLI** kurulması gerekir.

Node.js yüklü olmalı. (Node.js)
```
npm install -g firebase-tools
firebase --version
```

#### 2) Firebase login
Aşağıdaki komut ile google hesabına giriş yapılması için tarayıcıya yönlendirilir.
`firebase login`

#### 3) Firebase projesi oluştur
Firebase panelden oluşturabilirsin.
👉 [https://console.firebase.google.com](https://console.firebase.google.com)
Yeni proje oluştur.

#### 4) Proje klasörüne git
`cd my-project`

#### 5) Firebase'i projeye bağla (init)
Şimdi Firebase'i projeye initialize edilir.

`firebase init`

Burada bazı seçenekler çıkacak.
Seçilmesi gerekir:
`Hosting: Configure files for Firebase Hosting`

#### 6) 


