---
name: daily-ai-show-arabic
description: >
  Generate a daily Arabic YouTube show script about AI news, inspired by the "Summary/سامري" channel style but focused entirely on AI instead of politics. Use this skill whenever the user asks to create, generate, prepare, write, or produce a daily AI news show, AI news episode, Arabic AI recap, or YouTube AI script. Also trigger when the user says "today's AI show", "prepare the episode", "ما أخبار الذكاء الاصطناعي اليوم", "جهز حلقة اليوم", "AI news in Arabic", "run the daily show", or any variation involving Arabic AI news content for YouTube. Trigger broadly: if the user mentions AI news + Arabic + show/script/episode/YouTube in any combination, use this skill. The skill searches the user's Gmail (walied@walied.net) for AI newsletters, extracts 7-10 top stories, and produces a full teleprompter-ready Arabic script, YouTube SEO package, thumbnail suggestions, and English source summary.
---

# Daily AI Show — Arabic (يومياتي مع الذكاء الاصطناعي)

This skill transforms AI newsletters arriving daily in the user's Gmail into a polished Arabic YouTube show, modeled after the "Summary/سامري" channel format but dedicated entirely to AI and technology.

## What This Skill Produces

Every run generates **four deliverables** saved as files:

1. **Arabic YouTube Script** (`script_ar.md`) — Teleprompter-ready, 15-20 minutes of narration
2. **YouTube SEO Package** (`seo_package.md`) — Arabic title, description, tags, hashtags
3. **Thumbnail Suggestions** (`thumbnails.md`) — 3 Arabic thumbnail text/title options with visual direction
4. **English Source Summary** (`sources_en.md`) — Story-by-story English brief with source attribution

## The Pipeline

Follow these steps in order. Do not skip steps or combine them.

### Step 1: Harvest AI Newsletters from Gmail

Search the user's Gmail for AI newsletters received in the last 24-48 hours. Use multiple queries to catch all sources:

```
Query 1: to:walied@walied.net from:(deeplearning.ai OR substack.com OR beehiiv.com OR axios.com) newer_than:2d subject:(AI OR artificial intelligence OR machine learning OR LLM OR GPT OR Claude OR OpenAI OR Anthropic OR model OR agent)
Query 2: to:walied@walied.net newer_than:2d subject:(AI OR artificial intelligence OR neural OR deep learning OR Nvidia OR Google AI OR Meta AI)
```

Read the full body of the top 5-8 most relevant newsletter emails. Prioritize these known sources (in order of editorial quality):
- **The Batch** (DeepLearning.AI / Andrew Ng) — gold standard, always use if available
- **Axios AI+** — policy and industry focus
- **Product Growth / AI by Aakash** — product and builder perspective
- **Linas's Newsletter** — crypto-AI and frontier research
- **The Founders Corner** — startup/builder angle
- **TLDR AI** — concise daily roundup
- **Ben's Bites** — community and tools
- **Import AI** — research-heavy
- **The Neuron** — mainstream accessible

If fewer than 7 stories are found from email alone, supplement with a web search for "AI news today" or "أخبار الذكاء الاصطناعي اليوم" to fill the remaining slots.

### Step 2: Extract and Rank Stories

From the harvested newsletters, extract individual stories. For each story, capture:
- **Headline** (English original)
- **Core facts** (what happened, who is involved, numbers/metrics)
- **Why it matters** (impact on industry, developers, or users)
- **Source newsletter and date**

Rank stories using this priority framework:
1. **Breaking/Major**: New model releases, major acquisitions, regulatory moves, safety incidents
2. **Industry Shifts**: Partnerships, funding rounds >$100M, platform changes, open-source releases
3. **Builder/Developer**: New tools, APIs, frameworks, developer experience changes
4. **Research**: Papers with practical implications, benchmark breakthroughs
5. **Regional/GCC**: Any AI news relevant to UAE, Saudi, or Gulf region (always include if found)

Select 7-10 stories. Always lead with the strongest story. Always close with something forward-looking or inspiring.

### Step 3: Generate the Arabic Script

The script follows the "Summary/سامري" show structure adapted for AI content. The Arabic style is **Modern Standard Arabic (فصحى) with casual Gulf touches** — think Al Arabiya anchor who also codes. Formal enough for credibility, warm enough for YouTube engagement.

Read `references/script_template.md` for the exact template structure and tone guidance before writing.

