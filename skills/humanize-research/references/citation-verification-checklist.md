# Citation Verification Checklist

A step-by-step protocol for cross-checking every citation in an AI-generated draft. This is Pass 1 of the humanize-research skill. Skipping or shortcutting this protocol breaks the skill's primary value proposition.

## The four classes of citation that fail most often

### Class A, hallucinated sources

The source does not exist. The URL returns 404. The book or paper title was invented. The author name was fabricated, or invented by combining real names.

**Detection.** web_search for the exact title or URL. If no result returns, the source is hallucinated. Confirm with a second query that varies the wording.

**Action.** Find a real source for the same claim, or remove the claim.

### Class B, real sources, wrong claims

The source exists, but it does not say what the draft attributes to it.

**Detection.** web_fetch the source. Read the relevant section. Compare to the claim in the draft.

**Action.** Either replace the citation with one that supports the claim, or revise the claim to match what the source actually says.

### Class C, outdated figures

The source was real at one point, but the figure cited is from training data and has been superseded.

**Detection.** Numbers like revenue, employee count, valuation, market share. Always re-verify against the most recent reporting available, even if the source URL is correct.

**Action.** Update to the current figure. Cite the most recent source.

### Class D, slightly-wrong attribution

The fact is correct but credited to the wrong person, organisation, or date.

**Detection.** Verify the speaker, the publication date, and the venue. LLMs frequently muddle these.

**Action.** Fix the attribution.

## Step-by-step protocol

For each citation in the draft:

### Step 1, identify the claim

Read the sentence containing the citation. Write the claim as a single declarative sentence. For example:

- Draft sentence: "Cursor reached $1B ARR in 24 months with under 50 employees ([source])."
- The claim, parsed: "(a) Cursor reached $1B ARR. (b) The time to reach $1B ARR was 24 months. (c) Cursor had fewer than 50 employees at $1B ARR."

Each sub-claim must be independently verified.

### Step 2, check the source

If the citation includes a URL, web_fetch it. If it includes only a publication name, web_search for the title plus the publication.

### Step 3, verify each sub-claim

For each sub-claim, locate it in the source. If the source supports the claim, mark verified. If not, mark for action.

In the Cursor example:
- (a) "Cursor reached $1B ARR." Verified, multiple sources.
- (b) "The time to reach $1B ARR was 24 months." Verified, SaaStr called it the fastest in B2B history.
- (c) "Cursor had fewer than 50 employees at $1B ARR." False. Cursor had 300+ employees at the time of $1B ARR (Series D, November 2025). Action: correct the figure or remove the sub-claim.

### Step 4, apply corrections

Apply the corrections in the prose. Maintain the citation if it still supports the corrected claim. If the original source is now wrong, find a replacement.

### Step 5, log the result

In the Citation Cross-Check Log appended to the document, record:
- Original claim
- Verification result (verified, corrected, removed)
- New citation, if changed
- Source URL used for verification

## Special cases

### Quoted statements

When a draft quotes a named individual, verify three things.
1. The individual said it.
2. They said it in the context cited.
3. The quote is accurate (not paraphrased and presented as a quote).

If any of the three fails, either rewrite as paraphrase or remove the quote.

### Statistics from "studies"

When the draft cites "a study found" or "research shows", treat as Class A until proven otherwise. LLMs invent studies frequently.

Search for the study by its claimed finding. If you cannot find it in two searches with different wording, the study is likely hallucinated.

### Numbers in ranges

Ranges like "$30 billion to $50 billion" are suspicious. They are often LLM padding. Verify both bounds. If you cannot, replace with a single verified figure.

### Year-specific claims

Claims tied to specific years ("In 2024, the market was X") need year verification. LLMs frequently shift years by one. Always verify the year.

### Round numbers

"$100 million", "1 billion users", "10x improvement". Suspect these. Verify against named source. Often the real number is more specific.

## Verification volume

For a typical 5000-word whitepaper with 30 to 60 citations, full verification takes one to two hours. Do not skip it. The cost of one published falsehood, especially in an LP-facing document, is far higher than two hours of verification time.

If verification is genuinely impossible (paywalled source, dead link, region-locked), say so explicitly in the Cross-Check Log: "Could not verify, recommend the user confirm before publication."

## What "verified" means

A citation is verified when:
1. The source exists and is reachable.
2. The source supports the claim as stated.
3. The figures, dates, and attributions match the source exactly.
4. The source is current enough that the claim is still true (not superseded).

Anything less is not verified. Mark accordingly.
