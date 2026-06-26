# Extended AI-Tells Catalogue

This file is the canonical extended list of vocabulary, phrases, and structural patterns that mark AI-generated prose. Use during Pass 3 of the humanize-research skill. Read this file when the SKILL.md primary list is insufficient.

## Vocabulary tells, full list

### The "elevated" register tells

Words that signal an LLM is trying to sound impressive rather than be precise.

- delve, delve into, delving
- navigate (metaphorical)
- harness, unlock, unleash, ignite
- elevate, elevates, elevating (when not literal lifting)
- foster, cultivate, nurture (when not agricultural)
- embark, embarking on a journey
- pivotal, transformative, paradigm shift, paradigm-shifting
- groundbreaking, game-changing, revolutionary (when not literal)
- unprecedented (often overused)
- meticulously, painstakingly, scrupulously
- seamlessly, effortlessly, frictionlessly
- comprehensive, thorough (when used as filler)
- holistic, multifaceted, multidimensional
- realm, sphere, domain (when "area" or "field" would do)
- testament to, a testament
- bedrock, cornerstone, foundation (when used metaphorically)
- linchpin, lynchpin
- kaleidoscope, mosaic, tapestry, symphony, choreography (when used metaphorically)
- vibrant, dynamic, thriving, bustling
- crucible, crossroads, juncture
- imperative, paramount, vital, crucial (overused intensifiers)

### The "academic gloss" tells

Phrases that mimic academic writing without doing academic work.

- It is important to note that
- It is worth noting that
- It is essential to recognize that
- It is crucial to understand that
- One cannot overstate
- It bears mentioning
- It should be acknowledged that
- It is widely accepted that
- It is generally understood
- It has been established
- The aforementioned
- The phenomenon of
- The concept of (when followed by a common-knowledge term)

### The "discourse marker" tells

Connectives that LLMs overuse to fake flow.

- Moreover, furthermore, additionally, in addition
- However, nevertheless, nonetheless (acceptable in moderation, overused)
- Consequently, therefore, thus (acceptable, overused)
- In light of, in view of, given that
- Notably, importantly, significantly (as adverbs at sentence starts)
- It follows that
- This raises the question
- This begs the question (often used wrongly)
- Be that as it may
- All things considered

### The "executive summary" tells

Phrases that signal a closing in writing that does not need closing.

- In conclusion
- In summary
- To summarize
- In closing
- To put it simply
- At the end of the day
- When all is said and done
- Ultimately
- All in all

### The "scope expansion" tells

Phrases that gesture at importance without doing the work.

- In today's fast-paced world
- In an increasingly complex landscape
- In the modern era
- In the digital age
- In the age of AI
- More than ever before
- Now, more than ever
- The world we live in today
- Our increasingly interconnected world

### The "value proposition" tells

Marketing copy disguised as analysis.

- Best-in-class
- Cutting-edge
- State-of-the-art
- World-class
- Industry-leading
- Mission-critical
- Game-changing
- Next-generation
- Bleeding-edge
- Future-proof

### The "false-precision" tells

Numerical and quantitative claims that look specific but are vague.

- "Up to X" (especially when X is a round number)
- "As much as Y"
- "Studies have shown"
- "Research indicates"
- "Experts agree"
- "Many believe"
- "It is estimated that" (without source)
- "Recent reports suggest"
- "X to Y" ranges that are suspiciously round

## Structural tells

### The triplet abuse

LLMs love sets of three. Rewrite to use one or two.

- Bad: "Strategy, structure, and synergy"
- Bad: "To inform, to inspire, to ignite"
- Bad: "Fast, efficient, and reliable"

If a triplet is genuinely earning its place (e.g., legal liability triggers), keep it. Otherwise cut.

### The not-X-but-Y construction

Often a sign of LLM padding.

- Bad: "It is not just a tool, it is a movement."
- Bad: "This is not merely about cost, but about culture."

Replace with the direct claim. "This is about culture."

### The balanced parallel

Sentences that try to sound profound through parallel structure.

- Bad: "Where there is risk, there is reward; where there is challenge, there is opportunity."

Cut, or replace with a single concrete observation.

### The over-explained sentence

LLMs add appositive clauses that explain things the reader knows.