Key style rules for the Arabic:
- Write right-to-left Arabic natively, not translated-from-English Arabic
- Use Gulf colloquial expressions sparingly for warmth: "يعني" (ya3ni), "بالضبط" (bilzabt), "خلونا نشوف" (khaloona nshouf), "الحين" (alheen)
- Technical terms stay in English with Arabic transliteration on first use: "نموذج لغوي كبير (Large Language Model - LLM)"
- Numbers and metrics in Arabic numerals with Western digits in parentheses
- Never use em dashes (—) in the Arabic text. Use commas, periods, colons, or natural sentence breaks instead
- Each story segment: 1.5-2 minutes of narration (~200-250 Arabic words)
- Use the "hook → context → detail → so-what → bridge" structure per story
- Cite the source naturally: "وبحسب نشرة The Batch..." or "نقلاً عن Axios..."
- Address the viewer directly: "أنتم" (formal you) or "شباب" (guys) for casual moments

### Step 4: Generate YouTube SEO Package

Create the SEO package in `seo_package.md`:

**Title formula** (pick the catchiest):
- `[أقوى خبر] + وأخبار أخرى | يومياتي مع الذكاء الاصطناعي [التاريخ]`
- `[عدد] أخبار ذكاء اصطناعي لازم تعرفها اليوم | [التاريخ]`

**Description**: 
- Opening hook (2 lines in Arabic)
- Timestamp markers for each story (with Arabic titles)
- 3-line English summary for international discoverability
- Source credits with links
- Subscribe CTA and social links placeholder

**Tags**: 25-30 tags mixing Arabic and English:
- Arabic: أخبار الذكاء الاصطناعي, تقنية, ذكاء اصطناعي, أخبار التقنية, يومياتي مع الذكاء الاصطناعي
- English: AI news, artificial intelligence, daily AI, tech news Arabic, AI updates
- Story-specific: model names, company names, technology names

**Hashtags**: 5-8 for description and comments:
- #ذكاء_اصطناعي #AI #أخبار_التقنية #تكنولوجيا #ArabicAI

### Step 5: Generate Thumbnail Suggestions

Create 3 thumbnail concept options in `thumbnails.md`. Each includes:
- **Arabic text** (max 4-5 words, large, bold, readable on mobile)
- **Visual direction** (what the thumbnail image should show)
- **Color scheme** suggestion
- **Emotion/energy** (shock, curiosity, urgency, excitement)

Thumbnail text should be click-worthy but not misleading. Use Arabic text that creates curiosity gaps.

### Step 6: Generate English Source Summary

Create `sources_en.md` with a clean, structured English summary:
- Story number, headline, 2-3 sentence summary
- Source newsletter name and date
- Link to original (if available from email)
- How it was used in the Arabic script (which segment)

This serves as a reference document and fact-check sheet.

## Output Files

Save all outputs to the working directory, then copy final versions to `/mnt/user-data/outputs/`:

```
daily-ai-show-YYYY-MM-DD/
├── script_ar.md          # Full Arabic teleprompter script
├── seo_package.md        # YouTube title, description, tags
├── thumbnails.md         # 3 thumbnail concepts
└── sources_en.md         # English source summary + attribution
```

Use `present_files` to deliver all four files to the user.

## Show Branding

- **Show name**: يومياتي مع الذكاء الاصطناعي (My Daily AI Diary)
- **Tagline**: كل يوم، أهم أخبار الذكاء الاصطناعي بالعربي (Every day, the top AI news in Arabic)
- **Opening catchphrase**: "السلام عليكم ومرحباً بكم في يومياتي مع الذكاء الاصطناعي"
- **Closing catchphrase**: "هذا كل شيء لحلقة اليوم. لا تنسوا الاشتراك وتفعيل الجرس. نشوفكم بكرة إن شاء الله."

## Video Production

After generating the script and SEO package, the user needs to produce the actual video. Read `references/video_production_pipeline.md` for three complete production paths (fully AI-automated with HeyGen, hybrid with voice recording, and professional studio). If the user asks how to produce the video, read and follow that reference.

## Quality Checklist

Before delivering, verify:
- [ ] 7-10 stories covered
- [ ] Script reads naturally in Arabic (not translated English)
- [ ] Each story has source attribution
- [ ] Technical terms have English+Arabic on first mention
- [ ] Timestamps in SEO description match script segments
- [ ] No em dashes in Arabic text
- [ ] Gulf touches are sprinkled, not overdone (max 2-3 per story)
- [ ] Opening and closing follow the branding
- [ ] Thumbnail text is 4-5 words max and mobile-readable
