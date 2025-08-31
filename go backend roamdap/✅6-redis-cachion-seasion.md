
## ✅ 1-Kun: Redis + Caching

**Nazariya (2 soat)**

* Redis nima, qachon ishlatiladi
* Redis CLI komandalarini ko‘rish (`SET`, `GET`, `EXPIRE`, `TTL` va h.k.)
* Go’da `go-redis` bilan bog‘lanish, oddiy ma’lumot yozish/olish

**Amaliy mashq (3 soat)**

* JSON obyekt Redis’da saqlash
* Caching patternlar:

  * Read-through cache (DB → Redis → Response)
  * Write-through cache (DB + Redis birga update)

**Mini loyiha (3 soat)**

* `products` jadvali
* API endpoint: `/products/:id`

  * Birinchi marta DB’dan o‘qish
  * Redis’da saqlash
  * Keyingi chaqiruvlarda Redis’dan olish
* TTL qo‘shish

---

## ✅ 2-Kun: Session + Rate Limiting

**Nazariya (2 soat)**

* Session tushunchasi (cookie vs server-side storage)
* Redis’da session saqlash (TTL bilan)
* Rate limiting (fixed window, token bucket nazariyasi)

**Amaliy mashq (3 soat)**

* Session-based login:

  * `/login` → Redis’da session yaratish
  * `/me` → session orqali userni aniqlash
  * `/logout` → session o‘chirish

**Mini loyiha (3 soat)**

* Session-based auth + product cachingni birlashtirish
* Rate limiting qo‘shish: 1 user → 1 daqiqada max 5 request
* Postman orqali sinab chiqish

---


