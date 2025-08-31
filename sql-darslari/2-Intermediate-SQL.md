

## 📅 1-kun: `JOIN` va `Aggregate Functions`

### 🔹 Nazariya

1. **JOIN turlari**

   * `INNER JOIN` → faqat mos kelgan qatorlarni oladi
   * `LEFT JOIN` → chap table’ning hammasi + o‘ng tarafdagi mos kelganlari
   * `RIGHT JOIN` → o‘ng table’ning hammasi + chap tarafdagi mos kelganlari
   * `FULL JOIN` → ikkala table’dan hamma qator (mos bo‘lmagan joyda `NULL`)

2. **Aggregation functions**

   * `COUNT()`, `SUM()`, `AVG()`, `MAX()`, `MIN()`
   * `GROUP BY` bilan ishlatish
   * `HAVING` (filterlash uchun `WHERE` o‘rniga agg funksiyalarda ishlatiladi)

---

### 🔹 Amaliyot (ecommerce schema’da)

* `users(id, name, email)`
* `orders(id, user_id, product_id, quantity, total_price)`
* `products(id, name, price)`
* `payments(id, order_id, amount, status)`

**Mashqlar:**

1. Har bir userning qilgan buyurtmalari sonini chiqar (`COUNT`).
2. Har bir product qancha marta sotilgan (`SUM(quantity)`).
3. Eng ko‘p buyurtma qilgan userni top (`MAX`).
4. `INNER JOIN` orqali orderlar bilan userlarni ko‘rsat.
5. `LEFT JOIN` bilan hamma userlarni va ularning buyurtmalarini ko‘rsat.
6. `HAVING` bilan — faqat 5 tadan ko‘p order qilgan userlarni ko‘rsat.

---

## 📅 2-kun: Subquery, Advanced Operators, Index

### 🔹 Nazariya

1. **Subquery**

   * `SELECT` ichida `SELECT`
   * `WHERE` shartida subquery (`IN`, `EXISTS`)
   * `FROM` ichida subquery (derived table)

2. **Advanced operatorlar**

   * `DISTINCT`
   * `CASE` (if-else kabi shartli qiymat)
   * `COALESCE` (NULL bo‘lsa default qiymat)
   * `NULLIF` (ikki qiymat teng bo‘lsa `NULL`)
   * `UNION`, `INTERSECT`, `EXCEPT`

3. **Index asoslari**

   * Index nima? (qidiruvni tezlashtiradi)
   * Qachon kerak? (`WHERE`, `JOIN`, `ORDER BY` ustunlarida)
   * Kamchiliklari (ko‘p joy egallaydi, `INSERT`/`UPDATE` sekinlashishi mumkin)

---

### 🔹 Amaliyot

1. Subquery:

   * Eng qimmat productni sotib olgan userlarni chiqar.
   * O‘rtacha narxdan qimmat orderlarni chiqar.

2. `CASE`:

   * Payments’ni `status` bo‘yicha (`paid`, `pending`, `failed`) deb chiqar.

3. `COALESCE`:

   * Userning `username` NULL bo‘lsa, emailini ko‘rsat.

4. `UNION`, `INTERSECT`, `EXCEPT`:

   * `paid` va `pending` userlarni solishtirish.

5. Index:

   * `users.email` ustuniga index qo‘yish misoli.

---

## 🎯 Mini-proyekt mashqi

* **Ma’lumot olish**:

  * “Top 3 users with highest spending”
  * “Which product brings the most revenue?”
  * “How many orders were not paid?”
  * “Users who never made an order”

---

