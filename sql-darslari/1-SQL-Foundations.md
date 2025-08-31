
---

# 📅 **2-Kunlik SQL Reja (Har kuni 2 soat)**

---

## **1-kun: SQL asoslari va CRUD**

⏱️ 2 soat

### 🎯 Maqsad: SQL asoslarini tushunish va CRUD komandalarini ishlatish

1. **Nazariya (30 daqiqa):**

   * SQL nima? RDBMS nima?
   * Table, Row, Column tushunchalari
   * SQL vs NoSQL farqi (strukturaviy vs hujjatli ma’lumotlar)

2. **Amaliyot (90 daqiqa):** 

   * SQLite yoki MySQL o‘rnatish / ishlatish (SQLite osonroq)

   * `students` jadvali yaratish:

     ```sql
     CREATE TABLE students (
         id INTEGER PRIMARY KEY AUTOINCREMENT,
         name VARCHAR(50),
         age INT,
         email VARCHAR(100)
     );
     ```

   * `INSERT` bilan 3–4 ta student qo‘shish

   * `SELECT` bilan chiqarish

   * `UPDATE` bilan 1 ta student emailini yangilash

   * `DELETE` bilan 1 ta studentni o‘chirish

👉 Shu kuni oxirida sen **CRUD**ni ishlata oladigan bo‘lasan.

---

## **2-kun: SELECT operatori va shartlar**

⏱️ 2 soat

### 🎯 Maqsad: SELECT bilan murakkabroq query yozishni o‘rganish

1. **Nazariya (30 daqiqa):**

   * `WHERE` shartlari: `=`, `<`, `>`, `<=`, `>=`, `<>`
   * `AND`, `OR`, `BETWEEN`, `IN`, `IS NULL`
   * `ORDER BY`, `LIMIT`, `OFFSET`

2. **Amaliyot (90 daqiqa):**

   * `courses` jadvali yaratish:

     ```sql
     CREATE TABLE courses (
         id INTEGER PRIMARY KEY AUTOINCREMENT,
         title VARCHAR(100),
         credits INT
     );
     ```

   * `enrollments` jadvali yaratish (student va course’ni bog‘lash uchun):

     ```sql
     CREATE TABLE enrollments (
         id INTEGER PRIMARY KEY AUTOINCREMENT,
         student_id INT,
         course_id INT
     );
     ```

   * Bir nechta kurs qo‘shish (`INSERT`)

   * Studentlarni kurslarga yozish (`INSERT INTO enrollments`)

   * `SELECT` bilan mashqlar:

     * 18 yoshdan katta studentlarni chiqarish
     * 3–5 kredit oralig‘idagi kurslarni chiqarish (`BETWEEN`)
     * Studentlar ro‘yxatini `ORDER BY age DESC` tartibida chiqarish
     * Faqat 2 ta studentni chiqarish (`LIMIT`)
     * 3-chi studentdan boshlab chiqarish (`OFFSET`)
     * `IN` bilan ma’lum ID’li studentlarni tanlash
     * `IS NULL` bo‘lgan ma’lumotlarni tekshirish

👉 Shu kuni oxirida sen **SELECT bilan shartli query yozishni** va ma’lumotlarni **tartiblash/cheklashni** bilib olasan.

