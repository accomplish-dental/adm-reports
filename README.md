# ADM client reports

Campaign planner and performance pages for Accomplish Dental Marketing clients.

- `app.html` – the page template (`{{LOGO}}` is replaced with `logo.svg.txt`)
- `site/<scope>/` – one folder per practice or group, each with `index.html` and `data.json`
- Cloudflare Pages publishes the `site` folder. Logins are handled by Cloudflare Access per folder.
- `data.json` files are refreshed from HighLevel by a scheduled task.
