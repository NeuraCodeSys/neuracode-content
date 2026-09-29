# NeuraCode website content

Everything on https://www.neuracodeinc.com/projects comes from this repo.
Changes appear on the site about **5 minutes** after you commit. You never need to redeploy the website.

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

## Edit or hide a project

- Edit: open the file, click the pencil icon, change it, commit.
- Hide: add `draft: true` to the top section and commit.

## Rules the site checks

- `name`, `type`, `tagline` and `industry` are required. A file missing one is skipped (the rest of the site keeps working).
- `type` must be `product` or `client`.
- Files starting with `_` are ignored.
