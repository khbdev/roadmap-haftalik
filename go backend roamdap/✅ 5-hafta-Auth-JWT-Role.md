
---

## ✅ **5-Hafta: Auth + JWT + Role-Based Access (2 kunlik reja)**

🕒 **Umumiy vaqt/kun:** 8 soat x 2 kun = 16 soat
🎯 **Maqsad:**

* JWT asoslarini tushunish
* Go’da `github.com/golang-jwt/jwt` bilan token yaratish
* Access va refresh tokenlarni qo‘llash
* Middleware orqali tokenni tekshirish
* Role-based ruxsat (admin/user) implementatsiya qilish
* Real amaliy API yozish (Auth + Blog CRUD)

---

### 📅 **1-KUN (10:00 – 18:00): JWT asoslari + Auth API**

| Vaqt        | Bo‘lim               | Tavsif |
| ----------- | -------------------- | ------ |
| 10:00–11:30 | 🎓 **Nazariya: JWT** |        |

* JWT nima? Qanday ishlaydi?
* `Header.Payload.Signature` tuzilmasi
* Base64 encoding, HMAC-SHA256
* `Access` vs `Refresh` token
* JWT ni frontend va backend qanday ishlatadi
  📚 Manba: jwt.io, [golang-jwt/jwt](https://github.com/golang-jwt/jwt)

\| 11:30–13:00 | 🛠 **JWT bilan register/login API yozish** |

* `POST /register` — userni DBga yozish
* `POST /login` — token generatsiya qilish
* JWT kutubxonasi bilan `access` token yaratish
* `.env` dan JWT\_SECRET o‘qish
  ✅ Amaliyot: `auth/handler.go`, `auth/usecase.go`, `auth/model.go` yoz

\| 13:00–14:00 | 🍽 **Tushlik tanaffusi** |

\| 14:00–15:30 | 🔁 **Refresh token implementatsiyasi** |

* Access token: 15 daqiqa
* Refresh token: 7 kun
* `POST /refresh` endpoint
* Refresh tokenni DBda saqlash yoki memory (`map[uuid]token`)
  ✅ Amaliyot: `refresh_token.go` qo‘sh

\|	 15:30–17:00 | 🧪 **Middleware: JWT ni tekshirish** |

* Tokenni `Authorization: Bearer token` dan olish
* JWT parsing va validation
* UserID ni kontekstga o‘tkazish
  ✅ Amaliyot: `middleware/auth.go` yoz

\| 17:00–18:00 | 🔎 **Testing va Postman orqali tekshirish** |

* Register → Login → JWT bilan protected route chaqirish
* Refresh token ishlayaptimi tekshirish
  📌 **Homework**: Blog modeli ustida o‘yla (title, content, owner\_id)

---

### 📅 **2-KUN (10:00 – 18:00): Role-based access + Blog API**
	
| Vaqt        | Bo‘lim                              | Tavsif |
| ----------- | ----------------------------------- | ------ |
| 10:00–11:00 | 🧠 **Role-based nazariya + design** |        |

* Nima uchun kerak?
* DBda `role` (user, admin) ustuni
* Middleware orqali tekshirish: `IsAdmin()`
  ✅ Model: `User{ ID, Name, Email, Password, Role string }`

\| 11:00–13:00 | 🔐 **Role middleware yozish** |

* Faqat `admin` kirsin: `/admin/*`
* `CheckRole(ctx, "admin")`
  ✅ Amaliyot: `middleware/role.go` yoz
  🔄 Protected route: `/admin/users` - userlar ro‘yxati faqat admin ko‘rsin

\| 13:00–14:00 | 🍽 **Tushlik tanaffusi** |

\| 14:00–16:00 | 📝 **Blog CRUD API yaratish (JWT protected)** |

* `GET /blogs` – hammaga ochiq
* `POST /blogs` – faqat tokenli user
* `PUT/DELETE /blogs/:id` – faqat post egasi yoki admin
  ✅ Amaliyot: `blog/handler.go`, `blog/usecase.go`, `blog/model.go`

\| 16:00–17:00 | 🔒 **Ownership va role accessni birlashtirish** |

* Blogni faqat egasi tahrir/qilsin yoki admin
* `CheckOwnerOrAdmin(ctx, blog.OwnerID)`
  ✅ Amaliyot: `middleware/permission.go`

\| 17:00–18:00 | 🧪 **Yakuni: test + review + Postman** |

* Register -> Login -> JWT -> Blog CRUD
* Admin login -> ko‘rish → userlar list
  📌 Yakuniy tekshiruv checklist:

  * [ ] JWT to‘g‘ri ishlayaptimi?
  * [ ] Token muddati?
  * [ ] Refresh token?
  * [ ] Role ishlayaptimi?
  * [ ] Middlewarelar to‘g‘ri ketayaptimi?

---

## 🧱 Bonus: Papka Strukturasi (Clean-ish)

```
/internal
  /auth
    handler.go
    usecase.go
    model.go
  /blog
    handler.go
    usecase.go
    model.go
  /middleware
    auth.go
    role.go
    permission.go
  /config
    env.go
  /repository
    mysql.go
main.go
.env
```


---

## ❗ Tavsiyalar:

* JWT tokenni `short-lived` qil (15 min)
* Refresh tokenni alohida saqla (`uuid` bilan)
* Role’ni string emas, enum/int sifatida yozsang, validatsiya osonroq bo‘ladi
* Middleware’larni har doim log bilan yoz, qaysi user, qaysi ruxsat

---


