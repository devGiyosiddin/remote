Redux - bu katta loyihalarda state (holat)larni saqlash va boshqarishda keng qo'llaniladigan texnologiya bo'lib uni xuddi хранилище deb qabul qilsak ham bo'ladi.
![[remote/Programming/Technologies/Redux/assets/image.png]]
mana rasmda redux nega kerakligi aniq ko'rsatib o'tilgan

![[remote/Programming/Technologies/Redux/assets/image-1.png]]
Bu rasimda Reduxni tushunish uchun bank asnosida ko'rib chiqamiz. Biz mijozmiz va pul (state)imizni bankda saqlaymiz. Bizda pul qo'shish yoki olish xohishimiz bor, bular **<font color="#ff0000">actions</font>** deyiladi. biz to'g'ridan to'g'ri bankga bora olmaymiz balki bank hodimiga murojaat qilamiz. Bank hodimi bu **<font color="#f79646">Dispatch</font>** (dispetcher). Va u xohishlarimiz( actions) yozilgan qog'ozlarni olib kompyuteriga kiritadi. Bu yerda kompyuter **<font color="#8db3e2">Reducer</font>** bo'lib u bankdan pul olish yoki qo'shish uchun xizmat qiladi.