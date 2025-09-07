### 📌 4 soatlik ish rejasi (ertaga)

**1️⃣ RabbitMQ qismi (1 soat)**

* `welcome to todolist` email jo‘natish kodini yaxshilab ko‘rib chiqasan.
* Queue → Worker → Email job oqimini to‘liq ichiga gacha tushunib olasan.
* Tugallanmagan joylari bo‘lsa, yakunlab qo‘yasan.

**2️⃣ Redis + Asynq bilan Cron Job (1.5 soat)**

* Redis va `asynq` kutubxonasi orqali cron job yozasan.
* Har 1 soatda foydalanuvchiga `Todolist web appga qarang yoki yangi todo qo‘shing ✅` degan email yuboriladigan qilib sozlaysan.
* Shu yerda caching va job retry’ni ham sinab ko‘rsang zo‘r bo‘ladi.

**3️⃣ Real-time Notifications (1.5 soat)**

* Redis Pub/Sub yoki WebSocket orqali todo qo‘shilganda real-time xabar yuborish.
* Masalan: “Siz 1 ta yangi todo qo‘shdingiz”, yoki “Sizda hozir 7 ta todo bor”.
* Todo’lar sonini, qachon qo‘shganini real-time ko‘rsatib turadigan qism yozasan.

