# Setup — SahuPapun/SahuPapun profile README

1. Create a **new public repo** named exactly `SahuPapun` (must match your username).
2. Copy everything from this zip into the repo root, keeping the folder structure:
   ```
   SahuPapun/
   ├── README.md
   └── .github/
       └── workflows/
           ├── snake.yml
           └── contrib3d.yml
   ```
3. Push to `main`.
4. In the repo's **Settings → Actions → General**, under "Workflow permissions," select
   **"Read and write permissions"** — both workflows need this to push generated SVGs.
5. Go to the **Actions** tab and manually run both workflows once (`Run workflow` button)
   so the animations generate immediately instead of waiting for the first scheduled run.
6. After `snake.yml` runs, it creates an `output` branch holding the generated SVG/GIF —
   this is already wired up in `README.md` via `raw.githubusercontent.com/.../output/...`.
7. After `contrib3d.yml` runs, it commits `profile-3d-contrib/profile-night-rainbow.svg`
   directly to `main` — already linked in `README.md`.
8. Visit `github.com/SahuPapun` — your profile page will now show the full README.

### Notes
- The snake animation refreshes every 12 hours; the 3D calendar refreshes daily. Adjust
  the `cron` schedules in each workflow file if you want a different cadence.
- The snake SVG has separate dark/light variants that auto-switch using GitHub's
  `#gh-dark-mode-only` / `#gh-light-mode-only` image suffixes — no extra setup needed.
- All project links in `README.md` point to your real repos pulled directly from your
  GitHub profile.
