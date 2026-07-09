You can give Claude Code this prompt:

```text
I need you to convert my manuscript from an IEEEtran template to the official Elsevier template for submission to the Journal of Thermal Biology.

Important requirements:

1. DO NOT modify any scientific content, wording, equations, tables, figures, references, captions, or citations.
2. Preserve every section, subsection, figure, table, equation number, bibliography entry, and label exactly.
3. Only change the document structure and formatting so it follows the official Elsevier LaTeX template.

Template requirements:

• Replace
    \documentclass[lettersize,journal]{IEEEtran}
  with the appropriate Elsevier class (prefer cas-sc.cls unless cas-dc is specifically needed).

• Replace the IEEE title page with Elsevier frontmatter.

• Convert the author block to the Elsevier format using:
    - \author[]
    - \address[]
    - \cormark
    - \cortext
    - \ead

• Remove all IEEE-specific commands including:
    \maketitle
    \begin{IEEEkeywords}
    \end{IEEEkeywords}
    IEEE bibliography style
    any IEEE-specific formatting commands.

• Convert keywords to Elsevier keywords.

• Preserve the abstract.

• Keep all figures, tables, algorithms, equations, labels and references working.

• Replace the bibliography style with the appropriate Elsevier bibliography style used by the template.

• Ensure the document compiles without warnings related to the title page.

• Remove any custom author superscript macros that become unnecessary.

• Keep the paper in two-column format if the selected Elsevier template supports it.

Submission requirements from the Journal of Thermal Biology:

• The journal uses double anonymized peer review.
• The manuscript must NOT contain author names, affiliations, acknowledgements, or identifying information.
• Create TWO versions:

1. anonymized_manuscript.tex
   - Remove all author names
   - Remove affiliations
   - Remove acknowledgements
   - Remove author contributions
   - Remove funding statement if identifying
   - Remove competing interest statement only if the template expects it separately
   - Remove any identifying metadata
   - Keep everything else identical.

2. titlepage.tex
   Include:
   - Full title
   - All authors
   - Affiliations
   - Corresponding author
   - Email
   - Acknowledgements
   - Funding
   - Declaration of competing interests

Finally:

• Return a summary of every structural change you made.
• Do NOT rewrite or edit the manuscript text.
• Produce clean, production-quality LaTeX that compiles.
```

This prompt is based on the current **Journal of Thermal Biology** author guidelines, which recommend using Elsevier's LaTeX template and require a **separate title page and anonymized manuscript** for double anonymized peer review. ([sciencedirect.com][1])

[1]: https://www.sciencedirect.com/journal/journal-of-thermal-biology/publish/guide-for-authors?utm_source=chatgpt.com "Guide for authors - Journal of Thermal Biology - ISSN 0306-4565 | ScienceDirect.com by Elsevier"
