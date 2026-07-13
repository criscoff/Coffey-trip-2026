# Coffey Trip 2026

Trip website source. Edits made in this folder flow to production via git → Netlify.

**Live:** https://coffey-trip-2026.netlify.app/
**Repo:** https://github.com/criscoff/Coffey-trip-2026
**Netlify:** auto-builds on push to main (~30 sec)

## Workflow for future Claude sessions

1. Edit `index.html` (or any file) in place — use the file tools directly on paths under this folder.
2. Verify byte count via Read after every Write (OneDrive lag can truncate).
3. Commit + push:
   ```
   git add -A
   git commit -m "Describe change"
   git push
   ```
   Token is already embedded in `origin` URL. No env vars needed.
4. Netlify auto-builds. Live within ~30 sec.

## Notes

- Repo lives under `criscoff` (Cris's personal GitHub), not `crisrcoffey-tech`. The token in `Claude\.credentials.json` was granted Write access as a collaborator, so pushes work.
- Do NOT commit the token or the `.credentials.json`. This clone's remote already has the token baked into the URL — that stays local, not on GitHub.
- Never print, log, or echo the token in reports.
