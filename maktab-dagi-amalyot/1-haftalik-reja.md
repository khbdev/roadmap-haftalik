

## 🔹 Telegram Mini-Klon (6 kunlik reja, 9:00–12:00)

### 🔹 1-Kun: Loyihani boshlash va auth tizimi

**9:00 – 10:00 (Nazariya)**

* JWT asosida authentication tushunchasi
* Register, Login, Logout workflow
* Password hashing, validation

**10:00 – 11:00 (Amaliyot)**

* Go + Gin bilan auth endpoints yaratish
* Database (MySQL) ulanishi va `users` jadvali yaratish

**11:00 – 12:00 (Mini Project)**

* Register va Login endpointlarini ishlatib test qilish
* Logout va JWT invalidation funksiyasini qo‘shish

---

### 🔹 2-Kun: Profile bo‘limi

**9:00 – 10:00 (Nazariya)**

* Profile modeli: username, firstname, lastname, bio, rasm
* File upload va storage (local yoki cloud)
* Validation va authorization (faqat o‘z profile’ni o‘zgartira olishi)

**10:00 – 11:00 (Amaliyot)**

* Profile CRUD endpointlarini yaratish
* Rasm yuklash va serverda saqlash

**11:00 – 12:00 (Mini Project)**

* Postman bilan profile create/update/test qilish
* Rasm, bio va username’ni CRUD qilish

---

### 🔹 3-Kun: Foydalanuvchini qidirish

**9:00 – 10:00 (Nazariya)**

* Username orqali search workflow
* Pagination va basic filtering

**10:00 – 11:00 (Amaliyot)**

* `/search?username=` endpoint yaratish
* Query database bilan integratsiya qilish

**11:00 – 12:00 (Mini Project)**

* Search endpointni test qilish
* 5–10 test user qo‘shib qidirishni tekshirish

---

### 🔹 4-Kun: Chat bo‘limi — backend

**9:00 – 10:00 (Nazariya)**

* Real-time chat tushunchasi (WebSocket)
* Message model: sender\_id, receiver\_id, text, timestamp

**10:00 – 11:00 (Amaliyot)**

* Gin + Gorilla WebSocket bilan basic chat server yaratish
* Userlar bir-biriga xabar yuborishi

**11:00 – 12:00 (Mini Project)**

* Simple chat test: ikki user bir-biriga xabar yuboradi
* Messages DB ga yozilishi va o‘qilishi

---

### 🔹 5-Kun: Chat bo‘limi — frontend / integratsiya

**9:00 – 10:00 (Nazariya)**

* Chatni username orqali qidirib topish
* Message history olish, real-time update

**10:00 – 11:00 (Amaliyot)**

* Backend va frontend (oddiy HTML + JS) integratsiyasi
* WebSocket orqali real-time xabar yuborish va olish

**11:00 – 12:00 (Mini Project)**

* Oddiy web interface orqali chat test qilish
* Yozishmalarni saqlash va history ko‘rsatish

---

### 🔹 6-Kun: Yakuniy test va mini-deployment

**9:00 – 10:00 (Nazariya)**

* Deployment nazariyasi: Docker bilan API container qilish
* Basic error handling, validation, logging

**10:00 – 11:00 (Amaliyot)**

* Loyihani Docker container ichida ishga tushirish
* JWT auth, profile va chat endpoints’ni test qilish

**11:00 – 12:00 (Mini Project)**

* Full workflow test: register → profile → search → chat
* Yakuniy project review va code cleanup

---

💡 **Maslahat:**

* Har mini-projectdan so‘ng Git commit qil.
* Chat va WebSocket ishlashini **avval backendda alohida** test qil, keyin frontend bilan integratsiya qil.
* Docker bilan ishlash yakuniy kunni mukammal qiladi va deploy tushunchasini beradi.

