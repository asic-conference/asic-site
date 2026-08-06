# Editing the ASIC site

You don't need to be a programmer. Every page is a single HTML file you can edit
right in your web browser. Changes publish automatically about a minute after you
save, and everything is versioned — any mistake can be undone.

## What you need

- A free **GitHub account**.
- To be added to the repository: the owner adds you under
  **Settings → Collaborators**. Once added, you can edit directly.

## Edit an existing page

1. In the repository, open the folder for the page (for example
   `2026-conference/`) and click `index.html`.
2. Click the **pencil icon** near the top-right of the file to start editing.
3. Change the text. This is HTML: edit the words **between** the angle-bracket
   tags, and leave the tags themselves alone. For example, in

   ```html
   <div class="loc">Squamish</div>
   ```

   you would change `Squamish`, but not the `<div ...>` or `</div>` parts.
4. Scroll down, write a short note describing your change, and click
   **Commit changes**.
5. Wait about a minute, then reload the live page to see it.

Tip: on any repository page you can press the **`.`** (period) key to open a
fuller in-browser editor (github.dev), if you prefer that to the pencil.

## Add a new year

The easiest way is to copy an existing year as your starting point.

1. Open the `2026-conference` folder and copy its `index.html` into a **new
   folder** named `YEAR-conference` — for example `2019-conference`.
2. In the new file, update:
   - The `<title>` line and the description near the top.
   - Leave the `← All ASIC meetings` link exactly as it is.
   - In the coloured hero area: the **year**, **location**, and **dates**.
   - Each tab's content: Home, Registration, Lodging, Dining, Travel,
     Activities, Contact. Change the text; keep the structure.
3. Commit. The new page appears at `/YEAR-conference/`.
4. Add it to the master menu: open the top-level `index.html`, find the block of
   cards (each looks like `<a class="asic-card" ...> ... </a>`), copy one, and
   update its year, location, country, and link to point at your new folder.

## Golden rules

- **Edit text, not tags.** If a `<` or `>` gets deleted by accident the page can
  look broken — but nothing is ever lost.
- **Everything is reversible.** The repository's commit history lets you roll back
  any change.
- **When unsure, propose rather than publish.** You can make changes on a separate
  branch or as a *pull request* so someone reviews them before they go live — ask
  the repo owner how they'd like the team to work.
