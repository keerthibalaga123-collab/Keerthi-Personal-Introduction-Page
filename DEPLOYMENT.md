# Deployment & Rollback Notes

## GitHub Pages Deployment

1. Push the project to a public GitHub repository.
2. Open the repository on GitHub.
3. Go to **Settings → Pages**.
4. Under **Build and deployment**, select **Deploy from a branch**.
5. Select:
   - Branch: `main`
   - Folder: `/ (root)`
6. Save.
7. GitHub will provide the published website URL.

## Rollback Evidence

Only fill this section after performing a real rollback.

### Example evidence format

- Stable commit: `PASTE_REAL_COMMIT_HASH`
- Change introduced in newer commit: `DESCRIBE_REAL_CHANGE`
- Rollback commit/action: `PASTE_REAL_ROLLBACK_HASH`
- Date/time: `PASTE_REAL_DATE_AND_TIME`
- Result: `DESCRIBE WHAT YOU VERIFIED`

### Useful Git commands

View commits:

```bash
git log --oneline
```

Create a rollback commit:

```bash
git revert <commit-hash>
git push origin main
```

Verify the deployed website after GitHub Pages finishes rebuilding.

Never submit made-up commit hashes, screenshots, or rollback results.
