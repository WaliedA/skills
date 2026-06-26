---
name: humanize-research
description: "Final-pass editor for AI-generated research, whitepapers, memos, and academic papers. Trigger on phrases like 'humanize this', 'remove em dashes', 'remove colons', 'cross-check citations', 'verify references', 'tighten the prose', 'edit out the AI tells', 'make publication-ready', 'pass AI detection'. ALSO TRIGGER for academic work: 'peer review', 'academic standard', 'journal submission', 'conference paper', 'thesis', 'dissertation', 'PhD paper', 'WASD paper', 'literature review', 'IMRaD', 'Harvard referencing', 'APA 7th', 'methodology section', 'limitations section', 'reviewer-ready'. Trigger broadly: any time the user pastes AI prose and asks for a final pass before publishing or submitting, even with phrases like 'clean this up' or 'tighten this'. The skill verifies citations, strips em dashes and colons per Walied's rules, removes AI tells, calibrates voice, and in academic mode restructures to IMRaD, applies citation style, audits source tiers, and produces a peer-review-readiness scorecard."
license: Proprietary to Walied Elbashir / Intuitio Ventures. Internal use only.
---

# Humanize Research

A skill for converting AI-generated research, whitepapers, and thought-leadership prose into publication-ready or peer-review-ready output with verified citations. Modelled on the Jenni AI editorial process, adapted for Walied Elbashir's standing rules (no em dashes, minimal colons) and his two operating contexts. The first is Intuitio Ventures' professional thought-leadership tone for LP, partner, and client work. The second is academic peer-review-ready output for journal articles, conference papers, working papers, theses, and dissertations, including the WASD London 2026 stream and PhD pathway work at TalTech or Sorbonne.

## When this skill applies

This skill is the final pass before any AI-assisted research leaves Walied's hands. It runs after the substantive research is done and the draft exists. It does not generate research. It refines, verifies, and humanizes existing prose.

Typical triggers:
- A research output from Claude, ChatGPT, Gemini, or another AI tool needs to be sent to LPs, clients, partners, or published.
- A draft article, memo, or whitepaper needs an AI-detection-resistant final pass.
- Citations need verification before public release.
- The user wants the prose to sound like a senior human analyst rather than an AI assistant.

## What the skill does

Six passes total, in order. Passes 1 to 4 always run. Passes 5 and 6 run only in academic mode (Mode D). Do not reorder them.

**Pass 1, citation verification.** Every numerical claim, named entity, quoted statement, and source-attributed fact gets cross-checked against the cited source. Use web_search and web_fetch. Flag any claim where the source does not actually support the statement. Correct factual errors. Update outdated figures. Remove invented citations. In academic mode, also tier the source (peer-reviewed > working paper > government/regulatory > industry report > news > blog) and audit the tier mix.

**Pass 2, formatting strip.** Remove em dashes globally. Replace with commas, periods, parentheses, or natural sentence breaks. Remove colons in headings and lead-ins. Keep colons only where they are unavoidable (time stamps, ratios written as "1:1", URLs). Replace ratios with slashes (70/30 not 70:30). Replace "as X said:" patterns with natural attributions ("X said that..."). In academic mode, additional rules apply for in-text citations and reference lists. See `references/citation-styles.md`.

**Pass 3, AI-tell removal.** Identify and rewrite the markers below. Vary sentence rhythm. Break parallel structures. Use language that is specific rather than abstract. In academic mode, an extended list of academic-prose AI tells also applies (see `references/ai-tells.md` Section "Academic register tells").

**Pass 4, voice calibration.** Match the target voice. For LP and business work, this is Walied's senior-operator voice, formal but not stuffy, confident, declarative on recommendations. For academic work, the register shifts. Hedge methodological and empirical claims appropriately ("the data suggests", "results indicate"). Stay declarative on descriptive facts ("Cursor reached $1B ARR in November 2025"). Move recommendations into a separate "Implications" or "Discussion" section rather than scattering them through analysis.

