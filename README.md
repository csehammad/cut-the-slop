# Cut the Slop

**Cut the Slop** is a portable Agent Skill for writing and rewriting prose that avoids recurring LLM writing habits while preserving meaning, evidence, terminology, and voice.

It works with **ChatGPT, Claude Code, Cursor**, and other agents that support `SKILL.md`-based skills.

The Skill can clean up an existing draft or guide a new one from the start.

## Install

### ChatGPT

Download **`skill.zip`** from the latest GitHub Release.

In ChatGPT:

1. Open **Plugins** from the sidebar.
2. Open **Skills**.
3. Select **Create**.
4. Choose **Upload from your computer**.
5. Upload `skill.zip`.

ChatGPT scans uploaded Skills before making them available.

Once installed, use it through normal requests:

```text
Rewrite this so it sounds natural without changing the meaning.
```

```text
Remove the formulaic AI-writing patterns from this section.
```

```text
Keep my technical meaning and voice, but clean up the generated-sounding structure.
```

Skill availability and upload permissions depend on the user's ChatGPT account and workspace settings.

### Claude Code

Install globally:

```bash
git clone https://github.com/YOUR_USERNAME/cut-the-slop.git ~/.claude/skills/cut-the-slop
```

Or install it for one project:

```bash
git clone https://github.com/YOUR_USERNAME/cut-the-slop.git .claude/skills/cut-the-slop
```

Claude Code can load the Skill when it is relevant, or you can invoke it directly:

```text
/cut-the-slop
```

For example:

```text
/cut-the-slop rewrite this section without changing the technical meaning
```

### Cursor

Install globally:

```bash
git clone https://github.com/YOUR_USERNAME/cut-the-slop.git ~/.cursor/skills/cut-the-slop
```

Or install it for one project:

```bash
git clone https://github.com/YOUR_USERNAME/cut-the-slop.git .cursor/skills/cut-the-slop
```

Cursor can select the Skill automatically when the request matches its description.

You can also invoke it directly:

```text
/cut-the-slop
```

or attach it as context with:

```text
@cut-the-slop
```

### Use one install with Claude Code and Cursor

Cursor can also discover compatible Skills stored in Claude Code's skill directories.

If you use both tools, installing Cut the Slop here:

```bash
~/.claude/skills/cut-the-slop
```

can make the same Skill available to both Claude Code and Cursor.

## What it does

Cut the Slop reviews writing at the sentence, paragraph, section, and document level.

The current taxonomy contains **45 pattern rules** covering recurring structural and stylistic problems found in generated prose.

Examples include:

