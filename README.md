# Advanced Algebra

> Lecture notes and 42 weeks of fully worked homework for a course in advanced (linear) algebra, bilingual in Chinese and English, written in Markdown with inline LaTeX.

> **Note on the repository name:** the repo is spelled `advenced-algebra` (a long-standing typo) — the correct spelling is *advanced*. The name is kept for consistency with the remote URL.

The course follows **《高等代数》 (Advanced Algebra), 3rd edition, Volumes I–II, by Qiu Weisheng (丘维声)**, Peking University Press. Unlike the numbering in the other note repositories, entries here use a **flat numbering scheme** — **定义 1**, **定理 1**, **命题 1**, **基础知识 1** — without chapter prefixes.

## Repository structure

```
advenced-algebra/
├── cn/
│   ├── notes.md              # Chinese lecture notes (single file)
│   └── homework/
│       └── week1.md … week42.md
├── en/
│   ├── notes.md              # English version (complete)
│   └── homework/
│       └── week1.md … week42.md
└── textbooks/
    ├── advenced-algebra1.pdf         # Textbook Vol. I scan (270 pp.)
    ├── advenced-algebra1_ocr.pdf
    ├── advenced-algebra2.pdf         # Textbook Vol. II scan (268 pp.)
    └── advenced-algebra2_ocr.pdf
```

## The notes

`notes.md` is a single reference file organized as **8 chapters** with `##` headings:

1. Systems of linear equations
2. Determinants
3. Vector spaces and systems of linear equations
4. Matrix operations
5. Similarity canonical forms
6. Quadratic forms
7. Polynomials in one variable
8. Polynomials in several variables

The Chinese and English `notes.md` are **exactly aligned entry by entry** (549 lines / 95 entries each) — this is the most complete English translation of all the note repositories in this series.

## The homework

Each `homework/weekN.md` follows a fixed three-part format:

1. **Toolbox** — a blockquote listing the definitions and theorems needed for the week;
2. **Problems** — the assigned exercises;
3. **Solutions** — complete worked proofs ending with `$\blacksquare$`.

At **42 weeks**, this is the longest homework sequence in the series (84 homework files across the two languages).

## Bilingual layout

- `cn/` — authoritative Chinese version.
- `en/` — complete, entry-by-entry English translation with the same file structure.

## The `textbooks/` folder

The four PDFs are the scanned textbook (both volumes) plus OCR copies for text search. They are **external reference material**, not documents compiled from the notes. There is no build system; everything is plain Markdown rendered with GitHub's LaTeX support.

## Related repositories

Other course-notes repositories in the same series: [abstract-algebra](https://github.com/wenje-ma/abstract-algebra), [topology](https://github.com/wenje-ma/topology), [real-analysis](https://github.com/wenje-ma/real-analysis), and the full list on the [profile page](https://github.com/wenje-ma).
