
## 🔹 9-Hafta: Mikroservis Arxitekturasi (6 kunlik)

### 🔹 1-Kun: Mikroservis asoslari va Monolit vs Mikroservis

**17:00 – 18:30 (Nazariya)**

* Monolit arxitektura va uning kamchiliklari
* Mikroservis nima va qanday ishlaydi
* Service-to-service kommunikatsiya asoslari (REST, gRPC, messaging)
* API Gateway va Service Discovery tushunchalari

**18:30 – 20:00 (Amaliyot)**

* Oddiy monolit Go API yaratish (User, Product, Order endpointlari)
* Keyin ularni alohida mikroservislarga ajratish rejasini tuzish

**20:00 – 23:00 (Mini Project)**

* Monolitdan mikroservisga o‘tish diagrammasini chizish (ERD + service interaction)
* `user-service` skeletonini yaratish (Gin + REST endpoint)

---

### 🔹 2-Kun: User-service amaliyoti

**17:00 – 18:30 (Nazariya)**

* User-service CRUD endpointlari
* Service-to-service authentication (API Key, JWT)
* Database design (MySQL/PostgreSQL)

**18:30 – 20:00 (Amaliyot)**

* User-service uchun MySQL ulanishini sozlash
* Gin bilan RESTful CRUD endpointlar yaratish (Create, Read, Update, Delete)

**20:00 – 23:00 (Mini Project)**

* User-service’ni Docker container ichida ishga tushirish
* Postman orqali CRUD testlar

---

### 🔹 3-Kun: Product-service amaliyoti

**17:00 – 18:30 (Nazariya)**

* Product-service roli va relationshiplar (User -> Product)
* Service-to-service kommunikatsiya nazariyasi (HTTP client, gRPC)

**18:30 – 20:00 (Amaliyot)**

* Product-service CRUD endpointlarini yaratish
* User-service bilan oddiy REST call orqali integratsiya qilish

**20:00 – 23:00 (Mini Project)**

* Product-service container yaratish
* User-service’ga bog‘langan CRUD testlar
* Docker Compose yordamida ikkala servisni ishga tushirish

---

### 🔹 4-Kun: Order-service amaliyoti

**17:00 – 18:30 (Nazariya)**

* Order-service funksiyalari va mikroservislar bilan integratsiya
* Transactionlar va eventual consistency tushunchasi

**18:30 – 20:00 (Amaliyot)**

* Order-service CRUD endpointlari
* User-service va Product-service bilan service-to-service call

**20:00 – 23:00 (Mini Project)**

* Order-service container yaratish
* Docker Compose orqali 3 service’ni ishga tushurish va integratsiyani test qilish

---

### 🔹 5-Kun: API Gateway va Service Discovery

**17:00 – 18:30 (Nazariya)**

* API Gateway vazifasi (routing, authentication, rate limiting)
* Service Discovery tushunchasi (Consul, etcd, DNS-based)

**18:30 – 20:00 (Amaliyot)**

* Gin bilan oddiy API Gateway yaratish
* Gateway orqali User, Product, Order servislariga call

**20:00 – 23:00 (Mini Project)**

* Docker Compose bilan Gateway va 3 mikroservisni ishlatish
* Postman orqali end-to-end API testlar
* Gateway loglarini kuzatish va monitoring

---

### 🔹 6-Kun: Mini Full Stack Microservices Project

**17:00 – 18:30 (Nazariya)**

* Qo‘shimcha nazariya: logging, monitoring, tracing (Prometheus, Jaeger)
* Deployment nazariyasi (Docker Compose vs Kubernetes)

**18:30 – 20:00 (Amaliyot)**

* Barcha servislarni yagona Docker Compose faylda birlashtirish
* Swagger dokumentatsiyasini qo‘shish

**20:00 – 23:00 (Mini Project)**

* Full microservices project test qilish:

  * CRUD endpoints hammasi ishlashi
  * Gateway orqali calllar
  * Docker Compose bilan multi-container orchestration
* Endi o‘zing xohlasa logging va basic monitoring qo‘shish

