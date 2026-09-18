# Финальный шаг — добавить визуалы

✅ Репозиторий уже создан и опубликован:
**https://github.com/ekaterina-krasnyanskaya/bi-analytics-portfolio** (публичный).
Залито: hero-README, кейс проекта, весь код DAX, данные, конфиги, Git LFS.

Осталось одно — то, что можно сделать только руками в Power BI Desktop
(отрендерить страницы отчёта автоматически невозможно). ~10–15 минут.

---

## 1. Доделать модель в Power BI (рекомендуется)

Открой `ecommerce-customer-analytics.pbix` (в `Загрузки`):

- В представлении **Модель** удали таблицу **`online_retail_II (1)`** — это сырой
  дубликат на 1 млн строк (правой кнопкой → *Удалить*, или сними «Enable load»).
- *Файл → Параметры → Загрузка данных* → снять **Auto date/time**.
- Со страницы **Cohort Retention** убери слайсер `Year` (искажает Retention %).
- Сохрани файл.

## 2. Снять визуалы

- **5 скриншотов** страниц (`Win + Shift + S`) → положить в
  `projects/01-ecommerce-customer-analytics/images/` с именами:
  `01-executive-overview.png`, `02-product-analytics.png`, `03-customer-rfm.png`,
  `04-cohort-retention.png`, `05-geography-details.png`
  (по желанию `06-model.png` — вид модели).
- **PDF:** *Файл → Экспорт → Экспорт в PDF* →
  `projects/01-ecommerce-customer-analytics/report/report.pdf`.
- **Скопировать** `ecommerce-customer-analytics.pbix` →
  `projects/01-ecommerce-customer-analytics/report/`.

## 3. Залить (2 команды)

```
cd C:\Users\krasn\ekaterina-bi-portfolio
git add .
git commit -m "Add dashboard screenshots, PDF and .pbix"
git push
```

После этого напиши мне «визуалы добавила» — я включу картинки в README
(они сейчас спрятаны в комментариях, чтобы не висели «битыми») и добавлю
живую ссылку на отчёт.

---

## Дальше (по желанию)

- Опубликовать отчёт: Power BI Service → *Publish to web* → вставить ссылку в README.
- В резюме и LinkedIn указать ссылку на репозиторий.
- Обновлять что-либо потом: правки → `git add . && git commit -m "..." && git push`.
