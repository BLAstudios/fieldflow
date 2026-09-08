# FieldFlow

BLA Studios' shop job-tracking app. One file: `index.html`. Backend is Supabase
project `ejjxcumzfejvgfsuuyly`; hosting is Netlify site `fieldflowhub`.

## How changes ship

1. Work happens on a branch, never directly on `main`.
2. A pull request is opened for Joe to review.
3. **Joe merges.** That merge is the deploy: Netlify publishes `main` automatically.

Nobody runs `netlify deploy` by hand any more. The old manual command is retired.

## Rules

- Check the inline JavaScript before opening a PR: `node --check` on the extracted
  script blocks (see `CLAUDE.md`).
- The only key in this file is the Supabase **publishable** key, which is safe in a
  browser and safe in this repo. Never add a service-role key, password, or token.
- Data lives in Supabase. This repo is code only.

## Local preview

Open `index.html` in a browser, or run `netlify dev` from this folder.

## History

Moved out of `OneDrive\Desktop\CLAUDE CODE\BLA Studios\FieldFlow\` on 2026-09-03.
Pre-git backups from that folder's `_backups\` were not imported; git history takes
over from here.

