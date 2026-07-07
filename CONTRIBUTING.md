# Contributing

This is a living list. Adding a tool should take two minutes. Keep it simple and honest.

## What belongs here

- **Free or open-source**, or with a **genuinely useful free tier** (state the cap).
- **Basic → medium** level. If it needs real setup or know-how, flag it **●● medium** — but leave the deep/advanced/enterprise-only stuff out.
- **Widely trusted**, and downloaded from an **official site** (link the real homepage, never a mirror or "download portal").
- Actually used by IT people for real work. If you had to reach to justify it, skip it.

## The two places a tool lives

Each tool is listed in **two spots** — keep them in sync:

1. **`data/tools.js`** — the structured data that powers the searchable web page (`index.html`).
2. **`categories/NN-*.md`** — the human-readable table GitHub renders.

### 1. Add it to `data/tools.js`

Find the matching category block and add an object:

```js
{
  cat: "02",                                  // category id (see the list at the top of the file)
  name: "Tool Name",
  url: "https://official-homepage.example/",  // the real official site
  desc: "One tight sentence — how an IT tech actually uses it.",
  platform: "Win / macOS / Linux",            // or "Self-host / web", "mobile", "Bootable", etc.
  license: "OSS",                             // OSS | Free | Free (personal) | Free (tier) | Free (built-in)
  medium: true,                               // OPTIONAL — omit unless it needs extra setup/know-how
  caveat: "Free for personal use only."       // OPTIONAL — traps worth flagging
}
```

**`license` must be exactly one of:**

| Value | Meaning |
|-------|---------|
| `OSS` | Open source |
| `Free` | Free to use (may be closed-source) |
| `Free (personal)` | Free for personal use only — **not** commercial |
| `Free (tier)` | Free tier with limits (note the cap in `desc`/`caveat`) |
| `Free (built-in)` | Ships with the OS |

Use `caveat` for the honest gotchas: "free for personal use only", "free tier caps devices at N", "AV may flag it", etc.

### 2. Add a row to the matching `categories/NN-*.md`

Match the existing table format:

```md
| **[Tool Name](https://official-homepage.example/)** | One tight sentence. ●● medium. | Win / macOS / Linux | **OSS** |
```

Put the `●● medium` marker in the description if it applies, and keep the **Rule of thumb** line at the bottom of the file accurate.

## Adding a whole new category

1. Create `categories/NN-name.md` following the existing files (title, intro line, table, a **Rule of thumb**).
2. Add the category to the `categories` array **and** the tools to the `tools` array in `data/tools.js`.
3. Add a row to the table in the root `README.md`.

## Style

- One sentence per tool. Say what it *does* and when you'd reach for it — not marketing copy.
- No affiliate links, no "download portals," no bundled-installer sites.
- Be honest about limits. "Free tier caps at 100 sensors" beats pretending it's unlimited.

## Check your work

Open `index.html` in a browser (double-click works — no build step) and confirm your tool shows up, searches correctly, and the badges look right.