- manufactured contrasts (`not X, but Y`, `X isn't the problem. Y is.`)
- negative parallelism (`not faster, not cheaper, just better`)
- mirrored syntax (`X changes the model. Y changes the system.`)
- tidy binaries (`either control the model or accept the risk`)
- reflexive triads and tetrads (`fast, flexible, and reliable`)
- artificial counting (`there are three reasons` when the material was not naturally divided into three)
- fake structural precision (`the problem has exactly four layers`)
- false ranges (`from small startups to global enterprises`)
- over-clean taxonomies that force messy material into neat categories
- semantic restatement (`X happens. This means X is happening.`)
- headings immediately repeated by the first sentence (`## Context changes` followed by `Context changes during a run.`)
- redundant qualification loops (`this does not necessarily mean...` repeated several ways)
- thematic keyword saturation (repeating `boundary`, `trust`, or `control` long after the term has done its job)
- synonym rotation (`control`, `safeguard`, `guardrail`, `enforcement mechanism` for the same thing)
- repeated sentence cadence (`The model adapts. The system responds. The loop continues.`)
- repeated paragraph architecture (every paragraph following `claim → explanation → takeaway`)
- repeated section architecture (each section having the same opening, length, and closing shape)
- brand-message overfitting (restating the same product promise throughout the page)
- significance inflation (`this represents a fundamental shift`)
- empty importance markers (`this matters`, `why this matters`, `what matters here is`)
- add-on analysis (`this highlights the broader importance of...`)
- reader-value instruction (`what is crucial to understand is...`)
- totalizing statements (`everything depends on this`)
- pseudo-profound compression (`persistence is power until persistence becomes the problem`)
- micro-manifesto language (`the future belongs to systems that...`)
- inflated stakes (`this could redefine the future of AI`)
- abstract noun stacks (`alignment, optimization, execution, governance`)
- unnecessary concept labels (`contextual persistence drift`)
- unnamed authorities (`experts agree`, `researchers have long warned`)
- vague evidence claims (`research shows`, `studies suggest`) without an identified basis
- invented first-person experience (`we've seen this repeatedly in production`) when the source never established it
- manufactured personal reflection (`this stayed with me`, `I kept coming back to this`, `what struck me was`) when the writer never supplied that reaction
- unsupported absolutes (`agents will always find another route`)
- fake numerical precision (`even a 1% failure rate becomes catastrophic`) when no number was supplied
- generic openings (`in today's rapidly evolving AI landscape...`)
- mechanical signposting (`with that in mind`, `turning now to`, `this brings us to`)
- rhetorical questions immediately answered by the writer (`Why does this happen? The answer is context.`)
- reflective framing (`it is worth taking a moment to consider...`)
- generic conclusions (`ultimately, understanding this is essential`)
- quotable or mic-drop endings (`that is the real risk`, `and that changes everything`)
- chat residue in finished prose (`sure`, `absolutely`, `here's a polished version`)
- model-favored vocabulary clusters (`crucial`, `nuanced`, `robust`, `landscape`, `underscore`)
- inflated substitutes for simple verbs (`utilize` instead of `use`, `serves to demonstrate` instead of `shows`)
- em-dash dependence (`the state changed—and that changed everything`)
- unnecessary formatting (constant bolding, decorative headings, excessive lists)
- fake casualness (`Yep, totally`, `super quick`, `here's the thing`)
- pattern substitution (removing a triad and replacing it with `not X but Y`, or removing formal filler and replacing it with forced slang)

These are diagnostic patterns, not banned constructions.

A real three-item list is fine when there are actually three items. Technical writing may need repeated terminology because changing the term would reduce precision. A genuine technical distinction may require contrast.

The Skill asks whether the construction is helping the reader understand the material or merely giving ordinary prose a polished shape.

## The main idea

Many writing prompts focus on vocabulary.

They ban words such as `delve`, `crucial`, or `landscape`, remove em dashes, and tell the model to use simpler language.

Those edits can help, but much of the generated feel comes from structure.

Consider:

> The tools did not change. The task may not have changed either. The state the model was generating from did.

Replacing individual words leaves the three-part construction intact.

A better edit changes how the information is organized:

> The model was generating from a different state while using the same tools, possibly on the same task.

Cut the Slop looks for the structure that produced the problem.

## Pattern substitution

A rewrite can remove one obvious pattern and still fail.

For example:

> The tools did not change. The task may not have changed either. The state did.

A superficial rewrite might become:

> It was not the tools or the task that changed, but the state.

The triad disappeared, but a manufactured `not X but Y` contrast replaced it.

Cut the Slop checks the rewrite again after editing so one formulaic construction is not simply exchanged for another.

## Information should move

A common generated-writing problem is repetition disguised as explanation.

For example:

> The model operates from the current context. This means its behavior depends on the context it currently has.

The second sentence adds almost nothing.

A stronger continuation gives the reader something new:

> A failed tool call changes that context, so the next generation can differ even when the original task stays the same.

Each sentence should have a reason to exist.

Deletion is allowed. A sentence that contributes nothing does not need a replacement.

## Source fidelity

Cut the Slop should never improve prose by inventing material.

Rewrites preserve:

- factual claims
- uncertainty
- attribution
- technical distinctions
- numbers and dates
- scope
- established terminology
- the writer's intended point

It does not invent quotations, statistics, personal experiences, supporting evidence, examples, or authorities.

If the source says something *may* happen, the rewrite should not quietly change it to something that *will* happen.

If the source says something *contributed to* an outcome, the rewrite should not turn that into *caused*.

