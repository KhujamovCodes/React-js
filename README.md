# React Nima?

**React** — bu *JavaScript* kutubxonasi bo'lib, foydalanuvchi interfeyslarini (UI) yaratish uchun ishlatiladi. U **Facebook** tomonidan ishlab chiqilgan va hozirda keng qo'llaniladi. React asosan veb ilovalarda modulli va qayta foydalanishga yaroqli UI komponentlarini yaratishga yordam beradi.

## React-ning Asosiy Xususiyatlari:
- **Komponentlar:** React ilovalarini kichik, mustaqil komponentlarga bo'lish imkonini beradi.
- **Virtual DOM:** React-da Virtual DOM texnologiyasi yordamida o'zgarishlar samarali tarzda qo'llaniladi, bu esa ilova tezligini oshiradi.
- **Bir yo'nalishli ma'lumot oqimi:** React-da ma'lumotlar bir yo'nalishda oqadi, bu esa dastur loģikasini soddalashtiradi.

## React bilan Ishlash:
- **JSX:** HTML va JavaScript-ni birlashtiruvchi sintaksis bo'lib, komponentlarni yozish uchun ishlatiladi.
- **State va Props:** Komponentlar o'rtasida ma'lumot almashish va ichki holatlarni boshqarish uchun ishlatiladi.
- **React Hooks:** Funksional komponentlarda state va boshqa React xususiyatlaridan foydalanishga imkon beradi.

React dasturchilarga zamonaviy, dinamik va murakkab foydalanuvchi interfeyslarini yaratishda katta yordam beradi.

# JSX (JavaScript XML) Haqida

JSX (JavaScript XML) — bu React'da ishlatiladigan sintaksis kengaytmasi bo‘lib, JavaScript kodida HTML-ga o‘xshash sintaksisda UI komponentlarini yaratishga imkon beradi. JSX oddiy JavaScript emas, ammo React bu kodni shaxsiy `createElement` funksiyasiga kompilyatsiya qiladi.

## JSXning Afzalliklari

### 1. **Tushunarli sintaksis**
   JSX yordamida UI komponentlarini yozish ancha sodda va tushunarli bo‘ladi, chunki u HTML-ga o‘xshash ko‘rinishda. Bu esa ishlab chiquvchilar uchun kodni o‘qish va tushunishni osonlashtiradi.

### 2. **JSXda ifodalar**
   JSX ichida JavaScript ifodalaridan foydalanish mumkin. Bu imkoniyat orqali dinamik tarkib yaratish osonlashadi.

       const name = "Dunyo";
       const element = <h1>Salom, {name}!</h1>;


# `useState` Nima?

**`useState`** — bu React'dagi *hook* bo'lib, funksional komponentlarda state (holat) boshqarish uchun ishlatiladi. `useState` yordamida komponentning ichki holatini belgilash va keyinchalik o'zgartirish mumkin.

## `useState` Hook'ining Ishlatilishi

Quyida `useState` qanday ishlatilishini ko'rsatadigan oddiy misol keltirilgan:

    
      import React, { useState } from 'react';
      
      function Counter() {
        // useState hook bilan count o'zgaruvchisini va uni o'zgartiruvchi setCount funksiyasini yaratamiz
        const [count, setCount] = useState(0);
      
        return (
          <div>
            <p>Siz {count} marta bosdingiz</p>
            <button onClick={() => setCount(count + 1)}>
              Bosish
            </button>
          </div>
        );
      }
      
      export default Counter;

# `useEffect` Haqida

`useEffect` — bu React kutubxonasining asosiy `hook`laridan biri bo‘lib, komponentning yanada murakkab holatlarida yon ta’sirlarni (side effects) boshqarish uchun ishlatiladi. Yon ta’sirlar — bu komponentning render jarayonidan tashqaridagi funksiyalar, masalan, brauzerdan ma’lumotlarni olish, tashqi API ga murojaat qilish, vaqt o‘tkazgichlar (`timers`) yoki subskribtsiyalarni sozlash va ularni tozalash.

### 1. `useEffect`ning Asosiy Ishlatilishi

```javascript
import React, { useEffect } from 'react';

function MyComponent() {
  useEffect(() => {
    // Bu yerda yon ta’sirlarni amalga oshirish mumkin
    console.log('Komponent render qilindi yoki yangilandi.');

    // Bu yerda tozalash funksiyasini qaytarish mumkin
    return () => {
      console.log('Komponent tozalanmoqda.');
    };
  }, []);

  return (
    <div>
      <p>Salom, bu mening komponentim!</p>
    </div>
  );
}
