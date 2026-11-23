# Manage Startup Karlay articles without editing code

This GitHub Pages edition uses Pages CMS to edit `public/stories.json` directly in your GitHub repository.

1. Upload the contents of this project to a GitHub repository (keep `.pages.yml` at the repository root).
2. Enable GitHub Pages using **Settings → Pages → GitHub Actions**.
3. Open https://app.pagescms.org and sign in with GitHub.
4. Install/authorize the Pages CMS GitHub App for the account that owns your repository.
5. Select the `startup-karlay` repository. Pages CMS reads `.pages.yml` automatically.
6. Open **Articles & Updates** to add, edit, or delete stories. Save changes; Pages CMS commits them to GitHub.
7. GitHub Actions automatically redeploys the site after the commit.

Your site stays static on GitHub Pages. Pages CMS is a separate hosted editing interface; it does not add a Node.js backend or database. Only give repository access to people you trust.

Article slug should be unique and lowercase with hyphens. Use a publicly accessible image URL in the Cover image URL field. For uploads, add images under `public/uploads` in GitHub for now.
