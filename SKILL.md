---
name: cut-the-slop
description: Write and rewrite prose with source fidelity, natural progression, concrete language, varied structure, and restrained rhetoric. Use when a user asks to humanize writing, make text sound natural, remove AI-writing tells, clean up generated prose, reduce robotic or formulaic phrasing, match a supplied human voice, or avoid recurring LLM habits such as manufactured contrasts, repeated claims, slogan cadence, fake precision, abstract filler, mirrored syntax, rhetorical endings, and excessive structural symmetry.
---

# Cut the Slop

Produce clear, specific, natural prose while preserving the user's meaning, facts, terminology, and intended voice.

Do not imitate human writing by adding errors, fake anecdotes, invented opinions, arbitrary fragments, slang, or artificial casualness.

Do not make claims about AI detectors, detection probability, or guaranteed human classification.

## Reference navigation

Use the files in `references/` as part of this Skill.

### Required on every invocation

Read:

`references/patterns.md`

before drafting, rewriting, or reviewing prose.

This is the canonical reference for:

- pattern definitions
- detection signals
- decision tests
- legitimate exceptions
- short Avoid / Prefer examples

Do not rely only on the abbreviated pattern list in this file.

Do not begin the writing or rewriting task until `references/patterns.md` has been consulted.

### Load when the genre matters

Read:

`references/genres.md`

when the requested output has a recognizable genre, including:

- email
- chat or direct message
- product copy
- landing-page copy
- documentation
- technical writing
- analysis
- article or essay
- case study
- social post
- executive writing

Load only the guidance relevant to the current genre.

Also consult its voice-matching guidance when the user provides human-written reference samples.

### Load when detection or rewriting is ambiguous

Read:

`references/examples.md`

when:

- a pattern is difficult to classify
- a legitimate construction resembles a formulaic one
- multiple patterns interact in one passage
- several attempted rewrites still feel formulaic
- the user asks why wording sounds generated
- the short example in `patterns.md` is insufficient
- a detailed before/after comparison would help

Use examples to understand the transformation.

Never transfer names, facts, claims, numbers, or subject matter from an example into the user's writing.

### Load for document-level review

Read:

`references/audit.md`

when:

- the output is long-form
- the document contains several sections
- the user requests a careful final polish
- the writing is intended for publication or submission
- repeated claims may appear across distant sections
- section-level symmetry may be present
- sentence-level edits may have created document-level repetition

Run the audit silently unless the user asks to see the findings.

## Loading sequence

Follow this sequence whenever the Skill activates:

1. Read this `SKILL.md`.
2. Read `references/patterns.md`.
3. Identify the task, audience, genre, and source constraints.
4. Read `references/genres.md` if genre-specific guidance applies.
5. Draft or inspect the text.
6. Consult `references/examples.md` if detection or rewriting remains uncertain.
7. Read `references/audit.md` for substantial or publication-ready work.
8. Return the requested writing without exposing the internal review unless asked.

Do not load every reference automatically.

`references/patterns.md` is the exception. It is required because it defines the pattern system used by this Skill.

## Priority order

Apply these priorities in order:

1. Preserve factual accuracy and source fidelity.
2. Satisfy the user's request.
3. Preserve intended meaning and necessary terminology.
4. Make the writing useful and specific.
5. Maintain natural progression.
6. Remove formulaic writing habits.
7. Improve rhythm and presentation.

Never sacrifice factual support to make prose sound more natural.

## Source discipline

Use details supported by:

- the user's supplied material
- information established in the conversation
- supplied sources
- verified research when research is part of the task
- reliable general knowledge when appropriate

Do not invent:

- names
- dates
- statistics
- quotations
- studies
- customers
- companies
- product behavior
- personal experiences
- witnessed observations
- implementation details
- examples presented as factual

When the available evidence is general, keep the prose general.

When a specific claim lacks support, remove it, qualify it, or ask for the missing information when that information is essential.

During a rewrite, preserve the substantive claims in the source unless the user asks for fact-checking, correction, expansion, or research.

## Information progression

Make each sentence earn its place.

A sentence should usually contribute at least one useful element:

- fact
- mechanism
- reason
- consequence
- example
- constraint
- exception
- distinction
- action
- supported interpretation
- necessary context

Treat repeated meaning as repetition even when the wording changes.

Once an idea is clear, move forward.

Do not restate it as:

- a slogan
- a maxim
- a rhetorical question
- a conceptual label
- a summary sentence
- a mirrored sentence
- a synonym-heavy paraphrase
- a dramatic fragment
- a section-ending punchline

Prefer deletion when a sentence adds no information.

## Write from substance

Start with the material the reader needs.

Prefer concrete actors, actions, mechanisms, and consequences.

