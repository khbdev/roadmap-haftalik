

### **7:30 – 12:00: TodoList loyihasini backend/async qismi**

1. **Cron jobs + Asynq (Go)**

   * Har 1 soatda email yuborish funksiyasini yozish.
   * Delay va retry logikasini to‘liq sozlash.
   * Test qilish: bitta foydalanuvchiga cron orqali yuborishni tekshirish.

2. **Redis Pub/Sub bilan real-time notifications**

   * Foydalanuvchi todolist qo‘shganda, Redis channel orqali signal yuborish.
   * Subscriber foydalanuvchini 1 soat keyin ogohlantirishi kerak.
   * Test qilish: bir nechta subscriber bilan ishlash, real-time signal kelishini tekshirish.

3. **RabbitMQ bilan user welcome workflow**

   * User royhatdan o‘tganda, welcome todo yuborish.
   * Loglash: har bir message qanday ketayotganini, qayerda block bo‘layotganini yozib olish.
   * Scalability test: ko‘p user qo‘shib, queue va consumerlarni kuzatish.

> Shu qismni tugatgandan keyin, backend ishlari to‘liq ishlashi kerak.

---

### **14:00 – keyingi vaqt: Docker & Deployment**

1. **Docker Compose**

   * TodoList loyihasi + Redis + RabbitMQ + (agar kerak bo‘lsa) Postgres/MySQL containerlari.
   * `.env` va volume’larni sozlash.
   * Build & run test (`docker-compose up --build`).

2. **Image’larni Docker Hub’ga push qilish**

   * Har service uchun tag belgilash (`aziz/todolist:latest`).
   * Compose’ni Hub image’lar bilan ishlatish testini o‘tkazish.

3. **Render bilan deploy qilish (optional)**

   * Render’da image orqali service yaratish.
   * Agar VPS yo‘q bo‘lsa, Render trial yoki free tier orqali minimal test qilsa bo‘ladi.
   * Agar imkoni bo‘lmasa, localda docker-compose bilan simulyatsiya qil.

---
