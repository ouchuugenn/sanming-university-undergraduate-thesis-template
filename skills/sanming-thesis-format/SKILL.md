---
name: sanming-thesis-format
description: Review and correct LaTeX formatting for Sanming University undergraduate theses against the bundled 2018 writing guide. Use when auditing or adjusting thesis layout, front matter, headings, figures, tables, equations, citations, or references; preserve the author's research content and established template design.
---

# Sanming University Thesis Formatting

Use this skill to audit and, when requested, correct a LaTeX undergraduate thesis against the bundled 2018 guide:

`../../附件3：三明学院毕业论文(设计)撰写规范要求(明学院教字[2018]31).pdf`

Treat that PDF as the source of institutional requirements. Keep mandatory rules separate from recommendations. The guide permits colleges to make discipline-specific adjustments, so honor a supplied, approved local specification when it is explicit and report any conflict with the 2018 guide rather than silently overriding it.

## Workflow

1. Identify the project root, main TeX file, included source files, bibliography, and current build method. Read project instructions and inspect the existing layout before editing.
2. Check the source and, when available, the compiled PDF. Use PDF text extraction for content checks and rendered pages for margins, typography, spacing, alignment, headers, footers, and page breaks.
3. Report findings by severity and cite the relevant guide rule or page. Distinguish a confirmed violation from a visual judgment or a recommendation.
4. If asked to fix issues, edit the responsible `.tex`, `.cls`, or `.sty` sources. Preserve the template's established design and the thesis's research claims, wording, structure, figures, tables, equations, and citations unless the user asks for content edits. Do not edit generated build files as a substitute for source changes.
5. Compile with the project's available XeLaTeX workflow and inspect the affected pages in the resulting PDF. If compilation or visual checking is unavailable, state that limitation and do not claim the layout was verified.
6. Summarize each fix and any unresolved conflict or limitation. Do not commit, push, or publish the project unless explicitly requested.

For cover-text-only edits, treat the cover layout source as locked: change only the requested field values in `content.tex`. Do not edit the cover block or its layout macros in `main.tex`. Before finishing, inspect the diff and confirm that no cover-layout code, labels, typography, alignment, or spacing changed. If a requested value wraps or overflows, preserve the layout and report the limitation instead of adjusting it. If the user explicitly requests a specific cover-layout correction, change only the named element(s), keep all other cover geometry fixed, and update the nearby `COVER LAYOUT LOCK` comment when needed so it reflects the exception.

## Formatting checklist

### Page setup and pagination

- Use A4 paper.
- Margins: top 2.5 cm, bottom 2.4 cm, left 2.8 cm, right 2.2 cm.
- Use fixed 22 pt line spacing in the body and in sections where the guide specifies it. Keep character spacing at the default value unless a documented local rule says otherwise.
- Header and footer distances from the page edge: 1.7 cm and 1.5 cm, respectively.
- Center headers in small-five Song font. Odd-page header: `××届××专业毕业论文（设计）`; even-page header: `×××（作者姓名）：××××（论文题目）`.
- Begin page numbering at the main text, centered, with Arabic numerals (1, 2, …). Check that front matter does not consume visible body page numbers.

### Required order and standalone pages

The bound thesis sequence is: cover; table of contents; Chinese title, abstract, and keywords; main text; references; English title, abstract, and keywords; acknowledgments; commitment and authorization forms. The English title/abstract/keywords occupy one separate page, acknowledgments occupy a separate page, and the commitment and authorization forms are combined on one page. Appendices are optional; include only when relevant or required by the discipline. Other archival materials listed by the guide are not necessarily pages inside the bound thesis.

Check that the cover is separate. The guide refers to the official cover issued by the Academic Affairs Office; do not recreate or redesign it when an approved cover is supplied. Check that the table of contents is separate.

For this user's Sanming University template, appendices are required to stay enabled: keep `\IncludeAppendicestrue` in `content.tex` and preserve the appendix pages during formatting, review, and compilation. Do not disable the appendix switch or remove appendix sections merely because the institutional guide treats appendices as optional. Keep editable placeholders when appendix material has not yet been supplied; replace them with the user's material when available.

### Cover and table of contents

- Fill the student number and full major name in full; do not abbreviate them.
- Treat the cover layout and labels as locked template source. For content-only requests, change only the text values printed on existing underlined fields (for example, `\ThesisTitle`, `\ThesisMajor`, and `\ThesisAuthor` in `content.tex`). Do not edit the cover block or cover layout macros in `main.tex`. Do not rewrite labels such as `题　　目：`, change the logo or heading, move any cover element, or alter typography, alignment, or spacing. A direct, specific user request to change a named layout element is an exception: make only that requested correction and preserve every other cover element. After editing, inspect the diff to ensure changes stay within that scope.
- Preserve the existing title wrapping and centering behavior. If a title wraps, keep its wording intact and use the existing right-hand title field. Do not change the vertical distance between any cover underlines to accommodate a longer or shorter value; leave the underline row spacing exactly as defined by the template. Preserve the template's sample title `基于xxx的系统设计` unless the user asks to change it.
- Set `目录` in centered four-size Hei. Set entries in small-four Song with fixed 22 pt spacing; align page numbers at the line end and connect entries to page numbers with dotted leaders.

### Chinese title, author, affiliation, abstract, and keywords

