# mela-privacy

GitHub Pages site hosting the privacy policy for Mela (iPhone cycle tracker).

Lives at: `https://<your-github-username>.github.io/mela-privacy/`.

Source for the policy content is `index.md`. Jekyll renders it as HTML via the minimal theme.

## What to fill in before publishing

Open `index.md` and replace:

1. `EFFECTIVE_DATE_PLACEHOLDER` with the App Store launch date in `YYYY-MM-DD` form.
2. `LAST_UPDATED_PLACEHOLDER` (top of file) with today's date in `YYYY-MM-DD` form.
3. `CONTACT_EMAIL_PLACEHOLDER` (two places: English and Russian sections) with a real contact email. A dedicated address like `privacy@<domain>` or a personal one is fine, as long as you actually read it.

## How to publish

### Option A: GitHub CLI (one-time install via `brew install gh && gh auth login`)

```
cd ~/Code/mela-privacy
gh repo create mela-privacy --public --source=. --remote=origin --push
gh api repos/<your-username>/mela-privacy/pages -X POST -f source[branch]=main -f source[path]=/
```

The Pages URL prints in the second command's response. Use it in App Store Connect, App Information, Privacy Policy URL.

### Option B: GitHub web UI

1. Go to https://github.com/new
2. Repo name: `mela-privacy`. Visibility: Public. Do not init with README (we have one). Create.
3. Back in this directory: `git remote add origin https://github.com/<your-username>/mela-privacy.git`
4. `git push -u origin main`
5. On github.com/<your-username>/mela-privacy: Settings -> Pages -> Source: Deploy from a branch -> Branch: `main` / `/ (root)` -> Save.
6. Wait about a minute. The Pages URL appears on the same Settings page.

## Updating later

Edit `index.md`, commit, push. Pages rebuilds within 1-2 minutes.

If the substance of the policy changes (not just typos), bump `LAST_UPDATED_PLACEHOLDER` to the new date and consider notifying existing users via a "What's New" note in the next App Store release.
