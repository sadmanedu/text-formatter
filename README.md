# Text Formatter for MS Word

A browser-based formatter that converts markdown-style Bengali & English text into **Word-ready rich text** you can directly paste into Microsoft Word with bold, bullet points, underlines, headings, tables preserved.

## ✨ Features

- **Live Preview**: Type markdown on left, see Word-formatted output on right
- **Word-Compatible Copy**: Copies as `text/html` + `text/plain` so Word keeps formatting
- **Full Bengali Support**: Noto Sans Bengali, SolaimanLipi fonts, handles ১.২.৩ numbering
- **Supported Syntax**:
  - Headings: `# H1`, `## H2`, `### H3` ...
  - Bold: `**bold**` → **bold**
  - Underline: `__underline__` → <u>underline</u> (custom for Word)
  - Italic: `*italic*` → *italic*
  - Bullet: `- item` or `* item` or `• item`
  - Numbered: `1. item` , `১. item`
  - Tables: `| col | col |` markdown tables
  - Code blocks: ` ``` ... ``` ` for family trees etc
  - Horizontal line: `---`
  - Links, inline code, highlight `==text==`, strikethrough `~~text~~`

- **Export**: Download as `.doc` (Word opens directly) or `.html`
- **Offline**: No server, no data leaves browser

## 🚀 How to Use

1. Open `index.html` in browser (or run `python -m http.server 8000`)
2. Paste your raw text (like the Fatimid example) into left panel
3. See formatted output on right
4. Click **📋 Copy Formatted for Word**
5. Paste into MS Word with `Ctrl+V` → Choose "Keep Source Formatting" if prompted

## 📝 Example Input

```
# ফাতেমীয়দের পরিচয়

## ভূমিকা

ইসলামি ইতিহাসে **ফাতেমীয় খিলাফত** একটি অনন্য অধ্যায়।

- **৯০৯ খ্রি.:** উত্তর আফ্রিকা
- **৯৬৯ খ্রি.:** মিশর বিজয়

| খিলাফত | রাজধানী |
|---------|---------|
| আব্বাসীয় | বাগদাদ |
```

Output will have real bold, bullets, table borders ready for Word.

## 🎯 Why __underline__ ?

Standard markdown uses `__` for bold, but Word users often need underline. This formatter uses:
- `**` → Bold
- `__` → Underline (more useful for academic writing)
- `*` → Italic

## 📦 Files

- `index.html` – UI
- `style.css` – Styling
- `script.js` – Markdown → Word HTML parser

## 🌐 Live Preview

Run:
```bash
python3 -m http.server 8000
# open http://localhost:8000
```

For Arena preview, it auto-binds to 0.0.0.0.

## 📄 License

MIT – Free to use for academic work.
