# EasyRead site

Static pages for the EasyRead app, served by GitHub Pages:

- `index.html` – landing page
- `privacy.html` – privacy policy (App Store / Google Play "Privacy Policy URL")
- `support.html` – FAQ and contact form (App Store / Google Play "Support URL")

## Contact form

`support.html` posts to a Google Apps Script web app that emails the message to the developer.

- **The script is intentionally not in this repo.** `apps-script/` and `*.gs` are gitignored. The
  versioned copy lives in the private EasyRead repo (`support-form/Code.gs`). Deploy it from
  script.google.com. Never commit it here.
- Only the public web-app URL (`ENDPOINT` in `support.html`) is in this repo. The page has to call
  it, so it can't be hidden. The recipient address appears nowhere in the repo or the pages.
- After changing the script, redeploy it as a new version of the same deployment so the URL stays
  the same.
