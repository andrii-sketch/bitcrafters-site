# bitcrafters.io

Статичний сайт BitCraft Advisors. Без білдів, без залежностей — чистий HTML/CSS.

## Структура

```
index.html, services.html, cases.html, about.html, contact.html  — EN
ua/…                                                             — українська версія
styles.css                                                       — спільні стилі
CNAME                                                            — кастомний домен для GitHub Pages
404.html                                                         — сторінка помилки
```

## Деплой на GitHub Pages (разово, ~15 хв)

1. Створіть **публічний** репозиторій на GitHub (наприклад `bitcrafters-site`).
2. Запуште вміст цієї папки в корінь репозиторію:
   ```bash
   cd site
   git init && git add . && git commit -m "Initial site"
   git branch -M main
   git remote add origin git@github.com:ВАШ_ЮЗЕРНЕЙМ/bitcrafters-site.git
   git push -u origin main
   ```
3. У репозиторії: **Settings → Pages → Source: Deploy from a branch → main / (root) → Save.**
4. Через 1–2 хвилини сайт буде на `https://ВАШ_ЮЗЕРНЕЙМ.github.io/bitcrafters-site/`.

## Підключення домену bitcrafters.io

1. **Settings → Pages → Custom domain** → введіть `www.bitcrafters.io` → Save (файл CNAME вже в репозиторії).
2. У DNS-панелі домену (там, де зараз керується bitcrafters.io — імовірно Wix; домен варто перенести до реєстратора або Cloudflare DNS):
   - `CNAME`-запис: `www` → `ВАШ_ЮЗЕРНЕЙМ.github.io`
   - `A`-записи для кореневого домену `bitcrafters.io`:
     ```
     185.199.108.153
     185.199.109.153
     185.199.110.153
     185.199.111.153
     ```
3. Назад у **Settings → Pages** поставте галочку **Enforce HTTPS** (з'явиться після перевірки DNS, до години).

## Плейсхолдери

Всі підставлені: форма Web3Forms робоча, кнопка дзвінка веде на `cal.com/bitcrafters.io/30min`. Сайт готовий до деплою.

## Оновлення сайту

Правите HTML → `git add . && git commit -m "update" && git push` → зміни на проді за ~1 хв.
