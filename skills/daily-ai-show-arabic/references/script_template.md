# Script Template — يومياتي مع الذكاء الاصطناعي

This is the exact structure to follow when generating each episode script. The script should read naturally when spoken aloud in Arabic. Think: confident, knowledgeable presenter who genuinely loves AI and wants the Arab world to keep up.

## Tone and Voice

The presenter persona is an Arab tech enthusiast based in the Gulf who reads international AI sources daily and distills them for an Arabic audience. Think of a blend between:
- The authority and structure of Andrew Ng's "The Batch" newsletter
- The engaging, source-citing narration of "قناة سامري" (Summary Channel)
- The accessibility and warmth of a Gulf-based tech YouTuber

**Voice characteristics:**
- Confident but not arrogant
- Uses "نحن" (we) to include the viewer: "خلونا نفهم ليش هالشي مهم" (let's understand why this matters)
- Explains jargon immediately but never talks down
- Shows genuine excitement about breakthroughs
- Provides measured analysis, not hype
- Occasionally uses Gulf expressions for warmth: "والله إنه شي يحمّس" (honestly, this is exciting)

## Episode Structure

### 1. COLD OPEN (المقدمة الصاروخية) — 30 seconds
Start with the single most attention-grabbing headline of the day. No greeting yet. Drop the viewer straight into the action.

```
هل تتخيلون إن إنفيديا أطلقت نموذج ذكاء اصطناعي مفتوح المصدر يتفوق على نماذج بمليارات أكثر من المعاملات؟ هذا بس واحد من [عدد] أخبار جايتكم اليوم.
```

### 2. BRANDED INTRO (التحية والعلامة) — 15 seconds
Standard greeting and show identity.

```
السلام عليكم ومرحباً بكم في يومياتي مع الذكاء الاصطناعي. أنا وليد البشير، وهذي حلقة يوم [التاريخ بالعربي]. عندنا اليوم [عدد] أخبار مهمة، خلونا نبدأ.
```

### 3. STORY SEGMENTS (الأخبار) — 1.5-2 min each

Each story follows this internal structure:

#### a) HOOK (الخطّاف) — 1-2 sentences
A punchy opening that creates curiosity or states a surprising fact.

```
شركة أمازون استثمرت خمسة عشر مليار دولار (15 مليار) في OpenAI. لكن الأهم من الرقم هو ليش، وشنو التغيير اللي بيصير في السوق.
```

#### b) CONTEXT (السياق) — 2-3 sentences
Brief background so the viewer understands the significance even if they missed previous episodes.

```
عشان نفهم هالصفقة, لازم نعرف إن OpenAI كانت حصرياً على سحابة Microsoft Azure من 2019. يعني مايكروسوفت كانت الشريك الوحيد. الحين الوضع تغير.
```

#### c) DETAIL (التفاصيل) — 3-5 sentences
The meat of the story. Facts, numbers, what was announced.

```
بحسب نشرة The Batch من DeepLearning.AI, الشراكة الجديدة بين OpenAI وأمازون تشمل بناء بيئة تشغيل ذكية للوكلاء (AI agents) على منصة AWS. الفكرة إن الوكلاء يحتاجون ذاكرة مستمرة وإدارة حالة, وهالشي ما يوفره الـ API العادي. أمازون بتستثمر 15 مليار الحين مع إمكانية 35 مليار إضافية إذا تحققت شروط معينة.
```

#### d) SO-WHAT (ليش يهمنا) — 2-3 sentences
Why this matters to the viewer, to the region, or to the AI industry.

```
ليش يهمنا هالخبر؟ لأن المطورين في المنطقة العربية أغلبهم يستخدمون AWS. لو هالمنصة نزلت, معناها بناء وكلاء ذكاء اصطناعي بيصير أسهل بكثير لأي مطور خليجي أو عربي.
```

#### e) BRIDGE (الجسر) — 1 sentence
Transition to the next story. Create a thematic or emotional bridge.

```
ومن صفقات الشركات الكبيرة, ننتقل لأخبار النماذج مفتوحة المصدر.
```

### 4. REGIONAL SEGMENT (زاوية المنطقة) — if applicable
If any AI news touches the Gulf, UAE, Saudi, or Arab world, give it its own segment with extra analysis. Frame it as "وبما إننا في الخليج..." (since we're in the Gulf...)

### 5. QUICK HITS (أخبار سريعة) — 30-45 seconds
If there are 2-3 smaller stories that don't warrant full segments, bundle them into a rapid-fire section.

```
وعندنا أخبار سريعة:
أولاً: [خبر قصير في جملة واحدة]
ثانياً: [خبر قصير في جملة واحدة]  
ثالثاً: [خبر قصير في جملة واحدة]
```

### 6. CLOSING (الخاتمة) — 30-45 seconds
Wrap up with a forward-looking statement, ask for engagement, and sign off.

```
هذا كل شيء لحلقة اليوم. لو عجبكم المحتوى, لا تنسون اللايك والاشتراك وتفعيل الجرس عشان يوصلكم كل جديد. وإذا عندكم أي خبر تبون نغطيه, اكتبوه في التعليقات.

أنا وليد البشير, وهذي كانت يومياتي مع الذكاء الاصطناعي. نشوفكم بكرة إن شاء الله. سلام.
```

## Formatting Rules for the Script File

- Use markdown headers (##) for each segment
- Include `[TIMESTAMP: MM:SS]` markers at each segment start for easy YouTube timestamp creation
- Bold the first sentence of each story (the hook) for teleprompter emphasis
- Put English technical terms in parentheses after the Arabic: نموذج لغوي كبير (LLM)
- Include `[SOURCE: Newsletter Name, Date]` after each story for quick reference
- Use line breaks between sentences for teleprompter readability (one thought per line)
- Never use em dashes. Use commas or periods for pauses instead.

## Arabic Writing Quality Markers

Good Arabic narration for this show:
- ✅ "خلونا نشوف شنو صار" (let's see what happened) — natural Gulf
- ✅ "وبحسب تقرير من..." (according to a report from...) — MSA attribution
- ✅ "الحين السؤال المهم..." (now the important question...) — Gulf transition
- ✅ "نموذج الذكاء الاصطناعي (AI model)" — bilingual technical term

Bad Arabic that sounds like machine translation:
- ❌ "تم الإعلان عن إطلاق..." (passive voice, bureaucratic)
- ❌ "في إطار التعاون المشترك بين..." (stilted formal Arabic)
- ❌ "يُذكر أن..." (newspaper filler)
- ❌ Overuse of Gulf dialect that loses non-Gulf Arabic speakers
