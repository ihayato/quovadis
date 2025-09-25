# Agent Notes

- Deployments must remain publicly accessible. Never enable Vercel SSO / Deployment Protection for this project again.
- After each production deploy, verify `https://quovadis-domine.vercel.app` responds with HTTP 200 (no `_vercel_sso_nonce`). If protection toggles back on, immediately disable it via the Vercel dashboard (Team Settings → Authentication → Deployment Protection) or by clearing it with the Vercel API (`PATCH /v9/projects/{id}` with `"ssoProtection": null`).
- Keep the canonical OGP asset as `ogp.jpg`; do not reintroduce `ogp.png`.