**Pass 5, academic structure (Mode D only).** Restructure the document into IMRaD or an equivalent academic shape. Abstract with structured subsections. Keywords. Introduction with explicit research questions or hypotheses. Literature review with synthesis (not just listing). Methodology with data sources, analytical approach, and scope. Findings or Analysis. Discussion that places findings in the literature and engages counterarguments. Limitations as a distinct section, not a throwaway sentence. Conclusion with contributions and future research directions. References in the chosen style. See `references/academic-structure-template.md`.

**Pass 6, peer-review readiness (Mode D only).** Run the reviewer-readiness checklist. Reproducibility check. Falsifiability check. Source-tier audit with target ratios. Counter-argument engagement. Internal consistency. AI-disclosure language. Conflict of interest and funding statements. Plagiarism risk scan. Output a Peer-Review Readiness Scorecard appended to the document. See `references/peer-review-readiness-checklist.md`.

## Pass 1, citation verification protocol

For each citation in the source draft, do the following:

1. Identify the specific claim the citation supports. Write it as a single sentence in your head before checking.
2. web_search for the source title or URL. If the source is fresh (post-2024), prefer web_fetch on the actual URL.
3. Check three things. (a) Does the source exist as cited. (b) Does it actually support the claim. (c) Are the numbers, dates, and names exactly right.
4. If the citation passes, keep it.
5. If the citation fails, do one of the following. Find a better source for the same claim. Soften the claim to match what the source actually says. Or remove the claim.
6. Track all corrections in a "Citation Cross-Check Log" appended at the end of the document.

Common failure modes to look for:
- Round numbers that look invented (always verify "$1B", "100 million", "10x").
- Quotes attributed to named individuals (always verify who said it and where).
- Statistics from "recent reports" without a named publisher (almost always need a real source substituted).
- Year claims off by one (LLMs frequently hallucinate publication dates).
- Employee counts, valuations, and revenue figures (verify against the most recent reporting, not training data).

The output of this pass is a corrected draft plus a numbered list of corrections.

## Pass 2, formatting strip protocol

### Em dashes

Walied has a standing rule. Never use em dashes (—) anywhere. Replace them with one of the following, chosen to fit the rhythm of the sentence.

| AI-tell em dash usage | Replacement |
|---|---|
| `Statement A — statement B.` | `Statement A. Statement B.` or `Statement A, statement B.` |
| `Word — clarifying phrase — rest of sentence.` | `Word, clarifying phrase, rest of sentence.` or `Word (clarifying phrase) rest of sentence.` |
| `X — meaning Y.` | `X, meaning Y.` |
| `A — and B — are both true.` | `A and B are both true.` (drop the parenthetical entirely if it adds no information) |

### Colons

Walied wants colons minimized. Allowed only where unavoidable. Default to removing them.

