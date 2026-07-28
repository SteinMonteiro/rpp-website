# Research to action — website

This repository contains a minimal single-page site (static HTML + CSS).

Quick links
- `index.html`
- `styles.css`
- `.github/workflows/deploy.yml` (GitHub Actions workflow to deploy to Pages)

Preview locally

1. Open `index.html` directly in your browser (quick but may not reflect a real server).
2. Recommended: run a simple local HTTP server from the project root:

```bash
python3 -m http.server 8000
# then open http://localhost:8000 in your browser
```

Or use the VS Code Live Server extension and click **Go Live**.

Deploy to GitHub Pages (with Actions)

This repo includes a workflow at `.github/workflows/deploy.yml` that publishes the repository root from the `main` branch whenever you push to `main`.

This keeps the deployment simple and matches the GitHub Pages source setting that you can choose in the repository settings.

Steps:

1. Commit and push your changes to `main`:

```bash
git add .
git commit -m "Add site and deploy workflow"
git push origin main
```

2. Open the repository **Actions** tab on GitHub and watch the "Deploy to GitHub Pages" workflow run. If it succeeds, GitHub Pages will publish the site from the `main` branch.

3. In the repository **Settings → Pages**, set the source to **Deploy from a branch** and select the `main` branch with the `/ (root)` folder.

4. The default site URL will be:

```
https://SteinMonteiro.github.io/rpp-website/
```

Custom domain

- To use a custom domain, add a `CNAME` file with your domain (one line) to the repository root and configure DNS (CNAME or A records) per GitHub Pages docs.

Troubleshooting
- If the site does not appear, check the Actions run logs for errors in the **Actions** tab.
- In the repository Settings → Pages, confirm the site source and inspect the published URL.

Questions or changes
- If you want, I can: add a `CNAME` file, enable a custom domain workflow, or create a simple `README` badge showing the Pages URL.
# rpp-website
A website for the research.policy.practice
