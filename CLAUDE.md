# FieldFlow repo — instructions for Claude Code

This is the canonical source of the FieldFlow app (BLA Studios). Owner: Joe.
Read `..\..\Users\joe\OneDrive\Desktop\CLAUDE CODE\CLAUDE.md` for the wider handoff
rules with the Cowork hub (BLA HQ); they apply here too.

## Hard rules
- **Never commit to or push `main`.** Branch (`fix/...`, `feat/...`), commit, push
  the branch, open a pull request. Joe merges. The merge is the deploy.
- Before opening a PR, syntax-check the inline JS:
  `node -e "const fs=require('fs');const h=fs.readFileSync('index.html','utf8');const m=[...h.matchAll(/<script(?![^>]*src=)[^>]*>([\s\S]*?)<\/script>/g)];fs.writeFileSync('/tmp/ff.js',m.map(x=>x[1]).join('\n;\n'))" && node --check /tmp/ff.js`
- Keep it one file unless a ticket says otherwise. No build step, no framework.
- No secrets. The Supabase publishable key already in `index.html` is the only key
  allowed. Service-role keys, passwords, and tokens never enter this repo.
- Schema changes are not made here; they are Supabase migrations under the
  handoff protocol. This repo only changes what the browser runs.
- The OneDrive copy at `...\BLA Studios\FieldFlow\index.html` is retired. Do not
  edit it; do not copy from it.

## Verifying a change
Open `index.html` in the in-app browser (or `netlify dev`) and click through the
screen you touched. Log in with Joe's account only if Joe is present; otherwise
verify the pre-login screen and the code path by reading.