Name who does something when the source supports that information.

Use abstract language when the subject genuinely requires it.

Rewrite abstract noun chains when a clearer actor and action are available.

## Natural structure

Let the subject determine:

- sentence length
- paragraph length
- section length
- number of sections
- headings
- list length
- transitions
- endings

Allow unevenness when the information itself is uneven.

Do not give every section the same internal structure.

Avoid repeated templates such as:

1. claim
2. contrast
3. explanation
4. slogan

Vary structure because the content changes.

Do not manufacture variation for its own sake.

## Core pattern index

Use `references/patterns.md` for the full detection rules.

Continuously watch for:

- manufactured contrast
- negative parallelism
- artificial binaries
- mirrored syntax
- reflexive groups of three
- unnecessary groups of four
- fake numerical structure
- false ranges
- over-clean taxonomies
- repeated claims
- restated headings
- redundant qualification
- abstract noun stacking
- significance inflation
- inflated stakes
- pseudo-profound compression
- concept labeling
- micro-manifesto language
- thematic keyword saturation
- synonym rotation
- generic openings
- mechanical signposting
- rhetorical questions with immediate answers
- generic conclusions
- quotable closing lines
- unsupported absolutes
- repeated sentence cadence
- repeated paragraph architecture
- repeated section architecture
- model-favored vocabulary
- excessive formatting
- substitution of one formulaic pattern for another

Do not treat individual phrases as automatic violations.

Use the decision tests and exceptions in `references/patterns.md`.

## Pattern substitution

Do not fix one formulaic habit by replacing it with a nearby one.

Examples:

- em dash → semicolon without changing the sentence
- "not X but Y" → "rather than X, Y"
- triad → list of four
- one inflated verb → another inflated verb
- slogan → synonymous slogan
- conclusion → recap

Fix the underlying structure.

## Contrast

Use contrast when the material contains a real distinction.

Avoid manufacturing opposition merely to create emphasis.

Common suspicious forms include:

- not X, but Y
- not just X, but Y
- it is not about X; it is about Y
- X does this. Y does that.

Do not remove legitimate factual contrast.

Use `references/patterns.md` to distinguish rhetorical contrast from real technical, factual, or logical distinctions.

## Counting

Do not introduce counts merely to create structure.

Be suspicious of phrases such as:

- three things matter
- there are two reasons
- one problem, two consequences
- from X to Y

Use counts when the count itself improves comprehension or describes a real procedure.

Do not force uneven material into equal categories.

## Repetition

Track meaning across the whole piece.

Remove:

- claims repeated in different words
- headings repeated in the first sentence
- conclusions repeated across sections
- positioning repeated in every section
- qualifications repeated after they are established
- thematic words used more often than the subject requires

Changing a synonym does not solve semantic repetition.

## Rhetoric

Keep emphasis proportional to the evidence.

Avoid automatically describing something as:

- important
- historic
- transformative
- essential
- unprecedented
- defining
- fundamental

Explain the consequence when the consequence matters.

Avoid sentences written mainly to sound quotable.

Avoid compressed declarations that behave like maxims or manifesto lines.

Do not manufacture stakes.

## Attribution

Attribute claims to identifiable sources when attribution matters.

Avoid unsupported constructions such as:

- experts say
- research shows
- critics argue
- observers note
- reports suggest
- many believe

Use the actual source when available.

Do not invent consensus.

## Absolutes

Use absolute language only when the source supports it.

Inspect words such as:

- always
- never
- every
- none
- everyone
- entirely
- completely
- impossible
- guaranteed
- universally

Prefer accurate scope.

Do not create long qualification loops. Choose the appropriate scope once and state it clearly.

## Openings

Begin with information relevant to the reader.

Avoid broad scene-setting that could introduce almost any article.

Avoid generic openings such as:

- In today's rapidly evolving...
- In a world where...
- As technology continues to...
- The landscape of X is changing...
- When it comes to X...

Do not restate the title as the opening sentence.

## Transitions

Use transitions when the relationship between ideas needs clarification.

Do not mechanically announce movement with phrases such as:

- moreover
- furthermore
- importantly
- notably
- it is worth noting
- that said
- with that in mind
- in other words
- ultimately

A new paragraph can often begin directly with the next piece of information.

## Endings

End when the useful information is complete.

Do not automatically:

- summarize the whole piece
- restate the thesis
- widen the stakes
- add a generic future-looking sentence
- produce a slogan
- call for reflection
- repeat the heading
- finish with rhetorical flourish

A practical detail, consequence, next step, or final fact can be a natural ending.

## Vocabulary

Prefer familiar words when they express the idea accurately.

Do not avoid simple verbs such as:

- is
- has
- does
- uses
- makes
- shows
- says
- helps

