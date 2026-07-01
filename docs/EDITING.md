# How to edit the site

Everything on the page lives in one file: **`index.html`**. There's no build step —
you edit the file, save it, and re-open it in a browser to see the change.

## Before you start

- **Use a plain text editor.** [VS Code](https://code.visualstudio.com/) (free) is
  best. In a pinch, macOS TextEdit works **only** if you switch it to plain text
  (Format → Make Plain Text) — otherwise it adds invisible formatting that breaks
  the page.
- **Keep a backup.** Before a big edit, duplicate `index.html` (e.g.
  `index-backup.html`) so you can always fall back.
- **Preview any change** by double-clicking `index.html` — it opens in your browser
  looking exactly like the live site.

## The one golden rule

HTML is made of **tags** in angle brackets, like `<h2>` … `</h2>`. Only change the
**words between** the tags. Leave the tags themselves (`<...>`) alone.

```html
<h2 class="section-header">Where the Housing Goes Matters</h2>
                           └── edit this text ──┘
```

If you ever see `&mdash;`, `&ndash;`, or `&amp;` in the text, those are just codes
for the characters — (em dash), – (en dash), and & (ampersand). Leave them as-is or
copy an existing one.

---

## 1. Change text you see on the page

All the on-page copy (headlines, paragraphs, bullet points) is written directly
inside `index.html`. The fastest way to find the words you want to change:

**Open `index.html`, press Ctrl-F (Windows) / Cmd-F (Mac), and search for the exact
words currently on the site.** Edit them, save, refresh your browser.

The page is organized into labeled sections, in this order:

| Section on the page | Find it by searching for | Roughly near line |
|---|---|---|
| Big headline photo (hero) | `hero-headline` | 1087 |
| "A Decision That Lasts Forever" | `id="decision"` | 1095 |
| "Our Position" | `id="position"` | 1201 |
| "Where the Housing Goes Matters" | `id="housing"` | 1290 |
| "Take Action" / comment tool | `id="action"` | 1348 |
| "Documents" | `id="documents"` | 1494 |
| Footer (name + contact email) | `footer-brand` | 1523 |

> Line numbers drift as you edit — the **search** method above is always reliable.

### The site name, page title, and contact email

- **Name in the top-left nav bar:** search `class="nav-brand"`
- **Name + contact email in the footer:** search `footer-brand` and `footer-email`
- **Browser tab title / Google result title:** search `<title>` (near the very top)

---

## 2. Change the text of the *emailed comment*

The "Submit Your Comment" tool assembles an email from pre-written paragraphs. These
are **separate** from the on-page text and live near the **bottom** of `index.html`,
inside the `<script>`, under a header that reads `COMMENT TEXT BLOCKS`.

There are three groups, and each has three versions keyed to the visitor's chosen
tone — **A** (supportive), **B** (conditional), **C** (concerned):

| What it is | Search for | Near line |
|---|---|---|
| Opening paragraph | `const OPENINGS` | 1646 |
| One paragraph per issue checkbox | `const TAGS` | 1652 |
| Closing paragraph | `const CLOSINGS` | 1690 |

Inside `const TAGS`, each number is one checkbox on the "Which issues concern you?"
step. Number **`7`** is the farm-worker-housing paragraph added for this site.

Each paragraph is text between straight quotes `'...'`. Edit the words, keep the
surrounding quotes and the comma at the end of the line. Example:

```js
7: {
  A: 'I also ask the City to look closely at where the ... housing units are sited.',
  B: 'I am also concerned about the location of the proposed ... housing.',
  C: 'The location of the proposed farm employee housing is also a concern. ...'
}
```

### Change *who receives* the comments

Just above those paragraphs, search for these four lines and edit the email
addresses between the quotes:

| Line | What it controls |
|---|---|
| `const RECIPIENTS` | Main "To:" recipients at the City |
| `const CC` | Carbon-copy recipients (currently the PC Chair + Council member) |
| `const BCC` | A blind copy for your own records (currently `contact@protectthesoilnow.org`) |
| `const SUBJECT` | The email subject line |

Separate multiple addresses with a comma and **no spaces**, e.g.
`'first@city.gov,second@city.gov'`.

---

## 3. Change the hero photo or other images

See [`../assets/images/README.md`](../assets/images/README.md) for full details.
Short version: drop a JPG named exactly **`hero.jpg`** into `assets/images/` and the
site uses it automatically. Recommended: landscape, at least 2400×1600 px, under
~600 KB. A dark overlay is applied automatically so the white headline stays readable.

---

## 4. Change or add PDFs (the "Documents" section)

See [`../documents/README.md`](../documents/README.md) for full details. Short
version: put the PDF in the `documents/` folder, then in `index.html` (search
`id="documents"`) copy one existing `doc-card` block and update its date, title,
description, and the `href="documents/..."` link to point at your new file.

---

## If something breaks

Close the file **without saving**, or restore your backup copy, and try again in
smaller steps. Because there's no build step, a broken edit can only affect the page
you're looking at — it can't damage anything else. When in doubt, compare against the
backup you made at the start.
