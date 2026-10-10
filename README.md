# SayohatUz 2.0 — Turizm Hackathon platformasi

## Muammo
O'zbekistonda mustaqil sayohatni rejalashtirayotgan odamlar manzil, marshrut, taxminiy xarajat va tayyorgarlik ro'yxatini alohida joylardan izlashadi. Ayniqsa budjeti cheklangan talabalar, oilalar va birinchi marta sayohat qiluvchilar uchun bu ko'p vaqt oladi.

## Yechim
**SayohatUz — manzil tanlashdan safarga tayyorgarlikkacha bo'lgan jarayonni bitta interfeysga jamlovchi platforma.**

### Ishlaydigan imkoniyatlar
- 12 ta demo manzil; qidiruv, hudud va tur filtrlari, narx bo'yicha saralash
- Har bir manzil uchun batafsil tavsif, tavsiya etilgan mashg'ulotlar va OpenStreetMap havolasi
- Saqlangan joylar: brauzer xotirasida (localStorage)
- Smart Planner: jo'nash shahri, kunlar, odamlar soni, qiziqish va umumiy budjet asosida marshrut
- Marshrutni nusxalash yoki brauzer orqali chop etish / PDF sifatida saqlash
- Xarajat kalkulyatori: transport, turar joy, ovqat, faoliyat
- Tahrirlanadigan safar chek-listi va bajarilgan ishlar progressi
- FAQ, mobil moslashuv, scroll animatsiyalar, qulay interaktiv dizayn

## Ishga tushirish
1. ZIPni oching.
2. `index.html` faylini brauzerda oching yoki VS Code Live Server bilan ishga tushiring.
3. Internet rasmlar va shriftlar uchun kerak; qolgan asosiy imkoniyatlar statik brauzerda ishlaydi.

## Muhim cheklovlar — hakamlarga ochiq ayting
Bu **ishlaydigan frontend prototipi**, jonli ma'lumotlar bilan ishlaydigan tijoriy platforma emas. Manzil narxlari **taxminiy demo qiymatlar**; marshrut qoidalar asosida tuziladi, AI API emas. Yo'l xarajati planner hisobiga kiritilmagan; kalkulyatorda uni alohida kiritish mumkin. Saytda to'lov, jonli transport jadvali, mehmonxona bronlash yoki autentifikatsiya yo'q. Tasvirlar namuna sifatida ishlatilgan va hammasi haqiqiy manzil fotosi bo'lmasligi mumkin.

## Keyingi rivojlanish
1. Rasmiy turizm va transport ma'lumotlari integratsiyasi
2. Xarita asosidagi aniq yo'nalish va yo'l vaqti hisoblash
3. Tekshirilgan mahalliy gidlar va hamkor xizmatlar
4. Ko'p tillilik, akkaunt va bulutga saqlash
5. Hamkorlardan olinadigan real narxlar va mavjudlik

## Deploy
GitHub Pages: repositoryga `index.html`, `style.css`, `main.js` yuklang, Settings → Pages → Deploy from branch → main/root. Netlify Drop ham ishlaydi.

## 45 soniyalik pitch
“Sayohat qilmoqchi bo'lgan odam ko'pincha uchta savolga javob topolmaydi: qayerga boraman, qancha pul ketadi, qanday reja tuzaman? Ma'lumotlar tarqoq, vaqt esa cheklangan. SayohatUz shu muammoni bitta platformada hal qiladi: foydalanuvchi o'z budjeti, vaqti va qiziqishini kiritadi, mos manzil va kunlik marshrut oladi. Keyin xarajatlarni hisoblaydi, yoqqan joylarni saqlaydi va chek-list bilan safarga tayyorlanadi. Bizning maqsadimiz — mahalliy turizmni ayniqsa yoshlar va oilalar uchun osonroq qilish. Hozir bu funksional prototip, keyingi qadamimiz real transport va narx ma'lumotlarini ulash.”

## 3.0 visual experience update
- Light/dark theme toggle with localStorage persistence and OS theme detection.
- Uzbek, English and Russian interface selector with persistence. Key navigation, hero, discovery and planner labels are localized; some long-form explanatory text and dynamically generated itinerary content remain in Uzbek in this prototype.
- Refreshed editorial styling, destination hover interactions, floating hero badges, animated buttons, stronger depth and scroll effects.
- Respects `prefers-reduced-motion` for accessibility.
- `experience.css` and `experience.js` are loaded after the original files, keeping core functionality intact.

## Version 4 — Animated AI Travel Companion
- New cinematic animated ambient gradients, drifting dot background, hero image zoom, hover lift, shimmering CTA, and floating AI showcase.
- AI Travel Guide opens via the floating launcher or the showcase. It offers suggestions in Uzbek, English and Russian, keeps a short chat history locally, and can prefill the existing Smart Planner's trip style and duration.
- **Important:** This is a rule-based assistant, not a generative AI API. It works offline after initial assets load and does not invent real-time ticket prices or reservations. For a production AI service, connect a backend securely to an LLM API; never put API keys in client-side JavaScript.
- Accessibility: escape-to-close, ARIA labels, reduced-motion handling, mobile layout.
