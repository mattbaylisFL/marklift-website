# marklift-website

Marketing + legal site for [MarkLift](https://marklift.app), published via
**GitHub Pages** on the custom domain `marklift.app`.

Plain static HTML/CSS — no build step. The iOS app's in-app **Privacy** and
**Terms** links point at `/privacy.html` and `/terms.html` here, so this must be
live before App Store submission (Apple clicks the links on a real device).

## Pages
- `index.html` — landing page
- `privacy.html` — privacy policy (zero data collected, on-device)
- `terms.html` — terms of use (one-time $4.99 unlock, not a subscription)
- `support.html` — support + FAQ, contact `support@marklift.app`

## Publish (GitHub Pages)
1. Push to `main`.
2. Repo → Settings → Pages → Source: **Deploy from a branch**, branch `main` / root.
3. The `CNAME` file points the site at `marklift.app`; set that as the custom domain
   in Pages settings and add the DNS records GitHub shows (A/AAAA for apex + a
   `www` CNAME). Enable "Enforce HTTPS".

## Notes
- Absolute paths (`/css`, `/img`) are correct because the site is served at the apex
  custom domain, not a `github.io` subpath.
- Bump the `?v=` query on `style.css` references when you change the CSS so returning
  visitors don't get stale styles.
