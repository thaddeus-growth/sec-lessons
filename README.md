# SEC Lessons — Competitive Intelligence through SEC Filings

> A self-paced course teaching the **domain knowledge** behind using US public-company disclosures (10-K, 10-Q, 8-K, Form 4, 13F, 13D/G) for competitive intelligence and cross-holding analysis.

**Available in 7 languages** — pick yours:

| Language | Code | Directory | Status |
|----------|------|-----------|--------|
| 🇨🇳 中文 (Chinese, original) | `zh` | [`zh/`](./zh/) | ✅ **Complete** — all 9 lessons + learning records + reference |
| 🇺🇸 English | `en` | [`en/`](./en/) | 🟡 **6/9 lessons** — 0001-0006 done; 0007-0009 + learning records in progress |
| 🇰🇷 한국어 (Korean) | `ko` | [`ko/`](./ko/) | 🟡 **1/9 lessons** — all learning records + meta files done; lessons in progress |
| 🇪🇸 Español (Spanish) | `es` | [`es/`](./es/) | 🔴 **1/9 lessons** — meta files done; lessons mostly in progress |
| 🇩🇪 Deutsch (German) | `de` | [`de/`](./de/) | 🔴 **1/9 lessons** — meta files done; lessons in progress |
| 🇯🇵 日本語 (Japanese) | `ja` | [`ja/`](./ja/) | 🔴 **2/9 lessons** — lessons in progress |
| 🇫🇷 Français (French) | `fr` | [`fr/`](./fr/) | 🔴 **1/9 lessons** — lessons in progress |

> **Translations are a work in progress.** Primarily contributed by a model with occasional tool issues. If you are a native speaker of es/ja/ko/de/fr and can help complete the translations, please see [CONTRIBUTING.md](./CONTRIBUTING.md) — contributions welcome!

## What is this course?

This is a **9-lesson series** that teaches you how to monitor public companies using their SEC filings. It was originally built for a strategy team at a Chinese used-car company preparing for IPO, but the domain knowledge (US capital markets, EDGAR, 13F, Form 4, Schedule 13D/G, cross-holding analysis) is universal.

The course is **language-agnostic** — all examples use US public companies (Carvana, Carmax, AutoNation, AutoHome, Uxin) and US dollars. Translations keep company names, SEC form codes, and field names in their original English form so you can cross-reference EDGAR directly.

## Curriculum — 9 lessons

| # | Lesson | Topic |
|---|--------|-------|
| 0001 | [SEC Filing 101](./zh/lessons/0001-sec-filing-101.html) | 10-K, 10-Q, 8-K — the three core forms |
| 0002 | [Financial Metrics for Used-Car Industry](./zh/lessons/0002-financial-metrics-used-car.html) | Gross margin, SG&A, inventory, working capital |
| 0003 | [8-K Events Deep Dive](./zh/lessons/0003-8k-deep-dive.html) | When an 8-K matters enough to escalate |
| 0004 | [Earnings Call Strategy](./zh/lessons/0004-earnings-call.html) | Reading management's tone, not just numbers |
| 0005 | [Competitor Monitoring Framework](./zh/lessons/0005-monitoring-framework.html) | Why these 5 peers, what to watch on each |
| 0006 | [13F Institutional Holdings](./zh/lessons/0006-13f-institutional-holdings.html) | The data backbone for cross-holding analysis |
| 0007 | [Form 3/4/5 Insider Trading](./zh/lessons/0007-form4-insider-trading.html) | Reading insider sentiment with weighted scoring |
| 0008 | [Schedule 13D/G Activist Investors](./zh/lessons/0008-13dg-activist-investors.html) | Who's trying to change the company |
| 0009 | [Cross-Holding Methodology](./zh/lessons/0009-cross-holding-methodology.html) | How to assemble a complete analysis report |

**Recommended order**: 0001 → 0002 → 0003 → 0004 → 0005 → 0006 → 0007 → 0008 → 0009 (linear dependency).

Each lesson is a self-contained HTML file, ~10-15 minute read, with 3 quiz questions at the end.

## Repository structure

```
sec-lessons/
├── README.md           ← you are here (language picker)
├── en/                 ← English version
│   ├── MISSION.md
│   ├── NOTES.md
│   ├── RESOURCES.md
│   ├── lessons/        (9 HTML files)
│   ├── reference/      (SEC form types cheat sheet)
│   └── learning-records/  (9 markdown files)
├── zh/                 ← Chinese version (original)
├── es/                 ← Spanish
├── ja/                 ← Japanese
├── ko/                 ← Korean
├── de/                 ← German
└── fr/                 ← French
```

Each language is self-contained. Pick your language, open the `lessons/` folder, start at `0001-*.html`.

## How to read

- **Start at Lesson 0001** — every later lesson depends on concepts from earlier ones.
- **Don't skip the quizzes** — the questions are designed to surface common misjudgments. The most valuable learning comes from the "gotcha" questions.
- **Use the reference cheat sheet** — [`reference/sec-form-types.html`](./en/reference/sec-form-types.html) is printable. Keep it next to your monitor.
- **Re-read after 1 week** — the second pass has a much higher retention rate than the first.

## Contributing

- **Errors or unclear explanations?** Open an issue in your language.
- **Want to add a new language?** Open an issue; the pattern is straightforward (translate everything in `zh/` into your target language, mirror the structure under `xx/`).
- **Want to add a 10th lesson?** Open an issue with a topic proposal.

## License

CC BY 4.0 — share, remix, attribute. If this course helps you, attribute `@thaddeus-git` and link back to this repo.

## Acknowledgments

Originally developed for an internal competitive-intelligence training program. The 13F / Form 4 / 13D-G lessons (0006-0009) were inspired by IHS Markit's P4 cross-holding report, reproduced from public-domain 13F data via the SEC EDGAR API.
