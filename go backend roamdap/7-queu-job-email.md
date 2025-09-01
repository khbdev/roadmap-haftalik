

### 🔹 **1-kun: Background Jobs va Queue Asoslari**

**Nazariya (14:00–15:30):**

* Background job nima? Nega kerak?
* Sync va Async farqi
* Worker va Queue arxitekturasi
* Queue sistemalarida Retry, Delay, Priority, Dead Letter Queue tushunchalari

**Amaliy (15:30–17:00):**

* Oddiy **goroutine** va **channel** bilan background job simulation yozish
* Retry va delay’ni oddiy kodda implementatsiya qilish

**Mini Project (17:00–19:00):**

* **Email Queue Simulator**: Email yuborishni simulate qiladigan job yaratish (faqat log yozadi → retry va delay ishlaydi).

---

### 🔹 **2-kun: Asynq Asoslari**

**Nazariya (14:00–15:00):**

* Asynq nima va qanday ishlaydi (Redis asosida)
* Task, Queue, Worker, Client tushunchalari
* Retry va Delay mexanizmlari

**Amaliy (15:00–16:30):**

* Asynq o‘rnatish va ishlatish
* Oddiy `hello task` yaratish va worker bilan qayta ishlash

**Mini Project (16:30–19:00):**

* **Asynq Email Logger**: HTTP orqali task yuborish → worker uni background’da log qiladi (retry + delay sozlanadi).

---

### 🔹 **3-kun: Redis bilan Queue**

**Nazariya (14:00–15:00):**

* Redis asoslari: List, Pub/Sub
* Oddiy queue uchun `LPUSH/BRPOP` ishlatish
* TTL va Retry g‘oyasi

**Amaliy (15:00–16:30):**

* go-redis bilan oddiy producer/consumer yozish
* Pub/Sub orqali natijani kuzatish

**Mini Project (16:30–19:00):**

* **Redis Queue OTP Service**:

  * Producer: `signup` bo‘lsa `otp` yaratib queue’ga qo‘yadi
  * Consumer: OTP’ni olib log qiladi
  * TTL bilan OTP 5 daqiqa ichida eskiradi

---

### 🔹 **4-kun: RabbitMQ Asoslari**

**Nazariya (14:00–15:00):**

* RabbitMQ arxitekturasi: Exchange, Queue, Binding
* Ack/Nack va Prefetch tushunchalari

**Amaliy (15:00–16:30):**

* Producer → queue’ga xabar yuboradi
* Consumer → xabarni olib qayta ishlaydi

**Mini Project (16:30–19:00):**

* **RabbitMQ Email Queue**: producer email task yuboradi, consumer esa uni log qiladi (ack ishlaydi).

---

### 🔹 **5-kun: RabbitMQ Advanced**

**Nazariya (14:00–15:00):**

* Dead Letter Queue (DLQ) va Retry mexanizmi
* Topic exchange bilan routing
* Delay queue

**Amaliy (15:00–16:30):**

* DLX bilan retry qilishni sozlash
* 2 xil routing key (`signup`, `report`) bilan consumer yozish

**Mini Project (16:30–19:00):**

* **RabbitMQ Retry Service**:

  * Agar email yuborishda xato bo‘lsa → DLQ’ga tushadi
  * 5 soniyadan so‘ng qayta ishlanadi
  * Signup va Report xabarlari alohida consumer’larda ishlanadi

---

### 🔹 **6-kun: Yakuniy Integratsiya**

**Nazariya (14:00–15:00):**

* Real loyihalarda job queue best practices
* Monitoring (asynqmon, RabbitMQ UI)
* Logging va error handling

**Amaliy (15:00–16:30):**

* REST API orqali `signup` endpoint yaratish
* DB’da foydalanuvchini saqlash
* Background task queue’ga email yuborish

**Mini Project (16:30–19:00):**

* **Signup → Email Service** (yakuniy loyiha):

  * User signup bo‘ladi
  * Background job queue’ga task yuboriladi
  * Worker gomail orqali email yuboradi

