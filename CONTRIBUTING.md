# Contributing

Thanks for your interest in improving SEC Lessons! This document covers how to contribute.

## Reporting issues

Found a translation error, unclear explanation, or broken link? Open an issue:

- **Title**: Brief, specific (e.g., "Lesson 0003 Q2 answer is wrong" or "Spanish: 'margen bruto' should be 'margen bruto'")
- **Language tag**: Prefix with the language code, e.g., "[es] ..." or "[ja] ..."
- **Context**: Lesson number, section, what's wrong, what you expected
- **Suggested fix**: If you have one

## Proposing new lessons

We have 9 lessons. To add a 10th:

1. Open an issue with the topic, target audience, and 1-paragraph outline
2. Wait for discussion before writing — we want to maintain consistency with the existing series
3. Match the existing format: Tufte-inspired serif typography, ~10-15 min read, 3 quiz questions, "real data" boxes with Carvana examples
4. Write in **English first** — translations can come after

## Adding a new language

Want to translate this course into a new language?

1. Open an issue with the target language code and your background (native speaker? financial professional?)
2. Fork the repo
3. Create `<lang-code>/` directory with the same structure as `zh/` (lessons/, reference/, learning-records/, MISSION.md, NOTES.md, RESOURCES.md, README.md)
4. Translate file by file, keeping file names in English
5. Update the root `README.md` to add your language to the picker table
6. Submit a pull request

### Translation rules (recap)

- Translate body text only — keep SEC form codes, company names, ticker symbols, and `$` in original form
- Update `lang="..."` attribute and `<title>` tag
- Keep HTML/CSS structure intact
- File names stay in English
- Use professional financial/regulatory terminology in your target language

## Code style

The lesson HTML files follow a specific style:

- Tufte-inspired serif typography (Palatino / ET Book)
- Soft cream background (#fffff8)
- Yellow takeaway boxes
- Red blockquotes
- 3 quiz questions per lesson with `<details>` reveal blocks
- Meta navigation: `← Previous` / `Next →` links at the top

Match this style when creating new lessons.

## License

By contributing, you agree that your contributions will be licensed under CC BY 4.0.
