# CLAUDE.md for AI Reports Hub

When the user asks to build or update a report/dashboard:
1. Follow all rules in `AI_INSTRUCTIONS.md`.
2. MANDATORY: Include an **EN / UA** language switcher with dynamic UI labels.
3. MANDATORY: Include an **Export** dropdown supporting 5 formats: **CSV, EXCEL (.xlsx), PDF, JSON, MD**.
4. Create the report in a dedicated directory: `/[slug]/index.html`.
5. Use standalone single-file HTML with Tailwind CDN, Chart.js CDN, SheetJS CDN.
6. Update the root `index.html` catalog with a new card pointing to `./[slug]/`.
7. Run `git add . && git commit -m "Add report: <name>" && git push origin main` to deploy automatically to Cloudflare, Vercel, and Netlify.
