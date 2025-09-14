

# 🔵 8-Hafta: Docker + CI/CD (6 Kunlik Reja)

---

## 🔹 1-Kun: Docker Asoslari va Dockerfile

**17:00 – 18:30 (Nazariya):**

* Docker nima va nima uchun ishlatiladi?
* VM vs Container farqi
* Image, Container, Registry tushunchalari
* `Dockerfile` sintaksisi (`FROM`, `WORKDIR`, `COPY`, `RUN`, `CMD`, `EXPOSE`)

**18:30 – 20:00 (Amaliyot):**

* Oddiy **Go API** uchun `Dockerfile` yozish
* `docker build`, `docker run`, `docker ps`, `docker logs` bilan ishlash
* Image yaratib container ichida API’ni ishga tushirish

**20:00 – 23:00 (Mini Project):**

* `hello-api` loyihasi uchun Docker image yaratish
* Image’ni Docker Hub’ga push qilish (registry tushunchasini mustahkamlash)

---

## 🔹 2-Kun: Docker Compose va Multi-Container

**17:00 – 18:30 (Nazariya):**

* Docker Compose nima?
* `docker-compose.yml` tuzilishi
* Service, Network, Volume tushunchalari

**18:30 – 20:00 (Amaliyot):**

* API + MySQL + Redis uchun `docker-compose.yml` yozish
* Konteynerlar orasidagi ulanishni sinash (`ping`, `curl`)

**20:00 – 23:00 (Mini Project):**

* **TodoList API** (Go + MySQL + Redis) ni `docker-compose` orqali ishga tushirish

---

## 🔹 3-Kun: GitHub Actions Asoslari

**17:00 – 18:30 (Nazariya):**

* CI/CD tushunchasi: Continuous Integration & Deployment
* GitHub Actions arxitekturasi: Workflow, Job, Step, Action
* `.github/workflows/ci.yml` tuzilishi

**18:30 – 20:00 (Amaliyot):**

* Har commitda **Go test** va **Go build** qiladigan pipeline yozish
* Matrix build (Go 1.21 / 1.22) qilib ko‘rish

**20:00 – 23:00 (Mini Project):**

* TodoList API uchun GitHub Action → test va build pipeline qo‘shish

---

## 🔹 4-Kun: CI/CD Pipeline (Test → Build → Deploy)

**17:00 – 18:30 (Nazariya):**

* CI/CD bosqichlari (Test → Build → Deploy)
* Docker image build va push qilishni CI ichida ishlatish

**18:30 – 20:00 (Amaliyot):**

* GitHub Action’da Docker image build & push qilish
* Secrets (DOCKER\_USERNAME, DOCKER\_PASSWORD) bilan ishlash

**20:00 – 23:00 (Mini Project):**

* TodoList API → CI/CD pipeline:

  * test → build → docker hub’ga push

---

## 🔹 5-Kun: Deployment Asoslari

**17:00 – 18:30 (Nazariya):**

* Deploy turlari: Manual vs Automatic
* VPS/Serverga deploy qilish usullari
* GitHub Action’dan serverga `ssh` orqali ulanib deploy qilish

**18:30 – 20:00 (Amaliyot):**

* VPS yoki local serverda Docker o‘rnatish
* GitHub Action’dan serverga `scp` va `ssh` orqali fayl jo‘natish

**20:00 – 23:00 (Mini Project):**

* TodoList API → GitHub Action orqali avtomatik serverga deploy qilish

---

## 🔹 6-Kun: To‘liq CI/CD + Docker Compose Integration

**17:00 – 18:30 (Nazariya):**

* Real dunyo CI/CD pipeline arxitekturasi
* Production’da Docker Compose bilan ishlash
* Healthcheck va auto-restart policy

**18:30 – 20:00 (Amaliyot):**

* API + DB + Redis ni serverda `docker-compose` bilan ishga tushirish
* GitHub Actions orqali `ssh` qilib, serverda `docker-compose up -d` bajarish

**20:00 – 23:00 (Final Project):**

* TodoList API uchun **to‘liq CI/CD**:

  * Test → Build → Docker Hub Push → Serverga Deploy → Docker Compose restart
* Natija: Commit qilganingda API serverda avtomatik yangilanadi 🔥

---
