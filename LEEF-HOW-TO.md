# Editing FieldFlow — the short version for Leef

The whole app is one file, `index.html`, in this GitHub repo. Nothing goes live until
Joe approves it. Here is the entire process, no software to install.

## Make a change (about two minutes)

1. Open https://github.com/BLAstudios/fieldflow and click `index.html`.
2. Click the **pencil icon** (top right of the file, "Edit this file").
3. Make your change. Use Ctrl+F to find the text or section you want.
4. Click the green **Commit changes...** button (top right).
5. In the box that pops up:
   - Write one line saying what you changed, for example `Add install date to job card`.
   - Leave **"Create a new branch for this commit and start a pull request"** selected.
   - Click **Propose changes**.
6. On the next screen click **Create pull request**.

That's it. Joe gets a notification. When he clicks **Merge**, the live site updates on
its own within about a minute. Until then, nothing changes for anyone.

## Things to know

- **You cannot break the live site.** Your edit sits in a pull request until Joe merges
  it. If it's wrong, he just doesn't merge it.
- **Want to see it before Joe does?** Every pull request gets a preview link from
  Netlify. Look for the "Deploy Preview" link in the pull request's checks section a
  minute after you create it.
- **Bigger changes** (a new feature, something touching the database) are better as a
  request to BLA HQ, which turns them into a ticket for Claude Code. The pencil path is
  for small, visible tweaks: wording, a field, a colour, a column.
- **Never put a password or key in the file.** The only key allowed is the public
  Supabase one that's already there.
- The old copy of this file on Joe's OneDrive is retired. Edits there go nowhere.