- Bad: "Cursor, the AI coding assistant developed by Anysphere, has reached..."
- Better: "Cursor has reached..." (let the reader's context fill in if it is established)

### The redundant heading-summary pattern

Heading: "Why This Matters"
First sentence: "It is important to understand why this matters because..."

Cut the redundancy.

### The bulletpoint inflation

Lists with one-liner bullets that should be prose.

Bad:
> Key benefits include:
> - Faster delivery
> - Lower cost
> - Better quality

Better, as prose: "The studio ships faster, at lower cost, with better quality."

### The closing call-to-action

LLMs default to ending with motivation.

- Bad: "The future is bright. The opportunity is now."
- Bad: "Will you seize this moment?"

Cut. Let the analysis end where the analysis ends.

## Punctuation tells

### Em dashes

Already covered in SKILL.md. Strip globally.

### Colons in headings

Already covered. Strip globally.

### Quotation marks for "scare quotes"

LLMs use scare quotes excessively to flag a term as informal or contested.

- Bad: The "vibe coding" "revolution" is changing the "landscape".
- Better: Vibe coding has changed how studios ship code.

Use scare quotes only when a term genuinely is contested or being defined for first use.

### Semicolon overuse

LLMs use semicolons to fake sophistication. Most prose readers prefer two sentences.

- Bad: The studio ships fast; the team is small; the equity is concentrated.
- Better: The studio ships fast. The team is small. The equity is concentrated.

Or, when the semicolon really is doing connective work:

- Acceptable: The architect leads on technical risk; the partner leads on capital risk.

## Voice tells

### The royal we

LLMs default to "we" without reason.

- Bad: "We believe that AI will transform venture studios."
- Better: "AI will transform venture studios."

Use "we" only when speaking explicitly for an organisation (Intuitio, the studio team, the fund).

### The hedging stack

LLMs stack hedges.

- Bad: "It might be possible that this could potentially affect outcomes."
- Better: "This may affect outcomes." Or, sharper: "This affects outcomes."

### The qualifying onslaught

Adverbs and adjectives stacked for emphasis.

- Bad: "This is an extremely critically important fundamental shift."
- Better: "This is a fundamental shift."

## Voice-quality benchmarks (LP and business prose)

A paragraph of Walied-voice prose should pass the following tests:
1. A senior partner at a top-tier firm could plausibly have written it.
2. Each sentence makes a falsifiable claim or describes a specific mechanism.
3. The reader could not delete any sentence without losing information.
4. The prose has rhythm. Read aloud, it does not feel monotone.
5. The reader, when finished, knows something they did not know before, or sees something they already knew in a new shape.

If the paragraph fails any test, rewrite.

## Academic register tells (Mode D only)

The following appear specifically in AI-generated academic prose. They mark a paper as machine-drafted regardless of whether the substance is sound. Reviewers notice. Strip on Pass 3.

### Throat-clearing openers

- "This study seeks to delve into..."
- "The present research aims to explore..."
- "In recent years, there has been growing interest in..."
- "With the rise of [topic], it has become increasingly important to..."
- "This paper attempts to shed light on..."
- "The aim of this paper is to..." (used redundantly when already stated in the abstract)
- "It is the contention of this paper that..."

Replacements. State the research question directly. "This paper asks whether X." "We test the hypothesis that Y." "The study examines Z across the period 2024 to 2026."

### Hedging stacks

Some hedging is academic register. Stacked hedges are AI-tell.

- "It may potentially be the case that..." (pick one hedge)
- "The findings could perhaps suggest that..." (pick one)
- "It is arguably possible that..." (pick one or remove)
- "There appears to be some evidence that may indicate..." (collapse to "evidence indicates")

Rule. One hedge per claim, maximum. "Suggests" or "indicates" or "appears" but not all three.

### The literature-review filler

- "A growing body of literature suggests..."
- "Previous studies have shown..."
- "Researchers have long debated..."
- "There is consensus in the literature that..." (often false; verify)
- "Scholars have noted that..."
- "It has been widely argued that..."

Replacements. Name the scholars. "Eisenmann (2013) argues that..." "Recent studies (Smith 2024; Jones 2025) find that..."

### The findings filler

- "The results reveal that..."
- "Our analysis demonstrates..."
- "The data clearly shows..." (clearly is suspect; remove)
- "Strikingly, we find that..." (strikingly is rhetoric, remove)
- "Notably, the analysis indicates..." (notably is rhetoric, remove)

Replacements. Lead with the finding itself. "Studio teams using AI agents shipped MVPs in 4 to 10 weeks (Table 3) versus 6 to 12 months for matched non-AI-using teams."

### The discussion filler

- "These findings have important implications for..."
- "The implications of these results are far-reaching..."
- "This research contributes to the literature by..." (often used to inflate contribution)
- "Future research should explore..."

Replacements. Be specific about which literature. "These findings extend Eisenmann's (2013) studio-equity framework to AI-native production conditions, where Inventopia-style multipliers no longer fit."

### The conclusion filler

- "In conclusion, this paper has shown..."
- "To conclude, our findings underscore the importance of..."
- "This paper has made several contributions..."
- "By way of conclusion..."

Replacements. Cut the throat-clearing. State the contribution directly in one or two sentences. "The paper contributes a dual-scenario amendment to the venture-studio equity literature. It shows that under AI-native production conditions, the Inventopia 70/30 split should shift to 80/20 or 85/15."

### The "this study" overload

LLMs say "this study" a dozen times in a paper. Use it sparingly. Say "the paper" or "the analysis" or "the data" or just refer to what was done.

### The acknowledgement padding

- "The authors would like to express their sincere gratitude to..." (cut "sincere")
- "We are deeply indebted to..." (cut "deeply")
- "The first author would like to dedicate this work to..." (rare and usually inappropriate in journal articles)

Use plain language. "We thank X, Y, and Z for comments. Errors are our own."

### Calibration test for academic prose

Before submitting, read three random paragraphs aloud. Each should pass these tests:

1. Does the paragraph make a falsifiable claim or describe a specific mechanism? If not, cut.
2. Does it cite specific sources rather than gesture at a "body of literature"?
3. Does it engage with at least one counterargument or alternative explanation?
4. Could a reviewer rebuild the argument from the paragraph alone?
5. Has the paragraph survived Pass 3 with no remaining academic AI-tells from this list?

If any test fails, the paragraph is not yet peer-review-ready.
