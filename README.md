# EPUB Reading-Level Analyzer

Drop in any **EPUB** (or plain-text file) and instantly see how hard it is to read:
its reading grade level, vocabulary richness, and the small set of words that carry
most of the book. Everything runs in your browser — **nothing is uploaded**.

> 🌐 **Try it:** https://lyhjeremy.github.io/epub-reading-level-analyzer/

## What you get
- **Reading grade level** (Flesch–Kincaid) and **reading ease** (0–100).
- **Vocabulary richness** (type–token ratio) and total/unique word counts.
- **Top words** bar chart and a **coverage curve** showing how few distinct words
  you need to follow most of the book.

This is the same lens as my [Love Island lexical analysis](https://lyhjeremy.github.io/love-island-lexical-analysis/),
turned into a reusable tool you can point at any book.

## How it works (and why it's private)
EPUB files are just ZIP archives of HTML. The app unzips the file **in your browser**
using the native [`DecompressionStream`](https://developer.mozilla.org/docs/Web/API/DecompressionStream)
API — no third-party libraries and no server. The text is extracted with the
browser's HTML parser, then tokenized and scored. Your book never leaves your device.

A public-domain sample (*Alice's Adventures in Wonderland*, Project Gutenberg) is
included so you can try it with one click.

## Tech
Vanilla HTML/CSS/JavaScript, dependency-free. Charts drawn on `<canvas>`.

## License
[MIT](LICENSE) © 2026 Jeremy Lee · Sample text is public domain (Project Gutenberg).
