# Riri's Midnight Surprise 🌷

A private birthday website for Riri, styled with the user's own tulip, river, forest, mountain, cloud, and sunset photographs.

## Included experience
- Private page route: `/g/YOUR_ACCESS_TOKEN`
- Before midnight, the site shows only a countdown; the birthday content stays hidden until **December 17, 2026 at 00:00 Asia/Kathmandu**.
- Twelve notes unlock hourly from midnight through 11:00 AM Nepal time.
- A tulip garden featuring the supplied pink-tulip photo.
- A **Peaceful** gallery featuring the supplied landscape and sunset photos.
- A final, low-pressure girlfriend question after note 12, with one response submission.
- Optional email notification for the submitted answer via SMTP.

## Run locally
1. Install Node.js 18 or newer.
2. In this folder, run `npm install`.
3. Set `ACCESS_TOKEN` to a long random secret (at least 24 characters; 32+ is recommended). For email, also set `NOTIFY_EMAIL`, `SMTP_HOST`, `SMTP_PORT`, `SMTP_USER`, `SMTP_PASS`, and `SMTP_SECURE`.
4. Run `npm start` and open `http://localhost:3000/g/YOUR_ACCESS_TOKEN`.

## Deploy on Render
1. Put the contents of this folder in a private GitHub repository.
2. Create a Render Web Service from the repository. Build command: `npm install`; start command: `npm start`.
3. Add the environment variables listed above in Render's Environment settings.
4. Deploy and test `https://YOUR-SERVICE.onrender.com/health`.
5. The shareable page link will be `https://YOUR-SERVICE.onrender.com/g/YOUR_ACCESS_TOKEN`.

## Important before launch
- This ZIP is a project package, **not a live hosted website**. It still needs deployment to get a shareable public URL.
- Email notifications only work after valid SMTP settings are configured and tested.
- Responses are saved in `data/responses.json`. On hosting platforms, local files may be lost on restart/redeploy unless persistent storage is configured. Use a persistent disk or database before relying on response storage.
- Keep the access token and SMTP credentials private. Anyone with the private link can open the page.
- Test the full flow before sharing; the birthday unlock date is fixed to December 17, 2026, Nepal time.
