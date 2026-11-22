# GoDrive – учебные материалы (Mācību materiāli)

Статический сайт с анимированными уроками для автошколы: параллельная парковка и парковка задним ходом. Языки: латышский (по умолчанию) и русский. Адаптивная вёрстка: на узком экране сцена поворачивается вертикально.

Один файл `index.html`, без сборки и зависимостей. Разделы переключаются через hash: `#home`, `#parking`, `#reverse`.

## Брендинг
Цвета и шрифт собраны в блоке `:root` в начале `index.html` (комментарий «Brand tokens»). Значения временные, замените их на фирменные. Логотип сейчас текстовый («GoDrive» и значок машины) в `.logo`.

## Запуск локально
Откройте `index.html` в браузере или выполните `python3 -m http.server 8000` и зайдите на http://localhost:8000.

## Деплой на GitHub Pages
1. Создайте репозиторий на GitHub и отправьте туда файлы:
   ```
   git init -b main
   git add .
   git commit -m "GoDrive learning materials"
   git remote add origin https://github.com/<user>/<repo>.git
   git push -u origin main
   ```
2. В репозитории: Settings → Pages → Source: **GitHub Actions**.
3. Workflow `.github/workflows/pages.yml` опубликует сайт на `https://<user>.github.io/<repo>/`.

## Деплой на Vercel
- Через сайт: vercel.com → Add New → Project → импортируйте репозиторий. Framework Preset: **Other**, Build Command пустой, Output Directory `.`.
- Через CLI: `npm i -g vercel`, затем `vercel` (превью) или `vercel --prod`.

Файл `vercel.json` уже содержит базовые заголовки.
