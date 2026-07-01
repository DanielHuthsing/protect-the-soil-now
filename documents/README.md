# Documents

All downloadable PDFs for the site live in this folder, alongside `index.html`.
The Download buttons in the site's Documents section link here directly, so
filenames must match exactly.

## File naming convention

Use this exact pattern so links stay predictable and sort chronologically:

```
YYYY-MM_short-description.pdf
```

- Start with the document's own date (year then month).
- Follow with a short, lowercase, hyphenated description.
- No spaces, no capital letters, no special characters.

## Published at launch

Drop this file in to activate the one card on the site:

### `2024-12_cup-project-description.pdf`

- **Card:** CUP Project Description (December 2024)
- **Linked from:** Documents section -> "Download" button
- **If missing:** the Download button returns a 404; the card still displays.

## Adding more documents

1. Drop the PDF here using the naming convention above.
2. In `index.html`, find the Documents section, copy an existing `.doc-card`
   block, and update the date, title, description, and the `href`
   (e.g. `documents/2025-07_city-completeness-determination.pdf`).

Examples of likely future additions:

```
2025-02_applicant-response-table.pdf
2025-04_ate-response-to-city-comments.pdf
2025-07_city-completeness-determination.pdf
2025-11_ate-traffic-management-plan.pdf
2024-12_45db-acoustics-report.pdf
2024-12_land-trust-approval-letter.pdf
```
