# QRNova Privacy Policy website

This folder contains a simple static privacy-policy website for the QRNova Android app. It is designed to be published using GitHub Pages and served over HTTPS.

## Before publishing

1. Open `index.html` and replace **both occurrences** of `REPLACE-WITH-YOUR-SUPPORT-EMAIL@example.com` with an email address that you monitor.
2. Confirm the production APK/AAB uses only the data practices described on the page. In particular, verify which Firebase services are enabled and whether any advertising SDK or ad network is active.
3. If the app uploads QR contents, scan results, images, generated codes, or history to a server, update the policy to explain that before publishing.
4. If the app's developer identity or support contact needs to be shown by name or business, update the contact section.
5. The current draft is based on inspection of the APK supplied with the publishing request. It is a working draft, not a legal certification or a substitute for checking the app's source code and SDK configuration.

## Publish with Git and GitHub Pages

### 1. Create the GitHub repository

1. Sign in at <https://github.com>.
2. Click **New repository**.
3. Name it `qrnova-privacy-policy`.
4. Choose **Public** (required for GitHub Free Pages for a public repository).
5. Do not add a README or `.gitignore` if you are pushing this existing folder with Git.
6. Click **Create repository**.

### 2. Push this folder using Git

Open PowerShell or Git Bash in this folder (`qrnova-privacy-policy`) and run:

```bash
git init
git add index.html README.md
git commit -m "Add QRNova privacy policy"
git branch -M main
git remote add origin https://github.com/YOUR_GITHUB_USERNAME/qrnova-privacy-policy.git
git push -u origin main
```

Replace `YOUR_GITHUB_USERNAME` with your GitHub username. If Git asks you to sign in, complete the GitHub authentication prompt.

### 3. Enable GitHub Pages

1. Open the new repository on GitHub.
2. Select **Settings** → **Pages**.
3. Under **Build and deployment**, set **Source** to **Deploy from a branch**.
4. Set **Branch** to `main` and folder to `/(root)`.
5. Click **Save**.
6. Wait for the Pages deployment to finish. GitHub notes that publishing can take up to about 10 minutes.

Your privacy-policy URL will be:

```text
https://YOUR_GITHUB_USERNAME.github.io/qrnova-privacy-policy/
```

Replace `YOUR_GITHUB_USERNAME` with your actual username. Open the link in an incognito/private browser window to confirm it is public. In the repository's **Settings → Pages**, enable **Enforce HTTPS** when the option is available.

### 4. Add the URL to Google Play Console

In Play Console, open **Policy and programs → App content → Privacy policy** (the exact menu placement may vary). Paste the public HTTPS URL above, save, and check that the page opens without signing in.

## Updating the policy later

Edit `index.html`, then run:

```bash
git add index.html
git commit -m "Update QRNova privacy policy"
git push
```

GitHub Pages will redeploy the site after the push.