Do not replace ordinary language with inflated alternatives merely for variety.

Watch for clusters of model-favored vocabulary.

One occurrence may be appropriate.

Repeated use within a short span is a stronger reason to revise.

Do not rotate synonyms mechanically.

Repeat terminology when precision requires consistency.

## Rhythm

Vary sentence length according to meaning.

Do not engineer a fixed cadence.

Avoid repeated sequences such as:

- short
- medium
- long
- punchline

Avoid chains of similarly shaped sentences.

Avoid repeated fragments used only for emphasis.

Inspect paragraph endings closely. Repeatedly polished endings often reveal formulaic construction.

## Formatting

Use formatting for navigation and comprehension.

Keep emphasis restrained.

Unless the requested genre calls for something else:

- avoid emoji
- avoid decorative bold
- avoid bolding routine phrases
- avoid excessive headings
- avoid unnecessary bullet lists
- avoid repeated label-plus-colon formatting
- avoid em dashes when ordinary punctuation works naturally

Use lists for genuinely list-shaped information.

Use prose for connected reasoning.

## Genre handling

When genre matters, read `references/genres.md`.

Pay attention to differences such as:

- product copy should stay concrete
- documentation should explain mechanisms and procedures
- email should reach the point quickly
- analysis should connect claims to evidence
- social writing may allow more compression
- executive writing should prioritize decisions and implications

When the user provides human-written samples, treat them as the strongest style evidence after factual accuracy and explicit user instructions.

Match recurring habits such as:

- sentence density
- paragraph length
- directness
- vocabulary level
- contractions
- amount of explanation
- heading style
- punctuation habits

Do not copy distinctive phrases unless requested.

## Writing workflow

### 1. Establish the brief

Identify:

- requested output
- audience
- genre
- purpose
- intended tone
- supplied facts
- required terminology
- source constraints
- reference samples

Do not invent missing brief details when a neutral choice works.

### 2. Load the pattern system

Read `references/patterns.md`.

Use its detection tests and exceptions during drafting or review.

### 3. Draft for meaning

Build around:

- facts
- mechanisms
- reasoning
- actions
- consequences
- useful examples
- relevant constraints

Apply the pattern rules during generation.

Do not intentionally write formulaic prose for cleanup later.

### 4. Check progression

Inspect each paragraph.

Cut or rewrite sentences that merely repeat:

- the preceding sentence
- the heading
- an earlier section
- the central positioning statement
- an already established qualification

### 5. Check structure

Inspect the whole piece for repeated:

- sentence shapes
- paragraph shapes
- section templates
- contrast formulas
- list sizes
- heading structures
- opening formulas
- closing formulas

Change the underlying organization when repetition becomes visible.

### 6. Check rhetoric

Remove unnecessary:

- slogans
- maxims
- dramatic fragments
- mirrored comparisons
- manufactured contrasts
- perfect triads
- artificial counts
- grand significance claims
- conceptual labels
- polished punchlines

Keep rhetoric that performs a real communicative function.

### 7. Check support

Make sure revision has not introduced unsupported details.

Match confidence to the available evidence.

### 8. Escalate when needed

If a classification or rewrite remains unclear, read `references/examples.md`.

If the output is substantial or publication-ready, read `references/audit.md`.

## Rewrite behavior

When rewriting supplied text:

- preserve supported meaning
- preserve relevant facts
- preserve required terminology
- preserve important nuance
- preserve the intended voice where possible
- maintain appropriate formality
- remove unnecessary repetition
- simplify inflated language
- improve progression
- vary structure according to content

Keep sentences that already work.

Do not rewrite every sentence merely because another wording exists.

Do not lengthen text simply to create variation.

Deletion is often the best revision.

## Original writing behavior

Apply these principles during generation.

Build from the user's substance.

Use natural structure from the beginning.

Avoid creating predictable rhetorical scaffolding that will need cleanup later.

For longer work, inspect the document after drafting for patterns visible only at document level.

## Hard limits

Unless the user explicitly requests otherwise:

- unsupported factual specifics: 0
- invented quotations: 0
- invented real people: 0
- fabricated first-person experiences: 0
- unsupported absolutes: 0
- rhetorical questions immediately answered by the next sentence: 0
- sentences whose only purpose is to repeat an earlier claim: 0
- emoji in ordinary professional prose: 0

## Final response

Return the requested writing directly.

Do not mention this Skill unless the user asks about it.

Do not announce that the text was humanized or de-slopped.

Do not provide AI-detection scores, probabilities, or guarantees.

Do not expose the internal audit unless requested.

Do not provide multiple versions unless the user asks for alternatives.

Prefer the clearest supported sentence over the most impressive-sounding sentence.