## Voice preservation

Cleaning up generated patterns should not flatten the writer.

When human writing samples are available, Cut the Slop can use them to infer habits such as:

- sentence length
- paragraph density
- directness
- contraction use
- punctuation
- vocabulary
- parenthetical use
- fragments
- humor
- formality

The Skill looks for recurring habits across the sample instead of copying distinctive phrases or exaggerating quirks.

An occasional fragment, repeated word, unusual sentence, or uneven paragraph may belong to the writer's voice.

The goal is not perfectly regular prose.

## Genre matters

Different writing needs different editing decisions.

Cut the Slop includes guidance for:

- email
- chat and direct messages
- product and landing-page copy
- documentation
- technical writing
- analysis
- articles and essays
- case studies
- social posts
- executive writing

Documentation may need exact terminology repeated several times.

A direct message may naturally contain fragments.

An article can spend more time developing an argument.

Product copy needs to avoid repeating the same positioning statement across every section.

The genre changes the judgment. The underlying fidelity rules stay in place.

## Long-form auditing

Some problems only become visible after reading several sections together.

For longer work, Cut the Slop can audit:

- distant repetition
- recurring examples
- keyword saturation
- repeated paragraph shapes
- repeated section shapes
- suspiciously even section lengths
- recurring transition phrases
- repeated contrast structures
- recurring three-part constructions
- identical section endings
- conclusions that restate earlier conclusions
- changes in certainty
- terminology drift
- claims that became stronger during rewriting

This prevents a document from having individually acceptable paragraphs that all feel as though they came from the same template.

## It is not an AI detector

Cut the Slop does not produce an **AI score**.

It does not claim that prose style can prove whether a human or a model wrote a passage.

Human writers use many of the patterns in this library. Models can also produce excellent prose without them.

The rules are editorial.

They help identify repetition, weak progression, manufactured rhetoric, unsupported claims, and structures that make writing less natural or less precise.

## Example

Before:

> None of that requires consciousness, sentience, or malice. It also does not make the behavior safe. If the generated action is effective and the harness has the authority to execute it, the result is real.

After:

> The resulting behavior can still be dangerous. If a generated action works and the harness has enough authority to carry it out, the effect is real whether or not the model is sentient or acting with anything like human intent.

The edit removes a conspicuous three-item construction and lets the actual safety claim carry the paragraph.

## Another example

Before:

> This matters. The final action is not the whole story. What is crucial to understand is that the surrounding context determines how the model behaves.

After:

> The final action may be difficult to explain without the context the model received before generating it.

The rewrite removes the importance markers and states the useful point directly.

## Full sample

The examples above are single paragraphs. `Samples/` applies the same kind of rewrite to a complete essay about technology in education.

`Samples/before-cuttheslop.md` is the generated draft.

`Samples/after-cuttheslop.md` keeps the subject and the concrete claims. The generic opening, inflated significance, manufactured contrasts, and restated conclusion are gone.

## Project structure

```text
cut-the-slop/
├── SKILL.md
├── README.md
├── LICENSE
├── agents/
│   └── openai.yaml
├── references/
│   ├── patterns.md
│   ├── genres.md
│   ├── examples.md
│   └── audit.md
└── Samples/
    ├── before-cuttheslop.md
    └── after-cuttheslop.md
```

### `SKILL.md`

The control plane.

It defines the workflow, source-fidelity rules, reference-loading order, rewrite behavior, and output requirements.

### `references/patterns.md`

The canonical pattern library.

It contains the stable `SL-###` rule IDs, detection guidance, decision tests, exceptions, and short examples.

The Skill consults this file on every writing task.

### `references/genres.md`

Contains genre-specific editorial guidance and voice-matching rules.

### `references/examples.md`

Contains harder before-and-after cases for situations where several patterns interact or the first rewrite still feels formulaic.

### `references/audit.md`

Contains the long-form audit used for substantial documents.

### `agents/openai.yaml`

Contains metadata used by OpenAI products.

The core portable Skill remains `SKILL.md` plus its supporting reference files, so Claude Code, Cursor, and other compatible agents do not need to interpret the OpenAI-specific metadata.

