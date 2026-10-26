# Weekly Store Review — prototype

A single-page dashboard showing weekly sales, gross profit, estimated labour and "left after labour" for 27 stores, with week-on-week and same-week-last-year comparisons. All data is invented sample data.

Everything is in `index.html`. No build step.

## Before you share it

Open `index.html` and edit the `CONFIG` block near the top of the script:

- `feedbackEmail`: put your email here so the **Give feedback** button opens an email to you. If left empty, feedback is copied to the clipboard instead.
- `stores`: rename the 27 stores if you want them to match the group's real store names. Keep it at 27 names or adjust as needed; the sample data adapts.
- `defaults`: starting hourly rates, PRSI on/off, and the labour % target.

## Deploy on Vercel (easiest)

1. Create a GitHub repository and upload `index.html` (and this README).
2. Go to vercel.com → **Add New → Project** → import the repository.
3. Framework preset: **Other**. Leave the build command empty. Click **Deploy**.
4. Share the link Vercel gives you (e.g. `store-review.vercel.app`).

Or, without GitHub: install the Vercel CLI (`npm i -g vercel`), run `vercel` inside this folder, and follow the prompts.

## Deploy on GitHub Pages

1. Upload `index.html` to a GitHub repository.
2. **Settings → Pages → Deploy from a branch → main / root**.
3. The site appears at `https://<username>.github.io/<repo>/` after a minute.

## Notes

- Charts load Chart.js from cdnjs and the font from Google Fonts, so viewers need an internet connection.
- Labour rate settings are remembered per browser.
- The sample data includes a few deliberate situations to show what the flags catch: Balbriggan (thin margin after labour), Swords (hours up, sales not), Bray (deli waste spike), Naas (GP % down from tobacco mix), Clondalkin (fewer customers), Rathmines (long hours).
- In a live version, the sample-data block is replaced by a weekly import from Retail Solutions and Timepoint (see the "How it works" tab).
