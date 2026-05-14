BLOCK DROP — Tetris Discount Game
A retro arcade Tetris game that rewards players with project discount codes. Single HTML file, no build step, no dependencies. Designed to drop straight into GitHub Pages.
Discount tiers
Tier	Score target	Reward	Code
01	1,000	10% off	`BLOCK10`
02	2,500	20% off	`BLOCK20`
03	5,000	30% off	`BLOCK30`
The highest tier reached during a run is shown on the page and on the game-over screen. High score persists across sessions via `localStorage`.
Deploy to GitHub Pages
Create a new public repo on GitHub (e.g. `block-drop`).
Add `index.html` to the root of the repo and commit.
Go to Settings → Pages.
Under Source, pick the `main` branch and `/ (root)` folder. Save.
After ~30 seconds your game is live at `https://<your-username>.github.io/<repo-name>/`.
That's it. No build, no framework, no package manager.
Customising
Open `index.html` and edit:
Discount codes — search for `DISCOUNT_TIERS` in the script block. Change `code`, `percent`, or `score`.
Score thresholds — same `DISCOUNT_TIERS` array, plus the static numbers in the discount table HTML (search for `1,000`, `2,500`, `5,000`) and the progress-bar markers.
Branding — replace the `BLOCK DROP` heading and the footer text. The `--neon-pink`, `--neon-cyan`, `--neon-yellow` CSS variables at the top control the palette.
Claim instructions — edit the `claim-section` HTML block to describe how clients redeem the code (email you a screenshot, etc.).
Controls
Arrows — move and soft drop
Up / X — rotate
Space — hard drop
P — pause
Mobile users get on-screen buttons.
Tech
Plain HTML, CSS, and vanilla JS. Uses canvas for the game board and `localStorage` for high scores. Fonts are pulled from Google Fonts (`Press Start 2P`, `Syne`, `JetBrains Mono`).