- Chinese title: generally no more than 20 Chinese characters, four-size Hei, centered, on one or two lines. If it derives from a funded or other project, put the project name and number at the lower left of this page.
- Put the author one blank line below the title; use centered small-four Song.
- Put the affiliation on the next line in centered five-size Song, following the guide's pattern: `三明学院 XX 级 XX 专业，福建三明 365004`. Replace cohort and major with the student's actual information; retain the location and postal code.
- Aim for about 200 Chinese characters in the abstract. State the purpose, method, content, and main results concisely in the third person.
- Set `摘要` in top-aligned small-four Hei; set abstract text in five-size FangSong with fixed 22 pt spacing.
- Use 3–5 keywords. Set `关键词` in small-four Hei and the terms in five-size FangSong, separated by semicolons.

### Main text and technical elements

- Body text: five-size Song, fixed 22 pt line spacing, default character spacing.
- First-level headings: small-four Hei. Lower-level headings: five-size Song.
- For science and engineering, use decimal numbering such as `1`, `1.1`, `1.1.1`; left-align, then leave a space before the heading text. Humanities numbering and indentation differ; do not apply science/engineering numbering blindly to another discipline.
- An introduction may be unnumbered. Number the conclusion in the normal sequence when present. An introduction and conclusion are recommended, not stated as mandatory.
- Figures: number by chapter (`图3-1`); place a centered small-five Song caption below the figure. If a figure is cited, put its source at the upper left of the figure title. For bilingual captions, use small-five Times New Roman for English and small-five Song for Chinese. Label subfigures at their upper left and explain their labels below the caption.
- Tables: number by chapter (`表3-1`); put a centered small-five Song title above the table. Use small-five Song in cells, indicate units with the required symbols, and use a three-line table where practicable (the guide says this is the principle).
- Equations: set on their own centered line. Put the chapter-based number in parentheses at the right margin, without a dotted leader between equation and number. Short unreferenced formulas may remain inline; complex unnumbered equations may be centered on their own line.
- Notes explain or supplement a specific point. Mark them with circled Arabic numerals and place note text after the main text and before references.

### References and citations

- Include more than 10 references; prefer recent sources. The count is a guide requirement, but relevance and verified metadata still matter.
- Use numeric citations in order of first appearance. Repeated citations to the same work reuse its original number. Place citation markers as superscript bracketed Arabic numerals in the text.
- List references at the end of the main text in first-citation order. Set the heading `参考文献` in five-size Hei, left-aligned; set entries in small-five Song. End every entry with a period.
- Check that each listed work is cited in the text and that every citation resolves to a bibliography entry. Never fabricate missing authors, titles, publication details, page ranges, identifiers, or URLs; flag incomplete records for verification.
- Check the document type and available details against the guide's patterns:
  - Book/monograph `[M]`: author, title, place, publisher, year, pages.
  - Journal `[J]`: author, title, journal, year, volume(issue), pages.
  - Conference: author, paper title `[A]`, proceedings title `[C]`, publication place, publisher, year, pages.
  - Thesis `[D]`: author, title, place, institution, year.
  - Report `[R]`: author, title, report place/host, year.
  - Patent `[P]`: owner, title, country, patent number, publication date.
  - Standard `[S]`: standard code, title, place, publisher, year.
  - Newspaper `[N]`: author, article, newspaper, publication date, edition/page.
  - Electronic sources: use the appropriate source and carrier markers, such as `[J/OL]`, `[DB/OL]`, or `[EB/OL]`, and include the available access address and dates as specified in the guide.

The guide's source examples use slightly different punctuation conventions. Preserve the required fields and source markers, then apply one consistent punctuation style compatible with the thesis's chosen bibliography style. Do not convert citation or reference systems unless the source and the compiled output can both be checked.

### English abstract, acknowledgments, and length

- Put English title, abstract, and keywords together on one separate page. Use small-four Times New Roman for the English title and the words `Abstract` and `Keywords`; use five-size Times New Roman for abstract and keyword text; use fixed 22 pt line spacing and default character spacing.
- Render the author's name in Hanyu Pinyin: surname all caps, given name initial capitalized, and hyphenate a two-part given name (for example, `ZHANG Xin-ming`).
- Keep the Chinese and English front-matter content synchronized as an agreed template convention: the English title must express the same topic and scope as the Chinese title; author identity and cohort/major affiliation must match; and the English abstract must cover the same research objective, subject, method, validation conditions, key findings, and conclusion as the Chinese abstract. Translate or rewrite naturally rather than word-for-word, but do not add, omit, or strengthen factual claims in either language.
- Keep the keyword concepts and their count aligned across Chinese and English. When changing one language's title, author, affiliation, abstract, or keywords, inspect and update its counterpart in the same edit. In this template, the paired fields are macros in `content.tex`; if information is missing, retain a clear placeholder and report it instead of inventing details.
- Preserve the established page order and layout while synchronizing content: English title, author, affiliation, abstract, and keywords remain together on the English abstract page. Do not move the English content to a different page or change its formatting to compensate for a translation-length difference; adjust wording or line breaks within the existing layout and visually check the compiled page.
- Acknowledgments: separate page; heading `致谢` centered in small-four Hei, body in five-size Song with fixed 22 pt line spacing.
- Length guidance: normally at least 8,000 Chinese characters for humanities, 7,000 for science/engineering, 5,000 English words for English majors, and 3,000 characters of explanatory text for design projects. Apply the threshold that matches the discipline and thesis type; report it as a length check, not a layout defect.

## Editing boundaries

- Do not replace meaningful thesis text with sample prose, or change technical claims to make a page fit.
- Do not invent or normalize student details, author identity, project numbers, references, or approval status. Keep placeholders where information is unknown and identify them in the report.
- Fix layout at the narrowest responsible source location. Avoid global spacing or geometry changes when a local correction is sufficient.
- If the PDF guide and an explicitly supplied official template conflict, preserve the official template and report the discrepancy for the department to resolve; do not claim full compliance for conflicting rules.
