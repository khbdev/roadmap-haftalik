

---

## 📅 7-Hafta: Queue + Job + Email (6 kunlik)

---

### 🔹 **1-kun: Background Jobs va Queue Asoslari**

**Nazariya (07:00–10:00):**

* Background job nima? Nega kerak?
* Sync va Async farqi
* Worker va Queue arxitekturasi
* Queue sistemalarida: Retry, Delay, Priority, Dead Letter Queue tushunchalari

**Amaliy (10:30–15:00):**

* Oddiy **Go routine** va **channel** bilan background job simulation yozish
* Retry va delay’ni oddiy kodda implementatsiya qilish

**Mini Project (15:30–18:00):**

* “Email Queue Simulator”: Email yuborishni simulate qiladigan job yaratish (chunki haqiqiy email emas, faqat log yozadi → retry va delay ishlaydi).

---

### 🔹 **2-kun: Asynq bilan Background Jobs**

**Nazariya (07:00–10:00):**

* Asynq nima va qanday ishlaydi
* Redis asosida queue mexanizmi
* Task handler, worker, scheduler

**Amaliy (10:30–15:00):**

* Asynq bilan oddiy job yaratish (`send_welcome_email`)
* Retry, delay va priority qo‘llash
* Dashboard bilan kuzatish

**Mini Project (15:30–18:00):**

* “User Registration + Email Queue”: Foydalanuvchi ro‘yxatdan o‘tganda welcome email yuborish (Asynq + Redis).

---

### 🔹 **3-kun: RabbitMQ Fundamentals**

**Nazariya (07:00–10:00):**

* RabbitMQ nima? Kafka’dan farqi
* Exchange, Queue, Routing key
* Consumer va Producer modeli
* Ack/Nack, Dead Letter Queue

**Amaliy (10:30–15:00):**

* Go’da RabbitMQ producer va consumer yozish
* Oddiy job: `send_notification`

**Mini Project (15:30–18:00):**

* “Task Queue”: Foydalanuvchi `upload file` qilsa, RabbitMQ consumer uni backgroundda process qiladi (masalan: faylni kichraytirish / convert qilishni simulate).

---

### 🔹 **4-kun: Go Workers (Alternativ Worker Libraries)**

**Nazariya (07:00–09:30):**

* Go’da turli worker kutubxonalar (go-workers, machinery, faktoriya sifatida Resque style)
* Redis asosida task dispatch

**Amaliy (10:00–15:00):**

* Go-Workers bilan oddiy job qilish (`process_payment`)
* Parallel workers yaratish
* Error handling va retry mexanizmi

**Mini Project (15:30–18:00):**

* “Payment Worker”: User payment qilsa, job queue’da process bo‘ladi va natijasi loglanadi.

---

### 🔹 **5-kun: Email Yuborish**

**Nazariya (07:00–09:30):**

* SMTP protokoli
* `gomail` bilan email yuborish
* Transactional email (confirm email, password reset) tushunchasi

**Amaliy (10:00–15:00):**

* Gmail SMTP orqali oddiy email yuborish
* HTML email template yaratish
* Fayl attach qilish

**Mini Project (15:30–18:00):**

* “Password Reset Flow”: User parolni unutsa → Email yuboriladi (gomail bilan).

---

### 🔹 **6-kun: Yakuniy Katta Amaliy Loyiha**

👉 Oldingi kunlarda o‘rganilgan hamma narsani jamlash.

**Project:** **Task Processing System**

* User ro‘yxatdan o‘tadi → Email yuboriladi (gomail + asynq).
* User fayl upload qiladi → Fayl RabbitMQ orqali backgroundda process qilinadi.
* Admin panel → Asynq Dashboard orqali jobs monitoring.
* Retry, delay, priority qo‘llaniladi.

⏳ Kun oxirida → **to‘liq ishlaydigan background job + email + queue integratsiyasi** bo‘ladi.

---

✅ Shu rejada sen **RabbitMQ**ga alohida kun ajratilgan (3-kun).
✅ Har kuni nazariya → amaliy → mini project bilan tugaydi.
✅ 6-kuni esa **hamma narsani jamlab katta loyiha** qilasan.

---

