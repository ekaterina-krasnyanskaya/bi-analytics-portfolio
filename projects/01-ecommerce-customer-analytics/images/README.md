# Скриншоты дашборда

Сюда положи **экспортированные из своего .pbix** кадры страниц отчёта.
GitHub не рендерит `.pbix` — без картинок проект «невидим» для рекрутёра,
у которого нет Power BI Desktop. Это главный путь просмотра.

## Нужные файлы (имена важны — на них ссылается кейс `../README.md`)

| Файл | Страница отчёта |
|---|---|
| `01-executive-overview.png` | Executive Overview (KPI, тренд выручки, карта, топ-товары) |
| `02-product-analytics.png` | Product Analytics (Парето 80/20, матрица товар×месяц) |
| `03-customer-rfm.png` | Customer / RFM Segmentation (donut, scatter R×F) |
| `04-cohort-retention.png` | Cohort Retention (тепловая матрица когорт) |
| `05-geography-details.png` | Geography & Details (карта, decomposition tree, детальная таблица) |
| `report.pdf` | Полный экспорт отчёта в PDF (для рекрутёра без PBI) |

## Как снять красиво

- **Скриншот страницы:** в Power BI Desktop открой страницу → `Win + Shift + S`
  (или кнопкой Snip) → сохрани с нужным именем сюда.
- **PDF всего отчёта:** `Файл → Экспорт → Экспорт в PDF` → положи как `report.pdf`
  в папку `../report/`.

> ⚠️ Не клади сюда никакие кадры с рабочими данными — только этот учебный e-commerce проект.
