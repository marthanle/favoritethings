# favoritethings

A curated collection of my favorite things and most useful work, built as **context for AI agents**.
The goal: give an agent enough about who I am, what I like, and how I work that its results
are specific to me instead of generic.

## Layout

| Folder | What goes here |
|---|---|
| `about-me/` | Short profile: background, goals, interests, preferences. **Start here.** |
| `work-samples/` | My best / most useful pieces of work (essays, code, projects, designs). |
| `writing-style/` | How I write and talk; examples of my voice; words I like and avoid. |
| `favorites/` | Things I love, one file per item, sorted by category (`books/`, `music/`, `film-tv/`, `food/`, `places/`, `tools-apps/`). |
| `prompts/` | Prompts that gave me great results, with notes on why they worked. |
| `references/` | Articles, links, and notes I keep coming back to. |
| `_templates/` | Copy these when adding a new entry. |
| `INDEX.md` | Auto-generated table of every entry, searchable and sortable. |
| `AGENTS.md` | Instructions telling an AI how to read this folder. |

## Adding an entry

1. Copy `_templates/entry.md` into the right folder.
2. Name it in lowercase with hyphens, e.g. `favorites/books/the-night-circus.md`.
3. Fill in the front matter (`title`, `category`, `tags`, `rating`, `added`) and the sections below it.
4. Rebuild the index:

   ```sh
   python3 scripts/build_index.py
   ```

## Searching and sorting

- **By tag:** `grep -rl "tags:.*cozy" --include=*.md .`
- **By category:** browse the folder, or look at the `Category` column in `INDEX.md`.
- **By rating:** `INDEX.md` lists entries sorted by category, then rating (highest first).
- **Full text:** `grep -ri "keyword" .`
