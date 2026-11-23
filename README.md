# Startup Karlay — GitHub Pages Edition

A static, responsive editorial website for Pakistan’s startup ecosystem. This edition is designed to deploy directly from GitHub Pages — no Node.js, server, database, hosting subscription, or build command required.

## Publish it directly from GitHub
1. Create a new **public** GitHub repository, for example `startup-karlay`.
2. Extract this ZIP and upload the contents (the `.github` folder and `.nojekyll` file included) to the repository root.
3. Commit the files to the `main` branch.
4. In the repository, open **Settings → Pages**. Under **Build and deployment → Source**, select **GitHub Actions**.
5. Open the **Actions** tab and wait for **Deploy Startup Karlay to GitHub Pages** to finish successfully.
6. Your site will be available at `https://YOUR-USERNAME.github.io/REPOSITORY-NAME/`.

## Add or edit news
Open `public/stories.js`. Add a new object to the `window.STARTUP_KARLAY_STORIES` array, following the existing examples. Commit the change to `main`; GitHub Actions will publish the update automatically. Fields: `title`, `slug`, `category`, `excerpt`, `body`, `image`, `author`, `created_at` (`YYYY-MM-DD HH:MM:SS`), and `breaking` (`true`/`false`). Use your own verified reporting and image rights.

## Important static-hosting limitation
GitHub Pages serves static files only. This ZIP includes working browser-side story browsing, category filters, search, article reading, responsive layout and an email-based newsletter sign-up request. It does **not** include a server-side admin login, shared database, automatic email collection, push notifications, or server APIs. To add secure multi-user publishing, subscriber storage or real notifications, connect a separate backend/API later. Do not put passwords, API secrets or private tokens in this repository.

## Preview locally
You can open `public/index.html` in a browser, or run a simple local static server such as `python -m http.server 8000` from the `public` directory.

## Manage articles from a browser

This edition includes `.pages.yml` for Pages CMS. Sign in at https://app.pagescms.org with GitHub, authorize the GitHub App for this repository, and edit **Articles & Updates**. It commits changes to `public/stories.json`; the GitHub Pages workflow then redeploys the site. See `CMS-GUIDE.md`.
