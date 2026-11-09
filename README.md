# AI Reports Hub

Автоматизований хаб інтерактивних HTML-звітів та дашбордів. 
При кожному пуші в гілку `main` проєкт **автоматично розгортається на 3 платформах одночасно**:

| Платформа | Посилання на головний портал | Звіт Google Ads (gemini_test_1) |
| :--- | :--- | :--- |
| **Cloudflare Pages/Workers** | [ai-reports.lisitskyi.workers.dev](https://ai-reports.lisitskyi.workers.dev/) | [ai-reports.lisitskyi.workers.dev/gemini_test_1/](https://ai-reports.lisitskyi.workers.dev/gemini_test_1/) |
| **Vercel** | [ai-reports-lovat.vercel.app](https://ai-reports-lovat.vercel.app/) | [ai-reports-lovat.vercel.app/gemini_test_1/](https://ai-reports-lovat.vercel.app/gemini_test_1/) |
| **Netlify** | [alysytskyi.netlify.app](https://alysytskyi.netlify.app/) | [alysytskyi.netlify.app/gemini_test_1/](https://alysytskyi.netlify.app/gemini_test_1/) |

---

## 📁 Структура проєкту

```text
ai-reports/
├── index.html              # Головний портал-каталог усіх звітів
├── AI_INSTRUCTIONS.md      # Інструкції для будь-якого ШІ (Cursor, Copilot, Claude, ChatGPT)
├── CLAUDE.md               # Системні інструкції для Claude Code / IDE
├── template/
│   └── index.html          # Готовий стартовий шаблон для нових дашбордів
└── gemini_test_1/
    └── index.html          # Звіт: Google Ads Multi-Product Analytics
```

---

## 🚀 Як додати новий звіт

### Спосіб 1: Через ШІ у VS Code (Cursor, Copilot, Claude)
Просто напишіть у чаті ШІ:
> *«Створи новий звіт [назва/тема/дані] у папці `report_slug/index.html`, додай картку на головну сторінку `index.html` та зроби git push»*.

ШІ прочитає інструкції в `AI_INSTRUCTIONS.md` і зробить усе автоматично.

### Спосіб 2: Вручну
1. Створіть нову папку, наприклад `my_new_report/`.
2. Покладіть туди автономний `index.html` (можна скопіювати з `template/index.html`).
3. Додайте посилання/картку в головний `index.html`.
4. Зробіть `git push`:
   ```bash
   git add .
   git commit -m "Add new report: my_new_report"
   git push origin main
   ```
Через 10–15 секунд звіт буде онлайн на всіх 3 сервісах!
