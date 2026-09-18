# Как опубликовать это портфолио — пошагово

Репозиторий уже собран и закоммичен локально. Осталось три блока действий.
Всё, что можно было сделать за тебя, уже сделано — ниже только то, что требует
твоего входа в аккаунт и Power BI Desktop (их невозможно автоматизировать).

---

## Блок 1. Доделать визуалы в Power BI (~15 мин) — обязательно

GitHub не показывает `.pbix`. Без картинок и PDF рекрутёр без Power BI ничего не увидит,
а в README будут «битые» картинки. Поэтому сначала — визуалы.

Открой `ecommerce-customer-analytics.pbix` (лежит в `Загрузки/Downloads`):

1. **Почистить модель** (чтобы файл не был раздут вдвое):
   - В представлении *Модель* найди таблицу **`online_retail_II (1)`** → правой кнопкой →
     *Удалить* (или сними «Enable load» в Power Query). Это сырой дубликат на 1 млн строк.
   - *Файл → Параметры → Загрузка данных* → снять галку **Auto date/time**.
2. **Убрать слайсер `Year`** со страницы *Cohort Retention* (он искажает Retention %).
3. **Снять 5 скриншотов** страниц (`Win + Shift + S`) и сохранить в
   `projects/01-ecommerce-customer-analytics/images/` с именами:
   - `01-executive-overview.png`
   - `02-product-analytics.png`
   - `03-customer-rfm.png`
   - `04-cohort-retention.png`
   - `05-geography-details.png`
   - (по желанию `06-model.png` — вид модели)
4. **Экспорт PDF:** *Файл → Экспорт → Экспорт в PDF* → сохранить как
   `projects/01-ecommerce-customer-analytics/report/report.pdf`.
5. **Скопировать сам файл** `ecommerce-customer-analytics.pbix` в
   `projects/01-ecommerce-customer-analytics/report/`.

---

## Блок 2. Завести/войти в GitHub (один раз)

1. Аккаунта нет → зарегистрируйся: https://github.com/signup
   (ник в URL портфолио, выбирай аккуратный: `ekaterina-krasnyanskaya`, `katecipy` и т.п.)
2. Войти через gh CLI:
   ```
   gh auth login
   ```
   выбрать **GitHub.com → HTTPS → Login with a web browser** и войти своим аккаунтом.
3. Проверить, что активен именно твой аккаунт:
   ```
   gh auth status
   ```

---

## Блок 3. Опубликовать (2 команды)

```
cd C:\Users\krasn\ekaterina-bi-portfolio

# добавить довложенные визуалы и pbix в коммит
git add .
git commit -m "Add report, PDF and dashboard screenshots"

# создать публичный репозиторий под своим аккаунтом и запушить
gh repo create bi-analytics-portfolio --public --source=. --remote=origin --push
```

Готово — ссылка `github.com/<твой-ник>/bi-analytics-portfolio`. Её и вставляй в резюме
(в шапку рядом с email) и в LinkedIn.

> Файл `.pbix` уходит через **Git LFS** автоматически (настроено в `.gitattributes`) —
> ничего дополнительно делать не нужно, git-lfs уже установлен.

---

## Полезное

- Обновить что-то потом: правишь файлы → `git add . && git commit -m "..." && git push`.
- Сделать репозиторий заметнее: в настройках репо добавь *Description* и *Topics*
  (`power-bi`, `dax`, `data-analytics`, `portfolio`).
- Живую ссылку на отчёт (Publish to web) вставь в оба README вместо
  `_<укажи ссылку после публикации>_`.
