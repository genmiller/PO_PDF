# Order PDF Summarizer

A lightweight, browser-based tool that reads order PDFs and generates a clean size-by-size quantity summary table — no backend required.

## Features

- Upload any order PDF via drag & drop or file browser
- Automatically extracts all line items (item #, color, description, sizes, qty)
- Handles both youth sizes (YXS–YXL) and adult sizes (XS–4XL)
- Groups by item # with subtotals and a grand total
- Flags back-order items with a BO badge
- Export results as CSV
- Runs entirely in the browser — nothing is stored or sent except to the Anthropic API

## How to use

1. Open `index.html` in any modern browser
2. Enter your [Anthropic API key](https://console.anthropic.com) (stored in session only)
3. Drop your order PDF into the upload area
4. Click **Analyze PDF**
5. View the summary table and export to CSV if needed

## Setup

No build step or dependencies needed. Just open `index.html` directly in a browser.

```
git clone https://github.com/YOUR_USERNAME/order-pdf-summarizer.git
cd order-pdf-summarizer
open index.html
```

## API key

This tool uses the [Anthropic Claude API](https://console.anthropic.com) to read and extract data from PDFs. You'll need an API key:

1. Sign up at [console.anthropic.com](https://console.anthropic.com)
2. Create an API key
3. Paste it into the key field in the app

Cost is minimal — typically fractions of a cent per PDF.

## Tech

- Vanilla HTML/CSS/JS — no frameworks
- Claude claude-sonnet-4-20250514 via Anthropic API
- PDF parsed via Claude's native document understanding

## License

MIT
