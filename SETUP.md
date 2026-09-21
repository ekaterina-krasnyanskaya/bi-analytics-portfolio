# Портфолио — статус и обслуживание

✅ **Опубликовано:** https://github.com/ekaterina-krasnyanskaya/bi-analytics-portfolio (публичный).

Что внутри:
- **Проект 01 — E-commerce Customer Analytics:** кейс, весь код DAX, данные,
  5 скриншотов, PDF отчёта, файл `.pbix` (Git LFS).
- **Проект 02 — Сквозная аналитика (воронка + рекламные каналы):** кейс,
  2 скриншота, файл `.pbix` (Git LFS).

---

## Как обновлять

```
cd C:\Users\krasn\ekaterina-bi-portfolio
git add .
git commit -m "что изменила"
git push
```
(пуш идёт под аккаунтом `ekaterina-krasnyanskaya` — настроено).

---

## Что стоит доделать (по желанию, повышает качество)

1. **Живые ссылки на отчёты.** Power BI Service → *Publish to web* → вставить ссылки
   в README проектов вместо «_(скоро)_».
2. **Проект 01, блок Data Quality** на странице Executive Overview всё ещё показывает
   старые цифры (£17.74 млн / 805 549) — не совпадает с KPI (£20.12 млн). Поправить
   текст в Power BI и пере-экспортировать `report.pdf`.
3. **Проект 01, модель:** удалить сырую таблицу `online_retail_II (1)`, выключить
   Auto date/time — файл станет легче.
4. Указать ссылку на репозиторий в резюме и в Telegram-профиле.
