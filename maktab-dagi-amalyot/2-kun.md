
---

### **1️⃣ Docker Hub + hello-api**

* Docker image yaratish va Docker Hub’ga push qilish
* Bu **baza**, keyingi hamma ishlar shu image ustida ishlaydi
* **Prioritet:** 1️⃣

---

### **2️⃣ Redis + Asynq Cron Job**

* Har 1 soatda email yuborish
* Retry va caching’ni sinash
* Redis serverni container’da ishga tushurish
* **Prioritet:** 2️⃣

---

### **3️⃣ Real-time Notifications**

* Redis Pub/Sub yoki WebSocket orqali todo qo‘shilganda real-time xabar
* Todo soni va qo‘shilgan vaqtni ko‘rsatish
* **Prioritet:** 3️⃣

---
