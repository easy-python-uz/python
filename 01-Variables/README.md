# 🧠 Variables (O'zgaruvchilar)

## 🗂️ O'zgaruvchining ta'rifi
**O'zgaruvchi** — bu ma’lumotlarni vaqtincha saqlash uchun ishlatiladigan nomlangan konteyner. Ular yordamida ma’lumotlar bilan ishlash, ularni saqlash va qayta ishlatish qulaylashadi.

📌 **Masalan:**
```python
x = 5
name = "Alice"
```

![O'zgaruvchi tasviri](images/image.png)

---

## 🛠️ O'zgaruvchi yaratish (Creating Variables)

Python tilida o‘zgaruvchi yaratish uchun maxsus `keyword` yo‘q. O‘zgaruvchi unga **birinchi marta qiymat berilganda** yaratiladi:

```python
x = 5         # int (butun son)
y = 3.14      # float (o'nlik son)
name = "Alice"  # str (string)
is_active = True  # bool (mantiqiy qiymat)

print(x)
print(y)
print(name)
print(is_active)
```

> 🔄 O'zgaruvchilar qiymati istalgan payt o'zgartirilishi mumkin:

```python
x = 5
x = "Hello world"
print(x)  # Hello world
```

---

## 🔁 Type Casting (Ma'lumot turini o'zgartirish)

Ma’lumot turini biridan boshqasiga o‘tkazish uchun `str()`, `int()`, `float()` funksiyalaridan foydalanamiz:

```python
x = str(3)    # '3' (string)
y = int(3)    # 3 (butun son)
z = float(3)  # 3.0 (o'nlik son)
```

---

## 🔍 Ma'lumot turi qanday aniqlanadi?

`type()` funksiyasi yordamida o‘zgaruvchining ma’lumot turini aniqlash mumkin:

```python
x = 5
y = "John"

print(type(x))  # <class 'int'>
print(type(y))  # <class 'str'>
```

---

## 🧾 Single va Double Quotes farqi

Stringlar (`matn`) yozishda `''` yoki `""` ishlatish mumkin – ular bir xil ishlaydi:

```python
name = 'John'
name = "John"
```

🔸 Ba'zi holatlarda **bittasini tanlash qulayroq bo'ladi**:

```python
message = 'He said, "Python is awesome!"'
print(message)

message = "It's a beautiful day!"
print(message)
```

---

## 📜 Triple Quotes (Ko‘p qatorli matnlar uchun)

Agar string ko‘p qatorli bo‘lsa, uchlik qo‘shtirnoq (`'''` yoki `"""`) ishlatiladi:

```python
text = """This is a
multiline string."""
print(text)

text = '''This is also a
multiline string.'''
print(text)
```

---

## ⚠️ Katta-kichik harflarga sezuvchanlik (Case-sensitive)

Python dasturlash tili `case-sensitive`, ya'ni:

```python
a = 4
A = "Sally"

print(a)  # 4
print(A)  # Sally
```

> `a` va `A` bu yerda **ikkita turli o‘zgaruvchi** hisoblanadi.

# 🧠 Variable Names (O'zgaruvchi Nomlari)

## 📜 Qoidalarga muvofiq nomlash

O'zgaruvchilarga nom berishda quyidagi qoidalarga amal qiling:

> ⚠️ **E'tibor bering**:
> - O'zgaruvchi nomi **harf yoki pastki chiziq (`_`)** bilan boshlanishi kerak.
> - O'zgaruvchi nomi **raqam bilan boshlanishi mumkin emas.**
> - Nomda faqatgina **lotin alifbosi harflari (`A-z`), raqamlar (`0-9`) va pastki chiziq (`_`)** qatnashishi mumkin.
> - O'zgaruvchi nomida **bo'shliq (`пробел`)** bo'lishi mumkin emas.
> - Python tilida katta va kichik harflar **farqli** hisoblanadi:
>   - `ism`, `ISM`, va `Ism` uchta turli o'zgaruvchi sifatida qabul qilinadi.

📌 **Noto'g'ri misollar**:
```python
2myvar = "John"  # Raqam bilan boshlanishi mumkin emas
my-var = "John"  # Chiziqcha (-) ishlatish mumkin emas
my var = "John"  # Bo'shliq bo'lishi mumkin emas
```

---

## 🛠️ Qo'shimcha qoidalar
- O'zgaruvchi nomini **kichik harflar bilan** yozish tavsiya etiladi.
- Agar o'zgaruvchi nomida bir nechta so'z qatnashsa, ular orasini **pastki chiziq (`_`)** bilan ajrating:
  ```python
  ism_familiya = "Umid G'aybullayev"
  ```
- O'zgaruvchiga **tushunarli va ma'noli nom** bering:
  - `y=20` emas, balki `yosh=20` deb nomlang.
  - `d="Korea"` emas, balki `davlat="Korea"` deb nomlang.
- Pythonning maxsus **kalit so'zlari (keywords)** dan o'zgaruvchi nomi sifatida foydalanmang.

📌 **To'g'ri misollar**:
```python
myvar = "John"
my_var = "John"
_my_var = "John"
myVar = "John"
MYVAR = "John"
myvar2 = "John"
```

Kalit so'zlar ro'yxatini ko'rish uchun quyidagi koddan foydalaning:
```python
import keyword
print(keyword.kwlist)
```

---

## 🏷️ Nomlash uslublari (Naming Conventions)

Python dasturlash tilida o'zgaruvchilarni nomlashda bir nechta uslublardan foydalaniladi. Quyida ularning izohi va misollari keltirilgan:

### 🐪 Camel Case
So‘zlarning birinchi harfi kichik, ikkinchi va undan keyingi so‘zlarning birinchi harfi katta bo‘ladi.

📌 **Misol**:
```python
myVariableName = "John"
```

---

### 🏛️ Pascal Case
Har bir so‘zning birinchi harfi katta bo‘ladi.

📌 **Misol**:
```python
MyVariableName = "John"
```

---

### 🐍 Snake Case
So‘zlar kichik harflar bilan yoziladi va ular orasida pastki chiziq (`_`) ishlatiladi.

📌 **Misol**:
```python
my_variable_name = "John"
```

---

## 🔑 Kalit So'zlardan Foydalanish

Python tilida **kalit so‘zlar** (keywords) maxsus vazifalarni bajarish uchun ishlatiladi. Ushbu so‘zlardan o‘zgaruvchi nomi sifatida foydalanish **mumkin emas**.

📋 **Kalit so‘zlar ro'yxatini olish uchun**:
```python
import keyword
print(keyword.kwlist)
```

📌 **Misol**:
```python
class = "data"  # Xatolik! "class" kalit so'z hisoblanadi
```

---

## 📌 Yaxshi Amaliyotlar

O‘zgaruvchilarni nomlashda quyidagi amaliyotlar tavsiya etiladi:
1. O‘zgaruvchining **mazmunini bildiruvchi nomlar** tanlang:
   ```python
   x = 25  # Notushunarli
   yosh = 25  # Tushunarli
   ```
2. Foydalanuvchiga qulay va o‘qilishi oson bo‘lgan nomlardan foydalaning.
3. Katta loyihalarda **snake_case** uslubini qo‘llash afzalroq bo‘lishi mumkin.
4. Agar vaqtinchalik o‘zgaruvchi yaratayotgan bo‘lsangiz, ehtiyot bo‘ling va umumiy nomlardan foydalanmang:
   ```python
   data = "Ma'lumot"  # Umumiy nom
   user_data = "Ma'lumot"  # Tushunarli nom
   ```

---

## 🧪 Qo'shimcha Misollar
Quyida turli uslublar va qo'llanilishiga oid misollar keltirilgan:

```python
# Camel Case
userName = "Umid"

# Pascal Case
UserName = "Umid"

# Snake Case
user_name = "Umid"

# Noto'g'ri nomlash
2user = "Umid"  # Xatolik
user-name = "Umid"  # Xatolik
user name = "Umid"  # Xatolik
```


# 🧠 Assigning Multiple Values (Bir nechta qiymatlarni tayinlash)

Python dasturlash tilida bir nechta qiymatlarni bir vaqtning o‘zida bir nechta o‘zgaruvchilarga tayinlash mumkin. Quyida bu boradagi turli usullar keltirilgan.

---

## 🛠️ Bir xil qiymatni o'zgaruvchilarga berish (Assigning the Same Value)

Bir nechta o‘zgaruvchilarga **bir xil qiymatni** saqlash uchun quyidagi usuldan foydalanamiz:

📌 **Misol**:
```python
a = b = c = 100
print(a, b, c)
```

📋 **Natija**:
```
100 100 100
```

> 🔔 **Izoh**: Bu usul bir xil qiymatni bir nechta o‘zgaruvchilarga saqlash uchun juda qulay. Lekin, agar qiymat o‘zgaruvchi turiga qarab murakkab obyekt bo‘lsa (masalan, ro‘yxat), ehtiyot bo‘lish lozim. Chunki barcha o‘zgaruvchilar bitta obyektni ko‘rsatadi.

---

## 🛠️ Har xil qiymatlarni o'zgaruvchilarga berish (Assigning Different Values)

Bir nechta o‘zgaruvchilarga **har xil qiymatlarni** bitta qatorda tayinlash mumkin:

📌 **Misol**:
```python
a, b, c = 20, 2.5, "Python"
print(a)
print(b)
print(c)
```

📋 **Natija**:
```
20
2.5
Python
```

> 🔔 **Izoh**: O‘zgaruvchilar va qiymatlar soni bir xil bo‘lishi shart. Aks holda **ValueError** xatosi yuzaga keladi:
```python
a, b = 10, 20, 30  # ValueError: too many values to unpack
```

---

## 🛠️ Matnni kesib olish (Using String Slicing)

Matnni indekslar orqali **kesib olib**, bir nechta o‘zgaruvchilarga tayinlash mumkin:

📌 **Misol**:
```python
text = "Easy Python"
a, b = text[0:5], text[5:]
print(a)
print(b)
```

📋 **Natija**:
```
Easy 
Python
```

> 🔔 **Izoh**: Python indekslashda **0-indeksdan boshlab** hisoblaydi. `text[0:5]` 0-indeksdan 4-indeksgacha bo‘lgan belgilarni oladi, 5-indeksni esa kiritmaydi.

---

## 🛠️ `*` operatori bilan qiymatlarni ajratish (Using * for Arbitrary Values)

`*` operatori yordamida bir nechta qiymatni bitta o‘zgaruvchiga saqlash imkoniyati mavjud. Bu operator qolgan barcha qiymatlarni o‘zida jamlaydi:

📌 **Misol**:
```python
numbers = (10, 20, 30, 40, 50)
x, *y, z = numbers
print(x)
print(y)
print(z)
```

📋 **Natija**:
```
10
[20, 30, 40]
50
```

> 🔔 **Izoh**: `*y` barcha **oraliq qiymatlarni** oladi va ularni ro‘yxat (`list`) sifatida saqlaydi. Bu usul yordamida qiymatlarni tartib bilan ajratish qulay.

---

## 🧪 Qo‘shimcha Misollar

### 1. Dinamik qiymat tayinlash
O‘zgaruvchilarga qiymatlarni dinamik ravishda tayinlash uchun quyidagicha kod yozish mumkin:
```python
values = [1, 2, 3]
a, b, c = values
print(a, b, c)
```

📋 **Natija**:
```
1 2 3
```

### 2. Qolgan qiymatlarni bitta o‘zgaruvchiga saqlash
`*` operatori yordamida qolgan barcha qiymatlarni birlashtirish mumkin:
```python
names = ["Alice", "Bob", "Charlie", "David"]
first, *middle, last = names
print(first)   # Alice
print(middle)  # ['Bob', 'Charlie']
print(last)    # David
```

---

## 🏷️ Amaliyot uchun mashqlar

1. Quyidagi kodni to‘ldiring va xatolikni tuzating:
```python
x, *y = 10, 20, 30, 40
print(x)
print(y)
```

2. Quyidagi kod qanday natija beradi? O‘ylab ko‘ring va tekshiring:
```python
fruits = ("apple", "banana", "cherry", "date")
a, b, *c = fruits
print(a, b, c)
```

3. O‘zgaruvchi qiymatlarini almashish uchun quyidagi kodni yozing:
```python
x = 5
y = 10

# qiymatlarni almashish
x, y = y, x

print(x, y)
```

---

🎯 Ushbu usullar Python dasturlash tilida ko‘p hollarda qulay va samarali dastur yozish imkonini beradi.


# 🧠 Output Variables (O‘zgaruvchilarni chiqarish)

**Output variables** deganda, o‘zgaruvchilarga berilgan qiymatlarni terminalga chiqarish tushuniladi. Python tilida bu maqsadda eng ko‘p ishlatiladigan metod `print()` funksiyasi hisoblanadi. Quyida o‘zgaruvchilarni chiqarishning turli usullari va ularning afzalliklari keltirilgan.

---

## 🛠️ `print()` funksiyasidan foydalanish

O‘zgaruvchining qiymatini chiqarishning eng oddiy usuli — uni `print()` funksiyasiga uzatish.

📌 **Misol**:
```python
x = "Easy Python"
print(x)
```

📋 **Natija**:
```
Easy Python
```

> 🔔 **Izoh**: `print()` funksiyasi matnni va o‘zgaruvchilarning qiymatini ekranga chiqaradi.

---

## 🛠️ Bir nechta o‘zgaruvchini `print()` yordamida chiqarish

Bir nechta o‘zgaruvchini bitta `print()` funksiyasi yordamida chiqarish uchun, ularni vergul bilan ajratib yozish kerak. Python avtomatik ularning orasiga bo‘shliq qo‘yadi.

📌 **Misol**:
```python
name = "Umid"
age = 21
city = "Navoiy"
print(name, age, city)
```

📋 **Natija**:
```
Umid 21 Navoiy
```

> 🔔 **Izoh**: Vergul yordamida o‘zgaruvchilarni va matnlarni aralashtirib chiqarish qulay.

---

## 🛠️ String qo‘shish (concatenation)

O‘zgaruvchilarni matnlar bilan birlashtirib, bitta qatorda chiqarish mumkin.

📌 **Misol**:
```python
name = "Umid"
age = 21
print("My name is " + name + " and I am " + str(age) + " years old.")
```

📋 **Natija**:
```
My name is Umid and I am 21 years old.
```

> 🔔 **Izoh**: 
> - Raqamli qiymatlarni (`int`, `float`) matnga qo‘shishdan oldin ularni `str()` yordamida string turiga aylantirish kerak.
> - String concatenation kodni o‘qishda biroz qiyinchilik tug‘dirishi mumkin.

---

## 🛠️ f-Stringlardan foydalanish (Formatted String Literals)

Python 3.6 va undan keyingi versiyalarda f-string yordamida o‘zgaruvchilarni matnlar orasiga kiritish mumkin. Bu usul o‘qilishi oson va ishlatishga qulay.

📌 **Misol**:
```python
name = "Umid"
age = 25
print(f"My name is {name} and I am {age} years old.")
```

📋 **Natija**:
```
My name is Umid and I am 25 years old.
```

> 🟢 **Afzalliklari**:
> - O‘qilishi oson va aniq.
> - Qatorga o‘zgaruvchilarni kiritish juda qulay.
> - `.format()` usuliga nisbatan tezroq ishlaydi.

---

## 🛠️ `format()` metodidan foydalanish

`format()` metodi yordamida ham o‘zgaruvchilarni matnlar orasiga joylashtirish mumkin.

📌 **Misol**:
```python
name = "Umid"
age = 25
print("My name is {} and I am {} years old.".format(name, age))
```

📋 **Natija**:
```
My name is Umid and I am 25 years old.
```

> 🔔 **Izoh**: `format()` metodi f-stringga alternativ usul bo‘lib, Pythonning eski versiyalarida ham ishlatiladi.

---

## 🛠️ `repr()` funksiyasi bilan developer-friendly chiqish

`repr()` funksiyasi o‘zgaruvchilarni dasturchilar uchun qulayroq formatda qaytaradi. Bu funksiya debugging (xatoliklarni topish) jarayonida foydali bo‘ladi, chunki u qiymatlarni aniqroq ko‘rsatadi.

📌 **Misol**:
```python
name = "Umid"
print(repr(name))  # Outputs 'Umid'
```

📋 **Natija**:
```
'Umid'
```

> 🔔 **Izoh**: `repr()` qiymatlarni qo‘shtirnoqlar ichida chiqaradi va matnning ichki ko‘rinishini aks ettiradi.

---

## 🛠️ O‘zgaruvchilarning qiymatini bir qatorda chiqarish

Python 3.8 va undan keyingi versiyalarda `=` operatori yordamida o‘zgaruvchi nomini va uning qiymatini bir qatorda chiqarish mumkin.

📌 **Misol**:
```python
x = 42
y = "Python"
print(f"x = {x}, y = {y}")
```

📋 **Natija**:
```
x = 42, y = Python
```

---

## 🧪 Qo‘shimcha Misollar

1. Bir nechta o‘zgaruvchini birlashtirish:
```python
a = 10
b = 20
c = 30
print(f"a = {a}, b = {b}, c = {c}")
```

2. Matnlarni qo‘shish va o‘zgaruvchilarni chiqarish:
```python
name = "Python"
version = 3.10
print("I am learning " + name + " version " + str(version))
```

3. `repr()` funksiyasining qo‘llanilishi:
```python
text = "Hello\nWorld"
print(repr(text))  # Outputs 'Hello\nWorld'
```

---

## 🎯 Amaliyot uchun mashqlar

1. Quyidagi kodni to‘ldiring va natijasini toping:
```python
name = "Umid"
age = 21
print(f"My name is {name} and my age is {age}.")
```

2. Quyidagi kod qanday natija beradi? O‘ylab ko‘ring va tekshiring:
```python
x = 3.14159
print(f"The value of pi is approximately {x:.2f}.")
```

3. Matn va o‘zgaruvchilarni birlashtirib, yangi misol yozing:
```python
city = "Navoiy"
population = 125000
# Bu yerga kod yozing
```

---

🎯 Ushbu usullar Python dasturlash tilida o‘zgaruvchilarni terminalga chiqarishda ko‘p hollarda qulay va samarali dastur yozish imkonini beradi.