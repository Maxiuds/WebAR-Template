# WebAR-буклет «Комп'ютер»

Буклет створено як результат виконання лабораторної роботи з дисципліни «Операційні системи».

**Команда проєкту:**

- студент Михайлов Максим, група AI-254
- викладач – Блажко О.А., доцент кафедри інформаційних систем Національного університету «Одеська політехніка».


# Документування WebAR-проєкту та робота з Git

## 2.1 Редагування файлів у GitHub-репозиторії

### 2.1.1 Створення файлу README.md

У кореневому каталозі GitHub-репозиторію створено файл `README.md`, який містить короткий опис WebAR-проєкту, інформацію про дисципліну та команду проєкту. Зміни зафіксовано з коментарем **Created by GitHub**.

---

### 2.1.2 Редагування файлу index.html

Виконано редагування файлу `index.html`. Змінено привітальне повідомлення WebAR-застосунку відповідно до вимог лабораторної роботи. Зміни збережено з коментарем **Changed by GitHub**.

---

## 2.2 Налаштування Git-клієнту

### 2.2.1 Встановлення Git-клієнту

Встановлено Git-клієнт та запущено програму **Git Bash**. За допомогою команди `pwd` отримано повний шлях до поточного робочого каталогу.

```bash
pwd
```

<img width="347" height="72" alt="image" src="https://github.com/user-attachments/assets/b2280444-706c-451e-b75f-587dfdfc3fa2" />


Рис. 3 – Результат виконання команди `pwd` у середовищі Git Bash.

---

### 2.2.2 Налаштування Git-користувача

Виконано налаштування параметрів `user.name` та `user.email` відповідно до облікового запису GitHub.

```bash
git config --global user.name "Maxiuds"
git config --global user.email "your_email@example.com"

git config user.name
git config user.email
```

<img width="558" height="181" alt="image" src="https://github.com/user-attachments/assets/a00a018b-723a-4956-b659-f939698f5bb4" />

Рис. 4 – Перевірка параметрів `user.name` та `user.email`.

## 2.3.1 Налаштування SSH-ключів

Для забезпечення безпечної роботи з GitHub було створено пару SSH-ключів за допомогою команди `ssh-keygen`. У результаті створено приватний ключ `id_ed25519` та відкритий ключ `id_ed25519.pub`, які збережено в каталозі `.ssh`.

```bash
ssh-keygen -t ed25519 -C "lhh523918@gmail.com"
```

<img width="736" height="423" alt="image" src="https://github.com/user-attachments/assets/175a63f7-3f31-46d8-806c-3727b3b6e25d" />

Рис. 5 – Створення SSH-ключів за допомогою команди `ssh-keygen`.

### 2.3.1.3 Розміщення відкритого SSH-ключа в GitHub

Відкритий SSH-ключ було додано до облікового запису GitHub у розділі **SSH and GPG keys**. Це дозволяє виконувати безпечне клонування, зміну та відправлення файлів до GitHub-репозиторію через SSH-з’єднання.

<img width="1240" height="672" alt="image" src="https://github.com/user-attachments/assets/51775d47-2308-447c-9830-594c2a4282b6" />

Рис. 6 – Додавання відкритого SSH-ключа до облікового запису GitHub.

## 2.3.3 Створення нової гілки проєкту

Створено нову Git-гілку `WebAR-Template_with_pattern_marker`, після чого виконано перехід до неї для подальшого внесення змін до проєкту.

```bash
cd ~/WebAR-Template

git branch WebAR-Template_with_pattern_marker
git checkout WebAR-Template_with_pattern_marker
git branch
```

<img width="712" height="382" alt="image" src="https://github.com/user-attachments/assets/9018f248-78f8-4743-a8ca-db41babd5cce" />

Рис. 8 – Створення нової Git-гілки та перехід до неї.

## 9. Створення Pattern-маркера

Для одного з об'єктів WebAR-проєкту було створено Pattern-маркер за допомогою онлайн-генератора AR.js Marker Training. У результаті було отримано файли `pattern-device.patt` та `pattern-device.png`, які додано до репозиторію.

---

## 10. Заміна Barcode-маркера на Pattern-маркер

У файлі `index.html` внесено зміни до конфігурації маркерів. Один Barcode-маркер було замінено на Pattern-маркер шляхом зміни параметрів `patternNames` та `patternBarcode`.

```javascript
const patternNames = ['', 'pattern-device.patt', ''];
const patternBarcode = [1, -1, 3];
```

---

## 11. Оновлення буклету

У буклеті WebAR один із Barcode-маркерів було замінено на створений Pattern-маркер. Після внесення змін буклет було повторно збережено у форматі PDF.

---

## 12. Фіксація змін у Git

Після завершення редагування проєкту всі зміни було додано до локального Git-репозиторію, створено коміт та відправлено до віддаленого репозиторію GitHub.

```bash
git add .
git commit -m "Changed barcode marker to pattern marker"
git push origin WebAR-Template_with_pattern_marker
```

<img width="778" height="322" alt="image" src="https://github.com/user-attachments/assets/96c87f52-034e-4d7e-bad7-0249d2498bf2" />


## 13. Публікація через GitHub Pages

Для перевірки роботи WebAR-застосунку налаштовано GitHub Pages. Як джерело публікації обрано гілку `WebAR-Template_with_pattern_marker`, після чого зміни стали доступними через веббраузер.

---

## 14. Перевірка роботи застосунку

Після оновлення GitHub Pages виконано тестування WebAR-застосунку. Перевірено коректне розпізнавання Pattern-маркера та відображення мультимедійного контенту. Також підтверджено працездатність інших Barcode-маркерів.

<img width="710" height="1537" alt="image" src="https://github.com/user-attachments/assets/4f9fb9b4-c556-444e-b842-a25567dd3f85" />

## Висновок

Під час виконання лабораторної роботи було закріплено навички роботи з Git та GitHub, налаштовано безпечне підключення за допомогою SSH-ключів, створено окрему гілку проєкту, реалізовано використання Pattern-маркера замість Barcode-маркера, оновлено WebAR-буклет та успішно опубліковано результати за допомогою GitHub Pages. Усі поставлені завдання лабораторної роботи виконано.
