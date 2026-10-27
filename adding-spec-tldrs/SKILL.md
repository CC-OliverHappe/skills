---
name: adding-spec-tldrs
description: Use when a written Markdown specification needs concise summaries for easier scanning, especially when the user asks to add TL;DRs, executive summaries, or paragraph-level summaries directly to the source file.
---

# Adding Spec TL;DRs

Add concise TL;DR summaries directly to the specified Markdown specification file.

## Workflow

1. Read the complete file before making changes.
2. Identify every substantive prose paragraph and every longer or multi-sentence bullet point.
3. Add a summary immediately after each qualifying paragraph or bullet point.
4. Edit the original file in place.
5. Re-read the edited file and verify that every qualifying section has a summary and that the Markdown structure remains intact.
6. Report the file changed and the number of summaries added.

## Summary Format

Every summary must use exactly this format as a standalone Markdown paragraph:

```markdown
> **TL;DR:** <Summary>
```

Do not replace this with a blockquote, alternate label, different emphasis, or a format copied from the source file.

Use one or two concise sentences. Summarize the main requirement, decision, rationale, constraint, or conclusion. Do not introduce information that is absent from the source text.

## What to Summarize

Add a TL;DR after:

- A substantive prose paragraph containing an explanation, requirement, decision, rationale, or constraint.
- A longer bullet point containing multiple sentences or a substantial explanation.
- A bullet point that communicates an important requirement or constraint, even if it is only one sentence.

Treat wrapped lines as part of the same paragraph or bullet point. Add only one summary after the complete block.

## What to Skip

Do not add summaries after:

- Headings.
- Short labels or short, self-explanatory bullets.
- Single summarizing sentences already present in the file. 
- Checklist items that do not contain substantive explanation.
- Code blocks or inline code examples.
- Tables.
- Images, links presented on their own, or other standalone Markdown elements.
- Blockquotes unless they contain a substantive requirement that is part of the specification.
- Existing `> **TL;DR:** ...` lines.

Do not summarize a TL;DR line again.

## Markdown Preservation

Preserve the original:

- Wording and ordering.
- Heading levels.
- List markers, nesting, and indentation.
- Links, emphasis, code formatting, tables, and code blocks.
- Blank-line structure wherever possible.

Insert the summary as a separate paragraph immediately after the source paragraph. For a list item, place the summary after the complete item while preserving the surrounding list structure. Do not put the summary inside a code block or table.

If a paragraph is followed by a nested list, treat the nested list as part of that paragraph's block and place the paragraph summary after the complete nested list. Do not insert the summary between the paragraph and its nested list.

Do not rewrite, reorganize, or otherwise improve the specification unless explicitly asked.

## Quality Check

Before finishing, verify:

- Every substantive paragraph has exactly one TL;DR.
- Every qualifying longer bullet has exactly one TL;DR.
- Short bullets and excluded elements were left unchanged.
- Each summary is one or two sentences.
- Each summary begins with `> **TL;DR:**`.
- Each summary is a standalone Markdown blockquote not embedded in other blockquotes, lists, tables, or code blocks.
- No summary adds unsupported claims.
- Running the skill again would not create duplicate summaries.

If no qualifying paragraphs or bullets are present, leave the file unchanged and report that no summaries were needed.