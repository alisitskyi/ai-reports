# CLAUDE.md & Cursor Rules for AI Reports Hub

When the user asks to build or update a report/dashboard:
1. Follow the guidelines in `AI_INSTRUCTIONS.md`.
2. Create the report in a dedicated directory: `/[slug]/index.html`.
3. Use standalone single-file HTML with Tailwind CDN and Chart.js CDN.
4. Update the root `index.html` catalog with a new card pointing to `./[slug]/`.
5. Run `git add . && git commit -m "Add report: <name>" && git push origin main` to deploy automatically to Cloudflare, Vercel, and Netlify.
