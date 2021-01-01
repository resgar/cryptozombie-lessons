---
title: Arrays
actions: ['checkAnswer', 'hints']
material:
  editor:
    language: sol
    startingCode: |
      pragma solidity ^0.4.25;

      contract ZombieFactory {

          uint dnaDigits = 16;
          uint dnaModulus = 10 ** dnaDigits;

          struct Zombie {
              string name;
              uint dna;
          }

          // start here

      }
    answer: >
      pragma solidity ^0.4.25;


      contract ZombieFactory {

          uint dnaDigits = 16;
          uint dnaModulus = 10 ** dnaDigits;

          struct Zombie {
              string name;
              uint dna;
          }

          Zombie[] public zombies;

      }
---

شما هرگاه مجموعه‌ای از چیزها را می‌خواهید، می‌توانید از یک **_آرایه_** استفاده کنید. در سالیدیتی دو نوع آرایه وجود دارد، آرایه‌های **_ثابت_** و **_داینمیک_**:

```
// Array with a fixed length of 2 elements:
uint[2] fixedArray;

// Another fixed Array, can contain 5 strings:
string[5] stringArray;

// A dynamic Array - has no fixed size, can keep growing:
uint[] dynamicArray;
```

شما همچنین می‌توانید یک آرایه از **_ساختارها_** ایجاد کنید. با استفاده از ساختار `Person` فصل قبلی:

```
Person[] people; // dynamic Array, we can keep adding to it
```

به یاد دارید که متغیرهای حالت به طور پایدار در بلاک‌‌‌چین ذخیره می‌شوند؟ بنابراین ایجاد یک آرایه داینمیک از ساختارها مانند این می تواند برای ذخیره سازی داده‌های ساختارمند در قرارداد شما مفید باشد، به نوعی مانند یک پایگاه داده. 


## آرایه‌‌های عمومی

شما می‌توانید آرایه‌ها را به عنوان `public` تعريف کنید، و سالیدیتی به طور خودکار یک تابع **_گیرنده_** برای آن ايجاد می‌کند. سینتکس به صورت زیر است:

```
Person[] public people;
```

سایر قراردادها می‌توانند این آرایه را بخوانند، اما نمی‌توانند در آن بنویسند. بنابراین این یک الگوی مفید برای ذخیره سازی اطلاعات عمومی در قرارداد شما است.

# آن را امتحان کنید

می‌خواهیم یک ارتش زامبی‌ها را در اپ‌مان ذخیره کنیم، و می‌خواهیم تمام زامبی‌هایمان را برای اپ‌های دیگر به نمایش بگذاریم. بنابراین می‌خواهیم عمومی باشد.


1. یک آرایه عمومی از **_ساختار_** `Zombie` ایجاد کن و نام آن‌را `zombies` بگذار:
