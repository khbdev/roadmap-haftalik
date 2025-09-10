

## 🔹 Ertaga 9:00–12:00 ish rejasi

### 1️⃣ 9:00 – 9:20 : Tayyorlov

* Loyihalarni tayyorlash: `hello-api` va `todolist` ishlayaptimi tekshirish.
* Docker va Docker Compose o‘rnatilganligini tekshirish (`docker --version`, `docker compose version`).
* Docker Hub’ga login qilish (`docker login`).

### 2️⃣ 9:20 – 10:00 : `hello-api` container qilish va Docker Hub’ga push

* `hello-api` uchun Dockerfile yozish.
* Docker image yaratish: `docker build -t azizbek/hello-api:latest .`
* Image’ni lokalda test qilish: `docker run -p 8080:8080 azizbek/hello-api:latest`
* Docker Hub’ga push qilish: `docker push azizbek/hello-api:latest`

### 3️⃣ 10:00 – 10:40 : Docker Compose yaratish (`hello-api` + Redis + MySQL)

* `docker-compose.yml` yozish, har biri alohida containerda ishlaydi.
* Volumes va network sozlash.
* Compose orqali containerlarni ishga tushirish: `docker compose up -d`
* Containerlarni tekshirish: `docker ps`, `docker logs <container>`

### 4️⃣ 10:40 – 11:40 : `todolist` loyihasini Docker Compose qilish

* `todolist` uchun Dockerfile yaratish (Go yoki PHP/Laravel bo‘lsa mos yozish).
* Docker Compose faylga `todolist` containerini qo‘shish, alohida volume va network bilan.
* Compose orqali ishga tushirish va test qilish (`docker compose up -d`, `docker logs`, `curl` yoki brauzer orqali).

### 5️⃣ 11:40 – 12:00 : Yakuniy tekshiruv va tozalash

* Barcha containerlar ishlayaptimi tekshirish.
* Kerak bo‘lsa container va image’larni tozalash (`docker compose down`, `docker image prune -f`).
* Ishlar reja bo‘yicha tugaganini yozib qo‘yish.