| Colon usage | Allowed? | Replacement |
|---|---|---|
| Heading colons ("Section 1: Introduction") | No | "Section 1, Introduction" or "Section 1. Introduction" or just "Section 1 Introduction" |
| Lead-in to a list ("The components are: A, B, C.") | No | "The components are A, B, and C." or rewrite as a sentence flowing into the list. |
| Lead-in to a quote ("As Tan said: ...") | No | "Tan said that..." or "Tan put it plainly. ..." |
| Definition lead-in ("Multiplier: a factor that...") | No | "A multiplier is a factor that..." |
| Ratios (70:30) | No | 70/30 |
| Time stamps (10:30) | Yes | Keep |
| URLs (https://) | Yes | Keep |
| Citation lead-in (per APA) | Case by case | Usually rewrite. |

### Strip routine

For each paragraph:
1. Find every em dash. Replace.
2. Find every colon. Decide if it falls in the allowed list. If not, rewrite the sentence to remove it.
3. Re-read the paragraph aloud (mentally). If the rhythm broke, fix it.

## Pass 3, AI-tell removal

### High-frequency AI tells

The following words and phrases mark AI-generated text. Remove or rewrite when they appear.

**Vocabulary tells:**
- delve, delves, delving
- navigate, navigates, navigating (when used metaphorically)
- tapestry, mosaic, landscape (when used metaphorically for "set of things")
- underscore, underscores, underscoring
- elevate, elevates, elevating (when not literal)
- robust (overused, often vague)
- leverage (as a verb in business prose, except when literally about leverage)
- in conclusion, in summary, ultimately, to summarize
- moreover, furthermore, additionally, in addition (use sparingly, prefer "and" or new sentence)
- crucial, vital, essential, paramount (overused intensifiers)
- it is important to note that, it is worth noting that
- in today's world, in the modern era, in the digital age
- pivotal, transformative, groundbreaking (overused)
- meticulously, seamlessly, effortlessly
- comprehensive (when used as filler)
- multifaceted, holistic
- realm, sphere
- harness, unlock, unleash (when not literal)
- foster, cultivate (in non-agricultural contexts)
- testament to

**Structural tells:**
- The "It's not just X, it's Y" construction (rewrite as a single direct claim).
- The "While X, Y" balancing construction overused at sentence starts.
- Triplet parallel structures (e.g., "to inform, to inspire, to ignite"). Use one or two, not three.
- Paragraphs that all start with the same construction.
- Bullet lists that contain only one or two items per bullet (collapse into prose).
- Heading immediately followed by a one-sentence summary that re-states the heading.
- Closing every section with a sentence beginning "This means..." or "In short..."

**Citation tells:**
- "According to a recent study" without naming the study.
- "Experts agree" or "Many believe" without sources.
- "Studies have shown" without specifics.
- All-caps emphasis (rewrite for force without typography).

### Sentence rhythm

AI prose has uniform sentence length. Human prose varies. After Pass 2, sample any 200-word block. Sentences should range from 4 to 35 words. Mix declarative with conditional and interrogative shapes. Use one short sentence between every two long ones, on average.

### Specificity check

Every paragraph should answer the question: "What concrete thing does this paragraph add?" If a paragraph could be deleted without loss, delete it. If a paragraph could apply to any topic, rewrite it with topic-specific detail.

## Pass 4, voice calibration

Walied's voice. Formal but not stuffy. Confident but not bombastic. Concrete tradeoffs over vague recommendations. The voice of someone who has built and run companies for 30 years and is writing for peers who are also serious operators.

Rules:
- Avoid first-person plural overuse ("we believe", "our view"). Use it sparingly. Default to the sentence subject doing the work.
- Avoid hedging language stacked together ("might potentially possibly"). Pick one.
- Use industry vocabulary precisely. Do not over-explain to a sophisticated reader.
- Where there is a hard recommendation, state it. Do not soften it with "could" or "may".
- Prefer active over passive voice where the actor matters.
- Use British English spelling when writing for the GCC/Estonian/UAE context (organisation, behaviour, programme, prioritise). Use American spelling for US/Delaware-facing content.

Length discipline:
- A long-form whitepaper or memo can run 3000 to 8000 words. Cut everything that does not earn its place.
- An LP-facing executive summary should be no more than 400 words.
- A blog post or LinkedIn article should be 800 to 1500 words unless the user specifies otherwise.

## Academic citation handling (Mode D)

Academic citation conventions create tension with the no-em-dash and minimal-colon rules. The skill resolves this with the following adapted rules.

### Title and section colons

Default behaviour. Strip them. "Title: Subtitle" becomes "Title. Subtitle" or "Title, Subtitle". Section headings become "1. Introduction" and "2.1 Methodology" without colons.

Exception. If the journal's submission system rejects the title (rare), reinstate the colon at submission stage and document it in the Changes Log. The skill does not pre-emptively use journal house style. Walied's no-em-dash and minimal-colon rules take precedence over house style by default.

### In-text citations

Default style is Harvard Author-Date. The Walied-adapted form uses commas in place of colons for page numbers.

| Convention | Standard form | Walied-adapted form |
|---|---|---|
| Author with page | (Smith 2023: 45) | (Smith 2023, p. 45) |
| Two authors | (Smith and Jones 2023: 45) | (Smith and Jones 2023, p. 45) |
| Three plus authors | (Smith et al. 2023: 45) | (Smith et al. 2023, p. 45) |
| Multiple sources | (Smith 2023; Jones 2024) | (Smith 2023; Jones 2024) (semicolon retained, this is standard and not a colon) |
| Direct quote | "quote" (Smith 2023: 45) | "quote" (Smith 2023, p. 45) |

APA 7th and Chicago Author-Date variants are documented in `references/citation-styles.md`. Each has been adapted to remove em dashes and unnecessary colons while preserving the standard's recognisability to reviewers.

### Reference list formatting

The reference list is the one place where strict no-em-dash discipline can leak. Many style guides use en-dashes in page ranges (45–67). Default behaviour for the skill is to use a hyphen instead (45-67). If a journal's submission system requires en-dashes, flag it for final-stage adjustment.

DOIs are mandatory where available. Date of access is mandatory for web sources. Format examples are in `references/citation-styles.md`.

### Source tier discipline

In Mode D, every source gets tagged with a tier marker during Pass 1. Target ratios for academic submissions are documented in `references/source-tier-hierarchy.md`. Briefly, peer-reviewed and working-paper sources should constitute the majority of the reference list for journal submissions. Industry reports and news may appear but should be flagged in a footnote where they support a load-bearing claim.

## Output structure

The skill should produce a single output document plus supporting logs.

For Modes A, B, C:
1. The humanized prose itself, complete and ready to publish.
2. A Citation Cross-Check Log listing every citation in the original draft, marked verified, corrected, or removed, with the verifying source URL.
3. A Changes Log listing each substantive correction made (factual, not stylistic).

For Mode D, additionally:
4. A Peer-Review Readiness Scorecard (eight to twelve criteria, each scored Pass / Conditional / Fail, with notes).
5. A Reviewer Response Anticipation document listing the three to five most likely reviewer objections and a one-paragraph anticipated response for each.
6. A Source-Tier Audit table showing the count and percentage of references by tier (1 to 6).

Stylistic edits do not need to be logged. Only factual corrections, citation changes, voice changes that affect meaning, and academic structural changes.

## Working modes

The skill operates in four modes depending on input.

**Mode A, full pass.** User pastes a complete draft. Run passes 1 to 4. Output the full revised document plus the Citation Cross-Check Log and Changes Log.

**Mode B, scoped pass.** User pastes a draft and asks for one specific pass (e.g., "just remove em dashes"). Run only that pass. Skip the others.

**Mode C, audit pass.** User asks the skill to assess a document's AI-tell density without rewriting. Produce a scorecard. Number of em dashes. Number of colons (with category breakdown). Top ten AI-tell words used. Citation pass rate. Estimated time to fix.

**Mode D, academic peer-review pass.** Trigger when the user asks for peer-review-ready, journal-submission-ready, conference-paper, thesis, dissertation, or "top academic standard" output. Run all six passes. Apply the citation style chosen by the user (default Harvard, alternatives APA 7th and Chicago Author-Date). Restructure to IMRaD or equivalent. Add Methodology, Limitations, Conflict of Interest, AI Use Disclosure, and Funding sections. Append a Peer-Review Readiness Scorecard. The deliverable is a Word document formatted to journal-submission standards, plus a separate Reviewer Response Anticipation document listing the three to five most likely reviewer objections and a one-paragraph anticipated response for each.

### Selecting Mode D vs Mode A

| Cue | Mode |
|---|---|
| "humanize this for an LP", "tighten for client", "make publication-ready" (no academic context) | A |
| "peer review", "journal", "conference paper", "thesis", "PhD", "WASD", "academic standard" | D |
| "I just want the em dashes out" | B |
| "score this for AI-tells" | C |
| Ambiguous: ask the user. Do not assume Mode D unless an academic cue is present. | Ask |

## Output format selection

If the user requests no specific format, default to delivering the humanized prose inline in chat for short pieces (under 1500 words) and as a docx file for longer pieces. For Intuitio Ventures-branded outputs, use the inbound-brand styling pattern as a starting point and adapt to a navy/teal Intuitio palette.

## Reference files

See `references/` directory for:

Core (used in all modes):
- `ai-tells.md`, the canonical extended list of words, phrases, and structures that mark AI prose. Includes a dedicated "Academic register tells" section for Mode D.
- `citation-verification-checklist.md`, a step-by-step verification protocol with examples. Includes the source-tiering protocol used in Mode D.
- `walied-voice-samples.md`, paragraph-length examples of the target voice for LP and business work.

Academic mode (Mode D only):
- `academic-structure-template.md`, IMRaD template, conference paper template (WASD-style), working paper template, and word-count budgets per section.
- `citation-styles.md`, Harvard Author-Date, APA 7th, and Chicago Author-Date styles adapted for the no-em-dash and minimal-colon rules. Includes DOI handling and reference-list examples.
- `peer-review-readiness-checklist.md`, reviewer-readiness criteria with Pass / Conditional / Fail scoring rubric, and a Reviewer Response Anticipation template.
- `source-tier-hierarchy.md`, the six-tier source quality framework with target ratios for journal submissions, conference papers, and working papers.

## A worked example

Input paragraph (AI-generated):

> "It is crucial to note that the venture studio model has undergone a significant transformation. The advent of AI coding tools — particularly tools like Cursor and Claude Code — has fundamentally reshaped the landscape. Studios must now navigate this new paradigm carefully: the implications are profound."

Pass 1, citations: no citations to verify.

Pass 2, formatting: two em dashes and one colon.

Pass 3, AI tells:
- "It is crucial to note that" (filler)
- "undergone a significant transformation" (vague)
- "advent of" (cliche)
- "fundamentally reshaped the landscape" (cliche stack)
- "navigate this new paradigm" (cliche)
- "implications are profound" (vague)

Pass 4, voice:
The original paragraph says nothing concrete. Replace with specifics.

Output:

> "AI coding tools have changed venture studio economics. A studio using Cursor and Claude Code can ship a production MVP in four to ten weeks with one architect and the agent stack, where the same studio in 2022 needed eight to twelve engineers and six to twelve months. The implication for studio equity models is that the 'engineering hours' input shrinks by an order of magnitude, and the multiplier on the remaining humans must rise to compensate."

Word count similar. Information density much higher. No em dashes, no colons, no AI tells, voice consistent with Walied.

## Notes for the operator using this skill

- The skill is iterative. After a first pass, re-read the output and run pass 3 again. AI tells often hide in places they did not appear in the original.
- Citation verification is non-negotiable. Skipping it breaks the value proposition of the skill, which is publication-ready output with verified sources. In academic mode, citation verification is doubly non-negotiable. Reviewers will check.
- The skill assumes the user wants the prose tightened, not blandified. Tighten ruthlessly. Cut anything that does not earn its place. Preserve interesting argument structure, sharp edges, and anything that sounds like a real person made a real decision.
- If a draft is so AI-generated that there is nothing recoverable underneath, the right move is to rewrite from outline rather than to edit. Tell the user.
- In academic mode, do not over-hedge to the point of vacuity. Reviewers respect papers that take a clear position, defend it with evidence, and acknowledge limitations honestly. They do not respect papers that hide behind hedging on every claim.
- In academic mode, AI use disclosure is now standard at most journals. Default to including a one-paragraph AI Use Disclosure section that lists which tools were used (Claude, GPT, etc.) and for what purpose (drafting, editing, citation formatting). Do not claim the work is unaided when it is not.
- For Walied's PhD pathway and WASD work, the academic register matters more than the absolute compliance with any single journal's house style. Get the structure, evidence, methodology, and limitations right. Adjust house-style details (such as en-dashes, specific citation punctuation) at submission stage.
