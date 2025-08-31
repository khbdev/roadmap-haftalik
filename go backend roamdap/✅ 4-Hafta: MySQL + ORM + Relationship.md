3-kunlik o‘quv rejasi MySQL, GORM va relationship mavzularini o‘rganish uchun quyidagicha tuziladi. Har bir kun nazariy va amaliy qismlarga bo‘linadi, shunda siz asta-sekin bilimlaringizni mustahkamlaysiz.

---

### 1-kun: SQL asoslari va MySQL bilan ishlash
Maqsad: SQLning asosiy buyruqlarini o‘rganish, MySQL bilan ulanish va GORM bilan tanishish.

#### Nazariy qism (2-3 soat):
1. SQL asoslari:
   - SELECT: Ma’lumotlarni olish (WHERE, ORDER BY, LIMIT).
   - INSERT: Yangi ma’lumot qo‘shish.
   - UPDATE: Ma’lumotlarni yangilash.
   - DELETE: Ma’lumotlarni o‘chirish.
2. MySQL bilan ishlash:
   - MySQL o‘rnatish va sozlash.
   - Database va table yaratish.
   - MySQL Workbench yoki boshqa GUI bilan tanishish.
3. Go bilan MySQL:
   - database/sql paketi va gorm.io/gorm bilan ulanish.
   - GORM o‘rnatish va dastlabki sozlash.
4. SQL Injectiondan himoyalanish:
   - Prepared statements va parameterized queries.
   - GORM’da xavfsiz so‘rovlar yozish.

#### Amaliy qism (2-3 soat):
1. MySQL’da oddiy table yaratish:
   - users table (id, name, email, created_at).
   - posts table (id, user_id, title, content, created_at).
2. GORM bilan ulanish:
   - Go’da MySQL’ga ulanish va oddiy SELECT so‘rovini yozish.
   - users table’ga yangi foydalanuvchi qo‘shish (INSERT).
3. Amaliyot:
   - Foydalanuvchi ro‘yxatini chiqarish (SELECT * FROM users).
   - Ma’lum bir foydalanuvchini yangilash (UPDATE) va o‘chirish (DELETE).
   - SQL injectionga misol yozib, GORM’da xavfsiz usulni sinab ko‘rish.

Natija: SQL asosiy buyruqlari va GORM bilan ishlashni tushunasiz. Oddiy CRUD operatsiyalarni MySQL’da bajarishni o‘rganasiz.

---
	
### 2-kun: Relationship va JOIN
Maqsad: One-to-One, One-to-Many, Many-to-Many munosabatlarni tushunish va JOIN bilan ishlash.

#### Nazariy qism (2-3 soat):
1. Relationship turlari:
   - One-to-One: Har bir userning bitta profili bo‘lishi.
   - One-to-Many: Bir userning bir nechta posti bo‘lishi.
   - Many-to-Many: Postlar va tag’lar o‘rtasidagi munosabat.
2. Foreign Key:
   - Foreign key nima va qanday ishlatiladi.
   - Table’lar o‘rtasida munosabat o‘rnatish.
3. JOIN turlari:
   - INNER JOIN, LEFT JOIN, RIGHT JOIN.
   - JOIN yordamida bog‘langan ma’lumotlarni olish.
4. GORM’da relationship:
   - Has One, Has Many, Many to Many sozlamalari.
   - GORM’da Preload va Joins bilan ishlash.
5. Migration:
   - GORM’da avtomatik migration qilish.
   - Table tuzilmasini yangilash.

#### Amaliy qism (2-3 soat):
1. Table’lar yaratish:
   - posts table’ga user_id foreign key qo‘shish.
   - tags va post_tags (M:M uchun) table’larini yaratish.
2. GORM’da relationship o‘rnatish:
   - User va Post uchun One-to-Many munosabat.
   - Post va Tag uchun Many-to-Many munosabat.
3. JOIN bilan so‘rovlar:
   - User va uning postlarini INNER JOIN orqali olish.
   - GORM’da Preload bilan bog‘langan ma’lumotlarni olish.
4. Migration:
   - GORM yordamida users, posts, tags, post_tags table’larini avtomatik yaratish.

Natija: Relationship turlari va JOIN’ni tushunasiz. GORM’da munosabatlarni sozlash va migration qilishni o‘rganasiz.

---

### 3-kun: CRUD va kompleks amaliyot
Maqsad: User, Post, Comment va Tag bilan to‘liq CRUD amaliyotini bajarish, real loyiha sifatida.

#### Nazariy qism (1-2 soat):
1. Kompleks so‘rovlar:
   - GORM’da murakkab so‘rovlar (Where, Joins, Group By).
   - Paginated so‘rovlar yozish.
2. Xavfsizlik va optimallashtirish:
   - SQL injectiondan himoya (takrorlash).
   - Index qo‘shish va so‘rovlar optimallashtirish.
3. REST API bilan integratsiya:
   - GORM’dan olingan ma’lumotlarni REST API orqali chiqarish.
   - JSON formatida ma’lumotlarni qaytarish.
#### Amaliy qism (3-4 soat):
bitta qib aytgan tudolis qilamiz
shu yerddagi va boshqa organgan bilimlarni ishga solish 1-avgustgacha

Natija: To‘liq ishlaydigan CRUD tizimi va REST API qurasiz. GORM’da murakkab so‘rovlar va xavfsiz ma’lumotlar bilan ishlashni o‘rganasiz.
