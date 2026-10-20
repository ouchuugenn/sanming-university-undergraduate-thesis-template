# Chinese Thesis Template

This is a blank-content copy of the formatting and page structure used by the supplied Sanming University thesis project.

- main.tex retains the original page setup, font setup, headings, headers and footers, cover, abstracts, contents, bibliography layout, declaration page, and appendices.
- content.tex contains example metadata and drafting prompts inside a generic chapter outline.
- figures/sanming_logo.png is the original cover image.
- references/refs.bib contains 14 converter-control entries for demonstrating sequential numeric citations and bibliography output. Verify each record in Zotero, then replace the examples with sources actually cited in the thesis.

Replace the title and author examples in content.tex, then fill in grade, major, student number, advisor, and date. The Chinese abstract page places the title, author, and affiliation above the abstract and keywords. The English abstract page follows the same order in English: title, author, affiliation, abstract, and keywords. Keep both affiliation lines centered and on one line; include grade/year, major, Sanming University, Fujian Sanming, and postal code 365004, with visible spacing around the location and postal code. The Chinese and English abstracts, keyword lists, and acknowledgment are drafting examples; replace the bracketed prompts and all sample wording with content that reflects the completed research and actual contributions. The body chapters also contain drafting prompts to demonstrate the original chapter, section, subsection, and paragraph formatting. Replace every prompt with your own research content before submission, and do not change the formatting commands in main.tex.

The running header uses `xx届电子信息工程专业毕业论文（设计）` on odd pages; replace `xx` with the correct cohort year when preparing a thesis.

The supplied 2018 writing guide requires more than 10 references, recommends recent sources, and requires every listed source to be cited in the text. Use sequential numeric citations in order of first appearance, formatted as superscript bracketed numbers; the bibliography follows the citation order. The template uses the numerical GB/T 7714 style and prints entries in small Song font with bracketed numbering, without a period after the bracketed number. The sample literature-review paragraph and sample records are only for demonstrating this workflow; replace them with verified, topic-specific sources before submission. The guide lists common source types and markers, including books [M], newspapers [N], journal articles [J], theses [D], reports [R], conference papers [C], compilations [G], patents [P], standards [S], and electronic resources such as [J/OL] and [EB/OL].

The body uses fixed 22 pt line spacing. First-level numbered headings use 12 pt bold Hei; lower-level headings and body text use 10.5 pt Song. Figure and table captions use 9 pt Song, centered; table cells can use `\ThesisTableFont`. Number figures and tables by chapter as `图3-1` and `表3-1`. Use three-line tables, place table captions above tables and figure captions below figures, and number equations by chapter with the equation number in parentheses at the right margin. Three editable appendix pages are included as examples; replace their prompts with relevant material or remove only the appendix pages that do not apply to the final thesis. The guide also recommends about 200 Chinese characters for the abstract, 3–5 keywords, at least 7,000 Chinese characters for science and engineering theses, and at least 3,000 characters of explanatory text for design projects.

Compile with XeLaTeX. The current source uses font files from the TeX Live 2026 installation at `/usr/local/texlive/2026`; adjust those paths in `main.tex` if your TeX Live installation uses another location.

## License

The template source, example text, and project documentation are available under the MIT License; see `LICENSE`. The Sanming University logo and the bundled 2018 thesis-writing guide are third-party materials included as references and are not relicensed by this repository.
