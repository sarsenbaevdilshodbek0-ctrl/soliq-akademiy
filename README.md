# Soliq Akademiya — sodda online versiya

## Ishga tushirish
Node.js 20+ o‘rnating. Papkada terminal ochib `npm start` buyrug‘ini bajaring. Sayt: http://localhost:3000

## Admin akkaunti
Birinchi ishga tushirishdan oldin `ADMIN_EMAIL` va `ADMIN_PASSWORD` muhit o‘zgaruvchilarini o‘rnating. Parol kamida 10 belgi bo‘lishi kerak. Masalan Linux hostingda:

ADMIN_EMAIL=admin@example.com ADMIN_PASSWORD='uzun-va-maxfiy-parol' npm start

Admin paroli kodga joylanmagan. Admin akkaunt dastlabki ishga tushirishda yaratiladi.

## Internetga joylash
Node.js ishlaydigan hostingga yuklang, start command: `npm start`. Doimiy `DATA_DIR` disk/persistent volume biriktiring; aks holda hosting qayta qurilganda foydalanuvchi va darslar yo‘qolishi mumkin. Bepul statik hosting (Netlify Drop) bu versiya uchun yetarli emas.

## Cheklovlar
* 1-dars bepul, qolgan 14 ta dars va testlar server tekshiruvi bilan obunaga bog‘langan.
* 30 kunlik obuna 10 000 so‘m, 365 kunlik obuna 59 000 so‘m deb ko‘rsatiladi.
* Click/Payme avtomatik to‘lov integratsiyasi YO‘Q. Admin tekshirilgan to‘lovdan keyin obunani qo‘lda faollashtiradi.
* Ma’lumotlar oddiy JSON faylda saqlanadi; katta ommaviy xizmatga chiqishdan oldin PostgreSQL, avtomatik zaxira, rate limiting, CSRF himoyasi, parolni tiklash, to‘lov webhooklari va monitoring zarur.
* Server qayta ishga tushsa foydalanuvchilar qayta login qiladi.
* Rasm yuklash o‘rniga rasmning HTTPS havolasi kiritiladi.
* Mavzular soni hozir 15 ta. Cheksiz talabalar soni kafolatlanmaydi: server resurslari chegaralangan.


## Click / Payme orqali karta o‘tkazmasi
Obuna sahifasida 5614 6887 0970 1154 kartasi va Click/Payme sahifalariga tugmalar mavjud. Bu avtomatik merchant checkout EMAS: foydalanuvchi karta raqamini ko‘chirib, ilovada o‘tkazmani mustaqil amalga oshiradi. Administrator to‘lovni tekshirib, admin panelda obunani faollashtiradi. Haqiqiy bir bosishda to‘lov va avtomatik obuna uchun Click/Payme merchant hisobini ulash, serverda to‘lov yaratish, webhook orqali tasdiqlash va idempotent obuna faollashtirish zarur.

## Admin kirish (yangilangan)
Saytdagi 🔒 Admin tugmasini bosing va admin parolini kiriting. Dastlabki parol: 20080131. Admin email: admin@soliq-akademiya.uz. Serverda ADMIN_PASSWORD va ADMIN_EMAIL muhit o‘zgaruvchilari berilsa, ular ustunlik qiladi. Server qayta ishga tushganda mavjud admin paroli ushbu qiymatga moslanadi. Xavfsizlik uchun Render Environment bo‘limida ADMIN_PASSWORD ni uzunroq maxfiy parolga almashtirish tavsiya etiladi.
