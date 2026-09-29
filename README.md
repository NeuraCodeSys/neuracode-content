# NeuraCode website content

Everything on https://www.neuracodeinc.com/projects comes from this repo.
Changes appear on the site about **5–10 minutes** after you commit. You never need to redeploy the website.

## Add a project

1. Open the `projects/` folder and click `_template.md`.
2. Copy its contents (the copy button at the top right of the file).
3. Go back to `projects/`, choose **Add file → Create new file**.
4. Name it after the project in lowercase with dashes, e.g. `acme-portal.md`.
   That name becomes the page address: `neuracodeinc.com/projects/acme-portal`.
5. Paste, fill in the fields, write the text, and **delete the `draft: true` line**.
6. Click **Commit changes**.

## Add a logo or screenshot

1. Open `images/`, choose **Add file → Upload files**.
2. Upload into a folder named after the project, e.g. `images/acme-portal/logo.png`.
3. Put that path in the project file: `logo: images/acme-portal/logo.png`.

Images inside the project text (Markdown body) are not shown on the site — use `logo` and `cover` instead.

## Edit or hide a project

- Edit: open the file, click the pencil icon, change it, commit.
- Hide: add `draft: true` to the top section and commit.

## Rules the site checks

- `name`, `type`, `tagline` and `industry` are required. A file missing one is skipped (the rest of the site keeps working).
- `type` must be `product` or `client`.
- Files starting with `_` are ignored.

## Site settings (`site.json`)

Edit `site.json` on GitHub (pencil icon → commit). Changes appear on the site within about 5–10 minutes. Leave a value empty to turn it off.

| Field | Example | What it does |
|---|---|---|
| `gtmId` | `GTM-AB12CD3` | Google Tag Manager container. Add Google Analytics and other tags inside Tag Manager, not here. |
| `googleSiteVerification` | `abc123…` | Google Search Console "HTML tag" verification code (only the `content` value). |
| `bingSiteVerification` | `0123ABCD…` | Bing Webmaster Tools verification code. |
| `founded` | `2021` | Founding year shown on the About section. |
| `teamSize` | `12 people` | Team size shown on the About section. |
| `profiles` | `["https://www.linkedin.com/company/…"]` | Company profiles (LinkedIn, GitHub, directories). Google uses them to connect the site to the company. |

These values are public by design (they appear in every page's source). Never put passwords, API secrets or tokens in this repo.
