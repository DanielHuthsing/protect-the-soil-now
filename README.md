# Protect the Soil Now! — website

This folder is the complete website for **protectthesoilnow.org**. It is a single
web page (`index.html`) with no build step, no framework, and no server code —
just open it in a browser and it works. That makes it easy to edit and cheap to
host.

## What's in here

```
protect-the-soil-now/
├── index.html          ← the entire website (text, styling, and logic in one file)
├── assets/
│   └── images/
│       ├── hero.jpg     ← the big background photo at the top of the page
│       └── README.md    ← how to swap the photo
├── documents/
│   ├── 2024-12_cup-project-description.pdf   ← the PDF the "Documents" section links to
│   └── README.md        ← how to add or replace PDFs
├── docs/
│   ├── EDITING.md        ← ★ how to change text, images, PDFs, and who gets the emails
│   └── DEPLOYING.md      ← ★ how to publish this to your Cloudflare domain
├── wrangler.jsonc        ← optional config for one advanced deploy method (see DEPLOYING.md)
├── .assetsignore         ← developer file, safe to ignore
└── .gitignore            ← developer file, safe to ignore
```

## Start here

1. **To change the website's words, photos, or PDFs** → open [`docs/EDITING.md`](docs/EDITING.md)
2. **To put the site online at your domain** → open [`docs/DEPLOYING.md`](docs/DEPLOYING.md)

## Good to know

- Everything a visitor reads lives in **`index.html`**. You edit it with any plain
  text editor (a free one like [VS Code](https://code.visualstudio.com/) is ideal).
- The "Submit Your Comment" tool builds an email in the visitor's own email app and
  sends it from **their** address to the City. Nothing is stored on a server, and
  no visitor data passes through you. See EDITING.md to change who the comments go to.
- To preview a change before publishing, just double-click `index.html` — it opens
  in your browser exactly as it will appear online.