### `Samples/`

A full before-and-after essay.

`before-cuttheslop.md` is the generated draft. `after-cuttheslop.md` is the rewrite. These files are examples for readers. The Skill does not load them.

## How loading works

The Skill uses progressive loading.

`SKILL.md` stays relatively compact and acts as the control plane.

`references/patterns.md` contains the detailed pattern system and is required for writing tasks.

Other references are loaded when the task needs them:

```text
SKILL.md
    │
    ├── patterns.md   ← every invocation
    │
    ├── genres.md     ← genre or voice-sensitive writing
    │
    ├── examples.md   ← ambiguous or difficult rewrites
    │
    └── audit.md      ← substantial or multi-section documents
```

This keeps the Skill from putting its entire rule library into context when only part of it is needed.

## Pattern IDs

Rules have stable IDs so the same taxonomy can later be used by editors, linters, evaluations, and other tooling.

Examples:

```text
SL-001  Manufactured contrast
SL-005  Reflexive triad/tetrad
SL-010  Semantic restatement
SL-017  Section-level symmetry
SL-021  Reader-value instruction
SL-026  Abstract noun stack
SL-030  Invented first-person experience
SL-031  Unsupported absolute
SL-035  Rhetorical question + immediate answer
SL-036  Reflective framing
SL-038  Quotable/mic-drop ending
SL-042  Em-dash dependence
SL-045  Pattern substitution
```

## Example prompts

Rewrite existing prose:

```text
Rewrite this so it sounds natural without changing the meaning.
```

```text
Remove the formulaic AI-writing patterns from this section.
```

```text
Keep the technical content intact, but fix the generated-sounding structure.
```

Match a supplied voice:

```text
Edit this article in my voice. Use the attached samples as the style reference.
```

Audit a longer draft:

```text
Review this for repeated claims, fake contrasts, abstract filler, repeated section structure, and rhetorical endings.
```

Draft from source material:

```text
Write this section from my notes. Preserve the evidence and avoid formulaic AI prose from the start.
```

Ask for an explanation:

```text
Show me which Cut the Slop rules this paragraph is triggering and why.
```

By default, the Skill should return the finished writing rather than narrating its editing process.

## Design principles

### Preserve the claim

A cleaner sentence is worse if it changes the evidence.

### Fix the underlying structure

Changing a suspicious word rarely helps when the sentence architecture is the actual problem.

### Do not manufacture humanity

Random slang, fragments, typos, contractions, or awkward punctuation do not make writing more human.

### Keep legitimate repetition

Technical terms, commands, product names, legal language, and precision-sensitive wording should remain stable when consistency helps the reader.

### Let paragraph shapes vary naturally

Do not make every paragraph the same length or force each one through the same claim-explanation-takeaway structure.

### Stop when the writing works

Repeated editing can strip out useful voice and specificity.

## Distribution

The GitHub repository contains the editable source.

For **ChatGPT**, publish the packaged `skill.zip` as a GitHub Release asset.

For **Claude Code** and **Cursor**, users can clone or copy the repository directly into their supported Skill directory.

This keeps one canonical rule set across platforms.

## Planned tooling

The stable rule IDs also make it possible to build tooling around the same taxonomy.

Potential additions include:

- a local prose linter
- editor diagnostics tied to `SL-###` rules
- document-level repetition checks
- optional before-and-after explanations
- configurable rule severity
- personal voice profiles
- evaluation fixtures for comparing rewrites across models
- a desktop editor using the same rule library

The Agent Skill does not depend on those tools.

## Contributing

New patterns should describe a repeatable writing failure rather than a single disliked phrase.

A useful rule should document:

- what to detect
- the decision test
- legitimate exceptions
- what makes the construction weak
- what kind of edit usually fixes it
- examples showing the distinction

Do not create a new rule when an existing rule can be expanded cleanly.

Examples should preserve the original meaning and should not make the preferred rewrite look better by intentionally damaging the source version.

## License

Apache License 2.0.

See `LICENSE` for the complete license text.