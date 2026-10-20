# ADM client reports

Campaign planner and performance pages for Accomplish Dental Marketing clients.

- `app.html` – the page template (`{{LOGO}}` is replaced with `logo.svg.txt`)
- `site/<scope>/` – one folder per practice or group, each with `index.html` and `data.json`
- Cloudflare Pages publishes the `site` folder. Logins are handled by Cloudflare Access per folder.
- `data.json` files are refreshed from HighLevel by a scheduled task.
- `site/scopes.json` – the team practice switcher (behind the team-only login). Team views use `/adm/?p=<practice>` or `/adm/?g=<group>`.
- Campaign targets come from the ADM campaign card fields "Campaign - Target Consults Booked" and "Campaign - Target Treatments Going Ahead" (`plan[].target = {consults, ahead}`).
- 12-month targets come from the onboarding fields on the practice contact (`practice.annualTarget = {revenue, newPatients, start}`).
